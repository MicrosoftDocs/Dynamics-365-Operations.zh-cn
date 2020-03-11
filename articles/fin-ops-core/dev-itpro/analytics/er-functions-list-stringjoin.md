---
title: STRINGJOIN ER 函数
description: 本主题提供有关 STRINGJOIN 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 10a98e98d913b0b4fe36690f7effd5d8d9a3faf4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041783"
---
# <a name="STRINGJOIN">STRINGJOIN ER 函数</a>

[!include [banner](../includes/banner.md)]

`STRINGJOIN` 函数返回由指定列表中的指定字段的连接值组成的*字符串*值。 这些值可以通过指定分隔符分隔。

## <a name="syntax"></a>语法

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表*数据类型的数据源的有效路径。

`field`：*字段*

指定列表中*字符串*数据类型的字段的有效路径。

`delimiter`：*字符串*

用于分隔子字符串的分隔符。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="example"></a>示例

如果输入 `SPLIT("abc" , 1)` 作为数据源 **DS**，表达式 `STRINGJOIN (DS, DS.Value, "-")` 将返回 **"a-b-c"**。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)
