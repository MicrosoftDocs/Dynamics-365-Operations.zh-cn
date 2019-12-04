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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
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
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770796"
---
# <a name="overhead-calculation"></a><span data-ttu-id="5ac61-103">开销计算</span><span class="sxs-lookup"><span data-stu-id="5ac61-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ac61-104">此主题描述计算和分配间接成本的典型流程。</span><span class="sxs-lookup"><span data-stu-id="5ac61-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="5ac61-105">术语定义</span><span class="sxs-lookup"><span data-stu-id="5ac61-105">Term definition</span></span>
---------------

<span data-ttu-id="5ac61-106">间接成本是为业务运营支出的成本，但是不能直接归为任何具体的业务活动、产品或服务。</span><span class="sxs-lookup"><span data-stu-id="5ac61-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="5ac61-107">间接成本为营利活动的生成提供重要支持。</span><span class="sxs-lookup"><span data-stu-id="5ac61-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="5ac61-108">以下是一些开销成本示例：</span><span class="sxs-lookup"><span data-stu-id="5ac61-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="5ac61-109">租金</span><span class="sxs-lookup"><span data-stu-id="5ac61-109">Rent</span></span>
-   <span data-ttu-id="5ac61-110">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-110">Electricity</span></span>
-   <span data-ttu-id="5ac61-111">管理薪金</span><span class="sxs-lookup"><span data-stu-id="5ac61-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="5ac61-112">开销计算概览</span><span class="sxs-lookup"><span data-stu-id="5ac61-112">Overhead calculation overview</span></span>
<span data-ttu-id="5ac61-113">开销计算按正确顺序运行会计政策。</span><span class="sxs-lookup"><span data-stu-id="5ac61-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="5ac61-114">如果成本核算政策更改或检测到特定错误，您可以为同一个会计期间多次运行开销计算。</span><span class="sxs-lookup"><span data-stu-id="5ac61-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="5ac61-115">每次运行的开销计算将被存储并收到唯一版本 ID，让您可以比较各个版本的计算。</span><span class="sxs-lookup"><span data-stu-id="5ac61-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="5ac61-116">开销计算生成的成本条目接收会计日期。</span><span class="sxs-lookup"><span data-stu-id="5ac61-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="5ac61-117">此会计日期与计算中使用的会计期间的结束日期一致。</span><span class="sxs-lookup"><span data-stu-id="5ac61-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="5ac61-118">唯一版本 ID 由以下元素组成：</span><span class="sxs-lookup"><span data-stu-id="5ac61-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="5ac61-119">版本类型</span><span class="sxs-lookup"><span data-stu-id="5ac61-119">Version type</span></span>
-   <span data-ttu-id="5ac61-120">日期和时间</span><span class="sxs-lookup"><span data-stu-id="5ac61-120">Date and time</span></span>
-   <span data-ttu-id="5ac61-121">成本核算分类帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="5ac61-122">会计年度</span><span class="sxs-lookup"><span data-stu-id="5ac61-122">Fiscal year</span></span>
-   <span data-ttu-id="5ac61-123">会计期间</span><span class="sxs-lookup"><span data-stu-id="5ac61-123">Fiscal period</span></span>

<span data-ttu-id="5ac61-124">开销计算独立于版本运行。</span><span class="sxs-lookup"><span data-stu-id="5ac61-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="5ac61-125">因此，可以在实际版本前计算预算版本。</span><span class="sxs-lookup"><span data-stu-id="5ac61-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="5ac61-126">开销计算包括四个步骤，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="5ac61-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="5ac61-127">在每个步骤中，创建包含日记帐条目的日记帐标头。</span><span class="sxs-lookup"><span data-stu-id="5ac61-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="5ac61-128">此日记帐标头为每个计算步骤保留输入数据。</span><span class="sxs-lookup"><span data-stu-id="5ac61-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="5ac61-129">政策和规则应用于每个日记帐行，成本条目生成为输出。</span><span class="sxs-lookup"><span data-stu-id="5ac61-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="5ac61-130">因此，您始终具有完全的可跟踪性。</span><span class="sxs-lookup"><span data-stu-id="5ac61-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="5ac61-131">[![开销计算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="5ac61-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="5ac61-132">计算和分摊电间接成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="5ac61-133">在财务会计中，有些成本（如电）登记为总计。</span><span class="sxs-lookup"><span data-stu-id="5ac61-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="5ac61-134">因此，不为成本核算提供详细的管理洞察。</span><span class="sxs-lookup"><span data-stu-id="5ac61-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="5ac61-135">在成本核算中，为提供跨所有组织单位和级别的正确的管理洞察，成本必须流过各个组织单位。</span><span class="sxs-lookup"><span data-stu-id="5ac61-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="5ac61-136">此流必须基于消耗量的准确记录或公平评估。</span><span class="sxs-lookup"><span data-stu-id="5ac61-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="5ac61-137">在总帐中，可以过帐电成本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="5ac61-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ac61-138">会计日期</span><span class="sxs-lookup"><span data-stu-id="5ac61-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-139">成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-140">主科目</span><span class="sxs-lookup"><span data-stu-id="5ac61-140">Main account</span></span></th>
<th><span data-ttu-id="5ac61-141">按记帐币种计算的金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-142">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="5ac61-143">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-143">CC099</span></span></td>
<td><span data-ttu-id="5ac61-144">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-144">Default cost center</span></span></td>
<td><span data-ttu-id="5ac61-145">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-145">10001</span></span></td>
<td><span data-ttu-id="5ac61-146">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-146">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="5ac61-148">步骤 1：处理成本行为计算</span><span class="sxs-lookup"><span data-stu-id="5ac61-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="5ac61-149">默认情况下，当成本条目从源数据导入时，它们在成本核算中接收**未分类**成本行为分类。</span><span class="sxs-lookup"><span data-stu-id="5ac61-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="5ac61-150">通过应用成本行为政策规则，您可以将成本条目重新分类为**固定成本**或**可变成本**。</span><span class="sxs-lookup"><span data-stu-id="5ac61-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="5ac61-151">定义成本行为规则</span><span class="sxs-lookup"><span data-stu-id="5ac61-151">Define the cost behavior rule</span></span>

<span data-ttu-id="5ac61-152">在某些情况下，一部分成本是一项固定费用，其余成本基于消耗量。</span><span class="sxs-lookup"><span data-stu-id="5ac61-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="5ac61-153">通常电费帐单与此定义一致。</span><span class="sxs-lookup"><span data-stu-id="5ac61-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="5ac61-154">在支付特定固定费用后，您按千瓦时 (Kwh) 支付消耗量。</span><span class="sxs-lookup"><span data-stu-id="5ac61-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="5ac61-155">例如，如果固定成本费用为 1,000.00，以下是成本行为规则的定义：</span><span class="sxs-lookup"><span data-stu-id="5ac61-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="5ac61-156">固定金额 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="5ac61-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="5ac61-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="5ac61-158">1000,01 &lt; N = 可变</span><span class="sxs-lookup"><span data-stu-id="5ac61-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="5ac61-159">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ac61-160">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-160">Journal</span></span></th>
<th><span data-ttu-id="5ac61-161">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="5ac61-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ac61-162">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="5ac61-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ac61-163">版本</span><span class="sxs-lookup"><span data-stu-id="5ac61-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-164">00001</span><span class="sxs-lookup"><span data-stu-id="5ac61-164">00001</span></span></td>
<td><span data-ttu-id="5ac61-165">成本行为计算日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="5ac61-166">会计</span><span class="sxs-lookup"><span data-stu-id="5ac61-166">Fiscal</span></span></td>
<td><span data-ttu-id="5ac61-167">2017</span><span class="sxs-lookup"><span data-stu-id="5ac61-167">2017</span></span></td>
<td><span data-ttu-id="5ac61-168">期间 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-168">Period 1</span></span></td>
<td><span data-ttu-id="5ac61-169">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5ac61-170">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="5ac61-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ac61-171">会计日期</span><span class="sxs-lookup"><span data-stu-id="5ac61-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-172">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-173">成本元素</span><span class="sxs-lookup"><span data-stu-id="5ac61-173">Cost element</span></span></th>
<th><span data-ttu-id="5ac61-174">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-174">Cost behavior</span></span></th>
<th><span data-ttu-id="5ac61-175">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-176">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="5ac61-177">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-177">CC099</span></span></td>
<td><span data-ttu-id="5ac61-178">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-178">Default cost center</span></span></td>
<td><span data-ttu-id="5ac61-179">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-179">10001</span></span></td>
<td><span data-ttu-id="5ac61-180">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-180">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-181">未分类</span><span class="sxs-lookup"><span data-stu-id="5ac61-181">Unclassified</span></span></td>
<td><span data-ttu-id="5ac61-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ac61-183">成本条目</span><span class="sxs-lookup"><span data-stu-id="5ac61-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-184">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-185">成本元素</span><span class="sxs-lookup"><span data-stu-id="5ac61-185">Cost element</span></span></th>
<th><span data-ttu-id="5ac61-186">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-186">Cost behavior</span></span></th>
<th><span data-ttu-id="5ac61-187">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-187">Amount</span></span></th>
<th><span data-ttu-id="5ac61-188">会计日期</span><span class="sxs-lookup"><span data-stu-id="5ac61-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-189">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-189">CC099</span></span></td>
<td><span data-ttu-id="5ac61-190">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-190">Default cost center</span></span></td>
<td><span data-ttu-id="5ac61-191">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-191">10001</span></span></td>
<td><span data-ttu-id="5ac61-192">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-192">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-193">未分类</span><span class="sxs-lookup"><span data-stu-id="5ac61-193">Unclassified</span></span></td>
<td><span data-ttu-id="5ac61-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-194">10,000.00</span></span></td>
<td><span data-ttu-id="5ac61-195">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-196">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-196">CC099</span></span></td>
<td><span data-ttu-id="5ac61-197">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-197">Default cost center</span></span></td>
<td><span data-ttu-id="5ac61-198">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-198">10001</span></span></td>
<td><span data-ttu-id="5ac61-199">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-199">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-200">未分类</span><span class="sxs-lookup"><span data-stu-id="5ac61-200">Unclassified</span></span></td>
<td><span data-ttu-id="5ac61-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-201">-10,000.00</span></span></td>
<td><span data-ttu-id="5ac61-202">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-203">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-203">CC099</span></span></td>
<td><span data-ttu-id="5ac61-204">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-204">Default cost center</span></span></td>
<td><span data-ttu-id="5ac61-205">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-205">10001</span></span></td>
<td><span data-ttu-id="5ac61-206">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-206">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-207">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-207">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-208">1,000.00</span></span></td>
<td><span data-ttu-id="5ac61-209">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-210">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-210">CC099</span></span></td>
<td><span data-ttu-id="5ac61-211">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-211">Default cost center</span></span></td>
<td><span data-ttu-id="5ac61-212">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-212">10001</span></span></td>
<td><span data-ttu-id="5ac61-213">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-213">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-214">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-214">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-215">9,000.00</span></span></td>
<td><span data-ttu-id="5ac61-216">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-217">有关详细信息，请参阅[创建成本行为策略并将其分配到成本控制单元](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)。</span><span class="sxs-lookup"><span data-stu-id="5ac61-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="5ac61-218">步骤 2：处理成本分配计算</span><span class="sxs-lookup"><span data-stu-id="5ac61-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="5ac61-219">成本分配用于通过应用相关的分摊基数将成本从一个成本对象重新分配到一个或多个其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="5ac61-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="5ac61-220">成本分配和成本分摊的不同之处在于，成本分配始终发生在原始成本的主要成本元素级别。</span><span class="sxs-lookup"><span data-stu-id="5ac61-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="5ac61-221">定义成本分配规则</span><span class="sxs-lookup"><span data-stu-id="5ac61-221">Define the cost distribution rule</span></span>

<span data-ttu-id="5ac61-222">在财务会计中，电成本通常登记为总计。</span><span class="sxs-lookup"><span data-stu-id="5ac61-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="5ac61-223">在成本核算中，此方法不足够详细。</span><span class="sxs-lookup"><span data-stu-id="5ac61-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="5ac61-224">可变成本应公平分配到各个成本对象。</span><span class="sxs-lookup"><span data-stu-id="5ac61-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="5ac61-225">最合理的分配基础是电的消耗量 (Kwh)。</span><span class="sxs-lookup"><span data-stu-id="5ac61-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="5ac61-226">创建名为“电”的统计维度成员并记录电的消耗量。</span><span class="sxs-lookup"><span data-stu-id="5ac61-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="5ac61-227">默认情况下，所有统计维度成员均可作为分配基础。</span><span class="sxs-lookup"><span data-stu-id="5ac61-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-228">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-228">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="5ac61-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-230">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-230">CC001</span></span></td>
<td><span data-ttu-id="5ac61-231">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-231">HR</span></span></td>
<td><span data-ttu-id="5ac61-232">1,000</span><span class="sxs-lookup"><span data-stu-id="5ac61-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-233">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-233">CC002</span></span></td>
<td><span data-ttu-id="5ac61-234">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-234">Finance</span></span></td>
<td><span data-ttu-id="5ac61-235">6,000</span><span class="sxs-lookup"><span data-stu-id="5ac61-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-236">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-236">CC003</span></span></td>
<td><span data-ttu-id="5ac61-237">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-237">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-238">0</span><span class="sxs-lookup"><span data-stu-id="5ac61-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-239">下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="5ac61-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-240">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-240">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-241">度量值</span><span class="sxs-lookup"><span data-stu-id="5ac61-241">Magnitude</span></span></th>
<th><span data-ttu-id="5ac61-242">分配系数</span><span class="sxs-lookup"><span data-stu-id="5ac61-242">Allocation factor</span></span></th>
<th><span data-ttu-id="5ac61-243">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-244">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-244">CC001</span></span></td>
<td><span data-ttu-id="5ac61-245">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-245">HR</span></span></td>
<td><span data-ttu-id="5ac61-246">1,000</span><span class="sxs-lookup"><span data-stu-id="5ac61-246">1,000</span></span></td>
<td><span data-ttu-id="5ac61-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5ac61-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5ac61-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-249">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-249">CC002</span></span></td>
<td><span data-ttu-id="5ac61-250">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-250">Finance</span></span></td>
<td><span data-ttu-id="5ac61-251">6,000</span><span class="sxs-lookup"><span data-stu-id="5ac61-251">6,000</span></span></td>
<td><span data-ttu-id="5ac61-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5ac61-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5ac61-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-254">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-254">CC003</span></span></td>
<td><span data-ttu-id="5ac61-255">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-255">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-256">0</span><span class="sxs-lookup"><span data-stu-id="5ac61-256">0</span></span></td>
<td><span data-ttu-id="5ac61-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5ac61-258">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-259">固定成本应平均分配到消耗了电的单个成本对象。</span><span class="sxs-lookup"><span data-stu-id="5ac61-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="5ac61-260">可以通过在公式分配基础中使用电统计维度成员取得此结果：（电 &gt; 0.00）下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="5ac61-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-261">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-261">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-262">配方</span><span class="sxs-lookup"><span data-stu-id="5ac61-262">Formula</span></span></th>
<th><span data-ttu-id="5ac61-263">度量值</span><span class="sxs-lookup"><span data-stu-id="5ac61-263">Magnitude</span></span></th>
<th><span data-ttu-id="5ac61-264">分配系数</span><span class="sxs-lookup"><span data-stu-id="5ac61-264">Allocation factor</span></span></th>
<th><span data-ttu-id="5ac61-265">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-266">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-266">CC001</span></span></td>
<td><span data-ttu-id="5ac61-267">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-267">HR</span></span></td>
<td><span data-ttu-id="5ac61-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5ac61-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5ac61-269">1</span><span class="sxs-lookup"><span data-stu-id="5ac61-269">1</span></span></td>
<td><span data-ttu-id="5ac61-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5ac61-271">500.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-272">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-272">CC002</span></span></td>
<td><span data-ttu-id="5ac61-273">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-273">Finance</span></span></td>
<td><span data-ttu-id="5ac61-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5ac61-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5ac61-275">1</span><span class="sxs-lookup"><span data-stu-id="5ac61-275">1</span></span></td>
<td><span data-ttu-id="5ac61-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5ac61-277">500.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-278">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-278">CC003</span></span></td>
<td><span data-ttu-id="5ac61-279">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-279">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="5ac61-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5ac61-281">0</span><span class="sxs-lookup"><span data-stu-id="5ac61-281">0</span></span></td>
<td><span data-ttu-id="5ac61-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5ac61-283">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5ac61-284">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ac61-285">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-285">Journal</span></span></th>
<th><span data-ttu-id="5ac61-286">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="5ac61-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ac61-287">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="5ac61-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ac61-288">版本</span><span class="sxs-lookup"><span data-stu-id="5ac61-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-289">00002</span><span class="sxs-lookup"><span data-stu-id="5ac61-289">00002</span></span></td>
<td><span data-ttu-id="5ac61-290">成本分配计算日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="5ac61-291">会计</span><span class="sxs-lookup"><span data-stu-id="5ac61-291">Fiscal</span></span></td>
<td><span data-ttu-id="5ac61-292">2017</span><span class="sxs-lookup"><span data-stu-id="5ac61-292">2017</span></span></td>
<td><span data-ttu-id="5ac61-293">期间 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-293">Period 1</span></span></td>
<td><span data-ttu-id="5ac61-294">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5ac61-295">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="5ac61-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ac61-296">会计日期</span><span class="sxs-lookup"><span data-stu-id="5ac61-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-297">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-298">成本元素</span><span class="sxs-lookup"><span data-stu-id="5ac61-298">Cost element</span></span></th>
<th><span data-ttu-id="5ac61-299">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-299">Cost behavior</span></span></th>
<th><span data-ttu-id="5ac61-300">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-301">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-302">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-302">CC099</span></span></td>
<td><span data-ttu-id="5ac61-303">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-303">Default cost center</span></span></td>
<td><span data-ttu-id="5ac61-304">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-304">10001</span></span></td>
<td><span data-ttu-id="5ac61-305">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-305">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-306">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-306">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-308">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-309">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-309">CC099</span></span></td>
<td><span data-ttu-id="5ac61-310">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-310">Default cost center</span></span></td>
<td><span data-ttu-id="5ac61-311">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-311">10001</span></span></td>
<td><span data-ttu-id="5ac61-312">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-312">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-313">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-313">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ac61-315">成本条目</span><span class="sxs-lookup"><span data-stu-id="5ac61-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-316">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-317">成本元素</span><span class="sxs-lookup"><span data-stu-id="5ac61-317">Cost element</span></span></th>
<th><span data-ttu-id="5ac61-318">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-318">Cost behavior</span></span></th>
<th><span data-ttu-id="5ac61-319">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-319">Amount</span></span></th>
<th><span data-ttu-id="5ac61-320">会计日期</span><span class="sxs-lookup"><span data-stu-id="5ac61-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-321">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-321">CC099</span></span></td>
<td><span data-ttu-id="5ac61-322">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-322">Default cost center</span></span></td>
<td><span data-ttu-id="5ac61-323">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-323">10001</span></span></td>
<td><span data-ttu-id="5ac61-324">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-324">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-325">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-325">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-326">-1,000.00</span></span></td>
<td><span data-ttu-id="5ac61-327">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-328">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-328">CC001</span></span></td>
<td><span data-ttu-id="5ac61-329">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-329">HR</span></span></td>
<td><span data-ttu-id="5ac61-330">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-330">10001</span></span></td>
<td><span data-ttu-id="5ac61-331">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-331">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-332">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-332">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-333">500.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-333">500.00</span></span></td>
<td><span data-ttu-id="5ac61-334">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-335">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-335">CC002</span></span></td>
<td><span data-ttu-id="5ac61-336">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-336">Finance</span></span></td>
<td><span data-ttu-id="5ac61-337">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-337">10001</span></span></td>
<td><span data-ttu-id="5ac61-338">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-338">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-339">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-339">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-340">500.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-340">500.00</span></span></td>
<td><span data-ttu-id="5ac61-341">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-342">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-342">CC099</span></span></td>
<td><span data-ttu-id="5ac61-343">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="5ac61-343">Default cost center</span></span></td>
<td><span data-ttu-id="5ac61-344">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-344">10001</span></span></td>
<td><span data-ttu-id="5ac61-345">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-345">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-346">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-346">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-347">-9,000.00</span></span></td>
<td><span data-ttu-id="5ac61-348">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-349">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-349">CC001</span></span></td>
<td><span data-ttu-id="5ac61-350">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-350">HR</span></span></td>
<td><span data-ttu-id="5ac61-351">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-351">10001</span></span></td>
<td><span data-ttu-id="5ac61-352">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-352">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-353">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-353">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5ac61-354">1,285.71</span></span></td>
<td><span data-ttu-id="5ac61-355">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-356">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-356">CC002</span></span></td>
<td><span data-ttu-id="5ac61-357">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-357">Finance</span></span></td>
<td><span data-ttu-id="5ac61-358">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-358">10001</span></span></td>
<td><span data-ttu-id="5ac61-359">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-359">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-360">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-360">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5ac61-361">7,714.29</span></span></td>
<td><span data-ttu-id="5ac61-362">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-363">有关详细信息，请参阅[创建成本分配策略并将其分配到成本控制单元](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)。</span><span class="sxs-lookup"><span data-stu-id="5ac61-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="5ac61-364">步骤 3：处理开销比率计算</span><span class="sxs-lookup"><span data-stu-id="5ac61-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="5ac61-365">开销比率用于向一个或多个特定成本对象收费。</span><span class="sxs-lookup"><span data-stu-id="5ac61-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="5ac61-366">费用基于预先确定的成本率和来自指定的分配基础的度量值。</span><span class="sxs-lookup"><span data-stu-id="5ac61-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="5ac61-367">定义开销比率</span><span class="sxs-lookup"><span data-stu-id="5ac61-367">Define the overhead rate</span></span>

<span data-ttu-id="5ac61-368">成本对象 CC001 HR 生成一组内部项目。</span><span class="sxs-lookup"><span data-stu-id="5ac61-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="5ac61-369">创建名为“HR 项目”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="5ac61-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-370">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-370">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-371">工时</span><span class="sxs-lookup"><span data-stu-id="5ac61-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-372">项目 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-372">Proj 1</span></span></td>
<td><span data-ttu-id="5ac61-373">项目 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-373">Project 1</span></span></td>
<td><span data-ttu-id="5ac61-374">3</span><span class="sxs-lookup"><span data-stu-id="5ac61-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-375">项目 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-375">Proj 2</span></span></td>
<td><span data-ttu-id="5ac61-376">项目 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-376">Project 2</span></span></td>
<td><span data-ttu-id="5ac61-377">1</span><span class="sxs-lookup"><span data-stu-id="5ac61-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-378">成本项目份额预先确定的成本率已定义。</span><span class="sxs-lookup"><span data-stu-id="5ac61-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-379">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-379">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-380">成本元素</span><span class="sxs-lookup"><span data-stu-id="5ac61-380">Cost element</span></span></th>
<th><span data-ttu-id="5ac61-381">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-381">Cost behavior</span></span></th>
<th><span data-ttu-id="5ac61-382">单位</span><span class="sxs-lookup"><span data-stu-id="5ac61-382">Units</span></span></th>
<th><span data-ttu-id="5ac61-383">比率</span><span class="sxs-lookup"><span data-stu-id="5ac61-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-384">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-384">CC001</span></span></td>
<td><span data-ttu-id="5ac61-385">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-385">HR</span></span></td>
<td><span data-ttu-id="5ac61-386">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-386">10001</span></span></td>
<td><span data-ttu-id="5ac61-387">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-387">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-388">1</span><span class="sxs-lookup"><span data-stu-id="5ac61-388">1</span></span></td>
<td><span data-ttu-id="5ac61-389">10</span><span class="sxs-lookup"><span data-stu-id="5ac61-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-390">下表显示 HR 项目用作分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="5ac61-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-391">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-391">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-392">度量值</span><span class="sxs-lookup"><span data-stu-id="5ac61-392">Magnitude</span></span></th>
<th><span data-ttu-id="5ac61-393">成本元素</span><span class="sxs-lookup"><span data-stu-id="5ac61-393">Cost element</span></span></th>
<th><span data-ttu-id="5ac61-394">分配系数</span><span class="sxs-lookup"><span data-stu-id="5ac61-394">Allocation factor</span></span></th>
<th><span data-ttu-id="5ac61-395">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-396">项目 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-396">Proj 1</span></span></td>
<td><span data-ttu-id="5ac61-397">项目 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-397">Project 1</span></span></td>
<td><span data-ttu-id="5ac61-398">3</span><span class="sxs-lookup"><span data-stu-id="5ac61-398">3</span></span></td>
<td><span data-ttu-id="5ac61-399">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-399">10001</span></span></td>
<td><span data-ttu-id="5ac61-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5ac61-401">30.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-402">项目 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-402">Proj 2</span></span></td>
<td><span data-ttu-id="5ac61-403">项目 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-403">Project 2</span></span></td>
<td><span data-ttu-id="5ac61-404">1</span><span class="sxs-lookup"><span data-stu-id="5ac61-404">1</span></span></td>
<td><span data-ttu-id="5ac61-405">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-405">10001</span></span></td>
<td><span data-ttu-id="5ac61-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5ac61-407">10.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5ac61-408">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ac61-409">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-409">Journal</span></span></th>
<th><span data-ttu-id="5ac61-410">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="5ac61-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ac61-411">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="5ac61-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ac61-412">版本</span><span class="sxs-lookup"><span data-stu-id="5ac61-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-413">00003</span><span class="sxs-lookup"><span data-stu-id="5ac61-413">00003</span></span></td>
<td><span data-ttu-id="5ac61-414">开销比率计算日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="5ac61-415">会计</span><span class="sxs-lookup"><span data-stu-id="5ac61-415">Fiscal</span></span></td>
<td><span data-ttu-id="5ac61-416">2017</span><span class="sxs-lookup"><span data-stu-id="5ac61-416">2017</span></span></td>
<td><span data-ttu-id="5ac61-417">期间 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-417">Period 1</span></span></td>
<td><span data-ttu-id="5ac61-418">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="5ac61-419">日记帐条目（开销比率计算的日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="5ac61-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ac61-420">会计日期</span><span class="sxs-lookup"><span data-stu-id="5ac61-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-421">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-421">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-422">度量值</span><span class="sxs-lookup"><span data-stu-id="5ac61-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-423">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-424">项目 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-424">Proj 1</span></span></td>
<td><span data-ttu-id="5ac61-425">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5ac61-426">3.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-427">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-428">项目 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-428">Proj 2</span></span></td>
<td><span data-ttu-id="5ac61-429">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5ac61-430">1.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ac61-431">成本条目</span><span class="sxs-lookup"><span data-stu-id="5ac61-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-432">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-433">成本元素</span><span class="sxs-lookup"><span data-stu-id="5ac61-433">Cost element</span></span></th>
<th><span data-ttu-id="5ac61-434">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-434">Cost behavior</span></span></th>
<th><span data-ttu-id="5ac61-435">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-435">Amount</span></span></th>
<th><span data-ttu-id="5ac61-436">会计日期</span><span class="sxs-lookup"><span data-stu-id="5ac61-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="5ac61-437">CC0001</span></span></td>
<td><span data-ttu-id="5ac61-438">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-438">HR</span></span></td>
<td><span data-ttu-id="5ac61-439">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-439">10001</span></span></td>
<td><span data-ttu-id="5ac61-440">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-440">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-441">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-441">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-442">-30.00</span></span></td>
<td><span data-ttu-id="5ac61-443">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-444">项目 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-444">Proj 1</span></span></td>
<td><span data-ttu-id="5ac61-445">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5ac61-446">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-446">10001</span></span></td>
<td><span data-ttu-id="5ac61-447">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-447">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-448">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-448">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-449">30.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-449">30.00</span></span></td>
<td><span data-ttu-id="5ac61-450">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-451">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-451">CC001</span></span></td>
<td><span data-ttu-id="5ac61-452">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-452">HR</span></span></td>
<td><span data-ttu-id="5ac61-453">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-453">10001</span></span></td>
<td><span data-ttu-id="5ac61-454">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-454">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-455">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-455">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-456">-10.00</span></span></td>
<td><span data-ttu-id="5ac61-457">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-458">项目 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-458">Proj 2</span></span></td>
<td><span data-ttu-id="5ac61-459">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5ac61-460">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-460">10001</span></span></td>
<td><span data-ttu-id="5ac61-461">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-461">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-462">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-462">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-463">10.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-463">10.00</span></span></td>
<td><span data-ttu-id="5ac61-464">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-465">有关详细信息，请参阅 [执行开销计算](cost-rollup.md#perform-overhead-calculation)。</span><span class="sxs-lookup"><span data-stu-id="5ac61-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="5ac61-466">步骤 4：处理成本分摊计算</span><span class="sxs-lookup"><span data-stu-id="5ac61-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="5ac61-467">分摊用于通过应用分配基础将成本对象的余额分配给其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="5ac61-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="5ac61-468">Finance 支持互惠分摊方法。</span><span class="sxs-lookup"><span data-stu-id="5ac61-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="5ac61-469">在互惠分摊方法中，辅助成本对象交换的互助服务被完全识别。</span><span class="sxs-lookup"><span data-stu-id="5ac61-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="5ac61-470">系统自动确定执行分摊的正确顺序。</span><span class="sxs-lookup"><span data-stu-id="5ac61-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="5ac61-471">成本对象的余额按单一分配基础分配。</span><span class="sxs-lookup"><span data-stu-id="5ac61-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="5ac61-472">支持跨成本对象维度及其各自成员的分摊。</span><span class="sxs-lookup"><span data-stu-id="5ac61-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="5ac61-473">分摊顺序由成本控制单元控制。</span><span class="sxs-lookup"><span data-stu-id="5ac61-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="5ac61-474">[![互惠方法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="5ac61-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="5ac61-475">定义成本分摊</span><span class="sxs-lookup"><span data-stu-id="5ac61-475">Define the cost allocation</span></span>

<span data-ttu-id="5ac61-476">这是说明如何跟踪成本流的简单示例。</span><span class="sxs-lookup"><span data-stu-id="5ac61-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="5ac61-477">成本对象 CC001 HR 生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="5ac61-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="5ac61-478">创建名为“HR 服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="5ac61-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-479">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-479">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-480">HR 服务</span><span class="sxs-lookup"><span data-stu-id="5ac61-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-481">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-481">CC002</span></span></td>
<td><span data-ttu-id="5ac61-482">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-482">Finance</span></span></td>
<td><span data-ttu-id="5ac61-483">35</span><span class="sxs-lookup"><span data-stu-id="5ac61-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-484">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-484">CC003</span></span></td>
<td><span data-ttu-id="5ac61-485">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-485">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-486">55</span><span class="sxs-lookup"><span data-stu-id="5ac61-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-487">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-487">CC004</span></span></td>
<td><span data-ttu-id="5ac61-488">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-488">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-489">10</span><span class="sxs-lookup"><span data-stu-id="5ac61-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-490">成本对象 CC002 财务生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="5ac61-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="5ac61-491">创建名为“财务服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="5ac61-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-492">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-492">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-493">财务服务</span><span class="sxs-lookup"><span data-stu-id="5ac61-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-494">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-494">CC003</span></span></td>
<td><span data-ttu-id="5ac61-495">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-495">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-496">65</span><span class="sxs-lookup"><span data-stu-id="5ac61-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-497">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-497">CC004</span></span></td>
<td><span data-ttu-id="5ac61-498">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-498">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-499">35</span><span class="sxs-lookup"><span data-stu-id="5ac61-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-500">成本对象 CC003 装配生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="5ac61-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="5ac61-501">创建名为“装配服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="5ac61-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-502">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-502">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-503">装配服务（小时）</span><span class="sxs-lookup"><span data-stu-id="5ac61-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-504">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-504">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-505">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-505">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-506">60</span><span class="sxs-lookup"><span data-stu-id="5ac61-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-507">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-507">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-508">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-508">Product 2</span></span></td>
<td><span data-ttu-id="5ac61-509">20</span><span class="sxs-lookup"><span data-stu-id="5ac61-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-510">成本对象 CC004 包装生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="5ac61-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="5ac61-511">创建名为“包装服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="5ac61-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-512">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-512">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-513">包装服务（小时）</span><span class="sxs-lookup"><span data-stu-id="5ac61-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-514">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-514">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-515">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-515">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-516">80</span><span class="sxs-lookup"><span data-stu-id="5ac61-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-517">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-517">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-518">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-518">Product 2</span></span></td>
<td><span data-ttu-id="5ac61-519">15</span><span class="sxs-lookup"><span data-stu-id="5ac61-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5ac61-520">产品消耗的生产工时等统计度量可以派生自源数据。</span><span class="sxs-lookup"><span data-stu-id="5ac61-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="5ac61-521">有关详细信息，请参阅[统计度量提供方模板](statistical-measure-provider-template.md#statistical-measure-provider-template)。</span><span class="sxs-lookup"><span data-stu-id="5ac61-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="5ac61-522">下表显示当 HR 服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="5ac61-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-523">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-523">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-524">度量值</span><span class="sxs-lookup"><span data-stu-id="5ac61-524">Magnitude</span></span></th>
<th><span data-ttu-id="5ac61-525">分配系数</span><span class="sxs-lookup"><span data-stu-id="5ac61-525">Allocation factor</span></span></th>
<th><span data-ttu-id="5ac61-526">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-526">Amount</span></span></th>
<th><span data-ttu-id="5ac61-527">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-528">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-528">CC002</span></span></td>
<td><span data-ttu-id="5ac61-529">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-529">Finance</span></span></td>
<td><span data-ttu-id="5ac61-530">35</span><span class="sxs-lookup"><span data-stu-id="5ac61-530">35</span></span></td>
<td><span data-ttu-id="5ac61-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5ac61-532">175.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-532">175.00</span></span></td>
<td><span data-ttu-id="5ac61-533">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-534">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-534">CC003</span></span></td>
<td><span data-ttu-id="5ac61-535">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-535">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-536">55</span><span class="sxs-lookup"><span data-stu-id="5ac61-536">55</span></span></td>
<td><span data-ttu-id="5ac61-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5ac61-538">275.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-538">275.00</span></span></td>
<td><span data-ttu-id="5ac61-539">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-540">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-540">CC004</span></span></td>
<td><span data-ttu-id="5ac61-541">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-541">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-542">10</span><span class="sxs-lookup"><span data-stu-id="5ac61-542">10</span></span></td>
<td><span data-ttu-id="5ac61-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5ac61-544">50.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-544">50.00</span></span></td>
<td><span data-ttu-id="5ac61-545">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-546">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-546">CC002</span></span></td>
<td><span data-ttu-id="5ac61-547">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-547">Finance</span></span></td>
<td><span data-ttu-id="5ac61-548">35</span><span class="sxs-lookup"><span data-stu-id="5ac61-548">35</span></span></td>
<td><span data-ttu-id="5ac61-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5ac61-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5ac61-550">436.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-550">436.00</span></span></td>
<td><span data-ttu-id="5ac61-551">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-552">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-552">CC003</span></span></td>
<td><span data-ttu-id="5ac61-553">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-553">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-554">55</span><span class="sxs-lookup"><span data-stu-id="5ac61-554">55</span></span></td>
<td><span data-ttu-id="5ac61-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5ac61-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5ac61-556">685.14</span><span class="sxs-lookup"><span data-stu-id="5ac61-556">685.14</span></span></td>
<td><span data-ttu-id="5ac61-557">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-558">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-558">CC004</span></span></td>
<td><span data-ttu-id="5ac61-559">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-559">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-560">10</span><span class="sxs-lookup"><span data-stu-id="5ac61-560">10</span></span></td>
<td><span data-ttu-id="5ac61-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="5ac61-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5ac61-562">124.57</span><span class="sxs-lookup"><span data-stu-id="5ac61-562">124.57</span></span></td>
<td><span data-ttu-id="5ac61-563">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-564">下表显示当财务服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="5ac61-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-565">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-565">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-566">度量值</span><span class="sxs-lookup"><span data-stu-id="5ac61-566">Magnitude</span></span></th>
<th><span data-ttu-id="5ac61-567">分配系数</span><span class="sxs-lookup"><span data-stu-id="5ac61-567">Allocation factor</span></span></th>
<th><span data-ttu-id="5ac61-568">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-568">Amount</span></span></th>
<th><span data-ttu-id="5ac61-569">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-570">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-570">CC003</span></span></td>
<td><span data-ttu-id="5ac61-571">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-571">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-572">65</span><span class="sxs-lookup"><span data-stu-id="5ac61-572">65</span></span></td>
<td><span data-ttu-id="5ac61-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="5ac61-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5ac61-574">438.75</span><span class="sxs-lookup"><span data-stu-id="5ac61-574">438.75</span></span></td>
<td><span data-ttu-id="5ac61-575">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-576">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-576">CC004</span></span></td>
<td><span data-ttu-id="5ac61-577">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-577">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-578">35</span><span class="sxs-lookup"><span data-stu-id="5ac61-578">35</span></span></td>
<td><span data-ttu-id="5ac61-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="5ac61-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5ac61-580">236.25</span><span class="sxs-lookup"><span data-stu-id="5ac61-580">236.25</span></span></td>
<td><span data-ttu-id="5ac61-581">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-582">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-582">CC003</span></span></td>
<td><span data-ttu-id="5ac61-583">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-583">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-584">65</span><span class="sxs-lookup"><span data-stu-id="5ac61-584">65</span></span></td>
<td><span data-ttu-id="5ac61-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="5ac61-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5ac61-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5ac61-586">5,297.69</span></span></td>
<td><span data-ttu-id="5ac61-587">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-588">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-588">CC004</span></span></td>
<td><span data-ttu-id="5ac61-589">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-589">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-590">35</span><span class="sxs-lookup"><span data-stu-id="5ac61-590">35</span></span></td>
<td><span data-ttu-id="5ac61-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="5ac61-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5ac61-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5ac61-592">2,852.60</span></span></td>
<td><span data-ttu-id="5ac61-593">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-594">下表显示当装配服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="5ac61-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-595">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-595">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-596">度量值</span><span class="sxs-lookup"><span data-stu-id="5ac61-596">Magnitude</span></span></th>
<th><span data-ttu-id="5ac61-597">分配系数</span><span class="sxs-lookup"><span data-stu-id="5ac61-597">Allocation factor</span></span></th>
<th><span data-ttu-id="5ac61-598">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-598">Amount</span></span></th>
<th><span data-ttu-id="5ac61-599">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-600">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-600">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-601">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-601">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-602">60</span><span class="sxs-lookup"><span data-stu-id="5ac61-602">60</span></span></td>
<td><span data-ttu-id="5ac61-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="5ac61-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5ac61-604">535.31</span><span class="sxs-lookup"><span data-stu-id="5ac61-604">535.31</span></span></td>
<td><span data-ttu-id="5ac61-605">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-606">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-606">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-607">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-607">Product 2</span></span></td>
<td><span data-ttu-id="5ac61-608">20</span><span class="sxs-lookup"><span data-stu-id="5ac61-608">20</span></span></td>
<td><span data-ttu-id="5ac61-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="5ac61-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5ac61-610">178.44</span><span class="sxs-lookup"><span data-stu-id="5ac61-610">178.44</span></span></td>
<td><span data-ttu-id="5ac61-611">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-612">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-612">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-613">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-613">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-614">60</span><span class="sxs-lookup"><span data-stu-id="5ac61-614">60</span></span></td>
<td><span data-ttu-id="5ac61-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="5ac61-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5ac61-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5ac61-616">4,487.12</span></span></td>
<td><span data-ttu-id="5ac61-617">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-618">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-618">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-619">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-619">Product 2</span></span></td>
<td><span data-ttu-id="5ac61-620">20</span><span class="sxs-lookup"><span data-stu-id="5ac61-620">20</span></span></td>
<td><span data-ttu-id="5ac61-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="5ac61-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5ac61-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5ac61-622">1,495.71</span></span></td>
<td><span data-ttu-id="5ac61-623">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5ac61-624">下表显示当包装服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="5ac61-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-625">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-625">Cost object</span></span></th>
<th><span data-ttu-id="5ac61-626">度量值</span><span class="sxs-lookup"><span data-stu-id="5ac61-626">Magnitude</span></span></th>
<th><span data-ttu-id="5ac61-627">分配系数</span><span class="sxs-lookup"><span data-stu-id="5ac61-627">Allocation factor</span></span></th>
<th><span data-ttu-id="5ac61-628">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-628">Amount</span></span></th>
<th><span data-ttu-id="5ac61-629">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-630">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-630">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-631">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-631">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-632">80</span><span class="sxs-lookup"><span data-stu-id="5ac61-632">80</span></span></td>
<td><span data-ttu-id="5ac61-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="5ac61-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5ac61-634">241.05</span><span class="sxs-lookup"><span data-stu-id="5ac61-634">241.05</span></span></td>
<td><span data-ttu-id="5ac61-635">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-636">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-636">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-637">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-637">Product 2</span></span></td>
<td><span data-ttu-id="5ac61-638">15</span><span class="sxs-lookup"><span data-stu-id="5ac61-638">15</span></span></td>
<td><span data-ttu-id="5ac61-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="5ac61-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5ac61-640">45.20</span><span class="sxs-lookup"><span data-stu-id="5ac61-640">45.20</span></span></td>
<td><span data-ttu-id="5ac61-641">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-642">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-642">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-643">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-643">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-644">80</span><span class="sxs-lookup"><span data-stu-id="5ac61-644">80</span></span></td>
<td><span data-ttu-id="5ac61-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="5ac61-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5ac61-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5ac61-646">2,507.09</span></span></td>
<td><span data-ttu-id="5ac61-647">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-648">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-648">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-649">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-649">Product 2</span></span></td>
<td><span data-ttu-id="5ac61-650">15</span><span class="sxs-lookup"><span data-stu-id="5ac61-650">15</span></span></td>
<td><span data-ttu-id="5ac61-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="5ac61-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5ac61-652">470.08</span><span class="sxs-lookup"><span data-stu-id="5ac61-652">470.08</span></span></td>
<td><span data-ttu-id="5ac61-653">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5ac61-654">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="5ac61-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ac61-655">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-655">Journal</span></span></th>
<th><span data-ttu-id="5ac61-656">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="5ac61-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5ac61-657">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="5ac61-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5ac61-658">版本</span><span class="sxs-lookup"><span data-stu-id="5ac61-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-659">00004</span><span class="sxs-lookup"><span data-stu-id="5ac61-659">00004</span></span></td>
<td><span data-ttu-id="5ac61-660">成本分配日记帐</span><span class="sxs-lookup"><span data-stu-id="5ac61-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="5ac61-661">会计</span><span class="sxs-lookup"><span data-stu-id="5ac61-661">Fiscal</span></span></td>
<td><span data-ttu-id="5ac61-662">2017</span><span class="sxs-lookup"><span data-stu-id="5ac61-662">2017</span></span></td>
<td><span data-ttu-id="5ac61-663">期间 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-663">Period 1</span></span></td>
<td><span data-ttu-id="5ac61-664">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="5ac61-665">日记帐行</span><span class="sxs-lookup"><span data-stu-id="5ac61-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5ac61-666">会计日期</span><span class="sxs-lookup"><span data-stu-id="5ac61-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-667">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-668">成本元素</span><span class="sxs-lookup"><span data-stu-id="5ac61-668">Cost element</span></span></th>
<th><span data-ttu-id="5ac61-669">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-669">Cost behavior</span></span></th>
<th><span data-ttu-id="5ac61-670">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-671">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-672">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-672">CC001</span></span></td>
<td><span data-ttu-id="5ac61-673">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-673">HR</span></span></td>
<td><span data-ttu-id="5ac61-674">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-674">10001</span></span></td>
<td><span data-ttu-id="5ac61-675">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-675">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-676">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-676">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-677">500.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-678">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-679">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-679">CC001</span></span></td>
<td><span data-ttu-id="5ac61-680">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-680">HR</span></span></td>
<td><span data-ttu-id="5ac61-681">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-681">10001</span></span></td>
<td><span data-ttu-id="5ac61-682">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-682">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-683">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-683">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="5ac61-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-685">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-686">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-686">CC002</span></span></td>
<td><span data-ttu-id="5ac61-687">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-687">Finance</span></span></td>
<td><span data-ttu-id="5ac61-688">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-688">10001</span></span></td>
<td><span data-ttu-id="5ac61-689">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-689">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-690">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-690">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-691">675.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-692">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-693">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-693">CC002</span></span></td>
<td><span data-ttu-id="5ac61-694">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-694">Finance</span></span></td>
<td><span data-ttu-id="5ac61-695">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-695">10001</span></span></td>
<td><span data-ttu-id="5ac61-696">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-696">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-697">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-697">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="5ac61-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-699">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-700">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-700">CC003</span></span></td>
<td><span data-ttu-id="5ac61-701">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-701">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-702">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-702">10001</span></span></td>
<td><span data-ttu-id="5ac61-703">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-703">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-704">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-704">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-705">713.75</span><span class="sxs-lookup"><span data-stu-id="5ac61-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-706">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-707">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-707">CC003</span></span></td>
<td><span data-ttu-id="5ac61-708">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-708">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-709">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-709">10001</span></span></td>
<td><span data-ttu-id="5ac61-710">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-710">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-711">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-711">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="5ac61-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-713">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-714">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-714">CC003</span></span></td>
<td><span data-ttu-id="5ac61-715">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-715">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-716">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-716">10001</span></span></td>
<td><span data-ttu-id="5ac61-717">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-717">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-718">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-718">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-719">286.25</span><span class="sxs-lookup"><span data-stu-id="5ac61-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-720">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-721">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-721">CC003</span></span></td>
<td><span data-ttu-id="5ac61-722">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-722">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-723">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-723">10001</span></span></td>
<td><span data-ttu-id="5ac61-724">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-724">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-725">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-725">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="5ac61-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-727">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-728">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-728">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-729">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-729">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-730">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-730">10001</span></span></td>
<td><span data-ttu-id="5ac61-731">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-731">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-732">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-732">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-733">776.36</span><span class="sxs-lookup"><span data-stu-id="5ac61-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-734">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-735">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-735">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-736">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-736">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-737">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-737">10001</span></span></td>
<td><span data-ttu-id="5ac61-738">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-738">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-739">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-739">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5ac61-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-741">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-742">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-742">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-743">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-743">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-744">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-744">10001</span></span></td>
<td><span data-ttu-id="5ac61-745">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-745">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-746">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-746">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-747">223.64</span><span class="sxs-lookup"><span data-stu-id="5ac61-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-748">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="5ac61-749">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-749">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-750">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-750">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-751">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-751">10001</span></span></td>
<td><span data-ttu-id="5ac61-752">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-752">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-753">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-753">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5ac61-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5ac61-755">成本条目</span><span class="sxs-lookup"><span data-stu-id="5ac61-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5ac61-756">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5ac61-757">成本元素</span><span class="sxs-lookup"><span data-stu-id="5ac61-757">Cost element</span></span></th>
<th><span data-ttu-id="5ac61-758">成本行为</span><span class="sxs-lookup"><span data-stu-id="5ac61-758">Cost behavior</span></span></th>
<th><span data-ttu-id="5ac61-759">本币金额</span><span class="sxs-lookup"><span data-stu-id="5ac61-759">Amount</span></span></th>
<th><span data-ttu-id="5ac61-760">会计日期</span><span class="sxs-lookup"><span data-stu-id="5ac61-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5ac61-761">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-761">CC001</span></span></td>
<td><span data-ttu-id="5ac61-762">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-762">HR</span></span></td>
<td><span data-ttu-id="5ac61-763">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-763">10001</span></span></td>
<td><span data-ttu-id="5ac61-764">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-764">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-765">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-765">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-766">-500.00</span></span></td>
<td><span data-ttu-id="5ac61-767">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-768">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-768">CC002</span></span></td>
<td><span data-ttu-id="5ac61-769">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-769">Finance</span></span></td>
<td><span data-ttu-id="5ac61-770">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-770">10001</span></span></td>
<td><span data-ttu-id="5ac61-771">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-771">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-772">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-772">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-773">175.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-773">175.00</span></span></td>
<td><span data-ttu-id="5ac61-774">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-775">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-775">CC003</span></span></td>
<td><span data-ttu-id="5ac61-776">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-776">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-777">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-777">10001</span></span></td>
<td><span data-ttu-id="5ac61-778">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-778">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-779">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-779">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-780">275.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-780">275.00</span></span></td>
<td><span data-ttu-id="5ac61-781">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-782">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-782">CC004</span></span></td>
<td><span data-ttu-id="5ac61-783">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-783">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-784">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-784">10001</span></span></td>
<td><span data-ttu-id="5ac61-785">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-785">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-786">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-786">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-787">50,00</span><span class="sxs-lookup"><span data-stu-id="5ac61-787">50,00</span></span></td>
<td><span data-ttu-id="5ac61-788">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-789">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-789">CC001</span></span></td>
<td><span data-ttu-id="5ac61-790">HR</span><span class="sxs-lookup"><span data-stu-id="5ac61-790">HR</span></span></td>
<td><span data-ttu-id="5ac61-791">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-791">10001</span></span></td>
<td><span data-ttu-id="5ac61-792">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-792">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-793">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-793">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="5ac61-794">-1,245.71</span></span></td>
<td><span data-ttu-id="5ac61-795">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-796">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-796">CC002</span></span></td>
<td><span data-ttu-id="5ac61-797">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-797">Finance</span></span></td>
<td><span data-ttu-id="5ac61-798">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-798">10001</span></span></td>
<td><span data-ttu-id="5ac61-799">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-799">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-800">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-800">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-801">436.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-801">436.00</span></span></td>
<td><span data-ttu-id="5ac61-802">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-803">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-803">CC003</span></span></td>
<td><span data-ttu-id="5ac61-804">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-804">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-805">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-805">10001</span></span></td>
<td><span data-ttu-id="5ac61-806">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-806">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-807">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-807">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-808">685.14</span><span class="sxs-lookup"><span data-stu-id="5ac61-808">685.14</span></span></td>
<td><span data-ttu-id="5ac61-809">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-810">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-810">CC004</span></span></td>
<td><span data-ttu-id="5ac61-811">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-811">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-812">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-812">10001</span></span></td>
<td><span data-ttu-id="5ac61-813">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-813">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-814">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-814">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-815">124.57</span><span class="sxs-lookup"><span data-stu-id="5ac61-815">124.57</span></span></td>
<td><span data-ttu-id="5ac61-816">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-817">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-817">CC002</span></span></td>
<td><span data-ttu-id="5ac61-818">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-818">Finance</span></span></td>
<td><span data-ttu-id="5ac61-819">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-819">10001</span></span></td>
<td><span data-ttu-id="5ac61-820">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-820">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-821">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-821">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-822">-675.00</span></span></td>
<td><span data-ttu-id="5ac61-823">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-824">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-824">CC003</span></span></td>
<td><span data-ttu-id="5ac61-825">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-825">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-826">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-826">10001</span></span></td>
<td><span data-ttu-id="5ac61-827">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-827">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-828">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-828">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-829">438.75</span><span class="sxs-lookup"><span data-stu-id="5ac61-829">438.75</span></span></td>
<td><span data-ttu-id="5ac61-830">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-831">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-831">CC004</span></span></td>
<td><span data-ttu-id="5ac61-832">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-832">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-833">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-833">10001</span></span></td>
<td><span data-ttu-id="5ac61-834">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-834">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-835">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-835">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-836">236.25</span><span class="sxs-lookup"><span data-stu-id="5ac61-836">236.25</span></span></td>
<td><span data-ttu-id="5ac61-837">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-838">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-838">CC002</span></span></td>
<td><span data-ttu-id="5ac61-839">财务</span><span class="sxs-lookup"><span data-stu-id="5ac61-839">Finance</span></span></td>
<td><span data-ttu-id="5ac61-840">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-840">10001</span></span></td>
<td><span data-ttu-id="5ac61-841">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-841">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-842">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-842">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="5ac61-843">-8,150.29</span></span></td>
<td><span data-ttu-id="5ac61-844">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-845">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-845">CC003</span></span></td>
<td><span data-ttu-id="5ac61-846">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-846">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-847">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-847">10001</span></span></td>
<td><span data-ttu-id="5ac61-848">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-848">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-849">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-849">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5ac61-850">5,297.69</span></span></td>
<td><span data-ttu-id="5ac61-851">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-852">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-852">CC004</span></span></td>
<td><span data-ttu-id="5ac61-853">包装</span><span class="sxs-lookup"><span data-stu-id="5ac61-853">Packaging</span></span></td>
<td><span data-ttu-id="5ac61-854">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-854">10001</span></span></td>
<td><span data-ttu-id="5ac61-855">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-855">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-856">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-856">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5ac61-857">2,852.60</span></span></td>
<td><span data-ttu-id="5ac61-858">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-859">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-859">CC003</span></span></td>
<td><span data-ttu-id="5ac61-860">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-860">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-861">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-861">10001</span></span></td>
<td><span data-ttu-id="5ac61-862">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-862">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-863">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-863">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="5ac61-864">-713.75</span></span></td>
<td><span data-ttu-id="5ac61-865">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-866">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-866">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-867">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-867">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-868">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-868">10001</span></span></td>
<td><span data-ttu-id="5ac61-869">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-869">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-870">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-870">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-871">535.31</span><span class="sxs-lookup"><span data-stu-id="5ac61-871">535.31</span></span></td>
<td><span data-ttu-id="5ac61-872">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-873">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-873">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-874">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-874">Product 2</span></span></td>
<td><span data-ttu-id="5ac61-875">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-875">10001</span></span></td>
<td><span data-ttu-id="5ac61-876">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-876">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-877">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-877">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-878">178.44</span><span class="sxs-lookup"><span data-stu-id="5ac61-878">178.44</span></span></td>
<td><span data-ttu-id="5ac61-879">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-880">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-880">CC003</span></span></td>
<td><span data-ttu-id="5ac61-881">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-881">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-882">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-882">10001</span></span></td>
<td><span data-ttu-id="5ac61-883">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-883">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-884">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-884">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="5ac61-885">-5,982.83</span></span></td>
<td><span data-ttu-id="5ac61-886">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-887">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-887">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-888">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-888">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-889">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-889">10001</span></span></td>
<td><span data-ttu-id="5ac61-890">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-890">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-891">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-891">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5ac61-892">4,487.12</span></span></td>
<td><span data-ttu-id="5ac61-893">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-894">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-894">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-895">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-895">Product 2</span></span></td>
<td><span data-ttu-id="5ac61-896">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-896">10001</span></span></td>
<td><span data-ttu-id="5ac61-897">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-897">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-898">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-898">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5ac61-899">1,495.71</span></span></td>
<td><span data-ttu-id="5ac61-900">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-901">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-901">CC003</span></span></td>
<td><span data-ttu-id="5ac61-902">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-902">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-903">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-903">10001</span></span></td>
<td><span data-ttu-id="5ac61-904">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-904">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-905">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-905">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="5ac61-906">-286.25</span></span></td>
<td><span data-ttu-id="5ac61-907">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-908">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-908">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-909">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-909">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-910">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-910">10001</span></span></td>
<td><span data-ttu-id="5ac61-911">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-911">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-912">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-912">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-913">241.05</span><span class="sxs-lookup"><span data-stu-id="5ac61-913">241.05</span></span></td>
<td><span data-ttu-id="5ac61-914">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-915">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-915">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-916">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-916">Product 2</span></span></td>
<td><span data-ttu-id="5ac61-917">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-917">10001</span></span></td>
<td><span data-ttu-id="5ac61-918">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-918">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-919">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-919">Fixed cost</span></span></td>
<td><span data-ttu-id="5ac61-920">45.20</span><span class="sxs-lookup"><span data-stu-id="5ac61-920">45.20</span></span></td>
<td><span data-ttu-id="5ac61-921">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-922">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-922">CC003</span></span></td>
<td><span data-ttu-id="5ac61-923">程序集</span><span class="sxs-lookup"><span data-stu-id="5ac61-923">Assembly</span></span></td>
<td><span data-ttu-id="5ac61-924">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-924">10001</span></span></td>
<td><span data-ttu-id="5ac61-925">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-925">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-926">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-926">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="5ac61-927">-2,977.17</span></span></td>
<td><span data-ttu-id="5ac61-928">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-929">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-929">Prod 1</span></span></td>
<td><span data-ttu-id="5ac61-930">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-930">Product 1</span></span></td>
<td><span data-ttu-id="5ac61-931">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-931">10001</span></span></td>
<td><span data-ttu-id="5ac61-932">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-932">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-933">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-933">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5ac61-934">2,507.09</span></span></td>
<td><span data-ttu-id="5ac61-935">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5ac61-936">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-936">Prod 2</span></span></td>
<td><span data-ttu-id="5ac61-937">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-937">Product 2</span></span></td>
<td><span data-ttu-id="5ac61-938">10001</span><span class="sxs-lookup"><span data-stu-id="5ac61-938">10001</span></span></td>
<td><span data-ttu-id="5ac61-939">电</span><span class="sxs-lookup"><span data-stu-id="5ac61-939">Electricity</span></span></td>
<td><span data-ttu-id="5ac61-940">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-940">Variable cost</span></span></td>
<td><span data-ttu-id="5ac61-941">470.08</span><span class="sxs-lookup"><span data-stu-id="5ac61-941">470.08</span></span></td>
<td><span data-ttu-id="5ac61-942">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="5ac61-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="5ac61-943">结论</span><span class="sxs-lookup"><span data-stu-id="5ac61-943">Conclusion</span></span>
<span data-ttu-id="5ac61-944">在财务会计中，10,000.00 电成本过帐到虚拟成本中心 ID。</span><span class="sxs-lookup"><span data-stu-id="5ac61-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="5ac61-945">因此，成本会计员将了解必须分摊此成本。</span><span class="sxs-lookup"><span data-stu-id="5ac61-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="5ac61-946">在成本核算中，跨组织单位和级别的成本流，基于所应用的政策和规则。</span><span class="sxs-lookup"><span data-stu-id="5ac61-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="5ac61-947">每项成本已与为成本分摊提供最佳评估的分配基础关联。</span><span class="sxs-lookup"><span data-stu-id="5ac61-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="5ac61-948">成本元素</span><span class="sxs-lookup"><span data-stu-id="5ac61-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="5ac61-949">成本对象</span><span class="sxs-lookup"><span data-stu-id="5ac61-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="5ac61-950">合计</span><span class="sxs-lookup"><span data-stu-id="5ac61-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5ac61-951">CC099</span><span class="sxs-lookup"><span data-stu-id="5ac61-951">CC099</span></span></th>
<th><span data-ttu-id="5ac61-952">CC001</span><span class="sxs-lookup"><span data-stu-id="5ac61-952">CC001</span></span></th>
<th><span data-ttu-id="5ac61-953">CC002</span><span class="sxs-lookup"><span data-stu-id="5ac61-953">CC002</span></span></th>
<th><span data-ttu-id="5ac61-954">CC003</span><span class="sxs-lookup"><span data-stu-id="5ac61-954">CC003</span></span></th>
<th><span data-ttu-id="5ac61-955">CC004</span><span class="sxs-lookup"><span data-stu-id="5ac61-955">CC004</span></span></th>
<th><span data-ttu-id="5ac61-956">项目 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-956">Proj 1</span></span></th>
<th><span data-ttu-id="5ac61-957">项目 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-957">Proj 2</span></span></th>
<th><span data-ttu-id="5ac61-958">产品 1</span><span class="sxs-lookup"><span data-stu-id="5ac61-958">Prod 1</span></span></th>
<th><span data-ttu-id="5ac61-959">产品 2</span><span class="sxs-lookup"><span data-stu-id="5ac61-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="5ac61-960">10001 电</span><span class="sxs-lookup"><span data-stu-id="5ac61-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="5ac61-970">未分类</span><span class="sxs-lookup"><span data-stu-id="5ac61-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-971">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="5ac61-972">固定成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-973">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-974">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-975">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-976">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-977">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-978">776.36</span><span class="sxs-lookup"><span data-stu-id="5ac61-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-979">223.64</span><span class="sxs-lookup"><span data-stu-id="5ac61-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5ac61-981">可变成本</span><span class="sxs-lookup"><span data-stu-id="5ac61-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-982">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-983">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-984">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-985">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-986">0.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-987">30.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-988">10.00</span><span class="sxs-lookup"><span data-stu-id="5ac61-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5ac61-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5ac61-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5ac61-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5ac61-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5ac61-992">此主题显示主要成本元素“10001 电”如何流过成本对象。</span><span class="sxs-lookup"><span data-stu-id="5ac61-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="5ac61-993">因此，此间接成本分摊到组织的最低级别。</span><span class="sxs-lookup"><span data-stu-id="5ac61-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="5ac61-994">换言之，最低级别的成本对象承担成本。</span><span class="sxs-lookup"><span data-stu-id="5ac61-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="5ac61-995">如果您需要成本对象之间的可视成本流，可以使用成本累积政策规则实现成本流可视化。</span><span class="sxs-lookup"><span data-stu-id="5ac61-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="5ac61-996">有关详细信息，请参阅[成本累积政策和开销计算](cost-rollup.md)。</span><span class="sxs-lookup"><span data-stu-id="5ac61-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



