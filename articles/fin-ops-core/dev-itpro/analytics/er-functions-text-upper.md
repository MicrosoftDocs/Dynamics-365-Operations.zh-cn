---
title: UPPER ER 函数
description: 本主题提供有关 UPPER 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: ed862ab823cfc3539c420d3066c9397e1e6d870e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916675"
---
# <span data-ttu-id="c62f9-103"><a name="UPPER">UPPER ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="c62f9-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c62f9-104">在将指定的文本字符串转换为大写字母后，`UPPER` 函数作为*字符串*值返回该字符串。</span><span class="sxs-lookup"><span data-stu-id="c62f9-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="c62f9-105">语法</span><span class="sxs-lookup"><span data-stu-id="c62f9-105">Syntax</span></span>

```
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="c62f9-106">参数</span><span class="sxs-lookup"><span data-stu-id="c62f9-106">Arguments</span></span>

<span data-ttu-id="c62f9-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="c62f9-107">`text`: *String*</span></span>

<span data-ttu-id="c62f9-108">*字符串*类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="c62f9-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c62f9-109">返回值</span><span class="sxs-lookup"><span data-stu-id="c62f9-109">Return values</span></span>

<span data-ttu-id="c62f9-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="c62f9-110">*String*</span></span>

<span data-ttu-id="c62f9-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="c62f9-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c62f9-112">示例</span><span class="sxs-lookup"><span data-stu-id="c62f9-112">Example</span></span>

<span data-ttu-id="c62f9-113">`UPPER ("Sample")` 返回 **"SAMPLE"**。</span><span class="sxs-lookup"><span data-stu-id="c62f9-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c62f9-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="c62f9-114">Additional resources</span></span>

[<span data-ttu-id="c62f9-115">文本函数</span><span class="sxs-lookup"><span data-stu-id="c62f9-115">Text functions</span></span>](er-functions-category-text.md)
