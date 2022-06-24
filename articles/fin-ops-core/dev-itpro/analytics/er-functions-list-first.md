---
title: FIRST ER 函数
description: 本文提供有关 FIRST 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: a1f841fe11f025be95ffee2750da74ad7be51624
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906567"
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