---
title: 逻辑类别的 ER 函数列表
description: 本主题提供有关电子申报 (ER) 支持的逻辑函数的信息。
author: NickSelin
manager: kfend
ms.date: 02/11/2021
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
ms.openlocfilehash: 7310c2b269c3f4be03102160aebe0ed164a23a5c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561654"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="68cb5-103">逻辑类别的 ER 函数列表</span><span class="sxs-lookup"><span data-stu-id="68cb5-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="68cb5-104">电子申报 (ER) 逻辑函数可用于与逻辑值一起使用，来在单个表达式中执行多个比较或测试多个条件。</span><span class="sxs-lookup"><span data-stu-id="68cb5-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="68cb5-105">本主题提供这些函数的概要。</span><span class="sxs-lookup"><span data-stu-id="68cb5-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="68cb5-106">支持的函数列表</span><span class="sxs-lookup"><span data-stu-id="68cb5-106">List of supported functions</span></span>

| <span data-ttu-id="68cb5-107">职能</span><span class="sxs-lookup"><span data-stu-id="68cb5-107">Function</span></span> | <span data-ttu-id="68cb5-108">说明</span><span class="sxs-lookup"><span data-stu-id="68cb5-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="68cb5-109">并</span><span class="sxs-lookup"><span data-stu-id="68cb5-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="68cb5-110">此函数返回一个 *布尔* 值 **TRUE**（如果所有指定条件都为 true）。</span><span class="sxs-lookup"><span data-stu-id="68cb5-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="68cb5-111">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="68cb5-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="68cb5-112">包装箱</span><span class="sxs-lookup"><span data-stu-id="68cb5-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="68cb5-113">此函数根据指定的替代选项评估指定表达式的值，并返回等于指定表达式值的第一个选项的结果。</span><span class="sxs-lookup"><span data-stu-id="68cb5-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="68cb5-114">否则，如果将默认结果指定为被调用函数最后一个参数（前面没有选项），则返回可选默认结果。</span><span class="sxs-lookup"><span data-stu-id="68cb5-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="68cb5-115">返回的值可以是任何受支持的数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="68cb5-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="68cb5-116">包含</span><span class="sxs-lookup"><span data-stu-id="68cb5-116">Contains</span></span>](er-functions-logical-contains.md)             | <span data-ttu-id="68cb5-117">此函数确定指定的输入是否包含指定文本。</span><span class="sxs-lookup"><span data-stu-id="68cb5-117">This function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="68cb5-118">如果指定的输入包含指定的文本，此函数将返回一个 **TRUE** *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="68cb5-118">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="68cb5-119">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="68cb5-119">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="68cb5-120">EndsWith</span><span class="sxs-lookup"><span data-stu-id="68cb5-120">EndsWith</span></span>](er-functions-logical-endswith.md)             | <span data-ttu-id="68cb5-121">此函数确定指定的输入是否以指定文本结尾。</span><span class="sxs-lookup"><span data-stu-id="68cb5-121">This function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="68cb5-122">如果指定的输入以指定文本结尾，此函数将返回一个 **TRUE** *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="68cb5-122">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="68cb5-123">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="68cb5-123">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="68cb5-124">如果</span><span class="sxs-lookup"><span data-stu-id="68cb5-124">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="68cb5-125">如果满足指定条件，此函数返回第一个指定值。</span><span class="sxs-lookup"><span data-stu-id="68cb5-125">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="68cb5-126">否则，返回第二个指定值。</span><span class="sxs-lookup"><span data-stu-id="68cb5-126">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="68cb5-127">返回的值可以是任何受支持的数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="68cb5-127">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="68cb5-128">不</span><span class="sxs-lookup"><span data-stu-id="68cb5-128">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="68cb5-129">此函数作为 *布尔* 值返回指定条件的冲销逻辑值。</span><span class="sxs-lookup"><span data-stu-id="68cb5-129">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="68cb5-130">Or</span><span class="sxs-lookup"><span data-stu-id="68cb5-130">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="68cb5-131">此函数返回一个 *布尔* 值 **FALSE**（如果所有指定条件都为 false）。</span><span class="sxs-lookup"><span data-stu-id="68cb5-131">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="68cb5-132">如果所有指定条件都为 true，此函数返回一个 *布尔* 值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="68cb5-132">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="68cb5-133">StartsWith</span><span class="sxs-lookup"><span data-stu-id="68cb5-133">StartsWith</span></span>](er-functions-logical-startswith.md)         | <span data-ttu-id="68cb5-134">此函数确定指定的输入是否以指定文本开头。</span><span class="sxs-lookup"><span data-stu-id="68cb5-134">This function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="68cb5-135">如果指定的输入以指定文本开头，此函数将返回一个 **TRUE** *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="68cb5-135">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="68cb5-136">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="68cb5-136">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="68cb5-137">ValueIn</span><span class="sxs-lookup"><span data-stu-id="68cb5-137">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="68cb5-138">此函数确定指定的输入是否匹配指定列表中任何指定项目的值。</span><span class="sxs-lookup"><span data-stu-id="68cb5-138">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="68cb5-139">如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，它将返回 *布尔* 值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="68cb5-139">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="68cb5-140">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="68cb5-140">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="68cb5-141">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="68cb5-141">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="68cb5-142">此函数确定指定的 *Int64* 或 *整数* 类型的输入是否匹配指定列表中任何指定项目的值。</span><span class="sxs-lookup"><span data-stu-id="68cb5-142">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="68cb5-143">如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，它将返回 *布尔* 值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="68cb5-143">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="68cb5-144">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="68cb5-144">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="68cb5-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="68cb5-145">Additional resources</span></span>

[<span data-ttu-id="68cb5-146">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="68cb5-146">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="68cb5-147">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="68cb5-147">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="68cb5-148">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="68cb5-148">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]