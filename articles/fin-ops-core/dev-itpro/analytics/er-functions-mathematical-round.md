---
title: ROUND ER 函数
description: 本主题提供有关 ROUND 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 716ac0bbc9fec992ec1bbfc99bfc86434bf97984
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570390"
---
# <a name="round-er-function"></a><span data-ttu-id="2ebeb-103">ROUND ER 函数</span><span class="sxs-lookup"><span data-stu-id="2ebeb-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ebeb-104">`ROUND` 函数作为 *实数* 值返回已舍入到指定小数位数的指定数字。</span><span class="sxs-lookup"><span data-stu-id="2ebeb-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebeb-105">语法</span><span class="sxs-lookup"><span data-stu-id="2ebeb-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="2ebeb-106">参数</span><span class="sxs-lookup"><span data-stu-id="2ebeb-106">Arguments</span></span>

<span data-ttu-id="2ebeb-107">`number`：*实数*</span><span class="sxs-lookup"><span data-stu-id="2ebeb-107">`number`: *Real*</span></span>

<span data-ttu-id="2ebeb-108">必须舍入的数值。</span><span class="sxs-lookup"><span data-stu-id="2ebeb-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="2ebeb-109">`decimals`：*整数*</span><span class="sxs-lookup"><span data-stu-id="2ebeb-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="2ebeb-110">代表小数位数的数字值。</span><span class="sxs-lookup"><span data-stu-id="2ebeb-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ebeb-111">返回值</span><span class="sxs-lookup"><span data-stu-id="2ebeb-111">Return values</span></span>

<span data-ttu-id="2ebeb-112">*实数*</span><span class="sxs-lookup"><span data-stu-id="2ebeb-112">*Real*</span></span>

<span data-ttu-id="2ebeb-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="2ebeb-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2ebeb-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="2ebeb-114">Usage notes</span></span>

<span data-ttu-id="2ebeb-115">如果 `decimals` 参数的值大于 0（零），则指定的数值舍入到这个多位小数位数。</span><span class="sxs-lookup"><span data-stu-id="2ebeb-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="2ebeb-116">如果 `decimals` 参数的值为 **0**（零），则指定的数值舍入到最近的偶数。</span><span class="sxs-lookup"><span data-stu-id="2ebeb-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="2ebeb-117">如果 `decimals` 参数的值小于 0（零），则指定的数值舍入到小数点左边。</span><span class="sxs-lookup"><span data-stu-id="2ebeb-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="2ebeb-118">示例 1</span><span class="sxs-lookup"><span data-stu-id="2ebeb-118">Example 1</span></span>

<span data-ttu-id="2ebeb-119">`ROUND (1200.767, 2)` 舍入到两位小数，返回 **1200.77**。</span><span class="sxs-lookup"><span data-stu-id="2ebeb-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2ebeb-120">示例 2</span><span class="sxs-lookup"><span data-stu-id="2ebeb-120">Example 2</span></span>

<span data-ttu-id="2ebeb-121">`ROUND (1200.767, -3)` 舍入到最接近的 1,000 的倍数，返回 **1000**。</span><span class="sxs-lookup"><span data-stu-id="2ebeb-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="2ebeb-122">示例 3</span><span class="sxs-lookup"><span data-stu-id="2ebeb-122">Example 3</span></span>

<span data-ttu-id="2ebeb-123">`ROUND (1200.5, 0)` 舍入到最近的偶数并返回 **1200**，而 `ROUND (1201.5, 0)` 执行同样的操作并返回 **1202**。</span><span class="sxs-lookup"><span data-stu-id="2ebeb-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ebeb-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="2ebeb-124">Additional resources</span></span>

[<span data-ttu-id="2ebeb-125">数学函数</span><span class="sxs-lookup"><span data-stu-id="2ebeb-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]