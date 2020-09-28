---
title: VALUE ER 函数
description: 本主题提供有关 VALUE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: ecbffb7e39d7f2f2bccdfe32d593512a65da163c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745505"
---
# <a name="value-er-function"></a>VALUE ER 函数

[!include [banner](../includes/banner.md)]

`VALUE` 函数返回一个*实数*值，该值从指定的字符串转换而来。

## <a name="syntax"></a>语法

```vb
VALUE (text)
```

## <a name="arguments"></a>参数

`text`：*字符串*

必须转换为数字值的字符串值。

## <a name="return-values"></a>返回值

*实数*

生成的数字值。

## <a name="usage-notes"></a>使用说明

逗号和点字符 (.) 被视为小数分隔符，前导连字符 (-) 用作负号。 如果指定字符串中包含其他非数值字符，将在运行时引发异常。

## <a name="example-1"></a>示例 1

`VALUE ("1 234,56")` 引发异常。

## <a name="example-2"></a>示例 2

`VALUE ("1234,56")` 将返回 **1234.56**。

## <a name="additional-resources"></a>其他资源

[类型转换函数](er-functions-category-type-conversion.md)
