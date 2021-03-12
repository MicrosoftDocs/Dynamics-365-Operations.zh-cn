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
ms.openlocfilehash: eb2d4ab3434a563e907f6540809888cd3f671c1a
ms.sourcegitcommit: fcc4596eeadac5dfe9a3242afa49b9b1c0c96575
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/15/2020
ms.locfileid: "4740800"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>类型转换类别的 ER 函数列表

[!include [banner](../includes/banner.md)]

电子申报 (ER) 类型转换函数可用于在类型之间转换值。 本主题提供这些函数的概要。

## <a name="type-conversion-functions"></a>类型转换函数

| 职能 | 说明 |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | 此函数返回一个 *Int64* 值，该值表示指定的字符串。 |
| [IntValue](er-functions-conversion-intvalue.md)       | 此函数返回一个 *Int* 值，该值表示指定的字符串。 |
| [NumberValue](er-functions-conversion-numbervalue.md) | 此函数返回一个 *实数* 值，该值从指定的 *字符串* 值转换而来。 在转换过程中，将考虑指定的十进制和数字分组分隔符。 |
| [值](er-functions-conversion-value.md)             | 此函数返回一个 *实数* 值，该值从指定的 *字符串* 值转换而来。 |

## <a name="type-conversion-functions-in-the-container-category"></a>容器类别的类型转换函数

下表描述了[容器](er-functions-category-container.md)类别的类型转换函数。

| 函数 | 说明 |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | 此函数将 *字符串* 类型的指定输入转换为 *容器* 类型的数据项。 |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>日期和时间类别的类型转换函数

下表描述了[日期和时间类别](er-functions-category-datetime.md)的类型转换函数。

| 职能 | 说明 |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | 此函数返回一个 *日期时间* 值，此值从指定格式和指定的区域性（可选）的给定 *字符串* 值转换为日期/时间值。 |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | 此函数返回一个 *日期时间* 值，此值从给定日期/时间值转换为协调世界时（格林威治标准时间 \[GMT\]）的 *日期* 值。 |
| [DateValue](er-functions-datetime-datevalue.md)           | 此函数返回一个 *日期* 值，此值从指定格式和指定的区域性（可选）的给定 *字符串* 值转换为日期值。 |

## <a name="type-conversion-functions-in-the-list-category"></a>列表类别的类型转换函数

下表描述了[列表类别](er-functions-category-list.md)的类型转换函数。

| 职能 | 说明 |
|----------|-------------|
| [列表](er-functions-list-list.md)                 | 此函数作为从指定的 *容器（记录）* 类型的参数创建的新列表，返回一个 *记录列表* 值。 |
| [ListOfFields](er-functions-list-listoffields.md) | 此函数返回一个 *记录列表* 值，此值基于给定的 *枚举* 或 *容器（记录）* 类型的参数的结构创建。 |
| [拆分](er-functions-list-split.md)               | 此函数将指定的 *字符串* 值拆分为子字符串，并将结果作为新的 *记录列表* 值返回。 |
| [StringJoin](er-functions-list-stringjoin.md)     | 此函数返回由指定 *记录列表* 值中的指定字段的连接值组成的 *字符串* 值。 这些值可以通过指定分隔符分隔。 |

## <a name="type-conversion-functions-in-the-text-category"></a>文本类别的类型转换函数

下表描述了[文本类别](er-functions-category-text.md)的类型转换函数。

| 职能 | 说明 |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | 此函数返一个 *字符串* 值，该值代表指定 Unicode 数值引用的单个字符。 |
| [GuidValue](er-functions-text-guidvalue.md)       | 此函数将 *字符串* 类型的指定输入转换为 *GUID* 类型的数据项。 |
| [NumberFormat](er-functions-text-numberformat.md) | 此函数返回一个 *字符串* 值，此值以指定格式和指定的区域性（可选）表示指定数字。 |
| [QrCode](er-functions-text-qrcode.md)             | 此函数返回一个 *容器* 值，该值以二进制格式显示指定字符串的快速响应代码（QR 代码）图像。 |
| [文本](er-functions-text-text.md)                 | 在将指定的数字转换为根据当前应用程序实例的服务器区域设置设定格式的文本字符串后，此函数返回表示该数字的 *字符串* 值。 |

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[电子申报公式语言](er-formula-language.md)
