---
title: "设置费用的工作流"
description: "您可以设置用于查看和审核出差和支出单据的工作流流程。"
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 19d725f15f00afce1a2ae4b336226f1dafa94b41
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="c158e-103">设置费用的工作流</span><span class="sxs-lookup"><span data-stu-id="c158e-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="c158e-104">您可以设置用于查看和审核出差和支出单据的工作流流程。</span><span class="sxs-lookup"><span data-stu-id="c158e-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="c158e-105">工作流可以定义的单据包括费用报表、出差申请和预付现金请求。</span><span class="sxs-lookup"><span data-stu-id="c158e-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="c158e-106">“工作流”代表业务流程。</span><span class="sxs-lookup"><span data-stu-id="c158e-106">A workflow represents a business process.</span></span> <span data-ttu-id="c158e-107">它定义单据如何在系统中流动并指示必须由谁完成任务或审核单据。</span><span class="sxs-lookup"><span data-stu-id="c158e-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="c158e-108">在组织内使用工作流系统具有若干优点：</span><span class="sxs-lookup"><span data-stu-id="c158e-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="c158e-109">“**一致的流程**”— 您可定义特定单据（如采购申请和支出报表）的审核流程。</span><span class="sxs-lookup"><span data-stu-id="c158e-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="c158e-110">使用工作流系统有助于确保以一致且有效的方式来处理和审核单据。</span><span class="sxs-lookup"><span data-stu-id="c158e-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="c158e-111">“流程可见性”— 您可跟踪特定工作流实例的状态、历史记录和绩效指标。</span><span class="sxs-lookup"><span data-stu-id="c158e-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="c158e-112">这帮助您确定是否需要对该工作流做出更改，以提高效率。</span><span class="sxs-lookup"><span data-stu-id="c158e-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="c158e-113">“集中的工作列表”— 用户可以查看集中化的工作列表，以查看分配给他们的工作流任务和审核任务。</span><span class="sxs-lookup"><span data-stu-id="c158e-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="c158e-114">**您可以创建工作流类型**</span><span class="sxs-lookup"><span data-stu-id="c158e-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="c158e-115">下表列出了您可以在**费用**过程中创建的工作流类型。</span><span class="sxs-lookup"><span data-stu-id="c158e-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="c158e-116">**类型**</span><span class="sxs-lookup"><span data-stu-id="c158e-116">**Type**</span></span>                           | <span data-ttu-id="c158e-117">**使用此类型可以**</span><span class="sxs-lookup"><span data-stu-id="c158e-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="c158e-118">**支出报表**</span><span class="sxs-lookup"><span data-stu-id="c158e-118">**Expense report**</span></span>                 | <span data-ttu-id="c158e-119">为支出报表创建审核工作流。</span><span class="sxs-lookup"><span data-stu-id="c158e-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="c158e-120">**支出报表自动过帐**</span><span class="sxs-lookup"><span data-stu-id="c158e-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="c158e-121">为支出报表创建自动过账工作流。</span><span class="sxs-lookup"><span data-stu-id="c158e-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="c158e-122">**支出行项**</span><span class="sxs-lookup"><span data-stu-id="c158e-122">**Expense line item**</span></span>              | <span data-ttu-id="c158e-123">为支出报表行项创建审核工作流。</span><span class="sxs-lookup"><span data-stu-id="c158e-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="c158e-124">**支出行项自动过帐**</span><span class="sxs-lookup"><span data-stu-id="c158e-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="c158e-125">为支出报表行项创建自动过账工作流。</span><span class="sxs-lookup"><span data-stu-id="c158e-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="c158e-126">**出差申请**</span><span class="sxs-lookup"><span data-stu-id="c158e-126">**Travel requisition**</span></span>             | <span data-ttu-id="c158e-127">为出差申请创建审核工作流。</span><span class="sxs-lookup"><span data-stu-id="c158e-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="c158e-128">**预付现金请求**</span><span class="sxs-lookup"><span data-stu-id="c158e-128">**Cash advance request**</span></span>           | <span data-ttu-id="c158e-129">创建预付现金请求的审核工作流。</span><span class="sxs-lookup"><span data-stu-id="c158e-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="c158e-130">**增值税退税**</span><span class="sxs-lookup"><span data-stu-id="c158e-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="c158e-131">创建增值税 (VAT) 退税审核工作流。</span><span class="sxs-lookup"><span data-stu-id="c158e-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

