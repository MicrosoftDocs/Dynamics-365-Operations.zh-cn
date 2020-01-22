---
title: ADDDAYS ER 函数
description: 本主题提供有关 ADDDAYS 电子申报 (ER) 函数如何使用的信息。
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916445"
---
# <span data-ttu-id="21bd3-103"><a name="ADDDAYS">ADDDAYS ER 函数</a></span><span class="sxs-lookup"><span data-stu-id="21bd3-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21bd3-104">`ADDDAYS` 函数计算*日期时间*值，此值是指定开始日期之前或之后的指定的天数。</span><span class="sxs-lookup"><span data-stu-id="21bd3-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="21bd3-105">语法</span><span class="sxs-lookup"><span data-stu-id="21bd3-105">Syntax</span></span>

```
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="21bd3-106">参数</span><span class="sxs-lookup"><span data-stu-id="21bd3-106">Arguments</span></span>

<span data-ttu-id="21bd3-107">`datetime`：*日期时间*</span><span class="sxs-lookup"><span data-stu-id="21bd3-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="21bd3-108">代表开始日期的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="21bd3-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="21bd3-109">`days`：*整数*</span><span class="sxs-lookup"><span data-stu-id="21bd3-109">`days`: *Integer*</span></span>

<span data-ttu-id="21bd3-110">`datetime` 之前或之后的天数。</span><span class="sxs-lookup"><span data-stu-id="21bd3-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="21bd3-111">返回值</span><span class="sxs-lookup"><span data-stu-id="21bd3-111">Return values</span></span>

<span data-ttu-id="21bd3-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="21bd3-112">*DateTime*</span></span>

<span data-ttu-id="21bd3-113">生成的日期/时间值。</span><span class="sxs-lookup"><span data-stu-id="21bd3-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="21bd3-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="21bd3-114">Usage notes</span></span>

<span data-ttu-id="21bd3-115">`days` 的正值会产生一个将来的日期。</span><span class="sxs-lookup"><span data-stu-id="21bd3-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="21bd3-116">负值会产生一个过去的日期。</span><span class="sxs-lookup"><span data-stu-id="21bd3-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="21bd3-117">示例 1</span><span class="sxs-lookup"><span data-stu-id="21bd3-117">Example 1</span></span>

<span data-ttu-id="21bd3-118">`ADDDAYS (NOW(), 7)` 返回未来七天的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="21bd3-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="21bd3-119">示例 2</span><span class="sxs-lookup"><span data-stu-id="21bd3-119">Example 2</span></span>

<span data-ttu-id="21bd3-120">`ADDDAYS (NOW(), -3)` 返回过去三天的日期和时间。</span><span class="sxs-lookup"><span data-stu-id="21bd3-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21bd3-121">其他资源</span><span class="sxs-lookup"><span data-stu-id="21bd3-121">Additional resources</span></span>

[<span data-ttu-id="21bd3-122">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="21bd3-122">Date and time functions</span></span>](er-functions-category-datetime.md)
