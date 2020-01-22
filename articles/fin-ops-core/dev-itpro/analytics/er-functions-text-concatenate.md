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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915755"
---
# <span data-ttu-id="8eb45-103"><a name="CONCATENATE">CONCATENATE ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="8eb45-103"><a name="CONCATENATE">CONCATENATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8eb45-104">在将所有指定的文本字符串合并为一个字符串之后，`CONCATENATE` 函数将这些字符串作为*字符串*值返回。</span><span class="sxs-lookup"><span data-stu-id="8eb45-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb45-105">语法</span><span class="sxs-lookup"><span data-stu-id="8eb45-105">Syntax</span></span>

```
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="8eb45-106">参数</span><span class="sxs-lookup"><span data-stu-id="8eb45-106">Arguments</span></span>

<span data-ttu-id="8eb45-107">`text 1`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="8eb45-107">`text 1`: *String*</span></span>

<span data-ttu-id="8eb45-108">对*字符串*数据类型的数据源的引用。</span><span class="sxs-lookup"><span data-stu-id="8eb45-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="8eb45-109">此参数是必需的。</span><span class="sxs-lookup"><span data-stu-id="8eb45-109">This argument is required.</span></span>

<span data-ttu-id="8eb45-110">`text N`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="8eb45-110">`text N`: *String*</span></span>

<span data-ttu-id="8eb45-111">对*字符串*数据类型的数据源的引用。</span><span class="sxs-lookup"><span data-stu-id="8eb45-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="8eb45-112">其他参数是可选的。</span><span class="sxs-lookup"><span data-stu-id="8eb45-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="8eb45-113">返回值</span><span class="sxs-lookup"><span data-stu-id="8eb45-113">Return values</span></span>

<span data-ttu-id="8eb45-114">*字符串*</span><span class="sxs-lookup"><span data-stu-id="8eb45-114">*String*</span></span>

<span data-ttu-id="8eb45-115">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="8eb45-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="8eb45-116">示例</span><span class="sxs-lookup"><span data-stu-id="8eb45-116">Example</span></span>

<span data-ttu-id="8eb45-117">`CONCATENATE ("abc", "def")` 返回 **"abcdef"**。</span><span class="sxs-lookup"><span data-stu-id="8eb45-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8eb45-118">使用说明</span><span class="sxs-lookup"><span data-stu-id="8eb45-118">Usage notes</span></span>

<span data-ttu-id="8eb45-119">表达式 `"abc" & "def"` 也返回 **"abcdef"**。</span><span class="sxs-lookup"><span data-stu-id="8eb45-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8eb45-120">其他资源</span><span class="sxs-lookup"><span data-stu-id="8eb45-120">Additional resources</span></span>

[<span data-ttu-id="8eb45-121">文本函数</span><span class="sxs-lookup"><span data-stu-id="8eb45-121">Text functions</span></span>](er-functions-category-text.md)
