---
title: OR ER 函数
description: 本主题提供有关 OR 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: f6751c70599b5e3c05b9d1c69a95e82673b230210170cfead1e6a87c57d59c7f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747561"
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