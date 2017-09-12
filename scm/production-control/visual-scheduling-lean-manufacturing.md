---
title: "用于精益生产的可视排产"
description: "本主题提供关于看板计划板的信息，生产规划人员可以使用看板计划板控制和优化看板作业的生产计划。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: "KanbanBoard，KanbanJobSchedulingListPage，LeanProductionFlowVisulaization"
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
ms.openlocfilehash: 8549d088c094bc392ccaf1b68289e3b0b101db1a
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="visual-scheduling-for-lean-manufacturing"></a><span data-ttu-id="ab38e-104">用于精益生产的可视排产</span><span class="sxs-lookup"><span data-stu-id="ab38e-104">Visual scheduling for lean manufacturing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ab38e-105">本主题提供关于看板计划板的信息，生产规划人员可以使用看板计划板控制和优化看板作业的生产计划。</span><span class="sxs-lookup"><span data-stu-id="ab38e-105">This topic provides information about the Kanban schedule board, which the production planner can use to control and optimize the production plan for kanban jobs.</span></span>

<span data-ttu-id="ab38e-106">本主题提供关于看板计划板的信息，生产规划人员可以使用看板计划板控制和优化看板作业的生产计划。</span><span class="sxs-lookup"><span data-stu-id="ab38e-106">This topic provides information about the Kanban schedule board, which the production planner can use to control and optimize the production plan for kanban jobs.</span></span>

<span data-ttu-id="ab38e-107">看板计划板使生产规划人员可以控制和优化看板作业的生产计划。</span><span class="sxs-lookup"><span data-stu-id="ab38e-107">The Kanban schedule board lets the production planner control and optimize the production plan for kanban jobs.</span></span> <span data-ttu-id="ab38e-108">它使看板作业流透明，且为生产规划人员提供优化和调整 lean manufacturing 工作单元生产计划的工具。</span><span class="sxs-lookup"><span data-stu-id="ab38e-108">It makes the flow of kanban jobs transparent, and gives the production planner a tool that optimizes and adjusts the production plan for the lean manufacturing work cell.</span></span>

## <a name="visual-scheduling-of-kanban-jobs"></a><span data-ttu-id="ab38e-109">看板作业的可视排产</span><span class="sxs-lookup"><span data-stu-id="ab38e-109">Visual scheduling of kanban jobs</span></span>
<span data-ttu-id="ab38e-110">看板作业可以包括一个或多个看板作业。</span><span class="sxs-lookup"><span data-stu-id="ab38e-110">A kanban job can consist of one or many kanban jobs.</span></span> <span data-ttu-id="ab38e-111">有以下两种类型的看板作业：</span><span class="sxs-lookup"><span data-stu-id="ab38e-111">There are two types of kanban jobs:</span></span>

-   <span data-ttu-id="ab38e-112">进程</span><span class="sxs-lookup"><span data-stu-id="ab38e-112">Process</span></span>
-   <span data-ttu-id="ab38e-113">转移</span><span class="sxs-lookup"><span data-stu-id="ab38e-113">Transfer</span></span>

<span data-ttu-id="ab38e-114">您仅可以计划**流程**类型的作业。</span><span class="sxs-lookup"><span data-stu-id="ab38e-114">You can schedule only jobs of the **Process** type.</span></span> <span data-ttu-id="ab38e-115">看板作业及其属性（例如活动时间）在生产看板流中进行定义。</span><span class="sxs-lookup"><span data-stu-id="ab38e-115">The kanban job and its properties, such as the activity time, are defined in the production kanban flow.</span></span> <span data-ttu-id="ab38e-116">在生产看板流，看板作业还被分配到工作单元。</span><span class="sxs-lookup"><span data-stu-id="ab38e-116">In the production kanban flow, the kanban job is also assigned to a work cell.</span></span> <span data-ttu-id="ab38e-117">工作单元的每日产能基于在资源组上设置的工作单元产能进行计算。</span><span class="sxs-lookup"><span data-stu-id="ab38e-117">The work cell's daily capacity is calculated based on the work cell capacity that is set on the resource group.</span></span> <span data-ttu-id="ab38e-118">在相关日历中按每日工作时间进行调整。</span><span class="sxs-lookup"><span data-stu-id="ab38e-118">It's adjusted by the daily working time in the related calendar.</span></span> <span data-ttu-id="ab38e-119">计划看板作业后，该作业加载工作单元的产能。</span><span class="sxs-lookup"><span data-stu-id="ab38e-119">When a kanban job is scheduled, the job loads the capacity of the work cell.</span></span> <span data-ttu-id="ab38e-120">看板计划板提供以下主要功能：</span><span class="sxs-lookup"><span data-stu-id="ab38e-120">The Kanban schedule board provides the following main features:</span></span>

-   <span data-ttu-id="ab38e-121">精益工作单元中的生产计划的图形概览。</span><span class="sxs-lookup"><span data-stu-id="ab38e-121">A graphical overview of the production plan in a lean work cell.</span></span> <span data-ttu-id="ab38e-122">此概览显示在定义的期间的已计划的看板流程作业。</span><span class="sxs-lookup"><span data-stu-id="ab38e-122">This overview shows the planned kanban process jobs in the defined periods.</span></span>
-   <span data-ttu-id="ab38e-123">让您计划未计划的看板作业和重新计划之前已计划的作业的工具。</span><span class="sxs-lookup"><span data-stu-id="ab38e-123">A tool that lets you schedule unplanned kanban jobs and reschedule previously scheduled jobs.</span></span>

## <a name="kanban-schedule-board"></a><span data-ttu-id="ab38e-124">看板计划板</span><span class="sxs-lookup"><span data-stu-id="ab38e-124">Kanban schedule board</span></span>
<span data-ttu-id="ab38e-125">如下图中所示，**看板计划板**页包含七个主要元素。</span><span class="sxs-lookup"><span data-stu-id="ab38e-125">The **Kanban schedule board** page contains seven main elements, as shown in the following illustration.</span></span> 

![看板计划板](./media/kanban-schedule-board-1024x554.png)
1.  <span data-ttu-id="ab38e-127">操作窗格</span><span class="sxs-lookup"><span data-stu-id="ab38e-127">Action Pane</span></span>
2.  <span data-ttu-id="ab38e-128">筛选器字段</span><span class="sxs-lookup"><span data-stu-id="ab38e-128">Filter fields</span></span>
3.  <span data-ttu-id="ab38e-129">用于未计划的作业的按钮</span><span class="sxs-lookup"><span data-stu-id="ab38e-129">Button for unplanned jobs</span></span>
4.  <span data-ttu-id="ab38e-130">时间段节点</span><span class="sxs-lookup"><span data-stu-id="ab38e-130">Period node</span></span>
5.  <span data-ttu-id="ab38e-131">看板作业</span><span class="sxs-lookup"><span data-stu-id="ab38e-131">Kanban job</span></span>
6.  <span data-ttu-id="ab38e-132">产能条</span><span class="sxs-lookup"><span data-stu-id="ab38e-132">Capacity bar</span></span>
7.  <span data-ttu-id="ab38e-133">时间刻度</span><span class="sxs-lookup"><span data-stu-id="ab38e-133">Time scale</span></span>

### <a name="view-the-time-scale"></a><span data-ttu-id="ab38e-134">查看时间刻度</span><span class="sxs-lookup"><span data-stu-id="ab38e-134">View the time scale</span></span>

<span data-ttu-id="ab38e-135">该板划分为多个时间段，每个时间段表示为一个节点 (4)。</span><span class="sxs-lookup"><span data-stu-id="ab38e-135">The board is divided into periods, each of which is represented as a node (4).</span></span> <span data-ttu-id="ab38e-136">时间段节点列在垂直轴上，水平访问表示显示时间段长度的时间刻度 (7)。</span><span class="sxs-lookup"><span data-stu-id="ab38e-136">The period nodes are listed on the vertical axis, and the horizontal access represents a time scale (7) that shows the length of the period.</span></span> <span data-ttu-id="ab38e-137">时间段的长度为一天或一周。</span><span class="sxs-lookup"><span data-stu-id="ab38e-137">A period has a length of either one day or one week.</span></span> <span data-ttu-id="ab38e-138">时间段长度由为看板计划板 (2) 选择的工作单元的配置确定。</span><span class="sxs-lookup"><span data-stu-id="ab38e-138">The period length is determined by the configuration of the work cell that is selected for the Kanban schedule board (2).</span></span> <span data-ttu-id="ab38e-139">对于每个时间段节点，看板计划板指示有多少已计划的看板计划加载此时间段。</span><span class="sxs-lookup"><span data-stu-id="ab38e-139">For each period node, the Kanban schedule board indicates how much the scheduled kanban jobs are loading the period.</span></span> <span data-ttu-id="ab38e-140">此外还存在该时间段最大生产量的指示。</span><span class="sxs-lookup"><span data-stu-id="ab38e-140">There is also an indication of the maximum throughput for the period.</span></span> <span data-ttu-id="ab38e-141">如果已计划的生产量超出最大生产量，则该时间段被视为超负荷，并且显示红色警告符号。</span><span class="sxs-lookup"><span data-stu-id="ab38e-141">If the scheduled throughput exceeds the maximum throughput, the period is considered as overloaded, and a red warning symbol appears.</span></span> <span data-ttu-id="ab38e-142">已计划的看板作业显示在已计划了开始和结束时间 (5) 的时间段中。</span><span class="sxs-lookup"><span data-stu-id="ab38e-142">A scheduled kanban job appears in a period that has scheduled start and end times (5).</span></span> <span data-ttu-id="ab38e-143">作业的长度与活动时间相等。</span><span class="sxs-lookup"><span data-stu-id="ab38e-143">The length of the job is equal to the activity time.</span></span> <span data-ttu-id="ab38e-144">如果看板作业的活动时间超出工作单元的单位产品生产时间，则该看板作业在时间段中显示为重叠。</span><span class="sxs-lookup"><span data-stu-id="ab38e-144">Kanban jobs appear as overlapping in a period if their activity times exceed the takt time of the work cell.</span></span>

### <a name="view-job-status"></a><span data-ttu-id="ab38e-145">查看作业状态</span><span class="sxs-lookup"><span data-stu-id="ab38e-145">View job status</span></span>

<span data-ttu-id="ab38e-146">将指针悬停在作业上时显示的工具提示中提供有关看板作业的详细信息。</span><span class="sxs-lookup"><span data-stu-id="ab38e-146">More information about a kanban job is available in the tooltip that appears when you hover the pointer over the job.</span></span> <span data-ttu-id="ab38e-147">符号提供有关作业的状态的信息。</span><span class="sxs-lookup"><span data-stu-id="ab38e-147">A symbol provides information about the status of the job.</span></span> <span data-ttu-id="ab38e-148">例如，时钟符号表示看板作业逾期。</span><span class="sxs-lookup"><span data-stu-id="ab38e-148">For example, a clock symbol indicates that the kanban job is overdue.</span></span>

### <a name="use-colors-to-view-the-kanban-schedule-board"></a><span data-ttu-id="ab38e-149">使用颜色查看看板计划板</span><span class="sxs-lookup"><span data-stu-id="ab38e-149">Use colors to view the Kanban schedule board</span></span>

<span data-ttu-id="ab38e-150">要增强看板计划板提供的概览，可以使用颜色来区分看板作业。</span><span class="sxs-lookup"><span data-stu-id="ab38e-150">To enhance the overview that the Kanban schedule board provides, you can use colors to distinguish kanban jobs.</span></span> <span data-ttu-id="ab38e-151">看板作业的颜色在精益计划组中进行配置，您可以在精益计划组中聚合应在相同序列中生产的产品。</span><span class="sxs-lookup"><span data-stu-id="ab38e-151">The color of a kanban job is configured in the lean schedule group, where you can aggregate the products that should be produced in the same sequence.</span></span> <span data-ttu-id="ab38e-152">操作窗格**看板**选项卡上的**使用主题颜色**按钮让您能够在应用程序主题颜色与在精益计划组中配置的颜色之间切换。</span><span class="sxs-lookup"><span data-stu-id="ab38e-152">The **Use theme colors** button on the **Board** tab of the Action Pane lets you switch between the application theme colors and the colors that are configured in the lean schedule group.</span></span> <span data-ttu-id="ab38e-153">对于每个时间段，产能条 (6) 表示该时间段有多少个可用小时数已加载看板作业。</span><span class="sxs-lookup"><span data-stu-id="ab38e-153">For each period, a capacity bar (6) indicates how many of the available hours for the period have been loaded with kanban jobs.</span></span> <span data-ttu-id="ab38e-154">如果时间段超负荷，产能条变厚且显示红色。</span><span class="sxs-lookup"><span data-stu-id="ab38e-154">If the period is overloaded, the capacity bar appears thicker and in red.</span></span> <span data-ttu-id="ab38e-155">所有这些功能都在**看板计划板**页顶部的操作窗格 (1) 的**看板**选项卡上提供。</span><span class="sxs-lookup"><span data-stu-id="ab38e-155">All these functions are available on the **Board** tab of the Action Pane (1) at the top of the **Kanban schedule board** page.</span></span>

## <a name="plan-unplanned-jobs"></a><span data-ttu-id="ab38e-156">计划未计划的作业</span><span class="sxs-lookup"><span data-stu-id="ab38e-156">Plan unplanned jobs</span></span>
<span data-ttu-id="ab38e-157">您可以从**计划未计划的作业**对话框计划未计划的看板作业。</span><span class="sxs-lookup"><span data-stu-id="ab38e-157">You can schedule unplanned kanban jobs from the **Plan unplanned jobs** dialog box.</span></span> <span data-ttu-id="ab38e-158">要打开此对话框，单击**未计划的作业**按钮，此时将显示当前未计划作业的数量。</span><span class="sxs-lookup"><span data-stu-id="ab38e-158">To open this dialog box, click the **Unplanned jobs** button that shows the current number of unplanned jobs.</span></span> <span data-ttu-id="ab38e-159">或者单击操作窗格**看板**选项卡上的**计划未计划的作业**。</span><span class="sxs-lookup"><span data-stu-id="ab38e-159">Alternatively, click **Plan unplanned jobs** on the **Board** tab of the Action Pane.</span></span> <span data-ttu-id="ab38e-160">对话框显示工作单元的未计划的看板作业的列表。</span><span class="sxs-lookup"><span data-stu-id="ab38e-160">The dialog box shows a list of the unplanned kanban jobs for the work cell.</span></span> <span data-ttu-id="ab38e-161">您可以使用**筛选器**字段筛选网格中的所有字段。</span><span class="sxs-lookup"><span data-stu-id="ab38e-161">You can use the **Filter** field to filter on all fields in the grid.</span></span> <span data-ttu-id="ab38e-162">例如，您可以筛选特定产品的看板作业。</span><span class="sxs-lookup"><span data-stu-id="ab38e-162">For example, you can filter on kanban jobs for a specific product.</span></span> <span data-ttu-id="ab38e-163">筛选您要计划的作业的列表后，在列表中进行选择，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="ab38e-163">After you have a filtered list of the jobs that you want to schedule, select them in the list, and then click **OK**.</span></span> <span data-ttu-id="ab38e-164">要使用自动规划来计划作业，将**自动规划**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="ab38e-164">To use automatic planning to schedule the jobs, set the **Automatic planning** option to **Yes**.</span></span> <span data-ttu-id="ab38e-165">在这种情况下，将根据作业的到期日期将作业计划到一个时间段。</span><span class="sxs-lookup"><span data-stu-id="ab38e-165">In this case, the jobs are scheduled into a period according to their due date.</span></span> <span data-ttu-id="ab38e-166">您可以按时间段计划作业。</span><span class="sxs-lookup"><span data-stu-id="ab38e-166">You can also schedule the jobs by period.</span></span> <span data-ttu-id="ab38e-167">只需在**时间段**字段中选择一个时间段。</span><span class="sxs-lookup"><span data-stu-id="ab38e-167">Just select a period in the **Period** field.</span></span> <span data-ttu-id="ab38e-168">下图显示**计划未计划的作业**对话框的示例。</span><span class="sxs-lookup"><span data-stu-id="ab38e-168">The following illustration shows an example of the **Plan unplanned jobs** dialog box.</span></span> 

![计划未计划的作业对话框](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a><span data-ttu-id="ab38e-170">在相同时间段中为看板作业排序</span><span class="sxs-lookup"><span data-stu-id="ab38e-170">Sequence kanban jobs within the same period</span></span>
<span data-ttu-id="ab38e-171">您可以更改一个时间段内的一个或多个所选作业的序列。</span><span class="sxs-lookup"><span data-stu-id="ab38e-171">You can change the sequence of one or more selected jobs within a period.</span></span> <span data-ttu-id="ab38e-172">如果您要确定一些作业在时间段内的优先级，此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="ab38e-172">This capability can be useful if you want to prioritize some jobs within the period.</span></span> <span data-ttu-id="ab38e-173">或者，您可能要对具有相同产品属性的作业排序，以优化作业执行。</span><span class="sxs-lookup"><span data-stu-id="ab38e-173">Alternatively, you might want to sequence jobs that have the same product attributes, to optimize job execution.</span></span> <span data-ttu-id="ab38e-174">您可以通过拖放操作，或者使用操作窗格**看板**选项卡上的**后退**和**前进**菜单项更改序列。</span><span class="sxs-lookup"><span data-stu-id="ab38e-174">You can change the sequence through a drag-and-drop operation, or by using the **Backward** and **Forward** menu items on the **Board** tab of the Action Pane.</span></span>

## <a name="reassign-kanban-jobs-across-periods"></a><span data-ttu-id="ab38e-175">跨时间段重新分配看板作业</span><span class="sxs-lookup"><span data-stu-id="ab38e-175">Reassign kanban jobs across periods</span></span>
<span data-ttu-id="ab38e-176">作业可以从一个时间段重新分配到另一个时间段。</span><span class="sxs-lookup"><span data-stu-id="ab38e-176">Jobs can be reassigned from one period to another.</span></span> <span data-ttu-id="ab38e-177">如果一个时间段超负荷，且您要将负荷平衡到具有备用产能的时间段，此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="ab38e-177">This capability can be useful if a period is overloaded and you want to level the load to periods that have spare capacity.</span></span> <span data-ttu-id="ab38e-178">您可以通过拖放操作，或者使用操作窗格**看板**选项卡上的**下一个时间段**和**上一个时间段**菜单项重新分配作业。</span><span class="sxs-lookup"><span data-stu-id="ab38e-178">You can reassign jobs through a drag-and-drop operation, or by using the **Next period** and **Previous period** menu items on the **Board** tab of the Action Pane.</span></span>

## <a name="open-the-kanban-schedule-board"></a><span data-ttu-id="ab38e-179">打开看板计划板</span><span class="sxs-lookup"><span data-stu-id="ab38e-179">Open the Kanban schedule board</span></span>
<span data-ttu-id="ab38e-180">您可以使用以下页面上的菜单项打开看板计划板：</span><span class="sxs-lookup"><span data-stu-id="ab38e-180">You can open the Kanban schedule board by using the menu item on the following pages:</span></span>

-   <span data-ttu-id="ab38e-181">**生产区域**页</span><span class="sxs-lookup"><span data-stu-id="ab38e-181">**Production area** page</span></span>
-   <span data-ttu-id="ab38e-182">**看板作业计划**页</span><span class="sxs-lookup"><span data-stu-id="ab38e-182">**Kanban jobs scheduling** page</span></span>
-   <span data-ttu-id="ab38e-183">**生产流可视化**页</span><span class="sxs-lookup"><span data-stu-id="ab38e-183">**Production flow visualization** page</span></span>


<a name="see-also"></a><span data-ttu-id="ab38e-184">请参阅</span><span class="sxs-lookup"><span data-stu-id="ab38e-184">See also</span></span>
--------

[<span data-ttu-id="ab38e-185">Lean manufacturing – 看板作业计划</span><span class="sxs-lookup"><span data-stu-id="ab38e-185">Lean manufacturing – Kanban job scheduling</span></span>](lean-manufacturing-kanban-job-scheduling.md)


