---
title: 向看板规则中添加看板数量计算策略
description: 此过程重点是创建看板数量计算策略，并将其添加到看板规则，以优化看板大小和数量。
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules, KanbanQuantityCalculation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd53d21f26596ac9ef394f61588b7778dc3de0fa
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825078"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="7cd3f-103">向看板规则中添加看板数量计算策略</span><span class="sxs-lookup"><span data-stu-id="7cd3f-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7cd3f-104">此过程重点是创建看板数量计算策略，并将其添加到看板规则，以优化看板大小和数量。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="7cd3f-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7cd3f-106">此程序是专为价值流经理设计的。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="7cd3f-107">此过程是创建“计算看板数量建议”这一过程的先决条件。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="7cd3f-108">创建看板数量计算策略</span><span class="sxs-lookup"><span data-stu-id="7cd3f-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="7cd3f-109">转到“生产控制”>“定期任务”>“看板数量计算”>“看板数量计算策略”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="7cd3f-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-110">Click New.</span></span>
3. <span data-ttu-id="7cd3f-111">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="7cd3f-112">例如，键入“Speaker2016”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="7cd3f-113">在“主计划”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7cd3f-114">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7cd3f-115">选择静态计划 (StaticPlan) 以计算需求。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="7cd3f-116">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7cd3f-117">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-117">Click Save.</span></span>
8. <span data-ttu-id="7cd3f-118">在“最小看板数量”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="7cd3f-119">此为看板数量计算中包括的额外看板数。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="7cd3f-120">设置安全系数为“1”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="7cd3f-121">此为用于计算安全库存的额外数量的系数。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="7cd3f-122">在“提前天数”字段中，输入“30”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="7cd3f-123">此为在看板数量计算日前之前，包括在需求计算中的天数。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="7cd3f-124">在“滞后天数”字段中，输入“30”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="7cd3f-125">这是从包括在需求计算中的看板数量计算日期正推的天数。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="7cd3f-126">用于此计算的公式与实际值一起显示。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="7cd3f-127">例如，看板数量 = ((平均每日需求量 x 提前期 x 2.00) / 每物料处理单元的产品数量) + 1</span><span class="sxs-lookup"><span data-stu-id="7cd3f-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="7cd3f-128">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="7cd3f-129">向看板规则中添加看板数量计算策略</span><span class="sxs-lookup"><span data-stu-id="7cd3f-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="7cd3f-130">转到“产品信息管理”>“Lean manufacturing”>“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="7cd3f-131">在列表中，找到并选择所需记录。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7cd3f-132">为此过程选择看板规则 000020。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="7cd3f-133">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7cd3f-134">切换“看板数量计算策略”部分的展开项。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="7cd3f-135">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-135">Click Add.</span></span>
    * <span data-ttu-id="7cd3f-136">添加您刚刚在先前的子任务中创建的看板数量计算策略。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="7cd3f-137">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="7cd3f-138">在“名称”字段中，单击下拉按钮以打开查找。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="7cd3f-139">在列表中，单击所选行中的链接。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7cd3f-140">选择您刚刚在先前的子任务中创建的策略“Speaker2016”。</span><span class="sxs-lookup"><span data-stu-id="7cd3f-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]