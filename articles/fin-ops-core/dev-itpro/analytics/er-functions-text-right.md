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
ms.openlocfilehash: dd53ece77b08fc9723c838da5ba08bf3825b5e56
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743703"
---
# <a name="right-er-function"></a><span data-ttu-id="641f2-103">RIGHT ER 函数</span><span class="sxs-lookup"><span data-stu-id="641f2-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="641f2-104">`RIGHT` 函数返回*字符串*值，该值在指定字符串的末尾显示指定的字符数量。</span><span class="sxs-lookup"><span data-stu-id="641f2-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="641f2-105">语法</span><span class="sxs-lookup"><span data-stu-id="641f2-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="641f2-106">参数</span><span class="sxs-lookup"><span data-stu-id="641f2-106">Arguments</span></span>

<span data-ttu-id="641f2-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="641f2-107">`text`: *String*</span></span>

<span data-ttu-id="641f2-108">代表原始文本的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="641f2-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="641f2-109">`number`：*整数*</span><span class="sxs-lookup"><span data-stu-id="641f2-109">`number`: *Integer*</span></span>

<span data-ttu-id="641f2-110">必须在原始文本结尾返回的字符数。</span><span class="sxs-lookup"><span data-stu-id="641f2-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="641f2-111">返回值</span><span class="sxs-lookup"><span data-stu-id="641f2-111">Return values</span></span>

<span data-ttu-id="641f2-112">*字符串*</span><span class="sxs-lookup"><span data-stu-id="641f2-112">*String*</span></span>

<span data-ttu-id="641f2-113">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="641f2-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="641f2-114">示例</span><span class="sxs-lookup"><span data-stu-id="641f2-114">Example</span></span>

<span data-ttu-id="641f2-115">`RIGHT ("Sample", 3)` 返回 **"ple"**。</span><span class="sxs-lookup"><span data-stu-id="641f2-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="641f2-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="641f2-116">Additional resources</span></span>

[<span data-ttu-id="641f2-117">文本函数</span><span class="sxs-lookup"><span data-stu-id="641f2-117">Text functions</span></span>](er-functions-category-text.md)
