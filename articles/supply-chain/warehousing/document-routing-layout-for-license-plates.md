---
title: 牌照标签的文档路线选择布局
description: 此主题介绍如何使用格式设置方法打印标签上的值。
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: 6b5bf6815f225dcca8f9e89e2c85942ce8a2ccd7
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907979"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="45078-103">牌照标签的文档路线选择布局</span><span class="sxs-lookup"><span data-stu-id="45078-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="45078-104">文档路线选择布局定义牌照标签的布局，以及其上印刷的数据。</span><span class="sxs-lookup"><span data-stu-id="45078-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="45078-105">请在设置移动设备菜单项和工作模板时配置打印触发点。</span><span class="sxs-lookup"><span data-stu-id="45078-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="45078-106">在典型方案中，仓库验收员在记录到达收货区的托盘内容之后立即打印牌照标签。</span><span class="sxs-lookup"><span data-stu-id="45078-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="45078-107">将把物理标签应用于托盘。</span><span class="sxs-lookup"><span data-stu-id="45078-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="45078-108">然后可在后续入库处理流程和将来的出站操作中将其用于验证。</span><span class="sxs-lookup"><span data-stu-id="45078-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="45078-109">如果打印设备可以解读收到的文本，您可以打印极为复杂的标签。</span><span class="sxs-lookup"><span data-stu-id="45078-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="45078-110">例如，其中包含条形码的 Zebra 编程语言 (ZPL) 布局可能类似以下示例。</span><span class="sxs-lookup"><span data-stu-id="45078-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="45078-111">在标签打印流程中，此示例中的文本 `$LicensePlateId$` 将替换为数据值。</span><span class="sxs-lookup"><span data-stu-id="45078-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="45078-112">若要查看将打印的值，请转到 **仓库管理 \> 查看和报表 \> 牌照标签**。</span><span class="sxs-lookup"><span data-stu-id="45078-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="45078-113">几种广泛使用的标签生成工具可帮助您设置标签布局的文本的格式。</span><span class="sxs-lookup"><span data-stu-id="45078-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="45078-114">这些工具中许多都支持 `$FieldName$` 格式。</span><span class="sxs-lookup"><span data-stu-id="45078-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="45078-115">此外，Microsoft Dynamics 365 Supply Chain Management 在文档路线选择布局的字段映射中使用特殊格式设置逻辑。</span><span class="sxs-lookup"><span data-stu-id="45078-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="45078-116">为您的系统启用此功能</span><span class="sxs-lookup"><span data-stu-id="45078-116">Turn on this feature for your system</span></span>

<span data-ttu-id="45078-117">如果您的系统尚未包含本主题中所述的功能，请转到 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，打开 *增强的牌照标签布局* 功能。</span><span class="sxs-lookup"><span data-stu-id="45078-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Enhanced license plate label layouts* feature.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="45078-118">自定义数字格式</span><span class="sxs-lookup"><span data-stu-id="45078-118">Custom number formats</span></span>

<span data-ttu-id="45078-119">可自定义使用采用以下格式的代码打印的数值字段值的格式设置。</span><span class="sxs-lookup"><span data-stu-id="45078-119">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="45078-120">下面是对此格式的说明：</span><span class="sxs-lookup"><span data-stu-id="45078-120">Here is an explanation of this format:</span></span>

- <span data-ttu-id="45078-121">`FieldName` 是数据字段的名称（如 **Qty**）。</span><span class="sxs-lookup"><span data-stu-id="45078-121">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="45078-122">`FormatString` 定义必须如何打印数据。</span><span class="sxs-lookup"><span data-stu-id="45078-122">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="45078-123">下面的示例显示如何自定义工作数量 (**Qty**) 字段：</span><span class="sxs-lookup"><span data-stu-id="45078-123">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="45078-124">若要始终显示四位数（将零用作占位符），请使用 `$Qty:0000$`。</span><span class="sxs-lookup"><span data-stu-id="45078-124">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="45078-125">例如，如果数量为 10，则标签将显示“0010”。</span><span class="sxs-lookup"><span data-stu-id="45078-125">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="45078-126">若要始终显示两位数，请使用 `$Qty:0.00$`。</span><span class="sxs-lookup"><span data-stu-id="45078-126">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="45078-127">例如，如果数量为 10，则标签将显示“10.00”。</span><span class="sxs-lookup"><span data-stu-id="45078-127">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="45078-128">有关可用数字格式字符串的完整列表，请参阅[自定义数值格式字符串](/dotnet/standard/base-types/custom-numeric-format-strings)。</span><span class="sxs-lookup"><span data-stu-id="45078-128">For a complete list of the available number format strings, see [Custom numeric format strings](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="45078-129">自定义字符串格式</span><span class="sxs-lookup"><span data-stu-id="45078-129">Custom string formats</span></span>

<span data-ttu-id="45078-130">可使用以下字段和格式代码删除字符串的第一批字符。</span><span class="sxs-lookup"><span data-stu-id="45078-130">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="45078-131">下面，`#` 指定要跳过的字符数量。</span><span class="sxs-lookup"><span data-stu-id="45078-131">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="45078-132">例如，若要打印不包含前两个字符的系列货运包装箱代码 (SSCC) 牌照编号，请使用 `$LicensePlateId:2..$`。</span><span class="sxs-lookup"><span data-stu-id="45078-132">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="45078-133">在此示例中，牌照编号 0011111111111222221 将打印为“11111111111222221”。</span><span class="sxs-lookup"><span data-stu-id="45078-133">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="45078-134">自定义日期/时间格式</span><span class="sxs-lookup"><span data-stu-id="45078-134">Custom date/time formats</span></span>

<span data-ttu-id="45078-135">以下示例显示如何控制用于打印日期的格式。</span><span class="sxs-lookup"><span data-stu-id="45078-135">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="45078-136">在此示例中，日期 2020 年 4 月 30 日将被打印为“30-04-2020”。</span><span class="sxs-lookup"><span data-stu-id="45078-136">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="45078-137">有关可用日期/时间格式的完整列表，请参阅[自定义日期和时间格式字符串](/dotnet/standard/base-types/custom-date-and-time-format-strings)。</span><span class="sxs-lookup"><span data-stu-id="45078-137">For a complete list of the available date/time formats, see [Custom date and time format strings](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="45078-138">打印多行数据的单独行</span><span class="sxs-lookup"><span data-stu-id="45078-138">Print individual lines from multiline data</span></span>

<span data-ttu-id="45078-139">如果一个数据字段中包含多行（即换行符分隔的行），可以使用以下格式打印单行。</span><span class="sxs-lookup"><span data-stu-id="45078-139">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="45078-140">下面，`#` 是要打印的行号。</span><span class="sxs-lookup"><span data-stu-id="45078-140">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="45078-141">（1 代表第一行。）</span><span class="sxs-lookup"><span data-stu-id="45078-141">(Use 1 for the first line.)</span></span>

<span data-ttu-id="45078-142">例如，您的系统中有一个 `AdditionalAddress` 字段存储下面的多行地址：</span><span class="sxs-lookup"><span data-stu-id="45078-142">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="45078-143">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="45078-143">Contoso Inc.</span></span>  
<span data-ttu-id="45078-144">123 Street Name</span><span class="sxs-lookup"><span data-stu-id="45078-144">123 Street Name</span></span>  
<span data-ttu-id="45078-145">Some City, Some State</span><span class="sxs-lookup"><span data-stu-id="45078-145">Some City, Some State</span></span>

<span data-ttu-id="45078-146">可使用下面的代码一次一行打印此地址。</span><span class="sxs-lookup"><span data-stu-id="45078-146">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="45078-147">代码</span><span class="sxs-lookup"><span data-stu-id="45078-147">Code</span></span> | <span data-ttu-id="45078-148">打印的文本</span><span class="sxs-lookup"><span data-stu-id="45078-148">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="45078-149">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="45078-149">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="45078-150">123 Street Name</span><span class="sxs-lookup"><span data-stu-id="45078-150">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="45078-151">Some City, Some State</span><span class="sxs-lookup"><span data-stu-id="45078-151">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="45078-152">通过显示方法打印和设置格式</span><span class="sxs-lookup"><span data-stu-id="45078-152">Print and format from a display method</span></span>

<span data-ttu-id="45078-153">可使用以下格式通过显示方法进行打印。</span><span class="sxs-lookup"><span data-stu-id="45078-153">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="45078-154">可以将此格式与此主题中前面介绍的其他类型组合使用。</span><span class="sxs-lookup"><span data-stu-id="45078-154">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="45078-155">例如，您有一个显示方法名称为 `DisplayListOfItemsNumbers()`，而您希望打印此方法的第一个项目编号。</span><span class="sxs-lookup"><span data-stu-id="45078-155">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="45078-156">在这种情况下，可以使用以下代码。</span><span class="sxs-lookup"><span data-stu-id="45078-156">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="45078-157">有关如何打印标签的详细信息</span><span class="sxs-lookup"><span data-stu-id="45078-157">More information about how to print labels</span></span>

<span data-ttu-id="45078-158">有关如何设置和打印标签的详细信息，请参阅[启用牌照标签打印](tasks/license-plate-label-printing.md)。</span><span class="sxs-lookup"><span data-stu-id="45078-158">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]