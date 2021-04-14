---
title: NUMBERVALUE ER 函数
description: 本主题提供有关 NUMBERVALUE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755340"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="824ce-103">NUMBERVALUE ER 函数</span><span class="sxs-lookup"><span data-stu-id="824ce-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="824ce-104">`NUMBERVALUE` 函数返回一个 *实数* 值，该值从指定的 *字符串* 值转换而来。</span><span class="sxs-lookup"><span data-stu-id="824ce-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="824ce-105">在转换过程中，将考虑指定的十进制和数字分组分隔符。</span><span class="sxs-lookup"><span data-stu-id="824ce-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="824ce-106">语法</span><span class="sxs-lookup"><span data-stu-id="824ce-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="824ce-107">参数</span><span class="sxs-lookup"><span data-stu-id="824ce-107">Arguments</span></span>

<span data-ttu-id="824ce-108">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="824ce-108">`text`: *String*</span></span>

<span data-ttu-id="824ce-109">必须转换为 *实数* 数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="824ce-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="824ce-110">`decimal separator`：字符串</span><span class="sxs-lookup"><span data-stu-id="824ce-110">`decimal separator`: String</span></span>

<span data-ttu-id="824ce-111">小数点分隔符。</span><span class="sxs-lookup"><span data-stu-id="824ce-111">A decimal separator.</span></span> <span data-ttu-id="824ce-112">用于分隔十进制数的整数和小数部分。</span><span class="sxs-lookup"><span data-stu-id="824ce-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="824ce-113">`digit grouping separator`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="824ce-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="824ce-114">数字分组分隔符。</span><span class="sxs-lookup"><span data-stu-id="824ce-114">A digit grouping separator.</span></span> <span data-ttu-id="824ce-115">用作千位分隔符。</span><span class="sxs-lookup"><span data-stu-id="824ce-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="824ce-116">返回值</span><span class="sxs-lookup"><span data-stu-id="824ce-116">Return values</span></span>

<span data-ttu-id="824ce-117">*实数*</span><span class="sxs-lookup"><span data-stu-id="824ce-117">*Real*</span></span>

<span data-ttu-id="824ce-118">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="824ce-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="824ce-119">示例</span><span class="sxs-lookup"><span data-stu-id="824ce-119">Example</span></span>

<span data-ttu-id="824ce-120">`NUMBERVALUE( "1 234,56", ",", " ")` 将返回 **1234.56**。</span><span class="sxs-lookup"><span data-stu-id="824ce-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="824ce-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="824ce-121">Additional resources</span></span>

[<span data-ttu-id="824ce-122">类型转换函数</span><span class="sxs-lookup"><span data-stu-id="824ce-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]