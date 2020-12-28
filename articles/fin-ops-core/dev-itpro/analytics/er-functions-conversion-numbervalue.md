---
title: NUMBERVALUE ER 函数
description: 本主题提供有关 NUMBERVALUE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: d3eec6dc5a472f366c9029456fe05cf1e431e1c5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685971"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="228ef-103">NUMBERVALUE ER 函数</span><span class="sxs-lookup"><span data-stu-id="228ef-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="228ef-104">`NUMBERVALUE` 函数返回一个 *实数* 值，该值从指定的 *字符串* 值转换而来。</span><span class="sxs-lookup"><span data-stu-id="228ef-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="228ef-105">在转换过程中，将考虑指定的十进制和数字分组分隔符。</span><span class="sxs-lookup"><span data-stu-id="228ef-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="228ef-106">语法</span><span class="sxs-lookup"><span data-stu-id="228ef-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="228ef-107">参数</span><span class="sxs-lookup"><span data-stu-id="228ef-107">Arguments</span></span>

<span data-ttu-id="228ef-108">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="228ef-108">`text`: *String*</span></span>

<span data-ttu-id="228ef-109">必须转换为 *实数* 数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="228ef-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="228ef-110">`decimal separator`：字符串</span><span class="sxs-lookup"><span data-stu-id="228ef-110">`decimal separator`: String</span></span>

<span data-ttu-id="228ef-111">小数点分隔符。</span><span class="sxs-lookup"><span data-stu-id="228ef-111">A decimal separator.</span></span> <span data-ttu-id="228ef-112">用于分隔十进制数的整数和小数部分。</span><span class="sxs-lookup"><span data-stu-id="228ef-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="228ef-113">`digit grouping separator`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="228ef-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="228ef-114">数字分组分隔符。</span><span class="sxs-lookup"><span data-stu-id="228ef-114">A digit grouping separator.</span></span> <span data-ttu-id="228ef-115">用作千位分隔符。</span><span class="sxs-lookup"><span data-stu-id="228ef-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="228ef-116">返回值</span><span class="sxs-lookup"><span data-stu-id="228ef-116">Return values</span></span>

<span data-ttu-id="228ef-117">*实数*</span><span class="sxs-lookup"><span data-stu-id="228ef-117">*Real*</span></span>

<span data-ttu-id="228ef-118">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="228ef-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="228ef-119">示例</span><span class="sxs-lookup"><span data-stu-id="228ef-119">Example</span></span>

<span data-ttu-id="228ef-120">`NUMBERVALUE( "1 234,56", ",", " ")` 将返回 **1234.56**。</span><span class="sxs-lookup"><span data-stu-id="228ef-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="228ef-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="228ef-121">Additional resources</span></span>

[<span data-ttu-id="228ef-122">类型转换函数</span><span class="sxs-lookup"><span data-stu-id="228ef-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
