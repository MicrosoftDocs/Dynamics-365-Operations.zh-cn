---
title: Dynamics 365 for Talent Core HR（2019 年 1 月 11 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6e7edf52db663c7ad28f316c324d68e57bf6699a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "303445"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-january-11-2019"></a><span data-ttu-id="3543c-103">Dynamics 365 for Talent Core HR（2019 年 1 月 11 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="3543c-103">What's new or changed in Dynamics 365 for Talent Core HR (January 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3543c-104">**内部版本 8.1.2100**</span><span class="sxs-lookup"><span data-stu-id="3543c-104">**Build 8.1.2100**</span></span>

<span data-ttu-id="3543c-105">此主题介绍了 Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="3543c-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="3543c-106">更改</span><span class="sxs-lookup"><span data-stu-id="3543c-106">Changes</span></span>

### <a name="validate-leave-requests-by-forecasting-available-balance"></a><span data-ttu-id="3543c-107">通过预测可用余额验证休假请求</span><span class="sxs-lookup"><span data-stu-id="3543c-107">Validate leave requests by forecasting available balance</span></span>
<span data-ttu-id="3543c-108">在此版本中所做的更改允许员工请求未来的休假，而不减少当前余额。</span><span class="sxs-lookup"><span data-stu-id="3543c-108">Changes made in this release allow employees to request future leave time without subtracting from their current balance.</span></span> <span data-ttu-id="3543c-109">标准工作流将用于发起的所有未来请求。</span><span class="sxs-lookup"><span data-stu-id="3543c-109">Standard workflows will be used for any future requests made.</span></span> <span data-ttu-id="3543c-110">有关详细信息，请阅读[根据工作时数累积休假时间](leave-accrue-hours-worked.md)。</span><span class="sxs-lookup"><span data-stu-id="3543c-110">For more information, read [Accrue time off based on hours worked](leave-accrue-hours-worked.md).</span></span>

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a><span data-ttu-id="3543c-111">查看 ESS 和“人员”中的预测休假余额</span><span class="sxs-lookup"><span data-stu-id="3543c-111">View forecasted leave balance in ESS and People</span></span>
<span data-ttu-id="3543c-112">此功能支持按人力资源、经理和员工查看将来休假期间的余额。</span><span class="sxs-lookup"><span data-stu-id="3543c-112">This feature enables viewing of balances for future leave periods by HR, managers, and employees.</span></span> <span data-ttu-id="3543c-113">员工可以在**员工自助服务**工作区中查看将来的余额，HR 有权使用**人员**工作区访问相同信息。</span><span class="sxs-lookup"><span data-stu-id="3543c-113">Employees can view future balances in the **Employee Self-Service** workspace and HR has access to the same information using the **People** workspace.</span></span>

### <a name="notifications-for-changing-leave-balances"></a><span data-ttu-id="3543c-114">更改休假余额的通知</span><span class="sxs-lookup"><span data-stu-id="3543c-114">Notifications for changing leave balances</span></span>
<span data-ttu-id="3543c-115">休假余额将显示员工的当前余额。</span><span class="sxs-lookup"><span data-stu-id="3543c-115">Leave balances will display the employees current balance.</span></span> <span data-ttu-id="3543c-116">将来余额可以通过输入“截止日期”计算预测余额在**员工自助服务**和**人员**工作区提供。</span><span class="sxs-lookup"><span data-stu-id="3543c-116">Future balances are available on the **Employee Self-Service** and **People** workspaces by entering an “as of date” to calculate the forecasted balance.</span></span>

<span data-ttu-id="3543c-117">已在以下区域添加查看预测余额的导航：</span><span class="sxs-lookup"><span data-stu-id="3543c-117">Navigation has been added to view forecasted balances in the following areas:</span></span>
  - <span data-ttu-id="3543c-118">**员工自助服务**工作区的**休假**卡。</span><span class="sxs-lookup"><span data-stu-id="3543c-118">**Time off** card on the **Employee Self-Service** workspace.</span></span>
  - <span data-ttu-id="3543c-119">**经理自助服务**工作区的**休假和缺勤**卡。</span><span class="sxs-lookup"><span data-stu-id="3543c-119">**Leave and absence** card on the **Manager Self-Service** workspace.</span></span>
  - <span data-ttu-id="3543c-120">**人员**工作区的**休假和缺勤**页。</span><span class="sxs-lookup"><span data-stu-id="3543c-120">**Leave and absence** page on the **People** workspace.</span></span>

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a><span data-ttu-id="3543c-121">允许可变薪酬计划（现金计划）有小数位</span><span class="sxs-lookup"><span data-stu-id="3543c-121">Allow decimals for Variable compensation plans (Cash plans)</span></span>
<span data-ttu-id="3543c-122">可变现金奖励和计划现在对有小数金额的值有更多的金额和覆盖灵活性。</span><span class="sxs-lookup"><span data-stu-id="3543c-122">Variable cash awards and plans now have the additional flexibility for amounts and overrides for values with decimal amounts.</span></span>

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a><span data-ttu-id="3543c-123">在保存计划后无法更改可变薪酬登记的日期</span><span class="sxs-lookup"><span data-stu-id="3543c-123">Unable to change the dates on Variable comp enrollments after the plan is saved</span></span>
<span data-ttu-id="3543c-124">此更改允许在保存计划后更新计划结束日期（延长或到期）。</span><span class="sxs-lookup"><span data-stu-id="3543c-124">This change allows for the plan end date to be updated (extended or expired) after the plan has been saved.</span></span> <span data-ttu-id="3543c-125">您仍然可以启用或停用与开始日期和结束日期无关的计划。</span><span class="sxs-lookup"><span data-stu-id="3543c-125">You can still activate or de-activate plans independent of start and end dates.</span></span>

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a><span data-ttu-id="3543c-126">工资单信息在分配了工资管理员安全角色时可用</span><span class="sxs-lookup"><span data-stu-id="3543c-126">Payroll information available when assigned the Payroll admin security role</span></span>
<span data-ttu-id="3543c-127">工资管理员角色已更新，可以在请求过程中访问工资单信息。</span><span class="sxs-lookup"><span data-stu-id="3543c-127">The Payroll Administrator role has been updated to have access to the payroll information during the request process.</span></span>

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="3543c-128">从磁贴深化的员工自助服务 | 职位层次结构无法获取父节点</span><span class="sxs-lookup"><span data-stu-id="3543c-128">Employee self-service | Position hierarchy drill-down from tile fails to get parent node</span></span>
<span data-ttu-id="3543c-129">已进行更改以清除在向新工作区添加职位层次结构和在组织结构内导航时发生的错误。</span><span class="sxs-lookup"><span data-stu-id="3543c-129">Changes have been made to eliminate an error that occurred when adding the position hierarchy to new workspaces and navigating within the organizational structure.</span></span>

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a><span data-ttu-id="3543c-130">人员编号规则正在使用时的新验证消息</span><span class="sxs-lookup"><span data-stu-id="3543c-130">New validation message when personnel number sequence is in use</span></span>
<span data-ttu-id="3543c-131">已进行更改以澄清当您雇用员工且下一个人员编号正在使用时的问题。</span><span class="sxs-lookup"><span data-stu-id="3543c-131">A change has been made to clarify what the issue is when you hire an employee and the next personnel number is in use.</span></span>

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a><span data-ttu-id="3543c-132">选择作为初始启动页的员工自助服务工作区</span><span class="sxs-lookup"><span data-stu-id="3543c-132">Employee self-service workspace selected as the initial startup page</span></span>
<span data-ttu-id="3543c-133">在**员工自助服务**工作区被选择作为用户的初始启动页且该用户未被分配员工角色时，系统将重定向到默认仪表板。</span><span class="sxs-lookup"><span data-stu-id="3543c-133">When the **Employee self-service** workspace is selected as the initial startup page for a user and that user is not assigned the employee role, the system will redirect to the default dashboard.</span></span>

### <a name="termination-reason-code-updates-position-assignment-record"></a><span data-ttu-id="3543c-134">终止原因代码更新职位分配记录</span><span class="sxs-lookup"><span data-stu-id="3543c-134">Termination reason code updates position assignment record</span></span>
<span data-ttu-id="3543c-135">终止原因代码现在将在终止雇用员工和结束职位时更新职位分配。</span><span class="sxs-lookup"><span data-stu-id="3543c-135">The termination reason code will now update the position assignment when terminating an employee and ending the position.</span></span> 
