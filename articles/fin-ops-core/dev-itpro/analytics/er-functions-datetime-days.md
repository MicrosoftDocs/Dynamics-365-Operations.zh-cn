---
title: DAYS ER 函数
description: 本主题提供有关 DAYS 电子申报 (ER) 函数如何使用的信息。
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66398e624e4b9d69d4dc3ccf3ee8f97758f4f861
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682333"
---
# <a name="days-er-function"></a><span data-ttu-id="2634c-103">DAYS ER 函数</span><span class="sxs-lookup"><span data-stu-id="2634c-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2634c-104">`DAYS` 函数返回一个 *整数* 值，此值表示一个指定日期至第二个指定日期之间的天数。</span><span class="sxs-lookup"><span data-stu-id="2634c-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="2634c-105">语法</span><span class="sxs-lookup"><span data-stu-id="2634c-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="2634c-106">参数</span><span class="sxs-lookup"><span data-stu-id="2634c-106">Arguments</span></span>

<span data-ttu-id="2634c-107">`date 1`：*日期*</span><span class="sxs-lookup"><span data-stu-id="2634c-107">`date 1`: *Date*</span></span>

<span data-ttu-id="2634c-108">表示用于计算天数的开始日期的日期值。</span><span class="sxs-lookup"><span data-stu-id="2634c-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="2634c-109">`date 2`：*日期*</span><span class="sxs-lookup"><span data-stu-id="2634c-109">`date 2`: *Date*</span></span>

<span data-ttu-id="2634c-110">表示用于计算天数的结束日期的日期值。</span><span class="sxs-lookup"><span data-stu-id="2634c-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="2634c-111">返回值</span><span class="sxs-lookup"><span data-stu-id="2634c-111">Return values</span></span>

<span data-ttu-id="2634c-112">*整数*</span><span class="sxs-lookup"><span data-stu-id="2634c-112">*Integer*</span></span>

<span data-ttu-id="2634c-113">生成的数字值。</span><span class="sxs-lookup"><span data-stu-id="2634c-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2634c-114">使用说明</span><span class="sxs-lookup"><span data-stu-id="2634c-114">Usage notes</span></span>

<span data-ttu-id="2634c-115">第一个日期比第二个日期晚时，`DAYS` 函数返回正值，第一个日期等于第二个日期时返回 **0**（零），第一个日期比第二个日期早时返回负值。</span><span class="sxs-lookup"><span data-stu-id="2634c-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="2634c-116">示例</span><span class="sxs-lookup"><span data-stu-id="2634c-116">Example</span></span>

<span data-ttu-id="2634c-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` 将返回 **-1**。</span><span class="sxs-lookup"><span data-stu-id="2634c-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2634c-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="2634c-118">Additional resources</span></span>

[<span data-ttu-id="2634c-119">日期和时间函数</span><span class="sxs-lookup"><span data-stu-id="2634c-119">Date and time functions</span></span>](er-functions-category-datetime.md)
