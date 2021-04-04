---
title: 工作流审核流程中的操作
description: 本文说明每个工作流审核流程的参与者可以采取的操作。
author: ChrisGarty
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e6331746d2634a3686b0a7368d060d94567c4ff
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567948"
---
# <a name="actions-in-workflow-approval-processes"></a><span data-ttu-id="ffaba-103">工作流审核流程中的操作</span><span class="sxs-lookup"><span data-stu-id="ffaba-103">Actions in workflow approval processes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffaba-104">本文说明每个工作流审核流程的参与者可以采取的操作。</span><span class="sxs-lookup"><span data-stu-id="ffaba-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="ffaba-105">工作流可能涉及若干组人员：发起方、任务受托人、决策者和审核人。</span><span class="sxs-lookup"><span data-stu-id="ffaba-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="ffaba-106">例如，在以下支出报表工作流中，Sam 是发起方，队列的成员是任务受托人，John 是决策者，Frank、Sue 和 Ann 是审核人。</span><span class="sxs-lookup"><span data-stu-id="ffaba-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>

<span data-ttu-id="ffaba-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="ffaba-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span>

<span data-ttu-id="ffaba-108">以下部分说明各个组可以执行的工作流操作。</span><span class="sxs-lookup"><span data-stu-id="ffaba-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="ffaba-109">发起方可以执行的操作</span><span class="sxs-lookup"><span data-stu-id="ffaba-109">Actions that an originator can perform</span></span>

<span data-ttu-id="ffaba-110">发起方通过提交文档进行审查来启动工作流实例。</span><span class="sxs-lookup"><span data-stu-id="ffaba-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="ffaba-111">例如，Sam 必须在 **支出报表** 页上单击 **提交** 按钮，才能提交其支出报表。</span><span class="sxs-lookup"><span data-stu-id="ffaba-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="ffaba-112">任务受托人可执行的操作</span><span class="sxs-lookup"><span data-stu-id="ffaba-112">Actions that a task assignee can perform</span></span>

<span data-ttu-id="ffaba-113">一个任务可分配给多个人员或到由若干人员监控的工作项队列。</span><span class="sxs-lookup"><span data-stu-id="ffaba-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="ffaba-114">不过，只能由一个人来完成任务。</span><span class="sxs-lookup"><span data-stu-id="ffaba-114">However, only one person can complete a task.</span></span> <span data-ttu-id="ffaba-115">例如，Sam 提交了一份支出报表并将其收据发送到其组织的支出报表部门进行审查。</span><span class="sxs-lookup"><span data-stu-id="ffaba-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span>

<span data-ttu-id="ffaba-116">Adventure Works 支出报表部门的成员监控该队列。</span><span class="sxs-lookup"><span data-stu-id="ffaba-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="ffaba-117">该部门的成员 Julie 接受了审查 Sam 的支出报表和收据的任务。</span><span class="sxs-lookup"><span data-stu-id="ffaba-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ffaba-118">她现在可以执行以下操作之一：完成、拒绝、委托、请求更改、重新分配或下达。</span><span class="sxs-lookup"><span data-stu-id="ffaba-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span>

> [!NOTE]
> <span data-ttu-id="ffaba-119">可用操作将随软件开发人员设计任务的方式而变化。</span><span class="sxs-lookup"><span data-stu-id="ffaba-119">The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="ffaba-120">完成</span><span class="sxs-lookup"><span data-stu-id="ffaba-120">Complete</span></span>

<span data-ttu-id="ffaba-121">用户完成某项任务后，提请处理的文档分配给工作流中的下一用户（如果有）。</span><span class="sxs-lookup"><span data-stu-id="ffaba-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="ffaba-122">如果不需要进一步处理，该工作流程即告终止。</span><span class="sxs-lookup"><span data-stu-id="ffaba-122">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="ffaba-123">例如，Adventure Works 支出报表部门的成员 Julie 接受审查 Sam 的支出报表和收据的任务。</span><span class="sxs-lookup"><span data-stu-id="ffaba-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ffaba-124">在 Julie 完成自己的审核后，该单据将分配给 John。</span><span class="sxs-lookup"><span data-stu-id="ffaba-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="ffaba-125">拒绝</span><span class="sxs-lookup"><span data-stu-id="ffaba-125">Reject</span></span>

<span data-ttu-id="ffaba-126">如果用户拒绝了文档，该工作流程即告终止。</span><span class="sxs-lookup"><span data-stu-id="ffaba-126">When a user rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="ffaba-127">例如，Adventure Works 支出报表部门的成员 Julie 接受审查 Sam 的支出报表和收据的任务。</span><span class="sxs-lookup"><span data-stu-id="ffaba-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ffaba-128">如果 Julie 拒绝了该支出报表，该工作流程即告终止。</span><span class="sxs-lookup"><span data-stu-id="ffaba-128">If Julie rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="ffaba-129">然后 Sam 可以重新提交该支出报表。</span><span class="sxs-lookup"><span data-stu-id="ffaba-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="ffaba-130">他可以首先进行更改，或者可以重新提交原始版本。</span><span class="sxs-lookup"><span data-stu-id="ffaba-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="ffaba-131">如果 Sam 重新提交支出报表，则该工作流程将从手动审查任务开始。</span><span class="sxs-lookup"><span data-stu-id="ffaba-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="ffaba-132">委托</span><span class="sxs-lookup"><span data-stu-id="ffaba-132">Delegate</span></span>

<span data-ttu-id="ffaba-133">如果用户委托某项任务，该任务将分配给其他用户。</span><span class="sxs-lookup"><span data-stu-id="ffaba-133">When a user delegates a task, the task is assigned to another user.</span></span>

<span data-ttu-id="ffaba-134">例如，Adventure Works 支出报表部门的成员 Julie 接受审查 Sam 的支出报表和收据的任务。</span><span class="sxs-lookup"><span data-stu-id="ffaba-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ffaba-135">Julie 将此任务分配给她的助手 Tim。</span><span class="sxs-lookup"><span data-stu-id="ffaba-135">Julie delegates this task to Tim, who is her assistant.</span></span>

<span data-ttu-id="ffaba-136">然后，Tim 代表 Julie 采取操作。</span><span class="sxs-lookup"><span data-stu-id="ffaba-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="ffaba-137">因此，在 Tim 完成审查后，支出报表分配给 John，就像 Julie 完成了任务一样。</span><span class="sxs-lookup"><span data-stu-id="ffaba-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="ffaba-138">请求更改</span><span class="sxs-lookup"><span data-stu-id="ffaba-138">Request change</span></span>

<span data-ttu-id="ffaba-139">如果用户请求对提交的单据进行更改，该单据将发还发起方。</span><span class="sxs-lookup"><span data-stu-id="ffaba-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span>

<span data-ttu-id="ffaba-140">例如，Adventure Works 支出报表部门的成员 Julie 接受审查 Sam 的支出报表和收据的任务。</span><span class="sxs-lookup"><span data-stu-id="ffaba-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ffaba-141">Julie 注意到支出报表上的一些错误并请求进行更改。</span><span class="sxs-lookup"><span data-stu-id="ffaba-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="ffaba-142">该支出报表发还给 Sam。</span><span class="sxs-lookup"><span data-stu-id="ffaba-142">The expense report is sent back to Sam.</span></span>

<span data-ttu-id="ffaba-143">Sam 可以重新提交该支出报表。</span><span class="sxs-lookup"><span data-stu-id="ffaba-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="ffaba-144">他可以首先进行所请求的更改，或者可以重新提交原始版本。</span><span class="sxs-lookup"><span data-stu-id="ffaba-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="ffaba-145">如果 Sam 重新提交支出报表，则工作项队列的成员必须重新审查支出报告和收据。</span><span class="sxs-lookup"><span data-stu-id="ffaba-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="ffaba-146">重新分配</span><span class="sxs-lookup"><span data-stu-id="ffaba-146">Reassign</span></span>

<span data-ttu-id="ffaba-147">工作项队列的成员可以将该队列中的文档分配到另一个队列。</span><span class="sxs-lookup"><span data-stu-id="ffaba-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span>

<span data-ttu-id="ffaba-148">例如，该 Adventure Works 支出报表部门的成员 Julie 正在监控该队列。</span><span class="sxs-lookup"><span data-stu-id="ffaba-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="ffaba-149">为了帮助平衡工作量，她可以将支出报表和其中包含的收据重新分配到另一个队列。</span><span class="sxs-lookup"><span data-stu-id="ffaba-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="ffaba-150">发布</span><span class="sxs-lookup"><span data-stu-id="ffaba-150">Release</span></span>

<span data-ttu-id="ffaba-151">偶尔，工作项队列的成员可以接受任务，不过，随后确定他或她无法完成任务。</span><span class="sxs-lookup"><span data-stu-id="ffaba-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="ffaba-152">在这种情况下，接受任务的人员可以将文档释放后工作项队列。</span><span class="sxs-lookup"><span data-stu-id="ffaba-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span>

<span data-ttu-id="ffaba-153">例如，Adventure Works 支出报表部门的成员 Julie 接受审查 Sam 的支出报表和收据的任务。</span><span class="sxs-lookup"><span data-stu-id="ffaba-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="ffaba-154">如果 Julie 确定她不能完成此任务，则她可以下达文档。</span><span class="sxs-lookup"><span data-stu-id="ffaba-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="ffaba-155">支出报表返回到该队列，以便 Adventure Works 支出报表部门的其他成员可以完成任务。</span><span class="sxs-lookup"><span data-stu-id="ffaba-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="ffaba-156">决策者可以执行的操作</span><span class="sxs-lookup"><span data-stu-id="ffaba-156">Actions that a decision maker can perform</span></span>

<span data-ttu-id="ffaba-157">通常，文档分配给决策者，因为有必须由决策者回答的问题。</span><span class="sxs-lookup"><span data-stu-id="ffaba-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="ffaba-158">该问题的答案通常是 **是** 或 **否** 或者是 **True** 或 **False**。</span><span class="sxs-lookup"><span data-stu-id="ffaba-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="ffaba-159">如果决策者不选择这些选项之一，他或她可以委托决策。</span><span class="sxs-lookup"><span data-stu-id="ffaba-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="ffaba-160">\[选择 1\] 或\[选择 2\]</span><span class="sxs-lookup"><span data-stu-id="ffaba-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="ffaba-161">决策者必须回答与文档相关的问题。</span><span class="sxs-lookup"><span data-stu-id="ffaba-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="ffaba-162">该问题的答案通常是 **是** 或 **否** 或者是 **True** 或 **False**。</span><span class="sxs-lookup"><span data-stu-id="ffaba-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="ffaba-163">决策者选择的回答确定使用哪个分支处理文档。</span><span class="sxs-lookup"><span data-stu-id="ffaba-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span>

<span data-ttu-id="ffaba-164">例如，Sam 的支出报表分配给 John。</span><span class="sxs-lookup"><span data-stu-id="ffaba-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="ffaba-165">John 必须确定文档中的信息是否要求致电 Sam 的经理。</span><span class="sxs-lookup"><span data-stu-id="ffaba-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="ffaba-166">如果 John 确定需要呼叫，则支出报表分配给 Aretha，然后 Aretha 必须致电 Sam 的经理。</span><span class="sxs-lookup"><span data-stu-id="ffaba-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="ffaba-167">如果 John 决定不需要通话，则支出报表分配给 Frank 进行审核。</span><span class="sxs-lookup"><span data-stu-id="ffaba-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="ffaba-168">委托</span><span class="sxs-lookup"><span data-stu-id="ffaba-168">Delegate</span></span>

<span data-ttu-id="ffaba-169">在决策者委托决策时，该文档将分配给必须制定决策的其他用户。</span><span class="sxs-lookup"><span data-stu-id="ffaba-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span>

<span data-ttu-id="ffaba-170">例如，Sam 的支出报表分配给 John。</span><span class="sxs-lookup"><span data-stu-id="ffaba-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="ffaba-171">John 将决策委托给他的助手 Maria。</span><span class="sxs-lookup"><span data-stu-id="ffaba-171">John delegates the decision to Maria, who is his assistant.</span></span>

<span data-ttu-id="ffaba-172">然后，Maria 代表 John 采取操作。</span><span class="sxs-lookup"><span data-stu-id="ffaba-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="ffaba-173">如果 Maria 确定需要致电 Sam 的经理，则支出报表分配给 Aretha，然后 Aretha 必须致电 Sam 的经理。</span><span class="sxs-lookup"><span data-stu-id="ffaba-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="ffaba-174">如果 Maria 决定不需要通话，则支出报表分配给 Frank 进行审核。</span><span class="sxs-lookup"><span data-stu-id="ffaba-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="ffaba-175">审核人可以执行的操作</span><span class="sxs-lookup"><span data-stu-id="ffaba-175">Actions that an approver can perform</span></span>

<span data-ttu-id="ffaba-176">将单据分配给审核人后，审核人必须采取以下操作之一：批准、拒绝、委托或请求更改。</span><span class="sxs-lookup"><span data-stu-id="ffaba-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="ffaba-177">审核</span><span class="sxs-lookup"><span data-stu-id="ffaba-177">Approve</span></span>

<span data-ttu-id="ffaba-178">审核人审核单据后，该单据将根据需要分配给工作流中的下一用户（如果有）。</span><span class="sxs-lookup"><span data-stu-id="ffaba-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="ffaba-179">如果不需要进一步处理，该工作流程即告终止。</span><span class="sxs-lookup"><span data-stu-id="ffaba-179">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="ffaba-180">例如，Sam 提交了一份 6,000 美元的支出报表，而且该文档分配给 Frank。</span><span class="sxs-lookup"><span data-stu-id="ffaba-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="ffaba-181">在 Frank a审核该单据后，该单据将分配给 Sue 进行审核。</span><span class="sxs-lookup"><span data-stu-id="ffaba-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="ffaba-182">一旦 Sue 批准了该支出报表，工作流程即告结束。</span><span class="sxs-lookup"><span data-stu-id="ffaba-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="ffaba-183">拒绝</span><span class="sxs-lookup"><span data-stu-id="ffaba-183">Reject</span></span>

<span data-ttu-id="ffaba-184">如果审核人拒绝了单据，该工作流程即告终止。</span><span class="sxs-lookup"><span data-stu-id="ffaba-184">When an approver rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="ffaba-185">例如，Sam 提交了一份 12,000 美元的支出报表，而且该文档分配给 Sue。</span><span class="sxs-lookup"><span data-stu-id="ffaba-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="ffaba-186">如果 Sue 拒绝了该支出报表，该工作流程即告终止。</span><span class="sxs-lookup"><span data-stu-id="ffaba-186">If Sue rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="ffaba-187">Sam 可以重新提交该支出报表。</span><span class="sxs-lookup"><span data-stu-id="ffaba-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="ffaba-188">他可以首先进行更改，或者可以重新提交支出报表的原始版本。</span><span class="sxs-lookup"><span data-stu-id="ffaba-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="ffaba-189">如果 Sam 重新提交了该支出报表，该工作流程将从审核流程开始运行。</span><span class="sxs-lookup"><span data-stu-id="ffaba-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="ffaba-190">委托</span><span class="sxs-lookup"><span data-stu-id="ffaba-190">Delegate</span></span>

<span data-ttu-id="ffaba-191">如果审核人委托处理单据，该单据将分配给其他用户进行审核。</span><span class="sxs-lookup"><span data-stu-id="ffaba-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span>

<span data-ttu-id="ffaba-192">例如，Sam 提交了一份 12,000 美元的支出报表，而且该文档分配给 Frank。</span><span class="sxs-lookup"><span data-stu-id="ffaba-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="ffaba-193">晓辉将该支出报表委托给安然。</span><span class="sxs-lookup"><span data-stu-id="ffaba-193">Frank delegates the expense report to Ann.</span></span>

<span data-ttu-id="ffaba-194">随后，Ann 代表 Frank 执行操作。</span><span class="sxs-lookup"><span data-stu-id="ffaba-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="ffaba-195">因此，在 Ann 审核该单据后，该单据将分配给 Sue 进行审核 - 就如同 Frank 审核的一样。</span><span class="sxs-lookup"><span data-stu-id="ffaba-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="ffaba-196">Sue 批准了文档后，该文档将发送给 Ann 进行审核。</span><span class="sxs-lookup"><span data-stu-id="ffaba-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="ffaba-197">请求更改</span><span class="sxs-lookup"><span data-stu-id="ffaba-197">Request change</span></span>

<span data-ttu-id="ffaba-198">如果审核人请求对单据进行更改，该单据将发还发起方。</span><span class="sxs-lookup"><span data-stu-id="ffaba-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span>

<span data-ttu-id="ffaba-199">例如，Sam 提交了一份 12,000 美元的支出报表，而且该文档分配给 Sue。</span><span class="sxs-lookup"><span data-stu-id="ffaba-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="ffaba-200">如果 Sue 请求更改，该支出报表将发还 Sam。</span><span class="sxs-lookup"><span data-stu-id="ffaba-200">If Sue requests a change, the expense report is sent back to Sam.</span></span>

<span data-ttu-id="ffaba-201">Sam 可以重新提交该支出报表。</span><span class="sxs-lookup"><span data-stu-id="ffaba-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="ffaba-202">他可以首先进行所请求的更改，或者可以重新提交支出报表的原始版本。</span><span class="sxs-lookup"><span data-stu-id="ffaba-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="ffaba-203">如果 Sam 重新提交了该支出报表，该报表将发送给 Frank 审核，因为 Frank 是审核流程中的第一位审核人。</span><span class="sxs-lookup"><span data-stu-id="ffaba-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]