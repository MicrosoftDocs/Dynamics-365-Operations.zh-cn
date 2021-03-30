---
title: 库存日记帐审核工作流
description: 本主题介绍如何为各种类型的实际库存交易设置和使用库存日记帐审核工作流。 库存日记帐工作流有助于确保仅将批准的库存日记帐过帐到交易记录中。
author: sherry-zheng
manager: tfehr
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 596182dfd7430e4d1e35ffebb795fbcf98d45e33
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247902"
---
# <a name="inventory-journal-approval-workflows"></a><span data-ttu-id="4a556-104">库存日记帐审核工作流</span><span class="sxs-lookup"><span data-stu-id="4a556-104">Inventory journal approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a556-105">本主题介绍如何为各种类型的实际库存交易（如发货和收货、库存变动、物料清单 (BOM) 和实际库存对帐）设置和使用库存日记帐审核工作流。</span><span class="sxs-lookup"><span data-stu-id="4a556-105">This topic describes how to set up and use inventory journal approval workflows for various types of physical inventory transactions, such as issues and receipts, inventory movements, bills of materials (BOMs), and the reconciliation of physical inventory.</span></span> <span data-ttu-id="4a556-106">库存日记帐工作流有助于确保仅将批准的库存日记帐过帐到交易记录中。</span><span class="sxs-lookup"><span data-stu-id="4a556-106">Inventory journal workflows help ensure that only approved inventory journals can be posted to transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="4a556-107">库存日记帐审核工作流仅适用于使用库存管理模块记录的交易。</span><span class="sxs-lookup"><span data-stu-id="4a556-107">Inventory journal approval workflows apply only to transactions recorded using the Inventory Management module.</span></span> <span data-ttu-id="4a556-108">不适用于仓库管理模块触发的库存日记帐。</span><span class="sxs-lookup"><span data-stu-id="4a556-108">They don't work with inventory journals triggered from the Warehouse Management module.</span></span>

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a><span data-ttu-id="4a556-109">打开库存日记帐审核工作流功能</span><span class="sxs-lookup"><span data-stu-id="4a556-109">Turn on the inventory journal approval workflows feature</span></span>

<span data-ttu-id="4a556-110">此功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="4a556-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="4a556-111">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。</span><span class="sxs-lookup"><span data-stu-id="4a556-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="4a556-112">在 **功能管理** 工作区中，此功能按照下面的方式列出：</span><span class="sxs-lookup"><span data-stu-id="4a556-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="4a556-113">**模块**：*库存和仓库管理*</span><span class="sxs-lookup"><span data-stu-id="4a556-113">**Module:** *Inventory and warehouse management*</span></span>
- <span data-ttu-id="4a556-114">**功能名称**：*库存日记帐审核工作流*</span><span class="sxs-lookup"><span data-stu-id="4a556-114">**Feature name:** *Inventory journal approve workflow*</span></span>

## <a name="create-your-inventory-journal-approval-workflows"></a><span data-ttu-id="4a556-115">创建库存日记帐审核工作流</span><span class="sxs-lookup"><span data-stu-id="4a556-115">Create your inventory journal approval workflows</span></span>

<span data-ttu-id="4a556-116">要设置此功能，必须为要控制的每种库存日记帐类型创建工作流。</span><span class="sxs-lookup"><span data-stu-id="4a556-116">To set up this feature, you must create a workflow for each of the inventory journal types you want to control.</span></span> <span data-ttu-id="4a556-117">由于不同的库存日记帐类型可以具有不同的审核层次结构和工作流步骤，因此可以为每种库存日记帐类型配置单独的工作流。</span><span class="sxs-lookup"><span data-stu-id="4a556-117">Because different inventory journal types can have different approval hierarchies and workflow steps, you can configure individual workflows for each inventory journal type.</span></span>

<span data-ttu-id="4a556-118">工作流支持版本控制，每个工作流都有一个工作流 ID 和一个有效版本。</span><span class="sxs-lookup"><span data-stu-id="4a556-118">Workflows support version control, and each has a workflow ID and an active version.</span></span> <span data-ttu-id="4a556-119">您可以选择在创建后立即激活每个新的工作流版本，或不进行激活。</span><span class="sxs-lookup"><span data-stu-id="4a556-119">You can choose to activate each new workflow version immediately upon creation or keep it inactive.</span></span> <span data-ttu-id="4a556-120">如果同一日记帐类型需要不同的工作流，请为该日记帐类型创建多个工作流，然后将每个工作流分配给使用该类型的不同日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="4a556-120">If you need different workflows for the same journal type, then create multiple workflows for that journal type, and then assign each of these to a different journal name that uses that type.</span></span>

<span data-ttu-id="4a556-121">创建库存日记帐审核工作流：</span><span class="sxs-lookup"><span data-stu-id="4a556-121">To create your inventory journal approval workflows:</span></span>

1. <span data-ttu-id="4a556-122">转到 **库存管理 \> 设置 \> 库存管理工作流**。</span><span class="sxs-lookup"><span data-stu-id="4a556-122">Go to **Inventory Management \> Setup\> Inventory management workflows**.</span></span>
1. <span data-ttu-id="4a556-123">在操作窗格上选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="4a556-123">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="4a556-124">选择要为其设置工作流的库存日记帐类型：</span><span class="sxs-lookup"><span data-stu-id="4a556-124">Choose the inventory journal type for which you want to set up a workflow:</span></span>
    - <span data-ttu-id="4a556-125">**库存标签盘点日记帐**</span><span class="sxs-lookup"><span data-stu-id="4a556-125">**Inventory tag counting journal**</span></span>
    - <span data-ttu-id="4a556-126">**库存所有权更改日记帐**</span><span class="sxs-lookup"><span data-stu-id="4a556-126">**Inventory ownership change journal**</span></span>
    - <span data-ttu-id="4a556-127">**库存变动日记帐**</span><span class="sxs-lookup"><span data-stu-id="4a556-127">**Inventory movement journal**</span></span>
    - <span data-ttu-id="4a556-128">**库存转移日记帐**</span><span class="sxs-lookup"><span data-stu-id="4a556-128">**Inventory transfer journal**</span></span>
    - <span data-ttu-id="4a556-129">**库存盘点日记帐**</span><span class="sxs-lookup"><span data-stu-id="4a556-129">**Inventory counting journal**</span></span>
    - <span data-ttu-id="4a556-130">**库存物料清单日记帐**</span><span class="sxs-lookup"><span data-stu-id="4a556-130">**Inventory BOM journal**</span></span>
    - <span data-ttu-id="4a556-131">**库存调整日记帐**</span><span class="sxs-lookup"><span data-stu-id="4a556-131">**Inventory adjustment journal**</span></span>

    <span data-ttu-id="4a556-132">![“创建工作流”对话框](media/journal-workflow-create-workflow.png "“创建工作流”对话框")</span><span class="sxs-lookup"><span data-stu-id="4a556-132">![The Create workflow dialog box](media/journal-workflow-create-workflow.png "The Create workflow dialog box")</span></span>

1. <span data-ttu-id="4a556-133">工作流编辑器应用将在您的计算机上启动。</span><span class="sxs-lookup"><span data-stu-id="4a556-133">The workflow editor app launches on your machine.</span></span> <span data-ttu-id="4a556-134">（可能会要求您批准此操作。）请根据需要使用它来设计工作流。</span><span class="sxs-lookup"><span data-stu-id="4a556-134">(You may be asked to approve this action.) Use it to design your workflow as needed.</span></span> <span data-ttu-id="4a556-135">有关如何使用工作流编辑器的详细信息，请参阅[工作流系统概览](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md)。</span><span class="sxs-lookup"><span data-stu-id="4a556-135">For details about how to use the workflow editor, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).</span></span>
1. <span data-ttu-id="4a556-136">保存并关闭工作流编辑器应用后，您必须选择是激活此工作流版本还是保持非活动状态。</span><span class="sxs-lookup"><span data-stu-id="4a556-136">After saving and closing the workflow editor app, you must choose whether to activate this workflow version or keep it as inactivate.</span></span>

> [!NOTE]
> <span data-ttu-id="4a556-137">工作流提供版本控制，这意味着您可以查看已创建的版本列表并选择哪个版本处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="4a556-137">Workflows provide version control, which means that you can view a list of versions you have created and choose which one is active.</span></span> <span data-ttu-id="4a556-138">要查看可用版本列表和选择要激活的版本，请选择 **库存管理工作流** 页列出的工作流。</span><span class="sxs-lookup"><span data-stu-id="4a556-138">To view the list of available versions and choose which to activate, select a workflow listed on the **Inventory management workflows** page.</span></span> <span data-ttu-id="4a556-139">在操作窗格上，打开 **工作流** 选项卡，然后选择 **版本**。</span><span class="sxs-lookup"><span data-stu-id="4a556-139">On the Action Pane, open the **Workflow** tab, and select **Versions**.</span></span> <span data-ttu-id="4a556-140">每个工作流 ID 一次只能激活一个版本。</span><span class="sxs-lookup"><span data-stu-id="4a556-140">Only one version can be active at a time for each workflow ID.</span></span>

## <a name="assign-approval-workflows-to-inventory-journal-names"></a><span data-ttu-id="4a556-141">将审核工作流分配给库存日记帐名称</span><span class="sxs-lookup"><span data-stu-id="4a556-141">Assign approval workflows to inventory journal names</span></span>

<span data-ttu-id="4a556-142">下一步是为每个库存日记帐名称分配一个库存日记帐工作流。</span><span class="sxs-lookup"><span data-stu-id="4a556-142">The next step is to assign a inventory journal workflow to each inventory journal name.</span></span> <span data-ttu-id="4a556-143">对于每种库存日记帐类型，您可以设置多个库存日记帐名称。</span><span class="sxs-lookup"><span data-stu-id="4a556-143">For each inventory journal type, you can set up multiple inventory journal names.</span></span>

<span data-ttu-id="4a556-144">将库存日记帐工作流与库存日记帐名称关联：</span><span class="sxs-lookup"><span data-stu-id="4a556-144">To associate an inventory journal workflow with an inventory journal name:</span></span>

1. <span data-ttu-id="4a556-145">转到 **库存管理 \> 设置 \> 日记帐名称 \> 库存**。</span><span class="sxs-lookup"><span data-stu-id="4a556-145">Go to **Inventory management \> Setup \> Journal names \> Inventory**.</span></span>
1. <span data-ttu-id="4a556-146">从列表列中选择一个日记帐名称来打开其设置页面。</span><span class="sxs-lookup"><span data-stu-id="4a556-146">Select a journal name from the list column to open its settings page.</span></span>
1. <span data-ttu-id="4a556-147">在 **常规** 快速选项卡上，将 **审核工作流** 设置为 **是**。</span><span class="sxs-lookup"><span data-stu-id="4a556-147">On the **General** FastTab, set **Approval workflow** to **Yes**.</span></span> <span data-ttu-id="4a556-148">如果提示批准操作，请选择 **是**。</span><span class="sxs-lookup"><span data-stu-id="4a556-148">If you are prompted to approve the action, select **Yes**.</span></span>

    <span data-ttu-id="4a556-149">![将工作流分配给日记帐名称](media/journal-workflow-journal-name.png "将工作流分配给日记帐名称")</span><span class="sxs-lookup"><span data-stu-id="4a556-149">![Assign a workflow to a journal name](media/journal-workflow-journal-name.png "Assign a workflow to a journal name")</span></span>

1. <span data-ttu-id="4a556-150">打开 **工作流** 下拉列表，选择适当的工作流。</span><span class="sxs-lookup"><span data-stu-id="4a556-150">Open the **Workflow** drop-down list and select the appropriate workflow.</span></span> <span data-ttu-id="4a556-151">此列表显示您使用工作流编辑器应用创建的每个活动工作流。</span><span class="sxs-lookup"><span data-stu-id="4a556-151">The list shows each active workflow that you have created using the workflow editor app.</span></span>

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a><span data-ttu-id="4a556-152">创建库存日记帐并发送进行审核</span><span class="sxs-lookup"><span data-stu-id="4a556-152">Create an inventory journal and send it for approval</span></span>

<span data-ttu-id="4a556-153">将库存日记帐名称与其匹配的库存日记帐审核工作流关联之后，您将能够创建使用该名称的新库存日记帐，然后使用该工作流发送这些日记帐进行审核。</span><span class="sxs-lookup"><span data-stu-id="4a556-153">After you associate an inventory journal name with its matching inventory journal approval workflow, you'll be able to create new inventory journals that use that name and then send these journals for approval using that workflow.</span></span> <span data-ttu-id="4a556-154">在工作流中配置的审核人批准库存日记帐之前，您将无法过帐。</span><span class="sxs-lookup"><span data-stu-id="4a556-154">You won't be able post the inventory journal until it has been approved by the approvers configured in the workflow.</span></span>

1. <span data-ttu-id="4a556-155">在导航窗格上，展开 **库存管理 \> 日记帐条目 \> 商品**，然后选择库存日记帐类型。</span><span class="sxs-lookup"><span data-stu-id="4a556-155">On the navigation pane, expand **Inventory management \> Journal entries \> Items** and then select an inventory journal type.</span></span>
1. <span data-ttu-id="4a556-156">选择 **新建** 创建所选类型的新日记帐。</span><span class="sxs-lookup"><span data-stu-id="4a556-156">Select **New** to create a new journal of your selected type.</span></span>
1. <span data-ttu-id="4a556-157">**创建库存日记帐** 对话框将打开。</span><span class="sxs-lookup"><span data-stu-id="4a556-157">The **Create inventory journal** dialog box opens.</span></span> <span data-ttu-id="4a556-158">根据需要填写表单，然后选择 **确定** 保存日记帐。</span><span class="sxs-lookup"><span data-stu-id="4a556-158">Fill out the form as needed and then select **OK** to save the journal.</span></span>
1. <span data-ttu-id="4a556-159">根据需要完成日记帐。</span><span class="sxs-lookup"><span data-stu-id="4a556-159">Complete the journal as required.</span></span>
1. <span data-ttu-id="4a556-160">当创建或打开具有关联的审核工作流的库存日记帐时，**工作流** 按钮将在操作窗格中处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="4a556-160">When you create or open an inventory journal with an approval workflow associated with it, the **Workflow** button will be active in the Action Pane.</span></span> <span data-ttu-id="4a556-161">当您准备好要提交日记帐以供审核时，选择 **工作流** 按钮打开一个下拉对话框，然后选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="4a556-161">When you are ready to submit the journal for approval, select the **Workflow** button to open a drop-down dialog box and then select **Submit**.</span></span> <span data-ttu-id="4a556-162">然后，审核请求将路由到相关审核人，系统将使用为工作流配置的通知方法提醒审核人。</span><span class="sxs-lookup"><span data-stu-id="4a556-162">The approval request will then route to the relevant approver, who will be alerted using the notification method configured for the workflow.</span></span>

    <span data-ttu-id="4a556-163">![提交日记帐以供审核](media/journal-workflow-inventory-journal.png "提交日记帐以供审核")</span><span class="sxs-lookup"><span data-stu-id="4a556-163">![Submit a journal for approval](media/journal-workflow-inventory-journal.png "Submit a journal for approval")</span></span>

<span data-ttu-id="4a556-164">要撤回审核请求，请打开相关日记帐，选择 **工作流** 按钮，然后选择 **撤回**。</span><span class="sxs-lookup"><span data-stu-id="4a556-164">To recall an approval request, open the relevant journal, select the **Workflow** button and then select **Recall**.</span></span> <span data-ttu-id="4a556-165">这将重置工作流。</span><span class="sxs-lookup"><span data-stu-id="4a556-165">This will reset the workflow.</span></span>

<span data-ttu-id="4a556-166">日记帐被批准后，您可以进行过帐。</span><span class="sxs-lookup"><span data-stu-id="4a556-166">When your journal has been approved, you'll be able to post it.</span></span> <span data-ttu-id="4a556-167">要过帐日记帐，请从操作窗格中选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="4a556-167">To post the journal, select **Post** from the Action Pane.</span></span> <span data-ttu-id="4a556-168">如果 **过帐** 按钮未处于活动状态，说明日记帐还未被批准。</span><span class="sxs-lookup"><span data-stu-id="4a556-168">If the **Post** button isn't active the journal hasn't been approved yet.</span></span>

## <a name="respond-to-an-inventory-journal-approval-request"></a><span data-ttu-id="4a556-169">响应库存日记帐审核请求</span><span class="sxs-lookup"><span data-stu-id="4a556-169">Respond to an inventory journal approval request</span></span>

<span data-ttu-id="4a556-170">如果您是审核人，每次需要您审核时，您会收到一条消息（在相关工作流中配置）。</span><span class="sxs-lookup"><span data-stu-id="4a556-170">If you are an approver, you should receive a message each time your approval is needed (as configured in the relevant workflow).</span></span> <span data-ttu-id="4a556-171">然后，您可以通过执行以下操作批准或拒绝日记帐审核请求：</span><span class="sxs-lookup"><span data-stu-id="4a556-171">Then you can approve or reject a journal approval request by doing the following:</span></span>

1. <span data-ttu-id="4a556-172">在导航窗格上，展开 **库存管理 \> 日记帐条目 \> 商品**，然后选择库存日记帐类型。</span><span class="sxs-lookup"><span data-stu-id="4a556-172">On the navigation pane, expand **Inventory management \> Journal entries \> Items** and then select an inventory journal type.</span></span>
1. <span data-ttu-id="4a556-173">打开相关日记帐进行审核。</span><span class="sxs-lookup"><span data-stu-id="4a556-173">Open the relevant journal and review it.</span></span>
1. <span data-ttu-id="4a556-174">选择操作窗格上的 **工作流** 按钮打开一个下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="4a556-174">Select the **Workflow** button on the Action Pane to open a drop-down dialog box.</span></span> <span data-ttu-id="4a556-175">选择以下选项之一：</span><span class="sxs-lookup"><span data-stu-id="4a556-175">Select one of the following:</span></span>
    - <span data-ttu-id="4a556-176">**批准** - 批准请求。</span><span class="sxs-lookup"><span data-stu-id="4a556-176">**Approve** - To approve the request.</span></span>
    - <span data-ttu-id="4a556-177">**拒绝** - 拒绝请求。</span><span class="sxs-lookup"><span data-stu-id="4a556-177">**Reject** - To reject the reject the request.</span></span>
    - <span data-ttu-id="4a556-178">**更多 \> 请求更改** - 向申请人发送消息，要求他们更改特定内容，然后重新提交。</span><span class="sxs-lookup"><span data-stu-id="4a556-178">**More \> Request change** - To send a message to the requester asking them to change something specific and then resubmit.</span></span>
    - <span data-ttu-id="4a556-179">**更多 \> 委托** - 将审核委托给另一个用户。</span><span class="sxs-lookup"><span data-stu-id="4a556-179">**More \> Delegate** - To delegate the approval to another user.</span></span>
    - <span data-ttu-id="4a556-180">**更多 \> 撤回** - 撤回审核请求（重置工作流）。</span><span class="sxs-lookup"><span data-stu-id="4a556-180">**More \> Recall** - To recall the approval request (resets the workflow).</span></span>
    - <span data-ttu-id="4a556-181">**更多 \> 工作流历史记录** - 查看到目前为止此审核工作流的历史记录。</span><span class="sxs-lookup"><span data-stu-id="4a556-181">**More \> Workflow history** - To view the history of this approval workflow so far.</span></span>

## <a name="review-the-approval-history"></a><span data-ttu-id="4a556-182">查看审核历史记录</span><span class="sxs-lookup"><span data-stu-id="4a556-182">Review the approval history</span></span>

<span data-ttu-id="4a556-183">与其他类型的工作流一样，您可以使用 **工作流历史记录** 页查看任意日记帐的审核工作流历史记录。</span><span class="sxs-lookup"><span data-stu-id="4a556-183">As with other types of workflows, you can use the **Workflow history** page to view the approval workflow history for any journal.</span></span>

<span data-ttu-id="4a556-184">查看日记帐的工作流历史记录：</span><span class="sxs-lookup"><span data-stu-id="4a556-184">To review the workflow history for a journal:</span></span>

1. <span data-ttu-id="4a556-185">在导航窗格上，展开 **库存管理 \> 日记帐条目 \> 商品**，然后选择库存日记帐类型。</span><span class="sxs-lookup"><span data-stu-id="4a556-185">On the navigation pane, expand **Inventory management \> Journal entries \> Items** and then select an inventory journal type.</span></span>
1. <span data-ttu-id="4a556-186">打开相关日记帐。</span><span class="sxs-lookup"><span data-stu-id="4a556-186">Open the relevant journal.</span></span>
1. <span data-ttu-id="4a556-187">选择操作窗格上的 **工作流** 按钮打开一个下拉对话框。</span><span class="sxs-lookup"><span data-stu-id="4a556-187">Select the **Workflow** button on the Action Pane to open a drop-down dialog box.</span></span> <span data-ttu-id="4a556-188">选择 **工作流历史记录**。</span><span class="sxs-lookup"><span data-stu-id="4a556-188">Select **Workflow history**.</span></span> <span data-ttu-id="4a556-189">有关详细信息，请参阅[查看工作流历史记录](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md)。</span><span class="sxs-lookup"><span data-stu-id="4a556-189">For more information, see [View workflow history](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]