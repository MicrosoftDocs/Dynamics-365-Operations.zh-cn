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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917112"
---
# <span data-ttu-id="71b3b-103"><a name="OR">OR ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="71b3b-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71b3b-104">`OR` 函数返回一个*布尔*值 **FALSE**（如果所有指定条件都为 false）。</span><span class="sxs-lookup"><span data-stu-id="71b3b-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="71b3b-105">如果所有指定条件都为 true，此函数返回一个*布尔*值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="71b3b-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b3b-106">语法</span><span class="sxs-lookup"><span data-stu-id="71b3b-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="71b3b-107">参数</span><span class="sxs-lookup"><span data-stu-id="71b3b-107">Arguments</span></span>

<span data-ttu-id="71b3b-108">`condition 1`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="71b3b-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="71b3b-109">必须测试的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="71b3b-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="71b3b-110">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="71b3b-110">This argument is required.</span></span>

<span data-ttu-id="71b3b-111">`condition N`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="71b3b-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="71b3b-112">必须测试的有效条件表达式。</span><span class="sxs-lookup"><span data-stu-id="71b3b-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="71b3b-113">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="71b3b-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="71b3b-114">返回值</span><span class="sxs-lookup"><span data-stu-id="71b3b-114">Return values</span></span>

<span data-ttu-id="71b3b-115">*布尔值*</span><span class="sxs-lookup"><span data-stu-id="71b3b-115">*Boolean*</span></span>

<span data-ttu-id="71b3b-116">生成的*布尔*值。</span><span class="sxs-lookup"><span data-stu-id="71b3b-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="71b3b-117">示例</span><span class="sxs-lookup"><span data-stu-id="71b3b-117">Example</span></span>

<span data-ttu-id="71b3b-118">`OR (1=2, "a"="a")` 返回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="71b3b-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71b3b-119">其他资源</span><span class="sxs-lookup"><span data-stu-id="71b3b-119">Additional resources</span></span>

[<span data-ttu-id="71b3b-120">逻辑函数</span><span class="sxs-lookup"><span data-stu-id="71b3b-120">Logical functions</span></span>](er-functions-category-logical.md)
