---
title: CONCATENATE ER 函数
description: 本主题提供有关 CONCATENATE 电子申报 (ER) 函数如何使用的信息
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915755"
---
# <a name="CONCATENATE">CONCATENATE ER 函数</a>

[!include [banner](../includes/banner.md)]

在将所有指定的文本字符串合并为一个字符串之后，`CONCATENATE` 函数将这些字符串作为*字符串*值返回。

## <a name="syntax"></a>语法

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>参数

`text 1`：*字符串*

对*字符串*数据类型的数据源的引用。 此参数是必需的。

`text N`：*字符串*

对*字符串*数据类型的数据源的引用。 其他参数是可选的。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`CONCATENATE ("abc", "def")` 返回 **"abcdef"**。

## <a name="usage-notes"></a>使用说明

表达式 `"abc" & "def"` 也返回 **"abcdef"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)
