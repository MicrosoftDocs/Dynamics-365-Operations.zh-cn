---
title: AND ER 函数
description: 本主题提供有关 AND 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: dd9c0ed0238009f70ad7a9bf5a5e19ebfb95cccc
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917158"
---
# <span data-ttu-id="89553-103"><a name="AND">AND ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="89553-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89553-104">`AND` 函数返回一个*布尔*值 **TRUE**（如果所有指定条件都为 true）。</span><span class="sxs-lookup"><span data-stu-id="89553-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="89553-105">否则，返回*布尔*值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="89553-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="89553-106">语法</span><span class="sxs-lookup"><span data-stu-id="89553-106">Syntax</span></span>

```
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="89553-107">参数</span><span class="sxs-lookup"><span data-stu-id="89553-107">Arguments</span></span>

<span data-ttu-id="89553-108">`condition 1`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="89553-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="89553-109">必须测试的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="89553-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="89553-110">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="89553-110">This argument is required.</span></span>

<span data-ttu-id="89553-111">`condition N`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="89553-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="89553-112">必须测试的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="89553-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="89553-113">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="89553-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="89553-114">返回值</span><span class="sxs-lookup"><span data-stu-id="89553-114">Return values</span></span>

<span data-ttu-id="89553-115">*布尔值*</span><span class="sxs-lookup"><span data-stu-id="89553-115">*Boolean*</span></span>

<span data-ttu-id="89553-116">生成的*布尔*值。</span><span class="sxs-lookup"><span data-stu-id="89553-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="89553-117">使用说明</span><span class="sxs-lookup"><span data-stu-id="89553-117">Usage notes</span></span>

<span data-ttu-id="89553-118">在逻辑函数的参数中，可以使用数据源引用、数字和文本值、布尔值、比较运算符以及其他电子申报 (ER) 函数。</span><span class="sxs-lookup"><span data-stu-id="89553-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="89553-119">但是，必须将所有参数评估为*布尔*值 **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="89553-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="89553-120">示例</span><span class="sxs-lookup"><span data-stu-id="89553-120">Example</span></span>

<span data-ttu-id="89553-121">`AND (1=1, "a"="a")` 返回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="89553-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="89553-122">`AND (1=2, "a"="a")` 返回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="89553-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="89553-123">其他资源</span><span class="sxs-lookup"><span data-stu-id="89553-123">Additional resources</span></span>

[<span data-ttu-id="89553-124">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="89553-124">Logical functions</span></span>](er-functions-category-logical.md)
