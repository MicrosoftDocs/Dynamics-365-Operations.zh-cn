---
title: 采购工作流
description: 某些组织要求采购申请和采购订单由输入交易记录的人之外的用户进行审核。 若要设置审核流程，您可以创建一个工作流。
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ceab555bf278ced13d8360956f6db65ba275f8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813446"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="a5579-104">采购工作流</span><span class="sxs-lookup"><span data-stu-id="a5579-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5579-105">某些组织要求采购申请和采购订单由输入交易记录的人之外的用户进行审核。</span><span class="sxs-lookup"><span data-stu-id="a5579-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="a5579-106">若要设置审核流程，您可以创建一个工作流。</span><span class="sxs-lookup"><span data-stu-id="a5579-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="a5579-107">“工作流”代表业务流程。</span><span class="sxs-lookup"><span data-stu-id="a5579-107">A workflow represents a business process.</span></span> <span data-ttu-id="a5579-108">它定义单据如何在系统中流动并指示必须由谁完成任务或审核单据。</span><span class="sxs-lookup"><span data-stu-id="a5579-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="a5579-109">在组织内使用工作流系统具有若干优点：</span><span class="sxs-lookup"><span data-stu-id="a5579-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="a5579-110">**一致的流程**— 您可定义特定单据（如采购申请和支出报表）的审核流程。</span><span class="sxs-lookup"><span data-stu-id="a5579-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="a5579-111">使用工作流系统有助于确保以一致且有效的方式来处理和审核单据。</span><span class="sxs-lookup"><span data-stu-id="a5579-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="a5579-112">**流程可见性**— 您可跟踪特定工作流实例的状态、历史记录和绩效指标。</span><span class="sxs-lookup"><span data-stu-id="a5579-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="a5579-113">这帮助您确定是否需要对该工作流做出更改，以提高效率。</span><span class="sxs-lookup"><span data-stu-id="a5579-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="a5579-114">**集中的工作列表**— 用户可以查看集中的工作列表，以便跨他们所参与的所有工作流查看分配给他们的工作流任务和审核。</span><span class="sxs-lookup"><span data-stu-id="a5579-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="a5579-115">这在“工作项”页上可用。</span><span class="sxs-lookup"><span data-stu-id="a5579-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="a5579-116">您可以创建的工作流类型</span><span class="sxs-lookup"><span data-stu-id="a5579-116">The types of workflows that you can create</span></span>
<span data-ttu-id="a5579-117">以下工作流类型可用于采购。</span><span class="sxs-lookup"><span data-stu-id="a5579-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a5579-118">**类型**</span><span class="sxs-lookup"><span data-stu-id="a5579-118">**Type**</span></span>                         | <span data-ttu-id="a5579-119">**使用此类型可以**</span><span class="sxs-lookup"><span data-stu-id="a5579-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="a5579-120">采购申请审核</span><span class="sxs-lookup"><span data-stu-id="a5579-120">Purchase requisition review</span></span>      | <span data-ttu-id="a5579-121">为采购申请创建审核和批准工作流。</span><span class="sxs-lookup"><span data-stu-id="a5579-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="a5579-122">采购申请行审查</span><span class="sxs-lookup"><span data-stu-id="a5579-122">Purchase requisition line review</span></span> | <span data-ttu-id="a5579-123">为采购申请行创建审核和批准工作流。</span><span class="sxs-lookup"><span data-stu-id="a5579-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="a5579-124">采购订单工作流</span><span class="sxs-lookup"><span data-stu-id="a5579-124">Purchase order workflow</span></span>          | <span data-ttu-id="a5579-125">针对采购订单创建检查和审核工作流。</span><span class="sxs-lookup"><span data-stu-id="a5579-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="a5579-126">采购订单行工作流</span><span class="sxs-lookup"><span data-stu-id="a5579-126">Purchase order line workflow</span></span>     | <span data-ttu-id="a5579-127">针对采购订单行创建检查和审核工作流。</span><span class="sxs-lookup"><span data-stu-id="a5579-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="a5579-128">供应商添加申请工作流</span><span class="sxs-lookup"><span data-stu-id="a5579-128">Vendor add application workflow</span></span>  | <span data-ttu-id="a5579-129">为通过供应商请求添加新供应商创建审核和批准工作流。</span><span class="sxs-lookup"><span data-stu-id="a5579-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="a5579-130">创建工作流</span><span class="sxs-lookup"><span data-stu-id="a5579-130">Creating a workflow</span></span>

<span data-ttu-id="a5579-131">若要创建工作流，请转到“采购”&gt;“设置”&gt;“采购”工作流，并通过选择您要创建的工作流类型创建新工作流。</span><span class="sxs-lookup"><span data-stu-id="a5579-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="a5579-132">在工作流画布中，您可以将工作流元素拖动到设计器并将元素链接到流。</span><span class="sxs-lookup"><span data-stu-id="a5579-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="a5579-133">应配置工作流元素。</span><span class="sxs-lookup"><span data-stu-id="a5579-133">The workflow elements should be configured.</span></span> <span data-ttu-id="a5579-134">对于审核和任务工作流元素，您可以配置哪个参与者应采取行动。</span><span class="sxs-lookup"><span data-stu-id="a5579-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="a5579-135">参与者类型</span><span class="sxs-lookup"><span data-stu-id="a5579-135">Types of participants</span></span>

<span data-ttu-id="a5579-136">您可以将审核步骤分配到以下的参与者组。</span><span class="sxs-lookup"><span data-stu-id="a5579-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="a5579-137">用户组</span><span class="sxs-lookup"><span data-stu-id="a5579-137">User group</span></span>    | <span data-ttu-id="a5579-138">描述</span><span class="sxs-lookup"><span data-stu-id="a5579-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="a5579-139">参与者</span><span class="sxs-lookup"><span data-stu-id="a5579-139">Participant</span></span>   | <span data-ttu-id="a5579-140">将审核步骤分配到组的成员或角色。</span><span class="sxs-lookup"><span data-stu-id="a5579-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="a5579-141">层次结构</span><span class="sxs-lookup"><span data-stu-id="a5579-141">Hierarchy</span></span>     | <span data-ttu-id="a5579-142">将审核步骤分配给特定组织层次结构中的用户。</span><span class="sxs-lookup"><span data-stu-id="a5579-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="a5579-143">工作流用户</span><span class="sxs-lookup"><span data-stu-id="a5579-143">Workflow user</span></span> | <span data-ttu-id="a5579-144">将审核步骤分配给此工作流的用户。</span><span class="sxs-lookup"><span data-stu-id="a5579-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="a5579-145">队列</span><span class="sxs-lookup"><span data-stu-id="a5579-145">Queue</span></span>         | <span data-ttu-id="a5579-146">将审核步骤分配给工作项队列。</span><span class="sxs-lookup"><span data-stu-id="a5579-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="a5579-147">用户</span><span class="sxs-lookup"><span data-stu-id="a5579-147">User</span></span>          | <span data-ttu-id="a5579-148">将审核步骤分配给特定用户。</span><span class="sxs-lookup"><span data-stu-id="a5579-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="a5579-149">其他资源</span><span class="sxs-lookup"><span data-stu-id="a5579-149">Additional resources</span></span>

- [<span data-ttu-id="a5579-150">定义采购申请的业务流程工作流</span><span class="sxs-lookup"><span data-stu-id="a5579-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

- [<span data-ttu-id="a5579-151">采购申请工作流</span><span class="sxs-lookup"><span data-stu-id="a5579-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="a5579-152">载入供应商</span><span class="sxs-lookup"><span data-stu-id="a5579-152">Onboard vendors</span></span>](vendor-onboarding.md)

