---
title: UPPER ER 函数
description: 本主题提供有关 UPPER 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 0e0e9837765914c657a72c5ce04c6f565fa13788
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749133"
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