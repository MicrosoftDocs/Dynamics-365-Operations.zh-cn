---
title: "用于作业级排产的甘特图"
description: "甘特图旨在授权生产规划人员控制和优化生产计划。 甘特图使操作流透明，且易于在考虑材料或资源短缺的情况下调整生产计划。 这有助于规划人员最佳地利用可用资源、尽量减少在制品和优化生产订单的吞吐时间。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: johanhoffmann
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 71c95adbfe48c313bb0bfb23ada2cb69433bf0e1
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="gantt-chart-for-job-scheduling"></a><span data-ttu-id="b16e3-106">用于作业级排产的甘特图</span><span class="sxs-lookup"><span data-stu-id="b16e3-106">Gantt chart for job scheduling</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b16e3-107">甘特图旨在授权生产规划人员控制和优化生产计划。</span><span class="sxs-lookup"><span data-stu-id="b16e3-107">The Gantt chart is designed to empower production planners to control and optimize the production plan.</span></span> <span data-ttu-id="b16e3-108">甘特图使操作流透明，且易于在考虑材料或资源短缺的情况下调整生产计划。</span><span class="sxs-lookup"><span data-stu-id="b16e3-108">The Gantt chart makes the flow of operations transparent and makes it easy to adjust the production schedule while taking into account material or resource shortages.</span></span> <span data-ttu-id="b16e3-109">这有助于规划人员最佳地利用可用资源、尽量减少在制品和优化生产订单的吞吐时间。</span><span class="sxs-lookup"><span data-stu-id="b16e3-109">This helps planners make the best use of available resources, minimize work in progress, and optimize throughput times for production orders.</span></span>

<span data-ttu-id="b16e3-110">甘特图旨在授权生产规划人员控制和优化生产计划。</span><span class="sxs-lookup"><span data-stu-id="b16e3-110">The Gantt chart is designed to empower production planners to control and optimize the production plan.</span></span> <span data-ttu-id="b16e3-111">甘特图使操作流透明，且易于在考虑材料或资源短缺的情况下调整生产计划。</span><span class="sxs-lookup"><span data-stu-id="b16e3-111">The Gantt chart makes the flow of operations transparent and makes it easy to adjust the production schedule while taking into account material or resource shortages.</span></span> <span data-ttu-id="b16e3-112">这有助于规划人员最佳地利用可用资源、尽量减少在制品和优化生产订单的吞吐时间。</span><span class="sxs-lookup"><span data-stu-id="b16e3-112">This helps planners make the best use of available resources, minimize work in progress, and optimize throughput times for production orders.</span></span>

<span data-ttu-id="b16e3-113">甘特图是在定义的时间间隔内的已计划活动的视觉表现形式。</span><span class="sxs-lookup"><span data-stu-id="b16e3-113">A Gantt chart is a visual representation of scheduled activities within a defined time interval.</span></span> <span data-ttu-id="b16e3-114">活动基于具有由产能日历定义的产能的资源进行计划。</span><span class="sxs-lookup"><span data-stu-id="b16e3-114">The activities are scheduled on resources that have capacity defined by a capacity calendar.</span></span> <span data-ttu-id="b16e3-115">甘特图中可以显示以下类型的活动。</span><span class="sxs-lookup"><span data-stu-id="b16e3-115">The following types of activities can be shown in the Gantt chart.</span></span>

-   <span data-ttu-id="b16e3-116">来自生产订单的已计划作业的作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-116">Jobs from production orders that are job scheduled.</span></span>
-   <span data-ttu-id="b16e3-117">来自计划生产订单的作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-117">Jobs from planned production orders.</span></span>
-   <span data-ttu-id="b16e3-118">工时预测类型的作业已计划项目活动。</span><span class="sxs-lookup"><span data-stu-id="b16e3-118">Job scheduled project activities of type Hour forecasts.</span></span>

<span data-ttu-id="b16e3-119">甘特图可以在两种不同的视图中打开，**订单视图**和**资源视图**[。](https://authoring.help.dynamics.com/en/?post_type=incsub_wiki&p=1665154&preview=true)在**订单**中，活动按照生产订单进行分组。</span><span class="sxs-lookup"><span data-stu-id="b16e3-119">The Gantt chart can be opened in two different views, **Order view** and **Resource view**[.](https://authoring.help.dynamics.com/en/?post_type=incsub_wiki&p=1665154&preview=true)In **Order view**, activities are grouped under production orders.</span></span> <span data-ttu-id="b16e3-120">这非常实用，例如，如果您要维护属于相同订单的所有作业的概览时。</span><span class="sxs-lookup"><span data-stu-id="b16e3-120">This can be useful, for example, if you want to maintain an overview of all the jobs belonging to the same orders.</span></span> <span data-ttu-id="b16e3-121">在**资源视图**中，所有作业按照单独的资源进行分组。</span><span class="sxs-lookup"><span data-stu-id="b16e3-121">In **Resource view** all jobs are grouped under individual resources.</span></span> <span data-ttu-id="b16e3-122">优化资源级别（例如机器或机器组）的计划时，此视图非常实用。</span><span class="sxs-lookup"><span data-stu-id="b16e3-122">This view can be useful when optimizing the plan at a resource level, for example, a machine or a group of machines.</span></span> <span data-ttu-id="b16e3-123">下图显示的甘特图显示具有以下关键元素的**订单视图**和**资源视图**：</span><span class="sxs-lookup"><span data-stu-id="b16e3-123">The Gantt charts shown in the illustrations below show **Order view** and **Resource view** with these key elements:</span></span>

1.  <span data-ttu-id="b16e3-124">甘特图活动</span><span class="sxs-lookup"><span data-stu-id="b16e3-124">Gantt chart activity</span></span>
2.  <span data-ttu-id="b16e3-125">物料短缺图标</span><span class="sxs-lookup"><span data-stu-id="b16e3-125">Material shortage icon</span></span>
3.  <span data-ttu-id="b16e3-126">物料可用性图标</span><span class="sxs-lookup"><span data-stu-id="b16e3-126">Material availability icon</span></span>
4.  <span data-ttu-id="b16e3-127">订单交货日期图标</span><span class="sxs-lookup"><span data-stu-id="b16e3-127">Order delivery date icon</span></span>
5.  <span data-ttu-id="b16e3-128">产能条</span><span class="sxs-lookup"><span data-stu-id="b16e3-128">Capacity bar</span></span>

## <a name="order-view"></a><span data-ttu-id="b16e3-129">订单视图</span><span class="sxs-lookup"><span data-stu-id="b16e3-129">Order view</span></span>

<span data-ttu-id="b16e3-130">[![概览](./media/orderview.png)](./media/orderview.png)</span><span class="sxs-lookup"><span data-stu-id="b16e3-130">[![orderview](./media/orderview.png)](./media/orderview.png)</span></span>

## <a name="resource-view"></a><span data-ttu-id="b16e3-131">资源视图</span><span class="sxs-lookup"><span data-stu-id="b16e3-131">Resource view</span></span>
<span data-ttu-id="b16e3-132">[![审核](./media/resview.png)](./media/resview.png)</span><span class="sxs-lookup"><span data-stu-id="b16e3-132">[![resview](./media/resview.png)](./media/resview.png)</span></span>

## <a name="activities"></a><span data-ttu-id="b16e3-133">活动</span><span class="sxs-lookup"><span data-stu-id="b16e3-133">Activities</span></span>
<span data-ttu-id="b16e3-134">这些活动显示为条形，并且以具有计划开始和结束时间的时间刻度网格进行整理，使得条形长度与完成该活动所需的时间成比例。</span><span class="sxs-lookup"><span data-stu-id="b16e3-134">The activities appear as bars and are organized in a time scale grid with a scheduled start and end time, making the length of the bars proportional to the time that is necessary to complete the activity.</span></span> <span data-ttu-id="b16e3-135">这些活动根据时间刻度进行显示。</span><span class="sxs-lookup"><span data-stu-id="b16e3-135">The activities are shown according to a time scale.</span></span> <span data-ttu-id="b16e3-136">您可以调整您选择开始和结束日期和时间单位（例如小时或天数）的菜单上的时间刻度。</span><span class="sxs-lookup"><span data-stu-id="b16e3-136">You can adjust the time scale on the menu where you select a start and end date and a time unit, for example, hours or days.</span></span> <span data-ttu-id="b16e3-137">通过调整时间刻度可以设置您要管理活动的时间间隔的焦点。</span><span class="sxs-lookup"><span data-stu-id="b16e3-137">By adjusting the time scale you can set focus on a time interval in which you want to manage activities.</span></span> 

<span data-ttu-id="b16e3-138">要获得更清晰的概览，提供了用于控制活动颜色的不同选项。</span><span class="sxs-lookup"><span data-stu-id="b16e3-138">To get a better overview, there are different options for controlling the color of the activities.</span></span> <span data-ttu-id="b16e3-139">您可以为活动配置单独的颜色，使用用于应用的一般颜色主题的主题颜色，或将颜色设置为由生产订单的颜色代码控制。</span><span class="sxs-lookup"><span data-stu-id="b16e3-139">You can configure an individual color for activities, use the theme color that is the general color theme used for the application, or set up the color to be controlled by the color code for production orders.</span></span> 

<span data-ttu-id="b16e3-140">活动的时间间隔具有背景阴影。</span><span class="sxs-lookup"><span data-stu-id="b16e3-140">The time interval for activities has a background shade.</span></span> <span data-ttu-id="b16e3-141">具有白色阴影的期间表示对用于活动的资源定义了产能的时间间隔，而具有灰色阴影的期间表示未定义产能的时间间隔。</span><span class="sxs-lookup"><span data-stu-id="b16e3-141">Periods with a white shade indicate a time interval with defined capacity on the resource for the activity, whereas periods with a grey shade indicate time intervals with no capacity defined.</span></span> 

<span data-ttu-id="b16e3-142">在图表的左侧提供了关于活动的额外信息，例如，计划了活动的资源和生产订单编号。</span><span class="sxs-lookup"><span data-stu-id="b16e3-142">On the left side of the chart there is additional information about the activity, for example, the resource on which the activity is scheduled and production order number.</span></span> <span data-ttu-id="b16e3-143">属于同一订单的作业之间的关联使用箭头显示。</span><span class="sxs-lookup"><span data-stu-id="b16e3-143">The connection between jobs belonging to the same order is shown with an arrow.</span></span> 

<span data-ttu-id="b16e3-144">您可以在活动对话框中获取有关活动的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b16e3-144">You can get more information about an activity in the activity dialog box.</span></span> <span data-ttu-id="b16e3-145">要打开对话框，请双击活动或选择**信息**菜单。</span><span class="sxs-lookup"><span data-stu-id="b16e3-145">To open the dialog box, double-click the activity or select the **information** menu.</span></span> <span data-ttu-id="b16e3-146">在活动对话框中可以查看计划的开始和结束日期，以及关于活动计划使用哪些物料的时间信息。</span><span class="sxs-lookup"><span data-stu-id="b16e3-146">In the activity dialog you can see the scheduled start and end date, and time information about which materials the activity is planned to consume.</span></span> 

<span data-ttu-id="b16e3-147">活动可以在分组级别进行分组。</span><span class="sxs-lookup"><span data-stu-id="b16e3-147">The activities can be grouped in Grouping levels.</span></span> <span data-ttu-id="b16e3-148">分组级别为层次结构，可以用来对活动进行逻辑分组。</span><span class="sxs-lookup"><span data-stu-id="b16e3-148">The Grouping levels are hierarchical and can be used to make a logical grouping of activities.</span></span> <span data-ttu-id="b16e3-149">例如，如果您的布局是按照站点、生产单位、资源组和资源对制造活动进行分组，您可以使用分组级别按照该布局对活动进行分组。</span><span class="sxs-lookup"><span data-stu-id="b16e3-149">For example, if you have a layout where manufacturing activities are grouped by Site, Production units, Resource groups, and Resources, you can use the Grouping levels to group the activities according to that layout.</span></span> <span data-ttu-id="b16e3-150">使用菜单上的**全部展开**和**全部折叠**可以在图表中的单个分组级别或对所有级别展开和折叠分组级别。</span><span class="sxs-lookup"><span data-stu-id="b16e3-150">The grouping levels can be expanded and collapsed either on the individual grouping level or for all levels in the chart by using the **Expand all** and **Collapse all** buttons on the menu.</span></span> <span data-ttu-id="b16e3-151">您还可以将分组级别配置为在打开图表时展开或折叠分组级别。</span><span class="sxs-lookup"><span data-stu-id="b16e3-151">You can also configure the grouping levels to be expanded or collapsed when the chart is opened.</span></span>

### <a name="material-availability"></a><span data-ttu-id="b16e3-152">材料可用性</span><span class="sxs-lookup"><span data-stu-id="b16e3-152">Material availability</span></span>

<span data-ttu-id="b16e3-153">可以设置甘特图以向规划人员提供关于单个活动物料状态的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b16e3-153">The Gantt chart can be set up to provide the planner with detailed information about material status for the individual activities.</span></span> <span data-ttu-id="b16e3-154">例如，如果物料被延误且影响生产计划，这可能很有用。</span><span class="sxs-lookup"><span data-stu-id="b16e3-154">For example, this can be helpful if material is delayed and is affecting the production plan.</span></span> <span data-ttu-id="b16e3-155">在这种情况下，将在甘特图中突出显示物料问题，以帮助规划人员了解后果并做出必要的调整。</span><span class="sxs-lookup"><span data-stu-id="b16e3-155">In this case, the material issues will be highlighted in the Gantt chart to help the planner to understand consequences and make necessary adjustments.</span></span> 

<span data-ttu-id="b16e3-156">如果作业的计划开始日期晚于作业使用的物料的物料可用性日期，作业将显示物料短缺图标。</span><span class="sxs-lookup"><span data-stu-id="b16e3-156">A job will appear with a material shortage icon if the schedule start date of the job is later than the material availability date for materials consumed by the job.</span></span> <span data-ttu-id="b16e3-157">物料可用性日期基于在动态主计划中的限定标准信息进行计算。</span><span class="sxs-lookup"><span data-stu-id="b16e3-157">The material availability date is calculated based on the pegging information in the dynamic master plan.</span></span> <span data-ttu-id="b16e3-158">例如，如果作业使用的物料根据收据晚于作业计划开始日期的采购订单限定标准，将显示物料短缺图标。</span><span class="sxs-lookup"><span data-stu-id="b16e3-158">The material shortage icon will for example appear on a job that is consuming a material that is pegged against a purchase order that has a receipt that is later than the planned start date of the job.</span></span>

### <a name="indicator-of-material-availability-date"></a><span data-ttu-id="b16e3-159">物料可用性日期指示符</span><span class="sxs-lookup"><span data-stu-id="b16e3-159">Indicator of material availability date</span></span>

<span data-ttu-id="b16e3-160">如果将图表设置为显示具有物料短缺的作业，则也可以显示用于显示作业的物料可用性日期的图标。</span><span class="sxs-lookup"><span data-stu-id="b16e3-160">When you set up the chart to show jobs with material shortages an icon for showing the material availability date for the job can also be shown.</span></span> <span data-ttu-id="b16e3-161">仅当物料可用性日期在图表定义的时间间隔内时，才会显示图标。</span><span class="sxs-lookup"><span data-stu-id="b16e3-161">The icon will only be shown if the material availability date is within the defined time interval of the chart.</span></span> <span data-ttu-id="b16e3-162">如果物料可用性日期在定义的时间间隔以外，可以从作业对话框中的物料清单中检索更加详细的物料可用性信息。</span><span class="sxs-lookup"><span data-stu-id="b16e3-162">If the material availability date lies outside the defined time interval, then more detailed material availability information can be retrieved from the material list in the job dialog box.</span></span> <span data-ttu-id="b16e3-163">该列表中还有一个显示作业最近物料的图标。</span><span class="sxs-lookup"><span data-stu-id="b16e3-163">In the list there is also an icon showing late materials for the job.</span></span> <span data-ttu-id="b16e3-164">您可以使用物料可用性日期作为开始日期重新计划作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-164">You can reschedule a job using the material availability date as a start date.</span></span>

### <a name="indicator-of-order-delivery-date"></a><span data-ttu-id="b16e3-165">订单交货日期指示符</span><span class="sxs-lookup"><span data-stu-id="b16e3-165">Indicator of order delivery date</span></span>

<span data-ttu-id="b16e3-166">此图标指示生产订单的交货日期。</span><span class="sxs-lookup"><span data-stu-id="b16e3-166">This icon indicates the delivery date for a production order.</span></span> <span data-ttu-id="b16e3-167">此图标仅在订单视图中可见。</span><span class="sxs-lookup"><span data-stu-id="b16e3-167">The icon is only visible in the Order view.</span></span>

### <a name="capacity-bar"></a><span data-ttu-id="b16e3-168">产能条</span><span class="sxs-lookup"><span data-stu-id="b16e3-168">Capacity bar</span></span>

<span data-ttu-id="b16e3-169">您可以将图表配置为显示资源产能条。</span><span class="sxs-lookup"><span data-stu-id="b16e3-169">You can configure the chart to show a resource capacity bar.</span></span> <span data-ttu-id="b16e3-170">此栏提供图表定义的时间间隔内的活动的资源产能的概览。</span><span class="sxs-lookup"><span data-stu-id="b16e3-170">This bar provides an overview of the resource capacity for an activity in the defined time interval of the chart.</span></span> <span data-ttu-id="b16e3-171">不显示未预订资源的时间期间的产能条。</span><span class="sxs-lookup"><span data-stu-id="b16e3-171">The capacity bar is not shown for periods of the time where the resource is not booked.</span></span> <span data-ttu-id="b16e3-172">在资源预订为产能的期间，产能条显示为固定条。</span><span class="sxs-lookup"><span data-stu-id="b16e3-172">In periods where the resource is booked to capacity, the capacity bar is shown as a solid bar.</span></span> <span data-ttu-id="b16e3-173">在资源超额预订的期间，该条将显得更厚，且使用红色。</span><span class="sxs-lookup"><span data-stu-id="b16e3-173">In periods where the resource is overbooked, the bar will appear thicker and in a red color.</span></span> <span data-ttu-id="b16e3-174">例如，如果两个作业重叠，产能条将指示在存在重叠的时间间隔内超额预订。</span><span class="sxs-lookup"><span data-stu-id="b16e3-174">For example, if two jobs overlap, the capacity bar will indicate an overbooking in the time interval where there is an overlap.</span></span> <span data-ttu-id="b16e3-175">在您计划作业时，产能条动态更新。</span><span class="sxs-lookup"><span data-stu-id="b16e3-175">The capacity bar is updated dynamically when you schedule a job.</span></span> <span data-ttu-id="b16e3-176">您启用**显示产能条**菜单上的产能条。</span><span class="sxs-lookup"><span data-stu-id="b16e3-176">You enable the capacity bar on the **Show capacity bar** menu.</span></span> <span data-ttu-id="b16e3-177">它仅可在**资源视图**中显示。</span><span class="sxs-lookup"><span data-stu-id="b16e3-177">It can only be shown in **Resource view**.</span></span> <span data-ttu-id="b16e3-178">如果要获得资源上的产能负荷的更详细的视图，请使用**产能负荷**图表，该图表可从菜单或选定活动的上下文菜单中打开。</span><span class="sxs-lookup"><span data-stu-id="b16e3-178">If you want to get a more detailed view of the capacity load on a resource, use the **Capacity load** chart, which can be opened from the menu or the context menu for a selected activity.</span></span>

## <a name="job-scheduling-in-the-gantt-chart"></a><span data-ttu-id="b16e3-179">甘特图中的作业计划</span><span class="sxs-lookup"><span data-stu-id="b16e3-179">Job scheduling in the Gantt chart</span></span>
<span data-ttu-id="b16e3-180">甘特图提供用于对生产计划做出调整的不同选项。</span><span class="sxs-lookup"><span data-stu-id="b16e3-180">The Gantt chart offers different options for making adjustments to the production plan.</span></span> <span data-ttu-id="b16e3-181">在甘特图中，您可以作为拖放交互或从计划菜单中重新计划活动。</span><span class="sxs-lookup"><span data-stu-id="b16e3-181">In the Gantt chart, you can re-schedule activities as a drag-and-drop interaction or from a schedule menu.</span></span> <span data-ttu-id="b16e3-182">在计划过程中，您可以考虑资源产能、资源功能和物料约束。</span><span class="sxs-lookup"><span data-stu-id="b16e3-182">In the planning process, you can take resource capacity, resource capabilities, and material constraints into account.</span></span>

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a><span data-ttu-id="b16e3-183">作为拖放交互计划作业</span><span class="sxs-lookup"><span data-stu-id="b16e3-183">Schedule a job as a drag-and-drop interaction</span></span>

<span data-ttu-id="b16e3-184">您可以在定义的时间间隔内作为拖放交互重新计划作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-184">You can re-schedule job within the defined time interval as a drag-and-drop interaction.</span></span> <span data-ttu-id="b16e3-185">您仅可对相同的资源重新计划作业，且一次仅可计划一个作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-185">You can only re-schedule the job on the same resource, and you can only schedule one job at a time.</span></span>

### <a name="schedule-a-job-from-the-menu"></a><span data-ttu-id="b16e3-186">从菜单计划作业</span><span class="sxs-lookup"><span data-stu-id="b16e3-186">Schedule a job from the menu</span></span>

<span data-ttu-id="b16e3-187">在**计划作业**菜单中，您可以在图表中基于计划方向和计划日期时间计划一个或多个选定作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-187">On the **Schedule jobs** menu, you can schedule one or more selected job in the chart based on a scheduling direction and a scheduling date time.</span></span> <span data-ttu-id="b16e3-188">有三个可用的计划方向。</span><span class="sxs-lookup"><span data-stu-id="b16e3-188">There are three available schedule directions.</span></span>

-   <span data-ttu-id="b16e3-189">从计划日期正推</span><span class="sxs-lookup"><span data-stu-id="b16e3-189">Forward from scheduling date</span></span>
-   <span data-ttu-id="b16e3-190">从计划日期倒推</span><span class="sxs-lookup"><span data-stu-id="b16e3-190">Backward from scheduling date</span></span>
-   <span data-ttu-id="b16e3-191">从物料可用性日期正推</span><span class="sxs-lookup"><span data-stu-id="b16e3-191">Forward from material availability date</span></span>

<span data-ttu-id="b16e3-192">不能在甘特图定义的时间间隔以外计划作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-192">It is not possible to schedule a job outside the defined time interval of the Gantt chart.</span></span> <span data-ttu-id="b16e3-193">否则，该作业将为未计划，且您将收到错误消息，“无法在加载的时间段内计划作业。”</span><span class="sxs-lookup"><span data-stu-id="b16e3-193">If you do that, the job will be left unscheduled and you will receive the error message, "Could not schedule the job within the loaded time period."</span></span>

### <a name="schedule-previous-jobs"></a><span data-ttu-id="b16e3-194">计划上一个作业</span><span class="sxs-lookup"><span data-stu-id="b16e3-194">Schedule previous jobs</span></span>

<span data-ttu-id="b16e3-195">在活动网络中，例如属于同一生产订单的作业，您可以使用**计划上一个作业**功能计划相对于网络中的选定作业的上一个作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-195">In a network of activities, such as jobs belonging to the same production order, you can use the **Schedule previous jobs** function to schedule the previous jobs relative to a selected job in the network.</span></span> <span data-ttu-id="b16e3-196">在以下示例中，突出显示的活动是选定的作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-196">In the following example, the highlighted activity is the selected job.</span></span>

<table>
<tr>
<td>
<span data-ttu-id="b16e3-197">之前</span><span class="sxs-lookup"><span data-stu-id="b16e3-197">Before</span></span>
</td>
<td rowspan=2>
<img src='./media/schprevjob3.png'/>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="b16e3-198">之后</span><span class="sxs-lookup"><span data-stu-id="b16e3-198">After</span></span>
</td>
</tr>
</table>

### <a name="schedule-next-jobs"></a><span data-ttu-id="b16e3-199">计划下一个作业</span><span class="sxs-lookup"><span data-stu-id="b16e3-199">Schedule next jobs</span></span>

<span data-ttu-id="b16e3-200">您可以使用**计划下一个作业**功能计划相对于活动网络中的选定作业的下一个作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-200">You can use the **Schedule next jobs** function to schedule the next jobs relative to a selected job in a network of activities.</span></span> <span data-ttu-id="b16e3-201">在以下示例中，突出显示的活动是选定的作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-201">In the following example, the highlighted activity is the selected job.</span></span>

<table>
<tr>
<td>
<span data-ttu-id="b16e3-202">之前</span><span class="sxs-lookup"><span data-stu-id="b16e3-202">Before</span></span>
</td>
<td rowspan=2>
<img src='./media/schnxtjob.png'/>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="b16e3-203">之后</span><span class="sxs-lookup"><span data-stu-id="b16e3-203">After</span></span>
</td>
</tr>
</table>

### <a name="schedule-around-job"></a><span data-ttu-id="b16e3-204">针对作业计划</span><span class="sxs-lookup"><span data-stu-id="b16e3-204">Schedule around job</span></span>

<span data-ttu-id="b16e3-205">您可以使用**针对作业计划**功能计划相对于活动网络中的选定作业的下一个作业和上一个作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-205">You can use the **Schedule around job** function to schedule the next job and the previous job relative to a selected job in a network of activities.</span></span> <span data-ttu-id="b16e3-206">在以下示例中，突出显示的活动是选定的作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-206">In the following example, the highlighted activity is the selected job.</span></span>

<table>
<tr>
<td>
<span data-ttu-id="b16e3-207">之前</span><span class="sxs-lookup"><span data-stu-id="b16e3-207">Before</span></span>
</td>
<td rowspan=2>
<img src='./media/scharoundjob1.png'/>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="b16e3-208">之后</span><span class="sxs-lookup"><span data-stu-id="b16e3-208">After</span></span>
</td>
</tr>
</table>

### <a name="arrange-jobs"></a><span data-ttu-id="b16e3-209">安排作业</span><span class="sxs-lookup"><span data-stu-id="b16e3-209">Arrange jobs</span></span>

<span data-ttu-id="b16e3-210">您可以使用**安排**功能对相同的资源安排选定的活动。</span><span class="sxs-lookup"><span data-stu-id="b16e3-210">You can use the **Arrange** function to arrange selected activities on the same resource.</span></span> <span data-ttu-id="b16e3-211">这些活动可以处于相同的活动网络中，但也可以属于不同网络。</span><span class="sxs-lookup"><span data-stu-id="b16e3-211">These activities can be in the same network of activities, but can also belong to different networks.</span></span> <span data-ttu-id="b16e3-212">当您使用安排功能时，选定活动之间的时间差将被消除。</span><span class="sxs-lookup"><span data-stu-id="b16e3-212">When you use the arrange function the time gaps between the selected activities will be eliminated.</span></span> <span data-ttu-id="b16e3-213">您可以使用此功能优化资源的产能利用率。</span><span class="sxs-lookup"><span data-stu-id="b16e3-213">You can use this function to optimize the capacity utilization of the resources.</span></span>

<table>
<tr>
<td>
<span data-ttu-id="b16e3-214">之前</span><span class="sxs-lookup"><span data-stu-id="b16e3-214">Before</span></span>
</td>
<td rowspan=2>
<img src='./media/arrangejobs1.png'/>
</td>
</tr>
<tr>
<td>
<span data-ttu-id="b16e3-215">之后</span><span class="sxs-lookup"><span data-stu-id="b16e3-215">After</span></span>
</td>
</tr>
</table>

### <a name="reassign-activities-from-one-resource-to-another"></a><span data-ttu-id="b16e3-216">将一个资源的活动重新分配到另一个资源</span><span class="sxs-lookup"><span data-stu-id="b16e3-216">Reassign activities from one resource to another</span></span>

<span data-ttu-id="b16e3-217">您可以将一个资源的活动重新分配到另一个资源。</span><span class="sxs-lookup"><span data-stu-id="b16e3-217">You can reassign a job from one resource to another.</span></span> <span data-ttu-id="b16e3-218">当机器出现故障或超额预订，且您需要查找可以执行该作业的其他可用资源时，这可能很有用。</span><span class="sxs-lookup"><span data-stu-id="b16e3-218">This can be useful in situations where a machine is out of order or overbooked, and you need to find another available resource that can do the job.</span></span>

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a><span data-ttu-id="b16e3-219">作为拖放交互重新分配活动</span><span class="sxs-lookup"><span data-stu-id="b16e3-219">Reassigning an activity as a drag-and-drop interaction</span></span>

<span data-ttu-id="b16e3-220">在**资源**视图中，您可以在甘特图中作为拖放交互将活动重新分配到不同资源。</span><span class="sxs-lookup"><span data-stu-id="b16e3-220">In the **Resource** view, you can reassign an activity to a different resource in the Gantt chart as a drag-and-drop interaction.</span></span> <span data-ttu-id="b16e3-221">您可以通过选择在其中计划活动的行执行此操作。</span><span class="sxs-lookup"><span data-stu-id="b16e3-221">You do that by selecting the row in which the activity is scheduled.</span></span> <span data-ttu-id="b16e3-222">选择行后，您可以将此行拖放到图表中分组到不同资源分组级别的资源。</span><span class="sxs-lookup"><span data-stu-id="b16e3-222">After the row is selected you can drag the row to the resource in the chart grouped under a different resource grouping level.</span></span>

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a><span data-ttu-id="b16e3-223">从计划作业菜单重新分配活动</span><span class="sxs-lookup"><span data-stu-id="b16e3-223">Reassigning an activity from the Schedule jobs menu</span></span>

<span data-ttu-id="b16e3-224">您可以从**计划作业**菜单打开的**计划作业**对话框重新分配作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-224">You can reassign a job from the **Schedule job** dialog box opened from the **Schedule job** menu.</span></span> <span data-ttu-id="b16e3-225">从此菜单仅可将作业重新分配到已经加载到甘特图的资源。</span><span class="sxs-lookup"><span data-stu-id="b16e3-225">From this menu you can only reassign a job to a resource that is already loaded to the Gantt chart.</span></span> <span data-ttu-id="b16e3-226">如果您仅选择一个作业，则资源的下拉菜单将按适用的资源排序。</span><span class="sxs-lookup"><span data-stu-id="b16e3-226">If you only select one job, then the drop down for the resource will be sorted by applicable resources.</span></span> <span data-ttu-id="b16e3-227">如果您选择多作业，则不会有关于来自资源列表的可用资源的信息。</span><span class="sxs-lookup"><span data-stu-id="b16e3-227">If you select more jobs, then there will be no information about applicable resources from the resource list.</span></span>

## <a name="load-additional-resources-to-the-gantt-chart"></a><span data-ttu-id="b16e3-228">将其他资源加载到甘特图</span><span class="sxs-lookup"><span data-stu-id="b16e3-228">Load additional resources to the Gantt chart</span></span>
<span data-ttu-id="b16e3-229">在**资源视图**中，您有一个用于将其他资源加载到甘特图的选项。</span><span class="sxs-lookup"><span data-stu-id="b16e3-229">In the **Resource view**, you have an option to load additional resources to the Gantt chart.</span></span> <span data-ttu-id="b16e3-230">如果您要为在超额预订或出现故障的机器上计划的作业查找替代资源，这可能很有用。</span><span class="sxs-lookup"><span data-stu-id="b16e3-230">This can be useful if you want to find an alternative resource for a job that is scheduled on a machine that is overbooked or broken down.</span></span> <span data-ttu-id="b16e3-231">在**加载其他资源**页，您将获得从列表打开日期开始具有充足日期的资源列表。</span><span class="sxs-lookup"><span data-stu-id="b16e3-231">On the **Load additional resources** page, you will get a list of resources that are date efficient as of the date the list is opened.</span></span> <span data-ttu-id="b16e3-232">相对于甘特图中的选定作业的适用资源将先被列出来。</span><span class="sxs-lookup"><span data-stu-id="b16e3-232">Applicable resources, relative to a selected job in the Gantt chart, will be listed first.</span></span> <span data-ttu-id="b16e3-233">如果您选择了多个作业，在打开列表前，不会显示适用资源的指示。</span><span class="sxs-lookup"><span data-stu-id="b16e3-233">If you have multiple jobs selected, prior to opening the list, no indication of applicable resources will be shown.</span></span> <span data-ttu-id="b16e3-234">在**加载其他资源**页，您可以选择一个或多个资源，在您确认选择时，这些资源将被加载到甘特图。</span><span class="sxs-lookup"><span data-stu-id="b16e3-234">On the **Load additional resources** page, you can select one or more resources, that will be loaded to the Gantt chart when you confirm your selection.</span></span> <span data-ttu-id="b16e3-235">如果在甘特图的时间间隔内未对选定资源计划任何作业，则资源将被放在甘特图中的活动列表底部的资源分组级别下。</span><span class="sxs-lookup"><span data-stu-id="b16e3-235">If there are no jobs scheduled on the selected resource in the time interval of the Gantt chart, then the resource will be placed under a resource grouping level in the bottom of the list of activities in the Gantt chart.</span></span>

### <a name="access-the-gantt-chart"></a><span data-ttu-id="b16e3-236">访问甘特图</span><span class="sxs-lookup"><span data-stu-id="b16e3-236">Access the Gantt chart</span></span>

<span data-ttu-id="b16e3-237">甘特图不能从以下页面打开。</span><span class="sxs-lookup"><span data-stu-id="b16e3-237">The Gantt chart can be opened from the following pages.</span></span>

| <span data-ttu-id="b16e3-238">**页面**</span><span class="sxs-lookup"><span data-stu-id="b16e3-238">**Page**</span></span>                                                                                     | <span data-ttu-id="b16e3-239">**描述**</span><span class="sxs-lookup"><span data-stu-id="b16e3-239">**Description**</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b16e3-240">**生产订单列表和详细信息**</span><span class="sxs-lookup"><span data-stu-id="b16e3-240">**Production order list and detail**</span></span>                                                         | <span data-ttu-id="b16e3-241">在**生产订单列表和详细信息**页，您可以从一个或多个选择的订单打开甘特图。</span><span class="sxs-lookup"><span data-stu-id="b16e3-241">On the **Production order list and detail** page, you can open the Gantt chart from one or more selected orders.</span></span> <span data-ttu-id="b16e3-242">从**甘特图**菜单项打开图表将加载与选定生产订单有关的所有作业，但也会加载对相同资源计划的其他生产订单的作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-242">Opening the chart from the **Gantt chart** menu item will load all jobs related to the selected production orders, but also jobs from other production orders that are scheduled on the same resources.</span></span> <span data-ttu-id="b16e3-243">从**甘特图 - 快速查看**菜单项打开图表将仅加载与选定的生产订单有关的作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-243">Opening the chart from the **Gantt chart – Fast view** menu item will only load jobs related to the selected production orders.</span></span> <span data-ttu-id="b16e3-244">在此视图中无法计划作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-244">In this view, it is not possible to schedule jobs.</span></span> |
| <span data-ttu-id="b16e3-245">**资源**</span><span class="sxs-lookup"><span data-stu-id="b16e3-245">**Resource**</span></span>                                                                                 | <span data-ttu-id="b16e3-246">在**资源**页上，可以从菜单项**甘特图**打开甘特图。</span><span class="sxs-lookup"><span data-stu-id="b16e3-246">On the **Resource** page, you can open the Gantt chart from the menu item **Gantt chart**.</span></span> <span data-ttu-id="b16e3-247">如果选中，在选定时间间隔中对资源计划的所有作业将加载到图表。</span><span class="sxs-lookup"><span data-stu-id="b16e3-247">When selected, all the jobs scheduled on the resource in a selected time interval will be loaded to the chart.</span></span>                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b16e3-248">**资源组**</span><span class="sxs-lookup"><span data-stu-id="b16e3-248">**Resource group**</span></span>                                                                           | <span data-ttu-id="b16e3-249">在**资源组**页上，可以从菜单项**甘特**图打开甘特图。</span><span class="sxs-lookup"><span data-stu-id="b16e3-249">On the **Resource group** page, you can open the Gantt chart from the menu item **Gantt** chart.</span></span> <span data-ttu-id="b16e3-250">如果选中，对资源组中的资源计划的所有作业将显示在选定的时间间隔内。</span><span class="sxs-lookup"><span data-stu-id="b16e3-250">When selected, all the jobs scheduled on the resources in the resource group will be shown in a selected time interval.</span></span>                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="b16e3-251">**甘特图**</span><span class="sxs-lookup"><span data-stu-id="b16e3-251">**Gantt charts**</span></span>                                                                             | <span data-ttu-id="b16e3-252">在**甘特图**页可以按资源和资源组配置甘特图。</span><span class="sxs-lookup"><span data-stu-id="b16e3-252">On the **Gantt charts** page you can configure Gantt charts by resources and resource groups.</span></span> <span data-ttu-id="b16e3-253">例如，如果要控制特定的资源或资源组集合的生产活动，您可以在**甘特图**页上对其进行单独配置。</span><span class="sxs-lookup"><span data-stu-id="b16e3-253">For example, if you want to control production activities for specific sets of resources or resource groups, then you can make individual configurations of those on the **Gantt charts** page.</span></span> <span data-ttu-id="b16e3-254">然后，您可以从每个配置打开甘特图。</span><span class="sxs-lookup"><span data-stu-id="b16e3-254">You can then open the Gantt chart from each configuration.</span></span>                                                                                                                                                    |
| <span data-ttu-id="b16e3-255">**工时预测**（项目）</span><span class="sxs-lookup"><span data-stu-id="b16e3-255">**Hour forecasts** (project)</span></span>                                                                 | <span data-ttu-id="b16e3-256">**工时预测**类型的项目活动可对资源计划作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-256">Project activities of type **Hour forecast** can be job scheduled on resources.</span></span> <span data-ttu-id="b16e3-257">在**计划**菜单上的**工时预测**页上，可以按顺序打开甘特图以查看工时预测类型的已计划作业项目活动。</span><span class="sxs-lookup"><span data-stu-id="b16e3-257">On the **Hour forecast** page on the **Scheduling** menu you can open the Gantt chart on a order to see job scheduled project activities of type hour forecast.</span></span>                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b16e3-258">**要完成的作业**（**生产车间管理**工作区中的列表）</span><span class="sxs-lookup"><span data-stu-id="b16e3-258">**Job to complete** (List in **Production floor management** workspace)</span></span>                      | <span data-ttu-id="b16e3-259">**生产车间管理中要完成的作业列表**工作区显示来自工作区选定资源上正在进行的生产和批次订单的作业。</span><span class="sxs-lookup"><span data-stu-id="b16e3-259">The **Jobs to complete list in the Production floor management** workspace shows jobs from production and batch orders that are in progress on the selected resources for the workspace.</span></span> <span data-ttu-id="b16e3-260">在**甘特图**菜单项上可以打开甘特图，其中列表中的所有选定作业将加载到图表。</span><span class="sxs-lookup"><span data-stu-id="b16e3-260">On the **Gantt chart** menu item you can open the Gantt chart, where all the jobs selected in the list will be loaded to the chart.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="b16e3-261">**要下达的生产订单**（从**生产车间管理**工作区打开）</span><span class="sxs-lookup"><span data-stu-id="b16e3-261">**Production orders to release** (Opened from the **Production floor management** workspace)</span></span> | <span data-ttu-id="b16e3-262">要下达的生产订单页从**生产车间管理**工作区打开。</span><span class="sxs-lookup"><span data-stu-id="b16e3-262">The production orders to release page is opened from the **Production floor management** workspace.</span></span> <span data-ttu-id="b16e3-263">此页显示等待下达的已计划生产和批次订单。</span><span class="sxs-lookup"><span data-stu-id="b16e3-263">This page shows scheduled production and batch orders pending release.</span></span> <span data-ttu-id="b16e3-264">在此页上可以打开选定生产订单的甘特图。</span><span class="sxs-lookup"><span data-stu-id="b16e3-264">On this page you can open the Gantt chart for selected production orders.</span></span>                                                                                                                                                                                                                                                        |




