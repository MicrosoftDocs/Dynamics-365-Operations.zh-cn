---
title: 预测缩减参数
description: 本主题提供显示如何设置缩减参数的示例。 它包含有关各种缩减参数设置以及每个结果的信息。 可以使用缩减参数以定义如何缩减预测需求。
author: roxanadiaconu
manager: tfehr
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6191b4809c3785d92395bec1b7d51bfc978f9245
ms.sourcegitcommit: 5419f2b8f51cd5de55be66d1389b5b9d7771fd52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/15/2020
ms.locfileid: "3262688"
---
# <a name="forecast-reduction-keys"></a><span data-ttu-id="e05a1-105">预测缩减参数</span><span class="sxs-lookup"><span data-stu-id="e05a1-105">Forecast reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e05a1-106">本主题提供有关用于缩减预测需求的不同方法的信息。</span><span class="sxs-lookup"><span data-stu-id="e05a1-106">This topic provides information about the different methods that are used to reduce forecast requirements.</span></span> <span data-ttu-id="e05a1-107">其中包括每种方法的结果的示例。</span><span class="sxs-lookup"><span data-stu-id="e05a1-107">It includes examples of the results of each method.</span></span> <span data-ttu-id="e05a1-108">还介绍如何创建、设置和使用预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="e05a1-108">It also explains how to create, set up, and use a forecast reduction key.</span></span> <span data-ttu-id="e05a1-109">一些方法使用预测缩减参数缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-109">Some methods use a forecast reduction key to reduce forecast requirements.</span></span>

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a><span data-ttu-id="e05a1-110">用于缩减预测需求的方法</span><span class="sxs-lookup"><span data-stu-id="e05a1-110">Methods that are used to reduce forecast requirements</span></span>

<span data-ttu-id="e05a1-111">向主计划添加预测时，可以选择包含实际需求时如何缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-111">When you include a forecast in a master plan, you can select how the forecast requirements are reduced when actual demand is included.</span></span> <span data-ttu-id="e05a1-112">请注意，主计划中不包含过去的预测要求，即当天以前的所有预测要求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-112">Note that master planning excludes forecast requirements from the past, which means all forecast requirements before today's date.</span></span>

<span data-ttu-id="e05a1-113">若要在主计划中添加预测并选择用于缩减预测需求的方法，请转到**主计划 \> 设置 \> 计划 \> 主计划**。</span><span class="sxs-lookup"><span data-stu-id="e05a1-113">To include a forecast in a master plan and select the method that is used to reduce forecast requirements, go to **Master planning \> Setup \> Plans \> Master plans**.</span></span> <span data-ttu-id="e05a1-114">在**预测模型**字段中，选择一个预测模型。</span><span class="sxs-lookup"><span data-stu-id="e05a1-114">In the **Forecast model** field, select a forecast model.</span></span> <span data-ttu-id="e05a1-115">在**用于减少预测需求的方法**字段中，选择一个方法。</span><span class="sxs-lookup"><span data-stu-id="e05a1-115">In the **Method used to reduce forecast requirements** field, select a method.</span></span> <span data-ttu-id="e05a1-116">选项如下：</span><span class="sxs-lookup"><span data-stu-id="e05a1-116">The following options are available:</span></span>

- <span data-ttu-id="e05a1-117">无</span><span class="sxs-lookup"><span data-stu-id="e05a1-117">None</span></span>
- <span data-ttu-id="e05a1-118">百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="e05a1-118">Percent – reduction key</span></span>
- <span data-ttu-id="e05a1-119">交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="e05a1-119">Transactions – reduction key</span></span>
- <span data-ttu-id="e05a1-120">交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="e05a1-120">Transactions – dynamic period</span></span>

<span data-ttu-id="e05a1-121">以下部分提供有关每个选项的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e05a1-121">The following sections provide more information about each option.</span></span>

### <a name="none"></a><span data-ttu-id="e05a1-122">无</span><span class="sxs-lookup"><span data-stu-id="e05a1-122">None</span></span>

<span data-ttu-id="e05a1-123">如果您选择**无**，则在主计划编制期间不缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-123">If you select **None**, the forecast requirements aren't reduced during master scheduling.</span></span> <span data-ttu-id="e05a1-124">在此案例中，主计划将创建计划订单以供给预测的需求（预测需求）。</span><span class="sxs-lookup"><span data-stu-id="e05a1-124">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="e05a1-125">这些计划订单中维持建议的数量，不考虑其他类型的需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-125">These planned orders maintain the suggested quantity, regardless of other types of demand.</span></span> <span data-ttu-id="e05a1-126">例如，如果下达销售订单，主计划将创建更多计划订单以供给销售订单。</span><span class="sxs-lookup"><span data-stu-id="e05a1-126">For example, if sales orders are placed, master planning creates additional planned orders to supply the sales orders.</span></span> <span data-ttu-id="e05a1-127">将不缩减预测需求的数量。</span><span class="sxs-lookup"><span data-stu-id="e05a1-127">The quantity of the forecast requirements isn't reduced.</span></span>

### <a name="percent--reduction-key"></a><span data-ttu-id="e05a1-128">百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="e05a1-128">Percent – reduction key</span></span>

<span data-ttu-id="e05a1-129">如果选择**百分比 - 缩减参数**，则根据百分比和缩减参数定义的百分比和期间来缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-129">If you select **Percent - reduction key**, the forecast requirements are reduced according to the percentages and periods that are defined by the reduction key.</span></span> <span data-ttu-id="e05a1-130">在此案例中，主计划创建计划订单，在此类订单中，数量的计算方法是预测数量 × 各期间的缩减参数。</span><span class="sxs-lookup"><span data-stu-id="e05a1-130">In this case, master planning creates planned orders where the quantity is calculated as forecasted quantity × reduction key in each period.</span></span> <span data-ttu-id="e05a1-131">如果有其他类型的需求，主计划还将创建计划订单以满足该需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-131">If there are other types of demand, master planning also creates planned orders to supply that demand.</span></span>

#### <a name="example-percent--reduction-key"></a><span data-ttu-id="e05a1-132">示例：百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="e05a1-132">Example: Percent – reduction key</span></span>

<span data-ttu-id="e05a1-133">此示例显示由缩减参数如何根据由缩减参数定义的百分比和期间缩减需求预测要求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-133">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

<span data-ttu-id="e05a1-134">对于本示例，将在主计划中包含以下需求预测。</span><span class="sxs-lookup"><span data-stu-id="e05a1-134">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="e05a1-135">月</span><span class="sxs-lookup"><span data-stu-id="e05a1-135">Month</span></span>    | <span data-ttu-id="e05a1-136">需求预测</span><span class="sxs-lookup"><span data-stu-id="e05a1-136">Demand forecast</span></span> |
|----------|-----------------|
| <span data-ttu-id="e05a1-137">一月</span><span class="sxs-lookup"><span data-stu-id="e05a1-137">January</span></span>  | <span data-ttu-id="e05a1-138">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-138">1,000</span></span>           |
| <span data-ttu-id="e05a1-139">二月</span><span class="sxs-lookup"><span data-stu-id="e05a1-139">February</span></span> | <span data-ttu-id="e05a1-140">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-140">1,000</span></span>           |
| <span data-ttu-id="e05a1-141">三月</span><span class="sxs-lookup"><span data-stu-id="e05a1-141">March</span></span>    | <span data-ttu-id="e05a1-142">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-142">1,000</span></span>           |
| <span data-ttu-id="e05a1-143">四月</span><span class="sxs-lookup"><span data-stu-id="e05a1-143">April</span></span>    | <span data-ttu-id="e05a1-144">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-144">1,000</span></span>           |

<span data-ttu-id="e05a1-145">在**缩减参数**页上，设置以下行。</span><span class="sxs-lookup"><span data-stu-id="e05a1-145">On the **Reduction keys** page, you set up the following lines.</span></span>

| <span data-ttu-id="e05a1-146">找零</span><span class="sxs-lookup"><span data-stu-id="e05a1-146">Change</span></span> | <span data-ttu-id="e05a1-147">单位</span><span class="sxs-lookup"><span data-stu-id="e05a1-147">Unit</span></span>  | <span data-ttu-id="e05a1-148">百分比</span><span class="sxs-lookup"><span data-stu-id="e05a1-148">Percent</span></span> |
|--------|-------|---------|
| <span data-ttu-id="e05a1-149">1</span><span class="sxs-lookup"><span data-stu-id="e05a1-149">1</span></span>      | <span data-ttu-id="e05a1-150">月</span><span class="sxs-lookup"><span data-stu-id="e05a1-150">Month</span></span> | <span data-ttu-id="e05a1-151">100</span><span class="sxs-lookup"><span data-stu-id="e05a1-151">100</span></span>     |
| <span data-ttu-id="e05a1-152">2</span><span class="sxs-lookup"><span data-stu-id="e05a1-152">2</span></span>      | <span data-ttu-id="e05a1-153">月</span><span class="sxs-lookup"><span data-stu-id="e05a1-153">Month</span></span> | <span data-ttu-id="e05a1-154">75</span><span class="sxs-lookup"><span data-stu-id="e05a1-154">75</span></span>      |
| <span data-ttu-id="e05a1-155">3</span><span class="sxs-lookup"><span data-stu-id="e05a1-155">3</span></span>      | <span data-ttu-id="e05a1-156">月</span><span class="sxs-lookup"><span data-stu-id="e05a1-156">Month</span></span> | <span data-ttu-id="e05a1-157">50</span><span class="sxs-lookup"><span data-stu-id="e05a1-157">50</span></span>      |
| <span data-ttu-id="e05a1-158">4</span><span class="sxs-lookup"><span data-stu-id="e05a1-158">4</span></span>      | <span data-ttu-id="e05a1-159">月</span><span class="sxs-lookup"><span data-stu-id="e05a1-159">Month</span></span> | <span data-ttu-id="e05a1-160">25</span><span class="sxs-lookup"><span data-stu-id="e05a1-160">25</span></span>      |

<span data-ttu-id="e05a1-161">将缩减参数分配给物料的覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="e05a1-161">You assign the reduction key to the item's coverage group.</span></span> <span data-ttu-id="e05a1-162">然后在**主计划**页的**用于缩减预测需求的方法**字段中，选择**百分比 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="e05a1-162">Then, on the **Master plans** page, in the **Method used to reduce forecast requirements** field, you select **Percent - reduction key**.</span></span>

<span data-ttu-id="e05a1-163">在此案例中，如果在 1 月 1 日运行预测计划编制，则将根据您在**缩减参数**页上设置的百分比来消耗销售预测需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-163">In this case, if you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="e05a1-164">以下需求数量将转移到主计划。</span><span class="sxs-lookup"><span data-stu-id="e05a1-164">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="e05a1-165">月</span><span class="sxs-lookup"><span data-stu-id="e05a1-165">Month</span></span>                | <span data-ttu-id="e05a1-166">计划订单数量</span><span class="sxs-lookup"><span data-stu-id="e05a1-166">Planned order quantity</span></span> | <span data-ttu-id="e05a1-167">计算</span><span class="sxs-lookup"><span data-stu-id="e05a1-167">Calculation</span></span>    |
|----------------------|------------------------|----------------|
| <span data-ttu-id="e05a1-168">一月</span><span class="sxs-lookup"><span data-stu-id="e05a1-168">January</span></span>              | <span data-ttu-id="e05a1-169">0</span><span class="sxs-lookup"><span data-stu-id="e05a1-169">0</span></span>                      | <span data-ttu-id="e05a1-170">= 0% × 1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-170">= 0% × 1,000</span></span>   |
| <span data-ttu-id="e05a1-171">二月</span><span class="sxs-lookup"><span data-stu-id="e05a1-171">February</span></span>             | <span data-ttu-id="e05a1-172">250</span><span class="sxs-lookup"><span data-stu-id="e05a1-172">250</span></span>                    | <span data-ttu-id="e05a1-173">= 25% × 1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-173">= 25% × 1,000</span></span>  |
| <span data-ttu-id="e05a1-174">三月</span><span class="sxs-lookup"><span data-stu-id="e05a1-174">March</span></span>                | <span data-ttu-id="e05a1-175">500</span><span class="sxs-lookup"><span data-stu-id="e05a1-175">500</span></span>                    | <span data-ttu-id="e05a1-176">= 50% × 1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-176">= 50% × 1,000</span></span>  |
| <span data-ttu-id="e05a1-177">四月</span><span class="sxs-lookup"><span data-stu-id="e05a1-177">April</span></span>                | <span data-ttu-id="e05a1-178">750</span><span class="sxs-lookup"><span data-stu-id="e05a1-178">750</span></span>                    | <span data-ttu-id="e05a1-179">= 75% × 1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-179">= 75% × 1,000</span></span>  |
| <span data-ttu-id="e05a1-180">五月到十二月</span><span class="sxs-lookup"><span data-stu-id="e05a1-180">May through December</span></span> | <span data-ttu-id="e05a1-181">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-181">1,000</span></span>                  | <span data-ttu-id="e05a1-182">= 100% × 1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-182">= 100% × 1,000</span></span> |

### <a name="transactions--reduction-key"></a><span data-ttu-id="e05a1-183">交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="e05a1-183">Transactions – reduction key</span></span>

<span data-ttu-id="e05a1-184">如果选择**交易记录 - 缩减参数**，则通过在缩减参数定义的期间内发生的交易记录来缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-184">If you select **Transactions - reduction key**, the forecast requirements are reduced by the transactions that occur during the periods that are defined by the reduction key.</span></span>

#### <a name="example-transactions--reduction-key"></a><span data-ttu-id="e05a1-185">示例：交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="e05a1-185">Example: Transactions – reduction key</span></span>

<span data-ttu-id="e05a1-186">此示例显示如何实际订单，这将在由缩减参数和缩减需求预测要求定义的期间发生。</span><span class="sxs-lookup"><span data-stu-id="e05a1-186">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

<span data-ttu-id="e05a1-187">对于本示例，在**主计划**页的**用于缩减预测需求的方法**字段中，选择**交易记录 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="e05a1-187">For this example, you select **Transactions - reduction key** in the **Method used to reduce forecast requirements** field on the **Master plans** page.</span></span>

<span data-ttu-id="e05a1-188">1 月 1 日存在以下销售订单。</span><span class="sxs-lookup"><span data-stu-id="e05a1-188">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="e05a1-189">月</span><span class="sxs-lookup"><span data-stu-id="e05a1-189">Month</span></span>    | <span data-ttu-id="e05a1-190">订购的份数</span><span class="sxs-lookup"><span data-stu-id="e05a1-190">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="e05a1-191">一月</span><span class="sxs-lookup"><span data-stu-id="e05a1-191">January</span></span>  | <span data-ttu-id="e05a1-192">956</span><span class="sxs-lookup"><span data-stu-id="e05a1-192">956</span></span>                      |
| <span data-ttu-id="e05a1-193">二月</span><span class="sxs-lookup"><span data-stu-id="e05a1-193">February</span></span> | <span data-ttu-id="e05a1-194">1,176</span><span class="sxs-lookup"><span data-stu-id="e05a1-194">1,176</span></span>                    |
| <span data-ttu-id="e05a1-195">三月</span><span class="sxs-lookup"><span data-stu-id="e05a1-195">March</span></span>    | <span data-ttu-id="e05a1-196">451</span><span class="sxs-lookup"><span data-stu-id="e05a1-196">451</span></span>                      |
| <span data-ttu-id="e05a1-197">四月</span><span class="sxs-lookup"><span data-stu-id="e05a1-197">April</span></span>    | <span data-ttu-id="e05a1-198">119</span><span class="sxs-lookup"><span data-stu-id="e05a1-198">119</span></span>                      |

<span data-ttu-id="e05a1-199">如果您使用上一个示例中使用的同一个每月 1,000 份需求预测，将向主计划转移以下需求数量。</span><span class="sxs-lookup"><span data-stu-id="e05a1-199">If you use the same demand forecast of 1,000 pieces per month that was used in the previous example, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="e05a1-200">月</span><span class="sxs-lookup"><span data-stu-id="e05a1-200">Month</span></span>                | <span data-ttu-id="e05a1-201">所需的份数</span><span class="sxs-lookup"><span data-stu-id="e05a1-201">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="e05a1-202">一月</span><span class="sxs-lookup"><span data-stu-id="e05a1-202">January</span></span>              | <span data-ttu-id="e05a1-203">44</span><span class="sxs-lookup"><span data-stu-id="e05a1-203">44</span></span>                        |
| <span data-ttu-id="e05a1-204">二月</span><span class="sxs-lookup"><span data-stu-id="e05a1-204">February</span></span>             | <span data-ttu-id="e05a1-205">0</span><span class="sxs-lookup"><span data-stu-id="e05a1-205">0</span></span>                         |
| <span data-ttu-id="e05a1-206">三月</span><span class="sxs-lookup"><span data-stu-id="e05a1-206">March</span></span>                | <span data-ttu-id="e05a1-207">549</span><span class="sxs-lookup"><span data-stu-id="e05a1-207">549</span></span>                       |
| <span data-ttu-id="e05a1-208">四月</span><span class="sxs-lookup"><span data-stu-id="e05a1-208">April</span></span>                | <span data-ttu-id="e05a1-209">881</span><span class="sxs-lookup"><span data-stu-id="e05a1-209">881</span></span>                       |
| <span data-ttu-id="e05a1-210">五月到十二月</span><span class="sxs-lookup"><span data-stu-id="e05a1-210">May through December</span></span> | <span data-ttu-id="e05a1-211">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-211">1,000</span></span>                     |

### <a name="transactions--dynamic-period"></a><span data-ttu-id="e05a1-212">交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="e05a1-212">Transactions – dynamic period</span></span>

<span data-ttu-id="e05a1-213">如果选择**交易记录 - 动态期间**，将按动态期间进行的实际订单交易记录缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-213">If you select **Transactions - dynamic period**, the forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="e05a1-214">动态期间涵盖当前预测日期，并在下一预测开始时结束。</span><span class="sxs-lookup"><span data-stu-id="e05a1-214">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span> <span data-ttu-id="e05a1-215">在此案例中，主计划将创建计划订单以供给预测的需求（预测需求）。</span><span class="sxs-lookup"><span data-stu-id="e05a1-215">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="e05a1-216">但是，下达实际订单交易记录时，将缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-216">However, when actual order transactions are placed, the forecast requirements are reduced.</span></span> <span data-ttu-id="e05a1-217">实际交易记录占用部分预测需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-217">The actual transactions consume part of the forecasted requirements.</span></span>

<span data-ttu-id="e05a1-218">在使用此选项时，会发生以下行为：</span><span class="sxs-lookup"><span data-stu-id="e05a1-218">When this option is used, the following behavior occurs:</span></span>

- <span data-ttu-id="e05a1-219">将不需要或不使用缩减参数。</span><span class="sxs-lookup"><span data-stu-id="e05a1-219">Reduction keys aren't required or used.</span></span> 
- <span data-ttu-id="e05a1-220">如果完全缩减预测，则当前预测的预测需求变为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="e05a1-220">If the forecast is completely reduced, the forecast requirements for the current forecast become 0 (zero).</span></span>
- <span data-ttu-id="e05a1-221">如果没有将来的预测，则最后一个输入的预测的预测需求会缩减。</span><span class="sxs-lookup"><span data-stu-id="e05a1-221">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
- <span data-ttu-id="e05a1-222">时限包括在缩减预测计算中。</span><span class="sxs-lookup"><span data-stu-id="e05a1-222">Time fences are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="e05a1-223">正天数包括在缩减预测计算中。</span><span class="sxs-lookup"><span data-stu-id="e05a1-223">Positive days are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="e05a1-224">如果实际订单交易记录超过预测的需求，则其余的交易记录不会前进到下一预测期间。</span><span class="sxs-lookup"><span data-stu-id="e05a1-224">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>

#### <a name="example-1-transactions--dynamic-period"></a><span data-ttu-id="e05a1-225">示例 1：交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="e05a1-225">Example 1: Transactions – dynamic period</span></span>

<span data-ttu-id="e05a1-226">下面是一个简单示例，该示例显示**交易记录 - 动态期间**方法的工作原理。</span><span class="sxs-lookup"><span data-stu-id="e05a1-226">Here a simple example that shows how the **Transactions - dynamic period** method works.</span></span>

<span data-ttu-id="e05a1-227">对于本示例，将在主计划中包含以下需求预测。</span><span class="sxs-lookup"><span data-stu-id="e05a1-227">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="e05a1-228">日期</span><span class="sxs-lookup"><span data-stu-id="e05a1-228">Date</span></span>       | <span data-ttu-id="e05a1-229">需求预测</span><span class="sxs-lookup"><span data-stu-id="e05a1-229">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="e05a1-230">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-230">January 1</span></span>  | <span data-ttu-id="e05a1-231">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-231">1,000</span></span>           |
| <span data-ttu-id="e05a1-232">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-232">February 1</span></span> | <span data-ttu-id="e05a1-233">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-233">1,000</span></span>             |

<span data-ttu-id="e05a1-234">还将创建以下销售订单。</span><span class="sxs-lookup"><span data-stu-id="e05a1-234">You also create the following sales orders.</span></span>

| <span data-ttu-id="e05a1-235">日期</span><span class="sxs-lookup"><span data-stu-id="e05a1-235">Date</span></span>        | <span data-ttu-id="e05a1-236">销售订单数量</span><span class="sxs-lookup"><span data-stu-id="e05a1-236">Sales order quantity</span></span> |
|-------------|----------------------|
| <span data-ttu-id="e05a1-237">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-237">January 15</span></span>  | <span data-ttu-id="e05a1-238">200</span><span class="sxs-lookup"><span data-stu-id="e05a1-238">200</span></span>                  |
| <span data-ttu-id="e05a1-239">2 月 15 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-239">February 15</span></span> | <span data-ttu-id="e05a1-240">400</span><span class="sxs-lookup"><span data-stu-id="e05a1-240">400</span></span>                  |

<span data-ttu-id="e05a1-241">在此案例中，将创建以下计划订单。</span><span class="sxs-lookup"><span data-stu-id="e05a1-241">In this case, the following planned orders are created.</span></span>

| <span data-ttu-id="e05a1-242">需求预测日期</span><span class="sxs-lookup"><span data-stu-id="e05a1-242">Demand forecast date</span></span> | <span data-ttu-id="e05a1-243">数量</span><span class="sxs-lookup"><span data-stu-id="e05a1-243">Quantity</span></span> | <span data-ttu-id="e05a1-244">摘要</span><span class="sxs-lookup"><span data-stu-id="e05a1-244">Explanation</span></span>                           |
|--------------------- |----------|---------------------------------------|
| <span data-ttu-id="e05a1-245">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-245">January 1</span></span>            | <span data-ttu-id="e05a1-246">800</span><span class="sxs-lookup"><span data-stu-id="e05a1-246">800</span></span>      | <span data-ttu-id="e05a1-247">预测需求 (= 1,000 – 200)</span><span class="sxs-lookup"><span data-stu-id="e05a1-247">Forecast requirements (= 1,000 – 200)</span></span> |
| <span data-ttu-id="e05a1-248">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-248">January 15</span></span>           | <span data-ttu-id="e05a1-249">200</span><span class="sxs-lookup"><span data-stu-id="e05a1-249">200</span></span>      | <span data-ttu-id="e05a1-250">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="e05a1-250">Sales orders requirements</span></span>             |
| <span data-ttu-id="e05a1-251">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-251">February 1</span></span>           | <span data-ttu-id="e05a1-252">600</span><span class="sxs-lookup"><span data-stu-id="e05a1-252">600</span></span>      | <span data-ttu-id="e05a1-253">预测需求 (= 1,000 – 400)</span><span class="sxs-lookup"><span data-stu-id="e05a1-253">Forecast requirements (= 1,000 – 400)</span></span> |
| <span data-ttu-id="e05a1-254">2 月 15 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-254">February 15</span></span>          | <span data-ttu-id="e05a1-255">400</span><span class="sxs-lookup"><span data-stu-id="e05a1-255">400</span></span>      | <span data-ttu-id="e05a1-256">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="e05a1-256">Sales orders requirements</span></span>             |

#### <a name="example-2-transactions--dynamic-period"></a><span data-ttu-id="e05a1-257">示例 2：交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="e05a1-257">Example 2: Transactions – dynamic period</span></span>

<span data-ttu-id="e05a1-258">在大多数情况下，会设置系统以使交易记录在特定预测期间减少需求预测：周、月，等等。</span><span class="sxs-lookup"><span data-stu-id="e05a1-258">In most cases, systems are set up so that transactions reduce demand forecast in specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="e05a1-259">这些期间是在缩减参数中定义的。</span><span class="sxs-lookup"><span data-stu-id="e05a1-259">These periods are defined in the reduction key.</span></span> <span data-ttu-id="e05a1-260">但是，两个需求预测行之间的时间还可*提示*期间。</span><span class="sxs-lookup"><span data-stu-id="e05a1-260">However, the time between two demand forecast lines can also *imply* a period.</span></span>

<span data-ttu-id="e05a1-261">对于此示例，将为以下日期和数量创建需求预测。</span><span class="sxs-lookup"><span data-stu-id="e05a1-261">For this example, you create a demand forecast for the following dates and quantities.</span></span>

| <span data-ttu-id="e05a1-262">日期</span><span class="sxs-lookup"><span data-stu-id="e05a1-262">Date</span></span>       | <span data-ttu-id="e05a1-263">需求预测</span><span class="sxs-lookup"><span data-stu-id="e05a1-263">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="e05a1-264">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-264">January 1</span></span>  | <span data-ttu-id="e05a1-265">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-265">1,000</span></span>           |
| <span data-ttu-id="e05a1-266">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-266">January 5</span></span>  | <span data-ttu-id="e05a1-267">500</span><span class="sxs-lookup"><span data-stu-id="e05a1-267">500</span></span>             |
| <span data-ttu-id="e05a1-268">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-268">January 12</span></span> | <span data-ttu-id="e05a1-269">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-269">1,000</span></span>           |

<span data-ttu-id="e05a1-270">请注意，在此预测中，预测日期之间没有清晰的间隔。</span><span class="sxs-lookup"><span data-stu-id="e05a1-270">Notice that, in this forecast, there isn't a clear period between the forecast dates.</span></span> <span data-ttu-id="e05a1-271">第一个和第二个日期之间的间隔为四天，第二个和第三个日期之间的间隔为七天。</span><span class="sxs-lookup"><span data-stu-id="e05a1-271">Between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="e05a1-272">这些间隔就是动态期间。</span><span class="sxs-lookup"><span data-stu-id="e05a1-272">These spans are the dynamic periods.</span></span>

<span data-ttu-id="e05a1-273">还将创建以下销售订单行。</span><span class="sxs-lookup"><span data-stu-id="e05a1-273">You also create the following sales order lines.</span></span>

| <span data-ttu-id="e05a1-274">日期</span><span class="sxs-lookup"><span data-stu-id="e05a1-274">Date</span></span>                             | <span data-ttu-id="e05a1-275">销售订单数量</span><span class="sxs-lookup"><span data-stu-id="e05a1-275">Sales order quantity</span></span> |
|----------------------------------|----------------------|
| <span data-ttu-id="e05a1-276">上一年度的 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-276">December 15 in the previous year</span></span> | <span data-ttu-id="e05a1-277">500</span><span class="sxs-lookup"><span data-stu-id="e05a1-277">500</span></span>                  |
| <span data-ttu-id="e05a1-278">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-278">January 3</span></span>                        | <span data-ttu-id="e05a1-279">100</span><span class="sxs-lookup"><span data-stu-id="e05a1-279">100</span></span>                  |
| <span data-ttu-id="e05a1-280">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-280">January 10</span></span>                       | <span data-ttu-id="e05a1-281">200</span><span class="sxs-lookup"><span data-stu-id="e05a1-281">200</span></span>                  |

<span data-ttu-id="e05a1-282">在此案例中，将以下面的方式缩减预测：</span><span class="sxs-lookup"><span data-stu-id="e05a1-282">In this case, the forecast is reduced in the following manner:</span></span>

- <span data-ttu-id="e05a1-283">因为第一个销售订单不在任何期间，因此不会缩减任何预测。</span><span class="sxs-lookup"><span data-stu-id="e05a1-283">Because the first sales order isn't in any period, it doesn't reduce any forecast.</span></span>
- <span data-ttu-id="e05a1-284">因为第二个销售订单是从 1 月 1 日到 1 月 5 日，因此它会将 1 月 1 日的预测缩减 100。</span><span class="sxs-lookup"><span data-stu-id="e05a1-284">Because the second sales order is between January 1 and January 5, it reduces the forecast for January 1 by 100.</span></span>
- <span data-ttu-id="e05a1-285">因为第三个销售订单是从 5 月 5 日到 5 月 12 日，因此它会将 5 月 5 日的预测缩减 200。</span><span class="sxs-lookup"><span data-stu-id="e05a1-285">Because the third sales order is between January 5 and January 12, it reduces the forecast for January 5 by 200.</span></span>

<span data-ttu-id="e05a1-286">因此，将创建以下计划订单。</span><span class="sxs-lookup"><span data-stu-id="e05a1-286">Therefore, the following planned orders are created.</span></span>

| <span data-ttu-id="e05a1-287">需求预测日期</span><span class="sxs-lookup"><span data-stu-id="e05a1-287">Demand forecast date</span></span>             | <span data-ttu-id="e05a1-288">数量</span><span class="sxs-lookup"><span data-stu-id="e05a1-288">Quantity</span></span> | <span data-ttu-id="e05a1-289">摘要</span><span class="sxs-lookup"><span data-stu-id="e05a1-289">Explanation</span></span>                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| <span data-ttu-id="e05a1-290">上一年度的 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-290">December 15 in the previous year</span></span> | <span data-ttu-id="e05a1-291">500</span><span class="sxs-lookup"><span data-stu-id="e05a1-291">500</span></span>      | <span data-ttu-id="e05a1-292">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="e05a1-292">Sales order requirements</span></span>                                            |
| <span data-ttu-id="e05a1-293">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-293">January 1</span></span>                        | <span data-ttu-id="e05a1-294">900</span><span class="sxs-lookup"><span data-stu-id="e05a1-294">900</span></span>      | <span data-ttu-id="e05a1-295">预测需求期间 1 月 1 日到 1 月 5 日 (= 1,000 – 100)</span><span class="sxs-lookup"><span data-stu-id="e05a1-295">Forecast requirements period January 1 to January 5 (= 1,000 – 100)</span></span> |
| <span data-ttu-id="e05a1-296">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-296">January 3</span></span>                        | <span data-ttu-id="e05a1-297">100</span><span class="sxs-lookup"><span data-stu-id="e05a1-297">100</span></span>      | <span data-ttu-id="e05a1-298">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="e05a1-298">Sales order requirements</span></span>                                            |
| <span data-ttu-id="e05a1-299">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-299">January 5</span></span>                        | <span data-ttu-id="e05a1-300">300</span><span class="sxs-lookup"><span data-stu-id="e05a1-300">300</span></span>      | <span data-ttu-id="e05a1-301">预测需求期间 1 月 5 日到 1 月 10 日 (= 500 – 200)</span><span class="sxs-lookup"><span data-stu-id="e05a1-301">Forecast requirements period January 5 to January 10 (= 500 – 200)</span></span>  |
| <span data-ttu-id="e05a1-302">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="e05a1-302">January 12</span></span>                       | <span data-ttu-id="e05a1-303">1,000</span><span class="sxs-lookup"><span data-stu-id="e05a1-303">1,000</span></span>    | <span data-ttu-id="e05a1-304">预测需求期间 1 月 12 日到月底</span><span class="sxs-lookup"><span data-stu-id="e05a1-304">Forecast requirements period January 12 to end</span></span>                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a><span data-ttu-id="e05a1-305">创建和设置预测缩减参数</span><span class="sxs-lookup"><span data-stu-id="e05a1-305">Create and set up a forecast reduction key</span></span>

<span data-ttu-id="e05a1-306">用于缩减预测需求的**交易记录 - 缩减参数**和**百分比- 缩减参数**方法中使用预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="e05a1-306">A forecast reduction key is used in the **Transactions - reduction key** and **Percent- reduction key** methods for reducing forecast requirements.</span></span> <span data-ttu-id="e05a1-307">若要创建和设置缩减参数，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e05a1-307">Follow these steps to create and set up a reduction key.</span></span>

1. <span data-ttu-id="e05a1-308">转到**主计划 \> 设置 \> 覆盖范围 \> 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="e05a1-308">Go to **Master planning \> Setup \> Coverage \> Reduction keys**.</span></span>
2. <span data-ttu-id="e05a1-309">选择**新建**或按 **Ctrl+N** 创建一个缩减参数。</span><span class="sxs-lookup"><span data-stu-id="e05a1-309">Select **New** or press **Ctrl+N** to create a reduction key.</span></span>
3. <span data-ttu-id="e05a1-310">在**缩减参数**字段中，输入预测缩减参数的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e05a1-310">In the **Reduction key** field, enter a unique identifier for the forecast reduction key.</span></span> <span data-ttu-id="e05a1-311">然后在**名称**字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="e05a1-311">Then, in the **Name** field, enter a name.</span></span> 
4. <span data-ttu-id="e05a1-312">定义期间和每个期间中的缩减参数百分比：</span><span class="sxs-lookup"><span data-stu-id="e05a1-312">Define the periods and the reduction key percentage in each period:</span></span>

    - <span data-ttu-id="e05a1-313">**生效日期**字段指示开始创建期间的日期。</span><span class="sxs-lookup"><span data-stu-id="e05a1-313">The **Effective date** field indicates the date when creation of the periods starts.</span></span> <span data-ttu-id="e05a1-314">如果**使用生效日期**选项设置为**是**，期间将在生效日期开始。</span><span class="sxs-lookup"><span data-stu-id="e05a1-314">When the **Use the effective date** option is set to **Yes**, the periods start on the effective date.</span></span> <span data-ttu-id="e05a1-315">如果设置为**否**，期间将在运行主计划的日期开始。</span><span class="sxs-lookup"><span data-stu-id="e05a1-315">When it's set to **No**, the periods start on the date when master planning is run.</span></span>
    - <span data-ttu-id="e05a1-316">定义应进行预测缩减的期间。</span><span class="sxs-lookup"><span data-stu-id="e05a1-316">Define the periods that the forecast reduction should occur during.</span></span>
    - <span data-ttu-id="e05a1-317">为具体期间指定应缩减预测需求的百分比。</span><span class="sxs-lookup"><span data-stu-id="e05a1-317">For a specific period, specify the percentages that the forecast requirements should be reduced by.</span></span> <span data-ttu-id="e05a1-318">您可以输入正值以减少需求，或输入负值增加需求。</span><span class="sxs-lookup"><span data-stu-id="e05a1-318">You can enter positive values to decrease requirements or negative values to increase requirements.</span></span>

## <a name="use-a-reduction-key"></a><span data-ttu-id="e05a1-319">使用一个缩减参数</span><span class="sxs-lookup"><span data-stu-id="e05a1-319">Use a reduction key</span></span>

<span data-ttu-id="e05a1-320">必须为物料的覆盖范围组分配预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="e05a1-320">A forecast reduction key must be assigned to the coverage group of the item.</span></span> <span data-ttu-id="e05a1-321">若要为物料的覆盖范围组分配缩减参数，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="e05a1-321">Follow these steps to assign a reduction key to an item's coverage group.</span></span>

1. <span data-ttu-id="e05a1-322">转至**主计划 \> 设置 \> 覆盖范围 \> 覆盖范围组**。</span><span class="sxs-lookup"><span data-stu-id="e05a1-322">Go to **Master planning \> Setup \> Coverage \> Coverage groups**.</span></span>
2. <span data-ttu-id="e05a1-323">在**其他**快速选项卡上的**缩减参数**字段中，选择缩减参数分配给覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="e05a1-323">On the **Other** FastTab, in the **Reduction key** field, select the reduction key to assign to the coverage group.</span></span> <span data-ttu-id="e05a1-324">缩减参数然后运用于属于该覆盖范围组的所有物料。</span><span class="sxs-lookup"><span data-stu-id="e05a1-324">The reduction key then applies to all items that belong to the coverage group.</span></span>
3. <span data-ttu-id="e05a1-325">在主计划编制期间，若要使用缩减参数计算预测缩减，必须在设置预测计划或主计划时定义此设置。</span><span class="sxs-lookup"><span data-stu-id="e05a1-325">To use a reduction key to calculate forecast reduction during master scheduling, you must define this setting in the setup of the forecast plan or the master plan.</span></span> <span data-ttu-id="e05a1-326">转至以下位置之一：</span><span class="sxs-lookup"><span data-stu-id="e05a1-326">Go to one of the following locations:</span></span>

    - <span data-ttu-id="e05a1-327">主计划 \> 设置 \> 计划 \> 预测计划</span><span class="sxs-lookup"><span data-stu-id="e05a1-327">Master planning \> Setup \> Plans \> Forecast plans</span></span>
    - <span data-ttu-id="e05a1-328">主计划 \> 设置 \> 计划 \> 主计划</span><span class="sxs-lookup"><span data-stu-id="e05a1-328">Master planning \> Setup \> Plans \> Master plans</span></span>

4. <span data-ttu-id="e05a1-329">在**预测计划**或**主计划**页面**常规**快速选项卡上的**用于减少预测需求的方法**字段中，选择**百分比 - 缩减参数**或**交易记录 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="e05a1-329">On the **Forecast plans** or **Master plans** page, on the **General** FastTab, in the **Method used to reduce forecast requirements** field, select either **Percent - reduction key** or **Transactions - reduction key**.</span></span>

## <a name="reduce-a-forecast-by-transactions"></a><span data-ttu-id="e05a1-330">按交易记录缩减预测</span><span class="sxs-lookup"><span data-stu-id="e05a1-330">Reduce a forecast by transactions</span></span>

<span data-ttu-id="e05a1-331">如果用于缩减预测需求的方法选择**交易记录 - 缩减参数**或**交易记录 - 动态期间**，则可指定哪些交易记录缩减预测。</span><span class="sxs-lookup"><span data-stu-id="e05a1-331">When you select **Transactions - reduction key** or **Transactions - dynamic period** as the method for reducing forecast requirements, you can specify which transactions reduce the forecast.</span></span> <span data-ttu-id="e05a1-332">如果所有交易记录均应缩减预测，请在**覆盖范围组**页面**其他**快速选项卡上的**预测减少依据**字段中选择**所有交易记录**，如果只有销售订单才应缩减预测，请选择**订单**。</span><span class="sxs-lookup"><span data-stu-id="e05a1-332">On the **Coverage groups** page, on the **Other** FastTab, in the **Reduce forecast by** field, select **All transactions** if all transactions should reduce the forecast or **Orders** if only sales orders should reduce the forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e05a1-333">其他资源</span><span class="sxs-lookup"><span data-stu-id="e05a1-333">Additional resources</span></span>

[<span data-ttu-id="e05a1-334">主计划概览</span><span class="sxs-lookup"><span data-stu-id="e05a1-334">Master plans overview</span></span>](master-plans.md)
