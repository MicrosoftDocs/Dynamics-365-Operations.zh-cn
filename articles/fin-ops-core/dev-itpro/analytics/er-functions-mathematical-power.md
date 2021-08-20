---
title: POWER ER 函数
description: 本主题提供有关 POWER 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 6955d2787b2a9be6d38fe10165a9d5ef8310b108e3a9772709d9d1ff51712424
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6767136"
---
# <a name="power-er-function"></a>POWER ER 函数

[!include [banner](../includes/banner.md)]

`POWER` 函数返回一个 *实数* 值，其代表将指定正数提高到指定幂的结果的值。

## <a name="syntax"></a>语法

```vb
POWER (number, power)
```

## <a name="arguments"></a>参数

`number`：*实数* 或 *整数*

必须提高到指定幂的数值。

`power`：*实数* 或 *整数*

代表特定幂的数值。

## <a name="return-values"></a>返回值

*实数*

生成的数字值。

## <a name="example-1"></a>示例 1

`POWER (10, 2)` 将返回 **100**。

## <a name="example-2"></a>示例 2

`POWER (4, 0.5)` 将返回 **2**。

## <a name="additional-resources"></a>其他资源

[数学函数](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]