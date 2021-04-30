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
ms.openlocfilehash: 7790d7e581b9b4260a4c57af84b02a182dde953d
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894068"
---
# <a name="design-a-new-er-configuration-to-generate-reports-in-word-format"></a><span data-ttu-id="c4306-103">设计新 ER 配置以生成 Word 格式的报表</span><span class="sxs-lookup"><span data-stu-id="c4306-103">Design a new ER configuration to generate reports in Word format</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4306-104">以 Microsoft Word 文档形式生成报表，您必须使用 Word 桌面应用程序等为报表设计模板。</span><span class="sxs-lookup"><span data-stu-id="c4306-104">To generate reports as Microsoft Word documents, you must design a template for the reports by using, for example, the Word desktop application.</span></span> <span data-ttu-id="c4306-105">下图显示了控制报表的示例模板，生成后显示已处理供应商付款的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c4306-105">The following illustration shows the sample template for the control report that can be generated to show details of processed vendor payments.</span></span>

![Word 桌面应用程序中控制报表的示例模板](./media/er-design-configuration-word-image1.png)

<span data-ttu-id="c4306-107">要将 Word 文档用作 Word 格式的报表的模板，可以配置一个新的[电子报告 (ER)](general-electronic-reporting.md) [解决方案](er-quick-start1-new-solution.md)。</span><span class="sxs-lookup"><span data-stu-id="c4306-107">To use a Word document as a template for reports in Word format, you can configure a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="c4306-108">此解决方案必须包含一个包含 ER [格式](general-electronic-reporting.md#FormatComponentOutbound)组件的 ER [配置](general-electronic-reporting.md#Configuration)。</span><span class="sxs-lookup"><span data-stu-id="c4306-108">This solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span>

> [!NOTE]
> <span data-ttu-id="c4306-109">当您创建新 ER 格式配置以 Word 格式生成报表时，必须在 **创建配置** 下拉对话框中选择 **Word** 作为格式类型，或保留 **格式类型** 字段为空。</span><span class="sxs-lookup"><span data-stu-id="c4306-109">When you create a new ER format configuration to generate reports in Word format, you must either select **Word** as the format type in the **Create configuration** drop-down dialog box or leave the **Format type** field blank.</span></span>

![在“配置”页上创建格式配置](./media/er-design-configuration-word-image2.gif)

<span data-ttu-id="c4306-111">解决方案的 ER 格式组件必须包含 **Excel\\File** 格式元素，并且该格式元素必须链接到将在运行时用作所生成报表的模板的 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="c4306-111">The ER format component of the solution must contain the **Excel\\File** format element, and that format element must be linked to the Word document that will be used as the template for generated reports at runtime.</span></span> <span data-ttu-id="c4306-112">要配置 ER 格式组件，必须在 ER 格式设计器中打开已创建的 ER 配置的[草稿](general-electronic-reporting.md#component-versioning)版本。</span><span class="sxs-lookup"><span data-stu-id="c4306-112">To configure the ER format component, you must open the [draft](general-electronic-reporting.md#component-versioning) version of the created ER configuration in the ER format designer.</span></span> <span data-ttu-id="c4306-113">然后添加 **Excel\\File** 元素，将 Word 模板附加到可编辑 ER 格式，然后将该模板链接到添加的 **Excel\\File** 元素。</span><span class="sxs-lookup"><span data-stu-id="c4306-113">Then add the **Excel\\File** element, attach your Word template to the editable ER format, and link that template to the **Excel\\File** element that you added.</span></span>

> [!NOTE]
> <span data-ttu-id="c4306-114">在附加模板时，必须使用之前已在 ER 参数中[配置](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)的[文档类型](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types)来存储 ER 格式的模板。</span><span class="sxs-lookup"><span data-stu-id="c4306-114">When you attach a template, you must use a [document type](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types) that has previously been [configured](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

![在“格式设计器”页附加模板](./media/er-design-configuration-word-image3.gif)

<span data-ttu-id="c4306-116">您可以为 **Excel\\File** 元素添加 **Excel\\Range** 和 **Excel\\Cell** 嵌套元素，来指定运行时将在生成的报表中输入的数据结构。</span><span class="sxs-lookup"><span data-stu-id="c4306-116">You can add **Excel\\Range** and **Excel\\Cell** nested elements for the **Excel\\File** element to specify the structure of data that will be entered in generated reports at runtime.</span></span> <span data-ttu-id="c4306-117">然后，您必须将这些元素绑定到可编辑 ER 格式的数据源，来指定运行时将在生成的报表中输入的实际数据。</span><span class="sxs-lookup"><span data-stu-id="c4306-117">You must then bind those elements to data sources of the editable ER format to specify the actual data that will be entered in generated reports at runtime.</span></span>

![在“格式设计器”页添加嵌套元素](./media/er-design-configuration-word-image4.gif)

<span data-ttu-id="c4306-119">在设计期间保存对 ER 格式的更改时，分层格式结构将作为名为 **报表** 的[自定义 XML 部件](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019)存储在附加的 Word 模板中。</span><span class="sxs-lookup"><span data-stu-id="c4306-119">When you save your changes to the ER format at design time, the hierarchical format structure is stored in the attached Word template as a [custom XML part](/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) that is named **Report**.</span></span> <span data-ttu-id="c4306-120">您必须访问修改后的模板，从 Finance 中下载它，将它存储在本地，然后在 Word 桌面应用程序中打开它。</span><span class="sxs-lookup"><span data-stu-id="c4306-120">You must access the modified template, download it from Finance, store it locally, and open it in the Word desktop application.</span></span> <span data-ttu-id="c4306-121">下图显示了包含 **报表** 自定义 XML 部件的控制报表的本地存储的示例模板。</span><span class="sxs-lookup"><span data-stu-id="c4306-121">The following illustration shows the locally stored sample template for the control report that contains the **Report** custom XML part.</span></span>

![在 Word 桌面应用程序中预览示例报表模板](./media/er-design-configuration-word-image5.gif)

<span data-ttu-id="c4306-123">在运行时 **Excel\\Range** 和 **Excel\\Cell** 格式元素的绑定运行时，每个绑定提供的数据将作为 **报表** 自定义 XML 部件的单独字段进入生成的 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="c4306-123">When bindings of **Excel\\Range** and **Excel\\Cell** format elements are run at runtime, the data that every binding delivers comes into the generated Word document as an individual field of the **Report** custom XML part.</span></span> <span data-ttu-id="c4306-124">要在生成的文档中输入自定义 XML 部件的字段中的值，您必须将适当的 Word [内容控件](/office/client-developer/word/content-controls-in-word)添加到 Word 模板中，以在运行时用作将要填充的数据的占位符。</span><span class="sxs-lookup"><span data-stu-id="c4306-124">To enter the values from the fields of the custom XML part in a generated document, you must add the appropriate Word [content controls](/office/client-developer/word/content-controls-in-word) to your Word template to serve as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="c4306-125">要指定内容控件的填充方式，请将每个内容控件映射到 **报表** 自定义 XML 部件的相应字段。</span><span class="sxs-lookup"><span data-stu-id="c4306-125">To specify how content controls are filled in, map every content control to the appropriate field of the **Report** custom XML part.</span></span>

![在 Word 桌面应用程序中添加和映射内容控件](./media/er-design-configuration-word-image6.gif)

<span data-ttu-id="c4306-127">然后，您必须用修改后的模板替换可编辑 ER 格式的原始 Word 模板，修改后的模板现在包含映射到 **报表** 自定义 XML 部件的字段的 Word 内容控件。</span><span class="sxs-lookup"><span data-stu-id="c4306-127">You must then replace the original Word template of the editable ER format with the modified template that now contains Word content controls that were mapped to the fields of the **Report** custom XML part.</span></span>

![在“格式设计器”页替换模板](./media/er-design-configuration-word-image7.gif)

<span data-ttu-id="c4306-129">当您运行配置的 ER 格式时，附加的 Word 模板用于生成新报表。</span><span class="sxs-lookup"><span data-stu-id="c4306-129">When you run the configured ER format, the attached Word template is used to generate a new report.</span></span> <span data-ttu-id="c4306-130">实际数据作为名为 **报表** 的自定义 XML 部件存储在 Word 报表中。</span><span class="sxs-lookup"><span data-stu-id="c4306-130">The actual data is stored in the Word report as a custom XML part that is named **Report**.</span></span> <span data-ttu-id="c4306-131">打开生成的报表时，Word 内容控件中将填充来自 **报表** 自定义 XML 部件的数据。</span><span class="sxs-lookup"><span data-stu-id="c4306-131">When the generated report is opened, the Word content controls are filled in with data from the **Report** custom XML part.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="c4306-132">常见问题</span><span class="sxs-lookup"><span data-stu-id="c4306-132">Frequently asked questions</span></span>

<span data-ttu-id="c4306-133">**问题：** 我配置了 ER 格式来打印包含公司地址的 Word 文档。</span><span class="sxs-lookup"><span data-stu-id="c4306-133">**Question:** I configured an ER format to print a Word document that contains a company address.</span></span> <span data-ttu-id="c4306-134">在此 ER 格式的 Word 模板中，我插入了富文本内容控件来显示公司地址。</span><span class="sxs-lookup"><span data-stu-id="c4306-134">In the Word template for this ER format, I inserted a rich text content control to present a company address.</span></span> <span data-ttu-id="c4306-135">在 Finance 中，我使用多行文本输入了公司地址，然后选择 **Enter** 为我输入的每一行添加回车符。</span><span class="sxs-lookup"><span data-stu-id="c4306-135">In Finance, I entered the company address as multiline text and selected **Enter** to add a carriage return for every line that I entered.</span></span> <span data-ttu-id="c4306-136">所以，我预期公司地址在生成的文档中会显示为多行文本。</span><span class="sxs-lookup"><span data-stu-id="c4306-136">Therefore, I expect the company address to appear as multiline text in generated documents.</span></span> <span data-ttu-id="c4306-137">但是，地址显示为包含特殊符号而不是回车符的单行文本。</span><span class="sxs-lookup"><span data-stu-id="c4306-137">However, the address appears as a single line of text that contains special symbols instead of carriage returns.</span></span> <span data-ttu-id="c4306-138">我的设置有什么问题？</span><span class="sxs-lookup"><span data-stu-id="c4306-138">What is wrong with my settings?</span></span>

<span data-ttu-id="c4306-139">**回答：** 您必须使用纯文本内容控件，并选中控件属性中的 **允许回车符(多个段落)** 复选框，而不是使用富文本内容控件。</span><span class="sxs-lookup"><span data-stu-id="c4306-139">**Answer:** Instead of using a rich text content control, you must use a plain text content control and select the **Allow carriage returns (multiple paragraphs)** check box in the control's properties.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4306-140">其他资源</span><span class="sxs-lookup"><span data-stu-id="c4306-140">Additional resources</span></span>

- [<span data-ttu-id="c4306-141">重用带有 Excel 模板的 ER 配置以 Word 格式生成报表</span><span class="sxs-lookup"><span data-stu-id="c4306-141">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="c4306-142">使用 ER 在您生成的文档中嵌入图像和形状</span><span class="sxs-lookup"><span data-stu-id="c4306-142">Embed images and shapes in documents that you generate by using ER</span></span>](electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]