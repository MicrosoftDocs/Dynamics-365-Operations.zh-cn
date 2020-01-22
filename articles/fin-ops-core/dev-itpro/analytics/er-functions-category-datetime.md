---
title: 日期和时间类别的 ER 函数列表
description: 本主题提供有关电子申报 (ER) 支持的日期和时间函数的信息。
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916560"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="a5538-103">日期和时间类别的 ER 函数列表</span><span class="sxs-lookup"><span data-stu-id="a5538-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5538-104">电子申报 (ER) 日期和时间函数可用于从日期和时间值中提取信息，并可以对这些值执行操作。</span><span class="sxs-lookup"><span data-stu-id="a5538-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="a5538-105">本主题提供这些函数的概要。</span><span class="sxs-lookup"><span data-stu-id="a5538-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="a5538-106">支持的函数列表</span><span class="sxs-lookup"><span data-stu-id="a5538-106">List of supported functions</span></span>

| <span data-ttu-id="a5538-107">职能</span><span class="sxs-lookup"><span data-stu-id="a5538-107">Function</span></span> | <span data-ttu-id="a5538-108">说明</span><span class="sxs-lookup"><span data-stu-id="a5538-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="a5538-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="a5538-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="a5538-110">此函数返回一个*日期时间*值，此值是指定开始日期之前或之后的指定的天数。</span><span class="sxs-lookup"><span data-stu-id="a5538-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="a5538-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="a5538-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="a5538-112">此函数返回一个*字符串*值，此值以指定格式和指定的区域性（可选）将给定日期值显示为文本。</span><span class="sxs-lookup"><span data-stu-id="a5538-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="a5538-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a5538-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="a5538-114">此函数返回一个*字符串*值，此值以指定格式和指定的区域性（可选）将给定日期/时间值显示为文本。</span><span class="sxs-lookup"><span data-stu-id="a5538-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="a5538-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="a5538-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="a5538-116">此函数返回一个*日期时间*值，此值从指定格式和指定的区域性（可选）的给定文本值转换为日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="a5538-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="a5538-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="a5538-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="a5538-118">此函数返回一个*日期时间*值，此值从给定日期/时间值转换为协调世界时（格林威治标准时间 \[GMT\]）的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="a5538-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="a5538-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="a5538-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="a5538-120">此函数返回一个*日期*值，此值从指定格式和指定的区域性（可选）的给定文本值转换为日期值。</span><span class="sxs-lookup"><span data-stu-id="a5538-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="a5538-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="a5538-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="a5538-122">此函数返回一个*整数*值，此值表示 1 月 1 日到指定日期之间的天数。</span><span class="sxs-lookup"><span data-stu-id="a5538-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="a5538-123">天数</span><span class="sxs-lookup"><span data-stu-id="a5538-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="a5538-124">此函数返回一个*整数*值，此值表示一个指定日期至第二个指定日期之间的天数。</span><span class="sxs-lookup"><span data-stu-id="a5538-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="a5538-125">Now</span><span class="sxs-lookup"><span data-stu-id="a5538-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="a5538-126">此函数返回一个*日期时间*值，此值表示当前应用程序服务器的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a5538-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="a5538-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="a5538-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="a5538-128">此函数返回一个表示**空**日期（1900 年 1 月 1 日）的*日期*值。</span><span class="sxs-lookup"><span data-stu-id="a5538-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="a5538-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="a5538-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="a5538-130">此函数返回一个*日期时间*值，此值表示协调世界时的**空**日期/时间值（1900 年 1 月 1 日）。</span><span class="sxs-lookup"><span data-stu-id="a5538-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="a5538-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="a5538-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="a5538-132">此函数返回一个*日期时间*值，此值表示当前应用程序会话的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="a5538-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="a5538-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="a5538-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="a5538-134">此函数返回一个*日期*值，此值表示当前应用程序会话的日期。</span><span class="sxs-lookup"><span data-stu-id="a5538-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="a5538-135">今天</span><span class="sxs-lookup"><span data-stu-id="a5538-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="a5538-136">此函数返回一个*日期*值，此值表示当前应用程序服务器的日期。</span><span class="sxs-lookup"><span data-stu-id="a5538-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a5538-137">其他资源</span><span class="sxs-lookup"><span data-stu-id="a5538-137">Additional resources</span></span>

[<span data-ttu-id="a5538-138">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="a5538-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="a5538-139">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="a5538-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="a5538-140">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="a5538-140">Electronic reporting formula language</span></span>](er-formula-language.md)
