---
title: VALUEIN ER 函数
description: 本主题提供有关 VALUEIN 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 08/18/2020
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
ms.openlocfilehash: 44459ae56891a08eb11a6c254f4b4d5652a0e693
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705111"
---
# <a name=""></a><a name="VALUEIN">VALUEIN ER 函数</a>

[!include [banner](../includes/banner.md)]

`VALUEIN` 函数确定指定的输入是否匹配指定列表中任何指定项目的值。 如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，它将返回*布尔*值 **TRUE**。 否则，返回*布尔*值 **FALSE**。

## <a name="syntax"></a>语法

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>参数

`input`：*字段*

*记录列表*类型的数据源项目的有效路径。 将匹配此项目的值。

`list`：*记录列表*

*记录列表*数据类型的数据源的有效路径。

`list item expression`：*布尔值*

指向或包含应用于匹配的指定列表的一个字段的有效条件表达式。

## <a name="return-values"></a>返回值

*布尔值*

生成的*布尔*值。

## <a name="usage-notes"></a>使用说明

一般来说，`VALUEIN` 函数转换为一组 **OR** 条件。 如果 **OR** 条件的列表很大，可能超出了 SQL 语句的最大总长度，请考虑使用 [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) 函数。

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

在某些情况下，可以使用 `EXISTS JOIN` 运算符将其转换为数据库 SQL 语句。

## <a name="example-1"></a>示例 1

在模型映射中，定义*计算字段*类型的**列表**数据源。 此数据源包含表达式 `SPLIT ("a,b,c", ",")`。

调用数据源时，如果已将其配置为 `VALUEIN ("B", List, List.Value)` 表达式，它将返回 **TRUE**。 在这种情况下，`VALUEIN` 函数转换为以下一组条件：`(("B" = "a") or ("B" = "b") or ("B" = "c"))`，其中 `("B" = "b")` 等于 **TRUE**。

调用数据源时，如果已将其配置为 `VALUEIN ("B", List, LEFT(List.Value, 0))` 表达式，它将返回 **FALSE**。 在这种情况下，`VALUEIN` 函数转换为以下条件：`("B" = "")`，其不等于 **TRUE**。

此条件的文本中的字符数的上限为 32,768 个字符。 因此，您不应该在运行时创建可能超出此限制的数据源。 如果超出限制，应用程序将停止运行，并引发异常。 例如，如果数据源被配置为 `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`，并且 **List1** 和 **List2** 列表包含大量记录，将发生此情况。

在某些情况下，`VALUEIN` 函数通过使用 `EXISTS JOIN` 运算符转换为数据库语句。 此行为会在使用 [`FILTER`](er-functions-list-filter.md) 函数并且当满足以下条件时发生：

- **ASK FOR QUERY** 选项将对引用记录列表的 `VALUEIN` 函数的数据源关闭。 附加条件不会在运行时应用于此数据源。
- 不会为引用记录列表的 `VALUEIN` 函数的数据源配置嵌套表达式。
- `VALUEIN` 函数的列表项引用指定数据源的字段，不是该数据源的表达式或方法。

请考虑使用此选项而不是 [`WHERE`](er-functions-list-where.md) 函数，在本示例前面有述。

## <a name="example-2"></a>示例 2

在模型映射中定义以下数据源：

- *表记录*类型的 **In** 数据源。 此数据源引用 Intrastat 表。
- *表记录*类型的**端口**数据源。 此数据源引用 IntrastatPort 表。

在调用已配置为 `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` 表达式的数据源时，以下 SQL 语句将生成以返回筛选的 Intrastat 表记录。

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

对于 **dataAreaId** 字段，最后的 SQL 语句使用 `IN` 运算符生成。

## <a name="example-3"></a>示例 3

在模型映射中定义以下数据源：

- *计算字段*类型的 **Le** 数据源。 此数据源包含表达式 `SPLIT ("DEMF,GBSI,USMF", ",")`。
- *表记录*类型的 **In** 数据源。 此数据源引用 Intrastat 表，且已打开**跨公司**选项。

在调用已配置为 `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` 表达式的数据源时，最后的 SQL 语句包含以下条件。

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)

[VALUEINLARGE 函数](er-functions-logical-valueinlarge.md)
