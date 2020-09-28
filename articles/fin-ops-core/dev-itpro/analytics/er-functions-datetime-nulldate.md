---
title: NULLDATE ER 函数
description: 本主题提供有关 NULLDATE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: edf43cc19636f51387504a7d9da73d757d96e558
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744279"
---
# <a name="nulldate-er-function"></a>NULLDATE ER 函数

[!include [banner](../includes/banner.md)]

`NULLDATE` 函数返回一个表示**空**日期（1900 年 1 月 1 日）的*日期*值。

## <a name="syntax"></a>语法

```vb
NULLDATE () as 
```

## <a name="return-values"></a>返回值

*日期*

生成的日期值。

## <a name="example-1"></a>示例 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` 基于指定的自定义格式返回**空**日期 1900 年 1 月 1 日为 **"1900-01-01"**。

## <a name="example-2"></a>示例 2

当 **DocumentDate** 字段的值等于**空**日期时，表达式 `IF( Invoice.DocumentDate = NULLDATE(), true, false)` 返回 **True**。 在此示例中，**Invoice** 为 **Finance/Table 记录**类型的电子申报 (ER) 数据源，引用 CustInvoiceJour 表。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)
