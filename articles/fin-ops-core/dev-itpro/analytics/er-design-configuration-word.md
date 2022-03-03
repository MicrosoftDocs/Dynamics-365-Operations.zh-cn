---
title: 设计新 ER 配置以生成 Word 格式的报表
description: 本主题说明用户如何配置新的电子报告 (ER) 格式来以 Microsoft Word 文档形式生成报表。
author: NickSelin
ms.date: 12/17/2020
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
ms.openlocfilehash: 27e9e977193f9ff5c8188b780e8de955742c4ebe
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323867"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a>设计新 ER 配置以生成 Word 格式的报表

[!include [banner](../includes/banner.md)]

以 Microsoft Word 文档形式生成报表，您必须使用 Word 桌面应用程序等为报表设计模板。 下图显示了控制报表的示例模板，生成后显示已处理供应商付款的详细信息。

![Word 桌面应用程序中控制报表的示例模板。](./media/er-design-configuration-word-image1.png)

要将 Word 文档用作 Word 格式的报表的模板，可以配置一个新的[电子报告 (ER)](general-electronic-reporting.md) [解决方案](er-quick-start1-new-solution.md)。 此解决方案必须包含一个包含 ER 格式组件的 ER [配置](general-electronic-reporting.md#Configuration)。

> [!NOTE]
> 当您创建新 ER 格式配置以 Word 格式生成报表时，必须在 **创建配置** 下拉对话框中选择 **Word** 作为格式类型，或保留 **格式类型** 字段为空。

![在“配置”页面上创建格式配置。](./media/er-design-configuration-word-image2.gif)

解决方案的 ER 格式组件必须包含 **Excel\\File** 格式元素，并且该格式元素必须链接到将在运行时用作所生成报表的模板的 Word 文档。 要配置 ER 格式组件，必须在 ER 格式设计器中打开已创建的 ER 配置的[草稿](general-electronic-reporting.md#component-versioning)版本。 然后添加 **Excel\\File** 元素，将 Word 模板附加到可编辑 ER 格式，然后将该模板链接到添加的 **Excel\\File** 元素。

> [!NOTE]
> 在附加模板时，必须使用之前已在 ER 参数中[配置](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)的[文档类型](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types)来存储 ER 格式的模板。

![在“格式设计器”页面上附加模板。](./media/er-design-configuration-word-image3.gif)

您可以为 **Excel\\File** 元素添加 **Excel\\Range** 和 **Excel\\Cell** 嵌套元素，来指定运行时将在生成的报表中输入的数据结构。 然后，您必须将这些元素绑定到可编辑 ER 格式的数据源，来指定运行时将在生成的报表中输入的实际数据。

![在“格式设计器”页面上添加嵌套元素。](./media/er-design-configuration-word-image4.gif)

在设计期间保存对 ER 格式的更改时，分层格式结构将作为名为 **报表** 的[自定义 XML 部件](/visualstudio/vsto/custom-xml-parts-overview)存储在附加的 Word 模板中。 您必须访问修改后的模板，从 Finance 中下载它，将它存储在本地，然后在 Word 桌面应用程序中打开它。 下图显示了包含 **报表** 自定义 XML 部件的控制报表的本地存储的示例模板。

![在 Word 桌面应用程序中预览示例报表模板。](./media/er-design-configuration-word-image5.gif)

在运行时 **Excel\\Range** 和 **Excel\\Cell** 格式元素的绑定运行时，每个绑定提供的数据将作为 **报表** 自定义 XML 部件的单独字段进入生成的 Word 文档。 要在生成的文档中输入自定义 XML 部件的字段中的值，您必须将适当的 Word [内容控件](/office/client-developer/word/content-controls-in-word)添加到 Word 模板中，以在运行时用作将要填充的数据的占位符。 要指定内容控件的填充方式，请将每个内容控件映射到 **报表** 自定义 XML 部件的相应字段。

![在 Word 桌面应用程序中添加和映射内容控件。](./media/er-design-configuration-word-image6.gif)

然后，您必须用修改后的模板替换可编辑 ER 格式的原始 Word 模板，修改后的模板现在包含映射到 **报表** 自定义 XML 部件的字段的 Word 内容控件。

![在“格式设计器”页面上替换模板。](./media/er-design-configuration-word-image7.gif)

当您运行配置的 ER 格式时，附加的 Word 模板用于生成新报表。 实际数据作为名为 **报表** 的自定义 XML 部件存储在 Word 报表中。 打开生成的报表时，Word 内容控件中将填充来自 **报表** 自定义 XML 部件的数据。

## <a name="frequently-asked-questions"></a>常见问题

**问题：** 我配置了 ER 格式来打印包含公司地址的 Word 文档。 在此 ER 格式的 Word 模板中，我插入了富文本内容控件来显示公司地址。 在 Finance 中，我使用多行文本输入了公司地址，然后选择 **Enter** 为我输入的每一行添加回车符。 所以，我预期公司地址在生成的文档中会显示为多行文本。 但是，地址显示为包含特殊符号而不是回车符的单行文本。 我的设置有什么问题？

**回答：** 您必须使用纯文本内容控件，并选中控件属性中的 **允许回车符(多个段落)** 复选框，而不是使用富文本内容控件。

## <a name="additional-resources"></a>其他资源

- [重用带有 Excel 模板的 ER 配置以 Word 格式生成报表](./tasks/er-design-configuration-word-2016-11.md)
- [使用 ER 在您生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
