---
title: WHERE ER 函数
description: 本文提供有关 WHERE 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 90b9309b30986837855fb96389b234e504dadd4d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847508"
---
# <a name="where-er-function"></a>WHERE ER 函数

[!include [banner](../includes/banner.md)]

在根据指定的参数对指定列表进行筛选之后，`WHERE` 函数将指定的条件返回为 *记录列表* 值。

## <a name="syntax"></a>语法

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

`condition`：*布尔值*

用于筛选指定列表的记录的有效的条件表达式。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

此函数与 [FILTER](er-functions-list-filter.md) 函数不同，因为指定条件适用于在内存中呈现的 *记录列表* 类型的任何电子申报 (ER) 数据源。

如果为此函数配置的参数（`list` 和 `condition`）允许将此请求转换为直接 SQL 调用，在设计时会引发警告消息。 此消息通知用户，如果使用 [FILTER](er-functions-list-filter.md) 函数而不是 `WHERE`，性能可能会提高。

## <a name="example-1"></a>示例 1

如果 **供应商** 配置为引用 VendTable 表的 ER 数据源，表达式 `WHERE (Vendors, Vendors.VendGroup = "40")` 将返回仅包含属于供应商组 40 的供应商的列表。

## <a name="example-2"></a>示例 2

如果输入 *计算字段* 类型的数据源 **DS**，而该数据源中包含表达式 `SPLIT ("A|B|C", "|")`，则表达式 `WHERE( DS, DS.Value = "B")` 将返回仅在 **值** 字段中包含文本 **"B"** 的一条记录的列表。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]