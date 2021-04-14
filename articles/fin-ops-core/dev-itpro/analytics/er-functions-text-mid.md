---
title: MID ER 函数
description: 本主题提供有关 MID 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 9a9ff3f1055f6757d6d4073dbb816773d8bfc8ba
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746259"
---
# <a name="mid-er-function"></a><span data-ttu-id="0d30a-103">MID ER 函数</span><span class="sxs-lookup"><span data-stu-id="0d30a-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d30a-104">`MID` 函数返回 *字符串* 值，该值在指定位置的开始处，在指定的字符串中显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="0d30a-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d30a-105">语法</span><span class="sxs-lookup"><span data-stu-id="0d30a-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="0d30a-106">参数</span><span class="sxs-lookup"><span data-stu-id="0d30a-106">Arguments</span></span>

<span data-ttu-id="0d30a-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="0d30a-107">`text`: *String*</span></span>

<span data-ttu-id="0d30a-108">指定要从中返回字符的文本的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="0d30a-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="0d30a-109">`starting position`：*整数*</span><span class="sxs-lookup"><span data-stu-id="0d30a-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="0d30a-110">指定必须从指定文本返回的第一个字符的位置的 *整数* 值。</span><span class="sxs-lookup"><span data-stu-id="0d30a-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="0d30a-111">`number of characters`：*整数*</span><span class="sxs-lookup"><span data-stu-id="0d30a-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="0d30a-112">指定必须从指定开始位置开始返回的字符数量的 *整数* 值。</span><span class="sxs-lookup"><span data-stu-id="0d30a-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="0d30a-113">返回值</span><span class="sxs-lookup"><span data-stu-id="0d30a-113">Return values</span></span>

<span data-ttu-id="0d30a-114">*字符串*</span><span class="sxs-lookup"><span data-stu-id="0d30a-114">*String*</span></span>

<span data-ttu-id="0d30a-115">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="0d30a-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0d30a-116">使用说明</span><span class="sxs-lookup"><span data-stu-id="0d30a-116">Usage notes</span></span>

<span data-ttu-id="0d30a-117">如果 `starting position` 参数的值小于 0（零），返回的字符从指定字符串中的第一个位置开始计数。</span><span class="sxs-lookup"><span data-stu-id="0d30a-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="0d30a-118">如果 `starting position` 参数的值超过指定字符串的长度，将返回一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="0d30a-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="0d30a-119">示例</span><span class="sxs-lookup"><span data-stu-id="0d30a-119">Example</span></span>

<span data-ttu-id="0d30a-120">`MID ("Sample", 2, 3)` 返回 **"amp"**。</span><span class="sxs-lookup"><span data-stu-id="0d30a-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d30a-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="0d30a-121">Additional resources</span></span>

[<span data-ttu-id="0d30a-122">文本函数</span><span class="sxs-lookup"><span data-stu-id="0d30a-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]