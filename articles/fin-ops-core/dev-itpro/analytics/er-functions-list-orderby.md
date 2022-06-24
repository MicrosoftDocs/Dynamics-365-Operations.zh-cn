---
title: ORDERBY ER 函数
description: 本文提供有关 ORDERBY 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 1a922405ea23d2b1ff5ac062785e68626edbc8f0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883750"
---
# <a name="orderby-er-function"></a>ORDERBY ER 函数

[!include [banner](../includes/banner.md)]

在根据指定的参数对指定列表进行排序之后，`ORDERBY` 函数将指定列表返回为 *记录列表* 值。 可将这些变量定义为表达式。

## <a name="syntax-1"></a><a name="syntax-1"></a>语法 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>语法 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Microsoft Dynamics 365 Finance 版本 10.0.25 及更高版本支持此语法。

## <a name="arguments"></a>参数

`location`：*[字符串](er-formula-supported-data-types-primitive.md#string)*

应运行排序的位置。 以下选项有效：

- “Query”
- “InMemory”

`list`：*[记录列表](er-formula-supported-data-types-composite.md#record-list)*

*记录列表* 数据类型的数据源的有效路径。

`expression 1`：*字段*

被调用函数的 `list` 参数引用的数据源字段的有效路径。 引用的字段必须是原始数据类型的字段。 此参数是必需的。

`expression N`：*字段*

被调用函数的 `list` 参数引用的数据源字段的有效路径。 引用的字段必须是原始数据类型的字段。 其他参数是可选的。

## <a name="return-values"></a>返回值

*记录列表*

生成的记录列表。

## <a name="usage-notes"></a>使用说明

### <a name="syntax-1"></a>语法 1

数据排序始终在应用程序服务器的内存中完成。 有关更多详细信息，请参阅[示例 1](#example-1)。

### <a name="syntax-2"></a>语法 2

### <a name="sorting-in-memory"></a>在内存中排序

当 `location` 参数被指定为 **InMemory** 时，数据排序在应用服务器的内存中完成。 有关更多详细信息，请参阅[示例 2](#example-2)。

### <a name="sorting-in-database"></a>在数据库中排序

当 `location` 参数被指定为 **Query** 时，数据排序在数据库级别完成。 在这种情况下，`list` 参数必须指向以下[电子报告 (ER)](general-electronic-reporting.md) 数据源之一，该数据源指定可以为其建立直接数据库查询的应用程序源：

- *表记录* 类型的数据源
- *表记录* 类型的数据源的关系
- *计算字段* 类型的数据源

`expression 1` 和 `expression N` 参数必须指向 ER 数据源的字段，该数据源指定还可以为其建立直接数据库查询的应用程序源的相关字段。

如果无法建立直接数据库查询，ER 模型映射设计器中会发生验证[错误](er-components-inspections.md#i18)。 您收到的消息指出在运行时不能运行其中包含 `ORDERBY` 函数的 ER 表达式。

为了获得更好的性能，我们建议您在为可能包含大量记录的应用程序数据源（例如，对于事务性应用程序表）配置排序时使用 **Query** 选项。

> [!NOTE]
> `ORDEBY` 函数本身不能转换为直接数据库查询。 因此，包含此函数的 ER 数据源不能查询。 它也不能在只能使用可查询数据源的 ER 函数范围内使用，如 [FILTER](er-functions-list-filter.md) 和 [ALLITEMSQUERY](er-functions-list-allitemsquery.md)。

有关更多详细信息，请参阅[示例 3](#example-3) 和[示例 4](#example-4)。

### <a name="comparability"></a>相似性

由于 SQL 数据库引擎和 Finance 应用程序服务器可以对单个字符使用不同的排名值，因此在使用[字符串](er-formula-supported-data-types-primitive.md#string)字段进行排序时，同一记录列表的排序结果可能不同。 有关更多详细信息，请参阅[示例 5](#example-5)。

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>示例 1：内存中默认执行

如果输入 *计算字段* 类型的数据源 **DS**，并且它包含表达式 `SPLIT ("C|B|A", "|")`，表达式 `FIRST( ORDERBY( DS, DS. Value)).Value` 将返回文本值 **"A"**。

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>示例 2：内存中显示执行

如果 **Vendor** 被配置为引用 **VendTable** 表的 *表记录* 类型的 ER 数据源，表达式 `ORDERBY (Vendor, Vendor.'name()')` 和表达式 `ORDERBY ("InMemory", Vendor, Vendor.'name()')` 将返回按名称升序排列的供应商列表。

当您在 ER 模型映射设计器中配置表达式 `ORDERBY ("Query", Vendor, Vendor.'name()')` 时，在设计时会发生验证[错误](er-components-inspections.md#i8)，因为 `Vendor.'name()'` 路径引用具有无法转换为直接数据库查询的逻辑的应用程序方法。

## <a name="example-3-database-query"></a><a name="example-3"></a>示例 3：数据库查询

如果 **TaxTransaction** 被配置为引用 **TaxTrans** 表的 *表记录* 类型的 ER 数据源，表达式 `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` 将在应用程序数据库级别对记录进行排序，并返回按税码升序排列的税交易记录列表。

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>示例 4：可查询数据源

如果 **TaxTransaction** 被配置为引用 **TaxTrans** 表的 *表记录* 类型的 ER 数据源，可以配置 **TaxTransactionFiltered** ER 数据源，使其包含将提取指定税码的交易记录的表达式 `FILTER(TaxTransaction, TaxCode="VAT19")`。 由于配置的 **TaxTransactionFiltered** ER 数据源是可查询的，因此表达式 `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` 可以被配置为返回按交易日期升序排序的已筛选税交易记录的列表。

如果您将 **TaxTransactionOrdered** 配置为包含表达式 `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` 的 *计算字段* 类型的 ER 数据源，以及包含表达式 `FILTER(TaxTransactionOrdered, TaxCode="VAT19")` 的 *计算字段* 类型的 ER 数据源，验证[错误](er-components-inspections.md#i18)会在 ER 模型映射设计器中在设计时发生。 发生此错误是因为 [FILTER](er-functions-list-filter.md#usage-notes) 函数的第一个参数必须引用可查询的 ER 数据源，但包含 `ORDERBY` 函数的 **TaxTransactionOrdered** 数据源不可查询。

## <a name="example-5-comparability"></a><a name="example-5"></a>示例 5：相似性

### <a name="prerequisites"></a>先决条件

1. 输入包含表达式 `SPLIT ("D1|_D2|D3", "|")` 的 *计算字段* 类型的数据源 **DS1**。
2. 打开 **[财务维度值](../../../finance/general-ledger/financial-dimensions.md)** 页面，然后选择 **CostCenter** 维度。
3. 输入以下维度值：**D1**、**\_D2** 和 **D3**。

### <a name="sorting-in-memory"></a>在内存中排序

1. 配置包含表达式 `ORDERBY("InMemory", DS1, DS1.Value)` 的 *计算字段* 类型的数据源 **DS2**。
2. 请注意，表达式 `FIRST(DS2).Value` 返回文本值 **"D1"**，表达式 `INDEX(DS2, COUNT(DS2)).Value` 返回文本值 **"\_D2"**，表达式 `STRINGJOIN(DS2, DS2.Value, "|")` 返回文本值 **"D1\|D3\|\_D2"**。

### <a name="sorting-in-database"></a>在数据库中排序

1. 输入引用 **FinancialDimensionValueEntity** 实体的 *表记录* 类型的数据源 **DS3**。
2. 配置包含表达式 `FILTER(DS3, DS3.FinancialDimension="CostCenter")` 的 *计算字段* 类型的数据源 **DS4**。
3. 配置包含表达式 `ORDERBY(DS4, DS4.DimensionValue)` 的 *计算字段* 类型的数据源 **DS5**。
4. 请注意，表达式 `FIRST(DS5).Value` 返回文本值 **"\_D2"**，表达式 `INDEX(DS5, COUNT(DS5)).Value` 返回文本值 **"D3"**，表达式 `STRINGJOIN(DS5, DS5.Value, "|")` 返回文本值 **"\_D2\|D1\|D3"**。

## <a name="additional-resources"></a>其他资源

[列表函数](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
