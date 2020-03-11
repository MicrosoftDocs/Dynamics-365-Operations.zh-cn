---
title: LEFT ER 函数
description: 本主题提供有关 LEFT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 4293db244d04debf3679cf2bde0b892bd74e8ead
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041116"
---
# <a name="LEFT">LEFT ER 函数</a>

[!include [banner](../includes/banner.md)]

`LEFT` 函数返回*字符串*值，该值在指定字符串的开头显示指定的字符数量。

## <a name="syntax"></a>语法

```vb
LEFT (text, number)
```

## <a name="arguments"></a>参数

`text`：*字符串*

代表原始文本的*字符串*值。

`number`：*整数*

必须在原始文本开头返回的字符数。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`LEFT ("Sample", 3)` 返回 **"Sam"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)
