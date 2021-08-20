---
title: DATETODATETIME ER 函数
description: 本主题提供有关 DATETODATETIME 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 1e5fa64b776ed2702ac65a2f6416adcf657c748caa1156a71b4c3e99ee188880
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754999"
---
# <a name="datetodatetime-er-function"></a>DATETODATETIME ER 函数

[!include [banner](../includes/banner.md)]

`DATETODATETIME` 函数返回一个 *日期时间* 值，此值从给定日期/时间值转换为协调世界时（格林威治标准时间 \[GMT\]）的日期/时间值。

## <a name="syntax"></a>语法

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]