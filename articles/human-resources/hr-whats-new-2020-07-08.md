---
title: Dynamics 365 Human Resources 的新增功能或更改（2020 年 7 月 8 日）
description: 此主题介绍了 Microsoft Dynamics 365 Human Resources 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 07/08/2020
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
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c4382aa7473e2b67201ac00753ac9abe11b3c646
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614354"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="1e9c4-103">Dynamics 365 Human Resources 的新增功能或更改（2020 年 7 月 8 日）</span><span class="sxs-lookup"><span data-stu-id="1e9c4-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

<span data-ttu-id="1e9c4-104">此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="1e9c4-105">更改适用于内部版本号 8.1.3382。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="1e9c4-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="1e9c4-107">数据库记录</span><span class="sxs-lookup"><span data-stu-id="1e9c4-107">Database logging</span></span>

<span data-ttu-id="1e9c4-108">数据库日志记录功能让您可以确定要监视哪些表和字段。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="1e9c4-109">它还让您能够确定应该触发更改跟踪的事件。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="1e9c4-110">您可以使用数据库日志记录功能来查看一段时间内的更改。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="1e9c4-111">有关详细信息，请参阅[配置和管理数据库日志记录](hr-admin-database-logging.md)。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="1e9c4-112">配置员工自助服务的名称</span><span class="sxs-lookup"><span data-stu-id="1e9c4-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="1e9c4-113">现在，在 **Human Resources 参数**中，您可以将**员工自助服务**工作区的名称更改为**自助服务**。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="1e9c4-114">有关详细信息，请参阅[更改员工自助服务工作区名称](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="1e9c4-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="1e9c4-115">在期间之外访问福利管理开放登记</span><span class="sxs-lookup"><span data-stu-id="1e9c4-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="1e9c4-116">此版本修复了员工可以在登记期间之外或在没有生活事件的情况下访问福利开放登记的问题。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="1e9c4-117">因此，如果您需要在员工自助服务中演示开放登记，则必须将开放登记日期调整为今天（或更早）才能使用。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="1e9c4-118">您可以在**福利管理 > 规则和选项期间**下更改此设置。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="1e9c4-119">电子邮件员工登记确认</span><span class="sxs-lookup"><span data-stu-id="1e9c4-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="1e9c4-120">您现在可以在员工完成福利选择后向他们发送电子邮件。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="1e9c4-121">您可以发送默认消息，也可以使用组织电子邮件模板。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="1e9c4-122">这些设置在 **Human resource 参数 > 福利管理**下。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="1e9c4-123">已取消的休假仍然会在“人员”工作区上即将发生的休假中显示 (441358)</span><span class="sxs-lookup"><span data-stu-id="1e9c4-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="1e9c4-124">已取消休假不会再在**人员**工作区中的休假卡上显示为即将发生的休假。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="1e9c4-125">无法在 PositionV2 实体中使用部门实体属性 (456486)</span><span class="sxs-lookup"><span data-stu-id="1e9c4-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="1e9c4-126">现在，您可以添加部门而无需创建重复关系。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="1e9c4-127">PayrollWorkerEnrolledBenefitDetailEntity 应该仅将计算字段用于退休计划 (459779)</span><span class="sxs-lookup"><span data-stu-id="1e9c4-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="1e9c4-128">导出 **PayrollWorkerEnrolledBenefitDetailEntity** 实体时，导出确定应使用基于比率表的计算字段还是使用后备表上的 **ContributionAmountCur** 字段。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="1e9c4-129">数据实体使用的逻辑在应用程序通常不使用的情况下使用比率表。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="1e9c4-130">此逻辑导致实体导出以为此列返回零值，因为没有计算比率表并且产品不允许客户指定比率表。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="1e9c4-131">“人事管理”和“员工自助服务”中的捷克语翻译难以理解 (400276)</span><span class="sxs-lookup"><span data-stu-id="1e9c4-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="1e9c4-132">此版本更正了**公司目录**、**下一个注册的课程**、**工作**和**职位**的翻译。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="1e9c4-133">WorkCalendarEmployment 表未启用创建和修改的系统字段 (460171)</span><span class="sxs-lookup"><span data-stu-id="1e9c4-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="1e9c4-134">现在，在 Human Resources 中的 **WorkCalendarEmployment** 表中已启用创建和修改的系统字段。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="1e9c4-135">用于未来员工的“雇用并添加详细信息”的空引用异常 (455475)</span><span class="sxs-lookup"><span data-stu-id="1e9c4-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="1e9c4-136">此版本更正了当您使用**雇用并添加详细信息**选项雇用员工时，简化的员工输入中出现的错误（空引用）。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="1e9c4-137">Common Data Service“工作人员”实体中所作的更改不反映在 Human Resources 中 (455652)</span><span class="sxs-lookup"><span data-stu-id="1e9c4-137">Changes made in the Common Data Service Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="1e9c4-138">现在，在 Common Data Service 中对**工作人员**实体中的以下字段进行的更改将显示在 Human Resources 中：</span><span class="sxs-lookup"><span data-stu-id="1e9c4-138">Changes made to the following fields in the **Worker** entity in Common Data Service will now show up in Human Resources:</span></span>

- <span data-ttu-id="1e9c4-139">**在家办公**</span><span class="sxs-lookup"><span data-stu-id="1e9c4-139">**Works from home**</span></span>
- <span data-ttu-id="1e9c4-140">**受聘日期**</span><span class="sxs-lookup"><span data-stu-id="1e9c4-140">**Seniority date**</span></span>
- <span data-ttu-id="1e9c4-141">**周年纪念日日期**</span><span class="sxs-lookup"><span data-stu-id="1e9c4-141">**Anniversary date**</span></span>
- <span data-ttu-id="1e9c4-142">**原始雇用日期**</span><span class="sxs-lookup"><span data-stu-id="1e9c4-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="1e9c4-143">不能根据分配给职位的工作默认显示正确的薪酬级别 (394136)</span><span class="sxs-lookup"><span data-stu-id="1e9c4-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="1e9c4-144">进行此更改后，将根据**薪酬计划分配**的**职位详细信息**和**开始日期**的**生效日期**记录，默认显示正确的薪酬级别。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="1e9c4-145">预览模式</span><span class="sxs-lookup"><span data-stu-id="1e9c4-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="1e9c4-146">必填字段</span><span class="sxs-lookup"><span data-stu-id="1e9c4-146">Mandatory fields</span></span> 

<span data-ttu-id="1e9c4-147">现在可使用 Human Resources 个性化功能将字段设置为必填字段。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="1e9c4-148">此功能需要**保存的视图**。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="1e9c4-149">Teams 中的 Human Resources 应用程序</span><span class="sxs-lookup"><span data-stu-id="1e9c4-149">Human Resources application in Teams</span></span>

<span data-ttu-id="1e9c4-150">员工可以在 Microsoft Teams 中查看和请求离岗时间。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="1e9c4-151">他们可以与机器人交互来创建休假请求。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="1e9c4-152">有关详细信息，请参阅 [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="1e9c4-153">用于福利管理的数据管理框架 (DMF) 实体</span><span class="sxs-lookup"><span data-stu-id="1e9c4-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="1e9c4-154">福利管理实体即将发布。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="1e9c4-155">DMF 实体允许导入和导出数据，以轻松配置福利管理。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="1e9c4-156">福利管理模板可用于移动数据。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="1e9c4-157">模板按顺序导出和导入数据，以保持数据依赖关系。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="1e9c4-158">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="1e9c4-158">Buy and sell leave</span></span> 

<span data-ttu-id="1e9c4-159">一些组织提供允许员工购买和出售其休假的福利。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="1e9c4-160">此流程通常通过手动管理。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-160">This process is often managed manually.</span></span> <span data-ttu-id="1e9c4-161">此功能可自动管理人力资源部门的策略和请求。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="1e9c4-162">它将简化休假管理流程，并帮助消除错误。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="1e9c4-163">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="1e9c4-163">For more information, see:</span></span>

- [<span data-ttu-id="1e9c4-164">管理购买和出售休假策略</span><span class="sxs-lookup"><span data-stu-id="1e9c4-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="1e9c4-165">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="1e9c4-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="1e9c4-166">单个公司或单个计划的休假假期额度</span><span class="sxs-lookup"><span data-stu-id="1e9c4-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="1e9c4-167">客户可以处理单个公司或单个休假和缺勤计划的应计项目。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="1e9c4-168">此功能为具有不同休假年限或休假应计政策的客户提供清晰的应计流程。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="1e9c4-169">有关详细信息，请参阅[按公司或按休假计划累积休假](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan)。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="1e9c4-170">将附件添加到休假请求</span><span class="sxs-lookup"><span data-stu-id="1e9c4-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="1e9c4-171">在当前的 COVID-19 环境中，向批准的休假请求添加附件的功能至关重要。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="1e9c4-172">员工现在可以添加这些附件。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-172">Employees can now add these attachments.</span></span> <span data-ttu-id="1e9c4-173">他们还将对休假请求进行了怎样的更新有更多了解。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="1e9c4-174">有关详细信息，请参阅[将附件添加到现有请求](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="1e9c4-175">将原因代码添加到应计暂停</span><span class="sxs-lookup"><span data-stu-id="1e9c4-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="1e9c4-176">原因代码已添加到应计暂停。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="1e9c4-177">结转规则</span><span class="sxs-lookup"><span data-stu-id="1e9c4-177">Carry forward rules</span></span> 

<span data-ttu-id="1e9c4-178">可为转移了结转调整的结转余额指定结转休假类型。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="1e9c4-179">例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="1e9c4-180">有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="1e9c4-181">暂停指定休假类型的休假应计</span><span class="sxs-lookup"><span data-stu-id="1e9c4-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="1e9c4-182">您可以创建一个规则，以针对输入了无薪假休假请求的员工暂停休假应计。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="1e9c4-183">无薪假可以是一种类型，但不是必须的。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="1e9c4-184">您可以根据其他休假类型暂停任何休假。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="1e9c4-185">可用于暂停应计的 DMF 实体</span><span class="sxs-lookup"><span data-stu-id="1e9c4-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="1e9c4-186">DMF 实体现在可用于暂停应计。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="1e9c4-187">即将到期</span><span class="sxs-lookup"><span data-stu-id="1e9c4-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="1e9c4-188">Common Data Service 中包含的核对清单实体</span><span class="sxs-lookup"><span data-stu-id="1e9c4-188">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="1e9c4-189">Common Data Service 内很快将为入职、离职、转移和业务流程提供核对清单实体。</span><span class="sxs-lookup"><span data-stu-id="1e9c4-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e9c4-190">请参阅</span><span class="sxs-lookup"><span data-stu-id="1e9c4-190">See also</span></span>

[<span data-ttu-id="1e9c4-191">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="1e9c4-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="1e9c4-192">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="1e9c4-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="1e9c4-193">更新流程</span><span class="sxs-lookup"><span data-stu-id="1e9c4-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="1e9c4-194">管理功能</span><span class="sxs-lookup"><span data-stu-id="1e9c4-194">Manage features</span></span>](hr-admin-manage-features.md)
