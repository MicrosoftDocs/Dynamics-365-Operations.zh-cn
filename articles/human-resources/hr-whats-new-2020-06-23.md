---
title: Dynamics 365 Human Resources（2020 年 6 月 25 日）新增功能或更改
description: 此主题介绍了 2020 年 6 月 23 日 Microsoft Dynamics 365 Human Resources - Core HR 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9787df5f36c1f08ade40e3e8fc5d5189e3bd5b0
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711932"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="5f6a2-103">Dynamics 365 Human Resources（2020 年 6 月 23 日）新增功能或更改</span><span class="sxs-lookup"><span data-stu-id="5f6a2-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

<span data-ttu-id="5f6a2-104">此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5f6a2-105">更改适用于内部版本号 8.1.3347。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="5f6a2-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="5f6a2-107">当已离职员工的等记到期时，将彻底清除休假等记表中的休假类型、余额和数量 (444867)</span><span class="sxs-lookup"><span data-stu-id="5f6a2-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="5f6a2-108">现在在进行此项选择之后，将保留**休假类型**、**余额**和**数量**中的值，而不是清除。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="5f6a2-109">启用了新功能（单个公司或单个计划的休假应计）时，预测余额不正确 (456553)</span><span class="sxs-lookup"><span data-stu-id="5f6a2-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="5f6a2-110">已经启用了单个公司或单个计划的休假应计时，现在显示正确的预测余额。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="5f6a2-111">多个实体具有将导致重复导航属性的关系 (456486)</span><span class="sxs-lookup"><span data-stu-id="5f6a2-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="5f6a2-112">此版本解决了多个实体的导航属性（关系）问题。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="5f6a2-113">可以检测到重复关系。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-113">Duplicate relations are detected.</span></span> <span data-ttu-id="5f6a2-114">这些情况都已得到纠正。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="5f6a2-115">审查性能时的跨公司注释 (455536)</span><span class="sxs-lookup"><span data-stu-id="5f6a2-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="5f6a2-116">安装此修补程序之后，性能审查时会显示跨公司注释。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="5f6a2-117">此更改更正了审查者在不同公司为同一项性能审查输入的注释的视图。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="5f6a2-118">薪酬管理数据显示不一致 (432562)</span><span class="sxs-lookup"><span data-stu-id="5f6a2-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="5f6a2-119">现在经理自助服务中薪酬数据的视图保持一致。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="5f6a2-120">薪酬数据现在可以按照您导航到工作人员**薪酬详细信息**的方式一致地对经理显示。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="5f6a2-121">固定薪酬计划的生效日期默认为当天日期 (411994)</span><span class="sxs-lookup"><span data-stu-id="5f6a2-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="5f6a2-122">薪酬开始日期现在基于为员工分配的职位的开始日期。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="5f6a2-123">休假和缺勤窗体打开时禁用该窗体的“启用半天定义” (452607)</span><span class="sxs-lookup"><span data-stu-id="5f6a2-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="5f6a2-124">进行此更改之后，将启用**启用半天定义**，直到出现新的休假事务。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="5f6a2-125">无法通过 Excel 发布到 HcmDiscussionEntity；TotalRatingScore 字段错误 (453899)</span><span class="sxs-lookup"><span data-stu-id="5f6a2-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="5f6a2-126">现在可在 Excel 工作簿设计器中使用 **HCMDiscussionEntity** 更新 **TotalRatingScore** 字段。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="5f6a2-127">预览模式</span><span class="sxs-lookup"><span data-stu-id="5f6a2-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="5f6a2-128">数据库记录</span><span class="sxs-lookup"><span data-stu-id="5f6a2-128">Database logging</span></span>

<span data-ttu-id="5f6a2-129">数据库日志记录功能让您可以确定要监视哪些表和字段。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="5f6a2-130">它还让您能够确定应该触发更改跟踪的事件。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="5f6a2-131">您可以使用数据库日志记录功能来查看一段时间内的更改。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="5f6a2-132">有关详细信息，请参阅[配置和管理数据库日志记录](hr-admin-database-logging.md)。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="5f6a2-133">必填字段</span><span class="sxs-lookup"><span data-stu-id="5f6a2-133">Mandatory fields</span></span> 

<span data-ttu-id="5f6a2-134">现在可使用 Human Resources 个性化功能将字段设置为必填字段。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="5f6a2-135">此功能需要**保存的视图**。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="5f6a2-136">Teams 中的 Human Resources 应用程序</span><span class="sxs-lookup"><span data-stu-id="5f6a2-136">Human Resources application in Teams</span></span>

<span data-ttu-id="5f6a2-137">员工可以在 Microsoft Teams 中查看和请求离岗时间。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="5f6a2-138">他们可以与机器人交互来创建休假请求。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="5f6a2-139">有关详细信息，请参阅 [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="5f6a2-140">用于福利管理的数据管理框架 (DMF) 实体</span><span class="sxs-lookup"><span data-stu-id="5f6a2-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="5f6a2-141">福利管理实体即将发布。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="5f6a2-142">DMF 实体允许导入和导出数据，以轻松配置福利管理。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="5f6a2-143">福利管理模板可用于移动数据。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="5f6a2-144">模板按顺序导出和导入数据，以保持数据依赖关系。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="5f6a2-145">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="5f6a2-145">Buy and sell leave</span></span> 

<span data-ttu-id="5f6a2-146">一些组织提供允许员工购买和出售其休假的福利。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="5f6a2-147">此流程通常通过手动管理。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-147">This process is often managed manually.</span></span> <span data-ttu-id="5f6a2-148">此功能可自动管理人力资源部门的策略和请求。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="5f6a2-149">它将简化休假管理流程，并帮助消除错误。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="5f6a2-150">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="5f6a2-150">For more information, see:</span></span>

- [<span data-ttu-id="5f6a2-151">管理购买和出售休假策略</span><span class="sxs-lookup"><span data-stu-id="5f6a2-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="5f6a2-152">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="5f6a2-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="5f6a2-153">单个公司或单个计划的休假假期额度</span><span class="sxs-lookup"><span data-stu-id="5f6a2-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="5f6a2-154">客户可以处理单个公司或单个休假和缺勤计划的应计项目。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="5f6a2-155">此功能为具有不同休假年限或休假应计政策的客户提供清晰的应计流程。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="5f6a2-156">有关详细信息，请参阅[按公司或按休假计划累积休假](hr-leave-and-absence-accrue.md)。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="5f6a2-157">将附件添加到休假请求</span><span class="sxs-lookup"><span data-stu-id="5f6a2-157">Add attachments to time off requests</span></span>

<span data-ttu-id="5f6a2-158">在当前的 COVID-19 环境中，向批准的休假请求添加附件的功能至关重要。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="5f6a2-159">员工现在可以添加这些附件。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-159">Employees can now add these attachments.</span></span> <span data-ttu-id="5f6a2-160">他们还将对休假请求进行了怎样的更新有更多了解。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="5f6a2-161">有关详细信息，请参阅[将附件添加到现有请求](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="5f6a2-162">将原因代码添加到应计暂停</span><span class="sxs-lookup"><span data-stu-id="5f6a2-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="5f6a2-163">原因代码已添加到应计暂停。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="5f6a2-164">结转规则</span><span class="sxs-lookup"><span data-stu-id="5f6a2-164">Carry forward rules</span></span> 

<span data-ttu-id="5f6a2-165">可为转移了结转调整的结转余额指定结转休假类型。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="5f6a2-166">例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="5f6a2-167">有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="5f6a2-168">暂停指定休假类型的休假应计</span><span class="sxs-lookup"><span data-stu-id="5f6a2-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="5f6a2-169">您可以创建一个规则，以针对输入了无薪假休假请求的员工暂停休假应计。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="5f6a2-170">无薪假可以是一种类型，但不是必须的。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="5f6a2-171">您可以根据其他休假类型暂停任何休假。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="5f6a2-172">可用于暂停应计的 DMF 实体</span><span class="sxs-lookup"><span data-stu-id="5f6a2-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="5f6a2-173">DMF 实体现在可用于暂停应计。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="5f6a2-174">即将到期</span><span class="sxs-lookup"><span data-stu-id="5f6a2-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="5f6a2-175">配置员工自助服务的名称</span><span class="sxs-lookup"><span data-stu-id="5f6a2-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="5f6a2-176">**人力资源参数**中将提供一个新选项，可以将“员工自助服务”工作区的名称更新为“自助服务”。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="5f6a2-177">Common Data Service 中包含的核对清单实体</span><span class="sxs-lookup"><span data-stu-id="5f6a2-177">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="5f6a2-178">Common Data Service 内很快将为入职、离职、转移和业务流程提供核对清单实体。</span><span class="sxs-lookup"><span data-stu-id="5f6a2-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f6a2-179">请参阅</span><span class="sxs-lookup"><span data-stu-id="5f6a2-179">See also</span></span>

[<span data-ttu-id="5f6a2-180">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="5f6a2-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="5f6a2-181">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="5f6a2-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="5f6a2-182">更新流程</span><span class="sxs-lookup"><span data-stu-id="5f6a2-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="5f6a2-183">管理功能</span><span class="sxs-lookup"><span data-stu-id="5f6a2-183">Manage features</span></span>](hr-admin-manage-features.md)