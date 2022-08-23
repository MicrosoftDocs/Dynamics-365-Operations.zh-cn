---
title: LOWER ER 函数
description: 本文提供有关 LOWER 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 7a633c8cf68b611fcaa3f216823ef9b19cac16f5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288009"
---
# <a name="lower-er-function"></a>LOWER ER 函数

[!include [banner](../includes/banner.md)]

在将指定的文本字符串转换为小写字母后，`LOWER` 函数作为 *字符串* 值返回该字符串。

## <a name="syntax"></a>语法

```vb
LOWER (text)
```

## <a name="arguments"></a>参数

`text`：*字符串*

指定文本的 *字符串* 值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`LOWER ("Sample")` 返回 **"sample"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
