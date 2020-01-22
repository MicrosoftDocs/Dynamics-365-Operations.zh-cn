---
title: DAYOFYEAR ER 函数
description: 本主题提供有关 DAYOFYEAR 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 1080a1c2e30cd7ca64ea43120c11eb90d3c99416
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916330"
---
# <span data-ttu-id="a219a-103"><a name="DAYOFYEAR">DAYOFYEAR ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="a219a-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a219a-104">`DAYOFYEAR` 函数返回一个*整数*值，此值表示 1 月 1 日到指定日期之间的天数。</span><span class="sxs-lookup"><span data-stu-id="a219a-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="a219a-105">语法</span><span class="sxs-lookup"><span data-stu-id="a219a-105">Syntax</span></span>

```
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="a219a-106">参数</span><span class="sxs-lookup"><span data-stu-id="a219a-106">Arguments</span></span>

<span data-ttu-id="a219a-107">`date`：*日期*</span><span class="sxs-lookup"><span data-stu-id="a219a-107">`date`: *Date*</span></span>

<span data-ttu-id="a219a-108">表示用于计算天数的日期的日期值。</span><span class="sxs-lookup"><span data-stu-id="a219a-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="a219a-109">返回值</span><span class="sxs-lookup"><span data-stu-id="a219a-109">Return values</span></span>

<span data-ttu-id="a219a-110">*整数*</span><span class="sxs-lookup"><span data-stu-id="a219a-110">*Integer*</span></span>

<span data-ttu-id="a219a-111">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="a219a-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="a219a-112">示例 1</span><span class="sxs-lookup"><span data-stu-id="a219a-112">Example 1</span></span>

<span data-ttu-id="a219a-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` 将返回 **61**。</span><span class="sxs-lookup"><span data-stu-id="a219a-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a219a-114">示例 2</span><span class="sxs-lookup"><span data-stu-id="a219a-114">Example 2</span></span>

<span data-ttu-id="a219a-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` 将返回 **1**。</span><span class="sxs-lookup"><span data-stu-id="a219a-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a219a-116">其他资源</span><span class="sxs-lookup"><span data-stu-id="a219a-116">Additional resources</span></span>

[<span data-ttu-id="a219a-117">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="a219a-117">Date and time functions</span></span>](er-functions-category-datetime.md)
