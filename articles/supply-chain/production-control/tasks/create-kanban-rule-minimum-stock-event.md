---
title: 使用最小库存事件创建看板规则
description: 此过程重点介绍通过使用最低存货事件创建看板规则以确保特定产品在特定地点始终可用时所需的设置。
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 598af59a1b30cfeb5c25c89d95e1a60e6707c899
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829082"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="99ab9-103">使用最小库存事件创建看板规则</span><span class="sxs-lookup"><span data-stu-id="99ab9-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="99ab9-104">此过程重点介绍通过使用最低存货事件创建看板规则以确保特定产品在特定地点始终可用时所需的设置。</span><span class="sxs-lookup"><span data-stu-id="99ab9-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="99ab9-105">创建看板规则，以便在库存水平下降到低于 200 件时将物料转移到该地点。</span><span class="sxs-lookup"><span data-stu-id="99ab9-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="99ab9-106">通过运行需求声明事件处理，创建所需看板。</span><span class="sxs-lookup"><span data-stu-id="99ab9-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="99ab9-107">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="99ab9-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="99ab9-108">该任务面向工艺工程师或价值流经理，因为他们负责新型或改良产品的生产准备。</span><span class="sxs-lookup"><span data-stu-id="99ab9-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="99ab9-109">创建新看板规则</span><span class="sxs-lookup"><span data-stu-id="99ab9-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="99ab9-110">转到“产品信息管理”>“Lean manufacturing”>“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="99ab9-111">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-111">Click New.</span></span>
3. <span data-ttu-id="99ab9-112">在“类型”字段中选择“提领”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="99ab9-113">此类型用于创建转移看板。</span><span class="sxs-lookup"><span data-stu-id="99ab9-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="99ab9-114">在“补货策略”字段中，选择“事件”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="99ab9-115">事件策略用于基于事件创建看板的转移。</span><span class="sxs-lookup"><span data-stu-id="99ab9-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="99ab9-116">在此过程的后面，将通过使用补货触发转移看板。</span><span class="sxs-lookup"><span data-stu-id="99ab9-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="99ab9-117">在“第一个计划活动”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="99ab9-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="99ab9-118">输入或选择 ReplenishSpeakerComponents。</span><span class="sxs-lookup"><span data-stu-id="99ab9-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="99ab9-119">此转移活动具有收货（输出）仓库和库位 12，这意味着物料将移到仓库 12 中的库位 12。</span><span class="sxs-lookup"><span data-stu-id="99ab9-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="99ab9-120">展开“详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="99ab9-120">Expand the Details section.</span></span>
7. <span data-ttu-id="99ab9-121">在“产品”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="99ab9-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="99ab9-122">选择“M0007”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-122">Select M0007.</span></span>  
8. <span data-ttu-id="99ab9-123">展开“事件”部分。</span><span class="sxs-lookup"><span data-stu-id="99ab9-123">Expand the Events section.</span></span>
9. <span data-ttu-id="99ab9-124">在“补货事件”字段中，选择“批处理”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="99ab9-125">这将创建看板，以便满足处理需求声明事件期间相关地点的物料需求。</span><span class="sxs-lookup"><span data-stu-id="99ab9-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="99ab9-126">设置物料的最低数量</span><span class="sxs-lookup"><span data-stu-id="99ab9-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="99ab9-127">单击以访问“产品”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="99ab9-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="99ab9-128">单击并打开“物料编号”字段中的链接。</span><span class="sxs-lookup"><span data-stu-id="99ab9-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="99ab9-129">展开“产品图像”速见表。</span><span class="sxs-lookup"><span data-stu-id="99ab9-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="99ab9-130">在操作窗格上，单击“计划”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="99ab9-131">单击“物料覆盖范围”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-131">Click Item coverage.</span></span>
6. <span data-ttu-id="99ab9-132">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-132">Click New.</span></span>
7. <span data-ttu-id="99ab9-133">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="99ab9-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="99ab9-134">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="99ab9-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="99ab9-135">将“仓库”设置为 12。</span><span class="sxs-lookup"><span data-stu-id="99ab9-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="99ab9-136">将“最小值”设置为“200”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="99ab9-137">运行批量事件创建作业。</span><span class="sxs-lookup"><span data-stu-id="99ab9-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="99ab9-138">转到“生产控制”>“定期任务”>“看板作业批处理”>“需求声明事件处理”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="99ab9-139">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-139">Click OK.</span></span>
3. <span data-ttu-id="99ab9-140">转到“产品信息管理”>“Lean manufacturing”>“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="99ab9-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="99ab9-141">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="99ab9-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="99ab9-142">选择之前所创建的看板规则。</span><span class="sxs-lookup"><span data-stu-id="99ab9-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="99ab9-143">展开“看板”部分。</span><span class="sxs-lookup"><span data-stu-id="99ab9-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="99ab9-144">请注意，创建了一个看板来将所需物料转移到仓库 12。</span><span class="sxs-lookup"><span data-stu-id="99ab9-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]