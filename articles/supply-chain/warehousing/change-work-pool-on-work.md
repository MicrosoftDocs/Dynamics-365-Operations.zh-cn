---
title: 更改工作的工作池
description: 本主题说明如何使用工作项的“更改工作池”按钮来更改现有工作的工作池。
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 66d110c3235e8a87b64bf160bdad8524fad6abe5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001141"
---
# <a name="change-work-pool-on-work"></a><span data-ttu-id="d9483-103">更改工作的工作池</span><span class="sxs-lookup"><span data-stu-id="d9483-103">Change work pool on work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9483-104">您可以使用工作池将工作组织到组。</span><span class="sxs-lookup"><span data-stu-id="d9483-104">You can use work pools to organize work into groups.</span></span> <span data-ttu-id="d9483-105">例如，您可以创建工作池以为在特定仓库库位进行的工作分类。</span><span class="sxs-lookup"><span data-stu-id="d9483-105">For example, you can create a work pool to classify work that occurs in a specific warehouse location.</span></span>

<span data-ttu-id="d9483-106">*更改工作的工作池* 功能在工作项的“操作窗格”中添加了 **更改工作池** 按钮。</span><span class="sxs-lookup"><span data-stu-id="d9483-106">The *Change work pool on work* feature adds a **Change work pool** button to the Action Pane for work items.</span></span> <span data-ttu-id="d9483-107">因此，仓库经理可以轻松地更改现有工作的工作池。</span><span class="sxs-lookup"><span data-stu-id="d9483-107">Therefore, warehouse managers can easily change the work pool of existing work.</span></span> <span data-ttu-id="d9483-108">此功能使经理可以对仓库车间的变化做出快速反应，并有助于提高他们适应变化情况的能力，改进将工作转移到另一个工作池的需求。</span><span class="sxs-lookup"><span data-stu-id="d9483-108">This feature lets managers react quickly to changes on the warehouse shop floor, and it helps improve their ability to adapt to changing situations and the need to transfer work to another work pool.</span></span>

## <a name="turn-on-the-change-work-pool-on-work-feature"></a><span data-ttu-id="d9483-109">启用“更改工作的工作池”功能</span><span class="sxs-lookup"><span data-stu-id="d9483-109">Turn on the Change work pool on work feature</span></span>

<span data-ttu-id="d9483-110">在开始设置或使用此功能之前，必须确保它在系统中可用。</span><span class="sxs-lookup"><span data-stu-id="d9483-110">Before you begin to set up or use this feature, you must make sure that it's available in your system.</span></span> <span data-ttu-id="d9483-111">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="d9483-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d9483-112">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="d9483-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d9483-113">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="d9483-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d9483-114">**功能名称**：*更改工作的工作池*</span><span class="sxs-lookup"><span data-stu-id="d9483-114">**Feature name:** *Change work pool on work*</span></span>

## <a name="set-up-the-change-work-pool-on-work-feature"></a><span data-ttu-id="d9483-115">设置“更改工作的工作池”功能</span><span class="sxs-lookup"><span data-stu-id="d9483-115">Set up the Change work pool on work feature</span></span>

<span data-ttu-id="d9483-116">要使用此功能，您必须设置一些工作池。</span><span class="sxs-lookup"><span data-stu-id="d9483-116">To use this feature, you must have some work pools set up.</span></span> <span data-ttu-id="d9483-117">您还可以设置工作模板，让它们自动分配池。</span><span class="sxs-lookup"><span data-stu-id="d9483-117">You might also set up your work templates so that they automatically assign a pool.</span></span> <span data-ttu-id="d9483-118">如果要完成本主题后文提供的示例场景，请按照本部分中的说明设置系统。</span><span class="sxs-lookup"><span data-stu-id="d9483-118">If you want to work through the example scenario that is provided later in this topic, set up your system as described in this section.</span></span>

### <a name="set-up-work-pools"></a><span data-ttu-id="d9483-119">设置工作池</span><span class="sxs-lookup"><span data-stu-id="d9483-119">Set up work pools</span></span>

<span data-ttu-id="d9483-120">工作池让您可以按类型组织工作项。</span><span class="sxs-lookup"><span data-stu-id="d9483-120">Work pools let you organize work items by type.</span></span> <span data-ttu-id="d9483-121">要使用 *更改工作的工作池* 功能，您必须至少有两个可用工作池。</span><span class="sxs-lookup"><span data-stu-id="d9483-121">To work with the *Change work pool on work* feature, you must have at least two work pools available.</span></span> <span data-ttu-id="d9483-122">要查看和添加工作池，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d9483-122">To view and add work pools, follow these steps.</span></span>

1. <span data-ttu-id="d9483-123">转到 **仓库管理 \> 设置 \> 工作 \> 工作池**。</span><span class="sxs-lookup"><span data-stu-id="d9483-123">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="d9483-124">如果您使用的是 **USMF** 公司的演示数据，并将演练本主题后面的示例方案，请添加两个具有以下设置的工作池：</span><span class="sxs-lookup"><span data-stu-id="d9483-124">If you're working with demo data from the **USMF** company and will work through the example scenario later in this topic, add two work pools that have the following settings:</span></span>

    - <span data-ttu-id="d9483-125">工作池 1：</span><span class="sxs-lookup"><span data-stu-id="d9483-125">Work pool 1:</span></span>

        - <span data-ttu-id="d9483-126">**工作池 ID**：*Webshop*</span><span class="sxs-lookup"><span data-stu-id="d9483-126">**Work pool ID:** *Webshop*</span></span>
        - <span data-ttu-id="d9483-127">**描述**：*网上商店*</span><span class="sxs-lookup"><span data-stu-id="d9483-127">**Description:** *Web Shop*</span></span>

    - <span data-ttu-id="d9483-128">工作池 2：</span><span class="sxs-lookup"><span data-stu-id="d9483-128">Work pool 2:</span></span>

        - <span data-ttu-id="d9483-129">**工作池 ID**：*CallCenter*</span><span class="sxs-lookup"><span data-stu-id="d9483-129">**Work pool ID:** *CallCenter*</span></span>
        - <span data-ttu-id="d9483-130">**描述**：*呼叫中心*</span><span class="sxs-lookup"><span data-stu-id="d9483-130">**Description:** *Call Center*</span></span>

1. <span data-ttu-id="d9483-131">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d9483-131">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="d9483-132">设置工作模板</span><span class="sxs-lookup"><span data-stu-id="d9483-132">Set up work templates</span></span>

<span data-ttu-id="d9483-133">对于每个工作模板，您可以根据需要设置默认工作池。</span><span class="sxs-lookup"><span data-stu-id="d9483-133">For each of your work templates, you can set a default work pool, as you require.</span></span> <span data-ttu-id="d9483-134">对于每个相关模板，您可以在 **工作池 ID** 栏分配工作池。</span><span class="sxs-lookup"><span data-stu-id="d9483-134">For each relevant template, you assign a work pool in the **Work pool ID** column.</span></span> <span data-ttu-id="d9483-135">这样，使用给定模板生成的所有工作项将会自动继承分配的工作池。</span><span class="sxs-lookup"><span data-stu-id="d9483-135">In this case, all work items that are generated by using a given template automatically inherit the assigned work pool.</span></span> <span data-ttu-id="d9483-136">如果您使用的是 **USMF** 公司的演示数据，并将演练本主题后面的示例方案，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="d9483-136">If you're working with the demo data from the **USMF** company and will work through the example scenario later in this topic, follow these steps.</span></span>

1. <span data-ttu-id="d9483-137">转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="d9483-137">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="d9483-138">在操作窗格上，选择 **编辑** 将页面设置为编辑模式。</span><span class="sxs-lookup"><span data-stu-id="d9483-138">On the Action Pane, select **Edit** to put the page into editing mode.</span></span>
1. <span data-ttu-id="d9483-139">通过设置以下值来编辑模板：</span><span class="sxs-lookup"><span data-stu-id="d9483-139">Edit the template by setting the following values:</span></span>

    - <span data-ttu-id="d9483-140">**工作模板**：*62 领料装箱*</span><span class="sxs-lookup"><span data-stu-id="d9483-140">**Work template:** *62 Pick to pack*</span></span>
    - <span data-ttu-id="d9483-141">**工作池 ID**：*Webshop*</span><span class="sxs-lookup"><span data-stu-id="d9483-141">**Work pool ID:** *Webshop*</span></span>

1. <span data-ttu-id="d9483-142">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="d9483-142">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="d9483-143">示例场景</span><span class="sxs-lookup"><span data-stu-id="d9483-143">Example scenario</span></span>

<span data-ttu-id="d9483-144">此方案演示如何通过更改工作项的工作池来更改现有工作项的处理流。</span><span class="sxs-lookup"><span data-stu-id="d9483-144">This scenario shows how to change the stream of processing for an existing work item by changing its work pool.</span></span> <span data-ttu-id="d9483-145">它使用 **USMF** 公司的演示数据以及本主题前面建议的设置。</span><span class="sxs-lookup"><span data-stu-id="d9483-145">It uses demo data from the **USMF** company and the settings that were suggested earlier in this topic.</span></span>

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a><span data-ttu-id="d9483-146">创建销售订单并将其下达到仓库</span><span class="sxs-lookup"><span data-stu-id="d9483-146">Create a sales order and release it to the warehouse</span></span>

1. <span data-ttu-id="d9483-147">确认仓库 *62* 中的物料 *A0001* 和 *A0002* 有足够的现有库存量。</span><span class="sxs-lookup"><span data-stu-id="d9483-147">Confirm that there is enough on-hand inventory for items *A0001* and *A0002* in warehouse *62*.</span></span> <span data-ttu-id="d9483-148">转到 **库存管理 \> 查询和报表 \> 现有量列表**，然后按以下所示编辑筛选器：</span><span class="sxs-lookup"><span data-stu-id="d9483-148">Go to **Inventory management \> Inquiries and reports \> On-hand list**, and edit the filters as shown here:</span></span>

    - <span data-ttu-id="d9483-149">**仓库** 值以 *62* 开头。</span><span class="sxs-lookup"><span data-stu-id="d9483-149">The **Warehouse** value begins with *62*.</span></span>
    - <span data-ttu-id="d9483-150">**物料编号** 值为 *A001* 或 *A002*。</span><span class="sxs-lookup"><span data-stu-id="d9483-150">The **Item number** value is either *A001* or *A002*.</span></span>

    <span data-ttu-id="d9483-151">每一项的演示数据应有 10 个。</span><span class="sxs-lookup"><span data-stu-id="d9483-151">Demo data should have a quantity of 10 each.</span></span>

    <span data-ttu-id="d9483-152">接下来，您必须创建一个销售订单。</span><span class="sxs-lookup"><span data-stu-id="d9483-152">Next, you must create a sales order.</span></span>

1. <span data-ttu-id="d9483-153">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="d9483-153">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="d9483-154">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="d9483-154">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d9483-155">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="d9483-155">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="d9483-156">**客户帐户**：*US-007*</span><span class="sxs-lookup"><span data-stu-id="d9483-156">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="d9483-157">**仓库**：*62*</span><span class="sxs-lookup"><span data-stu-id="d9483-157">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="d9483-158">选择 **确定** 创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="d9483-158">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="d9483-159">将打开新销售订单。</span><span class="sxs-lookup"><span data-stu-id="d9483-159">The new sales order is opened.</span></span> <span data-ttu-id="d9483-160">**销售订单行** 快速选项卡上的网格中应包含一个新的空行。</span><span class="sxs-lookup"><span data-stu-id="d9483-160">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d9483-161">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="d9483-161">On this line, set the following values:</span></span>

    - <span data-ttu-id="d9483-162">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="d9483-162">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="d9483-163">**数量：** *2*</span><span class="sxs-lookup"><span data-stu-id="d9483-163">**Quantity:** *2*</span></span>

1. <span data-ttu-id="d9483-164">在网格上方的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="d9483-164">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="d9483-165">在 **预留** 页面的“操作窗格”中，选择 **预留批次** 预留库存。</span><span class="sxs-lookup"><span data-stu-id="d9483-165">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="d9483-166">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d9483-166">Close the page.</span></span>
1. <span data-ttu-id="d9483-167">在 **销售订单行** 快速选项卡上，选择 **添加行** 在您的销售订单中添加另一行。</span><span class="sxs-lookup"><span data-stu-id="d9483-167">On the **Sales order lines** FastTab, select **Add line** to add another line to your sales order.</span></span> <span data-ttu-id="d9483-168">在这个行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="d9483-168">On this line, set the following values:</span></span>

    - <span data-ttu-id="d9483-169">\**物料编号：\*\*\*A0002*</span><span class="sxs-lookup"><span data-stu-id="d9483-169">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="d9483-170">**数量：** *2*</span><span class="sxs-lookup"><span data-stu-id="d9483-170">**Quantity:** *2*</span></span>

1. <span data-ttu-id="d9483-171">在网格上方的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="d9483-171">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="d9483-172">在 **预留** 页面的“操作窗格”中，选择 **预留批次** 预留库存。</span><span class="sxs-lookup"><span data-stu-id="d9483-172">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve the inventory.</span></span>
1. <span data-ttu-id="d9483-173">关闭该页面。</span><span class="sxs-lookup"><span data-stu-id="d9483-173">Close the page.</span></span>
1. <span data-ttu-id="d9483-174">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="d9483-174">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="d9483-175">您将收到信息性消息，其中显示从下达创建的波次 ID 和装运 ID。</span><span class="sxs-lookup"><span data-stu-id="d9483-175">You receive informational messages that show the wave ID and shipment ID that were created from the release.</span></span> <span data-ttu-id="d9483-176">记录波次 ID。</span><span class="sxs-lookup"><span data-stu-id="d9483-176">Make a note of the wave ID.</span></span>

### <a name="review-the-outbound-wave"></a><span data-ttu-id="d9483-177">查看出站波次</span><span class="sxs-lookup"><span data-stu-id="d9483-177">Review the outbound wave</span></span>

1. <span data-ttu-id="d9483-178">转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。</span><span class="sxs-lookup"><span data-stu-id="d9483-178">Go to **Warehouse management \> Outbound waves \> Shipment waves \> All waves**.</span></span>
1. <span data-ttu-id="d9483-179">在网格中，搜索从销售订单下达创建的波次 ID。</span><span class="sxs-lookup"><span data-stu-id="d9483-179">In the grid, search for the wave ID that was created from the release of the sales order.</span></span>
1. <span data-ttu-id="d9483-180">选择波次 ID 查看详细信息。</span><span class="sxs-lookup"><span data-stu-id="d9483-180">Select the wave ID to view the details.</span></span>
1. <span data-ttu-id="d9483-181">在 **波次行** 快速选项卡上，确保显示了销售订单的装运 ID。</span><span class="sxs-lookup"><span data-stu-id="d9483-181">On the **Wave lines** FastTab, make sure that a shipment ID is shown for the sales order.</span></span>

    > [!TIP]
    > <span data-ttu-id="d9483-182">如果在装运波次模板的设置中将 **在发放到仓库时处理波次** 选项设置为 *否*，则必须通过从“操作窗格”上的 **波次** 选项卡选择 **处理** 来手动处理波次以创建工作。</span><span class="sxs-lookup"><span data-stu-id="d9483-182">If the **Process wave at release to warehouse** option is set to *No* in the setup for the shipping wave template, you must manually process the wave by selecting **Process** from the **Wave** tab on the Action Pane to create work.</span></span>

1. <span data-ttu-id="d9483-183">确保波次已处理。</span><span class="sxs-lookup"><span data-stu-id="d9483-183">Make sure that the wave has been processed.</span></span> <span data-ttu-id="d9483-184">此处理将创建所需的工作。</span><span class="sxs-lookup"><span data-stu-id="d9483-184">This processing creates the required work.</span></span>

### <a name="view-work-details-and-change-the-work-pool"></a><span data-ttu-id="d9483-185">查看工作详细信息与更改工作池</span><span class="sxs-lookup"><span data-stu-id="d9483-185">View work details and change the work pool</span></span>

<span data-ttu-id="d9483-186">您可以使用 **工作详细信息** 页面查看已创建的工作和管理工作池。</span><span class="sxs-lookup"><span data-stu-id="d9483-186">You can use the **Work details** page to view the work that was created and to manage the work pool.</span></span>

1. <span data-ttu-id="d9483-187">转到 **仓库管理 \> 工作 \> 工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="d9483-187">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="d9483-188">选择刚才创建的工作的行。</span><span class="sxs-lookup"><span data-stu-id="d9483-188">Select the row for the work that was just created.</span></span> <span data-ttu-id="d9483-189">**订单编号** 列将显示销售订单编号。</span><span class="sxs-lookup"><span data-stu-id="d9483-189">The **Order number** column will show the sales order number.</span></span>

    <span data-ttu-id="d9483-190">**工作池 ID** 字段将设置为在工作模板中设置的工作池 ID。</span><span class="sxs-lookup"><span data-stu-id="d9483-190">The **Work pool ID** field will be set to the work pool ID that was set up in the work template.</span></span>

    > [!TIP]
    > <span data-ttu-id="d9483-191">如果看不到 **工作池 ID** 字段，将列添加到网格，然后刷新页面。</span><span class="sxs-lookup"><span data-stu-id="d9483-191">If you don't see the **Work pool ID** field, add the column to the grid, and then refresh the page.</span></span>

1. <span data-ttu-id="d9483-192">要更改与工作 ID 关联的工作池，请在“操作”窗格上，在 **工作** 选项卡上，选择 **更改工作池 ID**。</span><span class="sxs-lookup"><span data-stu-id="d9483-192">To change the work pool that is associated with the work ID, on the Action Pane, on the **Work** tab, select **Change Work pool ID**.</span></span>
1. <span data-ttu-id="d9483-193">在 **更改工作池** 对话框中的 **参数** 快速选项卡上，在 **工作池 ID** 字段中，选择 *CallCenter*。</span><span class="sxs-lookup"><span data-stu-id="d9483-193">In the **Change work pool** dialog box, on the **Parameters** FastTab, in the **Work pool ID** field, select *CallCenter*.</span></span>
1. <span data-ttu-id="d9483-194">选择 **确定** 应用更改。</span><span class="sxs-lookup"><span data-stu-id="d9483-194">Select **OK** to apply your change.</span></span>
1. <span data-ttu-id="d9483-195">请注意，**工作池 ID** 字段的值现已更改为 *CallCenter*。</span><span class="sxs-lookup"><span data-stu-id="d9483-195">Notice that the value of the **Work pool ID** field has now been changed to *CallCenter*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9483-196">当出现 **更改工作池** 对话框时，默认情况下，**工作池 ID** 字段可能为空白。</span><span class="sxs-lookup"><span data-stu-id="d9483-196">When the **Change work pool** dialog box appears, the **Work pool ID** field might be blank by default.</span></span> <span data-ttu-id="d9483-197">如果选择 **确定** 应用更改时此字段为空白，则将工作池从工作中完全删除。</span><span class="sxs-lookup"><span data-stu-id="d9483-197">If the field is blank when you select **OK** to apply changes, you will remove the work pool completely from the work.</span></span>
>
> <span data-ttu-id="d9483-198">除了切换工作池外，您还可以使用此过程将工作池添加到没有工作池的任何工作项中，或从有工作池的任何工作项中删除工作池。</span><span class="sxs-lookup"><span data-stu-id="d9483-198">In addition to switching work pools, you can use this procedure to add a work pool to any work item that doesn't have one, or to remove a work pool from any work item that does have one.</span></span>
