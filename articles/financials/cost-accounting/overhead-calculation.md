---
title: "开销计算"
description: "此主题描述计算和分配间接成本的典型流程。"
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 549e9b4b073a4e93dd3a1dd52dd6f43e7420a31b
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="167e2-103">开销计算</span><span class="sxs-lookup"><span data-stu-id="167e2-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="167e2-104">此主题描述计算和分配间接成本的典型流程。</span><span class="sxs-lookup"><span data-stu-id="167e2-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="167e2-105">术语定义</span><span class="sxs-lookup"><span data-stu-id="167e2-105">Term definition</span></span>
---------------

<span data-ttu-id="167e2-106">间接成本是为业务运营支出的成本，但是不能直接归为任何具体的业务活动、产品或服务。</span><span class="sxs-lookup"><span data-stu-id="167e2-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="167e2-107">间接成本为营利活动的生成提供重要支持。</span><span class="sxs-lookup"><span data-stu-id="167e2-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="167e2-108">以下是一些开销成本示例：</span><span class="sxs-lookup"><span data-stu-id="167e2-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="167e2-109">租金</span><span class="sxs-lookup"><span data-stu-id="167e2-109">Rent</span></span>
-   <span data-ttu-id="167e2-110">电</span><span class="sxs-lookup"><span data-stu-id="167e2-110">Electricity</span></span>
-   <span data-ttu-id="167e2-111">管理薪金</span><span class="sxs-lookup"><span data-stu-id="167e2-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="167e2-112">开销计算概览</span><span class="sxs-lookup"><span data-stu-id="167e2-112">Overhead calculation overview</span></span>
<span data-ttu-id="167e2-113">开销计算按正确顺序运行会计政策。</span><span class="sxs-lookup"><span data-stu-id="167e2-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="167e2-114">如果成本核算政策更改或检测到特定错误，您可以为同一个会计期间多次运行开销计算。</span><span class="sxs-lookup"><span data-stu-id="167e2-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="167e2-115">每次运行的开销计算将被存储并收到唯一版本 ID，让您可以比较各个版本的计算。</span><span class="sxs-lookup"><span data-stu-id="167e2-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="167e2-116">开销计算生成的成本条目接收会计日期。</span><span class="sxs-lookup"><span data-stu-id="167e2-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="167e2-117">此会计日期与计算中使用的会计期间的结束日期一致。</span><span class="sxs-lookup"><span data-stu-id="167e2-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="167e2-118">唯一版本 ID 由以下元素组成：</span><span class="sxs-lookup"><span data-stu-id="167e2-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="167e2-119">版本类型</span><span class="sxs-lookup"><span data-stu-id="167e2-119">Version type</span></span>
-   <span data-ttu-id="167e2-120">日期和时间</span><span class="sxs-lookup"><span data-stu-id="167e2-120">Date and time</span></span>
-   <span data-ttu-id="167e2-121">成本核算分类帐</span><span class="sxs-lookup"><span data-stu-id="167e2-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="167e2-122">会计年度</span><span class="sxs-lookup"><span data-stu-id="167e2-122">Fiscal year</span></span>
-   <span data-ttu-id="167e2-123">会计期间</span><span class="sxs-lookup"><span data-stu-id="167e2-123">Fiscal period</span></span>

<span data-ttu-id="167e2-124">开销计算独立于版本运行。</span><span class="sxs-lookup"><span data-stu-id="167e2-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="167e2-125">因此，可以在实际版本前计算预算版本。</span><span class="sxs-lookup"><span data-stu-id="167e2-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="167e2-126">开销计算包括四个步骤，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="167e2-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="167e2-127">在每个步骤中，创建包含日记帐条目的日记帐标头。</span><span class="sxs-lookup"><span data-stu-id="167e2-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="167e2-128">此日记帐标头为每个计算步骤保留输入数据。</span><span class="sxs-lookup"><span data-stu-id="167e2-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="167e2-129">政策和规则应用于每个日记帐行，成本条目生成为输出。</span><span class="sxs-lookup"><span data-stu-id="167e2-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="167e2-130">因此，您始终具有完全的可跟踪性。</span><span class="sxs-lookup"><span data-stu-id="167e2-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="167e2-131">[![开销计算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="167e2-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="167e2-132">计算和分摊电间接成本</span><span class="sxs-lookup"><span data-stu-id="167e2-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="167e2-133">在财务会计中，有些成本（如电）登记为总计。</span><span class="sxs-lookup"><span data-stu-id="167e2-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="167e2-134">因此，不为成本核算提供详细的管理洞察。</span><span class="sxs-lookup"><span data-stu-id="167e2-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="167e2-135">在成本核算中，为提供跨所有组织单位和级别的正确的管理洞察，成本必须流过各个组织单位。</span><span class="sxs-lookup"><span data-stu-id="167e2-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="167e2-136">此流必须基于消耗量的准确记录或公平评估。</span><span class="sxs-lookup"><span data-stu-id="167e2-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="167e2-137">在总帐中，可以过帐电成本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="167e2-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="167e2-138">会计日期</span><span class="sxs-lookup"><span data-stu-id="167e2-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-139">成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-140">主科目</span><span class="sxs-lookup"><span data-stu-id="167e2-140">Main account</span></span></th>
<th><span data-ttu-id="167e2-141">按记帐币种计算的金额</span><span class="sxs-lookup"><span data-stu-id="167e2-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-142">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="167e2-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="167e2-143">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-143">CC099</span></span></td>
<td><span data-ttu-id="167e2-144">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-144">Default cost center</span></span></td>
<td><span data-ttu-id="167e2-145">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-145">10001</span></span></td>
<td><span data-ttu-id="167e2-146">电</span><span class="sxs-lookup"><span data-stu-id="167e2-146">Electricity</span></span></td>
<td><span data-ttu-id="167e2-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="167e2-148">步骤 1：处理成本行为计算</span><span class="sxs-lookup"><span data-stu-id="167e2-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="167e2-149">默认情况下，当成本条目从源数据导入时，它们在成本核算中接收**未分类**成本行为分类。</span><span class="sxs-lookup"><span data-stu-id="167e2-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="167e2-150">通过应用成本行为政策规则，您可以将成本条目重新分类为**固定成本**或**可变成本**。</span><span class="sxs-lookup"><span data-stu-id="167e2-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="167e2-151">定义成本行为规则</span><span class="sxs-lookup"><span data-stu-id="167e2-151">Define the cost behavior rule</span></span>

<span data-ttu-id="167e2-152">在某些情况下，一部分成本是一项固定费用，其余成本基于消耗量。</span><span class="sxs-lookup"><span data-stu-id="167e2-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="167e2-153">通常电费帐单与此定义一致。</span><span class="sxs-lookup"><span data-stu-id="167e2-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="167e2-154">在支付特定固定费用后，您按千瓦时 (Kwh) 支付消耗量。</span><span class="sxs-lookup"><span data-stu-id="167e2-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="167e2-155">例如，如果固定成本费用为 1,000.00，以下是成本行为规则的定义：</span><span class="sxs-lookup"><span data-stu-id="167e2-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="167e2-156">固定金额 1,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="167e2-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="167e2-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="167e2-158">1000,01 &lt; N = 可变</span><span class="sxs-lookup"><span data-stu-id="167e2-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="167e2-159">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="167e2-160">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-160">Journal</span></span></th>
<th><span data-ttu-id="167e2-161">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="167e2-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="167e2-162">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="167e2-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="167e2-163">版本</span><span class="sxs-lookup"><span data-stu-id="167e2-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-164">00001</span><span class="sxs-lookup"><span data-stu-id="167e2-164">00001</span></span></td>
<td><span data-ttu-id="167e2-165">成本行为计算日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="167e2-166">会计</span><span class="sxs-lookup"><span data-stu-id="167e2-166">Fiscal</span></span></td>
<td><span data-ttu-id="167e2-167">2017</span><span class="sxs-lookup"><span data-stu-id="167e2-167">2017</span></span></td>
<td><span data-ttu-id="167e2-168">期间 1</span><span class="sxs-lookup"><span data-stu-id="167e2-168">Period 1</span></span></td>
<td><span data-ttu-id="167e2-169">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="167e2-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="167e2-170">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="167e2-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="167e2-171">会计日期</span><span class="sxs-lookup"><span data-stu-id="167e2-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-172">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-173">成本元素</span><span class="sxs-lookup"><span data-stu-id="167e2-173">Cost element</span></span></th>
<th><span data-ttu-id="167e2-174">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-174">Cost behavior</span></span></th>
<th><span data-ttu-id="167e2-175">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-176">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="167e2-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="167e2-177">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-177">CC099</span></span></td>
<td><span data-ttu-id="167e2-178">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-178">Default cost center</span></span></td>
<td><span data-ttu-id="167e2-179">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-179">10001</span></span></td>
<td><span data-ttu-id="167e2-180">电</span><span class="sxs-lookup"><span data-stu-id="167e2-180">Electricity</span></span></td>
<td><span data-ttu-id="167e2-181">未分类</span><span class="sxs-lookup"><span data-stu-id="167e2-181">Unclassified</span></span></td>
<td><span data-ttu-id="167e2-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="167e2-183">成本条目</span><span class="sxs-lookup"><span data-stu-id="167e2-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-184">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-185">成本元素</span><span class="sxs-lookup"><span data-stu-id="167e2-185">Cost element</span></span></th>
<th><span data-ttu-id="167e2-186">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-186">Cost behavior</span></span></th>
<th><span data-ttu-id="167e2-187">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-187">Amount</span></span></th>
<th><span data-ttu-id="167e2-188">会计日期</span><span class="sxs-lookup"><span data-stu-id="167e2-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-189">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-189">CC099</span></span></td>
<td><span data-ttu-id="167e2-190">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-190">Default cost center</span></span></td>
<td><span data-ttu-id="167e2-191">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-191">10001</span></span></td>
<td><span data-ttu-id="167e2-192">电</span><span class="sxs-lookup"><span data-stu-id="167e2-192">Electricity</span></span></td>
<td><span data-ttu-id="167e2-193">未分类</span><span class="sxs-lookup"><span data-stu-id="167e2-193">Unclassified</span></span></td>
<td><span data-ttu-id="167e2-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-194">10,000.00</span></span></td>
<td><span data-ttu-id="167e2-195">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="167e2-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-196">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-196">CC099</span></span></td>
<td><span data-ttu-id="167e2-197">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-197">Default cost center</span></span></td>
<td><span data-ttu-id="167e2-198">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-198">10001</span></span></td>
<td><span data-ttu-id="167e2-199">电</span><span class="sxs-lookup"><span data-stu-id="167e2-199">Electricity</span></span></td>
<td><span data-ttu-id="167e2-200">未分类</span><span class="sxs-lookup"><span data-stu-id="167e2-200">Unclassified</span></span></td>
<td><span data-ttu-id="167e2-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-201">-10,000.00</span></span></td>
<td><span data-ttu-id="167e2-202">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-203">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-203">CC099</span></span></td>
<td><span data-ttu-id="167e2-204">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-204">Default cost center</span></span></td>
<td><span data-ttu-id="167e2-205">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-205">10001</span></span></td>
<td><span data-ttu-id="167e2-206">电</span><span class="sxs-lookup"><span data-stu-id="167e2-206">Electricity</span></span></td>
<td><span data-ttu-id="167e2-207">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-207">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-208">1,000.00</span></span></td>
<td><span data-ttu-id="167e2-209">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-210">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-210">CC099</span></span></td>
<td><span data-ttu-id="167e2-211">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-211">Default cost center</span></span></td>
<td><span data-ttu-id="167e2-212">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-212">10001</span></span></td>
<td><span data-ttu-id="167e2-213">电</span><span class="sxs-lookup"><span data-stu-id="167e2-213">Electricity</span></span></td>
<td><span data-ttu-id="167e2-214">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-214">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-215">9,000.00</span></span></td>
<td><span data-ttu-id="167e2-216">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-217">有关成本行为的详细信息，请参阅“成本行为政策”。</span><span class="sxs-lookup"><span data-stu-id="167e2-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="167e2-218">（请注意，此主题尚未完成，不过将很快推出。）</span><span class="sxs-lookup"><span data-stu-id="167e2-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="167e2-219">步骤 2：处理成本分配计算</span><span class="sxs-lookup"><span data-stu-id="167e2-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="167e2-220">成本分配用于通过应用相关的分摊基数将成本从一个成本对象重新分配到一个或多个其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="167e2-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="167e2-221">成本分配和成本分摊的不同之处在于，成本分配始终发生在原始成本的主要成本元素级别。</span><span class="sxs-lookup"><span data-stu-id="167e2-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="167e2-222">定义成本分配规则</span><span class="sxs-lookup"><span data-stu-id="167e2-222">Define the cost distribution rule</span></span>

<span data-ttu-id="167e2-223">在财务会计中，电成本通常登记为总计。</span><span class="sxs-lookup"><span data-stu-id="167e2-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="167e2-224">在成本核算中，此方法不足够详细。</span><span class="sxs-lookup"><span data-stu-id="167e2-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="167e2-225">可变成本应公平分配到各个成本对象。</span><span class="sxs-lookup"><span data-stu-id="167e2-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="167e2-226">最合理的分配基础是电的消耗量 (Kwh)。</span><span class="sxs-lookup"><span data-stu-id="167e2-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="167e2-227">创建名为“电”的统计维度成员并记录电的消耗量。</span><span class="sxs-lookup"><span data-stu-id="167e2-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="167e2-228">默认情况下，所有统计维度成员均可作为分配基础。</span><span class="sxs-lookup"><span data-stu-id="167e2-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-229">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-229">Cost object</span></span></th>
<th><span data-ttu-id="167e2-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="167e2-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-231">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-231">CC001</span></span></td>
<td><span data-ttu-id="167e2-232">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-232">HR</span></span></td>
<td><span data-ttu-id="167e2-233">1,000</span><span class="sxs-lookup"><span data-stu-id="167e2-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-234">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-234">CC002</span></span></td>
<td><span data-ttu-id="167e2-235">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-235">Finance</span></span></td>
<td><span data-ttu-id="167e2-236">6,000</span><span class="sxs-lookup"><span data-stu-id="167e2-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-237">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-237">CC003</span></span></td>
<td><span data-ttu-id="167e2-238">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-238">Assembly</span></span></td>
<td><span data-ttu-id="167e2-239">0</span><span class="sxs-lookup"><span data-stu-id="167e2-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-240">下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="167e2-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-241">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-241">Cost object</span></span></th>
<th><span data-ttu-id="167e2-242">度量值</span><span class="sxs-lookup"><span data-stu-id="167e2-242">Magnitude</span></span></th>
<th><span data-ttu-id="167e2-243">分配系数</span><span class="sxs-lookup"><span data-stu-id="167e2-243">Allocation factor</span></span></th>
<th><span data-ttu-id="167e2-244">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-245">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-245">CC001</span></span></td>
<td><span data-ttu-id="167e2-246">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-246">HR</span></span></td>
<td><span data-ttu-id="167e2-247">1,000</span><span class="sxs-lookup"><span data-stu-id="167e2-247">1,000</span></span></td>
<td><span data-ttu-id="167e2-248">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="167e2-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="167e2-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-250">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-250">CC002</span></span></td>
<td><span data-ttu-id="167e2-251">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-251">Finance</span></span></td>
<td><span data-ttu-id="167e2-252">6,000</span><span class="sxs-lookup"><span data-stu-id="167e2-252">6,000</span></span></td>
<td><span data-ttu-id="167e2-253">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="167e2-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="167e2-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-255">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-255">CC003</span></span></td>
<td><span data-ttu-id="167e2-256">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-256">Assembly</span></span></td>
<td><span data-ttu-id="167e2-257">0</span><span class="sxs-lookup"><span data-stu-id="167e2-257">0</span></span></td>
<td><span data-ttu-id="167e2-258">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="167e2-259">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-260">固定成本应平均分配到消耗了电的单个成本对象。</span><span class="sxs-lookup"><span data-stu-id="167e2-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="167e2-261">可以通过在公式分配基础中使用电统计维度成员取得此结果：（电 &gt; 0.00）下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="167e2-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-262">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-262">Cost object</span></span></th>
<th><span data-ttu-id="167e2-263">配方</span><span class="sxs-lookup"><span data-stu-id="167e2-263">Formula</span></span></th>
<th><span data-ttu-id="167e2-264">度量值</span><span class="sxs-lookup"><span data-stu-id="167e2-264">Magnitude</span></span></th>
<th><span data-ttu-id="167e2-265">分配系数</span><span class="sxs-lookup"><span data-stu-id="167e2-265">Allocation factor</span></span></th>
<th><span data-ttu-id="167e2-266">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-267">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-267">CC001</span></span></td>
<td><span data-ttu-id="167e2-268">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-268">HR</span></span></td>
<td><span data-ttu-id="167e2-269">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="167e2-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="167e2-270">1</span><span class="sxs-lookup"><span data-stu-id="167e2-270">1</span></span></td>
<td><span data-ttu-id="167e2-271">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="167e2-272">500.00</span><span class="sxs-lookup"><span data-stu-id="167e2-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-273">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-273">CC002</span></span></td>
<td><span data-ttu-id="167e2-274">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-274">Finance</span></span></td>
<td><span data-ttu-id="167e2-275">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="167e2-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="167e2-276">1</span><span class="sxs-lookup"><span data-stu-id="167e2-276">1</span></span></td>
<td><span data-ttu-id="167e2-277">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="167e2-278">500.00</span><span class="sxs-lookup"><span data-stu-id="167e2-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-279">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-279">CC003</span></span></td>
<td><span data-ttu-id="167e2-280">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-280">Assembly</span></span></td>
<td><span data-ttu-id="167e2-281">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="167e2-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="167e2-282">0</span><span class="sxs-lookup"><span data-stu-id="167e2-282">0</span></span></td>
<td><span data-ttu-id="167e2-283">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="167e2-284">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="167e2-285">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="167e2-286">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-286">Journal</span></span></th>
<th><span data-ttu-id="167e2-287">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="167e2-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="167e2-288">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="167e2-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="167e2-289">版本</span><span class="sxs-lookup"><span data-stu-id="167e2-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-290">00002</span><span class="sxs-lookup"><span data-stu-id="167e2-290">00002</span></span></td>
<td><span data-ttu-id="167e2-291">成本分配计算日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="167e2-292">会计</span><span class="sxs-lookup"><span data-stu-id="167e2-292">Fiscal</span></span></td>
<td><span data-ttu-id="167e2-293">2017</span><span class="sxs-lookup"><span data-stu-id="167e2-293">2017</span></span></td>
<td><span data-ttu-id="167e2-294">期间 1</span><span class="sxs-lookup"><span data-stu-id="167e2-294">Period 1</span></span></td>
<td><span data-ttu-id="167e2-295">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="167e2-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="167e2-296">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="167e2-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="167e2-297">会计日期</span><span class="sxs-lookup"><span data-stu-id="167e2-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-298">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-299">成本元素</span><span class="sxs-lookup"><span data-stu-id="167e2-299">Cost element</span></span></th>
<th><span data-ttu-id="167e2-300">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-300">Cost behavior</span></span></th>
<th><span data-ttu-id="167e2-301">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-302">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-303">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-303">CC099</span></span></td>
<td><span data-ttu-id="167e2-304">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-304">Default cost center</span></span></td>
<td><span data-ttu-id="167e2-305">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-305">10001</span></span></td>
<td><span data-ttu-id="167e2-306">电</span><span class="sxs-lookup"><span data-stu-id="167e2-306">Electricity</span></span></td>
<td><span data-ttu-id="167e2-307">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-307">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-308">1,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-309">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-310">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-310">CC099</span></span></td>
<td><span data-ttu-id="167e2-311">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-311">Default cost center</span></span></td>
<td><span data-ttu-id="167e2-312">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-312">10001</span></span></td>
<td><span data-ttu-id="167e2-313">电</span><span class="sxs-lookup"><span data-stu-id="167e2-313">Electricity</span></span></td>
<td><span data-ttu-id="167e2-314">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-314">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="167e2-316">成本条目</span><span class="sxs-lookup"><span data-stu-id="167e2-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-317">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-318">成本元素</span><span class="sxs-lookup"><span data-stu-id="167e2-318">Cost element</span></span></th>
<th><span data-ttu-id="167e2-319">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-319">Cost behavior</span></span></th>
<th><span data-ttu-id="167e2-320">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-320">Amount</span></span></th>
<th><span data-ttu-id="167e2-321">会计日期</span><span class="sxs-lookup"><span data-stu-id="167e2-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-322">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-322">CC099</span></span></td>
<td><span data-ttu-id="167e2-323">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-323">Default cost center</span></span></td>
<td><span data-ttu-id="167e2-324">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-324">10001</span></span></td>
<td><span data-ttu-id="167e2-325">电</span><span class="sxs-lookup"><span data-stu-id="167e2-325">Electricity</span></span></td>
<td><span data-ttu-id="167e2-326">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-326">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-327">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-327">-1,000.00</span></span></td>
<td><span data-ttu-id="167e2-328">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-329">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-329">CC001</span></span></td>
<td><span data-ttu-id="167e2-330">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-330">HR</span></span></td>
<td><span data-ttu-id="167e2-331">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-331">10001</span></span></td>
<td><span data-ttu-id="167e2-332">电</span><span class="sxs-lookup"><span data-stu-id="167e2-332">Electricity</span></span></td>
<td><span data-ttu-id="167e2-333">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-333">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-334">500.00</span><span class="sxs-lookup"><span data-stu-id="167e2-334">500.00</span></span></td>
<td><span data-ttu-id="167e2-335">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-336">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-336">CC002</span></span></td>
<td><span data-ttu-id="167e2-337">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-337">Finance</span></span></td>
<td><span data-ttu-id="167e2-338">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-338">10001</span></span></td>
<td><span data-ttu-id="167e2-339">电</span><span class="sxs-lookup"><span data-stu-id="167e2-339">Electricity</span></span></td>
<td><span data-ttu-id="167e2-340">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-340">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-341">500.00</span><span class="sxs-lookup"><span data-stu-id="167e2-341">500.00</span></span></td>
<td><span data-ttu-id="167e2-342">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-343">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-343">CC099</span></span></td>
<td><span data-ttu-id="167e2-344">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="167e2-344">Default cost center</span></span></td>
<td><span data-ttu-id="167e2-345">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-345">10001</span></span></td>
<td><span data-ttu-id="167e2-346">电</span><span class="sxs-lookup"><span data-stu-id="167e2-346">Electricity</span></span></td>
<td><span data-ttu-id="167e2-347">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-347">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-348">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="167e2-348">-9,000.00</span></span></td>
<td><span data-ttu-id="167e2-349">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-350">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-350">CC001</span></span></td>
<td><span data-ttu-id="167e2-351">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-351">HR</span></span></td>
<td><span data-ttu-id="167e2-352">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-352">10001</span></span></td>
<td><span data-ttu-id="167e2-353">电</span><span class="sxs-lookup"><span data-stu-id="167e2-353">Electricity</span></span></td>
<td><span data-ttu-id="167e2-354">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-354">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="167e2-355">1,285.71</span></span></td>
<td><span data-ttu-id="167e2-356">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-357">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-357">CC002</span></span></td>
<td><span data-ttu-id="167e2-358">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-358">Finance</span></span></td>
<td><span data-ttu-id="167e2-359">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-359">10001</span></span></td>
<td><span data-ttu-id="167e2-360">电</span><span class="sxs-lookup"><span data-stu-id="167e2-360">Electricity</span></span></td>
<td><span data-ttu-id="167e2-361">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-361">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="167e2-362">7,714.29</span></span></td>
<td><span data-ttu-id="167e2-363">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-364">有关成本分配和分配基础的详细信息，请参阅“成本分配成本”和“分配基础”。</span><span class="sxs-lookup"><span data-stu-id="167e2-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="167e2-365">（请注意，此主题尚未完成，不过将很快推出。）</span><span class="sxs-lookup"><span data-stu-id="167e2-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="167e2-366">步骤 3：处理开销比率计算</span><span class="sxs-lookup"><span data-stu-id="167e2-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="167e2-367">开销比率用于向一个或多个特定成本对象收费。</span><span class="sxs-lookup"><span data-stu-id="167e2-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="167e2-368">费用基于预先确定的成本率和来自指定的分配基础的度量值。</span><span class="sxs-lookup"><span data-stu-id="167e2-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="167e2-369">定义开销比率</span><span class="sxs-lookup"><span data-stu-id="167e2-369">Define the overhead rate</span></span>

<span data-ttu-id="167e2-370">成本对象 CC001 HR 生成一组内部项目。</span><span class="sxs-lookup"><span data-stu-id="167e2-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="167e2-371">创建名为“HR 项目”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="167e2-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-372">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-372">Cost object</span></span></th>
<th><span data-ttu-id="167e2-373">工时</span><span class="sxs-lookup"><span data-stu-id="167e2-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-374">项目 1</span><span class="sxs-lookup"><span data-stu-id="167e2-374">Proj 1</span></span></td>
<td><span data-ttu-id="167e2-375">项目 1</span><span class="sxs-lookup"><span data-stu-id="167e2-375">Project 1</span></span></td>
<td><span data-ttu-id="167e2-376">3</span><span class="sxs-lookup"><span data-stu-id="167e2-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-377">项目 2</span><span class="sxs-lookup"><span data-stu-id="167e2-377">Proj 2</span></span></td>
<td><span data-ttu-id="167e2-378">项目 2</span><span class="sxs-lookup"><span data-stu-id="167e2-378">Project 2</span></span></td>
<td><span data-ttu-id="167e2-379">1</span><span class="sxs-lookup"><span data-stu-id="167e2-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-380">成本项目份额预先确定的成本率已定义。</span><span class="sxs-lookup"><span data-stu-id="167e2-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-381">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-381">Cost object</span></span></th>
<th><span data-ttu-id="167e2-382">成本元素</span><span class="sxs-lookup"><span data-stu-id="167e2-382">Cost element</span></span></th>
<th><span data-ttu-id="167e2-383">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-383">Cost behavior</span></span></th>
<th><span data-ttu-id="167e2-384">单位</span><span class="sxs-lookup"><span data-stu-id="167e2-384">Units</span></span></th>
<th><span data-ttu-id="167e2-385">比率</span><span class="sxs-lookup"><span data-stu-id="167e2-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-386">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-386">CC001</span></span></td>
<td><span data-ttu-id="167e2-387">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-387">HR</span></span></td>
<td><span data-ttu-id="167e2-388">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-388">10001</span></span></td>
<td><span data-ttu-id="167e2-389">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-389">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-390">1</span><span class="sxs-lookup"><span data-stu-id="167e2-390">1</span></span></td>
<td><span data-ttu-id="167e2-391">10</span><span class="sxs-lookup"><span data-stu-id="167e2-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-392">下表显示 HR 项目用作分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="167e2-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-393">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-393">Cost object</span></span></th>
<th><span data-ttu-id="167e2-394">度量值</span><span class="sxs-lookup"><span data-stu-id="167e2-394">Magnitude</span></span></th>
<th><span data-ttu-id="167e2-395">成本元素</span><span class="sxs-lookup"><span data-stu-id="167e2-395">Cost element</span></span></th>
<th><span data-ttu-id="167e2-396">分配系数</span><span class="sxs-lookup"><span data-stu-id="167e2-396">Allocation factor</span></span></th>
<th><span data-ttu-id="167e2-397">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-398">项目 1</span><span class="sxs-lookup"><span data-stu-id="167e2-398">Proj 1</span></span></td>
<td><span data-ttu-id="167e2-399">项目 1</span><span class="sxs-lookup"><span data-stu-id="167e2-399">Project 1</span></span></td>
<td><span data-ttu-id="167e2-400">3</span><span class="sxs-lookup"><span data-stu-id="167e2-400">3</span></span></td>
<td><span data-ttu-id="167e2-401">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-401">10001</span></span></td>
<td><span data-ttu-id="167e2-402">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="167e2-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="167e2-403">30.00</span><span class="sxs-lookup"><span data-stu-id="167e2-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-404">项目 2</span><span class="sxs-lookup"><span data-stu-id="167e2-404">Proj 2</span></span></td>
<td><span data-ttu-id="167e2-405">项目 2</span><span class="sxs-lookup"><span data-stu-id="167e2-405">Project 2</span></span></td>
<td><span data-ttu-id="167e2-406">1</span><span class="sxs-lookup"><span data-stu-id="167e2-406">1</span></span></td>
<td><span data-ttu-id="167e2-407">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-407">10001</span></span></td>
<td><span data-ttu-id="167e2-408">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="167e2-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="167e2-409">10.00</span><span class="sxs-lookup"><span data-stu-id="167e2-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="167e2-410">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="167e2-411">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-411">Journal</span></span></th>
<th><span data-ttu-id="167e2-412">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="167e2-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="167e2-413">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="167e2-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="167e2-414">版本</span><span class="sxs-lookup"><span data-stu-id="167e2-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-415">00003</span><span class="sxs-lookup"><span data-stu-id="167e2-415">00003</span></span></td>
<td><span data-ttu-id="167e2-416">开销比率计算日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="167e2-417">会计</span><span class="sxs-lookup"><span data-stu-id="167e2-417">Fiscal</span></span></td>
<td><span data-ttu-id="167e2-418">2017</span><span class="sxs-lookup"><span data-stu-id="167e2-418">2017</span></span></td>
<td><span data-ttu-id="167e2-419">期间 1</span><span class="sxs-lookup"><span data-stu-id="167e2-419">Period 1</span></span></td>
<td><span data-ttu-id="167e2-420">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="167e2-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="167e2-421">日记帐条目（开销比率计算的日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="167e2-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="167e2-422">会计日期</span><span class="sxs-lookup"><span data-stu-id="167e2-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-423">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-423">Cost object</span></span></th>
<th><span data-ttu-id="167e2-424">度量值</span><span class="sxs-lookup"><span data-stu-id="167e2-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-425">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-426">项目 1</span><span class="sxs-lookup"><span data-stu-id="167e2-426">Proj 1</span></span></td>
<td><span data-ttu-id="167e2-427">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="167e2-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="167e2-428">3.00</span><span class="sxs-lookup"><span data-stu-id="167e2-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-429">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-430">项目 2</span><span class="sxs-lookup"><span data-stu-id="167e2-430">Proj 2</span></span></td>
<td><span data-ttu-id="167e2-431">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="167e2-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="167e2-432">1.00</span><span class="sxs-lookup"><span data-stu-id="167e2-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="167e2-433">成本条目</span><span class="sxs-lookup"><span data-stu-id="167e2-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-434">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-435">成本元素</span><span class="sxs-lookup"><span data-stu-id="167e2-435">Cost element</span></span></th>
<th><span data-ttu-id="167e2-436">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-436">Cost behavior</span></span></th>
<th><span data-ttu-id="167e2-437">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-437">Amount</span></span></th>
<th><span data-ttu-id="167e2-438">会计日期</span><span class="sxs-lookup"><span data-stu-id="167e2-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="167e2-439">CC0001</span></span></td>
<td><span data-ttu-id="167e2-440">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-440">HR</span></span></td>
<td><span data-ttu-id="167e2-441">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-441">10001</span></span></td>
<td><span data-ttu-id="167e2-442">电</span><span class="sxs-lookup"><span data-stu-id="167e2-442">Electricity</span></span></td>
<td><span data-ttu-id="167e2-443">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-443">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-444">-30.00</span><span class="sxs-lookup"><span data-stu-id="167e2-444">-30.00</span></span></td>
<td><span data-ttu-id="167e2-445">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-446">项目 1</span><span class="sxs-lookup"><span data-stu-id="167e2-446">Proj 1</span></span></td>
<td><span data-ttu-id="167e2-447">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="167e2-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="167e2-448">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-448">10001</span></span></td>
<td><span data-ttu-id="167e2-449">电</span><span class="sxs-lookup"><span data-stu-id="167e2-449">Electricity</span></span></td>
<td><span data-ttu-id="167e2-450">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-450">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-451">30.00</span><span class="sxs-lookup"><span data-stu-id="167e2-451">30.00</span></span></td>
<td><span data-ttu-id="167e2-452">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-453">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-453">CC001</span></span></td>
<td><span data-ttu-id="167e2-454">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-454">HR</span></span></td>
<td><span data-ttu-id="167e2-455">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-455">10001</span></span></td>
<td><span data-ttu-id="167e2-456">电</span><span class="sxs-lookup"><span data-stu-id="167e2-456">Electricity</span></span></td>
<td><span data-ttu-id="167e2-457">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-457">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-458">-10.00</span><span class="sxs-lookup"><span data-stu-id="167e2-458">-10.00</span></span></td>
<td><span data-ttu-id="167e2-459">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-460">项目 2</span><span class="sxs-lookup"><span data-stu-id="167e2-460">Proj 2</span></span></td>
<td><span data-ttu-id="167e2-461">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="167e2-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="167e2-462">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-462">10001</span></span></td>
<td><span data-ttu-id="167e2-463">电</span><span class="sxs-lookup"><span data-stu-id="167e2-463">Electricity</span></span></td>
<td><span data-ttu-id="167e2-464">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-464">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-465">10.00</span><span class="sxs-lookup"><span data-stu-id="167e2-465">10.00</span></span></td>
<td><span data-ttu-id="167e2-466">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-467">有关开销比率政策的详细信息，请参阅“开销比率政策”和“分配基础”。</span><span class="sxs-lookup"><span data-stu-id="167e2-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="167e2-468">（请注意，此主题尚未完成，不过将很快推出。）</span><span class="sxs-lookup"><span data-stu-id="167e2-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="167e2-469">步骤 4：处理成本分摊计算</span><span class="sxs-lookup"><span data-stu-id="167e2-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="167e2-470">分摊用于通过应用分配基础将成本对象的余额分配给其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="167e2-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="167e2-471">Finance and Operations 支持互惠分摊方法。</span><span class="sxs-lookup"><span data-stu-id="167e2-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="167e2-472">在互惠分摊方法中，辅助成本对象交换的互助服务被完全识别。</span><span class="sxs-lookup"><span data-stu-id="167e2-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="167e2-473">系统自动确定执行分摊的正确顺序。</span><span class="sxs-lookup"><span data-stu-id="167e2-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="167e2-474">成本对象的余额按单一分配基础分配。</span><span class="sxs-lookup"><span data-stu-id="167e2-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="167e2-475">支持跨成本对象维度及其各自成员的分摊。</span><span class="sxs-lookup"><span data-stu-id="167e2-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="167e2-476">分摊顺序由成本控制单元控制。</span><span class="sxs-lookup"><span data-stu-id="167e2-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="167e2-477">[![互惠方法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="167e2-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="167e2-478">定义成本分摊</span><span class="sxs-lookup"><span data-stu-id="167e2-478">Define the cost allocation</span></span>

<span data-ttu-id="167e2-479">这是说明如何跟踪成本流的简单示例。</span><span class="sxs-lookup"><span data-stu-id="167e2-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="167e2-480">成本对象 CC001 HR 生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="167e2-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="167e2-481">创建名为“HR 服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="167e2-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-482">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-482">Cost object</span></span></th>
<th><span data-ttu-id="167e2-483">HR 服务</span><span class="sxs-lookup"><span data-stu-id="167e2-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-484">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-484">CC002</span></span></td>
<td><span data-ttu-id="167e2-485">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-485">Finance</span></span></td>
<td><span data-ttu-id="167e2-486">35</span><span class="sxs-lookup"><span data-stu-id="167e2-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-487">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-487">CC003</span></span></td>
<td><span data-ttu-id="167e2-488">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-488">Assembly</span></span></td>
<td><span data-ttu-id="167e2-489">55</span><span class="sxs-lookup"><span data-stu-id="167e2-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-490">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-490">CC004</span></span></td>
<td><span data-ttu-id="167e2-491">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-491">Packaging</span></span></td>
<td><span data-ttu-id="167e2-492">10</span><span class="sxs-lookup"><span data-stu-id="167e2-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-493">成本对象 CC002 财务生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="167e2-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="167e2-494">创建名为“财务服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="167e2-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-495">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-495">Cost object</span></span></th>
<th><span data-ttu-id="167e2-496">财务服务</span><span class="sxs-lookup"><span data-stu-id="167e2-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-497">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-497">CC003</span></span></td>
<td><span data-ttu-id="167e2-498">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-498">Assembly</span></span></td>
<td><span data-ttu-id="167e2-499">65</span><span class="sxs-lookup"><span data-stu-id="167e2-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-500">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-500">CC004</span></span></td>
<td><span data-ttu-id="167e2-501">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-501">Packaging</span></span></td>
<td><span data-ttu-id="167e2-502">35</span><span class="sxs-lookup"><span data-stu-id="167e2-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-503">成本对象 CC003 装配生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="167e2-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="167e2-504">创建名为“装配服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="167e2-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-505">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-505">Cost object</span></span></th>
<th><span data-ttu-id="167e2-506">装配服务（小时）</span><span class="sxs-lookup"><span data-stu-id="167e2-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-507">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-507">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-508">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-508">Product 1</span></span></td>
<td><span data-ttu-id="167e2-509">60</span><span class="sxs-lookup"><span data-stu-id="167e2-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-510">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-510">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-511">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-511">Product 2</span></span></td>
<td><span data-ttu-id="167e2-512">20</span><span class="sxs-lookup"><span data-stu-id="167e2-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-513">成本对象 CC004 包装生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="167e2-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="167e2-514">创建名为“包装服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="167e2-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-515">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-515">Cost object</span></span></th>
<th><span data-ttu-id="167e2-516">包装服务（小时）</span><span class="sxs-lookup"><span data-stu-id="167e2-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-517">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-517">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-518">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-518">Product 1</span></span></td>
<td><span data-ttu-id="167e2-519">80</span><span class="sxs-lookup"><span data-stu-id="167e2-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-520">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-520">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-521">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-521">Product 2</span></span></td>
<td><span data-ttu-id="167e2-522">15</span><span class="sxs-lookup"><span data-stu-id="167e2-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-523">**注意：**在 Finance and Operations 中，产品消耗的生产工时等统计度量可以派生自源数据。</span><span class="sxs-lookup"><span data-stu-id="167e2-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="167e2-524">关于统计度量的更多详细信息，请参阅“统计度量提供方模板”。</span><span class="sxs-lookup"><span data-stu-id="167e2-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="167e2-525">（请注意，此主题尚未完成，不过将很快推出。）下表显示 HR 服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="167e2-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-526">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-526">Cost object</span></span></th>
<th><span data-ttu-id="167e2-527">度量值</span><span class="sxs-lookup"><span data-stu-id="167e2-527">Magnitude</span></span></th>
<th><span data-ttu-id="167e2-528">分配系数</span><span class="sxs-lookup"><span data-stu-id="167e2-528">Allocation factor</span></span></th>
<th><span data-ttu-id="167e2-529">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-529">Amount</span></span></th>
<th><span data-ttu-id="167e2-530">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-531">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-531">CC002</span></span></td>
<td><span data-ttu-id="167e2-532">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-532">Finance</span></span></td>
<td><span data-ttu-id="167e2-533">35</span><span class="sxs-lookup"><span data-stu-id="167e2-533">35</span></span></td>
<td><span data-ttu-id="167e2-534">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="167e2-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="167e2-535">175.00</span><span class="sxs-lookup"><span data-stu-id="167e2-535">175.00</span></span></td>
<td><span data-ttu-id="167e2-536">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-537">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-537">CC003</span></span></td>
<td><span data-ttu-id="167e2-538">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-538">Assembly</span></span></td>
<td><span data-ttu-id="167e2-539">55</span><span class="sxs-lookup"><span data-stu-id="167e2-539">55</span></span></td>
<td><span data-ttu-id="167e2-540">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="167e2-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="167e2-541">275.00</span><span class="sxs-lookup"><span data-stu-id="167e2-541">275.00</span></span></td>
<td><span data-ttu-id="167e2-542">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-543">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-543">CC004</span></span></td>
<td><span data-ttu-id="167e2-544">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-544">Packaging</span></span></td>
<td><span data-ttu-id="167e2-545">10</span><span class="sxs-lookup"><span data-stu-id="167e2-545">10</span></span></td>
<td><span data-ttu-id="167e2-546">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="167e2-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="167e2-547">50.00</span><span class="sxs-lookup"><span data-stu-id="167e2-547">50.00</span></span></td>
<td><span data-ttu-id="167e2-548">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-549">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-549">CC002</span></span></td>
<td><span data-ttu-id="167e2-550">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-550">Finance</span></span></td>
<td><span data-ttu-id="167e2-551">35</span><span class="sxs-lookup"><span data-stu-id="167e2-551">35</span></span></td>
<td><span data-ttu-id="167e2-552">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="167e2-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="167e2-553">436.00</span><span class="sxs-lookup"><span data-stu-id="167e2-553">436.00</span></span></td>
<td><span data-ttu-id="167e2-554">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-555">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-555">CC003</span></span></td>
<td><span data-ttu-id="167e2-556">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-556">Assembly</span></span></td>
<td><span data-ttu-id="167e2-557">55</span><span class="sxs-lookup"><span data-stu-id="167e2-557">55</span></span></td>
<td><span data-ttu-id="167e2-558">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="167e2-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="167e2-559">685.14</span><span class="sxs-lookup"><span data-stu-id="167e2-559">685.14</span></span></td>
<td><span data-ttu-id="167e2-560">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-561">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-561">CC004</span></span></td>
<td><span data-ttu-id="167e2-562">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-562">Packaging</span></span></td>
<td><span data-ttu-id="167e2-563">10</span><span class="sxs-lookup"><span data-stu-id="167e2-563">10</span></span></td>
<td><span data-ttu-id="167e2-564">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="167e2-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="167e2-565">124.57</span><span class="sxs-lookup"><span data-stu-id="167e2-565">124.57</span></span></td>
<td><span data-ttu-id="167e2-566">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-567">下表显示当财务服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="167e2-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-568">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-568">Cost object</span></span></th>
<th><span data-ttu-id="167e2-569">度量值</span><span class="sxs-lookup"><span data-stu-id="167e2-569">Magnitude</span></span></th>
<th><span data-ttu-id="167e2-570">分配系数</span><span class="sxs-lookup"><span data-stu-id="167e2-570">Allocation factor</span></span></th>
<th><span data-ttu-id="167e2-571">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-571">Amount</span></span></th>
<th><span data-ttu-id="167e2-572">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-573">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-573">CC003</span></span></td>
<td><span data-ttu-id="167e2-574">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-574">Assembly</span></span></td>
<td><span data-ttu-id="167e2-575">65</span><span class="sxs-lookup"><span data-stu-id="167e2-575">65</span></span></td>
<td><span data-ttu-id="167e2-576">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="167e2-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="167e2-577">438.75</span><span class="sxs-lookup"><span data-stu-id="167e2-577">438.75</span></span></td>
<td><span data-ttu-id="167e2-578">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-579">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-579">CC004</span></span></td>
<td><span data-ttu-id="167e2-580">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-580">Packaging</span></span></td>
<td><span data-ttu-id="167e2-581">35</span><span class="sxs-lookup"><span data-stu-id="167e2-581">35</span></span></td>
<td><span data-ttu-id="167e2-582">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="167e2-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="167e2-583">236.25</span><span class="sxs-lookup"><span data-stu-id="167e2-583">236.25</span></span></td>
<td><span data-ttu-id="167e2-584">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-585">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-585">CC003</span></span></td>
<td><span data-ttu-id="167e2-586">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-586">Assembly</span></span></td>
<td><span data-ttu-id="167e2-587">65</span><span class="sxs-lookup"><span data-stu-id="167e2-587">65</span></span></td>
<td><span data-ttu-id="167e2-588">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="167e2-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="167e2-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="167e2-589">5,297.69</span></span></td>
<td><span data-ttu-id="167e2-590">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-591">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-591">CC004</span></span></td>
<td><span data-ttu-id="167e2-592">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-592">Packaging</span></span></td>
<td><span data-ttu-id="167e2-593">35</span><span class="sxs-lookup"><span data-stu-id="167e2-593">35</span></span></td>
<td><span data-ttu-id="167e2-594">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="167e2-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="167e2-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="167e2-595">2,852.60</span></span></td>
<td><span data-ttu-id="167e2-596">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-597">下表显示当装配服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="167e2-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-598">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-598">Cost object</span></span></th>
<th><span data-ttu-id="167e2-599">度量值</span><span class="sxs-lookup"><span data-stu-id="167e2-599">Magnitude</span></span></th>
<th><span data-ttu-id="167e2-600">分配系数</span><span class="sxs-lookup"><span data-stu-id="167e2-600">Allocation factor</span></span></th>
<th><span data-ttu-id="167e2-601">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-601">Amount</span></span></th>
<th><span data-ttu-id="167e2-602">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-603">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-603">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-604">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-604">Product 1</span></span></td>
<td><span data-ttu-id="167e2-605">60</span><span class="sxs-lookup"><span data-stu-id="167e2-605">60</span></span></td>
<td><span data-ttu-id="167e2-606">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="167e2-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="167e2-607">535.31</span><span class="sxs-lookup"><span data-stu-id="167e2-607">535.31</span></span></td>
<td><span data-ttu-id="167e2-608">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-609">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-609">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-610">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-610">Product 2</span></span></td>
<td><span data-ttu-id="167e2-611">20</span><span class="sxs-lookup"><span data-stu-id="167e2-611">20</span></span></td>
<td><span data-ttu-id="167e2-612">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="167e2-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="167e2-613">178.44</span><span class="sxs-lookup"><span data-stu-id="167e2-613">178.44</span></span></td>
<td><span data-ttu-id="167e2-614">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-615">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-615">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-616">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-616">Product 1</span></span></td>
<td><span data-ttu-id="167e2-617">60</span><span class="sxs-lookup"><span data-stu-id="167e2-617">60</span></span></td>
<td><span data-ttu-id="167e2-618">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="167e2-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="167e2-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="167e2-619">4,487.12</span></span></td>
<td><span data-ttu-id="167e2-620">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-621">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-621">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-622">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-622">Product 2</span></span></td>
<td><span data-ttu-id="167e2-623">20</span><span class="sxs-lookup"><span data-stu-id="167e2-623">20</span></span></td>
<td><span data-ttu-id="167e2-624">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="167e2-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="167e2-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="167e2-625">1,495.71</span></span></td>
<td><span data-ttu-id="167e2-626">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="167e2-627">下表显示当包装服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="167e2-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-628">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-628">Cost object</span></span></th>
<th><span data-ttu-id="167e2-629">度量值</span><span class="sxs-lookup"><span data-stu-id="167e2-629">Magnitude</span></span></th>
<th><span data-ttu-id="167e2-630">分配系数</span><span class="sxs-lookup"><span data-stu-id="167e2-630">Allocation factor</span></span></th>
<th><span data-ttu-id="167e2-631">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-631">Amount</span></span></th>
<th><span data-ttu-id="167e2-632">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-633">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-633">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-634">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-634">Product 1</span></span></td>
<td><span data-ttu-id="167e2-635">80</span><span class="sxs-lookup"><span data-stu-id="167e2-635">80</span></span></td>
<td><span data-ttu-id="167e2-636">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="167e2-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="167e2-637">241.05</span><span class="sxs-lookup"><span data-stu-id="167e2-637">241.05</span></span></td>
<td><span data-ttu-id="167e2-638">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-639">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-639">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-640">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-640">Product 2</span></span></td>
<td><span data-ttu-id="167e2-641">15</span><span class="sxs-lookup"><span data-stu-id="167e2-641">15</span></span></td>
<td><span data-ttu-id="167e2-642">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="167e2-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="167e2-643">45.20</span><span class="sxs-lookup"><span data-stu-id="167e2-643">45.20</span></span></td>
<td><span data-ttu-id="167e2-644">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-645">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-645">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-646">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-646">Product 1</span></span></td>
<td><span data-ttu-id="167e2-647">80</span><span class="sxs-lookup"><span data-stu-id="167e2-647">80</span></span></td>
<td><span data-ttu-id="167e2-648">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="167e2-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="167e2-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="167e2-649">2,507.09</span></span></td>
<td><span data-ttu-id="167e2-650">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-651">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-651">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-652">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-652">Product 2</span></span></td>
<td><span data-ttu-id="167e2-653">15</span><span class="sxs-lookup"><span data-stu-id="167e2-653">15</span></span></td>
<td><span data-ttu-id="167e2-654">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="167e2-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="167e2-655">470.08</span><span class="sxs-lookup"><span data-stu-id="167e2-655">470.08</span></span></td>
<td><span data-ttu-id="167e2-656">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="167e2-657">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="167e2-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="167e2-658">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-658">Journal</span></span></th>
<th><span data-ttu-id="167e2-659">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="167e2-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="167e2-660">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="167e2-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="167e2-661">版本</span><span class="sxs-lookup"><span data-stu-id="167e2-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-662">00004</span><span class="sxs-lookup"><span data-stu-id="167e2-662">00004</span></span></td>
<td><span data-ttu-id="167e2-663">成本分配日记帐</span><span class="sxs-lookup"><span data-stu-id="167e2-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="167e2-664">会计</span><span class="sxs-lookup"><span data-stu-id="167e2-664">Fiscal</span></span></td>
<td><span data-ttu-id="167e2-665">2017</span><span class="sxs-lookup"><span data-stu-id="167e2-665">2017</span></span></td>
<td><span data-ttu-id="167e2-666">期间 1</span><span class="sxs-lookup"><span data-stu-id="167e2-666">Period 1</span></span></td>
<td><span data-ttu-id="167e2-667">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="167e2-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="167e2-668">日记帐行</span><span class="sxs-lookup"><span data-stu-id="167e2-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="167e2-669">会计日期</span><span class="sxs-lookup"><span data-stu-id="167e2-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-670">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-671">成本元素</span><span class="sxs-lookup"><span data-stu-id="167e2-671">Cost element</span></span></th>
<th><span data-ttu-id="167e2-672">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-672">Cost behavior</span></span></th>
<th><span data-ttu-id="167e2-673">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-674">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-675">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-675">CC001</span></span></td>
<td><span data-ttu-id="167e2-676">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-676">HR</span></span></td>
<td><span data-ttu-id="167e2-677">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-677">10001</span></span></td>
<td><span data-ttu-id="167e2-678">电</span><span class="sxs-lookup"><span data-stu-id="167e2-678">Electricity</span></span></td>
<td><span data-ttu-id="167e2-679">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-679">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-680">500.00</span><span class="sxs-lookup"><span data-stu-id="167e2-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-681">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-682">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-682">CC001</span></span></td>
<td><span data-ttu-id="167e2-683">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-683">HR</span></span></td>
<td><span data-ttu-id="167e2-684">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-684">10001</span></span></td>
<td><span data-ttu-id="167e2-685">电</span><span class="sxs-lookup"><span data-stu-id="167e2-685">Electricity</span></span></td>
<td><span data-ttu-id="167e2-686">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-686">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="167e2-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-688">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-689">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-689">CC002</span></span></td>
<td><span data-ttu-id="167e2-690">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-690">Finance</span></span></td>
<td><span data-ttu-id="167e2-691">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-691">10001</span></span></td>
<td><span data-ttu-id="167e2-692">电</span><span class="sxs-lookup"><span data-stu-id="167e2-692">Electricity</span></span></td>
<td><span data-ttu-id="167e2-693">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-693">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-694">675.00</span><span class="sxs-lookup"><span data-stu-id="167e2-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-695">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-696">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-696">CC002</span></span></td>
<td><span data-ttu-id="167e2-697">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-697">Finance</span></span></td>
<td><span data-ttu-id="167e2-698">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-698">10001</span></span></td>
<td><span data-ttu-id="167e2-699">电</span><span class="sxs-lookup"><span data-stu-id="167e2-699">Electricity</span></span></td>
<td><span data-ttu-id="167e2-700">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-700">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="167e2-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-702">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-703">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-703">CC003</span></span></td>
<td><span data-ttu-id="167e2-704">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-704">Assembly</span></span></td>
<td><span data-ttu-id="167e2-705">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-705">10001</span></span></td>
<td><span data-ttu-id="167e2-706">电</span><span class="sxs-lookup"><span data-stu-id="167e2-706">Electricity</span></span></td>
<td><span data-ttu-id="167e2-707">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-707">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-708">713.75</span><span class="sxs-lookup"><span data-stu-id="167e2-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-709">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-710">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-710">CC003</span></span></td>
<td><span data-ttu-id="167e2-711">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-711">Assembly</span></span></td>
<td><span data-ttu-id="167e2-712">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-712">10001</span></span></td>
<td><span data-ttu-id="167e2-713">电</span><span class="sxs-lookup"><span data-stu-id="167e2-713">Electricity</span></span></td>
<td><span data-ttu-id="167e2-714">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-714">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="167e2-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-716">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-717">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-717">CC003</span></span></td>
<td><span data-ttu-id="167e2-718">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-718">Packaging</span></span></td>
<td><span data-ttu-id="167e2-719">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-719">10001</span></span></td>
<td><span data-ttu-id="167e2-720">电</span><span class="sxs-lookup"><span data-stu-id="167e2-720">Electricity</span></span></td>
<td><span data-ttu-id="167e2-721">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-721">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-722">286.25</span><span class="sxs-lookup"><span data-stu-id="167e2-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-723">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-724">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-724">CC003</span></span></td>
<td><span data-ttu-id="167e2-725">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-725">Packaging</span></span></td>
<td><span data-ttu-id="167e2-726">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-726">10001</span></span></td>
<td><span data-ttu-id="167e2-727">电</span><span class="sxs-lookup"><span data-stu-id="167e2-727">Electricity</span></span></td>
<td><span data-ttu-id="167e2-728">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-728">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="167e2-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-730">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-731">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-731">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-732">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-732">Product 1</span></span></td>
<td><span data-ttu-id="167e2-733">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-733">10001</span></span></td>
<td><span data-ttu-id="167e2-734">电</span><span class="sxs-lookup"><span data-stu-id="167e2-734">Electricity</span></span></td>
<td><span data-ttu-id="167e2-735">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-735">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-736">776.36</span><span class="sxs-lookup"><span data-stu-id="167e2-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-737">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-738">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-738">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-739">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-739">Product 1</span></span></td>
<td><span data-ttu-id="167e2-740">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-740">10001</span></span></td>
<td><span data-ttu-id="167e2-741">电</span><span class="sxs-lookup"><span data-stu-id="167e2-741">Electricity</span></span></td>
<td><span data-ttu-id="167e2-742">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-742">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="167e2-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-744">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-745">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-745">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-746">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-746">Product 1</span></span></td>
<td><span data-ttu-id="167e2-747">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-747">10001</span></span></td>
<td><span data-ttu-id="167e2-748">电</span><span class="sxs-lookup"><span data-stu-id="167e2-748">Electricity</span></span></td>
<td><span data-ttu-id="167e2-749">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-749">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-750">223.64</span><span class="sxs-lookup"><span data-stu-id="167e2-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-751">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="167e2-752">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-752">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-753">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-753">Product 1</span></span></td>
<td><span data-ttu-id="167e2-754">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-754">10001</span></span></td>
<td><span data-ttu-id="167e2-755">电</span><span class="sxs-lookup"><span data-stu-id="167e2-755">Electricity</span></span></td>
<td><span data-ttu-id="167e2-756">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-756">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="167e2-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="167e2-758">成本条目</span><span class="sxs-lookup"><span data-stu-id="167e2-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="167e2-759">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="167e2-760">成本元素</span><span class="sxs-lookup"><span data-stu-id="167e2-760">Cost element</span></span></th>
<th><span data-ttu-id="167e2-761">成本行为</span><span class="sxs-lookup"><span data-stu-id="167e2-761">Cost behavior</span></span></th>
<th><span data-ttu-id="167e2-762">本币金额</span><span class="sxs-lookup"><span data-stu-id="167e2-762">Amount</span></span></th>
<th><span data-ttu-id="167e2-763">会计日期</span><span class="sxs-lookup"><span data-stu-id="167e2-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="167e2-764">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-764">CC001</span></span></td>
<td><span data-ttu-id="167e2-765">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-765">HR</span></span></td>
<td><span data-ttu-id="167e2-766">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-766">10001</span></span></td>
<td><span data-ttu-id="167e2-767">电</span><span class="sxs-lookup"><span data-stu-id="167e2-767">Electricity</span></span></td>
<td><span data-ttu-id="167e2-768">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-768">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-769">-500.00</span><span class="sxs-lookup"><span data-stu-id="167e2-769">-500.00</span></span></td>
<td><span data-ttu-id="167e2-770">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-771">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-771">CC002</span></span></td>
<td><span data-ttu-id="167e2-772">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-772">Finance</span></span></td>
<td><span data-ttu-id="167e2-773">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-773">10001</span></span></td>
<td><span data-ttu-id="167e2-774">电</span><span class="sxs-lookup"><span data-stu-id="167e2-774">Electricity</span></span></td>
<td><span data-ttu-id="167e2-775">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-775">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-776">175.00</span><span class="sxs-lookup"><span data-stu-id="167e2-776">175.00</span></span></td>
<td><span data-ttu-id="167e2-777">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-778">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-778">CC003</span></span></td>
<td><span data-ttu-id="167e2-779">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-779">Assembly</span></span></td>
<td><span data-ttu-id="167e2-780">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-780">10001</span></span></td>
<td><span data-ttu-id="167e2-781">电</span><span class="sxs-lookup"><span data-stu-id="167e2-781">Electricity</span></span></td>
<td><span data-ttu-id="167e2-782">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-782">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-783">275.00</span><span class="sxs-lookup"><span data-stu-id="167e2-783">275.00</span></span></td>
<td><span data-ttu-id="167e2-784">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-785">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-785">CC004</span></span></td>
<td><span data-ttu-id="167e2-786">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-786">Packaging</span></span></td>
<td><span data-ttu-id="167e2-787">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-787">10001</span></span></td>
<td><span data-ttu-id="167e2-788">电</span><span class="sxs-lookup"><span data-stu-id="167e2-788">Electricity</span></span></td>
<td><span data-ttu-id="167e2-789">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-789">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-790">50,00</span><span class="sxs-lookup"><span data-stu-id="167e2-790">50,00</span></span></td>
<td><span data-ttu-id="167e2-791">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-792">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-792">CC001</span></span></td>
<td><span data-ttu-id="167e2-793">HR</span><span class="sxs-lookup"><span data-stu-id="167e2-793">HR</span></span></td>
<td><span data-ttu-id="167e2-794">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-794">10001</span></span></td>
<td><span data-ttu-id="167e2-795">电</span><span class="sxs-lookup"><span data-stu-id="167e2-795">Electricity</span></span></td>
<td><span data-ttu-id="167e2-796">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-796">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-797">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="167e2-797">-1,245.71</span></span></td>
<td><span data-ttu-id="167e2-798">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-799">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-799">CC002</span></span></td>
<td><span data-ttu-id="167e2-800">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-800">Finance</span></span></td>
<td><span data-ttu-id="167e2-801">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-801">10001</span></span></td>
<td><span data-ttu-id="167e2-802">电</span><span class="sxs-lookup"><span data-stu-id="167e2-802">Electricity</span></span></td>
<td><span data-ttu-id="167e2-803">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-803">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-804">436.00</span><span class="sxs-lookup"><span data-stu-id="167e2-804">436.00</span></span></td>
<td><span data-ttu-id="167e2-805">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-806">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-806">CC003</span></span></td>
<td><span data-ttu-id="167e2-807">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-807">Assembly</span></span></td>
<td><span data-ttu-id="167e2-808">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-808">10001</span></span></td>
<td><span data-ttu-id="167e2-809">电</span><span class="sxs-lookup"><span data-stu-id="167e2-809">Electricity</span></span></td>
<td><span data-ttu-id="167e2-810">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-810">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-811">685.14</span><span class="sxs-lookup"><span data-stu-id="167e2-811">685.14</span></span></td>
<td><span data-ttu-id="167e2-812">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-813">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-813">CC004</span></span></td>
<td><span data-ttu-id="167e2-814">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-814">Packaging</span></span></td>
<td><span data-ttu-id="167e2-815">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-815">10001</span></span></td>
<td><span data-ttu-id="167e2-816">电</span><span class="sxs-lookup"><span data-stu-id="167e2-816">Electricity</span></span></td>
<td><span data-ttu-id="167e2-817">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-817">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-818">124.57</span><span class="sxs-lookup"><span data-stu-id="167e2-818">124.57</span></span></td>
<td><span data-ttu-id="167e2-819">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-820">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-820">CC002</span></span></td>
<td><span data-ttu-id="167e2-821">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-821">Finance</span></span></td>
<td><span data-ttu-id="167e2-822">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-822">10001</span></span></td>
<td><span data-ttu-id="167e2-823">电</span><span class="sxs-lookup"><span data-stu-id="167e2-823">Electricity</span></span></td>
<td><span data-ttu-id="167e2-824">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-824">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-825">-675.00</span><span class="sxs-lookup"><span data-stu-id="167e2-825">-675.00</span></span></td>
<td><span data-ttu-id="167e2-826">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-827">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-827">CC003</span></span></td>
<td><span data-ttu-id="167e2-828">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-828">Assembly</span></span></td>
<td><span data-ttu-id="167e2-829">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-829">10001</span></span></td>
<td><span data-ttu-id="167e2-830">电</span><span class="sxs-lookup"><span data-stu-id="167e2-830">Electricity</span></span></td>
<td><span data-ttu-id="167e2-831">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-831">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-832">438.75</span><span class="sxs-lookup"><span data-stu-id="167e2-832">438.75</span></span></td>
<td><span data-ttu-id="167e2-833">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-834">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-834">CC004</span></span></td>
<td><span data-ttu-id="167e2-835">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-835">Packaging</span></span></td>
<td><span data-ttu-id="167e2-836">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-836">10001</span></span></td>
<td><span data-ttu-id="167e2-837">电</span><span class="sxs-lookup"><span data-stu-id="167e2-837">Electricity</span></span></td>
<td><span data-ttu-id="167e2-838">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-838">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-839">236.25</span><span class="sxs-lookup"><span data-stu-id="167e2-839">236.25</span></span></td>
<td><span data-ttu-id="167e2-840">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-841">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-841">CC002</span></span></td>
<td><span data-ttu-id="167e2-842">财务</span><span class="sxs-lookup"><span data-stu-id="167e2-842">Finance</span></span></td>
<td><span data-ttu-id="167e2-843">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-843">10001</span></span></td>
<td><span data-ttu-id="167e2-844">电</span><span class="sxs-lookup"><span data-stu-id="167e2-844">Electricity</span></span></td>
<td><span data-ttu-id="167e2-845">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-845">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-846">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="167e2-846">-8,150.29</span></span></td>
<td><span data-ttu-id="167e2-847">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-848">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-848">CC003</span></span></td>
<td><span data-ttu-id="167e2-849">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-849">Assembly</span></span></td>
<td><span data-ttu-id="167e2-850">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-850">10001</span></span></td>
<td><span data-ttu-id="167e2-851">电</span><span class="sxs-lookup"><span data-stu-id="167e2-851">Electricity</span></span></td>
<td><span data-ttu-id="167e2-852">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-852">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="167e2-853">5,297.69</span></span></td>
<td><span data-ttu-id="167e2-854">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-855">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-855">CC004</span></span></td>
<td><span data-ttu-id="167e2-856">包装</span><span class="sxs-lookup"><span data-stu-id="167e2-856">Packaging</span></span></td>
<td><span data-ttu-id="167e2-857">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-857">10001</span></span></td>
<td><span data-ttu-id="167e2-858">电</span><span class="sxs-lookup"><span data-stu-id="167e2-858">Electricity</span></span></td>
<td><span data-ttu-id="167e2-859">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-859">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="167e2-860">2,852.60</span></span></td>
<td><span data-ttu-id="167e2-861">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-862">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-862">CC003</span></span></td>
<td><span data-ttu-id="167e2-863">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-863">Assembly</span></span></td>
<td><span data-ttu-id="167e2-864">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-864">10001</span></span></td>
<td><span data-ttu-id="167e2-865">电</span><span class="sxs-lookup"><span data-stu-id="167e2-865">Electricity</span></span></td>
<td><span data-ttu-id="167e2-866">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-866">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-867">-713.75</span><span class="sxs-lookup"><span data-stu-id="167e2-867">-713.75</span></span></td>
<td><span data-ttu-id="167e2-868">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-869">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-869">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-870">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-870">Product 1</span></span></td>
<td><span data-ttu-id="167e2-871">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-871">10001</span></span></td>
<td><span data-ttu-id="167e2-872">电</span><span class="sxs-lookup"><span data-stu-id="167e2-872">Electricity</span></span></td>
<td><span data-ttu-id="167e2-873">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-873">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-874">535.31</span><span class="sxs-lookup"><span data-stu-id="167e2-874">535.31</span></span></td>
<td><span data-ttu-id="167e2-875">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-876">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-876">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-877">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-877">Product 2</span></span></td>
<td><span data-ttu-id="167e2-878">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-878">10001</span></span></td>
<td><span data-ttu-id="167e2-879">电</span><span class="sxs-lookup"><span data-stu-id="167e2-879">Electricity</span></span></td>
<td><span data-ttu-id="167e2-880">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-880">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-881">178.44</span><span class="sxs-lookup"><span data-stu-id="167e2-881">178.44</span></span></td>
<td><span data-ttu-id="167e2-882">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-883">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-883">CC003</span></span></td>
<td><span data-ttu-id="167e2-884">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-884">Assembly</span></span></td>
<td><span data-ttu-id="167e2-885">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-885">10001</span></span></td>
<td><span data-ttu-id="167e2-886">电</span><span class="sxs-lookup"><span data-stu-id="167e2-886">Electricity</span></span></td>
<td><span data-ttu-id="167e2-887">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-887">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-888">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="167e2-888">-5,982.83</span></span></td>
<td><span data-ttu-id="167e2-889">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-890">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-890">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-891">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-891">Product 1</span></span></td>
<td><span data-ttu-id="167e2-892">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-892">10001</span></span></td>
<td><span data-ttu-id="167e2-893">电</span><span class="sxs-lookup"><span data-stu-id="167e2-893">Electricity</span></span></td>
<td><span data-ttu-id="167e2-894">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-894">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="167e2-895">4,487.12</span></span></td>
<td><span data-ttu-id="167e2-896">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-897">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-897">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-898">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-898">Product 2</span></span></td>
<td><span data-ttu-id="167e2-899">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-899">10001</span></span></td>
<td><span data-ttu-id="167e2-900">电</span><span class="sxs-lookup"><span data-stu-id="167e2-900">Electricity</span></span></td>
<td><span data-ttu-id="167e2-901">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-901">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="167e2-902">1,495.71</span></span></td>
<td><span data-ttu-id="167e2-903">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-904">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-904">CC003</span></span></td>
<td><span data-ttu-id="167e2-905">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-905">Assembly</span></span></td>
<td><span data-ttu-id="167e2-906">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-906">10001</span></span></td>
<td><span data-ttu-id="167e2-907">电</span><span class="sxs-lookup"><span data-stu-id="167e2-907">Electricity</span></span></td>
<td><span data-ttu-id="167e2-908">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-908">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-909">-286.25</span><span class="sxs-lookup"><span data-stu-id="167e2-909">-286.25</span></span></td>
<td><span data-ttu-id="167e2-910">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-911">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-911">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-912">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-912">Product 1</span></span></td>
<td><span data-ttu-id="167e2-913">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-913">10001</span></span></td>
<td><span data-ttu-id="167e2-914">电</span><span class="sxs-lookup"><span data-stu-id="167e2-914">Electricity</span></span></td>
<td><span data-ttu-id="167e2-915">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-915">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-916">241.05</span><span class="sxs-lookup"><span data-stu-id="167e2-916">241.05</span></span></td>
<td><span data-ttu-id="167e2-917">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-918">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-918">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-919">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-919">Product 2</span></span></td>
<td><span data-ttu-id="167e2-920">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-920">10001</span></span></td>
<td><span data-ttu-id="167e2-921">电</span><span class="sxs-lookup"><span data-stu-id="167e2-921">Electricity</span></span></td>
<td><span data-ttu-id="167e2-922">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-922">Fixed cost</span></span></td>
<td><span data-ttu-id="167e2-923">45.20</span><span class="sxs-lookup"><span data-stu-id="167e2-923">45.20</span></span></td>
<td><span data-ttu-id="167e2-924">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-925">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-925">CC003</span></span></td>
<td><span data-ttu-id="167e2-926">程序集</span><span class="sxs-lookup"><span data-stu-id="167e2-926">Assembly</span></span></td>
<td><span data-ttu-id="167e2-927">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-927">10001</span></span></td>
<td><span data-ttu-id="167e2-928">电</span><span class="sxs-lookup"><span data-stu-id="167e2-928">Electricity</span></span></td>
<td><span data-ttu-id="167e2-929">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-929">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-930">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="167e2-930">-2,977.17</span></span></td>
<td><span data-ttu-id="167e2-931">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-932">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-932">Prod 1</span></span></td>
<td><span data-ttu-id="167e2-933">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-933">Product 1</span></span></td>
<td><span data-ttu-id="167e2-934">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-934">10001</span></span></td>
<td><span data-ttu-id="167e2-935">电</span><span class="sxs-lookup"><span data-stu-id="167e2-935">Electricity</span></span></td>
<td><span data-ttu-id="167e2-936">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-936">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="167e2-937">2,507.09</span></span></td>
<td><span data-ttu-id="167e2-938">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="167e2-939">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-939">Prod 2</span></span></td>
<td><span data-ttu-id="167e2-940">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-940">Product 2</span></span></td>
<td><span data-ttu-id="167e2-941">10001</span><span class="sxs-lookup"><span data-stu-id="167e2-941">10001</span></span></td>
<td><span data-ttu-id="167e2-942">电</span><span class="sxs-lookup"><span data-stu-id="167e2-942">Electricity</span></span></td>
<td><span data-ttu-id="167e2-943">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-943">Variable cost</span></span></td>
<td><span data-ttu-id="167e2-944">470.08</span><span class="sxs-lookup"><span data-stu-id="167e2-944">470.08</span></span></td>
<td><span data-ttu-id="167e2-945">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="167e2-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="167e2-946">结论</span><span class="sxs-lookup"><span data-stu-id="167e2-946">Conclusion</span></span>
<span data-ttu-id="167e2-947">在财务会计中，10,000.00 电成本过帐到虚拟成本中心 ID。</span><span class="sxs-lookup"><span data-stu-id="167e2-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="167e2-948">因此，成本会计员将了解必须分摊此成本。</span><span class="sxs-lookup"><span data-stu-id="167e2-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="167e2-949">在成本核算中，跨组织单位和级别的成本流，基于所应用的政策和规则。</span><span class="sxs-lookup"><span data-stu-id="167e2-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="167e2-950">每项成本已与为成本分摊提供最佳评估的分配基础关联。</span><span class="sxs-lookup"><span data-stu-id="167e2-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="167e2-951">成本元素</span><span class="sxs-lookup"><span data-stu-id="167e2-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="167e2-952">成本对象</span><span class="sxs-lookup"><span data-stu-id="167e2-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="167e2-953">合计</span><span class="sxs-lookup"><span data-stu-id="167e2-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="167e2-954">CC099</span><span class="sxs-lookup"><span data-stu-id="167e2-954">CC099</span></span></th>
<th><span data-ttu-id="167e2-955">CC001</span><span class="sxs-lookup"><span data-stu-id="167e2-955">CC001</span></span></th>
<th><span data-ttu-id="167e2-956">CC002</span><span class="sxs-lookup"><span data-stu-id="167e2-956">CC002</span></span></th>
<th><span data-ttu-id="167e2-957">CC003</span><span class="sxs-lookup"><span data-stu-id="167e2-957">CC003</span></span></th>
<th><span data-ttu-id="167e2-958">CC004</span><span class="sxs-lookup"><span data-stu-id="167e2-958">CC004</span></span></th>
<th><span data-ttu-id="167e2-959">项目 1</span><span class="sxs-lookup"><span data-stu-id="167e2-959">Proj 1</span></span></th>
<th><span data-ttu-id="167e2-960">项目 2</span><span class="sxs-lookup"><span data-stu-id="167e2-960">Proj 2</span></span></th>
<th><span data-ttu-id="167e2-961">产品 1</span><span class="sxs-lookup"><span data-stu-id="167e2-961">Prod 1</span></span></th>
<th><span data-ttu-id="167e2-962">产品 2</span><span class="sxs-lookup"><span data-stu-id="167e2-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="167e2-963">10001 电</span><span class="sxs-lookup"><span data-stu-id="167e2-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="167e2-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="167e2-973">未分类</span><span class="sxs-lookup"><span data-stu-id="167e2-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-974">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-974">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="167e2-975">固定成本</span><span class="sxs-lookup"><span data-stu-id="167e2-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-976">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-977">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-978">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-979">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-980">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="167e2-981">776.36</span><span class="sxs-lookup"><span data-stu-id="167e2-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-982">223.64</span><span class="sxs-lookup"><span data-stu-id="167e2-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="167e2-984">可变成本</span><span class="sxs-lookup"><span data-stu-id="167e2-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-985">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-986">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-987">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-988">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-989">0.00</span><span class="sxs-lookup"><span data-stu-id="167e2-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-990">30.00</span><span class="sxs-lookup"><span data-stu-id="167e2-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-991">10.00</span><span class="sxs-lookup"><span data-stu-id="167e2-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="167e2-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="167e2-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="167e2-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="167e2-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="167e2-995">此主题显示主要成本元素“10001 电”如何流过成本对象。</span><span class="sxs-lookup"><span data-stu-id="167e2-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="167e2-996">因此，此间接成本分摊到组织的最低级别。</span><span class="sxs-lookup"><span data-stu-id="167e2-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="167e2-997">换言之，最低级别的成本对象承担成本。</span><span class="sxs-lookup"><span data-stu-id="167e2-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="167e2-998">如果您需要成本对象之间的可视成本流，可以使用成本累积政策规则实现成本流可视化。</span><span class="sxs-lookup"><span data-stu-id="167e2-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="167e2-999">更多详细信息，请参阅“成本累积政策”。</span><span class="sxs-lookup"><span data-stu-id="167e2-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="167e2-1000">（请注意，此主题尚未完成，不过将很快推出。）</span><span class="sxs-lookup"><span data-stu-id="167e2-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




