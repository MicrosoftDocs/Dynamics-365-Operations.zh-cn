---
title: INTVALUE ER 函数
description: 本文提供有关 INTVALUE 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: e2357541f922ad9af5c5ce342d0e7d89e8709734
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879882"
---
# <a name="intvalue-er-function"></a>INTVALUE ER 函数

[!include [banner](../includes/banner.md)]

`INTVALUE` 函数返回一个 *Int* 值，该值表示指定的字符串。

## <a name="syntax-1"></a>语法 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>语法 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>参数

`text`：*字符串*

必须转换为 *Int* 数字的文本值。

`number`：*实数* 或 *整数*

必须转换为 *Int* 数字的 *实数* 或 *整数* 数字值。

## <a name="return-values"></a>返回值

*Int*

生成的数字值。

## <a name="usage-notes"></a>使用说明

将截断所有小数部分。

## <a name="example-1"></a>示例 1

`INTVALUE ("100.77")` 返回 *Int* 值 **100**。

## <a name="example-2"></a>示例 2

`INTVALUE (-100.77)` 返回 *Int* 值 **-100**。

## <a name="additional-resources"></a>其他资源

[类型转换函数](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]