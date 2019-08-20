---
title: 移动计划的看板作业
description: 此程序用于将计划特殊处理的看板作业转移到另一个不同期间。
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2526c2bd106e35c736e930b5b5114d019718dc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836232"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="da847-103">移动计划的看板作业</span><span class="sxs-lookup"><span data-stu-id="da847-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da847-104">此程序用于将计划特殊处理的看板作业转移到另一个不同期间。</span><span class="sxs-lookup"><span data-stu-id="da847-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="da847-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="da847-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="da847-106">此程序用于车间主管与生产计划主任共同使用看板管理。</span><span class="sxs-lookup"><span data-stu-id="da847-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="da847-107">选择计划看板作业。</span><span class="sxs-lookup"><span data-stu-id="da847-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="da847-108">转到**生产控制 > 看板 > 安排看板作业**。</span><span class="sxs-lookup"><span data-stu-id="da847-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="da847-109">在**工作单元**字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="da847-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="da847-110">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="da847-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="da847-111">选择 1250 号工作单元。</span><span class="sxs-lookup"><span data-stu-id="da847-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="da847-112">单击**选择**。</span><span class="sxs-lookup"><span data-stu-id="da847-112">Click **Select**.</span></span> 

5. <span data-ttu-id="da847-113">在**显示作业状态**字段中，选择**预定作业**。</span><span class="sxs-lookup"><span data-stu-id="da847-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="da847-114">筛选作业列表，仅显示计划看板作业。</span><span class="sxs-lookup"><span data-stu-id="da847-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="da847-115">将看板作业转移到另一个不同期间。</span><span class="sxs-lookup"><span data-stu-id="da847-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="da847-116">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="da847-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="da847-117">选择一个**计划作业**状态的作业，例如，在**计划期间**字段中安排于 2012 年 12 月 20 日的作业。</span><span class="sxs-lookup"><span data-stu-id="da847-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="da847-118">然后将该作业转移到上一个期间。</span><span class="sxs-lookup"><span data-stu-id="da847-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="da847-119">单击**上一期间**。</span><span class="sxs-lookup"><span data-stu-id="da847-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="da847-120">单击**结束**可将该作业转移到作业列表的末尾，作为上一个期间的最后一个作业。</span><span class="sxs-lookup"><span data-stu-id="da847-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="da847-121">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="da847-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="da847-122">选择一个**计划作业**状态的作业，例如，在**计划期间**字段中安排于 2012 年 12 月 18 日的作业。</span><span class="sxs-lookup"><span data-stu-id="da847-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="da847-123">然后将该作业转移到下一个期间。</span><span class="sxs-lookup"><span data-stu-id="da847-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="da847-124">单击**下一期间**。</span><span class="sxs-lookup"><span data-stu-id="da847-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="da847-125">单击**开始**可将该作业转移到作业列表的开头，作为上一个期间的第一个作业。</span><span class="sxs-lookup"><span data-stu-id="da847-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="da847-126">将一个作业转移到一个期间内。</span><span class="sxs-lookup"><span data-stu-id="da847-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="da847-127">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="da847-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="da847-128">选择一个“计划作业状态”的作业，例如，在**计划期间**字段中安排于 2012 年 12 月 19 日的作业。</span><span class="sxs-lookup"><span data-stu-id="da847-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="da847-129">然后将该作业转移到计划期间。</span><span class="sxs-lookup"><span data-stu-id="da847-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="da847-130">单击**正推**。</span><span class="sxs-lookup"><span data-stu-id="da847-130">Click **Forward**.</span></span> <span data-ttu-id="da847-131">请注意该作业将转移到列表的下一行。</span><span class="sxs-lookup"><span data-stu-id="da847-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="da847-132">单击**后退**。</span><span class="sxs-lookup"><span data-stu-id="da847-132">Click **Backward**.</span></span> <span data-ttu-id="da847-133">请注意该作业将转移到列表的上一行。</span><span class="sxs-lookup"><span data-stu-id="da847-133">Notice that the job is moved one line up on the list.</span></span>
