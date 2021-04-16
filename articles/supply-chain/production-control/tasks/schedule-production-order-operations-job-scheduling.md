---
title: 使用工序级和作业级计划来计划生产订单
description: 此主题的重点是使用工序级排产和作业级排产计划生产订单。
author: ChristianRytt
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 883a68af78a9d91df089d30d8f1b3d7ba498d577
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841375"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="331aa-103">使用工序级和作业级计划来计划生产订单</span><span class="sxs-lookup"><span data-stu-id="331aa-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="331aa-104">此主题的重点是使用工序级排产和作业级排产计划生产订单。</span><span class="sxs-lookup"><span data-stu-id="331aa-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="331aa-105">不使用工序级排产创建作业，而使用作业级排产创建。</span><span class="sxs-lookup"><span data-stu-id="331aa-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="331aa-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="331aa-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="331aa-107">此过程适用于在离散制造环境中工作的生产经理、生产规划员或车间主管。</span><span class="sxs-lookup"><span data-stu-id="331aa-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="331aa-108">创建生产订单</span><span class="sxs-lookup"><span data-stu-id="331aa-108">Create a production order</span></span>
1. <span data-ttu-id="331aa-109">在导航窗格中，转到 **模块 > 生产控制 > 生产订单 > 所有生产订单**。</span><span class="sxs-lookup"><span data-stu-id="331aa-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="331aa-110">选择 **新建生产订单**。</span><span class="sxs-lookup"><span data-stu-id="331aa-110">Select **New production order**.</span></span>
3. <span data-ttu-id="331aa-111">在 **物料编号** 字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="331aa-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="331aa-112">选择物料编号 **D0001**。</span><span class="sxs-lookup"><span data-stu-id="331aa-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="331aa-113">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="331aa-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="331aa-114">为生产订单计划工序</span><span class="sxs-lookup"><span data-stu-id="331aa-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="331aa-115">标记新建的行。</span><span class="sxs-lookup"><span data-stu-id="331aa-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="331aa-116">在操作窗格上，选择 **计划**。</span><span class="sxs-lookup"><span data-stu-id="331aa-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="331aa-117">选择 **计划工序**。</span><span class="sxs-lookup"><span data-stu-id="331aa-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="331aa-118">在 **计划的方向** 字段中，选择 **从计划日期正推**。</span><span class="sxs-lookup"><span data-stu-id="331aa-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="331aa-119">在 **计划日期** 字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="331aa-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="331aa-120">选择一个将来的日期，例如，今天加上一周。</span><span class="sxs-lookup"><span data-stu-id="331aa-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="331aa-121">使用所选的计划的方向，将安排将生产订单从此日期正推。</span><span class="sxs-lookup"><span data-stu-id="331aa-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="331aa-122">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="331aa-122">Select **OK**.</span></span>
7. <span data-ttu-id="331aa-123">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="331aa-123">In the list, mark the selected row.</span></span> <span data-ttu-id="331aa-124">请注意，状态更改为 **已计划**。</span><span class="sxs-lookup"><span data-stu-id="331aa-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="331aa-125">选择 **所有作业**。</span><span class="sxs-lookup"><span data-stu-id="331aa-125">Select **All jobs**.</span></span> <span data-ttu-id="331aa-126">请注意，没有使用工序级排产创建作业。</span><span class="sxs-lookup"><span data-stu-id="331aa-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="331aa-127">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="331aa-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="331aa-128">为生产订单计划作业</span><span class="sxs-lookup"><span data-stu-id="331aa-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="331aa-129">在操作窗格上，选择 **计划**。</span><span class="sxs-lookup"><span data-stu-id="331aa-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="331aa-130">选择 **计划作业**。</span><span class="sxs-lookup"><span data-stu-id="331aa-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="331aa-131">在 **计划的方向** 字段中，选择 **从计划日期正推**。</span><span class="sxs-lookup"><span data-stu-id="331aa-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="331aa-132">在 **计划日期** 字段中，输入日期。</span><span class="sxs-lookup"><span data-stu-id="331aa-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="331aa-133">选择一个将来的日期，例如，今天加上一周。</span><span class="sxs-lookup"><span data-stu-id="331aa-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="331aa-134">使用所选的计划的方向，将安排将生产订单从此日期正推。</span><span class="sxs-lookup"><span data-stu-id="331aa-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="331aa-135">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="331aa-135">Select **OK**.</span></span>
6. <span data-ttu-id="331aa-136">在操作窗格中，选择 **生产订单**。</span><span class="sxs-lookup"><span data-stu-id="331aa-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="331aa-137">选择 **所有作业**。</span><span class="sxs-lookup"><span data-stu-id="331aa-137">Select **All jobs**.</span></span> <span data-ttu-id="331aa-138">请注意，根据有效的工艺路线，通过作业级排产创建 5 个作业。</span><span class="sxs-lookup"><span data-stu-id="331aa-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]