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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce2192c7bc849996e08573d71d8ed43956c8fb89
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070521"
---
# <span data-ttu-id="779f8-103"><a name="MOD_97">MOD_97 ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="779f8-103"><a name="MOD_97">MOD_97 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="779f8-104">`MOD_97` 函数基于指定发票编号的数字返回*字符串*值，该值作为 MOD97 表达式表示贷方引用。</span><span class="sxs-lookup"><span data-stu-id="779f8-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="779f8-105">语法</span><span class="sxs-lookup"><span data-stu-id="779f8-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="779f8-106">参数</span><span class="sxs-lookup"><span data-stu-id="779f8-106">Arguments</span></span>

<span data-ttu-id="779f8-107">`invoice number digits`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="779f8-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="779f8-108">代表发票编号数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="779f8-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="779f8-109">返回值</span><span class="sxs-lookup"><span data-stu-id="779f8-109">Return values</span></span>

<span data-ttu-id="779f8-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="779f8-110">*String*</span></span>

<span data-ttu-id="779f8-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="779f8-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="779f8-112">示例</span><span class="sxs-lookup"><span data-stu-id="779f8-112">Example</span></span>

<span data-ttu-id="779f8-113">`MOD_97 ("VEND-200002")` 将返回 **"20000285"**。</span><span class="sxs-lookup"><span data-stu-id="779f8-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="779f8-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="779f8-114">Additional resources</span></span>

[<span data-ttu-id="779f8-115">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="779f8-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
