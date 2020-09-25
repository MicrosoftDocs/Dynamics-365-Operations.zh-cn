---
title: CURCREDREF ER 函数
description: 本主题提供有关 CURCREDREF 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 95e90289f43896b83ba98a6edefe0cd6028f4043
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744183"
---
# <a name="curcredref-er-function"></a><span data-ttu-id="b02d7-103">CURCREDREF ER 函数</span><span class="sxs-lookup"><span data-stu-id="b02d7-103">CURCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b02d7-104">`CURCREDREF` 函数基于指定发票编号的数字返回表示贷方引用的*字符串*值。</span><span class="sxs-lookup"><span data-stu-id="b02d7-104">The `CURCREDREF` function returns a *String* value that represents a creditor reference, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="b02d7-105">语法</span><span class="sxs-lookup"><span data-stu-id="b02d7-105">Syntax</span></span>

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="b02d7-106">参数</span><span class="sxs-lookup"><span data-stu-id="b02d7-106">Arguments</span></span>

<span data-ttu-id="b02d7-107">`invoice number digits`：*字符串*</span><span class="sxs-lookup"><span data-stu-id="b02d7-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="b02d7-108">代表发票编号数字的文本值。</span><span class="sxs-lookup"><span data-stu-id="b02d7-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="b02d7-109">返回值</span><span class="sxs-lookup"><span data-stu-id="b02d7-109">Return values</span></span>

<span data-ttu-id="b02d7-110">*字符串*</span><span class="sxs-lookup"><span data-stu-id="b02d7-110">*String*</span></span>

<span data-ttu-id="b02d7-111">生成的文本值。</span><span class="sxs-lookup"><span data-stu-id="b02d7-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b02d7-112">示例</span><span class="sxs-lookup"><span data-stu-id="b02d7-112">Example</span></span>

<span data-ttu-id="b02d7-113">`CURCredRef ("VEND-200002")` 将返回 **"2200002"**。</span><span class="sxs-lookup"><span data-stu-id="b02d7-113">`CURCredRef ("VEND-200002")` returns **"2200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b02d7-114">其他资源</span><span class="sxs-lookup"><span data-stu-id="b02d7-114">Additional resources</span></span>

[<span data-ttu-id="b02d7-115">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="b02d7-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
