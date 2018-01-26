---
title: "使用移动设备登记物料消耗量"
description: "此主题介绍允许使用手持设备登记生产中的原材料消耗量的工作流。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3c43a42822f291607fbc9708dd07ebf99b9d7ec4
ms.openlocfilehash: 33e880107588b80c0944f166ff999b117356731b
ms.contentlocale: zh-cn
ms.lasthandoff: 01/26/2018

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="756fc-103">使用移动设备登记物料消耗量</span><span class="sxs-lookup"><span data-stu-id="756fc-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="756fc-104">此主题介绍允许使用手持设备登记生产中的原材料消耗量的工作流。</span><span class="sxs-lookup"><span data-stu-id="756fc-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="756fc-105">简介</span><span class="sxs-lookup"><span data-stu-id="756fc-105">Introduction</span></span>
------------

<span data-ttu-id="756fc-106">如果对物料可跟踪性有严格的要求，则此工作流相关。</span><span class="sxs-lookup"><span data-stu-id="756fc-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="756fc-107">在这些情况下，为了维护物料的可追踪性，必须申报消耗量的准确时间和数量。</span><span class="sxs-lookup"><span data-stu-id="756fc-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="756fc-108">此流程可能被视为与预先耗用或反向耗用工序（登记时间与发生实际消耗的时间之间存在偏移）相反。</span><span class="sxs-lookup"><span data-stu-id="756fc-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="756fc-109">这解释了为什么自动消耗策略无法用于具有可追踪性要求的一些物料。</span><span class="sxs-lookup"><span data-stu-id="756fc-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="756fc-110">我们来看一个简单的方案解释如何设置工作流以允许通过手持设备登记生产中的原材料消耗量。</span><span class="sxs-lookup"><span data-stu-id="756fc-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> <span data-ttu-id="756fc-111">[![设置使用手持设备启用原材料消耗量登记的工作流](./media/scenario3.png)](./media/scenario3.png)</span><span class="sxs-lookup"><span data-stu-id="756fc-111">[![set up a workflow to enable registration of raw material consumption by using a handheld device](./media/scenario3.png)](./media/scenario3.png)</span></span>

### <a name="scenario-details"></a><span data-ttu-id="756fc-112">方案详细信息</span><span class="sxs-lookup"><span data-stu-id="756fc-112">Scenario details</span></span>

<span data-ttu-id="756fc-113">一个连续生产流程 (5) 使用受批次控制的原材料 RM-100。</span><span class="sxs-lookup"><span data-stu-id="756fc-113">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="756fc-114">物料是牌照 PL-1 上的库位 Bulk-001 (1) 上的现有物料，具有两个批次，B1 和 B2，数量均为 100 磅。</span><span class="sxs-lookup"><span data-stu-id="756fc-114">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="756fc-115">仓库工作 (2) 为 RM-100 进行发布和处理，且物料从 Bulk-001 领取到被定义为非牌照控制的生产输入库位 PIL-01 (3)。</span><span class="sxs-lookup"><span data-stu-id="756fc-115">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="756fc-116">机器操作员从生产输入库位 (3) 称出物料并将重量和批处理号登记为已使用 (4)。</span><span class="sxs-lookup"><span data-stu-id="756fc-116">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="756fc-117">从生产输入库位，部分物料在定义的时间间隔内被手动添加到生产流程。</span><span class="sxs-lookup"><span data-stu-id="756fc-117">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="756fc-118">在机器操作员添加物料时，物料在秤上称重，并登记批号。</span><span class="sxs-lookup"><span data-stu-id="756fc-118">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="756fc-119">设置工作流以使用手持设备登记消耗量</span><span class="sxs-lookup"><span data-stu-id="756fc-119">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="756fc-120">使用具有受批次控制的原材料 RM-100 的物料清单创建成品产品 FG-100。</span><span class="sxs-lookup"><span data-stu-id="756fc-120">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="756fc-121">将数量为 100 的 RM-100 的两个批次，B1 和 B2，添加到库位：Bulk-001，牌照：PL-1。</span><span class="sxs-lookup"><span data-stu-id="756fc-121">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="756fc-122">RM-100 在物料清单行上的耗用原则设置为**手动**。</span><span class="sxs-lookup"><span data-stu-id="756fc-122">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="756fc-123">将生产输入库位设置为 PIL-01。</span><span class="sxs-lookup"><span data-stu-id="756fc-123">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="756fc-124">为此，您可以选择此库位作为仓库 51 上的默认生产输入库位。</span><span class="sxs-lookup"><span data-stu-id="756fc-124">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="756fc-125">创建新的移动设备菜单项：</span><span class="sxs-lookup"><span data-stu-id="756fc-125">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="756fc-126">**菜单项名称** - 登记物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="756fc-126">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="756fc-127">**标题** - 登记物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="756fc-127">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="756fc-128">**模式** - 间接。</span><span class="sxs-lookup"><span data-stu-id="756fc-128">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="756fc-129">**活动代码** - 登记物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="756fc-129">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="756fc-130">将菜单项添加到**生产移动**设备菜单。</span><span class="sxs-lookup"><span data-stu-id="756fc-130">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="756fc-131">创建成品的生产订单：</span><span class="sxs-lookup"><span data-stu-id="756fc-131">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="756fc-132">**物料编号** - FG-100</span><span class="sxs-lookup"><span data-stu-id="756fc-132">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="756fc-133">**站点** - 5</span><span class="sxs-lookup"><span data-stu-id="756fc-133">**Site** - 5</span></span> 
-    <span data-ttu-id="756fc-134">**仓库** - 51</span><span class="sxs-lookup"><span data-stu-id="756fc-134">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="756fc-135">**数量** - 150</span><span class="sxs-lookup"><span data-stu-id="756fc-135">**Quantity** - 150</span></span>

<span data-ttu-id="756fc-136">生产订单为**估计**和**已发布**，并创建仓库工作。</span><span class="sxs-lookup"><span data-stu-id="756fc-136">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="756fc-137">使用用于手持设备的原材料领料工作流完成工作。</span><span class="sxs-lookup"><span data-stu-id="756fc-137">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="756fc-138">这将把物料从堆放库位移到生产输入库位 PIL-01。</span><span class="sxs-lookup"><span data-stu-id="756fc-138">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="756fc-139">完成工作后，物料状态为**已在生产输入库位上领料**。</span><span class="sxs-lookup"><span data-stu-id="756fc-139">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="756fc-140">工作处理后的状态可能为**已领料**或**实际预留**。</span><span class="sxs-lookup"><span data-stu-id="756fc-140">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="756fc-141">这使用参数**置于仓库后的发货状态窗体**进行配置。</span><span class="sxs-lookup"><span data-stu-id="756fc-141">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="756fc-142">使用**生产开始**菜单项从客户端或从手持设备开始生产订单。</span><span class="sxs-lookup"><span data-stu-id="756fc-142">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="756fc-143">在开始执行生产订单后，您可以使用用于手持设备的工作流登记物料消耗量。</span><span class="sxs-lookup"><span data-stu-id="756fc-143">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="756fc-144">我们先将批次 B1 的消耗量登记为 25 磅。</span><span class="sxs-lookup"><span data-stu-id="756fc-144">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="756fc-145">在手持设备的菜单中选择**登记物料****消耗量**菜单项，输入以下详细信息：</span><span class="sxs-lookup"><span data-stu-id="756fc-145">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="756fc-146">生产订单编号。</span><span class="sxs-lookup"><span data-stu-id="756fc-146">The production order number.</span></span> 
-    <span data-ttu-id="756fc-147">要消耗物料的库位，在此例中为 PIL-01。</span><span class="sxs-lookup"><span data-stu-id="756fc-147">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="756fc-148">物料编号 RM-100。</span><span class="sxs-lookup"><span data-stu-id="756fc-148">Item number RM-100.</span></span> 
-    <span data-ttu-id="756fc-149">批处理号 B1。</span><span class="sxs-lookup"><span data-stu-id="756fc-149">Batch number B1.</span></span> 
-    <span data-ttu-id="756fc-150">数量 25。</span><span class="sxs-lookup"><span data-stu-id="756fc-150">A quantity of 25.</span></span>

7.  <span data-ttu-id="756fc-151">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="756fc-151">Select **OK**.</span></span>

<span data-ttu-id="756fc-152">请注意，显示屏上显示消息“已创建日记帐行”。</span><span class="sxs-lookup"><span data-stu-id="756fc-152">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="756fc-153">在生产订单上有一个针对物料编号 RM-100 和批处理号 B1 的**生产领料单**类型的未结日记帐。</span><span class="sxs-lookup"><span data-stu-id="756fc-153">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="756fc-154">您现在可以选择继续登记，例如在批处理号 B2 上，且每一次选择**确定**，都会在未结日记帐上添加新的日记帐行。</span><span class="sxs-lookup"><span data-stu-id="756fc-154">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="756fc-155">结束登记后，选择**完成**以过帐日记帐和结束工作流。</span><span class="sxs-lookup"><span data-stu-id="756fc-155">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="756fc-156">其他注释</span><span class="sxs-lookup"><span data-stu-id="756fc-156">Additional comments</span></span> 

-   <span data-ttu-id="756fc-157">如果用户在创建日记帐行后取消工作流，日记帐将处于未过帐状态，但如果用户稍后对相同生产订单使用工作流，则行将被添加到未结日记帐，而不是添加到新的日记帐上。</span><span class="sxs-lookup"><span data-stu-id="756fc-157">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="756fc-158">新工作流还支持序列号的登记。</span><span class="sxs-lookup"><span data-stu-id="756fc-158">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="756fc-159">只能登记在所选生产订单或批次订单的物料清单或配方中定义的物料编号。</span><span class="sxs-lookup"><span data-stu-id="756fc-159">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="756fc-160">物料可以过度消耗。</span><span class="sxs-lookup"><span data-stu-id="756fc-160">Material can be overconsumed.</span></span> <span data-ttu-id="756fc-161">例如，如果物料的估计消耗数量为 100 磅，则可以过度消耗，例如数量 105 磅。</span><span class="sxs-lookup"><span data-stu-id="756fc-161">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



