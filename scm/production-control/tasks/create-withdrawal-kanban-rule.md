--- 
title: "创建提款看板规则"
description: "此过程显示在精益环境中创建转移物料的提领看板规则所需的设置。"
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 02c7133d2e02b27fb428874deeda21e2bab28fb6
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="0421a-103">创建提款看板规则</span><span class="sxs-lookup"><span data-stu-id="0421a-103">Create a withdrawal kanban rule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0421a-104">此过程显示在精益环境中创建转移物料的提领看板规则所需的设置。</span><span class="sxs-lookup"><span data-stu-id="0421a-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="0421a-105">创建此程序的演示数据公司是 USMF。</span><span class="sxs-lookup"><span data-stu-id="0421a-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0421a-106">该过程面向工艺工程师和价值流经理，因为他们负责新型或改良物料的补货准备。</span><span class="sxs-lookup"><span data-stu-id="0421a-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="0421a-107">创建新看板规则</span><span class="sxs-lookup"><span data-stu-id="0421a-107">Create new kanban rule</span></span>
1. <span data-ttu-id="0421a-108">转到“看板规则”。</span><span class="sxs-lookup"><span data-stu-id="0421a-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="0421a-109">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="0421a-109">Click New.</span></span>
3. <span data-ttu-id="0421a-110">在“类型”字段中选择“提领”。</span><span class="sxs-lookup"><span data-stu-id="0421a-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="0421a-111">“提领”类型由看板规则用来转移物料或货物。</span><span class="sxs-lookup"><span data-stu-id="0421a-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="0421a-112">在“第一个计划活动”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0421a-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="0421a-113">选择 ReplenishSpeakerComponents。</span><span class="sxs-lookup"><span data-stu-id="0421a-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="0421a-114">设置此活动将组件从仓库 11，库位 11 移到仓库 12 和库位 12。</span><span class="sxs-lookup"><span data-stu-id="0421a-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="0421a-115">在“产品”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0421a-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="0421a-116">选择“M0007”。</span><span class="sxs-lookup"><span data-stu-id="0421a-116">Select M0007.</span></span>  
6. <span data-ttu-id="0421a-117">在“提前期”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="0421a-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="0421a-118">例如，60。</span><span class="sxs-lookup"><span data-stu-id="0421a-118">For example, 60.</span></span>  
7. <span data-ttu-id="0421a-119">在“度量单位”字段中，输入或选择一个值。</span><span class="sxs-lookup"><span data-stu-id="0421a-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="0421a-120">例如，分钟。</span><span class="sxs-lookup"><span data-stu-id="0421a-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="0421a-121">设置看板数量</span><span class="sxs-lookup"><span data-stu-id="0421a-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="0421a-122">设置“默认数量”为“5”。</span><span class="sxs-lookup"><span data-stu-id="0421a-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="0421a-123">这是将为每个看板转移的数量。</span><span class="sxs-lookup"><span data-stu-id="0421a-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="0421a-124">在“固定看板数量”字段中，输入 '2'。</span><span class="sxs-lookup"><span data-stu-id="0421a-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="0421a-125">此为活动看板的数量。</span><span class="sxs-lookup"><span data-stu-id="0421a-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="0421a-126">在此情况下，2 个看板的转移数量分别为 5。</span><span class="sxs-lookup"><span data-stu-id="0421a-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="0421a-127">在“预警边界最小值”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="0421a-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="0421a-128">用于记录为该目标的所有看板的最小金额。</span><span class="sxs-lookup"><span data-stu-id="0421a-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="0421a-129">例如，这在看板数量概览中使用。</span><span class="sxs-lookup"><span data-stu-id="0421a-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="0421a-130">在“预警边界最大值”字段中，输入“2”。</span><span class="sxs-lookup"><span data-stu-id="0421a-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="0421a-131">用于记录为该目标的所有看板的最大金额。</span><span class="sxs-lookup"><span data-stu-id="0421a-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="0421a-132">例如，这在看板数量概览中使用。</span><span class="sxs-lookup"><span data-stu-id="0421a-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="0421a-133">创建看板</span><span class="sxs-lookup"><span data-stu-id="0421a-133">Create kanbans</span></span>
1. <span data-ttu-id="0421a-134">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="0421a-134">Click Save.</span></span>
    * <span data-ttu-id="0421a-135">在创建看板前需要保存看板规则。</span><span class="sxs-lookup"><span data-stu-id="0421a-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="0421a-136">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="0421a-136">Click Add.</span></span>
    * <span data-ttu-id="0421a-137">请注意，由于建议的“新看板数”为 2（与“固定的看板数量”相等），没有有效看板。</span><span class="sxs-lookup"><span data-stu-id="0421a-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="0421a-138">单击“创建”。</span><span class="sxs-lookup"><span data-stu-id="0421a-138">Click Create.</span></span>
    * <span data-ttu-id="0421a-139">这将创建两个看板。</span><span class="sxs-lookup"><span data-stu-id="0421a-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="0421a-140">请注意，将为此提领看板规则创建 2 个看板，每个处理数量为 5。</span><span class="sxs-lookup"><span data-stu-id="0421a-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="0421a-141">这是该过程的最后一步。</span><span class="sxs-lookup"><span data-stu-id="0421a-141">This is the last step in this procedure.</span></span>  

