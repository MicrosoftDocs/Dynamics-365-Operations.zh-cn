---
title: Dynamics 365 for Talent Core HR（2018 年 12 月 14 日）中的新增功能或更改
description: 此主题介绍了 Microsoft Dynamics 365 for Talent Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
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
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/12/2019
ms.locfileid: "949843"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="3f629-103">Dynamics 365 for Talent Core HR（2018 年 12 月 14 日）中的新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="3f629-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f629-104">**内部版本 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="3f629-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="3f629-105">此主题介绍了 Core HR 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="3f629-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="3f629-106">更改</span><span class="sxs-lookup"><span data-stu-id="3f629-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="3f629-107">美国 - 纳税年度 2018 1095-B 和 1095-C 窗体的 ACA（平价医疗法案）支持</span><span class="sxs-lookup"><span data-stu-id="3f629-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="3f629-108">每年，适用大型雇主 (ALE) 必须为每位全职员工提供 1095-C。</span><span class="sxs-lookup"><span data-stu-id="3f629-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="3f629-109">此外，如果雇主提供自保型保险，他们还必须根据所提供的健康计划向任何员工提供 1095-C（如果是 ALE）和 1095-B（如果是小型雇主）。</span><span class="sxs-lookup"><span data-stu-id="3f629-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="3f629-110">此功能同时为 1095-C 和 1095-B 提供可打印表单。</span><span class="sxs-lookup"><span data-stu-id="3f629-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="3f629-111">在导入期间，将忽略 HcmPerfJournalEntity 上的 SubmittedByPersonId 字段</span><span class="sxs-lookup"><span data-stu-id="3f629-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="3f629-112">在导入/导出绩效日记帐条目时，**提交者**字段会被忽略。</span><span class="sxs-lookup"><span data-stu-id="3f629-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="3f629-113">通过此更改，值**已导入/已导出**将在导出时在表中反映此值，在导入时，系统将更新为导入文件中提供的值。</span><span class="sxs-lookup"><span data-stu-id="3f629-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="3f629-114">“休假和缺勤”工作区的“分析”选项卡显示非系统管理员角色的“OpenConnectionError”错误</span><span class="sxs-lookup"><span data-stu-id="3f629-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="3f629-115">通过此更新，在打开**休假和缺勤**工作区的**分析**选项卡时，不会发出错误。</span><span class="sxs-lookup"><span data-stu-id="3f629-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="3f629-116">从磁贴深化的员工自助服务“职位层次结构”无法获取父节点</span><span class="sxs-lookup"><span data-stu-id="3f629-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="3f629-117">已进行更改来更正当职位层次结构进行个性化设置以显示在现有工作区中并且在层次结构中选择了一个职位时出现的错误“获取父节点失败”。</span><span class="sxs-lookup"><span data-stu-id="3f629-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="3f629-118">必须是系统管理员才能够看到职位页面的“工资单”选项卡</span><span class="sxs-lookup"><span data-stu-id="3f629-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="3f629-119">已进行了更改以在现有权限中包含正确的安全元素：“维护工资单工作人员和职位详细信息”。</span><span class="sxs-lookup"><span data-stu-id="3f629-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="3f629-120">通过此更改，默认情况下，工资管理员将有权访问“职位”页面的“工资单”字段。</span><span class="sxs-lookup"><span data-stu-id="3f629-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="3f629-121">在向经理提交绩效审核并在提交说明中使用 %Reviews.PerfPeriod% 占位符时出错</span><span class="sxs-lookup"><span data-stu-id="3f629-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="3f629-122">已进行更改以更正在提交说明中使用 %Reviews.PerfPeriod% 占位符时出现的“空引用”错误。</span><span class="sxs-lookup"><span data-stu-id="3f629-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="3f629-123">当工作人员受聘日期是闰日时劳动力 Power BI 报表显示错误</span><span class="sxs-lookup"><span data-stu-id="3f629-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="3f629-124">通过此更改，闰日现在在 Power BI 中受支持。</span><span class="sxs-lookup"><span data-stu-id="3f629-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="3f629-125">Core HR 与 Attract 之间的集成</span><span class="sxs-lookup"><span data-stu-id="3f629-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="3f629-126">已进行了更改以更新与要雇用的应聘者相关的 Core HR 与 Attract 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="3f629-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="3f629-127">要使将要雇用的应聘者可以显示在**人员管理**工作区中，使用以下 Common Data Service 实体：</span><span class="sxs-lookup"><span data-stu-id="3f629-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="3f629-128">工作申请</span><span class="sxs-lookup"><span data-stu-id="3f629-128">Job Application</span></span>
- <span data-ttu-id="3f629-129">状态描述需要设置为“已接受聘约”</span><span class="sxs-lookup"><span data-stu-id="3f629-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="3f629-130">提供应聘者和空缺职位</span><span class="sxs-lookup"><span data-stu-id="3f629-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="3f629-131">应聘者</span><span class="sxs-lookup"><span data-stu-id="3f629-131">Candidate</span></span>
-   <span data-ttu-id="3f629-132">提供应聘者信息</span><span class="sxs-lookup"><span data-stu-id="3f629-132">Provides Candidate information</span></span>

<span data-ttu-id="3f629-133">空缺职位</span><span class="sxs-lookup"><span data-stu-id="3f629-133">Job Opening</span></span>
-   <span data-ttu-id="3f629-134">提供空缺职位 ID 和空缺职位参与者</span><span class="sxs-lookup"><span data-stu-id="3f629-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="3f629-135">空缺职位参与者</span><span class="sxs-lookup"><span data-stu-id="3f629-135">Job Opening Participants</span></span>
-   <span data-ttu-id="3f629-136">提供招聘经理</span><span class="sxs-lookup"><span data-stu-id="3f629-136">Provides Hiring Manager</span></span>

<span data-ttu-id="3f629-137">在将应聘者添加到“人员管理”时，应聘者现在还可以使用应聘者卡上的新选项消除。</span><span class="sxs-lookup"><span data-stu-id="3f629-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="3f629-138">即将到期</span><span class="sxs-lookup"><span data-stu-id="3f629-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="3f629-139">休假和缺勤：将来的休假和预测的休假余额</span><span class="sxs-lookup"><span data-stu-id="3f629-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="3f629-140">随着对允许员工预测休假和申请将来休假请求，而不会影响其当前休假余额的更改，显示休假余额的方式也在更改。</span><span class="sxs-lookup"><span data-stu-id="3f629-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="3f629-141">当前显示的可用余额是包括截至今天的应计在内的可以请求的时间量，以及时间结束前的所有批准的休假请求。</span><span class="sxs-lookup"><span data-stu-id="3f629-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="3f629-142">在预测功能发布时，显示的余额将更改为包括截至今天的应计和请求在内的当前休假余额。</span><span class="sxs-lookup"><span data-stu-id="3f629-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="3f629-143">员工和经理将在**休假**卡和**休假余额**窗口中的员工和经理自助服务中看到这些更新的余额。</span><span class="sxs-lookup"><span data-stu-id="3f629-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="3f629-144">HR 经理将在**人员**工作区和员工的**指定休假计划**窗口中看到这些更新的余额。</span><span class="sxs-lookup"><span data-stu-id="3f629-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="3f629-145">已知问题</span><span class="sxs-lookup"><span data-stu-id="3f629-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="3f629-146">Finance and Operations 集成中的映射错误</span><span class="sxs-lookup"><span data-stu-id="3f629-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="3f629-147">以下问题已在用于将 Talent 与 Dynamics 365 for Finance and Operations 集成的当前模板中发现。</span><span class="sxs-lookup"><span data-stu-id="3f629-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="3f629-148">新模板将很快发布并应用到创建的所有新集成项目中。</span><span class="sxs-lookup"><span data-stu-id="3f629-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="3f629-149">对于现有的集成项目，可以更新任务映射。</span><span class="sxs-lookup"><span data-stu-id="3f629-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="3f629-150">请参阅下表了解更新的映射。</span><span class="sxs-lookup"><span data-stu-id="3f629-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="3f629-151">“职位到职位父作业分配”任务不集成数据。</span><span class="sxs-lookup"><span data-stu-id="3f629-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="3f629-152">这是当前正在研究的问题。</span><span class="sxs-lookup"><span data-stu-id="3f629-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="3f629-153">当前映射没有解决方法。</span><span class="sxs-lookup"><span data-stu-id="3f629-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="3f629-154">“部门到运营单位”任务需要更新以下映射。</span><span class="sxs-lookup"><span data-stu-id="3f629-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="3f629-155">现有源字段</span><span class="sxs-lookup"><span data-stu-id="3f629-155">Existing source field</span></span>          | <span data-ttu-id="3f629-156">新源字段</span><span class="sxs-lookup"><span data-stu-id="3f629-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="3f629-157">cdm_description（描述）</span><span class="sxs-lookup"><span data-stu-id="3f629-157">cdm_description (Description)</span></span>  | <span data-ttu-id="3f629-158">cdm_name（名称）</span><span class="sxs-lookup"><span data-stu-id="3f629-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="3f629-159">还需要添加其他映射。</span><span class="sxs-lookup"><span data-stu-id="3f629-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="3f629-160">选择上一个**无**字段添加以下映射。</span><span class="sxs-lookup"><span data-stu-id="3f629-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="3f629-161">源字段</span><span class="sxs-lookup"><span data-stu-id="3f629-161">Source field</span></span>                   | <span data-ttu-id="3f629-162">目标字段</span><span class="sxs-lookup"><span data-stu-id="3f629-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="3f629-163">cdm_description（描述）</span><span class="sxs-lookup"><span data-stu-id="3f629-163">cdm_description (Description)</span></span>  | <span data-ttu-id="3f629-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="3f629-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="3f629-165">更新的映射应如以下图像所示。</span><span class="sxs-lookup"><span data-stu-id="3f629-165">The updated mappings should look like the following image.</span></span>

![“部门到运营单位”任务](./media/DepartmentMapping.png)


<span data-ttu-id="3f629-167">“作业到作业详细信息”任务需要更新以下映射。</span><span class="sxs-lookup"><span data-stu-id="3f629-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="3f629-168">现有源字段</span><span class="sxs-lookup"><span data-stu-id="3f629-168">Existing source field</span></span>          | <span data-ttu-id="3f629-169">新源字段</span><span class="sxs-lookup"><span data-stu-id="3f629-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="3f629-170">cdm_name（名称）</span><span class="sxs-lookup"><span data-stu-id="3f629-170">cdm_name (Name)</span></span>                | <span data-ttu-id="3f629-171">cdm_description（描述）</span><span class="sxs-lookup"><span data-stu-id="3f629-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="3f629-172">cdm_name（描述）</span><span class="sxs-lookup"><span data-stu-id="3f629-172">cdm_name (Description)</span></span>         | <span data-ttu-id="3f629-173">cdm_jobdescription（作业描述）</span><span class="sxs-lookup"><span data-stu-id="3f629-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="3f629-174">更新的映射应如下方图像所示。</span><span class="sxs-lookup"><span data-stu-id="3f629-174">The updated mappings should look like the image below.</span></span>

![“作业到作业详细信息”任务](./media/JobMapping.png)

<span data-ttu-id="3f629-176">“工作人员到工作”任务需要更新以下映射。</span><span class="sxs-lookup"><span data-stu-id="3f629-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="3f629-177">现有源字段</span><span class="sxs-lookup"><span data-stu-id="3f629-177">Existing source field</span></span>                 | <span data-ttu-id="3f629-178">新源字段</span><span class="sxs-lookup"><span data-stu-id="3f629-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="3f629-179">cdm_emailaddress1（电子邮件地址 1）</span><span class="sxs-lookup"><span data-stu-id="3f629-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="3f629-180">cdm_primaryemailaddress（主要电子邮件地址</span><span class="sxs-lookup"><span data-stu-id="3f629-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="3f629-181">cdm_telephone1（电话 1）</span><span class="sxs-lookup"><span data-stu-id="3f629-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="3f629-182">cdm_primarytelephone（主电话）</span><span class="sxs-lookup"><span data-stu-id="3f629-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="3f629-183">“性别”字段转换也需要更新。</span><span class="sxs-lookup"><span data-stu-id="3f629-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="3f629-184">为“性别”选择 **fn**（功能）映射类型并更新以下值映射。</span><span class="sxs-lookup"><span data-stu-id="3f629-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="3f629-185">Common Data Service 值</span><span class="sxs-lookup"><span data-stu-id="3f629-185">Common Data Service value</span></span>                   | <span data-ttu-id="3f629-186">Finance and Operations 值</span><span class="sxs-lookup"><span data-stu-id="3f629-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="3f629-187">75440000</span><span class="sxs-lookup"><span data-stu-id="3f629-187">75440000</span></span>                    | <span data-ttu-id="3f629-188">男</span><span class="sxs-lookup"><span data-stu-id="3f629-188">Male</span></span>                                             |
| <span data-ttu-id="3f629-189">75440001</span><span class="sxs-lookup"><span data-stu-id="3f629-189">75440001</span></span>                    | <span data-ttu-id="3f629-190">女</span><span class="sxs-lookup"><span data-stu-id="3f629-190">Female</span></span>                                           |
| <span data-ttu-id="3f629-191">75440002</span><span class="sxs-lookup"><span data-stu-id="3f629-191">75440002</span></span>                    | <span data-ttu-id="3f629-192">无</span><span class="sxs-lookup"><span data-stu-id="3f629-192">None</span></span>                                             | 
| <span data-ttu-id="3f629-193">75440003</span><span class="sxs-lookup"><span data-stu-id="3f629-193">75440003</span></span>                    | <span data-ttu-id="3f629-194">非特定</span><span class="sxs-lookup"><span data-stu-id="3f629-194">NonSpecific</span></span>                                      |

<span data-ttu-id="3f629-195">更新的映射应如以下图像所示。</span><span class="sxs-lookup"><span data-stu-id="3f629-195">The updated mappings should look like the following images.</span></span>

![“工作人员到工作人员”任务](./media/WorkerMapping.png)

![“性别”字段转换](./media/WorkerTransform.png)
