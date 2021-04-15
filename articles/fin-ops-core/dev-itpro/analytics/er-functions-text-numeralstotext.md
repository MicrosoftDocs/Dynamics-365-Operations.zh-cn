---
title: NUMERALSTOTEXT ER 函数
description: 本主题提供有关 NUMERALSTOTEXT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: e26890a0d99e0df631a3b3350d284e63aaed8e09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746139"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="ad06b-103">NUMERALSTOTEXT ER 函数</span><span class="sxs-lookup"><span data-stu-id="ad06b-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad06b-104">在使用指定语言拼出（即转换为文本字符串）指定数字后，`NUMERALSTOTEXT` 函数作为 *字符串* 返回指定数字。</span><span class="sxs-lookup"><span data-stu-id="ad06b-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad06b-105">语法</span><span class="sxs-lookup"><span data-stu-id="ad06b-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="ad06b-106">参数</span><span class="sxs-lookup"><span data-stu-id="ad06b-106">Arguments</span></span>

<span data-ttu-id="ad06b-107">`number`：*整数* 或 *实数*</span><span class="sxs-lookup"><span data-stu-id="ad06b-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="ad06b-108">指定必须拼出的数字的数字值。</span><span class="sxs-lookup"><span data-stu-id="ad06b-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="ad06b-109">`language`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="ad06b-109">`language`: *String*</span></span>

<span data-ttu-id="ad06b-110">代表语言代码的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="ad06b-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="ad06b-111">`currency`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="ad06b-111">`currency`: *String*</span></span>

<span data-ttu-id="ad06b-112">代表币种代码的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="ad06b-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="ad06b-113">`print currency name flag`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="ad06b-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="ad06b-114">指示是否必须将货币名称添加到拼出的文本的 *布尔* 值。</span><span class="sxs-lookup"><span data-stu-id="ad06b-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="ad06b-115">`decimal points`：*整数*</span><span class="sxs-lookup"><span data-stu-id="ad06b-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="ad06b-116">指示拼出的文本应具有的小数位数的 *整数* 值。</span><span class="sxs-lookup"><span data-stu-id="ad06b-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="ad06b-117">返回值</span><span class="sxs-lookup"><span data-stu-id="ad06b-117">Return values</span></span>

<span data-ttu-id="ad06b-118">*字符串*</span><span class="sxs-lookup"><span data-stu-id="ad06b-118">*String*</span></span>

<span data-ttu-id="ad06b-119">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="ad06b-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ad06b-120">使用说明</span><span class="sxs-lookup"><span data-stu-id="ad06b-120">Usage notes</span></span>

<span data-ttu-id="ad06b-121">语言代码可选。</span><span class="sxs-lookup"><span data-stu-id="ad06b-121">The language code is optional.</span></span> <span data-ttu-id="ad06b-122">如果定义为空字符串，将使用运行上下文的语言代码。</span><span class="sxs-lookup"><span data-stu-id="ad06b-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="ad06b-123">默认语言代码为 **EN-US**。</span><span class="sxs-lookup"><span data-stu-id="ad06b-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="ad06b-124">运行上下文的语言代码在正在运行的电子申报 (ER) 格式的 **文件夹** 或 **文件** 元素中定义。</span><span class="sxs-lookup"><span data-stu-id="ad06b-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="ad06b-125">币种代码可选。</span><span class="sxs-lookup"><span data-stu-id="ad06b-125">The currency code is optional.</span></span> <span data-ttu-id="ad06b-126">如果定义为空字符串，将使用运行上下文的公司币种。</span><span class="sxs-lookup"><span data-stu-id="ad06b-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="ad06b-127">仅为以下语言代码分析 `print currency name flag` 和 `decimal points` 参数：**CS**、**ET**、**HU**、**LT**、**LV**、**PL** 和 **RU**。</span><span class="sxs-lookup"><span data-stu-id="ad06b-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="ad06b-128">此外，仅为国家或地区的上下文支持货币名称偏差的公司分析 `print currency name flag` 参数。</span><span class="sxs-lookup"><span data-stu-id="ad06b-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="ad06b-129">示例 1</span><span class="sxs-lookup"><span data-stu-id="ad06b-129">Example 1</span></span>

<span data-ttu-id="ad06b-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` 返回 **"One Thousand Two Hundred Thirty Four and 56"**。</span><span class="sxs-lookup"><span data-stu-id="ad06b-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ad06b-131">示例 2</span><span class="sxs-lookup"><span data-stu-id="ad06b-131">Example 2</span></span>

<span data-ttu-id="ad06b-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` 返回 **"Sto dwadzieścia"**。</span><span class="sxs-lookup"><span data-stu-id="ad06b-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="ad06b-133">示例 3</span><span class="sxs-lookup"><span data-stu-id="ad06b-133">Example 3</span></span>

<span data-ttu-id="ad06b-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` 返回 **"Сто двадцать евро 21 евроцент"**。</span><span class="sxs-lookup"><span data-stu-id="ad06b-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad06b-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="ad06b-135">Additional resources</span></span>

[<span data-ttu-id="ad06b-136">文本函数</span><span class="sxs-lookup"><span data-stu-id="ad06b-136">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]