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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2333cfc21a16a5905acadd590982020fdf878330
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682259"
---
# <a name="listdistinct-er-function"></a><span data-ttu-id="b9b63-103">LISTDISTINCT ER 函数</span><span class="sxs-lookup"><span data-stu-id="b9b63-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="b9b63-104">`LISTDISTINCT` 函数将指定表达式计算为指定列表的每个记录的选择器。</span><span class="sxs-lookup"><span data-stu-id="b9b63-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="b9b63-105">将返回新的 *记录列表* 值，其中包含每个唯一选择器值的单个记录。</span><span class="sxs-lookup"><span data-stu-id="b9b63-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9b63-106">语法</span><span class="sxs-lookup"><span data-stu-id="b9b63-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="b9b63-107">参数</span><span class="sxs-lookup"><span data-stu-id="b9b63-107">Arguments</span></span>

<span data-ttu-id="b9b63-108">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="b9b63-108">`list`: *Record list*</span></span>

<span data-ttu-id="b9b63-109">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="b9b63-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="b9b63-110">`selector`：*原始数据类型*</span><span class="sxs-lookup"><span data-stu-id="b9b63-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="b9b63-111">用于为指定列表中的每个记录计算选择器值的有效表达式。</span><span class="sxs-lookup"><span data-stu-id="b9b63-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="b9b63-112">此参数支持以下数据类型：</span><span class="sxs-lookup"><span data-stu-id="b9b63-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="b9b63-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="b9b63-113">Boolean</span></span>
- <span data-ttu-id="b9b63-114">日期</span><span class="sxs-lookup"><span data-stu-id="b9b63-114">Date</span></span>
- <span data-ttu-id="b9b63-115">日期时间</span><span class="sxs-lookup"><span data-stu-id="b9b63-115">DateTime</span></span>
- <span data-ttu-id="b9b63-116">Guid</span><span class="sxs-lookup"><span data-stu-id="b9b63-116">GUID</span></span>
- <span data-ttu-id="b9b63-117">整数</span><span class="sxs-lookup"><span data-stu-id="b9b63-117">Integer</span></span>
- <span data-ttu-id="b9b63-118">Int64</span><span class="sxs-lookup"><span data-stu-id="b9b63-118">Int64</span></span>
- <span data-ttu-id="b9b63-119">实数</span><span class="sxs-lookup"><span data-stu-id="b9b63-119">Real</span></span>
- <span data-ttu-id="b9b63-120">字符串</span><span class="sxs-lookup"><span data-stu-id="b9b63-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="b9b63-121">返回值</span><span class="sxs-lookup"><span data-stu-id="b9b63-121">Return values</span></span>

<span data-ttu-id="b9b63-122">*记录列表*</span><span class="sxs-lookup"><span data-stu-id="b9b63-122">*Record list*</span></span>

<span data-ttu-id="b9b63-123">生成的记录列表。</span><span class="sxs-lookup"><span data-stu-id="b9b63-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b9b63-124">使用说明</span><span class="sxs-lookup"><span data-stu-id="b9b63-124">Usage notes</span></span>

<span data-ttu-id="b9b63-125">创建的列表的结构与指定列表的结构匹配。</span><span class="sxs-lookup"><span data-stu-id="b9b63-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="b9b63-126">可能会为指定列表中的多个记录计算相同的选择器值。</span><span class="sxs-lookup"><span data-stu-id="b9b63-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="b9b63-127">在这种情况下，创建的列表中相应记录的字段值，等于为其计算选择器值的指定列表中第一个记录的值。</span><span class="sxs-lookup"><span data-stu-id="b9b63-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="b9b63-128">此函数的执行在内存中存在的 *记录列表* 类型的任意[电子报告 (ER)](general-electronic-reporting.md) 数据源上进行。</span><span class="sxs-lookup"><span data-stu-id="b9b63-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="b9b63-129">**GROUPBY** 数据源还可用于生成为其计算具有不同值的选择器的记录列表。</span><span class="sxs-lookup"><span data-stu-id="b9b63-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="b9b63-130">但是，从性能和内存消耗角度看，使用 `LISTDISTINCT` 函数比使用 **GROUPBY** 数据源更好，因为此函数的执行在内存中进行。</span><span class="sxs-lookup"><span data-stu-id="b9b63-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="b9b63-131">示例</span><span class="sxs-lookup"><span data-stu-id="b9b63-131">Example</span></span>

<span data-ttu-id="b9b63-132">下面的示例显示如何获取在特定期间内至少已向其签发了一个销售发票或项目发票的唯一客户帐号的列表。</span><span class="sxs-lookup"><span data-stu-id="b9b63-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="b9b63-133">输入 `Record list` 类型的 **SalesInvoice** 数据源，该数据源引用 **CustInvoiceJour** 应用程序表并筛选特定期间的销售发票。</span><span class="sxs-lookup"><span data-stu-id="b9b63-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="b9b63-134">此数据源的 `InvoiceAccount` 字段返回已开票客户的帐号。</span><span class="sxs-lookup"><span data-stu-id="b9b63-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="b9b63-135">输入 `Record list` 类型的 **ProjectInvoice** 数据源，该数据源引用 **ProjInvoiceJour** 应用程序表并筛选特定期间的项目发票。</span><span class="sxs-lookup"><span data-stu-id="b9b63-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="b9b63-136">此数据源的 `InvoiceAccount` 字段返回已开票客户的帐号。</span><span class="sxs-lookup"><span data-stu-id="b9b63-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="b9b63-137">配置 `Calculated field` 类型的 **AllInvoices** 数据源，其中包含表达式 `LISTJOIN(SalesInvoice, ProjectInvoice)`。</span><span class="sxs-lookup"><span data-stu-id="b9b63-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="b9b63-138">此数据源返回销售发票和项目发票的合并列表。</span><span class="sxs-lookup"><span data-stu-id="b9b63-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="b9b63-139">配置 `Record list` 类型的 **InvoicedCustomer** 数据源，其中包含表达式 `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`。</span><span class="sxs-lookup"><span data-stu-id="b9b63-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="b9b63-140">此数据源返回一个新列表，其中包含在定义期间内已开发票的每个唯一客户的单个记录。</span><span class="sxs-lookup"><span data-stu-id="b9b63-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="b9b63-141">此列表的 `InvoiceAccount` 字段包含客户帐号。</span><span class="sxs-lookup"><span data-stu-id="b9b63-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9b63-142">其他资源</span><span class="sxs-lookup"><span data-stu-id="b9b63-142">Additional resources</span></span>

[<span data-ttu-id="b9b63-143">列表函数</span><span class="sxs-lookup"><span data-stu-id="b9b63-143">List functions</span></span>](er-functions-category-list.md)
