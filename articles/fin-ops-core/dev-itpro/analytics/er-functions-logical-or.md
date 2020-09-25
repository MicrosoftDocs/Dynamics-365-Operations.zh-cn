---
title: OR ER 函数
description: 本主题提供有关 OR 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: faf07c5d8b30cd3babe8a6a55ae7effe5ce457a0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744615"
---
# <a name="or-er-function"></a><span data-ttu-id="a282d-103">OR ER 函数</span><span class="sxs-lookup"><span data-stu-id="a282d-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a282d-104">`OR` 函数返回一个*布尔*值 **FALSE**（如果所有指定条件都为 false）。</span><span class="sxs-lookup"><span data-stu-id="a282d-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="a282d-105">如果所有指定条件都为 true，此函数返回一个*布尔*值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a282d-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a282d-106">语法</span><span class="sxs-lookup"><span data-stu-id="a282d-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="a282d-107">参数</span><span class="sxs-lookup"><span data-stu-id="a282d-107">Arguments</span></span>

<span data-ttu-id="a282d-108">`condition 1`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="a282d-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="a282d-109">必须测试的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="a282d-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="a282d-110">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="a282d-110">This argument is required.</span></span>

<span data-ttu-id="a282d-111">`condition N`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="a282d-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="a282d-112">必须测试的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="a282d-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="a282d-113">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="a282d-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="a282d-114">返回值</span><span class="sxs-lookup"><span data-stu-id="a282d-114">Return values</span></span>

<span data-ttu-id="a282d-115">*布尔值*</span><span class="sxs-lookup"><span data-stu-id="a282d-115">*Boolean*</span></span>

<span data-ttu-id="a282d-116">生成的*布尔*值。</span><span class="sxs-lookup"><span data-stu-id="a282d-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="a282d-117">示例</span><span class="sxs-lookup"><span data-stu-id="a282d-117">Example</span></span>

<span data-ttu-id="a282d-118">`OR (1=2, "a"="a")` 返回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a282d-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a282d-119">其他资源</span><span class="sxs-lookup"><span data-stu-id="a282d-119">Additional resources</span></span>

[<span data-ttu-id="a282d-120">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="a282d-120">Logical functions</span></span>](er-functions-category-logical.md)
