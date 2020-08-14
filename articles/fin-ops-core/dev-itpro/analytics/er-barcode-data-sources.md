---
title: 使用条码数据源生成条码图像
description: 本主题说明如何使用条码数据源生成条码图像。
author: NickSelin
manager: AnnBe
ms.date: 06/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.13
ms.openlocfilehash: fdb70c7e72647de4c6cd977b286c19c906559438
ms.sourcegitcommit: a56b22729fbbb941471e927e2f932acaf624cf5e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435457"
---
# <a name="use-barcode-data-sources-to-generate-bar-code-images"></a><span data-ttu-id="7c177-103">使用条码数据源生成条码图像</span><span class="sxs-lookup"><span data-stu-id="7c177-103">Use Barcode data sources to generate bar code images</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7c177-104">您可以使用[电子报告 (ER)](general-electronic-reporting.md) 框架来设计可以运行来生成所需的电子版和可打印传出文档的 [ER 格式组件](general-electronic-reporting.md#FormatComponentOutbound)。</span><span class="sxs-lookup"><span data-stu-id="7c177-104">You can use the [Electronic reporting (ER)](general-electronic-reporting.md) framework to design [ER format components](general-electronic-reporting.md#FormatComponentOutbound) that you can run to generate electronic and printable outbound documents that you require.</span></span> <span data-ttu-id="7c177-105">若要生成 Microsoft Office 格式的传出文档，必须使用 Microsoft Excel 文档或 Microsoft Word 文档作为报告模板来指定报告的布局。</span><span class="sxs-lookup"><span data-stu-id="7c177-105">To generate an outbound document in Microsoft Office format, you must specify the layout of the report by using either a Microsoft Excel document or a Microsoft Word document as a report template.</span></span> <span data-ttu-id="7c177-106">[ER 操作设计器](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base)使您可以将 Excel 或 Word 文档附加为 ER 格式的模板。</span><span class="sxs-lookup"><span data-stu-id="7c177-106">The [ER Operations designer](general-electronic-reporting.md#building-a-format-that-uses-a-data-model-as-a-base) lets you attach an Excel or Word document as a template for an ER format.</span></span> <span data-ttu-id="7c177-107">附加模板中的以下命名元素与配置的格式组件的元素相关联：</span><span class="sxs-lookup"><span data-stu-id="7c177-107">The following named elements in the attached template are associated with the elements of the configured format component:</span></span>

- <span data-ttu-id="7c177-108">Word 中的内容控件</span><span class="sxs-lookup"><span data-stu-id="7c177-108">Content controls in Word</span></span>
- <span data-ttu-id="7c177-109">Excel 中的命名工作表、范围、单元格、形状和图像</span><span class="sxs-lookup"><span data-stu-id="7c177-109">Named sheets, ranges, cells, shapes, and images in Excel</span></span>

<span data-ttu-id="7c177-110">这些命名元素用作运行 ER 格式时在生成的文档中输入的数据的占位符。</span><span class="sxs-lookup"><span data-stu-id="7c177-110">These named elements are used as placeholders for data that is entered in a generated document when an ER format is run.</span></span> <span data-ttu-id="7c177-111">ER 格式元素将绑定到数据源。</span><span class="sxs-lookup"><span data-stu-id="7c177-111">ER format elements are bound to data sources.</span></span> <span data-ttu-id="7c177-112">这些数据源指定在运行时将在生成的文档中输入的数据。</span><span class="sxs-lookup"><span data-stu-id="7c177-112">These data sources specify the data that will be entered in the generated documents at runtime.</span></span> <span data-ttu-id="7c177-113">有关详细信息，请参阅[使用 ER 在您生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)。</span><span class="sxs-lookup"><span data-stu-id="7c177-113">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

<span data-ttu-id="7c177-114">ER 现在支持**条码**数据源类型。</span><span class="sxs-lookup"><span data-stu-id="7c177-114">ER now supports the **Barcode** data source type.</span></span> <span data-ttu-id="7c177-115">因此，您现在可以生成一个代表指定文本的条码的图像。</span><span class="sxs-lookup"><span data-stu-id="7c177-115">Therefore, you can now generate an image that represents the bar code for specified text.</span></span> <span data-ttu-id="7c177-116">配置 ER 格式时，可以指定**条码**类型的数据源来生成条码图像。</span><span class="sxs-lookup"><span data-stu-id="7c177-116">When you configure an ER format, you can specify data sources of the **Barcode** type to generate bar code images.</span></span> <span data-ttu-id="7c177-117">然后，您可以将这些图像添加到生成的业务文档中，如订单、发票、装箱单和收据。</span><span class="sxs-lookup"><span data-stu-id="7c177-117">You can then add those images to generated business documents, such as orders, invoices, packing slips, and receipts.</span></span> <span data-ttu-id="7c177-118">您还可以将它们添加到各种标签中，如产品和货位标签以及包装和发货标签。</span><span class="sxs-lookup"><span data-stu-id="7c177-118">You can also add them to various kind of labels, such as product and shelf labels, and packaging and shipping labels.</span></span>

<span data-ttu-id="7c177-119">报告模板中可以使用以下占位符来输入条码图像：</span><span class="sxs-lookup"><span data-stu-id="7c177-119">The following placeholders can be used in report templates to enter bar code images:</span></span>

- <span data-ttu-id="7c177-120">Word 的[图片](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word)内容控件</span><span class="sxs-lookup"><span data-stu-id="7c177-120">[Picture](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) content control for Word</span></span>
- <span data-ttu-id="7c177-121">Excel 中的[图片](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344)对象</span><span class="sxs-lookup"><span data-stu-id="7c177-121">[Picture](https://support.office.com/article/insert-pictures-3c51edf4-22e1-460a-b372-9329a8724344) object in Excel</span></span>

<span data-ttu-id="7c177-122">通过使用**条码**类型的数据源，您可以生成以下格式的条码：</span><span class="sxs-lookup"><span data-stu-id="7c177-122">By using a data source of the **Barcode** type, you can generate bar codes in the following formats:</span></span>

- <span data-ttu-id="7c177-123">一维条码：</span><span class="sxs-lookup"><span data-stu-id="7c177-123">One-dimensional bar codes:</span></span>

    - <span data-ttu-id="7c177-124">Codabar</span><span class="sxs-lookup"><span data-stu-id="7c177-124">Codabar</span></span>
    - <span data-ttu-id="7c177-125">Code 39</span><span class="sxs-lookup"><span data-stu-id="7c177-125">Code 39</span></span>
    - <span data-ttu-id="7c177-126">Code 93</span><span class="sxs-lookup"><span data-stu-id="7c177-126">Code 93</span></span>
    - <span data-ttu-id="7c177-127">Code 128</span><span class="sxs-lookup"><span data-stu-id="7c177-127">Code 128</span></span>
    - <span data-ttu-id="7c177-128">EAN-8</span><span class="sxs-lookup"><span data-stu-id="7c177-128">EAN-8</span></span>
    - <span data-ttu-id="7c177-129">EAN-13</span><span class="sxs-lookup"><span data-stu-id="7c177-129">EAN-13</span></span>
    - <span data-ttu-id="7c177-130">ITF-14</span><span class="sxs-lookup"><span data-stu-id="7c177-130">ITF-14</span></span>
    - <span data-ttu-id="7c177-131">PDF417</span><span class="sxs-lookup"><span data-stu-id="7c177-131">PDF417</span></span>
    - <span data-ttu-id="7c177-132">UPC-A</span><span class="sxs-lookup"><span data-stu-id="7c177-132">UPC-A</span></span>
    - <span data-ttu-id="7c177-133">UPC-E</span><span class="sxs-lookup"><span data-stu-id="7c177-133">UPC-E</span></span>
    - <span data-ttu-id="7c177-134">MSI</span><span class="sxs-lookup"><span data-stu-id="7c177-134">MSI</span></span>
    - <span data-ttu-id="7c177-135">Plessey</span><span class="sxs-lookup"><span data-stu-id="7c177-135">Plessey</span></span>

- <span data-ttu-id="7c177-136">二维条码：</span><span class="sxs-lookup"><span data-stu-id="7c177-136">Two-dimensional bar codes:</span></span>

    - <span data-ttu-id="7c177-137">Aztec</span><span class="sxs-lookup"><span data-stu-id="7c177-137">Aztec</span></span>
    - <span data-ttu-id="7c177-138">DataMatrix</span><span class="sxs-lookup"><span data-stu-id="7c177-138">DataMatrix</span></span>
    - <span data-ttu-id="7c177-139">QR 码</span><span class="sxs-lookup"><span data-stu-id="7c177-139">QR Code</span></span>

<span data-ttu-id="7c177-140">当您配置**条码**数据源时，您可以定义用于生成图像的特定绘制参数：</span><span class="sxs-lookup"><span data-stu-id="7c177-140">When you configure a **Barcode** data source, you can define specific rendering parameters that are used to generate an image:</span></span>

- <span data-ttu-id="7c177-141">**宽度** – 以像素为单位指定条码的宽度。</span><span class="sxs-lookup"><span data-stu-id="7c177-141">**Width** – Specify the bar code's width in pixels.</span></span> <span data-ttu-id="7c177-142">值 **0**（零）指示使用默认宽度。</span><span class="sxs-lookup"><span data-stu-id="7c177-142">A value of **0** (zero) indicates that the default width is used.</span></span> <span data-ttu-id="7c177-143">对于不同的格式，含义可能有所不同。</span><span class="sxs-lookup"><span data-stu-id="7c177-143">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="7c177-144">**高度** – 以像素为单位指定条码的高度。</span><span class="sxs-lookup"><span data-stu-id="7c177-144">**Height** – Specify the bar code's height in pixels.</span></span> <span data-ttu-id="7c177-145">值 **0**（零）指示使用默认高度。</span><span class="sxs-lookup"><span data-stu-id="7c177-145">A value of **0** (zero) indicates that the default height is used.</span></span> <span data-ttu-id="7c177-146">对于不同的格式，含义可能有所不同。</span><span class="sxs-lookup"><span data-stu-id="7c177-146">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="7c177-147">**边距** – 以像素为单位指定条码边距的大小。</span><span class="sxs-lookup"><span data-stu-id="7c177-147">**Margin** – Specify the size of the bar code's margin in pixels.</span></span> <span data-ttu-id="7c177-148">边距是条码两侧必须留出的区域（静区）。</span><span class="sxs-lookup"><span data-stu-id="7c177-148">The margin is the area on each side of a bar code that must be kept clear (quiet zone).</span></span> <span data-ttu-id="7c177-149">值 **0**（零）指示使用默认边距。</span><span class="sxs-lookup"><span data-stu-id="7c177-149">A value of **0** (zero) indicates that the default margin is used.</span></span> <span data-ttu-id="7c177-150">对于不同的格式，含义可能有所不同。</span><span class="sxs-lookup"><span data-stu-id="7c177-150">The meaning can vary for different formats.</span></span>
- <span data-ttu-id="7c177-151">**输出内容** – 将值设置为**是**将生成包含编码信息作为文本的条码图像。</span><span class="sxs-lookup"><span data-stu-id="7c177-151">**Output content** – Set the value to **Yes** to generate a bar code image that contains the encoded information as text.</span></span> <span data-ttu-id="7c177-152">默认值为**否**。</span><span class="sxs-lookup"><span data-stu-id="7c177-152">The default value is **No**.</span></span>
- <span data-ttu-id="7c177-153">**编码** – 指定在生成的条码图像中编码的字符的类型。</span><span class="sxs-lookup"><span data-stu-id="7c177-153">**Encoding** – Specify the type of characters that are encoded in the generated bar code image.</span></span> <span data-ttu-id="7c177-154">默认情况下，使用 **UTF-8** 编码。</span><span class="sxs-lookup"><span data-stu-id="7c177-154">By default, the **UTF-8** encoding is used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c177-155">当您添加新的**条码**数据源时，必须将其作为嵌套元素放在另一个项目（容器）下。</span><span class="sxs-lookup"><span data-stu-id="7c177-155">When you add a new **Barcode** data source, you must place it under another item (container) as a nested element.</span></span>
>
> <span data-ttu-id="7c177-156">当您将**条码**数据源以某种格式绑定到单元格元素，并且该单元格元素表示 Word 内容控件或 Excel 图片时，数据源在该绑定中显示为具有单个**字符串**类型参数的函数。</span><span class="sxs-lookup"><span data-stu-id="7c177-156">When you bind a **Barcode** data source to a cell element in a format, and the cell element represents either a Word content control or an Excel picture, the data source is presented in that binding as a function that has a single parameter of the **String** type.</span></span> <span data-ttu-id="7c177-157">您必须使用此参数来指定应转换为条码图像并在扫描生成的条码时读取的文本。</span><span class="sxs-lookup"><span data-stu-id="7c177-157">You must use this parameter to specify the text that should be transformed into a bar code image and read when a generated bar code is scanned.</span></span>

<span data-ttu-id="7c177-158">有关此功能的详细信息，请完成本主题中的示例。</span><span class="sxs-lookup"><span data-stu-id="7c177-158">For more information about this feature, complete the examples in this topic.</span></span>

## <a name="example-generate-a-payment-check-that-contains-a-bar-code-that-encodes-the-payable-amount"></a><span data-ttu-id="7c177-159">示例：生成包含对应付金额进行编码的条码的付款支票</span><span class="sxs-lookup"><span data-stu-id="7c177-159">Example: Generate a payment check that contains a bar code that encodes the payable amount</span></span>

<span data-ttu-id="7c177-160">本示例说明具有**系统管理员**或**电子报告功能顾问**角色的用户如何配置 ER 格式，该格式包含用于生成包含条码的 Excel 格式传出文档的模板。</span><span class="sxs-lookup"><span data-stu-id="7c177-160">This example shows how a user in the **System administrator** or **Electronic reporting functional consultant** role can configure an ER format that contains a template that is used to generate an outbound document in Excel format that contains a bar code.</span></span> <span data-ttu-id="7c177-161">这里是所涉及步骤的概览。</span><span class="sxs-lookup"><span data-stu-id="7c177-161">Here is an overview of the steps that are involved.</span></span>

1. <span data-ttu-id="7c177-162">[完成先决条件](#ExamplePrerequisites)。</span><span class="sxs-lookup"><span data-stu-id="7c177-162">[Complete the prerequisites](#ExamplePrerequisites).</span></span>
2. <span data-ttu-id="7c177-163">[激活配置提供程序](#ExampleProvider)。</span><span class="sxs-lookup"><span data-stu-id="7c177-163">[Activate a configuration provider](#ExampleProvider).</span></span>
3. <span data-ttu-id="7c177-164">[导入提供的 ER 解决方案](#ExampleImportSolution)。</span><span class="sxs-lookup"><span data-stu-id="7c177-164">[Import the provided ER solution](#ExampleImportSolution).</span></span>
4. <span data-ttu-id="7c177-165">[生成付款支票](#ExampleGenerateCheque)。</span><span class="sxs-lookup"><span data-stu-id="7c177-165">[Generate a payment check](#ExampleGenerateCheque).</span></span>
5. <span data-ttu-id="7c177-166">[查看生成的付款支票](#ExampleReviewGeneratedCheque)。</span><span class="sxs-lookup"><span data-stu-id="7c177-166">[Review the generated payment check](#ExampleReviewGeneratedCheque).</span></span>
6. <span data-ttu-id="7c177-167">[修改提供的 ER 解决方案的格式](#ExampleModifyFormat)。</span><span class="sxs-lookup"><span data-stu-id="7c177-167">[Modify the format of the provided ER solution](#ExampleModifyFormat).</span></span>

    1. <span data-ttu-id="7c177-168">[应用新支票模板](#ExampleModifyFormatApplyTemplate)。</span><span class="sxs-lookup"><span data-stu-id="7c177-168">[Apply a new check template](#ExampleModifyFormatApplyTemplate).</span></span>
    2. <span data-ttu-id="7c177-169">[添加新条码数据源](#ExampleModifyFormatAddDataSource)。</span><span class="sxs-lookup"><span data-stu-id="7c177-169">[Add a new Barcode data source](#ExampleModifyFormatAddDataSource).</span></span>
    3. <span data-ttu-id="7c177-170">[绑定新格式元素](#ExampleModifyFormatBindFormatElement)。</span><span class="sxs-lookup"><span data-stu-id="7c177-170">[Bind a new format element](#ExampleModifyFormatBindFormatElement).</span></span>
    4. <span data-ttu-id="7c177-171">[使修改后的版本可用于测试运行](#ExampleModifyFormatMakeVersionAvailable)。</span><span class="sxs-lookup"><span data-stu-id="7c177-171">[Make the modified version available for test runs](#ExampleModifyFormatMakeVersionAvailable).</span></span>

        1. <span data-ttu-id="7c177-172">[完成修改后的格式版本](#CompleteToRun)。</span><span class="sxs-lookup"><span data-stu-id="7c177-172">[Complete the modified format version](#CompleteToRun).</span></span>
        2. <span data-ttu-id="7c177-173">[使草稿版本可供使用](#MarkToRun)。</span><span class="sxs-lookup"><span data-stu-id="7c177-173">[Make the draft version available for use](#MarkToRun).</span></span>

7. <span data-ttu-id="7c177-174">[生成付款支票](#ExampleGenerateCheque2)。</span><span class="sxs-lookup"><span data-stu-id="7c177-174">[Generate a payment check](#ExampleGenerateCheque2).</span></span>
8. <span data-ttu-id="7c177-175">[将生成的支票转换为 PDF](#ExampleConvertToPDF)。</span><span class="sxs-lookup"><span data-stu-id="7c177-175">[Convert the generated check to a PDF](#ExampleConvertToPDF).</span></span>

<span data-ttu-id="7c177-176">在此示例中，您将使用已配置为生成付款支票的提供的 ER 解决方案。</span><span class="sxs-lookup"><span data-stu-id="7c177-176">In this example, you will use the provided ER solution that has been configured to generate payment checks.</span></span> <span data-ttu-id="7c177-177">此解决方案生成应付金额同时以数字和文本形式书写的付款支票。</span><span class="sxs-lookup"><span data-stu-id="7c177-177">This solution generates payment checks where the payable amount is written both as a number and as text.</span></span> <span data-ttu-id="7c177-178">您将修改此 ER 解决方案，使支票还包括对应付金额进行编码的生成的条码，该条码可以使用条码扫描仪进行读取。</span><span class="sxs-lookup"><span data-stu-id="7c177-178">You will modify this ER solution so that the check also includes a generated bar code where the payable amount is encoded and can be read by using a bar code scanner.</span></span>

<span data-ttu-id="7c177-179">这些步骤可以在 Microsoft Dynamics 365 Finance 中在 **USMF** 公司中完成。</span><span class="sxs-lookup"><span data-stu-id="7c177-179">The steps can be completed in the **USMF** company in Microsoft Dynamics 365 Finance.</span></span>

### <a name="complete-the-prerequisites"></a><a name="ExamplePrerequisites"></a><span data-ttu-id="7c177-180">完成先决条件</span><span class="sxs-lookup"><span data-stu-id="7c177-180">Complete the prerequisites</span></span>

<span data-ttu-id="7c177-181">若要完成本示例，您必须能够用以下角色之一访问 USMF 公司的 Finance：</span><span class="sxs-lookup"><span data-stu-id="7c177-181">To complete this example, you must have access to the USMF company in Finance for one of the following roles:</span></span>

- <span data-ttu-id="7c177-182">电子申报功能顾问</span><span class="sxs-lookup"><span data-stu-id="7c177-182">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="7c177-183">系统管理员</span><span class="sxs-lookup"><span data-stu-id="7c177-183">System administrator</span></span>

<span data-ttu-id="7c177-184">如果您尚未完成[使用 ER 在您生成的文档中嵌入图像和形状](electronic-reporting-embed-images-shapes.md)主题中的示例，请下载示例 ER 解决方案的以下配置。</span><span class="sxs-lookup"><span data-stu-id="7c177-184">If you haven't yet completed the example in the [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md) topic, download the following configurations of the sample ER solution.</span></span>

| <span data-ttu-id="7c177-185">内容描述</span><span class="sxs-lookup"><span data-stu-id="7c177-185">Content description</span></span>         | <span data-ttu-id="7c177-186">文件名</span><span class="sxs-lookup"><span data-stu-id="7c177-186">File name</span></span>                   |
|-----------------------------|-----------------------------|
| <span data-ttu-id="7c177-187">ER 数据模型配置</span><span class="sxs-lookup"><span data-stu-id="7c177-187">ER data model configuration</span></span> | <span data-ttu-id="7c177-188">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="7c177-188">Model for cheques.xml</span></span>       |
| <span data-ttu-id="7c177-189">ER 格式配置</span><span class="sxs-lookup"><span data-stu-id="7c177-189">ER format configuration</span></span>     | <span data-ttu-id="7c177-190">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="7c177-190">Cheques printing format.xml</span></span> |

<span data-ttu-id="7c177-191">此外，下载以下 Excel 文件，其中包含所提供的 ER 解决方案的修改后的模板。</span><span class="sxs-lookup"><span data-stu-id="7c177-191">Additionally, download the following Excel file that contains the modified template for the provided ER solution.</span></span>

| <span data-ttu-id="7c177-192">内容描述</span><span class="sxs-lookup"><span data-stu-id="7c177-192">Content description</span></span> | <span data-ttu-id="7c177-193">文件名</span><span class="sxs-lookup"><span data-stu-id="7c177-193">File name</span></span>                 |
|---------------------|---------------------------|
| <span data-ttu-id="7c177-194">报告模板</span><span class="sxs-lookup"><span data-stu-id="7c177-194">Report template</span></span>     | <span data-ttu-id="7c177-195">Check template Excel.xlsx</span><span class="sxs-lookup"><span data-stu-id="7c177-195">Check template Excel.xlsx</span></span> |

### <a name="activate-a-configuration-provider"></a><a name="ExampleProvider"></a><span data-ttu-id="7c177-196">激活配置提供程序</span><span class="sxs-lookup"><span data-stu-id="7c177-196">Activate a configuration provider</span></span>

1. <span data-ttu-id="7c177-197">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="7c177-197">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7c177-198">在**本地化配置**页上的**配置提供程序**部分中，确保列出了示例公司 **Litware, Inc.** 的[配置提供程序](general-electronic-reporting.md#Provider)，并将其标记为活动状态。</span><span class="sxs-lookup"><span data-stu-id="7c177-198">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the [configuration provider](general-electronic-reporting.md#Provider) for the **Litware, Inc.** sample company is listed, and that it's marked as active.</span></span> <span data-ttu-id="7c177-199">如果未列出，或者未将其标记为活动状态，请按照[创建一个配置提供程序，并标记其为活动状态](tasks/er-configuration-provider-mark-it-active-2016-11.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="7c177-199">If it isn't listed, or if it isn't marked as active, follow the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic.</span></span>

![在“本地化配置”页面上将示例公司设置为活动状态](./media/er-barcode-data-source-active-provider.png)

### <a name="import-the-provided-er-solution"></a><a name="ExampleImportSolution"></a><span data-ttu-id="7c177-201">导入提供的 ER 解决方案</span><span class="sxs-lookup"><span data-stu-id="7c177-201">Import the provided ER solution</span></span>

1. <span data-ttu-id="7c177-202">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="7c177-202">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7c177-203">在**本地化配置**页面的**配置**部分中，选择**报告配置**磁贴。</span><span class="sxs-lookup"><span data-stu-id="7c177-203">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="7c177-204">在**配置**页面上，如果**支票的模型**配置在配置树中不可用，请按照以下步骤导入 ER 数据模型配置：</span><span class="sxs-lookup"><span data-stu-id="7c177-204">On the **Configurations** page, if the **Model for cheques** configuration isn't available in the configuration tree, follow these steps to import the ER data model configuration:</span></span>

    1. <span data-ttu-id="7c177-205">在操作窗格上，选择**交换** \> **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="7c177-205">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="7c177-206">在对话框中，选择**浏览**，找到并选择 **Model for cheques.xml** 文件，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c177-206">In the dialog box, select **Browse**, find and select the **Model for cheques.xml** file, and then select **OK**.</span></span>

4. <span data-ttu-id="7c177-207">如果**支票打印格式**配置在配置树中不可用，请按照以下步骤导入 ER 格式配置：</span><span class="sxs-lookup"><span data-stu-id="7c177-207">If the **Cheques printing format** configuration isn't available in the configuration tree, follow these steps to import the ER format configuration:</span></span>

    1. <span data-ttu-id="7c177-208">在操作窗格上，选择**交换** \> **从 XML 文件加载**。</span><span class="sxs-lookup"><span data-stu-id="7c177-208">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="7c177-209">在对话框中，选择**浏览**，找到并选择 **Cheques printing format.xml** 文件，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c177-209">In the dialog box, select **Browse**, find and select the **Cheques printing format.xml** file, and then select **OK**.</span></span>

5. <span data-ttu-id="7c177-210">在配置树中，展开**支票的模型**。</span><span class="sxs-lookup"><span data-stu-id="7c177-210">In the configuration tree, expand **Model for cheques**.</span></span>
6. <span data-ttu-id="7c177-211">在配置树中查看导入的 ER 配置的列表。</span><span class="sxs-lookup"><span data-stu-id="7c177-211">Review the list of imported ER configurations in the configuration tree.</span></span>

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque"></a><span data-ttu-id="7c177-212">生成付款支票</span><span class="sxs-lookup"><span data-stu-id="7c177-212">Generate a payment check</span></span>

1. <span data-ttu-id="7c177-213">转到**现金和银行管理** \> **银行账户** \> **银行账户**。</span><span class="sxs-lookup"><span data-stu-id="7c177-213">Go to **Cash and bank management** \> **Bank accounts** \> **Bank accounts**.</span></span>
2. <span data-ttu-id="7c177-214">在**银行账户**页面上，选择 **USMF OPER** 账户。</span><span class="sxs-lookup"><span data-stu-id="7c177-214">On the **Bank accounts** page, select the **USMF OPER** account.</span></span>
3. <span data-ttu-id="7c177-215">在银行账户详细信息页的操作窗格中，在**设置**选项卡的**布局**组中，选择**支票**。</span><span class="sxs-lookup"><span data-stu-id="7c177-215">On the bank account details page, on the Action Pane, on the **Set up** tab, in the **Layout** group, select **Check**.</span></span>
4. <span data-ttu-id="7c177-216">在**支票版式**页面上，选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="7c177-216">On the **Check layout** page, select **Edit**.</span></span>
5. <span data-ttu-id="7c177-217">在**常规**快速选项卡上，将**一般电子导出格式**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="7c177-217">On the **General** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
6. <span data-ttu-id="7c177-218">在**导出格式配置**字段中，选择您先前导入的**支票打印格式** ER 格式。</span><span class="sxs-lookup"><span data-stu-id="7c177-218">In the **Export format configuration** field, select the **Cheques printing format** ER format that you imported earlier.</span></span>
7. <span data-ttu-id="7c177-219">在操作窗格上，选择**打印测试**。</span><span class="sxs-lookup"><span data-stu-id="7c177-219">On the Action Pane, select **Print test**.</span></span>
8. <span data-ttu-id="7c177-220">在对话框中，将**可转让支票格式**选项设置为**是**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c177-220">In the dialog box, set the **Negotiable check format** option to **Yes**, and then select **OK**.</span></span>

    ![支票版式 - 打印测试对话框](./media/er-barcode-data-source-check-layout.png)

### <a name="review-the-generated-payment-check"></a><a name="ExampleReviewGeneratedCheque"></a><span data-ttu-id="7c177-222">查看生成的付款支票</span><span class="sxs-lookup"><span data-stu-id="7c177-222">Review the generated payment check</span></span>

- <span data-ttu-id="7c177-223">在 Excel 中打开生成的支票。</span><span class="sxs-lookup"><span data-stu-id="7c177-223">Open the generated check in Excel.</span></span>
2. <span data-ttu-id="7c177-224">检查生成的支票。</span><span class="sxs-lookup"><span data-stu-id="7c177-224">Review the generated check.</span></span>

    ![在 Excel 中生成的付款支票](./media/er-barcode-data-source-cheque1.png)

### <a name="modify-the-format-of-the-provided-er-solution"></a><a name="ExampleModifyFormat"></a><span data-ttu-id="7c177-226">修改提供的 ER 解决方案的格式</span><span class="sxs-lookup"><span data-stu-id="7c177-226">Modify the format of the provided ER solution</span></span>

#### <a name="apply-a-new-check-template"></a><a name="ExampleModifyFormatApplyTemplate"></a><span data-ttu-id="7c177-227">应用新支票模板</span><span class="sxs-lookup"><span data-stu-id="7c177-227">Apply a new check template</span></span>

<span data-ttu-id="7c177-228">您可以使用 Excel 桌面应用程序打开您先前导入的 **Cheque template Excel.xlsx** 文件。</span><span class="sxs-lookup"><span data-stu-id="7c177-228">You can use the Excel desktop application to open the **Cheque template Excel.xlsx** file that you imported earlier.</span></span> <span data-ttu-id="7c177-229">请注意，此模板与您在提供的 ER 解决方案中用于生成付款支票的模板不同。</span><span class="sxs-lookup"><span data-stu-id="7c177-229">Notice that this template differs from the template that you used to generate a payment check in the provided ER solution.</span></span> <span data-ttu-id="7c177-230">此外，它还包括条码图像的 **AmountBarcode** 元素。</span><span class="sxs-lookup"><span data-stu-id="7c177-230">In addition, it includes an **AmountBarcode** element for the bar code image.</span></span>

![Excel 模板中的 AmountBarcode 元素](./media/er-barcode-data-source-cheque2.png)

<span data-ttu-id="7c177-232">您现在必须修改 ER 解决方案，然后[重新应用](modify-electronic-reporting-format-reapply-excel-template.md)修改后的模板。</span><span class="sxs-lookup"><span data-stu-id="7c177-232">You must now modify the ER solution and then [reapply](modify-electronic-reporting-format-reapply-excel-template.md) the modified template.</span></span>

1. <span data-ttu-id="7c177-233">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="7c177-233">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7c177-234">在**本地化配置**页面的**配置**部分中，选择**报告配置**。</span><span class="sxs-lookup"><span data-stu-id="7c177-234">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7c177-235">在**配置**页面，在配置树中，展开**支票的模型**，然后选择**支票打印格式**。</span><span class="sxs-lookup"><span data-stu-id="7c177-235">On the **Configurations** page, in the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
4. <span data-ttu-id="7c177-236">在操作窗格上，选择**设计器**。</span><span class="sxs-lookup"><span data-stu-id="7c177-236">On the Action Pane, select **Designer**.</span></span>
5. <span data-ttu-id="7c177-237">在 ER 操作设计器中，选择页面右侧的**映射**选项卡，然后在左侧的格式树窗格中，选择**展开/折叠**。</span><span class="sxs-lookup"><span data-stu-id="7c177-237">In the ER Operations designer, select the **Mapping** tab on the right side of the page, and then, in the format tree pane on the left, select **Expand/collapse**.</span></span>
6. <span data-ttu-id="7c177-238">请注意，所有单元格格式元素都绑定到适当的数据源。</span><span class="sxs-lookup"><span data-stu-id="7c177-238">Notice that all cell format elements are bound to the appropriate data sources.</span></span>

    ![在 ER 操作设计器中将单元格格式元素绑定到数据源](./media/er-barcode-data-source-cells-bound.png)

7. <span data-ttu-id="7c177-240">选择页面右侧的**格式**选项卡。</span><span class="sxs-lookup"><span data-stu-id="7c177-240">Select the **Format** tab on the right side of the page.</span></span>
8. <span data-ttu-id="7c177-241">在操作窗格上，选择省略号 (**...**)，然后选择**导入**。</span><span class="sxs-lookup"><span data-stu-id="7c177-241">On the Action Pane, select the ellipsis (**...**), and then select **Import**.</span></span>
9. <span data-ttu-id="7c177-242">在**导入**组中，选择**从 Excel 更新**，然后选择**更新模板**。</span><span class="sxs-lookup"><span data-stu-id="7c177-242">In the **Import** group, select **Update from Excel**, and then select **Update template**.</span></span>
10. <span data-ttu-id="7c177-243">在对话框中，浏览到保存在计算机上的 **Cheque template Excel.xlsx** 文件，选择它，然后选择**确定**确认应该应用所选模板。</span><span class="sxs-lookup"><span data-stu-id="7c177-243">In the dialog box, browse to the **Cheque template Excel.xlsx** file that is saved on your computer, select it, and then select **OK** to confirm that the selected template should be applied.</span></span>
11. <span data-ttu-id="7c177-244">选择页面右侧的**映射**选项卡，然后在左侧的格式树窗格中，选择**展开/折叠**。</span><span class="sxs-lookup"><span data-stu-id="7c177-244">Select the **Mapping** tab on the right side of the page, and then, in the format tree pane on the left, select **Expand/collapse**.</span></span>
12. <span data-ttu-id="7c177-245">请注意，**AmountBarcode** 单元格元素已添加到格式。</span><span class="sxs-lookup"><span data-stu-id="7c177-245">Notice that the **AmountBarcode** cell element has been added to the format.</span></span> <span data-ttu-id="7c177-246">此元素与 **AmountBarcode** 元素相关联，后者已作为条码图像的占位符添加到修改后的 Excel 模板中。</span><span class="sxs-lookup"><span data-stu-id="7c177-246">This element is associated with the **AmountBarcode** element that has been added to the modified Excel template as a placeholder for a bar code image.</span></span>

    ![在 ER 操作设计器中添加到格式中的 AmountBarcode 单元格元素](./media/er-barcode-data-source-cell-added.png)

#### <a name="add-a-new-barcode-data-source"></a><a name="ExampleModifyFormatAddDataSource"></a><span data-ttu-id="7c177-248">添加新条码数据源</span><span class="sxs-lookup"><span data-stu-id="7c177-248">Add a new Barcode data source</span></span>

<span data-ttu-id="7c177-249">接下来，您必须添加**条码**类型的新数据源。</span><span class="sxs-lookup"><span data-stu-id="7c177-249">Next, you must add a new data source of the **Barcode** type.</span></span>

1. <span data-ttu-id="7c177-250">在 ER 操作设计器中，在页面右侧的**映射**选项卡上，选择**打印**数据源。</span><span class="sxs-lookup"><span data-stu-id="7c177-250">In the ER Operations designer, on the **Mapping** tab on the right side of the page, select the **print** data source.</span></span>
2. <span data-ttu-id="7c177-251">选择**添加**，然后在**函数**组中，选择**条码**数据源类型。</span><span class="sxs-lookup"><span data-stu-id="7c177-251">Select **Add**, and then, in the **Functions** group, select the **Barcode** data source type.</span></span>

    ![选择条码数据源类型](./media/er-barcode-data-source-add.png)

3. <span data-ttu-id="7c177-253">在对话框的**名称**字段中，输入**条码**。</span><span class="sxs-lookup"><span data-stu-id="7c177-253">In the dialog box, in the **Name** field, enter **barcode**.</span></span>
4. <span data-ttu-id="7c177-254">在**条码格式**中，选择 **Code 128**。</span><span class="sxs-lookup"><span data-stu-id="7c177-254">In the **Barcode format**, select **Code 128**.</span></span>
5. <span data-ttu-id="7c177-255">在**宽度**字段中，输入 **500**。</span><span class="sxs-lookup"><span data-stu-id="7c177-255">In the **Width** field, enter **500**.</span></span>
6. <span data-ttu-id="7c177-256">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c177-256">Select **OK**.</span></span>

    ![数据源属性对话框](./media/er-barcode-data-source-add2.png)

#### <a name="bind-a-new-format-element"></a><a name="ExampleModifyFormatBindFormatElement"></a><span data-ttu-id="7c177-258">绑定新格式元素</span><span class="sxs-lookup"><span data-stu-id="7c177-258">Bind a new format element</span></span>

<span data-ttu-id="7c177-259">接下来，必须将新的格式元素绑定到刚才添加的数据源。</span><span class="sxs-lookup"><span data-stu-id="7c177-259">Next, you must bind the new format element to the data source that you just added.</span></span>

1. <span data-ttu-id="7c177-260">在 ER 操作设计器中，在页面右侧的**映射**选项卡上，选择**打印\\条码**数据源。</span><span class="sxs-lookup"><span data-stu-id="7c177-260">In the ER Operations designer, on the **Mapping** tab on the right side of the page, select the **print\\barcode** data source.</span></span>
2. <span data-ttu-id="7c177-261">在左侧的格式树窗格中，选择 **AmountBarcode** 单元格元素，然后选择**绑定**。</span><span class="sxs-lookup"><span data-stu-id="7c177-261">In the format tree pane on the left, select the **AmountBarcode** cell element, and then select **Bind**.</span></span>
3. <span data-ttu-id="7c177-262">在操作窗格上，选择**显示详细信息**。</span><span class="sxs-lookup"><span data-stu-id="7c177-262">On the Action Pane, select **Show details**.</span></span>
4. <span data-ttu-id="7c177-263">请注意，由于**条码**数据源在绑定中表示为包含单个参数的函数，绑定格式元素的名称已自动提取为该参数的参数。</span><span class="sxs-lookup"><span data-stu-id="7c177-263">Notice that, because the **Barcode** data source is represented in the binding as a function that contains a single parameter, the name of the bound format element has been automatically taken as the argument of that parameter.</span></span>

    ![ER 操作设计器中条码数据源的详细信息](./media/er-barcode-data-source-bind1.png)

5. <span data-ttu-id="7c177-265">选择**编辑公式**调整绑定。</span><span class="sxs-lookup"><span data-stu-id="7c177-265">Select **Edit formula** to adjust the binding.</span></span>

    <span data-ttu-id="7c177-266">您不希望返回单元格元素的名称。</span><span class="sxs-lookup"><span data-stu-id="7c177-266">You don't want the name of the cell element to be returned.</span></span> <span data-ttu-id="7c177-267">因此，您必须配置一个返回包含当前支票的应付金额的文本的表达式。</span><span class="sxs-lookup"><span data-stu-id="7c177-267">Therefore, you must configure an expression that returns text that contains the payable amount of the current check.</span></span> <span data-ttu-id="7c177-268">由于父 **ChequeLines** 范围绑定到 **model.cheques** 数据源，因此当前支票的应付金额可在**实数**数据类型的 **model.cheques.attributes.amount** 字段中找到。</span><span class="sxs-lookup"><span data-stu-id="7c177-268">Because the parent **ChequeLines** range is bound to the **model.cheques** data source, the payable amount of the current check is available in the **model.cheques.attributes.amount** field of the **Real** data type.</span></span>

6. <span data-ttu-id="7c177-269">在**公式**字段中，输入 **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**。</span><span class="sxs-lookup"><span data-stu-id="7c177-269">In the **Formula** field, enter **print.barcode(NUMBERFORMAT(@.attributes.amount, "F2"))**.</span></span>
7. <span data-ttu-id="7c177-270">选择**保存**，然后关闭 [ER 公式设计器](general-electronic-reporting-formula-designer.md)。</span><span class="sxs-lookup"><span data-stu-id="7c177-270">Select **Save**, and then close the [ER Formula designer](general-electronic-reporting-formula-designer.md).</span></span>
8. <span data-ttu-id="7c177-271">请注意，绑定已调整。</span><span class="sxs-lookup"><span data-stu-id="7c177-271">Notice that the binding has been adjusted.</span></span>

    ![在 ER 操作设计器中调整的绑定](./media/er-barcode-data-source-bind2.png)

9. <span data-ttu-id="7c177-273">选择**保存**，然后关闭 ER 操作设计器。</span><span class="sxs-lookup"><span data-stu-id="7c177-273">Select **Save**, and then close the ER Operations designer.</span></span>

#### <a name="make-the-modified-version-available-for-test-runs"></a><a name="ExampleModifyFormatMakeVersionAvailable"></a><span data-ttu-id="7c177-274">使修改后的版本可用于测试运行</span><span class="sxs-lookup"><span data-stu-id="7c177-274">Make the modified version available for test runs</span></span>

<span data-ttu-id="7c177-275">默认情况下，只有状态为**已完成**和**已共享**的版本将在运行 ER 格式时使用。</span><span class="sxs-lookup"><span data-stu-id="7c177-275">By default, the only versions that have a status of **Completed** and **Shared** are used when you run an ER format.</span></span>

<span data-ttu-id="7c177-276">如果您已经完成更改，可以使用当前的草稿版本完成工作，然后使更改可供使用。</span><span class="sxs-lookup"><span data-stu-id="7c177-276">If you've finalized your changes, you can complete your work with the current draft version and make your changes available for use.</span></span> <span data-ttu-id="7c177-277">有关说明，请参阅接下来的[完成修改后的格式版本](#CompleteToRun)一节。</span><span class="sxs-lookup"><span data-stu-id="7c177-277">For instructions, see the [Complete the modified format version](#CompleteToRun) section that follows.</span></span>

<span data-ttu-id="7c177-278">如果要继续使用当前的草稿版本，但是必须使用它来生成支票，您必须明确指定要使用格式的草稿版本来执行。</span><span class="sxs-lookup"><span data-stu-id="7c177-278">If you want to continue to work with the current draft version, but you have to use it to generate checks, you must explicitly specify that you want to use the draft version of the format for execution.</span></span> <span data-ttu-id="7c177-279">有关说明，请参阅[使草稿版本可供使用](#MarkToRun)一节。</span><span class="sxs-lookup"><span data-stu-id="7c177-279">For instructions, see the [Make the draft version available for use](#MarkToRun) section.</span></span>

##### <a name="complete-the-modified-format-version"></a><a name="CompleteToRun"></a><span data-ttu-id="7c177-280">完成修改后的格式版本</span><span class="sxs-lookup"><span data-stu-id="7c177-280">Complete the modified format version</span></span>

1. <span data-ttu-id="7c177-281">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="7c177-281">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7c177-282">在**本地化配置**页面的**配置**部分中，选择**报告配置**。</span><span class="sxs-lookup"><span data-stu-id="7c177-282">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7c177-283">在**配置**页面，在配置树中，展开**支票的模型**，然后选择**支票打印格式**。</span><span class="sxs-lookup"><span data-stu-id="7c177-283">On the **Configurations** page, in the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
4. <span data-ttu-id="7c177-284">在**版本**快速选项卡上，选择状态为**草稿**的记录。</span><span class="sxs-lookup"><span data-stu-id="7c177-284">On the **Versions** FastTab, select the record that has a status of **Draft**.</span></span>
5. <span data-ttu-id="7c177-285">选择**更改状态**，然后选择**完成**。</span><span class="sxs-lookup"><span data-stu-id="7c177-285">Select **Change status**, and then select **Complete**.</span></span>
6. <span data-ttu-id="7c177-286">在对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c177-286">In the dialog box, select **OK**.</span></span>

<span data-ttu-id="7c177-287">当前版本的状态将从**草稿**更改为**已完成**，并将创建状态为**草稿**的新版本。</span><span class="sxs-lookup"><span data-stu-id="7c177-287">The status of the current version is changed from **Draft** to **Completed**, and a new version that has a status of **Draft** is created.</span></span> <span data-ttu-id="7c177-288">您可以使用此新的草稿版本来应用其他更改。</span><span class="sxs-lookup"><span data-stu-id="7c177-288">You can use this new draft version to apply additional changes.</span></span>

##### <a name="make-the-draft-version-available-for-use"></a><a name="MarkToRun"></a><span data-ttu-id="7c177-289">使草稿版本可供使用</span><span class="sxs-lookup"><span data-stu-id="7c177-289">Make the draft version available for use</span></span>

1. <span data-ttu-id="7c177-290">转到**组织管理** \> **工作区** \> **电子申报**。</span><span class="sxs-lookup"><span data-stu-id="7c177-290">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="7c177-291">在**本地化配置**页面的**配置**部分中，选择**报告配置**。</span><span class="sxs-lookup"><span data-stu-id="7c177-291">On the **Localization configurations** page, in the **Configurations** section, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="7c177-292">在**配置**页操作窗格中**配置**选项卡的**高级设置**组中，选择**用户参数**。</span><span class="sxs-lookup"><span data-stu-id="7c177-292">On the **Configurations** page, on the Action Pane, in the **Configurations** tab, in the **Advance settings** group, select **User parameters**.</span></span>
4. <span data-ttu-id="7c177-293">在对话框中，将**运行设置**选项设置为**是**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c177-293">In the dialog box, set the **Run setting** options to **Yes**, and then select **OK**.</span></span>
5. <span data-ttu-id="7c177-294">在配置树中，展开**支票的模型**，选择**支票打印格式**。</span><span class="sxs-lookup"><span data-stu-id="7c177-294">In the configuration tree, expand **Model for cheques**, and select **Cheques printing format**.</span></span>
6. <span data-ttu-id="7c177-295">将**运行草稿**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="7c177-295">Set the **Run draft** option to **Yes**.</span></span>
7. <span data-ttu-id="7c177-296">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="7c177-296">Select **Save**.</span></span>

<span data-ttu-id="7c177-297">运行所选格式时，所选格式的草稿版本将被标记为可以使用。</span><span class="sxs-lookup"><span data-stu-id="7c177-297">The draft version of the selected format is marked as available for use when the selected format is run.</span></span>

### <a name="generate-a-payment-check"></a><a name="ExampleGenerateCheque2"></a><span data-ttu-id="7c177-298">生成付款支票</span><span class="sxs-lookup"><span data-stu-id="7c177-298">Generate a payment check</span></span>

1. <span data-ttu-id="7c177-299">转到**现金和银行管理** \> **银行账户** \> **银行账户**。</span><span class="sxs-lookup"><span data-stu-id="7c177-299">Go to **Cash and bank management** \> **Bank accounts** \> **Bank accounts**.</span></span>
2. <span data-ttu-id="7c177-300">在**银行账户**页面上，选择 **USMF OPER** 账户。</span><span class="sxs-lookup"><span data-stu-id="7c177-300">On the **Bank accounts** page, select the **USMF OPER** account.</span></span>
3. <span data-ttu-id="7c177-301">在银行账户详细信息页的操作窗格中，在**设置**选项卡的**布局**组中，选择**支票**。</span><span class="sxs-lookup"><span data-stu-id="7c177-301">On the bank account details page, on the Action Pane, on the **Set up** tab, in the **Layout** group, select **Check**.</span></span>
4. <span data-ttu-id="7c177-302">在**支票版式**页面上的操作窗格上，选择**打印测试**。</span><span class="sxs-lookup"><span data-stu-id="7c177-302">On the **Check layout** page, on the Action Pane, select **Print test**.</span></span>
5. <span data-ttu-id="7c177-303">在对话框中，将**可转让支票格式**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="7c177-303">In the dialog box, set the **Negotiable check format** option to **Yes**.</span></span>
6. <span data-ttu-id="7c177-304">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c177-304">Select **OK**.</span></span>
7. <span data-ttu-id="7c177-305">检查生成的支票。</span><span class="sxs-lookup"><span data-stu-id="7c177-305">Review the generated check.</span></span> <span data-ttu-id="7c177-306">请注意，已生成条码以对支票的应付金额进行编码。</span><span class="sxs-lookup"><span data-stu-id="7c177-306">Notice that a bar code has been generated to encode the payable amount of the check.</span></span>

    ![在 Excel 中使用条码生成的付款支票](./media/er-barcode-data-source-cheque3.png)

> [!IMPORTANT]
> <span data-ttu-id="7c177-308">如果**条码**数据源的参数不符合特定于条码格式的适当要求，将引发异常。</span><span class="sxs-lookup"><span data-stu-id="7c177-308">An exception is thrown if the argument of a **Barcode** data source doesn't comply with the appropriate requirements that are specific to the bar code format.</span></span> <span data-ttu-id="7c177-309">例如，当调用**条码**数据源以为提供的文本生成 [EAN-8](https://wikipedia.org/wiki/EAN-8) 条码时，如果文本长度超过七个字符将引发异常。</span><span class="sxs-lookup"><span data-stu-id="7c177-309">For example, when the **Barcode** data source is called to generate an [EAN-8](https://wikipedia.org/wiki/EAN-8) bar code for the provided text, an exception is thrown if the length of the text exceeds seven characters.</span></span>

### <a name="convert-the-generated-check-to-a-pdf"></a><a name="ExampleConvertToPDF"></a><span data-ttu-id="7c177-310">将生成的支票转换为 PDF</span><span class="sxs-lookup"><span data-stu-id="7c177-310">Convert the generated check to a PDF</span></span>

<span data-ttu-id="7c177-311">如[生成可打印的 FTI 表单](er-generate-printable-fti-forms.md#finland)主题中所述，您可以使用特殊字体在生成的文档中生成条码。</span><span class="sxs-lookup"><span data-stu-id="7c177-311">As described in the [Generate printable FTI forms](er-generate-printable-fti-forms.md#finland) topic, you can use a special font to produce bar codes in a generated document.</span></span> <span data-ttu-id="7c177-312">在这种情况下，生成文档的其他转换可能取决于转换环境中该字体的可用性。</span><span class="sxs-lookup"><span data-stu-id="7c177-312">In this case, additional transformations of the generated document might depend on the availability of that font in the transformation environment.</span></span> <span data-ttu-id="7c177-313">例如，如果您尝试将文档转换为 PDF 格式或在缺少字体的环境中预览文档，条码将无法正确呈现。</span><span class="sxs-lookup"><span data-stu-id="7c177-313">For example, if you try to convert a document to PDF format or preview it in an environment where the font is missing, bar codes won't be rendered correctly.</span></span>

<span data-ttu-id="7c177-314">但是，当您使用**条码**数据源来生成条码时，这些条码的呈现将不依赖于任何字体。</span><span class="sxs-lookup"><span data-stu-id="7c177-314">However, when you use the **Barcode** data source to produce bar codes, the rendering of those bar codes doesn't depend on any font.</span></span> <span data-ttu-id="7c177-315">因此，您可以轻松地将包含条码的文档转换为 PDF 格式。</span><span class="sxs-lookup"><span data-stu-id="7c177-315">Therefore, you can easily convert documents that contain the bar codes to PDF format.</span></span> <span data-ttu-id="7c177-316">下图显示了生成的付款支票的预览，该支票已基于配置的 ER [目标](electronic-reporting-destinations.md)的设置[转换](electronic-reporting-destinations.md#OutputConversionToPDF)为 PDF。</span><span class="sxs-lookup"><span data-stu-id="7c177-316">The following illustration shows the preview of a generated payment check that has been [converted](electronic-reporting-destinations.md#OutputConversionToPDF) to a PDF, based on the setting of the configured ER [destination](electronic-reporting-destinations.md).</span></span>

![付款支票的 PDF 的预览](./media/er-barcode-data-source-cheque4.png)

## <a name="limitations"></a><span data-ttu-id="7c177-318">限制</span><span class="sxs-lookup"><span data-stu-id="7c177-318">Limitations</span></span>

> [!NOTE]
> <span data-ttu-id="7c177-319">生成的某些类型的条码具有固定的纵横比。</span><span class="sxs-lookup"><span data-stu-id="7c177-319">Some types of bar codes that are generated have a fixed aspect ratio.</span></span> <span data-ttu-id="7c177-320">如果您已打开**支持在电子申报框架中使用 EPPlus 库**功能以在 ER 中使用 Excel 文档，此行为将很重要。</span><span class="sxs-lookup"><span data-stu-id="7c177-320">This behavior makes sense if you've turned on the **Enable usage of EPPlus library in Electronic reporting framework** feature to work with Excel documents in ER.</span></span> <span data-ttu-id="7c177-321">在这种情况下，图像将输入到具有锁定纵横比的占位符中。</span><span class="sxs-lookup"><span data-stu-id="7c177-321">In that case, an image is entered into a placeholder that has a locked aspect ratio.</span></span> <span data-ttu-id="7c177-322">因此，当模板中占位符的尺寸对应于所输入图像的比例时，可以调整生成文档中的实际图片的大小，以保持所需的纵横比。</span><span class="sxs-lookup"><span data-stu-id="7c177-322">Therefore, when the dimensions of a placeholder in a template correspond to the ratio of an image that is entered, a real picture in a generated document might be resized to maintain the required aspect ratio.</span></span> <span data-ttu-id="7c177-323">为阻止图片调整大小，请使用具有预期纵横比的占位符。</span><span class="sxs-lookup"><span data-stu-id="7c177-323">To prevent picture resizing, use a placeholder that has an expected aspect ratio.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c177-324">其他资源</span><span class="sxs-lookup"><span data-stu-id="7c177-324">Additional resources</span></span>

- [<span data-ttu-id="7c177-325">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="7c177-325">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="7c177-326">电子报告目标</span><span class="sxs-lookup"><span data-stu-id="7c177-326">Electronic Reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="7c177-327">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="7c177-327">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="7c177-328">NUMBERFORMAT 函数</span><span class="sxs-lookup"><span data-stu-id="7c177-328">NUMBERFORMAT function</span></span>](er-functions-text-numberformat.md)