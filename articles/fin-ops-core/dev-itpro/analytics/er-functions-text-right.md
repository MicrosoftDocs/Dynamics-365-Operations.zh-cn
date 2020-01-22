---
title: RIGHT ER 函数
description: 本主题提供有关 RIGHT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 01718f9b153c1d6c46d50a9b17e899ccfba16915
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916721"
---
# <span data-ttu-id="5569c-103"><a name="RIGHT">RIGHT ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="5569c-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5569c-104">`RIGHT` 函数返回*字符串*值，该值在指定字符串的末尾显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="5569c-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5569c-105">语法</span><span class="sxs-lookup"><span data-stu-id="5569c-105">Syntax</span></span>

```
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="5569c-106">参数</span><span class="sxs-lookup"><span data-stu-id="5569c-106">Arguments</span></span>

<span data-ttu-id="5569c-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="5569c-107">`text`: *String*</span></span>

<span data-ttu-id="5569c-108">代表原始文本的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="5569c-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="5569c-109">`number`：*整数*</span><span class="sxs-lookup"><span data-stu-id="5569c-109">`number`: *Integer*</span></span>

<span data-ttu-id="5569c-110">必须在原始文本结尾返回的字符数。</span><span class="sxs-lookup"><span data-stu-id="5569c-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="5569c-111">返回值</span><span class="sxs-lookup"><span data-stu-id="5569c-111">Return values</span></span>

<span data-ttu-id="5569c-112">*字符串*</span><span class="sxs-lookup"><span data-stu-id="5569c-112">*String*</span></span>

<span data-ttu-id="5569c-113">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="5569c-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5569c-114">示例</span><span class="sxs-lookup"><span data-stu-id="5569c-114">Example</span></span>

<span data-ttu-id="5569c-115">`RIGHT ("Sample", 3)` 返回 **"ple"**。</span><span class="sxs-lookup"><span data-stu-id="5569c-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5569c-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="5569c-116">Additional resources</span></span>

[<span data-ttu-id="5569c-117">文本函数</span><span class="sxs-lookup"><span data-stu-id="5569c-117">Text functions</span></span>](er-functions-category-text.md)
