---
title: 用于精益生产的可视排产
description: 本主题提供关于看板计划板的信息，生产规划人员可以使用看板计划板控制和优化看板作业的生产计划。
author: johanhoffmann
manager: tfehr
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization, KanbanBoardUnplannedJobs
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45a63ab0f5baadf6bef646224b3f0bf5327ee923
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4422753"
---
# <a name="visual-scheduling-for-lean-manufacturing"></a><span data-ttu-id="ed036-103">用于精益生产的可视排产</span><span class="sxs-lookup"><span data-stu-id="ed036-103">Visual scheduling for lean manufacturing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed036-104">本主题提供关于看板计划板的信息，生产规划人员可以使用看板计划板控制和优化看板作业的生产计划。</span><span class="sxs-lookup"><span data-stu-id="ed036-104">This topic provides information about the Kanban schedule board, which the production planner can use to control and optimize the production plan for kanban jobs.</span></span>

<span data-ttu-id="ed036-105">本主题提供关于看板计划板的信息，生产规划人员可以使用看板计划板控制和优化看板作业的生产计划。</span><span class="sxs-lookup"><span data-stu-id="ed036-105">This topic provides information about the Kanban schedule board, which the production planner can use to control and optimize the production plan for kanban jobs.</span></span>

<span data-ttu-id="ed036-106">看板计划板使生产规划人员可以控制和优化看板作业的生产计划。</span><span class="sxs-lookup"><span data-stu-id="ed036-106">The Kanban schedule board lets the production planner control and optimize the production plan for kanban jobs.</span></span> <span data-ttu-id="ed036-107">它使看板作业流透明，且为生产规划人员提供优化和调整 lean manufacturing 工作单元生产计划的工具。</span><span class="sxs-lookup"><span data-stu-id="ed036-107">It makes the flow of kanban jobs transparent, and gives the production planner a tool that optimizes and adjusts the production plan for the lean manufacturing work cell.</span></span>

## <a name="visual-scheduling-of-kanban-jobs"></a><span data-ttu-id="ed036-108">看板作业的可视排产</span><span class="sxs-lookup"><span data-stu-id="ed036-108">Visual scheduling of kanban jobs</span></span>
<span data-ttu-id="ed036-109">看板作业可以包括一个或多个看板作业。</span><span class="sxs-lookup"><span data-stu-id="ed036-109">A kanban job can consist of one or many kanban jobs.</span></span> <span data-ttu-id="ed036-110">有以下两种类型的看板作业：</span><span class="sxs-lookup"><span data-stu-id="ed036-110">There are two types of kanban jobs:</span></span>

-   <span data-ttu-id="ed036-111">进程</span><span class="sxs-lookup"><span data-stu-id="ed036-111">Process</span></span>
-   <span data-ttu-id="ed036-112">转移</span><span class="sxs-lookup"><span data-stu-id="ed036-112">Transfer</span></span>

<span data-ttu-id="ed036-113">您仅可以计划 **流程** 类型的作业。</span><span class="sxs-lookup"><span data-stu-id="ed036-113">You can schedule only jobs of the **Process** type.</span></span> <span data-ttu-id="ed036-114">看板作业及其属性（例如活动时间）在生产看板流中进行定义。</span><span class="sxs-lookup"><span data-stu-id="ed036-114">The kanban job and its properties, such as the activity time, are defined in the production kanban flow.</span></span> <span data-ttu-id="ed036-115">在生产看板流，看板作业还被分配到工作单元。</span><span class="sxs-lookup"><span data-stu-id="ed036-115">In the production kanban flow, the kanban job is also assigned to a work cell.</span></span> <span data-ttu-id="ed036-116">工作单元的每日产能基于在资源组上设置的工作单元产能进行计算。</span><span class="sxs-lookup"><span data-stu-id="ed036-116">The work cell's daily capacity is calculated based on the work cell capacity that is set on the resource group.</span></span> <span data-ttu-id="ed036-117">在相关日历中按每日工作时间进行调整。</span><span class="sxs-lookup"><span data-stu-id="ed036-117">It's adjusted by the daily working time in the related calendar.</span></span> <span data-ttu-id="ed036-118">计划看板作业后，该作业加载工作单元的产能。</span><span class="sxs-lookup"><span data-stu-id="ed036-118">When a kanban job is scheduled, the job loads the capacity of the work cell.</span></span> <span data-ttu-id="ed036-119">看板计划板提供以下主要功能：</span><span class="sxs-lookup"><span data-stu-id="ed036-119">The Kanban schedule board provides the following main features:</span></span>

-   <span data-ttu-id="ed036-120">精益工作单元中的生产计划的图形概览。</span><span class="sxs-lookup"><span data-stu-id="ed036-120">A graphical overview of the production plan in a lean work cell.</span></span> <span data-ttu-id="ed036-121">此概览显示在定义的期间的已计划的看板流程作业。</span><span class="sxs-lookup"><span data-stu-id="ed036-121">This overview shows the planned kanban process jobs in the defined periods.</span></span>
-   <span data-ttu-id="ed036-122">让您计划未计划的看板作业和重新计划之前已计划的作业的工具。</span><span class="sxs-lookup"><span data-stu-id="ed036-122">A tool that lets you schedule unplanned kanban jobs and reschedule previously scheduled jobs.</span></span>

## <a name="kanban-schedule-board"></a><span data-ttu-id="ed036-123">看板计划板</span><span class="sxs-lookup"><span data-stu-id="ed036-123">Kanban schedule board</span></span>
<span data-ttu-id="ed036-124">如下图中所示，**看板计划板** 页包含七个主要元素。</span><span class="sxs-lookup"><span data-stu-id="ed036-124">The **Kanban schedule board** page contains seven main elements, as shown in the following illustration.</span></span> 

![看板计划板](./media/kanban-schedule-board-1024x554.png)
1.  <span data-ttu-id="ed036-126">操作窗格</span><span class="sxs-lookup"><span data-stu-id="ed036-126">Action Pane</span></span>
2.  <span data-ttu-id="ed036-127">筛选器字段</span><span class="sxs-lookup"><span data-stu-id="ed036-127">Filter fields</span></span>
3.  <span data-ttu-id="ed036-128">用于未计划的作业的按钮</span><span class="sxs-lookup"><span data-stu-id="ed036-128">Button for unplanned jobs</span></span>
4.  <span data-ttu-id="ed036-129">时间段节点</span><span class="sxs-lookup"><span data-stu-id="ed036-129">Period node</span></span>
5.  <span data-ttu-id="ed036-130">看板作业</span><span class="sxs-lookup"><span data-stu-id="ed036-130">Kanban job</span></span>
6.  <span data-ttu-id="ed036-131">产能条</span><span class="sxs-lookup"><span data-stu-id="ed036-131">Capacity bar</span></span>
7.  <span data-ttu-id="ed036-132">时间刻度</span><span class="sxs-lookup"><span data-stu-id="ed036-132">Time scale</span></span>

### <a name="view-the-time-scale"></a><span data-ttu-id="ed036-133">查看时间刻度</span><span class="sxs-lookup"><span data-stu-id="ed036-133">View the time scale</span></span>

<span data-ttu-id="ed036-134">该板划分为多个时间段，每个时间段表示为一个节点 (4)。</span><span class="sxs-lookup"><span data-stu-id="ed036-134">The board is divided into periods, each of which is represented as a node (4).</span></span> <span data-ttu-id="ed036-135">时间段节点列在垂直轴上，水平轴表示显示时间段长度的时间刻度 (7)。</span><span class="sxs-lookup"><span data-stu-id="ed036-135">The period nodes are listed on the vertical axis, and the horizontal axis represents a time scale (7) that shows the length of the period.</span></span> <span data-ttu-id="ed036-136">时间段的长度为一天或一周。</span><span class="sxs-lookup"><span data-stu-id="ed036-136">A period has a length of either one day or one week.</span></span> <span data-ttu-id="ed036-137">时间段长度由为看板计划板 (2) 选择的工作单元的配置确定。</span><span class="sxs-lookup"><span data-stu-id="ed036-137">The period length is determined by the configuration of the work cell that is selected for the Kanban schedule board (2).</span></span> <span data-ttu-id="ed036-138">对于每个时间段节点，看板计划板指示有多少已计划的看板计划加载此时间段。</span><span class="sxs-lookup"><span data-stu-id="ed036-138">For each period node, the Kanban schedule board indicates how much the scheduled kanban jobs are loading the period.</span></span> <span data-ttu-id="ed036-139">此外还存在该时间段最大生产量的指示。</span><span class="sxs-lookup"><span data-stu-id="ed036-139">There is also an indication of the maximum throughput for the period.</span></span> <span data-ttu-id="ed036-140">如果已计划的生产量超出最大生产量，则该时间段被视为超负荷，并且显示红色警告符号。</span><span class="sxs-lookup"><span data-stu-id="ed036-140">If the scheduled throughput exceeds the maximum throughput, the period is considered as overloaded, and a red warning symbol appears.</span></span> <span data-ttu-id="ed036-141">已计划的看板作业显示在已计划了开始和结束时间 (5) 的时间段中。</span><span class="sxs-lookup"><span data-stu-id="ed036-141">A scheduled kanban job appears in a period that has scheduled start and end times (5).</span></span> <span data-ttu-id="ed036-142">作业的长度与活动时间相等。</span><span class="sxs-lookup"><span data-stu-id="ed036-142">The length of the job is equal to the activity time.</span></span> <span data-ttu-id="ed036-143">如果看板作业的活动时间超出工作单元的任务时间，则该看板作业在时间段中显示为重叠。</span><span class="sxs-lookup"><span data-stu-id="ed036-143">Kanban jobs appear as overlapping in a period if their activity times exceed the task time of the work cell.</span></span>

### <a name="view-job-status"></a><span data-ttu-id="ed036-144">查看作业状态</span><span class="sxs-lookup"><span data-stu-id="ed036-144">View job status</span></span>

<span data-ttu-id="ed036-145">将指针悬停在作业上时显示的工具提示中提供有关看板作业的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ed036-145">More information about a kanban job is available in the tooltip that appears when you hover the pointer over the job.</span></span> <span data-ttu-id="ed036-146">符号提供有关作业的状态的信息。</span><span class="sxs-lookup"><span data-stu-id="ed036-146">A symbol provides information about the status of the job.</span></span> <span data-ttu-id="ed036-147">例如，时钟符号表示看板作业逾期。</span><span class="sxs-lookup"><span data-stu-id="ed036-147">For example, a clock symbol indicates that the kanban job is overdue.</span></span>

### <a name="use-colors-to-view-the-kanban-schedule-board"></a><span data-ttu-id="ed036-148">使用颜色查看看板计划板</span><span class="sxs-lookup"><span data-stu-id="ed036-148">Use colors to view the Kanban schedule board</span></span>

<span data-ttu-id="ed036-149">要增强看板计划板提供的概览，可以使用颜色来区分看板作业。</span><span class="sxs-lookup"><span data-stu-id="ed036-149">To enhance the overview that the Kanban schedule board provides, you can use colors to distinguish kanban jobs.</span></span> <span data-ttu-id="ed036-150">看板作业的颜色在精益计划组中进行配置，您可以在精益计划组中聚合应在相同序列中生产的产品。</span><span class="sxs-lookup"><span data-stu-id="ed036-150">The color of a kanban job is configured in the lean schedule group, where you can aggregate the products that should be produced in the same sequence.</span></span> <span data-ttu-id="ed036-151">操作窗格 **看板** 选项卡上的 **使用主题颜色** 按钮让您能够在应用程序主题颜色与在精益计划组中配置的颜色之间切换。</span><span class="sxs-lookup"><span data-stu-id="ed036-151">The **Use theme colors** button on the **Board** tab of the Action Pane lets you switch between the application theme colors and the colors that are configured in the lean schedule group.</span></span> <span data-ttu-id="ed036-152">对于每个时间段，产能条 (6) 表示该时间段有多少个可用小时数已加载看板作业。</span><span class="sxs-lookup"><span data-stu-id="ed036-152">For each period, a capacity bar (6) indicates how many of the available hours for the period have been loaded with kanban jobs.</span></span> <span data-ttu-id="ed036-153">如果时间段超负荷，产能条变厚且显示红色。</span><span class="sxs-lookup"><span data-stu-id="ed036-153">If the period is overloaded, the capacity bar appears thicker and in red.</span></span> <span data-ttu-id="ed036-154">所有这些功能都在 **看板计划板** 页顶部的操作窗格 (1) 的 **看板** 选项卡上提供。</span><span class="sxs-lookup"><span data-stu-id="ed036-154">All these functions are available on the **Board** tab of the Action Pane (1) at the top of the **Kanban schedule board** page.</span></span>

## <a name="plan-unplanned-jobs"></a><span data-ttu-id="ed036-155">计划未计划的作业</span><span class="sxs-lookup"><span data-stu-id="ed036-155">Plan unplanned jobs</span></span>
<span data-ttu-id="ed036-156">您可以从 **计划未计划的作业** 对话框计划未计划的看板作业。</span><span class="sxs-lookup"><span data-stu-id="ed036-156">You can schedule unplanned kanban jobs from the **Plan unplanned jobs** dialog box.</span></span> <span data-ttu-id="ed036-157">要打开此对话框，单击 **未计划的作业** 按钮，此时将显示当前未计划作业的数量。</span><span class="sxs-lookup"><span data-stu-id="ed036-157">To open this dialog box, click the **Unplanned jobs** button that shows the current number of unplanned jobs.</span></span> <span data-ttu-id="ed036-158">或者单击操作窗格 **看板** 选项卡上的 **计划未计划的作业**。</span><span class="sxs-lookup"><span data-stu-id="ed036-158">Alternatively, click **Plan unplanned jobs** on the **Board** tab of the Action Pane.</span></span> <span data-ttu-id="ed036-159">对话框显示工作单元的未计划的看板作业的列表。</span><span class="sxs-lookup"><span data-stu-id="ed036-159">The dialog box shows a list of the unplanned kanban jobs for the work cell.</span></span> <span data-ttu-id="ed036-160">您可以使用 **筛选器** 字段筛选网格中的所有字段。</span><span class="sxs-lookup"><span data-stu-id="ed036-160">You can use the **Filter** field to filter on all fields in the grid.</span></span> <span data-ttu-id="ed036-161">例如，您可以筛选特定产品的看板作业。</span><span class="sxs-lookup"><span data-stu-id="ed036-161">For example, you can filter on kanban jobs for a specific product.</span></span> <span data-ttu-id="ed036-162">筛选您要计划的作业的列表后，在列表中进行选择，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="ed036-162">After you have a filtered list of the jobs that you want to schedule, select them in the list, and then click **OK**.</span></span> <span data-ttu-id="ed036-163">要使用自动规划来计划作业，将 **自动规划** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="ed036-163">To use automatic planning to schedule the jobs, set the **Automatic planning** option to **Yes**.</span></span> <span data-ttu-id="ed036-164">在这种情况下，将根据作业的到期日期将作业计划到一个时间段。</span><span class="sxs-lookup"><span data-stu-id="ed036-164">In this case, the jobs are scheduled into a period according to their due date.</span></span> <span data-ttu-id="ed036-165">您可以按时间段计划作业。</span><span class="sxs-lookup"><span data-stu-id="ed036-165">You can also schedule the jobs by period.</span></span> <span data-ttu-id="ed036-166">只需在 **时间段** 字段中选择一个时间段。</span><span class="sxs-lookup"><span data-stu-id="ed036-166">Just select a period in the **Period** field.</span></span> <span data-ttu-id="ed036-167">下图显示 **计划未计划的作业** 对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="ed036-167">The following illustration shows an example of the **Plan unplanned jobs** dialog box.</span></span> 

![计划未计划的作业对话框](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a><span data-ttu-id="ed036-169">在相同时间段中为看板作业排序</span><span class="sxs-lookup"><span data-stu-id="ed036-169">Sequence kanban jobs within the same period</span></span>
<span data-ttu-id="ed036-170">您可以更改一个时间段内的一个或多个所选作业的序列。</span><span class="sxs-lookup"><span data-stu-id="ed036-170">You can change the sequence of one or more selected jobs within a period.</span></span> <span data-ttu-id="ed036-171">如果您要确定一些作业在时间段内的优先级，此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="ed036-171">This capability can be useful if you want to prioritize some jobs within the period.</span></span> <span data-ttu-id="ed036-172">或者，您可能要对具有相同产品属性的作业排序，以优化作业执行。</span><span class="sxs-lookup"><span data-stu-id="ed036-172">Alternatively, you might want to sequence jobs that have the same product attributes, to optimize job execution.</span></span> <span data-ttu-id="ed036-173">您可以通过拖放操作，或者使用操作窗格 **看板** 选项卡上的 **后退** 和 **前进** 菜单项更改序列。</span><span class="sxs-lookup"><span data-stu-id="ed036-173">You can change the sequence through a drag-and-drop operation, or by using the **Backward** and **Forward** menu items on the **Board** tab of the Action Pane.</span></span>

## <a name="reassign-kanban-jobs-across-periods"></a><span data-ttu-id="ed036-174">跨时间段重新分配看板作业</span><span class="sxs-lookup"><span data-stu-id="ed036-174">Reassign kanban jobs across periods</span></span>
<span data-ttu-id="ed036-175">作业可以从一个时间段重新分配到另一个时间段。</span><span class="sxs-lookup"><span data-stu-id="ed036-175">Jobs can be reassigned from one period to another.</span></span> <span data-ttu-id="ed036-176">如果一个时间段超负荷，且您要将负荷平衡到具有备用产能的时间段，此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="ed036-176">This capability can be useful if a period is overloaded and you want to level the load to periods that have spare capacity.</span></span> <span data-ttu-id="ed036-177">您可以通过拖放操作，或者使用操作窗格 **看板** 选项卡上的 **下一个时间段** 和 **上一个时间段** 菜单项重新分配作业。</span><span class="sxs-lookup"><span data-stu-id="ed036-177">You can reassign jobs through a drag-and-drop operation, or by using the **Next period** and **Previous period** menu items on the **Board** tab of the Action Pane.</span></span>

## <a name="open-the-kanban-schedule-board"></a><span data-ttu-id="ed036-178">打开看板计划板</span><span class="sxs-lookup"><span data-stu-id="ed036-178">Open the Kanban schedule board</span></span>
<span data-ttu-id="ed036-179">您可以使用以下页面上的菜单项打开看板计划板：</span><span class="sxs-lookup"><span data-stu-id="ed036-179">You can open the Kanban schedule board by using the menu item on the following pages:</span></span>

-   <span data-ttu-id="ed036-180">**生产区域** 页</span><span class="sxs-lookup"><span data-stu-id="ed036-180">**Production area** page</span></span>
-   <span data-ttu-id="ed036-181">**看板作业计划** 页</span><span class="sxs-lookup"><span data-stu-id="ed036-181">**Kanban jobs scheduling** page</span></span>
-   <span data-ttu-id="ed036-182">**生产流可视化** 页</span><span class="sxs-lookup"><span data-stu-id="ed036-182">**Production flow visualization** page</span></span>


<a name="additional-resources"></a><span data-ttu-id="ed036-183">其他资源</span><span class="sxs-lookup"><span data-stu-id="ed036-183">Additional resources</span></span>
--------

[<span data-ttu-id="ed036-184">用于精益生产的看板作业级排产</span><span class="sxs-lookup"><span data-stu-id="ed036-184">Kanban job scheduling for lean manufacturing</span></span>](lean-manufacturing-kanban-job-scheduling.md)

