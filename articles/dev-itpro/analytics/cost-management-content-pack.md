---
title: "成本管理 Power BI 内容"
description: "此主题介绍成本管理 Power BI 内容中的内容。"
author: ShylaThompson
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7d4a049a44374276655dce696b5bbbe2e6f9fba9
ms.openlocfilehash: f67b1c901267bdf79c94e4f4c698c8731c515bb4
ms.contentlocale: zh-cn
ms.lasthandoff: 09/12/2018

---

# <a name="cost-management-power-bi-content"></a><span data-ttu-id="3c43c-103">成本管理 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="3c43c-103">Cost management Power BI content</span></span>

[!include [banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="3c43c-104">概览</span><span class="sxs-lookup"><span data-stu-id="3c43c-104">Overview</span></span>

<span data-ttu-id="3c43c-105">**成本管理** Microsoft Power BI 内容面向库存核算师或负责库存或在制品 (WIP) 的状态或对此类状态感兴趣的个人，或负责分析标准成本差异或对此类差异感兴趣的人员。</span><span class="sxs-lookup"><span data-stu-id="3c43c-105">The **Cost management** Microsoft Power BI content is intended for inventory accountants or individuals in the organization who are responsible for or interested in the status of inventory or work in progress (WIP), or who are responsible for or interested in analyzing standard cost variances.</span></span>

> [!NOTE]
> <span data-ttu-id="3c43c-106">本主题中介绍的**成本管理** Power BI 内容适用于 Dynamics 365 for Finance and Operations 8.0。</span><span class="sxs-lookup"><span data-stu-id="3c43c-106">The **Cost management** Power BI content described in this this topic applies to Dynamics 365 for Finance and Operations 8.0.</span></span>
> 
> <span data-ttu-id="3c43c-107">已废弃了 AppSource 站点中的**成本管理** Power BI 内容包。</span><span class="sxs-lookup"><span data-stu-id="3c43c-107">The **Cost management** Power BI content pack, available on the AppSource site, has been deprecated.</span></span> <span data-ttu-id="3c43c-108">有关此项废弃的详细信息，请参阅 [AppSource 中的 Power BI 内容包](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource)。</span><span class="sxs-lookup"><span data-stu-id="3c43c-108">For more information about that deprecation, see [Power BI content packs available on AppSource](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).</span></span>

<span data-ttu-id="3c43c-109">此 Power BI 内容提供分类格式，帮助您监控库存性能，并显示库存中的成本分布。</span><span class="sxs-lookup"><span data-stu-id="3c43c-109">This Power BI content provides a categorized format that helps you monitor the performance of inventories and visualize how cost flows through them.</span></span> <span data-ttu-id="3c43c-110">您可获取管理见解，如周转率、现货库存天数，以及首选聚合级别的“ABC 分类”（公司、物料、物料组或站点）。</span><span class="sxs-lookup"><span data-stu-id="3c43c-110">You can gain managerial insights such as the turnover ratio, number of days that inventory is on hand, accuracy, and "ABC classification" at your preferred aggregated level (company, item, item group, or site).</span></span> <span data-ttu-id="3c43c-111">也可以将可用信息用作财务报表的详细补充。</span><span class="sxs-lookup"><span data-stu-id="3c43c-111">The information that is made available can also be used as a detailed supplement to the financial statement.</span></span>

<span data-ttu-id="3c43c-112">此 Power BI 内容基于 **CostObjectStatementCacheMonthly** 聚合度量构建，后者采用 **CostObjectStatementCache** 表充当主要数据源。</span><span class="sxs-lookup"><span data-stu-id="3c43c-112">The Power BI content is built on the **CostObjectStatementCacheMonthly** aggregated measurement, which has the **CostObjectStatementCache** table as its primary data source.</span></span> <span data-ttu-id="3c43c-113">此表由数据集高速缓存框架管理。</span><span class="sxs-lookup"><span data-stu-id="3c43c-113">This table is managed by the Data set cache framework.</span></span> <span data-ttu-id="3c43c-114">默认情况下，此表每隔 24 小时更新一次，但是您可以在数据集高速缓存配置中更改更新频率或启用手动更新。</span><span class="sxs-lookup"><span data-stu-id="3c43c-114">By default, the table is updated every 24 hours, but you can change the update frequency or enable manual updates in the configuration of the data set cache.</span></span> <span data-ttu-id="3c43c-115">可以在**成本管理**工作区或**成本分析**工作区中运行手动更新。</span><span class="sxs-lookup"><span data-stu-id="3c43c-115">Manual updates can be run in either the **Cost administration** workspace or the **Cost analysis** workspace.</span></span>

<span data-ttu-id="3c43c-116">每次更新 **CostObjectStatementCache** 表之后，必须先更新 **CostObjectStatementCacheMonthly** 聚合度量，再更新 Power BI 可视化中的数据。</span><span class="sxs-lookup"><span data-stu-id="3c43c-116">After every update of the **CostObjectStatementCache** table, the **CostObjectStatementCacheMonthly** aggregated measurement must updated before data in the Power BI visualizations is updated.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="3c43c-117">访问 Power BI 内容</span><span class="sxs-lookup"><span data-stu-id="3c43c-117">Accessing the Power BI content</span></span>

<span data-ttu-id="3c43c-118">**成本管理** Power BI 内容在**成本管理**和**成本分析**工作区中显示。</span><span class="sxs-lookup"><span data-stu-id="3c43c-118">The **Cost management** Power BI content is shown in the **Cost administration** and **Cost analysis** workspaces.</span></span>

<span data-ttu-id="3c43c-119">**成本管理**工作区中包含以下选项卡：</span><span class="sxs-lookup"><span data-stu-id="3c43c-119">The **Cost administration** workspace contains the following tabs:</span></span>

- <span data-ttu-id="3c43c-120">**概述** – 此选项卡显示应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="3c43c-120">**Overview** – This tab shows application data.</span></span>
- <span data-ttu-id="3c43c-121">**库存会计状态** – 此选项卡显示 Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="3c43c-121">**Inventory accounting status** – This tab shows Power BI content.</span></span>
- <span data-ttu-id="3c43c-122">**制造会计状态** – 此选项卡显示 Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="3c43c-122">**Manufacturing accounting status** – This tab shows Power BI content.</span></span>

<span data-ttu-id="3c43c-123">**成本分析**工作区中包含以下选项卡：</span><span class="sxs-lookup"><span data-stu-id="3c43c-123">The **Cost analysis** workspace contains the following tabs:</span></span>

- <span data-ttu-id="3c43c-124">**概述** – 此选项卡显示应用程序数据。</span><span class="sxs-lookup"><span data-stu-id="3c43c-124">**Overview** – This tab shows application data.</span></span>
- <span data-ttu-id="3c43c-125">**库存会计分析** – 此选项卡显示 Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="3c43c-125">**Inventory accounting analysis** – This tab shows Power BI content.</span></span>
- <span data-ttu-id="3c43c-126">**制造会计分析** – 此选项卡显示 Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="3c43c-126">**Manufacturing accounting analysis** – This tab shows Power BI content.</span></span>
- <span data-ttu-id="3c43c-127">**标准成本差异分析** – 此选项卡显示 Power BI 内容。</span><span class="sxs-lookup"><span data-stu-id="3c43c-127">**Std. cost variance analysis** – This tab shows Power BI content.</span></span>

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="3c43c-128">此 Power BI 内容中包含的报表页</span><span class="sxs-lookup"><span data-stu-id="3c43c-128">Report pages that are included in the Power BI content</span></span>

<span data-ttu-id="3c43c-129">**成本管理** Power BI 内容包括一组含有一组指标的报表页。</span><span class="sxs-lookup"><span data-stu-id="3c43c-129">The **Cost management** Power BI content includes a set of report pages that consist of a set of metrics.</span></span> <span data-ttu-id="3c43c-130">这些指标显示为图表、磁贴和表。</span><span class="sxs-lookup"><span data-stu-id="3c43c-130">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="3c43c-131">下面的表概要介绍**成本管理** Power BI 内容中的可视化。</span><span class="sxs-lookup"><span data-stu-id="3c43c-131">The following tables provide an overview of the visualizations in the **Cost management** Power BI content.</span></span>

### <a name="inventory-accounting-status"></a><span data-ttu-id="3c43c-132">库存会计状态</span><span class="sxs-lookup"><span data-stu-id="3c43c-132">Inventory accounting status</span></span>

| <span data-ttu-id="3c43c-133">报表页</span><span class="sxs-lookup"><span data-stu-id="3c43c-133">Report page</span></span>                               | <span data-ttu-id="3c43c-134">可视化</span><span class="sxs-lookup"><span data-stu-id="3c43c-134">Visualization</span></span>                                   |
|-------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="3c43c-135">库存概览</span><span class="sxs-lookup"><span data-stu-id="3c43c-135">Inventory overview</span></span>                        | <span data-ttu-id="3c43c-136">期初余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-136">Beginning balance</span></span>                               |
|                                           | <span data-ttu-id="3c43c-137">净改变</span><span class="sxs-lookup"><span data-stu-id="3c43c-137">Net change</span></span>                                      |
|                                           | <span data-ttu-id="3c43c-138">净改变百分比</span><span class="sxs-lookup"><span data-stu-id="3c43c-138">Net change %</span></span>                                    |
|                                           | <span data-ttu-id="3c43c-139">期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-139">Ending balance</span></span>                                  |
|                                           | <span data-ttu-id="3c43c-140">库存准确性</span><span class="sxs-lookup"><span data-stu-id="3c43c-140">Inventory accuracy</span></span>                              |
|                                           | <span data-ttu-id="3c43c-141">库存周转率</span><span class="sxs-lookup"><span data-stu-id="3c43c-141">Inventory turnover ratio</span></span>                        |
|                                           | <span data-ttu-id="3c43c-142">现货库存天数</span><span class="sxs-lookup"><span data-stu-id="3c43c-142">Days inventory on-hand</span></span>                          |
|                                           | <span data-ttu-id="3c43c-143">周期内的有效产品</span><span class="sxs-lookup"><span data-stu-id="3c43c-143">Active product in period</span></span>                        |
|                                           | <span data-ttu-id="3c43c-144">周期内的有效成本对象</span><span class="sxs-lookup"><span data-stu-id="3c43c-144">Active cost objects in period</span></span>                   |
|                                           | <span data-ttu-id="3c43c-145">按物料组分类的余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-145">Balance by item group</span></span>                           |
|                                           | <span data-ttu-id="3c43c-146">按站点分类的余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-146">Balance by site</span></span>                                 |
|                                           | <span data-ttu-id="3c43c-147">按类别分类的报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-147">Statement by category</span></span>                           |
|                                           | <span data-ttu-id="3c43c-148">按季度分类的净改变</span><span class="sxs-lookup"><span data-stu-id="3c43c-148">Net change by quarter</span></span>                           |
| <span data-ttu-id="3c43c-149">按站点和物料组分类的库存概览</span><span class="sxs-lookup"><span data-stu-id="3c43c-149">Inventory overview by site and item group</span></span> | <span data-ttu-id="3c43c-150">按站点分类的库存准确性</span><span class="sxs-lookup"><span data-stu-id="3c43c-150">Inventory accuracy by site</span></span>                      |
|                                           | <span data-ttu-id="3c43c-151">按站点分类的库存周转率</span><span class="sxs-lookup"><span data-stu-id="3c43c-151">Inventory turnover ratio by site</span></span>                |
|                                           | <span data-ttu-id="3c43c-152">按站点分类的库存期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-152">Inventory ending balance by site</span></span>                |
|                                           | <span data-ttu-id="3c43c-153">按物料组分类的库存准确性</span><span class="sxs-lookup"><span data-stu-id="3c43c-153">Inventory accuracy by item group</span></span>                |
|                                           | <span data-ttu-id="3c43c-154">按物料组分类的库存周转率</span><span class="sxs-lookup"><span data-stu-id="3c43c-154">Inventory turnover ratio by item group</span></span>          |
|                                           | <span data-ttu-id="3c43c-155">按站点和物料组分类的库存期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-155">Inventory ending balance by site and item group</span></span> |
| <span data-ttu-id="3c43c-156">库存报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-156">Inventory statement</span></span>                       | <span data-ttu-id="3c43c-157">库存报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-157">Inventory statement</span></span>                             |
| <span data-ttu-id="3c43c-158">按站点分类的库存报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-158">Inventory statement by site</span></span>               | <span data-ttu-id="3c43c-159">按站点分类的库存报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-159">Inventory statement by site</span></span>                     |
| <span data-ttu-id="3c43c-160">按产品层次结构分类的库存报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-160">Inventory statement by product hierarchy</span></span>  | <span data-ttu-id="3c43c-161">库存报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-161">Inventory statement</span></span>                             |
| <span data-ttu-id="3c43c-162">按产品层次结构分类的库存报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-162">Inventory statement by product hierarchy</span></span>  | <span data-ttu-id="3c43c-163">按站点分类的库存报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-163">Inventory statement by site</span></span>                     |

### <a name="manufacturing-accounting-status"></a><span data-ttu-id="3c43c-164">制造会计状态</span><span class="sxs-lookup"><span data-stu-id="3c43c-164">Manufacturing accounting status</span></span>

| <span data-ttu-id="3c43c-165">报表页</span><span class="sxs-lookup"><span data-stu-id="3c43c-165">Report page</span></span>                | <span data-ttu-id="3c43c-166">可视化</span><span class="sxs-lookup"><span data-stu-id="3c43c-166">Visualization</span></span>                       |
|----------------------------|-------------------------------------|
| <span data-ttu-id="3c43c-167">年初至今的 WIP 概览</span><span class="sxs-lookup"><span data-stu-id="3c43c-167">WIP overview YTD</span></span>           | <span data-ttu-id="3c43c-168">期初余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-168">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="3c43c-169">净改变</span><span class="sxs-lookup"><span data-stu-id="3c43c-169">Net change</span></span>                          |
|                            | <span data-ttu-id="3c43c-170">净改变百分比</span><span class="sxs-lookup"><span data-stu-id="3c43c-170">Net change %</span></span>                        |
|                            | <span data-ttu-id="3c43c-171">期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-171">Ending balance</span></span>                      |
|                            | <span data-ttu-id="3c43c-172">WIP 周转率</span><span class="sxs-lookup"><span data-stu-id="3c43c-172">WIP turnover ratio</span></span>                  |
|                            | <span data-ttu-id="3c43c-173">WIP 现货天数</span><span class="sxs-lookup"><span data-stu-id="3c43c-173">Days WIP on-hand</span></span>                    |
|                            | <span data-ttu-id="3c43c-174">周期内的有效成本对象</span><span class="sxs-lookup"><span data-stu-id="3c43c-174">Active cost object in period</span></span>        |
|                            | <span data-ttu-id="3c43c-175">按资源组分类的净改变</span><span class="sxs-lookup"><span data-stu-id="3c43c-175">Net change by resource group</span></span>        |
|                            | <span data-ttu-id="3c43c-176">按站点分类的余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-176">Balance by site</span></span>                     |
|                            | <span data-ttu-id="3c43c-177">按类别分类的报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-177">Statement by category</span></span>               |
|                            | <span data-ttu-id="3c43c-178">按季度分类的净改变</span><span class="sxs-lookup"><span data-stu-id="3c43c-178">Net change by quarter</span></span>               |
| <span data-ttu-id="3c43c-179">WIP statement / WIP 报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-179">WIP statement</span></span>              | <span data-ttu-id="3c43c-180">期初余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-180">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="3c43c-181">期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-181">Ending balance</span></span>                      |
|                            | <span data-ttu-id="3c43c-182">按类别分类的 WIP 报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-182">WIP statement by category</span></span>           |
| <span data-ttu-id="3c43c-183">按站点分类的 WIP 报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-183">WIP statement by site</span></span>      | <span data-ttu-id="3c43c-184">期初余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-184">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="3c43c-185">期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-185">Ending balance</span></span>                      |
|                            | <span data-ttu-id="3c43c-186">按类别和站点分类的 WIP 报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-186">WIP statement by category and site</span></span>  |
| <span data-ttu-id="3c43c-187">按层次结构分类的 WIP 报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-187">WIP statement by hierarchy</span></span> | <span data-ttu-id="3c43c-188">期初余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-188">Beginning balance</span></span>                   |
|                            | <span data-ttu-id="3c43c-189">期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-189">Ending balance</span></span>                      |
|                            | <span data-ttu-id="3c43c-190">按类别层次结构分类的 WIP 报表</span><span class="sxs-lookup"><span data-stu-id="3c43c-190">WIP statement by category hierarchy</span></span> |

### <a name="inventory-accounting-analysis"></a><span data-ttu-id="3c43c-191">库存会计分析</span><span class="sxs-lookup"><span data-stu-id="3c43c-191">Inventory accounting analysis</span></span>

| <span data-ttu-id="3c43c-192">报表页</span><span class="sxs-lookup"><span data-stu-id="3c43c-192">Report page</span></span>        | <span data-ttu-id="3c43c-193">可视化</span><span class="sxs-lookup"><span data-stu-id="3c43c-193">Visualization</span></span>                                                                |
|--------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="3c43c-194">库存详细信息</span><span class="sxs-lookup"><span data-stu-id="3c43c-194">Inventory details</span></span>  | <span data-ttu-id="3c43c-195">按期末余额分类的前 10 项资源</span><span class="sxs-lookup"><span data-stu-id="3c43c-195">Top 10 resources by ending balance</span></span>                                           |
|                    | <span data-ttu-id="3c43c-196">按净改变增加前 10 项资源</span><span class="sxs-lookup"><span data-stu-id="3c43c-196">Top 10 resources by net change increase</span></span>                                      |
|                    | <span data-ttu-id="3c43c-197">按净改变减小前 10 项资源</span><span class="sxs-lookup"><span data-stu-id="3c43c-197">Top 10 resources by net change decrease</span></span>                                      |
|                    | <span data-ttu-id="3c43c-198">按库存周转率分类的前 10 项资源</span><span class="sxs-lookup"><span data-stu-id="3c43c-198">Top 10 resources by inventory turnover ratio</span></span>                                 |
|                    | <span data-ttu-id="3c43c-199">按库存周转率和高于阈值的期末余额分类的资源</span><span class="sxs-lookup"><span data-stu-id="3c43c-199">Resources by low inventory turnover ratio and ending balance above threshold</span></span> |
|                    | <span data-ttu-id="3c43c-200">按低准确性分类的前 10 项资源</span><span class="sxs-lookup"><span data-stu-id="3c43c-200">Top 10 resources by low accuracy</span></span>                                             |
| <span data-ttu-id="3c43c-201">ABC 分类</span><span class="sxs-lookup"><span data-stu-id="3c43c-201">ABC classification</span></span> | <span data-ttu-id="3c43c-202">库存期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-202">Inventory ending balance</span></span>                                                     |
|                    | <span data-ttu-id="3c43c-203">已消耗的材料</span><span class="sxs-lookup"><span data-stu-id="3c43c-203">Consumed material</span></span>                                                            |
|                    | <span data-ttu-id="3c43c-204">已售(COGS)</span><span class="sxs-lookup"><span data-stu-id="3c43c-204">Sold (COGS)</span></span>                                                                  |
| <span data-ttu-id="3c43c-205">趋势库存</span><span class="sxs-lookup"><span data-stu-id="3c43c-205">Inventory trends</span></span>   | <span data-ttu-id="3c43c-206">库存期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-206">Inventory ending balance</span></span>                                                     |
|                    | <span data-ttu-id="3c43c-207">库存净更改</span><span class="sxs-lookup"><span data-stu-id="3c43c-207">Inventory net change</span></span>                                                         |
|                    | <span data-ttu-id="3c43c-208">库存周转率</span><span class="sxs-lookup"><span data-stu-id="3c43c-208">Inventory turnover ratio</span></span>                                                     |
|                    | <span data-ttu-id="3c43c-209">库存准确性</span><span class="sxs-lookup"><span data-stu-id="3c43c-209">Inventory accuracy</span></span>                                                           |

### <a name="manufacturing-accounting-analysis"></a><span data-ttu-id="3c43c-210">制造会计分析</span><span class="sxs-lookup"><span data-stu-id="3c43c-210">Manufacturing accounting analysis</span></span>

| <span data-ttu-id="3c43c-211">报表页</span><span class="sxs-lookup"><span data-stu-id="3c43c-211">Report page</span></span> | <span data-ttu-id="3c43c-212">可视化</span><span class="sxs-lookup"><span data-stu-id="3c43c-212">Visualization</span></span>      |
|-------------|--------------------|
| <span data-ttu-id="3c43c-213">WIP 趋势</span><span class="sxs-lookup"><span data-stu-id="3c43c-213">WIP trends</span></span>  | <span data-ttu-id="3c43c-214">WIP 期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-214">WIP ending balance</span></span> |
|             | <span data-ttu-id="3c43c-215">WIP 净改变</span><span class="sxs-lookup"><span data-stu-id="3c43c-215">WIP net change</span></span>     |
|             | <span data-ttu-id="3c43c-216">WIP 周转率</span><span class="sxs-lookup"><span data-stu-id="3c43c-216">WIP turnover ratio</span></span> |

### <a name="std-cost-variance-analysis"></a><span data-ttu-id="3c43c-217">标准成本差异分析</span><span class="sxs-lookup"><span data-stu-id="3c43c-217">Std. cost variance analysis</span></span>

| <span data-ttu-id="3c43c-218">报表页</span><span class="sxs-lookup"><span data-stu-id="3c43c-218">Report page</span></span>                             | <span data-ttu-id="3c43c-219">可视化</span><span class="sxs-lookup"><span data-stu-id="3c43c-219">Visualization</span></span>                                        |
|-----------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3c43c-220">年初至今的采购价差异（标准成本）</span><span class="sxs-lookup"><span data-stu-id="3c43c-220">Purchase price variance (Std. cost) YTD</span></span> | <span data-ttu-id="3c43c-221">已采购余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-221">Procured balance</span></span>                                     |
|                                         | <span data-ttu-id="3c43c-222">采购价差异</span><span class="sxs-lookup"><span data-stu-id="3c43c-222">Purchase price variance</span></span>                              |
|                                         | <span data-ttu-id="3c43c-223">采购价差异率</span><span class="sxs-lookup"><span data-stu-id="3c43c-223">Purchase price variance ratio</span></span>                        |
|                                         | <span data-ttu-id="3c43c-224">按物料组分类的差异</span><span class="sxs-lookup"><span data-stu-id="3c43c-224">Variance by item group</span></span>                               |
|                                         | <span data-ttu-id="3c43c-225">按站点分类的差异</span><span class="sxs-lookup"><span data-stu-id="3c43c-225">Variance by site</span></span>                                     |
|                                         | <span data-ttu-id="3c43c-226">按季节分类的采购价</span><span class="sxs-lookup"><span data-stu-id="3c43c-226">Purchase price by quarter</span></span>                            |
|                                         | <span data-ttu-id="3c43c-227">按季节和物料组分类的采购价</span><span class="sxs-lookup"><span data-stu-id="3c43c-227">Purchase price by quarter and Item group</span></span>             |
|                                         | <span data-ttu-id="3c43c-228">按不利采购价率分类的前 10 项资源</span><span class="sxs-lookup"><span data-stu-id="3c43c-228">Top 10 resources by unfavorable purchase price ratio</span></span> |
|                                         | <span data-ttu-id="3c43c-229">按有利采购价率分类的前 10 项资源</span><span class="sxs-lookup"><span data-stu-id="3c43c-229">Top 10 resources by favorable purchase price ratio</span></span>   |
| <span data-ttu-id="3c43c-230">年初至今的生产差异（标准成本）</span><span class="sxs-lookup"><span data-stu-id="3c43c-230">Production variance (Std. cost) YTD</span></span>     | <span data-ttu-id="3c43c-231">制造成本</span><span class="sxs-lookup"><span data-stu-id="3c43c-231">Manufactured cost</span></span>                                    |
|                                         | <span data-ttu-id="3c43c-232">生产差异</span><span class="sxs-lookup"><span data-stu-id="3c43c-232">Production variance</span></span>                                  |
|                                         | <span data-ttu-id="3c43c-233">生产差异率</span><span class="sxs-lookup"><span data-stu-id="3c43c-233">Production variance ratio</span></span>                            |
|                                         | <span data-ttu-id="3c43c-234">按物料组分类的差异</span><span class="sxs-lookup"><span data-stu-id="3c43c-234">Variance by item group</span></span>                               |
|                                         | <span data-ttu-id="3c43c-235">按站点分类的差异</span><span class="sxs-lookup"><span data-stu-id="3c43c-235">Variance by site</span></span>                                     |
|                                         | <span data-ttu-id="3c43c-236">按季节分类的生产差异</span><span class="sxs-lookup"><span data-stu-id="3c43c-236">Production variance by quarter</span></span>                       |
|                                         | <span data-ttu-id="3c43c-237">按季节和差异类型分类的生产差异</span><span class="sxs-lookup"><span data-stu-id="3c43c-237">Production variance by quarter and variance type</span></span>     |
|                                         | <span data-ttu-id="3c43c-238">按不利生产差异分类的前 10 项资源</span><span class="sxs-lookup"><span data-stu-id="3c43c-238">Top 10 resources by unfavorable production variance</span></span>  |
|                                         | <span data-ttu-id="3c43c-239">按有利生产差异分类的前 10 项资源</span><span class="sxs-lookup"><span data-stu-id="3c43c-239">Top 10 resources by favorable production variance</span></span>    |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="3c43c-240">了解数据模型和实体</span><span class="sxs-lookup"><span data-stu-id="3c43c-240">Understanding the data model and entities</span></span>

<span data-ttu-id="3c43c-241">将使用来自 Microsoft Dynamics 365 for Finance and Operations 的数据填充**成本管理** Power BI 内容中的报表页。</span><span class="sxs-lookup"><span data-stu-id="3c43c-241">Data from Microsoft Dynamics 365 for Finance and Operations is used to fill the report pages in the **Cost management** Power BI content.</span></span> <span data-ttu-id="3c43c-242">这些数据表示为实体商店（这是针对分析进行了优化的 Microsoft SQL Server 数据库）中暂存的聚合度量。</span><span class="sxs-lookup"><span data-stu-id="3c43c-242">This data is represented as aggregate measurements that are staged in the entity store, which is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="3c43c-243">有关详细信息，请参阅 [Power BI 与实体商店集成](power-bi-integration-entity-store.md)。</span><span class="sxs-lookup"><span data-stu-id="3c43c-243">For more information, see [Power BI integration with entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="3c43c-244">以下对象的关键聚合度量用作 Power BI 内容的基础。</span><span class="sxs-lookup"><span data-stu-id="3c43c-244">The key aggregate measurements of the following objects are used as the basis of the Power BI content.</span></span>

| <span data-ttu-id="3c43c-245">对象</span><span class="sxs-lookup"><span data-stu-id="3c43c-245">Object</span></span>                          | <span data-ttu-id="3c43c-246">关键聚合度量</span><span class="sxs-lookup"><span data-stu-id="3c43c-246">Key aggregate measurements</span></span> | <span data-ttu-id="3c43c-247">Finance and Operations 的数据源</span><span class="sxs-lookup"><span data-stu-id="3c43c-247">Data source for Finance and Operations</span></span> | <span data-ttu-id="3c43c-248">字段</span><span class="sxs-lookup"><span data-stu-id="3c43c-248">Field</span></span>               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| <span data-ttu-id="3c43c-249">CostObjectStatementCacheMonthly</span><span class="sxs-lookup"><span data-stu-id="3c43c-249">CostObjectStatementCacheMonthly</span></span> | <span data-ttu-id="3c43c-250">时长</span><span class="sxs-lookup"><span data-stu-id="3c43c-250">Amount</span></span>                     | <span data-ttu-id="3c43c-251">CostObjectStatementCache</span><span class="sxs-lookup"><span data-stu-id="3c43c-251">CostObjectStatementCache</span></span>               | <span data-ttu-id="3c43c-252">时长</span><span class="sxs-lookup"><span data-stu-id="3c43c-252">Amount</span></span>              |
| <span data-ttu-id="3c43c-253">CostObjectStatementCacheMonthly</span><span class="sxs-lookup"><span data-stu-id="3c43c-253">CostObjectStatementCacheMonthly</span></span> | <span data-ttu-id="3c43c-254">数量</span><span class="sxs-lookup"><span data-stu-id="3c43c-254">Quantity</span></span>                   | <span data-ttu-id="3c43c-255">CostObjectStatementCache</span><span class="sxs-lookup"><span data-stu-id="3c43c-255">CostObjectStatementCache</span></span>               | <span data-ttu-id="3c43c-256">数量</span><span class="sxs-lookup"><span data-stu-id="3c43c-256">Qty</span></span>                 |
| <span data-ttu-id="3c43c-257">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="3c43c-257">CostInventoryAccountingKPIGoal</span></span>  | <span data-ttu-id="3c43c-258">AnnualInventoryTurn</span><span class="sxs-lookup"><span data-stu-id="3c43c-258">AnnualInventoryTurn</span></span>        | <span data-ttu-id="3c43c-259">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="3c43c-259">CostInventoryAccountingKPIGoal</span></span>         | <span data-ttu-id="3c43c-260">AnnualInventoryTurn</span><span class="sxs-lookup"><span data-stu-id="3c43c-260">AnnualInventoryTurn</span></span> |
| <span data-ttu-id="3c43c-261">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="3c43c-261">CostInventoryAccountingKPIGoal</span></span>  | <span data-ttu-id="3c43c-262">InventoryAccuracy</span><span class="sxs-lookup"><span data-stu-id="3c43c-262">InventoryAccuracy</span></span>          | <span data-ttu-id="3c43c-263">CostInventoryAccountingKPIGoal</span><span class="sxs-lookup"><span data-stu-id="3c43c-263">CostInventoryAccountingKPIGoal</span></span>         | <span data-ttu-id="3c43c-264">InventoryAccuracy</span><span class="sxs-lookup"><span data-stu-id="3c43c-264">InventoryAccuracy</span></span>   |

<span data-ttu-id="3c43c-265">下表显示 Power BI content 中的关键计算度量。</span><span class="sxs-lookup"><span data-stu-id="3c43c-265">The following table shows the key calculated measurements in the Power BI content.</span></span>

| <span data-ttu-id="3c43c-266">度量</span><span class="sxs-lookup"><span data-stu-id="3c43c-266">Measure</span></span>                            | <span data-ttu-id="3c43c-267">计算</span><span class="sxs-lookup"><span data-stu-id="3c43c-267">Calculation</span></span> |
|------------------------------------|-------------|
| <span data-ttu-id="3c43c-268">期初余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-268">Beginning balance</span></span>                  | <span data-ttu-id="3c43c-269">期初余额 = \[期末余额\]-\[净改变\]</span><span class="sxs-lookup"><span data-stu-id="3c43c-269">Beginning balance = \[Ending balance\]-\[Net change\]</span></span> |
| <span data-ttu-id="3c43c-270">期初余额数量</span><span class="sxs-lookup"><span data-stu-id="3c43c-270">Beginning balance qty.</span></span>             | <span data-ttu-id="3c43c-271">期初余额数量 = \[期末余额数量\]-\[净改变数量\]</span><span class="sxs-lookup"><span data-stu-id="3c43c-271">Beginning balance qty. = \[Ending balance qty.\]-\[Net change qty.\]</span></span> |
| <span data-ttu-id="3c43c-272">期末余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-272">Ending balance</span></span>                     | <span data-ttu-id="3c43c-273">期末余额 = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))))</span><span class="sxs-lookup"><span data-stu-id="3c43c-273">Ending balance = (CALCULATE(SUM(\[Amount\]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\]))))</span></span> |
| <span data-ttu-id="3c43c-274">期末余额数量</span><span class="sxs-lookup"><span data-stu-id="3c43c-274">Ending balance qty.</span></span>                | <span data-ttu-id="3c43c-275">期末余额数量 = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))</span><span class="sxs-lookup"><span data-stu-id="3c43c-275">Ending balance qty. = CALCULATE(SUM(\[QTY\]), FILTER(ALL(FiscalCalendar),FiscalCalendar\[MONTHSTARTDATE\] \<= MAX(FiscalCalendar\[MONTHSTARTDATE\])))</span></span> |
| <span data-ttu-id="3c43c-276">净改变</span><span class="sxs-lookup"><span data-stu-id="3c43c-276">Net change</span></span>                         | <span data-ttu-id="3c43c-277">净改变 = SUM(\[AMOUNT\])</span><span class="sxs-lookup"><span data-stu-id="3c43c-277">Net change = SUM(\[AMOUNT\])</span></span> |
| <span data-ttu-id="3c43c-278">净改变数量</span><span class="sxs-lookup"><span data-stu-id="3c43c-278">Net change qty.</span></span>                    | <span data-ttu-id="3c43c-279">净改变数量 = SUM(\[QTY\])</span><span class="sxs-lookup"><span data-stu-id="3c43c-279">Net change qty. = SUM(\[QTY\])</span></span> |
| <span data-ttu-id="3c43c-280">按金额分类的库存周转率</span><span class="sxs-lookup"><span data-stu-id="3c43c-280">Inventory turnover ratio by amount</span></span> | <span data-ttu-id="3c43c-281">按金额分类的库存周转率 = if(OR(\[Inventory average balance\] \<= 0, \[Inventory sold or consumed issues\] \>= 0), 0, ABS(\[Inventory sold or consumed issues\])/\[Inventory average balance\])</span><span class="sxs-lookup"><span data-stu-id="3c43c-281">Inventory turnover ratio by amount = if(OR(\[Inventory average balance\] \<= 0, \[Inventory sold or consumed issues\] \>= 0), 0, ABS(\[Inventory sold or consumed issues\])/\[Inventory average balance\])</span></span> |
| <span data-ttu-id="3c43c-282">库存平均余额</span><span class="sxs-lookup"><span data-stu-id="3c43c-282">Inventory average balance</span></span>          | <span data-ttu-id="3c43c-283">库存平均余额 = ((\[期末余额\] + \[期初余额\]) / 2)</span><span class="sxs-lookup"><span data-stu-id="3c43c-283">Inventory average balance = ((\[Ending balance\] + \[Beginning balance\]) / 2)</span></span> |
| <span data-ttu-id="3c43c-284">现货库存天数</span><span class="sxs-lookup"><span data-stu-id="3c43c-284">Days inventory on-hand</span></span>             | <span data-ttu-id="3c43c-285">现货库存天数 = 365 / CostObjectStatementEntries\[Inventory turnover ratio by amount\]</span><span class="sxs-lookup"><span data-stu-id="3c43c-285">Days inventory onhand = 365 / CostObjectStatementEntries\[Inventory turnover ratio by amount\]</span></span> |
| <span data-ttu-id="3c43c-286">库存准确性</span><span class="sxs-lookup"><span data-stu-id="3c43c-286">Inventory accuracy</span></span>                 | <span data-ttu-id="3c43c-287">按金额的库存准确性 = IF(\[Ending balance\] \<= 0, IF(OR(\[Inventory counted amount\] \<\> 0, \[Ending balance\] \< 0), 0, 1), MAX(0, (\[Ending balance\] - ABS(\[Inventory counted amount\]))/\[Ending balance\]))</span><span class="sxs-lookup"><span data-stu-id="3c43c-287">Inventory accuracy by amount = IF(\[Ending balance\] \<= 0, IF(OR(\[Inventory counted amount\] \<\> 0, \[Ending balance\] \< 0), 0, 1), MAX(0, (\[Ending balance\] - ABS(\[Inventory counted amount\]))/\[Ending balance\]))</span></span> |

<span data-ttu-id="3c43c-288">以下关键维度用作筛选器以切分聚合度量，以便获得粒度更细微，更深入的分析洞察。</span><span class="sxs-lookup"><span data-stu-id="3c43c-288">The following key dimensions are used as filters to slice the aggregate measurements, so that you can achieve greater granularity and gain deeper analytical insights.</span></span>


| <span data-ttu-id="3c43c-289">实体</span><span class="sxs-lookup"><span data-stu-id="3c43c-289">Entity</span></span>                                                  | <span data-ttu-id="3c43c-290">属性示例</span><span class="sxs-lookup"><span data-stu-id="3c43c-290">Examples of attributes</span></span>                          |
|---------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="3c43c-291">产品</span><span class="sxs-lookup"><span data-stu-id="3c43c-291">Products</span></span>                                                | <span data-ttu-id="3c43c-292">产品编号、产品名称、单位、物料组</span><span class="sxs-lookup"><span data-stu-id="3c43c-292">Product number, Product name, Unit, Item groups</span></span> |
| <span data-ttu-id="3c43c-293">类别层次结构（已分配给角色成本管理）</span><span class="sxs-lookup"><span data-stu-id="3c43c-293">Category hierarchies (Assigned to role Cost management)</span></span> | <span data-ttu-id="3c43c-294">类别层次结构，类别级别</span><span class="sxs-lookup"><span data-stu-id="3c43c-294">Category hierarchy, Category level</span></span>              |
| <span data-ttu-id="3c43c-295">法人</span><span class="sxs-lookup"><span data-stu-id="3c43c-295">Legal entities</span></span>                                          | <span data-ttu-id="3c43c-296">法人名称</span><span class="sxs-lookup"><span data-stu-id="3c43c-296">Legal entity names</span></span>                              |
| <span data-ttu-id="3c43c-297">会计日历</span><span class="sxs-lookup"><span data-stu-id="3c43c-297">Fiscal calendars</span></span>                                        | <span data-ttu-id="3c43c-298">会计日历、年、季度、期间、月</span><span class="sxs-lookup"><span data-stu-id="3c43c-298">Fiscal calendar, Year, Quarter, Period, Month</span></span>   |
| <span data-ttu-id="3c43c-299">站点</span><span class="sxs-lookup"><span data-stu-id="3c43c-299">Site</span></span>                                                    | <span data-ttu-id="3c43c-300">ID、名称、地址、省/市/自治区、国家/地区</span><span class="sxs-lookup"><span data-stu-id="3c43c-300">ID, Name, Address, State, Country</span></span>               |

