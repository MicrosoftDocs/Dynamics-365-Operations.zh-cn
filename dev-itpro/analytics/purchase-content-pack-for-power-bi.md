---
title: "采购支出分析 Power BI 内容"
description: "此主题介绍采购支出分析 Power BI 内容中的内容。 它说明如何访问内容中包括的报表，并提供有关用于构建内容的数据模型和实体的信息。"
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4e60a6c7d79f59382b3958b849d78aac18550bc3
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="7f248-104">采购支出分析 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="7f248-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7f248-105">此主题介绍**采购支出分析** Microsoft Power BI 内容中的内容。</span><span class="sxs-lookup"><span data-stu-id="7f248-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="7f248-106">它说明如何访问 Power BI 报表，并提供有关用于构建内容的数据模型和实体的信息。</span><span class="sxs-lookup"><span data-stu-id="7f248-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="7f248-107">概览</span><span class="sxs-lookup"><span data-stu-id="7f248-107">Overview</span></span>

<span data-ttu-id="7f248-108">**采购支出分析** Power BI 内容的设计是为了帮助采购经理和负责预算的经理密切注意采购支出。</span><span class="sxs-lookup"><span data-stu-id="7f248-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="7f248-109">经理可以通过以下方式分析采购支出：</span><span class="sxs-lookup"><span data-stu-id="7f248-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="7f248-110">本年迄今的采购（按供应商组和单个供应商、采购类别和单个产品，以及供应商位置）</span><span class="sxs-lookup"><span data-stu-id="7f248-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="7f248-111">各年的采购变化（按供应商组和采购类别）</span><span class="sxs-lookup"><span data-stu-id="7f248-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="7f248-112">该内容使用采购交易数据，并且同时提供公司范围的采购数据聚合视图和按供应商与产品分类的采购支出分解。</span><span class="sxs-lookup"><span data-stu-id="7f248-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="7f248-113">报表突出显示一段时间的采购支出变化。</span><span class="sxs-lookup"><span data-stu-id="7f248-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="7f248-114">因此，这些报表可用于提醒经理有关单个供应商和产品的正负支出趋势的信息。</span><span class="sxs-lookup"><span data-stu-id="7f248-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="7f248-115">此外，图表显示不同采购类别和供应商组的采购支出。</span><span class="sxs-lookup"><span data-stu-id="7f248-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="7f248-116">因此，类别和区域经理可以使用这些图表来帮助识别支出行为的变化。</span><span class="sxs-lookup"><span data-stu-id="7f248-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="7f248-117">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="7f248-117">Accessing the Power BI content</span></span>
<span data-ttu-id="7f248-118">如果您使用的是 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 2017 年 7 月更新，则**采购支出分析** Power BI 内容显示在**采购和支出分析**页（**采购** > **查询和报表** > **采购绩效分析** > **采购和支出分析**）上。</span><span class="sxs-lookup"><span data-stu-id="7f248-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update, the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="7f248-119">此 Power BI 内容中包含的指标</span><span class="sxs-lookup"><span data-stu-id="7f248-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="7f248-120">**采购支出分析** Power BI 内容包含一个由一组指标构成的报表。</span><span class="sxs-lookup"><span data-stu-id="7f248-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="7f248-121">这些指标显示为图表、磁贴和表。</span><span class="sxs-lookup"><span data-stu-id="7f248-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="7f248-122">下表提供对可视化项的概览。</span><span class="sxs-lookup"><span data-stu-id="7f248-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f248-123">报表页</span><span class="sxs-lookup"><span data-stu-id="7f248-123">Report page</span></span></th>
<th><span data-ttu-id="7f248-124">图表</span><span class="sxs-lookup"><span data-stu-id="7f248-124">Charts</span></span></th>
<th><span data-ttu-id="7f248-125">磁贴</span><span class="sxs-lookup"><span data-stu-id="7f248-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f248-126">按供应商的采购</span><span class="sxs-lookup"><span data-stu-id="7f248-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="7f248-127">按采购排名前 10 位的供应商（堆积条形图）</span><span class="sxs-lookup"><span data-stu-id="7f248-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="7f248-128">按供应商组/国家或地区/名称的采购总额（饼图）</span><span class="sxs-lookup"><span data-stu-id="7f248-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="7f248-129">按供应商组/国家或地区/名称的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="7f248-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="7f248-130">按供应商组/国家或地区/名称的平均采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="7f248-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7f248-131">采购总额</span><span class="sxs-lookup"><span data-stu-id="7f248-131">Total purchase</span></span></li>
<li><span data-ttu-id="7f248-132">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="7f248-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="7f248-133">供应商总数</span><span class="sxs-lookup"><span data-stu-id="7f248-133">Total # vendors</span></span></li>
<li><span data-ttu-id="7f248-134">有效供应商总数</span><span class="sxs-lookup"><span data-stu-id="7f248-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f248-135">按产品的采购</span><span class="sxs-lookup"><span data-stu-id="7f248-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="7f248-136">按采购类别/产品名称的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="7f248-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="7f248-137">按采购类别/产品名称的采购总额（饼图）</span><span class="sxs-lookup"><span data-stu-id="7f248-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="7f248-138">按采购排名前 10 位的产品（堆积条形图）</span><span class="sxs-lookup"><span data-stu-id="7f248-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7f248-139">产品总数</span><span class="sxs-lookup"><span data-stu-id="7f248-139">Total # of products</span></span></li>
<li><span data-ttu-id="7f248-140">产品总数中有效产品所占总百分比</span><span class="sxs-lookup"><span data-stu-id="7f248-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="7f248-141">占采购中的 80% 的产品的数量</span><span class="sxs-lookup"><span data-stu-id="7f248-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f248-142">按期间的采购*</span><span class="sxs-lookup"><span data-stu-id="7f248-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="7f248-143">按月/天的采购（柱形图）</span><span class="sxs-lookup"><span data-stu-id="7f248-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="7f248-144">累积采购 YOY 差异（瀑布图）</span><span class="sxs-lookup"><span data-stu-id="7f248-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="7f248-145">采购 YOY 增长总额（柱形图）</span><span class="sxs-lookup"><span data-stu-id="7f248-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="7f248-146">采购报表（矩阵）</span><span class="sxs-lookup"><span data-stu-id="7f248-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="7f248-147">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="7f248-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="7f248-148">YOY 采购增长百分比</span><span class="sxs-lookup"><span data-stu-id="7f248-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f248-149">按供应商位置的采购</span><span class="sxs-lookup"><span data-stu-id="7f248-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="7f248-150">按城市的采购</span><span class="sxs-lookup"><span data-stu-id="7f248-150">Purchase by city</span></span></li>
<li><span data-ttu-id="7f248-151">采购 YOY 增长百分比</span><span class="sxs-lookup"><span data-stu-id="7f248-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="7f248-152">按国家/地区的采购</span><span class="sxs-lookup"><span data-stu-id="7f248-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f248-153">按时间的采购支出分析</span><span class="sxs-lookup"><span data-stu-id="7f248-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="7f248-154">按月/日的本年采购（折线图）</span><span class="sxs-lookup"><span data-stu-id="7f248-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="7f248-155">本年和去年的采购（折现柱形图）</span><span class="sxs-lookup"><span data-stu-id="7f248-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f248-156">按供应商的采购支出分析</span><span class="sxs-lookup"><span data-stu-id="7f248-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="7f248-157">排名前 10 位的供应商所占采购百分比（漏斗图）</span><span class="sxs-lookup"><span data-stu-id="7f248-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="7f248-158">排名前 10 位的供应商（带 YOY 的增加支出）</span><span class="sxs-lookup"><span data-stu-id="7f248-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="7f248-159">排名前 10 位的供应商（带 YOY 的降低支出）</span><span class="sxs-lookup"><span data-stu-id="7f248-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7f248-160">\* 今年和去年的采购，以及按采购类别的增长</span><span class="sxs-lookup"><span data-stu-id="7f248-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="7f248-161">扩展 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="7f248-161">Extending the Power BI content</span></span>
<span data-ttu-id="7f248-162">使用在 Microsoft Dynamics Lifecycle Services (LCS) 中可用的内容包可以对未登录到 Microsoft Dynamics 365 的人员提供出色的分析。</span><span class="sxs-lookup"><span data-stu-id="7f248-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="7f248-163">您可以修改这些内容包，使它们包含其他报表或视觉对象，然后将内容包发布到您的 Power BI.com 租户进行分析。</span><span class="sxs-lookup"><span data-stu-id="7f248-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="7f248-164">可在 LCS 中的共享资产库内找到**采购支出分析** Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="7f248-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="7f248-165">有关如何下载内容并在您的组织中实现的详细信息，请参阅 [LCS 中 Microsoft 和合作伙伴提供的 Power BI 内容](power-bi-content-microsoft-partners.md)。</span><span class="sxs-lookup"><span data-stu-id="7f248-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="7f248-166">若要观看显示如何实现 Power BI 内容的演示，请参阅 [Dynamics Lifecycle Services 中来自 Microsoft 和您的合作伙伴的 Power BI 内容](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix。</span><span class="sxs-lookup"><span data-stu-id="7f248-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="7f248-167">请确保下载适用于您使用的 Dynamics 365 版本的**采购支出分析**内容。</span><span class="sxs-lookup"><span data-stu-id="7f248-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="7f248-168">如果您使用的是 Microsoft Dynamics 365 for Operations 版本 1611，则 KB 4011327 是此 Power BI 内容的先决条件。</span><span class="sxs-lookup"><span data-stu-id="7f248-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="7f248-169">登录 LCS 之后，可以在以下位置访问该 KB：https://fix.lcs.dynamics.com/issue/results/?q=kb4011327。</span><span class="sxs-lookup"><span data-stu-id="7f248-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="7f248-170">数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="7f248-170">Data model and entities</span></span>
<span data-ttu-id="7f248-171">以下数据用于填充**采购支出分析** Power BI 内容中的报表页。</span><span class="sxs-lookup"><span data-stu-id="7f248-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="7f248-172">此数据表示为实体商店内已分组的聚合度量。</span><span class="sxs-lookup"><span data-stu-id="7f248-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="7f248-173">实体商店是针对分析进行优化的 Microsoft SQL Server 数据库。</span><span class="sxs-lookup"><span data-stu-id="7f248-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="7f248-174">有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md)。</span><span class="sxs-lookup"><span data-stu-id="7f248-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="7f248-175">此内容中的聚合度量是 Microsoft Dynamics AX 2012 和 Microsoft Dynamics AX 2012 R3 中的采购多维数据集中提供的聚合度量子集。</span><span class="sxs-lookup"><span data-stu-id="7f248-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="7f248-176">若要在实体商店中暂存多维数据集的聚合度量，必须将其设置为可部署。</span><span class="sxs-lookup"><span data-stu-id="7f248-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="7f248-177">有关详细信息，请参阅 [Power BI 与实体商店集成概览](power-bi-integration-entity-store.md) 中在实体商店中暂存聚合度量的过程。</span><span class="sxs-lookup"><span data-stu-id="7f248-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="7f248-178">以下关键聚合度量直接从发票行实体提供，并用作此内容的基础。</span><span class="sxs-lookup"><span data-stu-id="7f248-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="7f248-179">实体</span><span class="sxs-lookup"><span data-stu-id="7f248-179">Entity</span></span>        | <span data-ttu-id="7f248-180">关键聚合度量</span><span class="sxs-lookup"><span data-stu-id="7f248-180">Key aggregate measurements</span></span> | <span data-ttu-id="7f248-181">数据源</span><span class="sxs-lookup"><span data-stu-id="7f248-181">Data source</span></span>                                 | <span data-ttu-id="7f248-182">字段</span><span class="sxs-lookup"><span data-stu-id="7f248-182">Field</span></span>              | <span data-ttu-id="7f248-183">说明</span><span class="sxs-lookup"><span data-stu-id="7f248-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="7f248-184">发票行</span><span class="sxs-lookup"><span data-stu-id="7f248-184">Invoice lines</span></span> | <span data-ttu-id="7f248-185">采购</span><span class="sxs-lookup"><span data-stu-id="7f248-185">Purchase</span></span>                   | <span data-ttu-id="7f248-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="7f248-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="7f248-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="7f248-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="7f248-188">以记帐币种计算的金额。</span><span class="sxs-lookup"><span data-stu-id="7f248-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="7f248-189">下表显示内容中通过发票行实体计算出的关键度量。</span><span class="sxs-lookup"><span data-stu-id="7f248-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="7f248-190">度量</span><span class="sxs-lookup"><span data-stu-id="7f248-190">Measure</span></span>               | <span data-ttu-id="7f248-191">计算</span><span class="sxs-lookup"><span data-stu-id="7f248-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f248-192">本年的采购</span><span class="sxs-lookup"><span data-stu-id="7f248-192">Purchase current year</span></span> | <span data-ttu-id="7f248-193">本年的采购 = SUM('Invoice lines'\[Purchase\])</span><span class="sxs-lookup"><span data-stu-id="7f248-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="7f248-194">去年的采购</span><span class="sxs-lookup"><span data-stu-id="7f248-194">Purchase last year</span></span>    | <span data-ttu-id="7f248-195">去年的采购 = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="7f248-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="7f248-196">YOY 采购增长</span><span class="sxs-lookup"><span data-stu-id="7f248-196">YOY purchase growth</span></span>   | <span data-ttu-id="7f248-197">YOY 采购增长 = \[Purchase current year\] – \[Purchase last year\]</span><span class="sxs-lookup"><span data-stu-id="7f248-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="7f248-198">内容中的以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。</span><span class="sxs-lookup"><span data-stu-id="7f248-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="7f248-199">实体</span><span class="sxs-lookup"><span data-stu-id="7f248-199">Entity</span></span>                 | <span data-ttu-id="7f248-200">属性示例</span><span class="sxs-lookup"><span data-stu-id="7f248-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="7f248-201">供应商</span><span class="sxs-lookup"><span data-stu-id="7f248-201">Vendors</span></span>                | <span data-ttu-id="7f248-202">供应商组、供应商国家或地区、供应商名称</span><span class="sxs-lookup"><span data-stu-id="7f248-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="7f248-203">产品</span><span class="sxs-lookup"><span data-stu-id="7f248-203">Products</span></span>               | <span data-ttu-id="7f248-204">产品编号、产品名称、物料组名称</span><span class="sxs-lookup"><span data-stu-id="7f248-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="7f248-205">采购类别</span><span class="sxs-lookup"><span data-stu-id="7f248-205">Procurement categories</span></span> | <span data-ttu-id="7f248-206">采购类别、采购类别名称</span><span class="sxs-lookup"><span data-stu-id="7f248-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="7f248-207">法人</span><span class="sxs-lookup"><span data-stu-id="7f248-207">Legal entities</span></span>         | <span data-ttu-id="7f248-208">法人姓名</span><span class="sxs-lookup"><span data-stu-id="7f248-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="7f248-209">日期</span><span class="sxs-lookup"><span data-stu-id="7f248-209">Dates</span></span>                  | <span data-ttu-id="7f248-210">日期、年偏移</span><span class="sxs-lookup"><span data-stu-id="7f248-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="7f248-211">默认情况下，此内容显示当前日历年的数据。</span><span class="sxs-lookup"><span data-stu-id="7f248-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="7f248-212">但是，您可以更改报表筛选器部分中的数据筛选器。</span><span class="sxs-lookup"><span data-stu-id="7f248-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="7f248-213">还可以更改公司筛选器。</span><span class="sxs-lookup"><span data-stu-id="7f248-213">You can also change the company filter.</span></span>

