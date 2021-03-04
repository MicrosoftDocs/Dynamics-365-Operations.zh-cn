---
title: OR ER 函数
description: 本主题提供有关 OR 电子申报 (ER) 函数如何使用的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686970"
---
# <a name="or-er-function"></a>OR ER 函数

[!include [banner](../includes/banner.md)]

`OR` 函数返回一个 *布尔* 值 **FALSE**（如果所有指定条件都为 false）。 如果所有指定条件都为 true，此函数返回一个 *布尔* 值 **TRUE**。

## <a name="syntax"></a>语法

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>参数

`condition 1`：*布尔值*

必须测试的有效条件表达式。 此参数是必需的。

`condition N`：*布尔值*

必须测试的有效条件表达式。 其他参数是可选的。

## <a name="return-values"></a>返回值

*布尔值*

生成的 *布尔* 值。

## <a name="example"></a>示例

`OR (1=2, "a"="a")` 返回 **TRUE**。

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]