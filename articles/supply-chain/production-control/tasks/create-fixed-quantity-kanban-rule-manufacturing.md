--- 
title: "创建制造的固定数量看板规则"
description: "该过程的重点是为触发精益环境的工作单元的转换活动创建固定的制造看板规则所需的设置。"
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8020a37bf0c725fc260574cfe87861aeb017519e
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="72c22-103">创建制造的固定数量看板规则</span><span class="sxs-lookup"><span data-stu-id="72c22-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72c22-104">该过程的重点是为触发精益环境的工作单元的转换活动创建固定的制造看板规则所需的设置。</span><span class="sxs-lookup"><span data-stu-id="72c22-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="72c22-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="72c22-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="72c22-106">该过程面向工艺工程师和价值流经理，因为他们负责新型或改良产品的生产准备。</span><span class="sxs-lookup"><span data-stu-id="72c22-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="72c22-107">创建新看板规则</span><span class="sxs-lookup"><span data-stu-id="72c22-107">Create new kanban rule</span></span>
1. <span data-ttu-id="72c22-108">转到“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="72c22-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="72c22-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="72c22-109">Click New.</span></span>
    * <span data-ttu-id="72c22-110">请注意，默认类型“制造和补货策略”是固定的。</span><span class="sxs-lookup"><span data-stu-id="72c22-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="72c22-111">您不必更改这些参数。</span><span class="sxs-lookup"><span data-stu-id="72c22-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="72c22-112">在“第一个计划活动”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="72c22-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="72c22-113">将会对根据此看板规则创建的看板执行此活动。</span><span class="sxs-lookup"><span data-stu-id="72c22-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="72c22-114">选择“扬声器测试和包装”。</span><span class="sxs-lookup"><span data-stu-id="72c22-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="72c22-115">展开“详细信息”部分。</span><span class="sxs-lookup"><span data-stu-id="72c22-115">Expand the Details section.</span></span>
5. <span data-ttu-id="72c22-116">在“产品”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="72c22-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="72c22-117">选择“L0050”。</span><span class="sxs-lookup"><span data-stu-id="72c22-117">Select L0050.</span></span>  
6. <span data-ttu-id="72c22-118">在“度量单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="72c22-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="72c22-119">选择分钟。</span><span class="sxs-lookup"><span data-stu-id="72c22-119">Select minutes.</span></span>  
7. <span data-ttu-id="72c22-120">在“提前期”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="72c22-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="72c22-121">输入“5”。</span><span class="sxs-lookup"><span data-stu-id="72c22-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="72c22-122">设置数量</span><span class="sxs-lookup"><span data-stu-id="72c22-122">Set quantities</span></span>
1. <span data-ttu-id="72c22-123">展开“数量”部分。</span><span class="sxs-lookup"><span data-stu-id="72c22-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="72c22-124">设置“默认数量”为“10”。</span><span class="sxs-lookup"><span data-stu-id="72c22-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="72c22-125">这是将为每个看板转移的数量。</span><span class="sxs-lookup"><span data-stu-id="72c22-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="72c22-126">选择“产品数量差异”复选框。</span><span class="sxs-lookup"><span data-stu-id="72c22-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="72c22-127">这样，所选看板完成的数量可与默认数量不同。</span><span class="sxs-lookup"><span data-stu-id="72c22-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="72c22-128">若要允许看板完成数量介于 8 至 12 之间，将差异设为 2。</span><span class="sxs-lookup"><span data-stu-id="72c22-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="72c22-129">将差异设置为小于“2”。</span><span class="sxs-lookup"><span data-stu-id="72c22-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="72c22-130">这将允许完成的数量低至 10 - 2 = 8</span><span class="sxs-lookup"><span data-stu-id="72c22-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="72c22-131">将差异设置为大于“2”。</span><span class="sxs-lookup"><span data-stu-id="72c22-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="72c22-132">这将允许完成的数量高达 10 + 2 = 12</span><span class="sxs-lookup"><span data-stu-id="72c22-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="72c22-133">在“固定看板数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="72c22-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="72c22-134">此为活动看板的数量。</span><span class="sxs-lookup"><span data-stu-id="72c22-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="72c22-135">此时，5 个看板的处理数量分别为 10。</span><span class="sxs-lookup"><span data-stu-id="72c22-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="72c22-136">在“预警边界最小值”字段中，输入“2”。</span><span class="sxs-lookup"><span data-stu-id="72c22-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="72c22-137">用于记录为该目标的所有看板的最小金额。</span><span class="sxs-lookup"><span data-stu-id="72c22-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="72c22-138">例如，这在看板数量概览中使用。</span><span class="sxs-lookup"><span data-stu-id="72c22-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="72c22-139">在“预警边界最大值”字段中，输入“4”。</span><span class="sxs-lookup"><span data-stu-id="72c22-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="72c22-140">用于记录为该目标的所有看板的最大金额。</span><span class="sxs-lookup"><span data-stu-id="72c22-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="72c22-141">例如，这在看板数量概览中使用。</span><span class="sxs-lookup"><span data-stu-id="72c22-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="72c22-142">在“自动计划数量”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="72c22-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="72c22-143">将此项设置为 1 表示将自动规划每个看板。</span><span class="sxs-lookup"><span data-stu-id="72c22-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="72c22-144">如果我们输入了 3，直到 3 个空看板已准备就绪，可以规划，才会规划看板。</span><span class="sxs-lookup"><span data-stu-id="72c22-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="72c22-145">这对分组工作和避免设置过多非常有用。</span><span class="sxs-lookup"><span data-stu-id="72c22-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="72c22-146">创建看板</span><span class="sxs-lookup"><span data-stu-id="72c22-146">Create Kanbans</span></span>
1. <span data-ttu-id="72c22-147">展开“看板”部分。</span><span class="sxs-lookup"><span data-stu-id="72c22-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="72c22-148">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="72c22-148">Click Save.</span></span>
    * <span data-ttu-id="72c22-149">在创建看板前需要保存看板规则。</span><span class="sxs-lookup"><span data-stu-id="72c22-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="72c22-150">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="72c22-150">Click Add.</span></span>
    * <span data-ttu-id="72c22-151">请注意，由于建议的“新看板数”为 5，没有活动的看板。</span><span class="sxs-lookup"><span data-stu-id="72c22-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="72c22-152">这与“固定的看板数量”相等。</span><span class="sxs-lookup"><span data-stu-id="72c22-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="72c22-153">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="72c22-153">Click Create.</span></span>
    * <span data-ttu-id="72c22-154">这将创建 5 个看板。</span><span class="sxs-lookup"><span data-stu-id="72c22-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="72c22-155">请注意，将此制造看板规则创建为 5 个看板，每个处理数量为 10。</span><span class="sxs-lookup"><span data-stu-id="72c22-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="72c22-156">这是该过程的最后一步。</span><span class="sxs-lookup"><span data-stu-id="72c22-156">This is the last step in this procedure.</span></span>  


