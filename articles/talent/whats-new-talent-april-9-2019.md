---
title: Dynamics 365 for Talent（2019 年 4 月 9 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
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
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 25ef0d49c2600833aefa84d404e00c0c57cfbf52
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517403"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-9-2019"></a><span data-ttu-id="21708-103">Dynamics 365 for Talent（2019 年 4 月 9 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="21708-103">What's new or changed in Dynamics 365 for Talent (April 9, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="21708-104">此主题介绍了 Dynamics 365 for Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="21708-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="21708-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="21708-105">Changes in Attract</span></span>

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a><span data-ttu-id="21708-106">Lifecycle Services (LCS) 与“报告问题”集成</span><span class="sxs-lookup"><span data-stu-id="21708-106">Lifecycle Services (LCS) integration with 'report a problem'</span></span>
<span data-ttu-id="21708-107">在 Attract 和 Onboard 中，最终用户使用报告问题功能记录的问题现在会在客户的 LCS 项目中自动创建报告问题。</span><span class="sxs-lookup"><span data-stu-id="21708-107">In Attract and Onboard, issues logged by end users using the report a problem feature now automatically create support issues in the customer's LCS project.</span></span> <span data-ttu-id="21708-108">管理员然后可以诊断问题并在需要时提交给 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="21708-108">Admins can then triage the issues and submit them to Microsoft when needed.</span></span> <span data-ttu-id="21708-109">这与 Core HR 处理最终用户支持问题的方式一致。</span><span class="sxs-lookup"><span data-stu-id="21708-109">This is consistent with how Core HR handles end user support issues.</span></span>

### <a name="relevance-search"></a><span data-ttu-id="21708-110">相关性搜索</span><span class="sxs-lookup"><span data-stu-id="21708-110">Relevance search</span></span>
<span data-ttu-id="21708-111">现在可以在人才池中搜索整个应聘者数据库以查找特定技能、姓名或教育背景。</span><span class="sxs-lookup"><span data-stu-id="21708-111">In talent pools, you can now search your entire candidate database for particular skills, names, or educational background.</span></span> <span data-ttu-id="21708-112">不再需要指定要搜索应聘者个人资料的哪部分。</span><span class="sxs-lookup"><span data-stu-id="21708-112">You no longer need to specify which section of a candidate's profile you want to search through.</span></span> <span data-ttu-id="21708-113">Attract 搜索整个个人资料并突出显示找到的所有匹配项。</span><span class="sxs-lookup"><span data-stu-id="21708-113">Attract searches the entire profile and highlights all the matches found.</span></span> <span data-ttu-id="21708-114">Attract 还搜索应聘者的所有可用文档并为搜索结果智能分级。</span><span class="sxs-lookup"><span data-stu-id="21708-114">Attract also searches all documents that are available for a candidate and intelligently ranks the search results.</span></span> <span data-ttu-id="21708-115">错误，还可以按来源或是否为银奖获得者来筛选结果。</span><span class="sxs-lookup"><span data-stu-id="21708-115">In addition, you can filter the results by source or by whether they are a silver medalist.</span></span> <span data-ttu-id="21708-116">有关详细信息，请参阅[搜索和查看应聘者个人资料](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles)。</span><span class="sxs-lookup"><span data-stu-id="21708-116">For more information, see [Search and view candidate profiles](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).</span></span>

### <a name="prospect-recommendations"></a><span data-ttu-id="21708-117">潜在人选推荐</span><span class="sxs-lookup"><span data-stu-id="21708-117">Prospect recommendations</span></span>
<span data-ttu-id="21708-118">Attract 可以通过搜索组织的应聘者数据库智能推荐应聘者，在您激活工作帐户立即开始为该工作寻找资源。</span><span class="sxs-lookup"><span data-stu-id="21708-118">Attract can help kickstart sourcing for a job as soon as you activate it by making intelligent candidate recommendations from your organization's candidate database.</span></span> <span data-ttu-id="21708-119">推荐信息中包括在搜索相关潜在人选时确定的技能和教育信息。</span><span class="sxs-lookup"><span data-stu-id="21708-119">The recommendations include the skills and education information identified while searching for relevant prospects.</span></span> <span data-ttu-id="21708-120">如果您在工作的招聘流程中启用**潜在人选**选项卡，将在工作的该选项卡下显示这些推荐信息。</span><span class="sxs-lookup"><span data-stu-id="21708-120">These recommendations appear on the **Prospects** tab under a job, if you enable it during the job's hiring process.</span></span> <span data-ttu-id="21708-121">有关详细信息，请参见[潜在人选推荐](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations)。</span><span class="sxs-lookup"><span data-stu-id="21708-121">For more information, see [Prospect recommendations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).</span></span>

### <a name="interviewer-availability-statuses"></a><span data-ttu-id="21708-122">面试官可用性状态</span><span class="sxs-lookup"><span data-stu-id="21708-122">Interviewer availability statuses</span></span>
<span data-ttu-id="21708-123">面试安排人员很快将可以查看面试官的**外出，其他地点办公**状态，从而有助于安排更适合面试官的时间。</span><span class="sxs-lookup"><span data-stu-id="21708-123">Interview schedulers will soon be able to view **Out of office, working elsewhere** statuses for interviewers, to help schedule times that might work better for interviewers.</span></span>

### <a name="candidate-interview-experience-save-calendar-invites"></a><span data-ttu-id="21708-124">应聘者面试体验：保存日历邀请</span><span class="sxs-lookup"><span data-stu-id="21708-124">Candidate interview experience: Save calendar invites</span></span>
<span data-ttu-id="21708-125">应聘者现在可以使用发给自己的面试摘要电子邮件中附加的 .ics 文件把自己的面试事件下载并保存到个人日历中。</span><span class="sxs-lookup"><span data-stu-id="21708-125">Candidates can now download and save their interview events to their personal calendars using an .ics file attached to the interview summary email sent to the candidate.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="21708-126">Changes 中的更改</span><span class="sxs-lookup"><span data-stu-id="21708-126">Changes in Onboard</span></span>

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a><span data-ttu-id="21708-127">Lifecycle Services (LCS) 与“报告问题”集成</span><span class="sxs-lookup"><span data-stu-id="21708-127">Lifecycle Services (LCS) integration with report a problem</span></span>
<span data-ttu-id="21708-128">在 Attract 和 Onboard 中，最终用户使用报告问题功能记录的问题现在会在客户的 LCS 项目中自动创建报告问题。</span><span class="sxs-lookup"><span data-stu-id="21708-128">In Attract and Onboard, issues logged by end users using the report a problem feature now automatically create support issues in the customer's LCS project.</span></span> <span data-ttu-id="21708-129">管理员然后可以诊断问题并在需要时提交给 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="21708-129">Admins can then triage the issues and submit them to Microsoft when needed.</span></span> <span data-ttu-id="21708-130">这与 Core HR 处理最终用户支持问题的方式一致。</span><span class="sxs-lookup"><span data-stu-id="21708-130">This is consistent with how Core HR handles end user support issues.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="21708-131">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="21708-131">Changes in Core HR</span></span>
<span data-ttu-id="21708-132">本部分中的更改适用于内部版本号 8.1.2225。</span><span class="sxs-lookup"><span data-stu-id="21708-132">Changes described in this section apply to build number 8.1.2225.</span></span>

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a><span data-ttu-id="21708-133">基本可变计划百分比加载的金额不正确</span><span class="sxs-lookup"><span data-stu-id="21708-133">Percent of basis variable plans load incorrect amount</span></span>
<span data-ttu-id="21708-134">本周的版本更正了使用基本计划百分比加载可变薪酬奖励时出错。</span><span class="sxs-lookup"><span data-stu-id="21708-134">This week’s release corrects an issue when loading variable compensation awards using percent of basis plans.</span></span>
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a><span data-ttu-id="21708-135">“最后工作日期”上的日期选择器无法正常工作</span><span class="sxs-lookup"><span data-stu-id="21708-135">Date picker on Last day worked doesn’t work correctly</span></span>
<span data-ttu-id="21708-136">此项更改更正了下面的问题：用户使用日历控件编辑**雇佣结束日期**并选择日期时，向所选日期增加一天。</span><span class="sxs-lookup"><span data-stu-id="21708-136">This change corrects the issue: When users edit the **Employment end date** and select the date using the calendar control, a day is added to the selection.</span></span>

###  <a name="limit-personnel-action-types-by-the-action-taken"></a><span data-ttu-id="21708-137">按执行的操作限制个人操作类型</span><span class="sxs-lookup"><span data-stu-id="21708-137">Limit personnel action types by the action taken</span></span>
<span data-ttu-id="21708-138">此项更改限制执行特定操作时显示的操作类型。</span><span class="sxs-lookup"><span data-stu-id="21708-138">This change limits the action types that appear when taking specific actions.</span></span> <span data-ttu-id="21708-139">例如，请求新职位时，要选择的操作列表中仅显示新职位操作。</span><span class="sxs-lookup"><span data-stu-id="21708-139">For example, when a new position is requested, only the new position actions appear in the list of actions to select.</span></span> <span data-ttu-id="21708-140">以前仅显示新建操作和编辑操作。</span><span class="sxs-lookup"><span data-stu-id="21708-140">Previously, both new and edit actions appeared.</span></span> 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a><span data-ttu-id="21708-141">将员工转到下一个法人时带补偿</span><span class="sxs-lookup"><span data-stu-id="21708-141">Transferring an employee with compensation in a second legal entity</span></span>
<span data-ttu-id="21708-142">此版本允许跨公司转移员工时下一个法人中终止补偿。</span><span class="sxs-lookup"><span data-stu-id="21708-142">This release allows compensation to be ended in a second legal entity if the transfer is for a cross-company transfer.</span></span>

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a><span data-ttu-id="21708-143">转移期间无法为将来的雇佣关系选择补偿</span><span class="sxs-lookup"><span data-stu-id="21708-143">Unable to select compensation for a future employment during a transfer</span></span>
<span data-ttu-id="21708-144">将员工转给新法人时，现在可以在转移期间为新法人设置补偿。</span><span class="sxs-lookup"><span data-stu-id="21708-144">When transferring an employee to a new legal entity, you can now set compensation for the new legal entity during the transfer process.</span></span>

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a><span data-ttu-id="21708-145">用户无法在分配职位期间指定补偿</span><span class="sxs-lookup"><span data-stu-id="21708-145">User isn't able to assign compensation during position assignment</span></span>
<span data-ttu-id="21708-146">由于增加了新的职位分配，所以允许设置固定薪酬记录。</span><span class="sxs-lookup"><span data-stu-id="21708-146">Adding a new position assignment now allows setting up fixed compensation records.</span></span> 

## <a name="in-preview"></a><span data-ttu-id="21708-147">预览模式</span><span class="sxs-lookup"><span data-stu-id="21708-147">In preview</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="21708-148">允许为休假类型指定原因代码</span><span class="sxs-lookup"><span data-stu-id="21708-148">Allow reason codes to be specified on leave types</span></span>
<span data-ttu-id="21708-149">组织可能需要有关休假请求的更多信息。</span><span class="sxs-lookup"><span data-stu-id="21708-149">Organizations might need additional information about time-off requests.</span></span> <span data-ttu-id="21708-150">现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。</span><span class="sxs-lookup"><span data-stu-id="21708-150">You can now specify reason codes for leave types and enable employees to select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a><span data-ttu-id="21708-151">休假请求中的特定休假类型需要原因代码</span><span class="sxs-lookup"><span data-stu-id="21708-151">Require reason codes for certain leave types on time-off requests</span></span>
<span data-ttu-id="21708-152">组织可能会要求当员工提交请假时为特定休假类型设置原因代码。</span><span class="sxs-lookup"><span data-stu-id="21708-152">Organizations might require reason codes for specific leave types when employees submit time off.</span></span> <span data-ttu-id="21708-153">可能是因为公司政策或法规要求所致。</span><span class="sxs-lookup"><span data-stu-id="21708-153">This might be due to company policy or regulatory requirements.</span></span> <span data-ttu-id="21708-154">现在可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。</span><span class="sxs-lookup"><span data-stu-id="21708-154">You can now specify which leave types require a reason code, and you can require employees to provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="21708-155">为 HR 提供休假和缺勤交易记录列表</span><span class="sxs-lookup"><span data-stu-id="21708-155">Provide leave and absence transaction list for HR</span></span>
<span data-ttu-id="21708-156">跟踪员工休假和了解休假的计算方法不仅可以帮助 HR 解答员工的问题，还可以确保员工的休假奖励精确无误。</span><span class="sxs-lookup"><span data-stu-id="21708-156">Tracking employee time off and understanding how time off is calculated not only helps HR answer employee questions, but also ensures accurate time off awards for employees.</span></span> <span data-ttu-id="21708-157">HR 现在可以以新的视觉查看交易记录（授权、应计、调整和请求），以查看余额背后的原因。</span><span class="sxs-lookup"><span data-stu-id="21708-157">HR now has a new view into the transactions (grants, accruals, adjustments, and requests) to see the reasons behind balances.</span></span> 

## <a name="coming-soon"></a><span data-ttu-id="21708-158">即将到期</span><span class="sxs-lookup"><span data-stu-id="21708-158">Coming soon</span></span>

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a><span data-ttu-id="21708-159">改进了用户界面中的重复员工检查</span><span class="sxs-lookup"><span data-stu-id="21708-159">Improvements to the user interface for duplicate employee check</span></span>
<span data-ttu-id="21708-160">借助此更改，输入名称字段时可检测重复项，而状态将显示找到的重复项数量。</span><span class="sxs-lookup"><span data-stu-id="21708-160">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="21708-161">您可以选择提供的链接以打开一个新的页面来评估是否要使用检测到的匹配项。</span><span class="sxs-lookup"><span data-stu-id="21708-161">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="21708-162">为了避免中断数据输入，重复项窗体不会自动打开。</span><span class="sxs-lookup"><span data-stu-id="21708-162">To avoid interrupting data entry, the duplicates form doesn't automatically open.</span></span>

###  <a name="email-support-for-alerts"></a><span data-ttu-id="21708-163">警报的电子邮件支持</span><span class="sxs-lookup"><span data-stu-id="21708-163">Email support for alerts</span></span>
<span data-ttu-id="21708-164">安装平台更新 25 之后，用户可创建警报规则，用于在被事件触发后自动向联系人发送电子邮件通知。</span><span class="sxs-lookup"><span data-stu-id="21708-164">With Platform update 25, users can create alert rules that automatically send email notifications to contacts when triggered by an event.</span></span> 
