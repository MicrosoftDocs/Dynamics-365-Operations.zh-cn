---
title: SPLIT ER 函数
description: 本主题提供有关 SPLIT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 4a42b0c7cfa2a8d3dcb7448224c9e88a48276f7d8cdbcce484383a778b8275a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757313"
---
# <a name="split-er-function"></a>SPLIT ER 函数

[!include [banner](../includes/banner.md)]

`SPLIT` 函数将指定的输入字符串拆分为子字符串，并将结果作为新的 *记录列表* 值返回。

## <a name="syntax-1"></a>语法 1

```vb
SPLIT (input, length)
```

此语法用于拆分指定的输入字符串为子字符串，每个子字符串具有指定的长度。

## <a name="syntax-2"></a>语法 2

```vb
SPLIT (input, delimiter)
```

此语法用于根据指定的分隔符拆分指定的输入字符串为子字符串。

## <a name="arguments"></a>参数

`input`：*字符串*

要拆分的文本。

`length`：*整数*

单个子字符串的最大长度。

`delimiter`：*字符串*

用于分隔子字符串的分隔符。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

返回的列表的记录结构包括 *字符串* 类型的 **值** 字段。 返回的列表的每个记录在此字段中都包含生成的子字符串。

如果 `delimiter` 参数是空的，返回的新列表将包括一个具有 *字符串* 类型的 **值** 字段的记录。 此字段包含输入文本。

如果 `input` 参数为空，新的空列表将返回。 如果 `input` 或 `delimiter` 参数未指定（空），将引发应用程序异常。

## <a name="example-1"></a>示例 1

`SPLIT ("abcd", 3)` 返回包含具有 *字符串* 类型的 **值** 字段的两个记录的新列表。 第一个记录中的 **值** 字段包含文本 **"abc"**，第二个记录中的 **值** 字段包含文本 **"d"**。

## <a name="example-2"></a>示例 2

`SPLIT ("XAb aBy", "aB")` 返回包含具有 *字符串* 类型的 **值** 字段的三个记录的新列表。 第一个记录中的 **值** 字段包含文本 **"X"**，第二个记录中的 **值** 字段包含文本 **"&nbsp;"**，第三个记录中的 **值** 字段包含文本 **"y"**。 

## <a name="example-3"></a>示例 3

您可以使用 [INDEX](er-functions-list-index.md) 函数访问指定输入字符串的各个元素。 如果输入 **计算字段** 类型的 **MyList** 数据源并且为其配置 `SPLIT("abc", 1)` 表达式，表达式 `INDEX(MyList,2).Value` 将返回文本 **“b”**。

## <a name="example-4"></a>示例 4

[ENUMERATE](er-functions-list-enumerate.md) 函数也可帮助您访问指定输入字符串的各个元素。 如果您首先输入 **计算字段** 类型的 **MyList** 数据源并且为其配置 `SPLIT("abc", 1)` 表达式，然后输入 **计算字段** 类型的 **EnumeratedList** 数据源并且为其配置 `ENUMERATE(MyList)` 表达式，表达式 `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` 将返回文本 **“b”**。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
