---
title: 禁止在生成的报告中使用 Word 内容控件
description: 本文说明如何配置电子报告 (ER) 格式，以在禁止使用内容控件的地方生成 Microsoft Word 文件形式的报告。
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: e11b697b78c89a1758fa9e81c901bd29fe281539
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882104"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a>禁止在生成的报告中使用 Word 内容控件

[!include [banner](../includes/banner.md)]

要生成 Microsoft Word 文档形式的报告，必须将报告的模板设计为 Word 文档。 此模板必须包含 Word 内容控件作为将在运行时填充的数据的占位符。 要将创建的 Word 文档用作报表的模板，可以[配置](er-design-configuration-word.md)一个新的[电子报告 (ER)](general-electronic-reporting.md) [解决方案](er-quick-start1-new-solution.md)。 此解决方案必须包含一个包含 ER 格式组件的 ER [配置](general-electronic-reporting.md#Configuration)。 必须配置这种 ER 格式才能使用设计的模板来生成报告。

在 10.0.6 版及更高版本的 Dynamics 365 Finance 中，您可以以 ER 格式配置公式，以在生成的文档中禁止使用某些 Word 内容控件。

以下步骤说明了分配有系统管理员或电子报告功能顾问角色的用户如何配置 ER 格式，以生成 Word 文件形式的报告，并在使用 Word 模板配置的已生成报告中禁止使用某些内容控件。

这些步骤可以在 GBSI 公司完成。

## <a name="prerequisites"></a>先决条件

若要完成这些步骤，首先必须完成下面任务指南中的步骤：

- [设计以 OPENXML 格式生成报表的配置](./tasks/er-design-reports-openxml-2016-11.md)
- [重复使用带有 Excel 模板的电子报告配置以 Word 格式生成报表](./tasks/er-design-configuration-word-2016-11.md)

完成这些任务指南的步骤时，将准备以下项目：

- 一种配置为以 Word 格式生成文档的 **样本工作表报告** ER 格式
- 一种标记为 **可运行** 的 [草稿](general-electronic-reporting.md#component-versioning)版本的 **样本工作表报告** ER 格式
- 一种配置为使用 **样本工作表报告** ER 格式进行供应商付款处理的 **电子** 付款方式

您还必须为同一个报表下载和保存以下模板：

- [付款报表绑定模板 2 (SampleVendPaymDocReportBounded2.docx)](https://download.microsoft.com/download/1/9/b/19b36e39-861a-414e-9150-9880d9d2487c/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a>查看下载的 Word 模板

1. 在 Word 桌面应用程序中，打开您先前下载的 **SampleVendPaymDocReportBounded2.docx** 模板文件。
2. 验证模板文件是否包含摘要部分，该部分显示所处理付款中已满足的每种货币代码的总付款额。

    - 摘要部分位于 Word 文档的单独表中。
    - 该表的第一行将表列标题作为节标题。
    - 该表的第二行将重复的内容控件保留为节详细信息。
    - 此内容控件已映射到 **报告** 自定义 XML 部件的 **SummaryLines** 字段。
    - 根据此映射，内容控件与可编辑 ER 格式的 **SummaryLines** 元素关联。

    > [!NOTE]
    > 重复内容控件由 **SummaryLines** 键标记，此键与已映射到的自定义 XML 部件的字段相匹配。

    ![Word 模板布局。](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a>选择现有 ER 报表配置

对于以下步骤，您将重复使用在完成前面提到的任务指南中的步骤时配置的现有 ER 配置。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 选择 **申报配置**。
3. 在 **配置** 页的配置树中，展开 **付款模型**，选择 **示例工作表报表**。
4. 选择 **设计器** 以编辑所选 ER 格式的草稿版本。

## <a name="replace-the-current-template-with-the-new-template"></a>将当前模板替换为新模板

目前使用 SampleVendPaymDocReportBounded.docx 文件作为模板生成 Word 格式的输出。 在以下步骤中，您将此 Word 模板替换为前面下载的新 Word 模板，即 SampleVendPaymDocReportBounded2.docx。

1. 在 **格式设计器** 页上，选择 **附件**。
2. 在 **附件** 页上，选择 **删除** 删除现有的模板。
3. 选择 **是** 以确认删除。
4. 选择 **新建** \> **文件**。
5. 选择 **浏览**，然后浏览到并选择您先前下载的 **SampleVendPaymDocReportBounded2.docx** 文件。
6. 选择 **确定**。
7. 关闭 **附件** 页。
8. 在 **格式设计器** 页面上的 **模板** 字段中，输入或选择 **SampleVendPaymDocReportBounded2.docx** 文件。

## <a name="run-the-format-to-create-word-output"></a>运行此格式以创建 Word 输出

1. 转到 **应付帐款** \> **付款** \> **付款日记帐**。
2. 在 **供应商付款** 页面上的 **列表** 选项卡上，选择所有付款。
3. 选择 **付款状态**\>**无**。
4. 选择 **生成付款**。
5. 在 **付款方式** 字段中，选择 **电子**。
6. 在 **银行帐户** 字段中，选择 **GBSI OPER**。
7. 选择 **确定**。
8. 在 **电子报告参数** 对话框中，选择 **确定**，并分析生成的输出。

    ![供应商付款页面上要进行处理的付款。](./media/er-design-configuration-word-suppress-controls-image2.gif)

    输出以 Word 格式显示，并包含摘要部分。

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a>配置可编辑格式以禁止显示摘要部分

如果要在生成的文档中禁止显示摘要部分，则必须根据运行此 ER 格式的用户的要求来修改可编辑的 ER 格式。

1. 转到 **组织管理**\>**工作区**\>**电子报告**，然后打开 ER 格式的草稿版本进行编辑。
2. 选择 **申报配置**。 
3. 在 **配置** 页上的配置树中，展开 **付款模型** \> **示例工作表报表**。
4. 选择 **设计器**。
5. 在 **格式设计器** 页面上，展开 **Word**，然后选择 **SummaryLines**。
6. 在 **映射** 选项卡上，添加一个新的数据源以在运行时询问用户是否应禁止显示摘要部分：

    1. 选择 **添加根**。
    2. 在 **添加数据源** 对话框中，选择 **常规\用户输入参数** 以打开 **用户输入参数数据源属性** 对话框。
    3. 在 **名称** 字段中，输入 **uipSuppress**。
    4. 在 **标签** 字段中，输入 **禁止显示摘要部分**。
    5. 在 **操作数据类型名称** 字段中，选择或输入 **NoYes**。
    6. 选择 **确定**。

7. 添加 **NoYes** 应用程序枚举类型的新数据源：

    1. 选择 **添加根**。
    2. 在 **添加数据源** 对话框中，选择 **Dynamics 365 for Operations\枚举**，以打开 **枚举数据源属性** 对话框。
    3. 在 **名称** 字段中，输入 **enumNoYes**。
    4. 在 **标签** 字段中，输入 **禁止显示选项**。
    5. 在 **操作数据类型名称** 字段中，选择或输入 **NoYes**。
    6. 选择 **确定**。

8. 对于所选 **SummaryLines** 格式元素，配置公式以指定何时应禁止使用与所选格式元素关联的 Word 内容控件：

    1. 在 **映射** 选项卡上的 **已移除** 部分，选择 **编辑** 以打开 **[公式设计器](general-electronic-reporting-formula-designer.md)** 页。
    2. 在 **公式** 字段中，输入公式 `uipSuppress = enumNoYes.Yes`。
    3. 选择 **保存**，然后关闭 **公式设计器** 页面。

        > [!NOTE]
        > **在所有其他格式元素都运行之后**，此公式将应用于生成的文档。 为了应用此公式，会在生成的文档中查找一个被标记为配置公式所针对的格式元素（在本例中为 **SummaryLines**）的 Word 内容控件。 然后，将该内容控件以及保存它的 Word 表中的行一起完全删除。 摘要部分的详细信息行将从生成的文档中删除。
        >
        > 在设计时，您可以对格式元素配置 **已移除** 公式，即使您使用的 Word 模板中的内容控件没有与配置 **已移除** 属性所针对的格式元素名称相匹配的标签。 在设计时验证格式时，您会收到关于这种不一致的[警告](er-components-inspections.md#i14)。
        >
        > 在运行时，如果您使用的 Word 模板中的内容控件没有与配置 **已移除** 属性所针对的格式元素名称相匹配的标签，则会引发异常。

    4. 在 **映射** 选项卡上的 **已移除** 部分，将 **随父项一起** 选项设置为 **是**。

        > [!NOTE]
        > 您必须将此选项设置为 **是**，才能将整个 Word 表作为包含摘要部分详细信息的行的父对象删除。 如果将此选项设置为 **否**，则节标题行会保留在生成的文档中。

9. 选择 **保存** 以保存对可编辑格式所做的更改。

    ![以 Word 格式生成的输出。](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a>运行修改的格式以创建 Word 输出

1. 转到 **应付帐款** \> **付款** \> **付款日记帐**。
2. 选择所创建的付款日记帐，然后选择 **行**。
3. 在 **供应商付款** 页上，选择所有行，然后选择 **支付状态**\>**无**。
4. 选择 **生成付款**。
5. 在 **付款方式** 字段中，选择 **电子**。
6. 在 **银行帐户** 字段中，选择 **GBSI OPER**。
7. 选择 **确定**。
8. 在 **电子报告参数** 对话框内的 **禁止显示摘要部分** 字段中，选择 **是**。
9. 选择 **确定**，并分析生成的输出。

    ![以 Word 格式生成的输出。](./media/er-design-configuration-word-suppress-controls-image4.gif)

    请注意，该输出不包含摘要部分，因为它已被禁止显示。

## <a name="additional-resources"></a>其他资源

- [设计以 OPENXML 格式生成报表的配置](./tasks/er-design-reports-openxml-2016-11.md)
- [设计新的电子报告配置以生成 Word 格式的报表](er-design-configuration-word.md)
- [重复使用带有 Excel 模板的电子报告配置以 Word 格式生成报表](./tasks/er-design-configuration-word-2016-11.md)
- [检查配置的 ER 组件以防止运行时问题](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
