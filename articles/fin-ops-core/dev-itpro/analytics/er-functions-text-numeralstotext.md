---
title: NUMERALSTOTEXT ER 函数
description: 本主题提供有关 NUMERALSTOTEXT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 31fd4076d04ce7d849555bc8301c4d23ad8e1a7e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041001"
---
# <span data-ttu-id="2ee9c-103"><a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="2ee9c-103"><a name="NUMERALSTOTEXT">NUMERALSTOTEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ee9c-104">在使用指定语言拼出（即转换为文本字符串）指定数字后，`NUMERALSTOTEXT` 函数作为*字符串*返回指定数字。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ee9c-105">语法</span><span class="sxs-lookup"><span data-stu-id="2ee9c-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="2ee9c-106">参数</span><span class="sxs-lookup"><span data-stu-id="2ee9c-106">Arguments</span></span>

<span data-ttu-id="2ee9c-107">`number`：*整数*或*实数*</span><span class="sxs-lookup"><span data-stu-id="2ee9c-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="2ee9c-108">指定必须拼出的数字的数字值。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="2ee9c-109">`language`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="2ee9c-109">`language`: *String*</span></span>

<span data-ttu-id="2ee9c-110">代表语言代码的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="2ee9c-111">`currency`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="2ee9c-111">`currency`: *String*</span></span>

<span data-ttu-id="2ee9c-112">代表币种代码的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="2ee9c-113">`print currency name flag`：*布尔值*</span><span class="sxs-lookup"><span data-stu-id="2ee9c-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="2ee9c-114">指示是否必须将货币名称添加到拼出的文本的*布尔*值。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="2ee9c-115">`decimal points`：*整数*</span><span class="sxs-lookup"><span data-stu-id="2ee9c-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="2ee9c-116">指示拼出的文本应具有的小数位数的*整数*值。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ee9c-117">返回值</span><span class="sxs-lookup"><span data-stu-id="2ee9c-117">Return values</span></span>

<span data-ttu-id="2ee9c-118">*字符串*</span><span class="sxs-lookup"><span data-stu-id="2ee9c-118">*String*</span></span>

<span data-ttu-id="2ee9c-119">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2ee9c-120">使用说明</span><span class="sxs-lookup"><span data-stu-id="2ee9c-120">Usage notes</span></span>

<span data-ttu-id="2ee9c-121">语言代码可选。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-121">The language code is optional.</span></span> <span data-ttu-id="2ee9c-122">如果定义为空字符串，将使用运行上下文的语言代码。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="2ee9c-123">默认语言代码为 **EN-US**。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="2ee9c-124">运行上下文的语言代码在正在运行的电子申报 (ER) 格式的**文件夹**或**文件**元素中定义。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="2ee9c-125">币种代码可选。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-125">The currency code is optional.</span></span> <span data-ttu-id="2ee9c-126">如果定义为空字符串，将使用运行上下文的公司币种。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="2ee9c-127">仅为以下语言代码分析 `print currency name flag` 和 `decimal points` 参数：**CS**、**ET**、**HU**、**LT**、**LV**、**PL** 和 **RU**。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="2ee9c-128">此外，仅为国家或地区的上下文支持货币名称偏差的公司分析 `print currency name flag` 参数。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="2ee9c-129">示例 1</span><span class="sxs-lookup"><span data-stu-id="2ee9c-129">Example 1</span></span>

<span data-ttu-id="2ee9c-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` 返回 **"One Thousand Two Hundred Thirty Four and 56"**。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="2ee9c-131">示例 2</span><span class="sxs-lookup"><span data-stu-id="2ee9c-131">Example 2</span></span>

<span data-ttu-id="2ee9c-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` 返回 **"Sto dwadzieścia"**。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="2ee9c-133">示例 3</span><span class="sxs-lookup"><span data-stu-id="2ee9c-133">Example 3</span></span>

<span data-ttu-id="2ee9c-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` 返回 **"Сто двадцать евро 21 евроцент"**。</span><span class="sxs-lookup"><span data-stu-id="2ee9c-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ee9c-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="2ee9c-135">Additional resources</span></span>

[<span data-ttu-id="2ee9c-136">文本函数</span><span class="sxs-lookup"><span data-stu-id="2ee9c-136">Text functions</span></span>](er-functions-category-text.md)
