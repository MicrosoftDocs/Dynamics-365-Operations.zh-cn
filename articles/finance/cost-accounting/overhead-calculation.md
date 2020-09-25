---
title: 开销计算
description: 此主题描述计算和分配间接成本的典型流程。
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759464"
---
# <a name="overhead-calculation"></a><span data-ttu-id="0353b-103">开销计算</span><span class="sxs-lookup"><span data-stu-id="0353b-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0353b-104">此主题描述计算和分配间接成本的典型流程。</span><span class="sxs-lookup"><span data-stu-id="0353b-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="0353b-105">术语定义</span><span class="sxs-lookup"><span data-stu-id="0353b-105">Term definition</span></span>
---------------

<span data-ttu-id="0353b-106">间接成本是为业务运营支出的成本，但是不能直接归为任何具体的业务活动、产品或服务。</span><span class="sxs-lookup"><span data-stu-id="0353b-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="0353b-107">间接成本为营利活动的生成提供重要支持。</span><span class="sxs-lookup"><span data-stu-id="0353b-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="0353b-108">以下是一些开销成本示例：</span><span class="sxs-lookup"><span data-stu-id="0353b-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="0353b-109">租金</span><span class="sxs-lookup"><span data-stu-id="0353b-109">Rent</span></span>
-   <span data-ttu-id="0353b-110">电</span><span class="sxs-lookup"><span data-stu-id="0353b-110">Electricity</span></span>
-   <span data-ttu-id="0353b-111">管理薪金</span><span class="sxs-lookup"><span data-stu-id="0353b-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="0353b-112">开销计算概览</span><span class="sxs-lookup"><span data-stu-id="0353b-112">Overhead calculation overview</span></span>
<span data-ttu-id="0353b-113">开销计算按正确顺序运行会计政策。</span><span class="sxs-lookup"><span data-stu-id="0353b-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="0353b-114">如果成本核算政策更改或检测到特定错误，您可以为同一个会计期间多次运行开销计算。</span><span class="sxs-lookup"><span data-stu-id="0353b-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="0353b-115">每次运行的开销计算将被存储并收到唯一版本 ID，让您可以比较各个版本的计算。</span><span class="sxs-lookup"><span data-stu-id="0353b-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="0353b-116">开销计算生成的成本条目接收会计日期。</span><span class="sxs-lookup"><span data-stu-id="0353b-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="0353b-117">此会计日期与计算中使用的会计期间的结束日期一致。</span><span class="sxs-lookup"><span data-stu-id="0353b-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="0353b-118">唯一版本 ID 由以下元素组成：</span><span class="sxs-lookup"><span data-stu-id="0353b-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="0353b-119">版本类型</span><span class="sxs-lookup"><span data-stu-id="0353b-119">Version type</span></span>
-   <span data-ttu-id="0353b-120">日期和时间</span><span class="sxs-lookup"><span data-stu-id="0353b-120">Date and time</span></span>
-   <span data-ttu-id="0353b-121">成本核算分类帐</span><span class="sxs-lookup"><span data-stu-id="0353b-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="0353b-122">会计年度</span><span class="sxs-lookup"><span data-stu-id="0353b-122">Fiscal year</span></span>
-   <span data-ttu-id="0353b-123">会计期间</span><span class="sxs-lookup"><span data-stu-id="0353b-123">Fiscal period</span></span>

<span data-ttu-id="0353b-124">开销计算独立于版本运行。</span><span class="sxs-lookup"><span data-stu-id="0353b-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="0353b-125">因此，可以在实际版本前计算预算版本。</span><span class="sxs-lookup"><span data-stu-id="0353b-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="0353b-126">开销计算包括四个步骤，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="0353b-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="0353b-127">在每个步骤中，创建包含日记帐条目的日记帐标头。</span><span class="sxs-lookup"><span data-stu-id="0353b-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="0353b-128">此日记帐标头为每个计算步骤保留输入数据。</span><span class="sxs-lookup"><span data-stu-id="0353b-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="0353b-129">政策和规则应用于每个日记帐行，成本条目生成为输出。</span><span class="sxs-lookup"><span data-stu-id="0353b-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="0353b-130">因此，您始终具有完全的可跟踪性。</span><span class="sxs-lookup"><span data-stu-id="0353b-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="0353b-131">[![开销计算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="0353b-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="0353b-132">计算和分摊电间接成本</span><span class="sxs-lookup"><span data-stu-id="0353b-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="0353b-133">在财务会计中，有些成本（如电）登记为总计。</span><span class="sxs-lookup"><span data-stu-id="0353b-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="0353b-134">因此，不为成本核算提供详细的管理洞察。</span><span class="sxs-lookup"><span data-stu-id="0353b-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="0353b-135">在成本核算中，为提供跨所有组织单位和级别的正确的管理洞察，成本必须流过各个组织单位。</span><span class="sxs-lookup"><span data-stu-id="0353b-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="0353b-136">此流必须基于消耗量的准确记录或公平评估。</span><span class="sxs-lookup"><span data-stu-id="0353b-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="0353b-137">在总帐中，可以过帐电成本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="0353b-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0353b-138">会计日期</span><span class="sxs-lookup"><span data-stu-id="0353b-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-139">成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-140">主科目</span><span class="sxs-lookup"><span data-stu-id="0353b-140">Main account</span></span></th>
<th><span data-ttu-id="0353b-141">按记帐币种计算的金额</span><span class="sxs-lookup"><span data-stu-id="0353b-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-142">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="0353b-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="0353b-143">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-143">CC099</span></span></td>
<td><span data-ttu-id="0353b-144">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-144">Default cost center</span></span></td>
<td><span data-ttu-id="0353b-145">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-145">10001</span></span></td>
<td><span data-ttu-id="0353b-146">电</span><span class="sxs-lookup"><span data-stu-id="0353b-146">Electricity</span></span></td>
<td><span data-ttu-id="0353b-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="0353b-148">步骤 1：处理成本行为计算</span><span class="sxs-lookup"><span data-stu-id="0353b-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="0353b-149">默认情况下，当成本条目从源数据导入时，它们在成本核算中接收**未分类**成本行为分类。</span><span class="sxs-lookup"><span data-stu-id="0353b-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="0353b-150">通过应用成本行为政策规则，您可以将成本条目重新分类为**固定成本**或**可变成本**。</span><span class="sxs-lookup"><span data-stu-id="0353b-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="0353b-151">定义成本行为规则</span><span class="sxs-lookup"><span data-stu-id="0353b-151">Define the cost behavior rule</span></span>

<span data-ttu-id="0353b-152">在某些情况下，一部分成本是一项固定费用，其余成本基于消耗量。</span><span class="sxs-lookup"><span data-stu-id="0353b-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="0353b-153">通常电费帐单与此定义一致。</span><span class="sxs-lookup"><span data-stu-id="0353b-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="0353b-154">在支付特定固定费用后，您按千瓦时 (Kwh) 支付消耗量。</span><span class="sxs-lookup"><span data-stu-id="0353b-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="0353b-155">例如，如果固定成本费用为 1,000.00，以下是成本行为规则的定义：</span><span class="sxs-lookup"><span data-stu-id="0353b-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="0353b-156">固定金额 1,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="0353b-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="0353b-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="0353b-158">1000,01 &lt; N = 可变</span><span class="sxs-lookup"><span data-stu-id="0353b-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="0353b-159">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0353b-160">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-160">Journal</span></span></th>
<th><span data-ttu-id="0353b-161">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="0353b-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0353b-162">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="0353b-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0353b-163">版本</span><span class="sxs-lookup"><span data-stu-id="0353b-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-164">00001</span><span class="sxs-lookup"><span data-stu-id="0353b-164">00001</span></span></td>
<td><span data-ttu-id="0353b-165">成本行为计算日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="0353b-166">会计</span><span class="sxs-lookup"><span data-stu-id="0353b-166">Fiscal</span></span></td>
<td><span data-ttu-id="0353b-167">2017</span><span class="sxs-lookup"><span data-stu-id="0353b-167">2017</span></span></td>
<td><span data-ttu-id="0353b-168">期间 1</span><span class="sxs-lookup"><span data-stu-id="0353b-168">Period 1</span></span></td>
<td><span data-ttu-id="0353b-169">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="0353b-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="0353b-170">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="0353b-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0353b-171">会计日期</span><span class="sxs-lookup"><span data-stu-id="0353b-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-172">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-173">成本元素</span><span class="sxs-lookup"><span data-stu-id="0353b-173">Cost element</span></span></th>
<th><span data-ttu-id="0353b-174">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-174">Cost behavior</span></span></th>
<th><span data-ttu-id="0353b-175">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-176">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="0353b-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="0353b-177">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-177">CC099</span></span></td>
<td><span data-ttu-id="0353b-178">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-178">Default cost center</span></span></td>
<td><span data-ttu-id="0353b-179">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-179">10001</span></span></td>
<td><span data-ttu-id="0353b-180">电</span><span class="sxs-lookup"><span data-stu-id="0353b-180">Electricity</span></span></td>
<td><span data-ttu-id="0353b-181">未分类</span><span class="sxs-lookup"><span data-stu-id="0353b-181">Unclassified</span></span></td>
<td><span data-ttu-id="0353b-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0353b-183">成本条目</span><span class="sxs-lookup"><span data-stu-id="0353b-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-184">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-185">成本元素</span><span class="sxs-lookup"><span data-stu-id="0353b-185">Cost element</span></span></th>
<th><span data-ttu-id="0353b-186">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-186">Cost behavior</span></span></th>
<th><span data-ttu-id="0353b-187">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-187">Amount</span></span></th>
<th><span data-ttu-id="0353b-188">会计日期</span><span class="sxs-lookup"><span data-stu-id="0353b-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-189">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-189">CC099</span></span></td>
<td><span data-ttu-id="0353b-190">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-190">Default cost center</span></span></td>
<td><span data-ttu-id="0353b-191">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-191">10001</span></span></td>
<td><span data-ttu-id="0353b-192">电</span><span class="sxs-lookup"><span data-stu-id="0353b-192">Electricity</span></span></td>
<td><span data-ttu-id="0353b-193">未分类</span><span class="sxs-lookup"><span data-stu-id="0353b-193">Unclassified</span></span></td>
<td><span data-ttu-id="0353b-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-194">10,000.00</span></span></td>
<td><span data-ttu-id="0353b-195">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="0353b-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-196">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-196">CC099</span></span></td>
<td><span data-ttu-id="0353b-197">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-197">Default cost center</span></span></td>
<td><span data-ttu-id="0353b-198">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-198">10001</span></span></td>
<td><span data-ttu-id="0353b-199">电</span><span class="sxs-lookup"><span data-stu-id="0353b-199">Electricity</span></span></td>
<td><span data-ttu-id="0353b-200">未分类</span><span class="sxs-lookup"><span data-stu-id="0353b-200">Unclassified</span></span></td>
<td><span data-ttu-id="0353b-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-201">-10,000.00</span></span></td>
<td><span data-ttu-id="0353b-202">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-203">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-203">CC099</span></span></td>
<td><span data-ttu-id="0353b-204">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-204">Default cost center</span></span></td>
<td><span data-ttu-id="0353b-205">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-205">10001</span></span></td>
<td><span data-ttu-id="0353b-206">电</span><span class="sxs-lookup"><span data-stu-id="0353b-206">Electricity</span></span></td>
<td><span data-ttu-id="0353b-207">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-207">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-208">1,000.00</span></span></td>
<td><span data-ttu-id="0353b-209">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-210">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-210">CC099</span></span></td>
<td><span data-ttu-id="0353b-211">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-211">Default cost center</span></span></td>
<td><span data-ttu-id="0353b-212">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-212">10001</span></span></td>
<td><span data-ttu-id="0353b-213">电</span><span class="sxs-lookup"><span data-stu-id="0353b-213">Electricity</span></span></td>
<td><span data-ttu-id="0353b-214">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-214">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-215">9,000.00</span></span></td>
<td><span data-ttu-id="0353b-216">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-217">有关详细信息，请参阅[创建成本行为策略并将其分配到成本控制单元](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)。</span><span class="sxs-lookup"><span data-stu-id="0353b-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="0353b-218">步骤 2：处理成本分配计算</span><span class="sxs-lookup"><span data-stu-id="0353b-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="0353b-219">成本分配用于通过应用相关的分摊基数将成本从一个成本对象重新分配到一个或多个其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="0353b-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="0353b-220">成本分配和成本分摊的不同之处在于，成本分配始终发生在原始成本的主要成本元素级别。</span><span class="sxs-lookup"><span data-stu-id="0353b-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="0353b-221">定义成本分配规则</span><span class="sxs-lookup"><span data-stu-id="0353b-221">Define the cost distribution rule</span></span>

<span data-ttu-id="0353b-222">在财务会计中，电成本通常登记为总计。</span><span class="sxs-lookup"><span data-stu-id="0353b-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="0353b-223">在成本核算中，此方法不足够详细。</span><span class="sxs-lookup"><span data-stu-id="0353b-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="0353b-224">可变成本应公平分配到各个成本对象。</span><span class="sxs-lookup"><span data-stu-id="0353b-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="0353b-225">最合理的分配基础是电的消耗量 (Kwh)。</span><span class="sxs-lookup"><span data-stu-id="0353b-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="0353b-226">创建名为“电”的统计维度成员并记录电的消耗量。</span><span class="sxs-lookup"><span data-stu-id="0353b-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="0353b-227">默认情况下，所有统计维度成员均可作为分配基础。</span><span class="sxs-lookup"><span data-stu-id="0353b-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-228">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-228">Cost object</span></span></th>
<th><span data-ttu-id="0353b-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="0353b-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-230">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-230">CC001</span></span></td>
<td><span data-ttu-id="0353b-231">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-231">HR</span></span></td>
<td><span data-ttu-id="0353b-232">1,000</span><span class="sxs-lookup"><span data-stu-id="0353b-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-233">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-233">CC002</span></span></td>
<td><span data-ttu-id="0353b-234">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-234">Finance</span></span></td>
<td><span data-ttu-id="0353b-235">6,000</span><span class="sxs-lookup"><span data-stu-id="0353b-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-236">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-236">CC003</span></span></td>
<td><span data-ttu-id="0353b-237">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-237">Assembly</span></span></td>
<td><span data-ttu-id="0353b-238">0</span><span class="sxs-lookup"><span data-stu-id="0353b-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-239">下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="0353b-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-240">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-240">Cost object</span></span></th>
<th><span data-ttu-id="0353b-241">度量值</span><span class="sxs-lookup"><span data-stu-id="0353b-241">Magnitude</span></span></th>
<th><span data-ttu-id="0353b-242">分配系数</span><span class="sxs-lookup"><span data-stu-id="0353b-242">Allocation factor</span></span></th>
<th><span data-ttu-id="0353b-243">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-244">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-244">CC001</span></span></td>
<td><span data-ttu-id="0353b-245">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-245">HR</span></span></td>
<td><span data-ttu-id="0353b-246">1,000</span><span class="sxs-lookup"><span data-stu-id="0353b-246">1,000</span></span></td>
<td><span data-ttu-id="0353b-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="0353b-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="0353b-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-249">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-249">CC002</span></span></td>
<td><span data-ttu-id="0353b-250">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-250">Finance</span></span></td>
<td><span data-ttu-id="0353b-251">6,000</span><span class="sxs-lookup"><span data-stu-id="0353b-251">6,000</span></span></td>
<td><span data-ttu-id="0353b-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="0353b-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="0353b-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-254">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-254">CC003</span></span></td>
<td><span data-ttu-id="0353b-255">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-255">Assembly</span></span></td>
<td><span data-ttu-id="0353b-256">0</span><span class="sxs-lookup"><span data-stu-id="0353b-256">0</span></span></td>
<td><span data-ttu-id="0353b-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="0353b-258">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-259">固定成本应平均分配到消耗了电的单个成本对象。</span><span class="sxs-lookup"><span data-stu-id="0353b-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="0353b-260">可以通过在公式分配基础中使用电统计维度成员取得此结果：（电 &gt; 0.00）下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="0353b-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-261">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-261">Cost object</span></span></th>
<th><span data-ttu-id="0353b-262">配方</span><span class="sxs-lookup"><span data-stu-id="0353b-262">Formula</span></span></th>
<th><span data-ttu-id="0353b-263">度量值</span><span class="sxs-lookup"><span data-stu-id="0353b-263">Magnitude</span></span></th>
<th><span data-ttu-id="0353b-264">分配系数</span><span class="sxs-lookup"><span data-stu-id="0353b-264">Allocation factor</span></span></th>
<th><span data-ttu-id="0353b-265">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-266">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-266">CC001</span></span></td>
<td><span data-ttu-id="0353b-267">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-267">HR</span></span></td>
<td><span data-ttu-id="0353b-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="0353b-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="0353b-269">1</span><span class="sxs-lookup"><span data-stu-id="0353b-269">1</span></span></td>
<td><span data-ttu-id="0353b-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="0353b-271">500.00</span><span class="sxs-lookup"><span data-stu-id="0353b-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-272">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-272">CC002</span></span></td>
<td><span data-ttu-id="0353b-273">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-273">Finance</span></span></td>
<td><span data-ttu-id="0353b-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="0353b-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="0353b-275">1</span><span class="sxs-lookup"><span data-stu-id="0353b-275">1</span></span></td>
<td><span data-ttu-id="0353b-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="0353b-277">500.00</span><span class="sxs-lookup"><span data-stu-id="0353b-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-278">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-278">CC003</span></span></td>
<td><span data-ttu-id="0353b-279">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-279">Assembly</span></span></td>
<td><span data-ttu-id="0353b-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="0353b-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="0353b-281">0</span><span class="sxs-lookup"><span data-stu-id="0353b-281">0</span></span></td>
<td><span data-ttu-id="0353b-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="0353b-283">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="0353b-284">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0353b-285">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-285">Journal</span></span></th>
<th><span data-ttu-id="0353b-286">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="0353b-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0353b-287">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="0353b-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0353b-288">版本</span><span class="sxs-lookup"><span data-stu-id="0353b-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-289">00002</span><span class="sxs-lookup"><span data-stu-id="0353b-289">00002</span></span></td>
<td><span data-ttu-id="0353b-290">成本分配计算日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="0353b-291">会计</span><span class="sxs-lookup"><span data-stu-id="0353b-291">Fiscal</span></span></td>
<td><span data-ttu-id="0353b-292">2017</span><span class="sxs-lookup"><span data-stu-id="0353b-292">2017</span></span></td>
<td><span data-ttu-id="0353b-293">期间 1</span><span class="sxs-lookup"><span data-stu-id="0353b-293">Period 1</span></span></td>
<td><span data-ttu-id="0353b-294">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="0353b-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="0353b-295">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="0353b-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0353b-296">会计日期</span><span class="sxs-lookup"><span data-stu-id="0353b-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-297">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-298">成本元素</span><span class="sxs-lookup"><span data-stu-id="0353b-298">Cost element</span></span></th>
<th><span data-ttu-id="0353b-299">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-299">Cost behavior</span></span></th>
<th><span data-ttu-id="0353b-300">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-301">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-302">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-302">CC099</span></span></td>
<td><span data-ttu-id="0353b-303">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-303">Default cost center</span></span></td>
<td><span data-ttu-id="0353b-304">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-304">10001</span></span></td>
<td><span data-ttu-id="0353b-305">电</span><span class="sxs-lookup"><span data-stu-id="0353b-305">Electricity</span></span></td>
<td><span data-ttu-id="0353b-306">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-306">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-308">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-309">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-309">CC099</span></span></td>
<td><span data-ttu-id="0353b-310">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-310">Default cost center</span></span></td>
<td><span data-ttu-id="0353b-311">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-311">10001</span></span></td>
<td><span data-ttu-id="0353b-312">电</span><span class="sxs-lookup"><span data-stu-id="0353b-312">Electricity</span></span></td>
<td><span data-ttu-id="0353b-313">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-313">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0353b-315">成本条目</span><span class="sxs-lookup"><span data-stu-id="0353b-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-316">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-317">成本元素</span><span class="sxs-lookup"><span data-stu-id="0353b-317">Cost element</span></span></th>
<th><span data-ttu-id="0353b-318">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-318">Cost behavior</span></span></th>
<th><span data-ttu-id="0353b-319">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-319">Amount</span></span></th>
<th><span data-ttu-id="0353b-320">会计日期</span><span class="sxs-lookup"><span data-stu-id="0353b-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-321">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-321">CC099</span></span></td>
<td><span data-ttu-id="0353b-322">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-322">Default cost center</span></span></td>
<td><span data-ttu-id="0353b-323">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-323">10001</span></span></td>
<td><span data-ttu-id="0353b-324">电</span><span class="sxs-lookup"><span data-stu-id="0353b-324">Electricity</span></span></td>
<td><span data-ttu-id="0353b-325">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-325">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-326">-1,000.00</span></span></td>
<td><span data-ttu-id="0353b-327">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-328">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-328">CC001</span></span></td>
<td><span data-ttu-id="0353b-329">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-329">HR</span></span></td>
<td><span data-ttu-id="0353b-330">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-330">10001</span></span></td>
<td><span data-ttu-id="0353b-331">电</span><span class="sxs-lookup"><span data-stu-id="0353b-331">Electricity</span></span></td>
<td><span data-ttu-id="0353b-332">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-332">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-333">500.00</span><span class="sxs-lookup"><span data-stu-id="0353b-333">500.00</span></span></td>
<td><span data-ttu-id="0353b-334">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-335">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-335">CC002</span></span></td>
<td><span data-ttu-id="0353b-336">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-336">Finance</span></span></td>
<td><span data-ttu-id="0353b-337">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-337">10001</span></span></td>
<td><span data-ttu-id="0353b-338">电</span><span class="sxs-lookup"><span data-stu-id="0353b-338">Electricity</span></span></td>
<td><span data-ttu-id="0353b-339">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-339">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-340">500.00</span><span class="sxs-lookup"><span data-stu-id="0353b-340">500.00</span></span></td>
<td><span data-ttu-id="0353b-341">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-342">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-342">CC099</span></span></td>
<td><span data-ttu-id="0353b-343">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="0353b-343">Default cost center</span></span></td>
<td><span data-ttu-id="0353b-344">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-344">10001</span></span></td>
<td><span data-ttu-id="0353b-345">电</span><span class="sxs-lookup"><span data-stu-id="0353b-345">Electricity</span></span></td>
<td><span data-ttu-id="0353b-346">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-346">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="0353b-347">-9,000.00</span></span></td>
<td><span data-ttu-id="0353b-348">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-349">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-349">CC001</span></span></td>
<td><span data-ttu-id="0353b-350">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-350">HR</span></span></td>
<td><span data-ttu-id="0353b-351">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-351">10001</span></span></td>
<td><span data-ttu-id="0353b-352">电</span><span class="sxs-lookup"><span data-stu-id="0353b-352">Electricity</span></span></td>
<td><span data-ttu-id="0353b-353">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-353">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="0353b-354">1,285.71</span></span></td>
<td><span data-ttu-id="0353b-355">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-356">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-356">CC002</span></span></td>
<td><span data-ttu-id="0353b-357">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-357">Finance</span></span></td>
<td><span data-ttu-id="0353b-358">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-358">10001</span></span></td>
<td><span data-ttu-id="0353b-359">电</span><span class="sxs-lookup"><span data-stu-id="0353b-359">Electricity</span></span></td>
<td><span data-ttu-id="0353b-360">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-360">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="0353b-361">7,714.29</span></span></td>
<td><span data-ttu-id="0353b-362">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-363">有关详细信息，请参阅[创建成本分配策略并将其分配到成本控制单元](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)。</span><span class="sxs-lookup"><span data-stu-id="0353b-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="0353b-364">步骤 3：处理开销比率计算</span><span class="sxs-lookup"><span data-stu-id="0353b-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="0353b-365">开销比率用于向一个或多个特定成本对象收费。</span><span class="sxs-lookup"><span data-stu-id="0353b-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="0353b-366">费用基于预先确定的成本率和来自指定的分配基础的度量值。</span><span class="sxs-lookup"><span data-stu-id="0353b-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="0353b-367">定义开销比率</span><span class="sxs-lookup"><span data-stu-id="0353b-367">Define the overhead rate</span></span>

<span data-ttu-id="0353b-368">成本对象 CC001 HR 生成一组内部项目。</span><span class="sxs-lookup"><span data-stu-id="0353b-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="0353b-369">创建名为“HR 项目”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="0353b-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-370">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-370">Cost object</span></span></th>
<th><span data-ttu-id="0353b-371">工时</span><span class="sxs-lookup"><span data-stu-id="0353b-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-372">项目 1</span><span class="sxs-lookup"><span data-stu-id="0353b-372">Proj 1</span></span></td>
<td><span data-ttu-id="0353b-373">项目 1</span><span class="sxs-lookup"><span data-stu-id="0353b-373">Project 1</span></span></td>
<td><span data-ttu-id="0353b-374">3</span><span class="sxs-lookup"><span data-stu-id="0353b-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-375">项目 2</span><span class="sxs-lookup"><span data-stu-id="0353b-375">Proj 2</span></span></td>
<td><span data-ttu-id="0353b-376">项目 2</span><span class="sxs-lookup"><span data-stu-id="0353b-376">Project 2</span></span></td>
<td><span data-ttu-id="0353b-377">1</span><span class="sxs-lookup"><span data-stu-id="0353b-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-378">成本项目份额预先确定的成本率已定义。</span><span class="sxs-lookup"><span data-stu-id="0353b-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-379">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-379">Cost object</span></span></th>
<th><span data-ttu-id="0353b-380">成本元素</span><span class="sxs-lookup"><span data-stu-id="0353b-380">Cost element</span></span></th>
<th><span data-ttu-id="0353b-381">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-381">Cost behavior</span></span></th>
<th><span data-ttu-id="0353b-382">单位</span><span class="sxs-lookup"><span data-stu-id="0353b-382">Units</span></span></th>
<th><span data-ttu-id="0353b-383">比率</span><span class="sxs-lookup"><span data-stu-id="0353b-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-384">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-384">CC001</span></span></td>
<td><span data-ttu-id="0353b-385">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-385">HR</span></span></td>
<td><span data-ttu-id="0353b-386">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-386">10001</span></span></td>
<td><span data-ttu-id="0353b-387">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-387">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-388">1</span><span class="sxs-lookup"><span data-stu-id="0353b-388">1</span></span></td>
<td><span data-ttu-id="0353b-389">10</span><span class="sxs-lookup"><span data-stu-id="0353b-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-390">下表显示 HR 项目用作分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="0353b-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-391">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-391">Cost object</span></span></th>
<th><span data-ttu-id="0353b-392">度量值</span><span class="sxs-lookup"><span data-stu-id="0353b-392">Magnitude</span></span></th>
<th><span data-ttu-id="0353b-393">成本元素</span><span class="sxs-lookup"><span data-stu-id="0353b-393">Cost element</span></span></th>
<th><span data-ttu-id="0353b-394">分配系数</span><span class="sxs-lookup"><span data-stu-id="0353b-394">Allocation factor</span></span></th>
<th><span data-ttu-id="0353b-395">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-396">项目 1</span><span class="sxs-lookup"><span data-stu-id="0353b-396">Proj 1</span></span></td>
<td><span data-ttu-id="0353b-397">项目 1</span><span class="sxs-lookup"><span data-stu-id="0353b-397">Project 1</span></span></td>
<td><span data-ttu-id="0353b-398">3</span><span class="sxs-lookup"><span data-stu-id="0353b-398">3</span></span></td>
<td><span data-ttu-id="0353b-399">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-399">10001</span></span></td>
<td><span data-ttu-id="0353b-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="0353b-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="0353b-401">30.00</span><span class="sxs-lookup"><span data-stu-id="0353b-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-402">项目 2</span><span class="sxs-lookup"><span data-stu-id="0353b-402">Proj 2</span></span></td>
<td><span data-ttu-id="0353b-403">项目 2</span><span class="sxs-lookup"><span data-stu-id="0353b-403">Project 2</span></span></td>
<td><span data-ttu-id="0353b-404">1</span><span class="sxs-lookup"><span data-stu-id="0353b-404">1</span></span></td>
<td><span data-ttu-id="0353b-405">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-405">10001</span></span></td>
<td><span data-ttu-id="0353b-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="0353b-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="0353b-407">10.00</span><span class="sxs-lookup"><span data-stu-id="0353b-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="0353b-408">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0353b-409">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-409">Journal</span></span></th>
<th><span data-ttu-id="0353b-410">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="0353b-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0353b-411">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="0353b-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0353b-412">版本</span><span class="sxs-lookup"><span data-stu-id="0353b-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-413">00003</span><span class="sxs-lookup"><span data-stu-id="0353b-413">00003</span></span></td>
<td><span data-ttu-id="0353b-414">开销比率计算日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="0353b-415">会计</span><span class="sxs-lookup"><span data-stu-id="0353b-415">Fiscal</span></span></td>
<td><span data-ttu-id="0353b-416">2017</span><span class="sxs-lookup"><span data-stu-id="0353b-416">2017</span></span></td>
<td><span data-ttu-id="0353b-417">期间 1</span><span class="sxs-lookup"><span data-stu-id="0353b-417">Period 1</span></span></td>
<td><span data-ttu-id="0353b-418">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="0353b-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="0353b-419">日记帐条目（开销比率计算的日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="0353b-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0353b-420">会计日期</span><span class="sxs-lookup"><span data-stu-id="0353b-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-421">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-421">Cost object</span></span></th>
<th><span data-ttu-id="0353b-422">度量值</span><span class="sxs-lookup"><span data-stu-id="0353b-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-423">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-424">项目 1</span><span class="sxs-lookup"><span data-stu-id="0353b-424">Proj 1</span></span></td>
<td><span data-ttu-id="0353b-425">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="0353b-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="0353b-426">3.00</span><span class="sxs-lookup"><span data-stu-id="0353b-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-427">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-428">项目 2</span><span class="sxs-lookup"><span data-stu-id="0353b-428">Proj 2</span></span></td>
<td><span data-ttu-id="0353b-429">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="0353b-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="0353b-430">1.00</span><span class="sxs-lookup"><span data-stu-id="0353b-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0353b-431">成本条目</span><span class="sxs-lookup"><span data-stu-id="0353b-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-432">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-433">成本元素</span><span class="sxs-lookup"><span data-stu-id="0353b-433">Cost element</span></span></th>
<th><span data-ttu-id="0353b-434">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-434">Cost behavior</span></span></th>
<th><span data-ttu-id="0353b-435">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-435">Amount</span></span></th>
<th><span data-ttu-id="0353b-436">会计日期</span><span class="sxs-lookup"><span data-stu-id="0353b-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="0353b-437">CC0001</span></span></td>
<td><span data-ttu-id="0353b-438">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-438">HR</span></span></td>
<td><span data-ttu-id="0353b-439">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-439">10001</span></span></td>
<td><span data-ttu-id="0353b-440">电</span><span class="sxs-lookup"><span data-stu-id="0353b-440">Electricity</span></span></td>
<td><span data-ttu-id="0353b-441">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-441">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="0353b-442">-30.00</span></span></td>
<td><span data-ttu-id="0353b-443">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-444">项目 1</span><span class="sxs-lookup"><span data-stu-id="0353b-444">Proj 1</span></span></td>
<td><span data-ttu-id="0353b-445">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="0353b-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="0353b-446">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-446">10001</span></span></td>
<td><span data-ttu-id="0353b-447">电</span><span class="sxs-lookup"><span data-stu-id="0353b-447">Electricity</span></span></td>
<td><span data-ttu-id="0353b-448">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-448">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-449">30.00</span><span class="sxs-lookup"><span data-stu-id="0353b-449">30.00</span></span></td>
<td><span data-ttu-id="0353b-450">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-451">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-451">CC001</span></span></td>
<td><span data-ttu-id="0353b-452">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-452">HR</span></span></td>
<td><span data-ttu-id="0353b-453">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-453">10001</span></span></td>
<td><span data-ttu-id="0353b-454">电</span><span class="sxs-lookup"><span data-stu-id="0353b-454">Electricity</span></span></td>
<td><span data-ttu-id="0353b-455">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-455">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="0353b-456">-10.00</span></span></td>
<td><span data-ttu-id="0353b-457">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-458">项目 2</span><span class="sxs-lookup"><span data-stu-id="0353b-458">Proj 2</span></span></td>
<td><span data-ttu-id="0353b-459">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="0353b-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="0353b-460">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-460">10001</span></span></td>
<td><span data-ttu-id="0353b-461">电</span><span class="sxs-lookup"><span data-stu-id="0353b-461">Electricity</span></span></td>
<td><span data-ttu-id="0353b-462">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-462">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-463">10.00</span><span class="sxs-lookup"><span data-stu-id="0353b-463">10.00</span></span></td>
<td><span data-ttu-id="0353b-464">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-465">有关详细信息，请参阅 [执行开销计算](cost-rollup.md#perform-overhead-calculation)。</span><span class="sxs-lookup"><span data-stu-id="0353b-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="0353b-466">步骤 4：处理成本分摊计算</span><span class="sxs-lookup"><span data-stu-id="0353b-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="0353b-467">分摊用于通过应用分配基础将成本对象的余额分配给其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="0353b-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="0353b-468">Finance 支持互惠分摊方法。</span><span class="sxs-lookup"><span data-stu-id="0353b-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="0353b-469">在互惠分摊方法中，辅助成本对象交换的互助服务被完全识别。</span><span class="sxs-lookup"><span data-stu-id="0353b-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="0353b-470">系统自动确定执行分摊的正确顺序。</span><span class="sxs-lookup"><span data-stu-id="0353b-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="0353b-471">成本对象的余额按单一分配基础分配。</span><span class="sxs-lookup"><span data-stu-id="0353b-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="0353b-472">支持跨成本对象维度及其各自成员的分摊。</span><span class="sxs-lookup"><span data-stu-id="0353b-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="0353b-473">分摊顺序由成本控制单元控制。</span><span class="sxs-lookup"><span data-stu-id="0353b-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="0353b-474">[![互惠方法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="0353b-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="0353b-475">定义成本分摊</span><span class="sxs-lookup"><span data-stu-id="0353b-475">Define the cost allocation</span></span>

<span data-ttu-id="0353b-476">这是说明如何跟踪成本流的简单示例。</span><span class="sxs-lookup"><span data-stu-id="0353b-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="0353b-477">成本对象 CC001 HR 生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="0353b-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="0353b-478">创建名为“HR 服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="0353b-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-479">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-479">Cost object</span></span></th>
<th><span data-ttu-id="0353b-480">HR 服务</span><span class="sxs-lookup"><span data-stu-id="0353b-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-481">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-481">CC002</span></span></td>
<td><span data-ttu-id="0353b-482">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-482">Finance</span></span></td>
<td><span data-ttu-id="0353b-483">35</span><span class="sxs-lookup"><span data-stu-id="0353b-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-484">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-484">CC003</span></span></td>
<td><span data-ttu-id="0353b-485">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-485">Assembly</span></span></td>
<td><span data-ttu-id="0353b-486">55</span><span class="sxs-lookup"><span data-stu-id="0353b-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-487">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-487">CC004</span></span></td>
<td><span data-ttu-id="0353b-488">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-488">Packaging</span></span></td>
<td><span data-ttu-id="0353b-489">10</span><span class="sxs-lookup"><span data-stu-id="0353b-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-490">成本对象 CC002 财务生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="0353b-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="0353b-491">创建名为“财务服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="0353b-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-492">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-492">Cost object</span></span></th>
<th><span data-ttu-id="0353b-493">财务服务</span><span class="sxs-lookup"><span data-stu-id="0353b-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-494">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-494">CC003</span></span></td>
<td><span data-ttu-id="0353b-495">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-495">Assembly</span></span></td>
<td><span data-ttu-id="0353b-496">65</span><span class="sxs-lookup"><span data-stu-id="0353b-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-497">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-497">CC004</span></span></td>
<td><span data-ttu-id="0353b-498">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-498">Packaging</span></span></td>
<td><span data-ttu-id="0353b-499">35</span><span class="sxs-lookup"><span data-stu-id="0353b-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-500">成本对象 CC003 装配生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="0353b-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="0353b-501">创建名为“装配服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="0353b-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-502">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-502">Cost object</span></span></th>
<th><span data-ttu-id="0353b-503">装配服务（小时）</span><span class="sxs-lookup"><span data-stu-id="0353b-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-504">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-504">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-505">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-505">Product 1</span></span></td>
<td><span data-ttu-id="0353b-506">60</span><span class="sxs-lookup"><span data-stu-id="0353b-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-507">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-507">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-508">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-508">Product 2</span></span></td>
<td><span data-ttu-id="0353b-509">20</span><span class="sxs-lookup"><span data-stu-id="0353b-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-510">成本对象 CC004 包装生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="0353b-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="0353b-511">创建名为“包装服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="0353b-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-512">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-512">Cost object</span></span></th>
<th><span data-ttu-id="0353b-513">包装服务（小时）</span><span class="sxs-lookup"><span data-stu-id="0353b-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-514">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-514">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-515">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-515">Product 1</span></span></td>
<td><span data-ttu-id="0353b-516">80</span><span class="sxs-lookup"><span data-stu-id="0353b-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-517">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-517">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-518">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-518">Product 2</span></span></td>
<td><span data-ttu-id="0353b-519">15</span><span class="sxs-lookup"><span data-stu-id="0353b-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="0353b-520">产品消耗的生产工时等统计度量可以派生自源数据。</span><span class="sxs-lookup"><span data-stu-id="0353b-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="0353b-521">有关详细信息，请参阅[统计度量提供方模板](statistical-measure-provider-template.md#statistical-measure-provider-template)。</span><span class="sxs-lookup"><span data-stu-id="0353b-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="0353b-522">下表显示当 HR 服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="0353b-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-523">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-523">Cost object</span></span></th>
<th><span data-ttu-id="0353b-524">度量值</span><span class="sxs-lookup"><span data-stu-id="0353b-524">Magnitude</span></span></th>
<th><span data-ttu-id="0353b-525">分配系数</span><span class="sxs-lookup"><span data-stu-id="0353b-525">Allocation factor</span></span></th>
<th><span data-ttu-id="0353b-526">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-526">Amount</span></span></th>
<th><span data-ttu-id="0353b-527">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-528">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-528">CC002</span></span></td>
<td><span data-ttu-id="0353b-529">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-529">Finance</span></span></td>
<td><span data-ttu-id="0353b-530">35</span><span class="sxs-lookup"><span data-stu-id="0353b-530">35</span></span></td>
<td><span data-ttu-id="0353b-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="0353b-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="0353b-532">175.00</span><span class="sxs-lookup"><span data-stu-id="0353b-532">175.00</span></span></td>
<td><span data-ttu-id="0353b-533">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-534">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-534">CC003</span></span></td>
<td><span data-ttu-id="0353b-535">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-535">Assembly</span></span></td>
<td><span data-ttu-id="0353b-536">55</span><span class="sxs-lookup"><span data-stu-id="0353b-536">55</span></span></td>
<td><span data-ttu-id="0353b-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="0353b-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="0353b-538">275.00</span><span class="sxs-lookup"><span data-stu-id="0353b-538">275.00</span></span></td>
<td><span data-ttu-id="0353b-539">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-540">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-540">CC004</span></span></td>
<td><span data-ttu-id="0353b-541">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-541">Packaging</span></span></td>
<td><span data-ttu-id="0353b-542">10</span><span class="sxs-lookup"><span data-stu-id="0353b-542">10</span></span></td>
<td><span data-ttu-id="0353b-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="0353b-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="0353b-544">50.00</span><span class="sxs-lookup"><span data-stu-id="0353b-544">50.00</span></span></td>
<td><span data-ttu-id="0353b-545">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-546">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-546">CC002</span></span></td>
<td><span data-ttu-id="0353b-547">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-547">Finance</span></span></td>
<td><span data-ttu-id="0353b-548">35</span><span class="sxs-lookup"><span data-stu-id="0353b-548">35</span></span></td>
<td><span data-ttu-id="0353b-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="0353b-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="0353b-550">436.00</span><span class="sxs-lookup"><span data-stu-id="0353b-550">436.00</span></span></td>
<td><span data-ttu-id="0353b-551">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-552">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-552">CC003</span></span></td>
<td><span data-ttu-id="0353b-553">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-553">Assembly</span></span></td>
<td><span data-ttu-id="0353b-554">55</span><span class="sxs-lookup"><span data-stu-id="0353b-554">55</span></span></td>
<td><span data-ttu-id="0353b-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="0353b-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="0353b-556">685.14</span><span class="sxs-lookup"><span data-stu-id="0353b-556">685.14</span></span></td>
<td><span data-ttu-id="0353b-557">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-558">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-558">CC004</span></span></td>
<td><span data-ttu-id="0353b-559">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-559">Packaging</span></span></td>
<td><span data-ttu-id="0353b-560">10</span><span class="sxs-lookup"><span data-stu-id="0353b-560">10</span></span></td>
<td><span data-ttu-id="0353b-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="0353b-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="0353b-562">124.57</span><span class="sxs-lookup"><span data-stu-id="0353b-562">124.57</span></span></td>
<td><span data-ttu-id="0353b-563">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-564">下表显示当财务服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="0353b-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-565">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-565">Cost object</span></span></th>
<th><span data-ttu-id="0353b-566">度量值</span><span class="sxs-lookup"><span data-stu-id="0353b-566">Magnitude</span></span></th>
<th><span data-ttu-id="0353b-567">分配系数</span><span class="sxs-lookup"><span data-stu-id="0353b-567">Allocation factor</span></span></th>
<th><span data-ttu-id="0353b-568">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-568">Amount</span></span></th>
<th><span data-ttu-id="0353b-569">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-570">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-570">CC003</span></span></td>
<td><span data-ttu-id="0353b-571">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-571">Assembly</span></span></td>
<td><span data-ttu-id="0353b-572">65</span><span class="sxs-lookup"><span data-stu-id="0353b-572">65</span></span></td>
<td><span data-ttu-id="0353b-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="0353b-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="0353b-574">438.75</span><span class="sxs-lookup"><span data-stu-id="0353b-574">438.75</span></span></td>
<td><span data-ttu-id="0353b-575">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-576">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-576">CC004</span></span></td>
<td><span data-ttu-id="0353b-577">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-577">Packaging</span></span></td>
<td><span data-ttu-id="0353b-578">35</span><span class="sxs-lookup"><span data-stu-id="0353b-578">35</span></span></td>
<td><span data-ttu-id="0353b-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="0353b-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="0353b-580">236.25</span><span class="sxs-lookup"><span data-stu-id="0353b-580">236.25</span></span></td>
<td><span data-ttu-id="0353b-581">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-582">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-582">CC003</span></span></td>
<td><span data-ttu-id="0353b-583">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-583">Assembly</span></span></td>
<td><span data-ttu-id="0353b-584">65</span><span class="sxs-lookup"><span data-stu-id="0353b-584">65</span></span></td>
<td><span data-ttu-id="0353b-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="0353b-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="0353b-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="0353b-586">5,297.69</span></span></td>
<td><span data-ttu-id="0353b-587">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-588">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-588">CC004</span></span></td>
<td><span data-ttu-id="0353b-589">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-589">Packaging</span></span></td>
<td><span data-ttu-id="0353b-590">35</span><span class="sxs-lookup"><span data-stu-id="0353b-590">35</span></span></td>
<td><span data-ttu-id="0353b-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="0353b-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="0353b-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="0353b-592">2,852.60</span></span></td>
<td><span data-ttu-id="0353b-593">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-594">下表显示当装配服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="0353b-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-595">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-595">Cost object</span></span></th>
<th><span data-ttu-id="0353b-596">度量值</span><span class="sxs-lookup"><span data-stu-id="0353b-596">Magnitude</span></span></th>
<th><span data-ttu-id="0353b-597">分配系数</span><span class="sxs-lookup"><span data-stu-id="0353b-597">Allocation factor</span></span></th>
<th><span data-ttu-id="0353b-598">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-598">Amount</span></span></th>
<th><span data-ttu-id="0353b-599">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-600">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-600">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-601">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-601">Product 1</span></span></td>
<td><span data-ttu-id="0353b-602">60</span><span class="sxs-lookup"><span data-stu-id="0353b-602">60</span></span></td>
<td><span data-ttu-id="0353b-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="0353b-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="0353b-604">535.31</span><span class="sxs-lookup"><span data-stu-id="0353b-604">535.31</span></span></td>
<td><span data-ttu-id="0353b-605">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-606">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-606">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-607">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-607">Product 2</span></span></td>
<td><span data-ttu-id="0353b-608">20</span><span class="sxs-lookup"><span data-stu-id="0353b-608">20</span></span></td>
<td><span data-ttu-id="0353b-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="0353b-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="0353b-610">178.44</span><span class="sxs-lookup"><span data-stu-id="0353b-610">178.44</span></span></td>
<td><span data-ttu-id="0353b-611">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-612">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-612">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-613">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-613">Product 1</span></span></td>
<td><span data-ttu-id="0353b-614">60</span><span class="sxs-lookup"><span data-stu-id="0353b-614">60</span></span></td>
<td><span data-ttu-id="0353b-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="0353b-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="0353b-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="0353b-616">4,487.12</span></span></td>
<td><span data-ttu-id="0353b-617">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-618">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-618">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-619">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-619">Product 2</span></span></td>
<td><span data-ttu-id="0353b-620">20</span><span class="sxs-lookup"><span data-stu-id="0353b-620">20</span></span></td>
<td><span data-ttu-id="0353b-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="0353b-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="0353b-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="0353b-622">1,495.71</span></span></td>
<td><span data-ttu-id="0353b-623">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="0353b-624">下表显示当包装服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="0353b-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-625">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-625">Cost object</span></span></th>
<th><span data-ttu-id="0353b-626">度量值</span><span class="sxs-lookup"><span data-stu-id="0353b-626">Magnitude</span></span></th>
<th><span data-ttu-id="0353b-627">分配系数</span><span class="sxs-lookup"><span data-stu-id="0353b-627">Allocation factor</span></span></th>
<th><span data-ttu-id="0353b-628">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-628">Amount</span></span></th>
<th><span data-ttu-id="0353b-629">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-630">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-630">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-631">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-631">Product 1</span></span></td>
<td><span data-ttu-id="0353b-632">80</span><span class="sxs-lookup"><span data-stu-id="0353b-632">80</span></span></td>
<td><span data-ttu-id="0353b-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="0353b-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="0353b-634">241.05</span><span class="sxs-lookup"><span data-stu-id="0353b-634">241.05</span></span></td>
<td><span data-ttu-id="0353b-635">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-636">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-636">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-637">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-637">Product 2</span></span></td>
<td><span data-ttu-id="0353b-638">15</span><span class="sxs-lookup"><span data-stu-id="0353b-638">15</span></span></td>
<td><span data-ttu-id="0353b-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="0353b-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="0353b-640">45.20</span><span class="sxs-lookup"><span data-stu-id="0353b-640">45.20</span></span></td>
<td><span data-ttu-id="0353b-641">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-642">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-642">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-643">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-643">Product 1</span></span></td>
<td><span data-ttu-id="0353b-644">80</span><span class="sxs-lookup"><span data-stu-id="0353b-644">80</span></span></td>
<td><span data-ttu-id="0353b-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="0353b-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="0353b-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="0353b-646">2,507.09</span></span></td>
<td><span data-ttu-id="0353b-647">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-648">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-648">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-649">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-649">Product 2</span></span></td>
<td><span data-ttu-id="0353b-650">15</span><span class="sxs-lookup"><span data-stu-id="0353b-650">15</span></span></td>
<td><span data-ttu-id="0353b-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="0353b-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="0353b-652">470.08</span><span class="sxs-lookup"><span data-stu-id="0353b-652">470.08</span></span></td>
<td><span data-ttu-id="0353b-653">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="0353b-654">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="0353b-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0353b-655">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-655">Journal</span></span></th>
<th><span data-ttu-id="0353b-656">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="0353b-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="0353b-657">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="0353b-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="0353b-658">版本</span><span class="sxs-lookup"><span data-stu-id="0353b-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-659">00004</span><span class="sxs-lookup"><span data-stu-id="0353b-659">00004</span></span></td>
<td><span data-ttu-id="0353b-660">成本分配日记帐</span><span class="sxs-lookup"><span data-stu-id="0353b-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="0353b-661">会计</span><span class="sxs-lookup"><span data-stu-id="0353b-661">Fiscal</span></span></td>
<td><span data-ttu-id="0353b-662">2017</span><span class="sxs-lookup"><span data-stu-id="0353b-662">2017</span></span></td>
<td><span data-ttu-id="0353b-663">期间 1</span><span class="sxs-lookup"><span data-stu-id="0353b-663">Period 1</span></span></td>
<td><span data-ttu-id="0353b-664">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="0353b-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="0353b-665">日记帐行</span><span class="sxs-lookup"><span data-stu-id="0353b-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0353b-666">会计日期</span><span class="sxs-lookup"><span data-stu-id="0353b-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-667">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-668">成本元素</span><span class="sxs-lookup"><span data-stu-id="0353b-668">Cost element</span></span></th>
<th><span data-ttu-id="0353b-669">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-669">Cost behavior</span></span></th>
<th><span data-ttu-id="0353b-670">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-671">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-672">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-672">CC001</span></span></td>
<td><span data-ttu-id="0353b-673">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-673">HR</span></span></td>
<td><span data-ttu-id="0353b-674">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-674">10001</span></span></td>
<td><span data-ttu-id="0353b-675">电</span><span class="sxs-lookup"><span data-stu-id="0353b-675">Electricity</span></span></td>
<td><span data-ttu-id="0353b-676">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-676">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-677">500.00</span><span class="sxs-lookup"><span data-stu-id="0353b-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-678">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-679">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-679">CC001</span></span></td>
<td><span data-ttu-id="0353b-680">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-680">HR</span></span></td>
<td><span data-ttu-id="0353b-681">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-681">10001</span></span></td>
<td><span data-ttu-id="0353b-682">电</span><span class="sxs-lookup"><span data-stu-id="0353b-682">Electricity</span></span></td>
<td><span data-ttu-id="0353b-683">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-683">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="0353b-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-685">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-686">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-686">CC002</span></span></td>
<td><span data-ttu-id="0353b-687">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-687">Finance</span></span></td>
<td><span data-ttu-id="0353b-688">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-688">10001</span></span></td>
<td><span data-ttu-id="0353b-689">电</span><span class="sxs-lookup"><span data-stu-id="0353b-689">Electricity</span></span></td>
<td><span data-ttu-id="0353b-690">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-690">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-691">675.00</span><span class="sxs-lookup"><span data-stu-id="0353b-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-692">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-693">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-693">CC002</span></span></td>
<td><span data-ttu-id="0353b-694">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-694">Finance</span></span></td>
<td><span data-ttu-id="0353b-695">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-695">10001</span></span></td>
<td><span data-ttu-id="0353b-696">电</span><span class="sxs-lookup"><span data-stu-id="0353b-696">Electricity</span></span></td>
<td><span data-ttu-id="0353b-697">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-697">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="0353b-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-699">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-700">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-700">CC003</span></span></td>
<td><span data-ttu-id="0353b-701">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-701">Assembly</span></span></td>
<td><span data-ttu-id="0353b-702">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-702">10001</span></span></td>
<td><span data-ttu-id="0353b-703">电</span><span class="sxs-lookup"><span data-stu-id="0353b-703">Electricity</span></span></td>
<td><span data-ttu-id="0353b-704">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-704">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-705">713.75</span><span class="sxs-lookup"><span data-stu-id="0353b-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-706">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-707">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-707">CC003</span></span></td>
<td><span data-ttu-id="0353b-708">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-708">Assembly</span></span></td>
<td><span data-ttu-id="0353b-709">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-709">10001</span></span></td>
<td><span data-ttu-id="0353b-710">电</span><span class="sxs-lookup"><span data-stu-id="0353b-710">Electricity</span></span></td>
<td><span data-ttu-id="0353b-711">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-711">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="0353b-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-713">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-714">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-714">CC003</span></span></td>
<td><span data-ttu-id="0353b-715">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-715">Packaging</span></span></td>
<td><span data-ttu-id="0353b-716">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-716">10001</span></span></td>
<td><span data-ttu-id="0353b-717">电</span><span class="sxs-lookup"><span data-stu-id="0353b-717">Electricity</span></span></td>
<td><span data-ttu-id="0353b-718">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-718">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-719">286.25</span><span class="sxs-lookup"><span data-stu-id="0353b-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-720">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-721">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-721">CC003</span></span></td>
<td><span data-ttu-id="0353b-722">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-722">Packaging</span></span></td>
<td><span data-ttu-id="0353b-723">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-723">10001</span></span></td>
<td><span data-ttu-id="0353b-724">电</span><span class="sxs-lookup"><span data-stu-id="0353b-724">Electricity</span></span></td>
<td><span data-ttu-id="0353b-725">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-725">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="0353b-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-727">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-728">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-728">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-729">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-729">Product 1</span></span></td>
<td><span data-ttu-id="0353b-730">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-730">10001</span></span></td>
<td><span data-ttu-id="0353b-731">电</span><span class="sxs-lookup"><span data-stu-id="0353b-731">Electricity</span></span></td>
<td><span data-ttu-id="0353b-732">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-732">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-733">776.36</span><span class="sxs-lookup"><span data-stu-id="0353b-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-734">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-735">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-735">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-736">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-736">Product 1</span></span></td>
<td><span data-ttu-id="0353b-737">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-737">10001</span></span></td>
<td><span data-ttu-id="0353b-738">电</span><span class="sxs-lookup"><span data-stu-id="0353b-738">Electricity</span></span></td>
<td><span data-ttu-id="0353b-739">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-739">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="0353b-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-741">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-742">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-742">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-743">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-743">Product 1</span></span></td>
<td><span data-ttu-id="0353b-744">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-744">10001</span></span></td>
<td><span data-ttu-id="0353b-745">电</span><span class="sxs-lookup"><span data-stu-id="0353b-745">Electricity</span></span></td>
<td><span data-ttu-id="0353b-746">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-746">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-747">223.64</span><span class="sxs-lookup"><span data-stu-id="0353b-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-748">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="0353b-749">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-749">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-750">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-750">Product 1</span></span></td>
<td><span data-ttu-id="0353b-751">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-751">10001</span></span></td>
<td><span data-ttu-id="0353b-752">电</span><span class="sxs-lookup"><span data-stu-id="0353b-752">Electricity</span></span></td>
<td><span data-ttu-id="0353b-753">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-753">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="0353b-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="0353b-755">成本条目</span><span class="sxs-lookup"><span data-stu-id="0353b-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="0353b-756">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="0353b-757">成本元素</span><span class="sxs-lookup"><span data-stu-id="0353b-757">Cost element</span></span></th>
<th><span data-ttu-id="0353b-758">成本行为</span><span class="sxs-lookup"><span data-stu-id="0353b-758">Cost behavior</span></span></th>
<th><span data-ttu-id="0353b-759">本币金额</span><span class="sxs-lookup"><span data-stu-id="0353b-759">Amount</span></span></th>
<th><span data-ttu-id="0353b-760">会计日期</span><span class="sxs-lookup"><span data-stu-id="0353b-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0353b-761">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-761">CC001</span></span></td>
<td><span data-ttu-id="0353b-762">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-762">HR</span></span></td>
<td><span data-ttu-id="0353b-763">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-763">10001</span></span></td>
<td><span data-ttu-id="0353b-764">电</span><span class="sxs-lookup"><span data-stu-id="0353b-764">Electricity</span></span></td>
<td><span data-ttu-id="0353b-765">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-765">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="0353b-766">-500.00</span></span></td>
<td><span data-ttu-id="0353b-767">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-768">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-768">CC002</span></span></td>
<td><span data-ttu-id="0353b-769">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-769">Finance</span></span></td>
<td><span data-ttu-id="0353b-770">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-770">10001</span></span></td>
<td><span data-ttu-id="0353b-771">电</span><span class="sxs-lookup"><span data-stu-id="0353b-771">Electricity</span></span></td>
<td><span data-ttu-id="0353b-772">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-772">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-773">175.00</span><span class="sxs-lookup"><span data-stu-id="0353b-773">175.00</span></span></td>
<td><span data-ttu-id="0353b-774">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-775">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-775">CC003</span></span></td>
<td><span data-ttu-id="0353b-776">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-776">Assembly</span></span></td>
<td><span data-ttu-id="0353b-777">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-777">10001</span></span></td>
<td><span data-ttu-id="0353b-778">电</span><span class="sxs-lookup"><span data-stu-id="0353b-778">Electricity</span></span></td>
<td><span data-ttu-id="0353b-779">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-779">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-780">275.00</span><span class="sxs-lookup"><span data-stu-id="0353b-780">275.00</span></span></td>
<td><span data-ttu-id="0353b-781">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-782">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-782">CC004</span></span></td>
<td><span data-ttu-id="0353b-783">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-783">Packaging</span></span></td>
<td><span data-ttu-id="0353b-784">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-784">10001</span></span></td>
<td><span data-ttu-id="0353b-785">电</span><span class="sxs-lookup"><span data-stu-id="0353b-785">Electricity</span></span></td>
<td><span data-ttu-id="0353b-786">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-786">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-787">50,00</span><span class="sxs-lookup"><span data-stu-id="0353b-787">50,00</span></span></td>
<td><span data-ttu-id="0353b-788">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-789">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-789">CC001</span></span></td>
<td><span data-ttu-id="0353b-790">HR</span><span class="sxs-lookup"><span data-stu-id="0353b-790">HR</span></span></td>
<td><span data-ttu-id="0353b-791">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-791">10001</span></span></td>
<td><span data-ttu-id="0353b-792">电</span><span class="sxs-lookup"><span data-stu-id="0353b-792">Electricity</span></span></td>
<td><span data-ttu-id="0353b-793">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-793">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="0353b-794">-1,245.71</span></span></td>
<td><span data-ttu-id="0353b-795">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-796">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-796">CC002</span></span></td>
<td><span data-ttu-id="0353b-797">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-797">Finance</span></span></td>
<td><span data-ttu-id="0353b-798">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-798">10001</span></span></td>
<td><span data-ttu-id="0353b-799">电</span><span class="sxs-lookup"><span data-stu-id="0353b-799">Electricity</span></span></td>
<td><span data-ttu-id="0353b-800">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-800">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-801">436.00</span><span class="sxs-lookup"><span data-stu-id="0353b-801">436.00</span></span></td>
<td><span data-ttu-id="0353b-802">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-803">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-803">CC003</span></span></td>
<td><span data-ttu-id="0353b-804">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-804">Assembly</span></span></td>
<td><span data-ttu-id="0353b-805">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-805">10001</span></span></td>
<td><span data-ttu-id="0353b-806">电</span><span class="sxs-lookup"><span data-stu-id="0353b-806">Electricity</span></span></td>
<td><span data-ttu-id="0353b-807">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-807">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-808">685.14</span><span class="sxs-lookup"><span data-stu-id="0353b-808">685.14</span></span></td>
<td><span data-ttu-id="0353b-809">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-810">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-810">CC004</span></span></td>
<td><span data-ttu-id="0353b-811">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-811">Packaging</span></span></td>
<td><span data-ttu-id="0353b-812">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-812">10001</span></span></td>
<td><span data-ttu-id="0353b-813">电</span><span class="sxs-lookup"><span data-stu-id="0353b-813">Electricity</span></span></td>
<td><span data-ttu-id="0353b-814">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-814">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-815">124.57</span><span class="sxs-lookup"><span data-stu-id="0353b-815">124.57</span></span></td>
<td><span data-ttu-id="0353b-816">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-817">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-817">CC002</span></span></td>
<td><span data-ttu-id="0353b-818">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-818">Finance</span></span></td>
<td><span data-ttu-id="0353b-819">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-819">10001</span></span></td>
<td><span data-ttu-id="0353b-820">电</span><span class="sxs-lookup"><span data-stu-id="0353b-820">Electricity</span></span></td>
<td><span data-ttu-id="0353b-821">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-821">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="0353b-822">-675.00</span></span></td>
<td><span data-ttu-id="0353b-823">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-824">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-824">CC003</span></span></td>
<td><span data-ttu-id="0353b-825">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-825">Assembly</span></span></td>
<td><span data-ttu-id="0353b-826">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-826">10001</span></span></td>
<td><span data-ttu-id="0353b-827">电</span><span class="sxs-lookup"><span data-stu-id="0353b-827">Electricity</span></span></td>
<td><span data-ttu-id="0353b-828">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-828">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-829">438.75</span><span class="sxs-lookup"><span data-stu-id="0353b-829">438.75</span></span></td>
<td><span data-ttu-id="0353b-830">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-831">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-831">CC004</span></span></td>
<td><span data-ttu-id="0353b-832">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-832">Packaging</span></span></td>
<td><span data-ttu-id="0353b-833">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-833">10001</span></span></td>
<td><span data-ttu-id="0353b-834">电</span><span class="sxs-lookup"><span data-stu-id="0353b-834">Electricity</span></span></td>
<td><span data-ttu-id="0353b-835">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-835">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-836">236.25</span><span class="sxs-lookup"><span data-stu-id="0353b-836">236.25</span></span></td>
<td><span data-ttu-id="0353b-837">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-838">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-838">CC002</span></span></td>
<td><span data-ttu-id="0353b-839">财务</span><span class="sxs-lookup"><span data-stu-id="0353b-839">Finance</span></span></td>
<td><span data-ttu-id="0353b-840">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-840">10001</span></span></td>
<td><span data-ttu-id="0353b-841">电</span><span class="sxs-lookup"><span data-stu-id="0353b-841">Electricity</span></span></td>
<td><span data-ttu-id="0353b-842">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-842">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="0353b-843">-8,150.29</span></span></td>
<td><span data-ttu-id="0353b-844">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-845">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-845">CC003</span></span></td>
<td><span data-ttu-id="0353b-846">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-846">Assembly</span></span></td>
<td><span data-ttu-id="0353b-847">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-847">10001</span></span></td>
<td><span data-ttu-id="0353b-848">电</span><span class="sxs-lookup"><span data-stu-id="0353b-848">Electricity</span></span></td>
<td><span data-ttu-id="0353b-849">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-849">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="0353b-850">5,297.69</span></span></td>
<td><span data-ttu-id="0353b-851">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-852">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-852">CC004</span></span></td>
<td><span data-ttu-id="0353b-853">包装</span><span class="sxs-lookup"><span data-stu-id="0353b-853">Packaging</span></span></td>
<td><span data-ttu-id="0353b-854">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-854">10001</span></span></td>
<td><span data-ttu-id="0353b-855">电</span><span class="sxs-lookup"><span data-stu-id="0353b-855">Electricity</span></span></td>
<td><span data-ttu-id="0353b-856">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-856">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="0353b-857">2,852.60</span></span></td>
<td><span data-ttu-id="0353b-858">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-859">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-859">CC003</span></span></td>
<td><span data-ttu-id="0353b-860">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-860">Assembly</span></span></td>
<td><span data-ttu-id="0353b-861">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-861">10001</span></span></td>
<td><span data-ttu-id="0353b-862">电</span><span class="sxs-lookup"><span data-stu-id="0353b-862">Electricity</span></span></td>
<td><span data-ttu-id="0353b-863">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-863">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="0353b-864">-713.75</span></span></td>
<td><span data-ttu-id="0353b-865">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-866">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-866">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-867">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-867">Product 1</span></span></td>
<td><span data-ttu-id="0353b-868">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-868">10001</span></span></td>
<td><span data-ttu-id="0353b-869">电</span><span class="sxs-lookup"><span data-stu-id="0353b-869">Electricity</span></span></td>
<td><span data-ttu-id="0353b-870">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-870">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-871">535.31</span><span class="sxs-lookup"><span data-stu-id="0353b-871">535.31</span></span></td>
<td><span data-ttu-id="0353b-872">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-873">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-873">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-874">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-874">Product 2</span></span></td>
<td><span data-ttu-id="0353b-875">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-875">10001</span></span></td>
<td><span data-ttu-id="0353b-876">电</span><span class="sxs-lookup"><span data-stu-id="0353b-876">Electricity</span></span></td>
<td><span data-ttu-id="0353b-877">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-877">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-878">178.44</span><span class="sxs-lookup"><span data-stu-id="0353b-878">178.44</span></span></td>
<td><span data-ttu-id="0353b-879">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-880">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-880">CC003</span></span></td>
<td><span data-ttu-id="0353b-881">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-881">Assembly</span></span></td>
<td><span data-ttu-id="0353b-882">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-882">10001</span></span></td>
<td><span data-ttu-id="0353b-883">电</span><span class="sxs-lookup"><span data-stu-id="0353b-883">Electricity</span></span></td>
<td><span data-ttu-id="0353b-884">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-884">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="0353b-885">-5,982.83</span></span></td>
<td><span data-ttu-id="0353b-886">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-887">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-887">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-888">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-888">Product 1</span></span></td>
<td><span data-ttu-id="0353b-889">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-889">10001</span></span></td>
<td><span data-ttu-id="0353b-890">电</span><span class="sxs-lookup"><span data-stu-id="0353b-890">Electricity</span></span></td>
<td><span data-ttu-id="0353b-891">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-891">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="0353b-892">4,487.12</span></span></td>
<td><span data-ttu-id="0353b-893">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-894">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-894">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-895">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-895">Product 2</span></span></td>
<td><span data-ttu-id="0353b-896">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-896">10001</span></span></td>
<td><span data-ttu-id="0353b-897">电</span><span class="sxs-lookup"><span data-stu-id="0353b-897">Electricity</span></span></td>
<td><span data-ttu-id="0353b-898">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-898">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="0353b-899">1,495.71</span></span></td>
<td><span data-ttu-id="0353b-900">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-901">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-901">CC003</span></span></td>
<td><span data-ttu-id="0353b-902">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-902">Assembly</span></span></td>
<td><span data-ttu-id="0353b-903">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-903">10001</span></span></td>
<td><span data-ttu-id="0353b-904">电</span><span class="sxs-lookup"><span data-stu-id="0353b-904">Electricity</span></span></td>
<td><span data-ttu-id="0353b-905">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-905">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="0353b-906">-286.25</span></span></td>
<td><span data-ttu-id="0353b-907">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-908">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-908">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-909">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-909">Product 1</span></span></td>
<td><span data-ttu-id="0353b-910">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-910">10001</span></span></td>
<td><span data-ttu-id="0353b-911">电</span><span class="sxs-lookup"><span data-stu-id="0353b-911">Electricity</span></span></td>
<td><span data-ttu-id="0353b-912">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-912">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-913">241.05</span><span class="sxs-lookup"><span data-stu-id="0353b-913">241.05</span></span></td>
<td><span data-ttu-id="0353b-914">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-915">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-915">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-916">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-916">Product 2</span></span></td>
<td><span data-ttu-id="0353b-917">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-917">10001</span></span></td>
<td><span data-ttu-id="0353b-918">电</span><span class="sxs-lookup"><span data-stu-id="0353b-918">Electricity</span></span></td>
<td><span data-ttu-id="0353b-919">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-919">Fixed cost</span></span></td>
<td><span data-ttu-id="0353b-920">45.20</span><span class="sxs-lookup"><span data-stu-id="0353b-920">45.20</span></span></td>
<td><span data-ttu-id="0353b-921">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-922">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-922">CC003</span></span></td>
<td><span data-ttu-id="0353b-923">程序集</span><span class="sxs-lookup"><span data-stu-id="0353b-923">Assembly</span></span></td>
<td><span data-ttu-id="0353b-924">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-924">10001</span></span></td>
<td><span data-ttu-id="0353b-925">电</span><span class="sxs-lookup"><span data-stu-id="0353b-925">Electricity</span></span></td>
<td><span data-ttu-id="0353b-926">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-926">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="0353b-927">-2,977.17</span></span></td>
<td><span data-ttu-id="0353b-928">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-929">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-929">Prod 1</span></span></td>
<td><span data-ttu-id="0353b-930">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-930">Product 1</span></span></td>
<td><span data-ttu-id="0353b-931">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-931">10001</span></span></td>
<td><span data-ttu-id="0353b-932">电</span><span class="sxs-lookup"><span data-stu-id="0353b-932">Electricity</span></span></td>
<td><span data-ttu-id="0353b-933">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-933">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="0353b-934">2,507.09</span></span></td>
<td><span data-ttu-id="0353b-935">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0353b-936">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-936">Prod 2</span></span></td>
<td><span data-ttu-id="0353b-937">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-937">Product 2</span></span></td>
<td><span data-ttu-id="0353b-938">10001</span><span class="sxs-lookup"><span data-stu-id="0353b-938">10001</span></span></td>
<td><span data-ttu-id="0353b-939">电</span><span class="sxs-lookup"><span data-stu-id="0353b-939">Electricity</span></span></td>
<td><span data-ttu-id="0353b-940">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-940">Variable cost</span></span></td>
<td><span data-ttu-id="0353b-941">470.08</span><span class="sxs-lookup"><span data-stu-id="0353b-941">470.08</span></span></td>
<td><span data-ttu-id="0353b-942">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0353b-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="0353b-943">结论</span><span class="sxs-lookup"><span data-stu-id="0353b-943">Conclusion</span></span>
<span data-ttu-id="0353b-944">在财务会计中，10,000.00 电成本过帐到虚拟成本中心 ID。</span><span class="sxs-lookup"><span data-stu-id="0353b-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="0353b-945">因此，成本会计员将了解必须分摊此成本。</span><span class="sxs-lookup"><span data-stu-id="0353b-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="0353b-946">在成本核算中，跨组织单位和级别的成本流，基于所应用的政策和规则。</span><span class="sxs-lookup"><span data-stu-id="0353b-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="0353b-947">每项成本已与为成本分摊提供最佳评估的分配基础关联。</span><span class="sxs-lookup"><span data-stu-id="0353b-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="0353b-948">成本元素</span><span class="sxs-lookup"><span data-stu-id="0353b-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="0353b-949">成本对象</span><span class="sxs-lookup"><span data-stu-id="0353b-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="0353b-950">合计</span><span class="sxs-lookup"><span data-stu-id="0353b-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="0353b-951">CC099</span><span class="sxs-lookup"><span data-stu-id="0353b-951">CC099</span></span></th>
<th><span data-ttu-id="0353b-952">CC001</span><span class="sxs-lookup"><span data-stu-id="0353b-952">CC001</span></span></th>
<th><span data-ttu-id="0353b-953">CC002</span><span class="sxs-lookup"><span data-stu-id="0353b-953">CC002</span></span></th>
<th><span data-ttu-id="0353b-954">CC003</span><span class="sxs-lookup"><span data-stu-id="0353b-954">CC003</span></span></th>
<th><span data-ttu-id="0353b-955">CC004</span><span class="sxs-lookup"><span data-stu-id="0353b-955">CC004</span></span></th>
<th><span data-ttu-id="0353b-956">项目 1</span><span class="sxs-lookup"><span data-stu-id="0353b-956">Proj 1</span></span></th>
<th><span data-ttu-id="0353b-957">项目 2</span><span class="sxs-lookup"><span data-stu-id="0353b-957">Proj 2</span></span></th>
<th><span data-ttu-id="0353b-958">产品 1</span><span class="sxs-lookup"><span data-stu-id="0353b-958">Prod 1</span></span></th>
<th><span data-ttu-id="0353b-959">产品 2</span><span class="sxs-lookup"><span data-stu-id="0353b-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="0353b-960">10001 电</span><span class="sxs-lookup"><span data-stu-id="0353b-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="0353b-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="0353b-970">未分类</span><span class="sxs-lookup"><span data-stu-id="0353b-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-971">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="0353b-972">固定成本</span><span class="sxs-lookup"><span data-stu-id="0353b-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-973">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-974">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-975">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-976">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-977">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="0353b-978">776.36</span><span class="sxs-lookup"><span data-stu-id="0353b-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-979">223.64</span><span class="sxs-lookup"><span data-stu-id="0353b-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="0353b-981">可变成本</span><span class="sxs-lookup"><span data-stu-id="0353b-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-982">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-983">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-984">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-985">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-986">0.00</span><span class="sxs-lookup"><span data-stu-id="0353b-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-987">30.00</span><span class="sxs-lookup"><span data-stu-id="0353b-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-988">10.00</span><span class="sxs-lookup"><span data-stu-id="0353b-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="0353b-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="0353b-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="0353b-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="0353b-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="0353b-992">此主题显示主要成本元素“10001 电”如何流过成本对象。</span><span class="sxs-lookup"><span data-stu-id="0353b-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="0353b-993">因此，此间接成本分摊到组织的最低级别。</span><span class="sxs-lookup"><span data-stu-id="0353b-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="0353b-994">换言之，最低级别的成本对象承担成本。</span><span class="sxs-lookup"><span data-stu-id="0353b-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="0353b-995">如果您需要成本对象之间的可视成本流，可以使用成本累积政策规则实现成本流可视化。</span><span class="sxs-lookup"><span data-stu-id="0353b-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="0353b-996">有关详细信息，请参阅[成本累积政策和开销计算](cost-rollup.md)。</span><span class="sxs-lookup"><span data-stu-id="0353b-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



