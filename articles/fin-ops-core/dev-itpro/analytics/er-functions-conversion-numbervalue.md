---
title: NUMBERVALUE ER 函数
description: 本文提供有关 NUMBERVALUE 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 9701fe7a1ce2a96fa5fa8df8aeda125c861a117a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871518"
---
# <a name="numbervalue-er-function"></a>NUMBERVALUE ER 函数

[!include [banner](../includes/banner.md)]

`NUMBERVALUE` 函数返回一个 *实数* 值，该值从指定的 *字符串* 值转换而来。 在转换过程中，将考虑指定的十进制和数字分组分隔符。

## <a name="syntax"></a>语法

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>参数

`text`：*字符串*

必须转换为 *实数* 数字的文本值。

`decimal separator`：字符串

小数点分隔符。 用于分隔十进制数的整数和小数部分。

`digit grouping separator`：*字符串*

数字分组分隔符。 用作千位分隔符。

## <a name="return-values"></a>返回值

*实数*

生成的数字值。

## <a name="example"></a>示例

`NUMBERVALUE( "1 234,56", ",", " ")` 将返回 **1234.56**。

## <a name="additional-resources"></a>其他资源

[类型转换函数](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]