---
title: AND ER 函数
description: 本文提供有关 AND 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: d20e7c64f28082bae4b1319f479a95ee7d69d76b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284105"
---
# <a name="and-er-function"></a>AND ER 函数

[!include [banner](../includes/banner.md)]

`AND` 函数返回一个 *布尔* 值 **TRUE**（如果所有指定条件都为 true）。 否则，返回 *布尔* 值 **FALSE**。

## <a name="syntax"></a>语法

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>参数

`condition 1`：*布尔值*

必须测试的有效条件表达式。 此参数是必需的。

`condition N`：*布尔值*

必须测试的有效条件表达式。 其他参数是可选的。

## <a name="return-values"></a>返回值

*布尔值*

生成的 *布尔* 值。

## <a name="usage-notes"></a>使用说明

在逻辑函数的参数中，可以使用数据源引用、数字和文本值、布尔值、比较运算符以及其他电子申报 (ER) 函数。 但是，必须将所有参数评估为 *布尔* 值 **TRUE** 或 **FALSE**。

## <a name="example"></a>示例

`AND (1=1, "a"="a")` 返回 **TRUE**。

`AND (1=2, "a"="a")` 返回 **FALSE**。

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
