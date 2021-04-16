---
title: 使用看板行事件创建看板规则
description: 此过程通过使用看板行事件设置触发从进程活动的提取来创建看板规则。
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe92336c3f80909e5b0865b461e45d55bf08c4b4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829130"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="c4b9a-103">使用看板行事件创建看板规则</span><span class="sxs-lookup"><span data-stu-id="c4b9a-103">Create a kanban rule using a kanban line event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4b9a-104">此过程通过使用看板行事件设置触发从进程活动的提取来创建看板规则。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="c4b9a-105">看板规则由各数量等于或大于 25 的看板进程活动触发。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="c4b9a-106">创建此任务的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="c4b9a-107">该任务面向工艺工程师或价值流经理，因为他们负责新型或改良产品的生产准备。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="c4b9a-108">创建看板规则</span><span class="sxs-lookup"><span data-stu-id="c4b9a-108">Create a kanban rule</span></span>
1. <span data-ttu-id="c4b9a-109">转到“产品信息管理”>“Lean manufacturing”>“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="c4b9a-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-110">Click New.</span></span>
3. <span data-ttu-id="c4b9a-111">在“补货策略”字段中，选择“事件”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="c4b9a-112">这将直接从需求生成看板。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="c4b9a-113">它用于设置定义按订单生产方案的规则。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="c4b9a-114">在“第一个计划活动”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c4b9a-115">输入或选择 SpeakerAssemblyAndPolish。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="c4b9a-116">制造看板规则的第一项活动是生产流中的处理活动。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="c4b9a-117">在选择该活动时，该活动的生效日期将复制到看板规则的生效日期。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="c4b9a-118">展开“详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-118">Expand the Details section.</span></span>
6. <span data-ttu-id="c4b9a-119">在“产品”字段中，键入“L0001”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="c4b9a-120">展开“事件”部分。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-120">Expand the Events section.</span></span>
8. <span data-ttu-id="c4b9a-121">在“看板行事件”字段中，选择“自动”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="c4b9a-122">这将根据需要生成事件看板。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="c4b9a-123">此字段用于配置补充下游处理活动所需材料的看板规则。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="c4b9a-124">当您选择“自动”时，随需求创建事件看板。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="c4b9a-125">如果要在同一天进行生产，建议采用此设置。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="c4b9a-126">设置最小的事件数量为“25”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="c4b9a-127">当需求数量等于或大于此字段时，生成看板事件。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="c4b9a-128">如果一台机器上要生成的订单数量比此字段少，但另一台机器上要生成的订单数量比此字段多，则这很有用。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="c4b9a-129">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="c4b9a-130">创建销售订单和触发看板链</span><span class="sxs-lookup"><span data-stu-id="c4b9a-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="c4b9a-131">转至“销售和营销”>“销售订单”>“所有销售订单”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="c4b9a-132">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-132">Click New.</span></span>
3. <span data-ttu-id="c4b9a-133">在“客户帐户”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="c4b9a-134">选择客户帐户 US-003，Forest Wholesales。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="c4b9a-135">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-135">Click OK.</span></span>
5. <span data-ttu-id="c4b9a-136">在“物料编号”字段中，键入“L0001”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="c4b9a-137">L0001 是您为其创建了看板规则的物料。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="c4b9a-138">将“数量”设置为“27”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="c4b9a-139">由于 27 比看板规则中的 25 这一最小数量大，所以将触发事件看板。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="c4b9a-140">在“站点”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="c4b9a-141">在“仓库”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="c4b9a-142">选择“仓库 13”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="c4b9a-143">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="c4b9a-144">查看看板规则生成的看板</span><span class="sxs-lookup"><span data-stu-id="c4b9a-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="c4b9a-145">转到“产品信息管理”>“Lean manufacturing”>“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="c4b9a-146">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c4b9a-147">展开“看板”部分。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="c4b9a-148">请注意，为 27 创建了看板以基于创建的看板规则处理活动。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="c4b9a-149">这是最后一个步骤。</span><span class="sxs-lookup"><span data-stu-id="c4b9a-149">This is the last step.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]