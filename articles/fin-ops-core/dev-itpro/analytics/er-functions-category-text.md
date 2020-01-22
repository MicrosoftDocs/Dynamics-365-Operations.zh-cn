---
title: 文本类别的 ER 函数列表
description: 本主题提供有关电子申报 (ER) 支持的文本函数的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f519d242fe74196b0d12bdc9df4f1b4b0e585752
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916606"
---
# <a name="list-of-er-functions-of-the-text-category"></a><span data-ttu-id="3e57c-103">文本类别的 ER 函数列表</span><span class="sxs-lookup"><span data-stu-id="3e57c-103">List of ER functions of the text category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e57c-104">电子申报 (ER) 文本函数可用于对*字符串*数据类型的数据源执行操作。</span><span class="sxs-lookup"><span data-stu-id="3e57c-104">Electronic reporting (ER) text functions can be used to perform operations on data sources of the *String* data type.</span></span> <span data-ttu-id="3e57c-105">本主题提供这些函数的概要。</span><span class="sxs-lookup"><span data-stu-id="3e57c-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="3e57c-106">支持的函数列表</span><span class="sxs-lookup"><span data-stu-id="3e57c-106">List of supported functions</span></span>

| <span data-ttu-id="3e57c-107">职能</span><span class="sxs-lookup"><span data-stu-id="3e57c-107">Function</span></span> | <span data-ttu-id="3e57c-108">说明</span><span class="sxs-lookup"><span data-stu-id="3e57c-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="3e57c-109">Char</span><span class="sxs-lookup"><span data-stu-id="3e57c-109">Char</span></span>](er-functions-text-char.md) | <span data-ttu-id="3e57c-110">此函数返一个*字符串*值，该值表示指定 Unicode 数值引用的单个字符。</span><span class="sxs-lookup"><span data-stu-id="3e57c-110">This function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="3e57c-111">连接</span><span class="sxs-lookup"><span data-stu-id="3e57c-111">Concatenate</span></span>](er-functions-text-concatenate.md) | <span data-ttu-id="3e57c-112">在将所有指定的文本字符串合并为一个字符串之后，此函数将这些字符串作为*字符串*值返回。</span><span class="sxs-lookup"><span data-stu-id="3e57c-112">This function returns  all the specified text strings as a *String* value after they have been joined into one string.</span></span> |
| [<span data-ttu-id="3e57c-113">格式</span><span class="sxs-lookup"><span data-stu-id="3e57c-113">Format</span></span>](er-functions-text-format.md) | <span data-ttu-id="3e57c-114">通过使用第 *N* 个参数替换出现的所有 **%N** 设定指定字符串的格式后，此函数作为*字符串*值返回该字符串。</span><span class="sxs-lookup"><span data-stu-id="3e57c-114">This function returns the specified string a *String* value after it has been formatted by substituting any occurrences of **%N** with the *N*th argument.</span></span> |
| [<span data-ttu-id="3e57c-115">GetEnumValueByName</span><span class="sxs-lookup"><span data-stu-id="3e57c-115">GetEnumValueByName</span></span>](er-functions-text-getenumvaluebyname.md) | <span data-ttu-id="3e57c-116">此函数通过使用指定为*字符串*值的枚举名称在指定的枚举数据源中搜索特定的*枚举*值。</span><span class="sxs-lookup"><span data-stu-id="3e57c-116">This function searches for a specific *Enum* value in the specified enumeration data source by using the enumeration name that is specified as a *String* value.</span></span> <span data-ttu-id="3e57c-117">如果找到*枚举*值，函数将返回此值。</span><span class="sxs-lookup"><span data-stu-id="3e57c-117">If the *Enum* value is found, the function returns it.</span></span> |
| [<span data-ttu-id="3e57c-118">GuidValue</span><span class="sxs-lookup"><span data-stu-id="3e57c-118">GuidValue</span></span>](er-functions-text-guidvalue.md) | <span data-ttu-id="3e57c-119">此函数将*字符串*类型的指定输入转换为 *GUID* 类型的数据项。</span><span class="sxs-lookup"><span data-stu-id="3e57c-119">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="3e57c-120">JsonValue</span><span class="sxs-lookup"><span data-stu-id="3e57c-120">JsonValue</span></span>](er-functions-text-jsonvalue.md) | <span data-ttu-id="3e57c-121">此函数分析在指定路径访问且格式为 JavaScript Object Notation (JSON) 的数据，并提取基于指定 ID 的标量值。</span><span class="sxs-lookup"><span data-stu-id="3e57c-121">This function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that is based on the specified ID.</span></span> <span data-ttu-id="3e57c-122">然后将提取的标量值返回为*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="3e57c-122">It then returns the extracted scalar value as a *String* value.</span></span> |
| [<span data-ttu-id="3e57c-123">左对齐</span><span class="sxs-lookup"><span data-stu-id="3e57c-123">Left</span></span>](er-functions-text-left.md) | <span data-ttu-id="3e57c-124">此函数返回*字符串*值，该值在指定字符串的开头显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="3e57c-124">This function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span> |
| [<span data-ttu-id="3e57c-125">Len</span><span class="sxs-lookup"><span data-stu-id="3e57c-125">Len</span></span>](er-functions-text-len.md) | <span data-ttu-id="3e57c-126">此函数返回*整数*值，该值在指定的字符串中显示字符数量。</span><span class="sxs-lookup"><span data-stu-id="3e57c-126">This function returns an *Integer* value that presents the number of characters in the specified string.</span></span> |
| [<span data-ttu-id="3e57c-127">Lower</span><span class="sxs-lookup"><span data-stu-id="3e57c-127">Lower</span></span>](er-functions-text-lower.md) | <span data-ttu-id="3e57c-128">在将指定的文本字符串转换为小写字母后，此函数作为*字符串*值返回该字符串。</span><span class="sxs-lookup"><span data-stu-id="3e57c-128">This function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span> |
| [<span data-ttu-id="3e57c-129">Mid</span><span class="sxs-lookup"><span data-stu-id="3e57c-129">Mid</span></span>](er-functions-text-mid.md) | <span data-ttu-id="3e57c-130">此函数返回*字符串*值，该值在指定位置的开始处，在指定的字符串中显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="3e57c-130">This function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span> |
| [<span data-ttu-id="3e57c-131">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="3e57c-131">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="3e57c-132">此函数返回一个*字符串*值，此值以指定格式和指定的区域性（可选）显示指定数字。</span><span class="sxs-lookup"><span data-stu-id="3e57c-132">This function returns a *String* value that presents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="3e57c-133">NumeralsToText</span><span class="sxs-lookup"><span data-stu-id="3e57c-133">NumeralsToText</span></span>](er-functions-text-numeralstotext.md) | <span data-ttu-id="3e57c-134">在使用指定语言拼出（即转换为文本字符串）指定数字后，此函数作为*字符串*返回指定数字。</span><span class="sxs-lookup"><span data-stu-id="3e57c-134">This function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span> |
| [<span data-ttu-id="3e57c-135">PadLeft</span><span class="sxs-lookup"><span data-stu-id="3e57c-135">PadLeft</span></span>](er-functions-text-padleft.md) | <span data-ttu-id="3e57c-136">此函数返回指定长度的*字符串*值，其中指定字符串的开头是使用一个或多个指定字符的实例填充的。</span><span class="sxs-lookup"><span data-stu-id="3e57c-136">This function returns a *String* value of the specified length, where the start of the specified string is padded with one or more instances of the specified characters.</span></span> |
| [<span data-ttu-id="3e57c-137">QrCode</span><span class="sxs-lookup"><span data-stu-id="3e57c-137">QrCode</span></span>](er-functions-text-qrcode.md) | <span data-ttu-id="3e57c-138">此函数返回一个*容器*值，该值以二进制格式显示指定字符串的快速响应代码（QR 代码）图像。</span><span class="sxs-lookup"><span data-stu-id="3e57c-138">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="3e57c-139">替换</span><span class="sxs-lookup"><span data-stu-id="3e57c-139">Replace</span></span>](er-functions-text-replace.md) | <span data-ttu-id="3e57c-140">在将全部或部分指定文本字符串替换为另一个字符串之后，此函数作为*字符串*值返回指定的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="3e57c-140">This function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span> |
| [<span data-ttu-id="3e57c-141">右对齐</span><span class="sxs-lookup"><span data-stu-id="3e57c-141">Right</span></span>](er-functions-text-right.md) | <span data-ttu-id="3e57c-142">此函数返回*字符串*值，该值在指定字符串的末尾显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="3e57c-142">This function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span> |
| [<span data-ttu-id="3e57c-143">文本</span><span class="sxs-lookup"><span data-stu-id="3e57c-143">Text</span></span>](er-functions-text-text.md) | <span data-ttu-id="3e57c-144">在将指定的数字转换为根据当前应用程序实例的服务器区域设置设定格式的文本字符串后，此函数将该数字作为*字符串*值返回。</span><span class="sxs-lookup"><span data-stu-id="3e57c-144">This function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |
| [<span data-ttu-id="3e57c-145">翻译</span><span class="sxs-lookup"><span data-stu-id="3e57c-145">Translate</span></span>](er-functions-text-translate.md) | <span data-ttu-id="3e57c-146">在将全部或部分指定文本字符串替换为另一个字符串之后，此函数作为*字符串*值返回指定的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="3e57c-146">This function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span> |
| [<span data-ttu-id="3e57c-147">Trim</span><span class="sxs-lookup"><span data-stu-id="3e57c-147">Trim</span></span>](er-functions-text-trim.md) | <span data-ttu-id="3e57c-148">在删除前导和尾随空格以及删除单词之间的多个空格之后，此函数作为*字符串*值返回指定的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="3e57c-148">This function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span> |
| [<span data-ttu-id="3e57c-149">Upper</span><span class="sxs-lookup"><span data-stu-id="3e57c-149">Upper</span></span>](er-functions-text-upper.md) | <span data-ttu-id="3e57c-150">在将指定的文本字符串转换为大写字母后，此函数作为*字符串*值返回该字符串。</span><span class="sxs-lookup"><span data-stu-id="3e57c-150">This function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="3e57c-151">其他资源</span><span class="sxs-lookup"><span data-stu-id="3e57c-151">Additional resources</span></span>

[<span data-ttu-id="3e57c-152">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="3e57c-152">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="3e57c-153">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="3e57c-153">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="3e57c-154">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="3e57c-154">Electronic reporting formula language</span></span>](er-formula-language.md)
