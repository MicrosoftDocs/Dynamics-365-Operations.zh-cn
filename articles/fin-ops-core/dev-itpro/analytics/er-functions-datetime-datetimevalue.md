---
title: DATETIMEVALUE ER 函数
description: 本主题提供有关 DATETIMEVALUE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891273"
---
# <a name="datetimevalue-er-function"></a><span data-ttu-id="312d5-103">DATETIMEVALUE ER 函数</span><span class="sxs-lookup"><span data-stu-id="312d5-103">DATETIMEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="312d5-104">`DATETIMEVALUE` 函数返回一个 *日期时间* 值，此值从指定格式和指定的[区域性](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)（可选）的给定文本值转换为日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="312d5-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="312d5-105">有关支持格式的信息，请参阅[标准](/dotnet/standard/base-types/standard-date-and-time-format-strings)和[自定义](/dotnet/standard/base-types/custom-date-and-time-format-strings)。</span><span class="sxs-lookup"><span data-stu-id="312d5-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="312d5-106">语法 1</span><span class="sxs-lookup"><span data-stu-id="312d5-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="312d5-107">语法 2</span><span class="sxs-lookup"><span data-stu-id="312d5-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="312d5-108">参数</span><span class="sxs-lookup"><span data-stu-id="312d5-108">Arguments</span></span>

<span data-ttu-id="312d5-109">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="312d5-109">`text`: *String*</span></span>

<span data-ttu-id="312d5-110">代表要设定格式的值的文本。</span><span class="sxs-lookup"><span data-stu-id="312d5-110">Text that represents the value to format.</span></span>

<span data-ttu-id="312d5-111">`format`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="312d5-111">`format`: *String*</span></span>

<span data-ttu-id="312d5-112">给定文本的格式。</span><span class="sxs-lookup"><span data-stu-id="312d5-112">The format of the given text.</span></span>

<span data-ttu-id="312d5-113">`culture`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="312d5-113">`culture`: *String*</span></span>

<span data-ttu-id="312d5-114">用于设定给定文本的格式的区域性。</span><span class="sxs-lookup"><span data-stu-id="312d5-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="312d5-115">返回值</span><span class="sxs-lookup"><span data-stu-id="312d5-115">Return values</span></span>

<span data-ttu-id="312d5-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="312d5-116">*DateTime*</span></span>

<span data-ttu-id="312d5-117">生成的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="312d5-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="312d5-118">使用说明</span><span class="sxs-lookup"><span data-stu-id="312d5-118">Usage notes</span></span>

<span data-ttu-id="312d5-119">当区域性未被定义为被调用函数的参数时，`culture` 由调用上下文定义。</span><span class="sxs-lookup"><span data-stu-id="312d5-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="312d5-120">例如，如果对于配置为使用德国区域性的 **FILE** 元素，以电子申报 (ER) 格式使用语法 1 调用 `DATETIMEVALUE` 函数，则将使用德国区域性完成转换。</span><span class="sxs-lookup"><span data-stu-id="312d5-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="312d5-121">默认 `culture` 值为 **EN-US**。</span><span class="sxs-lookup"><span data-stu-id="312d5-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="312d5-122">示例 1</span><span class="sxs-lookup"><span data-stu-id="312d5-122">Example 1</span></span>

<span data-ttu-id="312d5-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` 基于指定的自定义格式和默认的应用程序的 **EN-US** 区域性返回 **2:55:00 AM on December 21, 2016**。</span><span class="sxs-lookup"><span data-stu-id="312d5-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="312d5-124">示例 2</span><span class="sxs-lookup"><span data-stu-id="312d5-124">Example 2</span></span>

<span data-ttu-id="312d5-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` 基于指定的自定义格式和区域性返回 **2:55:00 AM on December 21, 2016**。</span><span class="sxs-lookup"><span data-stu-id="312d5-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="312d5-126">但是，`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` 将引发异常，以通知用户指定字符串无法识别为指定区域性的有效日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="312d5-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="312d5-127">其他资源</span><span class="sxs-lookup"><span data-stu-id="312d5-127">Additional resources</span></span>

[<span data-ttu-id="312d5-128">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="312d5-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]