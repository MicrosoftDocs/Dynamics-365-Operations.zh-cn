---
title: Dynamics 365 Human Resources（2020 年 9 月 16 日）中的新增功能或更改
description: 此主题介绍了 2020 年 9 月 16 日 Microsoft Dynamics 365 Human Resources 中的新增功能和更改的功能。
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0fe3ac2393e66a00e070d8cb6862c29625d39b53
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057156"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="ac49a-103">Dynamics 365 Human Resources（2020 年 9 月 16 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="ac49a-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ac49a-104">此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="ac49a-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="ac49a-105">更改适用于内部版本号 8.1.3557。</span><span class="sxs-lookup"><span data-stu-id="ac49a-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="ac49a-106">部分功能旁边括号内的数字是 Lifecycle Services (LCS) 支持编号，以供参考。</span><span class="sxs-lookup"><span data-stu-id="ac49a-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="ac49a-107">此版本中包含的功能</span><span class="sxs-lookup"><span data-stu-id="ac49a-107">Included in this release</span></span>

-  [<span data-ttu-id="ac49a-108">已保存视图 - 正式发布</span><span class="sxs-lookup"><span data-stu-id="ac49a-108">Saved views - general availability</span></span>](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="ac49a-109">- 有关详细信息，请参阅[已保存视图](../fin-ops-core/fin-ops/get-started/saved-views.md)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-109">- For more information, see [Saved views](../fin-ops-core/fin-ops/get-started/saved-views.md).</span></span> 

- <span data-ttu-id="ac49a-110">**职位操作** 窗体具有更新的维度网格和新对话框 (469495)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="ac49a-111">如果您在 **Human Resources 共享参数** 的 **高级访问** 中将 **限制访问工作人员信息** 设置为“是”，福利窗体现在仅显示适当的工作人员 (393384)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="ac49a-112">**WorkCalendar** 实体中的新日历生成选项 (477055)：</span><span class="sxs-lookup"><span data-stu-id="ac49a-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="ac49a-113">- 默认结束时间</span><span class="sxs-lookup"><span data-stu-id="ac49a-113">- Default ending time</span></span><br><span data-ttu-id="ac49a-114">- 默认开始时间</span><span class="sxs-lookup"><span data-stu-id="ac49a-114">-    Default starting time</span></span><br><span data-ttu-id="ac49a-115">- 星期五工作日</span><span class="sxs-lookup"><span data-stu-id="ac49a-115">-  Is Friday working day</span></span><br><span data-ttu-id="ac49a-116">- 星期一工作日</span><span class="sxs-lookup"><span data-stu-id="ac49a-116">-  Is Monday working day</span></span><br><span data-ttu-id="ac49a-117">- 星期六工作日</span><span class="sxs-lookup"><span data-stu-id="ac49a-117">-  Is Saturday working day</span></span><br><span data-ttu-id="ac49a-118">- 星期日工作日</span><span class="sxs-lookup"><span data-stu-id="ac49a-118">- Is Sunday working day</span></span><br><span data-ttu-id="ac49a-119">- 星期四工作日</span><span class="sxs-lookup"><span data-stu-id="ac49a-119">- Is Thursday working day</span></span><br><span data-ttu-id="ac49a-120">- 星期二工作日</span><span class="sxs-lookup"><span data-stu-id="ac49a-120">- Is Tuesday working day</span></span><br><span data-ttu-id="ac49a-121">- 星期三工作日</span><span class="sxs-lookup"><span data-stu-id="ac49a-121">- Is Wednesday working day</span></span><br><span data-ttu-id="ac49a-122">- 工作日历假日 ID</span><span class="sxs-lookup"><span data-stu-id="ac49a-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="ac49a-123">**LeaveBankTransactionV1** 实体现在包含原因码 (477823)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="ac49a-124">现在，您可以保存任务录制 (492923)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="ac49a-125">数据现在已成功从 **HCMWorkerContactEntity** 发布 (427620)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="ac49a-126">现在，在 **工作人员操作** 窗体中为合同工工作人员类型显示 **薪酬** 快速选项卡 (482494)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="ac49a-127">现在，如果您设置了 **固定薪酬**，**级别** 和 **计划** 是必填字段。</span><span class="sxs-lookup"><span data-stu-id="ac49a-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="ac49a-128">如果将这些字段保留为空白，将显示错误消息 (482497)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="ac49a-129">现在，**福利** 中的 **计划类型** 字段是一个下拉列表 (488768)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="ac49a-130">如果从 Human Resources 中删除了自定义字段，系统管理员现在会收到通知 (481408)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="ac49a-131">在终止聘用员工流程中，Human Resources 可以正常工作，不会在好像锁定后更改所选公司(479877)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="ac49a-132">经理无法再通过个性化设置添加编号列 (485317)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="ac49a-133">经理无法再从到期的标识号中删除数据范围筛选器 (485321)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="ac49a-134">当 **报告** 字段为空时，将鼠标悬停在职位上仍会显示职位详细信息 (433328)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="ac49a-135">员工现在可以在员工自助服务中查看福利计划信息 (481676)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="ac49a-136">员工现在可以查看所有已注册的课程 (429048)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="ac49a-137">现在，您可以限制 **专业证书** 页的查看选项。</span><span class="sxs-lookup"><span data-stu-id="ac49a-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="ac49a-138">您可以按工作人员状态和工作人员类型将查看选项限制为当前法人 (451501)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="ac49a-139">预览模式</span><span class="sxs-lookup"><span data-stu-id="ac49a-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="ac49a-140">Teams 中的 Human Resources 应用</span><span class="sxs-lookup"><span data-stu-id="ac49a-140">Human Resources app in Teams</span></span>

<span data-ttu-id="ac49a-141">员工可以在 Microsoft Teams 中查看和请求离岗时间。</span><span class="sxs-lookup"><span data-stu-id="ac49a-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="ac49a-142">他们可以与机器人交互来创建休假请求。</span><span class="sxs-lookup"><span data-stu-id="ac49a-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="ac49a-143">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="ac49a-143">For more information, see:</span></span>

- <span data-ttu-id="ac49a-144">Dynamics 365 2020 年发行版本第 1 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="ac49a-144">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="ac49a-145">Human Resources 文档中的 [Teams 中的 Human Resources 应用](./hr-admin-teams-leave-app.md)</span><span class="sxs-lookup"><span data-stu-id="ac49a-145">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="ac49a-146">Teams 中的 Human Resources 应用预览功能</span><span class="sxs-lookup"><span data-stu-id="ac49a-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="ac49a-147">**通知**：休假请求的提交者和审核人将在 Teams 中的 Human Resources 应用中收到通知。</span><span class="sxs-lookup"><span data-stu-id="ac49a-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="ac49a-148">审批者可以批准或拒绝休假请求。</span><span class="sxs-lookup"><span data-stu-id="ac49a-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="ac49a-149">将通知提交者，说明批准还是拒绝了请求。</span><span class="sxs-lookup"><span data-stu-id="ac49a-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="ac49a-150">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="ac49a-150">For more information, see:</span></span>
   - <span data-ttu-id="ac49a-151">Dynamics 365 2020 年发行版本第 2 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="ac49a-151">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="ac49a-152">Human Resources 文档中的 [为 Teams 中的 Human Resources 应用启用通知](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams)</span><span class="sxs-lookup"><span data-stu-id="ac49a-152">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="ac49a-153">Human Resources 文档中的[为单个用户打开或关闭 Teams 通知](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users)</span><span class="sxs-lookup"><span data-stu-id="ac49a-153">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="ac49a-154">Human Resources 文档中的 [Teams 通知](./hr-teams-leave-app.md#respond-to-teams-notifications)</span><span class="sxs-lookup"><span data-stu-id="ac49a-154">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="ac49a-155">Human Resources 文档中的[查看团队的休假日历](./hr-teams-leave-app.md#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="ac49a-155">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="ac49a-156">**经理休假日历**：经理可以在日历视图中查看其直接下属的已批准和待处理的休假。</span><span class="sxs-lookup"><span data-stu-id="ac49a-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="ac49a-157">通过此视图，可以轻松了解其团队成员的离岗时间。</span><span class="sxs-lookup"><span data-stu-id="ac49a-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="ac49a-158">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="ac49a-158">For more information, see:</span></span>
   - <span data-ttu-id="ac49a-159">Dynamics 365 2020 年发行版本第 2 波计划中的 [Microsoft Teams 中的员工休假和缺勤体验](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams)</span><span class="sxs-lookup"><span data-stu-id="ac49a-159">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="ac49a-160">Human Resources 文档中的[查看团队的休假日历](./hr-teams-leave-app.md#view-your-teams-leave-calendar)</span><span class="sxs-lookup"><span data-stu-id="ac49a-160">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="ac49a-161">用于定位“分配给我的工作项”列表的配置选项 (477004)</span><span class="sxs-lookup"><span data-stu-id="ac49a-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="ac49a-162">现在在仪表板右侧列中提供了一个新的选项，用于定位 **分配给我的工作项** 列表。</span><span class="sxs-lookup"><span data-stu-id="ac49a-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="ac49a-163">通过此更改，所有工作项和待办事宜列表在同一个区域显示。</span><span class="sxs-lookup"><span data-stu-id="ac49a-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="ac49a-164">请通过在功能管理中打开 **预览 - 工作流体验增强** 启用此功能。</span><span class="sxs-lookup"><span data-stu-id="ac49a-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="ac49a-165">有关打开预览功能的详细信息，请参阅[管理功能](hr-admin-manage-features.md)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="ac49a-166">此功能还可以用于升级个人操作窗体中显示的工作流选项。</span><span class="sxs-lookup"><span data-stu-id="ac49a-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="ac49a-167">工作流选项还在操作快速选项卡上方显示，以便加快访问速度。</span><span class="sxs-lookup"><span data-stu-id="ac49a-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="ac49a-168">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="ac49a-168">For more information, see:</span></span> 

- <span data-ttu-id="ac49a-169">Dynamics 365 2020 发行波次 2 计划中的[组织和个人管理工作流体验增强](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements)</span><span class="sxs-lookup"><span data-stu-id="ac49a-169">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![分配给我的工作项](./media/hr-workflow-work-items-assigned-to-me.png)

![工作流项快速访问](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="ac49a-172">休假和缺勤日历</span><span class="sxs-lookup"><span data-stu-id="ac49a-172">Leave and absence calendar</span></span>

<span data-ttu-id="ac49a-173">此版本包括休假和缺勤日历的其他日历选项。</span><span class="sxs-lookup"><span data-stu-id="ac49a-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="ac49a-174">有关详细信息，请参阅[查看团队和公司日历](./hr-employee-self-service-calendar.md)。</span><span class="sxs-lookup"><span data-stu-id="ac49a-174">For more information, see [View team and company calendars](./hr-employee-self-service-calendar.md).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="ac49a-175">即将推出</span><span class="sxs-lookup"><span data-stu-id="ac49a-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="ac49a-176">Dataverse 中包含的核对清单实体</span><span class="sxs-lookup"><span data-stu-id="ac49a-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="ac49a-177">Dataverse 内很快将为入职、离职、转移和业务流程提供核对清单实体。</span><span class="sxs-lookup"><span data-stu-id="ac49a-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="ac49a-178">福利管理原因代码</span><span class="sxs-lookup"><span data-stu-id="ac49a-178">Benefits management reason codes</span></span>

<span data-ttu-id="ac49a-179">福利管理原因代码很快将与 Human Resources 中的现有原因代码合并。</span><span class="sxs-lookup"><span data-stu-id="ac49a-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="ac49a-180">如果在福利管理中创建了超过 15 个字符的原因代码，则必须在福利管理 **原因代码** 窗体中将该原因代码的名称更改为 15 个字符或更少。</span><span class="sxs-lookup"><span data-stu-id="ac49a-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="ac49a-181">更新名称后，该原因代码将在个人管理中现有原因代码窗体下显示。</span><span class="sxs-lookup"><span data-stu-id="ac49a-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="ac49a-182">此更改将在以后推出，不会影响现有功能。</span><span class="sxs-lookup"><span data-stu-id="ac49a-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="ac49a-183">请参阅</span><span class="sxs-lookup"><span data-stu-id="ac49a-183">See also</span></span>

[<span data-ttu-id="ac49a-184">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="ac49a-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="ac49a-185">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="ac49a-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="ac49a-186">更新流程</span><span class="sxs-lookup"><span data-stu-id="ac49a-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="ac49a-187">管理功能</span><span class="sxs-lookup"><span data-stu-id="ac49a-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
