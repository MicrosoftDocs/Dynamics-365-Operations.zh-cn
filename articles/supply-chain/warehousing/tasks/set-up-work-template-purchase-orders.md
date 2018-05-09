--- 
title: "设置采购订单的工作模板"
description: "该过程的重点是设置物料入库时使用的简单工作模板。"
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1bd59ffca94c57ad33f78f9e780d00b368750bc8
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="2f076-103">设置采购订单的工作模板</span><span class="sxs-lookup"><span data-stu-id="2f076-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2f076-104">该过程的重点是设置物料入库时使用的简单工作模板。</span><span class="sxs-lookup"><span data-stu-id="2f076-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="2f076-105">工作模板确定了在从接受区转移物料时，向仓管人员移动设备显示的指令集。</span><span class="sxs-lookup"><span data-stu-id="2f076-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="2f076-106">您可以使用演示数据公司 USMF 中提及的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="2f076-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="2f076-107">在您开始本指南之前，请创建工作池 ID。</span><span class="sxs-lookup"><span data-stu-id="2f076-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="2f076-108">在此示例中，将使用称为“进货”的工作池 ID。</span><span class="sxs-lookup"><span data-stu-id="2f076-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="2f076-109">该过程专门面向仓库经理。</span><span class="sxs-lookup"><span data-stu-id="2f076-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="2f076-110">转到“仓库管理”>“设置”>“工作”>“工作模板”。</span><span class="sxs-lookup"><span data-stu-id="2f076-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="2f076-111">在“工作订单类型”字段中，选择“采购订单”。</span><span class="sxs-lookup"><span data-stu-id="2f076-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="2f076-112">创建工作模板标题</span><span class="sxs-lookup"><span data-stu-id="2f076-112">Create a work template header</span></span>
1. <span data-ttu-id="2f076-113">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2f076-113">Click New.</span></span>
2. <span data-ttu-id="2f076-114">在“序列号”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="2f076-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="2f076-115">这是工作模板的评估顺序。</span><span class="sxs-lookup"><span data-stu-id="2f076-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="2f076-116">如果需要，可以修改此序列。</span><span class="sxs-lookup"><span data-stu-id="2f076-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="2f076-117">在“工作模板”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2f076-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="2f076-118">这是此模板的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="2f076-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="2f076-119">在“工作模板描述”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2f076-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="2f076-120">“有效”选项在您填写完模板所需的所有信息，以及单击“保存”后才会勾选。</span><span class="sxs-lookup"><span data-stu-id="2f076-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="2f076-121">采购订单类型的工作订单无法自动处理，因此将“自动处理”选项设置为“否”。</span><span class="sxs-lookup"><span data-stu-id="2f076-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="2f076-122">在”工作池 ID“字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2f076-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="2f076-123">工作池 ID 使您可组织工作组。</span><span class="sxs-lookup"><span data-stu-id="2f076-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="2f076-124">您在此处设置的值将为使用此模板创建的所有工作的默认值。</span><span class="sxs-lookup"><span data-stu-id="2f076-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="2f076-125">在“工作优先级”字段中，输入“1”。</span><span class="sxs-lookup"><span data-stu-id="2f076-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="2f076-126">这表明您在此处设置的工作重要性和值将会成为使用此模板创建的所有工作的默认值。</span><span class="sxs-lookup"><span data-stu-id="2f076-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="2f076-127">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="2f076-127">Click Save.</span></span>
    * <span data-ttu-id="2f076-128">您必须保存工作模板标题才能使用“编辑查询”按钮。</span><span class="sxs-lookup"><span data-stu-id="2f076-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="2f076-129">设置工作模板的查询</span><span class="sxs-lookup"><span data-stu-id="2f076-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="2f076-130">单击“编辑查询”。</span><span class="sxs-lookup"><span data-stu-id="2f076-130">Click Edit query.</span></span>
    * <span data-ttu-id="2f076-131">我们将设置模板仅在特定仓库中使用的限制。</span><span class="sxs-lookup"><span data-stu-id="2f076-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="2f076-132">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="2f076-132">Click Add.</span></span>
3. <span data-ttu-id="2f076-133">在列表中，标记所选的行。</span><span class="sxs-lookup"><span data-stu-id="2f076-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2f076-134">在“字段”字段中，键入“仓库”。</span><span class="sxs-lookup"><span data-stu-id="2f076-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="2f076-135">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="2f076-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="2f076-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="2f076-136">Click OK.</span></span>
7. <span data-ttu-id="2f076-137">单击“是”。</span><span class="sxs-lookup"><span data-stu-id="2f076-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="2f076-138">设置工作模板详细信息</span><span class="sxs-lookup"><span data-stu-id="2f076-138">Set work template details</span></span>
1. <span data-ttu-id="2f076-139">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2f076-139">Click New.</span></span>
2. <span data-ttu-id="2f076-140">在“工作类型”字段中，选择“领料”。</span><span class="sxs-lookup"><span data-stu-id="2f076-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="2f076-141">在“工作类 ID”字段中，键入“采购”。</span><span class="sxs-lookup"><span data-stu-id="2f076-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="2f076-142">您在此处设置的工作类将默认显示在使用此模板创建的领料类型的所有工作行上。</span><span class="sxs-lookup"><span data-stu-id="2f076-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="2f076-143">工作订单行上的工作类不能被覆盖。</span><span class="sxs-lookup"><span data-stu-id="2f076-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="2f076-144">工作类用于处理和/或限制工作订单行的类型，而仓管人员可以在移动设备上处理此类工作订单行。</span><span class="sxs-lookup"><span data-stu-id="2f076-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="2f076-145">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="2f076-145">Click New.</span></span>
5. <span data-ttu-id="2f076-146">在“工作类型”字段中，选择“放置”。</span><span class="sxs-lookup"><span data-stu-id="2f076-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="2f076-147">在“工作类 ID”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="2f076-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="2f076-148">已设置领料和放置指令。</span><span class="sxs-lookup"><span data-stu-id="2f076-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="2f076-149">每个领料/放置必须有相同的工作类。</span><span class="sxs-lookup"><span data-stu-id="2f076-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="2f076-150">使用与领料指令相同的工作类。</span><span class="sxs-lookup"><span data-stu-id="2f076-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="2f076-151">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="2f076-151">Click Save.</span></span>
    * <span data-ttu-id="2f076-152">请注意，“有效”复选框现在已勾选。</span><span class="sxs-lookup"><span data-stu-id="2f076-152">Note that the Valid checkbox is now checked.</span></span>  


