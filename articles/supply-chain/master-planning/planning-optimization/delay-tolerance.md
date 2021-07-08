---
title: 延迟容差（负天数）
description: 本主题提供有关延迟容差计算以及它如何影响计划优化中的计划订单创建的信息。
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306455"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="142a4-103">延迟容差（负天数）</span><span class="sxs-lookup"><span data-stu-id="142a4-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="142a4-104">延迟容差功能使计划优化能够考虑为覆盖范围组设置的 **负天数** 值。</span><span class="sxs-lookup"><span data-stu-id="142a4-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="142a4-105">它用于延长在主计划期间应用的延迟容差期间。</span><span class="sxs-lookup"><span data-stu-id="142a4-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="142a4-106">这样，如果现有供应能够在短暂延迟后满足需求，您就可以避免创建新的供应订单。</span><span class="sxs-lookup"><span data-stu-id="142a4-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="142a4-107">该功能的目的是确定为给定需求创建新的供应订单是否有意义。</span><span class="sxs-lookup"><span data-stu-id="142a4-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="142a4-108">在系统中开启此功能</span><span class="sxs-lookup"><span data-stu-id="142a4-108">Turn on the feature in your system</span></span>

<span data-ttu-id="142a4-109">若要使延迟容差在您的系统中可用，请转到 [功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，打开 *计划优化的负天数* 功能。</span><span class="sxs-lookup"><span data-stu-id="142a4-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="142a4-110">计划优化中的延迟容差</span><span class="sxs-lookup"><span data-stu-id="142a4-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="142a4-111">延迟容差表示在已计划现有供应时，您在订购新补货之前愿意等待的提前期之外的天数。</span><span class="sxs-lookup"><span data-stu-id="142a4-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="142a4-112">延迟容差通过使用日历天数而不是工作日来定义。</span><span class="sxs-lookup"><span data-stu-id="142a4-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="142a4-113">在主计划期间，当系统计算延迟容差时，它将考虑 **负天数** 设置。</span><span class="sxs-lookup"><span data-stu-id="142a4-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="142a4-114">您可以在 **覆盖范围组** 页面或 **物料覆盖范围** 页面上设置 **负天数** 值。</span><span class="sxs-lookup"><span data-stu-id="142a4-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="142a4-115">系统将延迟容差计算链接到 *最早补货日期*，该日期等于今天的日期加上提前期。</span><span class="sxs-lookup"><span data-stu-id="142a4-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="142a4-116">延迟容差使用以下公式计算，其中 *max()* 找到两个值中较大的一个：</span><span class="sxs-lookup"><span data-stu-id="142a4-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="142a4-117">*max（最早补货日期、需求截止日期）*– *需求截止日期* + *负天数*</span><span class="sxs-lookup"><span data-stu-id="142a4-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="142a4-118">此公式可确保在产品提前期内存在足够供应时，主计划不会创建新的供应订单。</span><span class="sxs-lookup"><span data-stu-id="142a4-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="142a4-119">计划优化中的延迟容差计算始终使用来自内置主计划的动态负天数计算。</span><span class="sxs-lookup"><span data-stu-id="142a4-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="142a4-120">**主计划参数** 页面上的 **使用动态负天数** 设置对此行为没有影响。</span><span class="sxs-lookup"><span data-stu-id="142a4-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="142a4-121">如果现有供应意味着需求延迟小于或等于计算的延迟容差，则计划优化将现有供应与需求相关联。</span><span class="sxs-lookup"><span data-stu-id="142a4-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="142a4-122">在某些情况下，延迟需求比最终供应过剩要好。</span><span class="sxs-lookup"><span data-stu-id="142a4-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="142a4-123">以下子部分提供了一些示例，说明延迟容差如何影响计划优化中计划订单的创建。</span><span class="sxs-lookup"><span data-stu-id="142a4-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="142a4-124">示例 1</span><span class="sxs-lookup"><span data-stu-id="142a4-124">Example 1</span></span>

<span data-ttu-id="142a4-125">产品具有以下配置：</span><span class="sxs-lookup"><span data-stu-id="142a4-125">A product has the following configuration:</span></span>

- <span data-ttu-id="142a4-126">**提前期**：*10*</span><span class="sxs-lookup"><span data-stu-id="142a4-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="142a4-127">**负天数**：*2*</span><span class="sxs-lookup"><span data-stu-id="142a4-127">**Negative days:** *2*</span></span>

<span data-ttu-id="142a4-128">该产品存在以下供应和需求：</span><span class="sxs-lookup"><span data-stu-id="142a4-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="142a4-129">**今日需求：** 数量为 10 的销售订单</span><span class="sxs-lookup"><span data-stu-id="142a4-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="142a4-130">**12 天供应：** 数量为 10 的采购订单</span><span class="sxs-lookup"><span data-stu-id="142a4-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="142a4-131">现有供应可以在 12 天内满足需求，该期间等于延迟容差。</span><span class="sxs-lookup"><span data-stu-id="142a4-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="142a4-132">因此，当主计划运行时，不会创建任何计划订单。</span><span class="sxs-lookup"><span data-stu-id="142a4-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="142a4-133">示例 2</span><span class="sxs-lookup"><span data-stu-id="142a4-133">Example 2</span></span>

<span data-ttu-id="142a4-134">产品具有以下配置：</span><span class="sxs-lookup"><span data-stu-id="142a4-134">A product has the following configuration:</span></span>

- <span data-ttu-id="142a4-135">**提前期**：*10*</span><span class="sxs-lookup"><span data-stu-id="142a4-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="142a4-136">**负天数**：*0*</span><span class="sxs-lookup"><span data-stu-id="142a4-136">**Negative days:** *0*</span></span>

<span data-ttu-id="142a4-137">该产品存在以下供应和需求：</span><span class="sxs-lookup"><span data-stu-id="142a4-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="142a4-138">**今日需求：** 数量为 10 的销售订单</span><span class="sxs-lookup"><span data-stu-id="142a4-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="142a4-139">**12 天供应：** 数量为 10 的采购订单</span><span class="sxs-lookup"><span data-stu-id="142a4-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="142a4-140">现有供应只能在 12 天后满足需求。</span><span class="sxs-lookup"><span data-stu-id="142a4-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="142a4-141">但是，延迟容差是 10 天。</span><span class="sxs-lookup"><span data-stu-id="142a4-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="142a4-142">因此，当主计划运行时，将创建数量为 10 的计划订单。</span><span class="sxs-lookup"><span data-stu-id="142a4-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="142a4-143">示例 3</span><span class="sxs-lookup"><span data-stu-id="142a4-143">Example 3</span></span>

<span data-ttu-id="142a4-144">产品具有以下配置：</span><span class="sxs-lookup"><span data-stu-id="142a4-144">A product has the following configuration:</span></span>

- <span data-ttu-id="142a4-145">**提前期**：*10*</span><span class="sxs-lookup"><span data-stu-id="142a4-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="142a4-146">**负天数**：*2*</span><span class="sxs-lookup"><span data-stu-id="142a4-146">**Negative days:** *2*</span></span>

<span data-ttu-id="142a4-147">该产品存在以下供应和需求：</span><span class="sxs-lookup"><span data-stu-id="142a4-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="142a4-148">**11 天需求：** 数量为 10 的销售订单</span><span class="sxs-lookup"><span data-stu-id="142a4-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="142a4-149">**14 天供应：** 数量为 10 的采购订单</span><span class="sxs-lookup"><span data-stu-id="142a4-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="142a4-150">现有供应只能在三天后满足需求。</span><span class="sxs-lookup"><span data-stu-id="142a4-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="142a4-151">但是，延迟容差是两天。</span><span class="sxs-lookup"><span data-stu-id="142a4-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="142a4-152">（在这种情况下，延迟容差仅包括两个负天数。</span><span class="sxs-lookup"><span data-stu-id="142a4-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="142a4-153">不包括需求日期，因为它晚于产品提前期。）因此，当主计划运行时，将创建数量为 10 的计划订单。</span><span class="sxs-lookup"><span data-stu-id="142a4-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
