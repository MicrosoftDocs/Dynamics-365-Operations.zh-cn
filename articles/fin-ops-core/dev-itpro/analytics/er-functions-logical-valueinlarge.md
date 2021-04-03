---
title: VALUEINLARGE ER 函数
description: 本主题提供有关 VALUEINLARGE 电子报告 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 1e35c695d697e0d0f42baeaf568548273f9d205b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565800"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="37240-103">VALUEINLARGE ER 函数</span><span class="sxs-lookup"><span data-stu-id="37240-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37240-104">`VALUEINLARGE` 函数确定指定的 *Int64* 或 *整数* 类型的输入是否匹配指定列表中任何指定项目的值。</span><span class="sxs-lookup"><span data-stu-id="37240-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="37240-105">如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，此函数将返回 *布尔* 值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="37240-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="37240-106">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="37240-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="37240-107">要了解与 `VALUEIN` 函数的区别，请参阅本主题后面的[使用说明](#usage_note)一节。</span><span class="sxs-lookup"><span data-stu-id="37240-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="37240-108">语法</span><span class="sxs-lookup"><span data-stu-id="37240-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="37240-109">参数</span><span class="sxs-lookup"><span data-stu-id="37240-109">Arguments</span></span>

<span data-ttu-id="37240-110">`input`：*字段*</span><span class="sxs-lookup"><span data-stu-id="37240-110">`input`: *Field*</span></span>

<span data-ttu-id="37240-111">*记录列表* 类型的数据源项的有效路径。</span><span class="sxs-lookup"><span data-stu-id="37240-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="37240-112">将匹配此项目的值。</span><span class="sxs-lookup"><span data-stu-id="37240-112">The value of this item will be matched.</span></span>

<span data-ttu-id="37240-113">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="37240-113">`list`: *Record list*</span></span>

<span data-ttu-id="37240-114">*记录列表* 数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="37240-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="37240-115">`list item expression`：*表达式*</span><span class="sxs-lookup"><span data-stu-id="37240-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="37240-116">指向或包含应用于匹配的指定列表的一个字段的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="37240-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="37240-117">返回值</span><span class="sxs-lookup"><span data-stu-id="37240-117">Return values</span></span>

<span data-ttu-id="37240-118">*Boolean*</span><span class="sxs-lookup"><span data-stu-id="37240-118">*Boolean*</span></span>

<span data-ttu-id="37240-119">生成的 *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="37240-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="37240-120"><a name="usage_note">使用说明</a></span><span class="sxs-lookup"><span data-stu-id="37240-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="37240-121">当指定的输入表示其调用可翻译为直接 SQL 语句的数据源项的 *Int64* 或 *整数* 类型（可转换为直接SQL语句的调用）时，指定的列表将转换为临时 SQL 表，匹配将通过执行单个 `EXISTS JOIN` 查询在数据库中执行。</span><span class="sxs-lookup"><span data-stu-id="37240-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="37240-122">否则，此函数将用作 [`VALUEIN`](er-functions-logical-valuein.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="37240-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="37240-123">当指定的输入表示设计为 *Int64* 和 *整数* 类型以外的项目的数据源项时，在设计时将发生错误，通知您 `VALUEINLARGE` 函数不适用于配置的 ER 表达式。</span><span class="sxs-lookup"><span data-stu-id="37240-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="37240-124">当执行 `VALUEINLARGE` 函数表达式并在此执行范围内使用多个临时表时，会发生运行时错误。</span><span class="sxs-lookup"><span data-stu-id="37240-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="37240-125">示例</span><span class="sxs-lookup"><span data-stu-id="37240-125">Example</span></span>

<span data-ttu-id="37240-126">在模型映射中定义以下数据源：</span><span class="sxs-lookup"><span data-stu-id="37240-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="37240-127">*表记录* 类型的 **In** 数据源。</span><span class="sxs-lookup"><span data-stu-id="37240-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="37240-128">此数据源引用 **内部统计** 表。</span><span class="sxs-lookup"><span data-stu-id="37240-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="37240-129">**跨公司** 选项将设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="37240-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="37240-130">*计算字段* 类型的 **InMemory** 数据源。</span><span class="sxs-lookup"><span data-stu-id="37240-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="37240-131">此数据源包含表达式 `WHERE (In, In.Port <> "")`。</span><span class="sxs-lookup"><span data-stu-id="37240-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="37240-132">*计算字段* 类型的 **InFiltered** 数据源。</span><span class="sxs-lookup"><span data-stu-id="37240-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="37240-133">此数据源包含表达式 `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`。</span><span class="sxs-lookup"><span data-stu-id="37240-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="37240-134">在公司 **DEMF** 的上下文下调用数据源 **InFiltered** 时，将在应用程序数据库中创建新的临时表，在记录标识代码的内存列表中收集的项将插入此表中，并生成以下 SQL 语句以返回 **内部统计** 表的筛选记录。</span><span class="sxs-lookup"><span data-stu-id="37240-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="37240-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="37240-135">Additional resources</span></span>

[<span data-ttu-id="37240-136">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="37240-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="37240-137">VALUEIN 函数</span><span class="sxs-lookup"><span data-stu-id="37240-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]