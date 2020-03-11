---
title: PADLEFT ER 函数
description: 本主题提供有关 PADLEFT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: d11e2d8b46614085156228ab1001d1f9340a05b0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040955"
---
# <a name="PADLEFT">PADLEFT ER 函数</a>

[!include [banner](../includes/banner.md)]

`PADLEFT` 函数返回指定长度的*字符串*值，其中指定字符串的开头是使用指定字符填充的。

## <a name="syntax"></a>语法

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>参数

`text`：*字符串*

代表原始文本的*字符串*值。

`length`：*整数*

表示填充的字符串中最终的字符数的*整数*值。

`padding chars`：*字符串*

用于填充的字符。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`PADLEFT ("1234", 10, "`&nbsp;`")` 返回文本字符串 **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)
