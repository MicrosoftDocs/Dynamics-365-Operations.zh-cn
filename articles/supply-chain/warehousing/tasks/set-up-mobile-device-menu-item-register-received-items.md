--- 
title: "设置登记已接收物料的移动设备菜单项"
description: "此任务重点是设置移动设备菜单项。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem, WHSRFMenu
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 3cab7eced20111b82afabe69b6f994333b16209a
ms.contentlocale: zh-cn
ms.lasthandoff: 09/14/2018

---
# <a name="set-up-a-mobile-device-menu-item-to-register-received-items"></a><span data-ttu-id="27e6f-103">设置登记已接收物料的移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="27e6f-103">Set up a mobile device menu item to register received items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="27e6f-104">此任务重点是设置移动设备菜单项。</span><span class="sxs-lookup"><span data-stu-id="27e6f-104">This task focuses on the setup of a mobile device menu item.</span></span> <span data-ttu-id="27e6f-105">此菜单项用于通过采购订单采购的物料的登记和接收。</span><span class="sxs-lookup"><span data-stu-id="27e6f-105">This menu item is used for registration of the receipt of items ordered via purchase orders.</span></span> 

<span data-ttu-id="27e6f-106">您可以使用演示数据公司 USMF 运行此指南。</span><span class="sxs-lookup"><span data-stu-id="27e6f-106">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="27e6f-107">该过程专门面向仓库经理。</span><span class="sxs-lookup"><span data-stu-id="27e6f-107">This procedure is intended for the warehouse manager.</span></span>


## <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="27e6f-108">创建移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="27e6f-108">Create a mobile device menu item</span></span>
1. <span data-ttu-id="27e6f-109">转到“仓库管理”>“设置”>“移动设备”>“移动设备菜单项”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-109">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="27e6f-110">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-110">Click New.</span></span>
3. <span data-ttu-id="27e6f-111">在“菜单项名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="27e6f-111">In the Menu item name field, type a value.</span></span>
    * <span data-ttu-id="27e6f-112">这是移动设备菜单项的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="27e6f-112">This is the unique identifier for this mobile device menu item.</span></span> <span data-ttu-id="27e6f-113">例如，您可以输入“我的采购订单登记”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-113">For example, you could type 'My PO registration'.</span></span>  
4. <span data-ttu-id="27e6f-114">在“标题”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="27e6f-114">In the Title field, type a value.</span></span>
    * <span data-ttu-id="27e6f-115">这是标题，将向移动设备用户显示。</span><span class="sxs-lookup"><span data-stu-id="27e6f-115">This is the title, which will be displayed to the user on the mobile device.</span></span> <span data-ttu-id="27e6f-116">例如，您可以输入“采购订单登记”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-116">For example, you could type 'PO registration'.</span></span>  
5. <span data-ttu-id="27e6f-117">在“模式”字段中，选择“工作”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-117">In the Mode field, select 'Work'.</span></span>
    * <span data-ttu-id="27e6f-118">登记采购订单的现有接收量会创建将物料从接收区移到库存的工作。</span><span class="sxs-lookup"><span data-stu-id="27e6f-118">Registration of on-hand quantities received for a purchase order line will create work to move the items from the receiving area into the inventory.</span></span> <span data-ttu-id="27e6f-119">在登记物料前不会创建工作。</span><span class="sxs-lookup"><span data-stu-id="27e6f-119">Work isn’t created until the items are registered.</span></span>  <span data-ttu-id="27e6f-120">因此，将“使用现有工作”选项的设置留为“否”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-120">Therefore, leave the Use existing work option set to No.</span></span>  
6. <span data-ttu-id="27e6f-121">展开或收起“常规”部分。</span><span class="sxs-lookup"><span data-stu-id="27e6f-121">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="27e6f-122">在“工作创建流程”字段中，选择“接收的采购订单物料”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-122">In the Work creation process field, select 'Purchase order item receiving'.</span></span>
    * <span data-ttu-id="27e6f-123">现有采购订单行必须具有唯一标识符才能在仓库中登记。</span><span class="sxs-lookup"><span data-stu-id="27e6f-123">A purchase order line must be uniquely identified before on-hand can be registered in the warehouse.</span></span> <span data-ttu-id="27e6f-124">在此场景中，移动设备将登记采购订单号和物料编号，并且这将允许系统识别采购订单行。</span><span class="sxs-lookup"><span data-stu-id="27e6f-124">In this scenario, the mobile device will register the purchase order number and item number, and this will allow the system to identify the PO line.</span></span> <span data-ttu-id="27e6f-125">将会创建入库工作，并且另一工作人员可承担该工作。</span><span class="sxs-lookup"><span data-stu-id="27e6f-125">Put away work will be created and can be picked up by another worker.</span></span>    <span data-ttu-id="27e6f-126"> 您选择的工作创建方法确定哪些字段会出现在“常规”快速选项卡上。</span><span class="sxs-lookup"><span data-stu-id="27e6f-126">The work creation method that you select determines which fields become available on the General fast tab.</span></span>  
    * <span data-ttu-id="27e6f-127">如果您选择“使用默认数据”选项，默认数据按钮将会启用。</span><span class="sxs-lookup"><span data-stu-id="27e6f-127">If you select the Use default data option, the Default data button is enabled.</span></span> <span data-ttu-id="27e6f-128">您可以在这里选择字段从而显示工作人员在日常工作中通常需要的数据，以在移动设备上显示这些值。</span><span class="sxs-lookup"><span data-stu-id="27e6f-128">Here you can select fields to display data that a worker typically needs in their daily work, so that these values are shown on the mobile device.</span></span>  
    * <span data-ttu-id="27e6f-129">牌照分组参数与分配给接收物料的单位序列组同样有效。</span><span class="sxs-lookup"><span data-stu-id="27e6f-129">The License plate grouping parameter  works in combination with the unit sequence group that’s assigned to the item that’s being received.</span></span> <span data-ttu-id="27e6f-130">您可以指定是否应将少于或多于一个托盘的收据分组到一个牌照中，或划分为适用于每个单位的单独牌照。</span><span class="sxs-lookup"><span data-stu-id="27e6f-130">You can specify whether receipts of less than or more than one pallet should be grouped into one license plate, or divided into a separate license plate for each unit.</span></span>  
    * <span data-ttu-id="27e6f-131">如果您选择“生成牌照”选项卡，将根据编号规则选项生成唯一牌照号。</span><span class="sxs-lookup"><span data-stu-id="27e6f-131">If you select the Generate license plate  option, this generates a unique license plate number based on the number sequence selection.</span></span>   
    * <span data-ttu-id="27e6f-132">您可以选择创建工作时使用的模板。</span><span class="sxs-lookup"><span data-stu-id="27e6f-132">You can select the template that will be used when work is created.</span></span> <span data-ttu-id="27e6f-133">例如，如果您登记了采购订单中的某个物料，那么会基于工作模板生成入库工作。</span><span class="sxs-lookup"><span data-stu-id="27e6f-133">For example, if you register an item for a purchase order, the put away work will be generated based on the work template.</span></span> <span data-ttu-id="27e6f-134">如果您没有选择工作模板，则系统将基于与模板相关的查询条件分配模板。</span><span class="sxs-lookup"><span data-stu-id="27e6f-134">If you don’t select a work template here, the system will assign a template based on the query criteria that are associated with the templates.</span></span>  
    * <span data-ttu-id="27e6f-135">如果处置代码在移动设备上显示，工作人员可评估物料的状态和质量，并选择相应代码。</span><span class="sxs-lookup"><span data-stu-id="27e6f-135">If disposition codes are displayed on the mobile device, workers can evaluate the status or quality of the items, and select the appropriate code.</span></span> <span data-ttu-id="27e6f-136">处置代码规则决定了物料是否可用于其他仓库流程。</span><span class="sxs-lookup"><span data-stu-id="27e6f-136">The rules for  the disposition code determine whether the items will be available to other warehouse processes.</span></span> <span data-ttu-id="27e6f-137">规则还决定哪个库位指令用于已创建的工作。</span><span class="sxs-lookup"><span data-stu-id="27e6f-137">The rules also determine which location directive is used for the work that’s created.</span></span>   
    * <span data-ttu-id="27e6f-138">如果您选择“批处置代码”选项，工作人员可评估批次的状态和质量，并选择相应处置代码。</span><span class="sxs-lookup"><span data-stu-id="27e6f-138">If you select the Batch disposition codes option, workers can evaluate the status or quality of a batch, and select the appropriate disposition code.</span></span>  <span data-ttu-id="27e6f-139">批处置代码设置的规则决定了该批次是否可用于其他仓库流程。</span><span class="sxs-lookup"><span data-stu-id="27e6f-139">The rules that are set on the batch disposition code determine whether the batch will be available to other warehouse processes.</span></span>  
    * <span data-ttu-id="27e6f-140">如果您选择“打印标签”选项，在接收物料时会自动打印牌照标签。</span><span class="sxs-lookup"><span data-stu-id="27e6f-140">If you select the Print labels option a license plate label will be printed automatically when items are received.</span></span>  
8. <span data-ttu-id="27e6f-141">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-141">Click Save.</span></span>
9. <span data-ttu-id="27e6f-142">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="27e6f-142">Close the page.</span></span>

## <a name="add-the-menu-item-to-a-mobile-device-menu"></a><span data-ttu-id="27e6f-143">添加菜单项到一个移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="27e6f-143">Add the menu item to a mobile device menu</span></span>
1. <span data-ttu-id="27e6f-144">转到“仓库管理”>“设置”>“设置”>“移动设备菜单”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-144">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
2. <span data-ttu-id="27e6f-145">使用“快速筛选器”以筛选带“入货”值的“名称”字段。</span><span class="sxs-lookup"><span data-stu-id="27e6f-145">Use the Quick Filter to filter on the Name field with a value of 'inbound'.</span></span>
3. <span data-ttu-id="27e6f-146">单击“编辑”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-146">Click Edit.</span></span>
4. <span data-ttu-id="27e6f-147">在树形图中，选择“在可用的菜单和物料树形图中，选择您先前创建的菜单项”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-147">In the tree, select 'In the Available menu's and items tree, select the menu item that you created before.'.</span></span>
    * <span data-ttu-id="27e6f-148">选择您之前创建的菜单项。</span><span class="sxs-lookup"><span data-stu-id="27e6f-148">Select the menu item that you created before.</span></span>  
5. <span data-ttu-id="27e6f-149">单击向右箭头。</span><span class="sxs-lookup"><span data-stu-id="27e6f-149">Click on the arrow that points to the right.</span></span>
6. <span data-ttu-id="27e6f-150">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="27e6f-150">Click Save.</span></span>
7. <span data-ttu-id="27e6f-151">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="27e6f-151">Close the page.</span></span>


