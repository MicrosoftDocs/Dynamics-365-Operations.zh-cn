---
title: 库龄报表示例和逻辑
description: 本主题提供了一些示例来展示如何解释库龄报表的结果。
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484522"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="a0755-103">库龄报表示例和逻辑</span><span class="sxs-lookup"><span data-stu-id="a0755-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0755-104">本主题提供了一些示例来展示如何解释**库龄**报表的结果。</span><span class="sxs-lookup"><span data-stu-id="a0755-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="a0755-105">此报表将所选物料或物料组的现有数量和现有库存量值分类为几个期间段。</span><span class="sxs-lookup"><span data-stu-id="a0755-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="a0755-106">本主题还展示了报表的内部逻辑。</span><span class="sxs-lookup"><span data-stu-id="a0755-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="a0755-107">本主题中的示例展示了标准**库龄**报表中呈现的结果。</span><span class="sxs-lookup"><span data-stu-id="a0755-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="a0755-108">但是，通常，建议您使用此报表的[库龄报表存储](inventory-aging-report-storage.md)版本，尤其是当您有许多必须处理的物料和仓库时。</span><span class="sxs-lookup"><span data-stu-id="a0755-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="a0755-109">库龄报表存储保存您生成的每个报表，将结果显示为交互式页面和图表，并允许您导出任何已保存的报表。</span><span class="sxs-lookup"><span data-stu-id="a0755-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="a0755-110">这些示例中使用的示例数据</span><span class="sxs-lookup"><span data-stu-id="a0755-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="a0755-111">本主题中的示例基于本节中介绍的示例库存交易数据。</span><span class="sxs-lookup"><span data-stu-id="a0755-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="a0755-112">存储维度设置</span><span class="sxs-lookup"><span data-stu-id="a0755-112">Storage dimension setup</span></span>

<span data-ttu-id="a0755-113">示例系统包含以下存储维度设置。</span><span class="sxs-lookup"><span data-stu-id="a0755-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="a0755-114">姓名</span><span class="sxs-lookup"><span data-stu-id="a0755-114">Name</span></span>      | <span data-ttu-id="a0755-115">活动</span><span class="sxs-lookup"><span data-stu-id="a0755-115">Active</span></span> | <span data-ttu-id="a0755-116">实际库存</span><span class="sxs-lookup"><span data-stu-id="a0755-116">Physical inventory</span></span> | <span data-ttu-id="a0755-117">财务库存</span><span class="sxs-lookup"><span data-stu-id="a0755-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="a0755-118">站点</span><span class="sxs-lookup"><span data-stu-id="a0755-118">Site</span></span>      | <span data-ttu-id="a0755-119">是</span><span class="sxs-lookup"><span data-stu-id="a0755-119">Yes</span></span>    | <span data-ttu-id="a0755-120">是</span><span class="sxs-lookup"><span data-stu-id="a0755-120">Yes</span></span>                | <span data-ttu-id="a0755-121">是</span><span class="sxs-lookup"><span data-stu-id="a0755-121">Yes</span></span>                 |
| <span data-ttu-id="a0755-122">存放地点</span><span class="sxs-lookup"><span data-stu-id="a0755-122">Warehouse</span></span> | <span data-ttu-id="a0755-123">是</span><span class="sxs-lookup"><span data-stu-id="a0755-123">Yes</span></span>    | <span data-ttu-id="a0755-124">是</span><span class="sxs-lookup"><span data-stu-id="a0755-124">Yes</span></span>                | <span data-ttu-id="a0755-125">无</span><span class="sxs-lookup"><span data-stu-id="a0755-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="a0755-126">库存模型</span><span class="sxs-lookup"><span data-stu-id="a0755-126">Inventory model</span></span>

<span data-ttu-id="a0755-127">对于示例系统，已发布产品的库存模型为*先进先出*，此库存模型的**成本价**设置为*包括实际成本*。</span><span class="sxs-lookup"><span data-stu-id="a0755-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="a0755-128">库存交易记录</span><span class="sxs-lookup"><span data-stu-id="a0755-128">Inventory transactions</span></span>

<span data-ttu-id="a0755-129">示例系统包含具有物料编号 *1000* 的已发布产品的以下库存交易记录。</span><span class="sxs-lookup"><span data-stu-id="a0755-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="a0755-130">参考</span><span class="sxs-lookup"><span data-stu-id="a0755-130">Reference</span></span>      | <span data-ttu-id="a0755-131">站点</span><span class="sxs-lookup"><span data-stu-id="a0755-131">Site</span></span> | <span data-ttu-id="a0755-132">存放地点</span><span class="sxs-lookup"><span data-stu-id="a0755-132">Warehouse</span></span> | <span data-ttu-id="a0755-133">收货</span><span class="sxs-lookup"><span data-stu-id="a0755-133">Receipt</span></span>   | <span data-ttu-id="a0755-134">发货</span><span class="sxs-lookup"><span data-stu-id="a0755-134">Issue</span></span> | <span data-ttu-id="a0755-135">实际日期</span><span class="sxs-lookup"><span data-stu-id="a0755-135">Physical date</span></span> | <span data-ttu-id="a0755-136">财务日期</span><span class="sxs-lookup"><span data-stu-id="a0755-136">Financial date</span></span> | <span data-ttu-id="a0755-137">数量</span><span class="sxs-lookup"><span data-stu-id="a0755-137">Quantity</span></span> | <span data-ttu-id="a0755-138">成本金额</span><span class="sxs-lookup"><span data-stu-id="a0755-138">Cost amount</span></span> | <span data-ttu-id="a0755-139">实际成本额</span><span class="sxs-lookup"><span data-stu-id="a0755-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="a0755-140">采购订单</span><span class="sxs-lookup"><span data-stu-id="a0755-140">Purchase order</span></span> | <span data-ttu-id="a0755-141">1</span><span class="sxs-lookup"><span data-stu-id="a0755-141">1</span></span>    | <span data-ttu-id="a0755-142">11</span><span class="sxs-lookup"><span data-stu-id="a0755-142">11</span></span>        | <span data-ttu-id="a0755-143">已采购</span><span class="sxs-lookup"><span data-stu-id="a0755-143">Purchased</span></span> |       | <span data-ttu-id="a0755-144">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a0755-144">March 15</span></span>      | <span data-ttu-id="a0755-145">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a0755-145">March 15</span></span>       | <span data-ttu-id="a0755-146">10</span><span class="sxs-lookup"><span data-stu-id="a0755-146">10</span></span>       | <span data-ttu-id="a0755-147">1,000</span><span class="sxs-lookup"><span data-stu-id="a0755-147">1,000</span></span>       | <span data-ttu-id="a0755-148">1,000</span><span class="sxs-lookup"><span data-stu-id="a0755-148">1,000</span></span>                |
| <span data-ttu-id="a0755-149">采购订单</span><span class="sxs-lookup"><span data-stu-id="a0755-149">Purchase order</span></span> | <span data-ttu-id="a0755-150">2</span><span class="sxs-lookup"><span data-stu-id="a0755-150">2</span></span>    | <span data-ttu-id="a0755-151">21</span><span class="sxs-lookup"><span data-stu-id="a0755-151">21</span></span>        | <span data-ttu-id="a0755-152">已采购</span><span class="sxs-lookup"><span data-stu-id="a0755-152">Purchased</span></span> |       | <span data-ttu-id="a0755-153">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a0755-153">March 15</span></span>      | <span data-ttu-id="a0755-154">3 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a0755-154">March 15</span></span>       | <span data-ttu-id="a0755-155">10</span><span class="sxs-lookup"><span data-stu-id="a0755-155">10</span></span>       | <span data-ttu-id="a0755-156">2,000</span><span class="sxs-lookup"><span data-stu-id="a0755-156">2,000</span></span>       | <span data-ttu-id="a0755-157">2,000</span><span class="sxs-lookup"><span data-stu-id="a0755-157">2,000</span></span>                |
| <span data-ttu-id="a0755-158">采购订单</span><span class="sxs-lookup"><span data-stu-id="a0755-158">Purchase order</span></span> | <span data-ttu-id="a0755-159">1</span><span class="sxs-lookup"><span data-stu-id="a0755-159">1</span></span>    | <span data-ttu-id="a0755-160">11</span><span class="sxs-lookup"><span data-stu-id="a0755-160">11</span></span>        | <span data-ttu-id="a0755-161">已收到</span><span class="sxs-lookup"><span data-stu-id="a0755-161">Received</span></span>  |       | <span data-ttu-id="a0755-162">4 月 15 日</span><span class="sxs-lookup"><span data-stu-id="a0755-162">April 15</span></span>      |                | <span data-ttu-id="a0755-163">5</span><span class="sxs-lookup"><span data-stu-id="a0755-163">5</span></span>        |             | <span data-ttu-id="a0755-164">375</span><span class="sxs-lookup"><span data-stu-id="a0755-164">375</span></span>                  |
| <span data-ttu-id="a0755-165">转移单</span><span class="sxs-lookup"><span data-stu-id="a0755-165">Transfer order</span></span> | <span data-ttu-id="a0755-166">1</span><span class="sxs-lookup"><span data-stu-id="a0755-166">1</span></span>    | <span data-ttu-id="a0755-167">11</span><span class="sxs-lookup"><span data-stu-id="a0755-167">11</span></span>        |           | <span data-ttu-id="a0755-168">已售出</span><span class="sxs-lookup"><span data-stu-id="a0755-168">Sold</span></span>  | <span data-ttu-id="a0755-169">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="a0755-169">May 2</span></span>         | <span data-ttu-id="a0755-170">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="a0755-170">May 2</span></span>          | <span data-ttu-id="a0755-171">-5</span><span class="sxs-lookup"><span data-stu-id="a0755-171">-5</span></span>       | <span data-ttu-id="a0755-172">-458.33</span><span class="sxs-lookup"><span data-stu-id="a0755-172">-458.33</span></span>     | <span data-ttu-id="a0755-173">-458.33</span><span class="sxs-lookup"><span data-stu-id="a0755-173">-458.33</span></span>              |
| <span data-ttu-id="a0755-174">转移单</span><span class="sxs-lookup"><span data-stu-id="a0755-174">Transfer order</span></span> | <span data-ttu-id="a0755-175">1</span><span class="sxs-lookup"><span data-stu-id="a0755-175">1</span></span>    | <span data-ttu-id="a0755-176">12</span><span class="sxs-lookup"><span data-stu-id="a0755-176">12</span></span>        | <span data-ttu-id="a0755-177">已采购</span><span class="sxs-lookup"><span data-stu-id="a0755-177">Purchased</span></span> |       | <span data-ttu-id="a0755-178">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="a0755-178">May 2</span></span>         | <span data-ttu-id="a0755-179">5 月 2 日</span><span class="sxs-lookup"><span data-stu-id="a0755-179">May 2</span></span>          | <span data-ttu-id="a0755-180">5</span><span class="sxs-lookup"><span data-stu-id="a0755-180">5</span></span>        | <span data-ttu-id="a0755-181">458.33</span><span class="sxs-lookup"><span data-stu-id="a0755-181">458.33</span></span>      | <span data-ttu-id="a0755-182">458.33</span><span class="sxs-lookup"><span data-stu-id="a0755-182">458.33</span></span>               |
| <span data-ttu-id="a0755-183">销售订单</span><span class="sxs-lookup"><span data-stu-id="a0755-183">Sales order</span></span>    | <span data-ttu-id="a0755-184">1</span><span class="sxs-lookup"><span data-stu-id="a0755-184">1</span></span>    | <span data-ttu-id="a0755-185">12</span><span class="sxs-lookup"><span data-stu-id="a0755-185">12</span></span>        |           | <span data-ttu-id="a0755-186">已售出</span><span class="sxs-lookup"><span data-stu-id="a0755-186">Sold</span></span>  | <span data-ttu-id="a0755-187">5 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a0755-187">May 3</span></span>         | <span data-ttu-id="a0755-188">5 月 3 日</span><span class="sxs-lookup"><span data-stu-id="a0755-188">May 3</span></span>          | <span data-ttu-id="a0755-189">-1</span><span class="sxs-lookup"><span data-stu-id="a0755-189">-1</span></span>       | <span data-ttu-id="a0755-190">-91.67</span><span class="sxs-lookup"><span data-stu-id="a0755-190">-91.67</span></span>      | <span data-ttu-id="a0755-191">-91.67</span><span class="sxs-lookup"><span data-stu-id="a0755-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="a0755-192">如何计算每个期间段内的数量和金额</span><span class="sxs-lookup"><span data-stu-id="a0755-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="a0755-193">通过使用前面几节中介绍的示例数据，您可以运行具有以下设置的**库龄**报表：</span><span class="sxs-lookup"><span data-stu-id="a0755-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="a0755-194">**截止日期**：*2020 年 5 月 9 日*</span><span class="sxs-lookup"><span data-stu-id="a0755-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="a0755-195">**站点**：*视图*</span><span class="sxs-lookup"><span data-stu-id="a0755-195">**Site:** *View*</span></span>
- <span data-ttu-id="a0755-196">**仓库**：*否*</span><span class="sxs-lookup"><span data-stu-id="a0755-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="a0755-197">**物料编号**：*总计*</span><span class="sxs-lookup"><span data-stu-id="a0755-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="a0755-198">**帐龄期间：** 将此字段设置为生成每月时段。</span><span class="sxs-lookup"><span data-stu-id="a0755-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="a0755-199">在此例中，生成的报表的内容类似于以下示例。</span><span class="sxs-lookup"><span data-stu-id="a0755-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="a0755-200">物料编号</span><span class="sxs-lookup"><span data-stu-id="a0755-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-201">站点</span><span class="sxs-lookup"><span data-stu-id="a0755-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-202">现有数量</span><span class="sxs-lookup"><span data-stu-id="a0755-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-203">现有量值</span><span class="sxs-lookup"><span data-stu-id="a0755-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-204">库存成本数量</span><span class="sxs-lookup"><span data-stu-id="a0755-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-205">库存成本</span><span class="sxs-lookup"><span data-stu-id="a0755-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-206">平均单位成本</span><span class="sxs-lookup"><span data-stu-id="a0755-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="a0755-207">2020 年 5 月 8 日 - 2020 年 5 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a0755-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a0755-208">2020 年 4 月 30 日 - 2020 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a0755-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a0755-209">2020 年 3 月 31 日 - 2020 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a0755-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="a0755-210">P1：数量</span><span class="sxs-lookup"><span data-stu-id="a0755-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="a0755-211">P1：金额</span><span class="sxs-lookup"><span data-stu-id="a0755-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="a0755-212">P2：数量</span><span class="sxs-lookup"><span data-stu-id="a0755-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="a0755-213">P2：金额</span><span class="sxs-lookup"><span data-stu-id="a0755-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="a0755-214">P3：数量</span><span class="sxs-lookup"><span data-stu-id="a0755-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="a0755-215">P3：金额</span><span class="sxs-lookup"><span data-stu-id="a0755-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="a0755-216">1000</span><span class="sxs-lookup"><span data-stu-id="a0755-216">1000</span></span></td>
    <td><span data-ttu-id="a0755-217">1</span><span class="sxs-lookup"><span data-stu-id="a0755-217">1</span></span></td>
    <td><span data-ttu-id="a0755-218">14</span><span class="sxs-lookup"><span data-stu-id="a0755-218">14</span></span></td>
    <td><span data-ttu-id="a0755-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="a0755-219">1,283.33</span></span></td>
    <td><span data-ttu-id="a0755-220">14</span><span class="sxs-lookup"><span data-stu-id="a0755-220">14</span></span></td>
    <td><span data-ttu-id="a0755-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="a0755-221">1,283.33</span></span></td>
    <td><span data-ttu-id="a0755-222">91.67</span><span class="sxs-lookup"><span data-stu-id="a0755-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a0755-223">5.00</span><span class="sxs-lookup"><span data-stu-id="a0755-223">5.00</span></span></td>
    <td><span data-ttu-id="a0755-224">458.33</span><span class="sxs-lookup"><span data-stu-id="a0755-224">458.33</span></span></td>
    <td><span data-ttu-id="a0755-225">9.00</span><span class="sxs-lookup"><span data-stu-id="a0755-225">9.00</span></span></td>
    <td><span data-ttu-id="a0755-226">825.00</span><span class="sxs-lookup"><span data-stu-id="a0755-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="a0755-227">1000</span><span class="sxs-lookup"><span data-stu-id="a0755-227">1000</span></span></td>
    <td><span data-ttu-id="a0755-228">2</span><span class="sxs-lookup"><span data-stu-id="a0755-228">2</span></span></td>
    <td><span data-ttu-id="a0755-229">10</span><span class="sxs-lookup"><span data-stu-id="a0755-229">10</span></span></td>
    <td><span data-ttu-id="a0755-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a0755-230">2,000.00</span></span></td>
    <td><span data-ttu-id="a0755-231">10</span><span class="sxs-lookup"><span data-stu-id="a0755-231">10</span></span></td>
    <td><span data-ttu-id="a0755-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a0755-232">2,000.00</span></span></td>
    <td><span data-ttu-id="a0755-233">200.00</span><span class="sxs-lookup"><span data-stu-id="a0755-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a0755-234">10.00</span><span class="sxs-lookup"><span data-stu-id="a0755-234">10.00</span></span></td>
    <td><span data-ttu-id="a0755-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a0755-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="a0755-236"><strong>总计 1000</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="a0755-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="a0755-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a0755-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="a0755-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="a0755-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="a0755-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="a0755-243">请注意此示例报表中的以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="a0755-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="a0755-244">报表中显示的**库存值数量**、**库存值**和**平均单位成本**值是财务库存维度的值（在此例中为**站点**）。</span><span class="sxs-lookup"><span data-stu-id="a0755-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="a0755-245">例如，对于站点 1，报表显示以下信息：</span><span class="sxs-lookup"><span data-stu-id="a0755-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="a0755-246">**库存值数量**值是 *14* (= 10 + 5 – 5 + 5 – 1)。</span><span class="sxs-lookup"><span data-stu-id="a0755-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="a0755-247">**库存值**值是 *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67)。</span><span class="sxs-lookup"><span data-stu-id="a0755-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="a0755-248">**平均单位成本**值是 *91.67*。</span><span class="sxs-lookup"><span data-stu-id="a0755-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="a0755-249">每个期间段中的**现有量值**值和**金额**值使用**平均单位成本**值计算得出。</span><span class="sxs-lookup"><span data-stu-id="a0755-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="a0755-250">此报表通过对每个期间段的总接收库存数量求和来确定每个期间段的现有数量。</span><span class="sxs-lookup"><span data-stu-id="a0755-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="a0755-251">然后，采用先进先出 (FIFO) 原则扣除总发货数量，不管物料使用的库存模型如何。</span><span class="sxs-lookup"><span data-stu-id="a0755-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="a0755-252">如果再次运行相同的报表，但是这次您将**站点**和**仓库**字段都设置为*视图*，新报表将类似于以下示例。</span><span class="sxs-lookup"><span data-stu-id="a0755-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="a0755-253">物料编号</span><span class="sxs-lookup"><span data-stu-id="a0755-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-254">站点</span><span class="sxs-lookup"><span data-stu-id="a0755-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-255">存放地点</span><span class="sxs-lookup"><span data-stu-id="a0755-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-256">现有数量</span><span class="sxs-lookup"><span data-stu-id="a0755-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-257">现有量值</span><span class="sxs-lookup"><span data-stu-id="a0755-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-258">库存成本数量</span><span class="sxs-lookup"><span data-stu-id="a0755-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-259">库存成本</span><span class="sxs-lookup"><span data-stu-id="a0755-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-260">平均单位成本</span><span class="sxs-lookup"><span data-stu-id="a0755-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="a0755-261">2020 年 5 月 8 日 - 2020 年 5 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a0755-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a0755-262">2020 年 4 月 30 日 - 2020 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a0755-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a0755-263">2020 年 3 月 31 日 - 2020 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a0755-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="a0755-264">P1：数量</span><span class="sxs-lookup"><span data-stu-id="a0755-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="a0755-265">P1：金额</span><span class="sxs-lookup"><span data-stu-id="a0755-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="a0755-266">P2：数量</span><span class="sxs-lookup"><span data-stu-id="a0755-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="a0755-267">P2：金额</span><span class="sxs-lookup"><span data-stu-id="a0755-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="a0755-268">P3：数量</span><span class="sxs-lookup"><span data-stu-id="a0755-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="a0755-269">P3：金额</span><span class="sxs-lookup"><span data-stu-id="a0755-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="a0755-270">1000</span><span class="sxs-lookup"><span data-stu-id="a0755-270">1000</span></span></td>
    <td><span data-ttu-id="a0755-271">1</span><span class="sxs-lookup"><span data-stu-id="a0755-271">1</span></span></td>
    <td><span data-ttu-id="a0755-272">11</span><span class="sxs-lookup"><span data-stu-id="a0755-272">11</span></span></td>
    <td><span data-ttu-id="a0755-273">10</span><span class="sxs-lookup"><span data-stu-id="a0755-273">10</span></span></td>
    <td><span data-ttu-id="a0755-274">916.67</span><span class="sxs-lookup"><span data-stu-id="a0755-274">916.67</span></span></td>
    <td><span data-ttu-id="a0755-275">14</span><span class="sxs-lookup"><span data-stu-id="a0755-275">14</span></span></td>
    <td><span data-ttu-id="a0755-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="a0755-276">1,283.33</span></span></td>
    <td><span data-ttu-id="a0755-277">91.67</span><span class="sxs-lookup"><span data-stu-id="a0755-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a0755-278">5.00</span><span class="sxs-lookup"><span data-stu-id="a0755-278">5.00</span></span></td>
    <td><span data-ttu-id="a0755-279">458.33</span><span class="sxs-lookup"><span data-stu-id="a0755-279">458.33</span></span></td>
    <td><span data-ttu-id="a0755-280">5.00</span><span class="sxs-lookup"><span data-stu-id="a0755-280">5.00</span></span></td>
    <td><span data-ttu-id="a0755-281">458.33</span><span class="sxs-lookup"><span data-stu-id="a0755-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="a0755-282">1000</span><span class="sxs-lookup"><span data-stu-id="a0755-282">1000</span></span></td>
    <td><span data-ttu-id="a0755-283">1</span><span class="sxs-lookup"><span data-stu-id="a0755-283">1</span></span></td>
    <td><span data-ttu-id="a0755-284">12</span><span class="sxs-lookup"><span data-stu-id="a0755-284">12</span></span></td>
    <td><span data-ttu-id="a0755-285">4</span><span class="sxs-lookup"><span data-stu-id="a0755-285">4</span></span></td>
    <td><span data-ttu-id="a0755-286">366.67</span><span class="sxs-lookup"><span data-stu-id="a0755-286">366.67</span></span></td>
    <td><span data-ttu-id="a0755-287">14</span><span class="sxs-lookup"><span data-stu-id="a0755-287">14</span></span></td>
    <td><span data-ttu-id="a0755-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="a0755-288">1,283.33</span></span></td>
    <td><span data-ttu-id="a0755-289">91.67</span><span class="sxs-lookup"><span data-stu-id="a0755-289">91.67</span></span></td>
    <td><span data-ttu-id="a0755-290">4.00</span><span class="sxs-lookup"><span data-stu-id="a0755-290">4.00</span></span></td>
    <td><span data-ttu-id="a0755-291">366.67</span><span class="sxs-lookup"><span data-stu-id="a0755-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="a0755-292">1000</span><span class="sxs-lookup"><span data-stu-id="a0755-292">1000</span></span></td>
    <td><span data-ttu-id="a0755-293">2</span><span class="sxs-lookup"><span data-stu-id="a0755-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="a0755-294">10</span><span class="sxs-lookup"><span data-stu-id="a0755-294">10</span></span></td>
    <td><span data-ttu-id="a0755-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a0755-295">2,000.00</span></span></td>
    <td><span data-ttu-id="a0755-296">10</span><span class="sxs-lookup"><span data-stu-id="a0755-296">10</span></span></td>
    <td><span data-ttu-id="a0755-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a0755-297">2,000.00</span></span></td>
    <td><span data-ttu-id="a0755-298">200.00</span><span class="sxs-lookup"><span data-stu-id="a0755-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a0755-299">10.00</span><span class="sxs-lookup"><span data-stu-id="a0755-299">10.00</span></span></td>
    <td><span data-ttu-id="a0755-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a0755-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="a0755-301"><strong>总计 1000</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a0755-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="a0755-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a0755-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="a0755-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="a0755-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="a0755-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="a0755-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="a0755-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="a0755-310">这次，站点 1 分为两行，一行就仓库 11，另一行是仓库 12。</span><span class="sxs-lookup"><span data-stu-id="a0755-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="a0755-311">但是，**库存值数量**、**库存值**和**平均单位成本**值相同，因为**仓库**不是财务库存维度。</span><span class="sxs-lookup"><span data-stu-id="a0755-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="a0755-312">此外，请注意，站点 1 的数量分配不同。</span><span class="sxs-lookup"><span data-stu-id="a0755-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="a0755-313">在您运行的第一份报表中，系统忽略了同一站点中发生的转移单，从站点 1 的 **2020 年 3 月 31 日 - 2020 年 3 月 1 日**期间段中扣除了销售发票的数量。</span><span class="sxs-lookup"><span data-stu-id="a0755-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="a0755-314">但是，在新报表中，系统从仓库 12 的 **2020 年 5 月 8 日 - 2020 年 5 月 1 日**期间段中扣除了销售发票的数量。</span><span class="sxs-lookup"><span data-stu-id="a0755-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="a0755-315">库存结转的影响</span><span class="sxs-lookup"><span data-stu-id="a0755-315">Effects of inventory closing</span></span>

<span data-ttu-id="a0755-316">如果您运行 5 月的库存结转，然后再次运行上一个报表，但是将**截止日期**字段设置为 *2020 年 5 月 31 日*，您将注意到以下结果：</span><span class="sxs-lookup"><span data-stu-id="a0755-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="a0755-317">**库存值**和**平均单位成本**值已更新。</span><span class="sxs-lookup"><span data-stu-id="a0755-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="a0755-318">每个期间段的**现有量值**值和所有**金额**值已相应更新。</span><span class="sxs-lookup"><span data-stu-id="a0755-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="a0755-319">新报表将类似于以下示例。</span><span class="sxs-lookup"><span data-stu-id="a0755-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="a0755-320">物料编号</span><span class="sxs-lookup"><span data-stu-id="a0755-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-321">站点</span><span class="sxs-lookup"><span data-stu-id="a0755-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-322">存放地点</span><span class="sxs-lookup"><span data-stu-id="a0755-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-323">现有数量</span><span class="sxs-lookup"><span data-stu-id="a0755-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-324">现有量值</span><span class="sxs-lookup"><span data-stu-id="a0755-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-325">库存成本数量</span><span class="sxs-lookup"><span data-stu-id="a0755-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-326">库存成本</span><span class="sxs-lookup"><span data-stu-id="a0755-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="a0755-327">平均单位成本</span><span class="sxs-lookup"><span data-stu-id="a0755-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="a0755-328">2020 年 5 月 31 日 - 2020 年 5 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a0755-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a0755-329">2020 年 4 月 30 日 - 2020 年 4 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a0755-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="a0755-330">2020 年 3 月 31 日 - 2020 年 3 月 1 日</span><span class="sxs-lookup"><span data-stu-id="a0755-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="a0755-331">P1：数量</span><span class="sxs-lookup"><span data-stu-id="a0755-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="a0755-332">P1：金额</span><span class="sxs-lookup"><span data-stu-id="a0755-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="a0755-333">P2：数量</span><span class="sxs-lookup"><span data-stu-id="a0755-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="a0755-334">P2：金额</span><span class="sxs-lookup"><span data-stu-id="a0755-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="a0755-335">P3：数量</span><span class="sxs-lookup"><span data-stu-id="a0755-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="a0755-336">P3：金额</span><span class="sxs-lookup"><span data-stu-id="a0755-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="a0755-337">1000</span><span class="sxs-lookup"><span data-stu-id="a0755-337">1000</span></span></td>
    <td><span data-ttu-id="a0755-338">1</span><span class="sxs-lookup"><span data-stu-id="a0755-338">1</span></span></td>
    <td><span data-ttu-id="a0755-339">11</span><span class="sxs-lookup"><span data-stu-id="a0755-339">11</span></span></td>
    <td><span data-ttu-id="a0755-340">10</span><span class="sxs-lookup"><span data-stu-id="a0755-340">10</span></span></td>
    <td><span data-ttu-id="a0755-341">910.70</span><span class="sxs-lookup"><span data-stu-id="a0755-341">910.70</span></span></td>
    <td><span data-ttu-id="a0755-342">14</span><span class="sxs-lookup"><span data-stu-id="a0755-342">14</span></span></td>
    <td><span data-ttu-id="a0755-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="a0755-343">1,275.00</span></span></td>
    <td><span data-ttu-id="a0755-344">91.07</span><span class="sxs-lookup"><span data-stu-id="a0755-344">91.07</span></span></td>
    <td><span data-ttu-id="a0755-345">0.00</span><span class="sxs-lookup"><span data-stu-id="a0755-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="a0755-346">5.00</span><span class="sxs-lookup"><span data-stu-id="a0755-346">5.00</span></span></td>
    <td><span data-ttu-id="a0755-347">455.36</span><span class="sxs-lookup"><span data-stu-id="a0755-347">455.36</span></span></td>
    <td><span data-ttu-id="a0755-348">5.00</span><span class="sxs-lookup"><span data-stu-id="a0755-348">5.00</span></span></td>
    <td><span data-ttu-id="a0755-349">455.36</span><span class="sxs-lookup"><span data-stu-id="a0755-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="a0755-350">1000</span><span class="sxs-lookup"><span data-stu-id="a0755-350">1000</span></span></td>
    <td><span data-ttu-id="a0755-351">1</span><span class="sxs-lookup"><span data-stu-id="a0755-351">1</span></span></td>
    <td><span data-ttu-id="a0755-352">12</span><span class="sxs-lookup"><span data-stu-id="a0755-352">12</span></span></td>
    <td><span data-ttu-id="a0755-353">4</span><span class="sxs-lookup"><span data-stu-id="a0755-353">4</span></span></td>
    <td><span data-ttu-id="a0755-354">364.29</span><span class="sxs-lookup"><span data-stu-id="a0755-354">364.29</span></span></td>
    <td><span data-ttu-id="a0755-355">14</span><span class="sxs-lookup"><span data-stu-id="a0755-355">14</span></span></td>
    <td><span data-ttu-id="a0755-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="a0755-356">1,275.00</span></span></td>
    <td><span data-ttu-id="a0755-357">91.07</span><span class="sxs-lookup"><span data-stu-id="a0755-357">91.07</span></span></td>
    <td><span data-ttu-id="a0755-358">4.00</span><span class="sxs-lookup"><span data-stu-id="a0755-358">4.00</span></span></td>
    <td><span data-ttu-id="a0755-359">364.29</span><span class="sxs-lookup"><span data-stu-id="a0755-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="a0755-360">1000</span><span class="sxs-lookup"><span data-stu-id="a0755-360">1000</span></span></td>
    <td><span data-ttu-id="a0755-361">2</span><span class="sxs-lookup"><span data-stu-id="a0755-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="a0755-362">10</span><span class="sxs-lookup"><span data-stu-id="a0755-362">10</span></span></td>
    <td><span data-ttu-id="a0755-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a0755-363">2,000.00</span></span></td>
    <td><span data-ttu-id="a0755-364">10</span><span class="sxs-lookup"><span data-stu-id="a0755-364">10</span></span></td>
    <td><span data-ttu-id="a0755-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a0755-365">2,000.00</span></span></td>
    <td><span data-ttu-id="a0755-366">200.00</span><span class="sxs-lookup"><span data-stu-id="a0755-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a0755-367">10.00</span><span class="sxs-lookup"><span data-stu-id="a0755-367">10.00</span></span></td>
    <td><span data-ttu-id="a0755-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="a0755-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="a0755-369"><strong>总计 1000</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a0755-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="a0755-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="a0755-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="a0755-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="a0755-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="a0755-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="a0755-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="a0755-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="a0755-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
