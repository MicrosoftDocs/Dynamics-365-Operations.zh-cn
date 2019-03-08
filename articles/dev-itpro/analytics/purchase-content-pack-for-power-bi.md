---
title: 采购花费分析 Power BI 内容
description: 此主题介绍采购支出分析 Power BI 内容中的内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "313834"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="b9a4f-104">采购花费分析 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="b9a4f-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9a4f-105">此主题介绍**采购支出分析** Microsoft Power BI 内容中的内容。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="b9a4f-106">它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="b9a4f-107">概览</span><span class="sxs-lookup"><span data-stu-id="b9a4f-107">Overview</span></span>

<span data-ttu-id="b9a4f-108">**采购支出分析** Power BI 内容的设计是为了帮助采购经理和负责预算的经理密切注意采购支出。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="b9a4f-109">经理可以通过以下方式分析采购支出：</span><span class="sxs-lookup"><span data-stu-id="b9a4f-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="b9a4f-110">本年迄今的采购（按供应商组和单个供应商、采购类别和单个产品，以及供应商位置）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="b9a4f-111">各年的采购变化（按供应商组和采购类别）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="b9a4f-112">该内容使用采购交易数据，并且同时提供公司范围的采购数据聚合视图和按供应商与产品分类的采购支出分解。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="b9a4f-113">报表突出显示一段时间的采购支出变化。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="b9a4f-114">因此，这些报表可用于提醒经理有关单个供应商和产品的正负支出趋势的信息。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="b9a4f-115">此外，图表显示不同采购类别和供应商组的采购支出。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="b9a4f-116">因此，类别和区域经理可以使用这些图表来帮助识别支出行为的变化。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="b9a4f-117">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="b9a4f-117">Accessing the Power BI content</span></span>
<span data-ttu-id="b9a4f-118">**采购花费分析** Power BI 内容显示在**采购和花费分析**页面（**采购** \> **查询和报表** \> **采购绩效分析** \> **采购和花费分析**）。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="b9a4f-119">此 Power BI 内容中包含的度量</span><span class="sxs-lookup"><span data-stu-id="b9a4f-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="b9a4f-120">**采购支出分析** Power BI 内容中包含一个由一组指标构成的报表。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="b9a4f-121">这些指标显示为图表、磁贴和表。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="b9a4f-122">下表提供对可视化项的概览。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b9a4f-123">报表页</span><span class="sxs-lookup"><span data-stu-id="b9a4f-123">Report page</span></span></th>
<th><span data-ttu-id="b9a4f-124">图表</span><span class="sxs-lookup"><span data-stu-id="b9a4f-124">Charts</span></span></th>
<th><span data-ttu-id="b9a4f-125">磁贴</span><span class="sxs-lookup"><span data-stu-id="b9a4f-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b9a4f-126">按供应商的采购</span><span class="sxs-lookup"><span data-stu-id="b9a4f-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="b9a4f-127">按采购排名前 10 位的供应商（堆积条形图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="b9a4f-128">按供应商组/国家或地区/名称的采购总额（饼图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="b9a4f-129">按供应商组/国家或地区/名称的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="b9a4f-130">按供应商组/国家或地区/名称的平均采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b9a4f-131">采购总额</span><span class="sxs-lookup"><span data-stu-id="b9a4f-131">Total purchase</span></span></li>
<li><span data-ttu-id="b9a4f-132">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="b9a4f-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="b9a4f-133">供应商总数</span><span class="sxs-lookup"><span data-stu-id="b9a4f-133">Total # vendors</span></span></li>
<li><span data-ttu-id="b9a4f-134">有效供应商总数</span><span class="sxs-lookup"><span data-stu-id="b9a4f-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="b9a4f-135">按产品的采购</span><span class="sxs-lookup"><span data-stu-id="b9a4f-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="b9a4f-136">按采购类别/产品名称的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="b9a4f-137">按采购类别/产品名称的采购总额（饼图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="b9a4f-138">按采购排名前 10 位的产品（堆积条形图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b9a4f-139">产品总数</span><span class="sxs-lookup"><span data-stu-id="b9a4f-139">Total # of products</span></span></li>
<li><span data-ttu-id="b9a4f-140">产品总数中有效产品所占总百分比</span><span class="sxs-lookup"><span data-stu-id="b9a4f-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="b9a4f-141">占采购中的 80% 的产品的数量</span><span class="sxs-lookup"><span data-stu-id="b9a4f-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="b9a4f-142">按期间的采购\*</span><span class="sxs-lookup"><span data-stu-id="b9a4f-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="b9a4f-143">按月/天的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="b9a4f-144">累积采购 YOY 差异（瀑布图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="b9a4f-145">采购 YOY 增长总额（柱形图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="b9a4f-146">采购报表（矩阵）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b9a4f-147">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="b9a4f-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="b9a4f-148">YOY 采购增长百分比</span><span class="sxs-lookup"><span data-stu-id="b9a4f-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="b9a4f-149">按供应商位置的采购</span><span class="sxs-lookup"><span data-stu-id="b9a4f-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="b9a4f-150">按城市的采购</span><span class="sxs-lookup"><span data-stu-id="b9a4f-150">Purchase by city</span></span></li>
<li><span data-ttu-id="b9a4f-151">采购 YOY 增长百分比</span><span class="sxs-lookup"><span data-stu-id="b9a4f-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="b9a4f-152">按国家/地区的采购</span><span class="sxs-lookup"><span data-stu-id="b9a4f-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="b9a4f-153">按时间的采购支出分析</span><span class="sxs-lookup"><span data-stu-id="b9a4f-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="b9a4f-154">按月/日的本年采购（折线图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="b9a4f-155">本年和去年的采购（折现柱形图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="b9a4f-156">按供应商的采购支出分析</span><span class="sxs-lookup"><span data-stu-id="b9a4f-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="b9a4f-157">排名前 10 位的供应商所占采购百分比（漏斗图）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="b9a4f-158">排名前 10 位的供应商（带 YOY 的增加支出）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="b9a4f-159">排名前 10 位的供应商（带 YOY 的降低支出）</span><span class="sxs-lookup"><span data-stu-id="b9a4f-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b9a4f-160">\* 今年和去年的采购，以及按采购类别的增长</span><span class="sxs-lookup"><span data-stu-id="b9a4f-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="b9a4f-161">数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="b9a4f-161">Data model and entities</span></span>
<span data-ttu-id="b9a4f-162">以下数据用于填充**采购支出分析** Power BI 内容中的报表页。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="b9a4f-163">此数据表示为实体商店内已分组的聚合度量。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="b9a4f-164">实体商店是针对分析进行优化的 Microsoft SQL Server 数据库。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="b9a4f-165">有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md)。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="b9a4f-166">此内容包中的聚合度量是 Microsoft Dynamics AX 2012 和 Microsoft Dynamics AX 2012 R3 中的采购多维数据集中提供的聚合度量子集。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="b9a4f-167">若要在实体商店中暂存多维数据集的聚合度量，必须将其设置为可部署。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="b9a4f-168">有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md)中在实体商店中暂存聚合度量的过程。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="b9a4f-169">以下关键聚合度量直接从发票行实体提供，并用作此内容的基础。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="b9a4f-170">实体</span><span class="sxs-lookup"><span data-stu-id="b9a4f-170">Entity</span></span>        | <span data-ttu-id="b9a4f-171">关键聚合度量</span><span class="sxs-lookup"><span data-stu-id="b9a4f-171">Key aggregate measurements</span></span> | <span data-ttu-id="b9a4f-172">数据源</span><span class="sxs-lookup"><span data-stu-id="b9a4f-172">Data source</span></span>                                 | <span data-ttu-id="b9a4f-173">字段</span><span class="sxs-lookup"><span data-stu-id="b9a4f-173">Field</span></span>              | <span data-ttu-id="b9a4f-174">说明</span><span class="sxs-lookup"><span data-stu-id="b9a4f-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="b9a4f-175">发票行</span><span class="sxs-lookup"><span data-stu-id="b9a4f-175">Invoice lines</span></span> | <span data-ttu-id="b9a4f-176">采购</span><span class="sxs-lookup"><span data-stu-id="b9a4f-176">Purchase</span></span>                   | <span data-ttu-id="b9a4f-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="b9a4f-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="b9a4f-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="b9a4f-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="b9a4f-179">以记帐币种计算的金额。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="b9a4f-180">下表显示内容中通过发票行实体计算出的关键度量。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="b9a4f-181">度量</span><span class="sxs-lookup"><span data-stu-id="b9a4f-181">Measure</span></span>               | <span data-ttu-id="b9a4f-182">计算</span><span class="sxs-lookup"><span data-stu-id="b9a4f-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9a4f-183">本年的采购</span><span class="sxs-lookup"><span data-stu-id="b9a4f-183">Purchase current year</span></span> | <span data-ttu-id="b9a4f-184">本年的采购 = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="b9a4f-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="b9a4f-185">去年的采购</span><span class="sxs-lookup"><span data-stu-id="b9a4f-185">Purchase last year</span></span>    | <span data-ttu-id="b9a4f-186">去年的采购 = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="b9a4f-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="b9a4f-187">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="b9a4f-187">YOY purchase growth</span></span>   | <span data-ttu-id="b9a4f-188">YOY 采购增长 = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="b9a4f-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="b9a4f-189">内容中的以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="b9a4f-190">实体</span><span class="sxs-lookup"><span data-stu-id="b9a4f-190">Entity</span></span>                 | <span data-ttu-id="b9a4f-191">属性示例</span><span class="sxs-lookup"><span data-stu-id="b9a4f-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b9a4f-192">供应商</span><span class="sxs-lookup"><span data-stu-id="b9a4f-192">Vendors</span></span>                | <span data-ttu-id="b9a4f-193">供应商组、供应商国家或地区、供应商名称</span><span class="sxs-lookup"><span data-stu-id="b9a4f-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="b9a4f-194">产品</span><span class="sxs-lookup"><span data-stu-id="b9a4f-194">Products</span></span>               | <span data-ttu-id="b9a4f-195">产品编号、产品名称、物料组名称</span><span class="sxs-lookup"><span data-stu-id="b9a4f-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="b9a4f-196">采购类别</span><span class="sxs-lookup"><span data-stu-id="b9a4f-196">Procurement categories</span></span> | <span data-ttu-id="b9a4f-197">采购类别、采购类别名称</span><span class="sxs-lookup"><span data-stu-id="b9a4f-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="b9a4f-198">法人</span><span class="sxs-lookup"><span data-stu-id="b9a4f-198">Legal entities</span></span>         | <span data-ttu-id="b9a4f-199">法人姓名</span><span class="sxs-lookup"><span data-stu-id="b9a4f-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="b9a4f-200">日期</span><span class="sxs-lookup"><span data-stu-id="b9a4f-200">Dates</span></span>                  | <span data-ttu-id="b9a4f-201">日期、年偏移</span><span class="sxs-lookup"><span data-stu-id="b9a4f-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="b9a4f-202">默认情况下，此内容显示当前日历年的数据。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="b9a4f-203">但是，您可以更改报表筛选器部分中的数据筛选器。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="b9a4f-204">还可以更改公司筛选器。</span><span class="sxs-lookup"><span data-stu-id="b9a4f-204">You can also change the company filter.</span></span>
