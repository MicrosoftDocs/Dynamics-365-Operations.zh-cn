---
title: 供应商的类别请求
description: 本主题介绍供应商如何为其帐户请求采购类别。 另外还介绍了由采购代理完成的审核流程。
author: kamaybac
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1951f85f84c3b8b2d42f49d5f464d90d410ebfa2
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015943"
---
# <a name="category-requests-from-vendors"></a><span data-ttu-id="a4e0d-104">供应商的类别请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-104">Category requests from vendors</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4e0d-105">类别请求流程让供应商可以请求将新的采购类别与其帐户关联。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-105">The category request process lets vendors request that new procurement categories be associated with their account.</span></span> <span data-ttu-id="a4e0d-106">这些采购类别然后可以由相关的采购流程使用。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-106">Those procurement categories can then be used by the related procurement and sourcing processes.</span></span> <span data-ttu-id="a4e0d-107">（有关详细信息，请参阅[采购目录概览](procurement-catalogs.md)。）</span><span class="sxs-lookup"><span data-stu-id="a4e0d-107">(For more information, see [Procurement catalogs overview](procurement-catalogs.md).)</span></span>

<span data-ttu-id="a4e0d-108">类别请求由供应商在 **供应商信息** 工作区发起。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-108">Category requests are initiated by vendors in the **Vendor information** workspace.</span></span> <span data-ttu-id="a4e0d-109">然后它们被提交给您的机构进行审查和审核。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-109">They are then submitted to your agency for review and approval.</span></span> <span data-ttu-id="a4e0d-110">批准的类别将被添加到供应商帐户的采购类别列表中。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-110">Approved categories are added to the list of procurement categories for the vendor's account.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="a4e0d-111">在系统中开启此功能</span><span class="sxs-lookup"><span data-stu-id="a4e0d-111">Turn on the feature in your system</span></span>

<span data-ttu-id="a4e0d-112">如果您的系统尚未包含本主题所述的功能，请转到 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，打开 *允许供应商通过供应商协作申请采购类别* 功能。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-112">If your system doesn't already include the feature that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Allow vendors to apply for procurement categories through vendor collaboration* feature.</span></span>

<span data-ttu-id="a4e0d-113">打开此功能后，您仍然可以将采购类别手动添加到供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-113">After the feature is turned on, you can still manually add procurement categories to vendor accounts.</span></span> <span data-ttu-id="a4e0d-114">有关信息，请参阅[审核特定采购类别的供应商](tasks/approve-vendors-specific-procurement-categories.md)。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-114">For information, see [Approve vendors for specific procurement categories](tasks/approve-vendors-specific-procurement-categories.md).</span></span>

## <a name="vendor-collaboration-requirements"></a><span data-ttu-id="a4e0d-115">供应商协作要求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-115">Vendor collaboration requirements</span></span>

<span data-ttu-id="a4e0d-116">供应商必须先进行供应商协作设置，然后才可以与类别请求进行交互。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-116">Before a vendor can interact with category requests, it must be set up for vendor collaboration.</span></span>

<span data-ttu-id="a4e0d-117">供应商必须至少有一个供应商协作用户。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-117">The vendor must have at least one vendor collaboration user.</span></span> <span data-ttu-id="a4e0d-118">只有具有 *供应商管理员(外部)* 安全角色的供应商用户可以创建和提交类别请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-118">Only vendor users with the *Vendor admin (external)* security role can create and submit category requests.</span></span>

<span data-ttu-id="a4e0d-119">有关详细信息，请参阅[设置和维护供应商协作](set-up-maintain-vendor-collaboration.md)。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-119">For more information, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span>

## <a name="set-up-the-vendor-category-request-workflow"></a><span data-ttu-id="a4e0d-120">设置供应商类别请求工作流</span><span class="sxs-lookup"><span data-stu-id="a4e0d-120">Set up the Vendor category request workflow</span></span>

<span data-ttu-id="a4e0d-121">*供应商类别请求* 工作流必须在采购工作流中设置。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-121">The *Vendor category request* workflow must be set up in the procurement and sourcing workflows.</span></span> <span data-ttu-id="a4e0d-122">供应商将提交新的类别请求，您可以对其进行审查和审核。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-122">Vendors will submit new category requests that you can review and approve.</span></span> <span data-ttu-id="a4e0d-123">审核类别请求后，所请求的采购类别将被添加到供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-123">Requested procurement categories are added to a vendor account after a category request is approved.</span></span>

<span data-ttu-id="a4e0d-124">以下示例显示如何设置一个有一位审核人的简单 *供应商类别请求* 工作流。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-124">The following example shows how to set up a simple *Vendor category request* workflow that has a single approver.</span></span> <span data-ttu-id="a4e0d-125">您必须查看内部流程来确定适合您的机构的工作流设置。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-125">You must review your internal processes to determine the appropriate workflow setup for your agency.</span></span>

1. <span data-ttu-id="a4e0d-126">转到 **采购 \> 设置 \> 采购工作流**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-126">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing workflows**.</span></span>
1. <span data-ttu-id="a4e0d-127">在操作窗格上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a4e0d-128">在对话框中，选择 **供应商类别请求工作流** 打开工作流编辑器。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-128">In the dialog box, select **Vendor category request workflow** to open the workflow editor.</span></span>
1. <span data-ttu-id="a4e0d-129">登录到工作流编辑器。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-129">Sign in to the workflow editor.</span></span>
1. <span data-ttu-id="a4e0d-130">在操作窗格上，选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-130">On the Action Pane, select **Properties**.</span></span>
1. <span data-ttu-id="a4e0d-131">在工作流的 **属性** 页上，在 **提交说明** 字段中，输入说明文本。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-131">On the **Properties** page for the workflow, in the **Submission instructions** field, enter instruction text.</span></span> <span data-ttu-id="a4e0d-132">说明会在供应商提交类别请求时对他们可见。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-132">The instructions will be visible to vendors when they submit a category request.</span></span>
1. <span data-ttu-id="a4e0d-133">关闭 **属性** 页。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-133">Close the **Properties** page.</span></span>
1. <span data-ttu-id="a4e0d-134">将 **审核新类别请求** 工作流元素拖到画布上。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-134">Drag the **Approve new category request** workflow element onto the canvas.</span></span>
1. <span data-ttu-id="a4e0d-135">将一个链接从 **开始** 工作流元素拖到 **审核新类别请求** 工作流元素。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-135">Drag a link from the **Start** workflow element to the **Approve new category request** workflow element.</span></span>
1. <span data-ttu-id="a4e0d-136">将一个链接从 **审核新类别请求** 工作流元素拖到 **结束** 工作流元素。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-136">Drag a link from the **Approve new category request** workflow element to the **End** workflow element.</span></span>
1. <span data-ttu-id="a4e0d-137">两次点击（或双击）**审核新类别请求** 工作流元素。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-137">Double-tap (or double-click) the **Approve new category request** workflow element.</span></span>
1. <span data-ttu-id="a4e0d-138">选择并按住（或右键单击）**步骤 1** 工作流元素，然后选择 **属性**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-138">Select and hold (or right-click) the **Step 1** workflow element, and then select **Properties**.</span></span>
1. <span data-ttu-id="a4e0d-139">在工作流元素的 **属性** 页上，在 **工作项主题** 字段中，输入主题文本。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-139">On the **Properties** page for the workflow element, in the **Work item subject** field, enter subject text.</span></span> <span data-ttu-id="a4e0d-140">此文本将显示为 **分配给我的工作项** 页上的 **主题** 字段的值。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-140">This text will be shown as the value of the **Subject** field on the **Work items assigned to me** page.</span></span>
1. <span data-ttu-id="a4e0d-141">在 **工作项说明** 字段中，输入说明文本。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-141">In the **Work item instructions** field, enter instruction text.</span></span> <span data-ttu-id="a4e0d-142">说明将在审核人在类别请求的操作窗格上选择 **工作流** 时对他们可见。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-142">The instructions will be visible to approvers when they select **Workflow** on the Action Pane of a category request.</span></span>
1. <span data-ttu-id="a4e0d-143">在左窗格中，选择 **分配**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-143">In the left pane, select **Assignment**.</span></span>
1. <span data-ttu-id="a4e0d-144">在 **分配类型** 选项卡上，将 **将用户分配给此工作流元素** 设置为 *用户*。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-144">On the **Assignment type** tab, set **Assign users to this workflow element** to *User*.</span></span>
1. <span data-ttu-id="a4e0d-145">在 **用户** 选项卡上，在 **可用用户** 列表中，选择一个审核人。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-145">On the **User** tab, in the **Available users** list, select an approver.</span></span> <span data-ttu-id="a4e0d-146">例如，在采购部门选择一个用户。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-146">For example, select a user in the Procurement department.</span></span>
1. <span data-ttu-id="a4e0d-147">选择向右箭头按钮 (**\>**) 将审核人移到 **所选用户** 列表中。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-147">Select the right arrow button (**\>**) to move the approver to the **Selected users** list.</span></span>
1. <span data-ttu-id="a4e0d-148">关闭 **属性** 页。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-148">Close the **Properties** page.</span></span>
1. <span data-ttu-id="a4e0d-149">选择 **保存并关闭**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-149">Select **Save and close**.</span></span>
1. <span data-ttu-id="a4e0d-150">在 **版本说明** 字段中，输入有关工作流的说明。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-150">In the **Version notes** field, enter notes about the workflow.</span></span>
1. <span data-ttu-id="a4e0d-151">选择 **确定** 保存工作流。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-151">Select **OK** to save the workflow.</span></span>
1. <span data-ttu-id="a4e0d-152">如果您已准备好开始测试工作流，选择 **激活新版本**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-152">If you're ready to start to test the workflow, select **Activate the new version**.</span></span> <span data-ttu-id="a4e0d-153">否则，选择 **不激活新版本**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-153">Otherwise, select **Do not activate the new version**.</span></span>
1. <span data-ttu-id="a4e0d-154">选择 **确定** 完成工作流设置。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-154">Select **OK** to complete the workflow setup.</span></span>

> [!TIP]
> <span data-ttu-id="a4e0d-155">如果您的机构不要求审核类别请求，您应该将工作流配置为自动审核。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-155">If your agency doesn't require approval of category requests, you should configure the workflow for automatic approval.</span></span>

<span data-ttu-id="a4e0d-156">有关如何设置工作流的详细信息，请参阅[工作流系统概述](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md)。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-156">For more information about how to set up workflows, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).</span></span>

## <a name="create-and-submit-a-category-request"></a><span data-ttu-id="a4e0d-157">创建和提交类别请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-157">Create and submit a category request</span></span>

<span data-ttu-id="a4e0d-158">本节介绍供应商如何使用 **供应商信息** 工作区创建、编辑、查看和提交类别请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-158">This section describes how vendors can use the **Vendor information** workspace to create, edit, view, and submit category requests.</span></span>

### <a name="start-a-new-request"></a><span data-ttu-id="a4e0d-159">发起新请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-159">Start a new request</span></span>

<span data-ttu-id="a4e0d-160">要发起新的类别请求，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-160">To start a new category request, follow these steps.</span></span>

1. <span data-ttu-id="a4e0d-161">在 **供应商信息** 工作区中，选择 **类别请求** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-161">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="a4e0d-162">在 **类别请求** 页上的操作窗格上，选择 **新类别请求**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-162">On the **Category requests** page, on the Action Pane, select **New category request**.</span></span>
1. <span data-ttu-id="a4e0d-163">在 **新类别请求** 对话框中，通过导航树和/或使用列表顶部的筛选器查找要申请的类别。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-163">In the **New category request** dialog box, find the category that you want to apply for by navigating the tree and/or using the filter at the top of the list.</span></span> <span data-ttu-id="a4e0d-164">选中每个相关类别的复选框。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-164">Select the checkbox for each relevant category.</span></span>

    <span data-ttu-id="a4e0d-165">请注意以下点：</span><span class="sxs-lookup"><span data-stu-id="a4e0d-165">Note the following points:</span></span>

    - <span data-ttu-id="a4e0d-166">供应商帐户上当前处于活动状态的类别显示为选中状态，无法删除。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-166">Categories that are currently active on your vendor account are shown as selected and can't be removed.</span></span>
    - <span data-ttu-id="a4e0d-167">您可以在一个类别请求中请求多个采购类别。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-167">You can request multiple procurement categories in a single category request.</span></span>

1. <span data-ttu-id="a4e0d-168">选择 **确定** 创建草稿请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-168">Select **OK** to create the draft request.</span></span>

    <span data-ttu-id="a4e0d-169">现在，新草稿请求显示在 **类别请求** 页上。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-169">The new draft request now appears on the **Category requests** page.</span></span>

1. <span data-ttu-id="a4e0d-170">打开新的草稿请求，根据需要进行审查和编辑。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-170">Open the new draft request to review and edit it as required.</span></span>

    - <span data-ttu-id="a4e0d-171">要查看请求中当前包含的类别列表，选择 **请求的类别** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-171">To view the list of categories that are currently included in the request, select the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="a4e0d-172">要查看您的活动类别，打开页面右侧的 **活动类别** 速见表。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-172">To view your active categories, open the **Active categories** FactBox on the right side of the page.</span></span>
    - <span data-ttu-id="a4e0d-173">要将类别添加到请求，在 **请求的类别** 快速选项卡上的工具栏上选择 **添加**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-173">To add a category to the request, select **Add** on the toolbar on the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="a4e0d-174">要从请求中删除类别，在 **请求的类别** 快速选项卡上选择类别，然后在工具栏上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-174">To remove a category from the request, select the category on the **Requested categories** FastTab, and then select **Remove** on the toolbar.</span></span>
    - <span data-ttu-id="a4e0d-175">要将文档附加到请求，在操作窗格上选择 **附件**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-175">To attach a document to the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="a4e0d-176">附加的文档将在审核人查看类别请求时对其可用。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-176">Attached documents will be available to approvers when they review the category request.</span></span>
    - <span data-ttu-id="a4e0d-177">要从请求中删除附加的文档，在操作窗格上选择 **附件**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-177">To remove an attached document from the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="a4e0d-178">选择要删除的文档，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-178">Select the document to remove, and then select **Delete** on the Action Pane.</span></span>

1. <span data-ttu-id="a4e0d-179">如果您已准备好提交请求，在操作窗格上选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-179">If you're ready to submit the request, select **Submit** on the Action Pane.</span></span> <span data-ttu-id="a4e0d-180">否则，只需关闭页面，跳过此过程的其余步骤。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-180">Otherwise, just close the page and skip the remaining steps of this procedure.</span></span> <span data-ttu-id="a4e0d-181">然后，您可以稍后返回到请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-181">You can then return to the request later.</span></span>
1. <span data-ttu-id="a4e0d-182">阅读出现的所有提交说明，然后选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-182">Read any submission instructions that appear, and then select **Submit**.</span></span>
1. <span data-ttu-id="a4e0d-183">在 **注释** 框中，输入所需的所有其他信息。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-183">In the **Comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="a4e0d-184">然后选择 **提交** 完成请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-184">Then select **Submit** to complete the request.</span></span>

### <a name="edit-a-draft-or-recalled-request"></a><span data-ttu-id="a4e0d-185">编辑草稿或撤回请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-185">Edit a draft or recalled request</span></span>

<span data-ttu-id="a4e0d-186">要编辑草稿或撤回的类别请求，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-186">To edit a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="a4e0d-187">在 **供应商信息** 工作区中，选择 **类别请求** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-187">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="a4e0d-188">选择草稿或撤回的请求将其打开。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-188">Select the draft or recalled request to open it.</span></span>
1. <span data-ttu-id="a4e0d-189">根据需要编辑请求，然后按照上一过程中所述关闭或提交请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-189">Edit the request as required, and then either close it or submit it as described in the previous procedure.</span></span>

### <a name="submit-a-draft-or-recalled-request"></a><span data-ttu-id="a4e0d-190">提交草稿或撤回请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-190">Submit a draft or recalled request</span></span>

<span data-ttu-id="a4e0d-191">要提交草稿或撤回的类别请求，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-191">To submit a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="a4e0d-192">在 **供应商信息** 工作区中，选择 **类别请求** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-192">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="a4e0d-193">选择您要提交的草稿或撤回请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-193">Select the draft or recalled request that you want to submit.</span></span>
1. <span data-ttu-id="a4e0d-194">在操作窗格上，选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-194">On the Action Pane, select **Submit**.</span></span>
1. <span data-ttu-id="a4e0d-195">阅读出现的所有提交说明，然后选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-195">Read any submission instructions that appear, and then select **Submit**.</span></span>
1. <span data-ttu-id="a4e0d-196">在 **注释** 框中，输入所需的所有其他信息。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-196">In the **Comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="a4e0d-197">然后选择 **提交** 完成请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-197">Then select **Submit** to complete the request.</span></span>

    <span data-ttu-id="a4e0d-198">类别请求的状态将更改为以下值之一：</span><span class="sxs-lookup"><span data-stu-id="a4e0d-198">The status of the category request is changed to one of the following values:</span></span>

    - <span data-ttu-id="a4e0d-199">_待审查_ – 请求在工作流中。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-199">_Pending review_ – The request is in the workflow.</span></span>
    - <span data-ttu-id="a4e0d-200">_待审核_ – 需要审核。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-200">_Pending approval_ – Approval is required.</span></span>

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a><span data-ttu-id="a4e0d-201">撤回尚未审核的已提交请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-201">Recall a submitted request that hasn't yet been approved</span></span>

<span data-ttu-id="a4e0d-202">要撤回已提交但尚未审核的类别请求，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-202">To recall a category request that has been submitted but hasn't yet been approved, follow these steps.</span></span>

1. <span data-ttu-id="a4e0d-203">在 **供应商信息** 工作区中，选择 **类别请求** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-203">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="a4e0d-204">选择您要撤回的待处理请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-204">Select the pending request that you want to recall.</span></span>
1. <span data-ttu-id="a4e0d-205">在操作窗格上，选择 **撤回**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-205">On the Action Pane, select **Recall**.</span></span>
1. <span data-ttu-id="a4e0d-206">在 **输入注释** 框中，输入所需的所有其他信息。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-206">In the **Enter a comment** box, enter any additional information that is required.</span></span> <span data-ttu-id="a4e0d-207">然后选择 **提交** 完成请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-207">Then select **Submit** to complete the request.</span></span>

    <span data-ttu-id="a4e0d-208">类别请求的状态将更改为 _已取消_。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-208">The status of the category request is changed to _Canceled_.</span></span> <span data-ttu-id="a4e0d-209">请求将保持此状态，直到您将其删除或重新提交。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-209">The request will remain in this status until you delete or resubmit it.</span></span>

### <a name="delete-a-draft-or-recalled-request"></a><span data-ttu-id="a4e0d-210">删除草稿或撤回请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-210">Delete a draft or recalled request</span></span>

<span data-ttu-id="a4e0d-211">要删除草稿或撤回的类别请求，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-211">To delete a draft or recalled category request, follow these steps.</span></span>

1. <span data-ttu-id="a4e0d-212">在 **供应商信息** 工作区中，选择 **类别请求** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-212">In the **Vendor information** workspace, select the **Category requests** tile.</span></span>
1. <span data-ttu-id="a4e0d-213">选择您要删除的草稿或撤回请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-213">Select the draft or recalled request that you want to delete.</span></span>
1. <span data-ttu-id="a4e0d-214">在操作窗格上，选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-214">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="a4e0d-215">选择 **是** 以确认删除。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-215">Select **Yes** to confirm the deletion.</span></span>

### <a name="view-completed-requests"></a><span data-ttu-id="a4e0d-216">查看完成的请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-216">View completed requests</span></span>

<span data-ttu-id="a4e0d-217">要查看已完成的请求，打开 **供应商信息** 工作区，选择 **类别请求** 磁贴。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-217">To view completed requests, open the **Vendor information** workspace and select the **Category requests** tile.</span></span> <span data-ttu-id="a4e0d-218">已完成的类别请求具有以下状态之一：</span><span class="sxs-lookup"><span data-stu-id="a4e0d-218">Category requests that have been completed will have one of the following statuses:</span></span>

- <span data-ttu-id="a4e0d-219">_已审核_ – 请求已经审核。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-219">_Approved_ – The request was approved.</span></span> <span data-ttu-id="a4e0d-220">要查看新添加的类别，返回 **供应商信息** 工作区，在左侧窗格中打开 **更多详细信息** 下拉列表，然后选择 **类别**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-220">To view the newly added categories, go back to the **Vendor information** workspace, open the **More details** drop-down list in the left pane, and then select **Categories**.</span></span>
- <span data-ttu-id="a4e0d-221">_已拒绝_ – 请求被拒绝。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-221">_Rejected_ – The request was rejected.</span></span> <span data-ttu-id="a4e0d-222">您可以根据需要创建新的类别请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-222">You can create a new category request as required.</span></span>

## <a name="review-category-requests"></a><span data-ttu-id="a4e0d-223">审查类别请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-223">Review category requests</span></span>

<span data-ttu-id="a4e0d-224">本节说明如何批准、拒绝和委托供应商提交的类别请求，以及如何查看已完成的请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-224">This section explains how to approve, reject, and delegate category requests that vendors submitted, and how to view completed requests.</span></span> <span data-ttu-id="a4e0d-225">这些工作流操作适用于整个类别请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-225">These workflow actions are for the whole category request.</span></span>

### <a name="view-category-requests"></a><span data-ttu-id="a4e0d-226">查看类别请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-226">View category requests</span></span>

<span data-ttu-id="a4e0d-227">要查看类别请求，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-227">To view category requests, follow these steps.</span></span>

1. <span data-ttu-id="a4e0d-228">转到 **采购 \> 供应商 \> 供应商协作请求 \> 类别请求**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-228">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>

    <span data-ttu-id="a4e0d-229">**类别请求** 页将出现。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-229">The **Category requests** page appears.</span></span> <span data-ttu-id="a4e0d-230">默认页面视图显示状态为 *待处理操作* 的类别请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-230">The default page view shows category requests that have a status of *Pending action*.</span></span>

1. <span data-ttu-id="a4e0d-231">要查看所有请求，在 **显示请求** 字段中选择 *所有*。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-231">To view all requests, select *All* in the **Show requests** field.</span></span>
1. <span data-ttu-id="a4e0d-232">打开请求以根据需要进行审查和编辑。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-232">Open a request to review and edit it as required.</span></span>

    - <span data-ttu-id="a4e0d-233">要查看请求中当前包含的类别列表，选择 **请求的类别** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-233">To view the list of categories that are currently included in the request, select the **Requested categories** FastTab.</span></span>
    - <span data-ttu-id="a4e0d-234">要查看活动类别，打开页面右侧的 **活动类别** 速见表。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-234">To view the active categories, open the **Active categories** FactBox on the right side of the page.</span></span>
    - <span data-ttu-id="a4e0d-235">如果提交了文档，操作窗格上的 **附件**（回形针）按钮将显示所附文档的数量。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-235">If documents were submitted, the  **Attachments** (paper clip) button on the Action Pane shows a count of the attached documents.</span></span> <span data-ttu-id="a4e0d-236">要查看附加的文档，选择 **附件** 按钮。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-236">To view attached documents, select the **Attachments** button.</span></span> <span data-ttu-id="a4e0d-237">然后选择要查看的文档并选择 **打开** 进行查看。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-237">Then select the document to view and select **Open** to view it.</span></span>
    - <span data-ttu-id="a4e0d-238">要将文档附加到请求，在操作窗格上选择 **附件**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-238">To attach a document to the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="a4e0d-239">附加的文档将在审核人查看类别请求时对其可用。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-239">Attached documents will be available to approvers when they review the category request.</span></span>
    - <span data-ttu-id="a4e0d-240">要从请求中删除附加的文档，在操作窗格上选择 **附件**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-240">To remove an attached document from the request, select **Attachments** on the Action Pane.</span></span> <span data-ttu-id="a4e0d-241">选择要删除的文档，然后在操作窗格上选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-241">Select the document to remove, and then select **Delete** on the Action Pane.</span></span>
    - <span data-ttu-id="a4e0d-242">要查看工作流历史记录，在操作窗格上选择 **工作流**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-242">To view the workflow history, select **Workflow** on the Action Pane.</span></span> <span data-ttu-id="a4e0d-243">在工作流选项中，选择 **更多**，然后选择 **工作流历史记录**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-243">In the workflow options, select **More** and then **Workflow history**.</span></span> <span data-ttu-id="a4e0d-244">**工作流历史记录** 页将出现。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-244">The **Workflow history** page appears.</span></span>

### <a name="approve-a-pending-category-request"></a><span data-ttu-id="a4e0d-245">批准待处理类别请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-245">Approve a pending category request</span></span>

<span data-ttu-id="a4e0d-246">要批准待处理类别请求，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-246">To approve a pending category request, follow these steps.</span></span>

1. <span data-ttu-id="a4e0d-247">转到 **采购 \> 供应商 \> 供应商协作请求 \> 类别请求**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-247">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="a4e0d-248">选择要批准的待处理请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-248">Select the pending request to approve.</span></span>
1. <span data-ttu-id="a4e0d-249">审查类别请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-249">Review the category request.</span></span>
1. <span data-ttu-id="a4e0d-250">可选：在 **常规** 快速选项卡上，在 **原因代码** 字段中，选择一个原因代码。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-250">Optional: On the **General** FastTab, in the **Reason code** field, select a reason code.</span></span> <span data-ttu-id="a4e0d-251">然后，在 **原因注释** 字段中，输入有关原因代码的注释。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-251">Then, in the **Reason comment** field, enter a comment about the reason code.</span></span>
1. <span data-ttu-id="a4e0d-252">在操作窗格上，选择 **工作流**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-252">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="a4e0d-253">在工作流选项中，选择 **批准**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-253">In the workflow options, select **Approve**.</span></span>
1. <span data-ttu-id="a4e0d-254">在 **注释** 字段中，输入所需的所有其他信息。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-254">In the **Comment** field, enter any additional information that is required.</span></span> <span data-ttu-id="a4e0d-255">然后选择 **批准** 完成请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-255">Then select **Approve** to complete the request.</span></span>

    <span data-ttu-id="a4e0d-256">类别请求的状态将更改为 _已审核_，采购类别将被添加到供应商帐户。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-256">The status of the category request is changed to _Approved_, and the procurement categories are added to the vendor account.</span></span>

### <a name="reject-a-pending-category-request"></a><span data-ttu-id="a4e0d-257">拒绝待处理类别请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-257">Reject a pending category request</span></span>

<span data-ttu-id="a4e0d-258">要拒绝待处理类别请求，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-258">To reject a pending category request, follow these steps.</span></span>

1. <span data-ttu-id="a4e0d-259">转到 **采购 \> 供应商 \> 供应商协作请求 \> 类别请求**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-259">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="a4e0d-260">选择要拒绝的待处理请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-260">Select the pending request to reject.</span></span>
1. <span data-ttu-id="a4e0d-261">审查类别请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-261">Review the category request.</span></span>
1. <span data-ttu-id="a4e0d-262">在操作窗格上，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-262">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="a4e0d-263">在 **常规** 快速选项卡上，在 **原因代码** 字段中，选择一个原因代码。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-263">On the **General** FastTab, in the **Reason code** field, select a reason code.</span></span> <span data-ttu-id="a4e0d-264">然后，在 **原因注释** 字段中，输入有关原因代码的注释。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-264">Then, in the **Reason comment** field, enter a comment about the reason code.</span></span>
1. <span data-ttu-id="a4e0d-265">在操作窗格上，选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-265">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="a4e0d-266">在操作窗格上，选择 **工作流**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-266">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="a4e0d-267">在工作流选项中，选择 **更多**，然后选择 **拒绝**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-267">In the workflow options, select **More** and then **Reject**.</span></span>
1. <span data-ttu-id="a4e0d-268">在 **注释** 字段中，输入所需的所有其他信息。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-268">In the **Comment** field, enter any additional information that is required.</span></span> <span data-ttu-id="a4e0d-269">然后选择 **拒绝** 完成请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-269">Then select **Reject** to complete the request.</span></span>

    <span data-ttu-id="a4e0d-270">类别请求的状态将更改为 _已拒绝_。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-270">The status of the category request is changed to _Rejected_.</span></span> <span data-ttu-id="a4e0d-271">此时，供应商可以根据需要创建新的类别请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-271">At this point, the vendor can create a new category request as required.</span></span>

### <a name="delegate-a-pending-category-request"></a><span data-ttu-id="a4e0d-272">委托待处理类别请求</span><span class="sxs-lookup"><span data-stu-id="a4e0d-272">Delegate a pending category request</span></span>

<span data-ttu-id="a4e0d-273">要将待处理类别请求委托给另一个用户，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-273">To delegate a pending category request to another user, follow these steps.</span></span>

1. <span data-ttu-id="a4e0d-274">转到 **采购 \> 供应商 \> 供应商协作请求 \> 类别请求**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-274">Go to **Procurement and sourcing \> Vendors \> Vendor collaboration requests \> Category requests**.</span></span>
1. <span data-ttu-id="a4e0d-275">选择您要审核的待处理请求。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-275">Select the pending request that you want to approve.</span></span>
1. <span data-ttu-id="a4e0d-276">在操作窗格上，选择 **工作流**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-276">On the Action Pane, select **Workflow**.</span></span>
1. <span data-ttu-id="a4e0d-277">在工作流选项中，选择 **更多**，然后选择 **委托**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-277">In the workflow options, select **More** and then **Delegate**.</span></span>
1. <span data-ttu-id="a4e0d-278">在 **用户** 字段中，选择要向其分配类别请求以进行审查的用户。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-278">In the **User** field, select the user to assign the category request to for review.</span></span>
1. <span data-ttu-id="a4e0d-279">在 **注释** 字段中，输入所需的所有其他信息。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-279">In the **Comment** field, enter any additional information that is required.</span></span>
1. <span data-ttu-id="a4e0d-280">选择 **委托** 完成委托。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-280">Select **Delegate** to complete the delegation.</span></span> <span data-ttu-id="a4e0d-281">所选用户现在可以审查类别请求了。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-281">The selected user can now review the category request.</span></span>

### <a name="view-procurement-categories-for-a-vendor"></a><span data-ttu-id="a4e0d-282">查看供应商的采购类别</span><span class="sxs-lookup"><span data-stu-id="a4e0d-282">View procurement categories for a vendor</span></span>

<span data-ttu-id="a4e0d-283">要在审核类别请求后查看供应商的采购类别，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-283">To view procurement categories for a vendor after a category request is approved, follow these steps.</span></span>

1. <span data-ttu-id="a4e0d-284">转到 **采购 \> 供应商 \> 所有供应商**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-284">Go to **Procurement and sourcing \> Vendors \> All vendors**.</span></span>
1. <span data-ttu-id="a4e0d-285">在 **所有供应商** 页上，选择要查看其采购类别的供应商。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-285">On the **All vendors** page, select the vendor that you want to view procurement categories for.</span></span>
1. <span data-ttu-id="a4e0d-286">在操作窗格上，打开 **常规** 选项卡，然后从 **设置** 组中，选择 **类别**。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-286">On the Action Pane, open the **General** tab and, from the **Set up** group, select **Categories**.</span></span>

    <span data-ttu-id="a4e0d-287">**类别** 页将显示。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-287">The **Categories** page appears.</span></span> <span data-ttu-id="a4e0d-288">**采购** 快速选项卡显示通过类别请求添加的采购类别。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-288">The **Procurement** FastTab shows procurement categories that were added through the category request.</span></span>

1. <span data-ttu-id="a4e0d-289">在 **采购** 快速选项卡上，您可以根据需要进行更改。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-289">On the **Procurement** FastTab, you can make changes if needed.</span></span> <span data-ttu-id="a4e0d-290">例如，您可以将 **供应商类别状态** 字段设置为 _首选_。</span><span class="sxs-lookup"><span data-stu-id="a4e0d-290">For example, you can set the **Vendor category status** field to _Preferred_.</span></span>
