---
title: LISTJOIN ER 函数
description: 本主题提供有关 LISTJOIN 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b5b82917e3083b5ffe4546a6a15fd14938383a
ms.sourcegitcommit: ff6dde637d2f5d2bd18a582eb41573d4c69acdd6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/08/2020
ms.locfileid: "3249027"
---
# <a name=""></a><a name="LISTJOIN">LISTJOIN ER 函数</a>

[!include [banner](../includes/banner.md)]

`LISTJOIN` 函数返回一个*记录列表*值，此值表示根据指定参数创建的记录的新连接列表。

## <a name="syntax"></a>语法

```vb
LIST (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>参数

`list 1`：*记录列表*

对*记录列表*数据类型的数据源的引用。 此参数是强制性的。

`list N`：*记录列表*

对*记录列表*数据类型的数据源的引用。 其他参数是可选的。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

创建的列表的结构仅包含在参数中提到的每个记录列表的结构中显示的字段。

## <a name="example"></a>示例

您输入 `Container` 类型的数据源**记录 1**。 此数据源包含 `Calculated field` 类型的以下嵌套字段：

- **代码**：此字段包含返回 `String` 类型的值的表达式。
- **金额**：此字段包含返回 `Real` 类型的值的表达式。

然后输入 `Container` 类型的数据源**记录 2**。 此数据源包含 `Calculated field` 类型的以下嵌套字段：

- **金额**：此字段包含返回 `Real` 类型的值的表达式。
- **IsValid**：此字段包含返回 `Boolean` 类型的值的表达式。

在此例中，表达式 `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` 返回包含两个记录的新列表。 此列表的结构由一个 `Real` 类型的**金额**字段组成，因为此字段是被调用函数每个参数中显示的唯一字段。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)