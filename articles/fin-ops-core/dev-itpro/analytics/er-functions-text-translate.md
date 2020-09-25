---
title: TRANSLATE ER 函数
description: 本主题提供有关 TRANSLATE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 51b9a2e25a9f1dfc08e9e0f7fc3ad84b359a6d1b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744231"
---
# <a name="translate-er-function"></a><span data-ttu-id="485fb-103">TRANSLATE ER 函数</span><span class="sxs-lookup"><span data-stu-id="485fb-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="485fb-104">`TRANSLATE` 函数返回一个*字符串*值，该值中包含对提供的另一个字符集中的指定文本进行字符替换的结果。</span><span class="sxs-lookup"><span data-stu-id="485fb-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="485fb-105">语法</span><span class="sxs-lookup"><span data-stu-id="485fb-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="485fb-106">参数</span><span class="sxs-lookup"><span data-stu-id="485fb-106">Arguments</span></span>

<span data-ttu-id="485fb-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="485fb-107">`text`: *String*</span></span>

<span data-ttu-id="485fb-108">*字符串*类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="485fb-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="485fb-109">`pattern`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="485fb-109">`pattern`: *String*</span></span>

<span data-ttu-id="485fb-110">必须替换的文本。</span><span class="sxs-lookup"><span data-stu-id="485fb-110">The text that must be replaced.</span></span>

<span data-ttu-id="485fb-111">`replacement`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="485fb-111">`replacement`: *String*</span></span>

<span data-ttu-id="485fb-112">用作替换的文本。</span><span class="sxs-lookup"><span data-stu-id="485fb-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="485fb-113">返回值</span><span class="sxs-lookup"><span data-stu-id="485fb-113">Return values</span></span>

<span data-ttu-id="485fb-114">*字符串*</span><span class="sxs-lookup"><span data-stu-id="485fb-114">*String*</span></span>

<span data-ttu-id="485fb-115">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="485fb-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="485fb-116">使用说明</span><span class="sxs-lookup"><span data-stu-id="485fb-116">Usage notes</span></span>

<span data-ttu-id="485fb-117">`TRANSLATE` 函数一次替换一个字符。</span><span class="sxs-lookup"><span data-stu-id="485fb-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="485fb-118">此函数将 `text` 变量的第一个字符替换为 `pattern` 参数的第一个字符，然后替换第二个字符，并执行相同流程，直到完成。</span><span class="sxs-lookup"><span data-stu-id="485fb-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="485fb-119">当 `text` 和 `pattern` 变量中有一个字符匹配时，将被替换为 `replacement` 变量中与 `pattern` 变量中的字符位于同一个位置的字符。</span><span class="sxs-lookup"><span data-stu-id="485fb-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="485fb-120">如果某个字符在 `pattern` 变量中多次出现，则使用与此字符的第一次出现对应的 `replacement` 变量映射。</span><span class="sxs-lookup"><span data-stu-id="485fb-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="485fb-121">示例 1</span><span class="sxs-lookup"><span data-stu-id="485fb-121">Example 1</span></span>

<span data-ttu-id="485fb-122">因为下面的原因，`TRANSLATE ("abcdef", "cd", "GH")` 将指定的 **abcdef** 文本的 **c** 字符替换为 `replacement` 文本的 **G** 字符：</span><span class="sxs-lookup"><span data-stu-id="485fb-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="485fb-123">`pattern` 文本中第一个位置有 **c** 字符。</span><span class="sxs-lookup"><span data-stu-id="485fb-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="485fb-124">`replacement` 文本的第一个位置中包含 **G** 字符。</span><span class="sxs-lookup"><span data-stu-id="485fb-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="485fb-125">示例 2</span><span class="sxs-lookup"><span data-stu-id="485fb-125">Example 2</span></span>

<span data-ttu-id="485fb-126">`TRANSLATE ("abcdef", "ccd", "GH")` 返回 **abGdef**。</span><span class="sxs-lookup"><span data-stu-id="485fb-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="485fb-127">示例 3</span><span class="sxs-lookup"><span data-stu-id="485fb-127">Example 3</span></span>

<span data-ttu-id="485fb-128">`TRANSLATE ("abccba", "abc", "123")` 将返回 **"123321"**。</span><span class="sxs-lookup"><span data-stu-id="485fb-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="485fb-129">其他资源</span><span class="sxs-lookup"><span data-stu-id="485fb-129">Additional resources</span></span>

[<span data-ttu-id="485fb-130">文本函数</span><span class="sxs-lookup"><span data-stu-id="485fb-130">Text functions</span></span>](er-functions-category-text.md)
