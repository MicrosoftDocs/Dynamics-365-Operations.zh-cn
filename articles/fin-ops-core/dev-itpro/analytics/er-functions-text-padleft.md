---
title: PADLEFT ER 函数
description: 本主题提供有关 PADLEFT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 806b1d318f18b0ade01f7b03909c90b1e4fd29b1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746235"
---
# <a name="padleft-er-function"></a><span data-ttu-id="0ddd4-103">PADLEFT ER 函数</span><span class="sxs-lookup"><span data-stu-id="0ddd4-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ddd4-104">`PADLEFT` 函数返回指定长度的 *字符串* 值，其中指定字符串的开头是使用指定字符填充的。</span><span class="sxs-lookup"><span data-stu-id="0ddd4-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ddd4-105">语法</span><span class="sxs-lookup"><span data-stu-id="0ddd4-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="0ddd4-106">参数</span><span class="sxs-lookup"><span data-stu-id="0ddd4-106">Arguments</span></span>

<span data-ttu-id="0ddd4-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="0ddd4-107">`text`: *String*</span></span>

<span data-ttu-id="0ddd4-108">代表原始文本的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="0ddd4-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="0ddd4-109">`length`：*整数*</span><span class="sxs-lookup"><span data-stu-id="0ddd4-109">`length`: *Integer*</span></span>

<span data-ttu-id="0ddd4-110">表示填充的字符串中最终的字符数的 *整数* 值。</span><span class="sxs-lookup"><span data-stu-id="0ddd4-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="0ddd4-111">`padding chars`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="0ddd4-111">`padding chars`: *String*</span></span>

<span data-ttu-id="0ddd4-112">用于填充的字符。</span><span class="sxs-lookup"><span data-stu-id="0ddd4-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="0ddd4-113">返回值</span><span class="sxs-lookup"><span data-stu-id="0ddd4-113">Return values</span></span>

<span data-ttu-id="0ddd4-114">*字符串*</span><span class="sxs-lookup"><span data-stu-id="0ddd4-114">*String*</span></span>

<span data-ttu-id="0ddd4-115">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="0ddd4-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0ddd4-116">示例</span><span class="sxs-lookup"><span data-stu-id="0ddd4-116">Example</span></span>

<span data-ttu-id="0ddd4-117">`PADLEFT ("1234", 10, "`&nbsp;`")` 返回文本字符串 **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**。</span><span class="sxs-lookup"><span data-stu-id="0ddd4-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0ddd4-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="0ddd4-118">Additional resources</span></span>

[<span data-ttu-id="0ddd4-119">文本函数</span><span class="sxs-lookup"><span data-stu-id="0ddd4-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]