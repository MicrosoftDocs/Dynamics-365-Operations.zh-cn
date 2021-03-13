---
title: Dataverse 表
description: Microsoft Dynamics 365 Human Resources 使用 Dataverse 实现可扩展性和集成方案。
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f075a8e96af55b1363d2d51db377c5b25c38775
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111670"
---
# <a name="dataverse-tables"></a><span data-ttu-id="b1c18-103">Dataverse 表</span><span class="sxs-lookup"><span data-stu-id="b1c18-103">Dataverse tables</span></span>

<span data-ttu-id="b1c18-104">Microsoft Dynamics 365 Human Resources 使用 Dataverse 实现可扩展性和集成方案。</span><span class="sxs-lookup"><span data-stu-id="b1c18-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="b1c18-105">Human Resources 实体与 Dataverse 表对应。</span><span class="sxs-lookup"><span data-stu-id="b1c18-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="b1c18-106">有关 Dataverse（以前的 Common Data Service）和术语更新的详细信息，请参阅[什么是 Microsoft Dataverse？](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="b1c18-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="b1c18-107">下列 Dataverse 表基于 Human Resources 实体提供。</span><span class="sxs-lookup"><span data-stu-id="b1c18-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="b1c18-108">福利表</span><span class="sxs-lookup"><span data-stu-id="b1c18-108">Benefit tables</span></span>

| <span data-ttu-id="b1c18-109">姓名</span><span class="sxs-lookup"><span data-stu-id="b1c18-109">Name</span></span> | <span data-ttu-id="b1c18-110">表</span><span class="sxs-lookup"><span data-stu-id="b1c18-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b1c18-111">福利计算频率</span><span class="sxs-lookup"><span data-stu-id="b1c18-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="b1c18-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="b1c18-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="b1c18-113">福利计算频率付薪期间</span><span class="sxs-lookup"><span data-stu-id="b1c18-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="b1c18-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="b1c18-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="b1c18-115">福利计算比率</span><span class="sxs-lookup"><span data-stu-id="b1c18-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="b1c18-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="b1c18-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="b1c18-117">福利计算比率详细信息</span><span class="sxs-lookup"><span data-stu-id="b1c18-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="b1c18-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="b1c18-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="b1c18-119">福利选项</span><span class="sxs-lookup"><span data-stu-id="b1c18-119">Benefit Option</span></span> | <span data-ttu-id="b1c18-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="b1c18-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="b1c18-121">福利计划</span><span class="sxs-lookup"><span data-stu-id="b1c18-121">Benefit Plan</span></span> | <span data-ttu-id="b1c18-122">cdm_benefitplan（未启用自定义字段支持）</span><span class="sxs-lookup"><span data-stu-id="b1c18-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="b1c18-123">福利类型</span><span class="sxs-lookup"><span data-stu-id="b1c18-123">Benefit Type</span></span> | <span data-ttu-id="b1c18-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="b1c18-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="b1c18-125">业务流程任务表</span><span class="sxs-lookup"><span data-stu-id="b1c18-125">Business process tasks tables</span></span>

| <span data-ttu-id="b1c18-126">姓名</span><span class="sxs-lookup"><span data-stu-id="b1c18-126">Name</span></span> | <span data-ttu-id="b1c18-127">表</span><span class="sxs-lookup"><span data-stu-id="b1c18-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b1c18-128">业务流程日历</span><span class="sxs-lookup"><span data-stu-id="b1c18-128">Business Process Calendar</span></span> | <span data-ttu-id="b1c18-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="b1c18-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="b1c18-130">业务流程组分配</span><span class="sxs-lookup"><span data-stu-id="b1c18-130">Business Process Group Assignment</span></span> | <span data-ttu-id="b1c18-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="b1c18-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="b1c18-132">业务流程库任务组</span><span class="sxs-lookup"><span data-stu-id="b1c18-132">Business Process Library Task Group</span></span> | <span data-ttu-id="b1c18-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="b1c18-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="b1c18-134">业务流程阶段</span><span class="sxs-lookup"><span data-stu-id="b1c18-134">Business Process Stage</span></span> | <span data-ttu-id="b1c18-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="b1c18-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="b1c18-136">核对清单模板标题</span><span class="sxs-lookup"><span data-stu-id="b1c18-136">Checklist Template Header</span></span> | <span data-ttu-id="b1c18-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="b1c18-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="b1c18-138">核对清单模板任务</span><span class="sxs-lookup"><span data-stu-id="b1c18-138">Checklist Template Task</span></span> | <span data-ttu-id="b1c18-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="b1c18-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="b1c18-140">薪酬表</span><span class="sxs-lookup"><span data-stu-id="b1c18-140">Compensation tables</span></span>

| <span data-ttu-id="b1c18-141">姓名</span><span class="sxs-lookup"><span data-stu-id="b1c18-141">Name</span></span> | <span data-ttu-id="b1c18-142">表</span><span class="sxs-lookup"><span data-stu-id="b1c18-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b1c18-143">固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="b1c18-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="b1c18-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="b1c18-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="b1c18-145">薪酬网格</span><span class="sxs-lookup"><span data-stu-id="b1c18-145">Compensation Grid</span></span> | <span data-ttu-id="b1c18-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="b1c18-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="b1c18-147">薪酬级别</span><span class="sxs-lookup"><span data-stu-id="b1c18-147">Compensation Level</span></span> | <span data-ttu-id="b1c18-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="b1c18-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="b1c18-149">薪酬付薪频率</span><span class="sxs-lookup"><span data-stu-id="b1c18-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="b1c18-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="b1c18-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="b1c18-151">薪酬参考点设置</span><span class="sxs-lookup"><span data-stu-id="b1c18-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="b1c18-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="b1c18-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="b1c18-153">薪酬参考点设置行</span><span class="sxs-lookup"><span data-stu-id="b1c18-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="b1c18-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="b1c18-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="b1c18-155">薪酬区域</span><span class="sxs-lookup"><span data-stu-id="b1c18-155">Compensation Region</span></span> | <span data-ttu-id="b1c18-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="b1c18-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="b1c18-157">薪酬结构</span><span class="sxs-lookup"><span data-stu-id="b1c18-157">Compensation Structure</span></span> | <span data-ttu-id="b1c18-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="b1c18-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="b1c18-159">可变薪酬计划</span><span class="sxs-lookup"><span data-stu-id="b1c18-159">Compensation Variable Plan</span></span> | <span data-ttu-id="b1c18-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="b1c18-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="b1c18-161">可变薪酬计划级别</span><span class="sxs-lookup"><span data-stu-id="b1c18-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="b1c18-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="b1c18-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="b1c18-163">可变薪酬计划类型</span><span class="sxs-lookup"><span data-stu-id="b1c18-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="b1c18-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="b1c18-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="b1c18-165">固定薪酬事件</span><span class="sxs-lookup"><span data-stu-id="b1c18-165">Fixed Compensation Event</span></span> | <span data-ttu-id="b1c18-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="b1c18-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="b1c18-167">股份行权规则</span><span class="sxs-lookup"><span data-stu-id="b1c18-167">Vesting Rule</span></span> | <span data-ttu-id="b1c18-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="b1c18-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="b1c18-169">工作人员固定薪酬</span><span class="sxs-lookup"><span data-stu-id="b1c18-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="b1c18-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="b1c18-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="b1c18-171">组织表</span><span class="sxs-lookup"><span data-stu-id="b1c18-171">Organization tables</span></span>

| <span data-ttu-id="b1c18-172">姓名</span><span class="sxs-lookup"><span data-stu-id="b1c18-172">Name</span></span> | <span data-ttu-id="b1c18-173">表</span><span class="sxs-lookup"><span data-stu-id="b1c18-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b1c18-174">部门</span><span class="sxs-lookup"><span data-stu-id="b1c18-174">Department</span></span> | <span data-ttu-id="b1c18-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="b1c18-175">cdm_department</span></span> |
| <span data-ttu-id="b1c18-176">雇用</span><span class="sxs-lookup"><span data-stu-id="b1c18-176">Employment</span></span> | <span data-ttu-id="b1c18-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="b1c18-177">cdm_employment</span></span> |
| <span data-ttu-id="b1c18-178">公司</span><span class="sxs-lookup"><span data-stu-id="b1c18-178">Company</span></span> | <span data-ttu-id="b1c18-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="b1c18-179">cdm_company</span></span> |
| <span data-ttu-id="b1c18-180">职位</span><span class="sxs-lookup"><span data-stu-id="b1c18-180">Job</span></span> | <span data-ttu-id="b1c18-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="b1c18-181">cdm_job</span></span> |
| <span data-ttu-id="b1c18-182">工作职能</span><span class="sxs-lookup"><span data-stu-id="b1c18-182">Job Function</span></span> | <span data-ttu-id="b1c18-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="b1c18-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="b1c18-184">工作职位</span><span class="sxs-lookup"><span data-stu-id="b1c18-184">Job Position</span></span> | <span data-ttu-id="b1c18-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="b1c18-185">cdm_jobposition</span></span> |
| <span data-ttu-id="b1c18-186">职位类型</span><span class="sxs-lookup"><span data-stu-id="b1c18-186">Position Type</span></span> | <span data-ttu-id="b1c18-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="b1c18-187">cdm_positiontype</span></span> |
| <span data-ttu-id="b1c18-188">职位工作人员分配</span><span class="sxs-lookup"><span data-stu-id="b1c18-188">Position Worker Assignment</span></span> | <span data-ttu-id="b1c18-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="b1c18-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="b1c18-190">工作职位维度</span><span class="sxs-lookup"><span data-stu-id="b1c18-190">Job Position Dimension</span></span> | <span data-ttu-id="b1c18-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="b1c18-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="b1c18-192">工作类型</span><span class="sxs-lookup"><span data-stu-id="b1c18-192">Job Type</span></span> | <span data-ttu-id="b1c18-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="b1c18-193">cdm_jobtype</span></span> |
| <span data-ttu-id="b1c18-194">语言</span><span class="sxs-lookup"><span data-stu-id="b1c18-194">Language</span></span> | <span data-ttu-id="b1c18-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="b1c18-195">cdm_language</span></span> |
| <span data-ttu-id="b1c18-196">职位</span><span class="sxs-lookup"><span data-stu-id="b1c18-196">Title</span></span> | <span data-ttu-id="b1c18-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="b1c18-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="b1c18-198">**职位类型**、**职位工作人员分配** 和 **雇用** 的财务维度提供到 Dataverse 的单向集成。</span><span class="sxs-lookup"><span data-stu-id="b1c18-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="b1c18-199">财务维度更新现在不能从 Dataverse 同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="b1c18-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="b1c18-200">休假和缺勤表</span><span class="sxs-lookup"><span data-stu-id="b1c18-200">Leave and absence tables</span></span>

| <span data-ttu-id="b1c18-201">姓名</span><span class="sxs-lookup"><span data-stu-id="b1c18-201">Name</span></span> | <span data-ttu-id="b1c18-202">表</span><span class="sxs-lookup"><span data-stu-id="b1c18-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b1c18-203">休假银行交易记录</span><span class="sxs-lookup"><span data-stu-id="b1c18-203">Leave Bank Transaction</span></span> | <span data-ttu-id="b1c18-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="b1c18-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="b1c18-205">休假登记</span><span class="sxs-lookup"><span data-stu-id="b1c18-205">Leave Enrollment</span></span> | <span data-ttu-id="b1c18-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="b1c18-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="b1c18-207">休假计划</span><span class="sxs-lookup"><span data-stu-id="b1c18-207">Leave Plan</span></span> | <span data-ttu-id="b1c18-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="b1c18-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="b1c18-209">休假请求</span><span class="sxs-lookup"><span data-stu-id="b1c18-209">Leave Request</span></span> | <span data-ttu-id="b1c18-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="b1c18-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="b1c18-211">休假请求详细信息</span><span class="sxs-lookup"><span data-stu-id="b1c18-211">Leave Request Detail</span></span> | <span data-ttu-id="b1c18-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="b1c18-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="b1c18-213">休假类型</span><span class="sxs-lookup"><span data-stu-id="b1c18-213">Leave Type</span></span> | <span data-ttu-id="b1c18-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="b1c18-214">cdm_leavetype</span></span> |
| <span data-ttu-id="b1c18-215">休假类型原因代码</span><span class="sxs-lookup"><span data-stu-id="b1c18-215">Leave Type Reason Code</span></span> | <span data-ttu-id="b1c18-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="b1c18-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="b1c18-217">工资表</span><span class="sxs-lookup"><span data-stu-id="b1c18-217">Payroll tables</span></span>

| <span data-ttu-id="b1c18-218">姓名</span><span class="sxs-lookup"><span data-stu-id="b1c18-218">Name</span></span> | <span data-ttu-id="b1c18-219">表</span><span class="sxs-lookup"><span data-stu-id="b1c18-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b1c18-220">付薪周期</span><span class="sxs-lookup"><span data-stu-id="b1c18-220">Pay Cycle</span></span> | <span data-ttu-id="b1c18-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="b1c18-221">cdm_paycycle</span></span> |
| <span data-ttu-id="b1c18-222">付薪期间</span><span class="sxs-lookup"><span data-stu-id="b1c18-222">Pay Period</span></span> | <span data-ttu-id="b1c18-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="b1c18-223">cdm_payperiod</span></span> |
| <span data-ttu-id="b1c18-224">工资单收入代码</span><span class="sxs-lookup"><span data-stu-id="b1c18-224">Payroll Earning Code</span></span> | <span data-ttu-id="b1c18-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="b1c18-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="b1c18-226">银行帐户付款</span><span class="sxs-lookup"><span data-stu-id="b1c18-226">Bank Account Disbursement</span></span> | <span data-ttu-id="b1c18-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="b1c18-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="b1c18-228">税区</span><span class="sxs-lookup"><span data-stu-id="b1c18-228">Tax Region</span></span> | <span data-ttu-id="b1c18-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="b1c18-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="b1c18-230">工作人员表</span><span class="sxs-lookup"><span data-stu-id="b1c18-230">Worker tables</span></span>

| <span data-ttu-id="b1c18-231">姓名</span><span class="sxs-lookup"><span data-stu-id="b1c18-231">Name</span></span> | <span data-ttu-id="b1c18-232">表</span><span class="sxs-lookup"><span data-stu-id="b1c18-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b1c18-233">工作线程</span><span class="sxs-lookup"><span data-stu-id="b1c18-233">Worker</span></span> | <span data-ttu-id="b1c18-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="b1c18-234">cdm_worker</span></span> |
| <span data-ttu-id="b1c18-235">工作人员地址</span><span class="sxs-lookup"><span data-stu-id="b1c18-235">Worker Address</span></span> | <span data-ttu-id="b1c18-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="b1c18-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="b1c18-237">工作人员个人详细信息</span><span class="sxs-lookup"><span data-stu-id="b1c18-237">Worker Personal Detail</span></span> | <span data-ttu-id="b1c18-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="b1c18-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="b1c18-239">工作人员标识号</span><span class="sxs-lookup"><span data-stu-id="b1c18-239">Worker Person Identification Number</span></span> | <span data-ttu-id="b1c18-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="b1c18-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="b1c18-241">工作人员标识类型</span><span class="sxs-lookup"><span data-stu-id="b1c18-241">Worker Person Identification Type</span></span> | <span data-ttu-id="b1c18-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="b1c18-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="b1c18-243">工作日历</span><span class="sxs-lookup"><span data-stu-id="b1c18-243">Work Calendar</span></span> | <span data-ttu-id="b1c18-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="b1c18-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="b1c18-245">工作日历天</span><span class="sxs-lookup"><span data-stu-id="b1c18-245">Work Calendar Day</span></span> | <span data-ttu-id="b1c18-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="b1c18-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="b1c18-247">工作日历的假日</span><span class="sxs-lookup"><span data-stu-id="b1c18-247">Work Calendar Holiday</span></span> |<span data-ttu-id="b1c18-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="b1c18-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="b1c18-249">工作日历假期行</span><span class="sxs-lookup"><span data-stu-id="b1c18-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="b1c18-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="b1c18-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="b1c18-251">工作日历时间间隔</span><span class="sxs-lookup"><span data-stu-id="b1c18-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="b1c18-252">cdm_workcalendartimeinterval（未启用自定义字段支持）</span><span class="sxs-lookup"><span data-stu-id="b1c18-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="b1c18-253">工作人员银行帐户</span><span class="sxs-lookup"><span data-stu-id="b1c18-253">Worker Bank Account</span></span> | <span data-ttu-id="b1c18-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="b1c18-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="b1c18-255">工作人员设置表</span><span class="sxs-lookup"><span data-stu-id="b1c18-255">Worker setup tables</span></span>

| <span data-ttu-id="b1c18-256">姓名</span><span class="sxs-lookup"><span data-stu-id="b1c18-256">Name</span></span> | <span data-ttu-id="b1c18-257">表</span><span class="sxs-lookup"><span data-stu-id="b1c18-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b1c18-258">退伍军人状态</span><span class="sxs-lookup"><span data-stu-id="b1c18-258">Veteran Status</span></span> | <span data-ttu-id="b1c18-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="b1c18-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="b1c18-260">所属种族</span><span class="sxs-lookup"><span data-stu-id="b1c18-260">Ethnic Origin</span></span> | <span data-ttu-id="b1c18-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="b1c18-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="b1c18-262">原因代码</span><span class="sxs-lookup"><span data-stu-id="b1c18-262">Reason Code</span></span> | <span data-ttu-id="b1c18-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="b1c18-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="b1c18-264">人员身份证明签发机构</span><span class="sxs-lookup"><span data-stu-id="b1c18-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="b1c18-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="b1c18-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="b1c18-266">能力表</span><span class="sxs-lookup"><span data-stu-id="b1c18-266">Competency tables</span></span>

| <span data-ttu-id="b1c18-267">姓名</span><span class="sxs-lookup"><span data-stu-id="b1c18-267">Name</span></span> | <span data-ttu-id="b1c18-268">表</span><span class="sxs-lookup"><span data-stu-id="b1c18-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="b1c18-269">技能类型</span><span class="sxs-lookup"><span data-stu-id="b1c18-269">Skill Type</span></span> | <span data-ttu-id="b1c18-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="b1c18-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="b1c18-271">表关系模型</span><span class="sxs-lookup"><span data-stu-id="b1c18-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="b1c18-272">工作线程</span><span class="sxs-lookup"><span data-stu-id="b1c18-272">Worker</span></span>

![工作线程](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="b1c18-274">工作和工作职位</span><span class="sxs-lookup"><span data-stu-id="b1c18-274">Job and Job Position</span></span>

![工作和工作职位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="b1c18-276">福利</span><span class="sxs-lookup"><span data-stu-id="b1c18-276">Benefits</span></span>

![福利](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="b1c18-278">薪酬</span><span class="sxs-lookup"><span data-stu-id="b1c18-278">Compensation</span></span>

![薪酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="b1c18-280">离开</span><span class="sxs-lookup"><span data-stu-id="b1c18-280">Leave</span></span>

![离开](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="b1c18-282">工作日历</span><span class="sxs-lookup"><span data-stu-id="b1c18-282">Work Calendar</span></span>

![工作日历](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="b1c18-284">请参阅</span><span class="sxs-lookup"><span data-stu-id="b1c18-284">See also</span></span>

[<span data-ttu-id="b1c18-285">选择数据集成技术</span><span class="sxs-lookup"><span data-stu-id="b1c18-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="b1c18-286">配置 Dataverse 集成</span><span class="sxs-lookup"><span data-stu-id="b1c18-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="b1c18-287">配置 Dataverse 虚拟表</span><span class="sxs-lookup"><span data-stu-id="b1c18-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="b1c18-288">Human Resources 虚拟表常见问题解答</span><span class="sxs-lookup"><span data-stu-id="b1c18-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="b1c18-289">什么是 Microsoft Dataverse？</span><span class="sxs-lookup"><span data-stu-id="b1c18-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="b1c18-290">术语更新</span><span class="sxs-lookup"><span data-stu-id="b1c18-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
