---
title: DAYOFYEAR ER 函数
description: 本主题提供有关 DAYOFYEAR 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: d24aabb582151b0b357b64a988cc932a9c9f3cea
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070659"
---
# <a name="DAYOFYEAR">DAYOFYEAR ER 函数</a>

[!include [banner](../includes/banner.md)]

`DAYOFYEAR` 函数返回一个*整数*值，此值表示 1 月 1 日到指定日期之间的天数。

## <a name="syntax"></a>语法

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>参数

`date`：*日期*

表示用于计算天数的日期的日期值。

## <a name="return-values"></a>返回值

*整数*

生成的数字值。

## <a name="example-1"></a>示例 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` 将返回 **61**。

## <a name="example-2"></a>示例 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` 将返回 **1**。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)
