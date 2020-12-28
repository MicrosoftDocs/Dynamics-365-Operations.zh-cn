---
title: CONCATENATE ER 函数
description: 本主题提供有关 CONCATENATE 电子申报 (ER) 函数如何使用的信息
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 903429994ae5618b597aa0ab0991e9f6783a96ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687930"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="3847e-103">CONCATENATE ER 函数</span><span class="sxs-lookup"><span data-stu-id="3847e-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3847e-104">在将所有指定的文本字符串合并为一个字符串之后，`CONCATENATE` 函数将这些字符串作为 *字符串* 值返回。</span><span class="sxs-lookup"><span data-stu-id="3847e-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3847e-105">语法</span><span class="sxs-lookup"><span data-stu-id="3847e-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="3847e-106">参数</span><span class="sxs-lookup"><span data-stu-id="3847e-106">Arguments</span></span>

<span data-ttu-id="3847e-107">`text 1`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="3847e-107">`text 1`: *String*</span></span>

<span data-ttu-id="3847e-108">对 *字符串* 数据类型的数据源的引用。</span><span class="sxs-lookup"><span data-stu-id="3847e-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="3847e-109">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="3847e-109">This argument is required.</span></span>

<span data-ttu-id="3847e-110">`text N`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="3847e-110">`text N`: *String*</span></span>

<span data-ttu-id="3847e-111">对 *字符串* 数据类型的数据源的引用。</span><span class="sxs-lookup"><span data-stu-id="3847e-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="3847e-112">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="3847e-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="3847e-113">返回值</span><span class="sxs-lookup"><span data-stu-id="3847e-113">Return values</span></span>

<span data-ttu-id="3847e-114">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3847e-114">*String*</span></span>

<span data-ttu-id="3847e-115">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="3847e-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3847e-116">示例</span><span class="sxs-lookup"><span data-stu-id="3847e-116">Example</span></span>

<span data-ttu-id="3847e-117">`CONCATENATE ("abc", "def")` 返回 **"abcdef"**。</span><span class="sxs-lookup"><span data-stu-id="3847e-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3847e-118">使用说明</span><span class="sxs-lookup"><span data-stu-id="3847e-118">Usage notes</span></span>

<span data-ttu-id="3847e-119">表达式 `"abc" & "def"` 也返回 **"abcdef"**。</span><span class="sxs-lookup"><span data-stu-id="3847e-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3847e-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="3847e-120">Additional resources</span></span>

[<span data-ttu-id="3847e-121">文本函数</span><span class="sxs-lookup"><span data-stu-id="3847e-121">Text functions</span></span>](er-functions-category-text.md)
