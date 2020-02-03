---
title: REPLACE ER 函数
description: 本主题提供有关 REPLACE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: d9c66f4c96f35e3ad5fc92e7925b5cd07c956aac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916859"
---
# <a name="REPLACE">REPLACE ER 函数</a>

[!include [banner](../includes/banner.md)]

在将全部或部分指定文本字符串替换为另一个字符串之后，`REPLACE` 函数作为*字符串*值返回指定的文本字符串。

## <a name="syntax"></a>语法

```
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>参数

`text`：*字符串*

*字符串*类型的数据源的有效路径。

`pattern`：*字符串*

如果 `regular expression flag` 参数是 **FALSE**，此参数包含必须替换的文本。

如果 `regular expression flag` 参数是 **TRUE**，此参数包含定义搜索模式和替换文本的正则表达式。

`replacement`：*字符串*

如果 `regular expression flag` 参数是 **FALSE**，此参数包含要用作替换的文本。

如果 `regular expression flag` 参数是 **TRUE**，则不使用此参数。

`regular expression flag`：*布尔值*

指示是否使用正则表达式进行替换的*布尔*值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

如果 `regular expression flag` 参数是 **TRUE**，此函数将在通过应用 `pattern` 参数指定的正则表达式更改指定的字符串后返回该字符串。 此正则表达式用于查找必须替换的字符。

如果 `regular expression flag` 参数是 **FALSE**，此函数的行为类似于 [TRANSLATE](er-functions-text-translate.md)。 由 `replacement` 参数指定的字符用于替换找到的字符。 

## <a name="example-1"></a>示例 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` 应用删除所有非数字符号的正则表达式，返回 **"19234564971"**。 

## <a name="example-2"></a>示例 2

`REPLACE ("abcdef", "cd", "GH", false)` 将模式 **"cd"** 替换为字符串 **"GH"**，返回 **"abGHef"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)