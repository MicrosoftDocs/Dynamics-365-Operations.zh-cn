---
title: ROUNDUP ER 函数
description: 本文提供有关 ROUNDUP 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 5266b0f74f348d936bde8948770e48dbbf9bb4f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268017"
---
# <a name="roundup-er-function"></a>ROUNDUP ER 函数

[!include [banner](../includes/banner.md)]

`ROUNDUP` 函数作为 *实数* 值返回已向上舍入到指定小数位数的指定数字。

## <a name="syntax"></a>语法

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>参数

`number`：*实数*

必须向上舍入的数值。

`decimals`：*整数*

代表小数位数的数字值。

## <a name="return-values"></a>返回值

*实数*

生成的数字值。

## <a name="usage-notes"></a>使用说明

此函数类似 [ROUND](er-functions-mathematical-round.md)，但始终向上（不朝零）化整到指定的数字。

## <a name="example-1"></a>示例 1

`ROUNDUP (1200.763, 2)` 向上舍入到两位小数，返回 **1200.77**。

## <a name="example-2"></a>示例 2

`ROUNDUP (1200.767, -3)` 向上舍入到最接近的 1,000 的倍数，返回 **2000**。

## <a name="additional-resources"></a>其他资源

[数学函数](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
