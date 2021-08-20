---
title: ADDDAYS ER 函数
description: 本主题提供有关 ADDDAYS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 8877bf5a1b6c06e1a25fa9ddaca9c3b039bd2e4d01f39eea9065125977f73e9a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740327"
---
# <a name="adddays-er-function"></a>ADDDAYS ER 函数

[!include [banner](../includes/banner.md)]

`ADDDAYS` 函数计算 *日期时间* 值，此值是指定开始日期之前或之后的指定的天数。

## <a name="syntax"></a>语法

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>参数

`datetime`：*日期时间*

代表开始日期的日期/时间值。

`days`：*整数*

`datetime` 之前或之后的天数。

## <a name="return-values"></a>返回值

*DateTime*

生成的日期/时间值。

## <a name="usage-notes"></a>使用说明

`days` 的正值会产生一个将来的日期。 负值会产生一个过去的日期。

## <a name="example-1"></a>示例 1

`ADDDAYS (NOW(), 7)` 返回未来七天的日期和时间。

## <a name="example-2"></a>示例 2

`ADDDAYS (NOW(), -3)` 返回过去三天的日期和时间。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]