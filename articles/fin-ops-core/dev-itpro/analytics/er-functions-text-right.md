---
title: RIGHT ER 函数
description: 本文提供有关 RIGHT 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 99e4d3811b1df25a7f6068e0dd31836d1b402952
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895357"
---
# <a name="right-er-function"></a>RIGHT ER 函数

[!include [banner](../includes/banner.md)]

`RIGHT` 函数返回 *字符串* 值，该值在指定字符串的末尾显示指定的字符数量。

## <a name="syntax"></a>语法

```vb
RIGHT (text, number)
```

## <a name="arguments"></a>参数

`text`：*字符串*

代表原始文本的 *字符串* 值。

`number`：*整数*

必须在原始文本结尾返回的字符数。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`RIGHT ("Sample", 3)` 返回 **"ple"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]