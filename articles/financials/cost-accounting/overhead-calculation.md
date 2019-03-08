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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "335109"
---
# <a name="overhead-calculation"></a><span data-ttu-id="c9c84-103">开销计算</span><span class="sxs-lookup"><span data-stu-id="c9c84-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9c84-104">此主题描述计算和分配间接成本的典型流程。</span><span class="sxs-lookup"><span data-stu-id="c9c84-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="c9c84-105">术语定义</span><span class="sxs-lookup"><span data-stu-id="c9c84-105">Term definition</span></span>
---------------

<span data-ttu-id="c9c84-106">间接成本是为业务运营支出的成本，但是不能直接归为任何具体的业务活动、产品或服务。</span><span class="sxs-lookup"><span data-stu-id="c9c84-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="c9c84-107">间接成本为营利活动的生成提供重要支持。</span><span class="sxs-lookup"><span data-stu-id="c9c84-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="c9c84-108">以下是一些开销成本示例：</span><span class="sxs-lookup"><span data-stu-id="c9c84-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="c9c84-109">租金</span><span class="sxs-lookup"><span data-stu-id="c9c84-109">Rent</span></span>
-   <span data-ttu-id="c9c84-110">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-110">Electricity</span></span>
-   <span data-ttu-id="c9c84-111">管理薪金</span><span class="sxs-lookup"><span data-stu-id="c9c84-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="c9c84-112">开销计算概览</span><span class="sxs-lookup"><span data-stu-id="c9c84-112">Overhead calculation overview</span></span>
<span data-ttu-id="c9c84-113">开销计算按正确顺序运行会计政策。</span><span class="sxs-lookup"><span data-stu-id="c9c84-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="c9c84-114">如果成本核算政策更改或检测到特定错误，您可以为同一个会计期间多次运行开销计算。</span><span class="sxs-lookup"><span data-stu-id="c9c84-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="c9c84-115">每次运行的开销计算将被存储并收到唯一版本 ID，让您可以比较各个版本的计算。</span><span class="sxs-lookup"><span data-stu-id="c9c84-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="c9c84-116">开销计算生成的成本条目接收会计日期。</span><span class="sxs-lookup"><span data-stu-id="c9c84-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="c9c84-117">此会计日期与计算中使用的会计期间的结束日期一致。</span><span class="sxs-lookup"><span data-stu-id="c9c84-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="c9c84-118">唯一版本 ID 由以下元素组成：</span><span class="sxs-lookup"><span data-stu-id="c9c84-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="c9c84-119">版本类型</span><span class="sxs-lookup"><span data-stu-id="c9c84-119">Version type</span></span>
-   <span data-ttu-id="c9c84-120">日期和时间</span><span class="sxs-lookup"><span data-stu-id="c9c84-120">Date and time</span></span>
-   <span data-ttu-id="c9c84-121">成本核算分类帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="c9c84-122">会计年度</span><span class="sxs-lookup"><span data-stu-id="c9c84-122">Fiscal year</span></span>
-   <span data-ttu-id="c9c84-123">会计期间</span><span class="sxs-lookup"><span data-stu-id="c9c84-123">Fiscal period</span></span>

<span data-ttu-id="c9c84-124">开销计算独立于版本运行。</span><span class="sxs-lookup"><span data-stu-id="c9c84-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="c9c84-125">因此，可以在实际版本前计算预算版本。</span><span class="sxs-lookup"><span data-stu-id="c9c84-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="c9c84-126">开销计算包括四个步骤，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="c9c84-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="c9c84-127">在每个步骤中，创建包含日记帐条目的日记帐标头。</span><span class="sxs-lookup"><span data-stu-id="c9c84-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="c9c84-128">此日记帐标头为每个计算步骤保留输入数据。</span><span class="sxs-lookup"><span data-stu-id="c9c84-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="c9c84-129">政策和规则应用于每个日记帐行，成本条目生成为输出。</span><span class="sxs-lookup"><span data-stu-id="c9c84-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="c9c84-130">因此，您始终具有完全的可跟踪性。</span><span class="sxs-lookup"><span data-stu-id="c9c84-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="c9c84-131">[![开销计算](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="c9c84-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="c9c84-132">计算和分摊电间接成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="c9c84-133">在财务会计中，有些成本（如电）登记为总计。</span><span class="sxs-lookup"><span data-stu-id="c9c84-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="c9c84-134">因此，不为成本核算提供详细的管理洞察。</span><span class="sxs-lookup"><span data-stu-id="c9c84-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="c9c84-135">在成本核算中，为提供跨所有组织单位和级别的正确的管理洞察，成本必须流过各个组织单位。</span><span class="sxs-lookup"><span data-stu-id="c9c84-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="c9c84-136">此流必须基于消耗量的准确记录或公平评估。</span><span class="sxs-lookup"><span data-stu-id="c9c84-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="c9c84-137">在总帐中，可以过帐电成本，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="c9c84-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9c84-138">会计日期</span><span class="sxs-lookup"><span data-stu-id="c9c84-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-139">成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-140">主科目</span><span class="sxs-lookup"><span data-stu-id="c9c84-140">Main account</span></span></th>
<th><span data-ttu-id="c9c84-141">按记帐币种计算的金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-142">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="c9c84-143">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-143">CC099</span></span></td>
<td><span data-ttu-id="c9c84-144">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-144">Default cost center</span></span></td>
<td><span data-ttu-id="c9c84-145">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-145">10001</span></span></td>
<td><span data-ttu-id="c9c84-146">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-146">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-147">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="c9c84-148">步骤 1：处理成本行为计算</span><span class="sxs-lookup"><span data-stu-id="c9c84-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="c9c84-149">默认情况下，当成本条目从源数据导入时，它们在成本核算中接收**未分类**成本行为分类。</span><span class="sxs-lookup"><span data-stu-id="c9c84-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="c9c84-150">通过应用成本行为政策规则，您可以将成本条目重新分类为**固定成本**或**可变成本**。</span><span class="sxs-lookup"><span data-stu-id="c9c84-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="c9c84-151">定义成本行为规则</span><span class="sxs-lookup"><span data-stu-id="c9c84-151">Define the cost behavior rule</span></span>

<span data-ttu-id="c9c84-152">在某些情况下，一部分成本是一项固定费用，其余成本基于消耗量。</span><span class="sxs-lookup"><span data-stu-id="c9c84-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="c9c84-153">通常电费帐单与此定义一致。</span><span class="sxs-lookup"><span data-stu-id="c9c84-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="c9c84-154">在支付特定固定费用后，您按千瓦时 (Kwh) 支付消耗量。</span><span class="sxs-lookup"><span data-stu-id="c9c84-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="c9c84-155">例如，如果固定成本费用为 1,000.00，以下是成本行为规则的定义：</span><span class="sxs-lookup"><span data-stu-id="c9c84-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="c9c84-156">固定金额 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="c9c84-157">0 &lt;= 1,000.00 = 固定</span><span class="sxs-lookup"><span data-stu-id="c9c84-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="c9c84-158">1000,01 &lt; N = 可变</span><span class="sxs-lookup"><span data-stu-id="c9c84-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="c9c84-159">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9c84-160">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-160">Journal</span></span></th>
<th><span data-ttu-id="c9c84-161">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="c9c84-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c9c84-162">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="c9c84-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c9c84-163">版本</span><span class="sxs-lookup"><span data-stu-id="c9c84-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-164">00001</span><span class="sxs-lookup"><span data-stu-id="c9c84-164">00001</span></span></td>
<td><span data-ttu-id="c9c84-165">成本行为计算日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="c9c84-166">会计</span><span class="sxs-lookup"><span data-stu-id="c9c84-166">Fiscal</span></span></td>
<td><span data-ttu-id="c9c84-167">2017</span><span class="sxs-lookup"><span data-stu-id="c9c84-167">2017</span></span></td>
<td><span data-ttu-id="c9c84-168">期间 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-168">Period 1</span></span></td>
<td><span data-ttu-id="c9c84-169">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c9c84-170">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="c9c84-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9c84-171">会计日期</span><span class="sxs-lookup"><span data-stu-id="c9c84-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-172">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-173">成本元素</span><span class="sxs-lookup"><span data-stu-id="c9c84-173">Cost element</span></span></th>
<th><span data-ttu-id="c9c84-174">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-174">Cost behavior</span></span></th>
<th><span data-ttu-id="c9c84-175">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-176">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="c9c84-177">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-177">CC099</span></span></td>
<td><span data-ttu-id="c9c84-178">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-178">Default cost center</span></span></td>
<td><span data-ttu-id="c9c84-179">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-179">10001</span></span></td>
<td><span data-ttu-id="c9c84-180">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-180">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-181">未分类</span><span class="sxs-lookup"><span data-stu-id="c9c84-181">Unclassified</span></span></td>
<td><span data-ttu-id="c9c84-182">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c9c84-183">成本条目</span><span class="sxs-lookup"><span data-stu-id="c9c84-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-184">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-185">成本元素</span><span class="sxs-lookup"><span data-stu-id="c9c84-185">Cost element</span></span></th>
<th><span data-ttu-id="c9c84-186">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-186">Cost behavior</span></span></th>
<th><span data-ttu-id="c9c84-187">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-187">Amount</span></span></th>
<th><span data-ttu-id="c9c84-188">会计日期</span><span class="sxs-lookup"><span data-stu-id="c9c84-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-189">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-189">CC099</span></span></td>
<td><span data-ttu-id="c9c84-190">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-190">Default cost center</span></span></td>
<td><span data-ttu-id="c9c84-191">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-191">10001</span></span></td>
<td><span data-ttu-id="c9c84-192">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-192">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-193">未分类</span><span class="sxs-lookup"><span data-stu-id="c9c84-193">Unclassified</span></span></td>
<td><span data-ttu-id="c9c84-194">10,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-194">10,000.00</span></span></td>
<td><span data-ttu-id="c9c84-195">2017 年 1 月 3 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-196">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-196">CC099</span></span></td>
<td><span data-ttu-id="c9c84-197">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-197">Default cost center</span></span></td>
<td><span data-ttu-id="c9c84-198">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-198">10001</span></span></td>
<td><span data-ttu-id="c9c84-199">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-199">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-200">未分类</span><span class="sxs-lookup"><span data-stu-id="c9c84-200">Unclassified</span></span></td>
<td><span data-ttu-id="c9c84-201">-10,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-201">-10,000.00</span></span></td>
<td><span data-ttu-id="c9c84-202">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-203">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-203">CC099</span></span></td>
<td><span data-ttu-id="c9c84-204">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-204">Default cost center</span></span></td>
<td><span data-ttu-id="c9c84-205">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-205">10001</span></span></td>
<td><span data-ttu-id="c9c84-206">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-206">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-207">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-207">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-208">1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-208">1,000.00</span></span></td>
<td><span data-ttu-id="c9c84-209">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-210">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-210">CC099</span></span></td>
<td><span data-ttu-id="c9c84-211">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-211">Default cost center</span></span></td>
<td><span data-ttu-id="c9c84-212">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-212">10001</span></span></td>
<td><span data-ttu-id="c9c84-213">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-213">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-214">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-214">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-215">9,000.00</span></span></td>
<td><span data-ttu-id="c9c84-216">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-217">有关详细信息，请参阅[创建成本行为策略并将其分配到成本控制单元](tasks/create-assign-cost-behavior-policy-cost-control-unit.md)。</span><span class="sxs-lookup"><span data-stu-id="c9c84-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="c9c84-218">步骤 2：处理成本分配计算</span><span class="sxs-lookup"><span data-stu-id="c9c84-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="c9c84-219">成本分配用于通过应用相关的分摊基数将成本从一个成本对象重新分配到一个或多个其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="c9c84-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="c9c84-220">成本分配和成本分摊的不同之处在于，成本分配始终发生在原始成本的主要成本元素级别。</span><span class="sxs-lookup"><span data-stu-id="c9c84-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="c9c84-221">定义成本分配规则</span><span class="sxs-lookup"><span data-stu-id="c9c84-221">Define the cost distribution rule</span></span>

<span data-ttu-id="c9c84-222">在财务会计中，电成本通常登记为总计。</span><span class="sxs-lookup"><span data-stu-id="c9c84-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="c9c84-223">在成本核算中，此方法不足够详细。</span><span class="sxs-lookup"><span data-stu-id="c9c84-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="c9c84-224">可变成本应公平分配到各个成本对象。</span><span class="sxs-lookup"><span data-stu-id="c9c84-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="c9c84-225">最合理的分配基础是电的消耗量 (Kwh)。</span><span class="sxs-lookup"><span data-stu-id="c9c84-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="c9c84-226">创建名为“电”的统计维度成员并记录电的消耗量。</span><span class="sxs-lookup"><span data-stu-id="c9c84-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="c9c84-227">默认情况下，所有统计维度成员均可作为分配基础。</span><span class="sxs-lookup"><span data-stu-id="c9c84-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-228">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-228">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="c9c84-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-230">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-230">CC001</span></span></td>
<td><span data-ttu-id="c9c84-231">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-231">HR</span></span></td>
<td><span data-ttu-id="c9c84-232">1,000</span><span class="sxs-lookup"><span data-stu-id="c9c84-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-233">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-233">CC002</span></span></td>
<td><span data-ttu-id="c9c84-234">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-234">Finance</span></span></td>
<td><span data-ttu-id="c9c84-235">6,000</span><span class="sxs-lookup"><span data-stu-id="c9c84-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-236">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-236">CC003</span></span></td>
<td><span data-ttu-id="c9c84-237">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-237">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-238">0</span><span class="sxs-lookup"><span data-stu-id="c9c84-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-239">下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="c9c84-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-240">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-240">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-241">度量值</span><span class="sxs-lookup"><span data-stu-id="c9c84-241">Magnitude</span></span></th>
<th><span data-ttu-id="c9c84-242">分配系数</span><span class="sxs-lookup"><span data-stu-id="c9c84-242">Allocation factor</span></span></th>
<th><span data-ttu-id="c9c84-243">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-244">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-244">CC001</span></span></td>
<td><span data-ttu-id="c9c84-245">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-245">HR</span></span></td>
<td><span data-ttu-id="c9c84-246">1,000</span><span class="sxs-lookup"><span data-stu-id="c9c84-246">1,000</span></span></td>
<td><span data-ttu-id="c9c84-247">(1,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c9c84-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c9c84-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-249">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-249">CC002</span></span></td>
<td><span data-ttu-id="c9c84-250">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-250">Finance</span></span></td>
<td><span data-ttu-id="c9c84-251">6,000</span><span class="sxs-lookup"><span data-stu-id="c9c84-251">6,000</span></span></td>
<td><span data-ttu-id="c9c84-252">(6,000 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c9c84-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c9c84-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-254">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-254">CC003</span></span></td>
<td><span data-ttu-id="c9c84-255">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-255">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-256">0</span><span class="sxs-lookup"><span data-stu-id="c9c84-256">0</span></span></td>
<td><span data-ttu-id="c9c84-257">(0 ÷ 7,000) × 9,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="c9c84-258">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-259">固定成本应平均分配到消耗了电的单个成本对象。</span><span class="sxs-lookup"><span data-stu-id="c9c84-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="c9c84-260">可以通过在公式分配基础中使用电统计维度成员取得此结果：（电 &gt; 0.00）下表显示当电消耗量用作可变成本的分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="c9c84-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-261">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-261">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-262">配方</span><span class="sxs-lookup"><span data-stu-id="c9c84-262">Formula</span></span></th>
<th><span data-ttu-id="c9c84-263">度量值</span><span class="sxs-lookup"><span data-stu-id="c9c84-263">Magnitude</span></span></th>
<th><span data-ttu-id="c9c84-264">分配系数</span><span class="sxs-lookup"><span data-stu-id="c9c84-264">Allocation factor</span></span></th>
<th><span data-ttu-id="c9c84-265">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-266">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-266">CC001</span></span></td>
<td><span data-ttu-id="c9c84-267">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-267">HR</span></span></td>
<td><span data-ttu-id="c9c84-268">(1,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c9c84-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c9c84-269">1</span><span class="sxs-lookup"><span data-stu-id="c9c84-269">1</span></span></td>
<td><span data-ttu-id="c9c84-270">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c9c84-271">500.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-272">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-272">CC002</span></span></td>
<td><span data-ttu-id="c9c84-273">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-273">Finance</span></span></td>
<td><span data-ttu-id="c9c84-274">(6,000 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c9c84-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c9c84-275">1</span><span class="sxs-lookup"><span data-stu-id="c9c84-275">1</span></span></td>
<td><span data-ttu-id="c9c84-276">(1 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c9c84-277">500.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-278">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-278">CC003</span></span></td>
<td><span data-ttu-id="c9c84-279">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-279">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-280">(0 &gt; 0.00)</span><span class="sxs-lookup"><span data-stu-id="c9c84-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="c9c84-281">0</span><span class="sxs-lookup"><span data-stu-id="c9c84-281">0</span></span></td>
<td><span data-ttu-id="c9c84-282">(0 ÷ 2) × 1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="c9c84-283">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c9c84-284">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9c84-285">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-285">Journal</span></span></th>
<th><span data-ttu-id="c9c84-286">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="c9c84-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c9c84-287">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="c9c84-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c9c84-288">版本</span><span class="sxs-lookup"><span data-stu-id="c9c84-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-289">00002</span><span class="sxs-lookup"><span data-stu-id="c9c84-289">00002</span></span></td>
<td><span data-ttu-id="c9c84-290">成本分配计算日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="c9c84-291">会计</span><span class="sxs-lookup"><span data-stu-id="c9c84-291">Fiscal</span></span></td>
<td><span data-ttu-id="c9c84-292">2017</span><span class="sxs-lookup"><span data-stu-id="c9c84-292">2017</span></span></td>
<td><span data-ttu-id="c9c84-293">期间 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-293">Period 1</span></span></td>
<td><span data-ttu-id="c9c84-294">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c9c84-295">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="c9c84-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9c84-296">会计日期</span><span class="sxs-lookup"><span data-stu-id="c9c84-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-297">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-298">成本元素</span><span class="sxs-lookup"><span data-stu-id="c9c84-298">Cost element</span></span></th>
<th><span data-ttu-id="c9c84-299">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-299">Cost behavior</span></span></th>
<th><span data-ttu-id="c9c84-300">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-301">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-302">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-302">CC099</span></span></td>
<td><span data-ttu-id="c9c84-303">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-303">Default cost center</span></span></td>
<td><span data-ttu-id="c9c84-304">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-304">10001</span></span></td>
<td><span data-ttu-id="c9c84-305">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-305">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-306">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-306">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-307">1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-308">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-309">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-309">CC099</span></span></td>
<td><span data-ttu-id="c9c84-310">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-310">Default cost center</span></span></td>
<td><span data-ttu-id="c9c84-311">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-311">10001</span></span></td>
<td><span data-ttu-id="c9c84-312">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-312">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-313">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-313">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c9c84-315">成本条目</span><span class="sxs-lookup"><span data-stu-id="c9c84-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-316">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-317">成本元素</span><span class="sxs-lookup"><span data-stu-id="c9c84-317">Cost element</span></span></th>
<th><span data-ttu-id="c9c84-318">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-318">Cost behavior</span></span></th>
<th><span data-ttu-id="c9c84-319">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-319">Amount</span></span></th>
<th><span data-ttu-id="c9c84-320">会计日期</span><span class="sxs-lookup"><span data-stu-id="c9c84-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-321">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-321">CC099</span></span></td>
<td><span data-ttu-id="c9c84-322">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-322">Default cost center</span></span></td>
<td><span data-ttu-id="c9c84-323">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-323">10001</span></span></td>
<td><span data-ttu-id="c9c84-324">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-324">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-325">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-325">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-326">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-326">-1,000.00</span></span></td>
<td><span data-ttu-id="c9c84-327">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-328">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-328">CC001</span></span></td>
<td><span data-ttu-id="c9c84-329">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-329">HR</span></span></td>
<td><span data-ttu-id="c9c84-330">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-330">10001</span></span></td>
<td><span data-ttu-id="c9c84-331">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-331">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-332">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-332">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-333">500.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-333">500.00</span></span></td>
<td><span data-ttu-id="c9c84-334">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-335">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-335">CC002</span></span></td>
<td><span data-ttu-id="c9c84-336">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-336">Finance</span></span></td>
<td><span data-ttu-id="c9c84-337">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-337">10001</span></span></td>
<td><span data-ttu-id="c9c84-338">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-338">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-339">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-339">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-340">500.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-340">500.00</span></span></td>
<td><span data-ttu-id="c9c84-341">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-342">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-342">CC099</span></span></td>
<td><span data-ttu-id="c9c84-343">默认成本中心</span><span class="sxs-lookup"><span data-stu-id="c9c84-343">Default cost center</span></span></td>
<td><span data-ttu-id="c9c84-344">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-344">10001</span></span></td>
<td><span data-ttu-id="c9c84-345">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-345">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-346">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-346">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-347">-9,000.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-347">-9,000.00</span></span></td>
<td><span data-ttu-id="c9c84-348">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-349">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-349">CC001</span></span></td>
<td><span data-ttu-id="c9c84-350">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-350">HR</span></span></td>
<td><span data-ttu-id="c9c84-351">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-351">10001</span></span></td>
<td><span data-ttu-id="c9c84-352">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-352">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-353">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-353">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="c9c84-354">1,285.71</span></span></td>
<td><span data-ttu-id="c9c84-355">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-356">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-356">CC002</span></span></td>
<td><span data-ttu-id="c9c84-357">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-357">Finance</span></span></td>
<td><span data-ttu-id="c9c84-358">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-358">10001</span></span></td>
<td><span data-ttu-id="c9c84-359">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-359">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-360">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-360">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="c9c84-361">7,714.29</span></span></td>
<td><span data-ttu-id="c9c84-362">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-363">有关详细信息，请参阅[创建成本分配策略并将其分配到成本控制单元](tasks/create-assign-cost-distribution-policy-cost-control-unit.md)。</span><span class="sxs-lookup"><span data-stu-id="c9c84-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="c9c84-364">步骤 3：处理开销比率计算</span><span class="sxs-lookup"><span data-stu-id="c9c84-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="c9c84-365">开销比率用于向一个或多个特定成本对象收费。</span><span class="sxs-lookup"><span data-stu-id="c9c84-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="c9c84-366">费用基于预先确定的成本率和来自指定的分配基础的度量值。</span><span class="sxs-lookup"><span data-stu-id="c9c84-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="c9c84-367">定义开销比率</span><span class="sxs-lookup"><span data-stu-id="c9c84-367">Define the overhead rate</span></span>

<span data-ttu-id="c9c84-368">成本对象 CC001 HR 生成一组内部项目。</span><span class="sxs-lookup"><span data-stu-id="c9c84-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="c9c84-369">创建名为“HR 项目”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="c9c84-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-370">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-370">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-371">工时</span><span class="sxs-lookup"><span data-stu-id="c9c84-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-372">项目 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-372">Proj 1</span></span></td>
<td><span data-ttu-id="c9c84-373">项目 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-373">Project 1</span></span></td>
<td><span data-ttu-id="c9c84-374">3</span><span class="sxs-lookup"><span data-stu-id="c9c84-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-375">项目 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-375">Proj 2</span></span></td>
<td><span data-ttu-id="c9c84-376">项目 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-376">Project 2</span></span></td>
<td><span data-ttu-id="c9c84-377">1</span><span class="sxs-lookup"><span data-stu-id="c9c84-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-378">成本项目份额预先确定的成本率已定义。</span><span class="sxs-lookup"><span data-stu-id="c9c84-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-379">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-379">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-380">成本元素</span><span class="sxs-lookup"><span data-stu-id="c9c84-380">Cost element</span></span></th>
<th><span data-ttu-id="c9c84-381">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-381">Cost behavior</span></span></th>
<th><span data-ttu-id="c9c84-382">单位</span><span class="sxs-lookup"><span data-stu-id="c9c84-382">Units</span></span></th>
<th><span data-ttu-id="c9c84-383">比率</span><span class="sxs-lookup"><span data-stu-id="c9c84-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-384">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-384">CC001</span></span></td>
<td><span data-ttu-id="c9c84-385">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-385">HR</span></span></td>
<td><span data-ttu-id="c9c84-386">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-386">10001</span></span></td>
<td><span data-ttu-id="c9c84-387">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-387">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-388">1</span><span class="sxs-lookup"><span data-stu-id="c9c84-388">1</span></span></td>
<td><span data-ttu-id="c9c84-389">10</span><span class="sxs-lookup"><span data-stu-id="c9c84-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-390">下表显示 HR 项目用作分配基础时的结果。</span><span class="sxs-lookup"><span data-stu-id="c9c84-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-391">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-391">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-392">度量值</span><span class="sxs-lookup"><span data-stu-id="c9c84-392">Magnitude</span></span></th>
<th><span data-ttu-id="c9c84-393">成本元素</span><span class="sxs-lookup"><span data-stu-id="c9c84-393">Cost element</span></span></th>
<th><span data-ttu-id="c9c84-394">分配系数</span><span class="sxs-lookup"><span data-stu-id="c9c84-394">Allocation factor</span></span></th>
<th><span data-ttu-id="c9c84-395">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-396">项目 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-396">Proj 1</span></span></td>
<td><span data-ttu-id="c9c84-397">项目 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-397">Project 1</span></span></td>
<td><span data-ttu-id="c9c84-398">3</span><span class="sxs-lookup"><span data-stu-id="c9c84-398">3</span></span></td>
<td><span data-ttu-id="c9c84-399">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-399">10001</span></span></td>
<td><span data-ttu-id="c9c84-400">(3 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c9c84-401">30.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-402">项目 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-402">Proj 2</span></span></td>
<td><span data-ttu-id="c9c84-403">项目 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-403">Project 2</span></span></td>
<td><span data-ttu-id="c9c84-404">1</span><span class="sxs-lookup"><span data-stu-id="c9c84-404">1</span></span></td>
<td><span data-ttu-id="c9c84-405">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-405">10001</span></span></td>
<td><span data-ttu-id="c9c84-406">(1 ÷ 1) × 10.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="c9c84-407">10.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="c9c84-408">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9c84-409">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-409">Journal</span></span></th>
<th><span data-ttu-id="c9c84-410">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="c9c84-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c9c84-411">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="c9c84-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c9c84-412">版本</span><span class="sxs-lookup"><span data-stu-id="c9c84-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-413">00003</span><span class="sxs-lookup"><span data-stu-id="c9c84-413">00003</span></span></td>
<td><span data-ttu-id="c9c84-414">开销比率计算日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="c9c84-415">会计</span><span class="sxs-lookup"><span data-stu-id="c9c84-415">Fiscal</span></span></td>
<td><span data-ttu-id="c9c84-416">2017</span><span class="sxs-lookup"><span data-stu-id="c9c84-416">2017</span></span></td>
<td><span data-ttu-id="c9c84-417">期间 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-417">Period 1</span></span></td>
<td><span data-ttu-id="c9c84-418">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="c9c84-419">日记帐条目（开销比率计算的日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="c9c84-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9c84-420">会计日期</span><span class="sxs-lookup"><span data-stu-id="c9c84-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-421">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-421">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-422">度量值</span><span class="sxs-lookup"><span data-stu-id="c9c84-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-423">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-424">项目 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-424">Proj 1</span></span></td>
<td><span data-ttu-id="c9c84-425">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c9c84-426">3.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-427">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-428">项目 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-428">Proj 2</span></span></td>
<td><span data-ttu-id="c9c84-429">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c9c84-430">1.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c9c84-431">成本条目</span><span class="sxs-lookup"><span data-stu-id="c9c84-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-432">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-433">成本元素</span><span class="sxs-lookup"><span data-stu-id="c9c84-433">Cost element</span></span></th>
<th><span data-ttu-id="c9c84-434">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-434">Cost behavior</span></span></th>
<th><span data-ttu-id="c9c84-435">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-435">Amount</span></span></th>
<th><span data-ttu-id="c9c84-436">会计日期</span><span class="sxs-lookup"><span data-stu-id="c9c84-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="c9c84-437">CC0001</span></span></td>
<td><span data-ttu-id="c9c84-438">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-438">HR</span></span></td>
<td><span data-ttu-id="c9c84-439">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-439">10001</span></span></td>
<td><span data-ttu-id="c9c84-440">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-440">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-441">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-441">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-442">-30.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-442">-30.00</span></span></td>
<td><span data-ttu-id="c9c84-443">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-444">项目 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-444">Proj 1</span></span></td>
<td><span data-ttu-id="c9c84-445">内部项目 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="c9c84-446">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-446">10001</span></span></td>
<td><span data-ttu-id="c9c84-447">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-447">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-448">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-448">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-449">30.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-449">30.00</span></span></td>
<td><span data-ttu-id="c9c84-450">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-451">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-451">CC001</span></span></td>
<td><span data-ttu-id="c9c84-452">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-452">HR</span></span></td>
<td><span data-ttu-id="c9c84-453">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-453">10001</span></span></td>
<td><span data-ttu-id="c9c84-454">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-454">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-455">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-455">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-456">-10.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-456">-10.00</span></span></td>
<td><span data-ttu-id="c9c84-457">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-458">项目 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-458">Proj 2</span></span></td>
<td><span data-ttu-id="c9c84-459">内部项目 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="c9c84-460">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-460">10001</span></span></td>
<td><span data-ttu-id="c9c84-461">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-461">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-462">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-462">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-463">10.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-463">10.00</span></span></td>
<td><span data-ttu-id="c9c84-464">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-465">有关详细信息，请参阅 [执行开销计算](cost-rollup.md#perform-overhead-calculation)。</span><span class="sxs-lookup"><span data-stu-id="c9c84-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="c9c84-466">步骤 4：处理成本分摊计算</span><span class="sxs-lookup"><span data-stu-id="c9c84-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="c9c84-467">分摊用于通过应用分配基础将成本对象的余额分配给其他成本对象。</span><span class="sxs-lookup"><span data-stu-id="c9c84-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="c9c84-468">Finance and Operations 支持互惠分摊方法。</span><span class="sxs-lookup"><span data-stu-id="c9c84-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="c9c84-469">在互惠分摊方法中，辅助成本对象交换的互助服务被完全识别。</span><span class="sxs-lookup"><span data-stu-id="c9c84-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="c9c84-470">系统自动确定执行分摊的正确顺序。</span><span class="sxs-lookup"><span data-stu-id="c9c84-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="c9c84-471">成本对象的余额按单一分配基础分配。</span><span class="sxs-lookup"><span data-stu-id="c9c84-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="c9c84-472">支持跨成本对象维度及其各自成员的分摊。</span><span class="sxs-lookup"><span data-stu-id="c9c84-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="c9c84-473">分摊顺序由成本控制单元控制。</span><span class="sxs-lookup"><span data-stu-id="c9c84-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="c9c84-474">[![互惠方法](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="c9c84-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="c9c84-475">定义成本分摊</span><span class="sxs-lookup"><span data-stu-id="c9c84-475">Define the cost allocation</span></span>

<span data-ttu-id="c9c84-476">这是说明如何跟踪成本流的简单示例。</span><span class="sxs-lookup"><span data-stu-id="c9c84-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="c9c84-477">成本对象 CC001 HR 生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="c9c84-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="c9c84-478">创建名为“HR 服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="c9c84-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-479">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-479">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-480">HR 服务</span><span class="sxs-lookup"><span data-stu-id="c9c84-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-481">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-481">CC002</span></span></td>
<td><span data-ttu-id="c9c84-482">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-482">Finance</span></span></td>
<td><span data-ttu-id="c9c84-483">35</span><span class="sxs-lookup"><span data-stu-id="c9c84-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-484">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-484">CC003</span></span></td>
<td><span data-ttu-id="c9c84-485">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-485">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-486">55</span><span class="sxs-lookup"><span data-stu-id="c9c84-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-487">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-487">CC004</span></span></td>
<td><span data-ttu-id="c9c84-488">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-488">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-489">10</span><span class="sxs-lookup"><span data-stu-id="c9c84-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-490">成本对象 CC002 财务生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="c9c84-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="c9c84-491">创建名为“财务服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="c9c84-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-492">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-492">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-493">财务服务</span><span class="sxs-lookup"><span data-stu-id="c9c84-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-494">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-494">CC003</span></span></td>
<td><span data-ttu-id="c9c84-495">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-495">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-496">65</span><span class="sxs-lookup"><span data-stu-id="c9c84-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-497">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-497">CC004</span></span></td>
<td><span data-ttu-id="c9c84-498">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-498">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-499">35</span><span class="sxs-lookup"><span data-stu-id="c9c84-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-500">成本对象 CC003 装配生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="c9c84-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="c9c84-501">创建名为“装配服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="c9c84-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-502">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-502">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-503">装配服务（小时）</span><span class="sxs-lookup"><span data-stu-id="c9c84-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-504">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-504">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-505">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-505">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-506">60</span><span class="sxs-lookup"><span data-stu-id="c9c84-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-507">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-507">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-508">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-508">Product 2</span></span></td>
<td><span data-ttu-id="c9c84-509">20</span><span class="sxs-lookup"><span data-stu-id="c9c84-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-510">成本对象 CC004 包装生成若干成本对象。</span><span class="sxs-lookup"><span data-stu-id="c9c84-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="c9c84-511">创建名为“包装服务”的统计维度成员来测量消耗度量值。</span><span class="sxs-lookup"><span data-stu-id="c9c84-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-512">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-512">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-513">包装服务（小时）</span><span class="sxs-lookup"><span data-stu-id="c9c84-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-514">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-514">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-515">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-515">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-516">80</span><span class="sxs-lookup"><span data-stu-id="c9c84-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-517">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-517">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-518">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-518">Product 2</span></span></td>
<td><span data-ttu-id="c9c84-519">15</span><span class="sxs-lookup"><span data-stu-id="c9c84-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c9c84-520">在 Finance and Operations 中，产品消耗的生产工时等统计度量可以派生自源数据。</span><span class="sxs-lookup"><span data-stu-id="c9c84-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="c9c84-521">有关详细信息，请参阅[统计度量提供方模板](statistical-measure-provider-template.md#statistical-measure-provider-template)。</span><span class="sxs-lookup"><span data-stu-id="c9c84-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="c9c84-522">下表显示当 HR 服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="c9c84-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-523">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-523">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-524">度量值</span><span class="sxs-lookup"><span data-stu-id="c9c84-524">Magnitude</span></span></th>
<th><span data-ttu-id="c9c84-525">分配系数</span><span class="sxs-lookup"><span data-stu-id="c9c84-525">Allocation factor</span></span></th>
<th><span data-ttu-id="c9c84-526">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-526">Amount</span></span></th>
<th><span data-ttu-id="c9c84-527">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-528">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-528">CC002</span></span></td>
<td><span data-ttu-id="c9c84-529">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-529">Finance</span></span></td>
<td><span data-ttu-id="c9c84-530">35</span><span class="sxs-lookup"><span data-stu-id="c9c84-530">35</span></span></td>
<td><span data-ttu-id="c9c84-531">(35 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c9c84-532">175.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-532">175.00</span></span></td>
<td><span data-ttu-id="c9c84-533">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-534">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-534">CC003</span></span></td>
<td><span data-ttu-id="c9c84-535">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-535">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-536">55</span><span class="sxs-lookup"><span data-stu-id="c9c84-536">55</span></span></td>
<td><span data-ttu-id="c9c84-537">(55 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c9c84-538">275.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-538">275.00</span></span></td>
<td><span data-ttu-id="c9c84-539">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-540">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-540">CC004</span></span></td>
<td><span data-ttu-id="c9c84-541">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-541">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-542">10</span><span class="sxs-lookup"><span data-stu-id="c9c84-542">10</span></span></td>
<td><span data-ttu-id="c9c84-543">(10 ÷ 100) × 500.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="c9c84-544">50.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-544">50.00</span></span></td>
<td><span data-ttu-id="c9c84-545">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-546">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-546">CC002</span></span></td>
<td><span data-ttu-id="c9c84-547">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-547">Finance</span></span></td>
<td><span data-ttu-id="c9c84-548">35</span><span class="sxs-lookup"><span data-stu-id="c9c84-548">35</span></span></td>
<td><span data-ttu-id="c9c84-549">(35 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c9c84-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c9c84-550">436.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-550">436.00</span></span></td>
<td><span data-ttu-id="c9c84-551">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-552">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-552">CC003</span></span></td>
<td><span data-ttu-id="c9c84-553">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-553">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-554">55</span><span class="sxs-lookup"><span data-stu-id="c9c84-554">55</span></span></td>
<td><span data-ttu-id="c9c84-555">(55 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c9c84-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c9c84-556">685.14</span><span class="sxs-lookup"><span data-stu-id="c9c84-556">685.14</span></span></td>
<td><span data-ttu-id="c9c84-557">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-558">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-558">CC004</span></span></td>
<td><span data-ttu-id="c9c84-559">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-559">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-560">10</span><span class="sxs-lookup"><span data-stu-id="c9c84-560">10</span></span></td>
<td><span data-ttu-id="c9c84-561">(10 ÷ 100) × 1,245.71</span><span class="sxs-lookup"><span data-stu-id="c9c84-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="c9c84-562">124.57</span><span class="sxs-lookup"><span data-stu-id="c9c84-562">124.57</span></span></td>
<td><span data-ttu-id="c9c84-563">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-564">下表显示当财务服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="c9c84-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-565">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-565">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-566">度量值</span><span class="sxs-lookup"><span data-stu-id="c9c84-566">Magnitude</span></span></th>
<th><span data-ttu-id="c9c84-567">分配系数</span><span class="sxs-lookup"><span data-stu-id="c9c84-567">Allocation factor</span></span></th>
<th><span data-ttu-id="c9c84-568">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-568">Amount</span></span></th>
<th><span data-ttu-id="c9c84-569">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-570">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-570">CC003</span></span></td>
<td><span data-ttu-id="c9c84-571">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-571">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-572">65</span><span class="sxs-lookup"><span data-stu-id="c9c84-572">65</span></span></td>
<td><span data-ttu-id="c9c84-573">(65 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c9c84-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c9c84-574">438.75</span><span class="sxs-lookup"><span data-stu-id="c9c84-574">438.75</span></span></td>
<td><span data-ttu-id="c9c84-575">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-576">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-576">CC004</span></span></td>
<td><span data-ttu-id="c9c84-577">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-577">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-578">35</span><span class="sxs-lookup"><span data-stu-id="c9c84-578">35</span></span></td>
<td><span data-ttu-id="c9c84-579">(35 ÷ 100) × (500.00 + 175.00)</span><span class="sxs-lookup"><span data-stu-id="c9c84-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="c9c84-580">236.25</span><span class="sxs-lookup"><span data-stu-id="c9c84-580">236.25</span></span></td>
<td><span data-ttu-id="c9c84-581">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-582">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-582">CC003</span></span></td>
<td><span data-ttu-id="c9c84-583">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-583">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-584">65</span><span class="sxs-lookup"><span data-stu-id="c9c84-584">65</span></span></td>
<td><span data-ttu-id="c9c84-585">(65 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c9c84-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c9c84-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c9c84-586">5,297.69</span></span></td>
<td><span data-ttu-id="c9c84-587">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-588">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-588">CC004</span></span></td>
<td><span data-ttu-id="c9c84-589">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-589">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-590">35</span><span class="sxs-lookup"><span data-stu-id="c9c84-590">35</span></span></td>
<td><span data-ttu-id="c9c84-591">(35 ÷ 100) × (7,714.29 + 436.00)</span><span class="sxs-lookup"><span data-stu-id="c9c84-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="c9c84-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c9c84-592">2,852.60</span></span></td>
<td><span data-ttu-id="c9c84-593">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-594">下表显示当装配服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="c9c84-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-595">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-595">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-596">度量值</span><span class="sxs-lookup"><span data-stu-id="c9c84-596">Magnitude</span></span></th>
<th><span data-ttu-id="c9c84-597">分配系数</span><span class="sxs-lookup"><span data-stu-id="c9c84-597">Allocation factor</span></span></th>
<th><span data-ttu-id="c9c84-598">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-598">Amount</span></span></th>
<th><span data-ttu-id="c9c84-599">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-600">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-600">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-601">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-601">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-602">60</span><span class="sxs-lookup"><span data-stu-id="c9c84-602">60</span></span></td>
<td><span data-ttu-id="c9c84-603">(60 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c9c84-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c9c84-604">535.31</span><span class="sxs-lookup"><span data-stu-id="c9c84-604">535.31</span></span></td>
<td><span data-ttu-id="c9c84-605">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-606">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-606">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-607">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-607">Product 2</span></span></td>
<td><span data-ttu-id="c9c84-608">20</span><span class="sxs-lookup"><span data-stu-id="c9c84-608">20</span></span></td>
<td><span data-ttu-id="c9c84-609">(20 ÷ 80) × (275.00 + 438.75)</span><span class="sxs-lookup"><span data-stu-id="c9c84-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="c9c84-610">178.44</span><span class="sxs-lookup"><span data-stu-id="c9c84-610">178.44</span></span></td>
<td><span data-ttu-id="c9c84-611">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-612">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-612">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-613">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-613">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-614">60</span><span class="sxs-lookup"><span data-stu-id="c9c84-614">60</span></span></td>
<td><span data-ttu-id="c9c84-615">(60 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c9c84-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c9c84-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c9c84-616">4,487.12</span></span></td>
<td><span data-ttu-id="c9c84-617">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-618">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-618">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-619">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-619">Product 2</span></span></td>
<td><span data-ttu-id="c9c84-620">20</span><span class="sxs-lookup"><span data-stu-id="c9c84-620">20</span></span></td>
<td><span data-ttu-id="c9c84-621">(20 ÷ 80) × (5,297.69 + 685.14)</span><span class="sxs-lookup"><span data-stu-id="c9c84-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="c9c84-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c9c84-622">1,495.71</span></span></td>
<td><span data-ttu-id="c9c84-623">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c9c84-624">下表显示当包装服务用作总成本的分配基础时的结果（固定成本和可变成本）。</span><span class="sxs-lookup"><span data-stu-id="c9c84-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-625">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-625">Cost object</span></span></th>
<th><span data-ttu-id="c9c84-626">度量值</span><span class="sxs-lookup"><span data-stu-id="c9c84-626">Magnitude</span></span></th>
<th><span data-ttu-id="c9c84-627">分配系数</span><span class="sxs-lookup"><span data-stu-id="c9c84-627">Allocation factor</span></span></th>
<th><span data-ttu-id="c9c84-628">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-628">Amount</span></span></th>
<th><span data-ttu-id="c9c84-629">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-630">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-630">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-631">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-631">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-632">80</span><span class="sxs-lookup"><span data-stu-id="c9c84-632">80</span></span></td>
<td><span data-ttu-id="c9c84-633">(80 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c9c84-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c9c84-634">241.05</span><span class="sxs-lookup"><span data-stu-id="c9c84-634">241.05</span></span></td>
<td><span data-ttu-id="c9c84-635">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-636">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-636">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-637">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-637">Product 2</span></span></td>
<td><span data-ttu-id="c9c84-638">15</span><span class="sxs-lookup"><span data-stu-id="c9c84-638">15</span></span></td>
<td><span data-ttu-id="c9c84-639">(15 ÷ 95) × (50.00 + 236.25)</span><span class="sxs-lookup"><span data-stu-id="c9c84-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="c9c84-640">45.20</span><span class="sxs-lookup"><span data-stu-id="c9c84-640">45.20</span></span></td>
<td><span data-ttu-id="c9c84-641">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-642">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-642">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-643">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-643">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-644">80</span><span class="sxs-lookup"><span data-stu-id="c9c84-644">80</span></span></td>
<td><span data-ttu-id="c9c84-645">(80 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c9c84-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c9c84-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c9c84-646">2,507.09</span></span></td>
<td><span data-ttu-id="c9c84-647">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-648">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-648">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-649">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-649">Product 2</span></span></td>
<td><span data-ttu-id="c9c84-650">15</span><span class="sxs-lookup"><span data-stu-id="c9c84-650">15</span></span></td>
<td><span data-ttu-id="c9c84-651">(15 ÷ 95) × (2,852.60 + 124.57)</span><span class="sxs-lookup"><span data-stu-id="c9c84-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="c9c84-652">470.08</span><span class="sxs-lookup"><span data-stu-id="c9c84-652">470.08</span></span></td>
<td><span data-ttu-id="c9c84-653">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="c9c84-654">日记帐条目（成本对象余额日记帐条目）</span><span class="sxs-lookup"><span data-stu-id="c9c84-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9c84-655">生产订单日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-655">Journal</span></span></th>
<th><span data-ttu-id="c9c84-656">日记帐类型</span><span class="sxs-lookup"><span data-stu-id="c9c84-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="c9c84-657">会计日历期间</span><span class="sxs-lookup"><span data-stu-id="c9c84-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="c9c84-658">版本</span><span class="sxs-lookup"><span data-stu-id="c9c84-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-659">00004</span><span class="sxs-lookup"><span data-stu-id="c9c84-659">00004</span></span></td>
<td><span data-ttu-id="c9c84-660">成本分配日记帐</span><span class="sxs-lookup"><span data-stu-id="c9c84-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="c9c84-661">会计</span><span class="sxs-lookup"><span data-stu-id="c9c84-661">Fiscal</span></span></td>
<td><span data-ttu-id="c9c84-662">2017</span><span class="sxs-lookup"><span data-stu-id="c9c84-662">2017</span></span></td>
<td><span data-ttu-id="c9c84-663">期间 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-663">Period 1</span></span></td>
<td><span data-ttu-id="c9c84-664">开销计算 / 01-02-2017 11:51:00 PM / 分类帐 /2017 / 期间 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="c9c84-665">日记帐行</span><span class="sxs-lookup"><span data-stu-id="c9c84-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c9c84-666">会计日期</span><span class="sxs-lookup"><span data-stu-id="c9c84-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-667">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-668">成本元素</span><span class="sxs-lookup"><span data-stu-id="c9c84-668">Cost element</span></span></th>
<th><span data-ttu-id="c9c84-669">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-669">Cost behavior</span></span></th>
<th><span data-ttu-id="c9c84-670">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-671">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-672">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-672">CC001</span></span></td>
<td><span data-ttu-id="c9c84-673">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-673">HR</span></span></td>
<td><span data-ttu-id="c9c84-674">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-674">10001</span></span></td>
<td><span data-ttu-id="c9c84-675">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-675">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-676">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-676">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-677">500.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-678">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-679">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-679">CC001</span></span></td>
<td><span data-ttu-id="c9c84-680">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-680">HR</span></span></td>
<td><span data-ttu-id="c9c84-681">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-681">10001</span></span></td>
<td><span data-ttu-id="c9c84-682">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-682">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-683">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-683">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="c9c84-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-685">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-686">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-686">CC002</span></span></td>
<td><span data-ttu-id="c9c84-687">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-687">Finance</span></span></td>
<td><span data-ttu-id="c9c84-688">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-688">10001</span></span></td>
<td><span data-ttu-id="c9c84-689">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-689">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-690">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-690">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-691">675.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-692">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-693">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-693">CC002</span></span></td>
<td><span data-ttu-id="c9c84-694">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-694">Finance</span></span></td>
<td><span data-ttu-id="c9c84-695">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-695">10001</span></span></td>
<td><span data-ttu-id="c9c84-696">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-696">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-697">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-697">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="c9c84-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-699">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-700">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-700">CC003</span></span></td>
<td><span data-ttu-id="c9c84-701">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-701">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-702">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-702">10001</span></span></td>
<td><span data-ttu-id="c9c84-703">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-703">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-704">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-704">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-705">713.75</span><span class="sxs-lookup"><span data-stu-id="c9c84-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-706">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-707">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-707">CC003</span></span></td>
<td><span data-ttu-id="c9c84-708">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-708">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-709">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-709">10001</span></span></td>
<td><span data-ttu-id="c9c84-710">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-710">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-711">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-711">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="c9c84-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-713">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-714">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-714">CC003</span></span></td>
<td><span data-ttu-id="c9c84-715">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-715">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-716">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-716">10001</span></span></td>
<td><span data-ttu-id="c9c84-717">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-717">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-718">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-718">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-719">286.25</span><span class="sxs-lookup"><span data-stu-id="c9c84-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-720">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-721">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-721">CC003</span></span></td>
<td><span data-ttu-id="c9c84-722">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-722">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-723">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-723">10001</span></span></td>
<td><span data-ttu-id="c9c84-724">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-724">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-725">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-725">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="c9c84-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-727">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-728">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-728">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-729">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-729">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-730">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-730">10001</span></span></td>
<td><span data-ttu-id="c9c84-731">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-731">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-732">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-732">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-733">776.36</span><span class="sxs-lookup"><span data-stu-id="c9c84-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-734">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-735">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-735">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-736">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-736">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-737">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-737">10001</span></span></td>
<td><span data-ttu-id="c9c84-738">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-738">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-739">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-739">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c9c84-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-741">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-742">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-742">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-743">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-743">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-744">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-744">10001</span></span></td>
<td><span data-ttu-id="c9c84-745">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-745">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-746">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-746">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-747">223.64</span><span class="sxs-lookup"><span data-stu-id="c9c84-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-748">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="c9c84-749">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-749">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-750">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-750">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-751">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-751">10001</span></span></td>
<td><span data-ttu-id="c9c84-752">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-752">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-753">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-753">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c9c84-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="c9c84-755">成本条目</span><span class="sxs-lookup"><span data-stu-id="c9c84-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="c9c84-756">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="c9c84-757">成本元素</span><span class="sxs-lookup"><span data-stu-id="c9c84-757">Cost element</span></span></th>
<th><span data-ttu-id="c9c84-758">成本行为</span><span class="sxs-lookup"><span data-stu-id="c9c84-758">Cost behavior</span></span></th>
<th><span data-ttu-id="c9c84-759">本币金额</span><span class="sxs-lookup"><span data-stu-id="c9c84-759">Amount</span></span></th>
<th><span data-ttu-id="c9c84-760">会计日期</span><span class="sxs-lookup"><span data-stu-id="c9c84-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c9c84-761">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-761">CC001</span></span></td>
<td><span data-ttu-id="c9c84-762">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-762">HR</span></span></td>
<td><span data-ttu-id="c9c84-763">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-763">10001</span></span></td>
<td><span data-ttu-id="c9c84-764">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-764">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-765">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-765">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-766">-500.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-766">-500.00</span></span></td>
<td><span data-ttu-id="c9c84-767">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-768">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-768">CC002</span></span></td>
<td><span data-ttu-id="c9c84-769">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-769">Finance</span></span></td>
<td><span data-ttu-id="c9c84-770">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-770">10001</span></span></td>
<td><span data-ttu-id="c9c84-771">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-771">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-772">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-772">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-773">175.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-773">175.00</span></span></td>
<td><span data-ttu-id="c9c84-774">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-775">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-775">CC003</span></span></td>
<td><span data-ttu-id="c9c84-776">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-776">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-777">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-777">10001</span></span></td>
<td><span data-ttu-id="c9c84-778">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-778">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-779">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-779">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-780">275.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-780">275.00</span></span></td>
<td><span data-ttu-id="c9c84-781">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-782">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-782">CC004</span></span></td>
<td><span data-ttu-id="c9c84-783">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-783">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-784">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-784">10001</span></span></td>
<td><span data-ttu-id="c9c84-785">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-785">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-786">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-786">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-787">50,00</span><span class="sxs-lookup"><span data-stu-id="c9c84-787">50,00</span></span></td>
<td><span data-ttu-id="c9c84-788">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-789">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-789">CC001</span></span></td>
<td><span data-ttu-id="c9c84-790">HR</span><span class="sxs-lookup"><span data-stu-id="c9c84-790">HR</span></span></td>
<td><span data-ttu-id="c9c84-791">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-791">10001</span></span></td>
<td><span data-ttu-id="c9c84-792">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-792">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-793">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-793">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-794">-1,245.71</span><span class="sxs-lookup"><span data-stu-id="c9c84-794">-1,245.71</span></span></td>
<td><span data-ttu-id="c9c84-795">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-796">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-796">CC002</span></span></td>
<td><span data-ttu-id="c9c84-797">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-797">Finance</span></span></td>
<td><span data-ttu-id="c9c84-798">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-798">10001</span></span></td>
<td><span data-ttu-id="c9c84-799">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-799">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-800">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-800">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-801">436.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-801">436.00</span></span></td>
<td><span data-ttu-id="c9c84-802">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-803">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-803">CC003</span></span></td>
<td><span data-ttu-id="c9c84-804">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-804">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-805">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-805">10001</span></span></td>
<td><span data-ttu-id="c9c84-806">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-806">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-807">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-807">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-808">685.14</span><span class="sxs-lookup"><span data-stu-id="c9c84-808">685.14</span></span></td>
<td><span data-ttu-id="c9c84-809">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-810">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-810">CC004</span></span></td>
<td><span data-ttu-id="c9c84-811">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-811">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-812">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-812">10001</span></span></td>
<td><span data-ttu-id="c9c84-813">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-813">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-814">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-814">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-815">124.57</span><span class="sxs-lookup"><span data-stu-id="c9c84-815">124.57</span></span></td>
<td><span data-ttu-id="c9c84-816">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-817">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-817">CC002</span></span></td>
<td><span data-ttu-id="c9c84-818">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-818">Finance</span></span></td>
<td><span data-ttu-id="c9c84-819">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-819">10001</span></span></td>
<td><span data-ttu-id="c9c84-820">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-820">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-821">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-821">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-822">-675.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-822">-675.00</span></span></td>
<td><span data-ttu-id="c9c84-823">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-824">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-824">CC003</span></span></td>
<td><span data-ttu-id="c9c84-825">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-825">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-826">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-826">10001</span></span></td>
<td><span data-ttu-id="c9c84-827">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-827">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-828">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-828">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-829">438.75</span><span class="sxs-lookup"><span data-stu-id="c9c84-829">438.75</span></span></td>
<td><span data-ttu-id="c9c84-830">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-831">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-831">CC004</span></span></td>
<td><span data-ttu-id="c9c84-832">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-832">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-833">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-833">10001</span></span></td>
<td><span data-ttu-id="c9c84-834">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-834">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-835">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-835">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-836">236.25</span><span class="sxs-lookup"><span data-stu-id="c9c84-836">236.25</span></span></td>
<td><span data-ttu-id="c9c84-837">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-838">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-838">CC002</span></span></td>
<td><span data-ttu-id="c9c84-839">财务</span><span class="sxs-lookup"><span data-stu-id="c9c84-839">Finance</span></span></td>
<td><span data-ttu-id="c9c84-840">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-840">10001</span></span></td>
<td><span data-ttu-id="c9c84-841">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-841">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-842">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-842">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-843">-8,150.29</span><span class="sxs-lookup"><span data-stu-id="c9c84-843">-8,150.29</span></span></td>
<td><span data-ttu-id="c9c84-844">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-845">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-845">CC003</span></span></td>
<td><span data-ttu-id="c9c84-846">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-846">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-847">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-847">10001</span></span></td>
<td><span data-ttu-id="c9c84-848">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-848">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-849">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-849">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="c9c84-850">5,297.69</span></span></td>
<td><span data-ttu-id="c9c84-851">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-852">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-852">CC004</span></span></td>
<td><span data-ttu-id="c9c84-853">包装</span><span class="sxs-lookup"><span data-stu-id="c9c84-853">Packaging</span></span></td>
<td><span data-ttu-id="c9c84-854">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-854">10001</span></span></td>
<td><span data-ttu-id="c9c84-855">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-855">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-856">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-856">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="c9c84-857">2,852.60</span></span></td>
<td><span data-ttu-id="c9c84-858">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-859">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-859">CC003</span></span></td>
<td><span data-ttu-id="c9c84-860">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-860">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-861">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-861">10001</span></span></td>
<td><span data-ttu-id="c9c84-862">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-862">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-863">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-863">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-864">-713.75</span><span class="sxs-lookup"><span data-stu-id="c9c84-864">-713.75</span></span></td>
<td><span data-ttu-id="c9c84-865">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-866">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-866">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-867">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-867">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-868">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-868">10001</span></span></td>
<td><span data-ttu-id="c9c84-869">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-869">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-870">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-870">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-871">535.31</span><span class="sxs-lookup"><span data-stu-id="c9c84-871">535.31</span></span></td>
<td><span data-ttu-id="c9c84-872">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-873">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-873">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-874">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-874">Product 2</span></span></td>
<td><span data-ttu-id="c9c84-875">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-875">10001</span></span></td>
<td><span data-ttu-id="c9c84-876">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-876">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-877">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-877">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-878">178.44</span><span class="sxs-lookup"><span data-stu-id="c9c84-878">178.44</span></span></td>
<td><span data-ttu-id="c9c84-879">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-880">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-880">CC003</span></span></td>
<td><span data-ttu-id="c9c84-881">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-881">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-882">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-882">10001</span></span></td>
<td><span data-ttu-id="c9c84-883">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-883">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-884">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-884">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-885">-5,982.83</span><span class="sxs-lookup"><span data-stu-id="c9c84-885">-5,982.83</span></span></td>
<td><span data-ttu-id="c9c84-886">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-887">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-887">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-888">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-888">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-889">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-889">10001</span></span></td>
<td><span data-ttu-id="c9c84-890">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-890">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-891">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-891">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="c9c84-892">4,487.12</span></span></td>
<td><span data-ttu-id="c9c84-893">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-894">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-894">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-895">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-895">Product 2</span></span></td>
<td><span data-ttu-id="c9c84-896">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-896">10001</span></span></td>
<td><span data-ttu-id="c9c84-897">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-897">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-898">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-898">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="c9c84-899">1,495.71</span></span></td>
<td><span data-ttu-id="c9c84-900">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-901">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-901">CC003</span></span></td>
<td><span data-ttu-id="c9c84-902">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-902">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-903">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-903">10001</span></span></td>
<td><span data-ttu-id="c9c84-904">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-904">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-905">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-905">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-906">-286.25</span><span class="sxs-lookup"><span data-stu-id="c9c84-906">-286.25</span></span></td>
<td><span data-ttu-id="c9c84-907">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-908">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-908">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-909">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-909">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-910">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-910">10001</span></span></td>
<td><span data-ttu-id="c9c84-911">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-911">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-912">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-912">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-913">241.05</span><span class="sxs-lookup"><span data-stu-id="c9c84-913">241.05</span></span></td>
<td><span data-ttu-id="c9c84-914">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-915">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-915">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-916">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-916">Product 2</span></span></td>
<td><span data-ttu-id="c9c84-917">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-917">10001</span></span></td>
<td><span data-ttu-id="c9c84-918">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-918">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-919">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-919">Fixed cost</span></span></td>
<td><span data-ttu-id="c9c84-920">45.20</span><span class="sxs-lookup"><span data-stu-id="c9c84-920">45.20</span></span></td>
<td><span data-ttu-id="c9c84-921">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-922">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-922">CC003</span></span></td>
<td><span data-ttu-id="c9c84-923">程序集</span><span class="sxs-lookup"><span data-stu-id="c9c84-923">Assembly</span></span></td>
<td><span data-ttu-id="c9c84-924">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-924">10001</span></span></td>
<td><span data-ttu-id="c9c84-925">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-925">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-926">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-926">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-927">-2,977.17</span><span class="sxs-lookup"><span data-stu-id="c9c84-927">-2,977.17</span></span></td>
<td><span data-ttu-id="c9c84-928">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-929">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-929">Prod 1</span></span></td>
<td><span data-ttu-id="c9c84-930">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-930">Product 1</span></span></td>
<td><span data-ttu-id="c9c84-931">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-931">10001</span></span></td>
<td><span data-ttu-id="c9c84-932">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-932">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-933">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-933">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="c9c84-934">2,507.09</span></span></td>
<td><span data-ttu-id="c9c84-935">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="c9c84-936">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-936">Prod 2</span></span></td>
<td><span data-ttu-id="c9c84-937">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-937">Product 2</span></span></td>
<td><span data-ttu-id="c9c84-938">10001</span><span class="sxs-lookup"><span data-stu-id="c9c84-938">10001</span></span></td>
<td><span data-ttu-id="c9c84-939">电</span><span class="sxs-lookup"><span data-stu-id="c9c84-939">Electricity</span></span></td>
<td><span data-ttu-id="c9c84-940">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-940">Variable cost</span></span></td>
<td><span data-ttu-id="c9c84-941">470.08</span><span class="sxs-lookup"><span data-stu-id="c9c84-941">470.08</span></span></td>
<td><span data-ttu-id="c9c84-942">2017 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="c9c84-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="c9c84-943">结论</span><span class="sxs-lookup"><span data-stu-id="c9c84-943">Conclusion</span></span>
<span data-ttu-id="c9c84-944">在财务会计中，10,000.00 电成本过帐到虚拟成本中心 ID。</span><span class="sxs-lookup"><span data-stu-id="c9c84-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="c9c84-945">因此，成本会计员将了解必须分摊此成本。</span><span class="sxs-lookup"><span data-stu-id="c9c84-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="c9c84-946">在成本核算中，跨组织单位和级别的成本流，基于所应用的政策和规则。</span><span class="sxs-lookup"><span data-stu-id="c9c84-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="c9c84-947">每项成本已与为成本分摊提供最佳评估的分配基础关联。</span><span class="sxs-lookup"><span data-stu-id="c9c84-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="c9c84-948">成本元素</span><span class="sxs-lookup"><span data-stu-id="c9c84-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="c9c84-949">成本对象</span><span class="sxs-lookup"><span data-stu-id="c9c84-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="c9c84-950">合计</span><span class="sxs-lookup"><span data-stu-id="c9c84-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="c9c84-951">CC099</span><span class="sxs-lookup"><span data-stu-id="c9c84-951">CC099</span></span></th>
<th><span data-ttu-id="c9c84-952">CC001</span><span class="sxs-lookup"><span data-stu-id="c9c84-952">CC001</span></span></th>
<th><span data-ttu-id="c9c84-953">CC002</span><span class="sxs-lookup"><span data-stu-id="c9c84-953">CC002</span></span></th>
<th><span data-ttu-id="c9c84-954">CC003</span><span class="sxs-lookup"><span data-stu-id="c9c84-954">CC003</span></span></th>
<th><span data-ttu-id="c9c84-955">CC004</span><span class="sxs-lookup"><span data-stu-id="c9c84-955">CC004</span></span></th>
<th><span data-ttu-id="c9c84-956">项目 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-956">Proj 1</span></span></th>
<th><span data-ttu-id="c9c84-957">项目 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-957">Proj 2</span></span></th>
<th><span data-ttu-id="c9c84-958">产品 1</span><span class="sxs-lookup"><span data-stu-id="c9c84-958">Prod 1</span></span></th>
<th><span data-ttu-id="c9c84-959">产品 2</span><span class="sxs-lookup"><span data-stu-id="c9c84-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="c9c84-960">10001 电</span><span class="sxs-lookup"><span data-stu-id="c9c84-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="c9c84-970">未分类</span><span class="sxs-lookup"><span data-stu-id="c9c84-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-971">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="c9c84-972">固定成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-973">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-974">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-975">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-976">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-977">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-978">776.36</span><span class="sxs-lookup"><span data-stu-id="c9c84-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-979">223.64</span><span class="sxs-lookup"><span data-stu-id="c9c84-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="c9c84-981">可变成本</span><span class="sxs-lookup"><span data-stu-id="c9c84-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-982">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-983">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-984">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-985">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-986">0.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-987">30.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-988">10.00</span><span class="sxs-lookup"><span data-stu-id="c9c84-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="c9c84-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="c9c84-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="c9c84-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="c9c84-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c9c84-992">此主题显示主要成本元素“10001 电”如何流过成本对象。</span><span class="sxs-lookup"><span data-stu-id="c9c84-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="c9c84-993">因此，此间接成本分摊到组织的最低级别。</span><span class="sxs-lookup"><span data-stu-id="c9c84-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="c9c84-994">换言之，最低级别的成本对象承担成本。</span><span class="sxs-lookup"><span data-stu-id="c9c84-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="c9c84-995">如果您需要成本对象之间的可视成本流，可以使用成本累积政策规则实现成本流可视化。</span><span class="sxs-lookup"><span data-stu-id="c9c84-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="c9c84-996">有关详细信息，请参阅[成本累积](cost-rollup.md)。</span><span class="sxs-lookup"><span data-stu-id="c9c84-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



