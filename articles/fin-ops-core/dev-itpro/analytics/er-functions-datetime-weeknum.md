---
title: WEEKNUM ER 函数
description: 本文提供有关 WEEKNUM 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: 2c6eef0d6e1f90a3f8d382591edad3d568da84ec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858761"
---
# <a name="weeknum-er-function"></a>WEEKNUM ER 函数

[!include [banner](../includes/banner.md)]

`WEEKNUM` 函数返回一个 *[整数](er-formula-supported-data-types-primitive.md#integer)* 值，此值表示包含指定 *[日期](er-formula-supported-data-types-primitive.md#date)* 值的一年中的第几周。 计算基于定义日历周和一周的第一天的区域性相关规则。

## <a name="syntax"></a>语法

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">参数</a>

`date`：*日期*

一个日期值，表示用于计算一年中的第几周的日期。

`culture`：*[字符串](er-formula-supported-data-types-primitive.md#string)*

用于计算的区域性。 您可以使用根据 .NET [标准](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0)支持的区域性代码。

## <a name="return-values"></a>返回值

*整数*

生成的数字值。

## <a name="usage-notes"></a>使用说明

如果 [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) 标准已被在运行时提供区域设置的国家或地区采用，一年中的第几周将基于此标准计算。 否则，计算基于国家/地区特定的国家标准。

如果在运行时将不受支持的[区域性](#arguments)代码作为 `WEEKNUM` 函数的参数提供，将会引发异常。 如果提供空白字符串作为区域性代码，将使用英语国家/地区中性日历来计算周数。

## <a name="examples"></a>示例

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` 将返回 **1**。

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` 将返回 **53**。

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` 将返回 **52**。

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` 将返回 **21**。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
