---
title: TRANSLATE ER 函数
description: 本主题提供有关 TRANSLATE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916698"
---
# <a name="TRANSLATE">TRANSLATE ER 函数</a>

[!include [banner](../includes/banner.md)]

在将全部或部分指定文本字符串替换为另一个字符串之后，`TRANSLATE` 函数作为*字符串*值返回指定的文本字符串。

## <a name="syntax"></a>语法

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>参数

`text`：*字符串*

*字符串*类型的数据源的有效路径。

`pattern`：*字符串*

必须替换的文本。

`replacement`：*字符串*

用作替换的文本。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`TRANSLATE ("abcdef", "cd", "GH")` 将模式 **"cd"** 替换为字符串 **"GH"**，返回 **"abGHef"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)
