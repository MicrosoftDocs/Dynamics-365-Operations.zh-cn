---
title: NULLDATE ER 函数
description: 本文提供有关 NULLDATE 电子报告 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 7d1f0535796da096253dbd3ed55e9407cc9150f4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870397"
---
# <a name="nulldate-er-function"></a>NULLDATE ER 函数

[!include [banner](../includes/banner.md)]

`NULLDATE` 函数返回一个表示 **空** 日期（1900 年 1 月 1 日）的 *日期* 值。

## <a name="syntax"></a>语法

```vb
NULLDATE () as 
```

## <a name="return-values"></a>返回值

*日期*

生成的日期值。

## <a name="example-1"></a>示例 1

`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` 基于指定的自定义格式返回 **空** 日期 1900 年 1 月 1 日为 **"1900-01-01"**。

## <a name="example-2"></a>示例 2

当 **DocumentDate** 字段的值等于 **空** 日期时，表达式 `IF( Invoice.DocumentDate = NULLDATE(), true, false)` 返回 **True**。 在此示例中，**Invoice** 为 **Finance/Table 记录** 类型的电子申报 (ER) 数据源，引用 CustInvoiceJour 表。

## <a name="additional-resources"></a>其他资源

[日期和时间函数](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]