---
title: SPLIT ER 函数
description: 本主题提供有关 SPLIT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 5c99ee5e8129ed45253893dc83acdef99b4ce2c9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745585"
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

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]