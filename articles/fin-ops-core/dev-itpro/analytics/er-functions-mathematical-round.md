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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041599"
---
# <span data-ttu-id="860ca-103"><a name="ROUND">ROUND ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="860ca-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="860ca-104">`ROUND` 函数作为*实数*值返回已舍入到指定小数位数的指定数字。</span><span class="sxs-lookup"><span data-stu-id="860ca-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="860ca-105">语法</span><span class="sxs-lookup"><span data-stu-id="860ca-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="860ca-106">参数</span><span class="sxs-lookup"><span data-stu-id="860ca-106">Arguments</span></span>

<span data-ttu-id="860ca-107">`number`：*实数*</span><span class="sxs-lookup"><span data-stu-id="860ca-107">`number`: *Real*</span></span>

<span data-ttu-id="860ca-108">必须舍入的数值。</span><span class="sxs-lookup"><span data-stu-id="860ca-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="860ca-109">`decimals`：*整数*</span><span class="sxs-lookup"><span data-stu-id="860ca-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="860ca-110">代表小数位数的数字值。</span><span class="sxs-lookup"><span data-stu-id="860ca-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="860ca-111">返回值</span><span class="sxs-lookup"><span data-stu-id="860ca-111">Return values</span></span>

<span data-ttu-id="860ca-112">*实数*</span><span class="sxs-lookup"><span data-stu-id="860ca-112">*Real*</span></span>

<span data-ttu-id="860ca-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="860ca-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="860ca-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="860ca-114">Usage notes</span></span>

<span data-ttu-id="860ca-115">如果 `decimals` 参数的值大于 0（零），则指定的数值舍入到这个多位小数位数。</span><span class="sxs-lookup"><span data-stu-id="860ca-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="860ca-116">如果 `decimals` 参数的值为 **0**（零），则指定的数值舍入到最近的整数。</span><span class="sxs-lookup"><span data-stu-id="860ca-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="860ca-117">如果 `decimals` 参数的值小于 0（零），则指定的数值舍入到小数点左边。</span><span class="sxs-lookup"><span data-stu-id="860ca-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="860ca-118">示例 1</span><span class="sxs-lookup"><span data-stu-id="860ca-118">Example 1</span></span>

<span data-ttu-id="860ca-119">`ROUND (1200.767, 2)` 舍入到两位小数，返回 **1200.77**。</span><span class="sxs-lookup"><span data-stu-id="860ca-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="860ca-120">示例 2</span><span class="sxs-lookup"><span data-stu-id="860ca-120">Example 2</span></span>

<span data-ttu-id="860ca-121">`ROUND (1200.767, -3)` 舍入到最接近的 1,000 的倍数，返回 **1000**。</span><span class="sxs-lookup"><span data-stu-id="860ca-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="860ca-122">其他资源</span><span class="sxs-lookup"><span data-stu-id="860ca-122">Additional resources</span></span>

[<span data-ttu-id="860ca-123">数学函数</span><span class="sxs-lookup"><span data-stu-id="860ca-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
