---
title: AND ER 函数
description: 本主题提供有关 AND 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 4a246496eca0d5a8538ac7f1577957e6b9eae4e3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743462"
---
# <a name="and-er-function"></a>AND ER 函数

[!include [banner](../includes/banner.md)]

`AND` 函数返回一个*布尔*值 **TRUE**（如果所有指定条件都为 true）。 否则，返回*布尔*值 **FALSE**。

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

生成的*布尔*值。

## <a name="usage-notes"></a>使用说明

在逻辑函数的参数中，可以使用数据源引用、数字和文本值、布尔值、比较运算符以及其他电子申报 (ER) 函数。 但是，必须将所有参数评估为*布尔*值 **TRUE** 或 **FALSE**。

## <a name="example"></a>示例

`AND (1=1, "a"="a")` 返回 **TRUE**。

`AND (1=2, "a"="a")` 返回 **FALSE**。

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)
