---
title: MID ER 函数
description: 本文提供有关 MID 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: ca5dbfb6de3057ad2c4a6dcc7ecce3d0ddc69595
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867631"
---
# <a name="mid-er-function"></a>MID ER 函数

[!include [banner](../includes/banner.md)]

`MID` 函数返回 *字符串* 值，该值在指定位置的开始处，在指定的字符串中显示指定的字符数量。

## <a name="syntax"></a>语法

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>参数

`text`：*字符串*

指定要从中返回字符的文本的 *字符串* 值。

`starting position`：*整数*

指定必须从指定文本返回的第一个字符的位置的 *整数* 值。

`number of characters`：*整数*

指定必须从指定开始位置开始返回的字符数量的 *整数* 值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

如果 `starting position` 参数的值小于 0（零），返回的字符从指定字符串中的第一个位置开始计数。

如果 `starting position` 参数的值超过指定字符串的长度，将返回一个空字符串。

## <a name="example"></a>示例

`MID ("Sample", 2, 3)` 返回 **"amp"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]