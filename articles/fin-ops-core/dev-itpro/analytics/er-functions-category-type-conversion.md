---
title: 类型转换类别的 ER 函数列表
description: 本主题提供有关电子申报 (ER) 支持的转换函数的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5613496d3131ccd39b198cac214eb791a6d07355
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561510"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="9993a-103">类型转换类别的 ER 函数列表</span><span class="sxs-lookup"><span data-stu-id="9993a-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9993a-104">电子申报 (ER) 类型转换函数可用于在类型之间转换值。</span><span class="sxs-lookup"><span data-stu-id="9993a-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="9993a-105">本主题提供这些函数的概要。</span><span class="sxs-lookup"><span data-stu-id="9993a-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="9993a-106">类型转换函数</span><span class="sxs-lookup"><span data-stu-id="9993a-106">Type conversion functions</span></span>

| <span data-ttu-id="9993a-107">职能</span><span class="sxs-lookup"><span data-stu-id="9993a-107">Function</span></span> | <span data-ttu-id="9993a-108">说明</span><span class="sxs-lookup"><span data-stu-id="9993a-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9993a-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="9993a-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="9993a-110">此函数返回一个 *Int64* 值，该值表示指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="9993a-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="9993a-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="9993a-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="9993a-112">此函数返回一个 *Int* 值，该值表示指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="9993a-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="9993a-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="9993a-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="9993a-114">此函数返回一个 *实数* 值，该值从指定的 *字符串* 值转换而来。</span><span class="sxs-lookup"><span data-stu-id="9993a-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="9993a-115">在转换过程中，将考虑指定的十进制和数字分组分隔符。</span><span class="sxs-lookup"><span data-stu-id="9993a-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="9993a-116">值</span><span class="sxs-lookup"><span data-stu-id="9993a-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="9993a-117">此函数返回一个 *实数* 值，该值从指定的 *字符串* 值转换而来。</span><span class="sxs-lookup"><span data-stu-id="9993a-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="9993a-118">容器类别的类型转换函数</span><span class="sxs-lookup"><span data-stu-id="9993a-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="9993a-119">下表描述了[容器](er-functions-category-container.md)类别的类型转换函数。</span><span class="sxs-lookup"><span data-stu-id="9993a-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="9993a-120">函数</span><span class="sxs-lookup"><span data-stu-id="9993a-120">Function</span></span> | <span data-ttu-id="9993a-121">说明</span><span class="sxs-lookup"><span data-stu-id="9993a-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9993a-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="9993a-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="9993a-123">此函数将 *字符串* 类型的指定输入转换为 *容器* 类型的数据项。</span><span class="sxs-lookup"><span data-stu-id="9993a-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="9993a-124">日期和时间类别的类型转换函数</span><span class="sxs-lookup"><span data-stu-id="9993a-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="9993a-125">下表描述了[日期和时间类别](er-functions-category-datetime.md)的类型转换函数。</span><span class="sxs-lookup"><span data-stu-id="9993a-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="9993a-126">职能</span><span class="sxs-lookup"><span data-stu-id="9993a-126">Function</span></span> | <span data-ttu-id="9993a-127">说明</span><span class="sxs-lookup"><span data-stu-id="9993a-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9993a-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="9993a-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="9993a-129">此函数返回一个 *日期时间* 值，此值从指定格式和指定的区域性（可选）的给定 *字符串* 值转换为日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="9993a-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="9993a-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="9993a-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="9993a-131">此函数返回一个 *日期时间* 值，此值从给定日期/时间值转换为协调世界时（格林威治标准时间 \[GMT\]）的 *日期* 值。</span><span class="sxs-lookup"><span data-stu-id="9993a-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="9993a-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="9993a-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="9993a-133">此函数返回一个 *日期* 值，此值从指定格式和指定的区域性（可选）的给定 *字符串* 值转换为日期值。</span><span class="sxs-lookup"><span data-stu-id="9993a-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="9993a-134">列表类别的类型转换函数</span><span class="sxs-lookup"><span data-stu-id="9993a-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="9993a-135">下表描述了[列表类别](er-functions-category-list.md)的类型转换函数。</span><span class="sxs-lookup"><span data-stu-id="9993a-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="9993a-136">职能</span><span class="sxs-lookup"><span data-stu-id="9993a-136">Function</span></span> | <span data-ttu-id="9993a-137">说明</span><span class="sxs-lookup"><span data-stu-id="9993a-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9993a-138">列表</span><span class="sxs-lookup"><span data-stu-id="9993a-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="9993a-139">此函数作为从指定的 *容器（记录）* 类型的参数创建的新列表，返回一个 *记录列表* 值。</span><span class="sxs-lookup"><span data-stu-id="9993a-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="9993a-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="9993a-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="9993a-141">此函数返回一个 *记录列表* 值，此值基于给定的 *枚举* 或 *容器（记录）* 类型的参数的结构创建。</span><span class="sxs-lookup"><span data-stu-id="9993a-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="9993a-142">拆分</span><span class="sxs-lookup"><span data-stu-id="9993a-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="9993a-143">此函数将指定的 *字符串* 值拆分为子字符串，并将结果作为新的 *记录列表* 值返回。</span><span class="sxs-lookup"><span data-stu-id="9993a-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="9993a-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="9993a-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="9993a-145">此函数返回由指定 *记录列表* 值中的指定字段的连接值组成的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="9993a-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="9993a-146">这些值可以通过指定分隔符分隔。</span><span class="sxs-lookup"><span data-stu-id="9993a-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="9993a-147">文本类别的类型转换函数</span><span class="sxs-lookup"><span data-stu-id="9993a-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="9993a-148">下表描述了[文本类别](er-functions-category-text.md)的类型转换函数。</span><span class="sxs-lookup"><span data-stu-id="9993a-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="9993a-149">职能</span><span class="sxs-lookup"><span data-stu-id="9993a-149">Function</span></span> | <span data-ttu-id="9993a-150">说明</span><span class="sxs-lookup"><span data-stu-id="9993a-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="9993a-151">Char</span><span class="sxs-lookup"><span data-stu-id="9993a-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="9993a-152">此函数返一个 *字符串* 值，该值代表指定 Unicode 数值引用的单个字符。</span><span class="sxs-lookup"><span data-stu-id="9993a-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="9993a-153">GuidValue</span><span class="sxs-lookup"><span data-stu-id="9993a-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="9993a-154">此函数将 *字符串* 类型的指定输入转换为 *GUID* 类型的数据项。</span><span class="sxs-lookup"><span data-stu-id="9993a-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="9993a-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="9993a-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="9993a-156">此函数返回一个 *字符串* 值，此值以指定格式和指定的区域性（可选）表示指定数字。</span><span class="sxs-lookup"><span data-stu-id="9993a-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="9993a-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="9993a-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="9993a-158">此函数返回一个 *容器* 值，该值以二进制格式显示指定字符串的快速响应代码（QR 代码）图像。</span><span class="sxs-lookup"><span data-stu-id="9993a-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="9993a-159">文本</span><span class="sxs-lookup"><span data-stu-id="9993a-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="9993a-160">在将指定的数字转换为根据当前应用程序实例的服务器区域设置设定格式的文本字符串后，此函数返回表示该数字的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="9993a-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="9993a-161">其他资源</span><span class="sxs-lookup"><span data-stu-id="9993a-161">Additional resources</span></span>

[<span data-ttu-id="9993a-162">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="9993a-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="9993a-163">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="9993a-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="9993a-164">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="9993a-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]