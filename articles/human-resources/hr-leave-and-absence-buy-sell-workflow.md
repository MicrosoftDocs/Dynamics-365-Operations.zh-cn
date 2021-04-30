---
title: 创建购买和出售休假请求工作流
description: 在 Dynamics 365 Human Resources 中创建购买和出售休假请求工作流来一致地管理购买和出售休假请求。
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15cedc16fbdbb5d25daa262f094a56bb8fe2f5cc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892697"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="eab45-103">创建购买和出售休假请求工作流</span><span class="sxs-lookup"><span data-stu-id="eab45-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eab45-104">您可以在 Dynamics 365 Human Resources 中创建工作流来一致地管理购买和出售休假请求。</span><span class="sxs-lookup"><span data-stu-id="eab45-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="eab45-105">**购买和出售休假** 工作流可让您：</span><span class="sxs-lookup"><span data-stu-id="eab45-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="eab45-106">定义任务</span><span class="sxs-lookup"><span data-stu-id="eab45-106">Define tasks</span></span>
- <span data-ttu-id="eab45-107">确定谁必须完成任务</span><span class="sxs-lookup"><span data-stu-id="eab45-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="eab45-108">指定谁可以批准或拒绝请求</span><span class="sxs-lookup"><span data-stu-id="eab45-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="eab45-109">创建购买和出售休假请求工作流</span><span class="sxs-lookup"><span data-stu-id="eab45-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="eab45-110">在 **休假和缺勤** 页面，选择 **链接** 选项卡。</span><span class="sxs-lookup"><span data-stu-id="eab45-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="eab45-111">在 **设置** 下，选择 **人力资源工作流**。</span><span class="sxs-lookup"><span data-stu-id="eab45-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="eab45-112">选择 **新建**，然后选择 **购买和出售休假请求**。</span><span class="sxs-lookup"><span data-stu-id="eab45-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="eab45-113">当 **打开此文件?** 消息框出现时，选择 **打开** 并使用您的公司凭据登录。</span><span class="sxs-lookup"><span data-stu-id="eab45-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="eab45-114">使用工作流编辑器为休假请求创建工作流。</span><span class="sxs-lookup"><span data-stu-id="eab45-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="eab45-115">有关使用工作流的详细信息，请参阅[创建工作流概述](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="eab45-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="eab45-116">休假和缺勤请求工作流数据元素</span><span class="sxs-lookup"><span data-stu-id="eab45-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="eab45-117">您可以使用以下数据元素在工作流中为购买和出售休假请求创建条件或自动审批：</span><span class="sxs-lookup"><span data-stu-id="eab45-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="eab45-118">**金额**</span><span class="sxs-lookup"><span data-stu-id="eab45-118">**Amount**</span></span>
- <span data-ttu-id="eab45-119">**购买和出售休假政策**</span><span class="sxs-lookup"><span data-stu-id="eab45-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="eab45-120">**公司**</span><span class="sxs-lookup"><span data-stu-id="eab45-120">**Company**</span></span>
- <span data-ttu-id="eab45-121">**创建人**</span><span class="sxs-lookup"><span data-stu-id="eab45-121">**Created by**</span></span>
- <span data-ttu-id="eab45-122">**创建日期和时间**</span><span class="sxs-lookup"><span data-stu-id="eab45-122">**Created date and time**</span></span>
- <span data-ttu-id="eab45-123">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="eab45-123">**End date**</span></span>
- <span data-ttu-id="eab45-124">**休假类型**</span><span class="sxs-lookup"><span data-stu-id="eab45-124">**Leave type**</span></span>
- <span data-ttu-id="eab45-125">**修改者**</span><span class="sxs-lookup"><span data-stu-id="eab45-125">**Modified by**</span></span>
- <span data-ttu-id="eab45-126">**修改日期和时间**</span><span class="sxs-lookup"><span data-stu-id="eab45-126">**Modified date and time**</span></span>
- <span data-ttu-id="eab45-127">**请求 ID**</span><span class="sxs-lookup"><span data-stu-id="eab45-127">**Request ID**</span></span>
- <span data-ttu-id="eab45-128">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="eab45-128">**Start date**</span></span>
- <span data-ttu-id="eab45-129">**状态**</span><span class="sxs-lookup"><span data-stu-id="eab45-129">**Status**</span></span> 
- <span data-ttu-id="eab45-130">**提交日期**</span><span class="sxs-lookup"><span data-stu-id="eab45-130">**Submission date**</span></span>
- <span data-ttu-id="eab45-131">**提交者**</span><span class="sxs-lookup"><span data-stu-id="eab45-131">**Submitted by**</span></span>
- <span data-ttu-id="eab45-132">**由人力资源部门提交**</span><span class="sxs-lookup"><span data-stu-id="eab45-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="eab45-133">**由经理提交**</span><span class="sxs-lookup"><span data-stu-id="eab45-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="eab45-134">**作为代表提交**</span><span class="sxs-lookup"><span data-stu-id="eab45-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="eab45-135">**工作线程**</span><span class="sxs-lookup"><span data-stu-id="eab45-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="eab45-136">工作流示例</span><span class="sxs-lookup"><span data-stu-id="eab45-136">Workflow examples</span></span>

<span data-ttu-id="eab45-137">这些示例说明如何使用以下数据元素创建不同类型的工作流条件：</span><span class="sxs-lookup"><span data-stu-id="eab45-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="eab45-138">在自动操作中使用 **由人力资源部门提交** 和 **由经理提交**，以自动批准这些角色代表员工提交的购买和出售休假请求。</span><span class="sxs-lookup"><span data-stu-id="eab45-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="eab45-139">有关自动操作的更多信息，请参阅[配置工作流中的批准流程](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md)。</span><span class="sxs-lookup"><span data-stu-id="eab45-139">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="eab45-140">在条件语句或自动操作中使用 **休假类型**，以控制工作流如何传送特定休假类型的请求。</span><span class="sxs-lookup"><span data-stu-id="eab45-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="eab45-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="eab45-141">See also</span></span>

[<span data-ttu-id="eab45-142">休假和缺勤概览</span><span class="sxs-lookup"><span data-stu-id="eab45-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="eab45-143">管理购买和出售休假策略</span><span class="sxs-lookup"><span data-stu-id="eab45-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]