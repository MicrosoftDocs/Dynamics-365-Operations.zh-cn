---
title: ROUNDDOWN ER 函数
description: 本主题提供有关 ROUNDDOWN 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: ef7d81852a0bbb84fd8f37cd89555766cc47f5f8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915847"
---
# <a name="ROUNDDOWN">ROUNDDOWN ER 函数</a>

[!include [banner](../includes/banner.md)]

`ROUNDDOWN` 函数作为*实数*值返回已向下舍入到指定小数位数的指定数字。

## <a name="syntax"></a>语法

```
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>参数

`number`：*实数*

必须向下舍入的数值。

`decimals`：*整数*

代表小数位数的数字值。

## <a name="return-values"></a>返回值

*实数*

生成的数字值。

## <a name="usage-notes"></a>使用说明

此函数类似 [ROUND](er-functions-mathematical-round.md)，但始终向下（朝零）化整到指定的数字。

## <a name="example-1"></a>示例 1

`ROUNDDOWN (1200.767, 2)` 向下舍入到两位小数，返回 **1200.76**。 

## <a name="example-2"></a>示例 2

`ROUNDDOWN (1700.767, -3)` 向下舍入到最接近的 1,000 的倍数，返回 **1000**。

## <a name="additional-resources"></a>其他资源

[数学函数](er-functions-category-mathematical.md)
