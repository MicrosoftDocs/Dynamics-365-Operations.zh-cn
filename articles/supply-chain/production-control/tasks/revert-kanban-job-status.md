---
title: 恢复看板作业状态
description: 该过程用于恢复一个不正确的看板作业状态。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cca5ea3a4c33c7f36acd18a8af7034466b3b580
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982664"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="f1179-103">恢复看板作业状态</span><span class="sxs-lookup"><span data-stu-id="f1179-103">Revert kanban job status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f1179-104">该过程用于恢复一个不正确的看板作业状态。</span><span class="sxs-lookup"><span data-stu-id="f1179-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="f1179-105">此用于机器操作员更新错误作业或设置错误状态的情况。</span><span class="sxs-lookup"><span data-stu-id="f1179-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="f1179-106">在该过程中，先把一项看板作业错误登记为已准备，然后恢复其状态。</span><span class="sxs-lookup"><span data-stu-id="f1179-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="f1179-107">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="f1179-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f1179-108">该过程是为在 lean manufacturing 公司工作的店铺主管或机器操作员设计的。</span><span class="sxs-lookup"><span data-stu-id="f1179-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="f1179-109">打开该工作单元的流程面板</span><span class="sxs-lookup"><span data-stu-id="f1179-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="f1179-110">转到“处理作业的看板面板”。</span><span class="sxs-lookup"><span data-stu-id="f1179-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="f1179-111">在“工作单元”字段中，输入或者选择一个值。</span><span class="sxs-lookup"><span data-stu-id="f1179-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="f1179-112">选择工作单元 1260。</span><span class="sxs-lookup"><span data-stu-id="f1179-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="f1179-113">准备看板作业</span><span class="sxs-lookup"><span data-stu-id="f1179-113">Prepare kanban job</span></span>
1. <span data-ttu-id="f1179-114">单击“准备”。</span><span class="sxs-lookup"><span data-stu-id="f1179-114">Click Prepare.</span></span>
    * <span data-ttu-id="f1179-115">若无法单击“准备”是因为其显示为灰色，请确保所选看板作业的状态为“已计划”（以空看板图标表示）。</span><span class="sxs-lookup"><span data-stu-id="f1179-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="f1179-116">如果“准备”失败，请确保“领料单”上的所有材料为可用。</span><span class="sxs-lookup"><span data-stu-id="f1179-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="f1179-117">在此列表中，选择已准备作业。</span><span class="sxs-lookup"><span data-stu-id="f1179-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="f1179-118">选择您已准备的第一个作业。</span><span class="sxs-lookup"><span data-stu-id="f1179-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="f1179-119">请注意，作业状态为“已准备”，以看板图标内的三角形表示。</span><span class="sxs-lookup"><span data-stu-id="f1179-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="f1179-120">恢复该已准备的看板作业的状态</span><span class="sxs-lookup"><span data-stu-id="f1179-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="f1179-121">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f1179-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f1179-122">选择您准备好的第一个作业。</span><span class="sxs-lookup"><span data-stu-id="f1179-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="f1179-123">在“操作窗格”上单击“制造”。</span><span class="sxs-lookup"><span data-stu-id="f1179-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="f1179-124">单击“恢复状态”。</span><span class="sxs-lookup"><span data-stu-id="f1179-124">Click Revert status.</span></span>
    * <span data-ttu-id="f1179-125">如果发生以下情况，您可以使用另一看板规则：- 两个规则的补货策略一致。</span><span class="sxs-lookup"><span data-stu-id="f1179-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="f1179-126">- 两个规则的生产流版本一样。</span><span class="sxs-lookup"><span data-stu-id="f1179-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="f1179-127">- 两个规则的产品供应相同。</span><span class="sxs-lookup"><span data-stu-id="f1179-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="f1179-128">- 两个规则的的任意下游活动必须相同，这些活动决定该看板规则的最后一项活动。</span><span class="sxs-lookup"><span data-stu-id="f1179-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="f1179-129">- 两个规则所设置的供应库存维度必须相同。</span><span class="sxs-lookup"><span data-stu-id="f1179-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="f1179-130">- 搬运单元状态必须为“未分配”。</span><span class="sxs-lookup"><span data-stu-id="f1179-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="f1179-131">- 事件看板的设置必须相同。</span><span class="sxs-lookup"><span data-stu-id="f1179-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="f1179-132">确认该新状态为“已计划”。</span><span class="sxs-lookup"><span data-stu-id="f1179-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="f1179-133">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="f1179-133">Click OK.</span></span>
5. <span data-ttu-id="f1179-134">在列表中，取消标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="f1179-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="f1179-135">选择相同作业。</span><span class="sxs-lookup"><span data-stu-id="f1179-135">Select the same job.</span></span>  
    * <span data-ttu-id="f1179-136">请注意，该看板作业的作业状态已恢复为“已计划”（以空看板图标表示）。</span><span class="sxs-lookup"><span data-stu-id="f1179-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  

