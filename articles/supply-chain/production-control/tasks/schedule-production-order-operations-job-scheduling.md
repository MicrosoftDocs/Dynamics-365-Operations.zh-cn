---
title: 使用工序级和作业级计划来计划生产订单
description: 此主题的重点是使用工序级排产和作业级排产计划生产订单。
author: ChristianRytt
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3023d6a6fe09c84b47839a2c4b78c37907754ded
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914876"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="0bc32-103">使用工序级和作业级计划来计划生产订单</span><span class="sxs-lookup"><span data-stu-id="0bc32-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0bc32-104">此主题的重点是使用工序级排产和作业级排产计划生产订单。</span><span class="sxs-lookup"><span data-stu-id="0bc32-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="0bc32-105">不使用工序级排产创建作业，而使用作业级排产创建。</span><span class="sxs-lookup"><span data-stu-id="0bc32-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="0bc32-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="0bc32-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="0bc32-107">此过程适用于在离散制造环境中工作的生产经理、生产规划员或车间主管。</span><span class="sxs-lookup"><span data-stu-id="0bc32-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="0bc32-108">创建生产订单</span><span class="sxs-lookup"><span data-stu-id="0bc32-108">Create a production order</span></span>
1. <span data-ttu-id="0bc32-109">在导航窗格中，转到**模块 > 生产控制 > 生产订单 > 所有生产订单**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="0bc32-110">选择**新建生产订单**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-110">Select **New production order**.</span></span>
3. <span data-ttu-id="0bc32-111">在**物料编号**字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0bc32-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="0bc32-112">选择物料编号 **D0001**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="0bc32-113">选择**创建**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="0bc32-114">为生产订单计划工序</span><span class="sxs-lookup"><span data-stu-id="0bc32-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="0bc32-115">标记新建的行。</span><span class="sxs-lookup"><span data-stu-id="0bc32-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="0bc32-116">在操作窗格上，选择**计划**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="0bc32-117">选择**计划工序**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="0bc32-118">在**计划的方向**字段中，选择**从计划日期正推**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="0bc32-119">在**计划日期**字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="0bc32-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="0bc32-120">选择一个将来的日期，例如，今天加上一周。</span><span class="sxs-lookup"><span data-stu-id="0bc32-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="0bc32-121">使用所选的计划的方向，将安排将生产订单从此日期正推。</span><span class="sxs-lookup"><span data-stu-id="0bc32-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="0bc32-122">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-122">Select **OK**.</span></span>
7. <span data-ttu-id="0bc32-123">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="0bc32-123">In the list, mark the selected row.</span></span> <span data-ttu-id="0bc32-124">请注意，状态更改为**已计划**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="0bc32-125">选择**所有作业**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-125">Select **All jobs**.</span></span> <span data-ttu-id="0bc32-126">请注意，没有使用工序级排产创建作业。</span><span class="sxs-lookup"><span data-stu-id="0bc32-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="0bc32-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="0bc32-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="0bc32-128">为生产订单计划作业</span><span class="sxs-lookup"><span data-stu-id="0bc32-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="0bc32-129">在操作窗格上，选择**计划**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="0bc32-130">选择**计划作业**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="0bc32-131">在**计划的方向**字段中，选择**从计划日期正推**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="0bc32-132">在**计划日期**字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="0bc32-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="0bc32-133">选择一个将来的日期，例如，今天加上一周。</span><span class="sxs-lookup"><span data-stu-id="0bc32-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="0bc32-134">使用所选的计划的方向，将安排将生产订单从此日期正推。</span><span class="sxs-lookup"><span data-stu-id="0bc32-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="0bc32-135">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-135">Select **OK**.</span></span>
6. <span data-ttu-id="0bc32-136">在操作窗格中，选择**生产订单**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="0bc32-137">选择**所有作业**。</span><span class="sxs-lookup"><span data-stu-id="0bc32-137">Select **All jobs**.</span></span> <span data-ttu-id="0bc32-138">请注意，根据有效的工艺路线，通过作业级排产创建 5 个作业。</span><span class="sxs-lookup"><span data-stu-id="0bc32-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

