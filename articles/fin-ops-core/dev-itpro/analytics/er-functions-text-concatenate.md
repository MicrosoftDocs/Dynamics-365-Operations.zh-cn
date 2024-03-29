---
title: CONCATENATE ER 函数
description: 本文提供有关 CONCATENATE 电子报告 (ER) 函数如何使用的信息
author: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 230bbbac5df7824c3ef7d0550cc45dbf6c374858
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267275"
---
# <a name="concatenate-er-function"></a>CONCATENATE ER 函数

[!include [banner](../includes/banner.md)]

在将所有指定的文本字符串合并为一个字符串之后，`CONCATENATE` 函数将这些字符串作为 *字符串* 值返回。

## <a name="syntax"></a>语法

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>参数

`text 1`：*字符串*

对 *字符串* 数据类型的数据源的引用。 此参数是必需的。

`text N`：*字符串*

对 *字符串* 数据类型的数据源的引用。 其他参数是可选的。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`CONCATENATE ("abc", "def")` 返回 **"abcdef"**。

## <a name="usage-notes"></a>使用说明

表达式 `"abc" & "def"` 也返回 **"abcdef"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
