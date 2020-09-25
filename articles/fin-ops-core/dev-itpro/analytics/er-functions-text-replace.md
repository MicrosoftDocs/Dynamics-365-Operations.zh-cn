---
title: REPLACE ER 函数
description: 本主题提供有关 REPLACE 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: c9e64bd8e039b4eeca829c3c37299f002ba03592
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743727"
---
# <a name="replace-er-function"></a><span data-ttu-id="a6780-103">REPLACE ER 函数</span><span class="sxs-lookup"><span data-stu-id="a6780-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6780-104">在将全部或部分指定文本字符串替换为另一个字符串之后，`REPLACE` 函数作为*字符串*值返回指定的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="a6780-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6780-105">语法</span><span class="sxs-lookup"><span data-stu-id="a6780-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="a6780-106">参数</span><span class="sxs-lookup"><span data-stu-id="a6780-106">Arguments</span></span>

<span data-ttu-id="a6780-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="a6780-107">`text`: *String*</span></span>

<span data-ttu-id="a6780-108">*字符串*类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="a6780-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="a6780-109">`pattern`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="a6780-109">`pattern`: *String*</span></span>

<span data-ttu-id="a6780-110">如果 `regular expression flag` 参数是 **FALSE**，此参数包含必须替换的文本。</span><span class="sxs-lookup"><span data-stu-id="a6780-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="a6780-111">如果 `regular expression flag` 参数是 **TRUE**，此参数包含定义搜索模式和替换文本的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="a6780-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="a6780-112">`replacement`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="a6780-112">`replacement`: *String*</span></span>

<span data-ttu-id="a6780-113">如果 `regular expression flag` 参数是 **FALSE**，此参数包含要用作替换的文本。</span><span class="sxs-lookup"><span data-stu-id="a6780-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="a6780-114">如果 `regular expression flag` 参数是 **TRUE**，则不使用此参数。</span><span class="sxs-lookup"><span data-stu-id="a6780-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="a6780-115">`regular expression flag`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="a6780-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="a6780-116">指示是否使用正则表达式进行替换的*布尔*值。</span><span class="sxs-lookup"><span data-stu-id="a6780-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="a6780-117">返回值</span><span class="sxs-lookup"><span data-stu-id="a6780-117">Return values</span></span>

<span data-ttu-id="a6780-118">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a6780-118">*String*</span></span>

<span data-ttu-id="a6780-119">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="a6780-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a6780-120">使用说明</span><span class="sxs-lookup"><span data-stu-id="a6780-120">Usage notes</span></span>

<span data-ttu-id="a6780-121">如果 `regular expression flag` 参数是 **TRUE**，此函数将在通过应用 `pattern` 参数指定的正则表达式更改指定的字符串后返回该字符串。</span><span class="sxs-lookup"><span data-stu-id="a6780-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="a6780-122">此正则表达式用于查找必须替换的字符。</span><span class="sxs-lookup"><span data-stu-id="a6780-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="a6780-123">如果 `regular expression flag` 参数为 **FALSE**，在 `pattern` 中定义的字符集被 `replacement` 参数的字符替换后，此函数将返回指定的字符串。</span><span class="sxs-lookup"><span data-stu-id="a6780-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="a6780-124">示例 1</span><span class="sxs-lookup"><span data-stu-id="a6780-124">Example 1</span></span>

<span data-ttu-id="a6780-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` 应用删除所有非数字符号的正则表达式，返回 **"19234564971"**。</span><span class="sxs-lookup"><span data-stu-id="a6780-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="a6780-126">示例 2</span><span class="sxs-lookup"><span data-stu-id="a6780-126">Example 2</span></span>

<span data-ttu-id="a6780-127">`REPLACE ("abcdef", "cd", "GH", false)` 将模式 **"cd"** 替换为字符串 **"GH"**，返回 **"abGHef"**。</span><span class="sxs-lookup"><span data-stu-id="a6780-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6780-128">其他资源</span><span class="sxs-lookup"><span data-stu-id="a6780-128">Additional resources</span></span>

[<span data-ttu-id="a6780-129">文本函数</span><span class="sxs-lookup"><span data-stu-id="a6780-129">Text functions</span></span>](er-functions-category-text.md)
