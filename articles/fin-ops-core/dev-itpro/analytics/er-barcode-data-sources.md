---
title: 使用条码数据源生成条码图像
description: 本主题说明如何使用条码数据源生成条码图像。
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: 72c79c37ca5b5f98637ba5069e25465bb1391306
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343255"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a>使用条码数据源生成条码图像

[!include[banner](../includes/banner.md)]

您可以使用[电子报告 (ER)](general-electronic-reporting.md) 框架来设计可以运行来生成所需的电子版和可打印传出文档的 [ER 格式组件](general-electronic-reporting.md#FormatComponentOutbound)。 若要生成 Microsoft Office 格式的传出文档，必须使用 Microsoft Excel 文档或 Microsoft Word 文档作为报告模板来指定报告的布局。 [ER 操作设计器](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base)使您可以将 Excel 或 Word 文档附加为 ER 格式的模板。 附加模板中的以下命名元素与配置的格式组件的元素相关联：

- Word 中的内容控件
- Excel 中的命名工作表、范围、单元格、形状和图像

这些命名元素用作运行 ER 格式时在生成的文档中输入的数据的占位符。 ER 格式元素将绑定到数据源。 这些数据源指定在运行时将在生成的文档中输入的数据。 有关详细信息，请参阅[使用 ER 在您生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)。

ER 现在支持 **条码** 数据源类型。 因此，您现在可以生成一个代表指定文本的条码的图像。 配置 ER 格式时，可以指定 **条码** 类型的数据源来生成条码图像。 然后，您可以将这些图像添加到生成的业务文档中，如订单、发票、装箱单和收据。 您还可以将它们添加到各种标签中，如产品和货位标签以及包装和发货标签。

报告模板中可以使用以下占位符来输入条码图像：

- Word 的[图片](/office/client-developer/word/content-controls-in-word)内容控件
- Excel 中的[图片](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344)对象

通过使用 **条码** 类型的数据源，您可以生成以下格式的条码：

- 一维条码：

    - Codabar
    - Code 39
    - Code 93
    - Code 128
    - EAN-8
    - EAN-13
    - ITF-14
    - 智能邮件
    - MSI
    - Plessey
    - PDF417
    - UPC-A
    - UPC-E

- 二维条码：

    - Aztec
    - 数据矩阵
    - QR 码

当您配置 **条码** 数据源时，您可以定义用于生成图像的特定绘制参数：

- **宽度** – 以像素为单位指定条码的宽度。 值 **0**（零）指示使用默认宽度。 对于不同的格式，含义可能有所不同。
- **高度** – 以像素为单位指定条码的高度。 值 **0**（零）指示使用默认高度。 对于不同的格式，含义可能有所不同。
- **边距** – 以像素为单位指定条码边距的大小。 边距是条码两侧必须留出的区域（静区）。 值 **0**（零）指示使用默认边距。 对于不同的格式，含义可能有所不同。
- **输出内容** – 将值设置为 **是** 将生成包含编码信息作为文本的条码图像。 默认值为 **否**。
- **编码** – 指定在生成的条码图像中编码的字符的类型。 默认情况下，使用 **UTF-8** 编码。

> [!IMPORTANT]
> 当您添加新的 **条码** 数据源时，必须将其作为嵌套元素放在另一个项目（容器）下。
>
> 当您将 **条码** 数据源以某种格式绑定到单元格元素，并且该单元格元素表示 Word 内容控件或 Excel 图片时，数据源在该绑定中显示为具有单个 **字符串** 类型参数的函数。 您必须使用此参数来指定应转换为条码图像并在扫描生成的条码时读取的文本。

有关此功能的详细信息，请完成本主题中的示例。

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a>示例：生成包含对应付金额进行编码的条码的付款支票

本示例说明具有 **系统管理员** 或 **电子报告功能顾问** 角色的用户如何配置 ER 格式，该格式包含用于生成包含条码的 Excel 格式传出文档的模板。 这里是所涉及步骤的概览。

1. [完成先决条件](#ExamplePrerequisites)。
2. [激活配置提供程序](#ExampleProvider)。
3. [导入提供的 ER 解决方案](#ExampleImportSolution)。
4. [生成付款支票](#ExampleGenerateCheque)。
5. [查看生成的付款支票](#ExampleReviewGeneratedCheque)。
6. [修改提供的 ER 解决方案的格式](#ExampleModifyFormat)。

    1. [应用新支票模板](#ExampleModifyFormatApplyTemplate)。
    2. [添加新条码数据源](#ExampleModifyFormatAddDataSource)。
    3. [绑定新格式元素](#ExampleModifyFormatBindFormatElement)。
    4. [使修改后的版本可用于测试运行](#ExampleModifyFormatMakeVersionAvailable)。

        1. [完成修改后的格式版本](#CompleteToRun)。
        2. [使草稿版本可供使用](#MarkToRun)。

7. [生成付款支票](#ExampleGenerateCheque2)。
8. [将生成的支票转换为 PDF](#ExampleConvertToPDF)。

在此示例中，您将使用已配置为生成付款支票的提供的 ER 解决方案。 此解决方案生成应付金额同时以数字和文本形式书写的付款支票。 您将修改此 ER 解决方案，使支票还包括对应付金额进行编码的生成的条码，该条码可以使用条码扫描仪进行读取。

这些步骤可以在 Microsoft Dynamics 365 Finance 中在 **USMF** 公司中完成。

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a>完成先决条件

若要完成本示例，您必须能够用以下角色之一访问 USMF 公司的 Finance：

- 电子申报功能顾问
- 系统管理员

如果您尚未完成[使用 ER 在您生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)主题中的示例，请下载示例 ER 解决方案的以下配置。

| 内容描述         | 文件名                   |
|-----------------------------|-----------------------------|
| ER 数据模型配置 | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)      |
| ER 格式配置     | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |

此外，下载以下 Excel 文件，其中包含所提供的 ER 解决方案的修改后的模板。

| 内容描述 | 文件名                 |
|---------------------|---------------------------|
| 报告模板     | [Check template Excel.xlsx](https://download.microsoft.com/download/3/b/d/3bd3b944-da8f-43b4-8533-3c1292a4c3ef/CheckTemplateExcel.xlsx) |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a>激活配置提供程序

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页上的 **配置提供程序** 部分中，确保列出了示例公司 **Litware, Inc.** 的[配置提供程序](general-electronic-reporting.md#Provider)，并将其标记为活动状态。 如果未列出，或者未将其标记为活动状态，请按照[创建一个配置提供程序，并标记其为活动状态](tasks/er-configuration-provider-mark-it-active-2016-11.md)中的步骤操作。

![在“本地化配置”页面上将示例公司设置为活动状态。](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a>导入提供的 ER 解决方案

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置** 磁贴。
3. 在 **配置** 页面上，如果 **支票的模型** 配置在配置树中不可用，请按照以下步骤导入 ER 数据模型配置：

    1. 在操作窗格上，选择 **交换** \> **从 XML 文件加载**。
    2. 在对话框中，选择 **浏览**，找到并选择 **Model for cheques.xml** 文件，然后选择 **确定**。

4. 如果 **支票打印格式** 配置在配置树中不可用，请按照以下步骤导入 ER 格式配置：

    1. 在操作窗格上，选择 **交换** \> **从 XML 文件加载**。
    2. 在对话框中，选择 **浏览**，找到并选择 **Cheques printing format.xml** 文件，然后选择 **确定**。

5. 在配置树中，展开 **支票的模型**。
6. 在配置树中查看导入的 ER 配置的列表。

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a>生成付款支票

1. 转到 **现金和银行管理** \> **银行帐户** \> **银行帐户**。
2. 在 **银行帐户** 页面上，选择 **USMF OPER** 帐户。
3. 在银行帐户详细信息页的操作窗格中，在 **设置** 选项卡的 **布局** 组中，选择 **支票**。
4. 在 **支票版式** 页面上，选择 **编辑**。
5. 在 **常规** 快速选项卡上，将 **一般电子导出格式** 选项设置为 **是**。
6. 在 **导出格式配置** 字段中，选择您先前导入的 **支票打印格式** ER 格式。
7. 在操作窗格上，选择 **打印测试**。
8. 在对话框中，将 **可转让支票格式** 选项设置为 **是**，然后选择 **确定**。

    ![支票版式 - 打印测试对话框。](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a>查看生成的付款支票

- 在 Excel 中打开生成的支票。
2. 检查生成的支票。

    ![在 Excel 中生成的付款支票。](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a>修改提供的 ER 解决方案的格式

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a>应用新支票模板

您可以使用 Excel 桌面应用程序打开您先前导入的 **Cheque template Excel.xlsx** 文件。 请注意，此模板与您在提供的 ER 解决方案中用于生成付款支票的模板不同。 此外，它还包括条码图像的 **AmountBarcode** 元素。

![Excel 模板中的 AmountBarcode 元素。](./media/er-barcode-data-source-cheque2.png)

您现在必须修改 ER 解决方案，然后[重新应用](modify-electronic-reporting-format-reapply-excel-template.md)修改后的模板。

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置**。
3. 在 **配置** 页面，在配置树中，展开 **支票的模型**，然后选择 **支票打印格式**。
4. 在操作窗格上，选择 **设计器**。
5. 在 ER 操作设计器中，选择页面右侧的 **映射** 选项卡，然后在左侧的格式树窗格中，选择 **展开/折叠**。
6. 请注意，所有单元格格式元素都绑定到适当的数据源。

    ![在 ER 操作设计器中将单元格格式元素绑定到数据源。](./media/er-barcode-data-source-cells-bound.png)

7. 选择页面右侧的 **格式** 选项卡。
8. 在操作窗格上，选择省略号 (**...**)，然后选择 **导入**。
9. 在 **导入** 组中，选择 **从 Excel 更新**，然后选择 **更新模板**。
10. 在对话框中，浏览到保存在计算机上的 **Cheque template Excel.xlsx** 文件，选择它，然后选择 **确定** 确认应该应用所选模板。
11. 选择页面右侧的 **映射** 选项卡，然后在左侧的格式树窗格中，选择 **展开/折叠**。
12. 请注意，**AmountBarcode** 单元格元素已添加到格式。 此元素与 **AmountBarcode** 元素相关联，后者已作为条码图像的占位符添加到修改后的 Excel 模板中。

    ![在 ER 操作设计器中添加到格式中的 AmountBarcode 单元格元素。](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a>添加新条码数据源

接下来，您必须添加 **条码** 类型的新数据源。

1. 在 ER 操作设计器中，在页面右侧的 **映射** 选项卡上，选择 **打印** 数据源。
2. 选择 **添加**，然后在 **函数** 组中，选择 **条码** 数据源类型。

    ![选择条码数据源类型。](./media/er-barcode-data-source-add.png)

3. 在对话框的 **名称** 字段中，输入 **条码**。
4. 在 **条码格式** 中，选择 **Code 128**。
5. 在 **宽度** 字段中，输入 **500**。
6. 选择 **确定**。

    ![数据源属性对话框。](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a>绑定新格式元素

接下来，必须将新的格式元素绑定到刚才添加的数据源。

1. 在 ER 操作设计器中，在页面右侧的 **映射** 选项卡上，选择 **打印\\条码** 数据源。
2. 在左侧的格式树窗格中，选择 **AmountBarcode** 单元格元素，然后选择 **绑定**。
3. 在操作窗格上，选择 **显示详细信息**。
4. 请注意，由于 **条码** 数据源在绑定中表示为包含单个参数的函数，绑定格式元素的名称已自动提取为该参数的参数。

    ![ER 操作设计器中条码数据源的详细信息。](./media/er-barcode-data-source-bind1.png)

5. 选择 **编辑公式** 调整绑定。

    您不希望返回单元格元素的名称。 因此，您必须配置一个返回包含当前支票的应付金额的文本的表达式。 由于父 **ChequeLines** 范围绑定到 **model.cheques** 数据源，因此当前支票的应付金额可在 **实数** 数据类型的 **model.cheques.attributes.amount** 字段中找到。

6. 在 **公式** 字段中，输入 **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**。
7. 选择 **保存**，然后关闭 [ER 公式设计器](general-electronic-reporting-formula-designer.md)。
8. 请注意，绑定已调整。

    ![在 ER 操作设计器中调整的绑定。](./media/er-barcode-data-source-bind2.png)

9. 选择 **保存**，然后关闭 ER 操作设计器。

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a>使修改后的版本可用于测试运行

默认情况下，只有状态为 **已完成** 和 **已共享** 的版本将在运行 ER 格式时使用。

如果您已经完成更改，可以使用当前的草稿版本完成工作，然后使更改可供使用。 有关说明，请参阅接下来的[完成修改后的格式版本](#CompleteToRun)一节。

如果要继续使用当前的草稿版本，但是必须使用它来生成支票，您必须明确指定要使用格式的草稿版本来执行。 有关说明，请参阅[使草稿版本可供使用](#MarkToRun)一节。

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a>完成修改后的格式版本

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置**。
3. 在 **配置** 页面，在配置树中，展开 **支票的模型**，然后选择 **支票打印格式**。
4. 在 **版本** 快速选项卡上，选择状态为 **草稿** 的记录。
5. 选择 **更改状态**，然后选择 **完成**。
6. 在对话框中，选择 **确定**。

当前版本的状态将从 **草稿** 更改为 **已完成**，并将创建状态为 **草稿** 的新版本。 您可以使用此新的草稿版本来应用其他更改。

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a>使草稿版本可供使用

1. 转到 **组织管理** \> **工作区** \> **电子申报**。
2. 在 **本地化配置** 页面的 **配置** 部分中，选择 **报告配置**。
3. 在 **配置** 页操作窗格中 **配置** 选项卡的 **高级设置** 组中，选择 **用户参数**。
4. 在对话框中，将 **运行设置** 选项设置为 **是**，然后选择 **确定**。
5. 在配置树中，展开 **支票的模型**，选择 **支票打印格式**。
6. 将 **运行草稿** 选项设置为 **是**。
7. 选择 **保存**。

运行所选格式时，所选格式的草稿版本将被标记为可以使用。

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a>生成付款支票

1. 转到 **现金和银行管理** \> **银行帐户** \> **银行帐户**。
2. 在 **银行帐户** 页面上，选择 **USMF OPER** 帐户。
3. 在银行帐户详细信息页的操作窗格中，在 **设置** 选项卡的 **布局** 组中，选择 **支票**。
4. 在 **支票版式** 页面上的操作窗格上，选择 **打印测试**。
5. 在对话框中，将 **可转让支票格式** 选项设置为 **是**。
6. 选择 **确定**。
7. 检查生成的支票。 请注意，已生成条码以对支票的应付金额进行编码。

    ![在 Excel 中使用条码生成的付款支票。](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> 如果 **条码** 数据源的参数不符合特定于条码格式的适当要求，将引发异常。 例如，当调用 **条码** 数据源以为提供的文本生成 [EAN-8](https://wikipedia.org/wiki/EAN-8) 条码时，如果文本长度超过七个字符将引发异常。

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a>将生成的支票转换为 PDF

如[生成可打印的 FTI 表单](er-generate-printable-fti-forms.md#finland)主题中所述，您可以使用特殊字体在生成的文档中生成条码。 在这种情况下，生成文档的其他转换可能取决于转换环境中该字体的可用性。 例如，如果您尝试将文档转换为 PDF 格式或在缺少字体的环境中预览文档，条码将无法正确呈现。

但是，当您使用 **条码** 数据源来生成条码时，这些条码的呈现将不依赖于任何字体。 因此，您可以轻松地将包含条码的文档转换为 PDF 格式。 下图显示了生成的付款支票的预览，该支票已基于配置的 ER [目标](electronic-reporting-destinations.md)的设置[转换](electronic-reporting-destinations.md#OutputConversionToPDF)为 PDF。

![付款支票的 PDF 的预览。](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a>限制

> [!NOTE]
> 生成的某些类型的条码具有固定的纵横比。 如果您已打开 **支持在电子申报框架中使用 EPPlus 库** 功能以在 ER 中使用 Excel 文档，此行为将很重要。 在这种情况下，图像将输入到具有锁定纵横比的占位符中。 因此，当模板中占位符的尺寸对应于所输入图像的比例时，可以调整生成文档中的实际图片的大小，以保持所需的纵横比。 为阻止图片调整大小，请使用具有预期纵横比的占位符。

## <a name="additional-resources"></a>其他资源

- [电子申报概览](general-electronic-reporting.md)
- [电子报告目标](electronic-reporting-destinations.md)
- [电子申报公式语言](er-formula-language.md)
- [NUMBERFORMAT 函数](er-functions-text-numberformat.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
