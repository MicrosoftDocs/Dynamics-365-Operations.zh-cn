---
title: NUMBERVALUE ER 函数
description: 本主题提供有关 NUMBERVALUE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: f542621c4bcc29e03d8c92b0c700e2c80c9846f6
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561414"
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