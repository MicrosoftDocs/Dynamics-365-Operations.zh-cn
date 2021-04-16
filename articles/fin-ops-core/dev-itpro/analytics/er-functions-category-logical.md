---
title: 逻辑类别的 ER 函数列表
description: 本主题提供有关电子申报 (ER) 支持的逻辑函数的信息。
author: NickSelin
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
ms.openlocfilehash: 452eae2b710429215939b712b12fe156943d2ac5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749409"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="7c62d-103">逻辑类别的 ER 函数列表</span><span class="sxs-lookup"><span data-stu-id="7c62d-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7c62d-104">电子申报 (ER) 逻辑函数可用于与逻辑值一起使用，来在单个表达式中执行多个比较或测试多个条件。</span><span class="sxs-lookup"><span data-stu-id="7c62d-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="7c62d-105">本主题提供这些函数的概要。</span><span class="sxs-lookup"><span data-stu-id="7c62d-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="7c62d-106">支持的函数列表</span><span class="sxs-lookup"><span data-stu-id="7c62d-106">List of supported functions</span></span>

| <span data-ttu-id="7c62d-107">职能</span><span class="sxs-lookup"><span data-stu-id="7c62d-107">Function</span></span> | <span data-ttu-id="7c62d-108">说明</span><span class="sxs-lookup"><span data-stu-id="7c62d-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7c62d-109">并</span><span class="sxs-lookup"><span data-stu-id="7c62d-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="7c62d-110">此函数返回一个 *布尔* 值 **TRUE**（如果所有指定条件都为 true）。</span><span class="sxs-lookup"><span data-stu-id="7c62d-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="7c62d-111">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7c62d-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="7c62d-112">包装箱</span><span class="sxs-lookup"><span data-stu-id="7c62d-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="7c62d-113">此函数根据指定的替代选项评估指定表达式的值，并返回等于指定表达式值的第一个选项的结果。</span><span class="sxs-lookup"><span data-stu-id="7c62d-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="7c62d-114">否则，如果将默认结果指定为被调用函数最后一个参数（前面没有选项），则返回可选默认结果。</span><span class="sxs-lookup"><span data-stu-id="7c62d-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="7c62d-115">返回的值可以是任何受支持的数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="7c62d-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="7c62d-116">包含</span><span class="sxs-lookup"><span data-stu-id="7c62d-116">Contains</span></span>](er-functions-logical-contains.md)             | <span data-ttu-id="7c62d-117">此函数确定指定的输入是否包含指定文本。</span><span class="sxs-lookup"><span data-stu-id="7c62d-117">This function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="7c62d-118">如果指定的输入包含指定的文本，此函数将返回一个 **TRUE** *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="7c62d-118">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="7c62d-119">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7c62d-119">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="7c62d-120">EndsWith</span><span class="sxs-lookup"><span data-stu-id="7c62d-120">EndsWith</span></span>](er-functions-logical-endswith.md)             | <span data-ttu-id="7c62d-121">此函数确定指定的输入是否以指定文本结尾。</span><span class="sxs-lookup"><span data-stu-id="7c62d-121">This function determines whether the specified input ends with the specified text.</span></span> <span data-ttu-id="7c62d-122">如果指定的输入以指定文本结尾，此函数将返回一个 **TRUE** *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="7c62d-122">It returns a *Boolean* value of **TRUE** if the specified input ends with the specified text.</span></span> <span data-ttu-id="7c62d-123">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7c62d-123">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="7c62d-124">如果</span><span class="sxs-lookup"><span data-stu-id="7c62d-124">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="7c62d-125">如果满足指定条件，此函数返回第一个指定值。</span><span class="sxs-lookup"><span data-stu-id="7c62d-125">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="7c62d-126">否则，返回第二个指定值。</span><span class="sxs-lookup"><span data-stu-id="7c62d-126">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="7c62d-127">返回的值可以是任何受支持的数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="7c62d-127">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="7c62d-128">不</span><span class="sxs-lookup"><span data-stu-id="7c62d-128">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="7c62d-129">此函数作为 *布尔* 值返回指定条件的冲销逻辑值。</span><span class="sxs-lookup"><span data-stu-id="7c62d-129">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="7c62d-130">Or</span><span class="sxs-lookup"><span data-stu-id="7c62d-130">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="7c62d-131">此函数返回一个 *布尔* 值 **FALSE**（如果所有指定条件都为 false）。</span><span class="sxs-lookup"><span data-stu-id="7c62d-131">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="7c62d-132">如果所有指定条件都为 true，此函数返回一个 *布尔* 值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7c62d-132">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="7c62d-133">StartsWith</span><span class="sxs-lookup"><span data-stu-id="7c62d-133">StartsWith</span></span>](er-functions-logical-startswith.md)         | <span data-ttu-id="7c62d-134">此函数确定指定的输入是否以指定文本开头。</span><span class="sxs-lookup"><span data-stu-id="7c62d-134">This function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="7c62d-135">如果指定的输入以指定文本开头，此函数将返回一个 **TRUE** *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="7c62d-135">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="7c62d-136">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7c62d-136">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="7c62d-137">ValueIn</span><span class="sxs-lookup"><span data-stu-id="7c62d-137">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="7c62d-138">此函数确定指定的输入是否匹配指定列表中任何指定项目的值。</span><span class="sxs-lookup"><span data-stu-id="7c62d-138">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="7c62d-139">如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，它将返回 *布尔* 值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7c62d-139">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="7c62d-140">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7c62d-140">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="7c62d-141">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="7c62d-141">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="7c62d-142">此函数确定指定的 *Int64* 或 *整数* 类型的输入是否匹配指定列表中任何指定项目的值。</span><span class="sxs-lookup"><span data-stu-id="7c62d-142">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="7c62d-143">如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，它将返回 *布尔* 值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7c62d-143">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="7c62d-144">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7c62d-144">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="7c62d-145">其他资源</span><span class="sxs-lookup"><span data-stu-id="7c62d-145">Additional resources</span></span>

[<span data-ttu-id="7c62d-146">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="7c62d-146">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="7c62d-147">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="7c62d-147">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="7c62d-148">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="7c62d-148">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]