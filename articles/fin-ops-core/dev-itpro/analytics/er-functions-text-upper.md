---
title: UPPER ER 函数
description: 本主题提供有关 UPPER 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 8fb89ca48c0035e672b2de6820d6ef08d36c02af
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559981"
---
# <a name="upper-er-function"></a><span data-ttu-id="f3a7c-103">UPPER ER 函数</span><span class="sxs-lookup"><span data-stu-id="f3a7c-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3a7c-104">在将指定的文本字符串转换为大写字母后，`UPPER` 函数作为 *字符串* 值返回该字符串。</span><span class="sxs-lookup"><span data-stu-id="f3a7c-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3a7c-105">语法</span><span class="sxs-lookup"><span data-stu-id="f3a7c-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="f3a7c-106">参数</span><span class="sxs-lookup"><span data-stu-id="f3a7c-106">Arguments</span></span>

<span data-ttu-id="f3a7c-107">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="f3a7c-107">`text`: *String*</span></span>

<span data-ttu-id="f3a7c-108">*字符串* 类型的数据源的有效路径。</span><span class="sxs-lookup"><span data-stu-id="f3a7c-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="f3a7c-109">返回值</span><span class="sxs-lookup"><span data-stu-id="f3a7c-109">Return values</span></span>

<span data-ttu-id="f3a7c-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f3a7c-110">*String*</span></span>

<span data-ttu-id="f3a7c-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="f3a7c-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f3a7c-112">示例</span><span class="sxs-lookup"><span data-stu-id="f3a7c-112">Example</span></span>

<span data-ttu-id="f3a7c-113">`UPPER ("Sample")` 返回 **"SAMPLE"**。</span><span class="sxs-lookup"><span data-stu-id="f3a7c-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3a7c-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="f3a7c-114">Additional resources</span></span>

[<span data-ttu-id="f3a7c-115">文本函数</span><span class="sxs-lookup"><span data-stu-id="f3a7c-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]