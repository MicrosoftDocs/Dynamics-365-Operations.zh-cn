---
title: TRANSLATE ER 函数
description: 本主题提供有关 TRANSLATE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: c5d192b8679d6df2c44a0038fe4ffc181a6a54df
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685295"
---
# <a name="translate-er-function"></a>TRANSLATE ER 函数

[!include [banner](../includes/banner.md)]

`TRANSLATE` 函数返回一个 *字符串* 值，该值中包含对提供的另一个字符集中的指定文本进行字符替换的结果。

## <a name="syntax"></a>语法

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>参数

`text`：*字符串*

*字符串* 类型的数据源的有效路径。

`pattern`：*字符串*

必须替换的文本。

`replacement`：*字符串*

用作替换的文本。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

`TRANSLATE` 函数一次替换一个字符。 此函数将 `text` 变量的第一个字符替换为 `pattern` 参数的第一个字符，然后替换第二个字符，并执行相同流程，直到完成。 当 `text` 和 `pattern` 变量中有一个字符匹配时，将被替换为 `replacement` 变量中与 `pattern` 变量中的字符位于同一个位置的字符。 如果某个字符在 `pattern` 变量中多次出现，则使用与此字符的第一次出现对应的 `replacement` 变量映射。

## <a name="example-1"></a>示例 1

因为下面的原因，`TRANSLATE ("abcdef", "cd", "GH")` 将指定的 **abcdef** 文本的 **c** 字符替换为 `replacement` 文本的 **G** 字符：
-   `pattern` 文本中第一个位置有 **c** 字符。
-   `replacement` 文本的第一个位置中包含 **G** 字符。

## <a name="example-2"></a>示例 2

`TRANSLATE ("abcdef", "ccd", "GH")` 返回 **abGdef**。

## <a name="example-3"></a>示例 3

`TRANSLATE ("abccba", "abc", "123")` 将返回 **"123321"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)
