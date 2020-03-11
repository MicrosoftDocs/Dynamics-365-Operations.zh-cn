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
ms.openlocfilehash: 6fbaf5952222d90a855956fb93713e0f9ef81305
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041016"
---
# <span data-ttu-id="52c13-103"><a name="MID">MID ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="52c13-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52c13-104">`MID` 函数返回*字符串*值，该值在指定位置的开始处，在指定的字符串中显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="52c13-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="52c13-105">语法</span><span class="sxs-lookup"><span data-stu-id="52c13-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="52c13-106">参数</span><span class="sxs-lookup"><span data-stu-id="52c13-106">Arguments</span></span>

<span data-ttu-id="52c13-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="52c13-107">`text`: *String*</span></span>

<span data-ttu-id="52c13-108">指定要从中返回字符的文本的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="52c13-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="52c13-109">`starting position`：*整数*</span><span class="sxs-lookup"><span data-stu-id="52c13-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="52c13-110">指定必须从指定文本返回的第一个字符的位置的*整数*值。</span><span class="sxs-lookup"><span data-stu-id="52c13-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="52c13-111">`number of characters`：*整数*</span><span class="sxs-lookup"><span data-stu-id="52c13-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="52c13-112">指定必须从指定开始位置开始返回的字符数量的*整数*值。</span><span class="sxs-lookup"><span data-stu-id="52c13-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="52c13-113">返回值</span><span class="sxs-lookup"><span data-stu-id="52c13-113">Return values</span></span>

<span data-ttu-id="52c13-114">*字符串*</span><span class="sxs-lookup"><span data-stu-id="52c13-114">*String*</span></span>

<span data-ttu-id="52c13-115">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="52c13-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="52c13-116">使用说明</span><span class="sxs-lookup"><span data-stu-id="52c13-116">Usage notes</span></span>

<span data-ttu-id="52c13-117">如果 `starting position` 参数的值小于 0（零），返回的字符从指定字符串中的第一个位置开始计数。</span><span class="sxs-lookup"><span data-stu-id="52c13-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="52c13-118">如果 `starting position` 参数的值超过指定字符串的长度，将返回一个空字符串。</span><span class="sxs-lookup"><span data-stu-id="52c13-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="52c13-119">示例</span><span class="sxs-lookup"><span data-stu-id="52c13-119">Example</span></span>

<span data-ttu-id="52c13-120">`MID ("Sample", 2, 3)` 返回 **"amp"**。</span><span class="sxs-lookup"><span data-stu-id="52c13-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52c13-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="52c13-121">Additional resources</span></span>

[<span data-ttu-id="52c13-122">文本函数</span><span class="sxs-lookup"><span data-stu-id="52c13-122">Text functions</span></span>](er-functions-category-text.md)
