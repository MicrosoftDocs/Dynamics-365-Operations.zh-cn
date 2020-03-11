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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c95663f1aacaf93c1c4bfc8d36d9515f495bf61e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040817"
---
# <span data-ttu-id="333f8-103"><a name="TRIM">TRIM ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="333f8-103"><a name="TRIM">TRIM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="333f8-104">在删除前导和尾随空格以及删除单词之间的多个空格之后，`TRIM` 函数作为*字符串*值返回指定的文本字符串。</span><span class="sxs-lookup"><span data-stu-id="333f8-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="333f8-105">语法</span><span class="sxs-lookup"><span data-stu-id="333f8-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="333f8-106">参数</span><span class="sxs-lookup"><span data-stu-id="333f8-106">Arguments</span></span>

<span data-ttu-id="333f8-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="333f8-107">`text`: *String*</span></span>

<span data-ttu-id="333f8-108">*字符串*类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="333f8-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="333f8-109">返回值</span><span class="sxs-lookup"><span data-stu-id="333f8-109">Return values</span></span>

<span data-ttu-id="333f8-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="333f8-110">*String*</span></span>

<span data-ttu-id="333f8-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="333f8-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="333f8-112">示例</span><span class="sxs-lookup"><span data-stu-id="333f8-112">Example</span></span>

<span data-ttu-id="333f8-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` 返回 **"Sample text"**。</span><span class="sxs-lookup"><span data-stu-id="333f8-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="333f8-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="333f8-114">Additional resources</span></span>

[<span data-ttu-id="333f8-115">文本函数</span><span class="sxs-lookup"><span data-stu-id="333f8-115">Text functions</span></span>](er-functions-category-text.md)
