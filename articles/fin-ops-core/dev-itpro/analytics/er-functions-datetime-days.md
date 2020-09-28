---
title: DAYS ER 函数
description: 本主题提供有关 DAYS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 47d992d061f8664a55332024ee5c6cd41e4bc495
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743559"
---
# <a name="days-er-function"></a>DAYS ER 函数

[!include [banner](../includes/banner.md)]

`DAYS` 函数返回一个*整数*值，此值表示一个指定日期至第二个指定日期之间的天数。

## <a name="syntax"></a>语法

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>参数

`date 1`：*日期*

表示用于计算天数的开始日期的日期值。

`date 2`：*日期*

表示用于计算天数的结束日期的日期值。

## <a name="return-values"></a>返回值

*整数*

生成的数字值。

## <a name="usage-notes"></a>使用说明

第一个日期比第二个日期晚时，`DAYS` 函数返回正值，第一个日期等于第二个日期时返回**0**（零），第一个日期比第二个日期早时返回负值。

## <a name="example"></a>示例

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` 将返回 **-1**。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)
