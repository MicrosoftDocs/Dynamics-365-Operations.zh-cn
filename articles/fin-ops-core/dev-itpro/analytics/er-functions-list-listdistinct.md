---
title: LISTDISTINCT ER 函数
description: 本主题提供有关 LISTDISTINCT 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 791038981e88d0f52026bfb17d2d1fa381f28c46
ms.sourcegitcommit: 41e165482b9bff4175c0e3b224dbeead13461956
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/11/2020
ms.locfileid: "3687999"
---
# <a name="listdistinct-er-function"></a>LISTDISTINCT ER 函数

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

`LISTDISTINCT` 函数将指定表达式计算为指定列表的每个记录的选择器。 将返回新的*记录列表*值，其中包含每个唯一选择器值的单个记录。

## <a name="syntax"></a>语法

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>参数

`list`：*记录列表*

*记录列表*数据类型的数据源的有效路径。

`selector`：*原始数据类型*

用于为指定列表中的每个记录计算选择器值的有效表达式。

此参数支持以下数据类型：

- Boolean
- 日期
- 日期时间
- Guid
- 整数
- Int64
- 实数
- 字符串

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

创建的列表的结构与指定列表的结构匹配。

可能会为指定列表中的多个记录计算相同的选择器值。 在这种情况下，创建的列表中相应记录的字段值，等于为其计算选择器值的指定列表中第一个记录的值。

此函数的执行在内存中存在的*记录列表*类型的任意[电子报告 (ER)](general-electronic-reporting.md) 数据源上进行。

**GROUPBY** 数据源还可用于生成为其计算具有不同值的选择器的记录列表。 但是，从性能和内存消耗角度看，使用 `LISTDISTINCT` 函数比使用 **GROUPBY** 数据源更好，因为此函数的执行在内存中进行。

## <a name="example"></a>示例

下面的示例显示如何获取在特定期间内至少已向其签发了一个销售发票或项目发票的唯一客户帐号的列表。

1. 输入 `Record list` 类型的 **SalesInvoice** 数据源，该数据源引用 **CustInvoiceJour** 应用程序表并筛选特定期间的销售发票。

    此数据源的 `InvoiceAccount` 字段返回已开票客户的帐号。

2. 输入 `Record list` 类型的 **ProjectInvoice** 数据源，该数据源引用 **ProjInvoiceJour** 应用程序表并筛选特定期间的项目发票。

    此数据源的 `InvoiceAccount` 字段返回已开票客户的帐号。

3. 配置 `Calculated field` 类型的 **AllInvoices** 数据源，其中包含表达式 `LISTJOIN(SalesInvoice, ProjectInvoice)`。

    此数据源返回销售发票和项目发票的合并列表。

4. 配置 `Record list` 类型的 **InvoicedCustomer** 数据源，其中包含表达式 `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`。

    此数据源返回一个新列表，其中包含在定义期间内已开发票的每个唯一客户的单个记录。 此列表的 `InvoiceAccount` 字段包含客户帐号。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)
