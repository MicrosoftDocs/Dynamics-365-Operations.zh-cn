---
title: MID ER 函数
description: 本主题提供有关 MID 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: e2addace5c5606ebaae56ca658700347978a805b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744711"
---
# <a name="mid-er-function"></a><span data-ttu-id="bab21-103">MID ER 函数</span><span class="sxs-lookup"><span data-stu-id="bab21-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bab21-104">`MID` 函数返回*字符串*值，该值在指定位置的开始处，在指定的字符串中显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="bab21-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab21-105">语法</span><span class="sxs-lookup"><span data-stu-id="bab21-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="bab21-106">参数</span><span class="sxs-lookup"><span data-stu-id="bab21-106">Arguments</span></span>

<span data-ttu-id="bab21-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="bab21-107">`text`: *String*</span></span>

<span data-ttu-id="bab21-108">指定要从中返回字符的文本的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="bab21-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="bab21-109">`starting position`：*整数*</span><span class="sxs-lookup"><span data-stu-id="bab21-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="bab21-110">指定必须从指定文本返回的第一个字符的位置的*整数*值。</span><span class="sxs-lookup"><span data-stu-id="bab21-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="bab21-111">`number of characters`：*整数*</span><span class="sxs-lookup"><span data-stu-id="bab21-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="bab21-112">指定必须从指定开始位置开始返回的字符数量的*整数*值。</span><span class="sxs-lookup"><span data-stu-id="bab21-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="bab21-113">返回值</span><span class="sxs-lookup"><span data-stu-id="bab21-113">Return values</span></span>

<span data-ttu-id="bab21-114">*字符串*</span><span class="sxs-lookup"><span data-stu-id="bab21-114">*String*</span></span>

<span data-ttu-id="bab21-115">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="bab21-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bab21-116">使用说明</span><span class="sxs-lookup"><span data-stu-id="bab21-116">Usage notes</span></span>

<span data-ttu-id="bab21-117">如果 `starting position` 参数的值小于 0（零），返回的字符从指定字符串中的第一个位置开始计数。</span><span class="sxs-lookup"><span data-stu-id="bab21-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="bab21-118">如果 `starting position` 参数的值超过指定字符串的长度，将返回一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="bab21-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="bab21-119">示例</span><span class="sxs-lookup"><span data-stu-id="bab21-119">Example</span></span>

<span data-ttu-id="bab21-120">`MID ("Sample", 2, 3)` 返回 **"amp"**。</span><span class="sxs-lookup"><span data-stu-id="bab21-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bab21-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="bab21-121">Additional resources</span></span>

[<span data-ttu-id="bab21-122">文本函数</span><span class="sxs-lookup"><span data-stu-id="bab21-122">Text functions</span></span>](er-functions-category-text.md)
