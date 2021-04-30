---
title: Dynamics 365 Human Resources（2020 年 9 月 3 日）中的新增功能或更改
description: 此主题介绍了 2020 年 9 月 3 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10978d8843e7bce2800d62b63e58152569be9631
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891761"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a><span data-ttu-id="a343d-103">Dynamics 365 Human Resources（2020 年 9 月 3 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="a343d-103">What's new or changed in Dynamics 365 Human Resources (September 3, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a343d-104">此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="a343d-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a343d-105">更改适用于内部版本号 8.1.3504。</span><span class="sxs-lookup"><span data-stu-id="a343d-105">Changes apply to build number 8.1.3504.</span></span> <span data-ttu-id="a343d-106">某些标题中括号内的数字是 Lifecycle Services (LCS) 支持编号，以供参考。</span><span class="sxs-lookup"><span data-stu-id="a343d-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

<span data-ttu-id="a343d-107">有关 Human Resources 中即将推出的功能的详细信息，请参阅 [Dynamics 365 Human Resources 2019 发布波次 2 概述](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)。</span><span class="sxs-lookup"><span data-stu-id="a343d-107">For more information about upcoming features in Human Resources, see [Overview of Dynamics 365 Human Resources 2019 release wave 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span></span> <span data-ttu-id="a343d-108">有关 Human Resources 的更新流程的详细信息，请参阅[更新流程](hr-admin-setup-update-process.md)。</span><span class="sxs-lookup"><span data-stu-id="a343d-108">For more information about the update process for Human Resources, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="in-this-release"></a><span data-ttu-id="a343d-109">在此发布中</span><span class="sxs-lookup"><span data-stu-id="a343d-109">In this release</span></span>

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a><span data-ttu-id="a343d-110">Human Resources 中新的默认财务维度网格和对话框模式 (469495)</span><span class="sxs-lookup"><span data-stu-id="a343d-110">New default financial dimensions grid and dialog pattern throughout Human Resources (469495)</span></span>

<span data-ttu-id="a343d-111">以下区域中现在提供财务维度的新模式：</span><span class="sxs-lookup"><span data-stu-id="a343d-111">The new pattern for financial dimensions is now available in the following areas:</span></span>

- <span data-ttu-id="a343d-112">位置操作（窗体：**HcmPositionActionDetail**）</span><span class="sxs-lookup"><span data-stu-id="a343d-112">Position actions  (Form: **HcmPositionActionDetail**)</span></span>
- <span data-ttu-id="a343d-113">工资单收入代码（窗体：**PayrollEarningCode**）</span><span class="sxs-lookup"><span data-stu-id="a343d-113">Payroll earning codes  (Form: **PayrollEarningCode**)</span></span>

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a><span data-ttu-id="a343d-114">如果未启用休假和缺勤日历增强，则公司休假日历中不显示条目 (484406)</span><span class="sxs-lookup"><span data-stu-id="a343d-114">Entries don't appear in company leave calendar if Leave and absence calendar enhancements aren't enabled (484406)</span></span>

<span data-ttu-id="a343d-115">此版本中解决了公司休假日历中不显示休假条目这一问题。</span><span class="sxs-lookup"><span data-stu-id="a343d-115">This release corrects an issue where leave entries aren't displayed in the company leave calendar.</span></span> <span data-ttu-id="a343d-116">仅当未启用功能管理选项 **休假和缺勤日历增强** 时，才会出现此问题。</span><span class="sxs-lookup"><span data-stu-id="a343d-116">This issue only occurs when the Feature management option **Leave and absence calendar enhancements** isn't enabled.</span></span>

### <a name="benefitplanemployeeentity-issue-467597"></a><span data-ttu-id="a343d-117">BenefitPlanEmployeeEntity 问题 (467597)</span><span class="sxs-lookup"><span data-stu-id="a343d-117">BenefitPlanEmployeeEntity issue (467597)</span></span>

<span data-ttu-id="a343d-118">此版本解决了 **BenefitsPlanEmployee** 实体的问题。</span><span class="sxs-lookup"><span data-stu-id="a343d-118">This release corrects an issue with the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="a343d-119">导入工作人员登记时，现在 **覆盖范围代码** 和 **计划类型代码** 设置正确。</span><span class="sxs-lookup"><span data-stu-id="a343d-119">When importing worker enrollments, the **Coverage code** and the **Plan type code** are now set correctly.</span></span> <span data-ttu-id="a343d-120">此问题导致了员工福利计划在“员工自助服务”的 **工作人员福利计划** 和 **开放登记** 窗体中显示不正确。</span><span class="sxs-lookup"><span data-stu-id="a343d-120">This issue caused employee benefit plans to display incorrectly in the **Worker benefits plan** and **Open enrollment** forms in Employee self service.</span></span>

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a><span data-ttu-id="a343d-121">XML 格式的电子文件 1094-C 输出中丢失字母 (435190)</span><span class="sxs-lookup"><span data-stu-id="a343d-121">Electronic file 1094-C output missing letter in XML (435190)</span></span>

<span data-ttu-id="a343d-122">此更改解决了在向 IRS 提交时 1094-C 输出文件丢失所需字符这一问题。</span><span class="sxs-lookup"><span data-stu-id="a343d-122">This change corrects an issue with the 1094-C output file missing a character needed when submitting to the IRS.</span></span>

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a><span data-ttu-id="a343d-123">“员工可变薪酬”表映射到固定薪酬窗体 (476117)</span><span class="sxs-lookup"><span data-stu-id="a343d-123">Employee variable compensation table mapped to fixed compensation form (476117)</span></span>

<span data-ttu-id="a343d-124">此更改已让固定薪酬字段与固定薪酬窗体一致。</span><span class="sxs-lookup"><span data-stu-id="a343d-124">This change aligns the fixed compensation fields with the fixed compensation form.</span></span> <span data-ttu-id="a343d-125">现在只有可变薪酬窗体中才有可变薪酬字段。</span><span class="sxs-lookup"><span data-stu-id="a343d-125">Variable compensation fields are now only available with the variable compensation form.</span></span>

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a><span data-ttu-id="a343d-126">休假类型的最低余额为负时等记前允许休假请求 (469917)</span><span class="sxs-lookup"><span data-stu-id="a343d-126">Leave requests allowed before enrollment if that leave type has a negative minimum balance (469917)</span></span>

<span data-ttu-id="a343d-127">此更改禁止在计划中等记之前输入休假请求，即使等记的最低余额为负。</span><span class="sxs-lookup"><span data-stu-id="a343d-127">This change prohibits entering leave requests before being enrolled in the plan, even if the enrollment has a negative minimum balance.</span></span> <span data-ttu-id="a343d-128">只能在计划生效时输入或提交请求。</span><span class="sxs-lookup"><span data-stu-id="a343d-128">You can only enter or submit requests when the plan is active.</span></span>

### <a name="document-templates-dont-download-457279"></a><span data-ttu-id="a343d-129">无法下载文档模板 (457279)</span><span class="sxs-lookup"><span data-stu-id="a343d-129">Document templates don't download (457279)</span></span>

<span data-ttu-id="a343d-130">通过此更改，现在可以下载所有文档模板。</span><span class="sxs-lookup"><span data-stu-id="a343d-130">With this change, you can now download all document templates.</span></span> 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a><span data-ttu-id="a343d-131">薪酬计划报表中的“付薪比率”字段的数据显示为列标题，而不是行 (476077)</span><span class="sxs-lookup"><span data-stu-id="a343d-131">Data displays as column headers instead of rows for the Pay rate field in the compensation plan report (476077)</span></span>

<span data-ttu-id="a343d-132">此分析报表现在显示正确的 **付薪比率** 信息。</span><span class="sxs-lookup"><span data-stu-id="a343d-132">The analytics report now displays the correct information for **Pay rate**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="a343d-133">预览模式</span><span class="sxs-lookup"><span data-stu-id="a343d-133">In preview</span></span>

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="a343d-134">Teams 中的 Human Resources 应用程序</span><span class="sxs-lookup"><span data-stu-id="a343d-134">Human Resources application in Teams</span></span>

<span data-ttu-id="a343d-135">员工可以在 Microsoft Teams 中查看和请求离岗时间。</span><span class="sxs-lookup"><span data-stu-id="a343d-135">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="a343d-136">他们可以与机器人交互来创建休假请求。</span><span class="sxs-lookup"><span data-stu-id="a343d-136">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="a343d-137">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="a343d-137">For more information, see:</span></span>

- <span data-ttu-id="a343d-138">Dynamics 365 2020 年发行版本第 1 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="a343d-138">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="a343d-139">Human Resources 文档中的 [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)</span><span class="sxs-lookup"><span data-stu-id="a343d-139">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="a343d-140">Teams 中的 Human Resources 应用预览功能</span><span class="sxs-lookup"><span data-stu-id="a343d-140">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="a343d-141">**通知**：休假请求的提交者和审核人将在 Teams 中的 Human Resources 应用中收到通知。</span><span class="sxs-lookup"><span data-stu-id="a343d-141">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="a343d-142">审批者将可以审批或拒绝休假请求。</span><span class="sxs-lookup"><span data-stu-id="a343d-142">Approvers will be able to approve or deny time-off requests.</span></span> <span data-ttu-id="a343d-143">将通知提交者，说明批准还是拒绝了请求。</span><span class="sxs-lookup"><span data-stu-id="a343d-143">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="a343d-144">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="a343d-144">For more information, see:</span></span>
   - <span data-ttu-id="a343d-145">Dynamics 365 2020 年发行版本第 2 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="a343d-145">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="a343d-146">Human Resources 文档中的 [为 Teams 中的 Human Resources 应用启用通知](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams)</span><span class="sxs-lookup"><span data-stu-id="a343d-146">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="a343d-147">Human Resources 文档中的[为单个用户打开或关闭 Teams 通知](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)</span><span class="sxs-lookup"><span data-stu-id="a343d-147">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="a343d-148">Human Resources 文档中的 [Teams 通知](./hr-teams-leave-app.md#respond-to-teams-notifications)</span><span class="sxs-lookup"><span data-stu-id="a343d-148">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="a343d-149">Human Resources 文档中的[查看团队的休假日历](./hr-teams-leave-app.md#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="a343d-149">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="a343d-150">**经理休假日历**：经理可以在日历视图中查看其直接下属的已批准和待处理的休假。</span><span class="sxs-lookup"><span data-stu-id="a343d-150">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="a343d-151">通过此视图，可以轻松了解其团队成员的离岗时间。</span><span class="sxs-lookup"><span data-stu-id="a343d-151">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="a343d-152">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="a343d-152">For more information, see:</span></span>
   - <span data-ttu-id="a343d-153">Dynamics 365 2020 年发行版本第 2 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="a343d-153">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="a343d-154">Human Resources 文档中的[查看团队的休假日历](./hr-teams-leave-app.md#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="a343d-154">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="a343d-155">用于定位“分配给我的工作项”列表的配置选项 (477004)</span><span class="sxs-lookup"><span data-stu-id="a343d-155">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="a343d-156">现在在仪表板右侧列中提供了一个新的选项，用于定位 **分配给我的工作项** 列表。</span><span class="sxs-lookup"><span data-stu-id="a343d-156">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="a343d-157">通过此更改，所有工作项和待办事宜列表在同一个区域显示。</span><span class="sxs-lookup"><span data-stu-id="a343d-157">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="a343d-158">请通过在功能管理中打开 **预览 - 工作流体验增强** 启用此功能。</span><span class="sxs-lookup"><span data-stu-id="a343d-158">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="a343d-159">有关打开预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。</span><span class="sxs-lookup"><span data-stu-id="a343d-159">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="a343d-160">此功能还可以用于升级个人操作窗体中显示的工作流选项。</span><span class="sxs-lookup"><span data-stu-id="a343d-160">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="a343d-161">工作流选项还在操作快速选项卡上方显示，以便加快访问速度。</span><span class="sxs-lookup"><span data-stu-id="a343d-161">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="a343d-162">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="a343d-162">For more information, see:</span></span> 

- <span data-ttu-id="a343d-163">Dynamics 365 2020 发行波次 2 计划中的[组织和个人管理工作流体验增强](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)</span><span class="sxs-lookup"><span data-stu-id="a343d-163">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![分配给我的工作项](./media/hr-workflow-work-items-assigned-to-me.png)

![工作流项快速访问](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a><span data-ttu-id="a343d-166">即将推出</span><span class="sxs-lookup"><span data-stu-id="a343d-166">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="a343d-167">Dataverse 中包含的核对清单实体</span><span class="sxs-lookup"><span data-stu-id="a343d-167">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="a343d-168">Dataverse 内很快将为入职、离职、转移和业务流程提供核对清单实体。</span><span class="sxs-lookup"><span data-stu-id="a343d-168">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="a343d-169">福利管理原因代码</span><span class="sxs-lookup"><span data-stu-id="a343d-169">Benefits management reason codes</span></span>

<span data-ttu-id="a343d-170">福利管理原因代码很快将与 Human Resources 中的现有原因代码合并。</span><span class="sxs-lookup"><span data-stu-id="a343d-170">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="a343d-171">如果在福利管理中创建了超过 15 个字符的原因代码，则必须在福利管理 **原因代码** 窗体中将该原因代码的名称更改为 15 个字符或更少。</span><span class="sxs-lookup"><span data-stu-id="a343d-171">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="a343d-172">更新名称后，该原因代码将在个人管理中现有原因代码窗体下显示。</span><span class="sxs-lookup"><span data-stu-id="a343d-172">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="a343d-173">此更改将在以后推出，不会影响现有功能。</span><span class="sxs-lookup"><span data-stu-id="a343d-173">This change will be available in the future and won't affect existing functionally.</span></span>

## <a name="see-also"></a><span data-ttu-id="a343d-174">请参阅</span><span class="sxs-lookup"><span data-stu-id="a343d-174">See also</span></span>

[<span data-ttu-id="a343d-175">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="a343d-175">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="a343d-176">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="a343d-176">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="a343d-177">更新流程</span><span class="sxs-lookup"><span data-stu-id="a343d-177">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="a343d-178">管理功能</span><span class="sxs-lookup"><span data-stu-id="a343d-178">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
