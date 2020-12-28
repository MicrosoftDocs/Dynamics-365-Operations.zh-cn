---
title: 使用租赁审批工作流
description: 本主题说明如何使用工作流审批资产租赁，以及如何跟踪工作流的状态和历史记录。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1805e1f87ee70a1f35d9105b8f7ad6c95861efcc
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440968"
---
# <a name="use-lease-approval-workflows"></a><span data-ttu-id="48878-103">使用租赁审批工作流</span><span class="sxs-lookup"><span data-stu-id="48878-103">Use lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="48878-104">本主题说明如何使用工作流审批资产租赁，以及如何跟踪工作流的状态和历史记录。</span><span class="sxs-lookup"><span data-stu-id="48878-104">This topic explains how to use workflows to approve asset leases, and how to track the status and history of the workflows.</span></span> <span data-ttu-id="48878-105">工作流通过提供一组标准的审批步骤并分配审批流程的每个步骤的特定用户，帮助租赁审批的管理保持一致。</span><span class="sxs-lookup"><span data-stu-id="48878-105">Workflows help bring consistency to the management of lease approvals by providing a standard set of approval steps and assigning specific users who approve each step of the process.</span></span> <span data-ttu-id="48878-106">审批者可以批准租赁，拒绝租赁，申请更改租赁或将租赁分配给其他用户进行审批。</span><span class="sxs-lookup"><span data-stu-id="48878-106">An approver can approve a lease, reject it, request a change to it, or assign it to another user for approval.</span></span> <span data-ttu-id="48878-107">通过让您跟踪其状态和历史记录，工作流还可以提高审批过程的可见性。</span><span class="sxs-lookup"><span data-stu-id="48878-107">Workflows can also bring more visibility into the approval process by letting you track their status and history.</span></span> <span data-ttu-id="48878-108">此外，您还可以查看集中工作清单，该清单列出了分配给特定审核者的任务和审批。</span><span class="sxs-lookup"><span data-stu-id="48878-108">Additionally, you can view a centralized worklist that lists the tasks and approvals that are assigned to specific approvers.</span></span>

<span data-ttu-id="48878-109">在使用此过程之前，请确保至少已创建“租赁审批”工作流。</span><span class="sxs-lookup"><span data-stu-id="48878-109">Before you use this procedure, make sure that at least on lease approval workflow has been created.</span></span> <span data-ttu-id="48878-110">如果不存在工作流，请创建一个。</span><span class="sxs-lookup"><span data-stu-id="48878-110">If no workflow exists, create one.</span></span> <span data-ttu-id="48878-111">有关如何设置工作流的详细信息，请参阅[设置审批工作流](set-up-lease-wrkflw.md)。</span><span class="sxs-lookup"><span data-stu-id="48878-111">For information about how to set up a workflow, see [Set up lease approval workflows](set-up-lease-wrkflw.md).</span></span>

1. <span data-ttu-id="48878-112">提交日记帐以供审核。</span><span class="sxs-lookup"><span data-stu-id="48878-112">Submit a lease for approval.</span></span> <span data-ttu-id="48878-113">在租赁的 **帐簿详细资料** 页面，选择 **工作流**，然后选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="48878-113">On the **Book details** page for the lease, select **Workflow**, and then select **Submit**.</span></span>
2. <span data-ttu-id="48878-114">在出现的对话框中，您可以添加注释。</span><span class="sxs-lookup"><span data-stu-id="48878-114">In the dialog box that appears, you can add a comment.</span></span> <span data-ttu-id="48878-115">指定的审批者将看到此注释以及租赁。</span><span class="sxs-lookup"><span data-stu-id="48878-115">The designated approver will see this comment together with the lease.</span></span> <span data-ttu-id="48878-116">输入完注释后，选择 **提交**。</span><span class="sxs-lookup"><span data-stu-id="48878-116">When you've finished entering the comment, select **Submit**.</span></span> <span data-ttu-id="48878-117">租赁已提交到工作流系统，审批者将接收以供审批。</span><span class="sxs-lookup"><span data-stu-id="48878-117">The lease is submitted to the workflow system, and the approver receives it for approval.</span></span>
3. <span data-ttu-id="48878-118">要查看指派给其审批的租赁，请转到 **模型 \> 通用 \> 工作项 \> 分配给我的工作项**。</span><span class="sxs-lookup"><span data-stu-id="48878-118">To view the leases that they are designated for approval, go to **Modules \> Common \> Work items \> Work items assigned to me**.</span></span>
4. <span data-ttu-id="48878-119">在 **分配给我的工作项** 页面上，选择要查看的租赁的 **租赁 ID**。</span><span class="sxs-lookup"><span data-stu-id="48878-119">On the **Work items assigned to me** page, select the **Lease ID** link for the lease that you want to view.</span></span> <span data-ttu-id="48878-120">出现的页面取决于您可以访问的租赁帐簿和租赁详细信息。</span><span class="sxs-lookup"><span data-stu-id="48878-120">The page that appears depends on the lease books and lease details that you have access to.</span></span>
5. <span data-ttu-id="48878-121">查看完租赁后，选择 **工作流**，并决定应采取的措施。</span><span class="sxs-lookup"><span data-stu-id="48878-121">When you've finish viewing the lease, select **Workflow**, and decide what action should be taken.</span></span> <span data-ttu-id="48878-122">选项包括 **批准**、**拒绝**、**请求更改**、**委派** 和 **取消**。</span><span class="sxs-lookup"><span data-stu-id="48878-122">The options include **Approve**, **Rejected**, **Request change**, **Delegate**, and **Canceled**.</span></span> <span data-ttu-id="48878-123">您也可以选择 **查看历史记录** 查看所选租赁的审批历史记录。</span><span class="sxs-lookup"><span data-stu-id="48878-123">You can also select **View history** to view the approval history for the selected lease.</span></span>
6. <span data-ttu-id="48878-124">选择操作后，输入注释以描述该操作。</span><span class="sxs-lookup"><span data-stu-id="48878-124">After you've selected an action, enter a comment to describe the action.</span></span> <span data-ttu-id="48878-125">输入完注释后，选择列表中的 **已批准** 操作。</span><span class="sxs-lookup"><span data-stu-id="48878-125">When you've finished entering the comment, select the **Approved** action in the list.</span></span>
7. <span data-ttu-id="48878-126">要查看审批操作，请从 **租赁摘要** 页面返回到 **租赁详细信息** 页，然后选择 **工作流 \> 查看历史记录**。</span><span class="sxs-lookup"><span data-stu-id="48878-126">To view the approval actions, go back to the **Lease details** page from the **Lease summary** page, and then select **Workflow \> View history**.</span></span>

    <span data-ttu-id="48878-127">您可以在 **工作流历史记录** 页上查看工作流活动。</span><span class="sxs-lookup"><span data-stu-id="48878-127">You can view the workflow activities on the **Workflow history** page.</span></span> <span data-ttu-id="48878-128">此页面显示已对特定租赁采取的工作流步骤。</span><span class="sxs-lookup"><span data-stu-id="48878-128">This page shows the workflow steps that have been taken on the specific lease.</span></span> <span data-ttu-id="48878-129">您也可以使用 **工作项** 字段查看已分配工作项的状态。</span><span class="sxs-lookup"><span data-stu-id="48878-129">You can also use the **Work items** field to view the status of the assigned work items.</span></span>

8. <span data-ttu-id="48878-130">要停止工作流，请在 **工作流历史记录** 页面上，选择 **撤回**。</span><span class="sxs-lookup"><span data-stu-id="48878-130">To stop a workflow, on the **Workflow history** page, select **Recall**.</span></span> <span data-ttu-id="48878-131">在显示的对话框中，选择一个注释，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="48878-131">In the dialog box that appears, enter a comment, and then select **OK**.</span></span>
9. <span data-ttu-id="48878-132">要停用工作流或激活先前创建的工作流，请转到 **资产租赁 \> 设置 \> 租赁工作流**。</span><span class="sxs-lookup"><span data-stu-id="48878-132">To inactivate a workflow, or to activate a workflow that was previously created, go to **Asset leasing \> Setup \> Lease workflow**.</span></span> <span data-ttu-id="48878-133">然后，在 **租赁工作流** 页面上，选择 **工作流 \> 版本**。</span><span class="sxs-lookup"><span data-stu-id="48878-133">Then, on the **Lease workflow** page, select **Workflow \> Versions**.</span></span> <span data-ttu-id="48878-134">要使当前工作流处于非活动状态，请在“租赁版本”对话框中选择活动的租赁，然后选择 **停用**。</span><span class="sxs-lookup"><span data-stu-id="48878-134">To make a current workflow inactive, select the active lease in the lease version dialog box, and then select **Make inactive**.</span></span> <span data-ttu-id="48878-135">要激活现有工作流，请选择工作流，然后选择 **激活**。</span><span class="sxs-lookup"><span data-stu-id="48878-135">To make an existing workflow active, select the workflow, and then select **Make active**.</span></span>
