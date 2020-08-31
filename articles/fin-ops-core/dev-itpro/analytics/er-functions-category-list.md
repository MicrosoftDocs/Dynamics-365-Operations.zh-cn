---
title: 列表类别的 ER 函数列表
description: 本主题提供有关电子申报 (ER) 支持的列表函数的信息。
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
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e51d9a1d68c48391a223fe48f396c63c206580e
ms.sourcegitcommit: 41e165482b9bff4175c0e3b224dbeead13461956
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/11/2020
ms.locfileid: "3687950"
---
# <a name="list-of-er-functions-in-the-list-category"></a>列表类别的 ER 函数列表

[!include [banner](../includes/banner.md)]

电子申报 (ER) 列表函数可用于从*记录列表*和*容器（记录）* 数据类型的数据源提取信息，并对数据源执行操作。 本主题提供这些函数的概要。

## <a name="list-of-supported-functions"></a>支持的函数列表

| 职能 | 说明 |
|----------|-------------|
| [AllItems](er-functions-list-allitems.md)                 | 此函数作为内存内选择运行。 它返回一个新的平展*记录列表*值，此值由代表与指定路径匹配的所有项目的记录的列表组成。 |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | 此函数返回一个联接的 SQL 查询。 它返回一个新的平展*记录列表*值，此值由代表与指定路径匹配的所有项目的记录的列表组成。 |
| [盘点](er-functions-list-count.md)                       | 此函数返回一个表示指定列表中的记录数的*整数*值（如果列表不为空）。 如果列表为空，此函数返回 **0**（零）。 |
| [EmptyList](er-functions-list-emptylist.md)               | 此函数通过使用指定的列表作为列表结构的来源返回空*记录列表*值。|
| [枚举](er-functions-list-enumerate.md)               | 此函数返回一个新的*记录列表*值，此值由指定列表的枚举记录组成。 |
| [筛选器](er-functions-list-filter.md)                     | 此函数在查询更改以针对指定条件进行筛选后作为*记录列表*值返回指定列表。 |
| [第一页](er-functions-list-first.md)                       | 此函数返回指定列表的第一条记录为*容器（记录）* 值（如果该列表不为空）。 如果列表为空，此函数将引发异常。 |
| [FirstOrNull](er-functions-list-firstornull.md)           | 此函数返回指定列表的第一条记录为*容器（记录）* 值（如果该记录不为空）。 如果记录为空，此函数将返回空*容器（记录）* 值。 |
| [索引](er-functions-list-index.md)                       | 此函数返回使用指定列表中的指定数字索引选择的*容器（记录）* 值。 如果索引超出指定列表中记录的范围，此函数将引发异常。 |
| [IsEmpty](er-functions-list-isempty.md)                   | 此函数返回一个*布尔*值 **TRUE**（如果指定列表未包含记录）。 否则，返回*布尔*值 **FALSE**。 |
| [列表](er-functions-list-list.md)                         | 此函数返回一个*记录列表*值，此值由根据指定参数创建的新列表组成。|
| [ListDistinct](er-functions-list-listdistinct.md)         | 此函数将指定表达式计算为指定列表的每个记录的选择器。 将返回新的*记录列表*值，其中包含每个唯一选择器值的单个记录。|
| [ListJoin](er-functions-list-listjoin.md)                 | 此函数返回一个*记录列表*值，此值表示根据指定参数创建的新连接列表。|
| [ListOfFields](er-functions-list-listoffields.md)         | 此函数返回一个*记录列表*值，此值基于指定的*枚举*或*容器（记录）* 类型的参数的结构创建。 |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | 此函数返回一个*记录列表*值，此值仅包含指定列表的第一条记录。|
| [OrderBy](er-functions-list-orderby.md)                   | 在根据指定的参数对指定列表进行排序之后，此函数将指定列表返回为*记录列表*值。 可将这些变量定义为表达式。 |
| [冲销](er-functions-list-reverse.md)                   | 此函数以相反的排序顺序将指定列表返回为*记录列表*值。 |
| [拆分](er-functions-list-split.md)                       | 此函数将指定的输入字符串拆分为子字符串，并将结果作为新的*记录列表*值返回。 |
| [SplitList](er-functions-list-splitlist.md)               | 此函数将指定的列表拆分为多个子列表（或批次），每个批次包含指定的记录数。 然后作为包含批次的新*记录列表*值返回结果。 |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | 此函数将指定列表拆分为新的子列表（批次）列表。 每个批次中的记录数是动态计算的。 然后此函数作为包含批次的新*记录列表*值返回结果。 |
| [StringJoin](er-functions-list-stringjoin.md)             | 此函数返回由指定列表中的指定字段的连接值组成的*字符串*值。 这些值可以通过指定分隔符分隔。 |
| [位置](er-functions-list-where.md)                       | 在根据指定的参数对指定列表进行筛选之后，此函数将指定的条件返回为*记录列表*值。 |

## <a name="additional-resources"></a>其他资源

[电子申报概览](general-electronic-reporting.md)

[电子报告中的配方设计器](general-electronic-reporting-formula-designer.md)

[电子申报公式语言](er-formula-language.md)
