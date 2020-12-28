---
title: ROUNDUP ER 函数
description: 本主题提供有关 ROUNDUP 电子申报 (ER) 函数如何使用的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8ed86e2a848248dd8f2fc99401d12e0a162bf20a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686826"
---
# <a name="roundup-er-function"></a><span data-ttu-id="6ee69-103">ROUNDUP ER 函数</span><span class="sxs-lookup"><span data-stu-id="6ee69-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ee69-104">`ROUNDUP` 函数作为 *实数* 值返回已向上舍入到指定小数位数的指定数字。</span><span class="sxs-lookup"><span data-stu-id="6ee69-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ee69-105">语法</span><span class="sxs-lookup"><span data-stu-id="6ee69-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="6ee69-106">参数</span><span class="sxs-lookup"><span data-stu-id="6ee69-106">Arguments</span></span>

<span data-ttu-id="6ee69-107">`number`：*实数*</span><span class="sxs-lookup"><span data-stu-id="6ee69-107">`number`: *Real*</span></span>

<span data-ttu-id="6ee69-108">必须向上舍入的数值。</span><span class="sxs-lookup"><span data-stu-id="6ee69-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="6ee69-109">`decimals`：*整数*</span><span class="sxs-lookup"><span data-stu-id="6ee69-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="6ee69-110">代表小数位数的数字值。</span><span class="sxs-lookup"><span data-stu-id="6ee69-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="6ee69-111">返回值</span><span class="sxs-lookup"><span data-stu-id="6ee69-111">Return values</span></span>

<span data-ttu-id="6ee69-112">*实数*</span><span class="sxs-lookup"><span data-stu-id="6ee69-112">*Real*</span></span>

<span data-ttu-id="6ee69-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="6ee69-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6ee69-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="6ee69-114">Usage notes</span></span>

<span data-ttu-id="6ee69-115">此函数类似 [ROUND](er-functions-mathematical-round.md)，但始终向上（不朝零）化整到指定的数字。</span><span class="sxs-lookup"><span data-stu-id="6ee69-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="6ee69-116">示例 1</span><span class="sxs-lookup"><span data-stu-id="6ee69-116">Example 1</span></span>

<span data-ttu-id="6ee69-117">`ROUNDUP (1200.763, 2)` 向上舍入到两位小数，返回 **1200.77**。</span><span class="sxs-lookup"><span data-stu-id="6ee69-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6ee69-118">示例 2</span><span class="sxs-lookup"><span data-stu-id="6ee69-118">Example 2</span></span>

<span data-ttu-id="6ee69-119">`ROUNDUP (1200.767, -3)` 向上舍入到最接近的 1,000 的倍数，返回 **2000**。</span><span class="sxs-lookup"><span data-stu-id="6ee69-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ee69-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="6ee69-120">Additional resources</span></span>

[<span data-ttu-id="6ee69-121">数学函数</span><span class="sxs-lookup"><span data-stu-id="6ee69-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
