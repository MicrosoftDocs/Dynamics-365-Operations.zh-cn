---
title: ROUNDUP ER 函数
description: 本主题提供有关 ROUNDUP 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 83262a11f92a924e5e49461cf414fb07ab278541
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744495"
---
# <a name="roundup-er-function"></a>ROUNDUP ER 函数

[!include [banner](../includes/banner.md)]

`ROUNDUP` 函数作为*实数*值返回已向上舍入到指定小数位数的指定数字。

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
