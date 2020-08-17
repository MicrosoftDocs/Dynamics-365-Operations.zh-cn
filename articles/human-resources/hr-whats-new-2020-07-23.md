---
title: Dynamics 365 Human Resources 的新增功能或更改（2020 年 7 月 23 日）
description: 此主题介绍了 Microsoft Dynamics 365 Human Resources 中的新增功能和更改的功能。
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
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
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dd71ab5c48be1bec5ce2272bbff37ab10a4aed67
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614402"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="0be05-103">Dynamics 365 Human Resources 的新增功能或更改（2020 年 7 月 23 日）</span><span class="sxs-lookup"><span data-stu-id="0be05-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

<span data-ttu-id="0be05-104">此主题介绍了 Dynamics 365 Human Resources 中的新增功能和更改的功能。</span><span class="sxs-lookup"><span data-stu-id="0be05-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0be05-105">更改适用于内部版本号 8.1.3416。</span><span class="sxs-lookup"><span data-stu-id="0be05-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="0be05-106">某些标题中括号内的数字是 LCS 支持号码，供您参考。</span><span class="sxs-lookup"><span data-stu-id="0be05-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="0be05-107">在位置上删除财务维度不能按预期进行 (445476)</span><span class="sxs-lookup"><span data-stu-id="0be05-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="0be05-108">现在，从某个位置删除维度会从 Common Data Service 中删除这些相同的位置。</span><span class="sxs-lookup"><span data-stu-id="0be05-108">Removing dimensions from a position now removes those same positions from Common Data Service.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="0be05-109">不在层次结构中的位置显示无效职位 (397257)</span><span class="sxs-lookup"><span data-stu-id="0be05-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="0be05-110">无效的位置（持续时间已过）将不再在位置层次结构中显示为**不在层次结构中的位置**。</span><span class="sxs-lookup"><span data-stu-id="0be05-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="0be05-111">在数据管理框架 (DMF) 导入时在 LeaveEnrollmentEntity 和 HcmWorkerEntity 之间进行的验证导致数据加载缓慢 (442324)</span><span class="sxs-lookup"><span data-stu-id="0be05-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="0be05-112">此版本中的更改提高了 **LeaveEnrollmentEntity** 的性能。</span><span class="sxs-lookup"><span data-stu-id="0be05-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="0be05-113">无法在“组织管理”中个性化 (447490)</span><span class="sxs-lookup"><span data-stu-id="0be05-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="0be05-114">进行此更改后，您现在可以在**组织管理**中个性化链接。</span><span class="sxs-lookup"><span data-stu-id="0be05-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="0be05-115">预览模式</span><span class="sxs-lookup"><span data-stu-id="0be05-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="0be05-116">必填字段</span><span class="sxs-lookup"><span data-stu-id="0be05-116">Mandatory fields</span></span> 

<span data-ttu-id="0be05-117">现在可使用 Human Resources 个性化功能将字段设置为必填字段。</span><span class="sxs-lookup"><span data-stu-id="0be05-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="0be05-118">此功能需要**保存的视图**。</span><span class="sxs-lookup"><span data-stu-id="0be05-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="0be05-119">Teams 中的 Human Resources 应用程序</span><span class="sxs-lookup"><span data-stu-id="0be05-119">Human Resources application in Teams</span></span>

<span data-ttu-id="0be05-120">员工可以在 Microsoft Teams 中查看和请求离岗时间。</span><span class="sxs-lookup"><span data-stu-id="0be05-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="0be05-121">他们可以与机器人交互来创建休假请求。</span><span class="sxs-lookup"><span data-stu-id="0be05-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="0be05-122">有关详细信息，请参阅 [Teams 中的 Human Resources 应用](https://go.microsoft.com/fwlink/?linkid=2127841)。</span><span class="sxs-lookup"><span data-stu-id="0be05-122">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="0be05-123">用于福利管理的数据管理框架 (DMF) 实体</span><span class="sxs-lookup"><span data-stu-id="0be05-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="0be05-124">福利管理实体即将发布。</span><span class="sxs-lookup"><span data-stu-id="0be05-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="0be05-125">DMF 实体允许导入和导出数据，以轻松配置福利管理。</span><span class="sxs-lookup"><span data-stu-id="0be05-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="0be05-126">福利管理模板可用于移动数据。</span><span class="sxs-lookup"><span data-stu-id="0be05-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="0be05-127">模板按顺序导出和导入数据，以保持数据依赖关系。</span><span class="sxs-lookup"><span data-stu-id="0be05-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="0be05-128">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="0be05-128">Buy and sell leave</span></span> 

<span data-ttu-id="0be05-129">一些组织提供允许员工购买和出售其休假的福利。</span><span class="sxs-lookup"><span data-stu-id="0be05-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="0be05-130">此流程通常通过手动管理。</span><span class="sxs-lookup"><span data-stu-id="0be05-130">This process is often managed manually.</span></span> <span data-ttu-id="0be05-131">此功能可自动管理人力资源部门的策略和请求。</span><span class="sxs-lookup"><span data-stu-id="0be05-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="0be05-132">它将简化休假管理流程，并帮助消除错误。</span><span class="sxs-lookup"><span data-stu-id="0be05-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="0be05-133">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="0be05-133">For more information, see:</span></span>

- [<span data-ttu-id="0be05-134">管理购买和出售休假策略</span><span class="sxs-lookup"><span data-stu-id="0be05-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="0be05-135">购买和出售休假</span><span class="sxs-lookup"><span data-stu-id="0be05-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="0be05-136">单个公司或单个计划的休假假期额度</span><span class="sxs-lookup"><span data-stu-id="0be05-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="0be05-137">客户可以处理单个公司或单个休假和缺勤计划的应计项目。</span><span class="sxs-lookup"><span data-stu-id="0be05-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="0be05-138">此功能为具有不同休假年限或休假应计政策的客户提供清晰的应计流程。</span><span class="sxs-lookup"><span data-stu-id="0be05-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="0be05-139">有关详细信息，请参阅[按公司或按休假计划累积休假](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan)。</span><span class="sxs-lookup"><span data-stu-id="0be05-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="0be05-140">将附件添加到休假请求</span><span class="sxs-lookup"><span data-stu-id="0be05-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="0be05-141">在当前的 COVID-19 环境中，向批准的休假请求添加附件的功能至关重要。</span><span class="sxs-lookup"><span data-stu-id="0be05-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="0be05-142">员工现在可以添加这些附件。</span><span class="sxs-lookup"><span data-stu-id="0be05-142">Employees can now add these attachments.</span></span> <span data-ttu-id="0be05-143">他们还将对休假请求进行了怎样的更新有更多了解。</span><span class="sxs-lookup"><span data-stu-id="0be05-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="0be05-144">有关详细信息，请参阅[将附件添加到现有请求](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request)。</span><span class="sxs-lookup"><span data-stu-id="0be05-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="0be05-145">将原因代码添加到应计暂停</span><span class="sxs-lookup"><span data-stu-id="0be05-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="0be05-146">原因代码已添加到应计暂停。</span><span class="sxs-lookup"><span data-stu-id="0be05-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="0be05-147">结转规则</span><span class="sxs-lookup"><span data-stu-id="0be05-147">Carry forward rules</span></span> 

<span data-ttu-id="0be05-148">可为转移了结转调整的结转余额指定结转休假类型。</span><span class="sxs-lookup"><span data-stu-id="0be05-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="0be05-149">例如，如果员工结转 10 天，则可为这 10 天选择其他休假类型。</span><span class="sxs-lookup"><span data-stu-id="0be05-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="0be05-150">有关详细信息，请参阅[配置休假和缺勤类型](hr-leave-and-absence-types.md)。</span><span class="sxs-lookup"><span data-stu-id="0be05-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="0be05-151">暂停指定休假类型的休假应计</span><span class="sxs-lookup"><span data-stu-id="0be05-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="0be05-152">您可以创建一个规则，以针对输入了无薪假休假请求的员工暂停休假应计。</span><span class="sxs-lookup"><span data-stu-id="0be05-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="0be05-153">无薪假可以是一种类型，但不是必须的。</span><span class="sxs-lookup"><span data-stu-id="0be05-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="0be05-154">您可以根据其他休假类型暂停任何休假。</span><span class="sxs-lookup"><span data-stu-id="0be05-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="0be05-155">可用于暂停应计的 DMF 实体</span><span class="sxs-lookup"><span data-stu-id="0be05-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="0be05-156">DMF 实体现在可用于暂停应计。</span><span class="sxs-lookup"><span data-stu-id="0be05-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="0be05-157">即将到期</span><span class="sxs-lookup"><span data-stu-id="0be05-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="0be05-158">Common Data Service 中包含的核对清单实体</span><span class="sxs-lookup"><span data-stu-id="0be05-158">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="0be05-159">Common Data Service 内很快将为入职、离职、转移和业务流程提供核对清单实体。</span><span class="sxs-lookup"><span data-stu-id="0be05-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="0be05-160">平台变更</span><span class="sxs-lookup"><span data-stu-id="0be05-160">Platform changes</span></span>

<span data-ttu-id="0be05-161">平台更新 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="0be05-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="0be05-162">请参阅</span><span class="sxs-lookup"><span data-stu-id="0be05-162">See also</span></span>

[<span data-ttu-id="0be05-163">Human Resources 中新增或更改的功能</span><span class="sxs-lookup"><span data-stu-id="0be05-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="0be05-164">Dynamics 365 Human Resources 2019 发布第 2 波概述</span><span class="sxs-lookup"><span data-stu-id="0be05-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="0be05-165">更新流程</span><span class="sxs-lookup"><span data-stu-id="0be05-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="0be05-166">管理功能</span><span class="sxs-lookup"><span data-stu-id="0be05-166">Manage features</span></span>](hr-admin-manage-features.md)
