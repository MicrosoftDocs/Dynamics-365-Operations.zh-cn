---
title: 为生成文档指定自定义存储位置
description: 本主题介绍如何扩展电子申报 (ER) 格式生成的单据的存储位置列表。
author: NickSelin
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 25719de3d86785442e00f7375de525b95bdb094d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753688"
---
# <a name="specify-custom-storage-locations-for-generated-documents"></a>为生成文档指定自定义存储位置

[!include[banner](../includes/banner.md)]

电子申报 (ER) 框架的应用程序编程接口 (API) 可用于扩展 ER 格式生成的单据的存储位置列表。 本主题说明如何通过将创建 ER 目标的任务委托给默认目标工厂，然后实现具有自己的目标逻辑的自定义类，来为生成的文档添加自定义存储位置。

## <a name="prerequisites"></a>先决条件

部署支持连续生成的拓扑。 有关详细信息，请参阅[部署支持连续生成和测试自动化的拓扑](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation)。 还必须可以访问以下角色之一的此拓扑：

- 电子申报开发人员
- 电子申报功能顾问
- 系统管理员

还必须可以访问此拓扑的开发环境。

本主题中的所有任务都可以在 **USMF** 公司完成。

## <a name="import-the-fixed-asset-roll-forward-er-format"></a>导入固定资产前滚 ER 格式

要生成您计划为其添加自定义存储位置的文档，请将 **固定资产前滚** ER 格式[导入](er-download-configurations-global-repo.md)到当前拓扑中。

![配置存储库页面](./media/er-custom-storage-generated-files-import-format.png)

## <a name="run-the-fixed-asset-roll-forward-report"></a>运行固定资产前滚报表

1. 转到 **固定资产** \> **查询和报表** \> **交易报表** \> **固定资产前滚**。
2. 在 **开始日期** 字段中输入 **1/1/2017**（2017 年 1 月 1 日）。
3. 在 **结束日期** 字段中输入 **1/31/2017**（2017 年 1 月 31 日）。
4. 在 **货币** 字段中，选择 **记帐币种**。
5. 在 **格式映射** 字段中，选择 **固定资产前滚**。
6. 选择 **确定**。

![固定资产前滚报表的“运行时”对话框](./media/er-custom-storage-generated-files-runtime-dialog.png)

在 Microsoft Excel 中，查看生成并可供下载的传出文档。 这种行为是未为其配置[目标](electronic-reporting-destinations.md)的 ER 格式且以交互模式运行的 ER 格式的[默认行为](electronic-reporting-destinations.md#default-behavior)。

## <a name="review-the-source-code"></a>查看源代码

查看 `AssetRollForwardService` 类的 `generateReportByGER()` 方法的代码。 请注意，`Run()` 方法用于调用 ER 框架和生成 **固定资产前滚** 报表。

```xpp
class AssetRollForwardService extends SysOperationServiceBase
{
    public const str ERFormatModelName = 'Fixed assets';
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'AssetRollForward';

    /// <summary>
    /// Generates report by general electronic reporting
    /// </summary>
    /// <param name = "_contract">The Asset Period Statement contract</param>
    public void generateReportByGER(AssetRollForwardContract _contract)
    {
        ERFormatMappingId   formatMappingId;
        AssetRollForwardDP  dataProvider;
        AssetRollForwardTmp assetRollForwardTmp;
        Query               query;

        query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
        dataProvider = AssetRollForwardDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

        if (assetRollForwardTmp)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                // Call ER to generate the report.
                ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName)
                    .withParameter(parameters)
                    .withFileDestination(_contract.getFileDestination())
                    .run();
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

## <a name="modify-the-source-code"></a>修改源代码

1. 在您的 Visual Studio 项目中，添加一个新类（本示例中为 `AssetRollForwardDestination`），并编写代码以实现生成的 **固定资产前滚** 报表的在定义目标。

    - `new()` 方法旨在获取原始 ER 目标对象和应用程序逻辑驱动的参数，该参数指定应在其中存储生成的报表的自定义位置。 在此示例中，自定义位置是运行应用程序对象服务器 (AOS) 服务的服务器的本地文件系统的文件夹的名称。
    - `saveFile()` 方法旨在将生成的文档保存到运行 AOS 服务的服务器的本地文件系统的文件夹中。

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;

    /// <summary>
    /// Destination class for <c>AssetRollForwardDestinationFactory</c> that stores a generated report.
    /// </summary>
    public class AssetRollForwardDestination implements ERIFileDestination
    {
        private ERIFileDestination originDestination;
        private str TargetFolder;

        /// <summary>
        /// Creates a stream for new file.
        /// </summary>
        /// <param name = "_fileName">Name of a new file.</param>
        /// <returns>Stream for new file.</returns>
        public System.IO.Stream newFileStream(System.String _fileName)
        {
            return originDestination.newFileStream(_fileName);
        }

        /// <summary>
        /// Saves file in destination.
        /// </summary>
        /// <param name = "_stream">A stream to save.</param>
        /// <param name = "_fileName">A file name.</param>
        /// <returns>Saved stream.</returns>
        public System.IO.Stream saveFile(System.IO.Stream _stream, System.String _fileName)
        {
            _stream.Seek(0, System.IO.SeekOrigin::Begin);
            using (var localStream = System.IO.File::OpenWrite(TargetFolder + _fileName))
            {
                _stream.CopyTo(localStream);
            }
            return _stream;
        }

        /// <summary>
        /// Constructs destination for fixed asset roll forward report.
        /// </summary>
        /// <param name = "_originDestination">The original destination.</param>
        /// <param name = "_TargetFoder">The folder to store a report that's being created.</param>
        /// <returns>The fixed asset roll forward destination.</returns>
        public static AssetRollForwardDestination construct(ERIFileDestination _originDestination, str _TargetFoder)
        {
            return new AssetRollForwardDestination(_originDestination, _TargetFoder);
        }

        protected void new(ERIFileDestination _originDestination, str _TargetFoder)
        {
            originDestination = _originDestination;
            TargetFolder = _TargetFoder;
        }
    }
    ```

2. 在您的 Visual Studio 项目中，添加一个新类（在此示例中为 `AssetRollForwardDestinationFactory`），并编写代码以设置将目标创建委托给默认目标工厂的自定义目标工厂，并将文件目标包装到您自己的目标中。

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    using Microsoft.Dynamics365.LocalizationFramework.Format.FileGeneration;

    /// <summary>
    /// Destination factory for using <c>AssetRollForwardDestinationFactory</c>.
    /// </summary>
    public class AssetRollForwardDestinationFactory implements ERIFileDestinationFactory, ERIFileDestinationFactoryPostProcessor
    {
        private ERIFileDestinationFactory originDestinationFactory;
        private str TargetFolder;

        /// <summary>
        /// Creates file destination for print management.
        /// </summary>
        /// <param name = "_fileDestination">A default file destination.</param>
        /// <param name = "_identification">An identification strategy.</param>
        /// <param name = "_rootContext">A root context.</param>
        /// <param name = "_root">A root element.</param>
        /// <returns>A file destination.</returns>
        public ERIDataDrivenFileDestination createPrintMgmtDestination(
            ERIFileDestination _fileDestination,
            ERIObjectIdentificationStrategy _identification,
            ERTextFormatDataContext _rootContext,
            ERTextFormatIFileComponent _root)
        {
            ERIDataDrivenFileDestination dataDrivenDestination = originDestinationFactory.createPrintMgmtDestination(
                _fileDestination,
                _identification,
                _rootContext,
                _root);

            IFileDestinationHost fileDestinationHost = dataDrivenDestination as IFileDestinationHost;
            if (fileDestinationHost)
            {
                fileDestinationHost.FileDestination = AssetRollForwardDestination::construct(
                    fileDestinationHost.get_FileDestination(),
                    TargetFolder);
            }

            return dataDrivenDestination;
        }

        /// <summary>
        /// Constructs the fixed asset roll forward destination factory.
        /// </summary>
        /// <param name = "_originDestinationFactory">The original destination.</param>
        /// <param name = "_TargetFolder">The string containing a folder name that corresponds to the report, that's being created.</param>
        /// <returns>The destination factory for the fixed asset roll forward report.</returns>
        public static AssetRollForwardDestinationFactory construct(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            AssetRollForwardDestinationFactory destinationFactory = new AssetRollForwardDestinationFactory(_originDestinationFactory, _TargetFolder);

            ERIFileDestinationFactoryPostProcessorsHost factoryPostProcessing = ERCast::asObject(destinationFactory.originDestinationFactory) as ERIFileDestinationFactoryPostProcessorsHost;

            if (factoryPostProcessing)
            {
                factoryPostProcessing.addDestinationPostProcessor(destinationFactory);
            }
            return destinationFactory;
        }

        public ERIFileDestination processDestinationAfterCreation(ERIFileDestination _sourceDestination)
        {
            return AssetRollForwardDestination::construct(_sourceDestination, TargetFolder);
        }

        protected void new(ERIFileDestinationFactory _originDestinationFactory, str _TargetFolder)
        {
            originDestinationFactory = _originDestinationFactory;
            TargetFolder = _TargetFolder;
        }
    }
    ```

3. 修改现有 `AssetRollForwardService` 类，并编写代码以为报表运行器设置自定义目标工厂。 请注意，在构建自定义目标工厂时，将传递指定目标文件夹的应用程序驱动参数。 这样，该目标文件夹用于存储生成的文件。

    > [!NOTE] 
    > 确保指定的文件夹（此示例中为 **C:\\0**）位于运行 AOS 服务的服务器的本地文件系统中。 否则，将在运行时引发 [DirectoryNotFoundException](https://docs.microsoft.com/dotnet/api/system.io.directorynotfoundexception?view=netcore-3.1) 异常。

    ```xpp
    using Microsoft.Dynamics365.LocalizationFramework;
    /// <summary>
    /// The electronic reporting service class for fixed asset roll forward report
    /// </summary>
    class AssetRollForwardService extends SysOperationServiceBase
    {
        public const str ERFormatModelName = 'Fixed assets';
        public const str ERModelDataSourceName = 'model';
        public const str DefaultExportedFileName = 'AssetRollForward';

        /// <summary>
        /// Generates report by general electronic reporting
        /// </summary>
        /// <param name = "_contract">The Asset Period Statement contract</param>
        public void generateReportByGER(AssetRollForwardContract _contract)
        {
            ERFormatMappingId   formatMappingId;
            AssetRollForwardDP  dataProvider;
            AssetRollForwardTmp assetRollForwardTmp;
            Query               query;

            query = new Query(SysOperationHelper::base64Decode(_contract.parmQuery()));
            dataProvider = AssetRollForwardDP::construct();
            formatMappingId = _contract.parmFormatMapping();
            assetRollForwardTmp = dataProvider.getAssetRollForwardTmp(_contract, query);

            if (assetRollForwardTmp)
            {
                try
                {
                    ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                        .add(new ERModelDefinitionDatabaseContext().addTemporaryTable(assetRollForwardTmp))
                        .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, 'MyParameters', _contract, true));

                    // Call ER to generate the report.
                    ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());

                    ERIFileDestinationFactoryHost factoryHost = ERCast::asObject(formatMappingRun) as ERIFileDestinationFactoryHost;
                    if (factoryHost)
                    {
                        ERIFileDestinationFactory fileDestinationFactory = factoryHost.getFileDestinationFactory();
                        factoryHost.setFileDestinationFactory(AssetRollForwardDestinationFactory::construct(fileDestinationFactory, @'c:\0\'));
                        formatMappingRun.run();
                    }
                }
                catch
                {
                    // An error occurred while exporting data.
                    error("@SYP4861341");
                }
            }
            else
            {
                // There is no data available.
                info("@SYS300117");
            }
        }
    }
    ```

4. 重新生成您的项目。

## <a name="re-run-the-fixed-asset-roll-forward-report"></a>重新运行固定资产前滚报表

1. 转到 **固定资产** \> **查询和报表** \> **交易报表** \> **固定资产前滚**。
2. 在 **开始日期** 字段中，输入 **1/1/2017**。
3. 在 **结束日期** 字段中，输入 **1/31/2017**。
4. 在 **货币** 字段中，选择 **记帐币种**。
5. 在 **格式映射** 字段中，选择 **固定资产前滚**。
6. 选择 **确定**。
7. 浏览本地 **C:\\0** 文件夹以查找生成的文件。

> [!NOTE]
> 因为在此示例中，`AssetRollForwardDestination`对象中不属于 `originDestination` 对象，所以运行时将忽略 ER 格式[目标](electronic-reporting-destinations.md)的配置。

## <a name="additional-resources"></a>其他资源

- [电子报告 (ER) 目标](electronic-reporting-destinations.md)
- [可扩展性主页](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]