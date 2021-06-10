---
title: Dynamics 365 Human Resources（2020 年 5 月 28 日）中的新增功能或更改
description: 此主题介绍了 2020 年 5 月 28 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: andreabichsel
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d5396e24f036e670ce276911cd3582442a98da7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054324"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="62504-103">Dynamics 365 Human Resources（2020 年 5 月 28 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="62504-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="62504-104">此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="62504-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="62504-105">更改适用于内部版本号 8.1.3287。</span><span class="sxs-lookup"><span data-stu-id="62504-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="62504-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="62504-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="62504-107">在每个休假计划中启用多种类型时，LeaveRequest 实体不起作用 (447498)</span><span class="sxs-lookup"><span data-stu-id="62504-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="62504-108">通过此更改，**LeaveEnrollmentV2Entity** 现在可用于更正启用多个休假类型时发生的错误。</span><span class="sxs-lookup"><span data-stu-id="62504-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="62504-109">批处理争用缩减功能（预览）(446619)</span><span class="sxs-lookup"><span data-stu-id="62504-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="62504-110">启用此功能后，可以减少选择任务和完成作业时对批处理框架表的阻碍。</span><span class="sxs-lookup"><span data-stu-id="62504-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="62504-111">保存工作人员时发生的 UpdateConflict 阻止在“人员”中编辑记录 (427915)</span><span class="sxs-lookup"><span data-stu-id="62504-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="62504-112">此更改更正添加新工作人员、更新地址信息和更改语言首选项时出现的错误。</span><span class="sxs-lookup"><span data-stu-id="62504-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="62504-113">在此特殊情况下，显示的错误指示无法更新记录。</span><span class="sxs-lookup"><span data-stu-id="62504-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="62504-114">无法向批准的请假添加附件以重新提交 (425407)</span><span class="sxs-lookup"><span data-stu-id="62504-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="62504-115">此更改现在允许附件添加到批准的休假请求中。</span><span class="sxs-lookup"><span data-stu-id="62504-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="62504-116">用户可以在其他法人窗体中为员工输入薪酬 (409529)</span><span class="sxs-lookup"><span data-stu-id="62504-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="62504-117">此更改禁用了薪酬选项，以防止为错误的法人误输入薪酬条目。</span><span class="sxs-lookup"><span data-stu-id="62504-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="62504-118">当您转移员工并且工作人员职位分配日期早于职位期限时发生错误 (429402)</span><span class="sxs-lookup"><span data-stu-id="62504-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="62504-119">在此情况下转移员工时显示的错误消息已更新，以更好地描述更正问题所需的更改。</span><span class="sxs-lookup"><span data-stu-id="62504-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="62504-120">员工自助服务福利登记中的附件功能</span><span class="sxs-lookup"><span data-stu-id="62504-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="62504-121">现在，您可以在福利登记流程中为员工登记的每个计划添加附件。</span><span class="sxs-lookup"><span data-stu-id="62504-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="62504-122">然后，您可以在 **工作人员登记福利** 窗体中查看附件。</span><span class="sxs-lookup"><span data-stu-id="62504-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="62504-123">预览模式</span><span class="sxs-lookup"><span data-stu-id="62504-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="62504-124">Teams 中的 Human Resources 应用程序</span><span class="sxs-lookup"><span data-stu-id="62504-124">Human Resources application in Teams</span></span>

<span data-ttu-id="62504-125">员工可以在 Microsoft Teams 中查看和请求离岗时间。</span><span class="sxs-lookup"><span data-stu-id="62504-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="62504-126">他们可以与机器人交互来创建休假请求。</span><span class="sxs-lookup"><span data-stu-id="62504-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="62504-127">有关详细信息，请参阅 [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)。</span><span class="sxs-lookup"><span data-stu-id="62504-127">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="62504-128">休假暂停</span><span class="sxs-lookup"><span data-stu-id="62504-128">Leave suspension</span></span>

<span data-ttu-id="62504-129">可在 Human Resources 中暂停员工的休假和缺勤。</span><span class="sxs-lookup"><span data-stu-id="62504-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="62504-130">暂停休假将停止所选休假类型的休假应计。</span><span class="sxs-lookup"><span data-stu-id="62504-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="62504-131">如果处理了应计后发生暂停，暂停休假将为员工的休假余额创建按比例调整。</span><span class="sxs-lookup"><span data-stu-id="62504-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="62504-132">有关详细信息，请参阅[暂停休假](hr-leave-and-absence-suspend-leave.md)。</span><span class="sxs-lookup"><span data-stu-id="62504-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="62504-133">更新用户体验以表明应计已暂停 (429550)</span><span class="sxs-lookup"><span data-stu-id="62504-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="62504-134">用户体验现在表明计划已暂停应计。</span><span class="sxs-lookup"><span data-stu-id="62504-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="62504-135">即将到期</span><span class="sxs-lookup"><span data-stu-id="62504-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="62504-136">数据库日志记录（6 月预览）</span><span class="sxs-lookup"><span data-stu-id="62504-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="62504-137">数据库日志记录功能让您可以确定应该监视哪些表和字段。</span><span class="sxs-lookup"><span data-stu-id="62504-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="62504-138">它还让您能够确定应该触发更改跟踪的事件。</span><span class="sxs-lookup"><span data-stu-id="62504-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="62504-139">查询功能可用于查看一段时间内发生的更改。</span><span class="sxs-lookup"><span data-stu-id="62504-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="62504-140">购买和出售休假（6 月 1 日预览）</span><span class="sxs-lookup"><span data-stu-id="62504-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="62504-141">一些组织提供允许员工购买和出售其休假的福利。</span><span class="sxs-lookup"><span data-stu-id="62504-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="62504-142">此流程通常通过手动管理。</span><span class="sxs-lookup"><span data-stu-id="62504-142">This process is often managed manually.</span></span> <span data-ttu-id="62504-143">此功能提供了一种更加自动化的方法来管理人力资源部门的政策和请求，它可以帮助消除错误并简化休假管理流程。</span><span class="sxs-lookup"><span data-stu-id="62504-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span> <span data-ttu-id="62504-144">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="62504-144">For more information, see:</span></span>

- [<span data-ttu-id="62504-145">管理购买和出售休假策略</span><span class="sxs-lookup"><span data-stu-id="62504-145">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="62504-146">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="62504-146">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="62504-147">用于福利管理的数据管理框架 (DMF) 实体</span><span class="sxs-lookup"><span data-stu-id="62504-147">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="62504-148">福利管理实体即将发布。</span><span class="sxs-lookup"><span data-stu-id="62504-148">Benefits management entities are releasing.</span></span> <span data-ttu-id="62504-149">DMF 实体允许导入和导出数据，以轻松配置福利管理。</span><span class="sxs-lookup"><span data-stu-id="62504-149">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="62504-150">福利管理模板也可用于移动数据。</span><span class="sxs-lookup"><span data-stu-id="62504-150">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="62504-151">模板以顺序方式导出和导入数据，以保持数据依赖关系。</span><span class="sxs-lookup"><span data-stu-id="62504-151">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="62504-152">将原因代码添加到应计暂停（6 月 1 日）</span><span class="sxs-lookup"><span data-stu-id="62504-152">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="62504-153">原因代码已添加到应计暂停。</span><span class="sxs-lookup"><span data-stu-id="62504-153">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="62504-154">结转规则（6 月 1 日）</span><span class="sxs-lookup"><span data-stu-id="62504-154">Carry forward rules (June 1)</span></span>

<span data-ttu-id="62504-155">可为转移了结转调整的结转余额指定结转休假类型。</span><span class="sxs-lookup"><span data-stu-id="62504-155">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="62504-156">例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。</span><span class="sxs-lookup"><span data-stu-id="62504-156">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="62504-157">有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。</span><span class="sxs-lookup"><span data-stu-id="62504-157">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="62504-158">暂停指定休假类型的休假应计（6 月 1 日）</span><span class="sxs-lookup"><span data-stu-id="62504-158">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="62504-159">在此版本中，HR 可以创建一个规则，以针对输入了无薪假休假请求的员工暂停休假应计。</span><span class="sxs-lookup"><span data-stu-id="62504-159">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="62504-160">无薪假可以是一种类型，但不是必须的。</span><span class="sxs-lookup"><span data-stu-id="62504-160">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="62504-161">您可以根据其他休假类型暂停任何休假。</span><span class="sxs-lookup"><span data-stu-id="62504-161">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="62504-162">可用于暂停应计的 DMF 实体（6 月 1 日）</span><span class="sxs-lookup"><span data-stu-id="62504-162">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="62504-163">DMF 实体现在可用于暂停应计。</span><span class="sxs-lookup"><span data-stu-id="62504-163">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="see-also"></a><span data-ttu-id="62504-164">请参阅</span><span class="sxs-lookup"><span data-stu-id="62504-164">See also</span></span>

[<span data-ttu-id="62504-165">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="62504-165">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="62504-166">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="62504-166">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="62504-167">更新流程</span><span class="sxs-lookup"><span data-stu-id="62504-167">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="62504-168">管理功能</span><span class="sxs-lookup"><span data-stu-id="62504-168">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]