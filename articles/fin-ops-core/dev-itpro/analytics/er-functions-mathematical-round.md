---
title: ROUND ER 函数
description: 本文提供有关 ROUND 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 10/21/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 57d41ed92a5577fdc5fffeccef2834e9b6fb5197
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286050"
---
# <a name="round-er-function"></a>ROUND ER 函数

[!include [banner](../includes/banner.md)]

`ROUND` 函数作为 *实数* 值返回已舍入到指定小数位数的指定数字。

## <a name="syntax"></a>语法

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>参数

`number`：*实数*

必须舍入的数值。

`decimals`：*整数*

代表小数位数的数字值。

## <a name="return-values"></a>返回值

*实数*

生成的数字值。

## <a name="usage-notes"></a>使用说明

如果 `decimals` 参数的值大于 0（零），则指定的数值舍入到这个多位小数位数。

如果 `decimals` 参数的值为 **0**（零），则指定的数值舍入到最近的偶数。

如果 `decimals` 参数的值小于 0（零），则指定的数值舍入到小数点左边。

## <a name="example-1"></a>示例 1

`ROUND (1200.767, 2)` 舍入到两位小数，返回 **1200.77**。

## <a name="example-2"></a>示例 2

`ROUND (1200.767, -3)` 舍入到最接近的 1,000 的倍数，返回 **1000**。

## <a name="example-3"></a>示例 3

`ROUND (1200.5, 0)` 舍入到最近的偶数并返回 **1200**，而 `ROUND (1201.5, 0)` 执行同样的操作并返回 **1202**。

## <a name="additional-resources"></a>其他资源

[数学函数](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
