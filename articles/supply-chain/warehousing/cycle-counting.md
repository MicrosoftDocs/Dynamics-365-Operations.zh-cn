---
title: "周期盘点"
description: "本文介绍如何使用仓库管理中提供的仓库解决方案使用周期盘点。 本文不适用于可用于库存管理的仓库解决方案。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ddb035eaa496a7c84f117f0523d509eccdf58505
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="cycle-counting"></a><span data-ttu-id="1ec56-104">周期盘点</span><span class="sxs-lookup"><span data-stu-id="1ec56-104">Cycle counting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1ec56-105">本文介绍如何使用仓库管理中提供的仓库解决方案使用周期盘点。</span><span class="sxs-lookup"><span data-stu-id="1ec56-105">This article describes how you can use cycle counting with the warehousing solution that is available in Warehouse management.</span></span> <span data-ttu-id="1ec56-106">本文不适用于可用于库存管理的仓库解决方案。</span><span class="sxs-lookup"><span data-stu-id="1ec56-106">This article doesn't apply to the warehousing solution that's available in Inventory management.</span></span>

<span data-ttu-id="1ec56-107">周期盘点是用于审计现有库存项目的仓库流程。</span><span class="sxs-lookup"><span data-stu-id="1ec56-107">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="1ec56-108">周期盘点流程可以在三个步骤中介绍：</span><span class="sxs-lookup"><span data-stu-id="1ec56-108">The cycle counting process can be described in three steps:</span></span>

1.  <span data-ttu-id="1ec56-109">**创建周期盘点工作** – 周期盘点工作可以是基于物料的临界值参数或通过周期盘点计划自动创建的。</span><span class="sxs-lookup"><span data-stu-id="1ec56-109">**Create cycle counting work** – Cycle counting work can be created automatically, based on threshold parameters for items or by using a cycle counting plan.</span></span> <span data-ttu-id="1ec56-110">或者，您可以通过在**按物料分类的周期盘点工作**页面或**按位置分类的周期盘点工作**页面中使用物料或仓库参数手动创建周期盘点计数工作。</span><span class="sxs-lookup"><span data-stu-id="1ec56-110">Alternatively, you can manually create cycle counting work by using the item or warehouse parameters on the **Cycle count work by item** page or the **Cycle count work by location** page.</span></span>
2.  <span data-ttu-id="1ec56-111">**处理周期盘点** – 在创建周期盘点工作之后，您通过盘点仓库库位的物料执行周期盘点，然后使用移动设备将结果输入到 Microsoft Dynamics 365 for Finance and Operations 中。</span><span class="sxs-lookup"><span data-stu-id="1ec56-111">**Process the cycle count** – After cycle counting work is created, you do the cycle counting work by counting items in a warehouse location and then using a mobile device to enter the result in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="1ec56-112">或者，您可以在不创建周期盘点的情况下在仓库场所盘点物料。</span><span class="sxs-lookup"><span data-stu-id="1ec56-112">Alternatively, you can count items in a warehouse location without creating cycle counting work.</span></span> <span data-ttu-id="1ec56-113">此过程被称为*现场周期盘点*。</span><span class="sxs-lookup"><span data-stu-id="1ec56-113">This process is referred to as *spot cycle counting*.</span></span>
3.  <span data-ttu-id="1ec56-114">**解决周期盘点值中的差异** – 周期盘点之后，与盘点值有差异的任何物料必须在**所有工作**页中设定为**待核查**的工作状态。</span><span class="sxs-lookup"><span data-stu-id="1ec56-114">**Resolve differences in the counted value** – After a cycle count, any items that have differences in the counted value will have a work status of **Pending review** on the **All work** page.</span></span> <span data-ttu-id="1ec56-115">您可以在**周期盘点工作待审阅**页上解决这些差异。</span><span class="sxs-lookup"><span data-stu-id="1ec56-115">You can resolve these differences on the **Cycle count work pending review** page.</span></span>

<span data-ttu-id="1ec56-116">下图显示了周期盘点流程。</span><span class="sxs-lookup"><span data-stu-id="1ec56-116">The following illustration shows the cycle counting process.</span></span> ![周期盘点流程](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a><span data-ttu-id="1ec56-118">周期盘点先决条件</span><span class="sxs-lookup"><span data-stu-id="1ec56-118">Cycle counting prerequisites</span></span>
<span data-ttu-id="1ec56-119">下表显示必须先就绪然后才能开始使用周期盘点。</span><span class="sxs-lookup"><span data-stu-id="1ec56-119">The following table shows the prerequisites that must be in place before you can use cycle counting.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1ec56-120">先决条件</span><span class="sxs-lookup"><span data-stu-id="1ec56-120">Prerequisite</span></span></th>
<th><span data-ttu-id="1ec56-121">描述</span><span class="sxs-lookup"><span data-stu-id="1ec56-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1ec56-122">物料</span><span class="sxs-lookup"><span data-stu-id="1ec56-122">Item</span></span></td>
<td><span data-ttu-id="1ec56-123">物料必须在仓库管理流程中启用。</span><span class="sxs-lookup"><span data-stu-id="1ec56-123">The item must be enabled for warehouse management processes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ec56-124">仓库</span><span class="sxs-lookup"><span data-stu-id="1ec56-124">Warehouse</span></span></td>
<td><span data-ttu-id="1ec56-125">仓库必须在仓库管理流程中启用。</span><span class="sxs-lookup"><span data-stu-id="1ec56-125">The warehouse must be enabled for warehouse management processes.</span></span> <span data-ttu-id="1ec56-126">要在仓库管理流程中启用仓库，请在<strong>仓库</strong>页中，选择仓库，然后选中<strong>使用仓库管理流程</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="1ec56-126">To enable the warehouse for warehouse management processes, on the <strong>Warehouses</strong> page, select the warehouse, and then select the <strong>Use warehouse management processes</strong> option.</span></span> <span data-ttu-id="1ec56-127">若要在周期盘点期间使工作人员能够移动栈板，在<strong>仓库管理</strong>快速选项卡上，选中<strong>允许在周期盘点期间移动托盘</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="1ec56-127">To enable workers to move pallets during a cycle count, on the <strong>Warehouse management</strong> FastTab, select the <strong>Allow pallet moves during cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ec56-128">工作池</span><span class="sxs-lookup"><span data-stu-id="1ec56-128">Work pools</span></span></td>
<td><span data-ttu-id="1ec56-129">可选：基于工作类型创建工作池来划分仓库工作（在这种情况下，周期盘点执行）。</span><span class="sxs-lookup"><span data-stu-id="1ec56-129">Optional: Create a work pool to segregate the warehouse work, based on the type of work (in this case, cycle counting work).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ec56-130">位置</span><span class="sxs-lookup"><span data-stu-id="1ec56-130">Locations</span></span></td>
<td><span data-ttu-id="1ec56-131">在场所中启用周期盘点。</span><span class="sxs-lookup"><span data-stu-id="1ec56-131">Enable cycle counting for locations.</span></span> <span data-ttu-id="1ec56-132">若要为仓库库位启用周期盘点，在<strong>位置配置文件</strong>页中，选择<strong>允许周期盘点</strong>选项。</span><span class="sxs-lookup"><span data-stu-id="1ec56-132">To enable cycle counting for a warehouse location, on the <strong>Location profiles</strong> page, select the <strong>Allow cycle counting</strong> option.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ec56-133">仓库管理参数</span><span class="sxs-lookup"><span data-stu-id="1ec56-133">Warehouse management parameters</span></span></td>
<td><span data-ttu-id="1ec56-134">为周期盘点设置参数。</span><span class="sxs-lookup"><span data-stu-id="1ec56-134">Set up parameters for cycle counting.</span></span> <span data-ttu-id="1ec56-135">在<strong>仓库管理参数</strong>页中，为周期盘点指定默认调整类型代码、工作类 ID 和工作优先级。</span><span class="sxs-lookup"><span data-stu-id="1ec56-135">On the <strong>Warehouse management parameters</strong> page, specify the default adjustment type code, work class ID, and work priority for cycle counting.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1ec56-136">移动设备</span><span class="sxs-lookup"><span data-stu-id="1ec56-136">Mobile device</span></span></td>
<td><ul>
<li><span data-ttu-id="1ec56-137">为<strong>移动设备菜单项</strong>页中以下方法中的一个创建一个菜单项：</span><span class="sxs-lookup"><span data-stu-id="1ec56-137">Create a menu item for one of the following methods on the <strong>Mobile device menu items</strong> page:</span></span>
<ul>
<li><span data-ttu-id="1ec56-138">用户指导的周期盘点</span><span class="sxs-lookup"><span data-stu-id="1ec56-138">User directed cycle counting</span></span></li>
<li><span data-ttu-id="1ec56-139">系统指导的周期盘点</span><span class="sxs-lookup"><span data-stu-id="1ec56-139">System directed cycle counting</span></span></li>
<li><span data-ttu-id="1ec56-140">周期盘点分组</span><span class="sxs-lookup"><span data-stu-id="1ec56-140">Cycle count grouping</span></span></li>
<li><span data-ttu-id="1ec56-141">现货周期盘点</span><span class="sxs-lookup"><span data-stu-id="1ec56-141">Spot cycle counting</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1ec56-142">设置移动设备的菜单。</span><span class="sxs-lookup"><span data-stu-id="1ec56-142">Set up a menu for the mobile device.</span></span></li>
<li><span data-ttu-id="1ec56-143">创建一个工作用户帐户并向工作用户 ID 分配一个移动设备菜单。</span><span class="sxs-lookup"><span data-stu-id="1ec56-143">Create a work user account, and assign a mobile device menu to the work user ID.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1ec56-144">相关设置任务</span><span class="sxs-lookup"><span data-stu-id="1ec56-144">Related setup task</span></span></td>
<td><span data-ttu-id="1ec56-145">为一个仓库场所设置一个周期盘点计划</span><span class="sxs-lookup"><span data-stu-id="1ec56-145">Set up a cycle counting plan for a warehouse location.</span></span></td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a><span data-ttu-id="1ec56-146">自动创建周期盘点工作</span><span class="sxs-lookup"><span data-stu-id="1ec56-146">Automatically create cycle counting work</span></span>
<span data-ttu-id="1ec56-147">有两种方法可以计划工作周期工作的重复创建：设置周期盘点阈值或设置周期盘点计划。</span><span class="sxs-lookup"><span data-stu-id="1ec56-147">There are two ways to schedule recurring creation of cycle counting work: set up cycle counting thresholds or set up cycle counting plans.</span></span>

-   <span data-ttu-id="1ec56-148">周期盘点阈值指示库存物料的数量或百分比限制。</span><span class="sxs-lookup"><span data-stu-id="1ec56-148">A cycle counting threshold indicates the quantity or percentage limit of inventory items.</span></span> <span data-ttu-id="1ec56-149">当达到周期盘点阈值时，会自动创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="1ec56-149">Cycle counting work is automatically created when the threshold limit is reached.</span></span>
-   <span data-ttu-id="1ec56-150">周期盘点计划通过批处理作业立即或定期创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="1ec56-150">A cycle counting plan creates cycle counting work either immediately or periodically through a batch job.</span></span> <span data-ttu-id="1ec56-151">当创建周期盘点工作时，盘点工作行包含有关要盘点的库位的信息。</span><span class="sxs-lookup"><span data-stu-id="1ec56-151">When cycle counting work is created, the counting work line includes information about the location to count.</span></span> <span data-ttu-id="1ec56-152">不会锁定与此位置相关联的现有库存，因此它可用于预留和传出处理，即使存在未结的盘点工作。</span><span class="sxs-lookup"><span data-stu-id="1ec56-152">The on-hand inventory that is associated with this location isn't blocked, and is therefore available for reservation and outbound processing, even though open counting work exists.</span></span>

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a><span data-ttu-id="1ec56-153">基于物料临界值参数创建周期盘点工作</span><span class="sxs-lookup"><span data-stu-id="1ec56-153">Create cycle counting work, based on threshold parameters for items</span></span>

<span data-ttu-id="1ec56-154">当物料数量减少至低于库位中某个特定的临界值，可以创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="1ec56-154">Cycle counting work can be created when the number of items falls below a specific threshold value in a location.</span></span> <span data-ttu-id="1ec56-155">例如，当一个库位的周期盘点临界数量是 40，而物料数量为 60。</span><span class="sxs-lookup"><span data-stu-id="1ec56-155">For example, there are 60 items in a location that has a cycle counting threshold of 40.</span></span> <span data-ttu-id="1ec56-156">在一次销售订单交易期间，有 25 个物料被从该场所领取并被放置在暂放库位。</span><span class="sxs-lookup"><span data-stu-id="1ec56-156">During a sales order transaction, 25 items are picked from the location and put in a staging location.</span></span> <span data-ttu-id="1ec56-157">因为新的物料数量 35 低于临界值，将自动为该库位创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="1ec56-157">Because the new item count, 35, is less than the threshold quantity, cycle counting work is automatically created for the location.</span></span>

### <a name="schedule-cycle-counting-work"></a><span data-ttu-id="1ec56-158">计划周期盘点工作</span><span class="sxs-lookup"><span data-stu-id="1ec56-158">Schedule cycle counting work</span></span>

<span data-ttu-id="1ec56-159">您可以计划周期盘点计划以立即或定期创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="1ec56-159">You can schedule cycle counting plans to create cycle counting work immediately or periodically.</span></span> <span data-ttu-id="1ec56-160">通过设置周期盘点计划，您可以控制为其创建周期盘点工作的工作池，为不同库位的物料创建的周期盘点的最大数，以及仓库库位再次盘点前的天数。</span><span class="sxs-lookup"><span data-stu-id="1ec56-160">By setting up cycle counting plans, you can control the work pool that cycle counting work is created for, the maximum number of cycle counts that are created for items in different locations, and the number of days before a warehouse location is counted again.</span></span> <span data-ttu-id="1ec56-161">例如，物料可在仓库中的三个库位可用；并且，周期盘点的最大数设置为 **2**。</span><span class="sxs-lookup"><span data-stu-id="1ec56-161">For example, an item is available in three locations in the warehouse, and the maximum number of cycle counts is set to **2**.</span></span> <span data-ttu-id="1ec56-162">在这种情况下，在您运行周期盘点计划时，会为存放物料的两个库位创建两个周期盘点。</span><span class="sxs-lookup"><span data-stu-id="1ec56-162">In this case, when you run the cycle counting plan, two cycle counts are created for the two locations where the item is present.</span></span> <span data-ttu-id="1ec56-163">作为另一个示例，您将周期盘点之间的天数设置为 **5**。</span><span class="sxs-lookup"><span data-stu-id="1ec56-163">As another example, you set the number of days between cycle counts to **5**.</span></span> <span data-ttu-id="1ec56-164">在这种情况下，周期盘点工作每五天创建一次。</span><span class="sxs-lookup"><span data-stu-id="1ec56-164">In this case, cycle counting work is created every five days.</span></span> <span data-ttu-id="1ec56-165">但是，如果在第三天处理周期盘点工作，则下一个周期盘点工作将在处理完最后的周期盘点之后的第五天被创建，即第八天。</span><span class="sxs-lookup"><span data-stu-id="1ec56-165">However, if cycle counting work is processed on day 3, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>

## <a name="create-cycle-counting-work-manually"></a><span data-ttu-id="1ec56-166">手动创建周期工作</span><span class="sxs-lookup"><span data-stu-id="1ec56-166">Create cycle counting work manually</span></span>
<span data-ttu-id="1ec56-167">若要手动创建周期盘点工作，则可以使用 **按物料分类的周期盘点工作**或**按位置分类的周期盘点工作**页。</span><span class="sxs-lookup"><span data-stu-id="1ec56-167">To create cycle counting work manually, you can use the **Cycle count work by item** or **Cycle count work by location** page.</span></span> <span data-ttu-id="1ec56-168">您可以指定创建的周期盘点的最大数量。</span><span class="sxs-lookup"><span data-stu-id="1ec56-168">You can specify the maximum number of cycle counts to create.</span></span> <span data-ttu-id="1ec56-169">例如，如果仓库经理指定该值为 **5**，那么将为五个场所创建周期盘点工作，即使该物料存放于 10 个不同的场所。</span><span class="sxs-lookup"><span data-stu-id="1ec56-169">For example, if the warehouse manager specifies a value of **5**, cycle counting work is created for five locations, even if the item is present in 10 locations.</span></span> <span data-ttu-id="1ec56-170">您还可以选择一个将所创建的周期盘点工作 ID 分配至的工作池 ID。</span><span class="sxs-lookup"><span data-stu-id="1ec56-170">You can also select a work pool ID to assign the cycle counting work IDs that are created to.</span></span> <span data-ttu-id="1ec56-171">当一个工作池 ID 被处理用于周期盘点，分配至此工作池的周期盘点工作 ID 被处理为一个组。</span><span class="sxs-lookup"><span data-stu-id="1ec56-171">When a work pool ID is processed for cycle counting, the cycle counting work IDs that are assigned to the work pool are processed as a group.</span></span>

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a><span data-ttu-id="1ec56-172">使用移动设备执行周期盘点</span><span class="sxs-lookup"><span data-stu-id="1ec56-172">Perform a cycle count by using a mobile device</span></span>
<span data-ttu-id="1ec56-173">使用移动设备上的 Finance and Operations 可以有几种方法处理周期盘点工作：</span><span class="sxs-lookup"><span data-stu-id="1ec56-173">There are several methods for processing cycle counting work by using Finance and Operations on a mobile device:</span></span>

-   <span data-ttu-id="1ec56-174">**用户导向** – 工作人员可以指定处于**未结**状态的周期盘点工作 ID。</span><span class="sxs-lookup"><span data-stu-id="1ec56-174">**User directed** – The worker can specify a cycle counting work ID that has a status of **Open**.</span></span>
-   <span data-ttu-id="1ec56-175">**系统导向** – Finance and Operations 分配一个周期盘点工作 ID 给工作人员。</span><span class="sxs-lookup"><span data-stu-id="1ec56-175">**System directed** – Finance and Operations assigns a cycle counting work ID to the worker.</span></span>
-   <span data-ttu-id="1ec56-176">**周期盘点分组** – 工作人员可以对特定场所、地带或工作池的特定的周期盘点工作 ID 进行分组。</span><span class="sxs-lookup"><span data-stu-id="1ec56-176">**Cycle count grouping** – The worker can group cycle counting work IDs that are specific to a particular location, zone, or work pool.</span></span>
-   <span data-ttu-id="1ec56-177">**现场周期盘点** – 工作人员可以随时盘点一个仓库库位中的物料，而无需创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="1ec56-177">**Spot cycle counting** – The worker can count items in a warehouse location at any time, without creating cycle counting work.</span></span> <span data-ttu-id="1ec56-178">若要在库位中执行现场周期盘点，工人人员输入库位 ID。</span><span class="sxs-lookup"><span data-stu-id="1ec56-178">To perform spot cycle counting in a location, the worker enters the location ID.</span></span>

<span data-ttu-id="1ec56-179">以下示例显示您如何通过使用移动设备来执行现场周期盘点。</span><span class="sxs-lookup"><span data-stu-id="1ec56-179">The following example shows how you can perform spot cycle counting by using a mobile device.</span></span> <span data-ttu-id="1ec56-180">工作人员看到的说明因设备而异，具体取决于现场周期盘点菜单项的设置。</span><span class="sxs-lookup"><span data-stu-id="1ec56-180">The instructions that the worker sees on the device vary, depending on the setup of the menu item for spot cycle counting.</span></span>

1.  <span data-ttu-id="1ec56-181">在移动设备上，选择处理现场周期盘点的菜单项。</span><span class="sxs-lookup"><span data-stu-id="1ec56-181">On the mobile device, select the menu item to process spot cycle counting work.</span></span>
2.  <span data-ttu-id="1ec56-182">登记要为其执行现场周期盘点的库位。</span><span class="sxs-lookup"><span data-stu-id="1ec56-182">Register the location to perform spot cycle counting for.</span></span>
3.  <span data-ttu-id="1ec56-183">登记并确认物料编号和已盘点的物料数量。</span><span class="sxs-lookup"><span data-stu-id="1ec56-183">Register and confirm the item number and the counted item quantity.</span></span> <span data-ttu-id="1ec56-184">**注意：**根据在**工作人员**页中设置的参数，周期盘点工作的状态在**所有工作**页中更新至**待审核**或**已关闭**。</span><span class="sxs-lookup"><span data-stu-id="1ec56-184">**Note:** The status of the cycle counting work is updated to either **Pending review** or **Closed** on the **All work** page, depending on the parameters that are set on the **Worker** page.</span></span>
4.  <span data-ttu-id="1ec56-185">可选择：为该库位中的剩余物料重复步骤 3，并确认没有更多的物料以供盘点。</span><span class="sxs-lookup"><span data-stu-id="1ec56-185">Optional: Repeat step 3 for the remaining items in the location, and confirm that no additional items are available for counting.</span></span>

## <a name="resolve-cycle-counting-differences"></a><span data-ttu-id="1ec56-186">解决周期盘点差异</span><span class="sxs-lookup"><span data-stu-id="1ec56-186">Resolve cycle counting differences</span></span>
<span data-ttu-id="1ec56-187">如果一个工作用户 ID 的**为周期盘点主管**选项设置为**否**，那么以下情况会发生周期盘点差异：</span><span class="sxs-lookup"><span data-stu-id="1ec56-187">A cycle counting difference occurs in the following scenarios if the **Is a cycle count supervisor** option is set to **No** for a work user ID:</span></span>

-   <span data-ttu-id="1ec56-188">盘点的结果值不在**工作用户**页中的**最大百分比限制**或**最大数量限制**字段中指定的偏差范围内。</span><span class="sxs-lookup"><span data-stu-id="1ec56-188">The counted value isn't within the deviation limits that are specified in the **Maximum percentage limit** or **Maximum quantity limit** fields on the **Work users** page.</span></span> <span data-ttu-id="1ec56-189">例如，某场所中现有库存数量为 50，而该工作用户的偏差限制为 10。</span><span class="sxs-lookup"><span data-stu-id="1ec56-189">For example, the on-hand inventory quantity in a location is 50, and the deviation limit for the work user is 10.</span></span> <span data-ttu-id="1ec56-190">如果该工作用户输入的值不介于 40 和 60 之间，就会发生差异。</span><span class="sxs-lookup"><span data-stu-id="1ec56-190">If the work user enters a value that isn't between 40 and 60, a difference occurs.</span></span>
-   <span data-ttu-id="1ec56-191">盘点结果值与现有库存数量不同，且没有设置偏差限制。</span><span class="sxs-lookup"><span data-stu-id="1ec56-191">The counted value differs from the on-hand inventory quantity, and no deviation limits are set.</span></span>

<span data-ttu-id="1ec56-192">您可以调整盘点结果值的差异，然后在**待审阅的周期盘点**页上接受该盘点结果值。</span><span class="sxs-lookup"><span data-stu-id="1ec56-192">You can adjust differences in the counted value and then accept the counted value on the **Cycle count pending review** page.</span></span> <span data-ttu-id="1ec56-193">您可以在**按库位显示的现有量**页中验证修改后的物料数量的盘点。</span><span class="sxs-lookup"><span data-stu-id="1ec56-193">You can verify the modified count of the item quantity on the **On hand by location** page.</span></span> <span data-ttu-id="1ec56-194">如果差异未被批准则盘点结果值将被拒绝。</span><span class="sxs-lookup"><span data-stu-id="1ec56-194">The counted value is rejected if the difference can't be approved.</span></span>

# <a name="see-also"></a><span data-ttu-id="1ec56-195">请参阅</span><span class="sxs-lookup"><span data-stu-id="1ec56-195">See also</span></span>
[<span data-ttu-id="1ec56-196">为仓库工作配置移动设备</span><span class="sxs-lookup"><span data-stu-id="1ec56-196">Configure mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)




