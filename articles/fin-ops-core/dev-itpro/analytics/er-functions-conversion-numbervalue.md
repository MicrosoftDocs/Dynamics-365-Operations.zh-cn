---
title: NUMBERVALUE ER 函数
description: 本主题提供有关 NUMBERVALUE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 80f0606dc3842cdfa56d41e2815eccd7518218b8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916514"
---
# <a name="NUMBERVALUE">NUMBERVALUE ER 函数</a>

[!include [banner](../includes/banner.md)]

`NUMBERVALUE` 函数返回一个*实数*值，该值从指定的*字符串*值转换而来。 在转换过程中，将考虑指定的十进制和数字分组分隔符。

## <a name="syntax"></a>语法

```
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>参数

`text`：*字符串*

必须转换为*实数*数字的文本值。

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