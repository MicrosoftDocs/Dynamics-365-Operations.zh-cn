--- 
title: "使用工序级和作业级排产计划生产订单"
description: "此过程的重点是使用工序级排产和作业级排产计划生产订单。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 0f443918890a36cebf5935b60ed66b495e5f353e
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="1e6c1-103">使用工序级和作业级排产计划生产订单</span><span class="sxs-lookup"><span data-stu-id="1e6c1-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e6c1-104">此过程的重点是使用工序级排产和作业级排产计划生产订单。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="1e6c1-105">不使用工序级排产创建作业，而使用作业级排产创建。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="1e6c1-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="1e6c1-107">此过程适用于在离散制造环境中工作的生产经理、生产规划员或车间主管。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="1e6c1-108">创建生产订单</span><span class="sxs-lookup"><span data-stu-id="1e6c1-108">Create a production order</span></span>
1. <span data-ttu-id="1e6c1-109">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="1e6c1-110">单击“新建生产订单”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-110">Click New production order.</span></span>
3. <span data-ttu-id="1e6c1-111">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="1e6c1-112">选择物料编号 D0001。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="1e6c1-113">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="1e6c1-114">为生产订单计划工序</span><span class="sxs-lookup"><span data-stu-id="1e6c1-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="1e6c1-115">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1e6c1-116">选择您刚才创建的生产订单。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-116">Select the production order that you have just created.</span></span> <span data-ttu-id="1e6c1-117">它应该在列表的顶部。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="1e6c1-118">在“操作窗格”上，单击“计划” 。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="1e6c1-119">单击“计划工序”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="1e6c1-120">在“计划的方向”字段中，选择“从计划日期正推”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="1e6c1-121">在“计划日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="1e6c1-122">选择一个将来的日期，例如，今天加上一周。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="1e6c1-123">使用所选的计划的方向，将安排将生产订单从此日期正推。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="1e6c1-124">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-124">Click OK.</span></span>
7. <span data-ttu-id="1e6c1-125">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1e6c1-126">请注意，状态更改为已计划</span><span class="sxs-lookup"><span data-stu-id="1e6c1-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="1e6c1-127">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1e6c1-128">单击“所有作业”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-128">Click All jobs.</span></span>
    * <span data-ttu-id="1e6c1-129">请注意，没有使用工序级排产创建作业。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="1e6c1-130">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="1e6c1-131">为生产订单计划作业</span><span class="sxs-lookup"><span data-stu-id="1e6c1-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="1e6c1-132">在“操作窗格”上，单击“计划” 。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="1e6c1-133">单击“计划作业”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="1e6c1-134">在“计划的方向”字段中，选择“从计划日期正推”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="1e6c1-135">在“计划日期”字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="1e6c1-136">选择一个将来的日期，例如，今天加上一周。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="1e6c1-137">使用所选的计划的方向，将安排将生产订单从此日期正推。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="1e6c1-138">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-138">Click OK.</span></span>
6. <span data-ttu-id="1e6c1-139">在操作窗格上单击“生产订单”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="1e6c1-140">单击“所有作业”。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-140">Click All jobs.</span></span>
    * <span data-ttu-id="1e6c1-141">请注意，根据有效的工艺路线，通过作业级排产创建 5 个作业。</span><span class="sxs-lookup"><span data-stu-id="1e6c1-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  


