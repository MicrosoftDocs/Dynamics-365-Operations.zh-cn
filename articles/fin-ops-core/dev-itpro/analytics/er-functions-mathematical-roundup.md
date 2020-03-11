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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1784ab3587a090c8e5535509a1ba52fc85111daa
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041569"
---
# <span data-ttu-id="73eab-103"><a name="ROUNDUP">ROUNDUP ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="73eab-103"><a name="ROUNDUP">ROUNDUP ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73eab-104">`ROUNDUP` 函数作为*实数*值返回已向上舍入到指定小数位数的指定数字。</span><span class="sxs-lookup"><span data-stu-id="73eab-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="73eab-105">语法</span><span class="sxs-lookup"><span data-stu-id="73eab-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="73eab-106">参数</span><span class="sxs-lookup"><span data-stu-id="73eab-106">Arguments</span></span>

<span data-ttu-id="73eab-107">`number`：*实数*</span><span class="sxs-lookup"><span data-stu-id="73eab-107">`number`: *Real*</span></span>

<span data-ttu-id="73eab-108">必须向上舍入的数值。</span><span class="sxs-lookup"><span data-stu-id="73eab-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="73eab-109">`decimals`：*整数*</span><span class="sxs-lookup"><span data-stu-id="73eab-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="73eab-110">代表小数位数的数字值。</span><span class="sxs-lookup"><span data-stu-id="73eab-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="73eab-111">返回值</span><span class="sxs-lookup"><span data-stu-id="73eab-111">Return values</span></span>

<span data-ttu-id="73eab-112">*实数*</span><span class="sxs-lookup"><span data-stu-id="73eab-112">*Real*</span></span>

<span data-ttu-id="73eab-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="73eab-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="73eab-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="73eab-114">Usage notes</span></span>

<span data-ttu-id="73eab-115">此函数类似 [ROUND](er-functions-mathematical-round.md)，但始终向上（不朝零）化整到指定的数字。</span><span class="sxs-lookup"><span data-stu-id="73eab-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="73eab-116">示例 1</span><span class="sxs-lookup"><span data-stu-id="73eab-116">Example 1</span></span>

<span data-ttu-id="73eab-117">`ROUNDUP (1200.763, 2)` 向上舍入到两位小数，返回 **1200.77**。</span><span class="sxs-lookup"><span data-stu-id="73eab-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="73eab-118">示例 2</span><span class="sxs-lookup"><span data-stu-id="73eab-118">Example 2</span></span>

<span data-ttu-id="73eab-119">`ROUNDUP (1200.767, -3)` 向上舍入到最接近的 1,000 的倍数，返回 **2000**。</span><span class="sxs-lookup"><span data-stu-id="73eab-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73eab-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="73eab-120">Additional resources</span></span>

[<span data-ttu-id="73eab-121">数学函数</span><span class="sxs-lookup"><span data-stu-id="73eab-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
