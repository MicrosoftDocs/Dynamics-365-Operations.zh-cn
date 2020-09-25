---
title: VALUEIN ER 函数
description: 本主题提供有关 VALUEIN 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 08/18/2020
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
ms.openlocfilehash: b4f88c0d71b6fa6980ee8e180ae5be482a463f1c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744663"
---
# <a name="valuein-er-function"></a><span data-ttu-id="99120-103">VALUEIN ER 函数</span><span class="sxs-lookup"><span data-stu-id="99120-103">VALUEIN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99120-104">`VALUEIN` 函数确定指定的输入是否匹配指定列表中任何指定项目的值。</span><span class="sxs-lookup"><span data-stu-id="99120-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="99120-105">如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，它将返回*布尔*值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="99120-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="99120-106">否则，返回*布尔*值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="99120-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="99120-107">语法</span><span class="sxs-lookup"><span data-stu-id="99120-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="99120-108">参数</span><span class="sxs-lookup"><span data-stu-id="99120-108">Arguments</span></span>

<span data-ttu-id="99120-109">`input`：*字段*</span><span class="sxs-lookup"><span data-stu-id="99120-109">`input`: *Field*</span></span>

<span data-ttu-id="99120-110">*记录列表*类型的数据源项目的有效路径。</span><span class="sxs-lookup"><span data-stu-id="99120-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="99120-111">将匹配此项目的值。</span><span class="sxs-lookup"><span data-stu-id="99120-111">The value of this item will be matched.</span></span>

<span data-ttu-id="99120-112">`list`：*记录列表*</span><span class="sxs-lookup"><span data-stu-id="99120-112">`list`: *Record list*</span></span>

<span data-ttu-id="99120-113">*记录列表*数据类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="99120-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="99120-114">`list item expression`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="99120-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="99120-115">指向或包含应用于匹配的指定列表的一个字段的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="99120-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="99120-116">返回值</span><span class="sxs-lookup"><span data-stu-id="99120-116">Return values</span></span>

<span data-ttu-id="99120-117">*布尔值*</span><span class="sxs-lookup"><span data-stu-id="99120-117">*Boolean*</span></span>

<span data-ttu-id="99120-118">生成的*布尔*值。</span><span class="sxs-lookup"><span data-stu-id="99120-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="99120-119">使用说明</span><span class="sxs-lookup"><span data-stu-id="99120-119">Usage notes</span></span>

<span data-ttu-id="99120-120">一般来说，`VALUEIN` 函数转换为一组 **OR** 条件。</span><span class="sxs-lookup"><span data-stu-id="99120-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="99120-121">如果 **OR** 条件的列表很大，可能超出了 SQL 语句的最大总长度，请考虑使用 [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="99120-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="99120-122">在某些情况下，可以使用 `EXISTS JOIN` 运算符将其转换为数据库 SQL 语句。</span><span class="sxs-lookup"><span data-stu-id="99120-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="99120-123">示例 1</span><span class="sxs-lookup"><span data-stu-id="99120-123">Example 1</span></span>

<span data-ttu-id="99120-124">在模型映射中，定义*计算字段*类型的**列表**数据源。</span><span class="sxs-lookup"><span data-stu-id="99120-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="99120-125">此数据源包含表达式 `SPLIT ("a,b,c", ",")`。</span><span class="sxs-lookup"><span data-stu-id="99120-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="99120-126">调用数据源时，如果已将其配置为 `VALUEIN ("B", List, List.Value)` 表达式，它将返回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="99120-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="99120-127">在这种情况下，`VALUEIN` 函数转换为以下一组条件：`(("B" = "a") or ("B" = "b") or ("B" = "c"))`，其中 `("B" = "b")` 等于 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="99120-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="99120-128">调用数据源时，如果已将其配置为 `VALUEIN ("B", List, LEFT(List.Value, 0))` 表达式，它将返回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="99120-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="99120-129">在这种情况下，`VALUEIN` 函数转换为以下条件：`("B" = "")`，其不等于 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="99120-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="99120-130">此条件的文本中的字符数的上限为 32,768 个字符。</span><span class="sxs-lookup"><span data-stu-id="99120-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="99120-131">因此，您不应该在运行时创建可能超出此限制的数据源。</span><span class="sxs-lookup"><span data-stu-id="99120-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="99120-132">如果超出限制，应用程序将停止运行，并引发异常。</span><span class="sxs-lookup"><span data-stu-id="99120-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="99120-133">例如，如果数据源被配置为 `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`，并且 **List1** 和 **List2** 列表包含大量记录，将发生此情况。</span><span class="sxs-lookup"><span data-stu-id="99120-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="99120-134">在某些情况下，`VALUEIN` 函数通过使用 `EXISTS JOIN` 运算符转换为数据库语句。</span><span class="sxs-lookup"><span data-stu-id="99120-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="99120-135">此行为会在使用 [`FILTER`](er-functions-list-filter.md) 函数并且当满足以下条件时发生：</span><span class="sxs-lookup"><span data-stu-id="99120-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="99120-136">**ASK FOR QUERY** 选项将对引用记录列表的 `VALUEIN` 函数的数据源关闭。</span><span class="sxs-lookup"><span data-stu-id="99120-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="99120-137">附加条件不会在运行时应用于此数据源。</span><span class="sxs-lookup"><span data-stu-id="99120-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="99120-138">不会为引用记录列表的 `VALUEIN` 函数的数据源配置嵌套表达式。</span><span class="sxs-lookup"><span data-stu-id="99120-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="99120-139">`VALUEIN` 函数的列表项引用指定数据源的字段，不是该数据源的表达式或方法。</span><span class="sxs-lookup"><span data-stu-id="99120-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="99120-140">请考虑使用此选项而不是 [`WHERE`](er-functions-list-where.md) 函数，在本示例前面有述。</span><span class="sxs-lookup"><span data-stu-id="99120-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="99120-141">示例 2</span><span class="sxs-lookup"><span data-stu-id="99120-141">Example 2</span></span>

<span data-ttu-id="99120-142">在模型映射中定义以下数据源：</span><span class="sxs-lookup"><span data-stu-id="99120-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="99120-143">*表记录*类型的 **In** 数据源。</span><span class="sxs-lookup"><span data-stu-id="99120-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="99120-144">此数据源引用 Intrastat 表。</span><span class="sxs-lookup"><span data-stu-id="99120-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="99120-145">*表记录*类型的**端口**数据源。</span><span class="sxs-lookup"><span data-stu-id="99120-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="99120-146">此数据源引用 IntrastatPort 表。</span><span class="sxs-lookup"><span data-stu-id="99120-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="99120-147">在调用已配置为 `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` 表达式的数据源时，以下 SQL 语句将生成以返回筛选的 Intrastat 表记录。</span><span class="sxs-lookup"><span data-stu-id="99120-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="99120-148">对于 **dataAreaId** 字段，最后的 SQL 语句使用 `IN` 运算符生成。</span><span class="sxs-lookup"><span data-stu-id="99120-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="99120-149">示例 3</span><span class="sxs-lookup"><span data-stu-id="99120-149">Example 3</span></span>

<span data-ttu-id="99120-150">在模型映射中定义以下数据源：</span><span class="sxs-lookup"><span data-stu-id="99120-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="99120-151">*计算字段*类型的 **Le** 数据源。</span><span class="sxs-lookup"><span data-stu-id="99120-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="99120-152">此数据源包含表达式 `SPLIT ("DEMF,GBSI,USMF", ",")`。</span><span class="sxs-lookup"><span data-stu-id="99120-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="99120-153">*表记录*类型的 **In** 数据源。</span><span class="sxs-lookup"><span data-stu-id="99120-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="99120-154">此数据源引用 Intrastat 表，且已打开**跨公司**选项。</span><span class="sxs-lookup"><span data-stu-id="99120-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="99120-155">在调用已配置为 `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` 表达式的数据源时，最后的 SQL 语句包含以下条件。</span><span class="sxs-lookup"><span data-stu-id="99120-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="99120-156">其他资源</span><span class="sxs-lookup"><span data-stu-id="99120-156">Additional resources</span></span>

[<span data-ttu-id="99120-157">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="99120-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="99120-158">VALUEINLARGE 函数</span><span class="sxs-lookup"><span data-stu-id="99120-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)
