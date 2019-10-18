---
title: Dynamics 365 Talent（2019 年 4 月 16 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 Talent 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0781a479ebf37334d8eba18ea6d69d7cfb9db9ea
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024129"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a><span data-ttu-id="93989-103">Dynamics 365 Talent（2019 年 4 月 16 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="93989-103">What's new or changed in Dynamics 365 Talent (April 16, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="93989-104">此主题介绍了 Dynamics 365 Talent 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="93989-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="93989-105">Attract 中的更改</span><span class="sxs-lookup"><span data-stu-id="93989-105">Changes in Attract</span></span>

### <a name="process-auditing"></a><span data-ttu-id="93989-106">流程审核</span><span class="sxs-lookup"><span data-stu-id="93989-106">Process auditing</span></span>

<span data-ttu-id="93989-107">现在可跟踪对应聘者、职位空缺和工作申请进行的更改。</span><span class="sxs-lookup"><span data-stu-id="93989-107">You can now track the changes made to candidates, job openings, and job applications.</span></span> <span data-ttu-id="93989-108">有关详细信息，请参阅[跟踪招聘数据的变化](process-auditing.md)。</span><span class="sxs-lookup"><span data-stu-id="93989-108">For more information, see [Track changes in recruiting data](process-auditing.md).</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="93989-109">Onboard 中的更改</span><span class="sxs-lookup"><span data-stu-id="93989-109">Changes in Onboard</span></span>

<span data-ttu-id="93989-110">本版本中包含 Dynamics 365 Talent: Onboard 的小缺陷修复。</span><span class="sxs-lookup"><span data-stu-id="93989-110">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="93989-111">Core HR 中的更改</span><span class="sxs-lookup"><span data-stu-id="93989-111">Changes in Core HR</span></span>

<span data-ttu-id="93989-112">本部分中的更改适用于内部版本号 8.1.2239。</span><span class="sxs-lookup"><span data-stu-id="93989-112">Changes described in this section apply to build number 8.1.2239.</span></span> <span data-ttu-id="93989-113">括号内的数字是 Lifecycle Services (LCS) 中的支持号码。</span><span class="sxs-lookup"><span data-stu-id="93989-113">Numbers in parentheses refer to support numbers in Lifecycle Services (LCS).</span></span>

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a><span data-ttu-id="93989-114">Common Data Service 中的“薪酬区域”、“薪酬级别”、“福利选项”和“技能类型”实体已更新，现在包含客户字段支持。</span><span class="sxs-lookup"><span data-stu-id="93989-114">Compensation region, Compensation level, Benefit option and Skill type entities in Common Data Service updated to include customer field support</span></span>

<span data-ttu-id="93989-115">在此版本中，已将这些 Common Data Service 实体更新为可包含通过 Talent: Core HR 添加的自定义字段。</span><span class="sxs-lookup"><span data-stu-id="93989-115">With this release, these Common Data Service entities have been updated to include the ability to include custom field added through Talent: Core HR.</span></span>

### <a name="new-common-data-service-entity-support-for-compensation-vesting-rules-compensation-variable-plan-variable-compensation"></a><span data-ttu-id="93989-116">新增了对以下 Common Data Service 实体的支持：“薪酬股份行权规则”、“薪酬可变计划”、“可变薪酬”</span><span class="sxs-lookup"><span data-stu-id="93989-116">New Common Data Service entity support for: Compensation vesting rules, Compensation variable plan, Variable compensation</span></span>

<span data-ttu-id="93989-117">在此版本中，已向 Common Data Service 添加了“薪酬股份行权规则”、“薪酬可变计划”和“可变薪酬”实体。</span><span class="sxs-lookup"><span data-stu-id="93989-117">With this release, Compensation vesting rules, Compensation variable plan, and Variable compensation entities have been added to Common Data Service.</span></span> <span data-ttu-id="93989-118">这些实体也支持通过 Talent: Core HR 添加的自定义字段。</span><span class="sxs-lookup"><span data-stu-id="93989-118">These entities also support custom fields added through Talent: Core HR.</span></span>

### <a name="powerbi-refresh-issues-314342"></a><span data-ttu-id="93989-119">PowerBI 刷新问题 (314342)</span><span class="sxs-lookup"><span data-stu-id="93989-119">PowerBI refresh issues (314342)</span></span>

<span data-ttu-id="93989-120">此项更改解决了 PowerBI 报告正确刷新的问题。</span><span class="sxs-lookup"><span data-stu-id="93989-120">This change corrects an issue with PowerBI reports refreshing correctly.</span></span>

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a><span data-ttu-id="93989-121">无法在员工自助服务中直接单击浏览转移任务 (303309)</span><span class="sxs-lookup"><span data-stu-id="93989-121">Unable to click directly through on transition tasks in employee self-service (303309)</span></span>

<span data-ttu-id="93989-122">此项更改让具有员工角色的用户可从 Talent 待办事宜列表中选择和更新转换任务。</span><span class="sxs-lookup"><span data-stu-id="93989-122">This change enables users with the employee role to select and update transition tasks from the Talent to-do list.</span></span>

### <a name="performance-feedback-email-message-updated-309615"></a><span data-ttu-id="93989-123">更新了性能反馈电子邮件消息 (309615)</span><span class="sxs-lookup"><span data-stu-id="93989-123">Performance feedback email message updated (309615)</span></span>

<span data-ttu-id="93989-124">在此版本中，成功提交反馈后，将显示确认消息。</span><span class="sxs-lookup"><span data-stu-id="93989-124">With this change, a confirmation message displays when feedback is successfully submitted.</span></span>

### <a name="missing-tables-in-word-template-308048"></a><span data-ttu-id="93989-125">Word 模板中缺少表 (308048)</span><span class="sxs-lookup"><span data-stu-id="93989-125">Missing tables in Word template (308048)</span></span>

<span data-ttu-id="93989-126">通过此更改，创建包含员工和技能信息的 Word 模板时，Word 文档中仅显示所选员工的技能。</span><span class="sxs-lookup"><span data-stu-id="93989-126">With this change, when creating a Word template with employee and skill information, only the skills for the selected employee appear in the Word document.</span></span>

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a><span data-ttu-id="93989-127">应用离职核对清单时显示错误。</span><span class="sxs-lookup"><span data-stu-id="93989-127">When applying an offboarding checklist an error is displayed.</span></span> <span data-ttu-id="93989-128">(299877)</span><span class="sxs-lookup"><span data-stu-id="93989-128">(299877)</span></span>

<span data-ttu-id="93989-129">此项更改解决了直接从工作人员表单应用离职核对清单时的问题。</span><span class="sxs-lookup"><span data-stu-id="93989-129">This change corrects an issue when applying an offboarding checklist directly from the worker form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="93989-130">预览模式</span><span class="sxs-lookup"><span data-stu-id="93989-130">In preview</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="93989-131">允许为休假类型指定原因代码</span><span class="sxs-lookup"><span data-stu-id="93989-131">Allow reason codes to be specified on leave types</span></span>

<span data-ttu-id="93989-132">组织可能需要有关休假请求的更多信息。</span><span class="sxs-lookup"><span data-stu-id="93989-132">Organizations might need additional information about time-off requests.</span></span> <span data-ttu-id="93989-133">现在可指定休假类型的原因代码，并让员工在休假请求中选择原因代码。</span><span class="sxs-lookup"><span data-stu-id="93989-133">You can now specify reason codes for leave types and enable employees to select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a><span data-ttu-id="93989-134">休假请求中的特定休假类型需要原因代码</span><span class="sxs-lookup"><span data-stu-id="93989-134">Require reason codes for certain leave types on time-off requests</span></span>

<span data-ttu-id="93989-135">组织可能会要求当员工提交请假时为特定休假类型设置原因代码。</span><span class="sxs-lookup"><span data-stu-id="93989-135">Organizations might require reason codes for specific leave types when employees submit time off.</span></span> <span data-ttu-id="93989-136">可能是因为公司政策或法规要求所致。</span><span class="sxs-lookup"><span data-stu-id="93989-136">This might be due to company policy or regulatory requirements.</span></span> <span data-ttu-id="93989-137">现在可以指定哪些休假类型需要原因代码，并且可以要求员工为自己的休假请求中的休假类型提供原因代码。</span><span class="sxs-lookup"><span data-stu-id="93989-137">You can now specify which leave types require a reason code, and you can require employees to provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="93989-138">为 HR 提供休假和缺勤交易记录列表</span><span class="sxs-lookup"><span data-stu-id="93989-138">Provide leave and absence transaction list for HR</span></span>

<span data-ttu-id="93989-139">跟踪员工休假和了解休假的计算方法不仅可以帮助 HR 解答员工的问题，还可以确保员工的休假奖励精确无误。</span><span class="sxs-lookup"><span data-stu-id="93989-139">Tracking employee time off and understanding how time off is calculated not only helps HR answer employee questions, but also ensures accurate time-off awards for employees.</span></span> <span data-ttu-id="93989-140">HR 现在可以以新的视觉查看交易记录（授权、应计、调整和请求），以查看余额背后的原因。</span><span class="sxs-lookup"><span data-stu-id="93989-140">HR now has a new view into the transactions (grants, accruals, adjustments, and requests) to see the reasons behind balances.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="93989-141">即将到期</span><span class="sxs-lookup"><span data-stu-id="93989-141">Coming soon</span></span>

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a><span data-ttu-id="93989-142">改进了用户界面中的重复员工检查</span><span class="sxs-lookup"><span data-stu-id="93989-142">Improvements to the user interface for duplicate employee check</span></span>

<span data-ttu-id="93989-143">借助此更改，输入名称字段时可检测重复项，而状态将显示找到的重复项数量。</span><span class="sxs-lookup"><span data-stu-id="93989-143">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="93989-144">您可以选择提供的链接以打开一个新的页面来评估是否要使用检测到的匹配项。</span><span class="sxs-lookup"><span data-stu-id="93989-144">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="93989-145">为了避免中断数据输入，重复项窗体不会自动打开。</span><span class="sxs-lookup"><span data-stu-id="93989-145">To avoid interrupting data entry, the duplicates form doesn't automatically open.</span></span>

### <a name="email-support-for-alerts"></a><span data-ttu-id="93989-146">警报的电子邮件支持</span><span class="sxs-lookup"><span data-stu-id="93989-146">Email support for alerts</span></span>

<span data-ttu-id="93989-147">安装 Finance and Operations 的平台更新 25 之后，用户可创建警报规则，用于在被事件触发后自动为联系人发送电子邮件通知。</span><span class="sxs-lookup"><span data-stu-id="93989-147">With Platform update 25 for Finance and Operations, users can create alert rules that automatically send email notifications to contacts when triggered by an event.</span></span>


