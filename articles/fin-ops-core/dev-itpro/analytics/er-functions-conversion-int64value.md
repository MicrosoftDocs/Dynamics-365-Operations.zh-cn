---
title: INT64VALUE ER 函数
description: 本文提供有关 INT64VALUE 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 37fae9cdc5a833009b0ca1cbeb851e5e6e1b6608
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892155"
---
# <a name="int64value-er-function"></a>INT64VALUE ER 函数

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

`number`：*实数* 或 *整数*

必须转换为 *Int64* 数字的 *实数* 或 *整数* 数字值。

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]