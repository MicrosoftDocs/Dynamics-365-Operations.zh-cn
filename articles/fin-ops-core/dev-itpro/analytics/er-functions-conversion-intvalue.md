---
title: INTVALUE ER 函数
description: 本主题提供有关 INTVALUE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: c5c3e4c8bd918fa1154d2c111970d2f6d0e90e08
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743631"
---
# <a name="intvalue-er-function"></a>INTVALUE ER 函数

[!include [banner](../includes/banner.md)]

`INTVALUE` 函数返回一个 *Int* 值，该值表示指定的字符串。

## <a name="syntax-1"></a>语法 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>语法 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>参数

`text`：*字符串*

必须转换为 *Int* 数字的文本值。

`number`：*实数*或*整数*

必须转换为 *Int* 数字的*实数*或*整数*数字值。

## <a name="return-values"></a>返回值

*Int*

生成的数字值。

## <a name="usage-notes"></a>使用说明

将截断所有小数部分。

## <a name="example-1"></a>示例 1

`INTVALUE ("100.77")` 返回 *Int* 值 **100**。

## <a name="example-2"></a>示例 2

`INTVALUE (-100.77)` 返回 *Int* 值 **-100**。

## <a name="additional-resources"></a>其他资源

[类型转换函数](er-functions-category-type-conversion.md)
