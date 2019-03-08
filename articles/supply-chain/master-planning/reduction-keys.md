---
title: 缩减参数
description: 文本提供显示如何设置缩减参数的示例。 它包含有关各种缩减参数设置以及每个结果的信息。 可以使用缩减参数以定义如何缩减预测需求。
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: 3e62431a1fdbeb81dda68297f034ee00adece079
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "364802"
---
# <a name="reduction-keys"></a><span data-ttu-id="60663-105">缩减参数</span><span class="sxs-lookup"><span data-stu-id="60663-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60663-106">文本提供显示如何设置缩减参数的示例。</span><span class="sxs-lookup"><span data-stu-id="60663-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="60663-107">它包含有关各种缩减参数设置以及每个结果的信息。</span><span class="sxs-lookup"><span data-stu-id="60663-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="60663-108">可以使用缩减参数以定义如何缩减预测需求。</span><span class="sxs-lookup"><span data-stu-id="60663-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="60663-109">示例 1：百分比 - 缩减参数预测缩减原则</span><span class="sxs-lookup"><span data-stu-id="60663-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="60663-110">此示例显示由缩减参数如何根据由缩减参数定义的百分比和期间缩减需求预测要求。</span><span class="sxs-lookup"><span data-stu-id="60663-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="60663-111">在**缩减参数**页上，设置以下行。</span><span class="sxs-lookup"><span data-stu-id="60663-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="60663-112">找零</span><span class="sxs-lookup"><span data-stu-id="60663-112">Change</span></span> | <span data-ttu-id="60663-113">单位</span><span class="sxs-lookup"><span data-stu-id="60663-113">Unit</span></span>  | <span data-ttu-id="60663-114">百分比</span><span class="sxs-lookup"><span data-stu-id="60663-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="60663-115">1</span><span class="sxs-lookup"><span data-stu-id="60663-115">1</span></span>    | <span data-ttu-id="60663-116">月</span><span class="sxs-lookup"><span data-stu-id="60663-116">Month</span></span> |   <span data-ttu-id="60663-117">100</span><span class="sxs-lookup"><span data-stu-id="60663-117">100</span></span>   |
   |   <span data-ttu-id="60663-118">2</span><span class="sxs-lookup"><span data-stu-id="60663-118">2</span></span>    | <span data-ttu-id="60663-119">月</span><span class="sxs-lookup"><span data-stu-id="60663-119">Month</span></span> |   <span data-ttu-id="60663-120">75</span><span class="sxs-lookup"><span data-stu-id="60663-120">75</span></span>    |
   |   <span data-ttu-id="60663-121">3</span><span class="sxs-lookup"><span data-stu-id="60663-121">3</span></span>    | <span data-ttu-id="60663-122">月</span><span class="sxs-lookup"><span data-stu-id="60663-122">Month</span></span> |   <span data-ttu-id="60663-123">50</span><span class="sxs-lookup"><span data-stu-id="60663-123">50</span></span>    |
   |   <span data-ttu-id="60663-124">4</span><span class="sxs-lookup"><span data-stu-id="60663-124">4</span></span>    | <span data-ttu-id="60663-125">月</span><span class="sxs-lookup"><span data-stu-id="60663-125">Month</span></span> |   <span data-ttu-id="60663-126">25</span><span class="sxs-lookup"><span data-stu-id="60663-126">25</span></span>    |


2. <span data-ttu-id="60663-127">链接缩减参数至物料的覆盖范围组。</span><span class="sxs-lookup"><span data-stu-id="60663-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="60663-128">在**主计划**页上，在**缩减原则**字段中，选择**百分比 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="60663-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="60663-129">创建每月 1,000 份的需求预测。</span><span class="sxs-lookup"><span data-stu-id="60663-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="60663-130">如果在 1 月 1 日运行预测计划编制，则将根据您在**缩减参数**页上设置的百分比来消耗销售预测需求。</span><span class="sxs-lookup"><span data-stu-id="60663-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="60663-131">以下需求数量将转移到主计划。</span><span class="sxs-lookup"><span data-stu-id="60663-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="60663-132">月</span><span class="sxs-lookup"><span data-stu-id="60663-132">Month</span></span>                | <span data-ttu-id="60663-133">所需的份数</span><span class="sxs-lookup"><span data-stu-id="60663-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="60663-134">一月</span><span class="sxs-lookup"><span data-stu-id="60663-134">January</span></span>              | <span data-ttu-id="60663-135">0</span><span class="sxs-lookup"><span data-stu-id="60663-135">0</span></span>                         |
| <span data-ttu-id="60663-136">二月</span><span class="sxs-lookup"><span data-stu-id="60663-136">February</span></span>             | <span data-ttu-id="60663-137">250</span><span class="sxs-lookup"><span data-stu-id="60663-137">250</span></span>                       |
| <span data-ttu-id="60663-138">三月</span><span class="sxs-lookup"><span data-stu-id="60663-138">March</span></span>                | <span data-ttu-id="60663-139">500</span><span class="sxs-lookup"><span data-stu-id="60663-139">500</span></span>                       |
| <span data-ttu-id="60663-140">四月</span><span class="sxs-lookup"><span data-stu-id="60663-140">April</span></span>                | <span data-ttu-id="60663-141">750</span><span class="sxs-lookup"><span data-stu-id="60663-141">750</span></span>                       |
| <span data-ttu-id="60663-142">五月到十二月</span><span class="sxs-lookup"><span data-stu-id="60663-142">May through December</span></span> | <span data-ttu-id="60663-143">1,000</span><span class="sxs-lookup"><span data-stu-id="60663-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="60663-144">示例 2：交易记录 - 缩减参数预测缩减原则</span><span class="sxs-lookup"><span data-stu-id="60663-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="60663-145">此示例显示如何实际订单，这将在由缩减参数和缩减需求预测要求定义的期间发生。</span><span class="sxs-lookup"><span data-stu-id="60663-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="60663-146">在**主计划**页上，在**缩减原则**字段中，选择**交易记录 - 缩减参数**。</span><span class="sxs-lookup"><span data-stu-id="60663-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="60663-147">1 月 1 日存在以下销售订单。</span><span class="sxs-lookup"><span data-stu-id="60663-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="60663-148">月</span><span class="sxs-lookup"><span data-stu-id="60663-148">Month</span></span>    | <span data-ttu-id="60663-149">订购的份数</span><span class="sxs-lookup"><span data-stu-id="60663-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="60663-150">一月</span><span class="sxs-lookup"><span data-stu-id="60663-150">January</span></span>  | <span data-ttu-id="60663-151">956</span><span class="sxs-lookup"><span data-stu-id="60663-151">956</span></span>                      |
| <span data-ttu-id="60663-152">二月</span><span class="sxs-lookup"><span data-stu-id="60663-152">February</span></span> | <span data-ttu-id="60663-153">1,176</span><span class="sxs-lookup"><span data-stu-id="60663-153">1,176</span></span>                    |
| <span data-ttu-id="60663-154">三月</span><span class="sxs-lookup"><span data-stu-id="60663-154">March</span></span>    | <span data-ttu-id="60663-155">451</span><span class="sxs-lookup"><span data-stu-id="60663-155">451</span></span>                      |
| <span data-ttu-id="60663-156">四月</span><span class="sxs-lookup"><span data-stu-id="60663-156">April</span></span>    | <span data-ttu-id="60663-157">119</span><span class="sxs-lookup"><span data-stu-id="60663-157">119</span></span>                      |

<span data-ttu-id="60663-158">如果您使用每月 1,000 份的相同需求预测，将向主计划转移以下需求数量。</span><span class="sxs-lookup"><span data-stu-id="60663-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="60663-159">月</span><span class="sxs-lookup"><span data-stu-id="60663-159">Month</span></span>                | <span data-ttu-id="60663-160">所需的份数</span><span class="sxs-lookup"><span data-stu-id="60663-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="60663-161">一月</span><span class="sxs-lookup"><span data-stu-id="60663-161">January</span></span>              | <span data-ttu-id="60663-162">44</span><span class="sxs-lookup"><span data-stu-id="60663-162">44</span></span>                        |
| <span data-ttu-id="60663-163">二月</span><span class="sxs-lookup"><span data-stu-id="60663-163">February</span></span>             | <span data-ttu-id="60663-164">0</span><span class="sxs-lookup"><span data-stu-id="60663-164">0</span></span>                         |
| <span data-ttu-id="60663-165">三月</span><span class="sxs-lookup"><span data-stu-id="60663-165">March</span></span>                | <span data-ttu-id="60663-166">549</span><span class="sxs-lookup"><span data-stu-id="60663-166">549</span></span>                       |
| <span data-ttu-id="60663-167">四月</span><span class="sxs-lookup"><span data-stu-id="60663-167">April</span></span>                | <span data-ttu-id="60663-168">881</span><span class="sxs-lookup"><span data-stu-id="60663-168">881</span></span>                       |
| <span data-ttu-id="60663-169">五月到十二月</span><span class="sxs-lookup"><span data-stu-id="60663-169">May through December</span></span> | <span data-ttu-id="60663-170">1,000</span><span class="sxs-lookup"><span data-stu-id="60663-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="60663-171">示例 3：交易记录 - 动态期间预测缩减原则</span><span class="sxs-lookup"><span data-stu-id="60663-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="60663-172">在大多数情况下，会设置系统以使交易记录在特定预测期间减少需求预测：周、月，等等。</span><span class="sxs-lookup"><span data-stu-id="60663-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="60663-173">这些期间是在缩减参数中定义的。</span><span class="sxs-lookup"><span data-stu-id="60663-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="60663-174">但是，两个需求预测行之间的时间还可*提示*期间。</span><span class="sxs-lookup"><span data-stu-id="60663-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="60663-175">为以下日期和数量创建需求预测。</span><span class="sxs-lookup"><span data-stu-id="60663-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="60663-176">日期</span><span class="sxs-lookup"><span data-stu-id="60663-176">Date</span></span>       | <span data-ttu-id="60663-177">需求预测</span><span class="sxs-lookup"><span data-stu-id="60663-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="60663-178">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="60663-178">January 1</span></span>  | <span data-ttu-id="60663-179">1,000</span><span class="sxs-lookup"><span data-stu-id="60663-179">1,000</span></span>           |
   | <span data-ttu-id="60663-180">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="60663-180">January 5</span></span>  | <span data-ttu-id="60663-181">500</span><span class="sxs-lookup"><span data-stu-id="60663-181">500</span></span>             |
   | <span data-ttu-id="60663-182">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="60663-182">January 12</span></span> | <span data-ttu-id="60663-183">1,000</span><span class="sxs-lookup"><span data-stu-id="60663-183">1,000</span></span>           |

   <span data-ttu-id="60663-184">在此预测中，预测日期之间没有明确的期间：在第一个和第二个日期之间有一个四天间隔，在第二个和第三个日期之间有一个七天间隔。</span><span class="sxs-lookup"><span data-stu-id="60663-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="60663-185">这些不同间隔是动态期间。</span><span class="sxs-lookup"><span data-stu-id="60663-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="60663-186">如下所示创建销售订单行。</span><span class="sxs-lookup"><span data-stu-id="60663-186">Create sales order lines as follows.</span></span>
   | <span data-ttu-id="60663-187">日期</span><span class="sxs-lookup"><span data-stu-id="60663-187">Date</span></span>                             | <span data-ttu-id="60663-188">销售订单数量</span><span class="sxs-lookup"><span data-stu-id="60663-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="60663-189">上一年度的 12 月 15 日</span><span class="sxs-lookup"><span data-stu-id="60663-189">December 15 in the previous year</span></span> | <span data-ttu-id="60663-190">500</span><span class="sxs-lookup"><span data-stu-id="60663-190">500</span></span>                  |
   | <span data-ttu-id="60663-191">1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="60663-191">January 3</span></span>                        | <span data-ttu-id="60663-192">100</span><span class="sxs-lookup"><span data-stu-id="60663-192">100</span></span>                  |
   | <span data-ttu-id="60663-193">1 月 10 日</span><span class="sxs-lookup"><span data-stu-id="60663-193">January 10</span></span>                       | <span data-ttu-id="60663-194">200</span><span class="sxs-lookup"><span data-stu-id="60663-194">200</span></span>                  |

<span data-ttu-id="60663-195">预测会减少，如下所示：</span><span class="sxs-lookup"><span data-stu-id="60663-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="60663-196">第一个销售订单不在任何期间内，因此，它不会减少任何预测。</span><span class="sxs-lookup"><span data-stu-id="60663-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="60663-197">第二个销售订单是从 1 月 1 日到 1 月 5 日，因此它会使 1 月 1 日的预测减少 100。</span><span class="sxs-lookup"><span data-stu-id="60663-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="60663-198">第三个销售订单是从 1 月 5 日到 1 月 12 日，因此它会使 1 月 5 日的预测减少 200。</span><span class="sxs-lookup"><span data-stu-id="60663-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="60663-199">将创建以下计划订单，以执行预测。</span><span class="sxs-lookup"><span data-stu-id="60663-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="60663-200">需求预测日期</span><span class="sxs-lookup"><span data-stu-id="60663-200">Demand forecast date</span></span> | <span data-ttu-id="60663-201">已缩减数量</span><span class="sxs-lookup"><span data-stu-id="60663-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="60663-202">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="60663-202">January 1</span></span>            | <span data-ttu-id="60663-203">900</span><span class="sxs-lookup"><span data-stu-id="60663-203">900</span></span>              |
| <span data-ttu-id="60663-204">1 月 5 日</span><span class="sxs-lookup"><span data-stu-id="60663-204">January 5</span></span>            | <span data-ttu-id="60663-205">300</span><span class="sxs-lookup"><span data-stu-id="60663-205">300</span></span>              |
| <span data-ttu-id="60663-206">1 月 12 日</span><span class="sxs-lookup"><span data-stu-id="60663-206">January 12</span></span>           | <span data-ttu-id="60663-207">1,000</span><span class="sxs-lookup"><span data-stu-id="60663-207">1,000</span></span>            |

<span data-ttu-id="60663-208">下面是**交易记录 - 动态期间**缩减的汇总：</span><span class="sxs-lookup"><span data-stu-id="60663-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="60663-209">预测需求是按在动态期间发生的实际订单交易记录缩减的。</span><span class="sxs-lookup"><span data-stu-id="60663-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="60663-210">动态期间涵盖当前预测日期，并在下一预测开始时结束。</span><span class="sxs-lookup"><span data-stu-id="60663-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="60663-211">此方法不使用也不需要缩减参数。</span><span class="sxs-lookup"><span data-stu-id="60663-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="60663-212">在使用此选项时，会发生以下行为：</span><span class="sxs-lookup"><span data-stu-id="60663-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="60663-213">如果预测完全减少，则当前预测的预测需求变为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="60663-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="60663-214">如果没有将来的预测，则最后一个输入的预测的预测需求会缩减。</span><span class="sxs-lookup"><span data-stu-id="60663-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="60663-215">时限包括在缩减预测计算中。</span><span class="sxs-lookup"><span data-stu-id="60663-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="60663-216">正天数包括在缩减预测计算中。</span><span class="sxs-lookup"><span data-stu-id="60663-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="60663-217">如果实际订单交易记录超过预测的需求，则其余的交易记录不会前进到下一预测期间。</span><span class="sxs-lookup"><span data-stu-id="60663-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="60663-218">其他资源</span><span class="sxs-lookup"><span data-stu-id="60663-218">Additional resources</span></span>
--------

[<span data-ttu-id="60663-219">主计划</span><span class="sxs-lookup"><span data-stu-id="60663-219">Master plans</span></span>](master-plans.md)



