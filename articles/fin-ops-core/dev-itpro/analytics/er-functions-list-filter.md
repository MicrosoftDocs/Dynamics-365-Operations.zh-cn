---
title: FILTER ER 函数
description: 本主题提供有关 FILTER 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: aa8c0b4601db625d442dd545151968f38bd58cf1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746595"
---
# <a name="filter-er-function"></a>FILTER ER 函数

[!include [banner](../includes/banner.md)]

`FILTER` 函数在查询更改以针对指定条件进行筛选后作为 *记录列表* 值返回指定列表。

## <a name="syntax"></a>语法

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表* 数据类型的数据源的有效路径。

`condition`：*布尔值*

用于筛选指定列表的记录的有效的条件表达式。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

此函数与 [WHERE](er-functions-list-where.md) 函数不同，因为指定条件适用于数据库级别的 *表格记录* 类型的任何电子申报 (ER) 数据源。 可使用表格和关系定义列表和条件。

如果为此函数配置的一个或两个参数（`list` 和 `condition`）不允许将此请求转换为直接 SQL 调用，在设计时会引发异常。 此异常通知用户 `list` 或 `condition` 不能用于查询数据库。

## <a name="example-1"></a>示例 1

如果 **供应商** 配置为引用 VendTable 表的 ER 数据源，表达式 `FILTER (Vendors, Vendors.VendGroup = "40")` 将返回仅包含属于供应商组 40 的供应商的列表。

## <a name="example-2"></a>示例 2

如果 **供应商** 配置为引用 VendTable 表的 ER 数据源，并且配置为 ER 数据源的 **parmVendorBankGroup** 返回 *字符串* 数据类型的值，表达式 `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` 将返回仅包含属于特定银行组的供应商帐户的列表。

## <a name="example-3"></a>示例 3

输入 *计算字段* 类型的数据源 **DS**，它包含表达式 `SPLIT ("A,B,C", ",")`。 然后输入另一个表达式 `FILTER( DS, DS.Value = "B")`。 当您尝试在 ER 公式设计器中保存此表达式时，将引发以下异常：“验证错误：FILTER 函数的列表表达式不可查询。”

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]