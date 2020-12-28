---
title: 工作行详细信息
description: 本主题介绍“工作行详细信息”页，该页显示系统中单个工作行丰富的可排序、可筛选列表。
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bcb340b21e06b294a40784bf3a1da71b0daf7655
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4423376"
---
# <a name="work-line-details"></a><span data-ttu-id="7bb44-103">工作行详细信息</span><span class="sxs-lookup"><span data-stu-id="7bb44-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bb44-104">**工作行详细信息** 页显示系统中单个工作行丰富的可排序、可筛选列表。</span><span class="sxs-lookup"><span data-stu-id="7bb44-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="7bb44-105">其提供窗口中正在规划和执行的工作的完整概览。</span><span class="sxs-lookup"><span data-stu-id="7bb44-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="7bb44-106">可以轻松地在查看所有工作行与仅查看未结工作行之间切换。</span><span class="sxs-lookup"><span data-stu-id="7bb44-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="7bb44-107">为每行提供的详细信息中包含工作状态、物料编号、货位、工作数量、负荷 ID 和装运 ID。</span><span class="sxs-lookup"><span data-stu-id="7bb44-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="7bb44-108">开启工作行详细信息功能</span><span class="sxs-lookup"><span data-stu-id="7bb44-108">Turn on the work line details feature</span></span>

<span data-ttu-id="7bb44-109">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="7bb44-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="7bb44-110">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="7bb44-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="7bb44-111">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="7bb44-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7bb44-112">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="7bb44-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="7bb44-113">**功能名称**：*工作行详细信息*</span><span class="sxs-lookup"><span data-stu-id="7bb44-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="7bb44-114">打开和使用“工作行详细信息”页</span><span class="sxs-lookup"><span data-stu-id="7bb44-114">Open and use the Work line details page</span></span>

<span data-ttu-id="7bb44-115">若要查看工作行详细信息列表，请转到 **仓库管理 \> 工作 \> 工作行详细信息**。</span><span class="sxs-lookup"><span data-stu-id="7bb44-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="7bb44-116">可从此处执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="7bb44-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="7bb44-117">使用 **筛选器** 中的搜索任何可用参数具有特定值的行。</span><span class="sxs-lookup"><span data-stu-id="7bb44-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="7bb44-118">（可用参数包括不在网格中显示为列的大量参数。）</span><span class="sxs-lookup"><span data-stu-id="7bb44-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="7bb44-119">使用 **显示已结** 复选框显示或隐藏已结行。</span><span class="sxs-lookup"><span data-stu-id="7bb44-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="7bb44-120">选择 **显示维度** 打开 **维度显示** 对话框，可在其中选择在网格中显示还是隐藏各维度列。</span><span class="sxs-lookup"><span data-stu-id="7bb44-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="7bb44-121">选择任何列标题打开一个菜单，可在其中选择按该列中的值排序或筛选。</span><span class="sxs-lookup"><span data-stu-id="7bb44-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="7bb44-122">选择一个工作行，然后选择 **更改货位** 打开一个对话框，可在其中更改该工作行的货位。</span><span class="sxs-lookup"><span data-stu-id="7bb44-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="7bb44-123">您指定的货位将覆盖货位指令的设置。</span><span class="sxs-lookup"><span data-stu-id="7bb44-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="7bb44-124">选择一个工作行，然后选择 **取消工作行** 打开一个对话框，可在其中部分或完全减少该工作行的数量。</span><span class="sxs-lookup"><span data-stu-id="7bb44-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="7bb44-125">调整数量。</span><span class="sxs-lookup"><span data-stu-id="7bb44-125">Adjust quantities.</span></span>
- <span data-ttu-id="7bb44-126">查看任何工作行后面的交易。</span><span class="sxs-lookup"><span data-stu-id="7bb44-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="7bb44-127">试用功能</span><span class="sxs-lookup"><span data-stu-id="7bb44-127">Try out the feature</span></span>

<span data-ttu-id="7bb44-128">此部分提供一个分三个部分的演示，该演示显示如何使用行详细信息。</span><span class="sxs-lookup"><span data-stu-id="7bb44-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="7bb44-129">提供示例数据</span><span class="sxs-lookup"><span data-stu-id="7bb44-129">Make sample data available</span></span>

<span data-ttu-id="7bb44-130">若要使用此处指定的示例记录和值完成此演示，使用的系统中必须已安装标准[演示数据](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="7bb44-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="7bb44-131">此外，开始前，还必须选择 **USMF** 法人。</span><span class="sxs-lookup"><span data-stu-id="7bb44-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="7bb44-132">使用生产系统时，也可以将此演示用作指导。</span><span class="sxs-lookup"><span data-stu-id="7bb44-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="7bb44-133">但是，必须替换为您自己的值，而您可能会缺少标准演示数据提供的某些类型的必需记录。</span><span class="sxs-lookup"><span data-stu-id="7bb44-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="7bb44-134">验证场景设置中包含足够的可用库存</span><span class="sxs-lookup"><span data-stu-id="7bb44-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="7bb44-135">如果要使用 **USMF** 演示数据，应该先确保已将系统设置为每个相关领料货位有足够的库存。</span><span class="sxs-lookup"><span data-stu-id="7bb44-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="7bb44-136">对于此演示，预计您有以下库存：</span><span class="sxs-lookup"><span data-stu-id="7bb44-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="7bb44-137">**物料 M9200：** 45 个。</span><span class="sxs-lookup"><span data-stu-id="7bb44-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="7bb44-138">（或更多）</span><span class="sxs-lookup"><span data-stu-id="7bb44-138">(or more)</span></span>
- <span data-ttu-id="7bb44-139">**物料 M9202：** 10 个。</span><span class="sxs-lookup"><span data-stu-id="7bb44-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="7bb44-140">（或更多）</span><span class="sxs-lookup"><span data-stu-id="7bb44-140">(or more)</span></span>

<span data-ttu-id="7bb44-141">执行以下步骤验证是否有足够库存，并进行所需的全部调整。</span><span class="sxs-lookup"><span data-stu-id="7bb44-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="7bb44-142">转到 **仓库管理 \> 设置 \> 货位指令**，然后确定哪些领料货位用于仓库 51 的销售订单领料。</span><span class="sxs-lookup"><span data-stu-id="7bb44-142">Go to **Warehouse management \> Setup \> Location directives**, and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="7bb44-143">（有关详细信息，请参阅[使用工作模板和货位指令控制仓库的工作](control-warehouse-location-directives.md)。）</span><span class="sxs-lookup"><span data-stu-id="7bb44-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="7bb44-144">检查相关货位的库存水平。</span><span class="sxs-lookup"><span data-stu-id="7bb44-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="7bb44-145">根据需要调整库存。</span><span class="sxs-lookup"><span data-stu-id="7bb44-145">Adjust inventory as required.</span></span> <span data-ttu-id="7bb44-146">可以创建手动移动，使用补货，或应用其他任何流以调整库存。</span><span class="sxs-lookup"><span data-stu-id="7bb44-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="7bb44-147">部分 1：创建领料工作</span><span class="sxs-lookup"><span data-stu-id="7bb44-147">Part 1: Create picking work</span></span>

<span data-ttu-id="7bb44-148">开始创建工作之前，请确保仓库设置为以预期方式响应工作请求。</span><span class="sxs-lookup"><span data-stu-id="7bb44-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="7bb44-149">执行以下步骤创建一些领料工作。</span><span class="sxs-lookup"><span data-stu-id="7bb44-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="7bb44-150">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="7bb44-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7bb44-151">选择 **新建** 以打开 **创建销售订单** 对话框。</span><span class="sxs-lookup"><span data-stu-id="7bb44-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="7bb44-152">在 **创建销售订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="7bb44-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7bb44-153">在 **客户** 快速选项卡上，将 **客户帐户** 字段设置为 _US-001_。</span><span class="sxs-lookup"><span data-stu-id="7bb44-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="7bb44-154">在 **常规** 快速选项卡上，将 **仓库** 字段设置为 _51_。</span><span class="sxs-lookup"><span data-stu-id="7bb44-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="7bb44-155">选择 **确定** 创建销售订单，然后关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="7bb44-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="7bb44-156">将打开您的新销售订单。</span><span class="sxs-lookup"><span data-stu-id="7bb44-156">Your new sales order is opened.</span></span> <span data-ttu-id="7bb44-157">将在 **销售订单行** 网格中添加一个新的空行。</span><span class="sxs-lookup"><span data-stu-id="7bb44-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="7bb44-158">在此订单行中设置以下值：</span><span class="sxs-lookup"><span data-stu-id="7bb44-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="7bb44-159">**物料编号：**_M9200_</span><span class="sxs-lookup"><span data-stu-id="7bb44-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="7bb44-160">**数量：** _20_</span><span class="sxs-lookup"><span data-stu-id="7bb44-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="7bb44-161">**单位：** _ea_</span><span class="sxs-lookup"><span data-stu-id="7bb44-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="7bb44-162">选择新订单行，然后在 **库存** 菜单中选择 **预留** 打开 **预留** 页。</span><span class="sxs-lookup"><span data-stu-id="7bb44-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="7bb44-163">在 **预留** 页中，选择 **预留批次** 在仓库中预留所选行的全部数量。</span><span class="sxs-lookup"><span data-stu-id="7bb44-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="7bb44-164">关闭 **预留** 页回到销售订单。</span><span class="sxs-lookup"><span data-stu-id="7bb44-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="7bb44-165">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="7bb44-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="7bb44-166">系统将创建一个装运，将其添加到新负荷，然后创建所需工作。</span><span class="sxs-lookup"><span data-stu-id="7bb44-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="7bb44-167">为用于第一个订单的相同客户帐户和仓库创建第二个销售订单。</span><span class="sxs-lookup"><span data-stu-id="7bb44-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="7bb44-168">将下面的两个订单行添加到此订单：</span><span class="sxs-lookup"><span data-stu-id="7bb44-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="7bb44-169">**行 1：** 将 **物料编号** 字段设置为 _M9200_，将 **数量** 字段设置为 _25_，将 **单位** 字段设置为 _个_。</span><span class="sxs-lookup"><span data-stu-id="7bb44-169">**Line 1:** Set the **Item number** field to _M9200_, the **Quantity** field to _25_, and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="7bb44-170">**行 2：** 将 **物料编号** 字段设置为 _M9202_，将 **数量** 字段设置为 _10_，将 **单位** 字段设置为 _个_。</span><span class="sxs-lookup"><span data-stu-id="7bb44-170">**Line 2:** Set the **Item number** field to _M9202_, the **Quantity** field to _10_, and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="7bb44-171">重复步骤 6 到 8 为每个订单行预留库存（一次一个），然后重复步骤 9 将订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="7bb44-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="7bb44-172">部分 2：更改工作行的货位</span><span class="sxs-lookup"><span data-stu-id="7bb44-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="7bb44-173">转到 **仓库管理 \> 工作 \> 工作行详细信息**。</span><span class="sxs-lookup"><span data-stu-id="7bb44-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="7bb44-174">找到并选择为此演示创建的一个工作行。</span><span class="sxs-lookup"><span data-stu-id="7bb44-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="7bb44-175">选择 **更改货位** 打开 **选择新货位** 对话框。</span><span class="sxs-lookup"><span data-stu-id="7bb44-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="7bb44-176">在 **选择新货位** 对话框的 **货位** 字段中，为工作行选择新货位。</span><span class="sxs-lookup"><span data-stu-id="7bb44-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="7bb44-177">选择 **确定** 应用更改并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="7bb44-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bb44-178">仅当新货位有足够多的可用库存（对于领料），或者通过了货位类型验证（对于放置），才可以提交货位更改。</span><span class="sxs-lookup"><span data-stu-id="7bb44-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="7bb44-179">部分 3：更改工作行的数量或取消工作行</span><span class="sxs-lookup"><span data-stu-id="7bb44-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="7bb44-180">转到 **仓库管理 \> 工作 \> 工作行详细信息**。</span><span class="sxs-lookup"><span data-stu-id="7bb44-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="7bb44-181">找到并选择为此演示创建的一个工作行。</span><span class="sxs-lookup"><span data-stu-id="7bb44-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="7bb44-182">请注意，只能取消或更改其中的工作类型为 _领料_ 的工作行的数量。</span><span class="sxs-lookup"><span data-stu-id="7bb44-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="7bb44-183">选择 **取消工作行** 打开 **要取消的数量** 对话框。</span><span class="sxs-lookup"><span data-stu-id="7bb44-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="7bb44-184">在 **要取消的数量** 对话框中，更改 **数量** 字段中的值以指定应该从当前为行指定的数量中 *扣除* 的数量。</span><span class="sxs-lookup"><span data-stu-id="7bb44-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="7bb44-185">默认情况下，**数量** 字段显示完整数量。</span><span class="sxs-lookup"><span data-stu-id="7bb44-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="7bb44-186">如果取消完整数量，**工作状态** 值将更改为 _已取消_，但是 **工作数量** 字段仍然显示原始值。</span><span class="sxs-lookup"><span data-stu-id="7bb44-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_, but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="7bb44-187">如果仅取消部分数量，**工作状态** 值将更新以显示新值，但是 **工作状态** 值不变。</span><span class="sxs-lookup"><span data-stu-id="7bb44-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="7bb44-188">选择 **确定** 应用更改并关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="7bb44-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bb44-189">如果仅取消工作行的部分数量，还必须从负荷行中删除过时数量。</span><span class="sxs-lookup"><span data-stu-id="7bb44-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="7bb44-190">不然，除非正确设置欠交，否则不会确认负荷行的装运。</span><span class="sxs-lookup"><span data-stu-id="7bb44-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>
