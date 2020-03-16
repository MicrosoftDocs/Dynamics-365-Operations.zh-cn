---
title: INT64VALUE ER 函数
description: 本主题提供有关 INT64VALUE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 7fcb8a617507801d82d16175e9e86c9193091a12
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042680"
---
# <a name="INT64VALUE">INT64VALUE ER 函数</a>

[!include [banner](../includes/banner.md)]

`INT64VALUE` 函数返回一个 *Int64* 值，该值表示指定的字符串。

## <a name="syntax-1"></a>语法 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>语法 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>参数

`text`：*字符串*

必须转换为 *Int64* 数字的文本值。

`number`：*实数*或*整数*

必须转换为 *Int64* 数字的*实数*或*整数*数字值。

## <a name="return-values"></a>返回值

*Int64*

生成的数字值。

## <a name="usage-notes"></a>使用说明

将截断所有小数部分。

## <a name="example-1"></a>示例 1

`INT64VALUE ("22565422744")` 返回 *Int64* 值 **22565422744**。

## <a name="example-2"></a>示例 2

`INT64VALUE ( VALUE("22565422744.77"))` 返回 *Int64* 值 **22565422744**。

## <a name="additional-resources"></a>其他资源

[类型转换函数](er-functions-category-type-conversion.md)
