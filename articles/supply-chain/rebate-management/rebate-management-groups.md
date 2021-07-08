---
title: 返点管理组
description: 本主题介绍如何设置返点管理组。 返点管理组可在返点计算期间使用，并可附加到主记录中。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee5a195b3d2881ff70fb1f0d4063ed681e874648
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271069"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="c72e2-104">返点管理组</span><span class="sxs-lookup"><span data-stu-id="c72e2-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c72e2-105">返点管理计算可以按组驱动。</span><span class="sxs-lookup"><span data-stu-id="c72e2-105">Rebate management calculations can be driven by groups.</span></span> <span data-ttu-id="c72e2-106">可以为客户、供应商和物料创建返点管理组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="c72e2-107">它们可以附加到主记录中。</span><span class="sxs-lookup"><span data-stu-id="c72e2-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="c72e2-108">返点管理客户组</span><span class="sxs-lookup"><span data-stu-id="c72e2-108">Rebate management customer groups</span></span>

<span data-ttu-id="c72e2-109">通常为连锁公司（例如，超市连锁店或特许经营公司）创建客户组的计算。</span><span class="sxs-lookup"><span data-stu-id="c72e2-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="c72e2-110">此类型的计算通常与返点有关。</span><span class="sxs-lookup"><span data-stu-id="c72e2-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="c72e2-111">通常在不考虑向谁出售合格订单的情况下计算扣缴。</span><span class="sxs-lookup"><span data-stu-id="c72e2-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="c72e2-112">但是，存在例外情况。</span><span class="sxs-lookup"><span data-stu-id="c72e2-112">However, there are exceptions.</span></span> <span data-ttu-id="c72e2-113">例如，许可接收方可能会创建如下扣缴方案：客户组 A 将接收 4%，但客户组 B 将仅接收 3%。</span><span class="sxs-lookup"><span data-stu-id="c72e2-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="c72e2-114">设置客户组</span><span class="sxs-lookup"><span data-stu-id="c72e2-114">Set up customer groups</span></span>

<span data-ttu-id="c72e2-115">若要使用返点管理客户组，请转到 **返点管理 \> 返点管理组设置 \> 客户组**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="c72e2-116">您可以使用操作窗格上的按钮根据需要添加和删除组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="c72e2-117">对于每个组，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c72e2-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="c72e2-118">**返点管理组** – 输入组的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="c72e2-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="c72e2-119">**描述** – 输入组的描述以提供有关应如何使用组的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c72e2-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="c72e2-120">管理客户组分配</span><span class="sxs-lookup"><span data-stu-id="c72e2-120">Manage customer group assignments</span></span>

<span data-ttu-id="c72e2-121">每个客户可以属于任何数量的返点管理组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="c72e2-122">若要查看和分配组成员，您可以从组列表或客户列表开始。</span><span class="sxs-lookup"><span data-stu-id="c72e2-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="c72e2-123">若要查看、添加或删除选定组的客户，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c72e2-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="c72e2-124">转到 **返点管理 \> 返点管理组设置 \> 客户组**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="c72e2-125">选择要管理的组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-125">Select the group to manage.</span></span>
1. <span data-ttu-id="c72e2-126">在操作窗格上，选择 **客户**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="c72e2-127">将显示 **返点管理组** 页面，其中显示已属于选定组成员的客户的列表。</span><span class="sxs-lookup"><span data-stu-id="c72e2-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="c72e2-128">若要向组添加新客户，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="c72e2-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c72e2-129">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c72e2-129">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="c72e2-130">**客户帐户** – 选择客户帐户 ID。</span><span class="sxs-lookup"><span data-stu-id="c72e2-130">**Customer account** – Select the customer account ID.</span></span>

1. <span data-ttu-id="c72e2-131">若要从组中删除客户，请选择该客户，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-131">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="c72e2-132">若要查看、添加或删除选定客户的组分配，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c72e2-132">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="c72e2-133">转到 **应付帐款 \> 客户 \> 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-133">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="c72e2-134">选择要使用的客户。</span><span class="sxs-lookup"><span data-stu-id="c72e2-134">Select the customer to work with.</span></span>
1. <span data-ttu-id="c72e2-135">在操作窗格的 **客户** 选项卡上，在 **返点管理** 组中，选择 **返点管理组**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-135">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="c72e2-136">将显示 **返点管理组** 页面，其中显示选定客户所属的组的列表。</span><span class="sxs-lookup"><span data-stu-id="c72e2-136">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="c72e2-137">若要向新组添加客户，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="c72e2-137">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c72e2-138">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c72e2-138">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="c72e2-139">**返点管理组** – 选择要将客户添加到的组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-139">**Rebate management group** – Select the group to add the customer to.</span></span>

1. <span data-ttu-id="c72e2-140">若要从组中删除客户，请选择该组，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-140">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="c72e2-141">返点管理供应商组</span><span class="sxs-lookup"><span data-stu-id="c72e2-141">Rebate management vendor groups</span></span>

<span data-ttu-id="c72e2-142">通常为一组交货点创建供应商组的计算。</span><span class="sxs-lookup"><span data-stu-id="c72e2-142">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="c72e2-143">此类型的计算通常与返点有关。</span><span class="sxs-lookup"><span data-stu-id="c72e2-143">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="c72e2-144">设置供应商组</span><span class="sxs-lookup"><span data-stu-id="c72e2-144">Set up vendor groups</span></span>

<span data-ttu-id="c72e2-145">若要使用返点管理供应商组，请转到 **返点管理 \> 返点管理组设置 \> 供应商组**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-145">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="c72e2-146">您可以使用操作窗格上的按钮根据需要添加和删除组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-146">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="c72e2-147">对于每个组，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c72e2-147">For each group, set the following fields:</span></span>

- <span data-ttu-id="c72e2-148">**返点管理组** – 输入组的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="c72e2-148">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="c72e2-149">**描述** – 输入组的描述以提供有关应如何使用组的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c72e2-149">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="c72e2-150">管理供应商组分配</span><span class="sxs-lookup"><span data-stu-id="c72e2-150">Manage vendor group assignments</span></span>

<span data-ttu-id="c72e2-151">每个供应商可以属于任何数量的返点管理组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-151">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="c72e2-152">若要查看和分配组成员，您可以从组列表或供应商列表开始。</span><span class="sxs-lookup"><span data-stu-id="c72e2-152">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="c72e2-153">若要查看、添加或删除选定组的供应商，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c72e2-153">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="c72e2-154">转到 **返点管理 \> 返点管理组设置 \> 供应商组**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-154">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="c72e2-155">选择要管理的组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-155">Select the group to manage.</span></span>
1. <span data-ttu-id="c72e2-156">在操作窗格上，选择 **供应商**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-156">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="c72e2-157">将显示 **返点管理组** 页面，其中显示已属于选定组成员的供应商的列表。</span><span class="sxs-lookup"><span data-stu-id="c72e2-157">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="c72e2-158">若要向组添加新供应商，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="c72e2-158">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c72e2-159">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c72e2-159">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="c72e2-160">**供应商帐户** – 选择供应商帐户 ID。</span><span class="sxs-lookup"><span data-stu-id="c72e2-160">**Vendor account** – Select the vendor account ID.</span></span>

1. <span data-ttu-id="c72e2-161">若要从组中删除供应商，请选择该供应商，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-161">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="c72e2-162">若要查看、添加或删除选定供应商的组分配，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c72e2-162">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="c72e2-163">转到 **应付帐款 \> 供应商 \> 所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-163">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="c72e2-164">选择要使用的供应商。</span><span class="sxs-lookup"><span data-stu-id="c72e2-164">Select the vendor to work with.</span></span>
1. <span data-ttu-id="c72e2-165">在操作窗格的 **供应商** 选项卡上，在 **返点管理** 组中，选择 **返点管理组**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-165">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="c72e2-166">将显示 **返点管理组** 页面，其中显示选定供应商所属的组的列表。</span><span class="sxs-lookup"><span data-stu-id="c72e2-166">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="c72e2-167">若要向新组添加供应商，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="c72e2-167">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c72e2-168">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c72e2-168">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="c72e2-169">**返点管理组** – 选择要将供应商添加到的组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-169">**Rebate management group** – Select the group to add the vendor to.</span></span>

1. <span data-ttu-id="c72e2-170">若要从组中删除供应商，请选择该组，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-170">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="c72e2-171">物料返点组</span><span class="sxs-lookup"><span data-stu-id="c72e2-171">Item rebate groups</span></span>

<span data-ttu-id="c72e2-172">通过对物料进行分组，您可以在计算返点和扣缴时具有更大的灵活性。</span><span class="sxs-lookup"><span data-stu-id="c72e2-172">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="c72e2-173">此方法通常是为客户和供应商设置返点和扣缴的更有效方法。</span><span class="sxs-lookup"><span data-stu-id="c72e2-173">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="c72e2-174">设置物料组</span><span class="sxs-lookup"><span data-stu-id="c72e2-174">Set up item groups</span></span>

<span data-ttu-id="c72e2-175">若要使用返点管理物料组，请转到 **返点管理 \> 返点管理组设置 \> 物料组**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-175">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="c72e2-176">您可以使用操作窗格上的按钮根据需要添加和删除组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-176">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="c72e2-177">对于每个组，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c72e2-177">For each group, set the following fields:</span></span>

- <span data-ttu-id="c72e2-178">**返点管理组** – 输入组的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="c72e2-178">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="c72e2-179">**描述** – 输入组的描述以提供有关应如何使用组的详细信息。</span><span class="sxs-lookup"><span data-stu-id="c72e2-179">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="c72e2-180">管理物料组分配</span><span class="sxs-lookup"><span data-stu-id="c72e2-180">Manage item group assignments</span></span>

<span data-ttu-id="c72e2-181">每个物料可以属于任何数量的返点管理组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-181">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="c72e2-182">若要查看和分配组成员，您可以从组列表或物料列表开始。</span><span class="sxs-lookup"><span data-stu-id="c72e2-182">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="c72e2-183">您还可以根据类别层次结构添加物料。</span><span class="sxs-lookup"><span data-stu-id="c72e2-183">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="c72e2-184">若要查看、添加或删除选定组的物料，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c72e2-184">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="c72e2-185">转到 **返点管理 \> 返点管理组设置 \> 物料组**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-185">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="c72e2-186">选择要管理的组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-186">Select the group to manage.</span></span>
1. <span data-ttu-id="c72e2-187">在操作窗格上，选择 **物料**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-187">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="c72e2-188">将显示 **返点管理组** 页面，其中显示已属于选定组成员的物料的列表。</span><span class="sxs-lookup"><span data-stu-id="c72e2-188">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="c72e2-189">若要向组添加新物料，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="c72e2-189">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c72e2-190">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c72e2-190">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="c72e2-191">**物料帐户** – 选择物料帐户 ID。</span><span class="sxs-lookup"><span data-stu-id="c72e2-191">**Item account** – Select the item account ID.</span></span>

1. <span data-ttu-id="c72e2-192">若要从组中删除物料，请选择该物料，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-192">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="c72e2-193">若要查看、添加或删除选定物料的组分配，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c72e2-193">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="c72e2-194">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-194">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="c72e2-195">选择要使用的物料。</span><span class="sxs-lookup"><span data-stu-id="c72e2-195">Select the item to work with.</span></span>
1. <span data-ttu-id="c72e2-196">在操作窗格的 **产品** 选项卡上，在 **返点管理** 组中，选择 **返点管理组**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-196">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="c72e2-197">将显示 **返点管理组** 页面，其中显示选定物料所属的组的列表。</span><span class="sxs-lookup"><span data-stu-id="c72e2-197">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="c72e2-198">若要向新组添加物料，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="c72e2-198">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="c72e2-199">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="c72e2-199">Then set the following field for the new row:</span></span>

    - <span data-ttu-id="c72e2-200">**返点管理组** – 选择要将物料添加到的组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-200">**Rebate management group** – Select the group to add the item to.</span></span>

1. <span data-ttu-id="c72e2-201">若要从组中删除物料，请选择该组，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-201">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="c72e2-202">若要根据类别层次结构向组添加物料，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="c72e2-202">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="c72e2-203">转到 **返点管理 \> 返点管理组设置 \> 物料组**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-203">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="c72e2-204">选择要管理的组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-204">Select the group to manage.</span></span>
1. <span data-ttu-id="c72e2-205">在操作窗格上，选择 **添加物料**。</span><span class="sxs-lookup"><span data-stu-id="c72e2-205">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="c72e2-206">在 **添加物料** 对话框中，在 **类别层次结构** 字段中，选择顶级类别。</span><span class="sxs-lookup"><span data-stu-id="c72e2-206">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="c72e2-207">在左侧窗格中打开物料层次结构。</span><span class="sxs-lookup"><span data-stu-id="c72e2-207">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="c72e2-208">选择您要查找的层次结构级别。</span><span class="sxs-lookup"><span data-stu-id="c72e2-208">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="c72e2-209">现在，右侧窗格中列出了选定层次结构和层次结构级别中的物料。</span><span class="sxs-lookup"><span data-stu-id="c72e2-209">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="c72e2-210">按照下列步骤使用窗格：</span><span class="sxs-lookup"><span data-stu-id="c72e2-210">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="c72e2-211">选中要添加的每个物料的复选框。</span><span class="sxs-lookup"><span data-stu-id="c72e2-211">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="c72e2-212">在网格标题上选中该复选框以选择列出的所有物料。</span><span class="sxs-lookup"><span data-stu-id="c72e2-212">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="c72e2-213">选择 **显示所选内容** 按钮以筛选网格，以便它仅显示您到目前为止选择的物料。</span><span class="sxs-lookup"><span data-stu-id="c72e2-213">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="c72e2-214">再次选择该按钮以返回到完整列表。</span><span class="sxs-lookup"><span data-stu-id="c72e2-214">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="c72e2-215">选择 **确定** 以将物料选择应用到选定组。</span><span class="sxs-lookup"><span data-stu-id="c72e2-215">Select **OK** to apply your item selection to the selected group.</span></span>
