---
title: TRIM ER 函数
description: 本主题提供有关 TRIM 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 908da840ffcb94f4a60bb41ce041f5f263c921eb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688357"
---
# <a name="trim-er-function"></a><span data-ttu-id="e879b-103">TRIM ER 函数</span><span class="sxs-lookup"><span data-stu-id="e879b-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e879b-104">在删除前导和尾随空格以及删除单词之间的多个空格之后，`TRIM` 函数作为 *字符串* 值返回指定的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="e879b-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="e879b-105">语法</span><span class="sxs-lookup"><span data-stu-id="e879b-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="e879b-106">参数</span><span class="sxs-lookup"><span data-stu-id="e879b-106">Arguments</span></span>

<span data-ttu-id="e879b-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="e879b-107">`text`: *String*</span></span>

<span data-ttu-id="e879b-108">*字符串* 类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="e879b-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e879b-109">返回值</span><span class="sxs-lookup"><span data-stu-id="e879b-109">Return values</span></span>

<span data-ttu-id="e879b-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e879b-110">*String*</span></span>

<span data-ttu-id="e879b-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="e879b-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e879b-112">示例</span><span class="sxs-lookup"><span data-stu-id="e879b-112">Example</span></span>

<span data-ttu-id="e879b-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` 返回 **"Sample text"**。</span><span class="sxs-lookup"><span data-stu-id="e879b-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e879b-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="e879b-114">Additional resources</span></span>

[<span data-ttu-id="e879b-115">文本函数</span><span class="sxs-lookup"><span data-stu-id="e879b-115">Text functions</span></span>](er-functions-category-text.md)
