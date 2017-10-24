---
title: "对基准预测进行手动调整"
description: "本文介绍如何手动调整基准预测和查看预测的详细信息。"
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 218374cdb6b5588648422d97c04fb60f26e47ac7
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="eff42-103">对基准预测进行手动调整</span><span class="sxs-lookup"><span data-stu-id="eff42-103">Make manual adjustments to the baseline forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="eff42-104">本文介绍如何手动调整基准预测和查看预测的详细信息。</span><span class="sxs-lookup"><span data-stu-id="eff42-104">This article explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="eff42-105">在进行手动调整之前，务需您理解各个页上的若干概念。</span><span class="sxs-lookup"><span data-stu-id="eff42-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="eff42-106">“调整后的需求预测”页上的网格</span><span class="sxs-lookup"><span data-stu-id="eff42-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="eff42-107">**调整后的需求预测**页包括具有以下结构的网格：</span><span class="sxs-lookup"><span data-stu-id="eff42-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="eff42-108">第一列显示为其生成预测的物料、物料分配参数、公司等。</span><span class="sxs-lookup"><span data-stu-id="eff42-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="eff42-109">该页的副标题提供在网格中显示的当前预测维度的描述。</span><span class="sxs-lookup"><span data-stu-id="eff42-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="eff42-110">例如，如果该页的副标题是**公司/站点/物料分配参数**，且网格中的行标题是 **USMF / 1 / D\_Alloc**，则该行显示 USMF 公司的预测、站点 1 和 **D\_Alloc** 物料分配参数。</span><span class="sxs-lookup"><span data-stu-id="eff42-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="eff42-111">随后的列表示为其生成预测的预测时段。</span><span class="sxs-lookup"><span data-stu-id="eff42-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="eff42-112">每一列标题是列显示的预测时段的第一个日期。</span><span class="sxs-lookup"><span data-stu-id="eff42-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="eff42-113">这些单元格中的值表示该特定预测时段的一个物料的预测、物料分配参数等。</span><span class="sxs-lookup"><span data-stu-id="eff42-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-deaggregation"></a><span data-ttu-id="eff42-114">预测合并和取消合并</span><span class="sxs-lookup"><span data-stu-id="eff42-114">Forecast aggregation and deaggregation</span></span>
<span data-ttu-id="eff42-115">该页的副标题显示预测合并的级别。</span><span class="sxs-lookup"><span data-stu-id="eff42-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="eff42-116">例如，如果页的副标题是**公司/站点/分配参数/物料编号/颜色/尺寸/配置/样式**，则没有预测合并，并且预测在物料及其维度级别显示。</span><span class="sxs-lookup"><span data-stu-id="eff42-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="eff42-117">若要更改合并，请使用**更改预测维度**页，可以从应用程序菜单打开。</span><span class="sxs-lookup"><span data-stu-id="eff42-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="eff42-118">若要修改预测，单击可用的任何单元格，并键入已调整的预测值。</span><span class="sxs-lookup"><span data-stu-id="eff42-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="eff42-119">编辑后的单元格将立即变为粗体，指示它显示的预测不是需求预测服务创建的预测，不过已进行手动调整。</span><span class="sxs-lookup"><span data-stu-id="eff42-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="eff42-120">如果您更改合并以使页显示更多聚合数据，可以使用**需求预测行**页查看构成聚合预测的单独预测行。</span><span class="sxs-lookup"><span data-stu-id="eff42-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="eff42-121">例如，您在物料级别生成了预测，不过，您知道由于促销或其他类似的事件，此物料的需求在所有站点都将增加。</span><span class="sxs-lookup"><span data-stu-id="eff42-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="eff42-122">在这种情况下，您可以在**更改预测维度**页设置合并为**公司/物料分配参数/物料**。</span><span class="sxs-lookup"><span data-stu-id="eff42-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="eff42-123">您可以为在**调整后的需求预测**网格中的所有站点的物料调整全局预测。</span><span class="sxs-lookup"><span data-stu-id="eff42-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="eff42-124">若要查看跨所有站点的更改的效果，请打开**需求预测行**页。</span><span class="sxs-lookup"><span data-stu-id="eff42-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="eff42-125">在此页，您将看到每个站点的物料、经调整的预测数量和原始预测数量在一行。</span><span class="sxs-lookup"><span data-stu-id="eff42-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="eff42-126">在聚合级别进行预测数量调整时，M此系统使用加权分配在创建合并的行中分配更改。</span><span class="sxs-lookup"><span data-stu-id="eff42-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="eff42-127">您还可以在**需求预测行**页进行手动调整，方法是通过修改取消合并网格中的**总数量**值或**数量**单元格。</span><span class="sxs-lookup"><span data-stu-id="eff42-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="eff42-128">查看预测详细信息</span><span class="sxs-lookup"><span data-stu-id="eff42-128">Viewing details of the forecast</span></span>
<span data-ttu-id="eff42-129">您可以打开**需求预测详细信息**页查看有关预测的更多信息。</span><span class="sxs-lookup"><span data-stu-id="eff42-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="eff42-130">**需求预测详细信息**页以图形和表格式显示以下信息：</span><span class="sxs-lookup"><span data-stu-id="eff42-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="eff42-131">预测所基于的历史需求。</span><span class="sxs-lookup"><span data-stu-id="eff42-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="eff42-132">主计划使用的当前预测。</span><span class="sxs-lookup"><span data-stu-id="eff42-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="eff42-133">新的需求预测值和按其手动调整的金额。</span><span class="sxs-lookup"><span data-stu-id="eff42-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="eff42-134">预测值的置信区间。</span><span class="sxs-lookup"><span data-stu-id="eff42-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="eff42-135">用于生成预测的预测模型。</span><span class="sxs-lookup"><span data-stu-id="eff42-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="eff42-136">如果您正在查看聚合数据，您将看到用于所有聚合时间系列的所有方法的列表。</span><span class="sxs-lookup"><span data-stu-id="eff42-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="eff42-137">内部模型准确性 (MAPE)。</span><span class="sxs-lookup"><span data-stu-id="eff42-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="eff42-138">有关预测准确性的详细信息，请参阅[监控预测准确性](monitor-forecast-accuracy.md)。</span><span class="sxs-lookup"><span data-stu-id="eff42-138">For more information about forecast accuracy, see [Monitoring forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="eff42-139">**注意：**</span><span class="sxs-lookup"><span data-stu-id="eff42-139">**Notes:**</span></span>

-   <span data-ttu-id="eff42-140">显示在该页的**预测**部分中的置信区间表示置信区间上限和置信区间下限之间的差异。</span><span class="sxs-lookup"><span data-stu-id="eff42-140">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="eff42-141">要查看上限和下限的值，将鼠标悬停在**以图形方式表示的历史需求和预测**部分的图表上。</span><span class="sxs-lookup"><span data-stu-id="eff42-141">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="eff42-142">如果您使用 Finance and Operations 需求预测 Microsoft Azure 机器学习服务，您可以指定生成的预测应具有的可信度百分比。</span><span class="sxs-lookup"><span data-stu-id="eff42-142">If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="eff42-143">置信区间包含一系列用作良好的需求预测估计的值。</span><span class="sxs-lookup"><span data-stu-id="eff42-143">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="eff42-144">可信度百分比 95% 表示需求预测有 5% 的几率超出置信区间范围。</span><span class="sxs-lookup"><span data-stu-id="eff42-144">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="eff42-145">您还可以手动调整**需求预测详细信息**页上的预测，方法是通过修改**预测**部分的**预测**行中的值。</span><span class="sxs-lookup"><span data-stu-id="eff42-145">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="see-also"></a><span data-ttu-id="eff42-146">请参阅</span><span class="sxs-lookup"><span data-stu-id="eff42-146">See also</span></span>
--------

[<span data-ttu-id="eff42-147">监控预测准确性</span><span class="sxs-lookup"><span data-stu-id="eff42-147">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="eff42-148">生成统计基准预测</span><span class="sxs-lookup"><span data-stu-id="eff42-148">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)



