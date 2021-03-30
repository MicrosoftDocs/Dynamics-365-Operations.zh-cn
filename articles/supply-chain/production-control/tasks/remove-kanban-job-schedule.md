---
title: 从计划中删除看板作业
description: 此程序用于通过恢复一个作业的“无计划”状态，从预定计划中移除该计划处理的看板作业。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 566a174c631391577441e0f890bd9553dac0891c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204512"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="0de83-103">从计划中删除看板作业</span><span class="sxs-lookup"><span data-stu-id="0de83-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0de83-104">此程序用于通过恢复一个作业的“无计划”状态，从预定计划中移除该计划处理的看板作业。</span><span class="sxs-lookup"><span data-stu-id="0de83-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="0de83-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="0de83-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0de83-106">此程序是为车间主管或生产计划主任而设计的。</span><span class="sxs-lookup"><span data-stu-id="0de83-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="0de83-107">查找一个计划看板作业。</span><span class="sxs-lookup"><span data-stu-id="0de83-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="0de83-108">转到“生产控制”>“看板管理”>“安排看板作业”。</span><span class="sxs-lookup"><span data-stu-id="0de83-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="0de83-109">在“工作单元”字段中，单击下拉按钮打开查找。</span><span class="sxs-lookup"><span data-stu-id="0de83-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0de83-110">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="0de83-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0de83-111">选择 1250 号工作单元。</span><span class="sxs-lookup"><span data-stu-id="0de83-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="0de83-112">单击“选择”。</span><span class="sxs-lookup"><span data-stu-id="0de83-112">Click Select.</span></span>
5. <span data-ttu-id="0de83-113">在“显示作业状态”字段中，选择“预定作业”。</span><span class="sxs-lookup"><span data-stu-id="0de83-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="0de83-114">从预定计划中移除该计划看板作业</span><span class="sxs-lookup"><span data-stu-id="0de83-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="0de83-115">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="0de83-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0de83-116">选择一个“计划状态”的作业，例如，开始于 2012 年 12 月 19 日的作业。</span><span class="sxs-lookup"><span data-stu-id="0de83-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="0de83-117">在操作窗格上，单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="0de83-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="0de83-118">单击“恢复作业原态”。</span><span class="sxs-lookup"><span data-stu-id="0de83-118">Click Revert job status.</span></span>
4. <span data-ttu-id="0de83-119">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="0de83-119">Click OK.</span></span>
    * <span data-ttu-id="0de83-120">这可以将当前作业状态从“计划”转变为“无计划”，并将其从进程栏上移除。</span><span class="sxs-lookup"><span data-stu-id="0de83-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]