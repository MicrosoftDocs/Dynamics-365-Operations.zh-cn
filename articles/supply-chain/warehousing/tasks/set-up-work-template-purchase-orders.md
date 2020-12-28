---
title: 设置采购订单的工作模板
description: 此主题介绍如何设置物料入库时使用的简单工作模板。
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6628936a56619de255ca7dc7b332b5819918c310
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423209"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="1b193-103">设置采购订单的工作模板</span><span class="sxs-lookup"><span data-stu-id="1b193-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b193-104">此主题介绍如何设置物料入库时使用的简单工作模板。</span><span class="sxs-lookup"><span data-stu-id="1b193-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="1b193-105">工作模板确定了在从接受区转移物料时，向仓管人员移动设备显示的指令集。</span><span class="sxs-lookup"><span data-stu-id="1b193-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="1b193-106">您可以使用演示数据公司 USMF 中提及的数据运行该过程。</span><span class="sxs-lookup"><span data-stu-id="1b193-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="1b193-107">在您开始本指南之前，请创建工作池 ID。</span><span class="sxs-lookup"><span data-stu-id="1b193-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="1b193-108">在此示例中，将使用称为“进货”的工作池 ID。</span><span class="sxs-lookup"><span data-stu-id="1b193-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="1b193-109">该过程专门面向仓库经理。</span><span class="sxs-lookup"><span data-stu-id="1b193-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="1b193-110">在导航窗格中，转到 **模块 > 仓库管理 > 设置 > 工作 > 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="1b193-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="1b193-111">在 **工作订单类型** 字段中，选择 **采购订单**。</span><span class="sxs-lookup"><span data-stu-id="1b193-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="1b193-112">创建工作模板标题</span><span class="sxs-lookup"><span data-stu-id="1b193-112">Create a work template header</span></span>
1. <span data-ttu-id="1b193-113">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1b193-113">Select **New**.</span></span>
2. <span data-ttu-id="1b193-114">在 **序列号** 字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="1b193-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="1b193-115">这是工作模板的评估顺序。</span><span class="sxs-lookup"><span data-stu-id="1b193-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="1b193-116">如果需要，可以修改此序列。</span><span class="sxs-lookup"><span data-stu-id="1b193-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="1b193-117">在 **工作模板** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1b193-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="1b193-118">这是此模板的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="1b193-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="1b193-119">在 **工作模板描述** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1b193-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="1b193-120">**有效** 选项在您填写完模板所需的所有信息，以及选择 **保存** 后才会勾选。</span><span class="sxs-lookup"><span data-stu-id="1b193-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="1b193-121">**采购订单** 类型的工作订单无法自动处理，因此将 **自动处理** 选项设置为 **否**。</span><span class="sxs-lookup"><span data-stu-id="1b193-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="1b193-122">在 **工作池 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1b193-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="1b193-123">工作池 ID 使您可组织工作组。</span><span class="sxs-lookup"><span data-stu-id="1b193-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="1b193-124">您在此处设置的值将为使用此模板创建的所有工作的默认值。</span><span class="sxs-lookup"><span data-stu-id="1b193-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="1b193-125">在 **工作优先级** 字段中，输入 `1`。</span><span class="sxs-lookup"><span data-stu-id="1b193-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="1b193-126">这表明您在此处设置的工作重要性和值将会成为使用此模板创建的所有工作的默认值。</span><span class="sxs-lookup"><span data-stu-id="1b193-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="1b193-127">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b193-127">Select **Save**.</span></span> <span data-ttu-id="1b193-128">您必须保存工作模板标题才能使用 **编辑查询** 按钮。</span><span class="sxs-lookup"><span data-stu-id="1b193-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="1b193-129">设置工作模板的查询</span><span class="sxs-lookup"><span data-stu-id="1b193-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="1b193-130">选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="1b193-130">Select **Edit query**.</span></span> <span data-ttu-id="1b193-131">我们将设置模板仅在特定仓库中使用的限制。</span><span class="sxs-lookup"><span data-stu-id="1b193-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="1b193-132">选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="1b193-132">Select **Add**.</span></span>
3. <span data-ttu-id="1b193-133">在新行的 **现场** 字段中，输入 `warehouse`。</span><span class="sxs-lookup"><span data-stu-id="1b193-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="1b193-134">在 **条件** 字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="1b193-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="1b193-135">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1b193-135">Select **OK**.</span></span>
6. <span data-ttu-id="1b193-136">选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="1b193-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="1b193-137">设置工作模板详细信息</span><span class="sxs-lookup"><span data-stu-id="1b193-137">Set work template details</span></span>
1. <span data-ttu-id="1b193-138">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1b193-138">Select **New**.</span></span>
2. <span data-ttu-id="1b193-139">在 **工作类型** 字段中，选择 **领料**。</span><span class="sxs-lookup"><span data-stu-id="1b193-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="1b193-140">在 **工作类 ID** 字段中，键入 `purchase`。</span><span class="sxs-lookup"><span data-stu-id="1b193-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="1b193-141">您在此处设置的工作类将默认显示在使用此模板创建的领料类型的所有工作行上。</span><span class="sxs-lookup"><span data-stu-id="1b193-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="1b193-142">工作订单行上的工作类不能被覆盖。</span><span class="sxs-lookup"><span data-stu-id="1b193-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="1b193-143">工作类用于处理和/或限制工作订单行的类型，而仓管人员可以在移动设备上处理此类工作订单行。</span><span class="sxs-lookup"><span data-stu-id="1b193-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="1b193-144">选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="1b193-144">Select **New**.</span></span>
5. <span data-ttu-id="1b193-145">在 **工作类型** 字段中，选择 **放置**。</span><span class="sxs-lookup"><span data-stu-id="1b193-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="1b193-146">在 **工作类 ID** 字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="1b193-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="1b193-147">已设置领料和放置指令。</span><span class="sxs-lookup"><span data-stu-id="1b193-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="1b193-148">每个领料/放置必须有相同的工作类。</span><span class="sxs-lookup"><span data-stu-id="1b193-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="1b193-149">使用与领料指令相同的工作类。</span><span class="sxs-lookup"><span data-stu-id="1b193-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="1b193-150">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="1b193-150">Select **Save**.</span></span> <span data-ttu-id="1b193-151">请注意，**有效** 复选框现在已勾选。</span><span class="sxs-lookup"><span data-stu-id="1b193-151">Note that the **Valid** checkbox is now checked.</span></span>  

