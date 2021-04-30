---
title: 设计 ER 配置以在生成的文件中禁止 BOM 字符
description: 本主题说明如何配置电子报告 (ER) 格式以生成禁止字节顺序标记 (BOM) 字符的报表。
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d5ada93c0192aadac70c38c8c8c4f3af86ff6fc3
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893268"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="ae167-103">设计 ER 配置以在生成的文件中禁止 BOM 字符</span><span class="sxs-lookup"><span data-stu-id="ae167-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae167-104">可以设计[电子报告 (ER)](general-electronic-reporting.md) [解决方案](er-quick-start1-new-solution.md)来生成传出文档。</span><span class="sxs-lookup"><span data-stu-id="ae167-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="ae167-105">要将文档生成为文本文件或 XML 文件，解决方案必须包括包含 ER [格式](general-electronic-reporting.md#FormatComponentOutbound)组件的 ER [配置](general-electronic-reporting.md#Configuration)。</span><span class="sxs-lookup"><span data-stu-id="ae167-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="ae167-106">若要指定表示生成文件中字符集的 [字符编码](/windows/win32/intl/character-sets)，ER 格式必须包含 **Common\\File** 格式元素。</span><span class="sxs-lookup"><span data-stu-id="ae167-106">To specify the [character encoding](/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="ae167-107">要配置 ER 格式组件，在 ER 格式设计器中打开 ER 配置的 [草稿](general-electronic-reporting.md#component-versioning)版本，添加 **Common\\File** 元素。</span><span class="sxs-lookup"><span data-stu-id="ae167-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="ae167-108">在 **编码** 字段中，指定使用此组件在运行时生成的传出文件的编码。</span><span class="sxs-lookup"><span data-stu-id="ae167-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="ae167-109">如果格式包含错误的编码名称，将更改保存到格式设置时会引发错误。</span><span class="sxs-lookup"><span data-stu-id="ae167-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![在“格式设计器”页添加根元素](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="ae167-111">如果您指定 **UTF-8**、**UTF-16** 或 **UTF-32** 作为编码，**禁止 BOM 表字符** 选项将变为可用。</span><span class="sxs-lookup"><span data-stu-id="ae167-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="ae167-112">将此选项设置为 **是**，将禁止在可编辑 ER 格式运行时在运行时生成的传出文件中的[字节顺序标记 (BOM) 字符](/globalization/encoding/byte-order-mark)。</span><span class="sxs-lookup"><span data-stu-id="ae167-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="ae167-113">如果将 **编码** 字段留空，将使用默认的 **UTF-8** 编码。</span><span class="sxs-lookup"><span data-stu-id="ae167-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![在“格式设计器”页上设置“禁止 BOM 字符”选项](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="ae167-115">要在运行时查看功能，请完成相应的过程。</span><span class="sxs-lookup"><span data-stu-id="ae167-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="ae167-116">例如，完成[推迟执行 ER 格式的 XML 元素](er-defer-xml-element.md)主题中的步骤。</span><span class="sxs-lookup"><span data-stu-id="ae167-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="ae167-117">完成该主题的[修改格式，以便根据生成的输出来进行计算](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output)一节中的步骤后，请执行以下其他步骤。</span><span class="sxs-lookup"><span data-stu-id="ae167-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="ae167-118">指定 UTF 编码：</span><span class="sxs-lookup"><span data-stu-id="ae167-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="ae167-119">选择 **Common\\File** 类型的 **报表** 元素。</span><span class="sxs-lookup"><span data-stu-id="ae167-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="ae167-120">在 **编码** 字段中，指定 **UTF-8** 编码。</span><span class="sxs-lookup"><span data-stu-id="ae167-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="ae167-121">生成包含 BOM 字符的 XML 文件：</span><span class="sxs-lookup"><span data-stu-id="ae167-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="ae167-122">将 **禁止 BOM 字符** 选项设置为 **否** 以在生成的 XML 文件中包含 BOM 字符。</span><span class="sxs-lookup"><span data-stu-id="ae167-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="ae167-123">完成 [推迟执行 ER 格式的 XML 元素](er-defer-xml-element.md)主题的 [推迟执行汇总 XML 元素，以便使用计算出的总和](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)一节中的步骤，并将生成的文件另存为 **SampleXmlReport.xml**。</span><span class="sxs-lookup"><span data-stu-id="ae167-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="ae167-124">生成不包含 BOM 字符的 XML 文件：</span><span class="sxs-lookup"><span data-stu-id="ae167-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="ae167-125">将 **禁止 BOM 字符** 选项设置为 **是** 以在生成的 XML 文件中禁止 BOM 字符。</span><span class="sxs-lookup"><span data-stu-id="ae167-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="ae167-126">完成 [推迟执行 ER 格式的 XML 元素](er-defer-xml-element.md)主题的 [推迟执行汇总 XML 元素，以便使用计算出的总和](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used)一节中的步骤，并将生成的文件另存为 **SampleXmlReport (1).xml**。</span><span class="sxs-lookup"><span data-stu-id="ae167-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="ae167-127">在文件比较实用程序中，比较生成的文件。</span><span class="sxs-lookup"><span data-stu-id="ae167-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="ae167-128">您将注意到的第一个区别是在文件标题中。</span><span class="sxs-lookup"><span data-stu-id="ae167-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="ae167-129">SampleXmlReport.xml 文件包含 BOM 字符，而 SampleXmlReport (1).xml 文件不包含。</span><span class="sxs-lookup"><span data-stu-id="ae167-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![使用文件比较实用程序比较生成的文件](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="ae167-131">请参阅</span><span class="sxs-lookup"><span data-stu-id="ae167-131">See also</span></span>

- [<span data-ttu-id="ae167-132">推迟执行电子报告格式的 XML 元素</span><span class="sxs-lookup"><span data-stu-id="ae167-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]