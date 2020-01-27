---
title: DATETODATETIME ER 函数
description: 本主题提供有关 DATETODATETIME 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916376"
---
# <a name="DATETODATETIME">DATETODATETIME ER 函数</a>

[!include [banner](../includes/banner.md)]

`DATETODATETIME` 函数返回一个*日期时间*值，此值从给定日期/时间值转换为协调世界时（格林威治标准时间 \[GMT\]）的日期/时间值。

## <a name="syntax"></a>语法

```
DATETODATETIME (date)
```

## <a name="arguments"></a>参数

`date`：*日期*

代表要转换的日期的日期值。

## <a name="return-values"></a>返回值

*DateTime*

生成的日期/时间值。

## <a name="example-1"></a>示例 1

`DATETODATETIME (CompInfo. 'getCurrentDate()')` 返回当前 Microsoft Dynamics 365 Finance 会话的日期，2015 年 12 月 24 日返回为 **12/24/2015 12:00:00 AM**。 在此示例中，**CompInfo** 为 **Finance and Operations/Table** 类型，引用 CompanyInfo 表的电子申报 (ER) 数据源。

## <a name="example-2"></a>示例 2

`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` 返回日期/时间值 **11/12/2019 12:00:00 AM**。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)
