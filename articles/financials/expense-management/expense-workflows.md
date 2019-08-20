---
title: 设置费用的工作流
description: 您可以设置用于查看和审核出差和支出单据的工作流流程。
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 86cadf7277fbb7e08dad4b5dc2a46e1c6ce5a888
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840953"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="8a8ef-103">设置费用的工作流</span><span class="sxs-lookup"><span data-stu-id="8a8ef-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a8ef-104">您可以设置用于查看和审核出差和支出单据的工作流流程。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="8a8ef-105">工作流可以定义的单据包括费用报表、出差申请和预付现金请求。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="8a8ef-106">“工作流”代表业务流程。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-106">A workflow represents a business process.</span></span> <span data-ttu-id="8a8ef-107">它定义单据如何在系统中流动并指示必须由谁完成任务或审核单据。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="8a8ef-108">在组织内使用工作流系统具有若干优点：</span><span class="sxs-lookup"><span data-stu-id="8a8ef-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="8a8ef-109">**一致的流程**— 您可定义特定单据（如采购申请和支出报表）的审核流程。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="8a8ef-110">使用工作流系统有助于确保以一致且有效的方式来处理和审核单据。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="8a8ef-111">“流程可见性”— 您可跟踪特定工作流实例的状态、历史记录和绩效指标。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="8a8ef-112">这帮助您确定是否需要对该工作流做出更改，以提高效率。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="8a8ef-113">“集中的工作列表”— 用户可以查看集中化的工作列表，以查看分配给他们的工作流任务和审核任务。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="8a8ef-114">**您可以创建工作流类型**</span><span class="sxs-lookup"><span data-stu-id="8a8ef-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="8a8ef-115">下表列出了您可以在**费用**过程中创建的工作流类型。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="8a8ef-116"><strong>类型</strong></span><span class="sxs-lookup"><span data-stu-id="8a8ef-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="8a8ef-117"><strong>使用此类型可以</strong></span><span class="sxs-lookup"><span data-stu-id="8a8ef-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="8a8ef-118"><strong>支出报表</strong></span><span class="sxs-lookup"><span data-stu-id="8a8ef-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="8a8ef-119">为支出报表创建审核工作流。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="8a8ef-120"><strong>支出报表自动过帐</strong></span><span class="sxs-lookup"><span data-stu-id="8a8ef-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="8a8ef-121">为支出报表创建自动过账工作流。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="8a8ef-122"><strong>支出行项</strong></span><span class="sxs-lookup"><span data-stu-id="8a8ef-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="8a8ef-123">为支出报表行项创建审核工作流。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="8a8ef-124"><strong>支出行项自动过帐</strong></span><span class="sxs-lookup"><span data-stu-id="8a8ef-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="8a8ef-125">为支出报表行项创建自动过账工作流。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="8a8ef-126"><strong>出差申请</strong></span><span class="sxs-lookup"><span data-stu-id="8a8ef-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="8a8ef-127">为出差申请创建审核工作流。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="8a8ef-128"><strong>预付现金请求</strong></span><span class="sxs-lookup"><span data-stu-id="8a8ef-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="8a8ef-129">创建预付现金请求的审核工作流。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="8a8ef-130"><strong>增值税退税</strong></span><span class="sxs-lookup"><span data-stu-id="8a8ef-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="8a8ef-131">创建增值税 (VAT) 退税审核工作流。</span><span class="sxs-lookup"><span data-stu-id="8a8ef-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

