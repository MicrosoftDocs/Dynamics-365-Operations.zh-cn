---
title: 返点管理组
description: 本主题介绍如何设置返点管理组。 返点管理组可在返点计算期间使用，并可附加到主记录中。
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 2d1f8ed9def03afc97c0b4c5ea86430ff089aac6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819224"
---
# <a name="rebate-management-groups"></a><span data-ttu-id="f4c29-104">返点管理组</span><span class="sxs-lookup"><span data-stu-id="f4c29-104">Rebate management groups</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f4c29-105">返点和扣缴计算可以按组驱动。</span><span class="sxs-lookup"><span data-stu-id="f4c29-105">Rebate and deduction calculations can be driven by groups.</span></span> <span data-ttu-id="f4c29-106">可以为客户、供应商和物料创建返点管理组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-106">Rebate management groups can be created for customers, vendors, and items.</span></span> <span data-ttu-id="f4c29-107">它们可以附加到主记录中。</span><span class="sxs-lookup"><span data-stu-id="f4c29-107">They can be attached to a master record.</span></span>

## <a name="rebate-management-customer-groups"></a><span data-ttu-id="f4c29-108">返点管理客户组</span><span class="sxs-lookup"><span data-stu-id="f4c29-108">Rebate management customer groups</span></span>

<span data-ttu-id="f4c29-109">通常为连锁公司（例如，超市连锁店或特许经营公司）创建客户组的计算。</span><span class="sxs-lookup"><span data-stu-id="f4c29-109">The calculation for a group of customers is often created for a chain of companies, such as a supermarket chain or a franchise company.</span></span> <span data-ttu-id="f4c29-110">此类型的计算通常与返点有关。</span><span class="sxs-lookup"><span data-stu-id="f4c29-110">This type of calculation is usually related to a rebate.</span></span>

<span data-ttu-id="f4c29-111">通常在不考虑向谁出售合格订单的情况下计算扣缴。</span><span class="sxs-lookup"><span data-stu-id="f4c29-111">A deduction is often calculated without considering who the qualifying order was sold to.</span></span> <span data-ttu-id="f4c29-112">但是，存在例外情况。</span><span class="sxs-lookup"><span data-stu-id="f4c29-112">However, there are exceptions.</span></span> <span data-ttu-id="f4c29-113">例如，许可接收方可能会创建如下扣缴方案：客户组 A 将接收 4%，但客户组 B 将仅接收 3%。</span><span class="sxs-lookup"><span data-stu-id="f4c29-113">For example, a licensee might create a deduction scheme where customer group A will receive 4 percent, but customer group B will receive only 3 percent.</span></span>

### <a name="set-up-customer-groups"></a><span data-ttu-id="f4c29-114">设置客户组</span><span class="sxs-lookup"><span data-stu-id="f4c29-114">Set up customer groups</span></span>

<span data-ttu-id="f4c29-115">若要使用返点管理客户组，请转到 **返点管理 \> 返点管理组设置 \> 客户组**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-115">To work with Rebate management customer groups, go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span> <span data-ttu-id="f4c29-116">您可以使用操作窗格上的按钮根据需要添加和删除组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-116">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="f4c29-117">对于每个组，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f4c29-117">For each group, set the following fields:</span></span>

- <span data-ttu-id="f4c29-118">**返点管理组** – 输入组的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="f4c29-118">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="f4c29-119">**描述** – 输入组的描述以提供有关应如何使用组的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f4c29-119">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-customer-group-assignments"></a><span data-ttu-id="f4c29-120">管理客户组分配</span><span class="sxs-lookup"><span data-stu-id="f4c29-120">Manage customer group assignments</span></span>

<span data-ttu-id="f4c29-121">每个客户可以属于任何数量的返点管理组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-121">Each customer can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="f4c29-122">若要查看和分配组成员，您可以从组列表或客户列表开始。</span><span class="sxs-lookup"><span data-stu-id="f4c29-122">To view and assign group members, you can start from either the group list or the customer list.</span></span>

<span data-ttu-id="f4c29-123">若要查看、添加或删除选定组的客户，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f4c29-123">To view, add, or remove customers for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="f4c29-124">转到 **返点管理 \> 返点管理组设置 \> 客户组**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-124">Go to **Rebate management \> Rebate management groups setup \> Customer groups**.</span></span>
1. <span data-ttu-id="f4c29-125">选择要管理的组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-125">Select the group to manage.</span></span>
1. <span data-ttu-id="f4c29-126">在操作窗格上，选择 **客户**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-126">On the Action Pane, select **Customers**.</span></span> <span data-ttu-id="f4c29-127">将显示 **返点管理组** 页面，其中显示已属于选定组成员的客户的列表。</span><span class="sxs-lookup"><span data-stu-id="f4c29-127">The **Rebate management groups** page appears and shows a list of customers that are already members of the selected group.</span></span>
1. <span data-ttu-id="f4c29-128">若要向组添加新客户，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="f4c29-128">To add a new customer to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="f4c29-129">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f4c29-129">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f4c29-130">**客户帐户** – 选择客户帐户 ID。</span><span class="sxs-lookup"><span data-stu-id="f4c29-130">**Customer account** – Select the customer account ID.</span></span>
    - <span data-ttu-id="f4c29-131">**名称** – 输入客户的名称和/或描述。</span><span class="sxs-lookup"><span data-stu-id="f4c29-131">**Name** – Enter a name and/or description of the customer.</span></span>

1. <span data-ttu-id="f4c29-132">若要从组中删除客户，请选择该客户，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-132">To remove a customer from the group, select the customer, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="f4c29-133">若要查看、添加或删除选定客户的组分配，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f4c29-133">To view, add, or remove group assignments for a selected customer, follow these steps.</span></span>

1. <span data-ttu-id="f4c29-134">转到 **应付帐款 \> 客户 \> 所有客户**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-134">Go to **Accounts receivable \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="f4c29-135">选择要使用的客户。</span><span class="sxs-lookup"><span data-stu-id="f4c29-135">Select the customer to work with.</span></span>
1. <span data-ttu-id="f4c29-136">在操作窗格的 **客户** 选项卡上，在 **返点管理** 组中，选择 **返点管理组**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-136">On the Action Pane, on the **Customer** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="f4c29-137">将显示 **返点管理组** 页面，其中显示选定客户所属的组的列表。</span><span class="sxs-lookup"><span data-stu-id="f4c29-137">The **Rebate management groups** page appears and shows a list of groups that the selected customer already belongs to.</span></span>
1. <span data-ttu-id="f4c29-138">若要向新组添加客户，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="f4c29-138">To add the customer to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="f4c29-139">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f4c29-139">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f4c29-140">**返点管理组** – 选择要将客户添加到的组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-140">**Rebate management group** – Select the group to add the customer to.</span></span>
    - <span data-ttu-id="f4c29-141">**描述** – 输入组的描述（例如，说明客户为什么是该组的成员）。</span><span class="sxs-lookup"><span data-stu-id="f4c29-141">**Description** – Enter a description of the group (for example, to explain why the customer is a member of it).</span></span>

1. <span data-ttu-id="f4c29-142">若要从组中删除客户，请选择该组，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-142">To remove a customer from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="rebate-management-vendor-groups"></a><span data-ttu-id="f4c29-143">返点管理供应商组</span><span class="sxs-lookup"><span data-stu-id="f4c29-143">Rebate management vendor groups</span></span>

<span data-ttu-id="f4c29-144">通常为一组交货点创建供应商组的计算。</span><span class="sxs-lookup"><span data-stu-id="f4c29-144">The calculation for a group of vendors is often created for a group of delivery points.</span></span> <span data-ttu-id="f4c29-145">此类型的计算通常与返点有关。</span><span class="sxs-lookup"><span data-stu-id="f4c29-145">This type of calculation is usually related to a rebate.</span></span>

### <a name="set-up-vendor-groups"></a><span data-ttu-id="f4c29-146">设置供应商组</span><span class="sxs-lookup"><span data-stu-id="f4c29-146">Set up vendor groups</span></span>

<span data-ttu-id="f4c29-147">若要使用返点管理供应商组，请转到 **返点管理 \> 返点管理组设置 \> 供应商组**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-147">To work with Rebate management vendor groups, go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span> <span data-ttu-id="f4c29-148">您可以使用操作窗格上的按钮根据需要添加和删除组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-148">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="f4c29-149">对于每个组，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f4c29-149">For each group, set the following fields:</span></span>

- <span data-ttu-id="f4c29-150">**返点管理组** – 输入组的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="f4c29-150">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="f4c29-151">**描述** – 输入组的描述以提供有关应如何使用组的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f4c29-151">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-vendor-group-assignments"></a><span data-ttu-id="f4c29-152">管理供应商组分配</span><span class="sxs-lookup"><span data-stu-id="f4c29-152">Manage vendor group assignments</span></span>

<span data-ttu-id="f4c29-153">每个供应商可以属于任何数量的返点管理组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-153">Each vendor can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="f4c29-154">若要查看和分配组成员，您可以从组列表或供应商列表开始。</span><span class="sxs-lookup"><span data-stu-id="f4c29-154">To view and assign group members, you can start from either the group list or the vendor list.</span></span>

<span data-ttu-id="f4c29-155">若要查看、添加或删除选定组的供应商，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f4c29-155">To view, add, or remove vendors for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="f4c29-156">转到 **返点管理 \> 返点管理组设置 \> 供应商组**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-156">Go to **Rebate management \> Rebate management groups setup \> Vendor groups**.</span></span>
1. <span data-ttu-id="f4c29-157">选择要管理的组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-157">Select the group to manage.</span></span>
1. <span data-ttu-id="f4c29-158">在操作窗格上，选择 **供应商**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-158">On the Action Pane, select **Vendors**.</span></span> <span data-ttu-id="f4c29-159">将显示 **返点管理组** 页面，其中显示已属于选定组成员的供应商的列表。</span><span class="sxs-lookup"><span data-stu-id="f4c29-159">The **Rebate management groups** page appears and shows a list of vendors that are already members of the selected group.</span></span>
1. <span data-ttu-id="f4c29-160">若要向组添加新供应商，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="f4c29-160">To add a new vendor to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="f4c29-161">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f4c29-161">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f4c29-162">**供应商帐户** – 选择供应商帐户 ID。</span><span class="sxs-lookup"><span data-stu-id="f4c29-162">**Vendor account** – Select the vendor account ID.</span></span>
    - <span data-ttu-id="f4c29-163">**名称** – 输入供应商的名称和/或描述。</span><span class="sxs-lookup"><span data-stu-id="f4c29-163">**Name** – Enter a name and/or description of the vendor.</span></span>

1. <span data-ttu-id="f4c29-164">若要从组中删除供应商，请选择该供应商，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-164">To remove a vendor from the group, select the vendor, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="f4c29-165">若要查看、添加或删除选定供应商的组分配，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f4c29-165">To view, add, or remove group assignments for a selected vendor, follow these steps.</span></span>

1. <span data-ttu-id="f4c29-166">转到 **应付帐款 \> 供应商 \> 所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-166">Go to **Accounts payable \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="f4c29-167">选择要使用的供应商。</span><span class="sxs-lookup"><span data-stu-id="f4c29-167">Select the vendor to work with.</span></span>
1. <span data-ttu-id="f4c29-168">在操作窗格的 **供应商** 选项卡上，在 **返点管理** 组中，选择 **返点管理组**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-168">On the Action Pane, on the **Vendor** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="f4c29-169">将显示 **返点管理组** 页面，其中显示选定供应商所属的组的列表。</span><span class="sxs-lookup"><span data-stu-id="f4c29-169">The **Rebate management groups** page appears and shows a list of groups that the selected vendor already belongs to.</span></span>
1. <span data-ttu-id="f4c29-170">若要向新组添加供应商，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="f4c29-170">To add the vendor to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="f4c29-171">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f4c29-171">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f4c29-172">**返点管理组** – 选择要将供应商添加到的组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-172">**Rebate management group** – Select the group to add the vendor to.</span></span>
    - <span data-ttu-id="f4c29-173">**描述** – 输入组的描述（例如，说明供应商为什么是该组的成员）。</span><span class="sxs-lookup"><span data-stu-id="f4c29-173">**Description** – Enter a description of the group (for example, to explain why the vendor is a member of it).</span></span>

1. <span data-ttu-id="f4c29-174">若要从组中删除供应商，请选择该组，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-174">To remove a vendor from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

## <a name="item-rebate-groups"></a><span data-ttu-id="f4c29-175">物料返点组</span><span class="sxs-lookup"><span data-stu-id="f4c29-175">Item rebate groups</span></span>

<span data-ttu-id="f4c29-176">通过对物料进行分组，您可以在计算返点和扣缴时具有更大的灵活性。</span><span class="sxs-lookup"><span data-stu-id="f4c29-176">By grouping items, you have more flexibility when rebates and deductions are calculated.</span></span> <span data-ttu-id="f4c29-177">此方法通常是为客户和供应商设置返点和扣缴的更有效方法。</span><span class="sxs-lookup"><span data-stu-id="f4c29-177">This approach is often a more efficient way to set up rebates and deductions for customers and vendors.</span></span>

### <a name="set-up-item-groups"></a><span data-ttu-id="f4c29-178">设置物料组</span><span class="sxs-lookup"><span data-stu-id="f4c29-178">Set up item groups</span></span>

<span data-ttu-id="f4c29-179">若要使用返点管理物料组，请转到 **返点管理 \> 返点管理组设置 \> 物料组**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-179">To work with Rebate management item groups, go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span> <span data-ttu-id="f4c29-180">您可以使用操作窗格上的按钮根据需要添加和删除组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-180">You can use the buttons on the Action Pane to add and remove groups as required.</span></span> <span data-ttu-id="f4c29-181">对于每个组，设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f4c29-181">For each group, set the following fields:</span></span>

- <span data-ttu-id="f4c29-182">**返点管理组** – 输入组的唯一名称。</span><span class="sxs-lookup"><span data-stu-id="f4c29-182">**Rebate management group** – Enter a unique name for the group.</span></span>
- <span data-ttu-id="f4c29-183">**描述** – 输入组的描述以提供有关应如何使用组的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f4c29-183">**Description** – Enter a description of the group to provide more information about how it should be used.</span></span>

### <a name="manage-item-group-assignments"></a><span data-ttu-id="f4c29-184">管理物料组分配</span><span class="sxs-lookup"><span data-stu-id="f4c29-184">Manage item group assignments</span></span>

<span data-ttu-id="f4c29-185">每个物料可以属于任何数量的返点管理组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-185">Each item can belong to any number of Rebate management groups.</span></span> <span data-ttu-id="f4c29-186">若要查看和分配组成员，您可以从组列表或物料列表开始。</span><span class="sxs-lookup"><span data-stu-id="f4c29-186">To view and assign group members, you can start from either the group list or the item list.</span></span> <span data-ttu-id="f4c29-187">您还可以根据类别层次结构添加物料。</span><span class="sxs-lookup"><span data-stu-id="f4c29-187">You can also add items based on your category hierarchy.</span></span>

<span data-ttu-id="f4c29-188">若要查看、添加或删除选定组的物料，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f4c29-188">To view, add, or remove items for a selected group, follow these steps.</span></span>

1. <span data-ttu-id="f4c29-189">转到 **返点管理 \> 返点管理组设置 \> 物料组**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-189">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="f4c29-190">选择要管理的组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-190">Select the group to manage.</span></span>
1. <span data-ttu-id="f4c29-191">在操作窗格上，选择 **物料**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-191">On the Action Pane, select **Items**.</span></span> <span data-ttu-id="f4c29-192">将显示 **返点管理组** 页面，其中显示已属于选定组成员的物料的列表。</span><span class="sxs-lookup"><span data-stu-id="f4c29-192">The **Rebate management groups** page appears and shows a list of items that are already members of the selected group.</span></span>
1. <span data-ttu-id="f4c29-193">若要向组添加新物料，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="f4c29-193">To add a new item to the group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="f4c29-194">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f4c29-194">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f4c29-195">**物料帐户** – 选择物料帐户 ID。</span><span class="sxs-lookup"><span data-stu-id="f4c29-195">**Item account** – Select the item account ID.</span></span>
    - <span data-ttu-id="f4c29-196">**产品名称** – 输入物料的名称和/或描述。</span><span class="sxs-lookup"><span data-stu-id="f4c29-196">**Product name** – Enter a name and/or description of the item.</span></span>

1. <span data-ttu-id="f4c29-197">若要从组中删除物料，请选择该物料，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-197">To remove an item from the group, select the item, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="f4c29-198">若要查看、添加或删除选定物料的组分配，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f4c29-198">To view, add, or remove group assignments for a selected item, follow these steps.</span></span>

1. <span data-ttu-id="f4c29-199">转到 **产品信息管理 \> 产品 \> 已发布产品**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-199">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="f4c29-200">选择要使用的物料。</span><span class="sxs-lookup"><span data-stu-id="f4c29-200">Select the item to work with.</span></span>
1. <span data-ttu-id="f4c29-201">在操作窗格的 **产品** 选项卡上，在 **返点管理** 组中，选择 **返点管理组**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-201">On the Action Pane, on the **Product** tab, in the **Rebate management** group, select **Rebate management groups**.</span></span> <span data-ttu-id="f4c29-202">将显示 **返点管理组** 页面，其中显示选定物料所属的组的列表。</span><span class="sxs-lookup"><span data-stu-id="f4c29-202">The **Rebate management groups** page appears and shows a list of groups that the selected item already belongs to.</span></span>
1. <span data-ttu-id="f4c29-203">若要向新组添加物料，请在操作窗格上选择 **新建** 以向网格添加行。</span><span class="sxs-lookup"><span data-stu-id="f4c29-203">To add the item to a new group, select **New** on the Action Pane to add a row to the grid.</span></span> <span data-ttu-id="f4c29-204">然后，针对新行设置以下字段：</span><span class="sxs-lookup"><span data-stu-id="f4c29-204">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="f4c29-205">**返点管理组** – 选择要将物料添加到的组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-205">**Rebate management group** – Select the group to add the item to.</span></span>
    - <span data-ttu-id="f4c29-206">**描述** – 输入组的描述（例如，说明物料为什么是该组的成员）。</span><span class="sxs-lookup"><span data-stu-id="f4c29-206">**Description** – Enter a description of the group (for example, to explain why the item is a member of it).</span></span>

1. <span data-ttu-id="f4c29-207">若要从组中删除物料，请选择该组，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-207">To remove an item from a group, select the group, and then select **Delete** on the Action Pane.</span></span>

<span data-ttu-id="f4c29-208">若要根据类别层次结构向组添加物料，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="f4c29-208">To add items to a group based on your category hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="f4c29-209">转到 **返点管理 \> 返点管理组设置 \> 物料组**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-209">Go to **Rebate management \> Rebate management groups setup \> Item groups**.</span></span>
1. <span data-ttu-id="f4c29-210">选择要管理的组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-210">Select the group to manage.</span></span>
1. <span data-ttu-id="f4c29-211">在操作窗格上，选择 **添加物料**。</span><span class="sxs-lookup"><span data-stu-id="f4c29-211">On the Action Pane, select **Add items**.</span></span>
1. <span data-ttu-id="f4c29-212">在 **添加物料** 对话框中，在 **类别层次结构** 字段中，选择顶级类别。</span><span class="sxs-lookup"><span data-stu-id="f4c29-212">In the **Add items** dialog box, in the **Category hierarchy** field, select a top-level category.</span></span>
1. <span data-ttu-id="f4c29-213">在左侧窗格中打开物料层次结构。</span><span class="sxs-lookup"><span data-stu-id="f4c29-213">The item hierarchy is opened in the left pane.</span></span> <span data-ttu-id="f4c29-214">选择您要查找的层次结构级别。</span><span class="sxs-lookup"><span data-stu-id="f4c29-214">Select the hierarchy level that you're looking for.</span></span> 
1. <span data-ttu-id="f4c29-215">现在，右侧窗格中列出了选定层次结构和层次结构级别中的物料。</span><span class="sxs-lookup"><span data-stu-id="f4c29-215">Items from the selected hierarchy and hierarchy level are now listed in the right pane.</span></span> <span data-ttu-id="f4c29-216">按照下列步骤使用窗格：</span><span class="sxs-lookup"><span data-stu-id="f4c29-216">Follow these steps to work with the pane:</span></span>

    - <span data-ttu-id="f4c29-217">选中要添加的每个物料的复选框。</span><span class="sxs-lookup"><span data-stu-id="f4c29-217">Select the check box for each item that you want to add.</span></span>
    - <span data-ttu-id="f4c29-218">在网格标题上选中该复选框以选择列出的所有物料。</span><span class="sxs-lookup"><span data-stu-id="f4c29-218">Select the check box on the grid header to select all the items that are listed.</span></span>
    - <span data-ttu-id="f4c29-219">选择 **显示所选内容** 按钮以筛选网格，以便它仅显示您到目前为止选择的物料。</span><span class="sxs-lookup"><span data-stu-id="f4c29-219">Select the **Show selected** button to filter the grid so that it shows only the items that you've selected so far.</span></span> <span data-ttu-id="f4c29-220">再次选择该按钮以返回到完整列表。</span><span class="sxs-lookup"><span data-stu-id="f4c29-220">Select the button again to return to the full list.</span></span>

1. <span data-ttu-id="f4c29-221">选择 **确定** 以将物料选择应用到选定组。</span><span class="sxs-lookup"><span data-stu-id="f4c29-221">Select **OK** to apply your item selection to the selected group.</span></span>
