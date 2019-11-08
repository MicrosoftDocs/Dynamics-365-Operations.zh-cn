---
title: 预测缩减参数
description: 本主题提供显示如何设置缩减参数的示例。 它包含有关各种缩减参数设置以及每个结果的信息。 可以使用缩减参数以定义如何缩减预测需求。
author: roxanadiaconu
manager: AnnBe
ms.date: 07/09/2019
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
ms.openlocfilehash: d303b08ed39232a1154c5170bf585a7c25e43f8d
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550451"
---
# <a name="forecast-reduction-keys"></a><span data-ttu-id="ccccd-105">预测缩减参数</span><span class="sxs-lookup"><span data-stu-id="ccccd-105">Forecast reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccccd-106">本主题提供有关用于缩减预测需求的不同方法的信息。</span><span class="sxs-lookup"><span data-stu-id="ccccd-106">This topic provides information about the different methods that are used to reduce forecast requirements.</span></span> <span data-ttu-id="ccccd-107">其中包括每种方法的结果的示例。</span><span class="sxs-lookup"><span data-stu-id="ccccd-107">It includes examples of the results of each method.</span></span> <span data-ttu-id="ccccd-108">还介绍如何创建、设置和使用预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="ccccd-108">It also explains how to create, set up, and use a forecast reduction key.</span></span> <span data-ttu-id="ccccd-109">一些方法使用预测缩减参数缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-109">Some methods use a forecast reduction key to reduce forecast requirements.</span></span>

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a><span data-ttu-id="ccccd-110">用于缩减预测需求的方法</span><span class="sxs-lookup"><span data-stu-id="ccccd-110">Methods that are used to reduce forecast requirements</span></span>

<span data-ttu-id="ccccd-111">向主计划添加预测时，可以选择包含实际需求时如何缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-111">When you include a forecast in a master plan, you can select how the forecast requirements are reduced when actual demand is included.</span></span>

<span data-ttu-id="ccccd-112">若要在主计划中添加预测并选择用于缩减预测需求的方法，请转到**主计划 \> 设置 \> 计划 \> 主计划**。</span><span class="sxs-lookup"><span data-stu-id="ccccd-112">To include a forecast in a master plan and select the method that is used to reduce forecast requirements, go to **Master planning \> Setup \> Plans \> Master plans**.</span></span> <span data-ttu-id="ccccd-113">在**预测模型**字段中，选择一个预测模型。</span><span class="sxs-lookup"><span data-stu-id="ccccd-113">In the **Forecast model** field, select a forecast model.</span></span> <span data-ttu-id="ccccd-114">在**用于减少预测需求的方法**字段中，选择一个方法。</span><span class="sxs-lookup"><span data-stu-id="ccccd-114">In the **Method used to reduce forecast requirements** field, select a method.</span></span> <span data-ttu-id="ccccd-115">选项如下：</span><span class="sxs-lookup"><span data-stu-id="ccccd-115">The following options are available:</span></span>

- <span data-ttu-id="ccccd-116">无</span><span class="sxs-lookup"><span data-stu-id="ccccd-116">None</span></span>
- <span data-ttu-id="ccccd-117">百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="ccccd-117">Percent – reduction key</span></span>
- <span data-ttu-id="ccccd-118">交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="ccccd-118">Transactions – reduction key</span></span>
- <span data-ttu-id="ccccd-119">交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="ccccd-119">Transactions – dynamic period</span></span>

<span data-ttu-id="ccccd-120">以下部分提供有关每个选项的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ccccd-120">The following sections provide more information about each option.</span></span>

### <a name="none"></a><span data-ttu-id="ccccd-121">无</span><span class="sxs-lookup"><span data-stu-id="ccccd-121">None</span></span>

<span data-ttu-id="ccccd-122">如果您选择**无**，则在主计划编制期间不缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-122">If you select **None**, the forecast requirements aren't reduced during master scheduling.</span></span> <span data-ttu-id="ccccd-123">在此案例中，主计划将创建计划订单以供给预测的需求（预测需求）。</span><span class="sxs-lookup"><span data-stu-id="ccccd-123">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="ccccd-124">这些计划订单中维持建议的数量，不考虑其他类型的需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-124">These planned orders maintain the suggested quantity, regardless of other types of demand.</span></span> <span data-ttu-id="ccccd-125">例如，如果下达销售订单，主计划将创建更多计划订单以供给销售订单。</span><span class="sxs-lookup"><span data-stu-id="ccccd-125">For example, if sales orders are placed, master planning creates additional planned orders to supply the sales orders.</span></span> <span data-ttu-id="ccccd-126">将不缩减预测需求的数量。</span><span class="sxs-lookup"><span data-stu-id="ccccd-126">The quantity of the forecast requirements isn't reduced.</span></span>

### <a name="percent--reduction-key"></a><span data-ttu-id="ccccd-127">百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="ccccd-127">Percent – reduction key</span></span>

<span data-ttu-id="ccccd-128">如果选择**百分比 - 缩减参数**，则根据百分比和缩减参数定义的百分比和期间来缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-128">If you select **Percent - reduction key**, the forecast requirements are reduced according to the percentages and periods that are defined by the reduction key.</span></span> <span data-ttu-id="ccccd-129">在此案例中，主计划创建计划订单，在此类订单中，数量的计算方法是预测数量 × 各期间的缩减参数。</span><span class="sxs-lookup"><span data-stu-id="ccccd-129">In this case, master planning creates planned orders where the quantity is calculated as forecasted quantity × reduction key in each period.</span></span> <span data-ttu-id="ccccd-130">如果有其他类型的需求，主计划还将创建计划订单以满足该需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-130">If there are other types of demand, master planning also creates planned orders to supply that demand.</span></span>

#### <a name="example-percent--reduction-key"></a><span data-ttu-id="ccccd-131">示例：百分比 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="ccccd-131">Example: Percent – reduction key</span></span>

<span data-ttu-id="ccccd-132">此示例显示由缩减参数如何根据由缩减参数定义的百分比和期间缩减需求预测要求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-132">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

<span data-ttu-id="ccccd-133">对于本示例，将在主计划中包含以下需求预测。</span><span class="sxs-lookup"><span data-stu-id="ccccd-133">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="ccccd-134">月</span><span class="sxs-lookup"><span data-stu-id="ccccd-134">Month</span></span>    | <span data-ttu-id="ccccd-135">需求预测</span><span class="sxs-lookup"><span data-stu-id="ccccd-135">Demand forecast</span></span> |
|----------|-----------------|
| <span data-ttu-id="ccccd-136">一月</span><span class="sxs-lookup"><span data-stu-id="ccccd-136">January</span></span>  | <span data-ttu-id="ccccd-137">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-137">1,000</span></span>           |
| <span data-ttu-id="ccccd-138">二月</span><span class="sxs-lookup"><span data-stu-id="ccccd-138">February</span></span> | <span data-ttu-id="ccccd-139">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-139">1,000</span></span>           |
| <span data-ttu-id="ccccd-140">三月</span><span class="sxs-lookup"><span data-stu-id="ccccd-140">March</span></span>    | <span data-ttu-id="ccccd-141">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-141">1,000</span></span>           |
| <span data-ttu-id="ccccd-142">四月</span><span class="sxs-lookup"><span data-stu-id="ccccd-142">April</span></span>    | <span data-ttu-id="ccccd-143">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-143">1,000</span></span>           |

<span data-ttu-id="ccccd-144">在**缩减参数**页上，设置以下行。</span><span class="sxs-lookup"><span data-stu-id="ccccd-144">On the **Reduction keys** page, you set up the following lines.</span></span>

| <span data-ttu-id="ccccd-145">找零</span><span class="sxs-lookup"><span data-stu-id="ccccd-145">Change</span></span> | <span data-ttu-id="ccccd-146">单位</span><span class="sxs-lookup"><span data-stu-id="ccccd-146">Unit</span></span>  | <span data-ttu-id="ccccd-147">百分比</span><span class="sxs-lookup"><span data-stu-id="ccccd-147">Percent</span></span> |
|--------|-------|---------|
| <span data-ttu-id="ccccd-148">1</span><span class="sxs-lookup"><span data-stu-id="ccccd-148">1</span></span>      | <span data-ttu-id="ccccd-149">月</span><span class="sxs-lookup"><span data-stu-id="ccccd-149">Month</span></span> | <span data-ttu-id="ccccd-150">100</span><span class="sxs-lookup"><span data-stu-id="ccccd-150">100</span></span>     |
| <span data-ttu-id="ccccd-151">2</span><span class="sxs-lookup"><span data-stu-id="ccccd-151">2</span></span>      | <span data-ttu-id="ccccd-152">月</span><span class="sxs-lookup"><span data-stu-id="ccccd-152">Month</span></span> | <span data-ttu-id="ccccd-153">75</span><span class="sxs-lookup"><span data-stu-id="ccccd-153">75</span></span>      |
| <span data-ttu-id="ccccd-154">3</span><span class="sxs-lookup"><span data-stu-id="ccccd-154">3</span></span>      | <span data-ttu-id="ccccd-155">月</span><span class="sxs-lookup"><span data-stu-id="ccccd-155">Month</span></span> | <span data-ttu-id="ccccd-156">50</span><span class="sxs-lookup"><span data-stu-id="ccccd-156">50</span></span>      |
| <span data-ttu-id="ccccd-157">4</span><span class="sxs-lookup"><span data-stu-id="ccccd-157">4</span></span>      | <span data-ttu-id="ccccd-158">月</span><span class="sxs-lookup"><span data-stu-id="ccccd-158">Month</span></span> | <span data-ttu-id="ccccd-159">25</span><span class="sxs-lookup"><span data-stu-id="ccccd-159">25</span></span>      |

<span data-ttu-id="ccccd-160">将缩减参数分配给物料的覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="ccccd-160">You assign the reduction key to the item's coverage group.</span></span> <span data-ttu-id="ccccd-161">然后在**主计划**页的**用于缩减预测需求的方法**字段中，选择**百分比 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="ccccd-161">Then, on the **Master plans** page, in the **Method used to reduce forecast requirements** field, you select **Percent - reduction key**.</span></span>

<span data-ttu-id="ccccd-162">在此案例中，如果在 1 月 1 日运行预测计划编制，则将根据您在**缩减参数**页上设置的百分比来消耗销售预测需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-162">In this case, if you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="ccccd-163">以下需求数量将转移到主计划。</span><span class="sxs-lookup"><span data-stu-id="ccccd-163">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="ccccd-164">月</span><span class="sxs-lookup"><span data-stu-id="ccccd-164">Month</span></span>                | <span data-ttu-id="ccccd-165">计划订单数量</span><span class="sxs-lookup"><span data-stu-id="ccccd-165">Planned order quantity</span></span> | <span data-ttu-id="ccccd-166">计算</span><span class="sxs-lookup"><span data-stu-id="ccccd-166">Calculation</span></span>    |
|----------------------|------------------------|----------------|
| <span data-ttu-id="ccccd-167">一月</span><span class="sxs-lookup"><span data-stu-id="ccccd-167">January</span></span>              | <span data-ttu-id="ccccd-168">0</span><span class="sxs-lookup"><span data-stu-id="ccccd-168">0</span></span>                      | <span data-ttu-id="ccccd-169">= 0% × 1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-169">= 0% × 1,000</span></span>   |
| <span data-ttu-id="ccccd-170">二月</span><span class="sxs-lookup"><span data-stu-id="ccccd-170">February</span></span>             | <span data-ttu-id="ccccd-171">250</span><span class="sxs-lookup"><span data-stu-id="ccccd-171">250</span></span>                    | <span data-ttu-id="ccccd-172">= 25% × 1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-172">= 25% × 1,000</span></span>  |
| <span data-ttu-id="ccccd-173">三月</span><span class="sxs-lookup"><span data-stu-id="ccccd-173">March</span></span>                | <span data-ttu-id="ccccd-174">500</span><span class="sxs-lookup"><span data-stu-id="ccccd-174">500</span></span>                    | <span data-ttu-id="ccccd-175">= 50% × 1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-175">= 50% × 1,000</span></span>  |
| <span data-ttu-id="ccccd-176">四月</span><span class="sxs-lookup"><span data-stu-id="ccccd-176">April</span></span>                | <span data-ttu-id="ccccd-177">750</span><span class="sxs-lookup"><span data-stu-id="ccccd-177">750</span></span>                    | <span data-ttu-id="ccccd-178">= 75% × 1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-178">= 75% × 1,000</span></span>  |
| <span data-ttu-id="ccccd-179">五月到十二月</span><span class="sxs-lookup"><span data-stu-id="ccccd-179">May through December</span></span> | <span data-ttu-id="ccccd-180">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-180">1,000</span></span>                  | <span data-ttu-id="ccccd-181">= 100% × 1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-181">= 100% × 1,000</span></span> |

### <a name="transactions--reduction-key"></a><span data-ttu-id="ccccd-182">交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="ccccd-182">Transactions – reduction key</span></span>

<span data-ttu-id="ccccd-183">如果选择**交易记录 - 缩减参数**，则通过在缩减参数定义的期间内发生的交易记录来缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-183">If you select **Transactions - reduction key**, the forecast requirements are reduced by the transactions that occur during the periods that are defined by the reduction key.</span></span>

#### <a name="example-transactions--reduction-key"></a><span data-ttu-id="ccccd-184">示例：交易记录 - 缩减参数</span><span class="sxs-lookup"><span data-stu-id="ccccd-184">Example: Transactions – reduction key</span></span>

<span data-ttu-id="ccccd-185">此示例显示如何实际订单，这将在由缩减参数和缩减需求预测要求定义的期间发生。</span><span class="sxs-lookup"><span data-stu-id="ccccd-185">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

<span data-ttu-id="ccccd-186">对于本示例，在**主计划**页的**用于缩减预测需求的方法**字段中，选择**交易记录 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="ccccd-186">For this example, you select **Transactions - reduction key** in the **Method used to reduce forecast requirements** field on the **Master plans** page.</span></span>

<span data-ttu-id="ccccd-187">1 月 1 日存在以下销售订单。</span><span class="sxs-lookup"><span data-stu-id="ccccd-187">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="ccccd-188">月</span><span class="sxs-lookup"><span data-stu-id="ccccd-188">Month</span></span>    | <span data-ttu-id="ccccd-189">订购的份数</span><span class="sxs-lookup"><span data-stu-id="ccccd-189">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="ccccd-190">一月</span><span class="sxs-lookup"><span data-stu-id="ccccd-190">January</span></span>  | <span data-ttu-id="ccccd-191">956</span><span class="sxs-lookup"><span data-stu-id="ccccd-191">956</span></span>                      |
| <span data-ttu-id="ccccd-192">二月</span><span class="sxs-lookup"><span data-stu-id="ccccd-192">February</span></span> | <span data-ttu-id="ccccd-193">1,176</span><span class="sxs-lookup"><span data-stu-id="ccccd-193">1,176</span></span>                    |
| <span data-ttu-id="ccccd-194">三月</span><span class="sxs-lookup"><span data-stu-id="ccccd-194">March</span></span>    | <span data-ttu-id="ccccd-195">451</span><span class="sxs-lookup"><span data-stu-id="ccccd-195">451</span></span>                      |
| <span data-ttu-id="ccccd-196">四月</span><span class="sxs-lookup"><span data-stu-id="ccccd-196">April</span></span>    | <span data-ttu-id="ccccd-197">119</span><span class="sxs-lookup"><span data-stu-id="ccccd-197">119</span></span>                      |

<span data-ttu-id="ccccd-198">如果您使用上一个示例中使用的同一个每月 1,000 份需求预测，将向主计划转移以下需求数量。</span><span class="sxs-lookup"><span data-stu-id="ccccd-198">If you use the same demand forecast of 1,000 pieces per month that was used in the previous example, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="ccccd-199">月</span><span class="sxs-lookup"><span data-stu-id="ccccd-199">Month</span></span>                | <span data-ttu-id="ccccd-200">所需的份数</span><span class="sxs-lookup"><span data-stu-id="ccccd-200">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="ccccd-201">一月</span><span class="sxs-lookup"><span data-stu-id="ccccd-201">January</span></span>              | <span data-ttu-id="ccccd-202">44</span><span class="sxs-lookup"><span data-stu-id="ccccd-202">44</span></span>                        |
| <span data-ttu-id="ccccd-203">二月</span><span class="sxs-lookup"><span data-stu-id="ccccd-203">February</span></span>             | <span data-ttu-id="ccccd-204">0</span><span class="sxs-lookup"><span data-stu-id="ccccd-204">0</span></span>                         |
| <span data-ttu-id="ccccd-205">三月</span><span class="sxs-lookup"><span data-stu-id="ccccd-205">March</span></span>                | <span data-ttu-id="ccccd-206">549</span><span class="sxs-lookup"><span data-stu-id="ccccd-206">549</span></span>                       |
| <span data-ttu-id="ccccd-207">四月</span><span class="sxs-lookup"><span data-stu-id="ccccd-207">April</span></span>                | <span data-ttu-id="ccccd-208">881</span><span class="sxs-lookup"><span data-stu-id="ccccd-208">881</span></span>                       |
| <span data-ttu-id="ccccd-209">五月到十二月</span><span class="sxs-lookup"><span data-stu-id="ccccd-209">May through December</span></span> | <span data-ttu-id="ccccd-210">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-210">1,000</span></span>                     |

### <a name="transactions--dynamic-period"></a><span data-ttu-id="ccccd-211">交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="ccccd-211">Transactions – dynamic period</span></span>

<span data-ttu-id="ccccd-212">如果选择**交易记录 - 动态期间**，将按动态期间进行的实际订单交易记录缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-212">If you select **Transactions - dynamic period**, the forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="ccccd-213">动态期间涵盖当前预测日期，并在下一预测开始时结束。</span><span class="sxs-lookup"><span data-stu-id="ccccd-213">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span> <span data-ttu-id="ccccd-214">在此案例中，主计划将创建计划订单以供给预测的需求（预测需求）。</span><span class="sxs-lookup"><span data-stu-id="ccccd-214">In this case, master planning creates planned orders to supply the forecasted demand (forecast requirements).</span></span> <span data-ttu-id="ccccd-215">但是，下达实际订单交易记录时，将缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-215">However, when actual order transactions are placed, the forecast requirements are reduced.</span></span> <span data-ttu-id="ccccd-216">实际交易记录占用部分预测需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-216">The actual transactions consume part of the forecasted requirements.</span></span>

<span data-ttu-id="ccccd-217">在使用此选项时，会发生以下行为：</span><span class="sxs-lookup"><span data-stu-id="ccccd-217">When this option is used, the following behavior occurs:</span></span>

- <span data-ttu-id="ccccd-218">将不需要或不使用缩减参数。</span><span class="sxs-lookup"><span data-stu-id="ccccd-218">Reduction keys aren't required or used.</span></span> 
- <span data-ttu-id="ccccd-219">如果完全缩减预测，则当前预测的预测需求变为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="ccccd-219">If the forecast is completely reduced, the forecast requirements for the current forecast become 0 (zero).</span></span>
- <span data-ttu-id="ccccd-220">如果没有将来的预测，则最后一个输入的预测的预测需求会缩减。</span><span class="sxs-lookup"><span data-stu-id="ccccd-220">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
- <span data-ttu-id="ccccd-221">时限包括在缩减预测计算中。</span><span class="sxs-lookup"><span data-stu-id="ccccd-221">Time fences are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="ccccd-222">正天数包括在缩减预测计算中。</span><span class="sxs-lookup"><span data-stu-id="ccccd-222">Positive days are included in the forecast reduction calculation.</span></span>
- <span data-ttu-id="ccccd-223">如果实际订单交易记录超过预测的需求，则其余的交易记录不会前进到下一预测期间。</span><span class="sxs-lookup"><span data-stu-id="ccccd-223">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>

#### <a name="example-1-transactions--dynamic-period"></a><span data-ttu-id="ccccd-224">示例 1：交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="ccccd-224">Example 1: Transactions – dynamic period</span></span>

<span data-ttu-id="ccccd-225">下面是一个简单示例，该示例显示**交易记录 - 动态期间**方法的工作原理。</span><span class="sxs-lookup"><span data-stu-id="ccccd-225">Here a simple example that shows how the **Transactions - dynamic period** method works.</span></span>

<span data-ttu-id="ccccd-226">对于本示例，将在主计划中包含以下需求预测。</span><span class="sxs-lookup"><span data-stu-id="ccccd-226">For this example, you include the following demand forecast in a master plan.</span></span>

| <span data-ttu-id="ccccd-227">日期</span><span class="sxs-lookup"><span data-stu-id="ccccd-227">Date</span></span>       | <span data-ttu-id="ccccd-228">需求预测</span><span class="sxs-lookup"><span data-stu-id="ccccd-228">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="ccccd-229">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-229">January 1</span></span>  | <span data-ttu-id="ccccd-230">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-230">1,000</span></span>           |
| <span data-ttu-id="ccccd-231">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-231">February 1</span></span> | <span data-ttu-id="ccccd-232">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-232">1,000</span></span>             |

<span data-ttu-id="ccccd-233">还将创建以下销售订单。</span><span class="sxs-lookup"><span data-stu-id="ccccd-233">You also create the following sales orders.</span></span>

| <span data-ttu-id="ccccd-234">日期</span><span class="sxs-lookup"><span data-stu-id="ccccd-234">Date</span></span>        | <span data-ttu-id="ccccd-235">销售订单数量</span><span class="sxs-lookup"><span data-stu-id="ccccd-235">Sales order quantity</span></span> |
|-------------|----------------------|
| <span data-ttu-id="ccccd-236">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-236">January 15</span></span>  | <span data-ttu-id="ccccd-237">200</span><span class="sxs-lookup"><span data-stu-id="ccccd-237">200</span></span>                  |
| <span data-ttu-id="ccccd-238">2 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-238">February 15</span></span> | <span data-ttu-id="ccccd-239">400</span><span class="sxs-lookup"><span data-stu-id="ccccd-239">400</span></span>                  |

<span data-ttu-id="ccccd-240">在此案例中，将创建以下计划订单。</span><span class="sxs-lookup"><span data-stu-id="ccccd-240">In this case, the following planned orders are created.</span></span>

| <span data-ttu-id="ccccd-241">需求预测日期</span><span class="sxs-lookup"><span data-stu-id="ccccd-241">Demand forecast date</span></span> | <span data-ttu-id="ccccd-242">数量</span><span class="sxs-lookup"><span data-stu-id="ccccd-242">Quantity</span></span> | <span data-ttu-id="ccccd-243">摘要</span><span class="sxs-lookup"><span data-stu-id="ccccd-243">Explanation</span></span>                           |
|--------------------- |----------|---------------------------------------|
| <span data-ttu-id="ccccd-244">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-244">January 1</span></span>            | <span data-ttu-id="ccccd-245">800</span><span class="sxs-lookup"><span data-stu-id="ccccd-245">800</span></span>      | <span data-ttu-id="ccccd-246">预测需求 (= 1,000 – 200)</span><span class="sxs-lookup"><span data-stu-id="ccccd-246">Forecast requirements (= 1,000 – 200)</span></span> |
| <span data-ttu-id="ccccd-247">1 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-247">January 15</span></span>           | <span data-ttu-id="ccccd-248">200</span><span class="sxs-lookup"><span data-stu-id="ccccd-248">200</span></span>      | <span data-ttu-id="ccccd-249">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="ccccd-249">Sales orders requirements</span></span>             |
| <span data-ttu-id="ccccd-250">2 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-250">February 1</span></span>           | <span data-ttu-id="ccccd-251">600</span><span class="sxs-lookup"><span data-stu-id="ccccd-251">600</span></span>      | <span data-ttu-id="ccccd-252">预测需求 (= 1,000 – 400)</span><span class="sxs-lookup"><span data-stu-id="ccccd-252">Forecast requirements (= 1,000 – 400)</span></span> |
| <span data-ttu-id="ccccd-253">2 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-253">February 15</span></span>          | <span data-ttu-id="ccccd-254">400</span><span class="sxs-lookup"><span data-stu-id="ccccd-254">400</span></span>      | <span data-ttu-id="ccccd-255">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="ccccd-255">Sales orders requirements</span></span>             |

#### <a name="example-2-transactions--dynamic-period"></a><span data-ttu-id="ccccd-256">示例 2：交易记录 - 动态期间</span><span class="sxs-lookup"><span data-stu-id="ccccd-256">Example 2: Transactions – dynamic period</span></span>

<span data-ttu-id="ccccd-257">在大多数情况下，会设置系统以使交易记录在特定预测期间减少需求预测：周、月，等等。</span><span class="sxs-lookup"><span data-stu-id="ccccd-257">In most cases, systems are set up so that transactions reduce demand forecast in specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="ccccd-258">这些期间是在缩减参数中定义的。</span><span class="sxs-lookup"><span data-stu-id="ccccd-258">These periods are defined in the reduction key.</span></span> <span data-ttu-id="ccccd-259">但是，两个需求预测行之间的时间还可*提示*期间。</span><span class="sxs-lookup"><span data-stu-id="ccccd-259">However, the time between two demand forecast lines can also *imply* a period.</span></span>

<span data-ttu-id="ccccd-260">对于此示例，将为以下日期和数量创建需求预测。</span><span class="sxs-lookup"><span data-stu-id="ccccd-260">For this example, you create a demand forecast for the following dates and quantities.</span></span>

| <span data-ttu-id="ccccd-261">日期</span><span class="sxs-lookup"><span data-stu-id="ccccd-261">Date</span></span>       | <span data-ttu-id="ccccd-262">需求预测</span><span class="sxs-lookup"><span data-stu-id="ccccd-262">Demand forecast</span></span> |
|------------|-----------------|
| <span data-ttu-id="ccccd-263">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-263">January 1</span></span>  | <span data-ttu-id="ccccd-264">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-264">1,000</span></span>           |
| <span data-ttu-id="ccccd-265">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-265">January 5</span></span>  | <span data-ttu-id="ccccd-266">500</span><span class="sxs-lookup"><span data-stu-id="ccccd-266">500</span></span>             |
| <span data-ttu-id="ccccd-267">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-267">January 12</span></span> | <span data-ttu-id="ccccd-268">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-268">1,000</span></span>           |

<span data-ttu-id="ccccd-269">请注意，在此预测中，预测日期之间没有清晰的间隔。</span><span class="sxs-lookup"><span data-stu-id="ccccd-269">Notice that, in this forecast, there isn't a clear period between the forecast dates.</span></span> <span data-ttu-id="ccccd-270">第一个和第二个日期之间的间隔为四天，第二个和第三个日期之间的间隔为七天。</span><span class="sxs-lookup"><span data-stu-id="ccccd-270">Between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="ccccd-271">这些间隔就是动态期间。</span><span class="sxs-lookup"><span data-stu-id="ccccd-271">These spans are the dynamic periods.</span></span>

<span data-ttu-id="ccccd-272">还将创建以下销售订单行。</span><span class="sxs-lookup"><span data-stu-id="ccccd-272">You also create the following sales order lines.</span></span>

| <span data-ttu-id="ccccd-273">日期</span><span class="sxs-lookup"><span data-stu-id="ccccd-273">Date</span></span>                             | <span data-ttu-id="ccccd-274">销售订单数量</span><span class="sxs-lookup"><span data-stu-id="ccccd-274">Sales order quantity</span></span> |
|----------------------------------|----------------------|
| <span data-ttu-id="ccccd-275">上一年度的 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-275">December 15 in the previous year</span></span> | <span data-ttu-id="ccccd-276">500</span><span class="sxs-lookup"><span data-stu-id="ccccd-276">500</span></span>                  |
| <span data-ttu-id="ccccd-277">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-277">January 3</span></span>                        | <span data-ttu-id="ccccd-278">100</span><span class="sxs-lookup"><span data-stu-id="ccccd-278">100</span></span>                  |
| <span data-ttu-id="ccccd-279">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-279">January 10</span></span>                       | <span data-ttu-id="ccccd-280">200</span><span class="sxs-lookup"><span data-stu-id="ccccd-280">200</span></span>                  |

<span data-ttu-id="ccccd-281">在此案例中，将以下面的方式缩减预测：</span><span class="sxs-lookup"><span data-stu-id="ccccd-281">In this case, the forecast is reduced in the following manner:</span></span>

- <span data-ttu-id="ccccd-282">因为第一个销售订单不在任何期间，因此不会缩减任何预测。</span><span class="sxs-lookup"><span data-stu-id="ccccd-282">Because the first sales order isn't in any period, it doesn't reduce any forecast.</span></span>
- <span data-ttu-id="ccccd-283">因为第二个销售订单是从 1 月 1 日到 1 月 5 日，因此它会将 1 月 1 日的预测缩减 100。</span><span class="sxs-lookup"><span data-stu-id="ccccd-283">Because the second sales order is between January 1 and January 5, it reduces the forecast for January 1 by 100.</span></span>
- <span data-ttu-id="ccccd-284">因为第三个销售订单是从 5 月 5 日到 5 月 12 日，因此它会将 5 月 5 日的预测缩减 200。</span><span class="sxs-lookup"><span data-stu-id="ccccd-284">Because the third sales order is between January 5 and January 12, it reduces the forecast for January 5 by 200.</span></span>

<span data-ttu-id="ccccd-285">因此，将创建以下计划订单。</span><span class="sxs-lookup"><span data-stu-id="ccccd-285">Therefore, the following planned orders are created.</span></span>

| <span data-ttu-id="ccccd-286">需求预测日期</span><span class="sxs-lookup"><span data-stu-id="ccccd-286">Demand forecast date</span></span>             | <span data-ttu-id="ccccd-287">数量</span><span class="sxs-lookup"><span data-stu-id="ccccd-287">Quantity</span></span> | <span data-ttu-id="ccccd-288">摘要</span><span class="sxs-lookup"><span data-stu-id="ccccd-288">Explanation</span></span>                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| <span data-ttu-id="ccccd-289">上一年度的 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-289">December 15 in the previous year</span></span> | <span data-ttu-id="ccccd-290">500</span><span class="sxs-lookup"><span data-stu-id="ccccd-290">500</span></span>      | <span data-ttu-id="ccccd-291">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="ccccd-291">Sales order requirements</span></span>                                            |
| <span data-ttu-id="ccccd-292">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-292">January 1</span></span>                        | <span data-ttu-id="ccccd-293">900</span><span class="sxs-lookup"><span data-stu-id="ccccd-293">900</span></span>      | <span data-ttu-id="ccccd-294">预测需求期间 1 月 1 日到 1 月 5 日 (= 1,000 – 100)</span><span class="sxs-lookup"><span data-stu-id="ccccd-294">Forecast requirements period January 1 to January 5 (= 1,000 – 100)</span></span> |
| <span data-ttu-id="ccccd-295">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-295">January 3</span></span>                        | <span data-ttu-id="ccccd-296">100</span><span class="sxs-lookup"><span data-stu-id="ccccd-296">100</span></span>      | <span data-ttu-id="ccccd-297">销售订单需求</span><span class="sxs-lookup"><span data-stu-id="ccccd-297">Sales order requirements</span></span>                                            |
| <span data-ttu-id="ccccd-298">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-298">January 5</span></span>                        | <span data-ttu-id="ccccd-299">300</span><span class="sxs-lookup"><span data-stu-id="ccccd-299">300</span></span>      | <span data-ttu-id="ccccd-300">预测需求期间 1 月 5 日到 1 月 10 日 (= 500 – 200)</span><span class="sxs-lookup"><span data-stu-id="ccccd-300">Forecast requirements period January 5 to January 10 (= 500 – 200)</span></span>  |
| <span data-ttu-id="ccccd-301">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="ccccd-301">January 12</span></span>                       | <span data-ttu-id="ccccd-302">1,000</span><span class="sxs-lookup"><span data-stu-id="ccccd-302">1,000</span></span>    | <span data-ttu-id="ccccd-303">预测需求期间 1 月 12 日到月底</span><span class="sxs-lookup"><span data-stu-id="ccccd-303">Forecast requirements period January 12 to end</span></span>                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a><span data-ttu-id="ccccd-304">创建和设置预测缩减参数</span><span class="sxs-lookup"><span data-stu-id="ccccd-304">Create and set up a forecast reduction key</span></span>

<span data-ttu-id="ccccd-305">用于缩减预测需求的**交易记录 - 缩减参数**和**百分比- 缩减参数**方法中使用预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="ccccd-305">A forecast reduction key is used in the **Transactions - reduction key** and **Percent- reduction key** methods for reducing forecast requirements.</span></span> <span data-ttu-id="ccccd-306">若要创建和设置缩减参数，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="ccccd-306">Follow these steps to create and set up a reduction key.</span></span>

1. <span data-ttu-id="ccccd-307">转到**主计划 \> 设置 \> 覆盖范围 \> 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="ccccd-307">Go to **Master planning \> Setup \> Coverage \> Reduction keys**.</span></span>
2. <span data-ttu-id="ccccd-308">选择**新建**或按 **Ctrl+N** 创建一个缩减参数。</span><span class="sxs-lookup"><span data-stu-id="ccccd-308">Select **New** or press **Ctrl+N** to create a reduction key.</span></span>
3. <span data-ttu-id="ccccd-309">在**缩减参数**字段中，输入预测缩减参数的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="ccccd-309">In the **Reduction key** field, enter a unique identifier for the forecast reduction key.</span></span> <span data-ttu-id="ccccd-310">然后在**名称**字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="ccccd-310">Then, in the **Name** field, enter a name.</span></span> 
4. <span data-ttu-id="ccccd-311">定义期间和每个期间中的缩减参数百分比：</span><span class="sxs-lookup"><span data-stu-id="ccccd-311">Define the periods and the reduction key percentage in each period:</span></span>

    - <span data-ttu-id="ccccd-312">**生效日期**字段指示开始创建期间的日期。</span><span class="sxs-lookup"><span data-stu-id="ccccd-312">The **Effective date** field indicates the date when creation of the periods starts.</span></span> <span data-ttu-id="ccccd-313">如果**使用生效日期**选项设置为**是**，期间将在生效日期开始。</span><span class="sxs-lookup"><span data-stu-id="ccccd-313">When the **Use the effective date** option is set to **Yes**, the periods start on the effective date.</span></span> <span data-ttu-id="ccccd-314">如果设置为**否**，期间将在运行主计划的日期开始。</span><span class="sxs-lookup"><span data-stu-id="ccccd-314">When it's set to **No**, the periods start on the date when master planning is run.</span></span>
    - <span data-ttu-id="ccccd-315">定义应进行预测缩减的期间。</span><span class="sxs-lookup"><span data-stu-id="ccccd-315">Define the periods that the forecast reduction should occur during.</span></span>
    - <span data-ttu-id="ccccd-316">为具体期间指定应缩减预测需求的百分比。</span><span class="sxs-lookup"><span data-stu-id="ccccd-316">For a specific period, specify the percentages that the forecast requirements should be reduced by.</span></span> <span data-ttu-id="ccccd-317">您可以输入正值以减少需求，或输入负值增加需求。</span><span class="sxs-lookup"><span data-stu-id="ccccd-317">You can enter positive values to decrease requirements or negative values to increase requirements.</span></span>

## <a name="use-a-reduction-key"></a><span data-ttu-id="ccccd-318">使用一个缩减参数</span><span class="sxs-lookup"><span data-stu-id="ccccd-318">Use a reduction key</span></span>

<span data-ttu-id="ccccd-319">必须为物料的覆盖范围组分配预测缩减参数。</span><span class="sxs-lookup"><span data-stu-id="ccccd-319">A forecast reduction key must be assigned to the coverage group of the item.</span></span> <span data-ttu-id="ccccd-320">若要为物料的覆盖范围组分配缩减参数，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="ccccd-320">Follow these steps to assign a reduction key to an item's coverage group.</span></span>

1. <span data-ttu-id="ccccd-321">转至**主计划 \> 设置 \> 覆盖范围 \> 覆盖范围组**。</span><span class="sxs-lookup"><span data-stu-id="ccccd-321">Go to **Master planning \> Setup \> Coverage \> Coverage groups**.</span></span>
2. <span data-ttu-id="ccccd-322">在**其他**快速选项卡上的**缩减参数**字段中，选择缩减参数分配给覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="ccccd-322">On the **Other** FastTab, in the **Reduction key** field, select the reduction key to assign to the coverage group.</span></span> <span data-ttu-id="ccccd-323">缩减参数然后运用于属于该覆盖范围组的所有物料。</span><span class="sxs-lookup"><span data-stu-id="ccccd-323">The reduction key then applies to all items that belong to the coverage group.</span></span>
3. <span data-ttu-id="ccccd-324">在主计划编制期间，若要使用缩减参数计算预测缩减，必须在设置预测计划或主计划时定义此设置。</span><span class="sxs-lookup"><span data-stu-id="ccccd-324">To use a reduction key to calculate forecast reduction during master scheduling, you must define this setting in the setup of the forecast plan or the master plan.</span></span> <span data-ttu-id="ccccd-325">转至以下位置之一：</span><span class="sxs-lookup"><span data-stu-id="ccccd-325">Go to one of the following locations:</span></span>

    - <span data-ttu-id="ccccd-326">主计划 \> 设置 \> 计划 \> 预测计划</span><span class="sxs-lookup"><span data-stu-id="ccccd-326">Master planning \> Setup \> Plans \> Forecast plans</span></span>
    - <span data-ttu-id="ccccd-327">主计划 \> 设置 \> 计划 \> 主计划</span><span class="sxs-lookup"><span data-stu-id="ccccd-327">Master planning \> Setup \> Plans \> Master plans</span></span>

4. <span data-ttu-id="ccccd-328">在**预测计划**或**主计划**页面**常规**快速选项卡上的**用于减少预测需求的方法**字段中，选择**百分比 - 缩减参数**或**交易记录 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="ccccd-328">On the **Forecast plans** or **Master plans** page, on the **General** FastTab, in the **Method used to reduce forecast requirements** field, select either **Percent - reduction key** or **Transactions - reduction key**.</span></span>

## <a name="reduce-a-forecast-by-transactions"></a><span data-ttu-id="ccccd-329">按交易记录缩减预测</span><span class="sxs-lookup"><span data-stu-id="ccccd-329">Reduce a forecast by transactions</span></span>

<span data-ttu-id="ccccd-330">如果用于缩减预测需求的方法选择**交易记录 - 缩减参数**或**交易记录 - 动态期间**，则可指定哪些交易记录缩减预测。</span><span class="sxs-lookup"><span data-stu-id="ccccd-330">When you select **Transactions - reduction key** or **Transactions - dynamic period** as the method for reducing forecast requirements, you can specify which transactions reduce the forecast.</span></span> <span data-ttu-id="ccccd-331">如果所有交易记录均应缩减预测，请在**已发布产品**页面**其他**快速选项卡上的**预测减少依据**字段中选择**所有交易记录**，如果只有销售订单才应缩减预测，请选择**订单**。</span><span class="sxs-lookup"><span data-stu-id="ccccd-331">On the **Released products** page, on the **Other** FastTab, in the **Reduce forecast by** field, select **All transactions** if all transactions should reduce the forecast or **Orders** if only sales orders should reduce the forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ccccd-332">其他资源</span><span class="sxs-lookup"><span data-stu-id="ccccd-332">Additional resources</span></span>

[<span data-ttu-id="ccccd-333">主计划</span><span class="sxs-lookup"><span data-stu-id="ccccd-333">Master plans</span></span>](master-plans.md)
