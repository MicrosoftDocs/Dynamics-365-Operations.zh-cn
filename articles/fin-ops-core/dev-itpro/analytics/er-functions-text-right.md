---
title: RIGHT ER 函数
description: 本主题提供有关 RIGHT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 75255eccf4da468b0946253f7570b1621f905cd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570232"
---
# <a name="right-er-function"></a><span data-ttu-id="727df-103">RIGHT ER 函数</span><span class="sxs-lookup"><span data-stu-id="727df-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="727df-104">`RIGHT` 函数返回 *字符串* 值，该值在指定字符串的末尾显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="727df-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="727df-105">语法</span><span class="sxs-lookup"><span data-stu-id="727df-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="727df-106">参数</span><span class="sxs-lookup"><span data-stu-id="727df-106">Arguments</span></span>

<span data-ttu-id="727df-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="727df-107">`text`: *String*</span></span>

<span data-ttu-id="727df-108">代表原始文本的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="727df-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="727df-109">`number`：*整数*</span><span class="sxs-lookup"><span data-stu-id="727df-109">`number`: *Integer*</span></span>

<span data-ttu-id="727df-110">必须在原始文本结尾返回的字符数。</span><span class="sxs-lookup"><span data-stu-id="727df-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="727df-111">返回值</span><span class="sxs-lookup"><span data-stu-id="727df-111">Return values</span></span>

<span data-ttu-id="727df-112">*字符串*</span><span class="sxs-lookup"><span data-stu-id="727df-112">*String*</span></span>

<span data-ttu-id="727df-113">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="727df-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="727df-114">示例</span><span class="sxs-lookup"><span data-stu-id="727df-114">Example</span></span>

<span data-ttu-id="727df-115">`RIGHT ("Sample", 3)` 返回 **"ple"**。</span><span class="sxs-lookup"><span data-stu-id="727df-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="727df-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="727df-116">Additional resources</span></span>

[<span data-ttu-id="727df-117">文本函数</span><span class="sxs-lookup"><span data-stu-id="727df-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]