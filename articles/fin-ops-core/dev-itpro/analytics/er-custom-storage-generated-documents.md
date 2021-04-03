---
title: 为生成的单据指定自定义存储位置
description: 本主题介绍如何扩展电子申报 (ER) 格式生成的单据的存储位置列表。
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: b71ad5a9701922eb94b1d611e2d3f6a945ce6c06
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562230"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>为生成的单据指定自定义存储位置

[!include[banner](../includes/banner.md)]

电子申报 (ER) 框架的应用程序编程接口 (API) 可用于扩展 ER 格式生成的单据的存储位置列表。 本主题中包含有关必须完成才能添加自定义存储位置的主要任务的概述。

## <a name="prerequisites"></a>先决条件

必须部署支持连续生成的拓扑。 （有关详细信息，请参阅[部署支持连续生成和测试自动化的拓扑](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation)。）必须可以访问以下角色之一的此拓扑：

- 电子申报开发人员
- 电子申报功能顾问
- 系统管理员

还必须可以访问此拓扑的开发环境。

## <a name="create-or-import-an-er-format-configuration"></a>创建或导入 ER 格式配置

在当前拓扑中，[创建新的 ER 格式](tasks/er-format-configuration-2016-11.md)以生成计划添加的自定义存储位置所属单据。 也可以[在此拓扑中导入现有 ER 格式](general-electronic-reporting-manage-configuration-lifecycle.md)。

![“格式设计器”页面](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> 创建或导入的 ER 格式中必须包含至少一个下面的格式元素：
>
> - 文件
> - 文件夹
> - 合并器
> - 附件

## <a name="create-a-new-document-type"></a>创建新的单据类型

若要指定如何路由 ER 格式生成的单据，必须配置[电子申报 (ER) 目标](electronic-reporting-destinations.md)。 在配置为将生成的单据作为文件存储的每个 ER 目标中，必须指定单据管理框架的单据类型。 可使用不同单据类型路由不同 ER 格式生成的单据。

1. 为之前创建或导入的 ER 格式添加新的[单据类型](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management)。 在下图中，单据类型为 **FileX**。
2. 若要区分此单据类型和其他单据类型，请在其名称中包含特定关键词。 例如，在下图中，名称为 **(LOCAL) 文件夹**。
3. 在 **类** 字段中，指定 **附加文件**。
4. 在 **组** 字段中，指定 **文件**。

![“单据类型”页面](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> 单据类型特定于公司。 若要在多个公司中使用某个 ER 格式和配置的目标，必须在每个公司中配置一个单独的单据类型。

## <a name="review-source-code"></a>查看源代码

可查看 **ERDocuManagement** 类的 **insertFile()** 方法的代码。 请注意，如果将生成的文件附加到记录，将引发 **AttachingFile()** 事件。


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

如果处理以下 ER 目标，将引发 **AttachingFile()** 事件。

- **存档** – 如果使用此目标，将在 ERFormatMappingRunJobTable 表中为运行的 ER 格式创建一个新记录。 此记录的 **已存档** 字段设置为 **False**。 如果 ER 格式运行成功，将把生成的单据附加到此记录，并引发 **AttachingFile()** 事件。 此 ER 目标中选择的单据类型决定附加的文件的存储位置（Microsoft Azure 存储或 Microsoft SharePoint 文件夹）。
- **作业存档** – 如果使用此目标，将在 ERFormatMappingRunJobTable 表中为运行的 ER 窗体创建一个新记录。 此记录的 **已存档** 字段设置为 **True**。 如果 ER 格式运行成功，将把生成的单据附加到此记录，并引发 **AttachingFile()** 事件。 此 ER 参数中配置的单据类型决定附加的文件的存储位置（Azure 存储或 Microsoft SharePoint 文件夹）。

![“电子申报参数”页面](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>配置 ER 目标

1. 为创建或导入的 ER 格式的之前介绍的一个元素（文件、文件夹、合并器或附件）配置存档目标。 有关指南，请参阅 [ER 配置目标](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11)。
2. 请使用前面为配置的目标添加的单据类型。 （例如，在本主题中，单据类型为 **FileX**。）

![“目标设置”对话框](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>修改源代码

1. 可向 Microsoft Visual Studio 项目添加新类，并编写代码以订阅前面介绍的 **AttachingFile()** 事件。 （有关所用可扩展性模式的详细信息，请参阅[使用 EventHandlerResult 响应](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result)。）例如，编写用于执行以下操作的代码：

    1. 将生成的文件存储到运行应用程序对象服务器 (AOS) 服务的服务器的本地系统的文件夹中。
    2. 仅当在将文件附加到 ER 执行作业日志中的记录时使用新的单据类型（例如，名称中包含“(LOCAL)”关键字的 **FileX** 类型），才存储这些生成的文件。

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. 重新生成您的项目。

## <a name="run-the-er-format-that-you-created-or-imported"></a>运行创建或导入的 ER 格式

1. 执行创建或导入的 ER 格式。
2. 转到 **组织管理 \> 电子报表 \> 电子报表作业**。 找到为此执行作业创建且生成的文件附加到的记录。
3. 浏览本地 **C:\\0** 文件夹以查找同一个生成的文件。

## <a name="additional-resources"></a>其他资源

- [电子申报 (ER) 目标](electronic-reporting-destinations.md)
- [可扩展性主页](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]