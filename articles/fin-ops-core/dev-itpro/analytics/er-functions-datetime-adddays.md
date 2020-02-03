---
title: ADDDAYS ER 函数
description: 本主题提供有关 ADDDAYS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916445"
---
# <a name="ADDDAYS">ADDDAYS ER 函数</a>

[!include [banner](../includes/banner.md)]

`ADDDAYS` 函数计算*日期时间*值，此值是指定开始日期之前或之后的指定的天数。

## <a name="syntax"></a>语法

```
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