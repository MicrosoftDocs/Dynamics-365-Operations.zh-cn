--- 
title: "移动计划的看板作业"
description: "此程序用于将计划特殊处理的看板作业转移到另一个不同期间。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a12a6859a3a436706822873bc6fdd781e0ef032
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="6e87c-103">移动计划的看板作业</span><span class="sxs-lookup"><span data-stu-id="6e87c-103">Move scheduled kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e87c-104">此程序用于将计划特殊处理的看板作业转移到另一个不同期间。</span><span class="sxs-lookup"><span data-stu-id="6e87c-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="6e87c-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="6e87c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6e87c-106">此程序用于车间主管与生产计划主任共同使用看板管理。</span><span class="sxs-lookup"><span data-stu-id="6e87c-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="6e87c-107">选择计划看板作业</span><span class="sxs-lookup"><span data-stu-id="6e87c-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="6e87c-108">转到“Produktionsstyring”>“看板”>“Tidsplanlægning af 看板作业”。</span><span class="sxs-lookup"><span data-stu-id="6e87c-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="6e87c-109">!MtCMR!在“工作单元”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="6e87c-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="6e87c-110">áçêìõý!</span><span class="sxs-lookup"><span data-stu-id="6e87c-110">áçêìõý !</span></span>
3. <span data-ttu-id="6e87c-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="6e87c-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="6e87c-112">选择 1250 号工作单元。</span><span class="sxs-lookup"><span data-stu-id="6e87c-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="6e87c-113">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="6e87c-113">Klik på Select.</span></span>
5. <span data-ttu-id="6e87c-114">Vælg 'Planlagt' i feltet 显示作业状态。</span><span class="sxs-lookup"><span data-stu-id="6e87c-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="6e87c-115">筛选作业列表，仅显示计划看板作业。</span><span class="sxs-lookup"><span data-stu-id="6e87c-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="6e87c-116">将看板作业转移到另一个不同期间</span><span class="sxs-lookup"><span data-stu-id="6e87c-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="6e87c-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6e87c-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="6e87c-118">选择一个“计划作业状态”的作业，例如，在“计划期间”字段中安排于 2012 年 12 月 20 日的作业。</span><span class="sxs-lookup"><span data-stu-id="6e87c-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="6e87c-119">然后将该作业转移到上一个期间。</span><span class="sxs-lookup"><span data-stu-id="6e87c-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="6e87c-120">单击“上一个期间”。</span><span class="sxs-lookup"><span data-stu-id="6e87c-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="6e87c-121">单击“结束”。</span><span class="sxs-lookup"><span data-stu-id="6e87c-121">Klik på End.</span></span>
    * <span data-ttu-id="6e87c-122">如此可将该作业转移到作业列表的末尾，作为上一个期间的最后一个作业。</span><span class="sxs-lookup"><span data-stu-id="6e87c-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="6e87c-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6e87c-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="6e87c-124">选择一个“计划作业状态”的作业，例如，在“计划期间”字段中安排于 2012 年 12 月 18 日的作业。</span><span class="sxs-lookup"><span data-stu-id="6e87c-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="6e87c-125">然后将该作业转移到下一个期间。</span><span class="sxs-lookup"><span data-stu-id="6e87c-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="6e87c-126">单击“下一个期间”。</span><span class="sxs-lookup"><span data-stu-id="6e87c-126">Klik på Next period.</span></span>
6. <span data-ttu-id="6e87c-127">单击“开始”。</span><span class="sxs-lookup"><span data-stu-id="6e87c-127">Klik på Start.</span></span>
    * <span data-ttu-id="6e87c-128">如此可将该作业转移到作业列表的开头，作为上一个期间的第一个作业。</span><span class="sxs-lookup"><span data-stu-id="6e87c-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="6e87c-129">任务：将一个作业转移到一个期间内</span><span class="sxs-lookup"><span data-stu-id="6e87c-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="6e87c-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="6e87c-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="6e87c-131">选择一个“计划作业状态”的作业，例如，在“计划期间”字段中安排于 2012 年 12 月 19 日的作业。</span><span class="sxs-lookup"><span data-stu-id="6e87c-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="6e87c-132">然后将该作业转移到计划期间。</span><span class="sxs-lookup"><span data-stu-id="6e87c-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="6e87c-133">单击“前进”。</span><span class="sxs-lookup"><span data-stu-id="6e87c-133">Klik på Forward.</span></span>
    * <span data-ttu-id="6e87c-134">请注意该作业将转移到列表的下一行。</span><span class="sxs-lookup"><span data-stu-id="6e87c-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="6e87c-135">单击“返回”。</span><span class="sxs-lookup"><span data-stu-id="6e87c-135">Klik på Backward.</span></span>
    * <span data-ttu-id="6e87c-136">请注意该作业将转移到列表的上一行。</span><span class="sxs-lookup"><span data-stu-id="6e87c-136">Notice that the job is moved one line up on the list.</span></span>  


