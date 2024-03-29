---
title: REPLACE ER 函数
description: 本文提供有关 REPLACE 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 04/02/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e7a27b5015615d9b0f26e8fcddd812b3f51fb945
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278462"
---
# <a name="replace-er-function"></a>REPLACE ER 函数

[!include [banner](../includes/banner.md)]

在将全部或部分指定文本字符串替换为另一个字符串之后，`REPLACE` 函数作为 *字符串* 值返回指定的文本字符串。

## <a name="syntax"></a>语法

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>参数

`text`：*字符串*

*字符串* 类型的数据源的有效路径。

`pattern`：*字符串*

如果 `regular expression flag` 参数是 **FALSE**，此参数包含必须替换的文本。

如果 `regular expression flag` 参数是 **TRUE**，此参数包含定义搜索模式和替换文本的正则表达式。

`replacement`：*字符串*

如果 `regular expression flag` 参数是 **FALSE**，此参数包含要用作替换的文本。

如果 `regular expression flag` 参数是 **TRUE**，则不使用此参数。

`regular expression flag`：*布尔值*

指示是否使用正则表达式进行替换的 *布尔* 值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

如果 `regular expression flag` 参数是 **TRUE**，此函数将在通过应用 `pattern` 参数指定的正则表达式更改指定的字符串后返回该字符串。 此正则表达式用于查找必须替换的字符。

如果 `regular expression flag` 参数为 **FALSE**，在 `pattern` 中定义的字符集被 `replacement` 参数的字符替换后，此函数将返回指定的字符串。 

## <a name="example-1"></a>示例 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` 应用删除所有非数字符号的正则表达式，返回 **"19234564971"**。 

## <a name="example-2"></a>示例 2

`REPLACE ("abcdef", "cd", "GH", false)` 将模式 **"cd"** 替换为字符串 **"GH"**，返回 **"abGHef"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
