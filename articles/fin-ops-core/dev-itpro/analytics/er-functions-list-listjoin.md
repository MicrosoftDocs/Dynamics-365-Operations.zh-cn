---
title: LISTJOIN ER 函数
description: 本文提供有关 LISTJOIN 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba7b4b52f5403232d3a32a6b2907c20de29c80d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877116"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER 函数

[!include [banner](../includes/banner.md)]

`LISTJOIN` 函数返回一个 *记录列表* 值，此值表示根据指定参数创建的记录的新连接列表。

## <a name="syntax"></a>语法

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>参数

`list 1`：*记录列表*

对 *记录列表* 数据类型的数据源的引用。 此参数是强制性的。

`list N`：*记录列表*

对 *记录列表* 数据类型的数据源的引用。 其他参数是可选的。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

创建的列表的结构仅包含在参数中提到的每个记录列表的结构中显示的字段。

## <a name="example"></a>示例

您输入 `Container` 类型的数据源 **记录 1**。 此数据源包含 `Calculated field` 类型的以下嵌套字段：

- **代码**：此字段包含返回 `String` 类型的值的表达式。
- **金额**：此字段包含返回 `Real` 类型的值的表达式。

然后输入 `Container` 类型的数据源 **记录 2**。 此数据源包含 `Calculated field` 类型的以下嵌套字段：

- **金额**：此字段包含返回 `Real` 类型的值的表达式。
- **IsValid**：此字段包含返回 `Boolean` 类型的值的表达式。

![ER 模型映射设计器页面。](./media/er-functions-list-listjoin-image1.gif)

在此例中，表达式 `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` 返回包含两个记录的新列表。

![带有两个记录的 ER 模型映射设计器页面。](./media/er-functions-list-listjoin-image2.gif)

此列表的结构由一个 `Real` 类型的 **金额** 字段组成，因为此字段是被调用函数每个参数中显示的唯一字段。

![ER 模型映射设计器页面金额字段。](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)

[调试已执行 ER 格式的数据源以分析数据流和转换](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
