---
title: 重用带有 Excel 模板的 ER 配置以 Word 格式生成报表
description: 本文介绍如何配置设计为以 Excel 工作簿形式生成报表的报表格式，来以 Word 文档形式生成报表。
author: kfend
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
ms.openlocfilehash: eea037751bc7ae4cb5e45fcaa0166d1f2f0b8292
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291165"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a>重用带有 Excel 模板的 ER 配置以 Word 格式生成报表

[!include [banner](../../includes/banner.md)]

要以 Microsoft Word 文档形式生成报表，您可以[配置](../er-design-configuration-word.md)一个新的[电子报告 (ER)](../general-electronic-reporting.md) 格式。 或者，您可以重用最初设计为以 Excel 工作簿形式生成报表的 ER 格式。 在这种情况下，您必须用 Word 模板替换 Excel 模板。

以下过程说明具有系统管理员角色或电子报告开发人员角色的用户，如何通过重用设计为以 Excel 文件形式生成报表的 ER 格式，来将 ER 格式配置为以 Word 文件形式生成报表。

这些过程可以在 GBSI 公司中完成。

## <a name="prerequisites"></a>先决条件

要完成这些过程，您必须首先按照[设计用于以 OPENXML 格式生成报表的配置](er-design-reports-openxml-2016-11.md)任务指南中的步骤操作。

您还必须为同一个报表下载以下模板并保存到本地：

- [付款报表模板 (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [付款报表绑定模板 (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

这些过程针对的是 Dynamics 365 for Operations 版本 1611（2016 年 11 月）中添加的功能。

## <a name="select-the-existing-er-report-configuration"></a>选择现有 ER 报表配置

1. 在 Dynamics 365 Finance 应用中，转到 **组织管理** \> **工作区** \> **电子申报**。
2. 确保 **Litware, Inc.** 配置提供程序已选择 **有效**。 否则，请按照[创建配置提供程序并将其标记为有效](er-configuration-provider-mark-it-active-2016-11.md)任务指南中的步骤操作。
3. 选择 **申报配置**。 您将重用设计为以 OPENXML 格式生成报表输出的现有 ER 配置。
4. 在 **配置** 页的左侧窗格的配置树中，展开 **付款模型**，选择 **示例工作表报表**。

    > [!NOTE]
    > 所选 ER 格式的草稿版本可以在 **版本** 快速选项卡上编辑。

5. 选择 **设计器**。
6. 在 **格式设计器** 页上，注意根格式元素的标题指示当前正在使用 Excel 模板。

![选择现有配置。](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a>查看下载的 Word 模板

1. 在 Word 桌面应用程序中，打开您先前下载的 **SampleVendPaymDocReport.docx** 模板文件。
2. 确认此模板仅包含要作为 ER 输出生成的文档的布局。

![桌面应用程序中的 Word 模板布局。](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a>将 Excel 模板替换为 Word 模板并添加自定义 XML 部件

目前使用 Excel 文档作为模板生成 OPENXML 格式的输出。 您将此模板替换为前面下载的 Word 模板文件 SampleVendPaymDocReport.docx。 您还将通过添加自定义 XML 部件扩展 Work 模板。

1. 在 Finance 中，在 **格式设计器** 页的 **格式** 选项卡上，选择 **附件**。
2. 在 **附件** 页上，选择 **删除** 删除现有的 Excel 模板。 选择 **是** 确认更改。
3. 选择 **新建** \> **文件**。

    > [!NOTE]
    > 您必须选择已在 ER 参数中[配置](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)的文档类型来存储 ER 格式的模板。

4. 选择 **浏览**，然后浏览到并选择您先前下载的 **SampleVendPaymDocReport.docx** 文件。
5. 选择 **确定**。
6. 关闭 **附件** 页。
7. 在 **格式设计器** 页上，在 **模板** 字段中，输入或选择 **SampleVendPaymDocReport.docx** 文件以使用该 Word 模板而不是以前使用的 Excel 模板。
8. 选择 **保存**。

    除了存储配置更改之外，**保存** 操作还会更新附加的 Word 模板。 所设计格式的层次结构采用名称 **报表**、作为新的自定义 XML 部件添加到附加的 Word 文档。 附加的 Word 模板包含要作为 ER 输出生成的文档的布局，以及 ER 将在运行时输入到该模板中的数据的结构。

9. 注意根格式元素的标题指示当前正在使用 Word 模板。

    ![将 Excel 模板替换为 Word 模板并添加自定义 XML 部件。](../media/er-design-configuration-word-2016-11-image03.gif)

10. 在 **格式** 选项卡中，选择 **附件**。

您现在可以将 **报表** 自定义 XML 部件的元素映射到 Word 文档的内容控件。

如果您熟悉此流程：将 Word 文档设计为包含映射到[自定义 XML 部件](/visualstudio/vsto/custom-xml-parts-overview)的元素的[内容控件](/office/client-developer/word/content-controls-in-word)的表单，请完成下一个过程中的所有步骤来创建文档。 有关详细信息，请参阅[在 Word 中创建用户填写或打印的表单](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b)。 否则，请跳过下一个过程。

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a>获取具有自定义 XML 部件的 Word 文档并进行数据映射

1. 在 Finance 中，在 **附件** 页上，选择 **打开** 从 Finance 下载所选模板并将其本地存储为 Word 文档。
3. 在 Word 桌面应用程序中，打开刚才下载的文档。
4. 在 **开发人员** 选项卡上，选择 **XML 映射窗格**。

    > [!NOTE]
    > 如果 **开发人员** 选项卡没有出现在功能区上，请自定义功能区来进行添加。

5. 在 **XML 映射** 窗格中的 **自定义 XML 部件** 字段中，选择 **报表** 自定义 XML 部件。
6. 将所选的 **报表** 自定义 XML 部件的元素与 Word 文档的内容控件进行映射。
7. 将更新的 Word 文档本地保存为 **SampleVendPaymDocReportBounded.docx**。

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>查看将自定义 XML 部件映射到内容控件的 Word 模板

1. 在 Word 桌面应用程序中，打开 **SampleVendPaymDocReportBounded.docx** 模板文件。
2. 确认此模板包含要作为 ER 输出生成的文档的布局。 用作 ER 将在运行时在此模板中输入的数据的占位符的内容控件，基于在 **报表** 自定义 XML 部件的元素与 Word 文档的内容控件之间配置的映射。

![桌面应用程序中的 Word 模板预览。](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a>上载将自定义 XML 部件映射到内容控件的 Word 模板

1. 在 Finance 中，在 **附件** 页上，选择 **删除** 删除在 **报表** 自定义 XML 部件的元素与内容控件之间没有映射的 Word 模板。 选择 **是** 确认更改。
2. 选择 **新建**\>**文件**，添加一个包含 **报表** 自定义 XML 部件的元素与内容控件之间的映射的新模板文件。

    > [!NOTE]
    > 您必须选择已在 ER 参数中[配置](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)的文档类型来存储 ER 格式的模板。

3. 选择 **浏览**，然后浏览到并选择您通过完成 [获取具有自定义 XML 部件的 Word 以进行数据映射](#get-word-doc)一节中的过程下载或准备的 **SampleVendPaymDocReportBounded.docx** 文件。
4. 选择 **确定**。
5. 关闭 **附件** 页。
6. 在 **格式设计器** 页上，在 **模板** 字段中，选择您刚才下载的文档。
7. 选择 **保存**。
8. 关闭 **格式设计器** 页。

## <a name="mark-the-configured-format-as-runnable"></a>将配置的格式标记为可运行

要运行可编辑格式的草稿版本，您必须先使其[可运行](../er-quick-start2-customize-report.md#MarkFormatRunnable)。

1. 在 Finance 中，在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
2. 在 **使用参数** 对话框中，将 **运行设置** 选项设置为 **是**，然后选择 **确定**。
3. 根据需要，选择 **编辑** 以使当前页面可供编辑。
4. 对于当前选择的 **示例工作表报表** 配置，将 **运行草稿** 选项设置为 **是**。
5. 选择 **保存**。

## <a name="run-the-format-to-create-output-in-word-format"></a>运行格式以 Word 格式创建输出

1. 在 Finance 中，转到 **应付帐款** \> **付款** \> **付款日记帐**。
2. 在您之前输入的付款日记帐中，选择 **行**。
3. 在 **供应商付款** 页上，选择网格中的所有行。
4. 选择 **付款状态**\>**无**。

    ![供应商付款页面上要进行处理的付款。](../media/er-design-configuration-word-2016-11-image05.png)

5. 在操作窗格上，选择 **生成付款**。
6. 在出现的对话框中，执行以下步骤：

    1. 在 **付款方式** 字段中，选择 **电子**。
    2. 在 **银行帐户** 字段中，选择 **GBSI OPER**。
    3. 选择 **确定**。

7. 在 **电子申报参数** 对话框中，选择 **确定**。
8. 生成的输出以 Word 格式表示，其中包含处理的付款的详细信息。 分析生成的输出。

    ![以 Word 格式生成的输出。](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a>其他资源

- [设计新的电子报告配置以生成 Word 格式的报表](../er-design-configuration-word.md)
- [使用 ER 在您生成的文档中嵌入图像和形状](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
