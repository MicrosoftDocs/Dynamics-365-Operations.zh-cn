---
title: LEFT ER 函数
description: 本主题提供有关 LEFT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6f1ec7a21a16c3a34bed9779b05f20f21815ab9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569984"
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