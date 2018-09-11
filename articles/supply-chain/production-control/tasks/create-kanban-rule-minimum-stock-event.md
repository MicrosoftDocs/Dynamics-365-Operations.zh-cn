--- 
title: "使用最小库存事件创建看板规则"
description: "此过程重点介绍通过使用最低存货事件创建看板规则以确保特定产品在特定地点始终可用时所需的设置。"
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: b325f659ea026797205cde8408c2fb3de27bb48d
ms.contentlocale: zh-cn
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="dafcf-103">使用最小库存事件创建看板规则</span><span class="sxs-lookup"><span data-stu-id="dafcf-103">Create a kanban rule using a minimum stock event</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dafcf-104">此过程重点介绍通过使用最低存货事件创建看板规则以确保特定产品在特定地点始终可用时所需的设置。</span><span class="sxs-lookup"><span data-stu-id="dafcf-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="dafcf-105">创建看板规则，以便在库存水平下降到低于 200 件时将物料转移到该地点。</span><span class="sxs-lookup"><span data-stu-id="dafcf-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="dafcf-106">通过运行需求声明事件处理，创建所需看板。</span><span class="sxs-lookup"><span data-stu-id="dafcf-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="dafcf-107">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="dafcf-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="dafcf-108">该任务面向工艺工程师或价值流经理，因为他们负责新型或改良产品的生产准备。</span><span class="sxs-lookup"><span data-stu-id="dafcf-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="dafcf-109">创建新看板规则</span><span class="sxs-lookup"><span data-stu-id="dafcf-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="dafcf-110">转到“产品信息管理”>“Lean manufacturing”>“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="dafcf-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-111">Click New.</span></span>
3. <span data-ttu-id="dafcf-112">在“类型”字段中选择“提领”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="dafcf-113">此类型用于创建转移看板。</span><span class="sxs-lookup"><span data-stu-id="dafcf-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="dafcf-114">在“补货策略”字段中，选择“事件”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="dafcf-115">事件策略用于基于事件创建看板的转移。</span><span class="sxs-lookup"><span data-stu-id="dafcf-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="dafcf-116">在此过程的后面，将通过使用补货触发转移看板。</span><span class="sxs-lookup"><span data-stu-id="dafcf-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="dafcf-117">在“第一个计划活动”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dafcf-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="dafcf-118">输入或选择 ReplenishSpeakerComponents。</span><span class="sxs-lookup"><span data-stu-id="dafcf-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="dafcf-119">此转移活动具有收货（输出）仓库和库位 12，这意味着物料将移到仓库 12 中的库位 12。</span><span class="sxs-lookup"><span data-stu-id="dafcf-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="dafcf-120">展开“详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="dafcf-120">Expand the Details section.</span></span>
7. <span data-ttu-id="dafcf-121">在“产品”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dafcf-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="dafcf-122">选择“M0007”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-122">Select M0007.</span></span>  
8. <span data-ttu-id="dafcf-123">展开“事件”部分。</span><span class="sxs-lookup"><span data-stu-id="dafcf-123">Expand the Events section.</span></span>
9. <span data-ttu-id="dafcf-124">在“补货事件”字段中，选择“批处理”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="dafcf-125">这将创建看板，以便满足处理需求声明事件期间相关地点的物料需求。</span><span class="sxs-lookup"><span data-stu-id="dafcf-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="dafcf-126">设置物料的最低数量</span><span class="sxs-lookup"><span data-stu-id="dafcf-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="dafcf-127">单击以访问“产品”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="dafcf-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="dafcf-128">单击并打开“物料编号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="dafcf-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="dafcf-129">展开“产品图像”速见表。</span><span class="sxs-lookup"><span data-stu-id="dafcf-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="dafcf-130">在操作窗格上，单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="dafcf-131">单击“物料覆盖范围”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-131">Click Item coverage.</span></span>
6. <span data-ttu-id="dafcf-132">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-132">Click New.</span></span>
7. <span data-ttu-id="dafcf-133">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="dafcf-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="dafcf-134">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="dafcf-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="dafcf-135">将“仓库”设置为 12。</span><span class="sxs-lookup"><span data-stu-id="dafcf-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="dafcf-136">将“最小值”设置为“200”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="dafcf-137">运行批量事件创建作业。</span><span class="sxs-lookup"><span data-stu-id="dafcf-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="dafcf-138">转到“生产控制”>“定期任务”>“看板作业批处理”>“需求声明事件处理”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="dafcf-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-139">Click OK.</span></span>
3. <span data-ttu-id="dafcf-140">转到“产品信息管理”>“Lean manufacturing”>“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="dafcf-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="dafcf-141">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="dafcf-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dafcf-142">选择之前所创建的看板规则。</span><span class="sxs-lookup"><span data-stu-id="dafcf-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="dafcf-143">展开“看板”部分。</span><span class="sxs-lookup"><span data-stu-id="dafcf-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="dafcf-144">请注意，创建了一个看板来将所需物料转移到仓库 12。</span><span class="sxs-lookup"><span data-stu-id="dafcf-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  


