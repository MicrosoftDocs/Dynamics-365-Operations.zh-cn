---
title: PADLEFT ER 函数
description: 本主题提供有关 PADLEFT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 3f8a8e2006fe279b25bbf154c6e1802babf51117
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744351"
---
# <a name="padleft-er-function"></a><span data-ttu-id="41771-103">PADLEFT ER 函数</span><span class="sxs-lookup"><span data-stu-id="41771-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41771-104">`PADLEFT` 函数返回指定长度的*字符串*值，其中指定字符串的开头是使用指定字符填充的。</span><span class="sxs-lookup"><span data-stu-id="41771-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="41771-105">语法</span><span class="sxs-lookup"><span data-stu-id="41771-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="41771-106">参数</span><span class="sxs-lookup"><span data-stu-id="41771-106">Arguments</span></span>

<span data-ttu-id="41771-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="41771-107">`text`: *String*</span></span>

<span data-ttu-id="41771-108">代表原始文本的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="41771-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="41771-109">`length`：*整数*</span><span class="sxs-lookup"><span data-stu-id="41771-109">`length`: *Integer*</span></span>

<span data-ttu-id="41771-110">表示填充的字符串中最终的字符数的*整数*值。</span><span class="sxs-lookup"><span data-stu-id="41771-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="41771-111">`padding chars`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="41771-111">`padding chars`: *String*</span></span>

<span data-ttu-id="41771-112">用于填充的字符。</span><span class="sxs-lookup"><span data-stu-id="41771-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="41771-113">返回值</span><span class="sxs-lookup"><span data-stu-id="41771-113">Return values</span></span>

<span data-ttu-id="41771-114">*字符串*</span><span class="sxs-lookup"><span data-stu-id="41771-114">*String*</span></span>

<span data-ttu-id="41771-115">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="41771-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="41771-116">示例</span><span class="sxs-lookup"><span data-stu-id="41771-116">Example</span></span>

<span data-ttu-id="41771-117">`PADLEFT ("1234", 10, "`&nbsp;`")` 返回文本字符串 **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**。</span><span class="sxs-lookup"><span data-stu-id="41771-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41771-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="41771-118">Additional resources</span></span>

[<span data-ttu-id="41771-119">文本函数</span><span class="sxs-lookup"><span data-stu-id="41771-119">Text functions</span></span>](er-functions-category-text.md)
