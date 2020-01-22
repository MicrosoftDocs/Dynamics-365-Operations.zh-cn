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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80f0606dc3842cdfa56d41e2815eccd7518218b8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916514"
---
# <span data-ttu-id="f0c6d-103"><a name="NUMBERVALUE">NUMBERVALUE ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="f0c6d-103"><a name="NUMBERVALUE">NUMBERVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0c6d-104">`NUMBERVALUE` 函数返回一个*实数*值，该值从指定的*字符串*值转换而来。</span><span class="sxs-lookup"><span data-stu-id="f0c6d-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="f0c6d-105">在转换过程中，将考虑指定的十进制和数字分组分隔符。</span><span class="sxs-lookup"><span data-stu-id="f0c6d-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c6d-106">语法</span><span class="sxs-lookup"><span data-stu-id="f0c6d-106">Syntax</span></span>

```
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="f0c6d-107">参数</span><span class="sxs-lookup"><span data-stu-id="f0c6d-107">Arguments</span></span>

<span data-ttu-id="f0c6d-108">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="f0c6d-108">`text`: *String*</span></span>

<span data-ttu-id="f0c6d-109">必须转换为*实数*数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="f0c6d-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="f0c6d-110">`decimal separator`：字符串</span><span class="sxs-lookup"><span data-stu-id="f0c6d-110">`decimal separator`: String</span></span>

<span data-ttu-id="f0c6d-111">小数点分隔符。</span><span class="sxs-lookup"><span data-stu-id="f0c6d-111">A decimal separator.</span></span> <span data-ttu-id="f0c6d-112">用于分隔十进制数的整数和小数部分。</span><span class="sxs-lookup"><span data-stu-id="f0c6d-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="f0c6d-113">`digit grouping separator`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="f0c6d-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="f0c6d-114">数字分组分隔符。</span><span class="sxs-lookup"><span data-stu-id="f0c6d-114">A digit grouping separator.</span></span> <span data-ttu-id="f0c6d-115">用作千位分隔符。</span><span class="sxs-lookup"><span data-stu-id="f0c6d-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="f0c6d-116">返回值</span><span class="sxs-lookup"><span data-stu-id="f0c6d-116">Return values</span></span>

<span data-ttu-id="f0c6d-117">*实数*</span><span class="sxs-lookup"><span data-stu-id="f0c6d-117">*Real*</span></span>

<span data-ttu-id="f0c6d-118">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="f0c6d-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="f0c6d-119">示例</span><span class="sxs-lookup"><span data-stu-id="f0c6d-119">Example</span></span>

<span data-ttu-id="f0c6d-120">`NUMBERVALUE( "1 234,56", ",", " ")` 将返回 **1234.56**。</span><span class="sxs-lookup"><span data-stu-id="f0c6d-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0c6d-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="f0c6d-121">Additional resources</span></span>

[<span data-ttu-id="f0c6d-122">类型转换函数</span><span class="sxs-lookup"><span data-stu-id="f0c6d-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
