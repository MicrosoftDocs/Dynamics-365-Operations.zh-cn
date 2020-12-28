---
title: 类型转换类别的 ER 函数列表
description: 本主题提供有关电子申报 (ER) 支持的转换函数的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d160c02403bf067ed523fbd634e65c622b522b97
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686066"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="7b840-103">类型转换类别的 ER 函数列表</span><span class="sxs-lookup"><span data-stu-id="7b840-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b840-104">电子申报 (ER) 类型转换函数可用于在类型之间转换值。</span><span class="sxs-lookup"><span data-stu-id="7b840-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="7b840-105">本主题提供这些函数的概要。</span><span class="sxs-lookup"><span data-stu-id="7b840-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="7b840-106">类型转换函数</span><span class="sxs-lookup"><span data-stu-id="7b840-106">Type conversion functions</span></span>

| <span data-ttu-id="7b840-107">职能</span><span class="sxs-lookup"><span data-stu-id="7b840-107">Function</span></span> | <span data-ttu-id="7b840-108">说明</span><span class="sxs-lookup"><span data-stu-id="7b840-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7b840-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="7b840-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="7b840-110">此函数返回一个 *Int64* 值，该值表示指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="7b840-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="7b840-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="7b840-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="7b840-112">此函数返回一个 *Int* 值，该值表示指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="7b840-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="7b840-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="7b840-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="7b840-114">此函数返回一个 *实数* 值，该值从指定的 *字符串* 值转换而来。</span><span class="sxs-lookup"><span data-stu-id="7b840-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="7b840-115">在转换过程中，将考虑指定的十进制和数字分组分隔符。</span><span class="sxs-lookup"><span data-stu-id="7b840-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="7b840-116">值</span><span class="sxs-lookup"><span data-stu-id="7b840-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="7b840-117">此函数返回一个 *实数* 值，该值从指定的 *字符串* 值转换而来。</span><span class="sxs-lookup"><span data-stu-id="7b840-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="7b840-118">日期和时间类别的类型转换函数</span><span class="sxs-lookup"><span data-stu-id="7b840-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="7b840-119">下表描述了[日期和时间类别](er-functions-category-datetime.md)的类型转换函数。</span><span class="sxs-lookup"><span data-stu-id="7b840-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="7b840-120">职能</span><span class="sxs-lookup"><span data-stu-id="7b840-120">Function</span></span> | <span data-ttu-id="7b840-121">说明</span><span class="sxs-lookup"><span data-stu-id="7b840-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7b840-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="7b840-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="7b840-123">此函数返回一个 *日期时间* 值，此值从指定格式和指定的区域性（可选）的给定 *字符串* 值转换为日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="7b840-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="7b840-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="7b840-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="7b840-125">此函数返回一个 *日期时间* 值，此值从给定日期/时间值转换为协调世界时（格林威治标准时间 \[GMT\]）的 *日期* 值。</span><span class="sxs-lookup"><span data-stu-id="7b840-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="7b840-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="7b840-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="7b840-127">此函数返回一个 *日期* 值，此值从指定格式和指定的区域性（可选）的给定 *字符串* 值转换为日期值。</span><span class="sxs-lookup"><span data-stu-id="7b840-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="7b840-128">列表类别的类型转换函数</span><span class="sxs-lookup"><span data-stu-id="7b840-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="7b840-129">下表描述了[列表类别](er-functions-category-list.md)的类型转换函数。</span><span class="sxs-lookup"><span data-stu-id="7b840-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="7b840-130">职能</span><span class="sxs-lookup"><span data-stu-id="7b840-130">Function</span></span> | <span data-ttu-id="7b840-131">说明</span><span class="sxs-lookup"><span data-stu-id="7b840-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7b840-132">列表</span><span class="sxs-lookup"><span data-stu-id="7b840-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="7b840-133">此函数作为从指定的 *容器（记录）* 类型的参数创建的新列表，返回一个 *记录列表* 值。</span><span class="sxs-lookup"><span data-stu-id="7b840-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="7b840-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="7b840-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="7b840-135">此函数返回一个 *记录列表* 值，此值基于给定的 *枚举* 或 *容器（记录）* 类型的参数的结构创建。</span><span class="sxs-lookup"><span data-stu-id="7b840-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="7b840-136">拆分</span><span class="sxs-lookup"><span data-stu-id="7b840-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="7b840-137">此函数将指定的 *字符串* 值拆分为子字符串，并将结果作为新的 *记录列表* 值返回。</span><span class="sxs-lookup"><span data-stu-id="7b840-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="7b840-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="7b840-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="7b840-139">此函数返回由指定 *记录列表* 值中的指定字段的连接值组成的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="7b840-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="7b840-140">这些值可以通过指定分隔符分隔。</span><span class="sxs-lookup"><span data-stu-id="7b840-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="7b840-141">文本类别的类型转换函数</span><span class="sxs-lookup"><span data-stu-id="7b840-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="7b840-142">下表描述了[文本类别](er-functions-category-text.md)的类型转换函数。</span><span class="sxs-lookup"><span data-stu-id="7b840-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="7b840-143">职能</span><span class="sxs-lookup"><span data-stu-id="7b840-143">Function</span></span> | <span data-ttu-id="7b840-144">说明</span><span class="sxs-lookup"><span data-stu-id="7b840-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7b840-145">Char</span><span class="sxs-lookup"><span data-stu-id="7b840-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="7b840-146">此函数返一个 *字符串* 值，该值代表指定 Unicode 数值引用的单个字符。</span><span class="sxs-lookup"><span data-stu-id="7b840-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="7b840-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="7b840-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="7b840-148">此函数将 *字符串* 类型的指定输入转换为 *GUID* 类型的数据项。</span><span class="sxs-lookup"><span data-stu-id="7b840-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="7b840-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="7b840-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="7b840-150">此函数返回一个 *字符串* 值，此值以指定格式和指定的区域性（可选）表示指定数字。</span><span class="sxs-lookup"><span data-stu-id="7b840-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="7b840-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="7b840-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="7b840-152">此函数返回一个 *容器* 值，该值以二进制格式显示指定字符串的快速响应代码（QR 代码）图像。</span><span class="sxs-lookup"><span data-stu-id="7b840-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="7b840-153">文本</span><span class="sxs-lookup"><span data-stu-id="7b840-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="7b840-154">在将指定的数字转换为根据当前应用程序实例的服务器区域设置设定格式的文本字符串后，此函数返回表示该数字的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="7b840-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7b840-155">其他资源</span><span class="sxs-lookup"><span data-stu-id="7b840-155">Additional resources</span></span>

[<span data-ttu-id="7b840-156">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="7b840-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="7b840-157">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="7b840-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="7b840-158">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="7b840-158">Electronic reporting formula language</span></span>](er-formula-language.md)
