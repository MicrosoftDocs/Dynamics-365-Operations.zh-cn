---
title: 储存群集
description: 储存群集提供了一种可以同时为多个牌照领料，然后将它们带到不同位置进行储存的方法。 它们对于零售业务非常有用，因为零售业务的牌照通常不是全部的库存托盘。
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5552959068d109bffe32b8074666bcd63b57183a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228433"
---
# <a name="putaway-clusters"></a><span data-ttu-id="c90a9-104">储存群集</span><span class="sxs-lookup"><span data-stu-id="c90a9-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c90a9-105">储存群集提供了一种可以同时为多个牌照领料，然后将它们带到不同位置进行储存的方法。</span><span class="sxs-lookup"><span data-stu-id="c90a9-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="c90a9-106">此流程通常称为 *循环取货*。</span><span class="sxs-lookup"><span data-stu-id="c90a9-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="c90a9-107">储存群集对于零售业务非常有用，因为零售业务的牌照通常不是全部的库存托盘。</span><span class="sxs-lookup"><span data-stu-id="c90a9-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="c90a9-108">开启群集储存功能</span><span class="sxs-lookup"><span data-stu-id="c90a9-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="c90a9-109">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="c90a9-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="c90a9-110">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="c90a9-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c90a9-111">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="c90a9-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c90a9-112">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="c90a9-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c90a9-113">**功能名称**：*群集储存功能*</span><span class="sxs-lookup"><span data-stu-id="c90a9-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="c90a9-114">针对示例场景设置</span><span class="sxs-lookup"><span data-stu-id="c90a9-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="c90a9-115">群集配置文件</span><span class="sxs-lookup"><span data-stu-id="c90a9-115">Cluster profiles</span></span>

<span data-ttu-id="c90a9-116">储存群集配置文件根据收货时分配给物料的位置来确定物料的去向。</span><span class="sxs-lookup"><span data-stu-id="c90a9-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="c90a9-117">如果需要不同的群集，则应创建不同的储存群集，每个移动设备菜单项创建一个。</span><span class="sxs-lookup"><span data-stu-id="c90a9-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="c90a9-118">转到 **仓库管理 \> 设置 \> 移动设备 \> 群集配置文件**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="c90a9-119">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c90a9-120">在 **标头** 视图中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="c90a9-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="c90a9-121">**储存群集配置文件 ID**：*Cluster putaway*</span><span class="sxs-lookup"><span data-stu-id="c90a9-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c90a9-122">**储存群集配置文件 ID 名称**：*群集储存*</span><span class="sxs-lookup"><span data-stu-id="c90a9-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c90a9-123">**群集类型**：*储存*</span><span class="sxs-lookup"><span data-stu-id="c90a9-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="c90a9-124">**序列号：** 接受默认值。</span><span class="sxs-lookup"><span data-stu-id="c90a9-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="c90a9-125">选择 **保存** 让 **常规** 快速选项卡上的必填字段显示。</span><span class="sxs-lookup"><span data-stu-id="c90a9-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="c90a9-126">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="c90a9-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c90a9-127">**群集分配时间**：*收货时*</span><span class="sxs-lookup"><span data-stu-id="c90a9-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="c90a9-128">此字段定义是否应在收到库存时立即分配储存群集，还是应在以后分类。</span><span class="sxs-lookup"><span data-stu-id="c90a9-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="c90a9-129">**群集分配规则**：*手动*</span><span class="sxs-lookup"><span data-stu-id="c90a9-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="c90a9-130">此字段定义应由系统自动确定群集分配还是由用户手动进行。</span><span class="sxs-lookup"><span data-stu-id="c90a9-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="c90a9-131">**指令代码：** 将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="c90a9-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="c90a9-132">**储存群集查找**：*收货*</span><span class="sxs-lookup"><span data-stu-id="c90a9-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="c90a9-133">提供以下值：</span><span class="sxs-lookup"><span data-stu-id="c90a9-133">The following values are available:</span></span>

        - <span data-ttu-id="c90a9-134">**收货** – 收货期间立即找到位置。</span><span class="sxs-lookup"><span data-stu-id="c90a9-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="c90a9-135">**群集关闭** – 在群集关闭时找到位置。</span><span class="sxs-lookup"><span data-stu-id="c90a9-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="c90a9-136">**用户导向** – 从群集为牌照领料以进行储存时找到位置。</span><span class="sxs-lookup"><span data-stu-id="c90a9-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="c90a9-137">在这种情况下，不在创建储存工作时指定位置。</span><span class="sxs-lookup"><span data-stu-id="c90a9-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="c90a9-138">在储存过程中，用户必须扫描牌照或工作 ID 来启动放置步骤。</span><span class="sxs-lookup"><span data-stu-id="c90a9-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="c90a9-139">然后，系统将再次查找放置位置，并告诉用户放置所领取数量的位置。</span><span class="sxs-lookup"><span data-stu-id="c90a9-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="c90a9-140">**按用户分配储存群集**：*否*</span><span class="sxs-lookup"><span data-stu-id="c90a9-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="c90a9-141">此字段定义在自动分配群集时每个群集对每个用户是否应是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c90a9-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="c90a9-142">它仅在 **群集分配规则** 字段设置为 *自动* 时显示。</span><span class="sxs-lookup"><span data-stu-id="c90a9-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="c90a9-143">**单位限制：** 将此字段留空。</span><span class="sxs-lookup"><span data-stu-id="c90a9-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="c90a9-144">此字段定义要让配置文件有效必须接收的单位。</span><span class="sxs-lookup"><span data-stu-id="c90a9-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="c90a9-145">如果为空，所有单位有效。</span><span class="sxs-lookup"><span data-stu-id="c90a9-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="c90a9-146">**工作单位中断**：*单个*</span><span class="sxs-lookup"><span data-stu-id="c90a9-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="c90a9-147">此字段定义群集关闭时是否应将所有库存合并（使用库存 ID 和牌照）到一个牌照，以及是应将其作为单个牌照储存还是应在接收的牌照上单独储存。</span><span class="sxs-lookup"><span data-stu-id="c90a9-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="c90a9-148">此字段在 **储存群集查找** 字段设置为 *收货* 时不显示。</span><span class="sxs-lookup"><span data-stu-id="c90a9-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="c90a9-149">**群集作为父牌照保留**：*否*</span><span class="sxs-lookup"><span data-stu-id="c90a9-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="c90a9-150">如果此选项设置为 *是*，完成放置步骤后，群集 ID 将成为父牌照，群集 ID 上的所有物料都将链接到该父牌照。</span><span class="sxs-lookup"><span data-stu-id="c90a9-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="c90a9-151">在 **群集排序** 快速选项卡上，您可以定义储存排序条件。</span><span class="sxs-lookup"><span data-stu-id="c90a9-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="c90a9-152">在工具栏上选择 **新建** 添加一行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="c90a9-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="c90a9-153">**序列号：** 接受默认值。</span><span class="sxs-lookup"><span data-stu-id="c90a9-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="c90a9-154">**字段名称**：*WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="c90a9-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="c90a9-155">此字段定义此行应用作排序条件的字段。</span><span class="sxs-lookup"><span data-stu-id="c90a9-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="c90a9-156">**排序**：*升序*</span><span class="sxs-lookup"><span data-stu-id="c90a9-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="c90a9-157">此字段定义排序应按升序还是降序进行。</span><span class="sxs-lookup"><span data-stu-id="c90a9-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="c90a9-158">在 **群集工作模板** 快速选项卡上，在工具栏上选择 **新建** 添加一行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="c90a9-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="c90a9-159">**工作订单类型**：*采购订单*</span><span class="sxs-lookup"><span data-stu-id="c90a9-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="c90a9-160">**工作模板**：*61 PO Direct*</span><span class="sxs-lookup"><span data-stu-id="c90a9-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="c90a9-161">在操作窗格上，选择 **保存**，然后选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="c90a9-162">在 **群集储存** 对话框中的 **范围** 选项卡中，选择 **添加** 向查询再添加一行。</span><span class="sxs-lookup"><span data-stu-id="c90a9-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="c90a9-163">然后更新查询行，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="c90a9-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="c90a9-164">表</span><span class="sxs-lookup"><span data-stu-id="c90a9-164">Table</span></span> | <span data-ttu-id="c90a9-165">派生表</span><span class="sxs-lookup"><span data-stu-id="c90a9-165">Derived table</span></span> | <span data-ttu-id="c90a9-166">字段</span><span class="sxs-lookup"><span data-stu-id="c90a9-166">Field</span></span> | <span data-ttu-id="c90a9-167">条件</span><span class="sxs-lookup"><span data-stu-id="c90a9-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="c90a9-168">工作</span><span class="sxs-lookup"><span data-stu-id="c90a9-168">Work</span></span> | <span data-ttu-id="c90a9-169">工作</span><span class="sxs-lookup"><span data-stu-id="c90a9-169">Work</span></span> | <span data-ttu-id="c90a9-170">仓库</span><span class="sxs-lookup"><span data-stu-id="c90a9-170">Warehouse</span></span> | <span data-ttu-id="c90a9-171">*61*</span><span class="sxs-lookup"><span data-stu-id="c90a9-171">*61*</span></span> |
    | <span data-ttu-id="c90a9-172">工作</span><span class="sxs-lookup"><span data-stu-id="c90a9-172">Work</span></span> | <span data-ttu-id="c90a9-173">工作</span><span class="sxs-lookup"><span data-stu-id="c90a9-173">Work</span></span> | <span data-ttu-id="c90a9-174">工作 ID</span><span class="sxs-lookup"><span data-stu-id="c90a9-174">Work ID</span></span> | <span data-ttu-id="c90a9-175">保持此字段为空。</span><span class="sxs-lookup"><span data-stu-id="c90a9-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="c90a9-176">选择 **确定** 保存查询并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="c90a9-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="c90a9-177">在操作窗格上，选择 **保存**，然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="c90a9-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c90a9-178">当 **生成群集 ID** 设置为 *是* 时，群集配置文件中灰显的字段不可用，不会在使用此功能时考虑。</span><span class="sxs-lookup"><span data-stu-id="c90a9-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="c90a9-179">移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="c90a9-179">Mobile device menu items</span></span>

<span data-ttu-id="c90a9-180">此功能提供了两个新的移动设备菜单项。</span><span class="sxs-lookup"><span data-stu-id="c90a9-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="c90a9-181">**群集接收和分类** 菜单项用于在收货后将收到的库存分类到储存群集。</span><span class="sxs-lookup"><span data-stu-id="c90a9-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="c90a9-182">**群集储存** 菜单项用于在分配群集后对其进行储存。</span><span class="sxs-lookup"><span data-stu-id="c90a9-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="c90a9-183">群集接收和分类</span><span class="sxs-lookup"><span data-stu-id="c90a9-183">Receive and sort cluster</span></span>

<span data-ttu-id="c90a9-184">创建一个新的移动设备菜单项，用于接收库存并将其分类到群集。</span><span class="sxs-lookup"><span data-stu-id="c90a9-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="c90a9-185">此菜单项将在接收库存后创建入站工作，这指示接收菜单项将用于储存群集。</span><span class="sxs-lookup"><span data-stu-id="c90a9-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="c90a9-186">**群集接收和分类** 菜单项可以与以下接收菜单项一起使用：</span><span class="sxs-lookup"><span data-stu-id="c90a9-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="c90a9-187">采购订单行接收</span><span class="sxs-lookup"><span data-stu-id="c90a9-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="c90a9-188">采购订单物料接收</span><span class="sxs-lookup"><span data-stu-id="c90a9-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="c90a9-189">加载物料接收</span><span class="sxs-lookup"><span data-stu-id="c90a9-189">Load item receiving</span></span>

1. <span data-ttu-id="c90a9-190">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c90a9-191">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c90a9-192">在 **标头** 视图中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="c90a9-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="c90a9-193">**菜单项名称**：*群集接收和分类*</span><span class="sxs-lookup"><span data-stu-id="c90a9-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="c90a9-194">**标题**：*群集接收和分类*</span><span class="sxs-lookup"><span data-stu-id="c90a9-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="c90a9-195">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="c90a9-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c90a9-196">**使用现有工作**：*否*</span><span class="sxs-lookup"><span data-stu-id="c90a9-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="c90a9-197">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="c90a9-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="c90a9-198">**工作创建流程**：*采购订单物料接收*</span><span class="sxs-lookup"><span data-stu-id="c90a9-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="c90a9-199">\**生成牌照：\*\*\*是*</span><span class="sxs-lookup"><span data-stu-id="c90a9-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="c90a9-200">**分配储存群集**：*是*</span><span class="sxs-lookup"><span data-stu-id="c90a9-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="c90a9-201">**分配储存群集** 选项仅对用于接收的一步式 *工作创建流程* 活动可用。</span><span class="sxs-lookup"><span data-stu-id="c90a9-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="c90a9-202">其余字段接受默认值。</span><span class="sxs-lookup"><span data-stu-id="c90a9-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="c90a9-203">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="c90a9-204">群集储存</span><span class="sxs-lookup"><span data-stu-id="c90a9-204">Cluster putaway</span></span>

<span data-ttu-id="c90a9-205">创建一个新的移动设备菜单项，用于在分配群集后对其进行储存。</span><span class="sxs-lookup"><span data-stu-id="c90a9-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="c90a9-206">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c90a9-207">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c90a9-208">在 **标头** 视图中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="c90a9-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="c90a9-209">**菜单项名称**：*群集储存*</span><span class="sxs-lookup"><span data-stu-id="c90a9-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c90a9-210">**标题**：*群集储存*</span><span class="sxs-lookup"><span data-stu-id="c90a9-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="c90a9-211">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="c90a9-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c90a9-212">**使用现有工作**：*是*</span><span class="sxs-lookup"><span data-stu-id="c90a9-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="c90a9-213">在 **常规** 快速选项卡上，将 **导向方式** 字段设置为 *群集储存*。</span><span class="sxs-lookup"><span data-stu-id="c90a9-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="c90a9-214">其余字段接受默认值。</span><span class="sxs-lookup"><span data-stu-id="c90a9-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="c90a9-215">在 **工作类** 快速选项卡上，为此移动设备菜单项设置有效的工作类：</span><span class="sxs-lookup"><span data-stu-id="c90a9-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="c90a9-216">**工作类 ID**：*Purchase*</span><span class="sxs-lookup"><span data-stu-id="c90a9-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="c90a9-217">**工作订单类型**：*采购订单*</span><span class="sxs-lookup"><span data-stu-id="c90a9-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="c90a9-218">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="c90a9-219">移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="c90a9-219">Mobile device menu</span></span>

<span data-ttu-id="c90a9-220">将刚才创建的菜单项添加到移动应用的入站菜单中。</span><span class="sxs-lookup"><span data-stu-id="c90a9-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="c90a9-221">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="c90a9-222">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c90a9-223">在菜单列表中，选择 **入站**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="c90a9-224">在 **可用菜单和菜单项** 列表中，找到并选择 **群集接收和分类**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="c90a9-225">选择向右箭头按钮将所选的菜单项移到 **菜单结构** 列表。</span><span class="sxs-lookup"><span data-stu-id="c90a9-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="c90a9-226">使用向上箭头或向下箭头按钮将菜单项移到菜单中的所需位置。</span><span class="sxs-lookup"><span data-stu-id="c90a9-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="c90a9-227">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c90a9-228">重复执行步骤 4 到 7，添加其余菜单项：</span><span class="sxs-lookup"><span data-stu-id="c90a9-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="c90a9-229">分配群集</span><span class="sxs-lookup"><span data-stu-id="c90a9-229">Assign cluster</span></span>
    - <span data-ttu-id="c90a9-230">群集储存</span><span class="sxs-lookup"><span data-stu-id="c90a9-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="c90a9-231">示例场景</span><span class="sxs-lookup"><span data-stu-id="c90a9-231">Example scenario</span></span>

<span data-ttu-id="c90a9-232">此场景模拟储存群集处理。</span><span class="sxs-lookup"><span data-stu-id="c90a9-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="c90a9-233">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="c90a9-233">Create a purchase order</span></span>

1. <span data-ttu-id="c90a9-234">转到 **应付帐款 \> 采购订单 \> 所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="c90a9-235">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="c90a9-236">在 **创建采购订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="c90a9-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="c90a9-237">**供应商帐户**：*1001*</span><span class="sxs-lookup"><span data-stu-id="c90a9-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="c90a9-238">**仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="c90a9-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="c90a9-239">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-239">Select **OK**.</span></span>

    <span data-ttu-id="c90a9-240">**所有采购订单** 页将出现。</span><span class="sxs-lookup"><span data-stu-id="c90a9-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="c90a9-241">在 **所有采购订单** 页上的 **采购订单行** 快速选项卡上，使用 **添加行** 按钮添加以下行：</span><span class="sxs-lookup"><span data-stu-id="c90a9-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="c90a9-242">采购订单行 1：</span><span class="sxs-lookup"><span data-stu-id="c90a9-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="c90a9-243">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="c90a9-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="c90a9-244">**数量：** *10*</span><span class="sxs-lookup"><span data-stu-id="c90a9-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="c90a9-245">采购订单行 2：</span><span class="sxs-lookup"><span data-stu-id="c90a9-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="c90a9-246">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="c90a9-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="c90a9-247">**数量：** *20*</span><span class="sxs-lookup"><span data-stu-id="c90a9-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="c90a9-248">采购订单行 3：</span><span class="sxs-lookup"><span data-stu-id="c90a9-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="c90a9-249">\**物料编号：\*\*\*M9215*</span><span class="sxs-lookup"><span data-stu-id="c90a9-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="c90a9-250">**数量：** *30*</span><span class="sxs-lookup"><span data-stu-id="c90a9-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="c90a9-251">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="c90a9-252">记下采购订单编号。</span><span class="sxs-lookup"><span data-stu-id="c90a9-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="c90a9-253">从移动设备接收库存和储存</span><span class="sxs-lookup"><span data-stu-id="c90a9-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="c90a9-254">接收库存并分类到群集</span><span class="sxs-lookup"><span data-stu-id="c90a9-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="c90a9-255">以已经为仓库 *61* 设置的用户的身份登录仓库应用。</span><span class="sxs-lookup"><span data-stu-id="c90a9-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="c90a9-256">在主菜单上，选择 **入站**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="c90a9-257">在 **入站** 菜单上，选择 **群集接收和分类**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="c90a9-258">在 **采购订单编号** 字段中，输入采购订单编号。</span><span class="sxs-lookup"><span data-stu-id="c90a9-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="c90a9-259">选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="c90a9-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="c90a9-260">选择 **物料** 字段，输入物料编号 *A0001*，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="c90a9-261">选择 **数量** 字段，使用数字键盘输入 *10*，然后选择复选标记按钮。</span><span class="sxs-lookup"><span data-stu-id="c90a9-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="c90a9-262">在 **数量** 任务页，选择 **确定**（复选标记按钮）确认您输入的数量。</span><span class="sxs-lookup"><span data-stu-id="c90a9-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="c90a9-263">在 **物料** 任务页，选择 **确定** 确认物料 *A0001* 已输入。</span><span class="sxs-lookup"><span data-stu-id="c90a9-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="c90a9-264">选择 **群集 ID** 字段，输入一个值来为要创建的群集分配 ID。</span><span class="sxs-lookup"><span data-stu-id="c90a9-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="c90a9-265">您在此处输入的 ID 将在接收采购订单上的其余两个物料时使用。</span><span class="sxs-lookup"><span data-stu-id="c90a9-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="c90a9-266">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-266">Select **OK**.</span></span>

    <span data-ttu-id="c90a9-267">**采购订单编号** 任务页将出现，显示“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="c90a9-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="c90a9-268">物料 *A0001* 现在已经被接收到 *RECV* 位置，并分配给您在步骤 10 中输入的群集 ID。</span><span class="sxs-lookup"><span data-stu-id="c90a9-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="c90a9-269">重复步骤 4 到 11 接收采购订单中的其余两个物料，然后将它们分配给群集 ID：</span><span class="sxs-lookup"><span data-stu-id="c90a9-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="c90a9-270">物料 *A0002* 的数量为 *20*</span><span class="sxs-lookup"><span data-stu-id="c90a9-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="c90a9-271">物料 *M9215* 的数量为 *30*</span><span class="sxs-lookup"><span data-stu-id="c90a9-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="c90a9-272">关闭群集</span><span class="sxs-lookup"><span data-stu-id="c90a9-272">Close the cluster</span></span>

<span data-ttu-id="c90a9-273">必须先关闭群集，然后才能储存群集中的物料。</span><span class="sxs-lookup"><span data-stu-id="c90a9-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="c90a9-274">在 Supply Chain Management 中，转到 **仓库管理 \> 工作 \> 出站 \> 工作群集**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="c90a9-275">在 **工作群集** 页上，在 **工作群集** 部分中，搜索您之前输入的群集 ID 的 **群集 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="c90a9-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="c90a9-276">如果群集未显示，说明它可能已经关闭。</span><span class="sxs-lookup"><span data-stu-id="c90a9-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="c90a9-277">要确定群集是否关闭，选择 **显示已关闭工作** 复选框，然后搜索您之前输入的群集 ID。</span><span class="sxs-lookup"><span data-stu-id="c90a9-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="c90a9-278">然后按照以下步骤之一操作：</span><span class="sxs-lookup"><span data-stu-id="c90a9-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="c90a9-279">如果群集已关闭，跳过此过程的其余步骤，进入下一个过程[储存群集](#put-the-cluster-away)。</span><span class="sxs-lookup"><span data-stu-id="c90a9-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="c90a9-280">如果群集未关闭，请按照此过程的其余步骤手动关闭群集。</span><span class="sxs-lookup"><span data-stu-id="c90a9-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="c90a9-281">然后进入下一个过程。</span><span class="sxs-lookup"><span data-stu-id="c90a9-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="c90a9-282">在 **工作群集** 部分，选择您之前输入的群集 ID。</span><span class="sxs-lookup"><span data-stu-id="c90a9-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="c90a9-283">在操作窗格上，选择 **关闭群集**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="c90a9-284">群集关闭后，不会再显示在 **工作群集** 部分（除非选中 **显示已关闭工作** 复选框）。</span><span class="sxs-lookup"><span data-stu-id="c90a9-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="c90a9-285">储存群集</span><span class="sxs-lookup"><span data-stu-id="c90a9-285">Put the cluster away</span></span>

1. <span data-ttu-id="c90a9-286">以已经为仓库 *61* 设置的用户的身份登录仓库应用。</span><span class="sxs-lookup"><span data-stu-id="c90a9-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="c90a9-287">在主菜单上，选择 **入站**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="c90a9-288">在 **入站** 菜单上，选择 **群集储存**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="c90a9-289">选择 **群集 ID**，输入您之前为已关闭群集输入的群集 ID。</span><span class="sxs-lookup"><span data-stu-id="c90a9-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="c90a9-290">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-290">Select **OK**.</span></span>

    <span data-ttu-id="c90a9-291">**群集储存: 领料** 页将出现。</span><span class="sxs-lookup"><span data-stu-id="c90a9-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="c90a9-292">此页面显示群集 ID、领料位置、物料（值 *多个* 将显示），以及必须领料的群集中的总数量。</span><span class="sxs-lookup"><span data-stu-id="c90a9-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="c90a9-293">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="c90a9-293">Select **OK**.</span></span>

    <span data-ttu-id="c90a9-294">**群集储存: 放置** 页将出现。</span><span class="sxs-lookup"><span data-stu-id="c90a9-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="c90a9-295">**放置** 指令标识群集 ID、放置位置、物料、总数量，以及群集上已接收的物料的牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="c90a9-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="c90a9-296">您可以使用标准选项来替代或跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="c90a9-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="c90a9-297">![“群集储存: 放置”页](media/Cluster_putaway-Put.png "“群集储存: 放置”页")</span><span class="sxs-lookup"><span data-stu-id="c90a9-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="c90a9-298">选择 **确定** 确认群集的储存。</span><span class="sxs-lookup"><span data-stu-id="c90a9-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="c90a9-299">“群集已完成”消息将显示。</span><span class="sxs-lookup"><span data-stu-id="c90a9-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="c90a9-300">说明和提示</span><span class="sxs-lookup"><span data-stu-id="c90a9-300">Notes and tips</span></span>

<span data-ttu-id="c90a9-301">对于群集 ID 成为嵌套托盘的父牌照的情况，扫描群集 ID 时会自动给出放置位置。</span><span class="sxs-lookup"><span data-stu-id="c90a9-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="c90a9-302">即使将牌照生成设置为手动，也无需再扫描牌照。</span><span class="sxs-lookup"><span data-stu-id="c90a9-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]