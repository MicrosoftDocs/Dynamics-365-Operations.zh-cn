---
title: COUNT ER 函数
description: 本主题提供有关 COUNT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: a0b780051684ef52d06a9baf78d9b513d9ac1f0e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746619"
---
# <a name="count-er-function"></a>COUNT ER 函数

[!include [banner](../includes/banner.md)]

`COUNT` 函数返回一个表示指定列表中的记录数的 *整数* 值（如果列表不为空）。 如果列表为空，此函数返回 **0**（零）。

## <a name="syntax"></a>语法

```vb
COUNT (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*整数*

生成的数字值。

## <a name="example"></a>示例

`COUNT (SPLIT("abcd" , 3))` 返回 **2**，因为本示例中使用的 `SPLIT` 函数创建一个包含两个记录的列表。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]