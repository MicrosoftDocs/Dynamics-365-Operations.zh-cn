---
title: 配置从 SharePoint 的数据导入
description: 本主题介绍如何从 Microsoft SharePoint 导入数据。
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 20e4e03a347cb046b58c4aceec8c473cf2aba6f50f09497b7bab2bcddc947cf2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718567"
---
# <a name="configure-data-import-from-sharepoint"></a>配置从 SharePoint 的数据导入

[!include[banner](../includes/banner.md)]

若要使用电子申报 (ER) 框架从传入文件导入数据，必须配置用于为导入提供支持的 ER 格式，然后运行将该格式用作数据源且类型为 **截止目标** 的模型映射。 若要导入数据，您必须导航到要导入的文件。 用户可以手动选择传入文件。 在新的 ER 功能中，为了为从 Microsoft SharePoint 导入数据提供支持，可将此过程配置为无人值守。 您可以使用 ER 配置从 Microsoft SharePoint 文件夹中存储的文件导入数据。 本主题介绍如何完成从 SharePoint 的导入。 示例将供应商交易记录用作业务数据。

## <a name="prerequisites"></a>先决条件
要完成本主题中的示例，您必须具有以下访问权限：

- 访问以下其中一个角色：

    - 电子申报开发人员
    - 电子申报功能顾问
    - 系统管理员

- 已针对与此应用程序配合使用配置了 Microsoft SharePoint Server 实例的访问权限。
- 1099 付款的 ER 格式和模型配置。

### <a name="create-required-er-configurations"></a>创建所需的 ER 配置
播放 **ER 从 Microsoft Excel 文件导入数据** 任务指南，该任务指南属于 **7.5.4.3 获取/开发 IT 服务/解决方案产品 (10677)** 业务流程。 这些任务指南将引导您完成设计和使用 ER 配置以便以交互方式从 Microsoft Excel 文件导入供应商交易记录这一过程。 有关详细信息，请参阅[分析 Excel 格式的传入文档](parse-incoming-documents-excel.md)。 在您完成任务指南后，将具有以下设置。

#### <a name="er-configurations"></a>ER 配置

- ER 模型配置 **1099 付款模型**
- ER 格式配置 **用于从 Excel 导入供应商的交易记录的格式**

![用于从 SharePoint 导入数据的 ER 配置。](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>用于数据导入的传入文件示例

- Excel 文件 **1099import-data.xlsx**，其中包含应导入的供应商交易记录。

![用于从 SharePoint 导入的 Excel 示例文件。](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> 将选择用于导入供应商交易记录的格式作为默认模型映射。 因此，如果运行 **1099 付款模型** 的模型映射，并且该模型映射类型为 **截止目标**，则该模型映射运行此格式以从外部文件导入数据。 然后使用这些数据更新申请表。

## <a name="configure-access-to-sharepoint-for-file-storage"></a>配置对用于文件存储的 SharePoint 的访问
要在 SharePoint 位置存储电子报表文件，您必须配置对当前公司将使用的 SharePoint Server 实例的访问。 在此示例中，该公司为 USMF。 有关说明，请参阅[配置 SharePoint 存储](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage)。

1. 完成[配置 SharePoint 存储中的步骤](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage)。
2. 打开配置的 SharePoint 站点。
3. 创建以下可以存储传入的电子报告文件的文件夹：

     - 文件导入源（主）（以下屏幕截图中显示的示例）
     - 文件导入源（备用）

    ![文件导入源（主）。](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. （可选）创建以下可以在文件导入后存储文件的文件夹。 

    - 文件存档文件夹 - 此文件夹将是成功导入的文件。
    - 文件警告文件夹 - 此文件夹将是包含警告的导入文件。
    - 文件错误文件夹 - 此文件夹将是导入失败的文件。

4. 转至 **组织管理 > 单据管理 > 单据类型**。
5. 创建将用于访问您创建的 SharePoint 文件夹的以下文档类型。 有关说明，请参阅[配置文档类型](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types)。

|单据类型       | 组合              | 库位      | SharePoint 文件夹      |
|--------------------|--------------------|---------------|------------------------|
|SP 主             |文件                |SharePoint     |文件导入源（主）|
|SP 备用             |文件                |SharePoint     |文件导入源（备用）|
|SP 存档             |文件                |SharePoint     |文件存档文件夹|
|SP 警告             |文件                |SharePoint     |文件警告文件夹|
|SP 错误             |文件                |SharePoint     |文件错误文件夹|

![SharePoint 设置 – 新文档类型。](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>为 ER 格式配置 ER 源
1. 单击 **组织管理** \> **电子申报** \> **电子申报来源**。
2. 在 **电子申报来源** 页面中，使用配置的 ER 格式为数据导入配置源文件。
3. 定义一个文件名掩码，以便导入 .xlsx 扩展名的文件。 该文件名掩码可选，仅当定义了才使用。 只能为每个 ER 定义一种掩码。
4. 如果存在若干要导入的文件，并且导入顺序不重要，将 **导入文件前先进行排序** 更改为 **不排序**
5. 选择前面创建的所有 SharePoint 文件夹。

    [![ER 文件来源设置。](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - 将为每家申请公司分别定义 ER *来源*。 相反，ER *配置* 则由多家公司共用。
> - 如果删除 ER 格式的 ER 来源设置，也将通过确认删除所有连接的文件的状态（见下文）。

## <a name="review-the-files-states-for-the-er-format"></a>检查 ER 格式的文件状态
1. 在 **电子申报来源** 页中，选择 **来源的文件状态** 检查为当前 ER 格式配置的文件来源的内容。
2. 在 **文件** 部分，检查文件的列表。 此列表提供以下信息：

    - 根据文件名掩码（如果定义了文件名掩码）适用且已准备就绪可导入的源文件。 对于这些文件，**导入格式的源日志** 部分为空。
    - 以前导入的文件。 对于每个这样的文件，可在 **导入格式的源日志** 部分中检查该文件的导入历史记录。

也可以打开 **源的文件状态** 页，方法是选择 **组织管理** \> **电子申报** \> **源的文件状态**。 这样，该页就提供了有关在您当前登录的公司中已经为其配置了文件来源的所有 ER 格式的文件来源的信息。

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>从 SharePoint 文件夹中的 Excel 文件导入数据
1. 在 SharePoint 中，将包含供应商交易记录的 Microsoft Excel 文件 **1099import-data.xlsx** 上传到您前面创建的 **文件导入源（主）** SharePoint 文件夹。

    [![SharePoint 内容 – 要导入的 Microsoft Excel 文件。](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. 在 **源的文件状态** 页中，选择 **刷新** 以刷新页面。 此页面中将显示已上传到 SharePoint 的 Excel 文件，其状态为 **就绪**。 现在支持以下状态：

    - **就绪** – 为 SharePoint 文件夹中的每个新文件自动分配的状态。 此状态表示该文件已准备就绪，可以导入。
    - **正在导入** – 导入过程（如果正在同时运行多个过程）将锁定文件以防其他过程使用时 ER 报表自动分配的状态。
    - **已导入** – 文件导入成功完成时 ER 报表自动分配的状态。 此状态表示已从配置的文件来源（SharePoint 文件夹）删除了导入的文件。
    - **失败** – 文件导入完成，但出现错误或异常时，ER 报表自动分配的状态。
    - **保留** – 用户在此页面中手动分配的状态。 此状态表示暂时不导入该文件。 此状态可用于推迟导入某些文件。

    [![所选来源的已刷新 ER 文件状态页面。](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>从 SharePoint 文件导入数据
1. 打开 ER 配置树，选择 **1099 付款模型**，然后展开 ER 模型组件列表。
2. 选择模型映射名称以打开所选 ER 模型配置的模型映射列表。

    [![配置页面。](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. 选择 **运行** 以运行所选模型映射。 因为您为 ER 格式配置了文件源，所以，如果需要，可以更改 **文件源** 选项的设置。 如果保留此选项的设置，将从配置的源（本示例中为 SharePoint 文件夹）导入 .xslx 文件。

    在本示例中，仅导入一个文件。 但是，如果有多个文件，将按这些文件添加到 SharePoint 文件夹的顺序选择导入。 每次运行 ER 格式都将导入选择的一个文件。

    [![从 SharePoint 导入和运行 ER 模型映射。](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. 该模型映射可以以批处理模式的[无人值守](#limitations)方式运行。 在这种情况下，只要批处理运行该 ER 格式，都将从配置的文件源导入一个文件。

    将文件从 SharePoint 文件夹成功导入时，它将从该文件夹中删除并移到存储成功导入文件的文件夹或存储包含警告的导入文件的文件夹。 否则，它将移到失败文件的文件夹或如果未设置失败文件的文件夹将留在此文件夹中。 

5. 输入凭证 ID（如 **V-00001**），然后选择 **确定**。

    [![运行 ER 模型映射。](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. 在 **源的文件状态** 页中，选择 **刷新** 以刷新页面。

    [![来源的 ER 文件状态页面。](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. 在 **文件** 部分，检查文件的列表。 **导入格式的源日志** 部分提供 Excel 文件导入历史记录。 由于该文件已成功导入，所以在 SharePoint 文件夹中标记为 **已删除**。
8. 检查 **文件导入源（主）** SharePoint 文件夹。 已从该文件夹删除了成功导入的 Excel 文件。
9. 转至 **应付帐款** \> **定期任务** \> **1099 税** \> **用于 1099 的供应商结算**。
10. 在 **开始日期** 和 **结束日期** 字段中，输入相应值。 然后选择 **手动 1099 交易记录**。

    此页面中将显示在 SharePoint 上为凭证 **V-00001** 通过 Excel 文件导入的供应商交易记录。

    [![1099 供应商交易页面。](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>准备要导入的 Excel 文件
1. 打开以前使用过的 Excel 文件。 在第 3 行第 1 列，添加一个申请中没有的供应商代码。 为该行添加更多虚假的供应商信息。

    [![要从 SharePoint 导入的 Microsoft Excel 示例文件。](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. 将已更新且包含供应商交易记录的 Excel 文件上传到 **文件导入源（主）** SharePoint 文件夹。
3. 打开 ER 配置树，选择 **1099 付款模型**，然后展开 ER 模型组件列表。
4. 选择模型映射的名称以更新该模型映射，从而在数据导入过程中将不正确的供应商代码视为错误。
5. 选择 **设计器**。
6. 在 **验证** 选项卡上，必须更改为了评估应用程序中是否存在导入的供应商科目而配置的验证规则的验证后操作。 将 **验证后操作** 字段的值更改为 **停止执行**，保存更改，然后关闭页面。

    [![ER 模型映射设计器页面。](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. 保存更改，然后关闭 ER 模型映射设计器。
8. 选择 **运行** 以运行修改后的 ER 模型映射。
9. 输入凭证 ID（如 **V-00002**），然后选择 **确定**。

    信息日志中包含用于说明 SharePoint 文件夹中存在包含不正确的供应商科目的文件，因此不能导入的通知。

    [![已完成的“运行 ER 模型映射”。](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. 在 **源的文件状态** 页，选择 **刷新**，然后在 **文件** 部分中查看文件列表。

    [![所选来源的 ER 文件状态页面。](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   **导入格式的源日志** 部分指示导入过程失败，文件在“文件错误”SharePoint 文件夹中（**已删除** 复选框未选中）。 如果您通过添加适当的供应商代码在 SharePoint 上修复了此文件，并将其移到“文件导入源（主）”SharePoint 文件夹，您可以再次导入该文件。

11. 选择 **应付帐款** \> **定期任务** \> **1099税** \> **1099 的供应商结算**，在 **开始日期** 和 **结束日期** 字段中输入相应值，然后选择 **手动 1099 交易记录**。

    只有凭证 V-00001 的交易记录。 即使在 Excel 文件中发现了上次导入的交易记录的错误，也没有凭证 V-00002 的交易记录。

## <a name=""></a><a name="limitations">限制</a>

ER 框架不提供启动新批处理作业的功能，该作业将以无人参与模式执行模型映射以进行数据导入。 为此，您必须开发新的逻辑，以便可以从应用程序用户界面 (UI) 调用配置的 ER 模型映射，以从传入文件中导入数据。 因此，需要一些工程工作。 

要了解有关 ER API 的详细信息，请参阅[针对 Application update 7.3 的 ER API 更改](er-apis-app73.md)中的[用于运行格式映射以导入数据的代码](er-apis-app73.md#code-to-run-a-format-mapping-for-data-import)部分。

查看 `Application Suite` 模型的 `BankImport_RU` 类中的代码，以了解如何实现自定义逻辑。 此类扩展了 `RunBaseBatch` 类。 特别是，查看 `runER()` 方法，在此方法中，创建的 `ERIModelMappingDestinationRun` 对象充当 ER 模型映射的运行器。

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[针对 Application update 7.3 的 ER API 更改](er-apis-app73.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]