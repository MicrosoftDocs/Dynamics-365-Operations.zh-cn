---
title: 工作拆分
description: 此主题提供有关工作拆分功能的信息。 使用此功能，您可以将大型工作订单拆分为几个较小的工作订单，然后将其分配给多个仓库工作人员。 这样，同一个工作可以同时由几个仓库工人工作人员选择。
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6dbf0f6dd0c691db74eaad2174d8f9849b4cb26a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245074"
---
# <a name="work-split"></a><span data-ttu-id="91a52-105">工作拆分</span><span class="sxs-lookup"><span data-stu-id="91a52-105">Work split</span></span>

<span data-ttu-id="91a52-106">使用工作拆分功能，您可以将较大的工作 ID（即有几个行的工作订单）拆分为几个较小的工作 ID，然后将其分配给多个仓库工作人员。</span><span class="sxs-lookup"><span data-stu-id="91a52-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="91a52-107">这样，同一个工作创建编号可以同时由几个仓库工人工作人员选择。</span><span class="sxs-lookup"><span data-stu-id="91a52-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91a52-108">只能拆分状态为 *未结* 或 *进行中* 的工作订单。</span><span class="sxs-lookup"><span data-stu-id="91a52-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="91a52-109">开启工作拆分功能</span><span class="sxs-lookup"><span data-stu-id="91a52-109">Turn on the work split functionality</span></span>

<span data-ttu-id="91a52-110">必须先在系统中开启工作拆分功能及其先决功能，然后才能够使用此功能。</span><span class="sxs-lookup"><span data-stu-id="91a52-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="91a52-111">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态，然后根据需要开启功能。</span><span class="sxs-lookup"><span data-stu-id="91a52-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="91a52-112">首先，开启 *组织范围内的工作锁定* 先决功能（如果尚未开启）。</span><span class="sxs-lookup"><span data-stu-id="91a52-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="91a52-113">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="91a52-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="91a52-114">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="91a52-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="91a52-115">**功能名称**：*组织范围内的工作锁定*</span><span class="sxs-lookup"><span data-stu-id="91a52-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="91a52-116">激活此功能后，在所有法人中开启此功能后，将自动应用数据升级。</span><span class="sxs-lookup"><span data-stu-id="91a52-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="91a52-117">接下来，开启 *工作拆分* 功能，它按以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="91a52-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="91a52-118">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="91a52-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="91a52-119">**功能名称**：*工作拆分*</span><span class="sxs-lookup"><span data-stu-id="91a52-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="91a52-120">工作详细信息和所有工作页的增强</span><span class="sxs-lookup"><span data-stu-id="91a52-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="91a52-121">*工作拆分* 功能将以下两个按钮添加到 **工作详细信息** 和 **所有工作** 页的操作窗格上的 **工作** 选项卡上：</span><span class="sxs-lookup"><span data-stu-id="91a52-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="91a52-122">**拆分工作** – 将当前的工作 ID 拆分为可以由单独的工作人员处理的多个较小的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="91a52-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="91a52-123">**取消工作拆分会话** – 取消工作拆分会话，让工作可以处理。</span><span class="sxs-lookup"><span data-stu-id="91a52-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="91a52-124">![拆分工作和取消工作拆分会话按钮](media/Work_split_buttons.png "拆分工作和取消工作拆分会话按钮")</span><span class="sxs-lookup"><span data-stu-id="91a52-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91a52-125">如果满足以下任一条件，**拆分工作** 按钮将不可用：</span><span class="sxs-lookup"><span data-stu-id="91a52-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="91a52-126">工作状态不是 *未结* 或 *进行中*。</span><span class="sxs-lookup"><span data-stu-id="91a52-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="91a52-127">容器 ID 与工作 ID 关联。</span><span class="sxs-lookup"><span data-stu-id="91a52-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="91a52-128">（容器无法系统拆分，因为它需要物理操作。）</span><span class="sxs-lookup"><span data-stu-id="91a52-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="91a52-129">工作与群集关联。</span><span class="sxs-lookup"><span data-stu-id="91a52-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="91a52-130">工作订单类型不是以下类型之一：</span><span class="sxs-lookup"><span data-stu-id="91a52-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="91a52-131">销售订单</span><span class="sxs-lookup"><span data-stu-id="91a52-131">Sales orders</span></span>
>    - <span data-ttu-id="91a52-132">原材料领取</span><span class="sxs-lookup"><span data-stu-id="91a52-132">Raw material picking</span></span>
>    - <span data-ttu-id="91a52-133">转移问题</span><span class="sxs-lookup"><span data-stu-id="91a52-133">Transfer issue</span></span>
>
> - <span data-ttu-id="91a52-134">工作目前正在由其他用户拆分。</span><span class="sxs-lookup"><span data-stu-id="91a52-134">The work is currently being split by another user.</span></span> <span data-ttu-id="91a52-135">如果您尝试打开其他用户已经在拆分的工作的拆分页面，将收到以下错误消息：“ID 为 \#\#\#\# 的工作目前正在拆分。</span><span class="sxs-lookup"><span data-stu-id="91a52-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="91a52-136">请在几分钟后重试。</span><span class="sxs-lookup"><span data-stu-id="91a52-136">Retry in a few minutes.</span></span> <span data-ttu-id="91a52-137">如果继续收到此消息，请与主管联系。”</span><span class="sxs-lookup"><span data-stu-id="91a52-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="91a52-138">新的工作锁定原因 *拆分工作* 会在工作 ID 正在进行拆分时给出指示。</span><span class="sxs-lookup"><span data-stu-id="91a52-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="91a52-139">如果用户尝试运行工作，它会同时显示在 **拆分工作** 页和仓库应用中。</span><span class="sxs-lookup"><span data-stu-id="91a52-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="91a52-140">使用锁定原因时，工作 ID 的 **锁定波次** 字段的名称将更改为 **已锁定**。</span><span class="sxs-lookup"><span data-stu-id="91a52-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="91a52-141">启动工作拆分</span><span class="sxs-lookup"><span data-stu-id="91a52-141">Initiate a work split</span></span>

<span data-ttu-id="91a52-142">此功能添加了一个新的 **拆分工作** 页，让用户可以拆分工作 ID 的工作行。</span><span class="sxs-lookup"><span data-stu-id="91a52-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="91a52-143">首次打开此页面时，它将显示工作状态为 *未结* 且可以拆分的行。</span><span class="sxs-lookup"><span data-stu-id="91a52-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="91a52-144">在操作窗格上，选择 **拆分工作** 处理选定的工作。</span><span class="sxs-lookup"><span data-stu-id="91a52-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="91a52-145">要拆分工作，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="91a52-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="91a52-146">打开以下工作页面之一：</span><span class="sxs-lookup"><span data-stu-id="91a52-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="91a52-147">**工作详细信息**（**仓库管理 \> 工作 \> 工作详细信息**）</span><span class="sxs-lookup"><span data-stu-id="91a52-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="91a52-148">**所有工作**（**仓库管理 \> 工作 \> 所有工作**）</span><span class="sxs-lookup"><span data-stu-id="91a52-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="91a52-149">在网格中，选择要拆分的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="91a52-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="91a52-150">**工作订单** 字段必须设置为以下值之一：</span><span class="sxs-lookup"><span data-stu-id="91a52-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="91a52-151">销售订单</span><span class="sxs-lookup"><span data-stu-id="91a52-151">Sales orders</span></span>
    - <span data-ttu-id="91a52-152">原材料领取</span><span class="sxs-lookup"><span data-stu-id="91a52-152">Raw material picking</span></span>
    - <span data-ttu-id="91a52-153">转移问题</span><span class="sxs-lookup"><span data-stu-id="91a52-153">Transfer issue</span></span>

1. <span data-ttu-id="91a52-154">在操作窗格 **工作** 选项卡上的 **工作** 组中，选择 **拆分工作**。</span><span class="sxs-lookup"><span data-stu-id="91a52-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="91a52-155">**拆分工作** 页将出现，显示未结的可以拆分的工作行。</span><span class="sxs-lookup"><span data-stu-id="91a52-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="91a52-156">默认情况下，仅显示可用工作行。</span><span class="sxs-lookup"><span data-stu-id="91a52-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="91a52-157">要查看工作 ID 的所有行（例如，工作类型为 *放置* 的行），选中网格上方的 **显示所有行** 复选框。</span><span class="sxs-lookup"><span data-stu-id="91a52-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="91a52-158">以下消息将显示：“用户只有在完成拆分并关闭此页面后才能处理工作的行。”</span><span class="sxs-lookup"><span data-stu-id="91a52-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="91a52-159">当前工作的 **工作锁定原因** 字段将设置为 *拆分工作*，工作将被锁定。</span><span class="sxs-lookup"><span data-stu-id="91a52-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="91a52-160">![锁定原因](media/Blocking_reason.png "锁定原因")</span><span class="sxs-lookup"><span data-stu-id="91a52-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="91a52-161">选择要从当前工作 ID 中删除的行，然后将其添加到新工作 ID 中。</span><span class="sxs-lookup"><span data-stu-id="91a52-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="91a52-162">将发生以下事件：</span><span class="sxs-lookup"><span data-stu-id="91a52-162">The following events occur:</span></span>

    - <span data-ttu-id="91a52-163">拆分工作时，原始工作 ID 中选择的一行或多行将被取消，然后被复制到新的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="91a52-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="91a52-164">现有工作模板结构和放置的位置（以及将来的领料/放置对）将保留。</span><span class="sxs-lookup"><span data-stu-id="91a52-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="91a52-165">以下工作 ID 字段的值将从原始工作复制到新工作：</span><span class="sxs-lookup"><span data-stu-id="91a52-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="91a52-166">装载 ID</span><span class="sxs-lookup"><span data-stu-id="91a52-166">Load ID</span></span>
        - <span data-ttu-id="91a52-167">装运 ID</span><span class="sxs-lookup"><span data-stu-id="91a52-167">Shipment ID</span></span>
        - <span data-ttu-id="91a52-168">工作订单类型</span><span class="sxs-lookup"><span data-stu-id="91a52-168">Work order type</span></span>
        - <span data-ttu-id="91a52-169">转移单编号</span><span class="sxs-lookup"><span data-stu-id="91a52-169">Order number</span></span>
        - <span data-ttu-id="91a52-170">站点</span><span class="sxs-lookup"><span data-stu-id="91a52-170">Site</span></span>
        - <span data-ttu-id="91a52-171">仓库</span><span class="sxs-lookup"><span data-stu-id="91a52-171">Warehouse</span></span>
        - <span data-ttu-id="91a52-172">工作优先级</span><span class="sxs-lookup"><span data-stu-id="91a52-172">Work priority</span></span>
        - <span data-ttu-id="91a52-173">工作池 ID</span><span class="sxs-lookup"><span data-stu-id="91a52-173">Work pool ID</span></span>
        - <span data-ttu-id="91a52-174">波次 ID</span><span class="sxs-lookup"><span data-stu-id="91a52-174">Wave ID</span></span>
        - <span data-ttu-id="91a52-175">工作创建编号</span><span class="sxs-lookup"><span data-stu-id="91a52-175">Work creation number</span></span>

    - <span data-ttu-id="91a52-176">以下字段不会复制到新工作 ID：</span><span class="sxs-lookup"><span data-stu-id="91a52-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="91a52-177">**工作 ID** – 新工作 ID 从适当的编号规则生成。</span><span class="sxs-lookup"><span data-stu-id="91a52-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="91a52-178">**工作状态** – 此字段设置为 *未结*。</span><span class="sxs-lookup"><span data-stu-id="91a52-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="91a52-179">**锁定者** – 此字段最初设置为空白。</span><span class="sxs-lookup"><span data-stu-id="91a52-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="91a52-180">**目标牌照 ID** – 此字段保留为空白。</span><span class="sxs-lookup"><span data-stu-id="91a52-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="91a52-181">**创建日期和时间** – 此字段设置为当前日期和时间。</span><span class="sxs-lookup"><span data-stu-id="91a52-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="91a52-182">**锁定波次/锁定** – 此字段将为原始工作 ID 和新工作 ID 重新计算。</span><span class="sxs-lookup"><span data-stu-id="91a52-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="91a52-183">在操作窗格上，选择 **拆分工作**。</span><span class="sxs-lookup"><span data-stu-id="91a52-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="91a52-184">拆分工作时，将显示以下消息：“处理操作 - 拆分工作”。</span><span class="sxs-lookup"><span data-stu-id="91a52-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="91a52-185">此消息显示时，您可以通过在消息框中选择 **取消** 来取消操作。</span><span class="sxs-lookup"><span data-stu-id="91a52-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="91a52-186">如果 **显示所有行** 复选框被清除，拆分和取消的行将不再出现在网格中。</span><span class="sxs-lookup"><span data-stu-id="91a52-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="91a52-187">如果选中此复选框，您应该会看到该行的 **工作状态** 字段的值已更改为 *已取消*。</span><span class="sxs-lookup"><span data-stu-id="91a52-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="91a52-188">以下通知将显示，指示新工作 ID 已创建：“工作 \#\#\#\# 已通过拆分原始工作 \#\#\#\# 创建。”</span><span class="sxs-lookup"><span data-stu-id="91a52-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="91a52-189">原始工作 ID 的其他工作行（如 *放置* 行）将根据需要进行调整，以反映已取消的工作行。</span><span class="sxs-lookup"><span data-stu-id="91a52-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="91a52-190">例如，如果原始工作 ID 有一个数量为 15 的 *放置* 行，总数量为 10 的 *领料* 行被取消，原始工作 ID 上的新 *放置* 数量现在将是 5。</span><span class="sxs-lookup"><span data-stu-id="91a52-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="91a52-191">新工作不会立即分配给任何用户。</span><span class="sxs-lookup"><span data-stu-id="91a52-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="91a52-192">不过，您现在可以根据需要使用 **工作详细信息** 页的标准功能将其分配给用户。</span><span class="sxs-lookup"><span data-stu-id="91a52-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="91a52-193">您只能拆分包含两个或更多可用工作行的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="91a52-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="91a52-194">如果您在只有一个工作行时选择 **拆分工作**，您将收到以下错误消息：“初始工作中必须至少保留一个工作行。”</span><span class="sxs-lookup"><span data-stu-id="91a52-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="91a52-195">在这种情况下，不会进行拆分。</span><span class="sxs-lookup"><span data-stu-id="91a52-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="91a52-196">完成工作拆分</span><span class="sxs-lookup"><span data-stu-id="91a52-196">Finish a work split</span></span>

<span data-ttu-id="91a52-197">要完成拆分工作，必须删除 *拆分工作* 锁定原因。</span><span class="sxs-lookup"><span data-stu-id="91a52-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="91a52-198">有两种方法可以完成此步骤：</span><span class="sxs-lookup"><span data-stu-id="91a52-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="91a52-199">拆分工作的用户通过选择右上角的 **关闭** 按钮 (**X**) 关闭 **拆分工作** 页。</span><span class="sxs-lookup"><span data-stu-id="91a52-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="91a52-200">关闭此页面后，*拆分工作* 锁定原因将被删除。</span><span class="sxs-lookup"><span data-stu-id="91a52-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="91a52-201">此工作的 *已锁定* 状态将被重新计算，此工作如果没有其余锁定原因，工作将解除锁定。</span><span class="sxs-lookup"><span data-stu-id="91a52-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="91a52-202">任意用户打开工作 ID 并选择操作窗格上的 **取消工作拆分会话** 按钮。</span><span class="sxs-lookup"><span data-stu-id="91a52-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="91a52-203">就像 **拆分工作** 页关闭时一样，*拆分工作* 锁定原因将被删除，此工作的 *已锁定* 状态将被重新计算。</span><span class="sxs-lookup"><span data-stu-id="91a52-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="91a52-204">*拆分工作* 锁定原因删除后，如果在工作 ID 上将 **已锁定** 状态设置为 *否*，工作可以在移动设备上运行。</span><span class="sxs-lookup"><span data-stu-id="91a52-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="91a52-205">仓库应用上的用户锁定</span><span class="sxs-lookup"><span data-stu-id="91a52-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="91a52-206">如果您尝试使用仓库应用对正在拆分的工作 ID 运行领料工作，将收到以下错误消息：“ID 为 \#\#\#\# 的工作目前正在拆分。”</span><span class="sxs-lookup"><span data-stu-id="91a52-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="91a52-207">如果收到此消息，请选择 **取消**。</span><span class="sxs-lookup"><span data-stu-id="91a52-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="91a52-208">然后，您可以继续处理其他工作。</span><span class="sxs-lookup"><span data-stu-id="91a52-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="91a52-209">其他锁定操作</span><span class="sxs-lookup"><span data-stu-id="91a52-209">Other blocked operations</span></span>

<span data-ttu-id="91a52-210">任何修改工作行、工作库存交易或与正在拆分的工作相关的补货链接的操作都会失败，并显示以下错误消息：“ID 为 \#\#\#\# 的工作目前正在拆分。”</span><span class="sxs-lookup"><span data-stu-id="91a52-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]