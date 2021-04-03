---
title: INTVALUE ER 函数
description: 本主题提供有关 INTVALUE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 64f43ad29d59ade1e124b6800734b003f6ca07df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561462"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="1d7fe-103">INTVALUE ER 函数</span><span class="sxs-lookup"><span data-stu-id="1d7fe-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d7fe-104">`INTVALUE` 函数返回一个 *Int* 值，该值表示指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="1d7fe-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1d7fe-105">语法 1</span><span class="sxs-lookup"><span data-stu-id="1d7fe-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="1d7fe-106">语法 2</span><span class="sxs-lookup"><span data-stu-id="1d7fe-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="1d7fe-107">参数</span><span class="sxs-lookup"><span data-stu-id="1d7fe-107">Arguments</span></span>

<span data-ttu-id="1d7fe-108">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="1d7fe-108">`text`: *String*</span></span>

<span data-ttu-id="1d7fe-109">必须转换为 *Int* 数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="1d7fe-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="1d7fe-110">`number`：*实数* 或 *整数*</span><span class="sxs-lookup"><span data-stu-id="1d7fe-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="1d7fe-111">必须转换为 *Int* 数字的 *实数* 或 *整数* 数字值。</span><span class="sxs-lookup"><span data-stu-id="1d7fe-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="1d7fe-112">返回值</span><span class="sxs-lookup"><span data-stu-id="1d7fe-112">Return values</span></span>

<span data-ttu-id="1d7fe-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="1d7fe-113">*Int*</span></span>

<span data-ttu-id="1d7fe-114">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="1d7fe-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1d7fe-115">使用说明</span><span class="sxs-lookup"><span data-stu-id="1d7fe-115">Usage notes</span></span>

<span data-ttu-id="1d7fe-116">将截断所有小数部分。</span><span class="sxs-lookup"><span data-stu-id="1d7fe-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="1d7fe-117">示例 1</span><span class="sxs-lookup"><span data-stu-id="1d7fe-117">Example 1</span></span>

<span data-ttu-id="1d7fe-118">`INTVALUE ("100.77")` 返回 *Int* 值 **100**。</span><span class="sxs-lookup"><span data-stu-id="1d7fe-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1d7fe-119">示例 2</span><span class="sxs-lookup"><span data-stu-id="1d7fe-119">Example 2</span></span>

<span data-ttu-id="1d7fe-120">`INTVALUE (-100.77)` 返回 *Int* 值 **-100**。</span><span class="sxs-lookup"><span data-stu-id="1d7fe-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d7fe-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="1d7fe-121">Additional resources</span></span>

[<span data-ttu-id="1d7fe-122">类型转换函数</span><span class="sxs-lookup"><span data-stu-id="1d7fe-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]