---
title: 预测缩减参数
description: 本主题提供显示如何设置缩减参数的示例。 它包含有关各种缩减参数设置以及每个结果的信息。 可以使用缩减参数以定义如何缩减预测需求。
author: roxanadiaconu
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b915570145a48db7a182b9fce34e1544e3600107
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1504071"
---
# <a name="method-used-to-reduce-forecast-requirements"></a><span data-ttu-id="baa75-105">用于减少预测需求的方法</span><span class="sxs-lookup"><span data-stu-id="baa75-105">Method used to reduce forecast requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="baa75-106">本主题提供有关用于缩减预测需求的不同方法的信息。</span><span class="sxs-lookup"><span data-stu-id="baa75-106">This topic provides information about the different methods that are used to reduce forecast requirements.</span></span> <span data-ttu-id="baa75-107">其中包括每种方法的结果的示例。</span><span class="sxs-lookup"><span data-stu-id="baa75-107">It includes examples of the results of each method.</span></span> <span data-ttu-id="baa75-108">还介绍如何创建、设置和使用预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="baa75-108">It also explains how to create, set up, and use a forecast reduction key.</span></span> <span data-ttu-id="baa75-109">一些方法使用预测缩减参数缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-109">Some methods use a forecast reduction key to reduce forecast requirements.</span></span>

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a><span data-ttu-id="baa75-110">用于缩减预测需求的方法</span><span class="sxs-lookup"><span data-stu-id="baa75-110">Methods that are used to reduce forecast requirements</span></span>

<span data-ttu-id="baa75-111">向主计划添加预测时，可以选择包含实际需求时如何缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-111">When you include a forecast in a master plan, you can select how the forecast requirements are reduced when actual demand is included.</span></span>

<span data-ttu-id="baa75-112">若要在主计划中添加预测并选择用于缩减预测需求的方法，请转到**主计划 \> 设置 \> 计划 \> 主计划**。</span><span class="sxs-lookup"><span data-stu-id="baa75-112">To include a forecast in a master plan and select the method that is used to reduce forecast requirements, go to **Master planning \> Setup \> Plans \> Master plans**.</span></span> <span data-ttu-id="baa75-113">在**预测模型**字段中，选择一个预测模型。</span><span class="sxs-lookup"><span data-stu-id="baa75-113">In the **Forecast model** field, select a forecast model.</span></span> <span data-ttu-id="baa75-114">在**用于减少预测需求的方法**字段中，选择一个方法。</span><span class="sxs-lookup"><span data-stu-id="baa75-114">In the **Method used to reduce forecast requirements** field, select a method.</span></span> <span data-ttu-id="baa75-115">选项如下：</span><span class="sxs-lookup"><span data-stu-id="baa75-115">The following options are available:</span></span>

- <span data-ttu-id="baa75-116">无</span><span class="sxs-lookup"><span data-stu-id="baa75-116">None</span></span>
- <span data-ttu-id="baa75-117">百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="baa75-117">Percent – reduction key</span></span>
- <span data-ttu-id="baa75-118">交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="baa75-118">Transactions – reduction key</span></span>
- <span data-ttu-id="baa75-119">交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="baa75-119">Transactions – dynamic period</span></span>

<span data-ttu-id="baa75-120">以下部分提供有关每个选项的详细信息。</span><span class="sxs-lookup"><span data-stu-id="baa75-120">The following sections provide more information about each option.</span></span>

### <a name="none"></a><span data-ttu-id="baa75-121">无</span><span class="sxs-lookup"><span data-stu-id="baa75-121">None</span></span>

<span data-ttu-id="baa75-122">如果您选择**无**，则在主计划编制期间不缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-122">If you select **None**, the forecast requirements aren't reduced during master scheduling.</span></span> <span data-ttu-id="baa75-123">在此案例中，主计划将创建计划订单以供给预测的需求（预测需求）。</span><span class="sxs-lookup"><span data-stu-id="baa75-123">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="baa75-124">这些计划订单中维持建议的数量，不考虑其他类型的需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-124">These planned orders maintain the suggested quantity, regardless of other types of demand.</span></span> <span data-ttu-id="baa75-125">例如，如果下达销售订单，主计划将创建更多计划订单以供给销售订单。</span><span class="sxs-lookup"><span data-stu-id="baa75-125">For example, if sales orders are placed, master planning creates additional planned orders to supply the sales orders.</span></span> <span data-ttu-id="baa75-126">将不缩减预测需求的数量。</span><span class="sxs-lookup"><span data-stu-id="baa75-126">The quantity of the forecast requirements isn't reduced.</span></span>

### <a name="percent--reduction-key"></a><span data-ttu-id="baa75-127">百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="baa75-127">Percent – reduction key</span></span>

<span data-ttu-id="baa75-128">如果选择**百分比 - 缩减参数**，则根据百分比和缩减参数定义的百分比和期间来缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-128">If you select **Percent - reduction key**, the forecast requirements are reduced according to the percentages and periods that are defined by the reduction key.</span></span> <span data-ttu-id="baa75-129">在此案例中，主计划创建计划订单，在此类订单中，数量的计算方法是预测数量 × 各期间的缩减参数。</span><span class="sxs-lookup"><span data-stu-id="baa75-129">In this case, master planning creates planned orders where the quantity is calculated as forecasted quantity × reduction key in each period.</span></span> <span data-ttu-id="baa75-130">如果有其他类型的需求，主计划还将创建计划订单以满足该需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-130">If there are other types of demand, master planning also creates planned orders to supply that demand.</span></span>

#### <a name="example-percent--reduction-key"></a><span data-ttu-id="baa75-131">示例：百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="baa75-131">Example: Percent – reduction key</span></span>

<span data-ttu-id="baa75-132">此示例显示由缩减参数如何根据由缩减参数定义的百分比和期间缩减需求预测要求。</span><span class="sxs-lookup"><span data-stu-id="baa75-132">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

<span data-ttu-id="baa75-133">对于本示例，将在主计划中包含以下需求预测。</span><span class="sxs-lookup"><span data-stu-id="baa75-133">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="baa75-134">月</span><span class="sxs-lookup"><span data-stu-id="baa75-134">Month</span></span>    | <span data-ttu-id="baa75-135">需求预测</span><span class="sxs-lookup"><span data-stu-id="baa75-135">Demand forecast</span></span> |
|----------|-----------------|
| <span data-ttu-id="baa75-136">一月</span><span class="sxs-lookup"><span data-stu-id="baa75-136">January</span></span>  | <span data-ttu-id="baa75-137">1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-137">1,000</span></span>           |
| <span data-ttu-id="baa75-138">二月</span><span class="sxs-lookup"><span data-stu-id="baa75-138">February</span></span> | <span data-ttu-id="baa75-139">1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-139">1,000</span></span>           |
| <span data-ttu-id="baa75-140">三月</span><span class="sxs-lookup"><span data-stu-id="baa75-140">March</span></span>    | <span data-ttu-id="baa75-141">1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-141">1,000</span></span>           |
| <span data-ttu-id="baa75-142">四月</span><span class="sxs-lookup"><span data-stu-id="baa75-142">April</span></span>    | <span data-ttu-id="baa75-143">1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-143">1,000</span></span>           |

<span data-ttu-id="baa75-144">在**缩减参数**页上，设置以下行。</span><span class="sxs-lookup"><span data-stu-id="baa75-144">On the **Reduction keys** page, you set up the following lines.</span></span>

| <span data-ttu-id="baa75-145">找零</span><span class="sxs-lookup"><span data-stu-id="baa75-145">Change</span></span> | <span data-ttu-id="baa75-146">单位</span><span class="sxs-lookup"><span data-stu-id="baa75-146">Unit</span></span>  | <span data-ttu-id="baa75-147">百分比</span><span class="sxs-lookup"><span data-stu-id="baa75-147">Percent</span></span> |
|--------|-------|---------|
| <span data-ttu-id="baa75-148">1</span><span class="sxs-lookup"><span data-stu-id="baa75-148">1</span></span>      | <span data-ttu-id="baa75-149">月</span><span class="sxs-lookup"><span data-stu-id="baa75-149">Month</span></span> | <span data-ttu-id="baa75-150">100</span><span class="sxs-lookup"><span data-stu-id="baa75-150">100</span></span>     |
| <span data-ttu-id="baa75-151">2</span><span class="sxs-lookup"><span data-stu-id="baa75-151">2</span></span>      | <span data-ttu-id="baa75-152">月</span><span class="sxs-lookup"><span data-stu-id="baa75-152">Month</span></span> | <span data-ttu-id="baa75-153">75</span><span class="sxs-lookup"><span data-stu-id="baa75-153">75</span></span>      |
| <span data-ttu-id="baa75-154">3</span><span class="sxs-lookup"><span data-stu-id="baa75-154">3</span></span>      | <span data-ttu-id="baa75-155">月</span><span class="sxs-lookup"><span data-stu-id="baa75-155">Month</span></span> | <span data-ttu-id="baa75-156">50</span><span class="sxs-lookup"><span data-stu-id="baa75-156">50</span></span>      |
| <span data-ttu-id="baa75-157">4</span><span class="sxs-lookup"><span data-stu-id="baa75-157">4</span></span>      | <span data-ttu-id="baa75-158">月</span><span class="sxs-lookup"><span data-stu-id="baa75-158">Month</span></span> | <span data-ttu-id="baa75-159">25</span><span class="sxs-lookup"><span data-stu-id="baa75-159">25</span></span>      |

<span data-ttu-id="baa75-160">将缩减参数分配给物料的覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="baa75-160">You assign the reduction key to the item's coverage group.</span></span> <span data-ttu-id="baa75-161">然后在**主计划**页的**用于缩减预测需求的方法**字段中，选择**百分比 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="baa75-161">Then, on the **Master plans** page, in the **Method used to reduce forecast requirements** field, you select **Percent - reduction key**.</span></span>

<span data-ttu-id="baa75-162">在此案例中，如果在 1 月 1 日运行预测计划编制，则将根据您在**缩减参数**页上设置的百分比来消耗销售预测需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-162">In this case, if you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="baa75-163">以下需求数量将转移到主计划。</span><span class="sxs-lookup"><span data-stu-id="baa75-163">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="baa75-164">月</span><span class="sxs-lookup"><span data-stu-id="baa75-164">Month</span></span>                | <span data-ttu-id="baa75-165">计划订单数量</span><span class="sxs-lookup"><span data-stu-id="baa75-165">Planned order quantity</span></span> | <span data-ttu-id="baa75-166">计算</span><span class="sxs-lookup"><span data-stu-id="baa75-166">Calculation</span></span>    |
|----------------------|------------------------|----------------|
| <span data-ttu-id="baa75-167">一月</span><span class="sxs-lookup"><span data-stu-id="baa75-167">January</span></span>              | <span data-ttu-id="baa75-168">0</span><span class="sxs-lookup"><span data-stu-id="baa75-168">0</span></span>                      | <span data-ttu-id="baa75-169">= 0% × 1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-169">= 0% × 1,000</span></span>   |
| <span data-ttu-id="baa75-170">二月</span><span class="sxs-lookup"><span data-stu-id="baa75-170">February</span></span>             | <span data-ttu-id="baa75-171">250</span><span class="sxs-lookup"><span data-stu-id="baa75-171">250</span></span>                    | <span data-ttu-id="baa75-172">= 25% × 1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-172">= 25% × 1,000</span></span>  |
| <span data-ttu-id="baa75-173">三月</span><span class="sxs-lookup"><span data-stu-id="baa75-173">March</span></span>                | <span data-ttu-id="baa75-174">500</span><span class="sxs-lookup"><span data-stu-id="baa75-174">500</span></span>                    | <span data-ttu-id="baa75-175">= 50% × 1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-175">= 50% × 1,000</span></span>  |
| <span data-ttu-id="baa75-176">四月</span><span class="sxs-lookup"><span data-stu-id="baa75-176">April</span></span>                | <span data-ttu-id="baa75-177">750</span><span class="sxs-lookup"><span data-stu-id="baa75-177">750</span></span>                    | <span data-ttu-id="baa75-178">= 75% × 1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-178">= 75% × 1,000</span></span>  |
| <span data-ttu-id="baa75-179">五月到十二月</span><span class="sxs-lookup"><span data-stu-id="baa75-179">May through December</span></span> | <span data-ttu-id="baa75-180">1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-180">1,000</span></span>                  | <span data-ttu-id="baa75-181">= 100% × 1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-181">= 100% × 1,000</span></span> |

### <a name="transactions--reduction-key"></a><span data-ttu-id="baa75-182">交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="baa75-182">Transactions – reduction key</span></span>

<span data-ttu-id="baa75-183">如果选择**交易记录 - 缩减参数**，则通过在缩减参数定义的期间内发生的交易记录来缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-183">If you select **Transactions - reduction key**, the forecast requirements are reduced by the transactions that occur during the periods that are defined by the reduction key.</span></span>

#### <a name="example-transactions--reduction-key"></a><span data-ttu-id="baa75-184">示例：交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="baa75-184">Example: Transactions – reduction key</span></span>

<span data-ttu-id="baa75-185">此示例显示如何实际订单，这将在由缩减参数和缩减需求预测要求定义的期间发生。</span><span class="sxs-lookup"><span data-stu-id="baa75-185">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

<span data-ttu-id="baa75-186">对于本示例，在**主计划**页的**用于缩减预测需求的方法**字段中，选择**交易记录 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="baa75-186">For this example, you select **Transactions - reduction key** in the **Method used to reduce forecast requirements** field on the **Master plans** page.</span></span>

<span data-ttu-id="baa75-187">1 月 1 日存在以下销售订单。</span><span class="sxs-lookup"><span data-stu-id="baa75-187">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="baa75-188">月</span><span class="sxs-lookup"><span data-stu-id="baa75-188">Month</span></span>    | <span data-ttu-id="baa75-189">订购的份数</span><span class="sxs-lookup"><span data-stu-id="baa75-189">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="baa75-190">一月</span><span class="sxs-lookup"><span data-stu-id="baa75-190">January</span></span>  | <span data-ttu-id="baa75-191">956</span><span class="sxs-lookup"><span data-stu-id="baa75-191">956</span></span>                      |
| <span data-ttu-id="baa75-192">二月</span><span class="sxs-lookup"><span data-stu-id="baa75-192">February</span></span> | <span data-ttu-id="baa75-193">1,176</span><span class="sxs-lookup"><span data-stu-id="baa75-193">1,176</span></span>                    |
| <span data-ttu-id="baa75-194">三月</span><span class="sxs-lookup"><span data-stu-id="baa75-194">March</span></span>    | <span data-ttu-id="baa75-195">451</span><span class="sxs-lookup"><span data-stu-id="baa75-195">451</span></span>                      |
| <span data-ttu-id="baa75-196">四月</span><span class="sxs-lookup"><span data-stu-id="baa75-196">April</span></span>    | <span data-ttu-id="baa75-197">119</span><span class="sxs-lookup"><span data-stu-id="baa75-197">119</span></span>                      |

<span data-ttu-id="baa75-198">如果您使用上一个示例中使用的同一个每月 1,000 份需求预测，将向主计划转移以下需求数量。</span><span class="sxs-lookup"><span data-stu-id="baa75-198">If you use the same demand forecast of 1,000 pieces per month that was used in the previous example, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="baa75-199">月</span><span class="sxs-lookup"><span data-stu-id="baa75-199">Month</span></span>                | <span data-ttu-id="baa75-200">所需的份数</span><span class="sxs-lookup"><span data-stu-id="baa75-200">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="baa75-201">一月</span><span class="sxs-lookup"><span data-stu-id="baa75-201">January</span></span>              | <span data-ttu-id="baa75-202">44</span><span class="sxs-lookup"><span data-stu-id="baa75-202">44</span></span>                        |
| <span data-ttu-id="baa75-203">二月</span><span class="sxs-lookup"><span data-stu-id="baa75-203">February</span></span>             | <span data-ttu-id="baa75-204">0</span><span class="sxs-lookup"><span data-stu-id="baa75-204">0</span></span>                         |
| <span data-ttu-id="baa75-205">三月</span><span class="sxs-lookup"><span data-stu-id="baa75-205">March</span></span>                | <span data-ttu-id="baa75-206">549</span><span class="sxs-lookup"><span data-stu-id="baa75-206">549</span></span>                       |
| <span data-ttu-id="baa75-207">四月</span><span class="sxs-lookup"><span data-stu-id="baa75-207">April</span></span>                | <span data-ttu-id="baa75-208">881</span><span class="sxs-lookup"><span data-stu-id="baa75-208">881</span></span>                       |
| <span data-ttu-id="baa75-209">五月到十二月</span><span class="sxs-lookup"><span data-stu-id="baa75-209">May through December</span></span> | <span data-ttu-id="baa75-210">1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-210">1,000</span></span>                     |

### <a name="transactions--dynamic-period"></a><span data-ttu-id="baa75-211">交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="baa75-211">Transactions – dynamic period</span></span>

<span data-ttu-id="baa75-212">如果选择**交易记录 - 动态期间**，将按动态期间进行的实际订单交易记录缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-212">If you select **Transactions - dynamic period**, the forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="baa75-213">动态期间涵盖当前预测日期，并在下一预测开始时结束。</span><span class="sxs-lookup"><span data-stu-id="baa75-213">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span> <span data-ttu-id="baa75-214">在此案例中，主计划将创建计划订单以供给预测的需求（预测需求）。</span><span class="sxs-lookup"><span data-stu-id="baa75-214">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="baa75-215">但是，下达实际订单交易记录时，将缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-215">However, when actual order transactions are placed, the forecast requirements are reduced.</span></span> <span data-ttu-id="baa75-216">实际交易记录占用部分预测需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-216">The actual transactions consume part of the forecasted requirements.</span></span>

<span data-ttu-id="baa75-217">在使用此选项时，会发生以下行为：</span><span class="sxs-lookup"><span data-stu-id="baa75-217">When this option is used, the following behavior occurs:</span></span>

- <span data-ttu-id="baa75-218">将不需要或不使用缩减参数。</span><span class="sxs-lookup"><span data-stu-id="baa75-218">Reduction keys aren't required or used.</span></span> 
- <span data-ttu-id="baa75-219">如果完全缩减预测，则当前预测的预测需求变为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="baa75-219">If the forecast is completely reduced, the forecast requirements for the current forecast become 0 (zero).</span></span>
- <span data-ttu-id="baa75-220">如果没有将来的预测，则最后一个输入的预测的预测需求会缩减。</span><span class="sxs-lookup"><span data-stu-id="baa75-220">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
- <span data-ttu-id="baa75-221">时限包括在缩减预测计算中。</span><span class="sxs-lookup"><span data-stu-id="baa75-221">Time fences are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="baa75-222">正天数包括在缩减预测计算中。</span><span class="sxs-lookup"><span data-stu-id="baa75-222">Positive days are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="baa75-223">如果实际订单交易记录超过预测的需求，则其余的交易记录不会前进到下一预测期间。</span><span class="sxs-lookup"><span data-stu-id="baa75-223">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>

#### <a name="example-1-transactions--dynamic-period"></a><span data-ttu-id="baa75-224">示例 1：交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="baa75-224">Example 1: Transactions – dynamic period</span></span>

<span data-ttu-id="baa75-225">下面是一个简单示例，该示例显示**交易记录 - 动态期间**方法的工作原理。</span><span class="sxs-lookup"><span data-stu-id="baa75-225">Here a simple example that shows how the **Transactions - dynamic period** method works.</span></span>

<span data-ttu-id="baa75-226">对于本示例，将在主计划中包含以下需求预测。</span><span class="sxs-lookup"><span data-stu-id="baa75-226">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="baa75-227">日期</span><span class="sxs-lookup"><span data-stu-id="baa75-227">Date</span></span>       | <span data-ttu-id="baa75-228">需求预测</span><span class="sxs-lookup"><span data-stu-id="baa75-228">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="baa75-229">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="baa75-229">January 1</span></span>  | <span data-ttu-id="baa75-230">1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-230">1,000</span></span>           |
| <span data-ttu-id="baa75-231">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="baa75-231">February 1</span></span> | <span data-ttu-id="baa75-232">500</span><span class="sxs-lookup"><span data-stu-id="baa75-232">500</span></span>             |

<span data-ttu-id="baa75-233">还将创建以下销售订单。</span><span class="sxs-lookup"><span data-stu-id="baa75-233">You also create the following sales orders.</span></span>

| <span data-ttu-id="baa75-234">日期</span><span class="sxs-lookup"><span data-stu-id="baa75-234">Date</span></span>        | <span data-ttu-id="baa75-235">销售订单数量</span><span class="sxs-lookup"><span data-stu-id="baa75-235">Sales order quantity</span></span> |
|-------------|----------------------|
| <span data-ttu-id="baa75-236">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="baa75-236">January 15</span></span>  | <span data-ttu-id="baa75-237">500</span><span class="sxs-lookup"><span data-stu-id="baa75-237">500</span></span>                  |
| <span data-ttu-id="baa75-238">2 月 15 日</span><span class="sxs-lookup"><span data-stu-id="baa75-238">February 15</span></span> | <span data-ttu-id="baa75-239">100</span><span class="sxs-lookup"><span data-stu-id="baa75-239">100</span></span>                  |

<span data-ttu-id="baa75-240">在此案例中，将创建以下计划订单。</span><span class="sxs-lookup"><span data-stu-id="baa75-240">In this case, the following planned orders are created.</span></span>

| <span data-ttu-id="baa75-241">需求预测日期</span><span class="sxs-lookup"><span data-stu-id="baa75-241">Demand forecast date</span></span> | <span data-ttu-id="baa75-242">数量</span><span class="sxs-lookup"><span data-stu-id="baa75-242">Quantity</span></span> | <span data-ttu-id="baa75-243">摘要</span><span class="sxs-lookup"><span data-stu-id="baa75-243">Explanation</span></span>                           |
|--------------------- |----------|---------------------------------------|
| <span data-ttu-id="baa75-244">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="baa75-244">January 1</span></span>            | <span data-ttu-id="baa75-245">800</span><span class="sxs-lookup"><span data-stu-id="baa75-245">800</span></span>      | <span data-ttu-id="baa75-246">预测需求 (= 1,000 – 200)</span><span class="sxs-lookup"><span data-stu-id="baa75-246">Forecast requirements (= 1,000 – 200)</span></span> |
| <span data-ttu-id="baa75-247">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="baa75-247">January 15</span></span>           | <span data-ttu-id="baa75-248">200</span><span class="sxs-lookup"><span data-stu-id="baa75-248">200</span></span>      | <span data-ttu-id="baa75-249">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="baa75-249">Sales orders requirements</span></span>             |
| <span data-ttu-id="baa75-250">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="baa75-250">February 1</span></span>           | <span data-ttu-id="baa75-251">600</span><span class="sxs-lookup"><span data-stu-id="baa75-251">600</span></span>      | <span data-ttu-id="baa75-252">预测需求 (= 1,000 – 400)</span><span class="sxs-lookup"><span data-stu-id="baa75-252">Forecast requirements (= 1,000 – 400)</span></span> |
| <span data-ttu-id="baa75-253">2 月 15 日</span><span class="sxs-lookup"><span data-stu-id="baa75-253">February 15</span></span>          | <span data-ttu-id="baa75-254">400</span><span class="sxs-lookup"><span data-stu-id="baa75-254">400</span></span>      | <span data-ttu-id="baa75-255">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="baa75-255">Sales orders requirements</span></span>             |

#### <a name="example-2-transactions--dynamic-period"></a><span data-ttu-id="baa75-256">示例 2：交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="baa75-256">Example 2: Transactions – dynamic period</span></span>

<span data-ttu-id="baa75-257">在大多数情况下，会设置系统以使交易记录在特定预测期间减少需求预测：周、月，等等。</span><span class="sxs-lookup"><span data-stu-id="baa75-257">In most cases, systems are set up so that transactions reduce demand forecast in specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="baa75-258">这些期间是在缩减参数中定义的。</span><span class="sxs-lookup"><span data-stu-id="baa75-258">These periods are defined in the reduction key.</span></span> <span data-ttu-id="baa75-259">但是，两个需求预测行之间的时间还可*提示*期间。</span><span class="sxs-lookup"><span data-stu-id="baa75-259">However, the time between two demand forecast lines can also *imply* a period.</span></span>

<span data-ttu-id="baa75-260">对于此示例，将为以下日期和数量创建需求预测。</span><span class="sxs-lookup"><span data-stu-id="baa75-260">For this example, you create a demand forecast for the following dates and quantities.</span></span>

| <span data-ttu-id="baa75-261">日期</span><span class="sxs-lookup"><span data-stu-id="baa75-261">Date</span></span>       | <span data-ttu-id="baa75-262">需求预测</span><span class="sxs-lookup"><span data-stu-id="baa75-262">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="baa75-263">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="baa75-263">January 1</span></span>  | <span data-ttu-id="baa75-264">1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-264">1,000</span></span>           |
| <span data-ttu-id="baa75-265">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="baa75-265">January 5</span></span>  | <span data-ttu-id="baa75-266">500</span><span class="sxs-lookup"><span data-stu-id="baa75-266">500</span></span>             |
| <span data-ttu-id="baa75-267">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="baa75-267">January 12</span></span> | <span data-ttu-id="baa75-268">1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-268">1,000</span></span>           |

<span data-ttu-id="baa75-269">请注意，在此预测中，预测日期之间没有清晰的间隔。</span><span class="sxs-lookup"><span data-stu-id="baa75-269">Notice that, in this forecast, there isn't a clear period between the forecast dates.</span></span> <span data-ttu-id="baa75-270">第一个和第二个日期之间的间隔为四天，第二个和第三个日期之间的间隔为七天。</span><span class="sxs-lookup"><span data-stu-id="baa75-270">Between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="baa75-271">这些间隔就是动态期间。</span><span class="sxs-lookup"><span data-stu-id="baa75-271">These spans are the dynamic periods.</span></span>

<span data-ttu-id="baa75-272">还将创建以下销售订单行。</span><span class="sxs-lookup"><span data-stu-id="baa75-272">You also create the following sales order lines.</span></span>

| <span data-ttu-id="baa75-273">日期</span><span class="sxs-lookup"><span data-stu-id="baa75-273">Date</span></span>                             | <span data-ttu-id="baa75-274">销售订单数量</span><span class="sxs-lookup"><span data-stu-id="baa75-274">Sales order quantity</span></span> |
|----------------------------------|----------------------|
| <span data-ttu-id="baa75-275">上一年度的 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="baa75-275">December 15 in the previous year</span></span> | <span data-ttu-id="baa75-276">500</span><span class="sxs-lookup"><span data-stu-id="baa75-276">500</span></span>                  |
| <span data-ttu-id="baa75-277">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="baa75-277">January 3</span></span>                        | <span data-ttu-id="baa75-278">100</span><span class="sxs-lookup"><span data-stu-id="baa75-278">100</span></span>                  |
| <span data-ttu-id="baa75-279">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="baa75-279">January 10</span></span>                       | <span data-ttu-id="baa75-280">200</span><span class="sxs-lookup"><span data-stu-id="baa75-280">200</span></span>                  |

<span data-ttu-id="baa75-281">在此案例中，将以下面的方式缩减预测：</span><span class="sxs-lookup"><span data-stu-id="baa75-281">In this case, the forecast is reduced in the following manner:</span></span>

- <span data-ttu-id="baa75-282">因为第一个销售订单不在任何期间，因此不会缩减任何预测。</span><span class="sxs-lookup"><span data-stu-id="baa75-282">Because the first sales order isn't in any period, it doesn't reduce any forecast.</span></span>
- <span data-ttu-id="baa75-283">因为第二个销售订单是从 1 月 1 日到 1 月 5 日，因此它会将 1 月 1 日的预测缩减 100。</span><span class="sxs-lookup"><span data-stu-id="baa75-283">Because the second sales order is between January 1 and January 5, it reduces the forecast for January 1 by 100.</span></span>
- <span data-ttu-id="baa75-284">因为第三个销售订单是从 5 月 5 日到 5 月 12 日，因此它会将 5 月 5 日的预测缩减 200。</span><span class="sxs-lookup"><span data-stu-id="baa75-284">Because the third sales order is between January 5 and January 12, it reduces the forecast for January 5 by 200.</span></span>

<span data-ttu-id="baa75-285">因此，将创建以下计划订单。</span><span class="sxs-lookup"><span data-stu-id="baa75-285">Therefore, the following planned orders are created.</span></span>

| <span data-ttu-id="baa75-286">需求预测日期</span><span class="sxs-lookup"><span data-stu-id="baa75-286">Demand forecast date</span></span>             | <span data-ttu-id="baa75-287">数量</span><span class="sxs-lookup"><span data-stu-id="baa75-287">Quantity</span></span> | <span data-ttu-id="baa75-288">摘要</span><span class="sxs-lookup"><span data-stu-id="baa75-288">Explanation</span></span>                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| <span data-ttu-id="baa75-289">上一年度的 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="baa75-289">December 15 in the previous year</span></span> | <span data-ttu-id="baa75-290">500</span><span class="sxs-lookup"><span data-stu-id="baa75-290">500</span></span>      | <span data-ttu-id="baa75-291">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="baa75-291">Sales order requirements</span></span>                                            |
| <span data-ttu-id="baa75-292">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="baa75-292">January 1</span></span>                        | <span data-ttu-id="baa75-293">900</span><span class="sxs-lookup"><span data-stu-id="baa75-293">900</span></span>      | <span data-ttu-id="baa75-294">预测需求期间 1 月 1 日到 1 月 5 日 (= 1,000 – 100)</span><span class="sxs-lookup"><span data-stu-id="baa75-294">Forecast requirements period January 1 to January 5 (= 1,000 – 100)</span></span> |
| <span data-ttu-id="baa75-295">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="baa75-295">January 3</span></span>                        | <span data-ttu-id="baa75-296">100</span><span class="sxs-lookup"><span data-stu-id="baa75-296">100</span></span>      | <span data-ttu-id="baa75-297">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="baa75-297">Sales order requirements</span></span>                                            |
| <span data-ttu-id="baa75-298">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="baa75-298">January 5</span></span>                        | <span data-ttu-id="baa75-299">300</span><span class="sxs-lookup"><span data-stu-id="baa75-299">300</span></span>      | <span data-ttu-id="baa75-300">预测需求期间 1 月 5 日到 1 月 10 日 (= 500 – 200)</span><span class="sxs-lookup"><span data-stu-id="baa75-300">Forecast requirements period January 5 to January 10 (= 500 – 200)</span></span>  |
| <span data-ttu-id="baa75-301">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="baa75-301">January 12</span></span>                       | <span data-ttu-id="baa75-302">1,000</span><span class="sxs-lookup"><span data-stu-id="baa75-302">1,000</span></span>    | <span data-ttu-id="baa75-303">预测需求期间 1 月 12 日到月底</span><span class="sxs-lookup"><span data-stu-id="baa75-303">Forecast requirements period January 12 to end</span></span>                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a><span data-ttu-id="baa75-304">创建和设置预测缩减参数</span><span class="sxs-lookup"><span data-stu-id="baa75-304">Create and set up a forecast reduction key</span></span>

<span data-ttu-id="baa75-305">用于缩减预测需求的**交易记录 - 缩减参数**和**百分比- 缩减参数**方法中使用预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="baa75-305">A forecast reduction key is used in the **Transactions - reduction key** and **Percent- reduction key** methods for reducing forecast requirements.</span></span> <span data-ttu-id="baa75-306">若要创建和设置缩减参数，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="baa75-306">Follow these steps to create and set up a reduction key.</span></span>

1. <span data-ttu-id="baa75-307">转到**主计划 \> 设置 \> 覆盖范围 \> 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="baa75-307">Go to **Master planning \> Setup \> Coverage \> Reduction keys**.</span></span>
2. <span data-ttu-id="baa75-308">选择**新建**或按 **Ctrl+N** 创建一个缩减参数。</span><span class="sxs-lookup"><span data-stu-id="baa75-308">Select **New** or press **Ctrl+N** to create a reduction key.</span></span>
3. <span data-ttu-id="baa75-309">在**缩减参数**字段中，输入预测缩减参数的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="baa75-309">In the **Reduction key** field, enter a unique identifier for the forecast reduction key.</span></span> <span data-ttu-id="baa75-310">然后在**名称**字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="baa75-310">Then, in the **Name** field, enter a name.</span></span> 
4. <span data-ttu-id="baa75-311">定义期间和每个期间中的缩减参数百分比：</span><span class="sxs-lookup"><span data-stu-id="baa75-311">Define the periods and the reduction key percentage in each period:</span></span>

    - <span data-ttu-id="baa75-312">**生效日期**字段指示开始创建期间的日期。</span><span class="sxs-lookup"><span data-stu-id="baa75-312">The **Effective date** field indicates the date when creation of the periods starts.</span></span> <span data-ttu-id="baa75-313">如果**使用生效日期**选项设置为**是**，期间将在生效日期开始。</span><span class="sxs-lookup"><span data-stu-id="baa75-313">When the **Use the effective date** option is set to **Yes**, the periods start on the effective date.</span></span> <span data-ttu-id="baa75-314">如果设置为**否**，期间将在运行主计划的日期开始。</span><span class="sxs-lookup"><span data-stu-id="baa75-314">When it's set to **No**, the periods start on the date when master planning is run.</span></span>
    - <span data-ttu-id="baa75-315">定义应进行预测缩减的期间。</span><span class="sxs-lookup"><span data-stu-id="baa75-315">Define the periods that the forecast reduction should occur during.</span></span>
    - <span data-ttu-id="baa75-316">为具体期间指定应缩减预测需求的百分比。</span><span class="sxs-lookup"><span data-stu-id="baa75-316">For a specific period, specify the percentages that the forecast requirements should be reduced by.</span></span> <span data-ttu-id="baa75-317">您可以输入正值以减少需求，或输入负值增加需求。</span><span class="sxs-lookup"><span data-stu-id="baa75-317">You can enter positive values to decrease requirements or negative values to increase requirements.</span></span>

## <a name="use-a-reduction-key"></a><span data-ttu-id="baa75-318">使用一个缩减参数</span><span class="sxs-lookup"><span data-stu-id="baa75-318">Use a reduction key</span></span>

<span data-ttu-id="baa75-319">必须为物料的覆盖范围组分配预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="baa75-319">A forecast reduction key must be assigned to the coverage group of the item.</span></span> <span data-ttu-id="baa75-320">若要为物料的覆盖范围组分配缩减参数，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="baa75-320">Follow these steps to assign a reduction key to an item's coverage group.</span></span>

1. <span data-ttu-id="baa75-321">转至**主计划 \> 设置 \> 覆盖范围 \> 覆盖范围组**。</span><span class="sxs-lookup"><span data-stu-id="baa75-321">Go to **Master planning \> Setup \> Coverage \> Coverage groups**.</span></span>
2. <span data-ttu-id="baa75-322">在**其他**快速选项卡上的**缩减参数**字段中，选择缩减参数分配给覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="baa75-322">On the **Other** FastTab, in the **Reduction key** field, select the reduction key to assign to the coverage group.</span></span> <span data-ttu-id="baa75-323">缩减参数然后运用于属于该覆盖范围组的所有物料。</span><span class="sxs-lookup"><span data-stu-id="baa75-323">The reduction key then applies to all items that belong to the coverage group.</span></span>
3. <span data-ttu-id="baa75-324">在主计划编制期间，若要使用缩减参数计算预测缩减，必须在设置预测计划或主计划时定义此设置。</span><span class="sxs-lookup"><span data-stu-id="baa75-324">To use a reduction key to calculate forecast reduction during master scheduling, you must define this setting in the setup of the forecast plan or the master plan.</span></span> <span data-ttu-id="baa75-325">转至以下位置之一：</span><span class="sxs-lookup"><span data-stu-id="baa75-325">Go to one of the following locations:</span></span>

    - <span data-ttu-id="baa75-326">主计划 \> 设置 \> 计划 \> 预测计划</span><span class="sxs-lookup"><span data-stu-id="baa75-326">Master planning \> Setup \> Plans \> Forecast plans</span></span>
    - <span data-ttu-id="baa75-327">主计划 \> 设置 \> 计划 \> 主计划</span><span class="sxs-lookup"><span data-stu-id="baa75-327">Master planning \> Setup \> Plans \> Master plans</span></span>

4. <span data-ttu-id="baa75-328">在**预测计划**或**主计划**页面**常规**快速选项卡上的**用于减少预测需求的方法**字段中，选择**百分比 - 缩减参数**或**交易记录 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="baa75-328">On the **Forecast plans** or **Master plans** page, on the **General** FastTab, in the **Method used to reduce forecast requirements** field, select either **Percent - reduction key** or **Transactions - reduction key**.</span></span>

## <a name="reduce-a-forecast-by-transactions"></a><span data-ttu-id="baa75-329">按交易记录缩减预测</span><span class="sxs-lookup"><span data-stu-id="baa75-329">Reduce a forecast by transactions</span></span>

<span data-ttu-id="baa75-330">如果用于缩减预测需求的方法选择**交易记录 - 缩减参数**或**交易记录 - 动态期间**，则可指定哪些交易记录缩减预测。</span><span class="sxs-lookup"><span data-stu-id="baa75-330">When you select **Transactions - reduction key** or **Transactions - dynamic period** as the method for reducing forecast requirements, you can specify which transactions reduce the forecast.</span></span> <span data-ttu-id="baa75-331">如果所有交易记录均应缩减预测，请在**已发布产品**页面**其他**快速选项卡上的**预测减少依据**字段中选择**所有交易记录**，如果只有销售订单才应缩减预测，请选择**订单**。</span><span class="sxs-lookup"><span data-stu-id="baa75-331">On the **Released products** page, on the **Other** FastTab, in the **Reduce forecast by** field, select **All transactions** if all transactions should reduce the forecast or **Orders** if only sales orders should reduce the forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="baa75-332">其他资源</span><span class="sxs-lookup"><span data-stu-id="baa75-332">Additional resources</span></span>

[<span data-ttu-id="baa75-333">主计划</span><span class="sxs-lookup"><span data-stu-id="baa75-333">Master plans</span></span>](master-plans.md)
