---
title: 采购花费分析 Power BI 内容
description: 此主题介绍采购支出分析 Power BI 内容中的内容。
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4149b13754b544558dbb5666fbec7df97e5c5d8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559541"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="3ff0f-103">采购花费分析 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="3ff0f-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ff0f-104">此主题介绍 **采购支出分析** Microsoft Power BI 内容中所包含的内容。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="3ff0f-105">它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="3ff0f-106">概览</span><span class="sxs-lookup"><span data-stu-id="3ff0f-106">Overview</span></span>

<span data-ttu-id="3ff0f-107">**采购支出分析** Power BI 内容的设计是为了帮助采购经理和负责预算的经理跟踪采购支出。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="3ff0f-108">经理可以通过以下方式分析采购支出：</span><span class="sxs-lookup"><span data-stu-id="3ff0f-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="3ff0f-109">本年迄今的采购（按供应商组和单个供应商、采购类别和单个产品，以及供应商位置）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="3ff0f-110">各年的采购变化（按供应商组和采购类别）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="3ff0f-111">该内容使用采购交易数据，并且同时提供公司范围的采购数据聚合视图和按供应商与产品分类的采购支出分解。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="3ff0f-112">报表突出显示一段时间的采购支出变化。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="3ff0f-113">因此，这些报表可用于提醒经理有关单个供应商和产品的正负支出趋势的信息。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="3ff0f-114">此外，图表显示不同采购类别和供应商组的采购支出。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="3ff0f-115">因此，类别和区域经理可以使用这些图表来帮助识别支出行为的变化。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="3ff0f-116">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="3ff0f-116">Accessing the Power BI content</span></span>
<span data-ttu-id="3ff0f-117">**采购花费分析** Power BI 内容显示在 **采购和花费分析** 页面（**采购** \> **查询和报表** \> **采购绩效分析** \> **采购和花费分析**）。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="3ff0f-118">此 Power BI 内容中包含的度量</span><span class="sxs-lookup"><span data-stu-id="3ff0f-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="3ff0f-119">**采购支出分析** Power BI 内容中包含一个由一组指标构成的报表。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="3ff0f-120">这些指标显示为图表、磁贴和表。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="3ff0f-121">以下部分提供对可视化项的概览。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="3ff0f-122">按供应商的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="3ff0f-122">Purchase by vendor report page</span></span>
<span data-ttu-id="3ff0f-123">**图表**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-123">**Charts**</span></span>
- <span data-ttu-id="3ff0f-124">按采购排名前 10 位的供应商（堆积条形图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="3ff0f-125">按供应商组/国家或地区/名称的采购总额（饼图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="3ff0f-126">按供应商组/国家或地区/名称的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="3ff0f-127">按供应商组/国家或地区/名称的平均采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="3ff0f-128">**磁贴**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-128">**Tiles**</span></span>
- <span data-ttu-id="3ff0f-129">采购总额</span><span class="sxs-lookup"><span data-stu-id="3ff0f-129">Total purchase</span></span>
- <span data-ttu-id="3ff0f-130">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="3ff0f-130">YOY purchase growth</span></span>
- <span data-ttu-id="3ff0f-131">供应商总数</span><span class="sxs-lookup"><span data-stu-id="3ff0f-131">Total # vendors</span></span>
- <span data-ttu-id="3ff0f-132">有效供应商总数</span><span class="sxs-lookup"><span data-stu-id="3ff0f-132">Total # of active vendors</span></span>

<span data-ttu-id="3ff0f-133">**示例**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="3ff0f-134">按产品的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="3ff0f-134">Purchase by product report page</span></span>

<span data-ttu-id="3ff0f-135">**图表**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-135">**Charts**</span></span>
- <span data-ttu-id="3ff0f-136">按采购类别/产品名称的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="3ff0f-137">按采购类别/产品名称的采购总额（饼图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="3ff0f-138">按采购排名前 10 位的产品（堆积条形图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="3ff0f-139">**磁贴**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-139">**Tiles**</span></span>
- <span data-ttu-id="3ff0f-140">产品总数</span><span class="sxs-lookup"><span data-stu-id="3ff0f-140">Total # of products</span></span></li>
- <span data-ttu-id="3ff0f-141">产品总数中有效产品所占总百分比</span><span class="sxs-lookup"><span data-stu-id="3ff0f-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="3ff0f-142">占采购中的 80% 的产品的数量</span><span class="sxs-lookup"><span data-stu-id="3ff0f-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="3ff0f-143">**示例**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="3ff0f-144">按期间的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="3ff0f-144">Purchase by period report page</span></span>
<span data-ttu-id="3ff0f-145">此页中显示 今年和去年的采购，以及按采购类别的采购。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="3ff0f-146">**图表**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-146">**Charts**</span></span> 
- <span data-ttu-id="3ff0f-147">按月/天的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="3ff0f-148">累积采购 YOY 差异（瀑布图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="3ff0f-149">采购 YOY 增长总额（柱形图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="3ff0f-150">采购报表（矩阵）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="3ff0f-151">**磁贴**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-151">**Tiles**</span></span>
- <span data-ttu-id="3ff0f-152">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="3ff0f-152">YOY purchase growth</span></span>
- <span data-ttu-id="3ff0f-153">YOY 采购增长百分比</span><span class="sxs-lookup"><span data-stu-id="3ff0f-153">YOY purchase growth %</span></span>

<span data-ttu-id="3ff0f-154">**示例**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="3ff0f-155">按供应商位置的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="3ff0f-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="3ff0f-156">**图表**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-156">**Charts**</span></span>
- <span data-ttu-id="3ff0f-157">按城市的采购</span><span class="sxs-lookup"><span data-stu-id="3ff0f-157">Purchase by city</span></span>
- <span data-ttu-id="3ff0f-158">采购 YOY 增长百分比</span><span class="sxs-lookup"><span data-stu-id="3ff0f-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="3ff0f-159">按国家/地区的采购</span><span class="sxs-lookup"><span data-stu-id="3ff0f-159">Purchase by country</span></span>

<span data-ttu-id="3ff0f-160">**示例**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="3ff0f-161">按时间的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="3ff0f-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="3ff0f-162">**图表**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-162">**Charts**</span></span> 
- <span data-ttu-id="3ff0f-163">按月/日的本年采购（折线图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="3ff0f-164">本年和去年的采购（折现柱形图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="3ff0f-165">**示例**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="3ff0f-166">按供应商的采购报表页面</span><span class="sxs-lookup"><span data-stu-id="3ff0f-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="3ff0f-167">**图表**</span><span class="sxs-lookup"><span data-stu-id="3ff0f-167">**Charts**</span></span> 
- <span data-ttu-id="3ff0f-168">排名前 10 位的供应商所占采购百分比（漏斗图）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="3ff0f-169">排名前 10 位的供应商（带 YOY 的增加支出）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="3ff0f-170">排名前 10 位的供应商（带 YOY 的降低支出）</span><span class="sxs-lookup"><span data-stu-id="3ff0f-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="3ff0f-171">**示例** 
</span><span class="sxs-lookup"><span data-stu-id="3ff0f-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="3ff0f-172">数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="3ff0f-172">Data model and entities</span></span>
<span data-ttu-id="3ff0f-173">以下数据用于填充 **采购支出分析** Power BI 内容中的报表页。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="3ff0f-174">此数据表示为实体商店内已分组的聚合度量。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="3ff0f-175">实体商店是针对分析进行优化的 Microsoft SQL Server 数据库。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="3ff0f-176">有关详细信息，请参阅 [Power BI 与实体商店集成](power-bi-integration-entity-store.md)。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="3ff0f-177">此内容包中的聚合度量是 Microsoft Dynamics AX 2012 和 Microsoft Dynamics AX 2012 R3 中的采购多维数据集中提供的聚合度量子集。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="3ff0f-178">若要在实体商店中暂存多维数据集的聚合度量，必须将其设置为可部署。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="3ff0f-179">有关详细信息，请参阅 [Power BI 与实体商店集成](power-bi-integration-entity-store.md)中在实体商店中暂存聚合度量的过程。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="3ff0f-180">以下关键聚合度量直接从发票行实体提供，并用作此内容的基础。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="3ff0f-181">实体</span><span class="sxs-lookup"><span data-stu-id="3ff0f-181">Entity</span></span>        | <span data-ttu-id="3ff0f-182">关键聚合度量</span><span class="sxs-lookup"><span data-stu-id="3ff0f-182">Key aggregate measurements</span></span> | <span data-ttu-id="3ff0f-183">数据源</span><span class="sxs-lookup"><span data-stu-id="3ff0f-183">Data source</span></span>                                 | <span data-ttu-id="3ff0f-184">字段</span><span class="sxs-lookup"><span data-stu-id="3ff0f-184">Field</span></span>              | <span data-ttu-id="3ff0f-185">说明</span><span class="sxs-lookup"><span data-stu-id="3ff0f-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="3ff0f-186">发票行</span><span class="sxs-lookup"><span data-stu-id="3ff0f-186">Invoice lines</span></span> | <span data-ttu-id="3ff0f-187">采购</span><span class="sxs-lookup"><span data-stu-id="3ff0f-187">Purchase</span></span>                   | <span data-ttu-id="3ff0f-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="3ff0f-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="3ff0f-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="3ff0f-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="3ff0f-190">以记帐币种计算的金额。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="3ff0f-191">下表显示内容中通过发票行实体计算出的关键度量。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="3ff0f-192">度量</span><span class="sxs-lookup"><span data-stu-id="3ff0f-192">Measure</span></span>               | <span data-ttu-id="3ff0f-193">计算</span><span class="sxs-lookup"><span data-stu-id="3ff0f-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff0f-194">本年的采购</span><span class="sxs-lookup"><span data-stu-id="3ff0f-194">Purchase current year</span></span> | <span data-ttu-id="3ff0f-195">本年的采购 = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="3ff0f-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="3ff0f-196">去年的采购</span><span class="sxs-lookup"><span data-stu-id="3ff0f-196">Purchase last year</span></span>    | <span data-ttu-id="3ff0f-197">去年的采购 = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="3ff0f-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="3ff0f-198">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="3ff0f-198">YOY purchase growth</span></span>   | <span data-ttu-id="3ff0f-199">YOY 采购增长 = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="3ff0f-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="3ff0f-200">内容中的以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="3ff0f-201">实体</span><span class="sxs-lookup"><span data-stu-id="3ff0f-201">Entity</span></span>                 | <span data-ttu-id="3ff0f-202">属性示例</span><span class="sxs-lookup"><span data-stu-id="3ff0f-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="3ff0f-203">供应商</span><span class="sxs-lookup"><span data-stu-id="3ff0f-203">Vendors</span></span>                | <span data-ttu-id="3ff0f-204">供应商组、供应商国家或地区、供应商名称</span><span class="sxs-lookup"><span data-stu-id="3ff0f-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="3ff0f-205">产品</span><span class="sxs-lookup"><span data-stu-id="3ff0f-205">Products</span></span>               | <span data-ttu-id="3ff0f-206">产品编号、产品名称、物料组名称</span><span class="sxs-lookup"><span data-stu-id="3ff0f-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="3ff0f-207">采购类别</span><span class="sxs-lookup"><span data-stu-id="3ff0f-207">Procurement categories</span></span> | <span data-ttu-id="3ff0f-208">采购类别、采购类别名称</span><span class="sxs-lookup"><span data-stu-id="3ff0f-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="3ff0f-209">法人</span><span class="sxs-lookup"><span data-stu-id="3ff0f-209">Legal entities</span></span>         | <span data-ttu-id="3ff0f-210">法人姓名</span><span class="sxs-lookup"><span data-stu-id="3ff0f-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="3ff0f-211">日期</span><span class="sxs-lookup"><span data-stu-id="3ff0f-211">Dates</span></span>                  | <span data-ttu-id="3ff0f-212">日期、年偏移</span><span class="sxs-lookup"><span data-stu-id="3ff0f-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="3ff0f-213">默认情况下，此内容显示当前日历年的数据。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="3ff0f-214">但是，您可以更改报表筛选器部分中的数据筛选器。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="3ff0f-215">还可以更改公司筛选器。</span><span class="sxs-lookup"><span data-stu-id="3ff0f-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]