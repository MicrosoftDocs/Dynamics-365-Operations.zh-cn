---
title: CASE ER 函数
description: 本主题提供有关 CASE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 38b51a4d8bf8dc997bae2ae9206d8e71ca48dec6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916054"
---
# <a name="CASE">CASE ER 函数</a>

[!include [banner](../includes/banner.md)]

`CASE` 函数根据指定的替代选项评估指定表达式的值，并返回等于指定表达式值的第一个选项的结果。 否则，如果将默认结果指定为被调用函数最后一个参数（前面没有选项），则返回可选默认结果。 返回的值可以是任何受支持的数据类型的值。

## <a name="syntax"></a>语法

```
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>参数

`expression`：*原始数据类型*（布尔值、数字或文本）

返回原始数据类型的值的有效表达式。

`option 1`：*原始数据类型*（布尔值、数字或文本）

一个有效表达式，返回与被调用函数的 `expression` 参数相同的原始数据类型的值。 此参数是必需的。

`result 1`：*任何受支持的数据类型*

返回的结果与前面的选项相对应。 此参数是必需的。

`option N`：*原始数据类型*（布尔值、数字或文本）

一个有效表达式，返回与被调用函数的 `expression` 参数相同的原始数据类型的值。 此参数是可选的。

`result N`：*任何受支持的数据类型*

返回的结果与前面的选项相对应。 此参数是可选的。

`default result`：*任何受支持的数据类型*

如果没有匹配项，应返回的结果。 此参数是可选的。

## <a name="return-values"></a>返回值

*任何受支持的数据类型*

生成的任何受支持数据类型的值。

## <a name="usage-notes"></a>使用说明

如果没有匹配项，并且未定义可选的默认结果，将在运行时引发异常。

必须使用相同的数据类型指定所有结果。 如果配置结果的数据类型不匹配，则会在设计时引发异常。

如果第一个结果值与第 *N* 个结果值是*容器（记录）* 或*记录列表*数据类型的值，结果只包含两个值中都存在的字段。

## <a name="example"></a>示例

如果当前应用程序会话日期在 10 月到 12 月之间，`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` 将返回字符串 **"WINTER"**。 否则，它返回一个空字符串。

## <a name="additional-resources"></a>其他资源

[逻辑函数](er-functions-category-logical.md)
