---
title: ISVALIDCHARACTERISO7064 ER 函数
description: 本主题提供有关 ISVALIDCHARACTERISO7064 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680654"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="73a87-103">ISVALIDCHARACTERISO7064 ER 函数</span><span class="sxs-lookup"><span data-stu-id="73a87-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73a87-104">如果指定字符串表示有效的国际银行帐号 (IBAN)，`ISVALIDCHARACTERISO7064` 函数返回 *布尔* 值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="73a87-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="73a87-105">否则，返回 *布尔* 值 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73a87-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a87-106">语法</span><span class="sxs-lookup"><span data-stu-id="73a87-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="73a87-107">参数</span><span class="sxs-lookup"><span data-stu-id="73a87-107">Arguments</span></span>

<span data-ttu-id="73a87-108">`text`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="73a87-108">`text`: *String*</span></span>

<span data-ttu-id="73a87-109">代表 IBAN 的文本值。</span><span class="sxs-lookup"><span data-stu-id="73a87-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="73a87-110">返回值</span><span class="sxs-lookup"><span data-stu-id="73a87-110">Return values</span></span>

<span data-ttu-id="73a87-111">*字符串*</span><span class="sxs-lookup"><span data-stu-id="73a87-111">*String*</span></span>

<span data-ttu-id="73a87-112">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="73a87-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="73a87-113">示例</span><span class="sxs-lookup"><span data-stu-id="73a87-113">Example</span></span>

<span data-ttu-id="73a87-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` 返回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="73a87-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="73a87-115">`ISVALIDCHARACTERISO7064 ("AT61")` 返回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="73a87-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="73a87-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="73a87-116">Additional resources</span></span>

[<span data-ttu-id="73a87-117">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="73a87-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
