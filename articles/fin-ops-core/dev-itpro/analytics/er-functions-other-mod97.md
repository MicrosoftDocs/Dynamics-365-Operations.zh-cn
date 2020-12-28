---
title: MOD_97 ER 函数
description: 本主题提供有关 MOD_97 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: b2e4e40fbd953b31225ccc0f54912b26933ccc48
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680630"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="3a094-103">MOD_97 ER 函数</span><span class="sxs-lookup"><span data-stu-id="3a094-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a094-104">`MOD_97` 函数基于指定发票编号的数字返回 *字符串* 值，该值作为 MOD97 表达式表示贷方引用。</span><span class="sxs-lookup"><span data-stu-id="3a094-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a094-105">语法</span><span class="sxs-lookup"><span data-stu-id="3a094-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="3a094-106">参数</span><span class="sxs-lookup"><span data-stu-id="3a094-106">Arguments</span></span>

<span data-ttu-id="3a094-107">`invoice number digits`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="3a094-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="3a094-108">代表发票编号数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="3a094-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="3a094-109">返回值</span><span class="sxs-lookup"><span data-stu-id="3a094-109">Return values</span></span>

<span data-ttu-id="3a094-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3a094-110">*String*</span></span>

<span data-ttu-id="3a094-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="3a094-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3a094-112">示例</span><span class="sxs-lookup"><span data-stu-id="3a094-112">Example</span></span>

<span data-ttu-id="3a094-113">`MOD_97 ("VEND-200002")` 将返回 **"20000285"**。</span><span class="sxs-lookup"><span data-stu-id="3a094-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a094-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="3a094-114">Additional resources</span></span>

[<span data-ttu-id="3a094-115">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="3a094-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
