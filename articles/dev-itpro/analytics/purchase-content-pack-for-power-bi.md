---
title: 采购花费分析 Power BI 内容
description: 此主题介绍采购支出分析 Power BI 内容中的内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
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
ms.openlocfilehash: 3206573022c0f843b07a468987a112ca6ac435ef
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1527709"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="fe287-104">采购花费分析 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="fe287-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe287-105">此主题介绍**采购支出分析** Microsoft Power BI 内容中的内容。</span><span class="sxs-lookup"><span data-stu-id="fe287-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="fe287-106">它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="fe287-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="fe287-107">概览</span><span class="sxs-lookup"><span data-stu-id="fe287-107">Overview</span></span>

<span data-ttu-id="fe287-108">**采购支出分析** Power BI 内容的设计是为了帮助采购经理和负责预算的经理跟踪采购支出。</span><span class="sxs-lookup"><span data-stu-id="fe287-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="fe287-109">经理可以通过以下方式分析采购支出：</span><span class="sxs-lookup"><span data-stu-id="fe287-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="fe287-110">本年迄今的采购（按供应商组和单个供应商、采购类别和单个产品，以及供应商位置）</span><span class="sxs-lookup"><span data-stu-id="fe287-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="fe287-111">各年的采购变化（按供应商组和采购类别）</span><span class="sxs-lookup"><span data-stu-id="fe287-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="fe287-112">该内容使用采购交易数据，并且同时提供公司范围的采购数据聚合视图和按供应商与产品分类的采购支出分解。</span><span class="sxs-lookup"><span data-stu-id="fe287-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="fe287-113">报表突出显示一段时间的采购支出变化。</span><span class="sxs-lookup"><span data-stu-id="fe287-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="fe287-114">因此，这些报表可用于提醒经理有关单个供应商和产品的正负支出趋势的信息。</span><span class="sxs-lookup"><span data-stu-id="fe287-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="fe287-115">此外，图表显示不同采购类别和供应商组的采购支出。</span><span class="sxs-lookup"><span data-stu-id="fe287-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="fe287-116">因此，类别和区域经理可以使用这些图表来帮助识别支出行为的变化。</span><span class="sxs-lookup"><span data-stu-id="fe287-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="fe287-117">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="fe287-117">Accessing the Power BI content</span></span>
<span data-ttu-id="fe287-118">**采购花费分析** Power BI 内容显示在**采购和花费分析**页面（**采购** \> **查询和报表** \> **采购绩效分析** \> **采购和花费分析**）。</span><span class="sxs-lookup"><span data-stu-id="fe287-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="fe287-119">此 Power BI 内容中包含的度量</span><span class="sxs-lookup"><span data-stu-id="fe287-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="fe287-120">**采购支出分析** Power BI 内容中包含一个由一组指标构成的报表。</span><span class="sxs-lookup"><span data-stu-id="fe287-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="fe287-121">这些指标显示为图表、磁贴和表。</span><span class="sxs-lookup"><span data-stu-id="fe287-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="fe287-122">以下部分提供对可视化项的概览。</span><span class="sxs-lookup"><span data-stu-id="fe287-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="fe287-123">按供应商的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="fe287-123">Purchase by vendor report page</span></span>
<span data-ttu-id="fe287-124">**图表**</span><span class="sxs-lookup"><span data-stu-id="fe287-124">**Charts**</span></span>
- <span data-ttu-id="fe287-125">按采购排名前 10 位的供应商（堆积条形图）</span><span class="sxs-lookup"><span data-stu-id="fe287-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="fe287-126">按供应商组/国家或地区/名称的采购总额（饼图）</span><span class="sxs-lookup"><span data-stu-id="fe287-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="fe287-127">按供应商组/国家或地区/名称的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="fe287-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="fe287-128">按供应商组/国家或地区/名称的平均采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="fe287-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="fe287-129">**磁贴**</span><span class="sxs-lookup"><span data-stu-id="fe287-129">**Tiles**</span></span>
- <span data-ttu-id="fe287-130">采购总额</span><span class="sxs-lookup"><span data-stu-id="fe287-130">Total purchase</span></span>
- <span data-ttu-id="fe287-131">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="fe287-131">YOY purchase growth</span></span>
- <span data-ttu-id="fe287-132">供应商总数</span><span class="sxs-lookup"><span data-stu-id="fe287-132">Total # vendors</span></span>
- <span data-ttu-id="fe287-133">有效供应商总数</span><span class="sxs-lookup"><span data-stu-id="fe287-133">Total # of active vendors</span></span>

<span data-ttu-id="fe287-134">**示例**</span><span class="sxs-lookup"><span data-stu-id="fe287-134">**Example**</span></span>
<img src="media/spend1.PNG" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="fe287-135">按产品的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="fe287-135">Purchase by product report page</span></span>

<span data-ttu-id="fe287-136">**图表**</span><span class="sxs-lookup"><span data-stu-id="fe287-136">**Charts**</span></span>
- <span data-ttu-id="fe287-137">按采购类别/产品名称的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="fe287-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="fe287-138">按采购类别/产品名称的采购总额（饼图）</span><span class="sxs-lookup"><span data-stu-id="fe287-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="fe287-139">按采购排名前 10 位的产品（堆积条形图）</span><span class="sxs-lookup"><span data-stu-id="fe287-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="fe287-140">**磁贴**</span><span class="sxs-lookup"><span data-stu-id="fe287-140">**Tiles**</span></span>
- <span data-ttu-id="fe287-141">产品总数</span><span class="sxs-lookup"><span data-stu-id="fe287-141">Total # of products</span></span></li>
- <span data-ttu-id="fe287-142">产品总数中有效产品所占总百分比</span><span class="sxs-lookup"><span data-stu-id="fe287-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="fe287-143">占采购中的 80% 的产品的数量</span><span class="sxs-lookup"><span data-stu-id="fe287-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="fe287-144">**示例**</span><span class="sxs-lookup"><span data-stu-id="fe287-144">**Example**</span></span>


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="fe287-145">按期间的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="fe287-145">Purchase by period report page</span></span>
<span data-ttu-id="fe287-146">此页中显示 今年和去年的采购，以及按采购类别的采购。</span><span class="sxs-lookup"><span data-stu-id="fe287-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="fe287-147">**图表**</span><span class="sxs-lookup"><span data-stu-id="fe287-147">**Charts**</span></span> 
- <span data-ttu-id="fe287-148">按月/天的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="fe287-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="fe287-149">累积采购 YOY 差异（瀑布图）</span><span class="sxs-lookup"><span data-stu-id="fe287-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="fe287-150">采购 YOY 增长总额（柱形图）</span><span class="sxs-lookup"><span data-stu-id="fe287-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="fe287-151">采购报表（矩阵）</span><span class="sxs-lookup"><span data-stu-id="fe287-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="fe287-152">**磁贴**</span><span class="sxs-lookup"><span data-stu-id="fe287-152">**Tiles**</span></span>
- <span data-ttu-id="fe287-153">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="fe287-153">YOY purchase growth</span></span>
- <span data-ttu-id="fe287-154">YOY 采购增长百分比</span><span class="sxs-lookup"><span data-stu-id="fe287-154">YOY purchase growth %</span></span>

<span data-ttu-id="fe287-155">**示例**</span><span class="sxs-lookup"><span data-stu-id="fe287-155">**Example**</span></span>
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="fe287-156">按供应商位置的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="fe287-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="fe287-157">**图表**</span><span class="sxs-lookup"><span data-stu-id="fe287-157">**Charts**</span></span>
- <span data-ttu-id="fe287-158">按城市的采购</span><span class="sxs-lookup"><span data-stu-id="fe287-158">Purchase by city</span></span>
- <span data-ttu-id="fe287-159">采购 YOY 增长百分比</span><span class="sxs-lookup"><span data-stu-id="fe287-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="fe287-160">按国家/地区的采购</span><span class="sxs-lookup"><span data-stu-id="fe287-160">Purchase by country</span></span>

<span data-ttu-id="fe287-161">**示例**</span><span class="sxs-lookup"><span data-stu-id="fe287-161">**Example**</span></span>
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="fe287-162">按时间的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="fe287-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="fe287-163">**图表**</span><span class="sxs-lookup"><span data-stu-id="fe287-163">**Charts**</span></span> 
- <span data-ttu-id="fe287-164">按月/日的本年采购（折线图）</span><span class="sxs-lookup"><span data-stu-id="fe287-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="fe287-165">本年和去年的采购（折现柱形图）</span><span class="sxs-lookup"><span data-stu-id="fe287-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="fe287-166">**示例**</span><span class="sxs-lookup"><span data-stu-id="fe287-166">**Example**</span></span>
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="fe287-167">按供应商的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="fe287-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="fe287-168">**图表**</span><span class="sxs-lookup"><span data-stu-id="fe287-168">**Charts**</span></span> 
- <span data-ttu-id="fe287-169">排名前 10 位的供应商所占采购百分比（漏斗图）</span><span class="sxs-lookup"><span data-stu-id="fe287-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="fe287-170">排名前 10 位的供应商（带 YOY 的增加支出）</span><span class="sxs-lookup"><span data-stu-id="fe287-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="fe287-171">排名前 10 位的供应商（带 YOY 的降低支出）</span><span class="sxs-lookup"><span data-stu-id="fe287-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="fe287-172">**示例** 
</span><span class="sxs-lookup"><span data-stu-id="fe287-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="fe287-173">数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="fe287-173">Data model and entities</span></span>
<span data-ttu-id="fe287-174">以下数据用于填充**采购支出分析** Power BI 内容中的报表页。</span><span class="sxs-lookup"><span data-stu-id="fe287-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="fe287-175">此数据表示为实体商店内已分组的聚合度量。</span><span class="sxs-lookup"><span data-stu-id="fe287-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="fe287-176">实体商店是针对分析进行优化的 Microsoft SQL Server 数据库。</span><span class="sxs-lookup"><span data-stu-id="fe287-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="fe287-177">有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md)。</span><span class="sxs-lookup"><span data-stu-id="fe287-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="fe287-178">此内容包中的聚合度量是 Microsoft Dynamics AX 2012 和 Microsoft Dynamics AX 2012 R3 中的采购多维数据集中提供的聚合度量子集。</span><span class="sxs-lookup"><span data-stu-id="fe287-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="fe287-179">若要在实体商店中暂存多维数据集的聚合度量，必须将其设置为可部署。</span><span class="sxs-lookup"><span data-stu-id="fe287-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="fe287-180">有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md)中在实体商店中暂存聚合度量的过程。</span><span class="sxs-lookup"><span data-stu-id="fe287-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="fe287-181">以下关键聚合度量直接从发票行实体提供，并用作此内容的基础。</span><span class="sxs-lookup"><span data-stu-id="fe287-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="fe287-182">实体</span><span class="sxs-lookup"><span data-stu-id="fe287-182">Entity</span></span>        | <span data-ttu-id="fe287-183">关键聚合度量</span><span class="sxs-lookup"><span data-stu-id="fe287-183">Key aggregate measurements</span></span> | <span data-ttu-id="fe287-184">数据源</span><span class="sxs-lookup"><span data-stu-id="fe287-184">Data source</span></span>                                 | <span data-ttu-id="fe287-185">字段</span><span class="sxs-lookup"><span data-stu-id="fe287-185">Field</span></span>              | <span data-ttu-id="fe287-186">说明</span><span class="sxs-lookup"><span data-stu-id="fe287-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="fe287-187">发票行</span><span class="sxs-lookup"><span data-stu-id="fe287-187">Invoice lines</span></span> | <span data-ttu-id="fe287-188">采购</span><span class="sxs-lookup"><span data-stu-id="fe287-188">Purchase</span></span>                   | <span data-ttu-id="fe287-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="fe287-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="fe287-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="fe287-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="fe287-191">以记帐币种计算的金额。</span><span class="sxs-lookup"><span data-stu-id="fe287-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="fe287-192">下表显示内容中通过发票行实体计算出的关键度量。</span><span class="sxs-lookup"><span data-stu-id="fe287-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="fe287-193">度量</span><span class="sxs-lookup"><span data-stu-id="fe287-193">Measure</span></span>               | <span data-ttu-id="fe287-194">计算</span><span class="sxs-lookup"><span data-stu-id="fe287-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe287-195">本年的采购</span><span class="sxs-lookup"><span data-stu-id="fe287-195">Purchase current year</span></span> | <span data-ttu-id="fe287-196">本年的采购 = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="fe287-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="fe287-197">去年的采购</span><span class="sxs-lookup"><span data-stu-id="fe287-197">Purchase last year</span></span>    | <span data-ttu-id="fe287-198">去年的采购 = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="fe287-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="fe287-199">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="fe287-199">YOY purchase growth</span></span>   | <span data-ttu-id="fe287-200">YOY 采购增长 = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="fe287-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="fe287-201">内容中的以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。</span><span class="sxs-lookup"><span data-stu-id="fe287-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="fe287-202">实体</span><span class="sxs-lookup"><span data-stu-id="fe287-202">Entity</span></span>                 | <span data-ttu-id="fe287-203">属性示例</span><span class="sxs-lookup"><span data-stu-id="fe287-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="fe287-204">供应商</span><span class="sxs-lookup"><span data-stu-id="fe287-204">Vendors</span></span>                | <span data-ttu-id="fe287-205">供应商组、供应商国家或地区、供应商名称</span><span class="sxs-lookup"><span data-stu-id="fe287-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="fe287-206">产品</span><span class="sxs-lookup"><span data-stu-id="fe287-206">Products</span></span>               | <span data-ttu-id="fe287-207">产品编号、产品名称、物料组名称</span><span class="sxs-lookup"><span data-stu-id="fe287-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="fe287-208">采购类别</span><span class="sxs-lookup"><span data-stu-id="fe287-208">Procurement categories</span></span> | <span data-ttu-id="fe287-209">采购类别、采购类别名称</span><span class="sxs-lookup"><span data-stu-id="fe287-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="fe287-210">法人</span><span class="sxs-lookup"><span data-stu-id="fe287-210">Legal entities</span></span>         | <span data-ttu-id="fe287-211">法人姓名</span><span class="sxs-lookup"><span data-stu-id="fe287-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="fe287-212">日期</span><span class="sxs-lookup"><span data-stu-id="fe287-212">Dates</span></span>                  | <span data-ttu-id="fe287-213">日期、年偏移</span><span class="sxs-lookup"><span data-stu-id="fe287-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="fe287-214">默认情况下，此内容显示当前日历年的数据。</span><span class="sxs-lookup"><span data-stu-id="fe287-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="fe287-215">但是，您可以更改报表筛选器部分中的数据筛选器。</span><span class="sxs-lookup"><span data-stu-id="fe287-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="fe287-216">还可以更改公司筛选器。</span><span class="sxs-lookup"><span data-stu-id="fe287-216">You can also change the company filter.</span></span>
