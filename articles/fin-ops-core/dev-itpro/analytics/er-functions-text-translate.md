---
title: TRANSLATE ER 函数
description: 本主题提供有关 TRANSLATE 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040902"
---
# <span data-ttu-id="1aa5c-103"><a name="TRANSLATE">TRANSLATE ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="1aa5c-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1aa5c-104">在将全部或部分指定文本字符串替换为另一个字符串之后，`TRANSLATE` 函数作为*字符串*值返回指定的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aa5c-105">语法</span><span class="sxs-lookup"><span data-stu-id="1aa5c-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="1aa5c-106">参数</span><span class="sxs-lookup"><span data-stu-id="1aa5c-106">Arguments</span></span>

<span data-ttu-id="1aa5c-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="1aa5c-107">`text`: *String*</span></span>

<span data-ttu-id="1aa5c-108">*字符串*类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="1aa5c-109">`pattern`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="1aa5c-109">`pattern`: *String*</span></span>

<span data-ttu-id="1aa5c-110">必须替换的文本。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-110">The text that must be replaced.</span></span>

<span data-ttu-id="1aa5c-111">`replacement`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="1aa5c-111">`replacement`: *String*</span></span>

<span data-ttu-id="1aa5c-112">用作替换的文本。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="1aa5c-113">返回值</span><span class="sxs-lookup"><span data-stu-id="1aa5c-113">Return values</span></span>

<span data-ttu-id="1aa5c-114">*字符串*</span><span class="sxs-lookup"><span data-stu-id="1aa5c-114">*String*</span></span>

<span data-ttu-id="1aa5c-115">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="1aa5c-116">示例</span><span class="sxs-lookup"><span data-stu-id="1aa5c-116">Example</span></span>

<span data-ttu-id="1aa5c-117">`TRANSLATE ("abcdef", "cd", "GH")` 将模式 **"cd"** 替换为字符串 **"GH"**，返回 **"abGHef"**。</span><span class="sxs-lookup"><span data-stu-id="1aa5c-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1aa5c-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="1aa5c-118">Additional resources</span></span>

[<span data-ttu-id="1aa5c-119">文本函数</span><span class="sxs-lookup"><span data-stu-id="1aa5c-119">Text functions</span></span>](er-functions-category-text.md)
