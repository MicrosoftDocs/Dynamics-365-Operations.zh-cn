---
title: LEFT ER 函数
description: 本文提供有关 LEFT 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 866c1b59fee9aa58afafbd82a83cff57e4cadeeb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267982"
---
# <a name="left-er-function"></a>LEFT ER 函数

[!include [banner](../includes/banner.md)]

`LEFT` 函数返回 *字符串* 值，该值在指定字符串的开头显示指定的字符数量。

## <a name="syntax"></a>语法

```vb
LEFT (text, number)
```

## <a name="arguments"></a>参数

`text`：*字符串*

代表原始文本的 *字符串* 值。

`number`：*整数*

必须在原始文本开头返回的字符数。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`LEFT ("Sample", 3)` 返回 **"Sam"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
