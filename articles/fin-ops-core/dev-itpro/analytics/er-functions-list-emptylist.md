---
title: EMPTYLIST ER 函数
description: 本文提供有关 EMPTYLIST 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 5fd14456a615d5dc6fb565f4bed523db5432c871
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268107"
---
# <a name="emptylist-er-function"></a>EMPTYLIST ER 函数

[!include [banner](../includes/banner.md)]

`EMPTYLIST` 函数通过使用指定的列表作为列表结构的来源返回空 *记录列表* 值。

## <a name="syntax"></a>语法

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="example"></a>示例

`EMPTYLIST (SPLIT ("abc", 1))` 返回具有与使用的 `SPLIT` 函数返回的列表相同结构的新空列表。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
