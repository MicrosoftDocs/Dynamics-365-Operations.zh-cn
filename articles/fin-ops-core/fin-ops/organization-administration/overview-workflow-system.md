---
title: 工作流系统概览
description: 此主题介绍工作流系统。
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd8fba1376dc5e3dbfea888ca5ff5fdeb608fc9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560693"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="ce328-103">工作流系统概览</span><span class="sxs-lookup"><span data-stu-id="ce328-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce328-104">此主题介绍工作流系统。</span><span class="sxs-lookup"><span data-stu-id="ce328-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="ce328-105">什么是工作流？</span><span class="sxs-lookup"><span data-stu-id="ce328-105">What is workflow?</span></span>

<span data-ttu-id="ce328-106">术语 *工作流* 可以通过两种方式定义：作为系统和作为业务流程。</span><span class="sxs-lookup"><span data-stu-id="ce328-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="ce328-107">工作流是一个系统</span><span class="sxs-lookup"><span data-stu-id="ce328-107">Workflow is a system</span></span>

<span data-ttu-id="ce328-108">工作流是在应用程序对象服务器 (AOS) 上运行的系统。</span><span class="sxs-lookup"><span data-stu-id="ce328-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="ce328-109">使用工作流系统提供的功能，您可以创建单独的工作流或业务流程。</span><span class="sxs-lookup"><span data-stu-id="ce328-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="ce328-110">工作流是一个业务流程</span><span class="sxs-lookup"><span data-stu-id="ce328-110">Workflow is a business process</span></span>

<span data-ttu-id="ce328-111">“工作流”代表业务流程。</span><span class="sxs-lookup"><span data-stu-id="ce328-111">A workflow represents a business process.</span></span> <span data-ttu-id="ce328-112">它通过显示谁必须完成任务、制定决策或批准文档定义单据如何在系统中流动或移动。</span><span class="sxs-lookup"><span data-stu-id="ce328-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="ce328-113">例如，下图显示支出报表的工作流。</span><span class="sxs-lookup"><span data-stu-id="ce328-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![具有分配给用户的元素的工作流](./media/workflow_user.gif)

<span data-ttu-id="ce328-115">为了更好地理解这一工作流，假定 Sam 提交 7,000 美元的支出报表。</span><span class="sxs-lookup"><span data-stu-id="ce328-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="ce328-116">在此场景中，Ivan 必须审核 Sam 传送给他的收据。</span><span class="sxs-lookup"><span data-stu-id="ce328-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="ce328-117">然后，晓辉和素心必须对该支出报表进行审核。</span><span class="sxs-lookup"><span data-stu-id="ce328-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="ce328-118">现在，假定 Sam 提交了一份 11,000 美元的支出报表。</span><span class="sxs-lookup"><span data-stu-id="ce328-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="ce328-119">在这种情况下，Ivan 必须复核相关收据，并且 Frank、Sue 和 Ann 必须审核该支出报表。</span><span class="sxs-lookup"><span data-stu-id="ce328-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="ce328-120">使用工作流系统的优点</span><span class="sxs-lookup"><span data-stu-id="ce328-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="ce328-121">在组织内使用工作流系统具有若干优点：</span><span class="sxs-lookup"><span data-stu-id="ce328-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="ce328-122">**一致的流程** - 您可定义处理特定文档（如采购申请和支出报表）的方法。</span><span class="sxs-lookup"><span data-stu-id="ce328-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="ce328-123">通过使用工作流系统，您可以确保以一致且有效的方式来处理和审核文档。</span><span class="sxs-lookup"><span data-stu-id="ce328-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="ce328-124">**流程可见性** - 您可跟踪工作流实例的状态、历史记录和绩效指标。</span><span class="sxs-lookup"><span data-stu-id="ce328-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="ce328-125">这帮助您确定是否需要对该工作流做出更改，以提高效率。</span><span class="sxs-lookup"><span data-stu-id="ce328-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="ce328-126">**工作列表集中化** - 用户可以查看集中化的工作列表，该列表显示分配给他们的工作流任务和审核任务。</span><span class="sxs-lookup"><span data-stu-id="ce328-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="ce328-127">工作流内容</span><span class="sxs-lookup"><span data-stu-id="ce328-127">Workflow content</span></span>

+ [<span data-ttu-id="ce328-128">工作流系统体系结构</span><span class="sxs-lookup"><span data-stu-id="ce328-128">Workflow system architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="ce328-129">工作流元素</span><span class="sxs-lookup"><span data-stu-id="ce328-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="ce328-130">工作流审核流程中的操作</span><span class="sxs-lookup"><span data-stu-id="ce328-130">Actions in workflow approval processes</span></span>](workflow-actions.md)
+ [<span data-ttu-id="ce328-131">创建工作流概览</span><span class="sxs-lookup"><span data-stu-id="ce328-131">Create workflows overview</span></span>](create-workflow.md)
+ [<span data-ttu-id="ce328-132">配置工作流属性</span><span class="sxs-lookup"><span data-stu-id="ce328-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="ce328-133">配置工作流中的手动任务</span><span class="sxs-lookup"><span data-stu-id="ce328-133">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="ce328-134">配置工作流中的自动化任务</span><span class="sxs-lookup"><span data-stu-id="ce328-134">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="ce328-135">配置工作流中的审核流程</span><span class="sxs-lookup"><span data-stu-id="ce328-135">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="ce328-136">配置工作流中的审核步骤</span><span class="sxs-lookup"><span data-stu-id="ce328-136">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="ce328-137">配置工作流中的手动决策</span><span class="sxs-lookup"><span data-stu-id="ce328-137">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="ce328-138">配置工作流中的有条件决策</span><span class="sxs-lookup"><span data-stu-id="ce328-138">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="ce328-139">配置工作流中的并行活动</span><span class="sxs-lookup"><span data-stu-id="ce328-139">Configure parallel activities in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="ce328-140">配置工作流中的并行分支</span><span class="sxs-lookup"><span data-stu-id="ce328-140">Configure parallel branches in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="ce328-141">配置行项工作流</span><span class="sxs-lookup"><span data-stu-id="ce328-141">Configure line-item workflows</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="ce328-142">工作流常见问题</span><span class="sxs-lookup"><span data-stu-id="ce328-142">Workflow FAQ</span></span>](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]