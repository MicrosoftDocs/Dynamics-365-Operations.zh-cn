---
title: TRIM ER 函数
description: 本主题提供有关 TRIM 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 2673b0167f7602a6d6eaa79be639905028e99822
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915525"
---
# <a name="TRIM">TRIM ER 函数</a>

[!include [banner](../includes/banner.md)]

在删除前导和尾随空格以及删除单词之间的多个空格之后，`TRIM` 函数作为*字符串*值返回指定的文本字符串。

## <a name="syntax"></a>语法

```
TRIM (text )
```

## <a name="arguments"></a>参数

`text`：*字符串*

*字符串*类型的数据源的有效路径。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` 返回 **"Sample text"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)