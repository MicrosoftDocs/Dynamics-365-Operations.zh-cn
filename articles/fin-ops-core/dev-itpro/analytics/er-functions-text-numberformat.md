---
title: NUMBERFORMAT ER 函数
description: 本主题提供有关 NUMBERFORMAT 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: a05a1e1c4cdb050bff30ea4710da927a537da14c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562701"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="36ea4-103">NUMBERFORMAT ER 函数</span><span class="sxs-lookup"><span data-stu-id="36ea4-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36ea4-104">`NUMBERFORMAT` 函数返回一个 *字符串* 值，此值以指定格式和指定的[区域性](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes)（可选）显示指定数字。</span><span class="sxs-lookup"><span data-stu-id="36ea4-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="36ea4-105">有关支持格式的信息，请参阅[标准](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx)和[自定义](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx)。</span><span class="sxs-lookup"><span data-stu-id="36ea4-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="36ea4-106">语法 1</span><span class="sxs-lookup"><span data-stu-id="36ea4-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="36ea4-107">语法 2</span><span class="sxs-lookup"><span data-stu-id="36ea4-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="36ea4-108">参数</span><span class="sxs-lookup"><span data-stu-id="36ea4-108">Arguments</span></span>

<span data-ttu-id="36ea4-109">`number`：*整数* 或 *实数*</span><span class="sxs-lookup"><span data-stu-id="36ea4-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="36ea4-110">指定必须设定格式的数字的数字值。</span><span class="sxs-lookup"><span data-stu-id="36ea4-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="36ea4-111">`format`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="36ea4-111">`format` : *String*</span></span>

<span data-ttu-id="36ea4-112">代表格式的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="36ea4-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="36ea4-113">`culture`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="36ea4-113">`culture`: *String*</span></span>

<span data-ttu-id="36ea4-114">代表用于设定格式的区域性的 *字符串* 值。</span><span class="sxs-lookup"><span data-stu-id="36ea4-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="36ea4-115">返回值</span><span class="sxs-lookup"><span data-stu-id="36ea4-115">Return values</span></span>

<span data-ttu-id="36ea4-116">*字符串*</span><span class="sxs-lookup"><span data-stu-id="36ea4-116">*String*</span></span>

<span data-ttu-id="36ea4-117">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="36ea4-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="36ea4-118">使用说明</span><span class="sxs-lookup"><span data-stu-id="36ea4-118">Usage notes</span></span>

<span data-ttu-id="36ea4-119">如果未将区域性定义为所调用函数的参数，运行此函数的上下文将确定用于设定数字格式的区域性。</span><span class="sxs-lookup"><span data-stu-id="36ea4-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="36ea4-120">示例 1</span><span class="sxs-lookup"><span data-stu-id="36ea4-120">Example 1</span></span>

<span data-ttu-id="36ea4-121">对于 **EN-US** 区域性，`NUMBERFORMAT (0.45, "p")` 将返回 **"45.00 %"**，`NUMBERFORMAT (10.45, "#")` 将返回 **"10"**。</span><span class="sxs-lookup"><span data-stu-id="36ea4-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="36ea4-122">示例 2</span><span class="sxs-lookup"><span data-stu-id="36ea4-122">Example 2</span></span>

<span data-ttu-id="36ea4-123">`NUMBERFORMAT (10/3, "F2", "de")` 将返回 **3,33**，而 `NUMBERFORMAT (10/3, "F2", "en-us")` 将返回 **3.33**。</span><span class="sxs-lookup"><span data-stu-id="36ea4-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36ea4-124">其他资源</span><span class="sxs-lookup"><span data-stu-id="36ea4-124">Additional resources</span></span>

[<span data-ttu-id="36ea4-125">文本函数</span><span class="sxs-lookup"><span data-stu-id="36ea4-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]