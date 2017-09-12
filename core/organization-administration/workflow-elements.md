---
title: "工作流元素"
description: "本文介绍构成工作流的不同元素。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5620a91ff9f300bed782170307a295ab79fc5b2e
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="workflow-elements"></a><span data-ttu-id="30a1b-103">工作流元素</span><span class="sxs-lookup"><span data-stu-id="30a1b-103">Workflow elements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="30a1b-104">本文介绍构成工作流的不同元素。</span><span class="sxs-lookup"><span data-stu-id="30a1b-104">This article describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="30a1b-105">工作流由“元素”构成。</span><span class="sxs-lookup"><span data-stu-id="30a1b-105">A workflow consists of elements.</span></span> <span data-ttu-id="30a1b-106">以下各节描述各个元素类型。</span><span class="sxs-lookup"><span data-stu-id="30a1b-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="30a1b-107">任务</span><span class="sxs-lookup"><span data-stu-id="30a1b-107">Tasks</span></span>
<span data-ttu-id="30a1b-108">*任务*是必须执行的工作单元。</span><span class="sxs-lookup"><span data-stu-id="30a1b-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="30a1b-109">有两种类型的任务可添加到工作流：手动任务或自动化任务。</span><span class="sxs-lookup"><span data-stu-id="30a1b-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="30a1b-110">手动任务</span><span class="sxs-lookup"><span data-stu-id="30a1b-110">Manual task</span></span>

<span data-ttu-id="30a1b-111">*手动任务*是必须由用户执行的工作单元。</span><span class="sxs-lookup"><span data-stu-id="30a1b-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="30a1b-112">例如，支出报表工作流中的手动任务可能要求所分配用户完成以下操作：</span><span class="sxs-lookup"><span data-stu-id="30a1b-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

-   <span data-ttu-id="30a1b-113">查看随支出报表一起提交的收据。</span><span class="sxs-lookup"><span data-stu-id="30a1b-113">Review the receipts that are submitted together with an expense report.</span></span>
-   <span data-ttu-id="30a1b-114">致电员工的经理。</span><span class="sxs-lookup"><span data-stu-id="30a1b-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="30a1b-115">自动化任务</span><span class="sxs-lookup"><span data-stu-id="30a1b-115">Automated task</span></span>

<span data-ttu-id="30a1b-116">*自动化任务*是必须由系统执行的工作单元。</span><span class="sxs-lookup"><span data-stu-id="30a1b-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="30a1b-117">不要求人工交互。</span><span class="sxs-lookup"><span data-stu-id="30a1b-117">No human interaction is required.</span></span> <span data-ttu-id="30a1b-118">例如，销售订单工作流中的自动化任务可能要求系统完成以下操作：</span><span class="sxs-lookup"><span data-stu-id="30a1b-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

-   <span data-ttu-id="30a1b-119">执行信用检查。</span><span class="sxs-lookup"><span data-stu-id="30a1b-119">Perform a credit check.</span></span>
-   <span data-ttu-id="30a1b-120">如果记录不存在，为客户创建客户记录。</span><span class="sxs-lookup"><span data-stu-id="30a1b-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="30a1b-121">审核流程</span><span class="sxs-lookup"><span data-stu-id="30a1b-121">Approval processes</span></span>
<span data-ttu-id="30a1b-122">“*审核流程*”是由各个独立步骤构成的流程。</span><span class="sxs-lookup"><span data-stu-id="30a1b-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="30a1b-123">在每个审核步骤，用户可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="30a1b-123">At each approval step, the user can perform the following actions:</span></span>

-   <span data-ttu-id="30a1b-124">批准单据。</span><span class="sxs-lookup"><span data-stu-id="30a1b-124">Approve the document.</span></span>
-   <span data-ttu-id="30a1b-125">拒绝单据。</span><span class="sxs-lookup"><span data-stu-id="30a1b-125">Reject the document.</span></span>
-   <span data-ttu-id="30a1b-126">请求对单据进行更改。</span><span class="sxs-lookup"><span data-stu-id="30a1b-126">Request a change to the document.</span></span>
-   <span data-ttu-id="30a1b-127">将单据分配给其他用户进行审核。</span><span class="sxs-lookup"><span data-stu-id="30a1b-127">Assign the document to another user for approval.</span></span>

## <a name="lineitem-workflow-elements"></a><span data-ttu-id="30a1b-128">行项工作流元素</span><span class="sxs-lookup"><span data-stu-id="30a1b-128">Lineitem workflow elements</span></span>
<span data-ttu-id="30a1b-129">可以创建工作流来处理文档或文档上的行项。</span><span class="sxs-lookup"><span data-stu-id="30a1b-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="30a1b-130">例如，您为工时单创建了审核工作流。</span><span class="sxs-lookup"><span data-stu-id="30a1b-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="30a1b-131">（我们将把此工作流称为*单据工作流*。）您可以向该单据工作流添加*行项工作流*元素。</span><span class="sxs-lookup"><span data-stu-id="30a1b-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="30a1b-132">在运行行项元素时，提交文档上的每个行项进行处理。</span><span class="sxs-lookup"><span data-stu-id="30a1b-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="30a1b-133">您可能想要由同一行项工作流来处理所有行项，或者您可能想要由不同的行项工作流来处理各行项。</span><span class="sxs-lookup"><span data-stu-id="30a1b-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="30a1b-134">假定员工提交了类似于下图的时间表。</span><span class="sxs-lookup"><span data-stu-id="30a1b-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span> <span data-ttu-id="30a1b-135">![具有行项的工作流](./media/workflow_lineitemworkflow.gif)在这种情况下，您可能要创建以下行项工作流：</span><span class="sxs-lookup"><span data-stu-id="30a1b-135">![Workflow with line items](./media/workflow_lineitemworkflow.gif) In this scenario, you might want to create the following line-item workflows:</span></span>

-   <span data-ttu-id="30a1b-136">**行项工作流 1** – 此工作流用于处理项目 ID 是 1111 的行项。</span><span class="sxs-lookup"><span data-stu-id="30a1b-136">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
-   <span data-ttu-id="30a1b-137">**行项工作流 2** – 此工作流用于处理项目 ID 是 2222 的行项。</span><span class="sxs-lookup"><span data-stu-id="30a1b-137">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
-   <span data-ttu-id="30a1b-138">**行项工作流 3** – 此工作流用于处理项目 ID 是 3333 的行项。</span><span class="sxs-lookup"><span data-stu-id="30a1b-138">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flowcontrol-elements"></a><span data-ttu-id="30a1b-139">流量控制元素</span><span class="sxs-lookup"><span data-stu-id="30a1b-139">Flowcontrol elements</span></span>
<span data-ttu-id="30a1b-140">以下元素可让您设计具有同时运行的备选分支或分支的工作流。</span><span class="sxs-lookup"><span data-stu-id="30a1b-140">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="30a1b-141">手动决策</span><span class="sxs-lookup"><span data-stu-id="30a1b-141">Manual decision</span></span>

<span data-ttu-id="30a1b-142">*手动决策*是工作流划分为两个分支处的点。</span><span class="sxs-lookup"><span data-stu-id="30a1b-142">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="30a1b-143">用户必须制定决策，并且此决策确定哪个分支用于处理提交的单据。</span><span class="sxs-lookup"><span data-stu-id="30a1b-143">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="30a1b-144">有条件决策</span><span class="sxs-lookup"><span data-stu-id="30a1b-144">Conditional decision</span></span>

<span data-ttu-id="30a1b-145">*有条件决策*还是工作流划分为两个分支处的点。</span><span class="sxs-lookup"><span data-stu-id="30a1b-145">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="30a1b-146">但是，系统将决定哪一个分支用于处理提交的单据。</span><span class="sxs-lookup"><span data-stu-id="30a1b-146">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="30a1b-147">要进行此决定，系统对该单据进行评估以确定是否符合指定的条件。</span><span class="sxs-lookup"><span data-stu-id="30a1b-147">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="30a1b-148">并行活动</span><span class="sxs-lookup"><span data-stu-id="30a1b-148">Parallel activity</span></span>

<span data-ttu-id="30a1b-149">*并行活动*是指包含两个或更多同时运行的工作流分支的工作流元素。</span><span class="sxs-lookup"><span data-stu-id="30a1b-149">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="30a1b-150">子工作流</span><span class="sxs-lookup"><span data-stu-id="30a1b-150">Subworkflow</span></span>

<span data-ttu-id="30a1b-151">*子工作流*是在其他工作流的上下文中运行的工作流。</span><span class="sxs-lookup"><span data-stu-id="30a1b-151">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>




