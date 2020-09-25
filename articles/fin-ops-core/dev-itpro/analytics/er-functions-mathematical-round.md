---
title: ROUND ER 函数
description: 本主题提供有关 ROUND 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 12af71a024a76fca98fc2e876da9b59e5762cf07
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744543"
---
# <a name="round-er-function"></a><span data-ttu-id="c10ba-103">ROUND ER 函数</span><span class="sxs-lookup"><span data-stu-id="c10ba-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c10ba-104">`ROUND` 函数作为*实数*值返回已舍入到指定小数位数的指定数字。</span><span class="sxs-lookup"><span data-stu-id="c10ba-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="c10ba-105">语法</span><span class="sxs-lookup"><span data-stu-id="c10ba-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="c10ba-106">参数</span><span class="sxs-lookup"><span data-stu-id="c10ba-106">Arguments</span></span>

<span data-ttu-id="c10ba-107">`number`：*实数*</span><span class="sxs-lookup"><span data-stu-id="c10ba-107">`number`: *Real*</span></span>

<span data-ttu-id="c10ba-108">必须舍入的数值。</span><span class="sxs-lookup"><span data-stu-id="c10ba-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="c10ba-109">`decimals`：*整数*</span><span class="sxs-lookup"><span data-stu-id="c10ba-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="c10ba-110">代表小数位数的数字值。</span><span class="sxs-lookup"><span data-stu-id="c10ba-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="c10ba-111">返回值</span><span class="sxs-lookup"><span data-stu-id="c10ba-111">Return values</span></span>

<span data-ttu-id="c10ba-112">*实数*</span><span class="sxs-lookup"><span data-stu-id="c10ba-112">*Real*</span></span>

<span data-ttu-id="c10ba-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="c10ba-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c10ba-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="c10ba-114">Usage notes</span></span>

<span data-ttu-id="c10ba-115">如果 `decimals` 参数的值大于 0（零），则指定的数值舍入到这个多位小数位数。</span><span class="sxs-lookup"><span data-stu-id="c10ba-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="c10ba-116">如果 `decimals` 参数的值为 **0**（零），则指定的数值舍入到最近的整数。</span><span class="sxs-lookup"><span data-stu-id="c10ba-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="c10ba-117">如果 `decimals` 参数的值小于 0（零），则指定的数值舍入到小数点左边。</span><span class="sxs-lookup"><span data-stu-id="c10ba-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="c10ba-118">示例 1</span><span class="sxs-lookup"><span data-stu-id="c10ba-118">Example 1</span></span>

<span data-ttu-id="c10ba-119">`ROUND (1200.767, 2)` 舍入到两位小数，返回 **1200.77**。</span><span class="sxs-lookup"><span data-stu-id="c10ba-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="c10ba-120">示例 2</span><span class="sxs-lookup"><span data-stu-id="c10ba-120">Example 2</span></span>

<span data-ttu-id="c10ba-121">`ROUND (1200.767, -3)` 舍入到最接近的 1,000 的倍数，返回 **1000**。</span><span class="sxs-lookup"><span data-stu-id="c10ba-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c10ba-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="c10ba-122">Additional resources</span></span>

[<span data-ttu-id="c10ba-123">数学函数</span><span class="sxs-lookup"><span data-stu-id="c10ba-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
