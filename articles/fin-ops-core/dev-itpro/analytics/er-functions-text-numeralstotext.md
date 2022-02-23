---
title: NUMERALSTOTEXT ER 函数
description: 本主题提供有关 NUMERALSTOTEXT 电子申报 (ER) 函数如何使用的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4af3926998d128f8269ab9af46caeb8be896509
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680210"
---
# <a name="numeralstotext-er-function"></a>NUMERALSTOTEXT ER 函数

[!include [banner](../includes/banner.md)]

在使用指定语言拼出（即转换为文本字符串）指定数字后，`NUMERALSTOTEXT` 函数作为 *字符串* 返回指定数字。

## <a name="syntax"></a>语法

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>参数

`number`：*整数* 或 *实数*

指定必须拼出的数字的数字值。

`language`：*字符串*

代表语言代码的 *字符串* 值。

`currency`：*字符串*

代表币种代码的 *字符串* 值。

`print currency name flag`：*布尔值*

指示是否必须将货币名称添加到拼出的文本的 *布尔* 值。

`decimal points`：*整数*

指示拼出的文本应具有的小数位数的 *整数* 值。

## <a name="return-values"></a>返回值

*字符串*

生成的文本值。

## <a name="usage-notes"></a>使用说明

语言代码可选。 如果定义为空字符串，将使用运行上下文的语言代码。 默认语言代码为 **EN-US**。 运行上下文的语言代码在正在运行的电子申报 (ER) 格式的 **文件夹** 或 **文件** 元素中定义。

币种代码可选。 如果定义为空字符串，将使用运行上下文的公司币种。

> [!NOTE] 
> 仅为以下语言代码分析 `print currency name flag` 和 `decimal points` 参数：**CS**、**ET**、**HU**、**LT**、**LV**、**PL** 和 **RU**。 此外，仅为国家或地区的上下文支持货币名称偏差的公司分析 `print currency name flag` 参数。

## <a name="example-1"></a>示例 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` 返回 **"One Thousand Two Hundred Thirty Four and 56"**。

## <a name="example-2"></a>示例 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` 返回 **"Sto dwadzieścia"**。 

## <a name="example-3"></a>示例 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` 返回 **"Сто двадцать евро 21 евроцент"**。

## <a name="additional-resources"></a>其他资源

[文本函数](er-functions-category-text.md)
