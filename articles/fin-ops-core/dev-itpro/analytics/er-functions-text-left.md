---
title: LEFT ER 函数
description: 本主题提供有关 LEFT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: 69b1d95ea0e82b1947b665b0724cff6c5b319633
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746331"
---
# <a name="left-er-function"></a><span data-ttu-id="4141a-103">LEFT ER 函数</span><span class="sxs-lookup"><span data-stu-id="4141a-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4141a-104">`LEFT` 函数返回 *字符串* 值，该值在指定字符串的开头显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="4141a-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4141a-105">语法</span><span class="sxs-lookup"><span data-stu-id="4141a-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="4141a-106">参数</span><span class="sxs-lookup"><span data-stu-id="4141a-106">Arguments</span></span>

<span data-ttu-id="4141a-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="4141a-107">`text`: *String*</span></span>

<span data-ttu-id="4141a-108">代表原始文本的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="4141a-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="4141a-109">`number`：*整数*</span><span class="sxs-lookup"><span data-stu-id="4141a-109">`number`: *Integer*</span></span>

<span data-ttu-id="4141a-110">必须在原始文本开头返回的字符数。</span><span class="sxs-lookup"><span data-stu-id="4141a-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="4141a-111">返回值</span><span class="sxs-lookup"><span data-stu-id="4141a-111">Return values</span></span>

<span data-ttu-id="4141a-112">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4141a-112">*String*</span></span>

<span data-ttu-id="4141a-113">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="4141a-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4141a-114">示例</span><span class="sxs-lookup"><span data-stu-id="4141a-114">Example</span></span>

<span data-ttu-id="4141a-115">`LEFT ("Sample", 3)` 返回 **"Sam"**。</span><span class="sxs-lookup"><span data-stu-id="4141a-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4141a-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="4141a-116">Additional resources</span></span>

[<span data-ttu-id="4141a-117">文本函数</span><span class="sxs-lookup"><span data-stu-id="4141a-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]