---
title: 货位产品维度混合
description: 此主题提供有关货位产品维度混合的信息。 在使用具有维度的产品变型或产品（如在时尚行业中）时，货位模板功能有助于改善货位管理。 其让您决定是混合特定货位模板的配置、颜色、样式和尺寸，还是只能将这些维度中的一个或其组合放入同一个货位。
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: b0309c7a7240d7cac9e5b5724a028f2dc70199e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217021"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="b9a14-105">货位产品维度混合</span><span class="sxs-lookup"><span data-stu-id="b9a14-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9a14-106">货位产品管理混合功能是一项货位模板功能，在使用具有维度的产品变型或产品（如在时尚行业中）时，该功能有助于改善货位管理。</span><span class="sxs-lookup"><span data-stu-id="b9a14-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="b9a14-107">其让您决定是混合特定货位模板的配置、颜色、样式和尺寸，还是只能将这些维度中的一个或其组合放入同一个货位。</span><span class="sxs-lookup"><span data-stu-id="b9a14-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="b9a14-108">开启“货位产品维度混合”功能</span><span class="sxs-lookup"><span data-stu-id="b9a14-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="b9a14-109">货位产品维度功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="b9a14-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="b9a14-110">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="b9a14-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b9a14-111">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="b9a14-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b9a14-112">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="b9a14-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b9a14-113">**功能名称**：*货位产品维度混合*</span><span class="sxs-lookup"><span data-stu-id="b9a14-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="b9a14-114">设置</span><span class="sxs-lookup"><span data-stu-id="b9a14-114">Setup</span></span>

<span data-ttu-id="b9a14-115">仓库中的每个货位都需要关联一个货位模板，用于描述货位的属性。</span><span class="sxs-lookup"><span data-stu-id="b9a14-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="b9a14-116">因此，设置产品维度混合功能后，使用同一个货位模板的所有货位都可以允许使用该功能。</span><span class="sxs-lookup"><span data-stu-id="b9a14-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="b9a14-117">将货位模板配置为允许产品维度混合功能</span><span class="sxs-lookup"><span data-stu-id="b9a14-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="b9a14-118">转到 **仓库管理 \> 设置 \> 仓库 \> 货位模板**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="b9a14-119">在货位模板列表中，选择 **BULK**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="b9a14-120">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b9a14-121">在 **常规** 快速选项卡上，将 **启用货位产品维度特定混合功能** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b9a14-122">仅当 **允许混合物料** 选项设置为 *否*，才能将此选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="b9a14-123">在 **允许的产品维度混合** 快速选项卡上，将 **尺寸** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="b9a14-124">在本主题介绍的场景中，只能对具有不同 **尺寸** 维度的产品使用混合功能。</span><span class="sxs-lookup"><span data-stu-id="b9a14-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="b9a14-125">但是，也提供了其他选项。</span><span class="sxs-lookup"><span data-stu-id="b9a14-125">However, other options are also available.</span></span>
1. <span data-ttu-id="b9a14-126">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="b9a14-127">创建新基础产品和产品变型</span><span class="sxs-lookup"><span data-stu-id="b9a14-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="b9a14-128">转到 **产品信息管理 \> 产品 \> 基础产品**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="b9a14-129">在“操作窗格”中，选择 **新建** 创建基础产品。</span><span class="sxs-lookup"><span data-stu-id="b9a14-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="b9a14-130">在 **新产品** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b9a14-131">**产品类型**：*物料*</span><span class="sxs-lookup"><span data-stu-id="b9a14-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="b9a14-132">**产品子类型**：*基础产品*</span><span class="sxs-lookup"><span data-stu-id="b9a14-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="b9a14-133">**产品编号**：*B0001*</span><span class="sxs-lookup"><span data-stu-id="b9a14-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="b9a14-134">**产品名称**：*B0001 尺寸*</span><span class="sxs-lookup"><span data-stu-id="b9a14-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="b9a14-135">**产品维度组**：*尺寸*</span><span class="sxs-lookup"><span data-stu-id="b9a14-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="b9a14-136">**配置技术**：*预定义的变型*</span><span class="sxs-lookup"><span data-stu-id="b9a14-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="b9a14-137">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-137">Select **OK**.</span></span>
1. <span data-ttu-id="b9a14-138">在 **产品详细信息** 页的 **常规** 快速选项卡，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b9a14-139">**自动生成变型**：*是*</span><span class="sxs-lookup"><span data-stu-id="b9a14-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="b9a14-140">**尺寸组**：*CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="b9a14-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="b9a14-141">若要查看预定义的变型，请在操作窗格上选择 **产品变型**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="b9a14-142">将显示 **产品变型** 页面，其中显示尺寸组配置中的变型列表。</span><span class="sxs-lookup"><span data-stu-id="b9a14-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="b9a14-143">将产品发布到 USMF 公司</span><span class="sxs-lookup"><span data-stu-id="b9a14-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="b9a14-144">在操作窗格上，选择 **发布产品**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="b9a14-145">在 **选择要发布的产品** 页上，确认列表中包含产品编号 *B0001*，然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="b9a14-146">选择 **下一步** 确认要发布的产品变型。</span><span class="sxs-lookup"><span data-stu-id="b9a14-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="b9a14-147">在 **选择要发布到的公司** 页面上，选择 *USMF*，然后选择 **下一步** 确认选择。</span><span class="sxs-lookup"><span data-stu-id="b9a14-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="b9a14-148">在 **确认选择** 页面上，选择 **完成** 完成发布。</span><span class="sxs-lookup"><span data-stu-id="b9a14-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="b9a14-149">将收到“操作已完成”消息。</span><span class="sxs-lookup"><span data-stu-id="b9a14-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="b9a14-150">更新 USMF 公司中的已发布产品</span><span class="sxs-lookup"><span data-stu-id="b9a14-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="b9a14-151">确保已登录 **USMF** 公司。</span><span class="sxs-lookup"><span data-stu-id="b9a14-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="b9a14-152">转到 **产品信息管理 \> 产品 \> 已发布产品** 完成已发布产品的创建。</span><span class="sxs-lookup"><span data-stu-id="b9a14-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="b9a14-153">找到并选择物料编号 *B0001* 打开 **已发布产品详细信息** 页面。</span><span class="sxs-lookup"><span data-stu-id="b9a14-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="b9a14-154">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b9a14-155">在 **常规** 快速选项卡上，确保 **物料模型组** 字段设置为 *FIFO*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="b9a14-156">在操作窗格的 **产品** 选项卡的 **设置** 组中，选择 **维度组**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="b9a14-157">设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-157">Set the following values:</span></span>

    - <span data-ttu-id="b9a14-158">**存储维度组**：*仓库*</span><span class="sxs-lookup"><span data-stu-id="b9a14-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="b9a14-159">**跟踪维度组**：*无*</span><span class="sxs-lookup"><span data-stu-id="b9a14-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="b9a14-160">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-160">Select **OK**.</span></span>
1. <span data-ttu-id="b9a14-161">在操作窗格的 **产品** 选项卡的 **设置** 组中，选择 **预留层次结构**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="b9a14-162">将 **预留层次结构** 字段设置为 *默认*，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="b9a14-163">在 **常规** 快速选项卡的 **管理** 部分中，注意已更新了您的选择。</span><span class="sxs-lookup"><span data-stu-id="b9a14-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="b9a14-164">在 **采购** 快速选项卡的 **价格** 字段中，输入 *10*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="b9a14-165">在 **管理成本** 快速选项卡上 **物料组** 字段中，选择 *音频*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="b9a14-166">在 **采购** 快速选项卡的 **价格** 字段中，输入 *10*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="b9a14-167">在 **仓库** 快速选项卡的 **单位序列组 ID** 字段中，输入 *个*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="b9a14-168">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="b9a14-169">创建地址指令</span><span class="sxs-lookup"><span data-stu-id="b9a14-169">Create a location directive</span></span>

1. <span data-ttu-id="b9a14-170">转到 **库存管理 \> 设置 \> 位置指令**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="b9a14-171">在左窗格的 **工作订单类型** 字段中，选择 *采购订单*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="b9a14-172">在列表中，选择名为 *24 PO Direct* 的货位指令。</span><span class="sxs-lookup"><span data-stu-id="b9a14-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="b9a14-173">在 **货位指令操作** 快速选项卡上，选择 **新建** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b9a14-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="b9a14-174">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b9a14-175">**序列号**：*1*</span><span class="sxs-lookup"><span data-stu-id="b9a14-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="b9a14-176">新行应该在之前的现有行的前面。</span><span class="sxs-lookup"><span data-stu-id="b9a14-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="b9a14-177">若要进行更改，请使用工具栏上的 **上移** 和 **下移** 按钮，或将现有行的 **序列号** 值更改为 *2*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="b9a14-178">**名称**：*放入 BULK 货位模板*</span><span class="sxs-lookup"><span data-stu-id="b9a14-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="b9a14-179">**固定货位使用情况**：*固定货位和非固定货位*</span><span class="sxs-lookup"><span data-stu-id="b9a14-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="b9a14-180">**允许负库存**：*清除此复选框（= 否）*</span><span class="sxs-lookup"><span data-stu-id="b9a14-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="b9a14-181">**批处理已启用**：*清除此复选框（= 否）*</span><span class="sxs-lookup"><span data-stu-id="b9a14-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="b9a14-182">**策略**：*无*</span><span class="sxs-lookup"><span data-stu-id="b9a14-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="b9a14-183">在新行仍处于选中状态的情况下，选择网格上方的 **编辑查询**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="b9a14-184">在产品查询对话框的 **范围** 选项卡中，选择 **添加** 向网格添加一行。</span><span class="sxs-lookup"><span data-stu-id="b9a14-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="b9a14-185">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b9a14-186">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="b9a14-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="b9a14-187">**派生表**：*货位*</span><span class="sxs-lookup"><span data-stu-id="b9a14-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="b9a14-188">\**字段：\*\*\*位置模板 ID*</span><span class="sxs-lookup"><span data-stu-id="b9a14-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="b9a14-189">**条件：** *BULK*</span><span class="sxs-lookup"><span data-stu-id="b9a14-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="b9a14-190">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-190">Select **OK**.</span></span>
1. <span data-ttu-id="b9a14-191">在 **货位指令** 页的操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="b9a14-192">如果您在 **货位指令操作** 快速选项卡上的 **策略** 字段中使用使用 *合并* 货位策略，将覆盖对 **货位模板** 上 **允许的产品维度混合** 快速选项卡的设置，并将物料放入同一个货位，即使设置不允许此行为也不例外。</span><span class="sxs-lookup"><span data-stu-id="b9a14-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="b9a14-193">创建移动设备菜单项</span><span class="sxs-lookup"><span data-stu-id="b9a14-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="b9a14-194">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="b9a14-195">在操作窗格上，选择 **新建** 创建用于排序的菜单项。</span><span class="sxs-lookup"><span data-stu-id="b9a14-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="b9a14-196">在标题中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="b9a14-197">**菜单项名称**：*PO 行收货*</span><span class="sxs-lookup"><span data-stu-id="b9a14-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="b9a14-198">**标题**：*PO 行收货*</span><span class="sxs-lookup"><span data-stu-id="b9a14-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="b9a14-199">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="b9a14-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="b9a14-200">**使用现有工作**：*否*</span><span class="sxs-lookup"><span data-stu-id="b9a14-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="b9a14-201">在 **常规** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b9a14-202">**工作创建流程**：*采购订单行收货和储存*</span><span class="sxs-lookup"><span data-stu-id="b9a14-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="b9a14-203">\**生成牌照：\*\*\*是*</span><span class="sxs-lookup"><span data-stu-id="b9a14-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="b9a14-204">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="b9a14-205">配置移动设备菜单</span><span class="sxs-lookup"><span data-stu-id="b9a14-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="b9a14-206">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="b9a14-207">在菜单列表中，选择 **入库**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="b9a14-208">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="b9a14-209">在 **可用菜单和菜单项** 列表中，找到并选择 **PO 行收货** 菜单项。</span><span class="sxs-lookup"><span data-stu-id="b9a14-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="b9a14-210">选择向右箭头按钮将 **PO 行收货** 菜单项移到 **菜单结构** 列表。</span><span class="sxs-lookup"><span data-stu-id="b9a14-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="b9a14-211">这样就把新菜单项添加到了所选菜单。</span><span class="sxs-lookup"><span data-stu-id="b9a14-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="b9a14-212">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="b9a14-213">应用场景</span><span class="sxs-lookup"><span data-stu-id="b9a14-213">Scenario</span></span>

<span data-ttu-id="b9a14-214">从演示创建显示如果货位模板不允许混合物料，但是已启用 *货位产品维度混合功能*，如何将不同产品变型放到同一个货位。</span><span class="sxs-lookup"><span data-stu-id="b9a14-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="b9a14-215">在此示例中，将使用 **尺寸** 变型作为条件。</span><span class="sxs-lookup"><span data-stu-id="b9a14-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="b9a14-216">首先，确保仓库 *24* 中有空货位在使用 *BULK* 货位模板。</span><span class="sxs-lookup"><span data-stu-id="b9a14-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="b9a14-217">创建采购订单</span><span class="sxs-lookup"><span data-stu-id="b9a14-217">Create a purchase order</span></span>

<span data-ttu-id="b9a14-218">将创建一个包含三行的采购订单：两行针对产品编号相同，但 **尺寸** 变型不同的产品，第三行针对另一个无变型的产品。</span><span class="sxs-lookup"><span data-stu-id="b9a14-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="b9a14-219">转到 **应付帐款 \> 采购订单 \> 所有采购订单**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="b9a14-220">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="b9a14-221">在 **创建采购订单** 对话框中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b9a14-222">**供应商帐户**：*1001*</span><span class="sxs-lookup"><span data-stu-id="b9a14-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="b9a14-223">**仓库**：*24*</span><span class="sxs-lookup"><span data-stu-id="b9a14-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="b9a14-224">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-224">Select **OK**.</span></span>
1. <span data-ttu-id="b9a14-225">将创建采购订单，并在 **采购订单行** 快速选项卡上创建一个新行。</span><span class="sxs-lookup"><span data-stu-id="b9a14-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="b9a14-226">记下采购订单编号。</span><span class="sxs-lookup"><span data-stu-id="b9a14-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="b9a14-227">在新行中，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="b9a14-228">\**物料编号：\*\*\*B0001*</span><span class="sxs-lookup"><span data-stu-id="b9a14-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="b9a14-229">**尺寸** *L*</span><span class="sxs-lookup"><span data-stu-id="b9a14-229">**Size** *L*</span></span>
    - <span data-ttu-id="b9a14-230">**数量：** *2*</span><span class="sxs-lookup"><span data-stu-id="b9a14-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="b9a14-231">选择网格上方的 **添加行** 添加第二个采购订单行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="b9a14-232">\**物料编号：\*\*\*B0001*</span><span class="sxs-lookup"><span data-stu-id="b9a14-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="b9a14-233">**尺寸** *XL*</span><span class="sxs-lookup"><span data-stu-id="b9a14-233">**Size** *XL*</span></span>
    - <span data-ttu-id="b9a14-234">**数量：** *2*</span><span class="sxs-lookup"><span data-stu-id="b9a14-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="b9a14-235">选择 **添加行** 添加第三个采购订单行，然后设置以下值：</span><span class="sxs-lookup"><span data-stu-id="b9a14-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="b9a14-236">\**物料编号：\*\*\*A0001*</span><span class="sxs-lookup"><span data-stu-id="b9a14-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="b9a14-237">**数量：** *1*</span><span class="sxs-lookup"><span data-stu-id="b9a14-237">**Quantity:** *1*</span></span>

<span data-ttu-id="b9a14-238">1. 选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="b9a14-239">在仓库应用中接收采购订单行</span><span class="sxs-lookup"><span data-stu-id="b9a14-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="b9a14-240">以已经为仓库 *24* 启用的用户的身份登录仓库应用。</span><span class="sxs-lookup"><span data-stu-id="b9a14-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="b9a14-241">选择 **入库** 菜单。</span><span class="sxs-lookup"><span data-stu-id="b9a14-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="b9a14-242">选择 **PO 行收货**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="b9a14-243">选择 **PONUM** 字段，然后输入采购订单编号。</span><span class="sxs-lookup"><span data-stu-id="b9a14-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="b9a14-244">通过选择页面底部的确认按钮 ( ✔ ) 确认输入。</span><span class="sxs-lookup"><span data-stu-id="b9a14-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="b9a14-245">输入正在收货的采购订单中的行号。</span><span class="sxs-lookup"><span data-stu-id="b9a14-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="b9a14-246">选择 **LINENUM** 字段，然后使用数字小键盘输入 *1*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="b9a14-247">确认您的输入。</span><span class="sxs-lookup"><span data-stu-id="b9a14-247">Confirm your entry.</span></span>
1. <span data-ttu-id="b9a14-248">输入要收货的数量。</span><span class="sxs-lookup"><span data-stu-id="b9a14-248">Enter the quantity to receive.</span></span> <span data-ttu-id="b9a14-249">选择加号 (**+**) 按钮两次将 **数量** 字段中的值增加到 *2*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="b9a14-250">选择页面底部的按钮 ( ✔ ) 注册您的输入，然后再次选择该按钮 ( ✔ ) 确认您的输入。</span><span class="sxs-lookup"><span data-stu-id="b9a14-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="b9a14-251">查看 **采购订单：放置** 页中的信息。</span><span class="sxs-lookup"><span data-stu-id="b9a14-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="b9a14-252">此页显示已经为储存（工作 1）创建的工作。</span><span class="sxs-lookup"><span data-stu-id="b9a14-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="b9a14-253">将显示将储存收到的物料的货位、牌照、物料、尺寸和刚才完成的 **PO 行收货** 任务的数量。</span><span class="sxs-lookup"><span data-stu-id="b9a14-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="b9a14-254">确认储存工作。</span><span class="sxs-lookup"><span data-stu-id="b9a14-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="b9a14-255">为采购订单行 2 重复步骤 4 到 11。</span><span class="sxs-lookup"><span data-stu-id="b9a14-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="b9a14-256">但是在步骤 8 中，指定数量 *1*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="b9a14-257">将为与工作 1 相同的货位创建新储存工作（工作 2）。</span><span class="sxs-lookup"><span data-stu-id="b9a14-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="b9a14-258">再次为采购订单行 2 重复步骤 4 到 11。</span><span class="sxs-lookup"><span data-stu-id="b9a14-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="b9a14-259">在步骤 8 中，指定剩余数量 *1*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="b9a14-260">将为与工作 1 和工作 2 相同的货位创建新储存工作（工作 3）。</span><span class="sxs-lookup"><span data-stu-id="b9a14-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="b9a14-261">发生此行为是因为，使用了 *合并* 货位指令策略，并且 *Bulk* 这个 **货位模板** 设置中 **允许的产品维度混合** 快速选项卡允许在货位混合 **尺寸** 变型。</span><span class="sxs-lookup"><span data-stu-id="b9a14-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="b9a14-262">为采购订单行 3 重复步骤 4 到 11。</span><span class="sxs-lookup"><span data-stu-id="b9a14-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="b9a14-263">在步骤 8 中，为物料编号 *A0001* 指定数量 *1*。</span><span class="sxs-lookup"><span data-stu-id="b9a14-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="b9a14-264">将为非用于采购订单行 1 和 2 的货位创建新储存工作（工作 4）。</span><span class="sxs-lookup"><span data-stu-id="b9a14-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="b9a14-265">发生此行为是因为，货位模板不允许混合产品，但是允许混合同一个基础产品的维度。</span><span class="sxs-lookup"><span data-stu-id="b9a14-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="b9a14-266">选择页面顶部的“菜单”按钮（有时称为汉堡包或汉堡包按钮），然后选择 **取消** 退出 **PO 行收货**。</span><span class="sxs-lookup"><span data-stu-id="b9a14-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="b9a14-267">可以重复此场景，但是这次在 *BULK* 这个 **货位模板** 中 **允许产品维度混合** 下设置 **尺寸** - *否*，以便不能混合任何产品维度。</span><span class="sxs-lookup"><span data-stu-id="b9a14-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="b9a14-268">在这种情况下，当您收到采购订单时，将把每个产品变型放置到一个新货位。</span><span class="sxs-lookup"><span data-stu-id="b9a14-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]