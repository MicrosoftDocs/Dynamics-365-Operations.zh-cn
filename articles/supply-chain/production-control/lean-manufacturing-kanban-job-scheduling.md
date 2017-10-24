---
title: "Lean manufacturing 的 看板作业计划"
description: "文本提供有关看板作业计划和各种看板作业计划方法的可视化控制的信息。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a8b2949fde28d83968f45535a5c47f263efbb18f
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a><span data-ttu-id="d0898-103">Lean manufacturing 的 看板作业计划</span><span class="sxs-lookup"><span data-stu-id="d0898-103">Kanban job scheduling for lean manufacturing</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d0898-104">文本提供有关看板作业计划和各种看板作业计划方法的可视化控制的信息。</span><span class="sxs-lookup"><span data-stu-id="d0898-104">This article provides information about visual control over kanban job scheduling and various ways to schedule kanban jobs.</span></span>  

<span data-ttu-id="d0898-105">**“看板作业计划”**页提供了对 lean manufacturing 工作单元的计划的可视化控制。</span><span class="sxs-lookup"><span data-stu-id="d0898-105">The **Kanban job scheduling** page provides visual control over the schedules of lean manufacturing work cells.</span></span> <span data-ttu-id="d0898-106">它概述了所有看板作业并提供了多种筛选功能。</span><span class="sxs-lookup"><span data-stu-id="d0898-106">It gives an overview of all kanban jobs and provides multiple filtering capabilities.</span></span> <span data-ttu-id="d0898-107">您可以从该页移至所有其他与看板配置和执行相关的页面。</span><span class="sxs-lookup"><span data-stu-id="d0898-107">From this page, you can move to all other pages that are related to kanban configuration and execution.</span></span>

## <a name="automatic-scheduling-of-kanban-jobs"></a><span data-ttu-id="d0898-108">自动计划看板作业</span><span class="sxs-lookup"><span data-stu-id="d0898-108">Automatic scheduling of kanban jobs</span></span>
<span data-ttu-id="d0898-109">如果您在看板规则上设置**自动计划数量**参数，则会自动触发计划。</span><span class="sxs-lookup"><span data-stu-id="d0898-109">Scheduling can be triggered automatically if you set the **Automatic planning quantity** parameter on the kanban rule.</span></span> <span data-ttu-id="d0898-110">如果您将**自动计划数量**设置为 <**1**，则会在创建每个看板作业后立即计划该作业。</span><span class="sxs-lookup"><span data-stu-id="d0898-110">If you set **Automatic planning quantity** to **1**, each kanban job is planned immediately when it's created.</span></span> <span data-ttu-id="d0898-111">该结果为一系列先拉先运行操作。</span><span class="sxs-lookup"><span data-stu-id="d0898-111">The result is a series of first pull, first serve operations.</span></span> <span data-ttu-id="d0898-112">如果您将**“自动计划数量”**设置为一个大于 1 的值，则会先对看板作业进行分组，然后再计划这些看板作业。</span><span class="sxs-lookup"><span data-stu-id="d0898-112">If you set **Automatic planning quantity** to a value that is more than 1, kanban jobs are grouped before they are planned.</span></span> 

<span data-ttu-id="d0898-113">此概念支持减小看板大小，直至其小于实际经济批次大小。</span><span class="sxs-lookup"><span data-stu-id="d0898-113">This concept enables kanban sizes to be reduced below the actual economic batch sizes.</span></span> <span data-ttu-id="d0898-114">例如，某个特定物料（或物料系列）的经济批次大小为 30。</span><span class="sxs-lookup"><span data-stu-id="d0898-114">For example, the economic batch size for a specific item (or item family) is 30.</span></span> <span data-ttu-id="d0898-115">您可以配置看板规则，使其产品数量为 10 且**自动计划数量**值为 **3**，而不是创建使用产品数量 30 的看板。</span><span class="sxs-lookup"><span data-stu-id="d0898-115">Instead of creating kanbans that use the product quantity, 30, you can configure the kanban rule so that it has a product quantity of 10 and an **Automatic planning quantity** value of **3**.</span></span> <span data-ttu-id="d0898-116">虽然自动计划仅在存在 3 个未计划的作业时为工作单元计划看板作业，但规划员或车间经理可以很清楚地知道，两个未计划的作业可能正在等待执行。</span><span class="sxs-lookup"><span data-stu-id="d0898-116">Although automatic planning schedules the kanban jobs for the work cell only when three unplanned jobs exist, it's fully transparent to the planner and the shop floor supervisor that two unplanned jobs might be awaiting execution.</span></span> <span data-ttu-id="d0898-117">随后，规划员或车间经理可通过手动计划这两个作业或创建附加看板来将二者投入生产中。</span><span class="sxs-lookup"><span data-stu-id="d0898-117">The planner or shop floor manager can then take those two jobs into production by manually planning them or creating additional kanbans.</span></span>

## <a name="manual-scheduling"></a><span data-ttu-id="d0898-118">手动计划</span><span class="sxs-lookup"><span data-stu-id="d0898-118">Manual scheduling</span></span>
<span data-ttu-id="d0898-119">对于手动计划，Microsoft Dynamics AX 2012 引入了看板计划板。</span><span class="sxs-lookup"><span data-stu-id="d0898-119">For manual scheduling, Microsoft Dynamics AX 2012 introduced the kanban scheduling board.</span></span> <span data-ttu-id="d0898-120">手动计划可与自动计划结合使用。</span><span class="sxs-lookup"><span data-stu-id="d0898-120">Manual scheduling can be combined with automatic scheduling.</span></span> <span data-ttu-id="d0898-121">利用看板计划板，您可以计划和取消计划作业、按顺序移动作业或在各个期间之间移动作业。</span><span class="sxs-lookup"><span data-stu-id="d0898-121">The kanban scheduling board lets you plan and unplan jobs, moved them in sequence, or move them from period to period.</span></span> <span data-ttu-id="d0898-122">可手动取消计划基于看板规则（其中，**“自动计划”**值大于 **0**）的作业。</span><span class="sxs-lookup"><span data-stu-id="d0898-122">Jobs that are based on a kanban rule where the **Automatic planning** value is more than **0** can be manually unplanned.</span></span> <span data-ttu-id="d0898-123">但是，在下一个自动计划事件发生时（即，在创建新的看板时），将重新计划这些作业。</span><span class="sxs-lookup"><span data-stu-id="d0898-123">However, these jobs will be replanned when the next automatic planning event occurs (that is, when a new kanban is created).</span></span> <span data-ttu-id="d0898-124">以下选项可用于手动计划：</span><span class="sxs-lookup"><span data-stu-id="d0898-124">The following options are available for manual scheduling:</span></span>

-   <span data-ttu-id="d0898-125">**计划** 根据所选作业的到期日期计划这些作业。</span><span class="sxs-lookup"><span data-stu-id="d0898-125">**Schedule** schedules the selected jobs according to their due date.</span></span> <span data-ttu-id="d0898-126">（此选项与自动计划类似。）</span><span class="sxs-lookup"><span data-stu-id="d0898-126">(This option resembles automatic planning.)</span></span>
-   <span data-ttu-id="d0898-127">**从某一日期正推时间表** 尝试根据所选作业的到期日期计划这些作业，但会使用指定的最早开始日期来约束结果。</span><span class="sxs-lookup"><span data-stu-id="d0898-127">**Schedule forward from date** tries to schedule the selected jobs according to their due date but constrains the result by using the specified earliest start date.</span></span>
-   <span data-ttu-id="d0898-128">**延后** 在期间内序列中将所选计划作业移后。</span><span class="sxs-lookup"><span data-stu-id="d0898-128">**Backward** moves the selected scheduled jobs back in the sequence within the period.</span></span>
-   <span data-ttu-id="d0898-129">**向前** 在期间内序列中将所选计划作业移前。</span><span class="sxs-lookup"><span data-stu-id="d0898-129">**Forward** moves the selected scheduled jobs forward in the sequence with the period.</span></span>
-   <span data-ttu-id="d0898-130">**上一期间** 将所选计划作业移到上一期间的开始日期或结束日期。</span><span class="sxs-lookup"><span data-stu-id="d0898-130">**Previous period** moves the selected scheduled jobs to the start or end of the previous period.</span></span>
-   <span data-ttu-id="d0898-131">**下一期间** 将所选计划作业移到下一期间的开始日期或结束日期。</span><span class="sxs-lookup"><span data-stu-id="d0898-131">**Next period** moves the selected scheduled jobs to the start or end of the next period.</span></span>
-   <span data-ttu-id="d0898-132">**计划** &gt; **恢复作业状态**可让您取消计划已计划的作业。</span><span class="sxs-lookup"><span data-stu-id="d0898-132">**Plan** &gt; **Revert job status** lets you unschedule a scheduled job.</span></span>

## <a name="lean-scheduling-groups"></a><span data-ttu-id="d0898-133">精益计划组</span><span class="sxs-lookup"><span data-stu-id="d0898-133">Lean scheduling groups</span></span>
<span data-ttu-id="d0898-134">每种颜色均代表一个精益计划组。</span><span class="sxs-lookup"><span data-stu-id="d0898-134">Each color represents a lean scheduling group.</span></span> <span data-ttu-id="d0898-135">可随意将精益计划组定义为通用组或属于单个工作单元的组。</span><span class="sxs-lookup"><span data-stu-id="d0898-135">Lean scheduling groups can be freely defined as generic groups or as groups that belong to a single work cell.</span></span> <span data-ttu-id="d0898-136">可随意将物料和维度分配给计划组。</span><span class="sxs-lookup"><span data-stu-id="d0898-136">Items and dimensions can be freely assigned to the scheduling groups.</span></span> <span data-ttu-id="d0898-137">例如，在“上漆”单元中，一个计划组可代表一种产品颜色。</span><span class="sxs-lookup"><span data-stu-id="d0898-137">For example, in a Painting cell, a schedule group can represent a color of the product.</span></span> <span data-ttu-id="d0898-138">在由特定的工具要求驱动的工作中，可按工具要求对物料分组，并且包装工作单元可按包装模板对物料进行分组。</span><span class="sxs-lookup"><span data-stu-id="d0898-138">In work that is driven by specific tooling requirements, items might be grouped by tool requirement, and a packaging work cell might group items by packaging template.</span></span> <span data-ttu-id="d0898-139">虽然对精益计划组使用颜色是一项可选操作，但建议执行此操作。</span><span class="sxs-lookup"><span data-stu-id="d0898-139">The use of colors for lean scheduling groups is optional but recommended.</span></span> <span data-ttu-id="d0898-140">它将提高计划状态的可见性。</span><span class="sxs-lookup"><span data-stu-id="d0898-140">It improves visibility into the status of the plan.</span></span> <span data-ttu-id="d0898-141">例如，可以很轻松地看到哪些颜色在哪一天生成，并且您可以快速说明此工作的优化方式。</span><span class="sxs-lookup"><span data-stu-id="d0898-141">For example, it's very easy to see which colors are produced on which day, and you can tell at a glance how this work can be optimized.</span></span>

## <a name="work-cell-capacity-and-period-capacity"></a><span data-ttu-id="d0898-142">工作单元产能和期间产能</span><span class="sxs-lookup"><span data-stu-id="d0898-142">Work cell capacity and period capacity</span></span>
<span data-ttu-id="d0898-143">精益工作单元的产能始终是并发产能。</span><span class="sxs-lookup"><span data-stu-id="d0898-143">The capacity of a lean work cell is always concurrent capacity.</span></span> <span data-ttu-id="d0898-144">换句话说，多个作业可在一个工作单元中同时处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="d0898-144">In other words, multiple jobs can be active in a work cell at the same time.</span></span> <span data-ttu-id="d0898-145">可在两种模式中跟踪产能：吞吐量和工时数。</span><span class="sxs-lookup"><span data-stu-id="d0898-145">The capacity can be tracked in two modes: throughput and hours.</span></span>

### <a name="throughput"></a><span data-ttu-id="d0898-146">吞吐量</span><span class="sxs-lookup"><span data-stu-id="d0898-146">Throughput</span></span>

<span data-ttu-id="d0898-147">工作单元的产能由引用期间（标准工作日、周或月）的平均吞吐量定义。</span><span class="sxs-lookup"><span data-stu-id="d0898-147">The capacity of a work cell is defined by the average throughput quantity of a reference period (standard workday, week, or month).</span></span> <span data-ttu-id="d0898-148">随后，根据分配给工作单元的日历的工作时间来按天或周计算实际产能。</span><span class="sxs-lookup"><span data-stu-id="d0898-148">The actual capacity per day or week is then calculated based on the working times of the calendar that is assigned to the work cell.</span></span> <span data-ttu-id="d0898-149">按作业加载的产能为作业的数量，并已按照工作单元中物料的吞吐率进行调整。</span><span class="sxs-lookup"><span data-stu-id="d0898-149">The capacity that is loaded by job is the quantity of the job, adjusted by the throughput ratio of the item in the work cell.</span></span>

### <a name="hours"></a><span data-ttu-id="d0898-150">工时数</span><span class="sxs-lookup"><span data-stu-id="d0898-150">Hours</span></span>

<span data-ttu-id="d0898-151">按天或周的可用产能由分配给工作单元的日历定义。</span><span class="sxs-lookup"><span data-stu-id="d0898-151">The available capacity by day or week is defined by the calendar that is assigned to the work cell.</span></span> <span data-ttu-id="d0898-152">按作业加载的产能为活动的周期时间，并已按照工作单元中物料的数量（默认活动数量和实际作业数量）和吞吐率进行调整。</span><span class="sxs-lookup"><span data-stu-id="d0898-152">The capacity that is loaded by job is the cycle time of the activity, adjusted by the quantity (default activity quantity versus actual job quantity) and the throughput ratio of the item in the work cell.</span></span>

#### <a name="period-capacity-factbox"></a><span data-ttu-id="d0898-153">期间产能速见表</span><span class="sxs-lookup"><span data-stu-id="d0898-153">Period capacity FactBox</span></span>

<span data-ttu-id="d0898-154">**“看板作业计划”**列表页包含一个速见表，此表显示所选工作单元的可用和预订的期间产能。</span><span class="sxs-lookup"><span data-stu-id="d0898-154">The **Kanban job scheduling** list page contains a FactBox that shows the available and booked period capacity for the selected work cell.</span></span> <span data-ttu-id="d0898-155">根据生产流模型中的所选计划期间，期间将显示天数或周数。</span><span class="sxs-lookup"><span data-stu-id="d0898-155">Depending on the selected schedule periods in the production flow model, the periods show days or weeks.</span></span>

<a name="see-also"></a><span data-ttu-id="d0898-156">请参阅</span><span class="sxs-lookup"><span data-stu-id="d0898-156">See also</span></span>
--------




