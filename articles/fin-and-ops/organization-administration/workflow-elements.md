---
title: "工作流元素"
description: "本主题介绍构成工作流的不同元素。"
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: abd2782ebe98fd25fc491b4b3cbcd4a6dd5c4cbd
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="workflow-elements"></a><span data-ttu-id="2f329-103">工作流元素</span><span class="sxs-lookup"><span data-stu-id="2f329-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f329-104">本主题介绍构成工作流的不同元素。</span><span class="sxs-lookup"><span data-stu-id="2f329-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="2f329-105">工作流由“元素”构成。</span><span class="sxs-lookup"><span data-stu-id="2f329-105">A workflow consists of elements.</span></span> <span data-ttu-id="2f329-106">以下各节描述各个元素类型。</span><span class="sxs-lookup"><span data-stu-id="2f329-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="2f329-107">任务</span><span class="sxs-lookup"><span data-stu-id="2f329-107">Tasks</span></span>
<span data-ttu-id="2f329-108">*任务*是必须执行的工作单元。</span><span class="sxs-lookup"><span data-stu-id="2f329-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="2f329-109">有两种类型的任务可添加到工作流：手动任务或自动化任务。</span><span class="sxs-lookup"><span data-stu-id="2f329-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="2f329-110">手动任务</span><span class="sxs-lookup"><span data-stu-id="2f329-110">Manual task</span></span>

<span data-ttu-id="2f329-111">*手动任务*是必须由用户执行的工作单元。</span><span class="sxs-lookup"><span data-stu-id="2f329-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="2f329-112">例如，支出报表工作流中的手动任务可能要求所分配用户完成以下操作：</span><span class="sxs-lookup"><span data-stu-id="2f329-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

-   <span data-ttu-id="2f329-113">查看随支出报表一起提交的收据。</span><span class="sxs-lookup"><span data-stu-id="2f329-113">Review the receipts that are submitted together with an expense report.</span></span>
-   <span data-ttu-id="2f329-114">致电员工的经理。</span><span class="sxs-lookup"><span data-stu-id="2f329-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="2f329-115">自动化任务</span><span class="sxs-lookup"><span data-stu-id="2f329-115">Automated task</span></span>

<span data-ttu-id="2f329-116">*自动化任务*是必须由系统执行的工作单元。</span><span class="sxs-lookup"><span data-stu-id="2f329-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="2f329-117">不要求人工交互。</span><span class="sxs-lookup"><span data-stu-id="2f329-117">No human interaction is required.</span></span> <span data-ttu-id="2f329-118">例如，销售订单工作流中的自动化任务可能要求系统完成以下操作：</span><span class="sxs-lookup"><span data-stu-id="2f329-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

-   <span data-ttu-id="2f329-119">执行信用检查。</span><span class="sxs-lookup"><span data-stu-id="2f329-119">Perform a credit check.</span></span>
-   <span data-ttu-id="2f329-120">如果记录不存在，为客户创建客户记录。</span><span class="sxs-lookup"><span data-stu-id="2f329-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="2f329-121">审核流程</span><span class="sxs-lookup"><span data-stu-id="2f329-121">Approval processes</span></span>
<span data-ttu-id="2f329-122">“*审核流程*”是由各个独立步骤构成的流程。</span><span class="sxs-lookup"><span data-stu-id="2f329-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="2f329-123">在每个审核步骤，用户可以执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="2f329-123">At each approval step, the user can perform the following actions:</span></span>

-   <span data-ttu-id="2f329-124">批准单据。</span><span class="sxs-lookup"><span data-stu-id="2f329-124">Approve the document.</span></span>
-   <span data-ttu-id="2f329-125">拒绝单据。</span><span class="sxs-lookup"><span data-stu-id="2f329-125">Reject the document.</span></span>
-   <span data-ttu-id="2f329-126">请求对单据进行更改。</span><span class="sxs-lookup"><span data-stu-id="2f329-126">Request a change to the document.</span></span>
-   <span data-ttu-id="2f329-127">将单据分配给其他用户进行审核。</span><span class="sxs-lookup"><span data-stu-id="2f329-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="2f329-128">行项工作流元素</span><span class="sxs-lookup"><span data-stu-id="2f329-128">Line-item workflow elements</span></span>
<span data-ttu-id="2f329-129">可以创建工作流来处理文档或文档上的行项。</span><span class="sxs-lookup"><span data-stu-id="2f329-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="2f329-130">例如，您为工时单创建了审核工作流。</span><span class="sxs-lookup"><span data-stu-id="2f329-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="2f329-131">（我们将把此工作流称为*单据工作流*。）您可以向该单据工作流添加*行项工作流*元素。</span><span class="sxs-lookup"><span data-stu-id="2f329-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="2f329-132">在运行行项元素时，提交文档上的每个行项进行处理。</span><span class="sxs-lookup"><span data-stu-id="2f329-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="2f329-133">您可能想要由同一行项工作流来处理所有行项，或者您可能想要由不同的行项工作流来处理各行项。</span><span class="sxs-lookup"><span data-stu-id="2f329-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="2f329-134">假定员工提交了类似于下图的时间表。</span><span class="sxs-lookup"><span data-stu-id="2f329-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![具有行项的工作流](./media/workflow_lineitemworkflow.gif) 

<span data-ttu-id="2f329-136">在这种情况下，您可能要创建以下行项工作流：</span><span class="sxs-lookup"><span data-stu-id="2f329-136">In this scenario, you might want to create the following line-item workflows:</span></span>

-   <span data-ttu-id="2f329-137">**行项工作流 1** – 此工作流用于处理项目 ID 是 1111 的行项。</span><span class="sxs-lookup"><span data-stu-id="2f329-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
-   <span data-ttu-id="2f329-138">**行项工作流 2** – 此工作流用于处理项目 ID 是 2222 的行项。</span><span class="sxs-lookup"><span data-stu-id="2f329-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
-   <span data-ttu-id="2f329-139">**行项工作流 3** – 此工作流用于处理项目 ID 是 3333 的行项。</span><span class="sxs-lookup"><span data-stu-id="2f329-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="2f329-140">流量控制元素</span><span class="sxs-lookup"><span data-stu-id="2f329-140">Flow-control elements</span></span>
<span data-ttu-id="2f329-141">以下元素可让您设计具有同时运行的备选分支或分支的工作流。</span><span class="sxs-lookup"><span data-stu-id="2f329-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="2f329-142">手动决策</span><span class="sxs-lookup"><span data-stu-id="2f329-142">Manual decision</span></span>

<span data-ttu-id="2f329-143">*手动决策*是工作流划分为两个分支处的点。</span><span class="sxs-lookup"><span data-stu-id="2f329-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="2f329-144">用户必须制定决策，并且此决策确定哪个分支用于处理提交的单据。</span><span class="sxs-lookup"><span data-stu-id="2f329-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="2f329-145">有条件决策</span><span class="sxs-lookup"><span data-stu-id="2f329-145">Conditional decision</span></span>

<span data-ttu-id="2f329-146">*有条件决策*还是工作流划分为两个分支处的点。</span><span class="sxs-lookup"><span data-stu-id="2f329-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="2f329-147">但是，系统将决定哪一个分支用于处理提交的单据。</span><span class="sxs-lookup"><span data-stu-id="2f329-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="2f329-148">要进行此决定，系统对该单据进行评估以确定是否符合指定的条件。</span><span class="sxs-lookup"><span data-stu-id="2f329-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="2f329-149">并行活动</span><span class="sxs-lookup"><span data-stu-id="2f329-149">Parallel activity</span></span>

<span data-ttu-id="2f329-150">*并行活动*是指包含两个或更多同时运行的工作流分支的工作流元素。</span><span class="sxs-lookup"><span data-stu-id="2f329-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="2f329-151">子工作流</span><span class="sxs-lookup"><span data-stu-id="2f329-151">Subworkflow</span></span>

<span data-ttu-id="2f329-152">*子工作流*是在其他工作流的上下文中运行的工作流。</span><span class="sxs-lookup"><span data-stu-id="2f329-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>




