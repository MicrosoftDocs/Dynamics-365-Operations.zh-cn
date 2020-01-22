---
title: 逻辑类别的 ER 函数列表
description: 本主题提供有关电子申报 (ER) 支持的逻辑函数的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916629"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="7eacf-103">逻辑类别的 ER 函数列表</span><span class="sxs-lookup"><span data-stu-id="7eacf-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7eacf-104">电子申报 (ER) 逻辑函数可用于与逻辑值一起使用，来在单个表达式中执行多个比较或测试多个条件。</span><span class="sxs-lookup"><span data-stu-id="7eacf-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="7eacf-105">本主题提供这些函数的概要。</span><span class="sxs-lookup"><span data-stu-id="7eacf-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="7eacf-106">支持的函数列表</span><span class="sxs-lookup"><span data-stu-id="7eacf-106">List of supported functions</span></span>

| <span data-ttu-id="7eacf-107">职能</span><span class="sxs-lookup"><span data-stu-id="7eacf-107">Function</span></span> | <span data-ttu-id="7eacf-108">说明</span><span class="sxs-lookup"><span data-stu-id="7eacf-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="7eacf-109">并</span><span class="sxs-lookup"><span data-stu-id="7eacf-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="7eacf-110">此函数返回一个*布尔*值 **TRUE**（如果所有指定条件都为 true）。</span><span class="sxs-lookup"><span data-stu-id="7eacf-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="7eacf-111">否则，返回*布尔*值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7eacf-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="7eacf-112">包装箱</span><span class="sxs-lookup"><span data-stu-id="7eacf-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="7eacf-113">此函数根据指定的替代选项评估指定表达式的值，并返回等于指定表达式值的第一个选项的结果。</span><span class="sxs-lookup"><span data-stu-id="7eacf-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="7eacf-114">否则，如果将默认结果指定为被调用函数最后一个参数（前面没有选项），则返回可选默认结果。</span><span class="sxs-lookup"><span data-stu-id="7eacf-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="7eacf-115">返回的值可以是任何受支持的数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="7eacf-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="7eacf-116">如果</span><span class="sxs-lookup"><span data-stu-id="7eacf-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="7eacf-117">如果满足指定条件，此函数返回第一个指定值。</span><span class="sxs-lookup"><span data-stu-id="7eacf-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="7eacf-118">否则，返回第二个指定值。</span><span class="sxs-lookup"><span data-stu-id="7eacf-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="7eacf-119">返回的值可以是任何受支持的数据类型的值。</span><span class="sxs-lookup"><span data-stu-id="7eacf-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="7eacf-120">不</span><span class="sxs-lookup"><span data-stu-id="7eacf-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="7eacf-121">此函数作为*布尔*值返回指定条件的冲销逻辑值。</span><span class="sxs-lookup"><span data-stu-id="7eacf-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="7eacf-122">Or</span><span class="sxs-lookup"><span data-stu-id="7eacf-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="7eacf-123">此函数返回一个*布尔*值 **FALSE**（如果所有指定条件都为 false）。</span><span class="sxs-lookup"><span data-stu-id="7eacf-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="7eacf-124">如果所有指定条件都为 true，此函数返回一个*布尔*值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7eacf-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="7eacf-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="7eacf-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="7eacf-126">此函数确定指定的输入是否匹配指定列表中任何指定项目的值。</span><span class="sxs-lookup"><span data-stu-id="7eacf-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="7eacf-127">如果指定的输入与为指定列表的至少一条记录运行指定表达式的结果匹配，它将返回*布尔*值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7eacf-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="7eacf-128">否则，返回*布尔*值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="7eacf-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="7eacf-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="7eacf-129">Additional resources</span></span>

[<span data-ttu-id="7eacf-130">电子申报概览</span><span class="sxs-lookup"><span data-stu-id="7eacf-130">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="7eacf-131">电子报告中的配方设计器</span><span class="sxs-lookup"><span data-stu-id="7eacf-131">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="7eacf-132">电子申报公式语言</span><span class="sxs-lookup"><span data-stu-id="7eacf-132">Electronic reporting formula language</span></span>](er-formula-language.md)
