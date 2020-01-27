---
title: COUNT ER 函数
description: 本主题提供有关 COUNT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 2d29b82a8c3b108f7651e6d593cb17e7ec8ca872
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916238"
---
# <a name="COUNT">COUNT ER 函数</a>

[!include [banner](../includes/banner.md)]

`COUNT` 函数返回一个表示指定列表中的记录数的*整数*值（如果列表不为空）。 如果列表为空，此函数返回 **0**（零）。

## <a name="syntax"></a>语法

```
COUNT (list)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表*数据类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*整数*

生成的数字值。

## <a name="example"></a>示例

`COUNT (SPLIT("abcd" , 3))` 返回 **2**，因为本示例中使用的 `SPLIT` 函数创建一个包含两个记录的列表。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)
