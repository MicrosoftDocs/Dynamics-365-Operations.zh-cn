---
title: REPLACE ER 函数
description: 本主题提供有关 REPLACE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: d9c66f4c96f35e3ad5fc92e7925b5cd07c956aac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916859"
---
# <span data-ttu-id="a7cdf-103"><a name="REPLACE">REPLACE ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="a7cdf-103"><a name="REPLACE">REPLACE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7cdf-104">在将全部或部分指定文本字符串替换为另一个字符串之后，`REPLACE` 函数作为*字符串*值返回指定的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7cdf-105">语法</span><span class="sxs-lookup"><span data-stu-id="a7cdf-105">Syntax</span></span>

```
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="a7cdf-106">参数</span><span class="sxs-lookup"><span data-stu-id="a7cdf-106">Arguments</span></span>

<span data-ttu-id="a7cdf-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="a7cdf-107">`text`: *String*</span></span>

<span data-ttu-id="a7cdf-108">*字符串*类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="a7cdf-109">`pattern`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="a7cdf-109">`pattern`: *String*</span></span>

<span data-ttu-id="a7cdf-110">如果 `regular expression flag` 参数是 **FALSE**，此参数包含必须替换的文本。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="a7cdf-111">如果 `regular expression flag` 参数是 **TRUE**，此参数包含定义搜索模式和替换文本的正则表达式。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="a7cdf-112">`replacement`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="a7cdf-112">`replacement`: *String*</span></span>

<span data-ttu-id="a7cdf-113">如果 `regular expression flag` 参数是 **FALSE**，此参数包含要用作替换的文本。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="a7cdf-114">如果 `regular expression flag` 参数是 **TRUE**，则不使用此参数。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="a7cdf-115">`regular expression flag`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="a7cdf-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="a7cdf-116">指示是否使用正则表达式进行替换的*布尔*值。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="a7cdf-117">返回值</span><span class="sxs-lookup"><span data-stu-id="a7cdf-117">Return values</span></span>

<span data-ttu-id="a7cdf-118">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a7cdf-118">*String*</span></span>

<span data-ttu-id="a7cdf-119">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a7cdf-120">使用说明</span><span class="sxs-lookup"><span data-stu-id="a7cdf-120">Usage notes</span></span>

<span data-ttu-id="a7cdf-121">如果 `regular expression flag` 参数是 **TRUE**，此函数将在通过应用 `pattern` 参数指定的正则表达式更改指定的字符串后返回该字符串。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="a7cdf-122">此正则表达式用于查找必须替换的字符。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="a7cdf-123">如果 `regular expression flag` 参数是 **FALSE**，此函数的行为类似于 [TRANSLATE](er-functions-text-translate.md)。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-123">If the `regular expression flag` argument is **FALSE**, this function behaves like [TRANSLATE](er-functions-text-translate.md).</span></span> <span data-ttu-id="a7cdf-124">由 `replacement` 参数指定的字符用于替换找到的字符。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-124">The characters that are specified by the `replacement` argument are used to replace the characters that are found.</span></span> 

## <a name="example-1"></a><span data-ttu-id="a7cdf-125">示例 1</span><span class="sxs-lookup"><span data-stu-id="a7cdf-125">Example 1</span></span>

<span data-ttu-id="a7cdf-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` 应用删除所有非数字符号的正则表达式，返回 **"19234564971"**。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-126">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="a7cdf-127">示例 2</span><span class="sxs-lookup"><span data-stu-id="a7cdf-127">Example 2</span></span>

<span data-ttu-id="a7cdf-128">`REPLACE ("abcdef", "cd", "GH", false)` 将模式 **"cd"** 替换为字符串 **"GH"**，返回 **"abGHef"**。</span><span class="sxs-lookup"><span data-stu-id="a7cdf-128">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7cdf-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="a7cdf-129">Additional resources</span></span>

[<span data-ttu-id="a7cdf-130">文本函数</span><span class="sxs-lookup"><span data-stu-id="a7cdf-130">Text functions</span></span>](er-functions-category-text.md)
