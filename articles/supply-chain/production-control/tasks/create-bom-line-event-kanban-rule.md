--- 
title: "创建物料清单行事件看板规则"
description: "此任务介绍在混合精益和经典生产环境中创建事件看板规则以确保生产物料清单行的供应所需的设置。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 4168a515f5bc1b69a24aac616aba7e447ccda11a
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="afa91-103">创建物料清单行事件看板规则</span><span class="sxs-lookup"><span data-stu-id="afa91-103">Create a BOM line event kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="afa91-104">此任务介绍在混合精益和经典生产环境中创建事件看板规则以确保生产物料清单行的供应所需的设置。</span><span class="sxs-lookup"><span data-stu-id="afa91-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="afa91-105">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="afa91-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="afa91-106">该任务面向工艺工程师和价值流经理，因为他们负责新型或改良产品的生产准备。</span><span class="sxs-lookup"><span data-stu-id="afa91-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="afa91-107">创建新看板规则</span><span class="sxs-lookup"><span data-stu-id="afa91-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="afa91-108">转到“生产控制”>“定期任务”>“看板数量计算”>“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="afa91-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="afa91-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="afa91-109">Click New.</span></span>
3. <span data-ttu-id="afa91-110">在“类型”字段中选择“提领”。</span><span class="sxs-lookup"><span data-stu-id="afa91-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="afa91-111">“提领”类型用于创建转移看板。</span><span class="sxs-lookup"><span data-stu-id="afa91-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="afa91-112">在“补货策略”字段中，选择“事件”。</span><span class="sxs-lookup"><span data-stu-id="afa91-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="afa91-113">选择事件策略来基于事件创建看板的转移。</span><span class="sxs-lookup"><span data-stu-id="afa91-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="afa91-114">稍后在任务指南中，我们将通过估计生产订单触发它。</span><span class="sxs-lookup"><span data-stu-id="afa91-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="afa91-115">在“第一个计划活动”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="afa91-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="afa91-116">输入或选择 ReplenishSpeakerComponents。</span><span class="sxs-lookup"><span data-stu-id="afa91-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="afa91-117">此转移活动具有收货（输出）仓库和库位 12，这意味着物料将移到仓库 12 中的库位 12。</span><span class="sxs-lookup"><span data-stu-id="afa91-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="afa91-118">展开“详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="afa91-118">Expand the Details section.</span></span>
7. <span data-ttu-id="afa91-119">在“产品”字段中，输入或选择 M0001。</span><span class="sxs-lookup"><span data-stu-id="afa91-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="afa91-120">展开“事件”部分。</span><span class="sxs-lookup"><span data-stu-id="afa91-120">Expand the Events section.</span></span>
9. <span data-ttu-id="afa91-121">在“物料清单事件”字段中，选择“自动”。</span><span class="sxs-lookup"><span data-stu-id="afa91-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="afa91-122">将“物料清单行事件”字段设置为“自动”将创建看板来履行生产订单物料清单行的物料需要。</span><span class="sxs-lookup"><span data-stu-id="afa91-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="afa91-123">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="afa91-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="afa91-124">创建和修改新的生产订单</span><span class="sxs-lookup"><span data-stu-id="afa91-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="afa91-125">转到“生产控制”>“生产订单”>“全部生产订单”。</span><span class="sxs-lookup"><span data-stu-id="afa91-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="afa91-126">单击“新建生产订单”。</span><span class="sxs-lookup"><span data-stu-id="afa91-126">Click New production order.</span></span>
3. <span data-ttu-id="afa91-127">在“物料编号”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="afa91-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="afa91-128">输入或选择 'L0001'。</span><span class="sxs-lookup"><span data-stu-id="afa91-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="afa91-129">因为物料 M0001 包括在物料 L0001 的物料清单中，我们使用物料 L0001。</span><span class="sxs-lookup"><span data-stu-id="afa91-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="afa91-130">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="afa91-130">Click Create.</span></span>
5. <span data-ttu-id="afa91-131">在列表中，单击 L0001 的行中的链接。</span><span class="sxs-lookup"><span data-stu-id="afa91-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="afa91-132">单击“物料清单”。</span><span class="sxs-lookup"><span data-stu-id="afa91-132">Click BOM.</span></span>
7. <span data-ttu-id="afa91-133">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="afa91-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="afa91-134">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="afa91-134">Click Edit.</span></span>
9. <span data-ttu-id="afa91-135">在“行类型”字段中选择“限定供应”。</span><span class="sxs-lookup"><span data-stu-id="afa91-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="afa91-136">选择限定供应来触发看板的供应创建。</span><span class="sxs-lookup"><span data-stu-id="afa91-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="afa91-137">在“资源消耗量”字段中选择“否”。</span><span class="sxs-lookup"><span data-stu-id="afa91-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="afa91-138">清除“资源消耗量”复选框让我们可以更改仓库。</span><span class="sxs-lookup"><span data-stu-id="afa91-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="afa91-139">展开“库存维度”部分。</span><span class="sxs-lookup"><span data-stu-id="afa91-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="afa91-140">在“仓库”字段中，键入“12”。</span><span class="sxs-lookup"><span data-stu-id="afa91-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="afa91-141">因为这是提领活动的输出仓库，仓库设置为 12。</span><span class="sxs-lookup"><span data-stu-id="afa91-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="afa91-142">在“位置”字段中，键入 '12'。</span><span class="sxs-lookup"><span data-stu-id="afa91-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="afa91-143">因为这是提领活动的输出库位，库位设置为 12。</span><span class="sxs-lookup"><span data-stu-id="afa91-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="afa91-144">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="afa91-144">Close the page.</span></span>
15. <span data-ttu-id="afa91-145">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="afa91-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="afa91-146">估计生产订单并查看已创建的看板</span><span class="sxs-lookup"><span data-stu-id="afa91-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="afa91-147">单击“估计”。</span><span class="sxs-lookup"><span data-stu-id="afa91-147">Click Estimate.</span></span>
    * <span data-ttu-id="afa91-148">估计生产订单将触发关联的看板的创建来供应物料 M0001。</span><span class="sxs-lookup"><span data-stu-id="afa91-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="afa91-149">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="afa91-149">Click OK.</span></span>
3. <span data-ttu-id="afa91-150">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="afa91-150">Close the page.</span></span>
4. <span data-ttu-id="afa91-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="afa91-151">Close the page.</span></span>
5. <span data-ttu-id="afa91-152">转到“产品信息管理”>“Lean manufacturing”>“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="afa91-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="afa91-153">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="afa91-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="afa91-154">选择为物料 M0001 创建的事件看板规则。</span><span class="sxs-lookup"><span data-stu-id="afa91-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="afa91-155">展开“看板”部分。</span><span class="sxs-lookup"><span data-stu-id="afa91-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="afa91-156">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="afa91-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="afa91-157">请注意创建的用来供应估计生产订单的 M0001 的看板。</span><span class="sxs-lookup"><span data-stu-id="afa91-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="afa91-158">这是最后一个步骤！</span><span class="sxs-lookup"><span data-stu-id="afa91-158">This is the last step!</span></span>  


