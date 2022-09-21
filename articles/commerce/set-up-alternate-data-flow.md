---
title: 设置备用建议数据流
description: 本文介绍如何使用备用数据流向建议服务提供数据来配置环境。
author: bebeale
ms.date: 09/08/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.openlocfilehash: b507b9bb57c68aca9424b53f8ccc009efea733bc
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460156"
---
# <a name="set-up-an-alternate-dataflow-for-recommendations"></a>设置备用建议数据流

[!include [banner](includes/banner.md)]

本文介绍如何使用备用数据流向建议服务提供数据来配置环境。

## <a name="comparison-of-out-of-the-box-dataflow-with-alternate-dataflow"></a>现成数据流与备用数据流的比较

下图描述了环境中的现成数据流。

![环境中的现成数据流](media/reco-out-of-the-box-dataflow-2.png)

下图描述了一个备用数据流，在此数据流中，实体存储同步批次作业被替换为备用数据流步骤。

![环境中的备用数据流](media/reco-alternate-dataflow-2.png)

## <a name="assumptions"></a>假设

- 本文假设您已经为您的环境启用了建议服务。 有关详细信息，请参阅[启用产品建议](enable-product-recommendations.md)。
- 当您使用 Microsoft Azure Data Lake storage 帐户处理文件和文件夹时：

    - 您可以使用 Azure Web 门户界面或 Azure 存储资源管理器应用程序。
    - 处理文件和文件夹的起点在 **dynamics365-financeandoperations** 容器中，该容器位于命名与您的环境 URL 一致的文件夹下。
    - 如果您的沙盒环境名称为 **MyUAT**，环境基 URL 将为 `myuat.sandbox.operations.dynamics.com`。
    - 如果有多个环境连接到同一个存储帐户，每个环境都有自己的根文件夹。

## <a name="prerequisites"></a>先决条件

您必须先满足以下先决条件，然后才能实施备用数据流方法。

### <a name="set-up-microsoft-power-platform"></a>设置 Microsoft Power Platform

要设置 Microsoft Power Platform，请按照[启用 Microsoft Power Platform 集成](../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md)中的说明操作。

### <a name="install-the-export-to-data-lake-add-in"></a>安装“导出到 Data Lake”加载项

要安装“导出到 Data Lake”加载项，请按照[安装“导出到 Azure Data Lake”加载项](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md)中的说明操作。

> [!NOTE]
> 记下配置值，您在接下来的一些步骤中将需要它们。

### <a name="configure-tables-to-export-in-dynamics-365"></a>在 Dynamics 365 中配置要导出的表

从 Dynamics 365 到 Azure Data Lake Storage 的表同步在 **导出到 Data Lake** 页面进行管理。 由于该页面当前没有菜单项，因此只有具有 **系统管理员** 安全角色的用户可以打开它。

要在 Dynamics 365 中配置要导出的表，请按照以下步骤操作。

1. 要打开 **导出到 Data Lake** 页面，将字符串 `?mi=DataFeedsDefinitionWorkspace` 添加到环境的基 URL，如以下示例所示：

    `https://<environment-URL>/?mi=DataFeedsDefinitionWorkspace`

1. 在 **导出到 Data Lake** 页面，复制本文 [RetailSales 多维数据集表列表](#list-of-retailsales-cube-tables)一节中列出的表。
1. 在 **系统名称** 列中，展开筛选器选项列表。
1. 对于筛选器类型，选择 **之一**。 然后将光标放在文本框中，粘贴您从 **导出到 Data Lake** 页面复制的表列表。
1. 在筛选器选项列表的底部，选择 **应用**。
1. 选择网格中的所有行，然后选择 **激活**。

> [!NOTE]
> 在继续下一步之前，必须将所有行更新为 **正在运行** 状态。 根据需要对所有错误进行故障排除和解决。

### <a name="create-a-synapse-workspace"></a>创建 Synapse 工作区

如果您还没有 Synapse 工作区，请按照[快速入门：创建 Synapse 工作区](/azure/synapse-analytics/quickstart-create-workspace)中的说明创建 Synapse 工作区。

为了保持 Azure 资源有序，我们建议将 Data Lake Storage 帐户和 Synapse 工作区一起放在 Azure 中的资源组中。 您可以重复使用在安装“导出到 Data Lake”加载项时创建的存储帐户。

## <a name="create-a-database-in-synapse-for-recommendation-data-processing"></a>在 Synapse 中创建数据库进行建议数据处理

使用 Common Data Model 实用程序控制台应用程序 (CDMUtil_ConsoleApp) 在 Synapse 工作区中创建一个数据库，并从 Data Lake Storage 中的 Common Data Model 表填充它。 我们建议您在开发环境中将 Common Data Model 实用程序与您的数据库一起使用，以防有任何扩展。

> [!NOTE]
> 以下步骤假定没有将扩展数据添加到 RetailSales 多维数据集。

要在 Synapse 中创建数据库，请执行以下步骤。

1. 转到 [Dynamics-365-FastTrack-Implementation-Assets GitHub](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Analytics/CDMUtilSolution#2-cdmutil-console-app)，然后按照步骤下载 **CDMUtilConsoleApp.zip** 文件。
1. 将 zip 文件提取到本地文件夹。
1. 在文本编辑器中打开 **CDMUtil_ConsoleApp.dll.config** 文件，更新以下值：

    1. 设置 **租户 ID** 值（Azure 租户 ID）。
    1. 设置 **访问密钥** 值（Data Lake Storage 帐户的访问密钥）。

        1. 在 Azure 门户中，打开您的存储帐户。
        1. 在页面左侧的菜单中，选择 **访问密钥**。
        1. 在页面顶部，选择 **显示密钥**。
        1. 选择两个键字段之一的复制按钮，然后将值粘贴到配置文件中的双引号之间。

    1. 将 **ManifestURL** 值设置为 Azure Data Lake Storage 中 **Tables.manifest.cdm.json** 文件的 URL。 要获取 URL，浏览到 Azure 门户中的文件，选择视图右侧的省略号 (**...**)，然后选择 **属性**。 URL 是显示在 **概览** 选项卡上的第一个属性。
    1. 将 **TargetDbConnectionString** 值设置为 Synapse 工作区的内置无服务器 SQL 池的连接字符串。

        1. 在 Synapse 工作区中，选择 **管理** 选项卡。
        1. 在子菜单上，选择 **SQL 池**。
        1. 选择名称 **内置** 查看池的属性。
        1. 在属性对话框中，选择要使用的 ADO.NET 连接类型。 然后复制连接字符串值，将其粘贴在配置文件中的双引号之间。

        > [!NOTE]
        > 您必须具有创建数据库的权限。 为了便于使用，您可能希望使用内置的 **sqladminuser** 管理员帐户。

    1. 取消对 **ProcessEntities** 节点的注释，并将其值设置为 **true**（例如，`<add key="ProcessEntities" value ="true"/>`）。

1. 保存并关闭 **CDMUtil_ConsoleApp.dll.config** 文件。
1. 将 **EntityList.json** 文件复制到 **/Manifest** 目录。
1. 在命令提示符窗口中，运行 **cdmutil_consoleapp.exe**。

> [!NOTE]
> 查看输出时，应该有 35 个实体/视图，至少 75 个表，没有错误。

## <a name="prepare-the-data-lake-retailsales-aggregate-measurements-directory"></a>准备 Data Lake RetailSales 聚合度量目录

### <a name="back-up-your-current-retailsales-cube-data-from-data-lake-storage"></a>从 Data Lake Storage 备份您当前的 RetailSales 多维数据集数据

备份当前 RetailSales 多维数据集数据的最简单方法是以 Data Lake Storage **RetailSales-backup** 或类似名称重命名 **RetailSales** 目录。 此方法会保留现有数据，以防以后需要进行故障排除。

**/RetailSales** 多维数据集文件夹位于以下位置：

`<storage-account>/dynamics365-financeandoperations/<environment-url (for example, myuat.sandbox.operations.dynamics.com)>/AggregateMeasurements/RetailSales`

### <a name="create-a-new-retailsales-folder-and-upload-the-model-file"></a>创建一个新的 RetailSales 文件夹并上载模型文件

要创建新的 **RetailSales** 目录并将 **model.json** 文件上载到 Data Lake Storage，请执行以下步骤。

1. 在与前一个目录相同的级别创建一个新的空目录，将其命名为 **RetailSales**。
1. 将 **model.json** 文件上载到新目录。

## <a name="create-a-pipeline-to-copy-the-retailsales-cube-data"></a>创建管道复制 RetailSales 多维数据集数据

管道将读取 RetailSales 多维数据集视图并将数据导出到 Data Lake Storage 中的 .csv 文件。

要创建管道来复制 RetailSales 多维数据集数据，请按照下列步骤操作。

1. 在 Synapse 工作区中，选择 **集成** 选项卡。
1. 选择加号 (**+**)，然后选择 **从管道模板导入**。
1. 下载然后选择 [ExportRetailSalesCubeViews.zip 文件](https://aka.ms/reco-alternate-dataflow-files)。
1. 选择您的 SQL 数据库链接服务。
1. 选择您的存储帐户链接服务。
1. 打开 **复制数据** 工具，将 **Folder path** 属性更改为 **\<environment_name\>/...**。

### <a name="test-execution-of-the-pipeline"></a>测试管道的执行

我们建议您只使用一个视图来测试管道。 **RetailSales_RetailMediaTemplateView** 视图效果很好，因为它通常包含少于 10 行。

## <a name="schedule-the-pipeline-to-run-on-a-recurring-schedule"></a>计划管道定期运行

每次管道运行时，都会发生 Azure 消耗。 我们建议您以 48 小时或更长的时间间隔计划执行。 如果您必须立即同步数据，始终可以手动运行管道。 
 
## <a name="table-list-for-synchronization-from-dynamics-365-to-data-lake-storage"></a>从 Dynamics 365 到 Data Lake Storage 的同步的表列表

以下表列表是整个 RetailSales 多维数据集所需的所有表的子集。 建议服务只使用了 RetailSales 多维数据集中的 15 个视图，所需表的列表相应经过筛选。

### <a name="list-of-retailsales-cube-tables"></a>RetailSales 多维数据集表列表

- BICalendarOffsets
- BIDateDimension
- BIDateDimensionValue
- 目录
- CatalogProduct
- CatalogProductCategory
- CustInvoiceJour
- CustInvoiceTrans
- CustTable
- DataArea
- DimensionAttributeValueCombination
- DimensionAttributeValueSet
- DirPartyTable
- EcoResCategory
- EcoResCategoryHierarchy
- EcoResCategoryHierarchyRole
- EcoResColor
- EcoResConfiguration
- EcoResProduct
- EcoResProductCategory
- EcoResProductTranslation
- EcoResSize
- EcoResStyle
- HcmWorker
- InventDim
- InventDimCombination
- InventItemGroup
- InventItemGroupItem
- InventItemSetupSupplyType
- InventTable
- InventTrans
- LogisticsAddressCountryRegion
- LogisticsAddressCountryRegionTranslation
- LogisticsLocation
- LogisticsPostalAddress
- OMHIERARCHYPURPOSE
- RetailAssortmentLookup
- RetailAssortmentLookupChannelGroup
- RetailChannelProfile
- RetailChannelProfileProperty
- RetailChannelTable
- RetailChannelTableExt
- RetailConnDatabaseProfile
- RetailCustInvoiceJourTable
- RetailCustTable
- RetailMediaTemplate
- RetailOfflineProfile
- RetailPeriodicDiscount
- RetailRecoListConfigurationParameters
- RetailSalesTaxOverrideGroup
- RetailSharedParameters
- RetailSpecialCategoryMember
- RetailTenderTypeCardTable
- RetailTenderTypeTable
- RetailTerminalTable
- RetailTmpProductMedia
- RetailTransactionDiscountTrans
- RetailTransactionPaymentTrans
- RetailTransactionPaymentTransExt
- RetailTransactionSalesTrans
- RetailTransactionSalesTransExt
- RetailTransactionTable
- SalesLine
- SalesTable
- SystemParameters
- RETAILCATALOGINTERNALORG
- RETAILGROUPMEMBERLINE
- RETAILINTERNALORGANIZATION
- RETAILSPECIALCATEGORYPRODUCT
- RETAILPRODUCTCATEGORY
- ECORESCONFIGURATION
- DIMENSIONATTRIBUTE
- DIMENSIONATTRIBUTEVALUESET
- DIMENSIONHIERARCHY
- DIMENSIONHIERARCHYINTEGRATION
- DIMENSIONHIERARCHYLEVEL
- DIMENSIONPARAMETER
- OMExplodedOrganizationSecurityGraph

### <a name="view-list-for-the-parameter-to-pass-to-the-synapse-pipeline"></a>查看要传递到 Synapse 管道的参数列表

以下逗号分隔的列表包含管道将对其执行“选择”操作的 RetailSales 多维数据集视图。 然后它将结果复制到 Data Lake Storage。

RetailSales_RetailAssortmentRulesView,RetailSales_RetailChannelNavigationHierarchiesView,RetailSales_RetailChannelNavigationHierarchyCatalogProductsView,RetailSales_RetailChannelNavigationHierarchyCategoryNodesView,RetailSales_RetailChannelNavigationHierarchyCategoryProductsView,RetailSales_RetailMediaBaseUrlChannelView,RetailSales_RetailMediaRelativeUrlProductView,RetailSales_RetailMediaTemplateView,RetailSales_RetailOptOutCustomersView,RetailSales_RetailProductCategory,RetailSales_RetailProductTransaction,RetailSales_RetailProductVariantDimensionsView,RetailSales_RetailRecoListConfigurationParametersView,RetailSales_RetailRecoListsSharedParametersView,RetailSales_RetailEcoResProductTranslation

> [!IMPORTANT]
> 管道参数必须是由单个逗号分隔的视图名称列表。 不能有空格或换行。

## <a name="environment-specific-fixes"></a>环境特定修复

### <a name="retailchannelview-fix"></a>RETAILCHANNELVIEW 修复

**RETAILCHANNELVIEW** 视图包含一个硬编码整数，表示“零售渠道”类型的组织。 类型的实际值可能因环境而异，或因租户而异。

```SQL
CREATE OR ALTER   VIEW [dbo].[RETAILCHANNELVIEW]
AS
SELECT T1.RECID AS RECID1,
       T1.STOREAREA AS STOREAREA,
       T1.OMOPERATINGUNITID AS OMOPERATINGUNITID,
       T1.DEFAULTCUSTACCOUNT AS DEFAULTCUSTOMER,
       T1.RETAILCHANNELID AS RETAILCHANNELID,
       T1.CHANNELTYPE AS CHANNELTYPE,
       T1.PARTITION AS PARTITION,
       T1.RECID AS RECID,
       T2.OMOPERATINGUNITNUMBER AS OMOPERATINGUNITNUMBER,
       T3.NAME AS NAME
FROM   dbo.RETAILCHANNELTABLE AS T1 CROSS JOIN dbo.DIRPARTYTABLE AS T2 CROSS JOIN dbo.DIRPARTYTABLE AS T3
WHERE  ((((T1.OMOPERATINGUNITID = T2.RECID)
          )
         AND ((T2.RECID = T3.RECID)
              ))
        AND T2.INSTANCERELATIONTYPE IN (8363));
```

要更新硬编码整数，请执行以下步骤。

1. 在 Dynamics 365 中，查找您的在线渠道的 **ChannelID** 值。
1. 在附加到 Synapse 数据库的 SQL Server Management Studio (SSMS) 实例中，运行以下查询。

    ```SQL
    select INSTANCERELATIONTYPE, NAME, NAMEALIAS, * from dbo.DIRPARTYTABLE where RECID IN (select OMOPERATINGUNITID from dbo.RETAILCHANNELTABLE where RETAILCHANNELID =     <channelID>)
    ```

1. 复制第一列中的值 (**INSTANCERELATIONTYPE**)，将其粘贴到视图定义中。

## <a name="troubleshooting"></a>疑难解答

### <a name="pipeline-task-fails"></a>管道任务失败

**CopyData** 任务应该有 15 个管道任务执行。 如果任何一个执行失败，您必须验证所有依赖 SQL 对象是否存在，以及查询是否运行。 访问所有依赖项的最简单方法是使用 SSMS 连接到数据库。 然后您可以选择并按住（或右键单击）一个视图，选择 **针对新窗口生成创建**。

错误消息可能包含以下文本：

- 错误：“源”端出现失败
- 处理外部文件时出错：“最大错误计数”。
- /RetailSales/RetailSales_xxxxxx

#### <a name="example-scenario"></a>示例场景

在此示例中，**RetailSales_RetailProductCategory** 任务失败，您收到“最大错误计数”错误。

要调试错误，请按照下列步骤操作。

1. 在文本编辑器中打开 **EntityList.json** 文件（例如，Visual Studio Code）。
1. 查找 **RetailSales_RetailProductCategory** 的视图定义。

    ```SQL
    CREATE  VIEW [dbo].[RetailSales_RetailProductCategory] AS SELECT 0 AS ROW_UNIQUEKEY ,CATEGORY AS CATEGORYID ,PRODUCT AS PRODUCTID ,PRODUCTNAME ,CATEGORYNAME     ,PARENTCATEGORY AS PARENTCATEGORYID ,PARTITION ,RECID FROM RetailProductCategoryView
    ```

1. 此视图仅依赖于另一个视图：**RetailProductCategoryView** _。 查找 _*RetailProductCategoryView** 的视图定义。

    ```SQL
    CREATE VIEW [DBO].[RETAILPRODUCTCATEGORYVIEW] AS SELECT T1.CATEGORY AS CATEGORY, T1.PRODUCT AS PRODUCT, T1.PARTITION AS PARTITION, T1.RECID AS RECID, T2.PRODUCTNAME AS PRODUCTNAME, T2.PARTITION AS PARTITION#2, T3.NAME AS CATEGORYNAME, T3.PARENTCATEGORY AS PARENTCATEGORY, T3.PARTITION AS PARTITION#3 FROM RETAILPRODUCTCATEGORY T1 CROSS JOIN ECORESPRODUCTTRANSLATIONS T2 CROSS JOIN RETAILCATEGORYEXPANDED T3 WHERE((( T1.PRODUCT = T2.PRODUCT) AND ( T1.PARTITION = T2.PARTITION)) AND (( T1.CATEGORY = T3.RECID) AND ( T1.PARTITION = T3.PARTITION)))
    ```

1. 此视图依赖于其他三个视图：**RETAILPRODUCTCATEGORY**、**ECORESPRODUCTTRANSLATIONS** 和 **RETAILCATEGORYEXPANDED**。 找到每个视图的定义，列出其依赖项。 继续查找，直到找到所有依赖视图。

    这里是按依赖项树顺序排列的整个列表。 必须验证十三个视图。

    - RetailSales_RetailProductCategory

        - RetailProductCategoryView

            - RETAILPRODUCTCATEGORY

                - ECORESPRODUCTCATEGORY
                - ECORESCATEGORYHIERARCHYROLE
                - RETAILSPECIALCATEGORYPRODUCT

                    - ECORESPRODUCT
                    - RETAILGROUPMEMBERLINE
                    - RETAILSPECIALCATEGORYMEMBER

            - ECORESPRODUCTTRANSLATIONS

                - ECORESPRODUCT
                - ECORESPRODUCTTRANSLATION
                - SYSTEMPARAMETERS

            - RETAILCATEGORYEXPANDED

                - ECORESCATEGORY
                - ECORESCATEGORYHIERARCHYROLE

1. 在 Excel 中，创建以下 13 个 **select count(\*) from \<view_name\>** 语句。 在 SSMS 中运行这些语句，并将结果发送到文本。 然后滚动浏览结果查看是否有任何视图失败。 最初的错误表明至少有一个视图会失败。

    ```SQL
    select count(*) from RetailProductCategoryView
    select count(*) from RETAILPRODUCTCATEGORY
    select count(*) from ECORESPRODUCTCATEGORY
    select count(*) from ECORESCATEGORYHIERARCHYROLE
    select count(*) from RETAILSPECIALCATEGORYPRODUCT
    select count(*) from ECORESPRODUCT
    select count(*) from RETAILGROUPMEMBERLINE
    select count(*) from RETAILSPECIALCATEGORYMEMBER
    select count(*) from ECORESPRODUCTTRANSLATIONS
    select count(*) from ECORESPRODUCTTRANSLATION
    select count(*) from SYSTEMPARAMETERS
    select count(*) from RETAILCATEGORYEXPANDED
    select count(*) from ECORESCATEGORY
    ```

1. 验证您正在查看的内容的一种方法是创建一个根依赖视图来在 SSMS 中生成视图定义。 然后验证是否存在名为 **r.filepath** 的 Azure Data Lake 文件列。 此列的存在表明您在检查的视图正在从 Data Lake Storage 读取数据。

## <a name="additional-resources"></a>其他资源

[产品建议概览](product-recommendations.md)

[在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage](enable-adls-environment.md)

[启用个性化建议](personalized-recommendations.md)

[启用“购买类似外观”建议](shop-similar-looks.md)

[选择退出个性化产品建议](personalization-gdpr.md)

[在 POS 中添加产品建议](product.md)

[向交易记录屏幕添加建议](add-recommendations-control-pos-screen.md)

[调整 AI-ML 建议结果](modify-product-recommendation-results.md)

[手动创建策划的建议](create-editorial-recommendation-lists.md)

[使用演示数据创建建议](product-recommendations-demo-data.md)

[产品建议常见问题](faq-recommendations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
