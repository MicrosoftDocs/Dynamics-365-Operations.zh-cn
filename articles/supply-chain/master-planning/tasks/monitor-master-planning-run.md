---
title: 监控主计划运行
description: 本主题说明生产规划员如何查看主计划运行是否正在进行。
author: josaw1
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1733562768b3fe869f326bbfb47b6135a91b5cb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829634"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="e3bfc-103">监控主计划运行</span><span class="sxs-lookup"><span data-stu-id="e3bfc-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="e3bfc-104">使用甘特图可视化主计划进度</span><span class="sxs-lookup"><span data-stu-id="e3bfc-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="e3bfc-105">在 **查看主计划进度** 页面上，您可以甘特图形式查看历史主计划运行的详细信息。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="e3bfc-106">此功能可以帮助您了解在主计划的各个阶段花费的时间。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="e3bfc-107">对于当前的活动计划作业，可以使用 **查看主计划进度** 页面来跟踪进度并查看估计的剩余时间。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="e3bfc-108">打开和使用主计划进度可视化功能</span><span class="sxs-lookup"><span data-stu-id="e3bfc-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="e3bfc-109">要使用此功能，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="e3bfc-110">在 **功能管理** 工作区中的 **新** 选项卡上，在列表中选择 **主计划进度可视化**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="e3bfc-111">如果该功能未出现在 **新** 选项卡上，请查看 **未启用** 和 **所有** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="e3bfc-112">选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-112">Select **Enable now**.</span></span> <span data-ttu-id="e3bfc-113">或者，选择 **时间表**，然后选择要启用该功能的时间。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="e3bfc-114">**查看主计划进度** 页面可以显示历史计划作业和活动计划作业。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="e3bfc-115">要查看历史计划作业，有两个选项。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="e3bfc-116">转到 **主计划 \> 设置 \> 计划 \> 主计划**，然后在操作窗格上选择 **历史记录**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="e3bfc-117">选择所需作业后，选择 **查询**，然后选择 **查看进度**</span><span class="sxs-lookup"><span data-stu-id="e3bfc-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="e3bfc-118">转到 **主计划 \> 工作区 \> 主计划**，在主计划磁贴上，单击 **历史记录**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="e3bfc-119">选择所需作业后，选择 **查询**，然后选择 **查看进度**</span><span class="sxs-lookup"><span data-stu-id="e3bfc-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="e3bfc-120">要查看活动计划作业，有两个选项。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="e3bfc-121">转到 **主计划 \> 工作区 \> 主计划**，在操作窗格上，选择 **未完成的计划流程**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="e3bfc-122">选择所需的作业后，选择 **查询**，然后选择 **查看进度**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="e3bfc-123">转到 **主计划 \> 工作区 \> 主计划**，在主计划磁贴上，单击 **查看进度**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="e3bfc-124">选择所需作业后，选择 **查询**，然后选择 **查看进度**</span><span class="sxs-lookup"><span data-stu-id="e3bfc-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="e3bfc-125">请注意，仅当正在处理计划作业时，才能查看活动作业。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="e3bfc-126">分析主计划作业</span><span class="sxs-lookup"><span data-stu-id="e3bfc-126">Analyze a master planning job</span></span>

<span data-ttu-id="e3bfc-127">在甘特图中，您可以展开以下每个计划流程以查看所花费时间的其他详细信息：</span><span class="sxs-lookup"><span data-stu-id="e3bfc-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="e3bfc-128">正在初始化</span><span class="sxs-lookup"><span data-stu-id="e3bfc-128">Initializing</span></span>
- <span data-ttu-id="e3bfc-129">正在删除和删除数据</span><span class="sxs-lookup"><span data-stu-id="e3bfc-129">Deleting and inserting data</span></span>
- <span data-ttu-id="e3bfc-130">覆盖范围计划</span><span class="sxs-lookup"><span data-stu-id="e3bfc-130">Coverage planning</span></span>
- <span data-ttu-id="e3bfc-131">延迟</span><span class="sxs-lookup"><span data-stu-id="e3bfc-131">Delays</span></span>
- <span data-ttu-id="e3bfc-132">行动消息</span><span class="sxs-lookup"><span data-stu-id="e3bfc-132">Action messages</span></span>
- <span data-ttu-id="e3bfc-133">最终完成</span><span class="sxs-lookup"><span data-stu-id="e3bfc-133">Finalization</span></span>
- <span data-ttu-id="e3bfc-134">自动固定</span><span class="sxs-lookup"><span data-stu-id="e3bfc-134">Auto-firming</span></span>

<span data-ttu-id="e3bfc-135">如果要查看使用操作消息的影响，甘特图是一个有用的工具。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="e3bfc-136">甘特图中的导航</span><span class="sxs-lookup"><span data-stu-id="e3bfc-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="e3bfc-137">要展开所选组并显示详细信息，请在树视图中选择加号 (**+**)。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="e3bfc-138">要折叠选定的组，请在树视图中选择减号 (**–**)。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="e3bfc-139">您可以使用键盘进行导航。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="e3bfc-140">使用 **向上箭头** 和 **向下箭头** 键在行之间移动。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="e3bfc-141">使用 **向右箭头** 和 **向左箭头** 键展开和折叠组。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="e3bfc-142">要打开或关闭甘特图中的所有级别，请选择 **全部展开** 或 **全部折叠**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="e3bfc-143">要查看相关的处理时间，将鼠标悬停在任务上。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="e3bfc-144">（任务是甘特图中的最低级别。）</span><span class="sxs-lookup"><span data-stu-id="e3bfc-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="e3bfc-145">查看其他主计划运行以比较作业</span><span class="sxs-lookup"><span data-stu-id="e3bfc-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="e3bfc-146">通过在 **显示其他主计划运行** 字段上选择一个主计划作业，您可以在甘特图中查看其他主计划运行并比较两个作业。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="e3bfc-147">BOM 级别显示</span><span class="sxs-lookup"><span data-stu-id="e3bfc-147">BOM-level display</span></span>

<span data-ttu-id="e3bfc-148">物料清单 (BOM) 级别对于覆盖范围计划、延迟、操作和确认的显示不同。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="e3bfc-149">**覆盖范围计划** – BOM 级别按预期显示。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="e3bfc-150">它们从上到下计算。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="e3bfc-151">**示例：** BOM 级别 0、1、2</span><span class="sxs-lookup"><span data-stu-id="e3bfc-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="e3bfc-152">**延迟** – BOM 级别显示为覆盖范围计划 BOM 级别乘以 –1。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="e3bfc-153">（换句话说，它们有一个负号。）</span><span class="sxs-lookup"><span data-stu-id="e3bfc-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="e3bfc-154">**示例：** BOM 级别 –2、–1、0</span><span class="sxs-lookup"><span data-stu-id="e3bfc-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="e3bfc-155">**操作消息** – BOM 级别按预期显示。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="e3bfc-156">它们从上到下计算。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="e3bfc-157">**示例：** BOM 级别 0、1、2</span><span class="sxs-lookup"><span data-stu-id="e3bfc-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="e3bfc-158">**自动确认** – BOM 级别显示为 999 减去覆盖范围计划 BOM 级别。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="e3bfc-159">**示例：** BOM 级别 999、998、997</span><span class="sxs-lookup"><span data-stu-id="e3bfc-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="e3bfc-160">下表汇总了此行为。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="e3bfc-161">显示的 BOM 级别</span><span class="sxs-lookup"><span data-stu-id="e3bfc-161">BOM level that is shown</span></span> | <span data-ttu-id="e3bfc-162">成品</span><span class="sxs-lookup"><span data-stu-id="e3bfc-162">End item</span></span> | <span data-ttu-id="e3bfc-163">子组件</span><span class="sxs-lookup"><span data-stu-id="e3bfc-163">Subcomponent</span></span> | <span data-ttu-id="e3bfc-164">原材料</span><span class="sxs-lookup"><span data-stu-id="e3bfc-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="e3bfc-165">覆盖范围计划</span><span class="sxs-lookup"><span data-stu-id="e3bfc-165">Coverage planning</span></span> | <span data-ttu-id="e3bfc-166">0</span><span class="sxs-lookup"><span data-stu-id="e3bfc-166">0</span></span> | <span data-ttu-id="e3bfc-167">1</span><span class="sxs-lookup"><span data-stu-id="e3bfc-167">1</span></span> | <span data-ttu-id="e3bfc-168">2</span><span class="sxs-lookup"><span data-stu-id="e3bfc-168">2</span></span> |
| <span data-ttu-id="e3bfc-169">延迟</span><span class="sxs-lookup"><span data-stu-id="e3bfc-169">Delays</span></span> | <span data-ttu-id="e3bfc-170">0</span><span class="sxs-lookup"><span data-stu-id="e3bfc-170">0</span></span> | <span data-ttu-id="e3bfc-171">–1</span><span class="sxs-lookup"><span data-stu-id="e3bfc-171">–1</span></span> | <span data-ttu-id="e3bfc-172">–2</span><span class="sxs-lookup"><span data-stu-id="e3bfc-172">–2</span></span> |
| <span data-ttu-id="e3bfc-173">行动消息</span><span class="sxs-lookup"><span data-stu-id="e3bfc-173">Action message</span></span> | <span data-ttu-id="e3bfc-174">0</span><span class="sxs-lookup"><span data-stu-id="e3bfc-174">0</span></span> | <span data-ttu-id="e3bfc-175">1</span><span class="sxs-lookup"><span data-stu-id="e3bfc-175">1</span></span> | <span data-ttu-id="e3bfc-176">2</span><span class="sxs-lookup"><span data-stu-id="e3bfc-176">2</span></span> |
| <span data-ttu-id="e3bfc-177">自动固定</span><span class="sxs-lookup"><span data-stu-id="e3bfc-177">Auto-firming</span></span> | <span data-ttu-id="e3bfc-178">999</span><span class="sxs-lookup"><span data-stu-id="e3bfc-178">999</span></span> | <span data-ttu-id="e3bfc-179">998</span><span class="sxs-lookup"><span data-stu-id="e3bfc-179">998</span></span> | <span data-ttu-id="e3bfc-180">997</span><span class="sxs-lookup"><span data-stu-id="e3bfc-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="e3bfc-181">可视化进度</span><span class="sxs-lookup"><span data-stu-id="e3bfc-181">Visualize progress</span></span>

<span data-ttu-id="e3bfc-182">如果查看当前正在运行的主计划作业，进度将通过甘特图中的颜色显示。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="e3bfc-183">以下颜色适用于蓝色主题。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="e3bfc-184">对于其他颜色主题，颜色将不同。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="e3bfc-185">**深蓝色** – 完成的计划任务。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="e3bfc-186">**橙色** – 当前正在进行的任务。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="e3bfc-187">**浅蓝色** – 剩余任务的估计值。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="e3bfc-188">颜色仅在甘特图的最低级别上显示。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="e3bfc-189">选择 **全部展开** 可以查看主计划作业中的所有任务。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="e3bfc-190">剩余任务的估计基于历史主计划作业。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="e3bfc-191">运行主计划和跟踪处理时间</span><span class="sxs-lookup"><span data-stu-id="e3bfc-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="e3bfc-192">在默认仪表板上，选择 **主计划**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="e3bfc-193">在 **计划** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="e3bfc-194">选择 **运行**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-194">Select **Run**.</span></span>
1. <span data-ttu-id="e3bfc-195">将 **跟踪处理时间** 选项设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="e3bfc-196">在 **线程数** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="e3bfc-197">在 **要包括的记录** 快速选项卡中，选择 **筛选**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="e3bfc-198">在网格中，选择将 **现场** 字段设置为 **物料编号** 的行。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="e3bfc-199">在 **条件** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="e3bfc-200">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e3bfc-200">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]