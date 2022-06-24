---
title: POWER ER 函数
description: 本文提供有关 POWER 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: da3ae988b57cb5588de1e2fd8ee962b77b5534ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864679"
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