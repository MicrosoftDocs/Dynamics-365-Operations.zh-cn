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
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>日期和时间类别的 ER 函数列表

[!include [banner](../includes/banner.md)]

电子申报 (ER) 日期和时间函数可用于从日期和时间值中提取信息，并可以对这些值执行操作。 本主题提供这些函数的概要。

## <a name="list-of-supported-functions"></a>支持的函数列表

| 职能 | 说明 |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | 此函数返回一个*日期时间*值，此值是指定开始日期之前或之后的指定的天数。 |
| [DateFormat](er-functions-datetime-dateformat.md) | 此函数返回一个*字符串*值，此值以指定格式和指定的区域性（可选）将给定日期值显示为文本。 |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | 此函数返回一个*字符串*值，此值以指定格式和指定的区域性（可选）将给定日期/时间值显示为文本。 |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | 此函数返回一个*日期时间*值，此值从指定格式和指定的区域性（可选）的给定文本值转换为日期/时间值。 |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | 此函数返回一个*日期时间*值，此值从给定日期/时间值转换为协调世界时（格林威治标准时间 \[GMT\]）的日期/时间值。 |
| [DateValue](er-functions-datetime-datevalue.md) | 此函数返回一个*日期*值，此值从指定格式和指定的区域性（可选）的给定文本值转换为日期值。 |
| [DayOfYear](er-functions-datetime-dayofyear.md) | 此函数返回一个*整数*值，此值表示 1 月 1 日到指定日期之间的天数。 |
| [天数](er-functions-datetime-days.md) | 此函数返回一个*整数*值，此值表示一个指定日期至第二个指定日期之间的天数。 |
| [Now](er-functions-datetime-now.md) | 此函数返回一个*日期时间*值，此值表示当前应用程序服务器的日期和时间。 |
| [NullDate](er-functions-datetime-nulldate.md) | 此函数返回一个表示**空**日期（1900 年 1 月 1 日）的*日期*值。 |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | 此函数返回一个*日期时间*值，此值表示协调世界时的**空**日期/时间值（1900 年 1 月 1 日）。 |
| [SessionNow](er-functions-datetime-sessionnow.md) | 此函数返回一个*日期时间*值，此值表示当前应用程序会话的日期和时间。 |
| [SessionToday](er-functions-datetime-sessiontoday.md) | 此函数返回一个*日期*值，此值表示当前应用程序会话的日期。 |
| [今天](er-functions-datetime-today.md) | 此函数返回一个*日期*值，此值表示当前应用程序服务器的日期。 |

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[电子申报公式语言](er-formula-language.md)
