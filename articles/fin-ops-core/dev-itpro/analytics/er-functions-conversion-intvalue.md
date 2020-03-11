---
title: INTVALUE ER 函数
description: 本主题提供有关 INTVALUE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 5e06236bf1d158a4cf579b8b89cc0a5f7d815c38
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042636"
---
# <span data-ttu-id="0d326-103"><a name="INTVALUE">INTVALUE ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="0d326-103"><a name="INTVALUE">INTVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d326-104">`INTVALUE` 函数返回一个 *Int* 值，该值表示指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="0d326-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0d326-105">语法 1</span><span class="sxs-lookup"><span data-stu-id="0d326-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="0d326-106">语法 2</span><span class="sxs-lookup"><span data-stu-id="0d326-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="0d326-107">参数</span><span class="sxs-lookup"><span data-stu-id="0d326-107">Arguments</span></span>

<span data-ttu-id="0d326-108">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="0d326-108">`text`: *String*</span></span>

<span data-ttu-id="0d326-109">必须转换为 *Int* 数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="0d326-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="0d326-110">`number`：*实数*或*整数*</span><span class="sxs-lookup"><span data-stu-id="0d326-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="0d326-111">必须转换为 *Int* 数字的*实数*或*整数*数字值。</span><span class="sxs-lookup"><span data-stu-id="0d326-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="0d326-112">返回值</span><span class="sxs-lookup"><span data-stu-id="0d326-112">Return values</span></span>

<span data-ttu-id="0d326-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="0d326-113">*Int*</span></span>

<span data-ttu-id="0d326-114">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="0d326-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0d326-115">使用说明</span><span class="sxs-lookup"><span data-stu-id="0d326-115">Usage notes</span></span>

<span data-ttu-id="0d326-116">将截断所有小数部分。</span><span class="sxs-lookup"><span data-stu-id="0d326-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="0d326-117">示例 1</span><span class="sxs-lookup"><span data-stu-id="0d326-117">Example 1</span></span>

<span data-ttu-id="0d326-118">`INTVALUE ("100.77")` 返回 *Int* 值 **100**。</span><span class="sxs-lookup"><span data-stu-id="0d326-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="0d326-119">示例 2</span><span class="sxs-lookup"><span data-stu-id="0d326-119">Example 2</span></span>

<span data-ttu-id="0d326-120">`INTVALUE (-100.77)` 返回 *Int* 值 **-100**。</span><span class="sxs-lookup"><span data-stu-id="0d326-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d326-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="0d326-121">Additional resources</span></span>

[<span data-ttu-id="0d326-122">类型转换函数</span><span class="sxs-lookup"><span data-stu-id="0d326-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
