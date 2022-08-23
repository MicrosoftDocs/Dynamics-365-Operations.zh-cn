---
title: FIRST ER 函数
description: 本文提供有关 FIRST 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: b06f07c4cfef5c74c22f60dfa37986ee88c544cf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275463"
---
# <a name="first-er-function"></a>FIRST ER 函数

[!include [banner](../includes/banner.md)]

`FIRST` 函数返回指定列表的第一条记录为 *容器（记录）* 值（如果该列表不为空）。 如果列表为空，此函数将引发异常。

## <a name="syntax"></a>语法

```vb
FIRST (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*容器（记录）*

生成的记录值。

## <a name="example-1"></a>示例 1

表达式 `FIRST(SPLIT("ABC",1)).Value` 返回文本值 **"A"**。

## <a name="example-2"></a>示例 2

表达式 `FIRST(SPLIT("",1)).Value` 在运行时引发异常。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
