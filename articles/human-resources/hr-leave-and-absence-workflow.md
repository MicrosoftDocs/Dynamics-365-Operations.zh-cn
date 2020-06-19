---
title: 创建休假请求工作流
description: 在 Dynamics 365 Human Resources 中创建休假和缺勤请求工作流以一致地管理休假请求。
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 209f0ec7236778cc0a828102e554b02206b45b73
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428677"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="99808-103">创建休假请求工作流</span><span class="sxs-lookup"><span data-stu-id="99808-103">Create a leave request workflow</span></span>

<span data-ttu-id="99808-104">您可以在 Dynamics 365 Human Resources 中创建工作流来一致地管理休假和缺勤请求。</span><span class="sxs-lookup"><span data-stu-id="99808-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="99808-105">**休假和缺勤**工作流可让您：</span><span class="sxs-lookup"><span data-stu-id="99808-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="99808-106">定义任务</span><span class="sxs-lookup"><span data-stu-id="99808-106">Define tasks</span></span>
- <span data-ttu-id="99808-107">确定谁必须完成任务</span><span class="sxs-lookup"><span data-stu-id="99808-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="99808-108">指定谁可以批准或拒绝请求</span><span class="sxs-lookup"><span data-stu-id="99808-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="99808-109">创建休假和缺勤请求工作流</span><span class="sxs-lookup"><span data-stu-id="99808-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="99808-110">在**休假和缺勤**页面，选择**链接**选项卡。</span><span class="sxs-lookup"><span data-stu-id="99808-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="99808-111">在**设置**下，选择**人力资源工作流**。</span><span class="sxs-lookup"><span data-stu-id="99808-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="99808-112">选择**新建**，然后选择**休假和缺勤请求**。</span><span class="sxs-lookup"><span data-stu-id="99808-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="99808-113">当**打开此文件?** 消息框出现时，选择**打开**并使用您的公司凭据登录。</span><span class="sxs-lookup"><span data-stu-id="99808-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="99808-114">使用工作流编辑器为休假请求创建工作流。</span><span class="sxs-lookup"><span data-stu-id="99808-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="99808-115">有关使用工作流的详细信息，请参阅[创建工作流概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="99808-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="99808-116">休假和缺勤请求工作流数据元素</span><span class="sxs-lookup"><span data-stu-id="99808-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="99808-117">您可以使用以下数据元素在工作流中为休假和缺勤请求创建条件或自动审批：</span><span class="sxs-lookup"><span data-stu-id="99808-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="99808-118">**金额**</span><span class="sxs-lookup"><span data-stu-id="99808-118">**Amount**</span></span>
- <span data-ttu-id="99808-119">**注释**</span><span class="sxs-lookup"><span data-stu-id="99808-119">**Comment**</span></span>
- <span data-ttu-id="99808-120">**公司**</span><span class="sxs-lookup"><span data-stu-id="99808-120">**Company**</span></span>
- <span data-ttu-id="99808-121">**创建人**</span><span class="sxs-lookup"><span data-stu-id="99808-121">**Created by**</span></span>
- <span data-ttu-id="99808-122">**创建日期和时间**</span><span class="sxs-lookup"><span data-stu-id="99808-122">**Created date and time**</span></span>
- <span data-ttu-id="99808-123">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="99808-123">**End date**</span></span>
- <span data-ttu-id="99808-124">**休假类型**</span><span class="sxs-lookup"><span data-stu-id="99808-124">**Leave type**</span></span>
- <span data-ttu-id="99808-125">**修改者**</span><span class="sxs-lookup"><span data-stu-id="99808-125">**Modified by**</span></span>
- <span data-ttu-id="99808-126">**修改日期和时间**</span><span class="sxs-lookup"><span data-stu-id="99808-126">**Modified date and time**</span></span>
- <span data-ttu-id="99808-127">**原因代码**</span><span class="sxs-lookup"><span data-stu-id="99808-127">**Reason code**</span></span>
- <span data-ttu-id="99808-128">**请求 ID**</span><span class="sxs-lookup"><span data-stu-id="99808-128">**Request ID**</span></span>
- <span data-ttu-id="99808-129">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="99808-129">**Start date**</span></span>
- <span data-ttu-id="99808-130">**状态**</span><span class="sxs-lookup"><span data-stu-id="99808-130">**Status**</span></span> 
- <span data-ttu-id="99808-131">**提交日期**</span><span class="sxs-lookup"><span data-stu-id="99808-131">**Submission date**</span></span>
- <span data-ttu-id="99808-132">**提交者**</span><span class="sxs-lookup"><span data-stu-id="99808-132">**Submitted by**</span></span>
- <span data-ttu-id="99808-133">**由人力资源部门提交**</span><span class="sxs-lookup"><span data-stu-id="99808-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="99808-134">**由经理提交**</span><span class="sxs-lookup"><span data-stu-id="99808-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="99808-135">**作为代表提交**</span><span class="sxs-lookup"><span data-stu-id="99808-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="99808-136">**工作线程**</span><span class="sxs-lookup"><span data-stu-id="99808-136">**Worker**</span></span>
- <span data-ttu-id="99808-137">**工作人员类型**</span><span class="sxs-lookup"><span data-stu-id="99808-137">**Worker type**</span></span>

<span data-ttu-id="99808-138">这些示例说明如何使用以下数据元素创建不同类型的工作流条件：</span><span class="sxs-lookup"><span data-stu-id="99808-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="99808-139">在条件语句中使用**原因代码**将病假请求和原因代码**外科**一起发送给 HR 审批，同时将所有其他原因代码发送给经理。</span><span class="sxs-lookup"><span data-stu-id="99808-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="99808-140">有关条件语句的更多信息，请参阅[配置工作流中的条件判定](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow)。</span><span class="sxs-lookup"><span data-stu-id="99808-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="99808-141">在自动操作中使用**由人力资源部门提交**和**由经理提交**，以自动批准这些角色代表员工提交的休假请求。</span><span class="sxs-lookup"><span data-stu-id="99808-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="99808-142">有关自动操作的更多信息，请参阅[配置工作流中的批准流程](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow)。</span><span class="sxs-lookup"><span data-stu-id="99808-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="99808-143">在条件语句或自动操作中使用**休假类型**，以控制工作流如何传送特定休假类型的请求。</span><span class="sxs-lookup"><span data-stu-id="99808-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="99808-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="99808-144">See also</span></span>

- [<span data-ttu-id="99808-145">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="99808-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
