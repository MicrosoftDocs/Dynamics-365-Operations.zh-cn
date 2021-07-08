---
title: 周期盘点示例场景
description: 本主题提供了一系列探索 Microsoft Dynamics 365 Supply Chain Management 的周期盘点功能的场景。
author: GalynaFedorova
ms.date: 06/08/2021
ms.topic: article
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 828954402d223c62f52d7a13fcc9efab84630c80
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261765"
---
# <a name="cycle-counting-example-scenarios"></a><span data-ttu-id="ba825-103">周期盘点示例场景</span><span class="sxs-lookup"><span data-stu-id="ba825-103">Cycle counting example scenarios</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba825-104">本主题提供了一系列探索 Microsoft Dynamics 365 Supply Chain Management 的周期盘点功能的场景。</span><span class="sxs-lookup"><span data-stu-id="ba825-104">This topic provides a collection of scenarios that explore the cycle counting features of Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="ba825-105">首先，它介绍了现有 Supply Chain Management 环境的要求。</span><span class="sxs-lookup"><span data-stu-id="ba825-105">It first describes the requirements for your existing Supply Chain Management environment.</span></span> <span data-ttu-id="ba825-106">然后，它说明了如何配置周期盘点并介绍了所有周期盘点阶段。</span><span class="sxs-lookup"><span data-stu-id="ba825-106">It then explains how to configure cycle counting and describes all the cycle counting stages.</span></span> <span data-ttu-id="ba825-107">完成后，您应该对周期盘点有很好的了解，包括指导周期盘点、盲目周期盘点、现场周期盘点、周期盘点阈值和周期盘点计划。</span><span class="sxs-lookup"><span data-stu-id="ba825-107">When you've finished, you should have a good understanding of cycle counting, including guided cycle counting, blind cycle counting, spot cycle counting, cycle count thresholds, and cycle count plans.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ba825-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="ba825-108">Prerequisites</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="ba825-109">提供演示数据</span><span class="sxs-lookup"><span data-stu-id="ba825-109">Make demo data available</span></span>

<span data-ttu-id="ba825-110">本主题中的每个场景引用为 Supply Chain Management 提供的标准演示数据中包含的值和记录。</span><span class="sxs-lookup"><span data-stu-id="ba825-110">Each scenario in this topic references values and records that are included in the standard demo data that is provided for Supply Chain Management.</span></span> <span data-ttu-id="ba825-111">如果要在完成场景时使用此处提供的值，请务必在安装了演示数据的环境中操作，并且在开始前将法人（公司）设置为 **USMF**。</span><span class="sxs-lookup"><span data-stu-id="ba825-111">If you want to use the values that are provided here as you work through the scenarios, be sure to work in an environment where the demo data is installed, and set the legal entity (company) to **USMF** before you begin.</span></span>

### <a name="turn-on-support-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="ba825-112">打开对 Warehouse Management 移动应用的支持</span><span class="sxs-lookup"><span data-stu-id="ba825-112">Turn on support for the Warehouse Management mobile app</span></span>

<span data-ttu-id="ba825-113">必须先在您的系统中添加对新 Warehouse Management 移动应用的支持，然后才能使用它。</span><span class="sxs-lookup"><span data-stu-id="ba825-113">Before you can use the new Warehouse Management mobile app, you must add support for it in your system.</span></span> <span data-ttu-id="ba825-114">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。</span><span class="sxs-lookup"><span data-stu-id="ba825-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="ba825-115">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="ba825-115">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ba825-116">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="ba825-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ba825-117">**功能名称**：*新仓库应用的用户设置、图标和步骤标题*</span><span class="sxs-lookup"><span data-stu-id="ba825-117">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

### <a name="prepare-demo-data-for-the-scenarios"></a><a name= "prepare-demo-data"></a><span data-ttu-id="ba825-118">为场景准备演示数据</span><span class="sxs-lookup"><span data-stu-id="ba825-118">Prepare demo data for the scenarios</span></span>

<span data-ttu-id="ba825-119">按照以下步骤确认场景所需的所有演示数据在您系统中的 USMF 公司中可用。</span><span class="sxs-lookup"><span data-stu-id="ba825-119">Follow these steps to confirm that all the demo data that is required for the scenarios is available in the USMF company in your system.</span></span> <span data-ttu-id="ba825-120">创建任何缺失的记录或值。</span><span class="sxs-lookup"><span data-stu-id="ba825-120">Create any records or values that are missing.</span></span>

1. <span data-ttu-id="ba825-121">转到 **仓库管理 \> 设置 \> 工作人员**。</span><span class="sxs-lookup"><span data-stu-id="ba825-121">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="ba825-122">在列表窗格中，选择 **Julia Funderburk**。</span><span class="sxs-lookup"><span data-stu-id="ba825-122">In the list pane, select **Julia Funderburk**.</span></span>
1. <span data-ttu-id="ba825-123">在 **用户** 快速选项卡上，选择具有以下值的行。</span><span class="sxs-lookup"><span data-stu-id="ba825-123">On the **Users** FastTab, select the row that has the following values.</span></span> <span data-ttu-id="ba825-124">如果没有现有行具有这些值，则创建它。</span><span class="sxs-lookup"><span data-stu-id="ba825-124">If no existing row has these values, create it.</span></span>

    - <span data-ttu-id="ba825-125">**用户 ID**：*61*</span><span class="sxs-lookup"><span data-stu-id="ba825-125">**User ID:** *61*</span></span>
    - <span data-ttu-id="ba825-126">**用户名**：*WH61*</span><span class="sxs-lookup"><span data-stu-id="ba825-126">**User name:** *WH61*</span></span>
    - <span data-ttu-id="ba825-127">**默认仓库**：*61*</span><span class="sxs-lookup"><span data-stu-id="ba825-127">**Default warehouse:** *61*</span></span>
    - <span data-ttu-id="ba825-128">**菜单名称**：*主*</span><span class="sxs-lookup"><span data-stu-id="ba825-128">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="ba825-129">在 **工作** 快速选项卡上，为用户 *61* 设置以下值（如果尚未设置）：</span><span class="sxs-lookup"><span data-stu-id="ba825-129">On the **Work** FastTab, set the following values for user *61* if they aren't already set:</span></span>

    - <span data-ttu-id="ba825-130">**为周期盘点主管**：*否*</span><span class="sxs-lookup"><span data-stu-id="ba825-130">**Is a cycle count supervisor:** *No*</span></span>
    - <span data-ttu-id="ba825-131">**最大百分比限制**：*0*</span><span class="sxs-lookup"><span data-stu-id="ba825-131">**Maximum percentage limit:** *0*</span></span>
    - <span data-ttu-id="ba825-132">**最大数量限制**：*0*</span><span class="sxs-lookup"><span data-stu-id="ba825-132">**Maximum quantity limit:** *0*</span></span>
    - <span data-ttu-id="ba825-133">**最大值限制**：*0*</span><span class="sxs-lookup"><span data-stu-id="ba825-133">**Maximum value limit:** *0*</span></span>

1. <span data-ttu-id="ba825-134">转到 **仓库管理 \> 设置 \> 工作 \> 工作池**。</span><span class="sxs-lookup"><span data-stu-id="ba825-134">Go to **Warehouse management \> Setup \> Work \> Work pools**.</span></span>
1. <span data-ttu-id="ba825-135">工作池用于基于工作类型划分仓库工作（在这种情况下，为周期盘点工作）。</span><span class="sxs-lookup"><span data-stu-id="ba825-135">Work pools are used to segregate warehouse work, based on the type of work (in this case, cycle counting work).</span></span> <span data-ttu-id="ba825-136">确保存在具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="ba825-136">Make sure that a record exists that has the following settings:</span></span>

    - <span data-ttu-id="ba825-137">**工作池 ID**：*CycleCount*</span><span class="sxs-lookup"><span data-stu-id="ba825-137">**Work pool ID:** *CycleCount*</span></span>
    - <span data-ttu-id="ba825-138">**描述**：*周期盘点*</span><span class="sxs-lookup"><span data-stu-id="ba825-138">**Description:** *Cycle Count*</span></span>

1. <span data-ttu-id="ba825-139">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单项**。</span><span class="sxs-lookup"><span data-stu-id="ba825-139">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="ba825-140">在列表窗格中，选择名为 *周期盘点* 的记录。</span><span class="sxs-lookup"><span data-stu-id="ba825-140">In the list pane, select the record that is named *Cycle Count*.</span></span> <span data-ttu-id="ba825-141">如果没有现有记录具有此名称，则创建它。</span><span class="sxs-lookup"><span data-stu-id="ba825-141">If no existing record has this name, create it.</span></span> <span data-ttu-id="ba825-142">确认或设置记录的以下值：</span><span class="sxs-lookup"><span data-stu-id="ba825-142">Confirm or set the following values for the record:</span></span>

    - <span data-ttu-id="ba825-143">**菜单项名称**：*周期盘点*</span><span class="sxs-lookup"><span data-stu-id="ba825-143">**Menu item name:** *Cycle Count*</span></span>
    - <span data-ttu-id="ba825-144">**标题**：*周期盘点指导*</span><span class="sxs-lookup"><span data-stu-id="ba825-144">**Title:** *Cycle Count Guided*</span></span>
    - <span data-ttu-id="ba825-145">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="ba825-145">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ba825-146">**使用现有工作**：*是*</span><span class="sxs-lookup"><span data-stu-id="ba825-146">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="ba825-147">**导向方式**：*系统导向*（此值指示 Supply Chain Management 将向工作人员分配周期盘点工作 ID。）</span><span class="sxs-lookup"><span data-stu-id="ba825-147">**Directed by:** *System directed* (This value indicates that Supply Chain Management will assign a cycle counting work ID to the worker.)</span></span>
    - <span data-ttu-id="ba825-148">**显示库存状态**：*是*</span><span class="sxs-lookup"><span data-stu-id="ba825-148">**Display inventory status:** *Yes*</span></span>

1. <span data-ttu-id="ba825-149">在操作窗格上，选择 **周期盘点**。</span><span class="sxs-lookup"><span data-stu-id="ba825-149">On the Action Pane, select **Cycle counting**.</span></span>
1. <span data-ttu-id="ba825-150">在 **移动设备周期盘点** 对话框中，确认或设置以下值：</span><span class="sxs-lookup"><span data-stu-id="ba825-150">In the **Mobile device cycle counting** dialog box, confirm or set the following values:</span></span>

    - <span data-ttu-id="ba825-151">**显示物料编号**：*是*</span><span class="sxs-lookup"><span data-stu-id="ba825-151">**Display item number:** *Yes*</span></span>
    - <span data-ttu-id="ba825-152">**显示牌照**：*是*</span><span class="sxs-lookup"><span data-stu-id="ba825-152">**Display license plate:** *Yes*</span></span>
    - <span data-ttu-id="ba825-153">**尝试次数**：*1*</span><span class="sxs-lookup"><span data-stu-id="ba825-153">**Number of attempts:** *1*</span></span>

1. <span data-ttu-id="ba825-154">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-154">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="ba825-155">在列表窗格中，选择名为 *周期盘点盲目* 的记录。</span><span class="sxs-lookup"><span data-stu-id="ba825-155">In the list pane, select the record that is named *Cycle Count Blind*.</span></span> <span data-ttu-id="ba825-156">如果没有现有记录具有此名称，则创建它。</span><span class="sxs-lookup"><span data-stu-id="ba825-156">If no existing record has this name, create it.</span></span> <span data-ttu-id="ba825-157">确认或设置记录的以下值：</span><span class="sxs-lookup"><span data-stu-id="ba825-157">Confirm or set the following values for the record:</span></span>

    - <span data-ttu-id="ba825-158">**菜单项名称**：*周期盘点盲目*</span><span class="sxs-lookup"><span data-stu-id="ba825-158">**Menu item name:** *Cycle Count Blind*</span></span>
    - <span data-ttu-id="ba825-159">**标题**：*周期盘点盲目*</span><span class="sxs-lookup"><span data-stu-id="ba825-159">**Title:** *Cycle Count Blind*</span></span>
    - <span data-ttu-id="ba825-160">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="ba825-160">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ba825-161">**使用现有工作**：*是*</span><span class="sxs-lookup"><span data-stu-id="ba825-161">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="ba825-162">**导向方式**：*周期盘点分组*（此值指示工作人员可以对特定于库位、区域或工作池的周期盘点工作 ID 进行分组。）</span><span class="sxs-lookup"><span data-stu-id="ba825-162">**Directed by:** *Cycle count grouping* (This value indicates that the worker can group cycle counting work IDs that are specific to a location, zone, or work pool.)</span></span>

1. <span data-ttu-id="ba825-163">在操作窗格上，选择 **周期盘点**。</span><span class="sxs-lookup"><span data-stu-id="ba825-163">On the Action Pane, select **Cycle counting**.</span></span>
1. <span data-ttu-id="ba825-164">在 **移动设备周期盘点** 对话框中，确认或设置以下值：</span><span class="sxs-lookup"><span data-stu-id="ba825-164">In the **Mobile device cycle counting** dialog box, confirm or set the following values:</span></span>

    - <span data-ttu-id="ba825-165">**显示物料编号**：*否*</span><span class="sxs-lookup"><span data-stu-id="ba825-165">**Display item number:** *No*</span></span>
    - <span data-ttu-id="ba825-166">**显示牌照**：*否*</span><span class="sxs-lookup"><span data-stu-id="ba825-166">**Display license plate:** *No*</span></span>
    - <span data-ttu-id="ba825-167">**尝试次数**：*0*</span><span class="sxs-lookup"><span data-stu-id="ba825-167">**Number of attempts:** *0*</span></span>

1. <span data-ttu-id="ba825-168">选择 **确定** 关闭对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-168">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="ba825-169">在列表窗格中，选择名为 *现场盘点* 的记录。</span><span class="sxs-lookup"><span data-stu-id="ba825-169">In the list pane, select the record that is named *Spot Counting*.</span></span> <span data-ttu-id="ba825-170">如果没有现有记录具有此名称，则创建它。</span><span class="sxs-lookup"><span data-stu-id="ba825-170">If no existing record has this name, create it.</span></span> <span data-ttu-id="ba825-171">确认或设置记录的以下值：</span><span class="sxs-lookup"><span data-stu-id="ba825-171">Confirm or set the following values for the record:</span></span>

    - <span data-ttu-id="ba825-172">**菜单项名称**：*现场盘点*</span><span class="sxs-lookup"><span data-stu-id="ba825-172">**Menu item name:** *Spot Counting*</span></span>
    - <span data-ttu-id="ba825-173">**标题**：*现场盘点*</span><span class="sxs-lookup"><span data-stu-id="ba825-173">**Title:** *Spot Counting*</span></span>
    - <span data-ttu-id="ba825-174">\**模式：\*\*\*工作*</span><span class="sxs-lookup"><span data-stu-id="ba825-174">**Mode:** *Work*</span></span>
    - <span data-ttu-id="ba825-175">**使用现有工作**：*否*</span><span class="sxs-lookup"><span data-stu-id="ba825-175">**Use existing work:** *No*</span></span>
    - <span data-ttu-id="ba825-176">**工作创建流程**：*现场周期盘点*（此值指示工作人员可以随时盘点一个仓库库位中的物料，而无需创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-176">**Work creation process:** *Spot cycle counting* (This value indicates that the worker can count items in a warehouse location at any time, without creating cycle counting work.</span></span> <span data-ttu-id="ba825-177">若要在库位中执行现场周期盘点，工作人员输入库位 ID。）</span><span class="sxs-lookup"><span data-stu-id="ba825-177">To do spot cycle counting in a location, the worker enters the location ID.)</span></span>

1. <span data-ttu-id="ba825-178">转到 **仓库管理 \> 设置 \> 移动设备 \> 移动设备菜单**。</span><span class="sxs-lookup"><span data-stu-id="ba825-178">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="ba825-179">在列表窗格中，选择名为 *库存* 的记录。</span><span class="sxs-lookup"><span data-stu-id="ba825-179">In the list pane, select the record that is named *Inventory*.</span></span> <span data-ttu-id="ba825-180">如果没有现有记录具有此名称，则创建它。</span><span class="sxs-lookup"><span data-stu-id="ba825-180">If no existing record has this name, create it.</span></span> <span data-ttu-id="ba825-181">确认以下周期盘点菜单项显示在 **菜单结构** 列中：</span><span class="sxs-lookup"><span data-stu-id="ba825-181">Confirm that the following cycle counting menu items appear in the **Menu structure** column:</span></span>

    - <span data-ttu-id="ba825-182">周期盘点</span><span class="sxs-lookup"><span data-stu-id="ba825-182">Cycle Count</span></span>
    - <span data-ttu-id="ba825-183">周期盘点盲目</span><span class="sxs-lookup"><span data-stu-id="ba825-183">Cycle Count Blind</span></span>
    - <span data-ttu-id="ba825-184">现场盘点</span><span class="sxs-lookup"><span data-stu-id="ba825-184">Spot counting</span></span>

1. <span data-ttu-id="ba825-185">转到 **仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="ba825-185">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="ba825-186">在 **周期盘点** 选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="ba825-186">On the **Cycle counting** tab, set the following values:</span></span>

    - <span data-ttu-id="ba825-187">**默认周期盘点调整类型**：*周期盘点*（此字段指定完成周期盘点时过帐的日记帐类型。）</span><span class="sxs-lookup"><span data-stu-id="ba825-187">**Default cycle counting adjustment type:** *Cycle Count* (This field specifies the journal type that is posted when cycle counting is done.)</span></span>
    - <span data-ttu-id="ba825-188">**默认周期盘点工作类 ID**：*CCount*（此字段指定用于周期盘点的工作类。）</span><span class="sxs-lookup"><span data-stu-id="ba825-188">**Default cycle counting work class ID:** *CCount* (This field specifies the work class that is used for cycle counting.)</span></span>
    - <span data-ttu-id="ba825-189">**默认周期盘点工作优先级**：*50*（此字段设置周期盘点工作相对于仓库中其他类型工作的优先级。</span><span class="sxs-lookup"><span data-stu-id="ba825-189">**Default cycle count work priority:** *50* (This field sets the priority that cycle counting work has relative to other types of work in the warehouse.</span></span> <span data-ttu-id="ba825-190">通过输入小于为其他类型工作输入的数量的数字，提升周期盘点工作的优先级。）</span><span class="sxs-lookup"><span data-stu-id="ba825-190">By entering a number that is lower than the number that is entered for other types of work, you raise the priority of the cycle counting work.)</span></span>

1. <span data-ttu-id="ba825-191">转到 **仓库管理 \> 设置 \> 库存 \> 调整类型**。</span><span class="sxs-lookup"><span data-stu-id="ba825-191">Go to **Warehouse management \> Setup \> Inventory \> Adjustment types**.</span></span>
1. <span data-ttu-id="ba825-192">**调整类型** 页面允许您为可能发生的不同调入和调出创建代码。</span><span class="sxs-lookup"><span data-stu-id="ba825-192">The **Adjustment types** page lets you create codes for the different in and out adjustments that might occur.</span></span> <span data-ttu-id="ba825-193">确认存在具有以下设置的记录：</span><span class="sxs-lookup"><span data-stu-id="ba825-193">Confirm that a record exists that has the following settings:</span></span>

    - <span data-ttu-id="ba825-194">**库存调整类型**：*周期盘点*</span><span class="sxs-lookup"><span data-stu-id="ba825-194">**Inventory adjustment type:** *Cycle Count*</span></span>
    - <span data-ttu-id="ba825-195">**描述**：*周期盘点*</span><span class="sxs-lookup"><span data-stu-id="ba825-195">**Description:** *Cycle Count*</span></span>
    - <span data-ttu-id="ba825-196">**名称**：*ICnt*</span><span class="sxs-lookup"><span data-stu-id="ba825-196">**Name:** *ICnt*</span></span>

1. <span data-ttu-id="ba825-197">转到 **仓库管理 \> 设置 \> 仓库设置 \> 仓库**。</span><span class="sxs-lookup"><span data-stu-id="ba825-197">Go to **Warehouse management \> Setup \> Warehouse setup \> Warehouses**.</span></span>
1. <span data-ttu-id="ba825-198">在列表窗格中，选择仓库 *61*。</span><span class="sxs-lookup"><span data-stu-id="ba825-198">In the list pane, select warehouse *61*.</span></span> <span data-ttu-id="ba825-199">如果没有现有记录具有此名称，则创建它。</span><span class="sxs-lookup"><span data-stu-id="ba825-199">If no existing record has this name, create it.</span></span>
1. <span data-ttu-id="ba825-200">在 **仓库** 快速选项卡上，设置以下值：</span><span class="sxs-lookup"><span data-stu-id="ba825-200">On the **Warehouse** FastTab, set the following values:</span></span>

    - <span data-ttu-id="ba825-201">**使用仓库管理流程**：*是*（此值为仓库管理流程启用仓库。）</span><span class="sxs-lookup"><span data-stu-id="ba825-201">**Use warehouse management process:** *Yes* (This value enables the warehouse for warehouse management processes.)</span></span>
    - <span data-ttu-id="ba825-202">**允许在周期盘点期间移动牌照**：*是*（此值使工作人员可以在周期盘点期间移动牌照。）</span><span class="sxs-lookup"><span data-stu-id="ba825-202">**Allow license plate moves during cycle counting:** *Yes* (This value enables workers to move license plates during a cycle count.)</span></span>

## <a name="scenario-1-guided-cycle-counting"></a><span data-ttu-id="ba825-203">场景 1：指导周期盘点</span><span class="sxs-lookup"><span data-stu-id="ba825-203">Scenario 1: Guided cycle counting</span></span>

<span data-ttu-id="ba825-204">您必须创建一些工作，才能进行指导周期盘点。</span><span class="sxs-lookup"><span data-stu-id="ba825-204">Before guided cycle counting can occur, you must create some work.</span></span> <span data-ttu-id="ba825-205">此工作将指导整个仓库中不同库位的分配人员完成在工作中设置的盘点。</span><span class="sxs-lookup"><span data-stu-id="ba825-205">This work will guide the assigned person through the warehouse, from location to location, to complete the counts that are set up in the work.</span></span>

### <a name="create-cycle-counting-work-for-scenario-1"></a><span data-ttu-id="ba825-206">为场景 1 创建周期盘点工作</span><span class="sxs-lookup"><span data-stu-id="ba825-206">Create cycle counting work for scenario 1</span></span>

<span data-ttu-id="ba825-207">按照以下步骤为仓库 *61* 中的物料库位 *01A02R2S2B* (BULK-06) 创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-207">Follow these steps to create cycle counting work for item location *01A02R2S2B* (BULK-06) in warehouse *61*.</span></span>

1. <span data-ttu-id="ba825-208">转到 **仓库管理 \> 周期盘点 \> 按库位分类的周期盘点工作**。</span><span class="sxs-lookup"><span data-stu-id="ba825-208">Go to **Warehouse management \> Cycle counting \> Cycle count work by location**.</span></span>
1. <span data-ttu-id="ba825-209">在 **按库位创建周期盘点工作** 对话框中，将 **工作池 ID** 字段设置为 *CycleCount*。</span><span class="sxs-lookup"><span data-stu-id="ba825-209">In the **Create cycle count work by location** dialog box, set the **Work pool ID** field to *CycleCount*.</span></span>
1. <span data-ttu-id="ba825-210">在 **要包括的记录** 快速选项卡中，选择 **筛选**。</span><span class="sxs-lookup"><span data-stu-id="ba825-210">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="ba825-211">在查询编辑器对话框中的 **范围** 选项卡上，按照以下步骤操作：</span><span class="sxs-lookup"><span data-stu-id="ba825-211">In the query editor dialog box, on the **Range** tab, follow these steps:</span></span>

    - <span data-ttu-id="ba825-212">对于 **字段** 字段设置为 *仓库* 的行，将 **条件** 字段设置为 *61*。</span><span class="sxs-lookup"><span data-stu-id="ba825-212">For the row where the **Field** field is set to *Warehouse*, set the **Criteria** field to *61*.</span></span>
    - <span data-ttu-id="ba825-213">对于 **字段** 字段设置为 *库位* 的行，将 **条件** 字段设置为 *01A02R2S2B*。</span><span class="sxs-lookup"><span data-stu-id="ba825-213">For the row where the **Field** field is set to *Location,* set the **Criteria** field to *01A02R2S2B*.</span></span>

1. <span data-ttu-id="ba825-214">选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-214">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ba825-215">选择 **确定** 以关闭 **按库位创建周期盘点工作** 对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-215">Select **OK** to close the **Create cycle count work by location** dialog box.</span></span>

    <span data-ttu-id="ba825-216">完成工作创建流程后，操作中心中会显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="ba825-216">When the work creation process is completed, a message appears in the Action center.</span></span>

1. <span data-ttu-id="ba825-217">转到 **仓库管理 \> 工作 \> 工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="ba825-217">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ba825-218">通过在 **工作池 ID** 列上设置筛选器以查找值为 *CycleCount* 的记录，找到最新创建的工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-218">Find the newly created work by setting a filter on the **Work pool ID** column to find records that have a value of *CycleCount*.</span></span>

### <a name="do-cycle-counting-work-for-scenario-1"></a><span data-ttu-id="ba825-219">为场景 1 执行周期盘点工作</span><span class="sxs-lookup"><span data-stu-id="ba825-219">Do cycle counting work for scenario 1</span></span>

<span data-ttu-id="ba825-220">创建周期盘点工作后，您通过盘点仓库库位中的物料，然后使用移动设备在 Supply Chain Management 中输入结果来执行工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-220">After you've created the cycle counting work, you do the work by counting items in a warehouse location and then using a mobile device to enter the results in Supply Chain Management.</span></span> <span data-ttu-id="ba825-221">按照以下步骤在 Warehouse Management 移动应用中执行周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-221">Follow these steps to do the cycle counting work in the Warehouse Management mobile app.</span></span>

1. <span data-ttu-id="ba825-222">以您在本主题前面的[为场景准备演示数据](#prepare-demo-data)部分中设置的工作用户身份登录到 Warehouse Management 移动应用。</span><span class="sxs-lookup"><span data-stu-id="ba825-222">Sign in to the Warehouse Management mobile app as the work user that you set up in the [Prepare demo data for the scenarios](#prepare-demo-data) section earlier in this topic.</span></span> <span data-ttu-id="ba825-223">对于本主题中的示例，用户名为 *Julia Funderburk* 并针对仓库 *61* 进行设置。</span><span class="sxs-lookup"><span data-stu-id="ba825-223">For the example in this topic, the user is named *Julia Funderburk* and is set up for warehouse *61*.</span></span> <span data-ttu-id="ba825-224">（USMF 演示数据应该允许您通过输入 *61* 作为用户 ID 和 *1* 作为密码来以此工作用户身份登录。）</span><span class="sxs-lookup"><span data-stu-id="ba825-224">(The USMF demo data should let you sign in as this work user by entering *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="ba825-225">在主菜单上，选择 **库存**。</span><span class="sxs-lookup"><span data-stu-id="ba825-225">On the main menu, select **Inventory**.</span></span>
1. <span data-ttu-id="ba825-226">在 **库存** 菜单上，选择 **周期盘点指导**。</span><span class="sxs-lookup"><span data-stu-id="ba825-226">On the **Inventory** menu, select **Cycle Count Guided**.</span></span>
1. <span data-ttu-id="ba825-227">选择 **数量** 字段，使用数字键盘输入 *9*，然后选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-227">Select the **Qty** field, enter *9* by using the number pad, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ba825-228">系统希望您为该物料、库位和牌照输入 10 件的盘点数量。</span><span class="sxs-lookup"><span data-stu-id="ba825-228">The system was expecting you to enter a count of 10 pieces for this item, location, and license plate.</span></span> <span data-ttu-id="ba825-229">因此，系统将要求您重新盘点。</span><span class="sxs-lookup"><span data-stu-id="ba825-229">Therefore, you're asked to recount.</span></span> <span data-ttu-id="ba825-230">选择 **数量** 字段，再次使用数字键盘输入 *9*，然后选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-230">Select the **Qty** field, enter *9* again by using the number pad, and then select **OK** (the check mark button).</span></span> <span data-ttu-id="ba825-231">在第二次尝试时，您的盘点将被接受。</span><span class="sxs-lookup"><span data-stu-id="ba825-231">On the second attempt, your count will be accepted.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ba825-232">当系统检测到预期的现有数量与您输入的数量之间存在差异时，它会要求您执行第二次盘点，因为 **周期盘点指导** 移动设备菜单项的 **尝试次数** 字段设置为 *1*。</span><span class="sxs-lookup"><span data-stu-id="ba825-232">When the system detected a difference between the expected on-hand quantity and the quantity that you entered, it asked you to count a second time because the **Number of attempts** field is set to *1* for the **Cycle Count Guided** mobile device menu item.</span></span> <span data-ttu-id="ba825-233">您将导向到特定物料编号和牌照编号，因为移动设备菜单项的 **显示物料编号** 选项和 **显示牌照** 选项都设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="ba825-233">You were guided to a specific item number and license plate number because both the **Display item number** option and the **Display license plate** option are set to *Yes* for the mobile device menu item.</span></span>

1. <span data-ttu-id="ba825-234">选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-234">Select **OK** (the check mark button).</span></span>

### <a name="review-the-cycle-counting-differences-for-scenario-1"></a><span data-ttu-id="ba825-235">审查场景 1 的周期盘点差异</span><span class="sxs-lookup"><span data-stu-id="ba825-235">Review the cycle counting differences for scenario 1</span></span>

<span data-ttu-id="ba825-236">按照以下步骤审查周期盘点差异。</span><span class="sxs-lookup"><span data-stu-id="ba825-236">Follow these steps to review the cycle counting differences.</span></span>

1. <span data-ttu-id="ba825-237">返回到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="ba825-237">Return to Supply Chain Management.</span></span>
1. <span data-ttu-id="ba825-238">转到 **仓库管理 \> 工作 \> 工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="ba825-238">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ba825-239">查找并选择您之前查看的周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-239">Find and select the cycle counting work that you looked at earlier.</span></span> <span data-ttu-id="ba825-240">（例如，在 **工作池 ID** 列上设置筛选器以查找值为 *CycleCount* 的记录。）请注意，此工作的 **工作状态** 字段现在设置为 *待审查*。</span><span class="sxs-lookup"><span data-stu-id="ba825-240">(For example, set a filter on the **Work pool ID** column to find records that have a value of *CycleCount*.) Notice that the **Work status** field for this work is now set to *Pending review*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ba825-241">对于用于执行盘点工作的工作用户帐户，**周期盘点主管** 选项设置为 *否*，**最大百分比限制**、**最大数量限制** 和 **最大值限制** 字段都设置为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="ba825-241">For the work user account that you used to do the counting work, the **Cycle count supervisor** option is set to *No*, and the **Maximum percentage limit**, **Maximum quantity limit**, and **Maximum value limit** fields are all set to *0* (zero).</span></span> <span data-ttu-id="ba825-242">因此，此用户报告的所有盘点差异都必须手动批准，并且相关工作的 **工作状态** 字段设置为 *待审查*。</span><span class="sxs-lookup"><span data-stu-id="ba825-242">Therefore, all counting differences that this user reports must be manually approved, and the **Work status** field for the related work is set to *Pending review*.</span></span> <span data-ttu-id="ba825-243">如果盘点的值在偏差限制范围内（如 **工作用户** 页面上的 **最大百分比限制** 或 **最大数量限制** 字段所指定），或者如果用户的 **周期盘点主管** 选项已设置为 *是*，则工作会自动关闭。</span><span class="sxs-lookup"><span data-stu-id="ba825-243">If the counted value were within the deviation limits (as specified in the **Maximum percentage limit** or **Maximum quantity limit** fields on the **Work users** page), or if the **Cycle count supervisor** option were set to *Yes* for the user, the work would have automatically been closed.</span></span>

1. <span data-ttu-id="ba825-244">在操作窗格上的 **工作** 选项卡上，选择 **周期盘点**。</span><span class="sxs-lookup"><span data-stu-id="ba825-244">On the Action Pane, on the **Work** tab, select **Cycle counting**.</span></span>
1. <span data-ttu-id="ba825-245">在操作窗格上，选择 **接受盘点**。</span><span class="sxs-lookup"><span data-stu-id="ba825-245">On the Action Pane, select **Accept count**.</span></span>

    <span data-ttu-id="ba825-246">使用标准盘点日记帐过帐差异，并创建新的工作订单。</span><span class="sxs-lookup"><span data-stu-id="ba825-246">The difference is posted by using the standard counting journal, and a new work order is created.</span></span>

1. <span data-ttu-id="ba825-247">在 **周期盘点交易** 页面上的操作窗格上，选择 **派生工作** 以查找已为批准的差异创建的工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-247">On the **Cycle counting transactions** page, on the Action Pane, select **Derived work** to find the work that was created for the approved difference.</span></span>

## <a name="scenario-2-blind-cycle-counting"></a><span data-ttu-id="ba825-248">场景 2：盲目周期盘点</span><span class="sxs-lookup"><span data-stu-id="ba825-248">Scenario 2: Blind cycle counting</span></span>

<span data-ttu-id="ba825-249">此场景要求已在您的系统中完成场景 1。</span><span class="sxs-lookup"><span data-stu-id="ba825-249">This scenario requires that scenario 1 already be completed in your system.</span></span>

### <a name="create-cycle-counting-work-for-scenario-2"></a><span data-ttu-id="ba825-250">为场景 2 创建周期盘点工作</span><span class="sxs-lookup"><span data-stu-id="ba825-250">Create cycle counting work for scenario 2</span></span>

<span data-ttu-id="ba825-251">您必须创建一些工作，才能进行盲目周期盘点。</span><span class="sxs-lookup"><span data-stu-id="ba825-251">Before blind cycle counting can occur, you must create some work.</span></span> <span data-ttu-id="ba825-252">按照以下步骤为仓库 *61* 中的物料库位 *01A02R2S2B* (BULK-06) 创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-252">Follow these steps to create cycle counting work for item location *01A02R2S2B* (BULK-06) in warehouse *61*.</span></span>

1. <span data-ttu-id="ba825-253">转到 **仓库管理 \> 周期盘点 \> 按物料分类的周期盘点工作**。</span><span class="sxs-lookup"><span data-stu-id="ba825-253">Go to **Warehouse management \> Cycle counting \> Cycle count work by item**.</span></span>
1. <span data-ttu-id="ba825-254">在 **按物料创建周期盘点工作** 对话框中，将 **工作池 ID** 字段设置为 *CycleCount*。</span><span class="sxs-lookup"><span data-stu-id="ba825-254">In the **Create cycle count work by item** dialog box, set the **Work pool ID** field to *CycleCount*.</span></span>
1. <span data-ttu-id="ba825-255">在 **要包括的记录** 快速选项卡中，选择 **筛选**。</span><span class="sxs-lookup"><span data-stu-id="ba825-255">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="ba825-256">在查询编辑器对话框的 **范围** 选项卡上，添加具有以下设置的三个行：</span><span class="sxs-lookup"><span data-stu-id="ba825-256">In the query editor dialog box, on the **Range** tab, add three rows that have the following settings:</span></span>

    - <span data-ttu-id="ba825-257">行 1：</span><span class="sxs-lookup"><span data-stu-id="ba825-257">Row 1:</span></span>

        - <span data-ttu-id="ba825-258">\**表：\*\*\*物料*</span><span class="sxs-lookup"><span data-stu-id="ba825-258">**Table:** *Items*</span></span>
        - <span data-ttu-id="ba825-259">\**字段：\*\*\*物料编号*</span><span class="sxs-lookup"><span data-stu-id="ba825-259">**Field:** *Item number*</span></span>
        - <span data-ttu-id="ba825-260">**条件：** *L0101*</span><span class="sxs-lookup"><span data-stu-id="ba825-260">**Criteria:** *L0101*</span></span>

    - <span data-ttu-id="ba825-261">行 2：</span><span class="sxs-lookup"><span data-stu-id="ba825-261">Row 2:</span></span>

        - <span data-ttu-id="ba825-262">**表**：*库存维度*</span><span class="sxs-lookup"><span data-stu-id="ba825-262">**Table:** *Inventory dimensions*</span></span>
        - <span data-ttu-id="ba825-263">**字段**：*仓库*</span><span class="sxs-lookup"><span data-stu-id="ba825-263">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="ba825-264">**条件**：*61*</span><span class="sxs-lookup"><span data-stu-id="ba825-264">**Criteria:** *61*</span></span>

    - <span data-ttu-id="ba825-265">行 3：</span><span class="sxs-lookup"><span data-stu-id="ba825-265">Row 3:</span></span>

        - <span data-ttu-id="ba825-266">**表**：*库存维度*</span><span class="sxs-lookup"><span data-stu-id="ba825-266">**Table:** *Inventory dimensions*</span></span>
        - <span data-ttu-id="ba825-267">**字段**：*货位*</span><span class="sxs-lookup"><span data-stu-id="ba825-267">**Field:** *Location*</span></span>
        - <span data-ttu-id="ba825-268">**条件：** *01A02R2S2B*</span><span class="sxs-lookup"><span data-stu-id="ba825-268">**Criteria:** *01A02R2S2B*</span></span>

1. <span data-ttu-id="ba825-269">选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-269">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ba825-270">选择 **确定** 以关闭 **按物料创建周期盘点工作** 对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-270">Select **OK** to close the **Create cycle count work by item** dialog box.</span></span>

    <span data-ttu-id="ba825-271">完成工作创建流程后，您将收到一条信息性消息。</span><span class="sxs-lookup"><span data-stu-id="ba825-271">When the work creation process is completed, you receive an informational message.</span></span>

### <a name="do-cycle-counting-work-for-scenario-2"></a><span data-ttu-id="ba825-272">为场景 2 执行周期盘点工作</span><span class="sxs-lookup"><span data-stu-id="ba825-272">Do cycle counting work for scenario 2</span></span>

<span data-ttu-id="ba825-273">创建周期盘点工作后，按照以下步骤在 Warehouse Management 移动应用中执行工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-273">After you've created the cycle counting work, following these steps to do the work in the Warehouse Management mobile app.</span></span>

1. <span data-ttu-id="ba825-274">以您在本主题前面的[为场景准备演示数据](#prepare-demo-data)部分中设置的工作用户身份登录到 Warehouse Management 移动应用。</span><span class="sxs-lookup"><span data-stu-id="ba825-274">Sign in to the Warehouse Management mobile app as the work user that you set up in the [Prepare demo data for the scenarios](#prepare-demo-data) section earlier in this topic.</span></span> <span data-ttu-id="ba825-275">对于本主题中的示例，用户名为 *Julia Funderburk* 并针对仓库 *61* 进行设置。</span><span class="sxs-lookup"><span data-stu-id="ba825-275">For the example in this topic, the user is named *Julia Funderburk* and is set up for warehouse *61*.</span></span> <span data-ttu-id="ba825-276">（USMF 演示数据应该允许您通过输入 *61* 作为用户 ID 和 *1* 作为密码来以此工作用户身份登录。）</span><span class="sxs-lookup"><span data-stu-id="ba825-276">(The USMF demo data should let you sign in as this work user by entering *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="ba825-277">在主菜单上，选择 **库存**。</span><span class="sxs-lookup"><span data-stu-id="ba825-277">On the main menu, select **Inventory**.</span></span>
1. <span data-ttu-id="ba825-278">在 **库存** 菜单上，选择 **周期盘点盲目**。</span><span class="sxs-lookup"><span data-stu-id="ba825-278">On the **Inventory** menu, select **Cycle Count Blind**.</span></span>
1. <span data-ttu-id="ba825-279">选择 **区域 ID** 字段，输入 *BULK06*，然后选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-279">Select the **Zone ID** field, enter *BULK06*, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ba825-280">选择 **物料** 字段，输入 *L0101*，然后选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-280">Select the **Item** field, enter *L0101*, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ba825-281">选择 **牌照** 字段，输入 *LP\_BULK\_06\_01*，然后选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-281">Select the **License plate** field, enter *LP\_BULK\_06\_01*, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ba825-282">选择 **数量** 字段，输入 *10*，然后选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-282">Select the **Qty** field, enter *10*, and then select **OK** (the check mark button).</span></span>

    > [!NOTE]
    > <span data-ttu-id="ba825-283">即使系统检测到预期的现有数量与您扫描的数量之间存在差异，但它不会要求您执行第二次盘点，因为 **周期盘点盲目** 移动设备菜单项的 **尝试次数** 字段设置为 *0*（零）。</span><span class="sxs-lookup"><span data-stu-id="ba825-283">Even though the system detected a difference between the expected on-hand quantity and the quantity that you scanned, it didn't ask you to count a second time because the **Number of attempts** field is set to *0* (zero) for the **Cycle Count Blind** mobile device menu item.</span></span> <span data-ttu-id="ba825-284">系统要求您扫描物料编号和牌照，因为移动设备菜单项的 **显示物料编号** 选项和 **显示牌照** 选项都设置为 *否*。</span><span class="sxs-lookup"><span data-stu-id="ba825-284">You were asked to scan the item number and license plate because both the **Display item number** option and the **Display license plate** option are set to *No* for the mobile device menu item.</span></span>

1. <span data-ttu-id="ba825-285">选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-285">Select **OK** (the check mark button).</span></span>

### <a name="review-the-cycle-counting-differences-for-scenario-2"></a><span data-ttu-id="ba825-286">审查场景 2 的周期盘点差异</span><span class="sxs-lookup"><span data-stu-id="ba825-286">Review the cycle counting differences for scenario 2</span></span>

<span data-ttu-id="ba825-287">按照以下步骤审查周期盘点差异。</span><span class="sxs-lookup"><span data-stu-id="ba825-287">Follow these steps to review the cycle counting differences.</span></span>

1. <span data-ttu-id="ba825-288">返回到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="ba825-288">Return to Supply Chain Management.</span></span>
1. <span data-ttu-id="ba825-289">转到 **仓库管理 \> 常用 \> 工作 \> 周期盘点工作待审查**。</span><span class="sxs-lookup"><span data-stu-id="ba825-289">Go to **Warehouse management \> Common \> Work \> Cycle count work pending review**.</span></span>
1. <span data-ttu-id="ba825-290">在操作窗格上的 **工作** 选项卡上，选择 **周期盘点**。</span><span class="sxs-lookup"><span data-stu-id="ba825-290">On the Action Pane, on the **Work** tab, select **Cycle counting**.</span></span>
1. <span data-ttu-id="ba825-291">在操作窗格上，选择 **拒绝盘点**。</span><span class="sxs-lookup"><span data-stu-id="ba825-291">On the Action Pane, select **Reject count**.</span></span>

    <span data-ttu-id="ba825-292">由于盘点差异遭拒绝，因此关闭工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-292">Because the counting difference was rejected, the work is closed.</span></span>

## <a name="scenario-3-spot-cycle-counting"></a><span data-ttu-id="ba825-293">场景 3：现场周期盘点</span><span class="sxs-lookup"><span data-stu-id="ba825-293">Scenario 3: Spot cycle counting</span></span>

<span data-ttu-id="ba825-294">现有记录表明物料 *L0101* 在库位 *01A02R2S2B* 有现有数量。</span><span class="sxs-lookup"><span data-stu-id="ba825-294">The on-hand record states that there is an on-hand quantity of item *L0101* at location *01A02R2S2B*.</span></span> <span data-ttu-id="ba825-295">仓库工作人员在库位 *01A02R2S1B* 处。</span><span class="sxs-lookup"><span data-stu-id="ba825-295">The warehouse worker is at location *01A02R2S1B*.</span></span> <span data-ttu-id="ba825-296">虽然此库位应该为空，但它已满。</span><span class="sxs-lookup"><span data-stu-id="ba825-296">Although this location should be empty, it's full.</span></span> <span data-ttu-id="ba825-297">因此，仓库工作人员会立即对该库位进行现场盘点。</span><span class="sxs-lookup"><span data-stu-id="ba825-297">Therefore, the warehouse worker immediately does a spot count of this location.</span></span>

### <a name="do-cycle-counting-work-for-scenario-3"></a><span data-ttu-id="ba825-298">为场景 3 执行周期盘点工作</span><span class="sxs-lookup"><span data-stu-id="ba825-298">Do cycle counting work for scenario 3</span></span>

<span data-ttu-id="ba825-299">按照以下步骤在 Warehouse Management 移动应用中执行周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-299">Follow these steps to do the cycle counting work in the Warehouse Management mobile app.</span></span>

1. <span data-ttu-id="ba825-300">以您在本主题前面的[为场景准备演示数据](#prepare-demo-data)部分中设置的工作用户身份登录到 Warehouse Management 移动应用。</span><span class="sxs-lookup"><span data-stu-id="ba825-300">Sign in to the Warehouse Management mobile app as the work user that you set up in the [Prepare demo data for the scenarios](#prepare-demo-data) section earlier in this topic.</span></span> <span data-ttu-id="ba825-301">对于本主题中的示例，用户名为 *Julia Funderburk* 并针对仓库 *61* 进行设置。</span><span class="sxs-lookup"><span data-stu-id="ba825-301">For the example in this topic, the user is named *Julia Funderburk* and is set up for warehouse *61*.</span></span> <span data-ttu-id="ba825-302">（USMF 演示数据应该允许您通过输入 *61* 作为用户 ID 和 *1* 作为密码来以此工作用户身份登录。）</span><span class="sxs-lookup"><span data-stu-id="ba825-302">(The USMF demo data should let you sign in as this work user by entering *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="ba825-303">在主菜单上，选择 **库存**。</span><span class="sxs-lookup"><span data-stu-id="ba825-303">On the main menu, select **Inventory**.</span></span>
1. <span data-ttu-id="ba825-304">在 **库存** 菜单上，选择 **现场盘点**。</span><span class="sxs-lookup"><span data-stu-id="ba825-304">On the **Inventory** menu, select **Spot counting**.</span></span>
1. <span data-ttu-id="ba825-305">选择 **库位** 字段，输入 *01A02R2S1B*，然后选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-305">Select the **Location** field, enter *01A02R2S1B*, and then select **OK** (the check mark button).</span></span>

    <span data-ttu-id="ba825-306">系统检测到在 Supply Chain Management 中该库位为空。</span><span class="sxs-lookup"><span data-stu-id="ba825-306">The system detects that the location is empty in Supply Chain Management.</span></span>

1. <span data-ttu-id="ba825-307">选择 **添加牌照或物料**。</span><span class="sxs-lookup"><span data-stu-id="ba825-307">Select **Add LP or Item**.</span></span>
1. <span data-ttu-id="ba825-308">选择 **物料** 字段，输入 *L0101*，然后选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-308">Select the **Item** field, enter *L0101*, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ba825-309">选择 **牌照** 字段，输入 *LP\_BULK\_06\_01*，然后选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-309">Select the **License plate** field, enter *LP\_BULK\_06\_01*, and then select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="ba825-310">选择 **数量** 字段，输入 *9*，然后选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-310">Select the **Qty** field, enter *9*, and then select **OK** (the check mark button).</span></span>

    <span data-ttu-id="ba825-311">因为系统检测到指定的牌照已在 Supply Chain Management 中的另一个库位可用，因此该牌照将移动到当前库位。</span><span class="sxs-lookup"><span data-stu-id="ba825-311">Because the system detects that the specified license plate is already available at another location in Supply Chain Management, that license plate will be moved to the current location.</span></span> <span data-ttu-id="ba825-312">因此，系统会要求您确认移动。</span><span class="sxs-lookup"><span data-stu-id="ba825-312">Therefore, the system asks you to confirm the movement.</span></span>

1. <span data-ttu-id="ba825-313">选择 **确定**（复选标记按钮）。</span><span class="sxs-lookup"><span data-stu-id="ba825-313">Select **OK** (the check mark button).</span></span>

### <a name="review-the-cycle-counting-differences-for-scenario-3"></a><span data-ttu-id="ba825-314">审查场景 3 的周期盘点差异</span><span class="sxs-lookup"><span data-stu-id="ba825-314">Review the cycle counting differences for scenario 3</span></span>

<span data-ttu-id="ba825-315">按照以下步骤审查盘点结果。</span><span class="sxs-lookup"><span data-stu-id="ba825-315">Follow these steps to review the counting results.</span></span>

1. <span data-ttu-id="ba825-316">返回到 Supply Chain Management。</span><span class="sxs-lookup"><span data-stu-id="ba825-316">Return to Supply Chain Management.</span></span>
1. <span data-ttu-id="ba825-317">转到 **仓库管理 \> 常用 \> 工作详细信息**。</span><span class="sxs-lookup"><span data-stu-id="ba825-317">Go to **Warehouse management \> Common \> Work details**.</span></span>
1. <span data-ttu-id="ba825-318">选中网格顶部的 **显示已关闭** 复选框。</span><span class="sxs-lookup"><span data-stu-id="ba825-318">Select the **Show closed** checkbox at the top of the grid.</span></span>
1. <span data-ttu-id="ba825-319">将 **工作订单类型** 列的筛选器设置为 *库存移动*。</span><span class="sxs-lookup"><span data-stu-id="ba825-319">Set the filter for the **Work order type** column to *Inventory movement*.</span></span>

    <span data-ttu-id="ba825-320">系统自动将此盘点检测为库存移动。</span><span class="sxs-lookup"><span data-stu-id="ba825-320">The system automatically detected this count as an inventory movement.</span></span> <span data-ttu-id="ba825-321">允许此移动，因为在 **仓库** 页面上，仓库 *61* 的 **允许在周期盘点期间移动牌照** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="ba825-321">This movement is permitted because the **Allow license plate moves during cycle counting** option is set to *Yes* for warehouse *61* on the **Warehouses** page.</span></span>

## <a name="scenario-4-define-cycle-count-thresholds"></a><span data-ttu-id="ba825-322">场景 4：定义周期盘点阈值</span><span class="sxs-lookup"><span data-stu-id="ba825-322">Scenario 4: Define cycle count thresholds</span></span>

<span data-ttu-id="ba825-323">创建周期盘点工作的一种方法是使用阈值。</span><span class="sxs-lookup"><span data-stu-id="ba825-323">One way to create cycle counting work is to use thresholds.</span></span> <span data-ttu-id="ba825-324">周期盘点阈值指示库存物料的数量或百分比限制。</span><span class="sxs-lookup"><span data-stu-id="ba825-324">A cycle count threshold indicates the quantity or percentage limit of inventory items.</span></span> <span data-ttu-id="ba825-325">当达到阈值时，会自动创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-325">Cycle counting work is automatically created when the threshold is reached.</span></span>

<span data-ttu-id="ba825-326">例如，一个库位的周期盘点阈值是 40，而物料数量是 60。</span><span class="sxs-lookup"><span data-stu-id="ba825-326">For example, there are 60 items in a location that has a cycle count threshold of 40.</span></span> <span data-ttu-id="ba825-327">在一次销售订单交易期间，有 25 个物料被从该场所领取并被放置在暂放库位。</span><span class="sxs-lookup"><span data-stu-id="ba825-327">During a sales order transaction, 25 items are picked from the location and put in a staging location.</span></span> <span data-ttu-id="ba825-328">因为新的物料数量 35 低于临界值，将自动为该库位创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-328">Because the new item count, 35, is less than the threshold quantity, cycle counting work is automatically created for the location.</span></span>

<span data-ttu-id="ba825-329">按照以下步骤设置周期盘点阈值。</span><span class="sxs-lookup"><span data-stu-id="ba825-329">Follow these steps to set up cycle count thresholds.</span></span>

1. <span data-ttu-id="ba825-330">转到 **仓库管理 \> 设置 \> 周期盘点 \> 周期盘点阈值**。</span><span class="sxs-lookup"><span data-stu-id="ba825-330">Go to **Warehouse management \> Setup \> Cycle counting \> Cycle count thresholds**.</span></span>
1. <span data-ttu-id="ba825-331">在操作窗格上，选择 **新建** 创建阈值，并为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="ba825-331">On the Action Pane, select **New** to create a threshold, and set the following values for it:</span></span>

    - <span data-ttu-id="ba825-332">**周期盘点阈值 ID**：*L0101*</span><span class="sxs-lookup"><span data-stu-id="ba825-332">**Cycle counting threshold ID:** *L0101*</span></span>
    - <span data-ttu-id="ba825-333">**描述**：*阈值 L0101*</span><span class="sxs-lookup"><span data-stu-id="ba825-333">**Description:** *Threshold L0101*</span></span>
    - <span data-ttu-id="ba825-334">**阈值数量**：*2*</span><span class="sxs-lookup"><span data-stu-id="ba825-334">**Threshold quantity:** *2*</span></span>
    - <span data-ttu-id="ba825-335">**单位：** *ea*</span><span class="sxs-lookup"><span data-stu-id="ba825-335">**Unit:** *ea*</span></span>
    - <span data-ttu-id="ba825-336">**基于百分比的产能阈值**：*0.00*</span><span class="sxs-lookup"><span data-stu-id="ba825-336">**Capacity threshold based on percentage:** *0.00*</span></span>
    - <span data-ttu-id="ba825-337">**周期盘点阈值类型**：*数量*</span><span class="sxs-lookup"><span data-stu-id="ba825-337">**Cycle counting threshold type:** *Quantity*</span></span>
    - <span data-ttu-id="ba825-338">**立即处理周期盘点**：*是*</span><span class="sxs-lookup"><span data-stu-id="ba825-338">**Process cycle count immediately:** *Yes*</span></span>
    - <span data-ttu-id="ba825-339">**周期盘点之间的天数**：*1*</span><span class="sxs-lookup"><span data-stu-id="ba825-339">**Days between cycle counting:** *1*</span></span>
    - <span data-ttu-id="ba825-340">**工作池 ID**：*CycleCount*</span><span class="sxs-lookup"><span data-stu-id="ba825-340">**Work pool ID:** *CycleCount*</span></span>

1. <span data-ttu-id="ba825-341">在操作窗格上，选择 **选择物料**。</span><span class="sxs-lookup"><span data-stu-id="ba825-341">On the Action Pane, select **Select items**.</span></span>
1. <span data-ttu-id="ba825-342">在查询编辑器对话框中的 **范围** 选项卡上，找到 **字段** 字段设置为 *物料编号* 的行。</span><span class="sxs-lookup"><span data-stu-id="ba825-342">In the query editor dialog box, on the **Range** tab, find the row where the **Field** field is set to *Item number*.</span></span> <span data-ttu-id="ba825-343">将该行的 **条件** 字段设置为 *L0101*。</span><span class="sxs-lookup"><span data-stu-id="ba825-343">Set the **Criteria** field for that row to *L0101*.</span></span>
1. <span data-ttu-id="ba825-344">选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-344">Select **OK** to close the query editor dialog box.</span></span>

    <span data-ttu-id="ba825-345">现在，您已为物料 *L0101* 定义了周期盘点阈值。</span><span class="sxs-lookup"><span data-stu-id="ba825-345">You've now defined a cycle count threshold for item *L0101*.</span></span>

<span data-ttu-id="ba825-346">现在，如果现有数量小于 2，并且如果任何库位的最后一个周期盘点的日期不是今天，将在该库位为物料 *L0101* 创建周期盘点。</span><span class="sxs-lookup"><span data-stu-id="ba825-346">Cycle counting will now be created for item *L0101* at any location if the on-hand quantity is less than 2, and if the date of the last cycle count for the location isn't today.</span></span>

## <a name="scenario-5-define-cycle-count-plans"></a><span data-ttu-id="ba825-347">场景 5：定义周期盘点计划</span><span class="sxs-lookup"><span data-stu-id="ba825-347">Scenario 5: Define cycle count plans</span></span>

<span data-ttu-id="ba825-348">周期盘点计划可让您自动创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-348">Cycle count plans let you automate the creation of cycle counting work.</span></span> <span data-ttu-id="ba825-349">您可以使用特定的物料和库位查询来设置每个周期盘点计划。</span><span class="sxs-lookup"><span data-stu-id="ba825-349">You can set up each cycle count plan with specific item and location queries.</span></span> <span data-ttu-id="ba825-350">当批处理作业运行时，它将为所有与物料和库位条件匹配的库位（最多为计划指定的最大盘点数）创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-350">When the batch job runs, it will create cycle counting work for all locations that match the item and location criteria (up to the maximum number of counts that is specified for the plan).</span></span> <span data-ttu-id="ba825-351">当创建周期盘点工作时，盘点工作行包含有关必须盘点的库位的信息。</span><span class="sxs-lookup"><span data-stu-id="ba825-351">When cycle counting work is created, the counting work line includes information about the location that must be counted.</span></span> <span data-ttu-id="ba825-352">与该库位关联的现有库存不会受阻止。</span><span class="sxs-lookup"><span data-stu-id="ba825-352">The on-hand inventory that is associated with that location isn't blocked.</span></span> <span data-ttu-id="ba825-353">因此，即使存在未结盘点工作，它也可用于预留和出站处理。</span><span class="sxs-lookup"><span data-stu-id="ba825-353">Therefore, it's available for reservation and outbound processing, even though open counting work exists.</span></span>

<span data-ttu-id="ba825-354">按照以下步骤设置周期盘点计划。</span><span class="sxs-lookup"><span data-stu-id="ba825-354">Follow these steps to set up a cycle count plan.</span></span>

1. <span data-ttu-id="ba825-355">转到 **仓库管理 \> 设置 \> 周期盘点 \> 周期盘点计划**。</span><span class="sxs-lookup"><span data-stu-id="ba825-355">Go to **Warehouse management \> Setup \> Cycle counting \> Cycle count plans**.</span></span>
1. <span data-ttu-id="ba825-356">在操作窗格上，选择 **新建** 以向网格添加一行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="ba825-356">On the Action Pane, select **New** to add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="ba825-357">**周期盘点计划 ID**：*BULK06*</span><span class="sxs-lookup"><span data-stu-id="ba825-357">**Cycle counting plan ID:** *BULK06*</span></span>
    - <span data-ttu-id="ba825-358">**描述**：*BULK06 的库位盘点*</span><span class="sxs-lookup"><span data-stu-id="ba825-358">**Description:** *Counting of location for BULK06*</span></span>
    - <span data-ttu-id="ba825-359">**工作池 ID**：*CycleCount*</span><span class="sxs-lookup"><span data-stu-id="ba825-359">**Work pool ID:** *CycleCount*</span></span>
    - <span data-ttu-id="ba825-360">**周期盘点的最大数量**：*10*</span><span class="sxs-lookup"><span data-stu-id="ba825-360">**Maximum number of cycle counts:** *10*</span></span>
    - <span data-ttu-id="ba825-361">**周期盘点之间的天数**：*10*</span><span class="sxs-lookup"><span data-stu-id="ba825-361">**Days between cycle counting:** *10*</span></span>
    - <span data-ttu-id="ba825-362">**空库位**：*排除空库位*</span><span class="sxs-lookup"><span data-stu-id="ba825-362">**Empty locations:** *Exclude empty*</span></span>
    - <span data-ttu-id="ba825-363">**工作模板**：将此字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="ba825-363">**Work template:** Leave this field blank.</span></span>

1. <span data-ttu-id="ba825-364">在操作窗格上，选择 **选择库位**。</span><span class="sxs-lookup"><span data-stu-id="ba825-364">On the Action Pane, select **Select locations**.</span></span>
1. <span data-ttu-id="ba825-365">将显示标准查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-365">A standard query editor dialog box appears.</span></span> <span data-ttu-id="ba825-366">在 **范围** 选项卡上，添加一行，然后为其设置以下值：</span><span class="sxs-lookup"><span data-stu-id="ba825-366">On the **Range** tab, add a row, and set the following values for it:</span></span>

    - <span data-ttu-id="ba825-367">**表：** *位置*</span><span class="sxs-lookup"><span data-stu-id="ba825-367">**Table:** *Locations*</span></span>
    - <span data-ttu-id="ba825-368">**字段：** *区域 ID*</span><span class="sxs-lookup"><span data-stu-id="ba825-368">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="ba825-369">**条件：** *BULK06*</span><span class="sxs-lookup"><span data-stu-id="ba825-369">**Criteria:** *BULK06*</span></span>

1. <span data-ttu-id="ba825-370">选择 **确定** 关闭查询编辑器对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-370">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="ba825-371">在操作窗格上，选择 **处理周期盘点计划**。</span><span class="sxs-lookup"><span data-stu-id="ba825-371">On the Action Pane, select **Process cycle counting plan**.</span></span>
1. <span data-ttu-id="ba825-372">在 **周期盘点计划** 对话框中，在 **在后台运行** 快速选项卡上，将 **批处理** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="ba825-372">In the **Cycle count plans** dialog box, on the **Run in the background** FastTab, set the **Batch processing** option to *Yes*.</span></span>
1. <span data-ttu-id="ba825-373">选择 **定期**。</span><span class="sxs-lookup"><span data-stu-id="ba825-373">Select **Recurrence**.</span></span>
1. <span data-ttu-id="ba825-374">在 **定义定期** 对话框中，设置批处理作业，以便它立即开始，每分钟运行一次，并且没有结束日期。</span><span class="sxs-lookup"><span data-stu-id="ba825-374">In the **Define recurrence** dialog box, set up the batch job so that it begins immediately and runs once every minute, and so that there is no end date.</span></span>
1. <span data-ttu-id="ba825-375">选择 **确定** 以关闭 **定义定期** 对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-375">Select **OK** to close the **Define recurrence** dialog box.</span></span>
1. <span data-ttu-id="ba825-376">选择 **确定** 以关闭 **周期盘点计划** 对话框。</span><span class="sxs-lookup"><span data-stu-id="ba825-376">Select **OK** to close the **Cycle count plans** dialog box.</span></span>

    <span data-ttu-id="ba825-377">将显示一条消息，通知您作业已添加到批处理队列。</span><span class="sxs-lookup"><span data-stu-id="ba825-377">A message informs you that the job was added to the batch queue.</span></span>

1. <span data-ttu-id="ba825-378">转到 **仓库管理 \> 常用 \> 周期盘点计划**。</span><span class="sxs-lookup"><span data-stu-id="ba825-378">Go to **Warehouse management \> Common \> Cycle count scheduling**.</span></span> <span data-ttu-id="ba825-379">该计划立即开始并创建盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-379">The plan begins immediately and creates counting work.</span></span> <span data-ttu-id="ba825-380">由于盘点工作尚未完成，因此 **状态** 字段设置为 *进行中*。</span><span class="sxs-lookup"><span data-stu-id="ba825-380">Because counting work hasn't been completed, the **Status** field is set to *In process*.</span></span> <span data-ttu-id="ba825-381">一分钟后，**总周期盘点** 列中的值更改为 *1*。</span><span class="sxs-lookup"><span data-stu-id="ba825-381">After one minute, the value in the **Total cycle counts** column changes to *1*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ba825-382">如果自上次周期盘点以来的天数小于您为周期盘点计划的 **周期盘点之间的天数** 字段设置的值，将不会创建周期盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-382">Cycle count work won't be created if the number of days since the last cycle counting is less than value that you set for the **Days between cycle counting** field for the cycle counting plan.</span></span> <span data-ttu-id="ba825-383">例如，如果 **周期盘点之间的天数** 字段设置为 *5*，则周期盘点工作每五天创建一次。</span><span class="sxs-lookup"><span data-stu-id="ba825-383">For example, if the **Days between cycle counting** field is set to *5*, cycle counting work will be created every five days.</span></span> <span data-ttu-id="ba825-384">但是，如果在第三天处理周期盘点工作，则下一个周期盘点工作将在处理完最后的周期盘点之后的第五天被创建，即第八天。</span><span class="sxs-lookup"><span data-stu-id="ba825-384">However, if cycle counting work is processed on day 3, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>

1. <span data-ttu-id="ba825-385">在操作窗格上，选择 **工作** 以查看创建的盘点工作。</span><span class="sxs-lookup"><span data-stu-id="ba825-385">On Action Pane, select **Work** to view the counting work that was created.</span></span>
