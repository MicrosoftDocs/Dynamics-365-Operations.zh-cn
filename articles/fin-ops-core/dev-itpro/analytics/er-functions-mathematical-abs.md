---
title: ABS ER 函数
description: 本主题提供有关 ABS 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 12165174806395b3c36a1dbb227ed7a86def77b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565776"
---
# <a name="abs-er-function"></a><span data-ttu-id="06399-103">ABS ER 函数</span><span class="sxs-lookup"><span data-stu-id="06399-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06399-104">`ABS` 函数作为 *实数* 值返回指定数字的绝对值（模数）。</span><span class="sxs-lookup"><span data-stu-id="06399-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="06399-105">即，返回不带符号的数字。</span><span class="sxs-lookup"><span data-stu-id="06399-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="06399-106">语法</span><span class="sxs-lookup"><span data-stu-id="06399-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="06399-107">参数</span><span class="sxs-lookup"><span data-stu-id="06399-107">Arguments</span></span>

<span data-ttu-id="06399-108">`number`：*实数*</span><span class="sxs-lookup"><span data-stu-id="06399-108">`number`: *Real*</span></span>

<span data-ttu-id="06399-109">您想要的模数的数值。</span><span class="sxs-lookup"><span data-stu-id="06399-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="06399-110">返回值</span><span class="sxs-lookup"><span data-stu-id="06399-110">Return values</span></span>

<span data-ttu-id="06399-111">*实数*</span><span class="sxs-lookup"><span data-stu-id="06399-111">*Real*</span></span>

<span data-ttu-id="06399-112">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="06399-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="06399-113">示例</span><span class="sxs-lookup"><span data-stu-id="06399-113">Example</span></span>

<span data-ttu-id="06399-114">`ABS (-1)` 将返回 **1**。</span><span class="sxs-lookup"><span data-stu-id="06399-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="06399-115">其他资源</span><span class="sxs-lookup"><span data-stu-id="06399-115">Additional resources</span></span>

[<span data-ttu-id="06399-116">数学函数</span><span class="sxs-lookup"><span data-stu-id="06399-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]