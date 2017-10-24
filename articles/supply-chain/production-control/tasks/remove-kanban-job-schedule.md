--- 
title: "从计划中删除看板作业"
description: "此程序用于通过恢复一个作业的“无计划”状态，从预定计划中移除该计划处理的看板作业。"
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
ms.openlocfilehash: 9a0f246bfe42dde0befdf5c4f01d2ad1e1200b12
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="cc359-103">从计划中删除看板作业</span><span class="sxs-lookup"><span data-stu-id="cc359-103">Remove a kanban job from the schedule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc359-104">此程序用于通过恢复一个作业的“无计划”状态，从预定计划中移除该计划处理的看板作业。</span><span class="sxs-lookup"><span data-stu-id="cc359-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="cc359-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="cc359-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cc359-106">此程序是为车间主管或生产计划主任而设计的。</span><span class="sxs-lookup"><span data-stu-id="cc359-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="cc359-107">查找一个计划看板作业。</span><span class="sxs-lookup"><span data-stu-id="cc359-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="cc359-108">转到“生产控制”>“看板管理”>“安排看板作业”。</span><span class="sxs-lookup"><span data-stu-id="cc359-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="cc359-109">在“工作单元”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="cc359-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cc359-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="cc359-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cc359-111">选择 1250 号工作单元。</span><span class="sxs-lookup"><span data-stu-id="cc359-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="cc359-112">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="cc359-112">Click Select.</span></span>
5. <span data-ttu-id="cc359-113">在“显示作业状态”字段中，选择“预定作业”。</span><span class="sxs-lookup"><span data-stu-id="cc359-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="cc359-114">从预定计划中移除该计划看板作业</span><span class="sxs-lookup"><span data-stu-id="cc359-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="cc359-115">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="cc359-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cc359-116">选择一个“计划状态”的作业，例如，开始于 2012 年 12 月 19 日的作业。</span><span class="sxs-lookup"><span data-stu-id="cc359-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="cc359-117">在操作窗格上，单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="cc359-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="cc359-118">单击“恢复作业原态”。</span><span class="sxs-lookup"><span data-stu-id="cc359-118">Click Revert job status.</span></span>
4. <span data-ttu-id="cc359-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="cc359-119">Click OK.</span></span>
    * <span data-ttu-id="cc359-120">这可以将当前作业状态从“计划”转变为“无计划”，并将其从进程栏上移除。</span><span class="sxs-lookup"><span data-stu-id="cc359-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   


