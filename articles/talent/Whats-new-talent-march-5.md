---
title: Dynamics 365 for Talent（2019 年 3 月 5 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e4ad32ef71c87f52e59959d80c21ae7fcd6d6524
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517465"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a><span data-ttu-id="9657b-103">Dynamics 365 for Talent（2019 年 3 月 5 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="9657b-103">What's new or changed in Dynamics 365 for Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9657b-104">此主题介绍了 Talent 中的新增功能和更改的功能</span><span class="sxs-lookup"><span data-stu-id="9657b-104">This topic describes features that are either new or changed in Talent</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="9657b-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="9657b-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="9657b-106">扩展了 Attract 中的选项集</span><span class="sxs-lookup"><span data-stu-id="9657b-106">Extending option sets in Attract</span></span>

<span data-ttu-id="9657b-107">在 Attract 中，有多个字段是 Common Data Service 内的选项集。</span><span class="sxs-lookup"><span data-stu-id="9657b-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="9657b-108">已引入了新功能，用于扩展选项集，从**拒绝原因**字段、**雇佣类型**字段和**任职类型**字段开始。</span><span class="sxs-lookup"><span data-stu-id="9657b-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9657b-109">工作发布到 LinkedIn 这一功能要求使用**工作详细信息**页中的**雇佣类型**和**任职类型**字段。</span><span class="sxs-lookup"><span data-stu-id="9657b-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="9657b-110">这些字段中的默认值受 LinkedIn 支持，将在发布工作时显示。</span><span class="sxs-lookup"><span data-stu-id="9657b-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="9657b-111">如果要将工作发布到 LinkedIn，并且修改这些字段的现有选项集值，仍将发布工作，但是 LinkedIn 不会显示自定义的**雇佣类型**和**任职类型**值。</span><span class="sxs-lookup"><span data-stu-id="9657b-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="9657b-112">Onboarding 中的更改</span><span class="sxs-lookup"><span data-stu-id="9657b-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="9657b-113">Onboard 工作组的专用预览</span><span class="sxs-lookup"><span data-stu-id="9657b-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="9657b-114">现在可在整个组织中轻松共享和协作处理模板。</span><span class="sxs-lookup"><span data-stu-id="9657b-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="9657b-115">有关详细信息，请参阅[使用 Onboard 工作组在组织中共享最佳实践](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams)。</span><span class="sxs-lookup"><span data-stu-id="9657b-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="9657b-116">受托人占位符的专用预览</span><span class="sxs-lookup"><span data-stu-id="9657b-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="9657b-117">可通过将活动分配给角色而不是个人来丰富模板。</span><span class="sxs-lookup"><span data-stu-id="9657b-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="9657b-118">然后在创建指南时将角色分配给个人。</span><span class="sxs-lookup"><span data-stu-id="9657b-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="9657b-119">有关详细信息，请参阅[通过将活动分配给角色简化指南管理](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles)。</span><span class="sxs-lookup"><span data-stu-id="9657b-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="9657b-120">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="9657b-120">Changes in Core HR</span></span>
<span data-ttu-id="9657b-121">**内部版本 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="9657b-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="9657b-122">将工作流配置为当 HR 或职能经理提交或更新请假时自动批准或执行工作流</span><span class="sxs-lookup"><span data-stu-id="9657b-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="9657b-123">已添加了新的工作流条件，以便在员工的经理或 HR 提交了请假时自动批准。</span><span class="sxs-lookup"><span data-stu-id="9657b-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="9657b-124">若要实现这种自动批准工作流，其中一种方法是为工作流的批准启用自动操作。</span><span class="sxs-lookup"><span data-stu-id="9657b-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="9657b-125">已添加的条件包括：</span><span class="sxs-lookup"><span data-stu-id="9657b-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="9657b-126">提交者 - 用于评估向工作流提交请求的用户的系统用户 ID。</span><span class="sxs-lookup"><span data-stu-id="9657b-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="9657b-127">提交的名义人 - 用于在请求是代表其关联的工作人员提交的时进行评估。</span><span class="sxs-lookup"><span data-stu-id="9657b-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="9657b-128">已由人力资源部门提交 - 用于在提交请求的系统用户属于人力资源角色时进行评估。</span><span class="sxs-lookup"><span data-stu-id="9657b-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="9657b-129">已由经理提交 - 用于在向工作流提交请假的用户是该请假的关联工作人员在层次结构中的职能经理时进行评估。</span><span class="sxs-lookup"><span data-stu-id="9657b-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="9657b-130">为将来的职位分配启用员工固定薪酬</span><span class="sxs-lookup"><span data-stu-id="9657b-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="9657b-131">通常适用于在将来的开始日期加入组织的员工。</span><span class="sxs-lookup"><span data-stu-id="9657b-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="9657b-132">通过此项更改，可以为将来分配的职位所属员工定义固定薪酬。</span><span class="sxs-lookup"><span data-stu-id="9657b-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="9657b-133">编辑职位时，“职位工资”字段为空</span><span class="sxs-lookup"><span data-stu-id="9657b-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="9657b-134">通过此更改，请求更改现有职位时，工资字段现在默认采用当前值。</span><span class="sxs-lookup"><span data-stu-id="9657b-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="9657b-135">其他杂项缺陷修复</span><span class="sxs-lookup"><span data-stu-id="9657b-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="9657b-136">此版本中还包含其他小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="9657b-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="9657b-137">升级到 Common Data Service</span><span class="sxs-lookup"><span data-stu-id="9657b-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="9657b-138">很快将到达 Common Data Service 的升级截止时间。</span><span class="sxs-lookup"><span data-stu-id="9657b-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="9657b-139">请登录 PowerApps 管理员中心以确定是否需要升级您的数据库。</span><span class="sxs-lookup"><span data-stu-id="9657b-139">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="9657b-140">有关截止时间和必要升级步骤的详细信息，请参阅[升级到 Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds)。</span><span class="sxs-lookup"><span data-stu-id="9657b-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="9657b-141">即将到期</span><span class="sxs-lookup"><span data-stu-id="9657b-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="9657b-142">高级薪酬安全（固定和可变）</span><span class="sxs-lookup"><span data-stu-id="9657b-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="9657b-143">在许多组织中，薪酬和福利经理只能访问特定薪酬记录，如管理层或区域员工的记录。</span><span class="sxs-lookup"><span data-stu-id="9657b-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="9657b-144">通过此更改，您可以管理和维护组织中不同员工群的薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="9657b-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="9657b-145">可为固定计划和可变计划分配安全角色，用于决定这些计划和与其有关的员工数据（例如，工资和奖金记录）的访问权限。</span><span class="sxs-lookup"><span data-stu-id="9657b-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="9657b-146">只有具有给定访问权限的角色才能处理这些员工的薪酬。</span><span class="sxs-lookup"><span data-stu-id="9657b-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24"></a><span data-ttu-id="9657b-147">平台 update 24</span><span class="sxs-lookup"><span data-stu-id="9657b-147">Platform update 24</span></span>
<span data-ttu-id="9657b-148">有关平台更新 24 的更多详细信息，请参阅 [Finance and Operations 平台更新 24（2019 年 3 月）中的新增功能或更改](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24)。</span><span class="sxs-lookup"><span data-stu-id="9657b-148">For additional details about Platform update 24, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
