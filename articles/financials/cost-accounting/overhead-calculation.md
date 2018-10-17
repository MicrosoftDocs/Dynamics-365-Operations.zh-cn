---
title: "开销计算"
description: "此主题描述计算和分配间接成本的典型流程。"
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: zh-cn
ms.lasthandoff: 10/05/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="faf1a-103">开销计算</span><span class="sxs-lookup"><span data-stu-id="faf1a-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="faf1a-104">此主题描述计算和分配间接成本的典型流程。</span><span class="sxs-lookup"><span data-stu-id="faf1a-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="faf1a-105">术语定义</span><span class="sxs-lookup"><span data-stu-id="faf1a-105">Term definition</span></span>
---------------

<span data-ttu-id="faf1a-106">间接成本是为业务运营支出的成本，但是不能直接归为任何具体的业务活动、产品或服务。</span><span class="sxs-lookup"><span data-stu-id="faf1a-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="faf1a-107">间接成本为营利活动的生成提供重要支持。</span><span class="sxs-lookup"><span data-stu-id="faf1a-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="faf1a-108">以下是一些开销成本示例：</span><span class="sxs-lookup"><span data-stu-id="faf1a-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="faf1a-109">租金</span><span class="sxs-lookup"><span data-stu-id="faf1a-109">Rent</span></span>
-   <span data-ttu-id="faf1a-110">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-110">Electricity</span></span>
-   <span data-ttu-id="faf1a-111">管理薪金</span><span class="sxs-lookup"><span data-stu-id="faf1a-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="faf1a-112">开销计算概览</span><span class="sxs-lookup"><span data-stu-id="faf1a-112">Overhead calculation overview</span></span>
<span data-ttu-id="faf1a-113">开销计算按正确顺序运行会计政策。</span><span class="sxs-lookup"><span data-stu-id="faf1a-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="faf1a-114">如果成本核算政策更改或检测到特定错误，您可以为同一个会计期间多次运行开销计算。</span><span class="sxs-lookup"><span data-stu-id="faf1a-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="faf1a-115">每次运行的开销计算将被存储并收到唯一版本 ID，让您可以比较各个版本的计算。</span><span class="sxs-lookup"><span data-stu-id="faf1a-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="faf1a-116">开销计算生成的成本条目接收会计日期。</span><span class="sxs-lookup"><span data-stu-id="faf1a-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="faf1a-117">此会计日期与计算中使用的会计期间的结束日期一致。</span><span class="sxs-lookup"><span data-stu-id="faf1a-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="faf1a-118">唯一版本 ID 由以下元素组成：</span><span class="sxs-lookup"><span data-stu-id="faf1a-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="faf1a-119">版本类型</span><span class="sxs-lookup"><span data-stu-id="faf1a-119">Version type</span></span>
-   <span data-ttu-id="faf1a-120">日期和时间</span><span class="sxs-lookup"><span data-stu-id="faf1a-120">Date and time</span></span>
-   <span data-ttu-id="faf1a-121">成本核算分类帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="faf1a-122">会计年度</span><span class="sxs-lookup"><span data-stu-id="faf1a-122">Fiscal year</span></span>
-   <span data-ttu-id="faf1a-123">会计期间</span><span class="sxs-lookup"><span data-stu-id="faf1a-123">Fiscal period</span></span>

<span data-ttu-id="faf1a-124">开销计算独立于版本运行。</span><span class="sxs-lookup"><span data-stu-id="faf1a-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="faf1a-125">因此，可以在实际版本前计算预算版本。</span><span class="sxs-lookup"><span data-stu-id="faf1a-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="faf1a-126">开销计算包括四个步骤，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="faf1a-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="faf1a-127">在每个步骤中，创建包含日记帐条目的日记帐标头。</span><span class="sxs-lookup"><span data-stu-id="faf1a-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="faf1a-128">此日记帐标头为每个计算步骤保留输入数据。</span><span class="sxs-lookup"><span data-stu-id="faf1a-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="faf1a-129">政策和规则应用于每个日记帐行，成本条目生成为输出。</span><span class="sxs-lookup"><span data-stu-id="faf1a-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="faf1a-130">因此，您始终具有完全的可跟踪性。</span><span class="sxs-lookup"><span data-stu-id="faf1a-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="faf1a-131">[![开销计算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="faf1a-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="faf1a-132">计算和分摊电间接成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="faf1a-133">在财务会计中，有些成本（如电）登记为总计。</span><span class="sxs-lookup"><span data-stu-id="faf1a-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="faf1a-134">因此，不为成本核算提供详细的管理洞察。</span><span class="sxs-lookup"><span data-stu-id="faf1a-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="faf1a-135">在成本核算中，为提供跨所有组织单位和级别的正确的管理洞察，成本必须流过各个组织单位。</span><span class="sxs-lookup"><span data-stu-id="faf1a-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="faf1a-136">此流必须基于消耗量的准确记录或公平评估。</span><span class="sxs-lookup"><span data-stu-id="faf1a-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="faf1a-137">在总帐中，可以过帐电成本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="faf1a-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="faf1a-138">会计日期</span><span class="sxs-lookup"><span data-stu-id="faf1a-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-139">成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-140">主科目</span><span class="sxs-lookup"><span data-stu-id="faf1a-140">Main account</span></span></th>
<th><span data-ttu-id="faf1a-141">按记帐币种计算的金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-142">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="faf1a-143">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-143">CC099</span></span></td>
<td><span data-ttu-id="faf1a-144">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-144">Default cost center</span></span></td>
<td><span data-ttu-id="faf1a-145">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-145">10001</span></span></td>
<td><span data-ttu-id="faf1a-146">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-146">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="faf1a-148">步骤 1：处理成本行为计算</span><span class="sxs-lookup"><span data-stu-id="faf1a-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="faf1a-149">默认情况下，当成本条目从源数据导入时，它们在成本核算中接收**未分类**成本行为分类。</span><span class="sxs-lookup"><span data-stu-id="faf1a-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="faf1a-150">通过应用成本行为政策规则，您可以将成本条目重新分类为**固定成本**或**可变成本**。</span><span class="sxs-lookup"><span data-stu-id="faf1a-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="faf1a-151">定义成本行为规则</span><span class="sxs-lookup"><span data-stu-id="faf1a-151">Define the cost behavior rule</span></span>

<span data-ttu-id="faf1a-152">在某些情况下，一部分成本是一项固定费用，其余成本基于消耗量。</span><span class="sxs-lookup"><span data-stu-id="faf1a-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="faf1a-153">通常电费帐单与此定义一致。</span><span class="sxs-lookup"><span data-stu-id="faf1a-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="faf1a-154">在支付特定固定费用后，您按千瓦时 (Kwh) 支付消耗量。</span><span class="sxs-lookup"><span data-stu-id="faf1a-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="faf1a-155">例如，如果固定成本费用为 1,000.00，以下是成本行为规则的定义：</span><span class="sxs-lookup"><span data-stu-id="faf1a-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="faf1a-156">固定金额 1,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="faf1a-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="faf1a-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="faf1a-158">1000,01 &lt; N = 可变</span><span class="sxs-lookup"><span data-stu-id="faf1a-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="faf1a-159">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="faf1a-160">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-160">Journal</span></span></th>
<th><span data-ttu-id="faf1a-161">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="faf1a-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="faf1a-162">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="faf1a-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="faf1a-163">版本</span><span class="sxs-lookup"><span data-stu-id="faf1a-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-164">00001</span><span class="sxs-lookup"><span data-stu-id="faf1a-164">00001</span></span></td>
<td><span data-ttu-id="faf1a-165">成本行为计算日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="faf1a-166">会计</span><span class="sxs-lookup"><span data-stu-id="faf1a-166">Fiscal</span></span></td>
<td><span data-ttu-id="faf1a-167">2017</span><span class="sxs-lookup"><span data-stu-id="faf1a-167">2017</span></span></td>
<td><span data-ttu-id="faf1a-168">期间 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-168">Period 1</span></span></td>
<td><span data-ttu-id="faf1a-169">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="faf1a-170">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="faf1a-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="faf1a-171">会计日期</span><span class="sxs-lookup"><span data-stu-id="faf1a-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-172">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-173">成本元素</span><span class="sxs-lookup"><span data-stu-id="faf1a-173">Cost element</span></span></th>
<th><span data-ttu-id="faf1a-174">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-174">Cost behavior</span></span></th>
<th><span data-ttu-id="faf1a-175">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-176">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="faf1a-177">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-177">CC099</span></span></td>
<td><span data-ttu-id="faf1a-178">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-178">Default cost center</span></span></td>
<td><span data-ttu-id="faf1a-179">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-179">10001</span></span></td>
<td><span data-ttu-id="faf1a-180">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-180">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-181">未分类</span><span class="sxs-lookup"><span data-stu-id="faf1a-181">Unclassified</span></span></td>
<td><span data-ttu-id="faf1a-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="faf1a-183">成本条目</span><span class="sxs-lookup"><span data-stu-id="faf1a-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-184">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-185">成本元素</span><span class="sxs-lookup"><span data-stu-id="faf1a-185">Cost element</span></span></th>
<th><span data-ttu-id="faf1a-186">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-186">Cost behavior</span></span></th>
<th><span data-ttu-id="faf1a-187">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-187">Amount</span></span></th>
<th><span data-ttu-id="faf1a-188">会计日期</span><span class="sxs-lookup"><span data-stu-id="faf1a-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-189">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-189">CC099</span></span></td>
<td><span data-ttu-id="faf1a-190">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-190">Default cost center</span></span></td>
<td><span data-ttu-id="faf1a-191">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-191">10001</span></span></td>
<td><span data-ttu-id="faf1a-192">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-192">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-193">未分类</span><span class="sxs-lookup"><span data-stu-id="faf1a-193">Unclassified</span></span></td>
<td><span data-ttu-id="faf1a-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-194">10,000.00</span></span></td>
<td><span data-ttu-id="faf1a-195">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-196">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-196">CC099</span></span></td>
<td><span data-ttu-id="faf1a-197">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-197">Default cost center</span></span></td>
<td><span data-ttu-id="faf1a-198">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-198">10001</span></span></td>
<td><span data-ttu-id="faf1a-199">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-199">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-200">未分类</span><span class="sxs-lookup"><span data-stu-id="faf1a-200">Unclassified</span></span></td>
<td><span data-ttu-id="faf1a-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-201">-10,000.00</span></span></td>
<td><span data-ttu-id="faf1a-202">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-203">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-203">CC099</span></span></td>
<td><span data-ttu-id="faf1a-204">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-204">Default cost center</span></span></td>
<td><span data-ttu-id="faf1a-205">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-205">10001</span></span></td>
<td><span data-ttu-id="faf1a-206">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-206">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-207">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-207">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-208">1,000.00</span></span></td>
<td><span data-ttu-id="faf1a-209">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-210">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-210">CC099</span></span></td>
<td><span data-ttu-id="faf1a-211">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-211">Default cost center</span></span></td>
<td><span data-ttu-id="faf1a-212">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-212">10001</span></span></td>
<td><span data-ttu-id="faf1a-213">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-213">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-214">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-214">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-215">9,000.00</span></span></td>
<td><span data-ttu-id="faf1a-216">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-217">有关详细信息，请参阅[创建成本行为策略并将其分配到成本控制单元](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)。</span><span class="sxs-lookup"><span data-stu-id="faf1a-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="faf1a-218">步骤 2：处理成本分配计算</span><span class="sxs-lookup"><span data-stu-id="faf1a-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="faf1a-219">成本分配用于通过应用相关的分摊基数将成本从一个成本对象重新分配到一个或多个其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="faf1a-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="faf1a-220">成本分配和成本分摊的不同之处在于，成本分配始终发生在原始成本的主要成本元素级别。</span><span class="sxs-lookup"><span data-stu-id="faf1a-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="faf1a-221">定义成本分配规则</span><span class="sxs-lookup"><span data-stu-id="faf1a-221">Define the cost distribution rule</span></span>

<span data-ttu-id="faf1a-222">在财务会计中，电成本通常登记为总计。</span><span class="sxs-lookup"><span data-stu-id="faf1a-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="faf1a-223">在成本核算中，此方法不足够详细。</span><span class="sxs-lookup"><span data-stu-id="faf1a-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="faf1a-224">可变成本应公平分配到各个成本对象。</span><span class="sxs-lookup"><span data-stu-id="faf1a-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="faf1a-225">最合理的分配基础是电的消耗量 (Kwh)。</span><span class="sxs-lookup"><span data-stu-id="faf1a-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="faf1a-226">创建名为“电”的统计维度成员并记录电的消耗量。</span><span class="sxs-lookup"><span data-stu-id="faf1a-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="faf1a-227">默认情况下，所有统计维度成员均可作为分配基础。</span><span class="sxs-lookup"><span data-stu-id="faf1a-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-228">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-228">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="faf1a-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-230">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-230">CC001</span></span></td>
<td><span data-ttu-id="faf1a-231">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-231">HR</span></span></td>
<td><span data-ttu-id="faf1a-232">1,000</span><span class="sxs-lookup"><span data-stu-id="faf1a-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-233">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-233">CC002</span></span></td>
<td><span data-ttu-id="faf1a-234">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-234">Finance</span></span></td>
<td><span data-ttu-id="faf1a-235">6,000</span><span class="sxs-lookup"><span data-stu-id="faf1a-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-236">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-236">CC003</span></span></td>
<td><span data-ttu-id="faf1a-237">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-237">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-238">0</span><span class="sxs-lookup"><span data-stu-id="faf1a-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-239">下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="faf1a-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-240">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-240">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-241">度量值</span><span class="sxs-lookup"><span data-stu-id="faf1a-241">Magnitude</span></span></th>
<th><span data-ttu-id="faf1a-242">分配系数</span><span class="sxs-lookup"><span data-stu-id="faf1a-242">Allocation factor</span></span></th>
<th><span data-ttu-id="faf1a-243">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-244">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-244">CC001</span></span></td>
<td><span data-ttu-id="faf1a-245">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-245">HR</span></span></td>
<td><span data-ttu-id="faf1a-246">1,000</span><span class="sxs-lookup"><span data-stu-id="faf1a-246">1,000</span></span></td>
<td><span data-ttu-id="faf1a-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="faf1a-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="faf1a-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-249">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-249">CC002</span></span></td>
<td><span data-ttu-id="faf1a-250">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-250">Finance</span></span></td>
<td><span data-ttu-id="faf1a-251">6,000</span><span class="sxs-lookup"><span data-stu-id="faf1a-251">6,000</span></span></td>
<td><span data-ttu-id="faf1a-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="faf1a-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="faf1a-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-254">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-254">CC003</span></span></td>
<td><span data-ttu-id="faf1a-255">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-255">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-256">0</span><span class="sxs-lookup"><span data-stu-id="faf1a-256">0</span></span></td>
<td><span data-ttu-id="faf1a-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="faf1a-258">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-259">固定成本应平均分配到消耗了电的单个成本对象。</span><span class="sxs-lookup"><span data-stu-id="faf1a-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="faf1a-260">可以通过在公式分配基础中使用电统计维度成员取得此结果：（电 &gt; 0.00）下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="faf1a-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-261">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-261">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-262">配方</span><span class="sxs-lookup"><span data-stu-id="faf1a-262">Formula</span></span></th>
<th><span data-ttu-id="faf1a-263">度量值</span><span class="sxs-lookup"><span data-stu-id="faf1a-263">Magnitude</span></span></th>
<th><span data-ttu-id="faf1a-264">分配系数</span><span class="sxs-lookup"><span data-stu-id="faf1a-264">Allocation factor</span></span></th>
<th><span data-ttu-id="faf1a-265">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-266">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-266">CC001</span></span></td>
<td><span data-ttu-id="faf1a-267">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-267">HR</span></span></td>
<td><span data-ttu-id="faf1a-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="faf1a-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="faf1a-269">1</span><span class="sxs-lookup"><span data-stu-id="faf1a-269">1</span></span></td>
<td><span data-ttu-id="faf1a-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="faf1a-271">500.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-272">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-272">CC002</span></span></td>
<td><span data-ttu-id="faf1a-273">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-273">Finance</span></span></td>
<td><span data-ttu-id="faf1a-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="faf1a-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="faf1a-275">1</span><span class="sxs-lookup"><span data-stu-id="faf1a-275">1</span></span></td>
<td><span data-ttu-id="faf1a-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="faf1a-277">500.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-278">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-278">CC003</span></span></td>
<td><span data-ttu-id="faf1a-279">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-279">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="faf1a-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="faf1a-281">0</span><span class="sxs-lookup"><span data-stu-id="faf1a-281">0</span></span></td>
<td><span data-ttu-id="faf1a-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="faf1a-283">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="faf1a-284">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="faf1a-285">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-285">Journal</span></span></th>
<th><span data-ttu-id="faf1a-286">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="faf1a-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="faf1a-287">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="faf1a-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="faf1a-288">版本</span><span class="sxs-lookup"><span data-stu-id="faf1a-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-289">00002</span><span class="sxs-lookup"><span data-stu-id="faf1a-289">00002</span></span></td>
<td><span data-ttu-id="faf1a-290">成本分配计算日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="faf1a-291">会计</span><span class="sxs-lookup"><span data-stu-id="faf1a-291">Fiscal</span></span></td>
<td><span data-ttu-id="faf1a-292">2017</span><span class="sxs-lookup"><span data-stu-id="faf1a-292">2017</span></span></td>
<td><span data-ttu-id="faf1a-293">期间 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-293">Period 1</span></span></td>
<td><span data-ttu-id="faf1a-294">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="faf1a-295">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="faf1a-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="faf1a-296">会计日期</span><span class="sxs-lookup"><span data-stu-id="faf1a-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-297">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-298">成本元素</span><span class="sxs-lookup"><span data-stu-id="faf1a-298">Cost element</span></span></th>
<th><span data-ttu-id="faf1a-299">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-299">Cost behavior</span></span></th>
<th><span data-ttu-id="faf1a-300">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-301">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-302">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-302">CC099</span></span></td>
<td><span data-ttu-id="faf1a-303">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-303">Default cost center</span></span></td>
<td><span data-ttu-id="faf1a-304">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-304">10001</span></span></td>
<td><span data-ttu-id="faf1a-305">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-305">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-306">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-306">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-308">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-309">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-309">CC099</span></span></td>
<td><span data-ttu-id="faf1a-310">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-310">Default cost center</span></span></td>
<td><span data-ttu-id="faf1a-311">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-311">10001</span></span></td>
<td><span data-ttu-id="faf1a-312">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-312">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-313">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-313">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="faf1a-315">成本条目</span><span class="sxs-lookup"><span data-stu-id="faf1a-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-316">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-317">成本元素</span><span class="sxs-lookup"><span data-stu-id="faf1a-317">Cost element</span></span></th>
<th><span data-ttu-id="faf1a-318">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-318">Cost behavior</span></span></th>
<th><span data-ttu-id="faf1a-319">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-319">Amount</span></span></th>
<th><span data-ttu-id="faf1a-320">会计日期</span><span class="sxs-lookup"><span data-stu-id="faf1a-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-321">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-321">CC099</span></span></td>
<td><span data-ttu-id="faf1a-322">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-322">Default cost center</span></span></td>
<td><span data-ttu-id="faf1a-323">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-323">10001</span></span></td>
<td><span data-ttu-id="faf1a-324">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-324">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-325">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-325">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-326">-1,000.00</span></span></td>
<td><span data-ttu-id="faf1a-327">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-328">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-328">CC001</span></span></td>
<td><span data-ttu-id="faf1a-329">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-329">HR</span></span></td>
<td><span data-ttu-id="faf1a-330">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-330">10001</span></span></td>
<td><span data-ttu-id="faf1a-331">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-331">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-332">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-332">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-333">500.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-333">500.00</span></span></td>
<td><span data-ttu-id="faf1a-334">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-335">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-335">CC002</span></span></td>
<td><span data-ttu-id="faf1a-336">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-336">Finance</span></span></td>
<td><span data-ttu-id="faf1a-337">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-337">10001</span></span></td>
<td><span data-ttu-id="faf1a-338">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-338">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-339">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-339">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-340">500.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-340">500.00</span></span></td>
<td><span data-ttu-id="faf1a-341">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-342">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-342">CC099</span></span></td>
<td><span data-ttu-id="faf1a-343">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="faf1a-343">Default cost center</span></span></td>
<td><span data-ttu-id="faf1a-344">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-344">10001</span></span></td>
<td><span data-ttu-id="faf1a-345">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-345">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-346">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-346">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-347">-9,000.00</span></span></td>
<td><span data-ttu-id="faf1a-348">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-349">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-349">CC001</span></span></td>
<td><span data-ttu-id="faf1a-350">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-350">HR</span></span></td>
<td><span data-ttu-id="faf1a-351">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-351">10001</span></span></td>
<td><span data-ttu-id="faf1a-352">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-352">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-353">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-353">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="faf1a-354">1,285.71</span></span></td>
<td><span data-ttu-id="faf1a-355">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-356">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-356">CC002</span></span></td>
<td><span data-ttu-id="faf1a-357">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-357">Finance</span></span></td>
<td><span data-ttu-id="faf1a-358">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-358">10001</span></span></td>
<td><span data-ttu-id="faf1a-359">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-359">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-360">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-360">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="faf1a-361">7,714.29</span></span></td>
<td><span data-ttu-id="faf1a-362">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-363">有关详细信息，请参阅[创建成本分配策略并将其分配到成本控制单元](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)。</span><span class="sxs-lookup"><span data-stu-id="faf1a-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="faf1a-364">步骤 3：处理开销比率计算</span><span class="sxs-lookup"><span data-stu-id="faf1a-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="faf1a-365">开销比率用于向一个或多个特定成本对象收费。</span><span class="sxs-lookup"><span data-stu-id="faf1a-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="faf1a-366">费用基于预先确定的成本率和来自指定的分配基础的度量值。</span><span class="sxs-lookup"><span data-stu-id="faf1a-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="faf1a-367">定义开销比率</span><span class="sxs-lookup"><span data-stu-id="faf1a-367">Define the overhead rate</span></span>

<span data-ttu-id="faf1a-368">成本对象 CC001 HR 生成一组内部项目。</span><span class="sxs-lookup"><span data-stu-id="faf1a-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="faf1a-369">创建名为“HR 项目”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="faf1a-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-370">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-370">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-371">工时</span><span class="sxs-lookup"><span data-stu-id="faf1a-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-372">项目 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-372">Proj 1</span></span></td>
<td><span data-ttu-id="faf1a-373">项目 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-373">Project 1</span></span></td>
<td><span data-ttu-id="faf1a-374">3</span><span class="sxs-lookup"><span data-stu-id="faf1a-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-375">项目 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-375">Proj 2</span></span></td>
<td><span data-ttu-id="faf1a-376">项目 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-376">Project 2</span></span></td>
<td><span data-ttu-id="faf1a-377">1</span><span class="sxs-lookup"><span data-stu-id="faf1a-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-378">成本项目份额预先确定的成本率已定义。</span><span class="sxs-lookup"><span data-stu-id="faf1a-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-379">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-379">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-380">成本元素</span><span class="sxs-lookup"><span data-stu-id="faf1a-380">Cost element</span></span></th>
<th><span data-ttu-id="faf1a-381">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-381">Cost behavior</span></span></th>
<th><span data-ttu-id="faf1a-382">单位</span><span class="sxs-lookup"><span data-stu-id="faf1a-382">Units</span></span></th>
<th><span data-ttu-id="faf1a-383">比率</span><span class="sxs-lookup"><span data-stu-id="faf1a-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-384">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-384">CC001</span></span></td>
<td><span data-ttu-id="faf1a-385">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-385">HR</span></span></td>
<td><span data-ttu-id="faf1a-386">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-386">10001</span></span></td>
<td><span data-ttu-id="faf1a-387">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-387">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-388">1</span><span class="sxs-lookup"><span data-stu-id="faf1a-388">1</span></span></td>
<td><span data-ttu-id="faf1a-389">10</span><span class="sxs-lookup"><span data-stu-id="faf1a-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-390">下表显示 HR 项目用作分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="faf1a-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-391">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-391">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-392">度量值</span><span class="sxs-lookup"><span data-stu-id="faf1a-392">Magnitude</span></span></th>
<th><span data-ttu-id="faf1a-393">成本元素</span><span class="sxs-lookup"><span data-stu-id="faf1a-393">Cost element</span></span></th>
<th><span data-ttu-id="faf1a-394">分配系数</span><span class="sxs-lookup"><span data-stu-id="faf1a-394">Allocation factor</span></span></th>
<th><span data-ttu-id="faf1a-395">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-396">项目 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-396">Proj 1</span></span></td>
<td><span data-ttu-id="faf1a-397">项目 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-397">Project 1</span></span></td>
<td><span data-ttu-id="faf1a-398">3</span><span class="sxs-lookup"><span data-stu-id="faf1a-398">3</span></span></td>
<td><span data-ttu-id="faf1a-399">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-399">10001</span></span></td>
<td><span data-ttu-id="faf1a-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="faf1a-401">30.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-402">项目 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-402">Proj 2</span></span></td>
<td><span data-ttu-id="faf1a-403">项目 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-403">Project 2</span></span></td>
<td><span data-ttu-id="faf1a-404">1</span><span class="sxs-lookup"><span data-stu-id="faf1a-404">1</span></span></td>
<td><span data-ttu-id="faf1a-405">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-405">10001</span></span></td>
<td><span data-ttu-id="faf1a-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="faf1a-407">10.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="faf1a-408">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="faf1a-409">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-409">Journal</span></span></th>
<th><span data-ttu-id="faf1a-410">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="faf1a-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="faf1a-411">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="faf1a-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="faf1a-412">版本</span><span class="sxs-lookup"><span data-stu-id="faf1a-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-413">00003</span><span class="sxs-lookup"><span data-stu-id="faf1a-413">00003</span></span></td>
<td><span data-ttu-id="faf1a-414">开销比率计算日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="faf1a-415">会计</span><span class="sxs-lookup"><span data-stu-id="faf1a-415">Fiscal</span></span></td>
<td><span data-ttu-id="faf1a-416">2017</span><span class="sxs-lookup"><span data-stu-id="faf1a-416">2017</span></span></td>
<td><span data-ttu-id="faf1a-417">期间 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-417">Period 1</span></span></td>
<td><span data-ttu-id="faf1a-418">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="faf1a-419">日记帐条目（开销比率计算的日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="faf1a-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="faf1a-420">会计日期</span><span class="sxs-lookup"><span data-stu-id="faf1a-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-421">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-421">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-422">度量值</span><span class="sxs-lookup"><span data-stu-id="faf1a-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-423">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-424">项目 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-424">Proj 1</span></span></td>
<td><span data-ttu-id="faf1a-425">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="faf1a-426">3.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-427">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-428">项目 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-428">Proj 2</span></span></td>
<td><span data-ttu-id="faf1a-429">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="faf1a-430">1.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="faf1a-431">成本条目</span><span class="sxs-lookup"><span data-stu-id="faf1a-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-432">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-433">成本元素</span><span class="sxs-lookup"><span data-stu-id="faf1a-433">Cost element</span></span></th>
<th><span data-ttu-id="faf1a-434">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-434">Cost behavior</span></span></th>
<th><span data-ttu-id="faf1a-435">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-435">Amount</span></span></th>
<th><span data-ttu-id="faf1a-436">会计日期</span><span class="sxs-lookup"><span data-stu-id="faf1a-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="faf1a-437">CC0001</span></span></td>
<td><span data-ttu-id="faf1a-438">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-438">HR</span></span></td>
<td><span data-ttu-id="faf1a-439">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-439">10001</span></span></td>
<td><span data-ttu-id="faf1a-440">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-440">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-441">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-441">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-442">-30.00</span></span></td>
<td><span data-ttu-id="faf1a-443">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-444">项目 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-444">Proj 1</span></span></td>
<td><span data-ttu-id="faf1a-445">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="faf1a-446">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-446">10001</span></span></td>
<td><span data-ttu-id="faf1a-447">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-447">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-448">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-448">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-449">30.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-449">30.00</span></span></td>
<td><span data-ttu-id="faf1a-450">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-451">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-451">CC001</span></span></td>
<td><span data-ttu-id="faf1a-452">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-452">HR</span></span></td>
<td><span data-ttu-id="faf1a-453">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-453">10001</span></span></td>
<td><span data-ttu-id="faf1a-454">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-454">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-455">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-455">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-456">-10.00</span></span></td>
<td><span data-ttu-id="faf1a-457">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-458">项目 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-458">Proj 2</span></span></td>
<td><span data-ttu-id="faf1a-459">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="faf1a-460">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-460">10001</span></span></td>
<td><span data-ttu-id="faf1a-461">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-461">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-462">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-462">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-463">10.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-463">10.00</span></span></td>
<td><span data-ttu-id="faf1a-464">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-465">有关详细信息，请参阅 [执行开销计算](cost-rollup.md#perform-overhead-calculation)。</span><span class="sxs-lookup"><span data-stu-id="faf1a-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="faf1a-466">步骤 4：处理成本分摊计算</span><span class="sxs-lookup"><span data-stu-id="faf1a-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="faf1a-467">分摊用于通过应用分配基础将成本对象的余额分配给其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="faf1a-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="faf1a-468">Finance and Operations 支持互惠分摊方法。</span><span class="sxs-lookup"><span data-stu-id="faf1a-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="faf1a-469">在互惠分摊方法中，辅助成本对象交换的互助服务被完全识别。</span><span class="sxs-lookup"><span data-stu-id="faf1a-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="faf1a-470">系统自动确定执行分摊的正确顺序。</span><span class="sxs-lookup"><span data-stu-id="faf1a-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="faf1a-471">成本对象的余额按单一分配基础分配。</span><span class="sxs-lookup"><span data-stu-id="faf1a-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="faf1a-472">支持跨成本对象维度及其各自成员的分摊。</span><span class="sxs-lookup"><span data-stu-id="faf1a-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="faf1a-473">分摊顺序由成本控制单元控制。</span><span class="sxs-lookup"><span data-stu-id="faf1a-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="faf1a-474">[![互惠方法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="faf1a-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="faf1a-475">定义成本分摊</span><span class="sxs-lookup"><span data-stu-id="faf1a-475">Define the cost allocation</span></span>

<span data-ttu-id="faf1a-476">这是说明如何跟踪成本流的简单示例。</span><span class="sxs-lookup"><span data-stu-id="faf1a-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="faf1a-477">成本对象 CC001 HR 生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="faf1a-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="faf1a-478">创建名为“HR 服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="faf1a-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-479">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-479">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-480">HR 服务</span><span class="sxs-lookup"><span data-stu-id="faf1a-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-481">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-481">CC002</span></span></td>
<td><span data-ttu-id="faf1a-482">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-482">Finance</span></span></td>
<td><span data-ttu-id="faf1a-483">35</span><span class="sxs-lookup"><span data-stu-id="faf1a-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-484">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-484">CC003</span></span></td>
<td><span data-ttu-id="faf1a-485">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-485">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-486">55</span><span class="sxs-lookup"><span data-stu-id="faf1a-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-487">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-487">CC004</span></span></td>
<td><span data-ttu-id="faf1a-488">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-488">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-489">10</span><span class="sxs-lookup"><span data-stu-id="faf1a-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-490">成本对象 CC002 财务生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="faf1a-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="faf1a-491">创建名为“财务服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="faf1a-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-492">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-492">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-493">财务服务</span><span class="sxs-lookup"><span data-stu-id="faf1a-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-494">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-494">CC003</span></span></td>
<td><span data-ttu-id="faf1a-495">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-495">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-496">65</span><span class="sxs-lookup"><span data-stu-id="faf1a-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-497">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-497">CC004</span></span></td>
<td><span data-ttu-id="faf1a-498">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-498">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-499">35</span><span class="sxs-lookup"><span data-stu-id="faf1a-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-500">成本对象 CC003 装配生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="faf1a-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="faf1a-501">创建名为“装配服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="faf1a-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-502">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-502">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-503">装配服务（小时）</span><span class="sxs-lookup"><span data-stu-id="faf1a-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-504">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-504">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-505">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-505">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-506">60</span><span class="sxs-lookup"><span data-stu-id="faf1a-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-507">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-507">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-508">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-508">Product 2</span></span></td>
<td><span data-ttu-id="faf1a-509">20</span><span class="sxs-lookup"><span data-stu-id="faf1a-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-510">成本对象 CC004 包装生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="faf1a-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="faf1a-511">创建名为“包装服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="faf1a-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-512">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-512">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-513">包装服务（小时）</span><span class="sxs-lookup"><span data-stu-id="faf1a-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-514">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-514">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-515">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-515">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-516">80</span><span class="sxs-lookup"><span data-stu-id="faf1a-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-517">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-517">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-518">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-518">Product 2</span></span></td>
<td><span data-ttu-id="faf1a-519">15</span><span class="sxs-lookup"><span data-stu-id="faf1a-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="faf1a-520">在 Finance and Operations 中，产品消耗的生产工时等统计度量可以派生自源数据。</span><span class="sxs-lookup"><span data-stu-id="faf1a-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="faf1a-521">有关详细信息，请参阅[统计度量提供方模板](statistical-measure-provider-template.md#statistical-measure-provider-template)。</span><span class="sxs-lookup"><span data-stu-id="faf1a-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="faf1a-522">下表显示当 HR 服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="faf1a-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-523">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-523">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-524">度量值</span><span class="sxs-lookup"><span data-stu-id="faf1a-524">Magnitude</span></span></th>
<th><span data-ttu-id="faf1a-525">分配系数</span><span class="sxs-lookup"><span data-stu-id="faf1a-525">Allocation factor</span></span></th>
<th><span data-ttu-id="faf1a-526">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-526">Amount</span></span></th>
<th><span data-ttu-id="faf1a-527">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-528">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-528">CC002</span></span></td>
<td><span data-ttu-id="faf1a-529">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-529">Finance</span></span></td>
<td><span data-ttu-id="faf1a-530">35</span><span class="sxs-lookup"><span data-stu-id="faf1a-530">35</span></span></td>
<td><span data-ttu-id="faf1a-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="faf1a-532">175.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-532">175.00</span></span></td>
<td><span data-ttu-id="faf1a-533">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-534">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-534">CC003</span></span></td>
<td><span data-ttu-id="faf1a-535">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-535">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-536">55</span><span class="sxs-lookup"><span data-stu-id="faf1a-536">55</span></span></td>
<td><span data-ttu-id="faf1a-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="faf1a-538">275.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-538">275.00</span></span></td>
<td><span data-ttu-id="faf1a-539">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-540">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-540">CC004</span></span></td>
<td><span data-ttu-id="faf1a-541">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-541">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-542">10</span><span class="sxs-lookup"><span data-stu-id="faf1a-542">10</span></span></td>
<td><span data-ttu-id="faf1a-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="faf1a-544">50.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-544">50.00</span></span></td>
<td><span data-ttu-id="faf1a-545">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-546">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-546">CC002</span></span></td>
<td><span data-ttu-id="faf1a-547">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-547">Finance</span></span></td>
<td><span data-ttu-id="faf1a-548">35</span><span class="sxs-lookup"><span data-stu-id="faf1a-548">35</span></span></td>
<td><span data-ttu-id="faf1a-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="faf1a-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="faf1a-550">436.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-550">436.00</span></span></td>
<td><span data-ttu-id="faf1a-551">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-552">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-552">CC003</span></span></td>
<td><span data-ttu-id="faf1a-553">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-553">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-554">55</span><span class="sxs-lookup"><span data-stu-id="faf1a-554">55</span></span></td>
<td><span data-ttu-id="faf1a-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="faf1a-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="faf1a-556">685.14</span><span class="sxs-lookup"><span data-stu-id="faf1a-556">685.14</span></span></td>
<td><span data-ttu-id="faf1a-557">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-558">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-558">CC004</span></span></td>
<td><span data-ttu-id="faf1a-559">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-559">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-560">10</span><span class="sxs-lookup"><span data-stu-id="faf1a-560">10</span></span></td>
<td><span data-ttu-id="faf1a-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="faf1a-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="faf1a-562">124.57</span><span class="sxs-lookup"><span data-stu-id="faf1a-562">124.57</span></span></td>
<td><span data-ttu-id="faf1a-563">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-564">下表显示当财务服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="faf1a-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-565">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-565">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-566">度量值</span><span class="sxs-lookup"><span data-stu-id="faf1a-566">Magnitude</span></span></th>
<th><span data-ttu-id="faf1a-567">分配系数</span><span class="sxs-lookup"><span data-stu-id="faf1a-567">Allocation factor</span></span></th>
<th><span data-ttu-id="faf1a-568">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-568">Amount</span></span></th>
<th><span data-ttu-id="faf1a-569">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-570">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-570">CC003</span></span></td>
<td><span data-ttu-id="faf1a-571">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-571">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-572">65</span><span class="sxs-lookup"><span data-stu-id="faf1a-572">65</span></span></td>
<td><span data-ttu-id="faf1a-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="faf1a-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="faf1a-574">438.75</span><span class="sxs-lookup"><span data-stu-id="faf1a-574">438.75</span></span></td>
<td><span data-ttu-id="faf1a-575">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-576">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-576">CC004</span></span></td>
<td><span data-ttu-id="faf1a-577">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-577">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-578">35</span><span class="sxs-lookup"><span data-stu-id="faf1a-578">35</span></span></td>
<td><span data-ttu-id="faf1a-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="faf1a-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="faf1a-580">236.25</span><span class="sxs-lookup"><span data-stu-id="faf1a-580">236.25</span></span></td>
<td><span data-ttu-id="faf1a-581">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-582">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-582">CC003</span></span></td>
<td><span data-ttu-id="faf1a-583">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-583">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-584">65</span><span class="sxs-lookup"><span data-stu-id="faf1a-584">65</span></span></td>
<td><span data-ttu-id="faf1a-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="faf1a-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="faf1a-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="faf1a-586">5,297.69</span></span></td>
<td><span data-ttu-id="faf1a-587">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-588">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-588">CC004</span></span></td>
<td><span data-ttu-id="faf1a-589">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-589">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-590">35</span><span class="sxs-lookup"><span data-stu-id="faf1a-590">35</span></span></td>
<td><span data-ttu-id="faf1a-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="faf1a-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="faf1a-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="faf1a-592">2,852.60</span></span></td>
<td><span data-ttu-id="faf1a-593">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-594">下表显示当装配服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="faf1a-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-595">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-595">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-596">度量值</span><span class="sxs-lookup"><span data-stu-id="faf1a-596">Magnitude</span></span></th>
<th><span data-ttu-id="faf1a-597">分配系数</span><span class="sxs-lookup"><span data-stu-id="faf1a-597">Allocation factor</span></span></th>
<th><span data-ttu-id="faf1a-598">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-598">Amount</span></span></th>
<th><span data-ttu-id="faf1a-599">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-600">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-600">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-601">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-601">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-602">60</span><span class="sxs-lookup"><span data-stu-id="faf1a-602">60</span></span></td>
<td><span data-ttu-id="faf1a-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="faf1a-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="faf1a-604">535.31</span><span class="sxs-lookup"><span data-stu-id="faf1a-604">535.31</span></span></td>
<td><span data-ttu-id="faf1a-605">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-606">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-606">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-607">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-607">Product 2</span></span></td>
<td><span data-ttu-id="faf1a-608">20</span><span class="sxs-lookup"><span data-stu-id="faf1a-608">20</span></span></td>
<td><span data-ttu-id="faf1a-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="faf1a-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="faf1a-610">178.44</span><span class="sxs-lookup"><span data-stu-id="faf1a-610">178.44</span></span></td>
<td><span data-ttu-id="faf1a-611">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-612">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-612">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-613">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-613">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-614">60</span><span class="sxs-lookup"><span data-stu-id="faf1a-614">60</span></span></td>
<td><span data-ttu-id="faf1a-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="faf1a-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="faf1a-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="faf1a-616">4,487.12</span></span></td>
<td><span data-ttu-id="faf1a-617">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-618">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-618">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-619">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-619">Product 2</span></span></td>
<td><span data-ttu-id="faf1a-620">20</span><span class="sxs-lookup"><span data-stu-id="faf1a-620">20</span></span></td>
<td><span data-ttu-id="faf1a-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="faf1a-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="faf1a-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="faf1a-622">1,495.71</span></span></td>
<td><span data-ttu-id="faf1a-623">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="faf1a-624">下表显示当包装服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="faf1a-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-625">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-625">Cost object</span></span></th>
<th><span data-ttu-id="faf1a-626">度量值</span><span class="sxs-lookup"><span data-stu-id="faf1a-626">Magnitude</span></span></th>
<th><span data-ttu-id="faf1a-627">分配系数</span><span class="sxs-lookup"><span data-stu-id="faf1a-627">Allocation factor</span></span></th>
<th><span data-ttu-id="faf1a-628">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-628">Amount</span></span></th>
<th><span data-ttu-id="faf1a-629">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-630">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-630">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-631">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-631">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-632">80</span><span class="sxs-lookup"><span data-stu-id="faf1a-632">80</span></span></td>
<td><span data-ttu-id="faf1a-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="faf1a-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="faf1a-634">241.05</span><span class="sxs-lookup"><span data-stu-id="faf1a-634">241.05</span></span></td>
<td><span data-ttu-id="faf1a-635">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-636">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-636">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-637">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-637">Product 2</span></span></td>
<td><span data-ttu-id="faf1a-638">15</span><span class="sxs-lookup"><span data-stu-id="faf1a-638">15</span></span></td>
<td><span data-ttu-id="faf1a-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="faf1a-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="faf1a-640">45.20</span><span class="sxs-lookup"><span data-stu-id="faf1a-640">45.20</span></span></td>
<td><span data-ttu-id="faf1a-641">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-642">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-642">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-643">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-643">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-644">80</span><span class="sxs-lookup"><span data-stu-id="faf1a-644">80</span></span></td>
<td><span data-ttu-id="faf1a-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="faf1a-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="faf1a-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="faf1a-646">2,507.09</span></span></td>
<td><span data-ttu-id="faf1a-647">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-648">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-648">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-649">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-649">Product 2</span></span></td>
<td><span data-ttu-id="faf1a-650">15</span><span class="sxs-lookup"><span data-stu-id="faf1a-650">15</span></span></td>
<td><span data-ttu-id="faf1a-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="faf1a-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="faf1a-652">470.08</span><span class="sxs-lookup"><span data-stu-id="faf1a-652">470.08</span></span></td>
<td><span data-ttu-id="faf1a-653">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="faf1a-654">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="faf1a-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="faf1a-655">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-655">Journal</span></span></th>
<th><span data-ttu-id="faf1a-656">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="faf1a-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="faf1a-657">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="faf1a-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="faf1a-658">版本</span><span class="sxs-lookup"><span data-stu-id="faf1a-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-659">00004</span><span class="sxs-lookup"><span data-stu-id="faf1a-659">00004</span></span></td>
<td><span data-ttu-id="faf1a-660">成本分配日记帐</span><span class="sxs-lookup"><span data-stu-id="faf1a-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="faf1a-661">会计</span><span class="sxs-lookup"><span data-stu-id="faf1a-661">Fiscal</span></span></td>
<td><span data-ttu-id="faf1a-662">2017</span><span class="sxs-lookup"><span data-stu-id="faf1a-662">2017</span></span></td>
<td><span data-ttu-id="faf1a-663">期间 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-663">Period 1</span></span></td>
<td><span data-ttu-id="faf1a-664">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="faf1a-665">日记帐行</span><span class="sxs-lookup"><span data-stu-id="faf1a-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="faf1a-666">会计日期</span><span class="sxs-lookup"><span data-stu-id="faf1a-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-667">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-668">成本元素</span><span class="sxs-lookup"><span data-stu-id="faf1a-668">Cost element</span></span></th>
<th><span data-ttu-id="faf1a-669">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-669">Cost behavior</span></span></th>
<th><span data-ttu-id="faf1a-670">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-671">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-672">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-672">CC001</span></span></td>
<td><span data-ttu-id="faf1a-673">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-673">HR</span></span></td>
<td><span data-ttu-id="faf1a-674">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-674">10001</span></span></td>
<td><span data-ttu-id="faf1a-675">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-675">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-676">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-676">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-677">500.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-678">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-679">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-679">CC001</span></span></td>
<td><span data-ttu-id="faf1a-680">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-680">HR</span></span></td>
<td><span data-ttu-id="faf1a-681">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-681">10001</span></span></td>
<td><span data-ttu-id="faf1a-682">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-682">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-683">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-683">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="faf1a-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-685">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-686">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-686">CC002</span></span></td>
<td><span data-ttu-id="faf1a-687">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-687">Finance</span></span></td>
<td><span data-ttu-id="faf1a-688">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-688">10001</span></span></td>
<td><span data-ttu-id="faf1a-689">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-689">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-690">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-690">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-691">675.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-692">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-693">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-693">CC002</span></span></td>
<td><span data-ttu-id="faf1a-694">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-694">Finance</span></span></td>
<td><span data-ttu-id="faf1a-695">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-695">10001</span></span></td>
<td><span data-ttu-id="faf1a-696">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-696">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-697">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-697">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="faf1a-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-699">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-700">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-700">CC003</span></span></td>
<td><span data-ttu-id="faf1a-701">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-701">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-702">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-702">10001</span></span></td>
<td><span data-ttu-id="faf1a-703">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-703">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-704">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-704">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-705">713.75</span><span class="sxs-lookup"><span data-stu-id="faf1a-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-706">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-707">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-707">CC003</span></span></td>
<td><span data-ttu-id="faf1a-708">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-708">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-709">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-709">10001</span></span></td>
<td><span data-ttu-id="faf1a-710">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-710">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-711">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-711">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="faf1a-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-713">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-714">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-714">CC003</span></span></td>
<td><span data-ttu-id="faf1a-715">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-715">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-716">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-716">10001</span></span></td>
<td><span data-ttu-id="faf1a-717">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-717">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-718">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-718">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-719">286.25</span><span class="sxs-lookup"><span data-stu-id="faf1a-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-720">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-721">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-721">CC003</span></span></td>
<td><span data-ttu-id="faf1a-722">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-722">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-723">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-723">10001</span></span></td>
<td><span data-ttu-id="faf1a-724">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-724">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-725">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-725">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="faf1a-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-727">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-728">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-728">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-729">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-729">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-730">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-730">10001</span></span></td>
<td><span data-ttu-id="faf1a-731">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-731">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-732">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-732">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-733">776.36</span><span class="sxs-lookup"><span data-stu-id="faf1a-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-734">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-735">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-735">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-736">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-736">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-737">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-737">10001</span></span></td>
<td><span data-ttu-id="faf1a-738">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-738">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-739">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-739">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="faf1a-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-741">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-742">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-742">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-743">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-743">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-744">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-744">10001</span></span></td>
<td><span data-ttu-id="faf1a-745">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-745">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-746">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-746">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-747">223.64</span><span class="sxs-lookup"><span data-stu-id="faf1a-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-748">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="faf1a-749">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-749">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-750">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-750">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-751">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-751">10001</span></span></td>
<td><span data-ttu-id="faf1a-752">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-752">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-753">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-753">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="faf1a-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="faf1a-755">成本条目</span><span class="sxs-lookup"><span data-stu-id="faf1a-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="faf1a-756">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="faf1a-757">成本元素</span><span class="sxs-lookup"><span data-stu-id="faf1a-757">Cost element</span></span></th>
<th><span data-ttu-id="faf1a-758">成本行为</span><span class="sxs-lookup"><span data-stu-id="faf1a-758">Cost behavior</span></span></th>
<th><span data-ttu-id="faf1a-759">本币金额</span><span class="sxs-lookup"><span data-stu-id="faf1a-759">Amount</span></span></th>
<th><span data-ttu-id="faf1a-760">会计日期</span><span class="sxs-lookup"><span data-stu-id="faf1a-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faf1a-761">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-761">CC001</span></span></td>
<td><span data-ttu-id="faf1a-762">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-762">HR</span></span></td>
<td><span data-ttu-id="faf1a-763">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-763">10001</span></span></td>
<td><span data-ttu-id="faf1a-764">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-764">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-765">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-765">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-766">-500.00</span></span></td>
<td><span data-ttu-id="faf1a-767">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-768">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-768">CC002</span></span></td>
<td><span data-ttu-id="faf1a-769">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-769">Finance</span></span></td>
<td><span data-ttu-id="faf1a-770">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-770">10001</span></span></td>
<td><span data-ttu-id="faf1a-771">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-771">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-772">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-772">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-773">175.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-773">175.00</span></span></td>
<td><span data-ttu-id="faf1a-774">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-775">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-775">CC003</span></span></td>
<td><span data-ttu-id="faf1a-776">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-776">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-777">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-777">10001</span></span></td>
<td><span data-ttu-id="faf1a-778">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-778">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-779">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-779">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-780">275.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-780">275.00</span></span></td>
<td><span data-ttu-id="faf1a-781">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-782">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-782">CC004</span></span></td>
<td><span data-ttu-id="faf1a-783">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-783">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-784">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-784">10001</span></span></td>
<td><span data-ttu-id="faf1a-785">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-785">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-786">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-786">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-787">50,00</span><span class="sxs-lookup"><span data-stu-id="faf1a-787">50,00</span></span></td>
<td><span data-ttu-id="faf1a-788">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-789">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-789">CC001</span></span></td>
<td><span data-ttu-id="faf1a-790">HR</span><span class="sxs-lookup"><span data-stu-id="faf1a-790">HR</span></span></td>
<td><span data-ttu-id="faf1a-791">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-791">10001</span></span></td>
<td><span data-ttu-id="faf1a-792">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-792">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-793">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-793">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="faf1a-794">-1,245.71</span></span></td>
<td><span data-ttu-id="faf1a-795">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-796">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-796">CC002</span></span></td>
<td><span data-ttu-id="faf1a-797">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-797">Finance</span></span></td>
<td><span data-ttu-id="faf1a-798">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-798">10001</span></span></td>
<td><span data-ttu-id="faf1a-799">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-799">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-800">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-800">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-801">436.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-801">436.00</span></span></td>
<td><span data-ttu-id="faf1a-802">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-803">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-803">CC003</span></span></td>
<td><span data-ttu-id="faf1a-804">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-804">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-805">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-805">10001</span></span></td>
<td><span data-ttu-id="faf1a-806">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-806">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-807">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-807">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-808">685.14</span><span class="sxs-lookup"><span data-stu-id="faf1a-808">685.14</span></span></td>
<td><span data-ttu-id="faf1a-809">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-810">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-810">CC004</span></span></td>
<td><span data-ttu-id="faf1a-811">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-811">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-812">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-812">10001</span></span></td>
<td><span data-ttu-id="faf1a-813">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-813">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-814">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-814">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-815">124.57</span><span class="sxs-lookup"><span data-stu-id="faf1a-815">124.57</span></span></td>
<td><span data-ttu-id="faf1a-816">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-817">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-817">CC002</span></span></td>
<td><span data-ttu-id="faf1a-818">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-818">Finance</span></span></td>
<td><span data-ttu-id="faf1a-819">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-819">10001</span></span></td>
<td><span data-ttu-id="faf1a-820">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-820">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-821">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-821">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-822">-675.00</span></span></td>
<td><span data-ttu-id="faf1a-823">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-824">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-824">CC003</span></span></td>
<td><span data-ttu-id="faf1a-825">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-825">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-826">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-826">10001</span></span></td>
<td><span data-ttu-id="faf1a-827">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-827">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-828">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-828">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-829">438.75</span><span class="sxs-lookup"><span data-stu-id="faf1a-829">438.75</span></span></td>
<td><span data-ttu-id="faf1a-830">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-831">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-831">CC004</span></span></td>
<td><span data-ttu-id="faf1a-832">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-832">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-833">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-833">10001</span></span></td>
<td><span data-ttu-id="faf1a-834">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-834">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-835">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-835">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-836">236.25</span><span class="sxs-lookup"><span data-stu-id="faf1a-836">236.25</span></span></td>
<td><span data-ttu-id="faf1a-837">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-838">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-838">CC002</span></span></td>
<td><span data-ttu-id="faf1a-839">财务</span><span class="sxs-lookup"><span data-stu-id="faf1a-839">Finance</span></span></td>
<td><span data-ttu-id="faf1a-840">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-840">10001</span></span></td>
<td><span data-ttu-id="faf1a-841">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-841">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-842">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-842">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="faf1a-843">-8,150.29</span></span></td>
<td><span data-ttu-id="faf1a-844">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-845">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-845">CC003</span></span></td>
<td><span data-ttu-id="faf1a-846">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-846">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-847">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-847">10001</span></span></td>
<td><span data-ttu-id="faf1a-848">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-848">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-849">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-849">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="faf1a-850">5,297.69</span></span></td>
<td><span data-ttu-id="faf1a-851">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-852">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-852">CC004</span></span></td>
<td><span data-ttu-id="faf1a-853">包装</span><span class="sxs-lookup"><span data-stu-id="faf1a-853">Packaging</span></span></td>
<td><span data-ttu-id="faf1a-854">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-854">10001</span></span></td>
<td><span data-ttu-id="faf1a-855">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-855">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-856">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-856">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="faf1a-857">2,852.60</span></span></td>
<td><span data-ttu-id="faf1a-858">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-859">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-859">CC003</span></span></td>
<td><span data-ttu-id="faf1a-860">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-860">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-861">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-861">10001</span></span></td>
<td><span data-ttu-id="faf1a-862">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-862">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-863">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-863">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="faf1a-864">-713.75</span></span></td>
<td><span data-ttu-id="faf1a-865">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-866">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-866">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-867">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-867">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-868">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-868">10001</span></span></td>
<td><span data-ttu-id="faf1a-869">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-869">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-870">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-870">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-871">535.31</span><span class="sxs-lookup"><span data-stu-id="faf1a-871">535.31</span></span></td>
<td><span data-ttu-id="faf1a-872">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-873">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-873">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-874">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-874">Product 2</span></span></td>
<td><span data-ttu-id="faf1a-875">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-875">10001</span></span></td>
<td><span data-ttu-id="faf1a-876">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-876">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-877">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-877">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-878">178.44</span><span class="sxs-lookup"><span data-stu-id="faf1a-878">178.44</span></span></td>
<td><span data-ttu-id="faf1a-879">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-880">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-880">CC003</span></span></td>
<td><span data-ttu-id="faf1a-881">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-881">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-882">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-882">10001</span></span></td>
<td><span data-ttu-id="faf1a-883">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-883">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-884">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-884">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="faf1a-885">-5,982.83</span></span></td>
<td><span data-ttu-id="faf1a-886">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-887">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-887">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-888">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-888">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-889">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-889">10001</span></span></td>
<td><span data-ttu-id="faf1a-890">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-890">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-891">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-891">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="faf1a-892">4,487.12</span></span></td>
<td><span data-ttu-id="faf1a-893">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-894">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-894">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-895">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-895">Product 2</span></span></td>
<td><span data-ttu-id="faf1a-896">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-896">10001</span></span></td>
<td><span data-ttu-id="faf1a-897">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-897">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-898">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-898">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="faf1a-899">1,495.71</span></span></td>
<td><span data-ttu-id="faf1a-900">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-901">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-901">CC003</span></span></td>
<td><span data-ttu-id="faf1a-902">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-902">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-903">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-903">10001</span></span></td>
<td><span data-ttu-id="faf1a-904">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-904">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-905">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-905">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="faf1a-906">-286.25</span></span></td>
<td><span data-ttu-id="faf1a-907">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-908">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-908">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-909">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-909">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-910">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-910">10001</span></span></td>
<td><span data-ttu-id="faf1a-911">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-911">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-912">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-912">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-913">241.05</span><span class="sxs-lookup"><span data-stu-id="faf1a-913">241.05</span></span></td>
<td><span data-ttu-id="faf1a-914">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-915">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-915">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-916">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-916">Product 2</span></span></td>
<td><span data-ttu-id="faf1a-917">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-917">10001</span></span></td>
<td><span data-ttu-id="faf1a-918">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-918">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-919">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-919">Fixed cost</span></span></td>
<td><span data-ttu-id="faf1a-920">45.20</span><span class="sxs-lookup"><span data-stu-id="faf1a-920">45.20</span></span></td>
<td><span data-ttu-id="faf1a-921">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-922">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-922">CC003</span></span></td>
<td><span data-ttu-id="faf1a-923">程序集</span><span class="sxs-lookup"><span data-stu-id="faf1a-923">Assembly</span></span></td>
<td><span data-ttu-id="faf1a-924">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-924">10001</span></span></td>
<td><span data-ttu-id="faf1a-925">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-925">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-926">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-926">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="faf1a-927">-2,977.17</span></span></td>
<td><span data-ttu-id="faf1a-928">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-929">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-929">Prod 1</span></span></td>
<td><span data-ttu-id="faf1a-930">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-930">Product 1</span></span></td>
<td><span data-ttu-id="faf1a-931">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-931">10001</span></span></td>
<td><span data-ttu-id="faf1a-932">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-932">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-933">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-933">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="faf1a-934">2,507.09</span></span></td>
<td><span data-ttu-id="faf1a-935">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faf1a-936">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-936">Prod 2</span></span></td>
<td><span data-ttu-id="faf1a-937">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-937">Product 2</span></span></td>
<td><span data-ttu-id="faf1a-938">10001</span><span class="sxs-lookup"><span data-stu-id="faf1a-938">10001</span></span></td>
<td><span data-ttu-id="faf1a-939">电</span><span class="sxs-lookup"><span data-stu-id="faf1a-939">Electricity</span></span></td>
<td><span data-ttu-id="faf1a-940">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-940">Variable cost</span></span></td>
<td><span data-ttu-id="faf1a-941">470.08</span><span class="sxs-lookup"><span data-stu-id="faf1a-941">470.08</span></span></td>
<td><span data-ttu-id="faf1a-942">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="faf1a-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="faf1a-943">结论</span><span class="sxs-lookup"><span data-stu-id="faf1a-943">Conclusion</span></span>
<span data-ttu-id="faf1a-944">在财务会计中，10,000.00 电成本过帐到虚拟成本中心 ID。</span><span class="sxs-lookup"><span data-stu-id="faf1a-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="faf1a-945">因此，成本会计员将了解必须分摊此成本。</span><span class="sxs-lookup"><span data-stu-id="faf1a-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="faf1a-946">在成本核算中，跨组织单位和级别的成本流，基于所应用的政策和规则。</span><span class="sxs-lookup"><span data-stu-id="faf1a-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="faf1a-947">每项成本已与为成本分摊提供最佳评估的分配基础关联。</span><span class="sxs-lookup"><span data-stu-id="faf1a-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="faf1a-948">成本元素</span><span class="sxs-lookup"><span data-stu-id="faf1a-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="faf1a-949">成本对象</span><span class="sxs-lookup"><span data-stu-id="faf1a-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="faf1a-950">合计</span><span class="sxs-lookup"><span data-stu-id="faf1a-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="faf1a-951">CC099</span><span class="sxs-lookup"><span data-stu-id="faf1a-951">CC099</span></span></th>
<th><span data-ttu-id="faf1a-952">CC001</span><span class="sxs-lookup"><span data-stu-id="faf1a-952">CC001</span></span></th>
<th><span data-ttu-id="faf1a-953">CC002</span><span class="sxs-lookup"><span data-stu-id="faf1a-953">CC002</span></span></th>
<th><span data-ttu-id="faf1a-954">CC003</span><span class="sxs-lookup"><span data-stu-id="faf1a-954">CC003</span></span></th>
<th><span data-ttu-id="faf1a-955">CC004</span><span class="sxs-lookup"><span data-stu-id="faf1a-955">CC004</span></span></th>
<th><span data-ttu-id="faf1a-956">项目 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-956">Proj 1</span></span></th>
<th><span data-ttu-id="faf1a-957">项目 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-957">Proj 2</span></span></th>
<th><span data-ttu-id="faf1a-958">产品 1</span><span class="sxs-lookup"><span data-stu-id="faf1a-958">Prod 1</span></span></th>
<th><span data-ttu-id="faf1a-959">产品 2</span><span class="sxs-lookup"><span data-stu-id="faf1a-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="faf1a-960">10001 电</span><span class="sxs-lookup"><span data-stu-id="faf1a-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="faf1a-970">未分类</span><span class="sxs-lookup"><span data-stu-id="faf1a-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-971">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="faf1a-972">固定成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-973">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-974">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-975">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-976">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-977">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-978">776.36</span><span class="sxs-lookup"><span data-stu-id="faf1a-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-979">223.64</span><span class="sxs-lookup"><span data-stu-id="faf1a-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="faf1a-981">可变成本</span><span class="sxs-lookup"><span data-stu-id="faf1a-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-982">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-983">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-984">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-985">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-986">0.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-987">30.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-988">10.00</span><span class="sxs-lookup"><span data-stu-id="faf1a-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="faf1a-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="faf1a-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="faf1a-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="faf1a-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="faf1a-992">此主题显示主要成本元素“10001 电”如何流过成本对象。</span><span class="sxs-lookup"><span data-stu-id="faf1a-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="faf1a-993">因此，此间接成本分摊到组织的最低级别。</span><span class="sxs-lookup"><span data-stu-id="faf1a-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="faf1a-994">换言之，最低级别的成本对象承担成本。</span><span class="sxs-lookup"><span data-stu-id="faf1a-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="faf1a-995">如果您需要成本对象之间的可视成本流，可以使用成本累积政策规则实现成本流可视化。</span><span class="sxs-lookup"><span data-stu-id="faf1a-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="faf1a-996">有关详细信息，请参阅[成本累积](cost-rollup.md)。</span><span class="sxs-lookup"><span data-stu-id="faf1a-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




