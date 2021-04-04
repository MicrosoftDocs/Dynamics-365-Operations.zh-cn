---
title: Dynamics 365 Human Resources 的新增功能或更改（2020 年 8 月 20 日）
description: 此主题介绍了 2020 年 8 月 20 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d964f9a532582b18471550a68032d00e19a065c4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467257"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a><span data-ttu-id="d5f54-103">Dynamics 365 Human Resources 的新增功能或更改（2020 年 8 月 20 日）</span><span class="sxs-lookup"><span data-stu-id="d5f54-103">What's new or changed in Dynamics 365 Human Resources (August 20, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d5f54-104">此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="d5f54-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d5f54-105">更改适用于内部版本号 8.1.3478。</span><span class="sxs-lookup"><span data-stu-id="d5f54-105">Changes apply to build number 8.1.3478.</span></span> <span data-ttu-id="d5f54-106">某些标题中括号内的数字是 Lifecycle Services (LCS) 支持编号，以供参考。</span><span class="sxs-lookup"><span data-stu-id="d5f54-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a><span data-ttu-id="d5f54-107">在“人员”工作区向卡显示即将发生和待处理休假信息</span><span class="sxs-lookup"><span data-stu-id="d5f54-107">Show upcoming and pending leave of absence information to cards in People workspace</span></span>

<span data-ttu-id="d5f54-108">现在，待处理和即将发生的休假请求选项可在 **人员** 工作区中的休假和缺勤卡上找到。</span><span class="sxs-lookup"><span data-stu-id="d5f54-108">Pending and upcoming leave request options are now available on the Leave and absence cards in the **People** workspace.</span></span>

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a><span data-ttu-id="d5f54-109">默认情况下，“员工自助服务”中“员工”角色的“专用”字段不是“是” (477106)</span><span class="sxs-lookup"><span data-stu-id="d5f54-109">Private field isn't Yes by default for Employee role in Employee self service (477106)</span></span>

<span data-ttu-id="d5f54-110">现在，当员工通过“员工自助服务”中的 **个人信息** 页面添加新地址记录时，**专用** 字段将默认为 **是**。</span><span class="sxs-lookup"><span data-stu-id="d5f54-110">The **Private** field now defaults to **Yes** when employees add new address records through the **Personal information** page in Employee self service.</span></span> 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a><span data-ttu-id="d5f54-111">“人事管理”中的“可雇用的应聘者”快速选项卡显示不正确的应聘者计数 (470110)</span><span class="sxs-lookup"><span data-stu-id="d5f54-111">Candidates to hire FastTab in Personnel management shows an incorrect count of candidates (470110)</span></span>

<span data-ttu-id="d5f54-112">**人事管理** 页面现在可以准确显示要雇用的应聘者数量。</span><span class="sxs-lookup"><span data-stu-id="d5f54-112">The **Personnel management** page now accurately displays the number of candidates to hire.</span></span> 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a><span data-ttu-id="d5f54-113">当应计设置为零时，无法为离职员工输入疾病 (446195)</span><span class="sxs-lookup"><span data-stu-id="d5f54-113">Can’t enter sickness for terminated employee when accrual is set to zero (446195)</span></span>

<span data-ttu-id="d5f54-114">现在允许将来离职员工的休假交易记录，应计将设置为零。</span><span class="sxs-lookup"><span data-stu-id="d5f54-114">Leave transactions are now allowed for employees that have been terminated in the future and the accrual is set to zero.</span></span> <span data-ttu-id="d5f54-115">一直到员工的离职日期均可以输入休假交易记录。</span><span class="sxs-lookup"><span data-stu-id="d5f54-115">Leave transactions can be entered up to the termination date of the employee.</span></span> 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a><span data-ttu-id="d5f54-116">将自定义字段添加到新的工作人员窗体会禁用“管理休假”操作窗格中的字段 (473314)</span><span class="sxs-lookup"><span data-stu-id="d5f54-116">Adding custom fields to the new Worker form disables the fields in the action pane for Manage leave (473314)</span></span>

<span data-ttu-id="d5f54-117">如果已将自定义字段添加到新的 **工作人员** 窗体中，将不再禁用 **管理休假** 中新的 **工作人员** 窗体上的操作窗格选项。</span><span class="sxs-lookup"><span data-stu-id="d5f54-117">Action pane options on the new **Worker** form in **Manage leave** will no longer be disabled if custom fields have been added to the new **Worker** form.</span></span>

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a><span data-ttu-id="d5f54-118">将“休假注释”字段设为必填字段会允许在未输入注释时提交休假请求 (473543)</span><span class="sxs-lookup"><span data-stu-id="d5f54-118">Making the Leave comment field mandatory allows a leave request to be submitted when no comment is entered (473543)</span></span>

<span data-ttu-id="d5f54-119">注释字段现在可以是必填字段，休假请求将遵循此设置。</span><span class="sxs-lookup"><span data-stu-id="d5f54-119">Comment fields can now be mandatory, and leave requests honor this setting.</span></span> <span data-ttu-id="d5f54-120">必填字段是预览功能。</span><span class="sxs-lookup"><span data-stu-id="d5f54-120">Mandatory fields is a preview feature.</span></span>

### <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="d5f54-121">可用于暂停应计的 DMF 实体</span><span class="sxs-lookup"><span data-stu-id="d5f54-121">DMF entity available for accrual suspensions</span></span>

<span data-ttu-id="d5f54-122">DMF 实体现在可用于暂停应计。</span><span class="sxs-lookup"><span data-stu-id="d5f54-122">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="in-preview"></a><span data-ttu-id="d5f54-123">预览模式</span><span class="sxs-lookup"><span data-stu-id="d5f54-123">In preview</span></span>

### <a name="mandatory-fields"></a><span data-ttu-id="d5f54-124">必填字段</span><span class="sxs-lookup"><span data-stu-id="d5f54-124">Mandatory fields</span></span>

<span data-ttu-id="d5f54-125">您可以使用 Human Resources 个性化功能将字段设置为必填字段。</span><span class="sxs-lookup"><span data-stu-id="d5f54-125">You can make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="d5f54-126">此功能需要 **保存的视图**。</span><span class="sxs-lookup"><span data-stu-id="d5f54-126">This feature requires **Saved views**.</span></span> <span data-ttu-id="d5f54-127">有关已保存视图的详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="d5f54-127">For more information about saved views, see:</span></span>

- <span data-ttu-id="d5f54-128">Dynamics 365 2020 年发行版本第 2 波计划中的[已保存视图 - 正式发布](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)</span><span class="sxs-lookup"><span data-stu-id="d5f54-128">[Saved views - general availability](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="d5f54-129">生成可充分利用已保存视图的窗体</span><span class="sxs-lookup"><span data-stu-id="d5f54-129">Build forms that fully utilize saved views</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="d5f54-130">Teams 中的 Human Resources 应用程序</span><span class="sxs-lookup"><span data-stu-id="d5f54-130">Human Resources application in Teams</span></span>

<span data-ttu-id="d5f54-131">员工可以在 Microsoft Teams 中查看和请求离岗时间。</span><span class="sxs-lookup"><span data-stu-id="d5f54-131">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="d5f54-132">他们可以与机器人交互来创建休假请求。</span><span class="sxs-lookup"><span data-stu-id="d5f54-132">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="d5f54-133">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="d5f54-133">For more information, see:</span></span>

- <span data-ttu-id="d5f54-134">Dynamics 365 2020 年发行版本第 1 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="d5f54-134">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- [<span data-ttu-id="d5f54-135">Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="d5f54-135">Human Resources app in Teams</span></span>](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a><span data-ttu-id="d5f54-136">即将到期</span><span class="sxs-lookup"><span data-stu-id="d5f54-136">Coming soon</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="d5f54-137">Teams 中的 Human Resources 应用预览功能</span><span class="sxs-lookup"><span data-stu-id="d5f54-137">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="d5f54-138">**通知**：休假请求的提交者和审核人将在 Teams 中的 Human Resources 应用中收到通知。</span><span class="sxs-lookup"><span data-stu-id="d5f54-138">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="d5f54-139">审核人能够批准或拒绝休假请求，如果请求被批准或拒绝，将通知提交者。</span><span class="sxs-lookup"><span data-stu-id="d5f54-139">Approvers will be able to approve or deny time-off requests, and submitters will be notified if the request was approved or denied.</span></span>
 
- <span data-ttu-id="d5f54-140">**经理休假日历**：经理可以在日历视图中查看其直接下属的已批准和待处理的休假。</span><span class="sxs-lookup"><span data-stu-id="d5f54-140">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="d5f54-141">通过此视图，可以轻松了解其团队成员的离岗时间。</span><span class="sxs-lookup"><span data-stu-id="d5f54-141">This view provides an easy understanding of when their team members are away from work.</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="d5f54-142">Dataverse 中包含的核对清单实体</span><span class="sxs-lookup"><span data-stu-id="d5f54-142">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="d5f54-143">Dataverse 内很快将为入职、离职、转移和业务流程提供核对清单实体。</span><span class="sxs-lookup"><span data-stu-id="d5f54-143">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="known-issues"></a><span data-ttu-id="d5f54-144">已知问题</span><span class="sxs-lookup"><span data-stu-id="d5f54-144">Known issues</span></span>

<span data-ttu-id="d5f54-145">**功能管理** 工作区可能会显示正式发布时被作为预览功能禁用的功能。</span><span class="sxs-lookup"><span data-stu-id="d5f54-145">The **Feature management** workspace may be displaying features that are disabled as preview features when they are generally available.</span></span> <span data-ttu-id="d5f54-146">以下是显示错误状态的正式发布功能的列表。</span><span class="sxs-lookup"><span data-stu-id="d5f54-146">Below is a list of generally available features that show an incorrect status.</span></span> 

- <span data-ttu-id="d5f54-147">福利管理</span><span class="sxs-lookup"><span data-stu-id="d5f54-147">Benefits management</span></span>
- <span data-ttu-id="d5f54-148">案例管理</span><span class="sxs-lookup"><span data-stu-id="d5f54-148">Case management</span></span>
- <span data-ttu-id="d5f54-149">数据库日志记录(审核)</span><span class="sxs-lookup"><span data-stu-id="d5f54-149">Database logging (Auditing)</span></span>
- <span data-ttu-id="d5f54-150">单个公司或单个计划的休假假期额度</span><span class="sxs-lookup"><span data-stu-id="d5f54-150">Leave accrual for a single company or a single plan</span></span>
- <span data-ttu-id="d5f54-151">休假和缺勤假期额度记录暂停</span><span class="sxs-lookup"><span data-stu-id="d5f54-151">Leave and absence accrual suspension</span></span>
- <span data-ttu-id="d5f54-152">余额调整原因代码和注释</span><span class="sxs-lookup"><span data-stu-id="d5f54-152">Balance adjustment reason code and comment</span></span>
- <span data-ttu-id="d5f54-153">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="d5f54-153">Buy and sell leave</span></span>
- <span data-ttu-id="d5f54-154">休假和缺勤日历</span><span class="sxs-lookup"><span data-stu-id="d5f54-154">Leave and absence calendar</span></span>
- <span data-ttu-id="d5f54-155">休假结转规则</span><span class="sxs-lookup"><span data-stu-id="d5f54-155">Leave carry-forward rules</span></span>
- <span data-ttu-id="d5f54-156">休假假期额度记录审核</span><span class="sxs-lookup"><span data-stu-id="d5f54-156">Leave accrual auditing</span></span>
- <span data-ttu-id="d5f54-157">休假假期额度记录删除</span><span class="sxs-lookup"><span data-stu-id="d5f54-157">Leave accrual deletion</span></span>
- <span data-ttu-id="d5f54-158">休假假期额度记录舍入</span><span class="sxs-lookup"><span data-stu-id="d5f54-158">Leave accrual rounding</span></span>
- <span data-ttu-id="d5f54-159">在单个休假计划上配置多个休假类型</span><span class="sxs-lookup"><span data-stu-id="d5f54-159">Configure multiple leave types on a single leave plan</span></span>
- <span data-ttu-id="d5f54-160">更新请假增强功能</span><span class="sxs-lookup"><span data-stu-id="d5f54-160">Update time-off enhancements</span></span>
- <span data-ttu-id="d5f54-161">将员工的全职人力工时用于假期额度记录</span><span class="sxs-lookup"><span data-stu-id="d5f54-161">Use an employee's FTE for accruals</span></span>
- <span data-ttu-id="d5f54-162">跨公司薪酬视图</span><span class="sxs-lookup"><span data-stu-id="d5f54-162">Cross company compensation view</span></span>
- <span data-ttu-id="d5f54-163">打印绩效复查</span><span class="sxs-lookup"><span data-stu-id="d5f54-163">Print performance reviews</span></span>
- <span data-ttu-id="d5f54-164">休假假期额度记录节假日更正</span><span class="sxs-lookup"><span data-stu-id="d5f54-164">Leave accrual holiday corrections</span></span>

### <a name="benefit-plan-employee-entity"></a><span data-ttu-id="d5f54-165">福利计划员工实体</span><span class="sxs-lookup"><span data-stu-id="d5f54-165">Benefit plan employee entity</span></span> 

<span data-ttu-id="d5f54-166">我们最近发现了两个有关 **BenefitsPlanEmployee** 实体的问题。</span><span class="sxs-lookup"><span data-stu-id="d5f54-166">We have recently discovered two issues regarding the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="d5f54-167">导入工作人员登记时，**覆盖范围代码** 和 **计划类型代码** 设置不正确。</span><span class="sxs-lookup"><span data-stu-id="d5f54-167">When importing worker enrollments, the **Coverage code** and the **Plan type code** are being set incorrectly.</span></span> <span data-ttu-id="d5f54-168">此问题导致员工福利计划在“员工自助服务”的 **工作人员福利计划** 窗体和 **开放登记** 窗体中显示不正确。</span><span class="sxs-lookup"><span data-stu-id="d5f54-168">This issue causes employee benefit plans to display incorrectly in the **Worker benefits plan** form and in the **Open enrollment** form in Employee self service.</span></span> <span data-ttu-id="d5f54-169">此问题还会影响员工在“员工自助服务”中选择计划的能力。</span><span class="sxs-lookup"><span data-stu-id="d5f54-169">This issue can also impact the employee's ability to select plans in Employee self service.</span></span> <span data-ttu-id="d5f54-170">当前没有解决方法。</span><span class="sxs-lookup"><span data-stu-id="d5f54-170">Currently there isn't a workaround.</span></span> <span data-ttu-id="d5f54-171">我们将此问题视为高优先级修复，将在我们的下一个版本中推出修复程序。</span><span class="sxs-lookup"><span data-stu-id="d5f54-171">We're treating this as a high-priority fix and will roll out the fix with our next release.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5f54-172">请参阅</span><span class="sxs-lookup"><span data-stu-id="d5f54-172">See also</span></span>

[<span data-ttu-id="d5f54-173">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="d5f54-173">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d5f54-174">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="d5f54-174">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="d5f54-175">更新流程</span><span class="sxs-lookup"><span data-stu-id="d5f54-175">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="d5f54-176">管理功能</span><span class="sxs-lookup"><span data-stu-id="d5f54-176">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]