---
title: LEFT ER 函数
description: 本主题提供有关 LEFT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 9e9cdff9bb5c22c74803cf17c056c0ff1af5ef43
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685875"
---
# <a name="left-er-function"></a><span data-ttu-id="11254-103">LEFT ER 函数</span><span class="sxs-lookup"><span data-stu-id="11254-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11254-104">`LEFT` 函数返回 *字符串* 值，该值在指定字符串的开头显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="11254-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="11254-105">语法</span><span class="sxs-lookup"><span data-stu-id="11254-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="11254-106">参数</span><span class="sxs-lookup"><span data-stu-id="11254-106">Arguments</span></span>

<span data-ttu-id="11254-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="11254-107">`text`: *String*</span></span>

<span data-ttu-id="11254-108">代表原始文本的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="11254-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="11254-109">`number`：*整数*</span><span class="sxs-lookup"><span data-stu-id="11254-109">`number`: *Integer*</span></span>

<span data-ttu-id="11254-110">必须在原始文本开头返回的字符数。</span><span class="sxs-lookup"><span data-stu-id="11254-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="11254-111">返回值</span><span class="sxs-lookup"><span data-stu-id="11254-111">Return values</span></span>

<span data-ttu-id="11254-112">*字符串*</span><span class="sxs-lookup"><span data-stu-id="11254-112">*String*</span></span>

<span data-ttu-id="11254-113">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="11254-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="11254-114">示例</span><span class="sxs-lookup"><span data-stu-id="11254-114">Example</span></span>

<span data-ttu-id="11254-115">`LEFT ("Sample", 3)` 返回 **"Sam"**。</span><span class="sxs-lookup"><span data-stu-id="11254-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11254-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="11254-116">Additional resources</span></span>

[<span data-ttu-id="11254-117">文本函数</span><span class="sxs-lookup"><span data-stu-id="11254-117">Text functions</span></span>](er-functions-category-text.md)
