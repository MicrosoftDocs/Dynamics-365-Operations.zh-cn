---
title: ABS ER 函数
description: 本主题提供有关 ABS 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 3c7156b9990397822a6bea9ed8b3df8f65490572
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683273"
---
# <a name="abs-er-function"></a><span data-ttu-id="5acc5-103">ABS ER 函数</span><span class="sxs-lookup"><span data-stu-id="5acc5-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5acc5-104">`ABS` 函数作为 *实数* 值返回指定数字的绝对值（模数）。</span><span class="sxs-lookup"><span data-stu-id="5acc5-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="5acc5-105">即，返回不带符号的数字。</span><span class="sxs-lookup"><span data-stu-id="5acc5-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="5acc5-106">语法</span><span class="sxs-lookup"><span data-stu-id="5acc5-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="5acc5-107">参数</span><span class="sxs-lookup"><span data-stu-id="5acc5-107">Arguments</span></span>

<span data-ttu-id="5acc5-108">`number`：*实数*</span><span class="sxs-lookup"><span data-stu-id="5acc5-108">`number`: *Real*</span></span>

<span data-ttu-id="5acc5-109">您想要的模数的数值。</span><span class="sxs-lookup"><span data-stu-id="5acc5-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="5acc5-110">返回值</span><span class="sxs-lookup"><span data-stu-id="5acc5-110">Return values</span></span>

<span data-ttu-id="5acc5-111">*实数*</span><span class="sxs-lookup"><span data-stu-id="5acc5-111">*Real*</span></span>

<span data-ttu-id="5acc5-112">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="5acc5-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="5acc5-113">示例</span><span class="sxs-lookup"><span data-stu-id="5acc5-113">Example</span></span>

<span data-ttu-id="5acc5-114">`ABS (-1)` 将返回 **1**。</span><span class="sxs-lookup"><span data-stu-id="5acc5-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5acc5-115">其他资源</span><span class="sxs-lookup"><span data-stu-id="5acc5-115">Additional resources</span></span>

[<span data-ttu-id="5acc5-116">数学函数</span><span class="sxs-lookup"><span data-stu-id="5acc5-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
