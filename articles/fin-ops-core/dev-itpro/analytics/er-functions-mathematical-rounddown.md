---
title: ROUNDDOWN ER 函数
description: 本主题提供有关 ROUNDDOWN 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686874"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="22436-103">ROUNDDOWN ER 函数</span><span class="sxs-lookup"><span data-stu-id="22436-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22436-104">`ROUNDDOWN` 函数作为 *实数* 值返回已向下舍入到指定小数位数的指定数字。</span><span class="sxs-lookup"><span data-stu-id="22436-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="22436-105">语法</span><span class="sxs-lookup"><span data-stu-id="22436-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="22436-106">参数</span><span class="sxs-lookup"><span data-stu-id="22436-106">Arguments</span></span>

<span data-ttu-id="22436-107">`number`：*实数*</span><span class="sxs-lookup"><span data-stu-id="22436-107">`number`: *Real*</span></span>

<span data-ttu-id="22436-108">必须向下舍入的数值。</span><span class="sxs-lookup"><span data-stu-id="22436-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="22436-109">`decimals`：*整数*</span><span class="sxs-lookup"><span data-stu-id="22436-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="22436-110">代表小数位数的数字值。</span><span class="sxs-lookup"><span data-stu-id="22436-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="22436-111">返回值</span><span class="sxs-lookup"><span data-stu-id="22436-111">Return values</span></span>

<span data-ttu-id="22436-112">*实数*</span><span class="sxs-lookup"><span data-stu-id="22436-112">*Real*</span></span>

<span data-ttu-id="22436-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="22436-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="22436-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="22436-114">Usage notes</span></span>

<span data-ttu-id="22436-115">此函数类似 [ROUND](er-functions-mathematical-round.md)，但始终向下（朝零）化整到指定的数字。</span><span class="sxs-lookup"><span data-stu-id="22436-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="22436-116">示例 1</span><span class="sxs-lookup"><span data-stu-id="22436-116">Example 1</span></span>

<span data-ttu-id="22436-117">`ROUNDDOWN (1200.767, 2)` 向下舍入到两位小数，返回 **1200.76**。</span><span class="sxs-lookup"><span data-stu-id="22436-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="22436-118">示例 2</span><span class="sxs-lookup"><span data-stu-id="22436-118">Example 2</span></span>

<span data-ttu-id="22436-119">`ROUNDDOWN (1700.767, -3)` 向下舍入到最接近的 1,000 的倍数，返回 **1000**。</span><span class="sxs-lookup"><span data-stu-id="22436-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="22436-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="22436-120">Additional resources</span></span>

[<span data-ttu-id="22436-121">数学函数</span><span class="sxs-lookup"><span data-stu-id="22436-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
