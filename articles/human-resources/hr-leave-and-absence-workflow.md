---
title: 创建休假请求工作流
description: 在 Dynamics 365 Human Resources 中创建休假和缺勤请求工作流以一致地管理休假请求。
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c2c2020c68c4aca3594a2532d32f968ab76f6b7b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463302"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="6e876-103">创建休假请求工作流</span><span class="sxs-lookup"><span data-stu-id="6e876-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6e876-104">您可以在 Dynamics 365 Human Resources 中创建工作流来一致地管理休假和缺勤请求。</span><span class="sxs-lookup"><span data-stu-id="6e876-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="6e876-105">**休假和缺勤** 工作流可让您：</span><span class="sxs-lookup"><span data-stu-id="6e876-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="6e876-106">定义任务</span><span class="sxs-lookup"><span data-stu-id="6e876-106">Define tasks</span></span>
- <span data-ttu-id="6e876-107">确定谁必须完成任务</span><span class="sxs-lookup"><span data-stu-id="6e876-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="6e876-108">指定谁可以批准或拒绝请求</span><span class="sxs-lookup"><span data-stu-id="6e876-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="6e876-109">创建休假和缺勤请求工作流</span><span class="sxs-lookup"><span data-stu-id="6e876-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="6e876-110">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="6e876-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6e876-111">在 **设置** 下，选择 **人力资源工作流**。</span><span class="sxs-lookup"><span data-stu-id="6e876-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="6e876-112">选择 **新建**，然后选择 **休假和缺勤请求**。</span><span class="sxs-lookup"><span data-stu-id="6e876-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="6e876-113">当 **打开此文件?** 消息框出现时，选择 **打开** 并使用您的公司凭据登录。</span><span class="sxs-lookup"><span data-stu-id="6e876-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="6e876-114">使用工作流编辑器为休假请求创建工作流。</span><span class="sxs-lookup"><span data-stu-id="6e876-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="6e876-115">有关使用工作流的详细信息，请参阅[创建工作流概述](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="6e876-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="6e876-116">休假和缺勤请求工作流数据元素</span><span class="sxs-lookup"><span data-stu-id="6e876-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="6e876-117">您可以使用以下数据元素在工作流中为休假和缺勤请求创建条件或自动审批：</span><span class="sxs-lookup"><span data-stu-id="6e876-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="6e876-118">**金额**</span><span class="sxs-lookup"><span data-stu-id="6e876-118">**Amount**</span></span>
- <span data-ttu-id="6e876-119">**注释**</span><span class="sxs-lookup"><span data-stu-id="6e876-119">**Comment**</span></span>
- <span data-ttu-id="6e876-120">**公司**</span><span class="sxs-lookup"><span data-stu-id="6e876-120">**Company**</span></span>
- <span data-ttu-id="6e876-121">**创建人**</span><span class="sxs-lookup"><span data-stu-id="6e876-121">**Created by**</span></span>
- <span data-ttu-id="6e876-122">**创建日期和时间**</span><span class="sxs-lookup"><span data-stu-id="6e876-122">**Created date and time**</span></span>
- <span data-ttu-id="6e876-123">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="6e876-123">**End date**</span></span>
- <span data-ttu-id="6e876-124">**休假类型**</span><span class="sxs-lookup"><span data-stu-id="6e876-124">**Leave type**</span></span>
- <span data-ttu-id="6e876-125">**修改者**</span><span class="sxs-lookup"><span data-stu-id="6e876-125">**Modified by**</span></span>
- <span data-ttu-id="6e876-126">**修改日期和时间**</span><span class="sxs-lookup"><span data-stu-id="6e876-126">**Modified date and time**</span></span>
- <span data-ttu-id="6e876-127">**原因代码**</span><span class="sxs-lookup"><span data-stu-id="6e876-127">**Reason code**</span></span>
- <span data-ttu-id="6e876-128">**请求 ID**</span><span class="sxs-lookup"><span data-stu-id="6e876-128">**Request ID**</span></span>
- <span data-ttu-id="6e876-129">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="6e876-129">**Start date**</span></span>
- <span data-ttu-id="6e876-130">**状态**</span><span class="sxs-lookup"><span data-stu-id="6e876-130">**Status**</span></span> 
- <span data-ttu-id="6e876-131">**提交日期**</span><span class="sxs-lookup"><span data-stu-id="6e876-131">**Submission date**</span></span>
- <span data-ttu-id="6e876-132">**提交者**</span><span class="sxs-lookup"><span data-stu-id="6e876-132">**Submitted by**</span></span>
- <span data-ttu-id="6e876-133">**由人力资源部门提交**</span><span class="sxs-lookup"><span data-stu-id="6e876-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="6e876-134">**由经理提交**</span><span class="sxs-lookup"><span data-stu-id="6e876-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="6e876-135">**作为代表提交**</span><span class="sxs-lookup"><span data-stu-id="6e876-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="6e876-136">**工作线程**</span><span class="sxs-lookup"><span data-stu-id="6e876-136">**Worker**</span></span>
- <span data-ttu-id="6e876-137">**工作人员类型**</span><span class="sxs-lookup"><span data-stu-id="6e876-137">**Worker type**</span></span>

<span data-ttu-id="6e876-138">这些示例说明如何使用以下数据元素创建不同类型的工作流条件：</span><span class="sxs-lookup"><span data-stu-id="6e876-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="6e876-139">在条件语句中使用 **原因代码** 将病假请求和原因代码 **外科** 一起发送给 HR 审批，同时将所有其他原因代码发送给经理。</span><span class="sxs-lookup"><span data-stu-id="6e876-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="6e876-140">有关条件语句的更多信息，请参阅[配置工作流中的条件判定](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow)。</span><span class="sxs-lookup"><span data-stu-id="6e876-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="6e876-141">在自动操作中使用 **由人力资源部门提交** 和 **由经理提交**，以自动批准这些角色代表员工提交的休假请求。</span><span class="sxs-lookup"><span data-stu-id="6e876-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="6e876-142">有关自动操作的更多信息，请参阅[配置工作流中的批准流程](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow)。</span><span class="sxs-lookup"><span data-stu-id="6e876-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="6e876-143">在条件语句或自动操作中使用 **休假类型**，以控制工作流如何传送特定休假类型的请求。</span><span class="sxs-lookup"><span data-stu-id="6e876-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="6e876-144">请参阅</span><span class="sxs-lookup"><span data-stu-id="6e876-144">See also</span></span>

- [<span data-ttu-id="6e876-145">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="6e876-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]