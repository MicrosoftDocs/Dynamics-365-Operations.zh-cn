---
title: 计划看板作业
description: 此程序是为特定工作单元调度处理看板作业而设计的。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5170fecf0190591d74f45d35fecc4472e7f5e900
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "359535"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="551e2-103">计划看板作业</span><span class="sxs-lookup"><span data-stu-id="551e2-103">Schedule kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="551e2-104">此程序是为特定工作单元调度处理看板作业而设计的。</span><span class="sxs-lookup"><span data-stu-id="551e2-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="551e2-105">创建该程序的先决条件是该程序为“在材料不可用的情况下特殊处理看板作业备用”。</span><span class="sxs-lookup"><span data-stu-id="551e2-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="551e2-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="551e2-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="551e2-107">此任务用于车间主管与生产计划主任共同使用看板管理。</span><span class="sxs-lookup"><span data-stu-id="551e2-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="551e2-108">为工作单元选择看板作业</span><span class="sxs-lookup"><span data-stu-id="551e2-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="551e2-109">转到“生产控制”>“看板管理”>“安排看板作业”。</span><span class="sxs-lookup"><span data-stu-id="551e2-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="551e2-110">展开“期间产能事实资料箱”</span><span class="sxs-lookup"><span data-stu-id="551e2-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="551e2-111">展开“看板事实资料箱”。</span><span class="sxs-lookup"><span data-stu-id="551e2-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="551e2-112">在“工作单元”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="551e2-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="551e2-113">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="551e2-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="551e2-114">选择 1250 号工作单元。</span><span class="sxs-lookup"><span data-stu-id="551e2-114">Select work cell 1250.</span></span> <span data-ttu-id="551e2-115">筛选资料之后将只展示 1250 号工作单元的工作情况。</span><span class="sxs-lookup"><span data-stu-id="551e2-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="551e2-116">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="551e2-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="551e2-117">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="551e2-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="551e2-118">在第一个可用期间内安排一个看板作业</span><span class="sxs-lookup"><span data-stu-id="551e2-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="551e2-119">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="551e2-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="551e2-120">在“无计划状态”列表中选择第一行。</span><span class="sxs-lookup"><span data-stu-id="551e2-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="551e2-121">“作业状态”字段中的可见图标为无计划状态。</span><span class="sxs-lookup"><span data-stu-id="551e2-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="551e2-122">单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="551e2-122">Click Schedule.</span></span>
    * <span data-ttu-id="551e2-123">在第一个可用期间内安排看板作业。</span><span class="sxs-lookup"><span data-stu-id="551e2-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="551e2-124">请注意该看板作业已转移到列表末尾，因为它已经添加到今天开始的这个期间。</span><span class="sxs-lookup"><span data-stu-id="551e2-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="551e2-125">如果从今天开始的期间已经预订完毕，该作业将转移到第一个可用期间。</span><span class="sxs-lookup"><span data-stu-id="551e2-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="551e2-126">在具体日期安排两个计划作业</span><span class="sxs-lookup"><span data-stu-id="551e2-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="551e2-127">在列表中，选择第一行 。</span><span class="sxs-lookup"><span data-stu-id="551e2-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="551e2-128">请查看“作业状态”字段中显示“无计划状态”的第一行。</span><span class="sxs-lookup"><span data-stu-id="551e2-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="551e2-129">在列表中，选择第 2 行。</span><span class="sxs-lookup"><span data-stu-id="551e2-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="551e2-130">请查看“作业状态”字段中显示“无计划状态”的第二行。</span><span class="sxs-lookup"><span data-stu-id="551e2-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="551e2-131">现在您已经选择了第一行的两个作业。</span><span class="sxs-lookup"><span data-stu-id="551e2-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="551e2-132">单击“日期安排”打开下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="551e2-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="551e2-133">选中或取消选中“覆盖产能短缺反应箱”。</span><span class="sxs-lookup"><span data-stu-id="551e2-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="551e2-134">此选项允许覆盖默认产能短缺反应。</span><span class="sxs-lookup"><span data-stu-id="551e2-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="551e2-135">在“产能短缺反应”字段中，选择“添加到请求期间”。</span><span class="sxs-lookup"><span data-stu-id="551e2-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="551e2-136">此选项确保该作业添加到所请求的期间，无论该工作单元是否出现超负荷状态。</span><span class="sxs-lookup"><span data-stu-id="551e2-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="551e2-137">单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="551e2-137">Click Schedule.</span></span>
    * <span data-ttu-id="551e2-138">请注意这两个作业都添加到了预期期间。</span><span class="sxs-lookup"><span data-stu-id="551e2-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="551e2-139">在“期间产能”部分中，可查看每个期间的工作量。</span><span class="sxs-lookup"><span data-stu-id="551e2-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="551e2-140">“消耗量”字段显示该期间内的预定消耗量。</span><span class="sxs-lookup"><span data-stu-id="551e2-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="551e2-141">如果该期间内预定消耗量高于可用消耗量，将选择超负荷消耗量。</span><span class="sxs-lookup"><span data-stu-id="551e2-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  

