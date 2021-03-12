---
title: 领料行分组
description: 本主题概述领料行分组。
author: Mirzaab
manager: tfehr
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: e70244d46ec2787fefdb097d0354af7910b55e9c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989710"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="a7004-103">领料行分组</span><span class="sxs-lookup"><span data-stu-id="a7004-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7004-104">领料行分组可以将具有相同物料和位置的多个工作行合并为一个领料，来在移动设备上向用户显示。</span><span class="sxs-lookup"><span data-stu-id="a7004-104">Pick line grouping enables multiple work lines that have the same item and location to be combined into a single pick that is presented to the user on the mobile device.</span></span> <span data-ttu-id="a7004-105">因此，仓库工作人员可以收到最有效的指令，但仍可以在系统中维护所需的工作线分隔（针对不同的集装箱、订单等）。</span><span class="sxs-lookup"><span data-stu-id="a7004-105">Therefore, warehouse workers can receive the most efficient instructions, but required work line separation (for different containers, orders, and so on) can still be maintained in the system.</span></span>

## <a name="turn-on-the-pick-line-grouping-feature"></a><span data-ttu-id="a7004-106">打开领料行分组功能</span><span class="sxs-lookup"><span data-stu-id="a7004-106">Turn on the pick line grouping feature</span></span>

<span data-ttu-id="a7004-107">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="a7004-107">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="a7004-108">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查此功能的状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="a7004-108">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="a7004-109">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="a7004-109">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="a7004-110">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="a7004-110">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="a7004-111">**功能名称**：*领料行分组*</span><span class="sxs-lookup"><span data-stu-id="a7004-111">**Feature name:** *Pick line grouping*</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="a7004-112">设置领料行分组</span><span class="sxs-lookup"><span data-stu-id="a7004-112">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="a7004-113">创建移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="a7004-113">Create a mobile device menu item</span></span>

1. <span data-ttu-id="a7004-114">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="a7004-114">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a7004-115">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="a7004-115">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a7004-116">在 **菜单项名称** 字段中，输入 *销售组行领料*。</span><span class="sxs-lookup"><span data-stu-id="a7004-116">In the **Menu item name** field, enter *Sales group line picking*.</span></span>
1. <span data-ttu-id="a7004-117">在 **标题** 字段中，输入 *销售组行领料*。</span><span class="sxs-lookup"><span data-stu-id="a7004-117">In the **Title** field, enter *Sales group line picking*.</span></span> <span data-ttu-id="a7004-118">此标题将显示在移动设备菜单上。</span><span class="sxs-lookup"><span data-stu-id="a7004-118">This title will be shown on the mobile device menu.</span></span>
1. <span data-ttu-id="a7004-119">在 **模式** 字段中，选择 *工作*。</span><span class="sxs-lookup"><span data-stu-id="a7004-119">In the **Mode** field, select *Work*.</span></span>
1. <span data-ttu-id="a7004-120">将 **使用现有工作** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="a7004-120">Set the **Use existing work** option to *Yes*.</span></span>
1. <span data-ttu-id="a7004-121">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a7004-121">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="a7004-122">在 **导向方式** 字段中，选择 *用户导向*。</span><span class="sxs-lookup"><span data-stu-id="a7004-122">In the **Directed by** field, select *User directed*.</span></span>
    - <span data-ttu-id="a7004-123">将 **生成牌照** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="a7004-123">Set the **Generate license plate** option to *Yes*.</span></span>
    - <span data-ttu-id="a7004-124">将 **组领料** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="a7004-124">Set the **Group pick** option to *Yes*.</span></span>
    - <span data-ttu-id="a7004-125">其余选项接受默认值。</span><span class="sxs-lookup"><span data-stu-id="a7004-125">Accept the default values for the remaining options.</span></span>

1. <span data-ttu-id="a7004-126">按照以下步骤为移动设备菜单项配置有效的工作类：</span><span class="sxs-lookup"><span data-stu-id="a7004-126">Follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="a7004-127">在 **工作类** 快速选项卡上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="a7004-127">On the **Work classes** FastTab, elect **New**.</span></span>
    2. <span data-ttu-id="a7004-128">在 **工作类 ID** 字段中，您可以选择 *销售* 或 *SO 领料*，具体取决于您要使用的仓库。</span><span class="sxs-lookup"><span data-stu-id="a7004-128">In the **Work class ID** field, you can select either *Sales* or *SO Pick*, depending on the warehouse that you will use.</span></span> <span data-ttu-id="a7004-129">对于此场景，选择 *SO 领料*。</span><span class="sxs-lookup"><span data-stu-id="a7004-129">For this scenario, select *SO Pick*.</span></span>

        <span data-ttu-id="a7004-130">**工作订单类型** 字段将自动设置为 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="a7004-130">The **Work order type** field is automatically set to *Sales orders*.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="a7004-131">设置移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="a7004-131">Set up a mobile device menu</span></span>

<span data-ttu-id="a7004-132">请按照以下步骤将刚才创建的菜单项添加到 **出站** 菜单。</span><span class="sxs-lookup"><span data-stu-id="a7004-132">Follow these steps to add the menu item that you just created to the **Outbound** menu.</span></span>

1. <span data-ttu-id="a7004-133">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="a7004-133">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="a7004-134">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="a7004-134">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a7004-135">列表窗格显示所有现有的移动设备菜单。</span><span class="sxs-lookup"><span data-stu-id="a7004-135">The list pane shows all existing mobile device menus.</span></span> <span data-ttu-id="a7004-136">在列表中选择 *出站*。</span><span class="sxs-lookup"><span data-stu-id="a7004-136">Select *Outbound* in the list.</span></span>
1. <span data-ttu-id="a7004-137">在 **可用菜单和菜单项** 网格中，找到并选择您创建的 *销售组行领料* 菜单项。</span><span class="sxs-lookup"><span data-stu-id="a7004-137">In the **Available menus and menu items** list, find and select the *Sales group line picking* menu item that you created.</span></span>
1. <span data-ttu-id="a7004-138">选择向右箭头按钮将 *销售组行领料* 菜单项移到 **菜单结构** 列表。</span><span class="sxs-lookup"><span data-stu-id="a7004-138">Select the right arrow button to move the *Sales group line picking* menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="a7004-139">使用向上箭头和向下箭头按钮将菜单项移到菜单结构中的所需位置。</span><span class="sxs-lookup"><span data-stu-id="a7004-139">Use the up arrow and down arrow buttons to move the menu item into the desired position in the menu structure.</span></span>
1. <span data-ttu-id="a7004-140">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a7004-140">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="a7004-141">设置工作模板</span><span class="sxs-lookup"><span data-stu-id="a7004-141">Set up a work template</span></span>

1. <span data-ttu-id="a7004-142">转到 **仓库管理 \> 设置 \> 工作 \> 工作模板**。</span><span class="sxs-lookup"><span data-stu-id="a7004-142">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a7004-143">在 **工作订单类型** 字段中，选择 *销售订单*。</span><span class="sxs-lookup"><span data-stu-id="a7004-143">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="a7004-144">在 **概览** 网格中，找到并选择此功能应使用的工作模板。</span><span class="sxs-lookup"><span data-stu-id="a7004-144">In the **Overview** grid, find and select the work template that should be used with this function.</span></span> <span data-ttu-id="a7004-145">对于此场景，选择 *51 领料到暂存位置* 模板。</span><span class="sxs-lookup"><span data-stu-id="a7004-145">For this scenario, select the *51 Pick to stage* template.</span></span>
1. <span data-ttu-id="a7004-146">在操作窗格上，选择 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="a7004-146">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="a7004-147">在查询编辑器对话框的 **分类** 选项卡上，选择 **添加**，然后为新行设置以下值：</span><span class="sxs-lookup"><span data-stu-id="a7004-147">In the query editor dialog box, on the **Sorting** tab, select **Add**, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="a7004-148">在 **表** 列中，选择 *临时工作交易记录*。</span><span class="sxs-lookup"><span data-stu-id="a7004-148">In the **Table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="a7004-149">在 **派生表** 列中，选择 *临时工作交易记录*。</span><span class="sxs-lookup"><span data-stu-id="a7004-149">In the **Derived table** column, select *Temporary work transactions*.</span></span>
    - <span data-ttu-id="a7004-150">在 **字段** 列中，选择 *物料编号*。</span><span class="sxs-lookup"><span data-stu-id="a7004-150">In the **Field** column, select *Item number*.</span></span>
    - <span data-ttu-id="a7004-151">在 **搜索方向** 列中，选择 *升序*。</span><span class="sxs-lookup"><span data-stu-id="a7004-151">In the **Search direction** column, select *Ascending*.</span></span>

1. <span data-ttu-id="a7004-152">选择 **确定** 关闭对话框并保存您的选择。</span><span class="sxs-lookup"><span data-stu-id="a7004-152">Select **OK** to close the dialog box and save your selection.</span></span>
1. <span data-ttu-id="a7004-153">您将收到以下消息：“分组将重置，是否继续？”</span><span class="sxs-lookup"><span data-stu-id="a7004-153">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="a7004-154">选择 **是** 继续。</span><span class="sxs-lookup"><span data-stu-id="a7004-154">Select **Yes** to continue.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a7004-155">为了使领料行分组功能正常工作，必须按物料 ID 对工作行进行排序。</span><span class="sxs-lookup"><span data-stu-id="a7004-155">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="a7004-156">如果具有相同物料的行没有逐个排序，将不会对它们分组。</span><span class="sxs-lookup"><span data-stu-id="a7004-156">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="a7004-157">示例</span><span class="sxs-lookup"><span data-stu-id="a7004-157">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="a7004-158">创建领料工作</span><span class="sxs-lookup"><span data-stu-id="a7004-158">Create picking work</span></span>

<span data-ttu-id="a7004-159">您必须先创建一些合格的出货工作，然后才能设置领料行分组。</span><span class="sxs-lookup"><span data-stu-id="a7004-159">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="a7004-160">转到 **销售和营销 \> 销售订单 \> 所有销售订单**。</span><span class="sxs-lookup"><span data-stu-id="a7004-160">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a7004-161">选择 **新建** 以创建新的销售订单。</span><span class="sxs-lookup"><span data-stu-id="a7004-161">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="a7004-162">在 **客户帐户** 字段中选择 *US-004*。</span><span class="sxs-lookup"><span data-stu-id="a7004-162">In the **Customer account** field, select *US-004*.</span></span>
1. <span data-ttu-id="a7004-163">在 **常规** 快速选项卡上的 **仓库** 字段中，选择 *51*。</span><span class="sxs-lookup"><span data-stu-id="a7004-163">On the **General** FastTab, in the **Warehouse** field, select *51*.</span></span>
1. <span data-ttu-id="a7004-164">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="a7004-164">Select **OK**.</span></span>
1. <span data-ttu-id="a7004-165">在 **销售订单行** 快速选项卡上，添加以下六行：</span><span class="sxs-lookup"><span data-stu-id="a7004-165">On the **Sales order lines** FastTab, add the following six lines:</span></span>

    - <span data-ttu-id="a7004-166">**行 1：** 在 **物料编号** 字段中，选择 *M9200*。</span><span class="sxs-lookup"><span data-stu-id="a7004-166">**Line 1:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="a7004-167">在 **数量** 字段中，输入 *3*。</span><span class="sxs-lookup"><span data-stu-id="a7004-167">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="a7004-168">**行 2：** 在 **物料编号** 字段中，选择 *M9201*。</span><span class="sxs-lookup"><span data-stu-id="a7004-168">**Line 2:** In the **Item number** field, select *M9201*.</span></span> <span data-ttu-id="a7004-169">在 **数量** 字段中，输入 *3*。</span><span class="sxs-lookup"><span data-stu-id="a7004-169">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="a7004-170">**行 3：** 在 **物料编号** 字段中，选择 *M9202*。</span><span class="sxs-lookup"><span data-stu-id="a7004-170">**Line 3:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="a7004-171">在 **数量** 字段中，输入 *2*。</span><span class="sxs-lookup"><span data-stu-id="a7004-171">In the **Quantity** field, enter *2*.</span></span>
    - <span data-ttu-id="a7004-172">**行 4：** 在 **物料编号** 字段中，选择 *M9200*。</span><span class="sxs-lookup"><span data-stu-id="a7004-172">**Line 4:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="a7004-173">在 **数量** 字段中，输入 *1*。</span><span class="sxs-lookup"><span data-stu-id="a7004-173">In the **Quantity** field, enter *1*.</span></span>
    - <span data-ttu-id="a7004-174">**行 5：** 在 **物料编号** 字段中，选择 *M9200*。</span><span class="sxs-lookup"><span data-stu-id="a7004-174">**Line 5:** In the **Item number** field, select *M9200*.</span></span> <span data-ttu-id="a7004-175">在 **数量** 字段中，输入 *3*。</span><span class="sxs-lookup"><span data-stu-id="a7004-175">In the **Quantity** field, enter *3*.</span></span>
    - <span data-ttu-id="a7004-176">**行 6：** 在 **物料编号** 字段中，选择 *M9202*。</span><span class="sxs-lookup"><span data-stu-id="a7004-176">**Line 6:** In the **Item number** field, select *M9202*.</span></span> <span data-ttu-id="a7004-177">在 **数量** 字段中，输入 *7*。</span><span class="sxs-lookup"><span data-stu-id="a7004-177">In the **Quantity** field, enter *7*.</span></span>

    <span data-ttu-id="a7004-178">以下是每个物料的总数量的汇总：</span><span class="sxs-lookup"><span data-stu-id="a7004-178">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="a7004-179">**物料 M9200：** 各 *7*</span><span class="sxs-lookup"><span data-stu-id="a7004-179">**Item M9200:** *7* each</span></span>
    - <span data-ttu-id="a7004-180">**物料 M9201：** 各 *3*</span><span class="sxs-lookup"><span data-stu-id="a7004-180">**Item M9201:** *3* each</span></span>
    - <span data-ttu-id="a7004-181">**物料 M9202：** 各 *9*</span><span class="sxs-lookup"><span data-stu-id="a7004-181">**Item M9202:** *9* each</span></span>

1. <span data-ttu-id="a7004-182">在将订单下达到仓库之前，必须确保领料库位有满足所有订单上的所有物料的足够库存。</span><span class="sxs-lookup"><span data-stu-id="a7004-182">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="a7004-183">查看 **库位指令** 设置，确定用于销售订单领料的领料库位。</span><span class="sxs-lookup"><span data-stu-id="a7004-183">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span> <span data-ttu-id="a7004-184">如果您将 Contoso 演示数据环境用于仓库 *51*，请确认有可用库存。</span><span class="sxs-lookup"><span data-stu-id="a7004-184">If you're using the Contoso demo data environment for warehouse *51*, confirm that there is available inventory.</span></span>

    <span data-ttu-id="a7004-185">现在，您必须为每个行预留库存。</span><span class="sxs-lookup"><span data-stu-id="a7004-185">You must now reserve the inventory for each line.</span></span>

1. <span data-ttu-id="a7004-186">在 **销售订单行** 快速选项卡上，选择必须预留的行之一。</span><span class="sxs-lookup"><span data-stu-id="a7004-186">On the **Sales order lines** FastTab, select one of the lines that must be reserved.</span></span>
1. <span data-ttu-id="a7004-187">在网格上方的 **库存** 菜单中，选择 **预留**。</span><span class="sxs-lookup"><span data-stu-id="a7004-187">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="a7004-188">在 **预留** 页的操作窗格中，选择 **预留批次** 应用预留。</span><span class="sxs-lookup"><span data-stu-id="a7004-188">On the **Reservation** page, on the Action Pane, select **Reserve lot** to apply the reservation.</span></span> <span data-ttu-id="a7004-189">然后关闭页面。</span><span class="sxs-lookup"><span data-stu-id="a7004-189">Then close the page.</span></span>
1. <span data-ttu-id="a7004-190">对必须预留的其余行重复步骤 8 到 10。</span><span class="sxs-lookup"><span data-stu-id="a7004-190">Repeat steps 8 through 10 for the remaining lines that must be reserved.</span></span>

    <span data-ttu-id="a7004-191">现在您必须将销售订单下达到仓库。</span><span class="sxs-lookup"><span data-stu-id="a7004-191">You must now release the sales order to the warehouse.</span></span>

1. <span data-ttu-id="a7004-192">在“操作窗格”上的 **仓库** 选项卡上，选择 **发放到仓库**。</span><span class="sxs-lookup"><span data-stu-id="a7004-192">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a7004-193">您将收到一条消息，指示已创建装运和波次，且波次已经提交以在批处理中运行。</span><span class="sxs-lookup"><span data-stu-id="a7004-193">You receive a message that states that a shipment and a wave have been created, and that the wave has been submitted to run in a batch.</span></span>

    <span data-ttu-id="a7004-194">在波次和所有下游作业完成后，将为具有六行的工作创建工作 ID。</span><span class="sxs-lookup"><span data-stu-id="a7004-194">When the wave and all downstream jobs have been completed, a work ID is created for work that has six lines.</span></span> <span data-ttu-id="a7004-195">这些行按物料编号排序。</span><span class="sxs-lookup"><span data-stu-id="a7004-195">The lines are sorted by item number.</span></span>

1. <span data-ttu-id="a7004-196">转到 **仓库管理 \> 工作 \> 所有工作** 查看创建的工作。</span><span class="sxs-lookup"><span data-stu-id="a7004-196">Go to **Warehouse management \> Work \> All work** to view the work that was created.</span></span> <span data-ttu-id="a7004-197">记下 **工作 ID** 值，因为您在下一个过程中需要用到。</span><span class="sxs-lookup"><span data-stu-id="a7004-197">Make a note of the **Work ID** value, because you will need it in the next procedure.</span></span>

### <a name="initiate-picking-from-the-mobile-device"></a><span data-ttu-id="a7004-198">从移动设备启动领料</span><span class="sxs-lookup"><span data-stu-id="a7004-198">Initiate picking from the mobile device</span></span>

1. <span data-ttu-id="a7004-199">以为仓库 *51* 设置的用户身份登录到移动设备。</span><span class="sxs-lookup"><span data-stu-id="a7004-199">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="a7004-200">在移动设备上，选择包含新的移动设备菜单项的菜单。</span><span class="sxs-lookup"><span data-stu-id="a7004-200">On the mobile device, select the menu that includes the new mobile device menu item.</span></span> <span data-ttu-id="a7004-201">对于此场景，选择 **出站**。</span><span class="sxs-lookup"><span data-stu-id="a7004-201">For this scenario, select **Outbound**.</span></span>
1. <span data-ttu-id="a7004-202">选择 **销售组行领料** 菜单项来启动领料。</span><span class="sxs-lookup"><span data-stu-id="a7004-202">Select the **Sales group line picking** menu item to initiate the pick.</span></span>
1. <span data-ttu-id="a7004-203">输入您在上一过程中记下的 **工作 ID** 值。</span><span class="sxs-lookup"><span data-stu-id="a7004-203">Enter the **Work ID** value that you made a note of in the previous procedure.</span></span>

    <span data-ttu-id="a7004-204">您应该会看到一个领料步骤，其中将物料 *M9200* 的所有领料行分组，并且应该会收到一条为每个 *M9200* 物料领取 *7* 的指令。</span><span class="sxs-lookup"><span data-stu-id="a7004-204">You should see a pick step where all pick lines for item *M9200* are grouped, and you should receive an instruction to pick *7* each of item *M9200*.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="a7004-205">在移动设备上，三个领料工作行的领料工作已聚合到用户的一个领料步骤。</span><span class="sxs-lookup"><span data-stu-id="a7004-205">On the mobile device, the pick work for the three pick work lines has been aggregated into one picking step for the user.</span></span>

1. <span data-ttu-id="a7004-206">确认领料步骤。</span><span class="sxs-lookup"><span data-stu-id="a7004-206">Confirm the pick step.</span></span>
1. <span data-ttu-id="a7004-207">转到工作 ID 的工作页，注意物料 *M9200* 的所有三个领料行已同时关闭。</span><span class="sxs-lookup"><span data-stu-id="a7004-207">Go to the work page for the work ID, and notice that all three pick lines for item *M9200* were closed simultaneously.</span></span>
1. <span data-ttu-id="a7004-208">返回到移动设备，继续领料。</span><span class="sxs-lookup"><span data-stu-id="a7004-208">Go back to the mobile device, and continue to pick.</span></span> <span data-ttu-id="a7004-209">物料 *M9201* 的工作行 4 应该显示。</span><span class="sxs-lookup"><span data-stu-id="a7004-209">Work line 4 for item *M9201* should be presented.</span></span> <span data-ttu-id="a7004-210">因为订单上只有一个工作行，所以没有要聚合的内容。</span><span class="sxs-lookup"><span data-stu-id="a7004-210">Because there was only one work line on the order, there is nothing to aggregate.</span></span>
1. <span data-ttu-id="a7004-211">确认领料步骤。</span><span class="sxs-lookup"><span data-stu-id="a7004-211">Confirm the pick step.</span></span>
1. <span data-ttu-id="a7004-212">移动设备上的最后一个领料步骤聚合了工作订单的最后两个领料行。</span><span class="sxs-lookup"><span data-stu-id="a7004-212">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>
1. <span data-ttu-id="a7004-213">完成每个 *M9202* 物料领取 *9* 的领料步骤。</span><span class="sxs-lookup"><span data-stu-id="a7004-213">Complete the pick step for *9* each of item *M9202*.</span></span>
1. <span data-ttu-id="a7004-214">确认放置步骤以及所有其他领料/放置对以完成工作。</span><span class="sxs-lookup"><span data-stu-id="a7004-214">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!IMPORTANT]
>
> - <span data-ttu-id="a7004-215">只有处于序列中时工作行才会被分组。</span><span class="sxs-lookup"><span data-stu-id="a7004-215">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="a7004-216">不支持以下功能：</span><span class="sxs-lookup"><span data-stu-id="a7004-216">The following functionality isn't supported:</span></span>
>
>   - <span data-ttu-id="a7004-217">实际称重物料</span><span class="sxs-lookup"><span data-stu-id="a7004-217">Catch-weight items</span></span>
>
>    <span data-ttu-id="a7004-218">如果工作中有任何实际称重物料，在开始领料之前您会收到一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="a7004-218">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>
>   - <span data-ttu-id="a7004-219">单件领料</span><span class="sxs-lookup"><span data-stu-id="a7004-219">Piece picking</span></span>
>   - <span data-ttu-id="a7004-220">有未完成的补货工作的工作行</span><span class="sxs-lookup"><span data-stu-id="a7004-220">Work lines that have unfinished replenishment work</span></span>
>   - <span data-ttu-id="a7004-221">过量领料</span><span class="sxs-lookup"><span data-stu-id="a7004-221">Over-picking</span></span>
>   - <span data-ttu-id="a7004-222">物料重新分配的领料短缺</span><span class="sxs-lookup"><span data-stu-id="a7004-222">Short picking with item reallocation</span></span>
