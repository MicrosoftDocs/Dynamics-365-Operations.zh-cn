---
title: 创建销售事件看板规则
description: 该过程的重点是创建在销售订单创建期间触发的看板规则所需的设置。
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2bee6e81acd029406c95237f0b4ba4ab2565ea1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573059"
---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="20dd1-103">创建销售事件看板规则</span><span class="sxs-lookup"><span data-stu-id="20dd1-103">Create a sales event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="20dd1-104">该过程的重点是创建在销售订单创建期间触发的看板规则所需的设置。</span><span class="sxs-lookup"><span data-stu-id="20dd1-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="20dd1-105">事件看板规则源自销售订单行的补货要求。</span><span class="sxs-lookup"><span data-stu-id="20dd1-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="20dd1-106">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="20dd1-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="20dd1-107">这面向工艺工程师和价值流经理，因为他们负责新型或改良产品的生产准备。</span><span class="sxs-lookup"><span data-stu-id="20dd1-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="20dd1-108">创建新看板规则</span><span class="sxs-lookup"><span data-stu-id="20dd1-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="20dd1-109">转到“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="20dd1-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-110">Click New.</span></span>
3. <span data-ttu-id="20dd1-111">在“补货策略”字段中，选择“事件”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="20dd1-112">选择“事件”表示看板规则由事件（如创建销售订单行）触发。</span><span class="sxs-lookup"><span data-stu-id="20dd1-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="20dd1-113">这适用于每个看板应涵盖特定需求的区域。</span><span class="sxs-lookup"><span data-stu-id="20dd1-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="20dd1-114">在“第一个计划活动”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="20dd1-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="20dd1-115">选择“最终装配”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="20dd1-116">展开“详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="20dd1-116">Expand the Details section.</span></span>
6. <span data-ttu-id="20dd1-117">在“产品”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="20dd1-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="20dd1-118">选择“L0050”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="20dd1-119">定义事件</span><span class="sxs-lookup"><span data-stu-id="20dd1-119">Define an event</span></span>
1. <span data-ttu-id="20dd1-120">展开“事件”部分。</span><span class="sxs-lookup"><span data-stu-id="20dd1-120">Expand the Events section.</span></span>
2. <span data-ttu-id="20dd1-121">在“销售事件”字段中，选择“自动”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="20dd1-122">将销售事件选为“自动”后，在销售行匹配产品和收货库位时，将会自动触发此看板规则。</span><span class="sxs-lookup"><span data-stu-id="20dd1-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="20dd1-123">在该过程中，使用的是仓库 13 的 L0050 产品。</span><span class="sxs-lookup"><span data-stu-id="20dd1-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="20dd1-124">设置最小的事件数量为“50”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="20dd1-125">如果最小事件数量为 50，只有事件数量为 50 或以上时才会触发看板规则。</span><span class="sxs-lookup"><span data-stu-id="20dd1-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="20dd1-126">展开“生产流”部分。</span><span class="sxs-lookup"><span data-stu-id="20dd1-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="20dd1-127">请注意收货库位是仓库 13。</span><span class="sxs-lookup"><span data-stu-id="20dd1-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="20dd1-128">这意味着此库位将会触发看板规则。</span><span class="sxs-lookup"><span data-stu-id="20dd1-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="20dd1-129">在此示例中，位于仓库 13，数量为 50 或以上的 L0050 产品的销售行将触发此看板规则。</span><span class="sxs-lookup"><span data-stu-id="20dd1-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="20dd1-130">创建销售行以触发事件看板规则</span><span class="sxs-lookup"><span data-stu-id="20dd1-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="20dd1-131">转到“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="20dd1-132">在保存看板规则时会显示警告，这意味着在销售订单创建期间将实时创建看板。</span><span class="sxs-lookup"><span data-stu-id="20dd1-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="20dd1-133">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-133">Click New.</span></span>
3. <span data-ttu-id="20dd1-134">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="20dd1-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="20dd1-135">例如，选择 US-003。</span><span class="sxs-lookup"><span data-stu-id="20dd1-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="20dd1-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-136">Click OK.</span></span>
5. <span data-ttu-id="20dd1-137">在“物料编号”字段中，键入“L0050”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="20dd1-138">在“站点”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="20dd1-139">选择站点 1，因为仓库 13 位于站点 1。</span><span class="sxs-lookup"><span data-stu-id="20dd1-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="20dd1-140">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="20dd1-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="20dd1-141">将“仓库”设置为 13。</span><span class="sxs-lookup"><span data-stu-id="20dd1-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="20dd1-142">将“数量”设置为“75”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="20dd1-143">输入 50 或更多数量，以触发已创建的看板规则。</span><span class="sxs-lookup"><span data-stu-id="20dd1-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="20dd1-144">核实已创建看板。</span><span class="sxs-lookup"><span data-stu-id="20dd1-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="20dd1-145">单击“产品和供应”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-145">Click Product and supply.</span></span>
2. <span data-ttu-id="20dd1-146">单击“查看限定标准树”。</span><span class="sxs-lookup"><span data-stu-id="20dd1-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="20dd1-147">请注意，创建的看板的数量与销售行数量相同。</span><span class="sxs-lookup"><span data-stu-id="20dd1-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="20dd1-148">您还可以查看生产 L0050 所需的物料领料单。</span><span class="sxs-lookup"><span data-stu-id="20dd1-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="20dd1-149">这是该过程的最后一步。</span><span class="sxs-lookup"><span data-stu-id="20dd1-149">This is the last step in this procedure.</span></span>  

