---
title: FIRSTORNULL ER 函数
description: 本文说明 FIRSTORNULL 电子报告 (ER) 函数如何使用
author: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: 7ee1a5c1b6ac13581608f9adbda42fae0706d225
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273179"
---
# <a name="firstornull-er-function"></a>FIRSTORNULL ER 函数

[!include [banner](../includes/banner.md)]

`FIRSTORNULL` 函数返回指定列表的第一条记录为 *容器（记录）* 值（如果该记录不为空）。 如果记录为空，此函数将返回空 *容器（记录）* 值。

## <a name="syntax"></a>语法

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*容器（记录）*

生成的记录值。

## <a name="example"></a>示例

表达式 `FIRSTORNULL(SPLIT("",1)).Value` 返回一个空字符串 (**""**)。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
