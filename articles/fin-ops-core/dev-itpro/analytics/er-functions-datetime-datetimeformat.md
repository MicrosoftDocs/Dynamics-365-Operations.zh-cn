---
title: DATETIMEFORMAT ER 函数
description: 本主题提供有关 DATETIMEFORMAT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 8044f81ee59af4a11bfab38525afdac5a46acd2c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891249"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="e5698-103">DATETIMEFORMAT ER 函数</span><span class="sxs-lookup"><span data-stu-id="e5698-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5698-104">`DATETIMEFORMAT` 函数返回一个 *字符串* 值，此值以指定格式和指定的[区域性](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)（可选）将给定日期/时间值显示为文本。</span><span class="sxs-lookup"><span data-stu-id="e5698-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="e5698-105">有关支持格式的信息，请参阅[标准](/dotnet/standard/base-types/standard-date-and-time-format-strings)和[自定义](/dotnet/standard/base-types/custom-date-and-time-format-strings)。</span><span class="sxs-lookup"><span data-stu-id="e5698-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="e5698-106">语法 1</span><span class="sxs-lookup"><span data-stu-id="e5698-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="e5698-107">语法 2</span><span class="sxs-lookup"><span data-stu-id="e5698-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="e5698-108">参数</span><span class="sxs-lookup"><span data-stu-id="e5698-108">Arguments</span></span>

<span data-ttu-id="e5698-109">`datetime`：*日期时间*</span><span class="sxs-lookup"><span data-stu-id="e5698-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="e5698-110">表示要设定格式的日期和时间的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="e5698-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="e5698-111">`format`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="e5698-111">`format`: *String*</span></span>

<span data-ttu-id="e5698-112">输出字符串的格式。</span><span class="sxs-lookup"><span data-stu-id="e5698-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="e5698-113">当您使用标准格式或自定义格式时，格式字符串区分大小写。</span><span class="sxs-lookup"><span data-stu-id="e5698-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="e5698-114">例如，[标准](/dotnet/standard/base-types/standard-date-and-time-format-strings)“d”格式说明符使用短日期模式返回日期，而标准“D”格式说明符使用长日期模式返回日期。</span><span class="sxs-lookup"><span data-stu-id="e5698-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="e5698-115">而且，[自定义](/dotnet/standard/base-types/custom-date-and-time-format-strings)“M”格式说明符返回月份 1 到 12，而自定义“m”格式说明符返回分钟 0 到 59。</span><span class="sxs-lookup"><span data-stu-id="e5698-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="e5698-116">`culture`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="e5698-116">`culture`: *String*</span></span>

<span data-ttu-id="e5698-117">用于设定格式的区域性。</span><span class="sxs-lookup"><span data-stu-id="e5698-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="e5698-118">返回值</span><span class="sxs-lookup"><span data-stu-id="e5698-118">Return values</span></span>

<span data-ttu-id="e5698-119">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e5698-119">*String*</span></span>

<span data-ttu-id="e5698-120">生成的字符串值。</span><span class="sxs-lookup"><span data-stu-id="e5698-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e5698-121">使用说明</span><span class="sxs-lookup"><span data-stu-id="e5698-121">Usage notes</span></span>

<span data-ttu-id="e5698-122">如果区域性未被定义为被调用函数的参数，`culture` 由调用上下文定义。</span><span class="sxs-lookup"><span data-stu-id="e5698-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="e5698-123">例如，如果对于配置为使用德国区域性的 **FILE** 元素，以电子申报 (ER) 格式使用语法 1 调用 `DATETIMEFORMAT` 函数，则将使用德国区域性完成转换。</span><span class="sxs-lookup"><span data-stu-id="e5698-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="e5698-124">默认 `culture` 值为 **EN-US**。</span><span class="sxs-lookup"><span data-stu-id="e5698-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="e5698-125">当 `DATETIMEFORMAT` 函数转换给定的日期/时间值时，它将考虑正在运行 ER 格式（调用该函数的上下文的 ER 格式）的应用程序用户的时区设置。</span><span class="sxs-lookup"><span data-stu-id="e5698-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="e5698-126">示例 1</span><span class="sxs-lookup"><span data-stu-id="e5698-126">Example 1</span></span>

<span data-ttu-id="e5698-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` 根据指定的自定义格式返回当前应用程序服务器日期/时间值 2015 年 12 月 24 日为 **"24-12-2015"**。</span><span class="sxs-lookup"><span data-stu-id="e5698-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="e5698-128">示例 2</span><span class="sxs-lookup"><span data-stu-id="e5698-128">Example 2</span></span>

<span data-ttu-id="e5698-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` 根据所选的德国区域性和指定格式，返回当前应用程序会话的日期/时间值 2015 年 12 月 24 日为 **"24.12.2015"**。</span><span class="sxs-lookup"><span data-stu-id="e5698-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="e5698-130">示例 3</span><span class="sxs-lookup"><span data-stu-id="e5698-130">Example 3</span></span>

<span data-ttu-id="e5698-131">当此函数在 **语言和国家/地区首选项** 部分具有时区值 **(GMT-08:00)太平洋时间(美国和加拿大)** 的应用程序用户启动的流程中调用时，`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` 返回字符串值 **2019-11-12T08:00:00.0000000-08:00**。</span><span class="sxs-lookup"><span data-stu-id="e5698-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5698-132">其他资源</span><span class="sxs-lookup"><span data-stu-id="e5698-132">Additional resources</span></span>

[<span data-ttu-id="e5698-133">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="e5698-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]