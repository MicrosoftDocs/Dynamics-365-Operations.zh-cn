---
title: 出站排序
description: 文主题提供有关出站分类的信息。 此功能使处理小集装箱更轻松，并帮助仓库工作人员更好地计划和组织卡车内的托盘容量。
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e72249e26fb8f291f804cf5f2e4ce98bf88cd5bf
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596204"
---
# <a name="outbound-sorting"></a><span data-ttu-id="b586f-104">出站排序</span><span class="sxs-lookup"><span data-stu-id="b586f-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b586f-105">此功能使处理小集装箱更轻松，并帮助仓库工作人员更好地计划和组织卡车内的托盘容量。</span><span class="sxs-lookup"><span data-stu-id="b586f-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="b586f-106">使用出站排序时，可以在已装箱集装箱进入装箱工作站后再分类到正确的托盘。</span><span class="sxs-lookup"><span data-stu-id="b586f-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="b586f-107">您还可以建立装箱层次结构。</span><span class="sxs-lookup"><span data-stu-id="b586f-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="b586f-108">通过此功能，您可以从通过装箱功能装箱的集装箱建立托盘。</span><span class="sxs-lookup"><span data-stu-id="b586f-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="b586f-109">集装箱不会像原始装箱流那样被发送到最终装运位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="b586f-110">工作人员可以封闭集装箱，然后将其移动到分类类型位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="b586f-111">然后，他们可以将集装箱分类到各个位置，每个位置都有一个牌照 (LP)。</span><span class="sxs-lookup"><span data-stu-id="b586f-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="b586f-112">在对集装箱进行分类之后，可以根据位置指令或您自己的要求创建工作来将整个牌照发送到最终装运台或暂存位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="b586f-113">而且，关闭分类位置的操作可以立即将库存移至最终装运位置，然后将其领取到订单。</span><span class="sxs-lookup"><span data-stu-id="b586f-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="b586f-114">打开出站分类功能</span><span class="sxs-lookup"><span data-stu-id="b586f-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="b586f-115">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="b586f-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="b586f-116">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="b586f-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b586f-117">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="b586f-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b586f-118">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="b586f-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b586f-119">**功能名称**：*出站分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="b586f-120">设置</span><span class="sxs-lookup"><span data-stu-id="b586f-120">Setup</span></span>

<span data-ttu-id="b586f-121">对于此方案，您必须使用标准 **USMF** 演示数据和仓库 *62*。</span><span class="sxs-lookup"><span data-stu-id="b586f-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="b586f-122">您还必须完成以下小节中介绍的设置。</span><span class="sxs-lookup"><span data-stu-id="b586f-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="b586f-123">设置波次模板</span><span class="sxs-lookup"><span data-stu-id="b586f-123">Set up a wave template</span></span>

<span data-ttu-id="b586f-124">当将某一行发放到仓库时，此设置会自动处理波次并创建工作。</span><span class="sxs-lookup"><span data-stu-id="b586f-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="b586f-125">转到**仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="b586f-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b586f-126">在模板列表中，选择**仓库 62**。</span><span class="sxs-lookup"><span data-stu-id="b586f-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="b586f-127">在**常规**快速选项卡上，确保将**在发放到仓库时处理波次**选项设置为*是*。</span><span class="sxs-lookup"><span data-stu-id="b586f-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="b586f-128">设置工作人员</span><span class="sxs-lookup"><span data-stu-id="b586f-128">Set up a worker</span></span>

<span data-ttu-id="b586f-129">装箱工作站被视为一个位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-129">The packing station is considered a location.</span></span> <span data-ttu-id="b586f-130">在装箱工作站登录的仓库工作人员只能看到和处理在该特定装箱位置计划的装运和集装箱。</span><span class="sxs-lookup"><span data-stu-id="b586f-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="b586f-131">登录到 Microsoft Dynamics 365 的用户必须在“仓库管理”中设置为工作人员。</span><span class="sxs-lookup"><span data-stu-id="b586f-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="b586f-132">如果用户的名称未出现在工作用户列表中，请使用以下过程添加。</span><span class="sxs-lookup"><span data-stu-id="b586f-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="b586f-133">这些步骤假定用户已经存在于系统中，并且已在**人力资源**模块中关联为员工或工作人员。</span><span class="sxs-lookup"><span data-stu-id="b586f-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="b586f-134">转到**仓库管理 \> 设置 \> 工作人员**。</span><span class="sxs-lookup"><span data-stu-id="b586f-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="b586f-135">选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b586f-135">Select **New**.</span></span>
1. <span data-ttu-id="b586f-136">在**工作人员**字段中，在员工列表中选择目标用户。</span><span class="sxs-lookup"><span data-stu-id="b586f-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="b586f-137">选择**选择**。</span><span class="sxs-lookup"><span data-stu-id="b586f-137">Select **Select**.</span></span>
1. <span data-ttu-id="b586f-138">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b586f-139">在**用户**快速选项卡上，选择**新建**创建一个移动设备帐户，并为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="b586f-140">**用户 ID：** 输入一个唯一 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="b586f-141">**用户名：** 为 ID 输入名称。</span><span class="sxs-lookup"><span data-stu-id="b586f-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="b586f-142">**默认仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="b586f-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="b586f-143">**菜单名称**：*主*</span><span class="sxs-lookup"><span data-stu-id="b586f-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="b586f-144">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="b586f-145">**设置密码**对话框将出现，您可以在其中创建一个简单的密码，用户可用来登录移动应用。</span><span class="sxs-lookup"><span data-stu-id="b586f-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="b586f-146">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-146">Set the following values:</span></span>

    - <span data-ttu-id="b586f-147">**密码：** 输入一个简单的密码。</span><span class="sxs-lookup"><span data-stu-id="b586f-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="b586f-148">**确认密码：** 再次输入相同密码。</span><span class="sxs-lookup"><span data-stu-id="b586f-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="b586f-149">选择**设置密码**。</span><span class="sxs-lookup"><span data-stu-id="b586f-149">Select **Set password**.</span></span>

    <span data-ttu-id="b586f-150">“操作中心”的通知将通知您已为您创建的用户设置了密码。</span><span class="sxs-lookup"><span data-stu-id="b586f-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="b586f-151">创建位置类型</span><span class="sxs-lookup"><span data-stu-id="b586f-151">Create a location type</span></span>

1. <span data-ttu-id="b586f-152">转到**仓库管理 \> 设置 \> 仓库 \> 位置类型**。</span><span class="sxs-lookup"><span data-stu-id="b586f-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="b586f-153">在操作窗格上，选择**新建**创建位置类型，并为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="b586f-154">**位置类型**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="b586f-155">**描述**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="b586f-156">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="b586f-157">设置仓库管理参数</span><span class="sxs-lookup"><span data-stu-id="b586f-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="b586f-158">转到**仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="b586f-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="b586f-159">在**常规**选项卡上的**位置类型**快速选项卡上，将**分类位置类型**字段设置为*分类*。</span><span class="sxs-lookup"><span data-stu-id="b586f-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="b586f-160">在操作窗格上，选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="b586f-161">设置位置模板</span><span class="sxs-lookup"><span data-stu-id="b586f-161">Set up a location profile</span></span>

1. <span data-ttu-id="b586f-162">转到**仓库管理 \> 设置 \> 仓库 \> 货位模板**。</span><span class="sxs-lookup"><span data-stu-id="b586f-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="b586f-163">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b586f-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b586f-164">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="b586f-165">**位置模板 ID**：*Sorting*</span><span class="sxs-lookup"><span data-stu-id="b586f-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="b586f-166">**名称**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="b586f-167">在**常规**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b586f-168">**位置格式**：*ASRB*（通道-货架-货位-储料箱）</span><span class="sxs-lookup"><span data-stu-id="b586f-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="b586f-169">**位置类型**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="b586f-170">**使用牌照跟踪**：*是*</span><span class="sxs-lookup"><span data-stu-id="b586f-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="b586f-171">**允许混合物料**：*是*（当您将此选项设置为*是*时，**允许混合的库存批处理**选项将自动设置为*是*，并且不能单独更改。）</span><span class="sxs-lookup"><span data-stu-id="b586f-171">**Allow mixed items:** *Yes* (When you set this option to *Yes*, the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="b586f-172">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="b586f-173">设置位置</span><span class="sxs-lookup"><span data-stu-id="b586f-173">Set up a location</span></span>

1. <span data-ttu-id="b586f-174">转到**仓库管理 \> 设置 \> 仓库 \> 货位**。</span><span class="sxs-lookup"><span data-stu-id="b586f-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="b586f-175">在标题中，清除**生成位置校验位**复选框。</span><span class="sxs-lookup"><span data-stu-id="b586f-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="b586f-176">在操作窗格上，选择**新建**创建位置，并为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="b586f-177">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="b586f-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b586f-178">**货位**：*SORT*</span><span class="sxs-lookup"><span data-stu-id="b586f-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="b586f-179">**位置模板 ID**：*SORTING*</span><span class="sxs-lookup"><span data-stu-id="b586f-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="b586f-180">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="b586f-181">设置出站分类模板</span><span class="sxs-lookup"><span data-stu-id="b586f-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="b586f-182">出站分类模板确定是否在分类位置之外创建工作，以及是手动还是自动进行分类。</span><span class="sxs-lookup"><span data-stu-id="b586f-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="b586f-183">对于此方案，您将创建出站分类模板来在装箱工作站之后建立托盘。</span><span class="sxs-lookup"><span data-stu-id="b586f-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="b586f-184">转到**仓库管理 \> 设置 \> 装箱 \> 出站分类模板**。</span><span class="sxs-lookup"><span data-stu-id="b586f-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="b586f-185">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b586f-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b586f-186">在新模板的标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="b586f-187">**出站分类模板 ID**：*AutoWork*</span><span class="sxs-lookup"><span data-stu-id="b586f-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="b586f-188">**描述**：*自动工作创建*</span><span class="sxs-lookup"><span data-stu-id="b586f-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="b586f-189">**出站分类模板类型**：*集装箱*</span><span class="sxs-lookup"><span data-stu-id="b586f-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="b586f-190">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="b586f-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b586f-191">**货位**：*SORT*</span><span class="sxs-lookup"><span data-stu-id="b586f-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="b586f-192">在**常规**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b586f-193">**分类验证**：*位置扫描*</span><span class="sxs-lookup"><span data-stu-id="b586f-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="b586f-194">**在位置关闭时创建工作**：*是*</span><span class="sxs-lookup"><span data-stu-id="b586f-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="b586f-195">如果此选项设置为*是*，在位置关闭时，将创建工作以将库存移至最终装运位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-195">If this option is set to *Yes*, when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="b586f-196">如果设置为*否*，在位置关闭时，库存将被立即领取到订单。</span><span class="sxs-lookup"><span data-stu-id="b586f-196">If it's set to *No*, inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="b586f-197">**位置分配**：*自动*</span><span class="sxs-lookup"><span data-stu-id="b586f-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="b586f-198">如果此字段设置为*手动*，用户必须始终指出库存应分类到的位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-198">If this field is set to *Manual*, the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="b586f-199">如果设置为*自动*，系统会根据分类模板中断自动将库存引导至某个位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-199">If it's set to *Automatic*, the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="b586f-200">选择**保存**让操作窗格上的**编辑查询**按钮可用。</span><span class="sxs-lookup"><span data-stu-id="b586f-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="b586f-201">在操作窗格上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="b586f-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="b586f-202">在查询编辑器中的**分类**选项卡上，添加具有以下值的行：</span><span class="sxs-lookup"><span data-stu-id="b586f-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="b586f-203">**表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="b586f-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="b586f-204">**派生表**：*装运*</span><span class="sxs-lookup"><span data-stu-id="b586f-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="b586f-205">**字段**：*承运人服务*</span><span class="sxs-lookup"><span data-stu-id="b586f-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="b586f-206">选择此值之时，可能会收到以下消息：“承运人服务字段不是索引字段。</span><span class="sxs-lookup"><span data-stu-id="b586f-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="b586f-207">是否要为其添加排序？”</span><span class="sxs-lookup"><span data-stu-id="b586f-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="b586f-208">选择**是**。</span><span class="sxs-lookup"><span data-stu-id="b586f-208">Select **Yes**.</span></span>

    - <span data-ttu-id="b586f-209">**搜索方向**：*升序*</span><span class="sxs-lookup"><span data-stu-id="b586f-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="b586f-210">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-210">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-211">您可能会收到以下消息：“分组将重置，是否继续？”</span><span class="sxs-lookup"><span data-stu-id="b586f-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="b586f-212">选择**是**。</span><span class="sxs-lookup"><span data-stu-id="b586f-212">Select **Yes**.</span></span>

    <span data-ttu-id="b586f-213">“操作窗格”上的**出站分类模板中断**按钮将变为可用。</span><span class="sxs-lookup"><span data-stu-id="b586f-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="b586f-214">在“操作窗格”上，选择**出站分类模板中断**。</span><span class="sxs-lookup"><span data-stu-id="b586f-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="b586f-215">在**出站分类条件**对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b586f-216">**参考表名称**：*装运*</span><span class="sxs-lookup"><span data-stu-id="b586f-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="b586f-217">**参考字段名称**：*承运人服务*</span><span class="sxs-lookup"><span data-stu-id="b586f-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="b586f-218">**按字段分组：** 选中此复选框可以按承运人服务对装运分组。</span><span class="sxs-lookup"><span data-stu-id="b586f-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="b586f-219">选择**确定**保存设置并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="b586f-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="b586f-220">设置集装箱装箱策略</span><span class="sxs-lookup"><span data-stu-id="b586f-220">Set up container packing policies</span></span>

1. <span data-ttu-id="b586f-221">转到**仓库管理 \> 设置 \> 集装箱 \> 集装箱装箱策略**。</span><span class="sxs-lookup"><span data-stu-id="b586f-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="b586f-222">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b586f-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b586f-223">在新策略的标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="b586f-224">**集装箱装箱策略**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="b586f-225">**描述**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="b586f-226">在**概览**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b586f-227">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="b586f-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b586f-228">**默认分类位置**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="b586f-229">**重量单位**：*千克*</span><span class="sxs-lookup"><span data-stu-id="b586f-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="b586f-230">**集装箱封闭策略**：*自动发放*</span><span class="sxs-lookup"><span data-stu-id="b586f-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="b586f-231">**集装箱发放策略**：*将集装箱分配到出站分类位置*</span><span class="sxs-lookup"><span data-stu-id="b586f-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="b586f-232">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="b586f-233">设置包装模板</span><span class="sxs-lookup"><span data-stu-id="b586f-233">Set up packing profiles</span></span>

<span data-ttu-id="b586f-234">创建一个将与分类功能一起使用的新装箱模板。</span><span class="sxs-lookup"><span data-stu-id="b586f-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="b586f-235">转到**仓库管理 \> 设置 \> 装箱 \> 装箱模板**。</span><span class="sxs-lookup"><span data-stu-id="b586f-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="b586f-236">在操作窗格上，选择**新建**创建行，并为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="b586f-237">**装箱模板 ID**：*Sort*</span><span class="sxs-lookup"><span data-stu-id="b586f-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="b586f-238">**描述**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="b586f-239">**集装箱装箱策略**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="b586f-240">**集装箱 ID 模式**：*自动*</span><span class="sxs-lookup"><span data-stu-id="b586f-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="b586f-241">**集装箱类型**：*大箱*</span><span class="sxs-lookup"><span data-stu-id="b586f-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="b586f-242">**在集装箱封闭时自动创建集装箱：** 清除（= *否*）</span><span class="sxs-lookup"><span data-stu-id="b586f-242">**Auto create container at container close:** Cleared (= *No*)</span></span>

1. <span data-ttu-id="b586f-243">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="b586f-244">设置工作类</span><span class="sxs-lookup"><span data-stu-id="b586f-244">Set up work classes</span></span>

<span data-ttu-id="b586f-245">设置将与分类一起使用的工作类。</span><span class="sxs-lookup"><span data-stu-id="b586f-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="b586f-246">转到**仓库管理 \> 设置 \> 工作 \> 工作类**。</span><span class="sxs-lookup"><span data-stu-id="b586f-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="b586f-247">在操作窗格上，选择**新建**创建用于分类的工作类，并为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="b586f-248">**工作类 ID**：*Sort*</span><span class="sxs-lookup"><span data-stu-id="b586f-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="b586f-249">**描述**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="b586f-250">**工作订单类型**：*分类库存领料*</span><span class="sxs-lookup"><span data-stu-id="b586f-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="b586f-251">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="b586f-252">设置移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="b586f-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="b586f-253">设置新托盘菜单项</span><span class="sxs-lookup"><span data-stu-id="b586f-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="b586f-254">创建移动设备菜单项以在分类过程中建立托盘。</span><span class="sxs-lookup"><span data-stu-id="b586f-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="b586f-255">转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="b586f-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b586f-256">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b586f-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b586f-257">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="b586f-258">**菜单项名称**：*建立托盘*</span><span class="sxs-lookup"><span data-stu-id="b586f-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="b586f-259">**标题**：*建立托盘*</span><span class="sxs-lookup"><span data-stu-id="b586f-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="b586f-260">**模式**：*间接*</span><span class="sxs-lookup"><span data-stu-id="b586f-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="b586f-261">**使用现有工作**：*否*</span><span class="sxs-lookup"><span data-stu-id="b586f-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="b586f-262">在**常规**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b586f-263">**活动代码**：*Outbound sorting*</span><span class="sxs-lookup"><span data-stu-id="b586f-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="b586f-264">当此字段设置为*出站分类*时，将显示**出站分类模板 ID** 字段。</span><span class="sxs-lookup"><span data-stu-id="b586f-264">When this field is set to *Outbound sorting*, the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="b586f-265">**使用流程指南**：*是*</span><span class="sxs-lookup"><span data-stu-id="b586f-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="b586f-266">当**活动代码**字段设置为*出站分类*时，此选项将自动设置为*是*。</span><span class="sxs-lookup"><span data-stu-id="b586f-266">When the **Activity code** field is set to *Outbound sorting*, this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="b586f-267">**出站分类模板 ID**：*AutoWork*</span><span class="sxs-lookup"><span data-stu-id="b586f-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="b586f-268">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="b586f-269">设置新装载菜单项</span><span class="sxs-lookup"><span data-stu-id="b586f-269">Set up a new loading menu item</span></span>

<span data-ttu-id="b586f-270">接下来，创建一个菜单项，让用户可以将已分类的库存物料移至装运位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="b586f-271">转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="b586f-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b586f-272">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b586f-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b586f-273">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="b586f-274">**菜单项名称**：*从分类装载*</span><span class="sxs-lookup"><span data-stu-id="b586f-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="b586f-275">**标题**：*从分类装载*</span><span class="sxs-lookup"><span data-stu-id="b586f-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="b586f-276">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="b586f-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="b586f-277">**使用现有工作**：*是*</span><span class="sxs-lookup"><span data-stu-id="b586f-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="b586f-278">在**常规**快速选项卡上，将**导向方式**字段设置为*用户导向*。</span><span class="sxs-lookup"><span data-stu-id="b586f-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="b586f-279">在**工作类**快速选项卡上，选择**新建**，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-279">On the **Work classes** FastTab, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="b586f-280">**工作类 ID**：*SORT*</span><span class="sxs-lookup"><span data-stu-id="b586f-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="b586f-281">**工作订单类型**：*分类库存领料*</span><span class="sxs-lookup"><span data-stu-id="b586f-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="b586f-282">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="b586f-283">设置移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="b586f-283">Set up the mobile device menu</span></span>

<span data-ttu-id="b586f-284">现在，您必须将新菜单项添加到移动设备菜单中。</span><span class="sxs-lookup"><span data-stu-id="b586f-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="b586f-285">转到**仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="b586f-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="b586f-286">选择**出货**菜单。</span><span class="sxs-lookup"><span data-stu-id="b586f-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="b586f-287">在操作窗格上，选择**编辑**。</span><span class="sxs-lookup"><span data-stu-id="b586f-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b586f-288">在**可用菜单和菜单项**栏，找到并选择**建立托盘**。</span><span class="sxs-lookup"><span data-stu-id="b586f-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="b586f-289">选择向右箭头按钮，将**建立托盘**移至**菜单结构**栏。</span><span class="sxs-lookup"><span data-stu-id="b586f-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="b586f-290">使用向上箭头和向下箭头按钮将**建立托盘**菜单项放置在移动设备菜单上的所需位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="b586f-291">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-291">Select **Save**.</span></span>
1. <span data-ttu-id="b586f-292">重复此过程，将**从分类装载**菜单项添加到**出站**菜单中。</span><span class="sxs-lookup"><span data-stu-id="b586f-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="b586f-293">设置库位指令</span><span class="sxs-lookup"><span data-stu-id="b586f-293">Set up location directives</span></span>

<span data-ttu-id="b586f-294">*位置指令*是帮助标识领料和使位置用于库存移动的规则。</span><span class="sxs-lookup"><span data-stu-id="b586f-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="b586f-295">现在，您必须创建一个规则来管理分类工作。</span><span class="sxs-lookup"><span data-stu-id="b586f-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="b586f-296">设置单 SKU 指令</span><span class="sxs-lookup"><span data-stu-id="b586f-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="b586f-297">转到**库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="b586f-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b586f-298">在左窗格中，将**工作订单类型**字段的值更改为*分类库存领料*。</span><span class="sxs-lookup"><span data-stu-id="b586f-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="b586f-299">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b586f-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b586f-300">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="b586f-301">**序列：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b586f-302">**名称**：*Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b586f-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="b586f-303">在**位置指令**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b586f-304">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="b586f-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b586f-305">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="b586f-305">**Site:** *6*</span></span>
    - <span data-ttu-id="b586f-306">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="b586f-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b586f-307">**多 SKU**：*否*</span><span class="sxs-lookup"><span data-stu-id="b586f-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="b586f-308">选择**保存**让**行**快速选项卡上的工具栏可用。</span><span class="sxs-lookup"><span data-stu-id="b586f-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="b586f-309">在**行**快速选项卡上，选择**新建**，然后在新行上设置以下值。</span><span class="sxs-lookup"><span data-stu-id="b586f-309">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="b586f-310">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="b586f-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="b586f-311">**序列：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b586f-312">**从**：*0*</span><span class="sxs-lookup"><span data-stu-id="b586f-312">**From:** *0*</span></span>
    - <span data-ttu-id="b586f-313">**到**：*1,000,000*</span><span class="sxs-lookup"><span data-stu-id="b586f-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="b586f-314">选择**保存**让**位置指令操作**快速选项卡上的工具栏可用。</span><span class="sxs-lookup"><span data-stu-id="b586f-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="b586f-315">在**位置指令操作**快速选项卡上，选择**新建**，然后在新行上设置以下值。</span><span class="sxs-lookup"><span data-stu-id="b586f-315">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="b586f-316">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="b586f-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="b586f-317">**序列：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b586f-318">**名称**：*Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b586f-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="b586f-319">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-319">Select **Save**.</span></span>
1. <span data-ttu-id="b586f-320">在**位置指令操作**快速选项卡上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="b586f-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="b586f-321">在查询编辑器中的**范围**选项卡上，找到**字段**字段设置为*位置*的行。</span><span class="sxs-lookup"><span data-stu-id="b586f-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="b586f-322">将此行的**条件**字段设置为*货架门*。</span><span class="sxs-lookup"><span data-stu-id="b586f-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="b586f-323">选择**确定**保存设置并关闭查询编辑器。</span><span class="sxs-lookup"><span data-stu-id="b586f-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="b586f-324">设置多 SKU 指令</span><span class="sxs-lookup"><span data-stu-id="b586f-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="b586f-325">转到**库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="b586f-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b586f-326">在左窗格中，将**工作订单类型**字段的值更改为*分类库存领料*。</span><span class="sxs-lookup"><span data-stu-id="b586f-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="b586f-327">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b586f-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b586f-328">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="b586f-329">**序列：** *2*</span><span class="sxs-lookup"><span data-stu-id="b586f-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="b586f-330">**名称**：*货架门（多）*</span><span class="sxs-lookup"><span data-stu-id="b586f-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="b586f-331">在**位置指令**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b586f-332">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="b586f-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b586f-333">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="b586f-333">**Site:** *6*</span></span>
    - <span data-ttu-id="b586f-334">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="b586f-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b586f-335">**多 SKU**：*是*</span><span class="sxs-lookup"><span data-stu-id="b586f-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="b586f-336">选择**保存**让**行**快速选项卡上的工具栏可用。</span><span class="sxs-lookup"><span data-stu-id="b586f-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="b586f-337">在**行**快速选项卡上，选择**新建**，然后在新行上设置以下值。</span><span class="sxs-lookup"><span data-stu-id="b586f-337">On the **Lines** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="b586f-338">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="b586f-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="b586f-339">**序列：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b586f-340">**从**：*0*</span><span class="sxs-lookup"><span data-stu-id="b586f-340">**From:** *0*</span></span>
    - <span data-ttu-id="b586f-341">**到**：*1,000,000*</span><span class="sxs-lookup"><span data-stu-id="b586f-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="b586f-342">选择**保存**让**位置指令操作**快速选项卡上的工具栏可用。</span><span class="sxs-lookup"><span data-stu-id="b586f-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="b586f-343">在**位置指令操作**快速选项卡上，选择**新建**，然后在新行上设置以下值。</span><span class="sxs-lookup"><span data-stu-id="b586f-343">On the **Location Directive Actions** FastTab, select **New**, and then set the following values on the new line.</span></span> <span data-ttu-id="b586f-344">接受其他所有字段的默认值。</span><span class="sxs-lookup"><span data-stu-id="b586f-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="b586f-345">**序列：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b586f-346">**名称**：*货架门（多）*</span><span class="sxs-lookup"><span data-stu-id="b586f-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="b586f-347">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-347">Select **Save**.</span></span>
1. <span data-ttu-id="b586f-348">在**位置指令操作**快速选项卡上，选择**编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="b586f-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="b586f-349">在查询编辑器中的**范围**选项卡上，找到**字段**字段设置为*位置*的行。</span><span class="sxs-lookup"><span data-stu-id="b586f-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="b586f-350">将此行的**条件**字段设置为*货架门*。</span><span class="sxs-lookup"><span data-stu-id="b586f-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="b586f-351">选择**确定**保存设置并关闭查询编辑器。</span><span class="sxs-lookup"><span data-stu-id="b586f-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="b586f-352">设置工作模板</span><span class="sxs-lookup"><span data-stu-id="b586f-352">Set up work templates</span></span>

1. <span data-ttu-id="b586f-353">转到**仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="b586f-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="b586f-354">将**工作订单类型**字段的值更改为*分类库存领料*。</span><span class="sxs-lookup"><span data-stu-id="b586f-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="b586f-355">在“操作窗格”中，选择**新建**创建一个工作模板。</span><span class="sxs-lookup"><span data-stu-id="b586f-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="b586f-356">在**概览**选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="b586f-357">**序列：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="b586f-358">**工作模板**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="b586f-359">**工作模板描述**：*分类*</span><span class="sxs-lookup"><span data-stu-id="b586f-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="b586f-360">选择**保存**激活**工作模板详细信息**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="b586f-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="b586f-361">在**工作模板详细信息**快速选项卡上，选择**新**添加一行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="b586f-362">**工作类型：** *领料*</span><span class="sxs-lookup"><span data-stu-id="b586f-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="b586f-363">**工作类 ID**：*SORT*</span><span class="sxs-lookup"><span data-stu-id="b586f-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="b586f-364">再次选择**新**添加第二行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="b586f-365">**工作类型：** *放入*</span><span class="sxs-lookup"><span data-stu-id="b586f-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="b586f-366">**工作类 ID**：*SORT*</span><span class="sxs-lookup"><span data-stu-id="b586f-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="b586f-367">选择**保存**。</span><span class="sxs-lookup"><span data-stu-id="b586f-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b586f-368">应用场景</span><span class="sxs-lookup"><span data-stu-id="b586f-368">Scenario</span></span>

<span data-ttu-id="b586f-369">此方案模拟了一种情况：根据装运承运人服务，装箱集装箱应在装箱工作站之后自动分类到不同位置（托盘）。</span><span class="sxs-lookup"><span data-stu-id="b586f-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="b586f-370">将来自负荷的所有物料装箱并按地址分类后，托盘将被移至货架门。</span><span class="sxs-lookup"><span data-stu-id="b586f-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="b586f-371">创建销售订单和领料工作</span><span class="sxs-lookup"><span data-stu-id="b586f-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="b586f-372">创建销售订单 1</span><span class="sxs-lookup"><span data-stu-id="b586f-372">Create sales order 1</span></span>

1. <span data-ttu-id="b586f-373">转到**销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="b586f-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b586f-374">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b586f-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b586f-375">在**创建销售订单**对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b586f-376">**客户帐户**：*US-005*</span><span class="sxs-lookup"><span data-stu-id="b586f-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="b586f-377">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="b586f-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b586f-378">选择**确定**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="b586f-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="b586f-379">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="b586f-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="b586f-380">切换到**标题**视图。</span><span class="sxs-lookup"><span data-stu-id="b586f-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="b586f-381">在**交货**快速选项卡的**运输**部分中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="b586f-382">**装运承运人**：*空运货物*</span><span class="sxs-lookup"><span data-stu-id="b586f-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="b586f-383">**承运人服务**：*航运*</span><span class="sxs-lookup"><span data-stu-id="b586f-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="b586f-384">切换到**行**视图。</span><span class="sxs-lookup"><span data-stu-id="b586f-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="b586f-385">如果没有在**销售订单行**快速选项卡上自动将新的空行添加到网格，选择**添加行**进行添加。</span><span class="sxs-lookup"><span data-stu-id="b586f-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="b586f-386">在新订单行上设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="b586f-387">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="b586f-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b586f-388">**数量：** *2*</span><span class="sxs-lookup"><span data-stu-id="b586f-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="b586f-389">在**销售订单行**快速选项卡上仍选择新订单行时，在网格上方的**库存**菜单上，选择**预留**。</span><span class="sxs-lookup"><span data-stu-id="b586f-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b586f-390">在**预留**页中，选择**预留批次**在仓库中预留所选行的全部数量。</span><span class="sxs-lookup"><span data-stu-id="b586f-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="b586f-391">关闭**预留**页回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="b586f-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b586f-392">在“操作窗格”上的**仓库**选项卡上，在**操作**组中，选择**发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="b586f-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="b586f-393">将收到参考消息，其中显示该订单的装运和波次。</span><span class="sxs-lookup"><span data-stu-id="b586f-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="b586f-394">记下波次 ID 和装运 ID 编号。</span><span class="sxs-lookup"><span data-stu-id="b586f-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="b586f-395">销售订单 2</span><span class="sxs-lookup"><span data-stu-id="b586f-395">Sales order 2</span></span>

1. <span data-ttu-id="b586f-396">转到**销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="b586f-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b586f-397">在操作窗格上，选择**新建**。</span><span class="sxs-lookup"><span data-stu-id="b586f-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b586f-398">在**创建销售订单**对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b586f-399">**客户帐户**：*US-006*</span><span class="sxs-lookup"><span data-stu-id="b586f-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="b586f-400">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="b586f-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b586f-401">选择**确定**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="b586f-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="b586f-402">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="b586f-402">The new sales order is opened.</span></span> <span data-ttu-id="b586f-403">**销售订单行**快速选项卡上的网格中应包含一个新的空行。</span><span class="sxs-lookup"><span data-stu-id="b586f-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="b586f-404">在此订单行上设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="b586f-405">\**物料：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="b586f-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="b586f-406">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="b586f-407">在**行详细信息**快速选项卡上的**交货**选项卡中，将**交货方式**字段设置为 *Flowe-STD*。</span><span class="sxs-lookup"><span data-stu-id="b586f-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="b586f-408">在**销售订单行**快速选项卡上，选择**添加行**，然后在第二个订单行上设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-408">On the **Sales order lines** FastTab, select **Add line**, and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="b586f-409">\**物料：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="b586f-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="b586f-410">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="b586f-411">在**行详细信息**快速选项卡上的**交货**选项卡中，将**交货方式**字段的值更改为*航运 C - 航运*。</span><span class="sxs-lookup"><span data-stu-id="b586f-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="b586f-412">在**销售订单行**快速选项卡上，选择第一个订单行。</span><span class="sxs-lookup"><span data-stu-id="b586f-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="b586f-413">然后，在网格上方的**库存**菜单中，选择**预留**。</span><span class="sxs-lookup"><span data-stu-id="b586f-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b586f-414">在**预留**页中，选择**预留批次**在仓库中预留所选行的全部数量。</span><span class="sxs-lookup"><span data-stu-id="b586f-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="b586f-415">关闭**预留**页回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="b586f-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b586f-416">在**销售订单行**快速选项卡上，选择第二个订单行。</span><span class="sxs-lookup"><span data-stu-id="b586f-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="b586f-417">然后，在网格上方的**库存**菜单中，选择**预留**。</span><span class="sxs-lookup"><span data-stu-id="b586f-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="b586f-418">在**预留**页中，选择**预留批次**在仓库中预留所选行的全部数量。</span><span class="sxs-lookup"><span data-stu-id="b586f-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="b586f-419">关闭**预留**页回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="b586f-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b586f-420">在“操作窗格”上的**仓库**选项卡上，在**操作**组中，选择**发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="b586f-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="b586f-421">将收到参考消息，其中显示该订单的装运和波次。</span><span class="sxs-lookup"><span data-stu-id="b586f-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="b586f-422">请注意，已经创建了两个波次 ID 编号和两个装运 ID 编号，每一个分别对应销售订单行的每个交货方式。</span><span class="sxs-lookup"><span data-stu-id="b586f-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="b586f-423">从工作详细信息中获取工作 ID</span><span class="sxs-lookup"><span data-stu-id="b586f-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="b586f-424">转到**仓库管理 \> 工作 \> 工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="b586f-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="b586f-425">此页面显示已从销售订单创建的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="b586f-426">使用您创建的销售订单中的波次 ID 和装运 ID 查找每个波次和装运的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="b586f-427">记下这些工作 ID，因为在接下来的步骤中将需要它们。</span><span class="sxs-lookup"><span data-stu-id="b586f-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="b586f-428">请注意，为第二个销售订单创建了两个工作 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="b586f-429">如果从不同位置领取了不同物料，将生成单独的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="b586f-430">为销售订单领取物料</span><span class="sxs-lookup"><span data-stu-id="b586f-430">Pick items for the sales orders</span></span>

<span data-ttu-id="b586f-431">通过使用移动设备将物料移至装箱工作站来完成创建的工作。</span><span class="sxs-lookup"><span data-stu-id="b586f-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="b586f-432">在移动设备上，使用为此方案创建的用户 ID（或现有演示数据用户的用户 ID）登录到仓库 *62*。</span><span class="sxs-lookup"><span data-stu-id="b586f-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="b586f-433">在主菜单上，选择**出站**。</span><span class="sxs-lookup"><span data-stu-id="b586f-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="b586f-434">在**出站**菜单上，选择**销售领料**。</span><span class="sxs-lookup"><span data-stu-id="b586f-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="b586f-435">在 **ID** 字段中，输入为销售订单 1 创建的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="b586f-436">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-436">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-437">在**销售订单 - 领料**页面上，输入为销售订单 1 创建的目标牌照。</span><span class="sxs-lookup"><span data-stu-id="b586f-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="b586f-438">请注意，将显示领料位置 (*bulk-001*)、物料 (*A0001*) 和数量（*2 件*）。</span><span class="sxs-lookup"><span data-stu-id="b586f-438">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*2 pcs*) are shown.</span></span>
1. <span data-ttu-id="b586f-439">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-439">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-440">查看**销售订单 - 放置**页上的信息。</span><span class="sxs-lookup"><span data-stu-id="b586f-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="b586f-441">**位置**字段应指示已领取物料将转到*装箱*位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="b586f-442">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-442">Select **OK**.</span></span>

    <span data-ttu-id="b586f-443">在**扫描工作 ID/牌照 ID** 页面上，您会收到“工作已完成”消息，指示销售订单 1 中的工作 ID 已完成。</span><span class="sxs-lookup"><span data-stu-id="b586f-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="b586f-444">现在，您将为销售订单 2 领料。</span><span class="sxs-lookup"><span data-stu-id="b586f-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="b586f-445">在 **ID** 字段中，输入为销售订单 2 创建的工作 ID，其中行 1 包含物料 *A0001*。</span><span class="sxs-lookup"><span data-stu-id="b586f-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="b586f-446">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-446">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-447">在**销售订单 - 领料**页上，输入目标牌照。</span><span class="sxs-lookup"><span data-stu-id="b586f-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="b586f-448">请注意，将显示领料位置 (*bulk-001*)、物料 (*A0001*) 和数量（*1 件*）。</span><span class="sxs-lookup"><span data-stu-id="b586f-448">Notice that the picking location (*bulk-001*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="b586f-449">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-449">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-450">查看**销售订单 - 放置**页上的信息。</span><span class="sxs-lookup"><span data-stu-id="b586f-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="b586f-451">**位置**字段应指示已领取物料将转到*装箱*位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="b586f-452">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-452">Select **OK**.</span></span>

    <span data-ttu-id="b586f-453">在**扫描工作 ID/牌照 ID** 页面上，您会收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="b586f-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="b586f-454">此消息指示销售订单 2 的行 1 中的工作 ID 已完成。</span><span class="sxs-lookup"><span data-stu-id="b586f-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="b586f-455">在 **ID** 字段中，输入为销售订单 2 创建的工作 ID，其中行 2 包含物料 *A0002*。</span><span class="sxs-lookup"><span data-stu-id="b586f-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="b586f-456">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-456">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-457">在**销售订单 - 领料**页上，输入目标牌照。</span><span class="sxs-lookup"><span data-stu-id="b586f-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="b586f-458">请注意，将显示领料位置 (*bulk-002*)、物料 (*A0001*) 和数量（*1 件*）。</span><span class="sxs-lookup"><span data-stu-id="b586f-458">Notice that the picking location (*bulk-002*), item (*A0001*), and quantity (*1 pcs*) are shown.</span></span>
1. <span data-ttu-id="b586f-459">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-459">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-460">查看**销售订单 - 放置**页上的信息。</span><span class="sxs-lookup"><span data-stu-id="b586f-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="b586f-461">**位置**字段应指示已领取物料将转到*装箱*位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="b586f-462">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-462">Select **OK**.</span></span>

    <span data-ttu-id="b586f-463">在**扫描工作 ID/牌照 ID** 页面上，您会收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="b586f-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="b586f-464">此消息指示销售订单 2 的行 2 中的工作 ID 已完成。</span><span class="sxs-lookup"><span data-stu-id="b586f-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="b586f-465">将销售订单装箱到集装箱</span><span class="sxs-lookup"><span data-stu-id="b586f-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="b586f-466">将销售订单 1 装箱到集装箱</span><span class="sxs-lookup"><span data-stu-id="b586f-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="b586f-467">转到**仓库管理 \> 装箱和集装化 \> 装箱**。</span><span class="sxs-lookup"><span data-stu-id="b586f-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="b586f-468">**选择装箱工作站**对话框将出现。</span><span class="sxs-lookup"><span data-stu-id="b586f-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="b586f-469">默认情况下，**工作人员**字段应设置为您之前设置的工作人员的名称。</span><span class="sxs-lookup"><span data-stu-id="b586f-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="b586f-470">设置以下值以查看和处理在特定装箱位置计划的装运和集装箱：</span><span class="sxs-lookup"><span data-stu-id="b586f-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="b586f-471">**站点**：*6*</span><span class="sxs-lookup"><span data-stu-id="b586f-471">**Site:** *6*</span></span>
    - <span data-ttu-id="b586f-472">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="b586f-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b586f-473">**位置**：*装箱*</span><span class="sxs-lookup"><span data-stu-id="b586f-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="b586f-474">**装箱模板 ID**：*Sort*</span><span class="sxs-lookup"><span data-stu-id="b586f-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="b586f-475">选择**确定**关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="b586f-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="b586f-476">在**装箱**页上的**牌照或装运**字段中，输入销售订单 1 的目标牌照。</span><span class="sxs-lookup"><span data-stu-id="b586f-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="b586f-477">然后，选择键盘上的 **Tab** 或 **Enter** 键移开此字段。</span><span class="sxs-lookup"><span data-stu-id="b586f-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="b586f-478">在“操作窗格”上，选择**新建集装箱**。</span><span class="sxs-lookup"><span data-stu-id="b586f-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="b586f-479">接受所有默认设置，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="b586f-480">记录集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="b586f-481">在**物料领取**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b586f-482">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="b586f-483">**标识符：** 物料 *A0001*</span><span class="sxs-lookup"><span data-stu-id="b586f-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="b586f-484">在“操作窗格”上，选择**封闭集装箱**。</span><span class="sxs-lookup"><span data-stu-id="b586f-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="b586f-485">在**封闭集装箱**对话框中，选择**获取系统重量**，让系统更新**毛重**字段。</span><span class="sxs-lookup"><span data-stu-id="b586f-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="b586f-486">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-486">Select **OK**.</span></span> <span data-ttu-id="b586f-487">集装箱将移至*分类*位置并准备好进行分类。</span><span class="sxs-lookup"><span data-stu-id="b586f-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="b586f-488">创建第二个集装箱，将销售订单 1 的牌照中的第二个物料添加到新集装箱中。</span><span class="sxs-lookup"><span data-stu-id="b586f-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="b586f-489">在“操作窗格”上，选择**新建集装箱**。</span><span class="sxs-lookup"><span data-stu-id="b586f-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="b586f-490">接受所有默认设置，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="b586f-491">记录集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="b586f-492">在**物料领取**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b586f-493">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="b586f-494">**标识符：** 物料 *A0001*</span><span class="sxs-lookup"><span data-stu-id="b586f-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="b586f-495">在“操作窗格”上，选择**封闭集装箱**。</span><span class="sxs-lookup"><span data-stu-id="b586f-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="b586f-496">在**封闭集装箱**对话框中，选择**获取系统重量**，让系统更新**毛重**字段。</span><span class="sxs-lookup"><span data-stu-id="b586f-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="b586f-497">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-497">Select **OK**.</span></span> <span data-ttu-id="b586f-498">集装箱将移至*分类*位置并准备好进行分类。</span><span class="sxs-lookup"><span data-stu-id="b586f-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="b586f-499">将销售订单 2 装箱到集装箱</span><span class="sxs-lookup"><span data-stu-id="b586f-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="b586f-500">在**装箱**页上的**牌照或装运**字段中，输入销售订单 2 的行 1 的目标牌照。</span><span class="sxs-lookup"><span data-stu-id="b586f-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="b586f-501">然后，选择键盘上的 **Tab** 或 **Enter** 键移开此字段。</span><span class="sxs-lookup"><span data-stu-id="b586f-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="b586f-502">在“操作窗格”上，选择**新建集装箱**。</span><span class="sxs-lookup"><span data-stu-id="b586f-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="b586f-503">接受所有默认设置，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="b586f-504">记录集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="b586f-505">在**物料领取**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b586f-506">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="b586f-507">**标识符：** 物料 *A0001*</span><span class="sxs-lookup"><span data-stu-id="b586f-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="b586f-508">在“操作窗格”上，选择**封闭集装箱**。</span><span class="sxs-lookup"><span data-stu-id="b586f-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="b586f-509">在**封闭集装箱**对话框中，选择**获取系统重量**，让系统更新**毛重**字段。</span><span class="sxs-lookup"><span data-stu-id="b586f-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="b586f-510">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-510">Select **OK**.</span></span> <span data-ttu-id="b586f-511">集装箱将移至*分类*位置并准备好进行分类。</span><span class="sxs-lookup"><span data-stu-id="b586f-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="b586f-512">在**牌照或装运**字段中，输入销售订单 2 的行 2 的目标牌照。</span><span class="sxs-lookup"><span data-stu-id="b586f-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="b586f-513">然后，选择键盘上的 **Tab** 或 **Enter** 键移开此字段。</span><span class="sxs-lookup"><span data-stu-id="b586f-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="b586f-514">在“操作窗格”上，选择**新建集装箱**。</span><span class="sxs-lookup"><span data-stu-id="b586f-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="b586f-515">接受所有默认设置，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="b586f-516">记录集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="b586f-517">在**物料领取**快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b586f-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b586f-518">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="b586f-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="b586f-519">**标识符字段：** 物料 *A0002*</span><span class="sxs-lookup"><span data-stu-id="b586f-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="b586f-520">在“操作窗格”上，选择**封闭集装箱**。</span><span class="sxs-lookup"><span data-stu-id="b586f-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="b586f-521">在**封闭集装箱**对话框中，选择**获取系统重量**，让系统更新**毛重**字段。</span><span class="sxs-lookup"><span data-stu-id="b586f-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="b586f-522">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-522">Select **OK**.</span></span> <span data-ttu-id="b586f-523">集装箱将移至*分类*位置并准备好进行分类。</span><span class="sxs-lookup"><span data-stu-id="b586f-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="b586f-524">要查看集装箱详细信息，转到**仓库管理 \> 装箱和集装化 \> 集装箱**，搜索在装箱过程中创建的集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers**, and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="b586f-525">对集装箱分类</span><span class="sxs-lookup"><span data-stu-id="b586f-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b586f-526">当您在移动应用上访问**建立托盘**菜单项以进行出站分类时，您将看到一个标记为**全部**的按钮。</span><span class="sxs-lookup"><span data-stu-id="b586f-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="b586f-527">*不要使用**全部**按钮来分类或关闭位置。*</span><span class="sxs-lookup"><span data-stu-id="b586f-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="b586f-528">**全部**按钮是默认提供的，不能禁用或从页面中删除。</span><span class="sxs-lookup"><span data-stu-id="b586f-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="b586f-529">它不用于*出站分类*功能。</span><span class="sxs-lookup"><span data-stu-id="b586f-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="b586f-530">分类第一个集装箱</span><span class="sxs-lookup"><span data-stu-id="b586f-530">Sort the first container</span></span>

1. <span data-ttu-id="b586f-531">在移动设备上，使用为此方案创建的用户 ID（或现有演示数据用户的用户 ID）登录到仓库 *62*。</span><span class="sxs-lookup"><span data-stu-id="b586f-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="b586f-532">在主菜单上，选择**出站**。</span><span class="sxs-lookup"><span data-stu-id="b586f-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="b586f-533">在**出站**菜单上，选择**建立托盘**。</span><span class="sxs-lookup"><span data-stu-id="b586f-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="b586f-534">在 **牌照/集装箱**字段中，输入与销售订单 1 相关联的第一个集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="b586f-535">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-535">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-536">由于当前不存在分类位置，因此必须指定一个。</span><span class="sxs-lookup"><span data-stu-id="b586f-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="b586f-537">在**分类位置 ID** 字段中，输入 *SP01*。</span><span class="sxs-lookup"><span data-stu-id="b586f-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="b586f-538">因为当前没有牌照与分类位置 *SP01* 关联，您必须指定一个。</span><span class="sxs-lookup"><span data-stu-id="b586f-538">Because no LP is currently associated with sort position *SP01*, you must specify one.</span></span> <span data-ttu-id="b586f-539">在**牌照**字段中，输入 *PLP01*。</span><span class="sxs-lookup"><span data-stu-id="b586f-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="b586f-540">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-540">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-541">由于分类位置验证已打开，因此您必须再次输入分类位置 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="b586f-542">在**分类位置 ID** 字段中，输入 *SP01*。</span><span class="sxs-lookup"><span data-stu-id="b586f-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="b586f-543">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-543">Select **OK**.</span></span>

    <span data-ttu-id="b586f-544">您将收到“工作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="b586f-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="b586f-545">要查看分类位置及其中的牌照，请转到**仓库管理 \> 装箱和集装化 \> 出站分类位置分配**。</span><span class="sxs-lookup"><span data-stu-id="b586f-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="b586f-546">**出站分类位置分配**页显示当前处于活动状态的所有分类位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="b586f-547">**分类位置事务**字段显示与每个分类位置关联的牌照，以及处于分类位置的集装箱。</span><span class="sxs-lookup"><span data-stu-id="b586f-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="b586f-548">请注意，当前存在一个分类位置，**分类位置条件**快速选项卡显示条件**装运 – 承运人服务 - 航运**。</span><span class="sxs-lookup"><span data-stu-id="b586f-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="b586f-549">对其余集装箱分类</span><span class="sxs-lookup"><span data-stu-id="b586f-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="b586f-550">在移动设备上，使用为此方案创建的用户 ID（或现有演示数据用户的用户 ID）登录到仓库 *62*。</span><span class="sxs-lookup"><span data-stu-id="b586f-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="b586f-551">在主菜单上，选择**出站**。</span><span class="sxs-lookup"><span data-stu-id="b586f-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="b586f-552">在**出站**菜单上，选择**建立托盘**。</span><span class="sxs-lookup"><span data-stu-id="b586f-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="b586f-553">在 **牌照/集装箱**字段中，输入与销售订单 1 相关联的第二个集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="b586f-554">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-554">Select **OK**.</span></span> <span data-ttu-id="b586f-555">由于分类模板已设置为自动分类，并且已经存在具有匹配条件的分类位置，因此您将被自动定向到正确的分类位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="b586f-556">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-556">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-557">确认分类位置 ID 指示库存位于正确的位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="b586f-558">在**分类位置 ID** 字段中，输入 *SP01*。</span><span class="sxs-lookup"><span data-stu-id="b586f-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="b586f-559">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-559">Select **OK**.</span></span>

    <span data-ttu-id="b586f-560">销售订单 1 中第二个集装箱的工作已完成。</span><span class="sxs-lookup"><span data-stu-id="b586f-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="b586f-561">现在，您将对销售订单 2 中的其余容器进行分类。</span><span class="sxs-lookup"><span data-stu-id="b586f-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="b586f-562">在**牌照/集装箱**字段中，输入包含物料 *A0001* 的销售订单 2 中的集装箱的集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="b586f-563">由于承运人服务不同，因此系统会提示您输入新的分类位置，并为该位置分配牌照。</span><span class="sxs-lookup"><span data-stu-id="b586f-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="b586f-564">使用分类位置 *SP02* 和牌照 *PLP02*。</span><span class="sxs-lookup"><span data-stu-id="b586f-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="b586f-565">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-565">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-566">在**分类位置 ID** 字段中输入 *SP02* 来确认分类位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="b586f-567">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-567">Select **OK**.</span></span>

    <span data-ttu-id="b586f-568">此集装箱的工作已完成。</span><span class="sxs-lookup"><span data-stu-id="b586f-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="b586f-569">在**牌照/集装箱**字段中，输入包含物料 *A0002* 的销售订单 2 中的其余集装箱的集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="b586f-570">因为承运人服务与销售订单 1 的承运人服务相同，系统显示具有匹配条件的现有分类位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="b586f-571">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-571">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-572">在**分类位置 ID** 字段中输入 *SP01* 来确认分类位置。</span><span class="sxs-lookup"><span data-stu-id="b586f-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="b586f-573">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-573">Select **OK**.</span></span>

    <span data-ttu-id="b586f-574">此集装箱的工作已完成。</span><span class="sxs-lookup"><span data-stu-id="b586f-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="b586f-575">关闭出站分类位置</span><span class="sxs-lookup"><span data-stu-id="b586f-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="b586f-576">对所有库存进行分类后，必须先关闭该位置，然后才能创建工作。</span><span class="sxs-lookup"><span data-stu-id="b586f-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="b586f-577">将创建已分类库存的领料工作来将库存带到货架门。</span><span class="sxs-lookup"><span data-stu-id="b586f-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="b586f-578">从移动设备关闭位置</span><span class="sxs-lookup"><span data-stu-id="b586f-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="b586f-579">在移动设备上，使用为此方案创建的用户 ID（或现有演示数据用户的用户 ID）登录到仓库 *62*。</span><span class="sxs-lookup"><span data-stu-id="b586f-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="b586f-580">在主菜单上，选择**出站**。</span><span class="sxs-lookup"><span data-stu-id="b586f-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="b586f-581">在**出站**菜单上，选择**建立托盘**。</span><span class="sxs-lookup"><span data-stu-id="b586f-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="b586f-582">在**牌照/集装箱**字段中，输入已分类到分类位置 *SP01* 的集装箱 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="b586f-583">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-583">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-584">您将收到以下消息：“此集装箱已被分类到位置 SP01。</span><span class="sxs-lookup"><span data-stu-id="b586f-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="b586f-585">是否关闭此位置？”</span><span class="sxs-lookup"><span data-stu-id="b586f-585">Close the position?"</span></span> <span data-ttu-id="b586f-586">选择**关闭**。</span><span class="sxs-lookup"><span data-stu-id="b586f-586">Select **Close**.</span></span>

    <span data-ttu-id="b586f-587">工作已完成。</span><span class="sxs-lookup"><span data-stu-id="b586f-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="b586f-588">从出站分类位置分配关闭位置</span><span class="sxs-lookup"><span data-stu-id="b586f-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="b586f-589">转到**仓库管理 \> 装箱和集装化 \> 出站分类位置分配**。</span><span class="sxs-lookup"><span data-stu-id="b586f-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="b586f-590">在左栏中，选择 **SP02**。</span><span class="sxs-lookup"><span data-stu-id="b586f-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="b586f-591">此出站分类位置行是您将要关闭的行。</span><span class="sxs-lookup"><span data-stu-id="b586f-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="b586f-592">在“操作窗格”上，选择**关闭位置**。</span><span class="sxs-lookup"><span data-stu-id="b586f-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="b586f-593">分类位置记录将关闭并且不再显示。</span><span class="sxs-lookup"><span data-stu-id="b586f-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="b586f-594">要显示所有关闭的位置记录，选择**显示已关闭**复选框。</span><span class="sxs-lookup"><span data-stu-id="b586f-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="b586f-595">已排序库存领料</span><span class="sxs-lookup"><span data-stu-id="b586f-595">Sorted inventory picking</span></span>

<span data-ttu-id="b586f-596">您必须完成已分类库存的领料工作。</span><span class="sxs-lookup"><span data-stu-id="b586f-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="b586f-597">完成后，库存将被领取到销售订单。</span><span class="sxs-lookup"><span data-stu-id="b586f-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="b586f-598">这时，所有其他仓库流程都适用。</span><span class="sxs-lookup"><span data-stu-id="b586f-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="b586f-599">在移动设备上，使用为此方案创建的用户 ID（或现有演示数据用户的用户 ID）登录到仓库 *62*。</span><span class="sxs-lookup"><span data-stu-id="b586f-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="b586f-600">在主菜单上，选择**出站**。</span><span class="sxs-lookup"><span data-stu-id="b586f-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="b586f-601">在**出站**菜单上，选择**从分类装载**。</span><span class="sxs-lookup"><span data-stu-id="b586f-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="b586f-602">输入第一个分类位置 *SP01* 的目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="b586f-603">将 **ID** 字段设置为 *PLP01*。</span><span class="sxs-lookup"><span data-stu-id="b586f-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="b586f-604">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-604">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-605">**已分类库存领料：领料**页显示必须完成的领料工作。</span><span class="sxs-lookup"><span data-stu-id="b586f-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="b586f-606">从*分类*位置和目标牌照 *PLP01* 领料，将有多个物料，数量为 *3*。</span><span class="sxs-lookup"><span data-stu-id="b586f-606">Pick from the *SORT* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="b586f-607">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-607">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-608">**已分类库存领料：放置**页显示必须完成的放置工作。</span><span class="sxs-lookup"><span data-stu-id="b586f-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="b586f-609">放置到*货架门*位置和目标牌照 *PLP01*，将有多个物料，数量为 *3*。</span><span class="sxs-lookup"><span data-stu-id="b586f-609">Put to the *Baydoor* location and target LP *PLP01*, which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="b586f-610">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-610">Select **OK**.</span></span>

    <span data-ttu-id="b586f-611">工作已完成。</span><span class="sxs-lookup"><span data-stu-id="b586f-611">Work is completed.</span></span>

1. <span data-ttu-id="b586f-612">输入第二个分类位置 *SP02* 的目标牌照 ID。</span><span class="sxs-lookup"><span data-stu-id="b586f-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="b586f-613">将 **ID** 字段设置为 *PLP02*。</span><span class="sxs-lookup"><span data-stu-id="b586f-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="b586f-614">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-614">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-615">**已分类库存领料：领料**页显示必须完成的领料工作。</span><span class="sxs-lookup"><span data-stu-id="b586f-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="b586f-616">从*分类*位置和目标牌照 *PLP02* 领料，将有多个物料，数量为 *1*。</span><span class="sxs-lookup"><span data-stu-id="b586f-616">Pick from the *SORT* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="b586f-617">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-617">Select **OK**.</span></span>
1. <span data-ttu-id="b586f-618">**已分类库存领料：放置**页显示必须完成的放置工作。</span><span class="sxs-lookup"><span data-stu-id="b586f-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="b586f-619">放置到*货架门*位置和目标牌照 *PLP02*，将有多个物料，数量为 *1*。</span><span class="sxs-lookup"><span data-stu-id="b586f-619">Put to the *Baydoor* location and target LP *PLP02*, which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="b586f-620">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b586f-620">Select **OK**.</span></span>

    <span data-ttu-id="b586f-621">工作已完成。</span><span class="sxs-lookup"><span data-stu-id="b586f-621">Work is completed.</span></span>

<span data-ttu-id="b586f-622">从此时开始，所有其他仓库流程都将适用。</span><span class="sxs-lookup"><span data-stu-id="b586f-622">From this point forward, all other warehouse processes apply.</span></span>