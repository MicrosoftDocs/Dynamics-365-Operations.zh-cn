---
title: PADLEFT ER 函数
description: 本文提供有关 PADLEFT 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: dac1f9142a381238bf116c4bce65958da8afc4db
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278879"
---
# <a name="padleft-er-function"></a>PADLEFT ER 函数

[!include [banner](../includes/banner.md)]

`PADLEFT` 函数返回指定长度的 *字符串* 值，其中指定字符串的开头是使用指定字符填充的。

## <a name="syntax"></a>语法

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>参数

`text`：*字符串*

代表原始文本的 *字符串* 值。

`length`：*整数*

表示填充的字符串中最终的字符数的 *整数* 值。

`padding chars`：*字符串*

用于填充的字符。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`PADLEFT ("1234", 10, "`&nbsp;`")` 返回文本字符串 **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
