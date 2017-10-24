--- 
title: "设置采购订单储存的位置指令"
description: "此过程显示如何设置简单的位置指令。"
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 45e1e54c807597d4d5ff7370748012cbf28c1c6b
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a><span data-ttu-id="286eb-103">设置采购订单储存的位置指令</span><span class="sxs-lookup"><span data-stu-id="286eb-103">Set up a location directive for purchase order put-away</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="286eb-104">此过程显示如何设置简单的位置指令。</span><span class="sxs-lookup"><span data-stu-id="286eb-104">This procedure shows you how to set up a simple location directive.</span></span> <span data-ttu-id="286eb-105">显示的示例创建将用于确定在何处放置已收到的采购订单的物料的位置指令。</span><span class="sxs-lookup"><span data-stu-id="286eb-105">The example that’s shown creates a location directive to be used to determine where to put items that have been received for a purchase order.</span></span> <span data-ttu-id="286eb-106">您可以使用演示数据公司 USMF 提及的数据运行此任务指南。</span><span class="sxs-lookup"><span data-stu-id="286eb-106">You can play this task guide with the data mentioned using demo data company USMF.</span></span> <span data-ttu-id="286eb-107">先决条件：您需要创建一个处置代码。</span><span class="sxs-lookup"><span data-stu-id="286eb-107">Pre-conditions: You need to create a disposition code.</span></span> <span data-ttu-id="286eb-108">在该过程中，我们使用了一个被称为“重新贴标签”的处置代码。</span><span class="sxs-lookup"><span data-stu-id="286eb-108">In this procedure we use a disposition code called Relabel.</span></span> <span data-ttu-id="286eb-109">如果您正使用您自己的数据创建位置指令，您需要为您的仓库和物料设置高级仓库管理。</span><span class="sxs-lookup"><span data-stu-id="286eb-109">If you’re creating a location directive in your own data, you need to have set up advanced warehouse management for your warehouse and items.</span></span>  <span data-ttu-id="286eb-110">该过程专门面向仓库经理。</span><span class="sxs-lookup"><span data-stu-id="286eb-110">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="286eb-111">转到“库存管理”>“设置”>“位置指令”。</span><span class="sxs-lookup"><span data-stu-id="286eb-111">Go to Warehouse management > Setup > Location directives.</span></span>
2. <span data-ttu-id="286eb-112">在“工作订单类型”字段中，选择“采购订单”。</span><span class="sxs-lookup"><span data-stu-id="286eb-112">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-location-directive-header"></a><span data-ttu-id="286eb-113">创建位置指令标题</span><span class="sxs-lookup"><span data-stu-id="286eb-113">Create a location directive header</span></span>
1. <span data-ttu-id="286eb-114">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="286eb-114">Click New.</span></span>
2. <span data-ttu-id="286eb-115">在“序列号”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="286eb-115">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="286eb-116">这是处理选定工作类型的位置指令所需的序列。</span><span class="sxs-lookup"><span data-stu-id="286eb-116">This is the sequence in which the location directive is processed for the selected work type.</span></span> <span data-ttu-id="286eb-117">如果需要，您还可以修改序列。</span><span class="sxs-lookup"><span data-stu-id="286eb-117">You can also modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="286eb-118">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="286eb-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="286eb-119">这是此指令的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="286eb-119">This is the unique identifier for this directive.</span></span>  
4. <span data-ttu-id="286eb-120">在“工作类型”字段中，选择“放置”。</span><span class="sxs-lookup"><span data-stu-id="286eb-120">In the Work type field, select 'Put'.</span></span>
    * <span data-ttu-id="286eb-121">选择要执行的工作类型。</span><span class="sxs-lookup"><span data-stu-id="286eb-121">Select the type of work to be performed.</span></span> <span data-ttu-id="286eb-122">对于带有工作订单类型“采购订单”的指令，“放置”指令是唯一的支持值。</span><span class="sxs-lookup"><span data-stu-id="286eb-122">For directive with work order type Purchase order, Put is the only supported value.</span></span>  
5. <span data-ttu-id="286eb-123">在“站点”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="286eb-123">In the Site field, type a value.</span></span>
6. <span data-ttu-id="286eb-124">在“仓库”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="286eb-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="286eb-125">将指令代码留为空。</span><span class="sxs-lookup"><span data-stu-id="286eb-125">Leave the Directive code blank.</span></span>  <span data-ttu-id="286eb-126">指令代码用于将类型为“放置”的工作订单行链接到一个特定的指令。</span><span class="sxs-lookup"><span data-stu-id="286eb-126">Directive codes are used to link a work order line of type Put to a specific directive.</span></span> <span data-ttu-id="286eb-127">对于采购订单，在确定工作模板之前解决类型为“放置”的最后一个工作订单行的位置。</span><span class="sxs-lookup"><span data-stu-id="286eb-127">For purchase orders, the location of the last work order line of type Put is resolved before the work template is determined.</span></span> <span data-ttu-id="286eb-128">因此，不能工作模板的最后一行连接到一个特定的指令。</span><span class="sxs-lookup"><span data-stu-id="286eb-128">Therefore it is not possible to connect the last line of a work template to a specific directive.</span></span>   
7. <span data-ttu-id="286eb-129">在“处置码”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="286eb-129">In the Disposition code field, type a value.</span></span>
    * <span data-ttu-id="286eb-130">“处置代码”会限制使用位置指令，因此，仅当仓库工人使用移动设备登记物料期间输入此特定值时，可以使用位置指令。</span><span class="sxs-lookup"><span data-stu-id="286eb-130">The Disposition code limits the use of the location directive, so the location directive is only used if the warehouse worker enters this specific value during registration of the item using a mobile device.</span></span>  
8. <span data-ttu-id="286eb-131">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="286eb-131">Click Save.</span></span>

## <a name="edit-the-query-for-directive"></a><span data-ttu-id="286eb-132">编辑指令查询</span><span class="sxs-lookup"><span data-stu-id="286eb-132">Edit the query for directive</span></span>
1. <span data-ttu-id="286eb-133">单击“编辑查询”。</span><span class="sxs-lookup"><span data-stu-id="286eb-133">Click Edit query.</span></span>
    * <span data-ttu-id="286eb-134">本指令的使用已被限制用于在您指定的仓库中，使用您指定的处置代码登记的物料。</span><span class="sxs-lookup"><span data-stu-id="286eb-134">The use of this directive is already limited to be used for items registered in the warehouse that you specified, and with the disposition code that you specified.</span></span> <span data-ttu-id="286eb-135">您可以使用查询添加其他限制条件。</span><span class="sxs-lookup"><span data-stu-id="286eb-135">You can add other constraints using the query.</span></span>  
2. <span data-ttu-id="286eb-136">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="286eb-136">Click OK.</span></span>

## <a name="add-directive-lines"></a><span data-ttu-id="286eb-137">添加指令行</span><span class="sxs-lookup"><span data-stu-id="286eb-137">Add directive lines</span></span>
1. <span data-ttu-id="286eb-138">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="286eb-138">Click New.</span></span>
    * <span data-ttu-id="286eb-139">这是处理选定工作类型的位置指令行所需的序列。</span><span class="sxs-lookup"><span data-stu-id="286eb-139">This is the sequence in which the location directive lines are processed for the selected work type.</span></span> <span data-ttu-id="286eb-140">如果需要，您还可以修改序列。</span><span class="sxs-lookup"><span data-stu-id="286eb-140">You can also modify the sequence, if needed.</span></span>  
2. <span data-ttu-id="286eb-141">在“起始数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="286eb-141">In the From quantity field, enter a number.</span></span>
    * <span data-ttu-id="286eb-142">这是本治疗行适用的最低数量。</span><span class="sxs-lookup"><span data-stu-id="286eb-142">This is the lowest quantity that this directive line is valid for.</span></span>  
3. <span data-ttu-id="286eb-143">在“截止数量”字段中，输入一个数字。</span><span class="sxs-lookup"><span data-stu-id="286eb-143">In the To quantity field, enter a number.</span></span>
4. <span data-ttu-id="286eb-144">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="286eb-144">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="286eb-145">“起始数量”和“截止数量”会显示在单位中。</span><span class="sxs-lookup"><span data-stu-id="286eb-145">The unit the From quantity and To quantity is expressed in.</span></span> <span data-ttu-id="286eb-146">如果您将此字段留空，则将使用该物料的库存单位。</span><span class="sxs-lookup"><span data-stu-id="286eb-146">If you leave this field blank the inventory unit from the item is used.</span></span>  
5. <span data-ttu-id="286eb-147">在“查找数量”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="286eb-147">In the Locate quantity field, select an option.</span></span>
    * <span data-ttu-id="286eb-148">“无”或“牌照数量”：每个牌照上登记的数量。</span><span class="sxs-lookup"><span data-stu-id="286eb-148">None, or licence plate quantity: The quantity registered on each licence plate.</span></span> <span data-ttu-id="286eb-149">统一的数量：已登记的整个数量。</span><span class="sxs-lookup"><span data-stu-id="286eb-149">Unitized quantity: The entire quantity that’s been registered.</span></span> <span data-ttu-id="286eb-150">剩余数量：尚未登记的源自采购订单行的数量。</span><span class="sxs-lookup"><span data-stu-id="286eb-150">Remaining quantity: The quantity that is yet to be registered from the purchase order line.</span></span> <span data-ttu-id="286eb-151">预计数量：采购订单行上指明的总数量。</span><span class="sxs-lookup"><span data-stu-id="286eb-151">Expected quantity: The total quantity that is specified on the purchase order line.</span></span>  
6. <span data-ttu-id="286eb-152">选中或取消选中“按单位施加限制”复选框。</span><span class="sxs-lookup"><span data-stu-id="286eb-152">Check or uncheck the Restrict by unit checkbox.</span></span>
    * <span data-ttu-id="286eb-153">如果您选择此选项，并在“按单位施加限制”页上指定单位，则只有带该度量单位的物料可以放置到该位置中。</span><span class="sxs-lookup"><span data-stu-id="286eb-153">If you select this option, and specify the unit on the Restrict by unit page, only items with that unit of measurement can be put into the location.</span></span> <span data-ttu-id="286eb-154">例如，如果度量单位是 PL（托盘），则仅可将托盘中的物料存放到指定位置中。</span><span class="sxs-lookup"><span data-stu-id="286eb-154">For example, if the unit of measurement is PL (pallets), only items in pallets can be put into the specified location.</span></span>  
7. <span data-ttu-id="286eb-155">选中或取消选中“允许分割”复选框。</span><span class="sxs-lookup"><span data-stu-id="286eb-155">Check or uncheck the Allow split checkbox.</span></span>
    * <span data-ttu-id="286eb-156">这允许该指令在多个位置之间划分数量。</span><span class="sxs-lookup"><span data-stu-id="286eb-156">This allows the directive to split the quantity across multiple locations.</span></span>  
8. <span data-ttu-id="286eb-157">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="286eb-157">Click Save.</span></span>

## <a name="restrict-the-directive-line-to-a-specific-unit"></a><span data-ttu-id="286eb-158">将指令行限制为特订单位</span><span class="sxs-lookup"><span data-stu-id="286eb-158">Restrict the directive line to a specific unit</span></span>
1. <span data-ttu-id="286eb-159">单击“按单位施加限制”。</span><span class="sxs-lookup"><span data-stu-id="286eb-159">Click Restrict by unit.</span></span>
    * <span data-ttu-id="286eb-160">仅在您已选择“按单位施加限制”复选框之后，按下“保存”时，此按钮才可用。</span><span class="sxs-lookup"><span data-stu-id="286eb-160">This button is only available when you press Save after you have selected the Restrict by unit check box.</span></span>  
2. <span data-ttu-id="286eb-161">在“单位”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="286eb-161">In the Unit field, type a value.</span></span>
3. <span data-ttu-id="286eb-162">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="286eb-162">Close the page.</span></span>

## <a name="add-a-location-directive-action-line"></a><span data-ttu-id="286eb-163">添加位置指令操作行</span><span class="sxs-lookup"><span data-stu-id="286eb-163">Add a location directive action line</span></span>
1. <span data-ttu-id="286eb-164">单击“新建”。</span><span class="sxs-lookup"><span data-stu-id="286eb-164">Click New.</span></span>
    * <span data-ttu-id="286eb-165">这是处理选定工作类型的位置指令行操作所需的序列。</span><span class="sxs-lookup"><span data-stu-id="286eb-165">This is the sequence in which the location directive action lines are processed for the selected work type.</span></span> <span data-ttu-id="286eb-166">如果需要，您还可以修改序列。</span><span class="sxs-lookup"><span data-stu-id="286eb-166">You can also modify the sequence, if needed.</span></span>  
2. <span data-ttu-id="286eb-167">在“名称”字段中，键入一个值。</span><span class="sxs-lookup"><span data-stu-id="286eb-167">In the Name field, type a value.</span></span>
    * <span data-ttu-id="286eb-168">这是此指令操作适用的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="286eb-168">This is the unique identifier for this directive action.</span></span>  
3. <span data-ttu-id="286eb-169">在“固定位置使用”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="286eb-169">In the Fixed location usage field, select an option.</span></span>
    * <span data-ttu-id="286eb-170">固定和非固定货位︰所有非固定货位以及产品所有的固定货位均有效，在查询中指定的范围之内。</span><span class="sxs-lookup"><span data-stu-id="286eb-170">Fixed and non-fixed locations: All non-fixed locations are valid as well as the product’s own fixed location, within the range specified in the query.</span></span>  <span data-ttu-id="286eb-171">仅产品的固定货位︰产品的固定货位是有效的，所有产品变型都共享一组相同的固定货位。</span><span class="sxs-lookup"><span data-stu-id="286eb-171">Only fixed location for the product: Fixed locations for the product are valid, and all product variants share the same set of fixed locations.</span></span> <span data-ttu-id="286eb-172">仅产品变型固定货位︰仅为每个产品变型指定的固定货位有效。</span><span class="sxs-lookup"><span data-stu-id="286eb-172">Only fixed location for the product variants: Only fixed locations specified for each product variant are valid.</span></span>  
4. <span data-ttu-id="286eb-173">在“策略”字段中，选择一个选项。</span><span class="sxs-lookup"><span data-stu-id="286eb-173">In the Strategy field, select an option.</span></span>
    * <span data-ttu-id="286eb-174">工作订单类型“采购订单”支持以下策略：无：物料被存放到找到的第一个位置中。</span><span class="sxs-lookup"><span data-stu-id="286eb-174">Work orders of type Purchase order support the following strategies: None: the item is placed at the first location that’s found.</span></span> <span data-ttu-id="286eb-175">合并：物料被存放到类似物料已经可用的位置中。</span><span class="sxs-lookup"><span data-stu-id="286eb-175">Consolidate: The item is placed in a location where similar items are already available.</span></span> <span data-ttu-id="286eb-176">无传入工作的空位置：物料被存放到找到的第一个空位置中。</span><span class="sxs-lookup"><span data-stu-id="286eb-176">Empty location with no incoming work: the item is placed in the first empty location that’s found.</span></span> <span data-ttu-id="286eb-177">如果没有实际库存且没有预计的传入工作，则该位置将被视为空位置。</span><span class="sxs-lookup"><span data-stu-id="286eb-177">A location is considered to be empty if it has no physical inventory and no expected incoming work.</span></span>  
5. <span data-ttu-id="286eb-178">单击“保存”。</span><span class="sxs-lookup"><span data-stu-id="286eb-178">Click Save.</span></span>

## <a name="edit-the-query-for-directive-action-line"></a><span data-ttu-id="286eb-179">编辑指令操作行查询</span><span class="sxs-lookup"><span data-stu-id="286eb-179">Edit the query for directive action line</span></span>
1. <span data-ttu-id="286eb-180">单击“编辑查询”。</span><span class="sxs-lookup"><span data-stu-id="286eb-180">Click Edit query.</span></span>
2. <span data-ttu-id="286eb-181">单击“添加”。</span><span class="sxs-lookup"><span data-stu-id="286eb-181">Click Add.</span></span>
3. <span data-ttu-id="286eb-182">在“字段”字段中，键入“位置模板 ID”。</span><span class="sxs-lookup"><span data-stu-id="286eb-182">In the Field field, type 'location profile ID'.</span></span>
    * <span data-ttu-id="286eb-183">在此示例中，我们将使用位置模板 ID，限制可能的位置。</span><span class="sxs-lookup"><span data-stu-id="286eb-183">In this example, we’ll restrict the possible locations using a location profile ID.</span></span>  
4. <span data-ttu-id="286eb-184">在“标准”字段中，输入一个值。</span><span class="sxs-lookup"><span data-stu-id="286eb-184">In the Criteria field, type a value.</span></span>
5. <span data-ttu-id="286eb-185">单击“确定”。</span><span class="sxs-lookup"><span data-stu-id="286eb-185">Click OK.</span></span>
    * <span data-ttu-id="286eb-186">您可以继续添加指令行和指令操作，直到您已覆盖您的仓库的所有可能场景。</span><span class="sxs-lookup"><span data-stu-id="286eb-186">You can continue to add directive lines and directive actions until you have covered all the possible scenarios in your warehouse.</span></span>  

