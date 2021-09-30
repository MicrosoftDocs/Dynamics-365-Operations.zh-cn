---
title: 设计电子报告格式以对 Excel 中生成的文档进行分页
description: 本主题说明如何设计电子报告 (ER) 格式，以在 Microsoft Excel 中对生成的文档进行分页。
author: NickSelin
ms.date: 09/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-08-01
ms.dyn365.ops.version: Version 10.0.22
ms.openlocfilehash: ce29225c4bce24adc2abefc3d3d6f20774852af4
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488331"
---
# <a name="design-an-er-format-to-paginate-generated-documents-in-excel"></a>设计电子报告格式以对 Excel 中生成的文档进行分页

[!include [banner](../includes/banner.md)]

本主题说明系统管理员或电子报告功能顾问角色的用户如何配置[电子报告 (ER)](general-electronic-reporting.md) 格式以在 Microsoft Excel 中生成出站文档并管理文档分页。

在此示例中，您将修改 Microsoft 提供的电子报告格式，该格式用于在[生成](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md)内部统计声明时打印控制报表。 此报表可让您观察报告的内部统计交易。 您的修改将让您能够管理生成的控制报表的分页。

本主题中的过程可以在 **DEMF** 公司完成。 无需进行编码。 在开始之前，请下载并保存以下文件。

| 说明       | 文件名 |
|-------------------|-----------| 
| 报表模板 1 | [ERIntrastatReportDemo1.xlsx](https://download.microsoft.com/download/7/2/a/72ae292a-8bb2-4b9d-8397-9764218f6fa8/ERIntrastatReportDemo1%20.xlsx) |
| 报表模板 2 | [ERIntrastatReportDemo2.xlsx](https://download.microsoft.com/download/7/d/1/7d15858d-6260-4afa-9dda-d8b955e59b1a/ERIntrastatReportDemo2.xlsx) |

## <a name="configure-the-er-framework"></a>配置 ER 框架

按照[配置电子报告框架](er-quick-start2-customize-report.md#ConfigureFramework)中的步骤设置最低限度的电子报告参数集。 在开始使用电子报告框架设计标准电子报告格式的自定义版本之前，您必须完成此设置。

## <a name="import-the-standard-er-format-configuration"></a>导入标准电子报告格式配置

按照[导入标准电子报告格式配置](er-quick-start2-customize-report.md#ImportERSolution1)中的步骤将标准电子报告配置添加到您当前的 Dynamics 365 Finance 实例。 导入 **内部统计报表** 格式配置的 **1.9** 版本。 基础 **内部统计模型** 配置的基础版本 1 会自动从存储库导入。

## <a name="customize-the-standard-er-format"></a>自定义标准 ER 格式

### <a name="create-the-custom-er-format"></a>创建自定义电子报告格式

在此场景中，您是 Litware, Inc. 的代表，该公司当前被选为可用的电子报告配置提供商。 您必须使用 **内部统计报表** 配置作为基础来创建新的电子报告格式配置。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的左侧窗格的配置树中，展开 **内部统计模型**，选择 **内部统计报表**。 Litware, Inc. 将把此 ER 格式配置的版本 1.9 用作自定义版本的基础。
3. 选择 **创建配置**，以打开下拉对话框。 可使用此对话框创建自定义付款格式的新配置。
4. 在 **新建** 字段组中，选择 **从以下名称派生: 内部统计报表, Microsoft** 选项。
5. 在 **名称** 字段中，输入 **内部统计报表 Litware**。
6. 选择 **创建配置** 创建新格式。

将创建 **内部统计报表 Litware** 电子报告格式配置的版本 1.9.1。 此版本的 [状态](general-electronic-reporting.md#component-versioning)为 **草稿**，可以编辑。 自定义 ER 格式的当前内容与 Microsoft 提供的格式的内容匹配。

### <a name="make-the-custom-format-runnable"></a>让自定义格式可运行

已创建自定义格式的第一个版本，并且其状态为 **操作**，您可以针对测试用途运行该格式。 若要运行此报表，请使用引用自定义 ER 格式的付款方式处理供应商付款。 默认情况下，从应用程序调用 ER 格式时，仅 [考虑](general-electronic-reporting.md#component-versioning)状态为 **已完成** 或 **已共享** 的版本。 此行为有助于避免使用未完成设计的 ER 格式。 但是，对于测试运行，可以强制应用程序使用状态为 **草稿** 的 ER 格式版本。 因此，如果需要进行任何修改，可以调整当前格式版本。 有关详细信息，请参阅[适用性](electronic-reporting-destinations.md#applicability)。

要使用 ER 格式的草稿版本，必须显式标记 ER 格式。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
3. 在 **使用参数** 对话框中，将 **运行设置** 选项设置为 **是**，然后选择 **确定**。
4. 根据需要，选择 **编辑** 以使当前页面可供编辑。
5. 在左侧窗格的配置树中，选择 **内部统计报表 Litware**。
6. 将 **运行草稿** 选项设置为 **是**，然后选择 **保存**。

    !["配置"页面上的"运行草稿"选项。](./media/er-paginate-excel-reports-derived-format-configuration.png)

## <a name="set-up-foreign-trade-parameters-to-use-the-custom-er-format"></a>设置外贸参数使用自定义电子报告格式

按照以下步骤配置外贸参数，以便您可以使用自定义格式。

1. 转到 **税务** \> **>设置** \> **外贸** \> **外贸参数**。
2. 在 **外贸参数** 页面的 **电子报告** 快速选项卡上，在 **文件格式映射** 字段中，选择 **内部统计报表 Litware**。
3. 在 **报表格式映射** 字段中，选择 **内部统计报表 Litware**。
4. 选择 **保存**。

## <a name="configure-the-custom-format-to-use-the-downloaded-report-template"></a>配置自定义格式以使用下载的报表模板

### <a name="review-the-first-downloaded-excel-template"></a>查看第一个下载的 Excel 模板

1. 在 Excel 桌面应用程序中，打开您先前下载的 **ERIntrastatReportDemo1.xlsx** 模板文件。
2. 验证模板是否包含命名范围以在生成的文档中创建报表页眉、报表详细信息和报表页脚部分。

    ![桌面应用程序中 Excel 模板 1 的布局。](./media/er-paginate-excel-reports-template1.gif)

### <a name="replace-the-current-excel-template-in-the-custom-er-format"></a><a id="replace-template"></a>替换当前的自定义电子报告格式的 Excel 模板

必须将新 Excel 模板添加到自定义电子报告格式。

1. 转到 **组织管理** \> **电子申报** \> **配置**。
2. 在 **配置** 页的左侧窗格的配置树中，展开 **内部统计模型** \> **内部统计报表**，然后选择 **内部统计报表 Litware** 配置。
3. 选择 **设计器**。
4. 在 **格式设计器** 页的操作窗格上，选择 **显示详细信息**。
5. 确保已选择 **内部统计: Excel** 根格式组件，然后，在操作窗格上，在 **导入** 选项卡上的 **导入** 组中，选择 **从 Excel 更新**。
6. 在 **从 Excel 更新** 对话框中，选择 **更新模板**。
7. 在 **打开** 对话框中，浏览到并选择您之前下载的 **ERIntrastatReportDemo1.xlsx** 文件，然后选择 **打开**。
8. 选择 **确定**。
9. 选择 **保存**。

![添加新 Excel 模板后电子报告格式设计器中的格式结构。](./media/er-paginate-excel-reports-format1.png)

## <a name="change-the-data-binding-to-show-the-item-description-on-a-generated-report"></a>更改数据绑定以在生成的报表上显示物料描述

1. 在 **格式设计器** 页中，选择 **映射** 选项卡。
2. 展开 **内部统计** \> **报表行**，选择 **商品代码** 组件。
3. 选择 **编辑公式**。
4. 将绑定公式从 `@.CommodityCode` 更改为 `CONCATENATE(@.CommodityCode, " ", @.ProductName)`。
5. 选择 **保存**。

![已配置绑定以在电子报告格式设计器中显示物料描述。](./media/er-paginate-excel-reports-format1a.png)

## <a name="generate-an-intrastat-declaration-control-report"></a><a id="generate-intrastat-control-report"></a>生成内部统计申报控制报表

首先，确保您在 **内部统计** 页面上有用于报告的内部统计交易。

![内部统计页面上的交易。](./media/er-paginate-excel-reports-transactions1.gif)

然后使用自定义电子报告格式生成内部统计申报的控制报表。

1. 转到 **税务** \> **申报** \> **外贸** \> **内部统计**。
2. 在 **内部统计** 页面上的操作窗格上，选择 **输出** \> **报表**。
3. 在 **内部统计报表** 对话框中，按照以下步骤运行报表：

    1. 设置 **开始日期** 和 **结束日期** 字段以将特定内部统计交易包括到报表中。
    2. 将 **生成文件** 选项设置为 **否**。
    3. 将 **生成报表** 选项设置为 **是**。
    4. 选择 **确定**。

4. 下载并保存生成的文档。
5. 在 Excel 中打开文档，进行查看。

    ![桌面应用程序中生成的 Excel 文档。](./media/er-paginate-excel-reports-document1.png)

## <a name="configure-the-custom-format-to-paginate-generated-documents"></a>配置自定义格式以对生成的文档进行分页

### <a name="review-the-second-downloaded-excel-template"></a>查看第二个下载的 Excel 模板

1. 在 Excel 中，打开您先前下载的 **ERIntrastatReportDemo2.xlsx** 模板文件。
2. 将此模板与 **ERIntrastatReportDemo1.xlsx** 模板进行比较，验证它是否包含几个新的 Excel 名称以在生成的文档中创建和填充特定于页面的部分：

    - **ReportPageHeader** 范围已添加以创建页眉。
    - **ReportPageFooter** 范围已添加以创建页脚。
    - **ReportPageFooter\_PageLines** 单元格已配置为显示每页的交易数。
    - **ReportPageFooter\_PageAmount** 单元格已配置为显示每页的交易总金额。
    - **ReportPageFooter\_PageWeight** 单元格已配置为显示每页的交易总重量。
    - **ReportPageFooter\_RunningCounterLines** 单元格已配置为显示从报表开头一直到当前页面的正在运行的交易计数器。
    - **ReportPageFooter\_RunningTotalAmount** 单元格已配置为显示从报表开头一直到当前页面正在运行的所有交易的金额累计总和。
    - **ReportPageFooter\_RunningTotalWeight** 单元格已配置为显示从报表开头一直到当前页面的交易的重量累计总和。

    ![桌面应用程序中 Excel 模板 2 的布局。](./media/er-paginate-excel-reports-template2a.gif)

    此模板的 **CommodityCode** 单元格已配置为包装单元格文本。 由于交易详细信息行被配置为自动适应行高度，所以当 **CommodityCode** 单元格中的文本换行时，整行的高度必须自动改变。

    ![配置为包装单元格文本的 CommerceCode 单元格。](./media/er-paginate-excel-reports-template2b.gif)

### <a name="repeat-the-replacement-of-the-current-excel-template-in-the-custom-er-format"></a>重复替换当前的自定义电子报告格式的 Excel 模板

1. 按照本主题的[替换当前的自定义电子报告格式的 Excel 模板](#replace-template)一节中的步骤操作。 但是，在步骤 7 中，选择 **ERIntrastatReportDemo2.xlsx** 文件。
2. 在 **格式设计器** 页上，展开 **内部统计**。
3. 命名已添加到可编辑电子报告格式的[范围](er-fillable-excel.md#range-component)格式组件，以将结构与应用的 Excel 模板的结构同步：

    1. 选择与 Excel 名称 **ReportPageHeader** 关联的 **范围** 组件。
    2. 在 **格式** 选项卡上，在 **名称** 字段中输入 **报表页面页眉**。
    3. 选择与 Excel 名称 **ReportPageFooter** 关联的 **范围** 组件。
    4. 在 **格式** 选项卡上，在 **名称** 字段中输入 **报表页面页脚**。

4. 选择 **保存**。

![替换 Excel 模板后电子报告格式设计器中的格式结构。](./media/er-paginate-excel-reports-format2.png)

### <a name="change-the-format-structure-to-implement-document-pagination"></a>更改格式结构以实现文档分页

1. 在 **格式设计器** 页上，在左窗格中的格式树中，选择 **内部统计** 根组件。
2. 选择 **添加**。
3. 在 **添加** 对话框中，在组件的 **Excel** 组中选择[页面](er-fillable-excel.md#page-component)组件。
4. 在 **组件属性** 对话框的 **名称** 字段中，输入 **报表页**。 然后选择 **确定**。
5. 要在每个生成的页面上使用 **报表页面页眉** 组件作为页眉，请执行以下步骤：

    1. 选择 **报表页面页眉** 组件，然后选择 **剪切**。
    2. 选择 **报表页** 组件，然后选择 **粘贴**。
    3. 展开 **报表页**。
    4. 要强制 **页面** 组件 [考虑](er-fillable-excel.md#page-component-structure)将此范围用于页眉，选择 **报表页面页眉**，然后，在 **格式** 选项卡上，在 **复制方向** 字段中，选择 **无复制**。

6. 要对生成的文档进行分页以考虑报表行上的内容，请执行以下步骤：

    1. 选择 **报表行** 组件，然后选择 **剪切**。
    2. 选择 **报表页** 组件，然后选择 **粘贴**。

7. 要在报表行之后但在最后一页页脚之前包含报表页脚，请执行以下步骤：

    1. 选择 **报表页脚** 组件，然后选择 **剪切**。
    2. 选择 **报表页** 组件，然后选择 **粘贴**。

8. 要在每个生成的页面上使用 **报表页面页脚** 组件作为页脚，请执行以下步骤：

    1. 选择 **报表页面页脚** 组件，然后选择 **剪切**。
    2. 选择 **报表页** 组件，然后选择 **粘贴**。
    3. 要强制 **页面** 组件 [考虑](er-fillable-excel.md#page-component-structure)将此范围用于页脚，选择 **报表页面页脚**，然后，在 **格式** 选项卡上，在 **复制方向** 字段中，选择 **无复制**。

![实现文档分页后电子报告格式设计器中的格式结构。](./media/er-paginate-excel-reports-format3.png)

### <a name="add-data-sources-to-calculate-page-footer-totals"></a>添加数据源以计算页脚总计

您必须配置新数据源以计算页面总计、正在运行的计数器和累计总和值，并将它们显示在页脚部分。 为此，我们建议您使用[数据集合](er-data-collection-data-sources.md)数据源。

1. 在 **格式设计器** 页中，选择 **映射** 选项卡。
2. 选择 **添加根**，然后按照以下步骤操作：

    1. 在 **添加数据源** 对话框中，在 **常规** 部分，选择 **空容器**。
    2. 在 **“空容器”数据源属性** 对话框中，在 **名称** 字段中输入 **总计**。
    3. 选择 **确定**。

3. 选择 **总计** 数据源，选择 **添加**，然后按照以下步骤操作：

    1. 在 **添加数据源** 对话框中，在 **常规** 部分，选择 **空容器**。
    2. 在 **“空容器”数据源属性** 对话框中，在 **名称** 字段中输入 **页面**。
    3. 选择 **确定**。

4. 再次选择 **添加**，然后按照以下步骤操作：

    1. 在 **添加数据源** 对话框中，在 **常规** 部分，选择 **空容器**。
    2. 在 **“空容器”数据源属性** 对话框中，在 **名称** 字段中输入 **累计**。
    3. 选择 **确定**。

5. 选择 **Total.Page** 数据源，选择 **添加**，然后按照以下步骤操作：

    1. 在 **添加数据源** 对话框中，在 **功能** 部分，选择 **数据收集**。
    2. 在 **“数据集合”数据源属性** 对话框中，在 **名称** 字段中输入 **金额**。
    3. 在 **物料类型** 字段中，选择 **实际**。
    4. 将 **收集所有值** 选项设置为 **是**。
    5. 选择 **确定**。

6. 再次选择 **添加**，然后按照以下步骤操作：

    1. 在 **添加数据源** 对话框中，在 **功能** 部分，选择 **数据收集**。
    2. 在 **“数据集合”数据源属性** 对话框中，在 **名称** 字段中输入 **重量**。
    3. 在 **物料类型** 字段中，选择 **实际**。
    4. 将 **收集所有值** 选项设置为 **是**。
    5. 选择 **确定**。

7. 选择 **Total.Running** 数据源，选择 **添加**，然后按照以下步骤操作：

    1. 在 **添加数据源** 对话框中，在 **功能** 部分，选择 **数据收集**。
    2. 在 **“数据集合”数据源属性** 对话框中，在 **名称** 字段中输入 **金额**。
    3. 在 **物料类型** 字段中，选择 **实际**。
    4. 将 **收集所有值** 字段设置为 **是**。
    5. 选择 **确定**。

8. 再次选择 **添加**，然后按照以下步骤操作：

    1. 在 **添加数据源** 对话框中，在 **功能** 部分，选择 **数据收集**。
    2. 在 **“数据集合”数据源属性** 对话框中，在 **名称** 字段中输入 **重量**。
    3. 在 **物料类型** 字段中，选择 **实际**。
    4. 将 **收集所有值** 字段设置为 **是**。
    5. 选择 **确定**。

9. 再次选择 **添加**，然后按照以下步骤操作：

    1. 在 **添加数据源** 对话框中，在 **功能** 部分，选择 **数据收集**。
    2. 在 **“数据集合”数据源属性** 对话框中，在 **名称** 字段中输入 **行**。
    3. 在 **物料类型** 字段中，选择 **整数**。
    4. 将 **收集所有值** 字段设置为 **是**。
    5. 选择 **确定**。

10. 选择 **保存**。

### <a name="add-data-sources-to-control-page-footer-visibility"></a>添加数据源以控制页脚可见性

如果您计划控制页脚可见性，且不打算将页脚包含在包含交易的最终页面上，配置一个新数据源来计算所需的运行计数器。

1. 在 **格式设计器** 页中，选择 **映射** 选项卡。
2. 选择 **Total.Running** 数据源，选择 **添加**。
3. 在 **添加数据源** 对话框中，在 **功能** 部分，选择 **数据收集**。
4. 在 **“数据集合”数据源属性** 对话框中，在 **名称** 字段中输入 **行 2**。
5. 在 **物料类型** 字段中，选择 **整数**。
6. 将 **收集所有值** 选项设置为 **是**。
7. 选择 **确定**。
8. 选择 **保存**。

![在电子报告格式设计器中添加的数据源。](./media/er-paginate-excel-reports-format4.png)

### <a name="configure-bindings-to-collect-total-values"></a>配置绑定以收集总计值

1. 在 **格式设计器** 页上，在格式树中，展开 **报表行** 组件，选择嵌套 **发票值** 组件。
2. 选择 **编辑公式**。
3. 将绑定公式从 `NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", "")` 更改为 `Total.Page.Amount.Collect(NUMBERVALUE(NUMBERFORMAT(@.InvoiceValue, "F"&TEXT(model.Parameters.IntrastatAmountDecimals)), ".", ""))`。

    > [!NOTE]
    > 除了将每个迭代交易的金额值放在 Excel 单元格中外，此绑定还会收集数据集合 **Total.Page.Amount** 数据源中的值。

4. 选择嵌套 **重量** 组件。
5. 选择 **编辑公式**。
6. 将绑定公式从 `@.'$RoundedWeight'` 更改为 `Total.Page.Weight.Collect(@.'$RoundedWeight')`。

    > [!NOTE]
    > 除了将每个迭代交易的重量值放在 Excel 单元格中外，此绑定还会收集 **Total.Page.Weight** 数据源中的值。

![已配置绑定以在电子报告格式设计器中收集总计值。](./media/er-paginate-excel-reports-format5.png)

### <a name="configure-bindings-to-fill-in-page-footer-totals"></a>配置绑定以填充页脚总计

1. 在 **格式设计器** 页上的格式树中，展开 **报表页面页脚** 组件，选择引用 Excel **ReportPageFooter\_PageAmount** 单元格的嵌套 **范围** 组件，然后按照以下步骤操作：

    1. 在右侧窗格中的数据源树中，选择 **Total.Page.Amount.Sum()** 项。
    2. 选择 **绑定**。
    3. 选择 **编辑公式**。
    4. 将公式更新为 `Total.Page.Amount.Sum(false)`。

    > [!NOTE]
    > 您必须将此函数的参数指定为 **False** 以保留当前页面的收集数据，因为需要这些数据来计算金额累计总和、每页总行数以及正在运行的行计数器。

2. 在格式树中，选择引用 Excel **ReportPageFooter\_PageWeight** 单元格的嵌套 **范围** 组件，然后执行以下步骤：

    1. 在右侧窗格中的数据源树中，选择 **Total.Page.Weight.Sum()** 项。
    2. 选择 **绑定**。
    3. 选择 **编辑公式**。
    4. 将公式更新为 `Total.Page.Weight.Sum(false)`。

### <a name="configure-bindings-to-fill-in-page-running-totals"></a>配置绑定以填充页面的累计总和

1. 在 **格式设计器** 页上的格式树中，展开 **报表页面页脚** 组件，选择引用 Excel **ReportPageFooter\_RunningTotalAmount** 单元格的嵌套 **范围** 组件，然后按照以下步骤操作：

    1. 在右侧窗格中的数据源树中，选择 **Total.Running.Amount.Collect()** 项。
    2. 选择 **绑定**。
    3. 选择 **编辑公式**。
    4. 将公式更新为 `Total.Running.Amount.Sum(false)+Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))`。

    > [!NOTE]
    > `Total.Running.Amount.Sum(false)` 操作数返回先前收集的金额累计总和。 `Total.Running.Amount.Collect(Total.Page.Amount.Sum(true))` 操作数返回当前页面的总金额。 您必须将第二个操作数的嵌套函数的参数指定为 **True** 以在将此值放入 `Total.Running.Amount` 累计总和集合时立即重置 `Total.Page.Amount` 数据集合。 指定的参数必须从 0（零）值开始收集下一页的总计。
    >
    > `Total.Running.Amount.Sum(false)` 函数将被调用以在当前页面的 Excel **ReportPageFooter\_RunningTotalAmount** 单元格中输入金额累计总和。

2. 在格式树中，选择引用 Excel **ReportPageFooter\_RunningTotalWeight** 单元格的嵌套 **范围** 组件，然后执行以下步骤：

    1. 在右侧窗格中的数据源树中，选择 **Total.Running.Weight.Collect()** 项。
    2. 选择 **绑定**。
    3. 选择 **编辑公式**。
    4. 将公式更新为 `Total.Running.Weight.Sum(false)+Total.Running.Weight.Collect(Total.Page.Weight.Sum(true))`。

### <a name="configure-bindings-to-fill-in-the-page-running-counter"></a>配置绑定以填充页面正在运行的计数器

1. 在 **格式设计器** 页上的格式树中，展开 **报表页面页脚** 组件，选择引用 Excel **ReportPageFooter\_RunningCounterLines** 单元格的嵌套 **范围** 组件。
2. 选择 **编辑公式**。
3. 添加公式 `Total.Running.Lines.Collect(COUNT(Total.Page.Amount.Result))`。

    > [!NOTE]
    > 此公式返回整个报表的收集的金额值的数量。 此数字等于当前时刻已经迭代的交易数。 同时，公式将在 **Total.Running.Lines** 集合中收集返回值。

### <a name="configure-bindings-to-fill-in-the-page-footer-counter"></a>配置绑定以填充页面的页脚计数器

1. 在 **格式设计器** 页上的格式树中，展开 **报表页面页脚** 组件，选择引用 Excel **ReportPageFooter\_PageLines** 单元格的嵌套 **范围** 组件。
2. 选择 **编辑公式**。
3. 添加公式 `COUNT(Total.Page.Amount.Result)-Total.Running.Lines.Sum(false)`。

    > [!NOTE]
    > 此公式将当前页面上的交易数量计算为整个报表的 **Total.Page.Amount.Result** 中收集的交易数与在此阶段 **Total.Running.Lines.Sum** 中存储的交易数量之间的差值。 由于当前页面的交易数存储在 **范围** 组件绑定中的 **Total.Running.Lines** 中，该组件引用 Excel **ReportPageFooter\_RunningCounterLines** 单元格，因此当前页面上的交易数尚未包括在内。 因此，此差值等于当前页面上的交易数。

![已配置绑定以填充电子报告格式设计器中的页脚计数器。](./media/er-paginate-excel-reports-format6.png)

### <a name="configure-component-visibility"></a>配置组件可见性

您可以在生成的文档的特定页面上更改页眉和页脚的可见性以隐藏以下元素：

- 第一个页面的页眉，因为报表页眉已经包含列标题
- 没有最后一页可能发生的交易的任何页面的页眉
- 没有最后一页可能发生的交易的任何页面的页脚

要更改可见性，更新 **报表页面页眉** 和 **报表页面页脚** 组件的 **已启用** 属性。

1. 在 **格式设计器** 页上，在格式树中，展开 **报表页面** 组件，选择嵌套 **报表页面页眉** 组件，然后按照以下步骤操作：

    1. 为 **已启用** 字段选择 **编辑**。
    2. 在 **公式设计器** 页面的 **公式** 字段中，输入以下表达式：

        `AND(`<br>
        `COUNT(Total.Page.Amount.Result)<>0,`<br>
        `COUNT(Total.Page.Amount.Result)<>COUNT(model.CommodityRecord)`<br>
        `)`

2. 在格式树中，选择嵌套 **报表页面页脚** 组件，然后按照以下步骤操作：

    1. 为 **已启用** 字段选择 **编辑**。
    2. 在 **公式设计器** 页面的 **公式** 字段中，输入以下表达式：

        `(`<br>
        `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)+`<br>
        `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result))`<br>
        `)<>0`

    > [!NOTE]
    > `COUNT(Total.Page.Amount.Result)-Total.Running.Lines2.Sum(false)` 结构用于计算当前页面上的交易数量。 `0*Total.Running.Lines2.Collect(COUNT(Total.Page.Amount.Result)` 结构用于将当前页面上的交易数添加到集合中，以正确处理下一个页面页脚的可见性。
    >
    > `Total.Running.Lines` 集合不能在这里重用，因为基础组件的 **已启用** 属性在处理嵌套组件的绑定 **后** 处理。 当处理 **已启用** 属性时，`Total.Running.Lines` 集合已经增加了当前页面上的交易数。

3. 选择 **保存**。

## <a name="generate-an-intrastat-declaration-control-report-updated"></a>生成内部统计申报控制报表（已更新）

1. 请确保您在 **内部统计** 页面上有 24 个交易。 重复本主题[生成内部统计申报控制报表](#generate-intrastat-control-report)一节中的步骤生成和查看控制报表。

    所有交易都显示在第一个页面上。 页面总计和计数器等于报表总计和计数器。 页面页眉范围将在第一个页面上隐藏，因为报表页眉已经包含列标题。 页面页眉和页脚将在第二个页面上隐藏，因为该页面不包含任何交易。

    ![桌面应用程序中生成的 Excel 文档。](./media/er-paginate-excel-reports-document2.gif)

2. 通过将 **物料编号** 代码从 **D00006** 更改为 **L0010**，更新 **内部统计** 页面上的两个交易。 请注意，新商品的产品名称 **有源立体声扬声器对** 比原始商品的产品名称 **标准扬声器** 长。 这种情况会强制在生成的文档的相应单元格中自动换行。 现在必须更新文档分页以及与页面相关的合计和盘点。 重复[生成内部统计申报控制报表](#generate-intrastat-control-report)一节中的步骤生成和查看控制报表。

    现在，交易显示在两个页面上，已正确计算了页面总计和计数器。 页面页眉范围已在第一个页面上正确隐藏，在第二个页面上可见。 页面页脚在两个页面上都可见，因为它们包含交易。

    ![已更新桌面应用程序中生成的 Excel 文档。](./media/er-paginate-excel-reports-document3.gif)

## <a name="frequently-asked-questions"></a>常见问题解答

### <a name="is-there-any-way-to-recognize-when-the-final-page-is-processed-by-the-page-format-component"></a>有什么方法可以识别页面格式组件何时处理最终页面？

**页面** 组件[不公开](er-fillable-excel.md#page-component-limitations)有关已处理页面数和生成的文档中的总页数的信息。 不过，您可以配置电子报告[公式](er-formula-language.md)来识别最终页面。 下面是一个示例：

- 使用 **报表页面** 组件计算已处理的交易总数。 您可以使用公式 `COUNT(Total.Page.Amount.Result)` 进行此计算。 
- 根据为 **报表行** 组件配置的 `model.CommodityRecord` 绑定计算必须处理的交易总数。 您可以使用公式 `COUNT(model.CommodityRecord)` 进行此计算。
- 比较两个数字来识别最后一个页面。 当两个值相等时，将生成最后一个页面。

> [!NOTE]
> 我们建议您仅在这一情况下使用此方法：**报表行** 组件的 **已启用** 属性不包含可能在运行时为绑定[记录列表](er-formula-supported-data-types-composite.md#record-list)的一些迭代[记录](er-formula-supported-data-types-composite.md#record)返回 [False](er-formula-supported-data-types-primitive.md#boolean) 的公式。

## <a name="additional-resources"></a>其他资源

- [设计配置以生成 Excel 格式的文档](er-fillable-excel.md)
- [使用电子报告格式 (ER) 的数据集合数据源](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
