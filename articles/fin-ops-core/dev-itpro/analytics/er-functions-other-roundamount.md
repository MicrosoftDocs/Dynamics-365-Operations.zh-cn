---
title: ROUNDAMOUNT ER 函数
description: 本主题提供有关 ROUNDAMOUNT 电子申报 (ER) 函数如何使用的信息。
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
ms.openlocfilehash: 15a84b086b324ec390d88e8b2617022ad4773977
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683055"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="836cf-103">ROUNDAMOUNT ER 函数</span><span class="sxs-lookup"><span data-stu-id="836cf-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="836cf-104">`ROUNDAMOUNT` 函数根据指定的舍入规则，作为将指定数字舍入为另一个数字的最接近倍数的结果返回 *实数* 值。</span><span class="sxs-lookup"><span data-stu-id="836cf-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="836cf-105">语法</span><span class="sxs-lookup"><span data-stu-id="836cf-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="836cf-106">参数</span><span class="sxs-lookup"><span data-stu-id="836cf-106">Arguments</span></span>

<span data-ttu-id="836cf-107">`number`：*Int* 或 *实数*</span><span class="sxs-lookup"><span data-stu-id="836cf-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="836cf-108">必须舍入的数值。</span><span class="sxs-lookup"><span data-stu-id="836cf-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="836cf-109">`decimals`：*Int* 或 *实数*</span><span class="sxs-lookup"><span data-stu-id="836cf-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="836cf-110">`number` 参数的值必须舍入到其倍数的数字。</span><span class="sxs-lookup"><span data-stu-id="836cf-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="836cf-111">`round rule`：*枚举值*</span><span class="sxs-lookup"><span data-stu-id="836cf-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="836cf-112">定义舍入规则的 **RoundOffType** 枚举的枚举值。</span><span class="sxs-lookup"><span data-stu-id="836cf-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="836cf-113">此枚举提供以下值：</span><span class="sxs-lookup"><span data-stu-id="836cf-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="836cf-114">一般（常规）</span><span class="sxs-lookup"><span data-stu-id="836cf-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="836cf-115">向下 (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="836cf-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="836cf-116">向上舍入 (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="836cf-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="836cf-117">返回值</span><span class="sxs-lookup"><span data-stu-id="836cf-117">Return values</span></span>

<span data-ttu-id="836cf-118">*实数*</span><span class="sxs-lookup"><span data-stu-id="836cf-118">*Real*</span></span>

<span data-ttu-id="836cf-119">产生的数值是 `decimals` 参数指定的值的倍数，并且最接近 `number` 参数指定的值。</span><span class="sxs-lookup"><span data-stu-id="836cf-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="836cf-120">使用说明</span><span class="sxs-lookup"><span data-stu-id="836cf-120">Usage notes</span></span>

<span data-ttu-id="836cf-121">当 `number` 参数为零时，此函数始终返回零。</span><span class="sxs-lookup"><span data-stu-id="836cf-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="836cf-122">当 `decimals` 参数为零时，此函数将舍入为默认舍入值。</span><span class="sxs-lookup"><span data-stu-id="836cf-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="836cf-123">当 `round rule` 参数设置为 **RoundOffType.Ordinary** 时，默认舍入值为 **0.01**。</span><span class="sxs-lookup"><span data-stu-id="836cf-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="836cf-124">否则，默认舍入值为 **1.0**。</span><span class="sxs-lookup"><span data-stu-id="836cf-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="836cf-125">当 `round rule` 参数设置为 **RoundOffType.Ordinary** 时，此函数舍入到最接近的舍入金额。</span><span class="sxs-lookup"><span data-stu-id="836cf-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="836cf-126">当 `round rule` 参数设置为 **RoundOffType.RoundDown** 时，此函数朝零舍入到最接近的舍入金额。</span><span class="sxs-lookup"><span data-stu-id="836cf-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="836cf-127">当 `round rule` 参数设置为 **RoundOffType.RoundUp** 时，此函数离零舍入到最接近的舍入金额。</span><span class="sxs-lookup"><span data-stu-id="836cf-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="836cf-128">当 `round rule` 参数设置为 **RoundOffType.Ordinary** 时，此函数的行为类似于 [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel 函数和 [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ 函数。</span><span class="sxs-lookup"><span data-stu-id="836cf-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="836cf-129">注解</span><span class="sxs-lookup"><span data-stu-id="836cf-129">Remarks</span></span>

<span data-ttu-id="836cf-130">要将数值舍入到指定的小数位数，请使用 [ROUND](er-functions-mathematical-round.md) 函数。</span><span class="sxs-lookup"><span data-stu-id="836cf-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="836cf-131">示例</span><span class="sxs-lookup"><span data-stu-id="836cf-131">Example</span></span>

<span data-ttu-id="836cf-132">如果 **model.RoundOff** 参数设置为 **RoundOffType.Ordinary**，`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 将返回 7.35。</span><span class="sxs-lookup"><span data-stu-id="836cf-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="836cf-133">如果 **model.RoundOff** 参数设置为 **RoundOffType.RoundDown**，`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 将返回 7.35。</span><span class="sxs-lookup"><span data-stu-id="836cf-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="836cf-134">如果 **model.RoundOff** 参数设置为 **RoundOffType.RoundUp**，`ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 将返回 8.4。</span><span class="sxs-lookup"><span data-stu-id="836cf-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="836cf-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="836cf-135">Additional resources</span></span>

[<span data-ttu-id="836cf-136">其他（业务域特定的）函数</span><span class="sxs-lookup"><span data-stu-id="836cf-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="836cf-137">数学函数</span><span class="sxs-lookup"><span data-stu-id="836cf-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)
