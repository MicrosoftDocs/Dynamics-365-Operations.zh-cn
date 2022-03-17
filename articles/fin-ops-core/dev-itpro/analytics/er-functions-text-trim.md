---
title: TRIM ER 函数
description: 本主题提供有关 TRIM 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: 816f6d6623bb778c9186d294c9b67db7edddd671
ms.sourcegitcommit: 753714ac0dabc4b7ce91509757cd19f7be4a4793
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/01/2022
ms.locfileid: "8367784"
---
# <a name="trim-er-function"></a>TRIM ER 函数

[!include [banner](../includes/banner.md)]

`TRIM` 函数在制表符、回车符、换行符和换页符被单个空格字符替换后，在前导和尾随空格被截断后，以及字词之间的多个空格被删除后，将指定的文本字符串作为 *字符串* 值返回。

## <a name="syntax"></a>语法

```vb
TRIM (text)
```

## <a name="arguments"></a>参数

`text`：*字符串*

*字符串* 类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

在某些情况下，您可能希望截断前导和尾随空格，但更希望保留指定文本的格式。 例如，当此文本表示可以在多行文本框中输入的地址并且可以包含换行和回车格式时。 在这种情况下，请使用以下表达式：`REPLACE(text,"^[ \t]+|[ \t]+$","", true)`，其中 `text` 是引用指定文本字符串的参数。

## <a name="example-1"></a>示例 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` 返回 **"Sample text"**。

## <a name="example-2"></a>示例 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` 返回 **“示例文本”**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)

[REPLACE ER 函数](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
