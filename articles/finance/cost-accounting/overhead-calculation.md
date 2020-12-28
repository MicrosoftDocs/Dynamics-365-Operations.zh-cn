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
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440864"
---
# <a name="overhead-calculation"></a><span data-ttu-id="4e3a1-103">开销计算</span><span class="sxs-lookup"><span data-stu-id="4e3a1-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e3a1-104">此主题描述计算和分配间接成本的典型流程。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="4e3a1-105">术语定义</span><span class="sxs-lookup"><span data-stu-id="4e3a1-105">Term definition</span></span>
---------------

<span data-ttu-id="4e3a1-106">间接成本是为业务运营支出的成本，但是不能直接归为任何具体的业务活动、产品或服务。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="4e3a1-107">间接成本为营利活动的生成提供重要支持。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="4e3a1-108">以下是一些开销成本示例：</span><span class="sxs-lookup"><span data-stu-id="4e3a1-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="4e3a1-109">租金</span><span class="sxs-lookup"><span data-stu-id="4e3a1-109">Rent</span></span>
-   <span data-ttu-id="4e3a1-110">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-110">Electricity</span></span>
-   <span data-ttu-id="4e3a1-111">管理薪金</span><span class="sxs-lookup"><span data-stu-id="4e3a1-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="4e3a1-112">开销计算概览</span><span class="sxs-lookup"><span data-stu-id="4e3a1-112">Overhead calculation overview</span></span>
<span data-ttu-id="4e3a1-113">开销计算按正确顺序运行会计政策。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="4e3a1-114">如果成本核算政策更改或检测到特定错误，您可以为同一个会计期间多次运行开销计算。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="4e3a1-115">每次运行的开销计算将被存储并收到唯一版本 ID，让您可以比较各个版本的计算。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="4e3a1-116">开销计算生成的成本条目接收会计日期。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="4e3a1-117">此会计日期与计算中使用的会计期间的结束日期一致。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="4e3a1-118">唯一版本 ID 由以下元素组成：</span><span class="sxs-lookup"><span data-stu-id="4e3a1-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="4e3a1-119">版本类型</span><span class="sxs-lookup"><span data-stu-id="4e3a1-119">Version type</span></span>
-   <span data-ttu-id="4e3a1-120">日期和时间</span><span class="sxs-lookup"><span data-stu-id="4e3a1-120">Date and time</span></span>
-   <span data-ttu-id="4e3a1-121">成本核算分类帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="4e3a1-122">会计年度</span><span class="sxs-lookup"><span data-stu-id="4e3a1-122">Fiscal year</span></span>
-   <span data-ttu-id="4e3a1-123">会计期间</span><span class="sxs-lookup"><span data-stu-id="4e3a1-123">Fiscal period</span></span>

<span data-ttu-id="4e3a1-124">开销计算独立于版本运行。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="4e3a1-125">因此，可以在实际版本前计算预算版本。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="4e3a1-126">开销计算包括四个步骤，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="4e3a1-127">在每个步骤中，创建包含日记帐条目的日记帐标头。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="4e3a1-128">此日记帐标头为每个计算步骤保留输入数据。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="4e3a1-129">政策和规则应用于每个日记帐行，成本条目生成为输出。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="4e3a1-130">因此，您始终具有完全的可跟踪性。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="4e3a1-131">[![开销计算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="4e3a1-132">计算和分摊电间接成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="4e3a1-133">在财务会计中，有些成本（如电）登记为总计。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="4e3a1-134">因此，不为成本核算提供详细的管理洞察。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="4e3a1-135">在成本核算中，为提供跨所有组织单位和级别的正确的管理洞察，成本必须流过各个组织单位。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="4e3a1-136">此流必须基于消耗量的准确记录或公平评估。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="4e3a1-137">在总帐中，可以过帐电成本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e3a1-138">会计日期</span><span class="sxs-lookup"><span data-stu-id="4e3a1-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-139">成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-140">主科目</span><span class="sxs-lookup"><span data-stu-id="4e3a1-140">Main account</span></span></th>
<th><span data-ttu-id="4e3a1-141">按记帐币种计算的金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-142">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-143">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-143">CC099</span></span></td>
<td><span data-ttu-id="4e3a1-144">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-144">Default cost center</span></span></td>
<td><span data-ttu-id="4e3a1-145">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-145">10001</span></span></td>
<td><span data-ttu-id="4e3a1-146">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-146">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="4e3a1-148">步骤 1：处理成本行为计算</span><span class="sxs-lookup"><span data-stu-id="4e3a1-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="4e3a1-149">默认情况下，当成本条目从源数据导入时，它们在成本核算中接收 **未分类** 成本行为分类。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="4e3a1-150">通过应用成本行为政策规则，您可以将成本条目重新分类为 **固定成本** 或 **可变成本**。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="4e3a1-151">定义成本行为规则</span><span class="sxs-lookup"><span data-stu-id="4e3a1-151">Define the cost behavior rule</span></span>

<span data-ttu-id="4e3a1-152">在某些情况下，一部分成本是一项固定费用，其余成本基于消耗量。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="4e3a1-153">通常电费帐单与此定义一致。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="4e3a1-154">在支付特定固定费用后，您按千瓦时 (Kwh) 支付消耗量。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="4e3a1-155">例如，如果固定成本费用为 1,000.00，以下是成本行为规则的定义：</span><span class="sxs-lookup"><span data-stu-id="4e3a1-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="4e3a1-156">固定金额 1,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="4e3a1-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="4e3a1-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="4e3a1-158">1000,01 &lt; N = 可变</span><span class="sxs-lookup"><span data-stu-id="4e3a1-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="4e3a1-159">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e3a1-160">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-160">Journal</span></span></th>
<th><span data-ttu-id="4e3a1-161">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="4e3a1-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e3a1-162">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="4e3a1-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e3a1-163">版本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-164">00001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-164">00001</span></span></td>
<td><span data-ttu-id="4e3a1-165">成本行为计算日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="4e3a1-166">会计</span><span class="sxs-lookup"><span data-stu-id="4e3a1-166">Fiscal</span></span></td>
<td><span data-ttu-id="4e3a1-167">2017</span><span class="sxs-lookup"><span data-stu-id="4e3a1-167">2017</span></span></td>
<td><span data-ttu-id="4e3a1-168">期间 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-168">Period 1</span></span></td>
<td><span data-ttu-id="4e3a1-169">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4e3a1-170">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="4e3a1-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e3a1-171">会计日期</span><span class="sxs-lookup"><span data-stu-id="4e3a1-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-172">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-173">成本元素</span><span class="sxs-lookup"><span data-stu-id="4e3a1-173">Cost element</span></span></th>
<th><span data-ttu-id="4e3a1-174">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-174">Cost behavior</span></span></th>
<th><span data-ttu-id="4e3a1-175">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-176">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-177">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-177">CC099</span></span></td>
<td><span data-ttu-id="4e3a1-178">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-178">Default cost center</span></span></td>
<td><span data-ttu-id="4e3a1-179">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-179">10001</span></span></td>
<td><span data-ttu-id="4e3a1-180">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-180">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-181">未分类</span><span class="sxs-lookup"><span data-stu-id="4e3a1-181">Unclassified</span></span></td>
<td><span data-ttu-id="4e3a1-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e3a1-183">成本条目</span><span class="sxs-lookup"><span data-stu-id="4e3a1-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-184">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-185">成本元素</span><span class="sxs-lookup"><span data-stu-id="4e3a1-185">Cost element</span></span></th>
<th><span data-ttu-id="4e3a1-186">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-186">Cost behavior</span></span></th>
<th><span data-ttu-id="4e3a1-187">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-187">Amount</span></span></th>
<th><span data-ttu-id="4e3a1-188">会计日期</span><span class="sxs-lookup"><span data-stu-id="4e3a1-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-189">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-189">CC099</span></span></td>
<td><span data-ttu-id="4e3a1-190">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-190">Default cost center</span></span></td>
<td><span data-ttu-id="4e3a1-191">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-191">10001</span></span></td>
<td><span data-ttu-id="4e3a1-192">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-192">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-193">未分类</span><span class="sxs-lookup"><span data-stu-id="4e3a1-193">Unclassified</span></span></td>
<td><span data-ttu-id="4e3a1-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-194">10,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-195">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-196">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-196">CC099</span></span></td>
<td><span data-ttu-id="4e3a1-197">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-197">Default cost center</span></span></td>
<td><span data-ttu-id="4e3a1-198">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-198">10001</span></span></td>
<td><span data-ttu-id="4e3a1-199">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-199">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-200">未分类</span><span class="sxs-lookup"><span data-stu-id="4e3a1-200">Unclassified</span></span></td>
<td><span data-ttu-id="4e3a1-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-201">-10,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-202">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-203">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-203">CC099</span></span></td>
<td><span data-ttu-id="4e3a1-204">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-204">Default cost center</span></span></td>
<td><span data-ttu-id="4e3a1-205">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-205">10001</span></span></td>
<td><span data-ttu-id="4e3a1-206">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-206">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-207">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-207">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-208">1,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-209">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-210">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-210">CC099</span></span></td>
<td><span data-ttu-id="4e3a1-211">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-211">Default cost center</span></span></td>
<td><span data-ttu-id="4e3a1-212">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-212">10001</span></span></td>
<td><span data-ttu-id="4e3a1-213">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-213">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-214">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-214">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-215">9,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-216">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-217">有关详细信息，请参阅[创建成本行为策略并将其分配到成本控制单元](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="4e3a1-218">步骤 2：处理成本分配计算</span><span class="sxs-lookup"><span data-stu-id="4e3a1-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="4e3a1-219">成本分配用于通过应用相关的分摊基数将成本从一个成本对象重新分配到一个或多个其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="4e3a1-220">成本分配和成本分摊的不同之处在于，成本分配始终发生在原始成本的主要成本元素级别。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="4e3a1-221">定义成本分配规则</span><span class="sxs-lookup"><span data-stu-id="4e3a1-221">Define the cost distribution rule</span></span>

<span data-ttu-id="4e3a1-222">在财务会计中，电成本通常登记为总计。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="4e3a1-223">在成本核算中，此方法不足够详细。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="4e3a1-224">可变成本应公平分配到各个成本对象。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="4e3a1-225">最合理的分配基础是电的消耗量 (Kwh)。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="4e3a1-226">创建名为“电”的统计维度成员并记录电的消耗量。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="4e3a1-227">默认情况下，所有统计维度成员均可作为分配基础。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-228">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-228">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="4e3a1-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-230">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-230">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-231">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-231">HR</span></span></td>
<td><span data-ttu-id="4e3a1-232">1,000</span><span class="sxs-lookup"><span data-stu-id="4e3a1-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-233">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-233">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-234">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-234">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-235">6,000</span><span class="sxs-lookup"><span data-stu-id="4e3a1-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-236">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-236">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-237">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-237">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-238">0</span><span class="sxs-lookup"><span data-stu-id="4e3a1-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-239">下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-240">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-240">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-241">度量值</span><span class="sxs-lookup"><span data-stu-id="4e3a1-241">Magnitude</span></span></th>
<th><span data-ttu-id="4e3a1-242">分配系数</span><span class="sxs-lookup"><span data-stu-id="4e3a1-242">Allocation factor</span></span></th>
<th><span data-ttu-id="4e3a1-243">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-244">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-244">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-245">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-245">HR</span></span></td>
<td><span data-ttu-id="4e3a1-246">1,000</span><span class="sxs-lookup"><span data-stu-id="4e3a1-246">1,000</span></span></td>
<td><span data-ttu-id="4e3a1-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4e3a1-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-249">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-249">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-250">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-250">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-251">6,000</span><span class="sxs-lookup"><span data-stu-id="4e3a1-251">6,000</span></span></td>
<td><span data-ttu-id="4e3a1-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4e3a1-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-254">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-254">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-255">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-255">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-256">0</span><span class="sxs-lookup"><span data-stu-id="4e3a1-256">0</span></span></td>
<td><span data-ttu-id="4e3a1-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-258">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-259">固定成本应平均分配到消耗了电的单个成本对象。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="4e3a1-260">可以通过在公式分配基础中使用电统计维度成员取得此结果：（电 &gt; 0.00）下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-261">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-261">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-262">配方</span><span class="sxs-lookup"><span data-stu-id="4e3a1-262">Formula</span></span></th>
<th><span data-ttu-id="4e3a1-263">度量值</span><span class="sxs-lookup"><span data-stu-id="4e3a1-263">Magnitude</span></span></th>
<th><span data-ttu-id="4e3a1-264">分配系数</span><span class="sxs-lookup"><span data-stu-id="4e3a1-264">Allocation factor</span></span></th>
<th><span data-ttu-id="4e3a1-265">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-266">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-266">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-267">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-267">HR</span></span></td>
<td><span data-ttu-id="4e3a1-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4e3a1-269">1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-269">1</span></span></td>
<td><span data-ttu-id="4e3a1-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-271">500.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-272">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-272">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-273">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-273">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4e3a1-275">1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-275">1</span></span></td>
<td><span data-ttu-id="4e3a1-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-277">500.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-278">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-278">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-279">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-279">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="4e3a1-281">0</span><span class="sxs-lookup"><span data-stu-id="4e3a1-281">0</span></span></td>
<td><span data-ttu-id="4e3a1-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-283">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4e3a1-284">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e3a1-285">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-285">Journal</span></span></th>
<th><span data-ttu-id="4e3a1-286">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="4e3a1-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e3a1-287">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="4e3a1-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e3a1-288">版本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-289">00002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-289">00002</span></span></td>
<td><span data-ttu-id="4e3a1-290">成本分配计算日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="4e3a1-291">会计</span><span class="sxs-lookup"><span data-stu-id="4e3a1-291">Fiscal</span></span></td>
<td><span data-ttu-id="4e3a1-292">2017</span><span class="sxs-lookup"><span data-stu-id="4e3a1-292">2017</span></span></td>
<td><span data-ttu-id="4e3a1-293">期间 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-293">Period 1</span></span></td>
<td><span data-ttu-id="4e3a1-294">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4e3a1-295">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="4e3a1-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e3a1-296">会计日期</span><span class="sxs-lookup"><span data-stu-id="4e3a1-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-297">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-298">成本元素</span><span class="sxs-lookup"><span data-stu-id="4e3a1-298">Cost element</span></span></th>
<th><span data-ttu-id="4e3a1-299">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-299">Cost behavior</span></span></th>
<th><span data-ttu-id="4e3a1-300">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-301">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-302">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-302">CC099</span></span></td>
<td><span data-ttu-id="4e3a1-303">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-303">Default cost center</span></span></td>
<td><span data-ttu-id="4e3a1-304">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-304">10001</span></span></td>
<td><span data-ttu-id="4e3a1-305">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-305">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-306">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-306">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-308">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-309">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-309">CC099</span></span></td>
<td><span data-ttu-id="4e3a1-310">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-310">Default cost center</span></span></td>
<td><span data-ttu-id="4e3a1-311">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-311">10001</span></span></td>
<td><span data-ttu-id="4e3a1-312">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-312">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-313">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-313">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e3a1-315">成本条目</span><span class="sxs-lookup"><span data-stu-id="4e3a1-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-316">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-317">成本元素</span><span class="sxs-lookup"><span data-stu-id="4e3a1-317">Cost element</span></span></th>
<th><span data-ttu-id="4e3a1-318">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-318">Cost behavior</span></span></th>
<th><span data-ttu-id="4e3a1-319">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-319">Amount</span></span></th>
<th><span data-ttu-id="4e3a1-320">会计日期</span><span class="sxs-lookup"><span data-stu-id="4e3a1-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-321">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-321">CC099</span></span></td>
<td><span data-ttu-id="4e3a1-322">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-322">Default cost center</span></span></td>
<td><span data-ttu-id="4e3a1-323">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-323">10001</span></span></td>
<td><span data-ttu-id="4e3a1-324">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-324">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-325">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-325">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-326">-1,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-327">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-328">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-328">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-329">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-329">HR</span></span></td>
<td><span data-ttu-id="4e3a1-330">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-330">10001</span></span></td>
<td><span data-ttu-id="4e3a1-331">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-331">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-332">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-332">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-333">500.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-333">500.00</span></span></td>
<td><span data-ttu-id="4e3a1-334">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-335">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-335">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-336">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-336">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-337">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-337">10001</span></span></td>
<td><span data-ttu-id="4e3a1-338">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-338">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-339">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-339">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-340">500.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-340">500.00</span></span></td>
<td><span data-ttu-id="4e3a1-341">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-342">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-342">CC099</span></span></td>
<td><span data-ttu-id="4e3a1-343">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="4e3a1-343">Default cost center</span></span></td>
<td><span data-ttu-id="4e3a1-344">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-344">10001</span></span></td>
<td><span data-ttu-id="4e3a1-345">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-345">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-346">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-346">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-347">-9,000.00</span></span></td>
<td><span data-ttu-id="4e3a1-348">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-349">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-349">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-350">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-350">HR</span></span></td>
<td><span data-ttu-id="4e3a1-351">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-351">10001</span></span></td>
<td><span data-ttu-id="4e3a1-352">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-352">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-353">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-353">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="4e3a1-354">1,285.71</span></span></td>
<td><span data-ttu-id="4e3a1-355">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-356">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-356">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-357">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-357">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-358">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-358">10001</span></span></td>
<td><span data-ttu-id="4e3a1-359">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-359">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-360">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-360">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="4e3a1-361">7,714.29</span></span></td>
<td><span data-ttu-id="4e3a1-362">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-363">有关详细信息，请参阅[创建成本分配策略并将其分配到成本控制单元](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="4e3a1-364">步骤 3：处理开销比率计算</span><span class="sxs-lookup"><span data-stu-id="4e3a1-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="4e3a1-365">开销比率用于向一个或多个特定成本对象收费。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="4e3a1-366">费用基于预先确定的成本率和来自指定的分配基础的度量值。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="4e3a1-367">定义开销比率</span><span class="sxs-lookup"><span data-stu-id="4e3a1-367">Define the overhead rate</span></span>

<span data-ttu-id="4e3a1-368">成本对象 CC001 HR 生成一组内部项目。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="4e3a1-369">创建名为“HR 项目”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-370">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-370">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-371">工时</span><span class="sxs-lookup"><span data-stu-id="4e3a1-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-372">项目 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-372">Proj 1</span></span></td>
<td><span data-ttu-id="4e3a1-373">项目 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-373">Project 1</span></span></td>
<td><span data-ttu-id="4e3a1-374">3</span><span class="sxs-lookup"><span data-stu-id="4e3a1-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-375">项目 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-375">Proj 2</span></span></td>
<td><span data-ttu-id="4e3a1-376">项目 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-376">Project 2</span></span></td>
<td><span data-ttu-id="4e3a1-377">1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-378">成本项目份额预先确定的成本率已定义。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-379">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-379">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-380">成本元素</span><span class="sxs-lookup"><span data-stu-id="4e3a1-380">Cost element</span></span></th>
<th><span data-ttu-id="4e3a1-381">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-381">Cost behavior</span></span></th>
<th><span data-ttu-id="4e3a1-382">单位</span><span class="sxs-lookup"><span data-stu-id="4e3a1-382">Units</span></span></th>
<th><span data-ttu-id="4e3a1-383">比率</span><span class="sxs-lookup"><span data-stu-id="4e3a1-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-384">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-384">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-385">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-385">HR</span></span></td>
<td><span data-ttu-id="4e3a1-386">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-386">10001</span></span></td>
<td><span data-ttu-id="4e3a1-387">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-387">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-388">1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-388">1</span></span></td>
<td><span data-ttu-id="4e3a1-389">10</span><span class="sxs-lookup"><span data-stu-id="4e3a1-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-390">下表显示 HR 项目用作分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-391">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-391">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-392">度量值</span><span class="sxs-lookup"><span data-stu-id="4e3a1-392">Magnitude</span></span></th>
<th><span data-ttu-id="4e3a1-393">成本元素</span><span class="sxs-lookup"><span data-stu-id="4e3a1-393">Cost element</span></span></th>
<th><span data-ttu-id="4e3a1-394">分配系数</span><span class="sxs-lookup"><span data-stu-id="4e3a1-394">Allocation factor</span></span></th>
<th><span data-ttu-id="4e3a1-395">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-396">项目 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-396">Proj 1</span></span></td>
<td><span data-ttu-id="4e3a1-397">项目 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-397">Project 1</span></span></td>
<td><span data-ttu-id="4e3a1-398">3</span><span class="sxs-lookup"><span data-stu-id="4e3a1-398">3</span></span></td>
<td><span data-ttu-id="4e3a1-399">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-399">10001</span></span></td>
<td><span data-ttu-id="4e3a1-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4e3a1-401">30.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-402">项目 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-402">Proj 2</span></span></td>
<td><span data-ttu-id="4e3a1-403">项目 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-403">Project 2</span></span></td>
<td><span data-ttu-id="4e3a1-404">1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-404">1</span></span></td>
<td><span data-ttu-id="4e3a1-405">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-405">10001</span></span></td>
<td><span data-ttu-id="4e3a1-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="4e3a1-407">10.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="4e3a1-408">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e3a1-409">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-409">Journal</span></span></th>
<th><span data-ttu-id="4e3a1-410">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="4e3a1-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e3a1-411">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="4e3a1-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e3a1-412">版本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-413">00003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-413">00003</span></span></td>
<td><span data-ttu-id="4e3a1-414">开销比率计算日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="4e3a1-415">会计</span><span class="sxs-lookup"><span data-stu-id="4e3a1-415">Fiscal</span></span></td>
<td><span data-ttu-id="4e3a1-416">2017</span><span class="sxs-lookup"><span data-stu-id="4e3a1-416">2017</span></span></td>
<td><span data-ttu-id="4e3a1-417">期间 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-417">Period 1</span></span></td>
<td><span data-ttu-id="4e3a1-418">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="4e3a1-419">日记帐条目（开销比率计算的日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="4e3a1-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e3a1-420">会计日期</span><span class="sxs-lookup"><span data-stu-id="4e3a1-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-421">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-421">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-422">度量值</span><span class="sxs-lookup"><span data-stu-id="4e3a1-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-423">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-424">项目 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-424">Proj 1</span></span></td>
<td><span data-ttu-id="4e3a1-425">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4e3a1-426">3.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-427">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-428">项目 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-428">Proj 2</span></span></td>
<td><span data-ttu-id="4e3a1-429">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4e3a1-430">1.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e3a1-431">成本条目</span><span class="sxs-lookup"><span data-stu-id="4e3a1-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-432">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-433">成本元素</span><span class="sxs-lookup"><span data-stu-id="4e3a1-433">Cost element</span></span></th>
<th><span data-ttu-id="4e3a1-434">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-434">Cost behavior</span></span></th>
<th><span data-ttu-id="4e3a1-435">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-435">Amount</span></span></th>
<th><span data-ttu-id="4e3a1-436">会计日期</span><span class="sxs-lookup"><span data-stu-id="4e3a1-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-437">CC0001</span></span></td>
<td><span data-ttu-id="4e3a1-438">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-438">HR</span></span></td>
<td><span data-ttu-id="4e3a1-439">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-439">10001</span></span></td>
<td><span data-ttu-id="4e3a1-440">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-440">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-441">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-441">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-442">-30.00</span></span></td>
<td><span data-ttu-id="4e3a1-443">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-444">项目 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-444">Proj 1</span></span></td>
<td><span data-ttu-id="4e3a1-445">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="4e3a1-446">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-446">10001</span></span></td>
<td><span data-ttu-id="4e3a1-447">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-447">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-448">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-448">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-449">30.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-449">30.00</span></span></td>
<td><span data-ttu-id="4e3a1-450">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-451">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-451">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-452">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-452">HR</span></span></td>
<td><span data-ttu-id="4e3a1-453">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-453">10001</span></span></td>
<td><span data-ttu-id="4e3a1-454">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-454">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-455">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-455">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-456">-10.00</span></span></td>
<td><span data-ttu-id="4e3a1-457">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-458">项目 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-458">Proj 2</span></span></td>
<td><span data-ttu-id="4e3a1-459">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="4e3a1-460">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-460">10001</span></span></td>
<td><span data-ttu-id="4e3a1-461">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-461">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-462">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-462">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-463">10.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-463">10.00</span></span></td>
<td><span data-ttu-id="4e3a1-464">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-465">有关详细信息，请参阅 [执行开销计算](cost-rollup.md#perform-overhead-calculation)。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="4e3a1-466">步骤 4：处理成本分摊计算</span><span class="sxs-lookup"><span data-stu-id="4e3a1-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="4e3a1-467">分摊用于通过应用分配基础将成本对象的余额分配给其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="4e3a1-468">Finance 支持互惠分摊方法。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="4e3a1-469">在互惠分摊方法中，辅助成本对象交换的互助服务被完全识别。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="4e3a1-470">系统自动确定执行分摊的正确顺序。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="4e3a1-471">成本对象的余额按单一分配基础分配。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="4e3a1-472">支持跨成本对象维度及其各自成员的分摊。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="4e3a1-473">分摊顺序由成本控制单元控制。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="4e3a1-474">[![互惠方法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="4e3a1-475">定义成本分摊</span><span class="sxs-lookup"><span data-stu-id="4e3a1-475">Define the cost allocation</span></span>

<span data-ttu-id="4e3a1-476">这是说明如何跟踪成本流的简单示例。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="4e3a1-477">成本对象 CC001 HR 生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="4e3a1-478">创建名为“HR 服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-479">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-479">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-480">HR 服务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-481">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-481">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-482">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-482">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-483">35</span><span class="sxs-lookup"><span data-stu-id="4e3a1-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-484">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-484">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-485">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-485">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-486">55</span><span class="sxs-lookup"><span data-stu-id="4e3a1-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-487">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-487">CC004</span></span></td>
<td><span data-ttu-id="4e3a1-488">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-488">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-489">10</span><span class="sxs-lookup"><span data-stu-id="4e3a1-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-490">成本对象 CC002 财务生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="4e3a1-491">创建名为“财务服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-492">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-492">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-493">财务服务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-494">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-494">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-495">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-495">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-496">65</span><span class="sxs-lookup"><span data-stu-id="4e3a1-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-497">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-497">CC004</span></span></td>
<td><span data-ttu-id="4e3a1-498">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-498">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-499">35</span><span class="sxs-lookup"><span data-stu-id="4e3a1-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-500">成本对象 CC003 装配生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="4e3a1-501">创建名为“装配服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-502">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-502">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-503">装配服务（小时）</span><span class="sxs-lookup"><span data-stu-id="4e3a1-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-504">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-504">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-505">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-505">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-506">60</span><span class="sxs-lookup"><span data-stu-id="4e3a1-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-507">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-507">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-508">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-508">Product 2</span></span></td>
<td><span data-ttu-id="4e3a1-509">20</span><span class="sxs-lookup"><span data-stu-id="4e3a1-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-510">成本对象 CC004 包装生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="4e3a1-511">创建名为“包装服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-512">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-512">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-513">包装服务（小时）</span><span class="sxs-lookup"><span data-stu-id="4e3a1-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-514">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-514">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-515">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-515">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-516">80</span><span class="sxs-lookup"><span data-stu-id="4e3a1-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-517">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-517">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-518">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-518">Product 2</span></span></td>
<td><span data-ttu-id="4e3a1-519">15</span><span class="sxs-lookup"><span data-stu-id="4e3a1-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4e3a1-520">产品消耗的生产工时等统计度量可以派生自源数据。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="4e3a1-521">有关详细信息，请参阅[统计度量提供方模板](statistical-measure-provider-template.md#statistical-measure-provider-template)。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="4e3a1-522">下表显示当 HR 服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-523">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-523">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-524">度量值</span><span class="sxs-lookup"><span data-stu-id="4e3a1-524">Magnitude</span></span></th>
<th><span data-ttu-id="4e3a1-525">分配系数</span><span class="sxs-lookup"><span data-stu-id="4e3a1-525">Allocation factor</span></span></th>
<th><span data-ttu-id="4e3a1-526">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-526">Amount</span></span></th>
<th><span data-ttu-id="4e3a1-527">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-528">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-528">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-529">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-529">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-530">35</span><span class="sxs-lookup"><span data-stu-id="4e3a1-530">35</span></span></td>
<td><span data-ttu-id="4e3a1-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4e3a1-532">175.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-532">175.00</span></span></td>
<td><span data-ttu-id="4e3a1-533">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-534">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-534">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-535">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-535">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-536">55</span><span class="sxs-lookup"><span data-stu-id="4e3a1-536">55</span></span></td>
<td><span data-ttu-id="4e3a1-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4e3a1-538">275.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-538">275.00</span></span></td>
<td><span data-ttu-id="4e3a1-539">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-540">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-540">CC004</span></span></td>
<td><span data-ttu-id="4e3a1-541">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-541">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-542">10</span><span class="sxs-lookup"><span data-stu-id="4e3a1-542">10</span></span></td>
<td><span data-ttu-id="4e3a1-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="4e3a1-544">50.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-544">50.00</span></span></td>
<td><span data-ttu-id="4e3a1-545">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-546">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-546">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-547">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-547">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-548">35</span><span class="sxs-lookup"><span data-stu-id="4e3a1-548">35</span></span></td>
<td><span data-ttu-id="4e3a1-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="4e3a1-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4e3a1-550">436.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-550">436.00</span></span></td>
<td><span data-ttu-id="4e3a1-551">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-552">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-552">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-553">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-553">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-554">55</span><span class="sxs-lookup"><span data-stu-id="4e3a1-554">55</span></span></td>
<td><span data-ttu-id="4e3a1-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="4e3a1-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4e3a1-556">685.14</span><span class="sxs-lookup"><span data-stu-id="4e3a1-556">685.14</span></span></td>
<td><span data-ttu-id="4e3a1-557">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-558">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-558">CC004</span></span></td>
<td><span data-ttu-id="4e3a1-559">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-559">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-560">10</span><span class="sxs-lookup"><span data-stu-id="4e3a1-560">10</span></span></td>
<td><span data-ttu-id="4e3a1-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="4e3a1-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="4e3a1-562">124.57</span><span class="sxs-lookup"><span data-stu-id="4e3a1-562">124.57</span></span></td>
<td><span data-ttu-id="4e3a1-563">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-564">下表显示当财务服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-565">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-565">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-566">度量值</span><span class="sxs-lookup"><span data-stu-id="4e3a1-566">Magnitude</span></span></th>
<th><span data-ttu-id="4e3a1-567">分配系数</span><span class="sxs-lookup"><span data-stu-id="4e3a1-567">Allocation factor</span></span></th>
<th><span data-ttu-id="4e3a1-568">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-568">Amount</span></span></th>
<th><span data-ttu-id="4e3a1-569">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-570">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-570">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-571">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-571">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-572">65</span><span class="sxs-lookup"><span data-stu-id="4e3a1-572">65</span></span></td>
<td><span data-ttu-id="4e3a1-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4e3a1-574">438.75</span><span class="sxs-lookup"><span data-stu-id="4e3a1-574">438.75</span></span></td>
<td><span data-ttu-id="4e3a1-575">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-576">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-576">CC004</span></span></td>
<td><span data-ttu-id="4e3a1-577">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-577">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-578">35</span><span class="sxs-lookup"><span data-stu-id="4e3a1-578">35</span></span></td>
<td><span data-ttu-id="4e3a1-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="4e3a1-580">236.25</span><span class="sxs-lookup"><span data-stu-id="4e3a1-580">236.25</span></span></td>
<td><span data-ttu-id="4e3a1-581">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-582">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-582">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-583">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-583">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-584">65</span><span class="sxs-lookup"><span data-stu-id="4e3a1-584">65</span></span></td>
<td><span data-ttu-id="4e3a1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4e3a1-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4e3a1-586">5,297.69</span></span></td>
<td><span data-ttu-id="4e3a1-587">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-588">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-588">CC004</span></span></td>
<td><span data-ttu-id="4e3a1-589">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-589">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-590">35</span><span class="sxs-lookup"><span data-stu-id="4e3a1-590">35</span></span></td>
<td><span data-ttu-id="4e3a1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="4e3a1-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4e3a1-592">2,852.60</span></span></td>
<td><span data-ttu-id="4e3a1-593">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-594">下表显示当装配服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-595">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-595">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-596">度量值</span><span class="sxs-lookup"><span data-stu-id="4e3a1-596">Magnitude</span></span></th>
<th><span data-ttu-id="4e3a1-597">分配系数</span><span class="sxs-lookup"><span data-stu-id="4e3a1-597">Allocation factor</span></span></th>
<th><span data-ttu-id="4e3a1-598">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-598">Amount</span></span></th>
<th><span data-ttu-id="4e3a1-599">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-600">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-600">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-601">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-601">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-602">60</span><span class="sxs-lookup"><span data-stu-id="4e3a1-602">60</span></span></td>
<td><span data-ttu-id="4e3a1-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4e3a1-604">535.31</span><span class="sxs-lookup"><span data-stu-id="4e3a1-604">535.31</span></span></td>
<td><span data-ttu-id="4e3a1-605">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-606">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-606">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-607">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-607">Product 2</span></span></td>
<td><span data-ttu-id="4e3a1-608">20</span><span class="sxs-lookup"><span data-stu-id="4e3a1-608">20</span></span></td>
<td><span data-ttu-id="4e3a1-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="4e3a1-610">178.44</span><span class="sxs-lookup"><span data-stu-id="4e3a1-610">178.44</span></span></td>
<td><span data-ttu-id="4e3a1-611">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-612">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-612">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-613">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-613">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-614">60</span><span class="sxs-lookup"><span data-stu-id="4e3a1-614">60</span></span></td>
<td><span data-ttu-id="4e3a1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4e3a1-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4e3a1-616">4,487.12</span></span></td>
<td><span data-ttu-id="4e3a1-617">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-618">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-618">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-619">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-619">Product 2</span></span></td>
<td><span data-ttu-id="4e3a1-620">20</span><span class="sxs-lookup"><span data-stu-id="4e3a1-620">20</span></span></td>
<td><span data-ttu-id="4e3a1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="4e3a1-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4e3a1-622">1,495.71</span></span></td>
<td><span data-ttu-id="4e3a1-623">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4e3a1-624">下表显示当包装服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-625">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-625">Cost object</span></span></th>
<th><span data-ttu-id="4e3a1-626">度量值</span><span class="sxs-lookup"><span data-stu-id="4e3a1-626">Magnitude</span></span></th>
<th><span data-ttu-id="4e3a1-627">分配系数</span><span class="sxs-lookup"><span data-stu-id="4e3a1-627">Allocation factor</span></span></th>
<th><span data-ttu-id="4e3a1-628">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-628">Amount</span></span></th>
<th><span data-ttu-id="4e3a1-629">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-630">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-630">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-631">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-631">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-632">80</span><span class="sxs-lookup"><span data-stu-id="4e3a1-632">80</span></span></td>
<td><span data-ttu-id="4e3a1-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4e3a1-634">241.05</span><span class="sxs-lookup"><span data-stu-id="4e3a1-634">241.05</span></span></td>
<td><span data-ttu-id="4e3a1-635">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-636">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-636">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-637">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-637">Product 2</span></span></td>
<td><span data-ttu-id="4e3a1-638">15</span><span class="sxs-lookup"><span data-stu-id="4e3a1-638">15</span></span></td>
<td><span data-ttu-id="4e3a1-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="4e3a1-640">45.20</span><span class="sxs-lookup"><span data-stu-id="4e3a1-640">45.20</span></span></td>
<td><span data-ttu-id="4e3a1-641">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-642">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-642">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-643">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-643">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-644">80</span><span class="sxs-lookup"><span data-stu-id="4e3a1-644">80</span></span></td>
<td><span data-ttu-id="4e3a1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4e3a1-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4e3a1-646">2,507.09</span></span></td>
<td><span data-ttu-id="4e3a1-647">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-648">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-648">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-649">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-649">Product 2</span></span></td>
<td><span data-ttu-id="4e3a1-650">15</span><span class="sxs-lookup"><span data-stu-id="4e3a1-650">15</span></span></td>
<td><span data-ttu-id="4e3a1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="4e3a1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="4e3a1-652">470.08</span><span class="sxs-lookup"><span data-stu-id="4e3a1-652">470.08</span></span></td>
<td><span data-ttu-id="4e3a1-653">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="4e3a1-654">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="4e3a1-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e3a1-655">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-655">Journal</span></span></th>
<th><span data-ttu-id="4e3a1-656">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="4e3a1-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="4e3a1-657">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="4e3a1-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="4e3a1-658">版本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-659">00004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-659">00004</span></span></td>
<td><span data-ttu-id="4e3a1-660">成本分配日记帐</span><span class="sxs-lookup"><span data-stu-id="4e3a1-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="4e3a1-661">会计</span><span class="sxs-lookup"><span data-stu-id="4e3a1-661">Fiscal</span></span></td>
<td><span data-ttu-id="4e3a1-662">2017</span><span class="sxs-lookup"><span data-stu-id="4e3a1-662">2017</span></span></td>
<td><span data-ttu-id="4e3a1-663">期间 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-663">Period 1</span></span></td>
<td><span data-ttu-id="4e3a1-664">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="4e3a1-665">日记帐行</span><span class="sxs-lookup"><span data-stu-id="4e3a1-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="4e3a1-666">会计日期</span><span class="sxs-lookup"><span data-stu-id="4e3a1-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-667">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-668">成本元素</span><span class="sxs-lookup"><span data-stu-id="4e3a1-668">Cost element</span></span></th>
<th><span data-ttu-id="4e3a1-669">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-669">Cost behavior</span></span></th>
<th><span data-ttu-id="4e3a1-670">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-671">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-672">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-672">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-673">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-673">HR</span></span></td>
<td><span data-ttu-id="4e3a1-674">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-674">10001</span></span></td>
<td><span data-ttu-id="4e3a1-675">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-675">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-676">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-676">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-677">500.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-678">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-679">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-679">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-680">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-680">HR</span></span></td>
<td><span data-ttu-id="4e3a1-681">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-681">10001</span></span></td>
<td><span data-ttu-id="4e3a1-682">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-682">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-683">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-683">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="4e3a1-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-685">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-686">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-686">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-687">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-687">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-688">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-688">10001</span></span></td>
<td><span data-ttu-id="4e3a1-689">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-689">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-690">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-690">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-691">675.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-692">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-693">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-693">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-694">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-694">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-695">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-695">10001</span></span></td>
<td><span data-ttu-id="4e3a1-696">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-696">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-697">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-697">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="4e3a1-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-699">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-700">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-700">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-701">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-701">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-702">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-702">10001</span></span></td>
<td><span data-ttu-id="4e3a1-703">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-703">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-704">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-704">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-705">713.75</span><span class="sxs-lookup"><span data-stu-id="4e3a1-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-706">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-707">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-707">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-708">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-708">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-709">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-709">10001</span></span></td>
<td><span data-ttu-id="4e3a1-710">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-710">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-711">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-711">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="4e3a1-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-713">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-714">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-714">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-715">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-715">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-716">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-716">10001</span></span></td>
<td><span data-ttu-id="4e3a1-717">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-717">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-718">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-718">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-719">286.25</span><span class="sxs-lookup"><span data-stu-id="4e3a1-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-720">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-721">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-721">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-722">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-722">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-723">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-723">10001</span></span></td>
<td><span data-ttu-id="4e3a1-724">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-724">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-725">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-725">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="4e3a1-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-727">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-728">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-728">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-729">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-729">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-730">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-730">10001</span></span></td>
<td><span data-ttu-id="4e3a1-731">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-731">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-732">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-732">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-733">776.36</span><span class="sxs-lookup"><span data-stu-id="4e3a1-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-734">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-735">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-735">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-736">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-736">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-737">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-737">10001</span></span></td>
<td><span data-ttu-id="4e3a1-738">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-738">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-739">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-739">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4e3a1-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-741">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-742">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-742">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-743">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-743">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-744">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-744">10001</span></span></td>
<td><span data-ttu-id="4e3a1-745">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-745">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-746">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-746">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-747">223.64</span><span class="sxs-lookup"><span data-stu-id="4e3a1-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-748">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="4e3a1-749">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-749">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-750">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-750">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-751">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-751">10001</span></span></td>
<td><span data-ttu-id="4e3a1-752">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-752">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-753">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-753">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4e3a1-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="4e3a1-755">成本条目</span><span class="sxs-lookup"><span data-stu-id="4e3a1-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="4e3a1-756">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="4e3a1-757">成本元素</span><span class="sxs-lookup"><span data-stu-id="4e3a1-757">Cost element</span></span></th>
<th><span data-ttu-id="4e3a1-758">成本行为</span><span class="sxs-lookup"><span data-stu-id="4e3a1-758">Cost behavior</span></span></th>
<th><span data-ttu-id="4e3a1-759">本币金额</span><span class="sxs-lookup"><span data-stu-id="4e3a1-759">Amount</span></span></th>
<th><span data-ttu-id="4e3a1-760">会计日期</span><span class="sxs-lookup"><span data-stu-id="4e3a1-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="4e3a1-761">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-761">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-762">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-762">HR</span></span></td>
<td><span data-ttu-id="4e3a1-763">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-763">10001</span></span></td>
<td><span data-ttu-id="4e3a1-764">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-764">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-765">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-765">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-766">-500.00</span></span></td>
<td><span data-ttu-id="4e3a1-767">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-768">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-768">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-769">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-769">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-770">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-770">10001</span></span></td>
<td><span data-ttu-id="4e3a1-771">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-771">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-772">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-772">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-773">175.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-773">175.00</span></span></td>
<td><span data-ttu-id="4e3a1-774">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-775">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-775">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-776">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-776">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-777">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-777">10001</span></span></td>
<td><span data-ttu-id="4e3a1-778">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-778">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-779">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-779">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-780">275.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-780">275.00</span></span></td>
<td><span data-ttu-id="4e3a1-781">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-782">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-782">CC004</span></span></td>
<td><span data-ttu-id="4e3a1-783">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-783">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-784">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-784">10001</span></span></td>
<td><span data-ttu-id="4e3a1-785">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-785">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-786">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-786">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-787">50,00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-787">50,00</span></span></td>
<td><span data-ttu-id="4e3a1-788">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-789">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-789">CC001</span></span></td>
<td><span data-ttu-id="4e3a1-790">HR</span><span class="sxs-lookup"><span data-stu-id="4e3a1-790">HR</span></span></td>
<td><span data-ttu-id="4e3a1-791">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-791">10001</span></span></td>
<td><span data-ttu-id="4e3a1-792">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-792">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-793">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-793">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="4e3a1-794">-1,245.71</span></span></td>
<td><span data-ttu-id="4e3a1-795">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-796">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-796">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-797">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-797">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-798">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-798">10001</span></span></td>
<td><span data-ttu-id="4e3a1-799">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-799">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-800">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-800">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-801">436.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-801">436.00</span></span></td>
<td><span data-ttu-id="4e3a1-802">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-803">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-803">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-804">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-804">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-805">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-805">10001</span></span></td>
<td><span data-ttu-id="4e3a1-806">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-806">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-807">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-807">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-808">685.14</span><span class="sxs-lookup"><span data-stu-id="4e3a1-808">685.14</span></span></td>
<td><span data-ttu-id="4e3a1-809">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-810">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-810">CC004</span></span></td>
<td><span data-ttu-id="4e3a1-811">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-811">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-812">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-812">10001</span></span></td>
<td><span data-ttu-id="4e3a1-813">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-813">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-814">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-814">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-815">124.57</span><span class="sxs-lookup"><span data-stu-id="4e3a1-815">124.57</span></span></td>
<td><span data-ttu-id="4e3a1-816">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-817">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-817">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-818">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-818">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-819">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-819">10001</span></span></td>
<td><span data-ttu-id="4e3a1-820">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-820">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-821">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-821">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-822">-675.00</span></span></td>
<td><span data-ttu-id="4e3a1-823">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-824">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-824">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-825">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-825">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-826">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-826">10001</span></span></td>
<td><span data-ttu-id="4e3a1-827">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-827">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-828">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-828">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-829">438.75</span><span class="sxs-lookup"><span data-stu-id="4e3a1-829">438.75</span></span></td>
<td><span data-ttu-id="4e3a1-830">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-831">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-831">CC004</span></span></td>
<td><span data-ttu-id="4e3a1-832">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-832">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-833">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-833">10001</span></span></td>
<td><span data-ttu-id="4e3a1-834">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-834">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-835">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-835">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-836">236.25</span><span class="sxs-lookup"><span data-stu-id="4e3a1-836">236.25</span></span></td>
<td><span data-ttu-id="4e3a1-837">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-838">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-838">CC002</span></span></td>
<td><span data-ttu-id="4e3a1-839">财务</span><span class="sxs-lookup"><span data-stu-id="4e3a1-839">Finance</span></span></td>
<td><span data-ttu-id="4e3a1-840">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-840">10001</span></span></td>
<td><span data-ttu-id="4e3a1-841">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-841">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-842">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-842">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="4e3a1-843">-8,150.29</span></span></td>
<td><span data-ttu-id="4e3a1-844">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-845">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-845">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-846">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-846">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-847">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-847">10001</span></span></td>
<td><span data-ttu-id="4e3a1-848">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-848">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-849">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-849">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="4e3a1-850">5,297.69</span></span></td>
<td><span data-ttu-id="4e3a1-851">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-852">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-852">CC004</span></span></td>
<td><span data-ttu-id="4e3a1-853">包装</span><span class="sxs-lookup"><span data-stu-id="4e3a1-853">Packaging</span></span></td>
<td><span data-ttu-id="4e3a1-854">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-854">10001</span></span></td>
<td><span data-ttu-id="4e3a1-855">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-855">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-856">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-856">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="4e3a1-857">2,852.60</span></span></td>
<td><span data-ttu-id="4e3a1-858">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-859">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-859">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-860">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-860">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-861">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-861">10001</span></span></td>
<td><span data-ttu-id="4e3a1-862">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-862">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-863">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-863">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="4e3a1-864">-713.75</span></span></td>
<td><span data-ttu-id="4e3a1-865">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-866">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-866">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-867">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-867">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-868">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-868">10001</span></span></td>
<td><span data-ttu-id="4e3a1-869">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-869">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-870">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-870">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-871">535.31</span><span class="sxs-lookup"><span data-stu-id="4e3a1-871">535.31</span></span></td>
<td><span data-ttu-id="4e3a1-872">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-873">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-873">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-874">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-874">Product 2</span></span></td>
<td><span data-ttu-id="4e3a1-875">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-875">10001</span></span></td>
<td><span data-ttu-id="4e3a1-876">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-876">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-877">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-877">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-878">178.44</span><span class="sxs-lookup"><span data-stu-id="4e3a1-878">178.44</span></span></td>
<td><span data-ttu-id="4e3a1-879">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-880">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-880">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-881">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-881">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-882">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-882">10001</span></span></td>
<td><span data-ttu-id="4e3a1-883">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-883">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-884">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-884">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="4e3a1-885">-5,982.83</span></span></td>
<td><span data-ttu-id="4e3a1-886">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-887">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-887">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-888">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-888">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-889">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-889">10001</span></span></td>
<td><span data-ttu-id="4e3a1-890">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-890">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-891">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-891">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="4e3a1-892">4,487.12</span></span></td>
<td><span data-ttu-id="4e3a1-893">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-894">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-894">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-895">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-895">Product 2</span></span></td>
<td><span data-ttu-id="4e3a1-896">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-896">10001</span></span></td>
<td><span data-ttu-id="4e3a1-897">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-897">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-898">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-898">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="4e3a1-899">1,495.71</span></span></td>
<td><span data-ttu-id="4e3a1-900">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-901">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-901">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-902">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-902">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-903">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-903">10001</span></span></td>
<td><span data-ttu-id="4e3a1-904">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-904">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-905">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-905">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="4e3a1-906">-286.25</span></span></td>
<td><span data-ttu-id="4e3a1-907">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-908">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-908">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-909">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-909">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-910">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-910">10001</span></span></td>
<td><span data-ttu-id="4e3a1-911">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-911">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-912">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-912">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-913">241.05</span><span class="sxs-lookup"><span data-stu-id="4e3a1-913">241.05</span></span></td>
<td><span data-ttu-id="4e3a1-914">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-915">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-915">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-916">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-916">Product 2</span></span></td>
<td><span data-ttu-id="4e3a1-917">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-917">10001</span></span></td>
<td><span data-ttu-id="4e3a1-918">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-918">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-919">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-919">Fixed cost</span></span></td>
<td><span data-ttu-id="4e3a1-920">45.20</span><span class="sxs-lookup"><span data-stu-id="4e3a1-920">45.20</span></span></td>
<td><span data-ttu-id="4e3a1-921">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-922">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-922">CC003</span></span></td>
<td><span data-ttu-id="4e3a1-923">程序集</span><span class="sxs-lookup"><span data-stu-id="4e3a1-923">Assembly</span></span></td>
<td><span data-ttu-id="4e3a1-924">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-924">10001</span></span></td>
<td><span data-ttu-id="4e3a1-925">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-925">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-926">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-926">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="4e3a1-927">-2,977.17</span></span></td>
<td><span data-ttu-id="4e3a1-928">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-929">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-929">Prod 1</span></span></td>
<td><span data-ttu-id="4e3a1-930">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-930">Product 1</span></span></td>
<td><span data-ttu-id="4e3a1-931">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-931">10001</span></span></td>
<td><span data-ttu-id="4e3a1-932">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-932">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-933">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-933">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="4e3a1-934">2,507.09</span></span></td>
<td><span data-ttu-id="4e3a1-935">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4e3a1-936">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-936">Prod 2</span></span></td>
<td><span data-ttu-id="4e3a1-937">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-937">Product 2</span></span></td>
<td><span data-ttu-id="4e3a1-938">10001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-938">10001</span></span></td>
<td><span data-ttu-id="4e3a1-939">电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-939">Electricity</span></span></td>
<td><span data-ttu-id="4e3a1-940">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-940">Variable cost</span></span></td>
<td><span data-ttu-id="4e3a1-941">470.08</span><span class="sxs-lookup"><span data-stu-id="4e3a1-941">470.08</span></span></td>
<td><span data-ttu-id="4e3a1-942">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="4e3a1-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="4e3a1-943">结论</span><span class="sxs-lookup"><span data-stu-id="4e3a1-943">Conclusion</span></span>
<span data-ttu-id="4e3a1-944">在财务会计中，10,000.00 电成本过帐到虚拟成本中心 ID。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="4e3a1-945">因此，成本会计员将了解必须分摊此成本。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="4e3a1-946">在成本核算中，跨组织单位和级别的成本流，基于所应用的政策和规则。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="4e3a1-947">每项成本已与为成本分摊提供最佳评估的分配基础关联。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="4e3a1-948">成本元素</span><span class="sxs-lookup"><span data-stu-id="4e3a1-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="4e3a1-949">成本对象</span><span class="sxs-lookup"><span data-stu-id="4e3a1-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="4e3a1-950">合计</span><span class="sxs-lookup"><span data-stu-id="4e3a1-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="4e3a1-951">CC099</span><span class="sxs-lookup"><span data-stu-id="4e3a1-951">CC099</span></span></th>
<th><span data-ttu-id="4e3a1-952">CC001</span><span class="sxs-lookup"><span data-stu-id="4e3a1-952">CC001</span></span></th>
<th><span data-ttu-id="4e3a1-953">CC002</span><span class="sxs-lookup"><span data-stu-id="4e3a1-953">CC002</span></span></th>
<th><span data-ttu-id="4e3a1-954">CC003</span><span class="sxs-lookup"><span data-stu-id="4e3a1-954">CC003</span></span></th>
<th><span data-ttu-id="4e3a1-955">CC004</span><span class="sxs-lookup"><span data-stu-id="4e3a1-955">CC004</span></span></th>
<th><span data-ttu-id="4e3a1-956">项目 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-956">Proj 1</span></span></th>
<th><span data-ttu-id="4e3a1-957">项目 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-957">Proj 2</span></span></th>
<th><span data-ttu-id="4e3a1-958">产品 1</span><span class="sxs-lookup"><span data-stu-id="4e3a1-958">Prod 1</span></span></th>
<th><span data-ttu-id="4e3a1-959">产品 2</span><span class="sxs-lookup"><span data-stu-id="4e3a1-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="4e3a1-960">10001 电</span><span class="sxs-lookup"><span data-stu-id="4e3a1-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="4e3a1-970">未分类</span><span class="sxs-lookup"><span data-stu-id="4e3a1-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-971">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="4e3a1-972">固定成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-973">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-974">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-975">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-976">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-977">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-978">776.36</span><span class="sxs-lookup"><span data-stu-id="4e3a1-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-979">223.64</span><span class="sxs-lookup"><span data-stu-id="4e3a1-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="4e3a1-981">可变成本</span><span class="sxs-lookup"><span data-stu-id="4e3a1-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-982">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-983">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-984">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-985">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-986">0.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-987">30.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-988">10.00</span><span class="sxs-lookup"><span data-stu-id="4e3a1-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="4e3a1-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="4e3a1-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="4e3a1-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="4e3a1-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="4e3a1-992">此主题显示主要成本元素“10001 电”如何流过成本对象。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="4e3a1-993">因此，此间接成本分摊到组织的最低级别。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="4e3a1-994">换言之，最低级别的成本对象承担成本。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="4e3a1-995">如果您需要成本对象之间的可视成本流，可以使用成本累积政策规则实现成本流可视化。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="4e3a1-996">有关详细信息，请参阅[成本累积政策和开销计算](cost-rollup.md)。</span><span class="sxs-lookup"><span data-stu-id="4e3a1-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



