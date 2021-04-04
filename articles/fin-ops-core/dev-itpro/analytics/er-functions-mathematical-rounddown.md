---
title: ROUNDDOWN ER 函数
description: 本主题提供有关 ROUNDDOWN 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: f199d662eb31f184b6f978b3d251e64907254584
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567132"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="339b3-103">ROUNDDOWN ER 函数</span><span class="sxs-lookup"><span data-stu-id="339b3-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="339b3-104">`ROUNDDOWN` 函数作为 *实数* 值返回已向下舍入到指定小数位数的指定数字。</span><span class="sxs-lookup"><span data-stu-id="339b3-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="339b3-105">语法</span><span class="sxs-lookup"><span data-stu-id="339b3-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="339b3-106">参数</span><span class="sxs-lookup"><span data-stu-id="339b3-106">Arguments</span></span>

<span data-ttu-id="339b3-107">`number`：*实数*</span><span class="sxs-lookup"><span data-stu-id="339b3-107">`number`: *Real*</span></span>

<span data-ttu-id="339b3-108">必须向下舍入的数值。</span><span class="sxs-lookup"><span data-stu-id="339b3-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="339b3-109">`decimals`：*整数*</span><span class="sxs-lookup"><span data-stu-id="339b3-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="339b3-110">代表小数位数的数字值。</span><span class="sxs-lookup"><span data-stu-id="339b3-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="339b3-111">返回值</span><span class="sxs-lookup"><span data-stu-id="339b3-111">Return values</span></span>

<span data-ttu-id="339b3-112">*实数*</span><span class="sxs-lookup"><span data-stu-id="339b3-112">*Real*</span></span>

<span data-ttu-id="339b3-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="339b3-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="339b3-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="339b3-114">Usage notes</span></span>

<span data-ttu-id="339b3-115">此函数类似 [ROUND](er-functions-mathematical-round.md)，但始终向下（朝零）化整到指定的数字。</span><span class="sxs-lookup"><span data-stu-id="339b3-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="339b3-116">示例 1</span><span class="sxs-lookup"><span data-stu-id="339b3-116">Example 1</span></span>

<span data-ttu-id="339b3-117">`ROUNDDOWN (1200.767, 2)` 向下舍入到两位小数，返回 **1200.76**。</span><span class="sxs-lookup"><span data-stu-id="339b3-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="339b3-118">示例 2</span><span class="sxs-lookup"><span data-stu-id="339b3-118">Example 2</span></span>

<span data-ttu-id="339b3-119">`ROUNDDOWN (1700.767, -3)` 向下舍入到最接近的 1,000 的倍数，返回 **1000**。</span><span class="sxs-lookup"><span data-stu-id="339b3-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="339b3-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="339b3-120">Additional resources</span></span>

[<span data-ttu-id="339b3-121">数学函数</span><span class="sxs-lookup"><span data-stu-id="339b3-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]