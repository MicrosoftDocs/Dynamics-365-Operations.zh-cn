---
title: 物料合并 - 位置利用率
description: 本主题提供有关使仓库经理可以轻松查看和筛选整个仓库中各个位置的容量利用率的功能的信息。 经理可以直接从“物料合并”页面选择位置和创建库存移动工作来合并物料，从而更好地利用仓库空间。
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3b20b41d27e5faeac7ea88940c086ae33390dc29
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216997"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="e6b32-104">物料合并 - 位置利用率</span><span class="sxs-lookup"><span data-stu-id="e6b32-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e6b32-105">本主题提供有关使仓库经理可以轻松查看和筛选整个仓库中各个位置的容量利用率的功能的信息。</span><span class="sxs-lookup"><span data-stu-id="e6b32-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="e6b32-106">经理可以直接从 **物料合并** 页面选择位置和创建库存移动工作来合并物料，从而更好地利用仓库空间。</span><span class="sxs-lookup"><span data-stu-id="e6b32-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="e6b32-107">开启功能</span><span class="sxs-lookup"><span data-stu-id="e6b32-107">Turn on the features</span></span>

<span data-ttu-id="e6b32-108">在使用本主题介绍的功能之前，必须在系统中将其打开。</span><span class="sxs-lookup"><span data-stu-id="e6b32-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="e6b32-109">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查这些功能的状态，并在需要这些功能时将其开启。</span><span class="sxs-lookup"><span data-stu-id="e6b32-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="e6b32-110">按照列出的顺序打开以下两个功能。</span><span class="sxs-lookup"><span data-stu-id="e6b32-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="e6b32-111">（这两个功能都是针对 **仓库管理** 模块。）</span><span class="sxs-lookup"><span data-stu-id="e6b32-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="e6b32-112">仓库库位状态</span><span class="sxs-lookup"><span data-stu-id="e6b32-112">Warehouse location status</span></span>
2. <span data-ttu-id="e6b32-113">物料合并库位利用率</span><span class="sxs-lookup"><span data-stu-id="e6b32-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="e6b32-114">仓库库位状态</span><span class="sxs-lookup"><span data-stu-id="e6b32-114">Warehouse location status</span></span>

<span data-ttu-id="e6b32-115">*仓库位置状态* 功能向 **位置** 页面添加四个新字段，来跟踪有关位置当前状态的其他信息：</span><span class="sxs-lookup"><span data-stu-id="e6b32-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="e6b32-116">**物料编号** – 当前位于货位中的物料。</span><span class="sxs-lookup"><span data-stu-id="e6b32-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="e6b32-117">如果位置中有多个物料，此字段将为空。</span><span class="sxs-lookup"><span data-stu-id="e6b32-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="e6b32-118">**最后一个活动的日期和时间** – 上次对货位执行的仓库事务的时间戳。</span><span class="sxs-lookup"><span data-stu-id="e6b32-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="e6b32-119">**帐龄日期** – 将货位中的库存导入仓库时的日期。</span><span class="sxs-lookup"><span data-stu-id="e6b32-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="e6b32-120">此日期基于牌照的帐龄日期计算。</span><span class="sxs-lookup"><span data-stu-id="e6b32-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="e6b32-121">虽然此日期对于牌照跟踪位置是准确的，但是对不是牌照跟踪的位置来说可能不准确。</span><span class="sxs-lookup"><span data-stu-id="e6b32-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="e6b32-122">**货位状态** – 货位的状态。</span><span class="sxs-lookup"><span data-stu-id="e6b32-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="e6b32-123">有四个值：</span><span class="sxs-lookup"><span data-stu-id="e6b32-123">Four values are available:</span></span>

    - <span data-ttu-id="e6b32-124">**未确定** – 位置模板不跟踪状态。</span><span class="sxs-lookup"><span data-stu-id="e6b32-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="e6b32-125">因此，当前状态未知。</span><span class="sxs-lookup"><span data-stu-id="e6b32-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="e6b32-126">**空** – 位置中当前无库存。</span><span class="sxs-lookup"><span data-stu-id="e6b32-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="e6b32-127">**正在领料** – 在位置上次为空后对该位置执行了出站事务。</span><span class="sxs-lookup"><span data-stu-id="e6b32-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="e6b32-128">**存储** – 自位置上次为空以来执行了入站事务。</span><span class="sxs-lookup"><span data-stu-id="e6b32-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="e6b32-129">这些字段使仓库经理可以更好地了解仓库中位置的状态。</span><span class="sxs-lookup"><span data-stu-id="e6b32-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="e6b32-130">还可以用于进行更高级的报告和筛选。</span><span class="sxs-lookup"><span data-stu-id="e6b32-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="e6b32-131">设置物料合并和位置利用</span><span class="sxs-lookup"><span data-stu-id="e6b32-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="e6b32-132">本节介绍如何准备系统以使用物料合并和位置利用。</span><span class="sxs-lookup"><span data-stu-id="e6b32-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="e6b32-133">这些过程使用标准演示数据中的示例值。</span><span class="sxs-lookup"><span data-stu-id="e6b32-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="e6b32-134">如果您打算解演练主题后面提供的示例方案，请选择 **USMF** 法人（其包含标准演示数据），并创建本节中介绍的每个记录。</span><span class="sxs-lookup"><span data-stu-id="e6b32-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="e6b32-135">如果您不打算演练示例方案，可以将此处提供的值视为要使用这些功能必须完成的设置类型的示例。</span><span class="sxs-lookup"><span data-stu-id="e6b32-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="e6b32-136">已发布产品</span><span class="sxs-lookup"><span data-stu-id="e6b32-136">Released product</span></span>

1. <span data-ttu-id="e6b32-137">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e6b32-138">在 **物料编号** 字段中，选择 *M9201*，然后打开详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="e6b32-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="e6b32-139">在“操作窗格”上的 **管理库存** 选项卡上，在 **仓库** 组中，选择 **物理维度**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="e6b32-140">在 **物理维度** 页的“操作窗格”上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="e6b32-141">新行将添加到网格中。</span><span class="sxs-lookup"><span data-stu-id="e6b32-141">A new line is added to the grid.</span></span> <span data-ttu-id="e6b32-142">**物料编号** 字段将预设。</span><span class="sxs-lookup"><span data-stu-id="e6b32-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="e6b32-143">在 **单位** 字段中，选择 *个*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="e6b32-144">行上的其余字段将自动设置。</span><span class="sxs-lookup"><span data-stu-id="e6b32-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="e6b32-145">选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="e6b32-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="e6b32-146">位置模板</span><span class="sxs-lookup"><span data-stu-id="e6b32-146">Location profile</span></span>

1. <span data-ttu-id="e6b32-147">转到 **仓库管理 \> 设置 \> 仓库 \> 货位模板**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="e6b32-148">在位置模板列表中，选择 **FLOOR-05**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="e6b32-149">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e6b32-150">在 **常规** 快速选项卡上，确保将以下两个选项都设置为 *是*：</span><span class="sxs-lookup"><span data-stu-id="e6b32-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="e6b32-151">在库位中启用物料</span><span class="sxs-lookup"><span data-stu-id="e6b32-151">Enable item in location</span></span>
    - <span data-ttu-id="e6b32-152">启用库位状态</span><span class="sxs-lookup"><span data-stu-id="e6b32-152">Enable location status</span></span>

1. <span data-ttu-id="e6b32-153">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e6b32-154">如果 **在位置中启用物料** 和 **启用位置状态** 选项已经设置为 *是*，直接跳至步骤 10 中设置 **维度** 快速选项卡的说明。</span><span class="sxs-lookup"><span data-stu-id="e6b32-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="e6b32-155">如果尚未将选项设置为 *是*，您必须在手动设置选项之后对 **仓库管理** 模块运行一致性检查。</span><span class="sxs-lookup"><span data-stu-id="e6b32-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="e6b32-156">在这种情况下，继续下一步。</span><span class="sxs-lookup"><span data-stu-id="e6b32-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="e6b32-157">要运行一致性检查，转到 **系统管理 \> 定期任务 \> 数据库 \> 一致性检查**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="e6b32-158">在 **一致性检查** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="e6b32-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e6b32-159">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="e6b32-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="e6b32-160">**检查/修复**：*检查*</span><span class="sxs-lookup"><span data-stu-id="e6b32-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="e6b32-161">**开始日期：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="e6b32-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="e6b32-162">**仓库位置状态一致性检查：** 选择此复选框。</span><span class="sxs-lookup"><span data-stu-id="e6b32-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="e6b32-163">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="e6b32-164">一致性检查完成后，您会收到一条通知。</span><span class="sxs-lookup"><span data-stu-id="e6b32-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="e6b32-165">打开[操作中心](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications)查看消息。</span><span class="sxs-lookup"><span data-stu-id="e6b32-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="e6b32-166">选择 **消息详细信息** 查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="e6b32-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="e6b32-167">如果一致性检查的消息指示“发现仓库 XX 中位置 XXXX 的位置状态信息有误”，则必须再次运行一致性检查。</span><span class="sxs-lookup"><span data-stu-id="e6b32-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="e6b32-168">这次，将 **检查/修复** 字段设置为 *修复错误*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="e6b32-169">查看消息以确保没有发现错误。</span><span class="sxs-lookup"><span data-stu-id="e6b32-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="e6b32-170">现在，您必须完成位置模板的设置。</span><span class="sxs-lookup"><span data-stu-id="e6b32-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="e6b32-171">转到 **仓库管理 \> 设置 \> 仓库 \> 位置模板**，选择位置模板 **FLOOR-05**，然后在“操作窗格”上选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e6b32-172">在 **维度** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="e6b32-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e6b32-173">**容量利用率百分比**：*100*</span><span class="sxs-lookup"><span data-stu-id="e6b32-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="e6b32-174">**用于库存位置的容量法**：*使用位置容量*</span><span class="sxs-lookup"><span data-stu-id="e6b32-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="e6b32-175">**实际位置高度**：*10*</span><span class="sxs-lookup"><span data-stu-id="e6b32-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="e6b32-176">**实际位置宽度**：*10*</span><span class="sxs-lookup"><span data-stu-id="e6b32-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="e6b32-177">**实际位置深度**：*10*</span><span class="sxs-lookup"><span data-stu-id="e6b32-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="e6b32-178">**最大重量**：*100*</span><span class="sxs-lookup"><span data-stu-id="e6b32-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="e6b32-179">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="e6b32-180">移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="e6b32-180">Mobile device menu items</span></span>

1. <span data-ttu-id="e6b32-181">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e6b32-182">在“操作窗格”上，选择 **新建** 创建用于排序的菜单项。</span><span class="sxs-lookup"><span data-stu-id="e6b32-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="e6b32-183">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="e6b32-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="e6b32-184">**菜单项名称**：*调入*</span><span class="sxs-lookup"><span data-stu-id="e6b32-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="e6b32-185">**标题**：*调入*</span><span class="sxs-lookup"><span data-stu-id="e6b32-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="e6b32-186">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="e6b32-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="e6b32-187">**使用现有工作**：*否*</span><span class="sxs-lookup"><span data-stu-id="e6b32-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="e6b32-188">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="e6b32-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e6b32-189">**工作创建流程**：*调入*</span><span class="sxs-lookup"><span data-stu-id="e6b32-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="e6b32-190">**库存调整类型**：*调入*</span><span class="sxs-lookup"><span data-stu-id="e6b32-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="e6b32-191">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="e6b32-192">移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="e6b32-192">Mobile device menu</span></span>

1. <span data-ttu-id="e6b32-193">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="e6b32-194">在菜单列表中，选择 **库存**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="e6b32-195">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e6b32-196">在 **可用菜单和菜单项** 列表中，找到并选择 **调入** 菜单项。</span><span class="sxs-lookup"><span data-stu-id="e6b32-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="e6b32-197">选择向右箭头按钮，将 **调入** 移至 **菜单结构** 列表中。</span><span class="sxs-lookup"><span data-stu-id="e6b32-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="e6b32-198">这样就将新菜单项添加到了所选菜单。</span><span class="sxs-lookup"><span data-stu-id="e6b32-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="e6b32-199">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="e6b32-200">变动类型</span><span class="sxs-lookup"><span data-stu-id="e6b32-200">Movement types</span></span>

1. <span data-ttu-id="e6b32-201">转到 **仓库管理 \> 设置 \> 库存 \> 移动类型**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="e6b32-202">在“操作窗格”中，选择 **新建**，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="e6b32-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="e6b32-203">**移动类型代码**：*CONSOLIDATE*</span><span class="sxs-lookup"><span data-stu-id="e6b32-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="e6b32-204">**描述**：*合并位置*</span><span class="sxs-lookup"><span data-stu-id="e6b32-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="e6b32-205">**工作类 ID**：*InvMov*</span><span class="sxs-lookup"><span data-stu-id="e6b32-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="e6b32-206">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="e6b32-207">示例场景</span><span class="sxs-lookup"><span data-stu-id="e6b32-207">Example scenario</span></span>

<span data-ttu-id="e6b32-208">以下方案使用移动设备上的仓库应用对仓库中的两个位置进行库存 *调入*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="e6b32-209">将库存添加到位置</span><span class="sxs-lookup"><span data-stu-id="e6b32-209">Add inventory to locations</span></span>

1. <span data-ttu-id="e6b32-210">以为仓库 *51* 设置的用户身份登录到移动设备。</span><span class="sxs-lookup"><span data-stu-id="e6b32-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="e6b32-211">转到 **库存 \> 调入**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="e6b32-212">现在，您将进入第一个位置调整。</span><span class="sxs-lookup"><span data-stu-id="e6b32-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="e6b32-213">在 **调入** 任务中，选择要进行库存调整的位置。</span><span class="sxs-lookup"><span data-stu-id="e6b32-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="e6b32-214">在 **位置** 字段中，选择 *LP-001*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="e6b32-215">确认位置。</span><span class="sxs-lookup"><span data-stu-id="e6b32-215">Confirm the location.</span></span>
1. <span data-ttu-id="e6b32-216">为将添加到位置的物料创建牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="e6b32-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="e6b32-217">在 **牌照** 字段中，输入 *LP00101*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="e6b32-218">确认牌照。</span><span class="sxs-lookup"><span data-stu-id="e6b32-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="e6b32-219">输入将添加到牌照的物料。</span><span class="sxs-lookup"><span data-stu-id="e6b32-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="e6b32-220">在 **ITEM** 字段中，输入 *M9201*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="e6b32-221">确认物料。</span><span class="sxs-lookup"><span data-stu-id="e6b32-221">Confirm the item.</span></span>
1. <span data-ttu-id="e6b32-222">输入将添加的物料的数量。</span><span class="sxs-lookup"><span data-stu-id="e6b32-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="e6b32-223">在 **数量** 字段中，输入 *10*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="e6b32-224">确认数量。</span><span class="sxs-lookup"><span data-stu-id="e6b32-224">Confirm the quantity.</span></span>

    <span data-ttu-id="e6b32-225">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="e6b32-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="e6b32-226">现在，您将进入第二个位置调整。</span><span class="sxs-lookup"><span data-stu-id="e6b32-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="e6b32-227">在 **调入** 任务中，选择要进行库存调整的位置。</span><span class="sxs-lookup"><span data-stu-id="e6b32-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="e6b32-228">在 **位置** 字段中，选择 *LP-002*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="e6b32-229">确认位置。</span><span class="sxs-lookup"><span data-stu-id="e6b32-229">Confirm the location.</span></span>
1. <span data-ttu-id="e6b32-230">为将添加到位置的物料创建牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="e6b32-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="e6b32-231">在 **牌照** 字段中，输入 *LP00201*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="e6b32-232">确认牌照。</span><span class="sxs-lookup"><span data-stu-id="e6b32-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="e6b32-233">输入将添加到牌照的物料。</span><span class="sxs-lookup"><span data-stu-id="e6b32-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="e6b32-234">在 **ITEM** 字段中，输入 *M9201*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="e6b32-235">确认物料。</span><span class="sxs-lookup"><span data-stu-id="e6b32-235">Confirm the item.</span></span>
1. <span data-ttu-id="e6b32-236">输入将添加的物料的数量。</span><span class="sxs-lookup"><span data-stu-id="e6b32-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="e6b32-237">在 **数量** 字段中，输入 *15*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="e6b32-238">确认数量。</span><span class="sxs-lookup"><span data-stu-id="e6b32-238">Confirm the quantity.</span></span>

    <span data-ttu-id="e6b32-239">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="e6b32-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="e6b32-240">选择“菜单”按钮（有时称为汉堡包或汉堡包按钮），然后选择 **取消** 退出 **调入** 任务。</span><span class="sxs-lookup"><span data-stu-id="e6b32-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="e6b32-241">合并位置</span><span class="sxs-lookup"><span data-stu-id="e6b32-241">Consolidate locations</span></span>

1. <span data-ttu-id="e6b32-242">转到 **仓库管理 \> 定期任务 \> 物料合并**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="e6b32-243">在标题中，选择要进行合并的仓库。</span><span class="sxs-lookup"><span data-stu-id="e6b32-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="e6b32-244">在 **仓库** 字段中，输入 *51*。</span><span class="sxs-lookup"><span data-stu-id="e6b32-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="e6b32-245">将显示调整了 *M9201* 物料的每个位置的记录。</span><span class="sxs-lookup"><span data-stu-id="e6b32-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="e6b32-246">**利用率百分比** 列显示每个位置的容量利用率。</span><span class="sxs-lookup"><span data-stu-id="e6b32-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="e6b32-247">要合并库存，请选择必须合并的所有位置，然后在“操作窗格”上，选择 **合并库存**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="e6b32-248">在 **合并库存** 对话框中，指定应用于创建库存移动工作的位置和移动类型。</span><span class="sxs-lookup"><span data-stu-id="e6b32-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="e6b32-249">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="e6b32-249">Set the following values:</span></span>

    - <span data-ttu-id="e6b32-250">**位置**：*LP-001*</span><span class="sxs-lookup"><span data-stu-id="e6b32-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="e6b32-251">**移动类型代码**：*CONSOLIDATE*</span><span class="sxs-lookup"><span data-stu-id="e6b32-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="e6b32-252">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-252">Select **OK**.</span></span>
1. <span data-ttu-id="e6b32-253">您将收到显示创建的移动工作的信息性消息。</span><span class="sxs-lookup"><span data-stu-id="e6b32-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="e6b32-254">记录移动工作 ID。</span><span class="sxs-lookup"><span data-stu-id="e6b32-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="e6b32-255">查看移动工作</span><span class="sxs-lookup"><span data-stu-id="e6b32-255">View movement work</span></span>

1. <span data-ttu-id="e6b32-256">转到 **仓库管理 \> 工作 \> 工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="e6b32-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="e6b32-257">查看创建的工作。</span><span class="sxs-lookup"><span data-stu-id="e6b32-257">View the work that was created.</span></span> <span data-ttu-id="e6b32-258">使用库存合并中的移动工作 ID 筛选或搜索工作网格。</span><span class="sxs-lookup"><span data-stu-id="e6b32-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="e6b32-259">在此方案中，具有库存的现有位置被用作库存合并位置。</span><span class="sxs-lookup"><span data-stu-id="e6b32-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="e6b32-260">因此，仅创建了一个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="e6b32-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="e6b32-261">系统会为必须完成的每个移动创建一个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="e6b32-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="e6b32-262">如果您指定的位置已经包含库存，将仅创建一个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="e6b32-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="e6b32-263">如果指定新位置，将创建两个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="e6b32-263">If you specify a new location, two work IDs are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]