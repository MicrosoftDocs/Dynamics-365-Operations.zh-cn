---
title: UPPER ER 函数
description: 本文提供有关 UPPER 电子报告 (ER) 函数如何使用的信息。
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: bdea427dda5f09a3903378012679e9dd3fa86be9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275332"
---
# <a name="upper-er-function"></a>UPPER ER 函数

[!include [banner](../includes/banner.md)]

在将指定的文本字符串转换为大写字母后，`UPPER` 函数作为 *字符串* 值返回该字符串。

## <a name="syntax"></a>语法

```vb
UPPER (text )
```

## <a name="arguments"></a>参数

`text`：*字符串*

*字符串* 类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`UPPER ("Sample")` 返回 **"SAMPLE"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
