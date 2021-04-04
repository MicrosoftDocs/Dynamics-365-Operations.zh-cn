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
ms.openlocfilehash: caf8b0a5d0b24ef3619f45a6d236acae6d29c8ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465214"
---
# <a name="dataverse-tables"></a><span data-ttu-id="43006-103">Dataverse 表</span><span class="sxs-lookup"><span data-stu-id="43006-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="43006-104">Microsoft Dynamics 365 Human Resources 使用 Dataverse 实现可扩展性和集成方案。</span><span class="sxs-lookup"><span data-stu-id="43006-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="43006-105">Human Resources 实体与 Dataverse 表对应。</span><span class="sxs-lookup"><span data-stu-id="43006-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="43006-106">有关 Dataverse（以前的 Common Data Service）和术语更新的详细信息，请参阅[什么是 Microsoft Dataverse？](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="43006-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="43006-107">下列 Dataverse 表基于 Human Resources 实体提供。</span><span class="sxs-lookup"><span data-stu-id="43006-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="43006-108">福利表</span><span class="sxs-lookup"><span data-stu-id="43006-108">Benefit tables</span></span>

| <span data-ttu-id="43006-109">姓名</span><span class="sxs-lookup"><span data-stu-id="43006-109">Name</span></span> | <span data-ttu-id="43006-110">表</span><span class="sxs-lookup"><span data-stu-id="43006-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43006-111">福利计算频率</span><span class="sxs-lookup"><span data-stu-id="43006-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="43006-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="43006-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="43006-113">福利计算频率付薪期间</span><span class="sxs-lookup"><span data-stu-id="43006-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="43006-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="43006-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="43006-115">福利计算比率</span><span class="sxs-lookup"><span data-stu-id="43006-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="43006-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="43006-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="43006-117">福利计算比率详细信息</span><span class="sxs-lookup"><span data-stu-id="43006-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="43006-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="43006-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="43006-119">福利选项</span><span class="sxs-lookup"><span data-stu-id="43006-119">Benefit Option</span></span> | <span data-ttu-id="43006-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="43006-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="43006-121">福利计划</span><span class="sxs-lookup"><span data-stu-id="43006-121">Benefit Plan</span></span> | <span data-ttu-id="43006-122">cdm_benefitplan（未启用自定义字段支持）</span><span class="sxs-lookup"><span data-stu-id="43006-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="43006-123">福利类型</span><span class="sxs-lookup"><span data-stu-id="43006-123">Benefit Type</span></span> | <span data-ttu-id="43006-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="43006-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="43006-125">业务流程任务表</span><span class="sxs-lookup"><span data-stu-id="43006-125">Business process tasks tables</span></span>

| <span data-ttu-id="43006-126">姓名</span><span class="sxs-lookup"><span data-stu-id="43006-126">Name</span></span> | <span data-ttu-id="43006-127">表</span><span class="sxs-lookup"><span data-stu-id="43006-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43006-128">业务流程日历</span><span class="sxs-lookup"><span data-stu-id="43006-128">Business Process Calendar</span></span> | <span data-ttu-id="43006-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="43006-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="43006-130">业务流程组分配</span><span class="sxs-lookup"><span data-stu-id="43006-130">Business Process Group Assignment</span></span> | <span data-ttu-id="43006-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="43006-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="43006-132">业务流程库任务组</span><span class="sxs-lookup"><span data-stu-id="43006-132">Business Process Library Task Group</span></span> | <span data-ttu-id="43006-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="43006-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="43006-134">业务流程阶段</span><span class="sxs-lookup"><span data-stu-id="43006-134">Business Process Stage</span></span> | <span data-ttu-id="43006-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="43006-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="43006-136">核对清单模板标题</span><span class="sxs-lookup"><span data-stu-id="43006-136">Checklist Template Header</span></span> | <span data-ttu-id="43006-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="43006-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="43006-138">核对清单模板任务</span><span class="sxs-lookup"><span data-stu-id="43006-138">Checklist Template Task</span></span> | <span data-ttu-id="43006-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="43006-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="43006-140">薪酬表</span><span class="sxs-lookup"><span data-stu-id="43006-140">Compensation tables</span></span>

| <span data-ttu-id="43006-141">姓名</span><span class="sxs-lookup"><span data-stu-id="43006-141">Name</span></span> | <span data-ttu-id="43006-142">表</span><span class="sxs-lookup"><span data-stu-id="43006-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43006-143">固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="43006-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="43006-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="43006-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="43006-145">薪酬网格</span><span class="sxs-lookup"><span data-stu-id="43006-145">Compensation Grid</span></span> | <span data-ttu-id="43006-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="43006-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="43006-147">薪酬级别</span><span class="sxs-lookup"><span data-stu-id="43006-147">Compensation Level</span></span> | <span data-ttu-id="43006-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="43006-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="43006-149">薪酬付薪频率</span><span class="sxs-lookup"><span data-stu-id="43006-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="43006-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="43006-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="43006-151">薪酬参考点设置</span><span class="sxs-lookup"><span data-stu-id="43006-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="43006-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="43006-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="43006-153">薪酬参考点设置行</span><span class="sxs-lookup"><span data-stu-id="43006-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="43006-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="43006-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="43006-155">薪酬区域</span><span class="sxs-lookup"><span data-stu-id="43006-155">Compensation Region</span></span> | <span data-ttu-id="43006-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="43006-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="43006-157">薪酬结构</span><span class="sxs-lookup"><span data-stu-id="43006-157">Compensation Structure</span></span> | <span data-ttu-id="43006-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="43006-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="43006-159">可变薪酬计划</span><span class="sxs-lookup"><span data-stu-id="43006-159">Compensation Variable Plan</span></span> | <span data-ttu-id="43006-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="43006-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="43006-161">可变薪酬计划级别</span><span class="sxs-lookup"><span data-stu-id="43006-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="43006-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="43006-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="43006-163">可变薪酬计划类型</span><span class="sxs-lookup"><span data-stu-id="43006-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="43006-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="43006-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="43006-165">固定薪酬事件</span><span class="sxs-lookup"><span data-stu-id="43006-165">Fixed Compensation Event</span></span> | <span data-ttu-id="43006-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="43006-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="43006-167">股份行权规则</span><span class="sxs-lookup"><span data-stu-id="43006-167">Vesting Rule</span></span> | <span data-ttu-id="43006-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="43006-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="43006-169">工作人员固定薪酬</span><span class="sxs-lookup"><span data-stu-id="43006-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="43006-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="43006-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="43006-171">组织表</span><span class="sxs-lookup"><span data-stu-id="43006-171">Organization tables</span></span>

| <span data-ttu-id="43006-172">姓名</span><span class="sxs-lookup"><span data-stu-id="43006-172">Name</span></span> | <span data-ttu-id="43006-173">表</span><span class="sxs-lookup"><span data-stu-id="43006-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43006-174">部门</span><span class="sxs-lookup"><span data-stu-id="43006-174">Department</span></span> | <span data-ttu-id="43006-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="43006-175">cdm_department</span></span> |
| <span data-ttu-id="43006-176">雇用</span><span class="sxs-lookup"><span data-stu-id="43006-176">Employment</span></span> | <span data-ttu-id="43006-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="43006-177">cdm_employment</span></span> |
| <span data-ttu-id="43006-178">公司</span><span class="sxs-lookup"><span data-stu-id="43006-178">Company</span></span> | <span data-ttu-id="43006-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="43006-179">cdm_company</span></span> |
| <span data-ttu-id="43006-180">职位</span><span class="sxs-lookup"><span data-stu-id="43006-180">Job</span></span> | <span data-ttu-id="43006-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="43006-181">cdm_job</span></span> |
| <span data-ttu-id="43006-182">工作职能</span><span class="sxs-lookup"><span data-stu-id="43006-182">Job Function</span></span> | <span data-ttu-id="43006-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="43006-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="43006-184">工作职位</span><span class="sxs-lookup"><span data-stu-id="43006-184">Job Position</span></span> | <span data-ttu-id="43006-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="43006-185">cdm_jobposition</span></span> |
| <span data-ttu-id="43006-186">职位类型</span><span class="sxs-lookup"><span data-stu-id="43006-186">Position Type</span></span> | <span data-ttu-id="43006-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="43006-187">cdm_positiontype</span></span> |
| <span data-ttu-id="43006-188">职位工作人员分配</span><span class="sxs-lookup"><span data-stu-id="43006-188">Position Worker Assignment</span></span> | <span data-ttu-id="43006-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="43006-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="43006-190">工作职位维度</span><span class="sxs-lookup"><span data-stu-id="43006-190">Job Position Dimension</span></span> | <span data-ttu-id="43006-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="43006-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="43006-192">工作类型</span><span class="sxs-lookup"><span data-stu-id="43006-192">Job Type</span></span> | <span data-ttu-id="43006-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="43006-193">cdm_jobtype</span></span> |
| <span data-ttu-id="43006-194">语言</span><span class="sxs-lookup"><span data-stu-id="43006-194">Language</span></span> | <span data-ttu-id="43006-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="43006-195">cdm_language</span></span> |
| <span data-ttu-id="43006-196">职位</span><span class="sxs-lookup"><span data-stu-id="43006-196">Title</span></span> | <span data-ttu-id="43006-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="43006-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="43006-198">**职位类型**、**职位工作人员分配** 和 **雇用** 的财务维度提供到 Dataverse 的单向集成。</span><span class="sxs-lookup"><span data-stu-id="43006-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="43006-199">财务维度更新现在不能从 Dataverse 同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="43006-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="43006-200">休假和缺勤表</span><span class="sxs-lookup"><span data-stu-id="43006-200">Leave and absence tables</span></span>

| <span data-ttu-id="43006-201">姓名</span><span class="sxs-lookup"><span data-stu-id="43006-201">Name</span></span> | <span data-ttu-id="43006-202">表</span><span class="sxs-lookup"><span data-stu-id="43006-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43006-203">休假银行交易记录</span><span class="sxs-lookup"><span data-stu-id="43006-203">Leave Bank Transaction</span></span> | <span data-ttu-id="43006-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="43006-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="43006-205">休假登记</span><span class="sxs-lookup"><span data-stu-id="43006-205">Leave Enrollment</span></span> | <span data-ttu-id="43006-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="43006-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="43006-207">休假计划</span><span class="sxs-lookup"><span data-stu-id="43006-207">Leave Plan</span></span> | <span data-ttu-id="43006-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="43006-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="43006-209">休假请求</span><span class="sxs-lookup"><span data-stu-id="43006-209">Leave Request</span></span> | <span data-ttu-id="43006-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="43006-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="43006-211">休假请求详细信息</span><span class="sxs-lookup"><span data-stu-id="43006-211">Leave Request Detail</span></span> | <span data-ttu-id="43006-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="43006-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="43006-213">休假类型</span><span class="sxs-lookup"><span data-stu-id="43006-213">Leave Type</span></span> | <span data-ttu-id="43006-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="43006-214">cdm_leavetype</span></span> |
| <span data-ttu-id="43006-215">休假类型原因代码</span><span class="sxs-lookup"><span data-stu-id="43006-215">Leave Type Reason Code</span></span> | <span data-ttu-id="43006-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="43006-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="43006-217">工资表</span><span class="sxs-lookup"><span data-stu-id="43006-217">Payroll tables</span></span>

| <span data-ttu-id="43006-218">姓名</span><span class="sxs-lookup"><span data-stu-id="43006-218">Name</span></span> | <span data-ttu-id="43006-219">表</span><span class="sxs-lookup"><span data-stu-id="43006-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43006-220">付薪周期</span><span class="sxs-lookup"><span data-stu-id="43006-220">Pay Cycle</span></span> | <span data-ttu-id="43006-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="43006-221">cdm_paycycle</span></span> |
| <span data-ttu-id="43006-222">付薪期间</span><span class="sxs-lookup"><span data-stu-id="43006-222">Pay Period</span></span> | <span data-ttu-id="43006-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="43006-223">cdm_payperiod</span></span> |
| <span data-ttu-id="43006-224">工资单收入代码</span><span class="sxs-lookup"><span data-stu-id="43006-224">Payroll Earning Code</span></span> | <span data-ttu-id="43006-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="43006-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="43006-226">银行帐户付款</span><span class="sxs-lookup"><span data-stu-id="43006-226">Bank Account Disbursement</span></span> | <span data-ttu-id="43006-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="43006-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="43006-228">税区</span><span class="sxs-lookup"><span data-stu-id="43006-228">Tax Region</span></span> | <span data-ttu-id="43006-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="43006-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="43006-230">工作人员表</span><span class="sxs-lookup"><span data-stu-id="43006-230">Worker tables</span></span>

| <span data-ttu-id="43006-231">姓名</span><span class="sxs-lookup"><span data-stu-id="43006-231">Name</span></span> | <span data-ttu-id="43006-232">表</span><span class="sxs-lookup"><span data-stu-id="43006-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43006-233">工作线程</span><span class="sxs-lookup"><span data-stu-id="43006-233">Worker</span></span> | <span data-ttu-id="43006-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="43006-234">cdm_worker</span></span> |
| <span data-ttu-id="43006-235">工作人员地址</span><span class="sxs-lookup"><span data-stu-id="43006-235">Worker Address</span></span> | <span data-ttu-id="43006-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="43006-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="43006-237">工作人员个人详细信息</span><span class="sxs-lookup"><span data-stu-id="43006-237">Worker Personal Detail</span></span> | <span data-ttu-id="43006-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="43006-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="43006-239">工作人员标识号</span><span class="sxs-lookup"><span data-stu-id="43006-239">Worker Person Identification Number</span></span> | <span data-ttu-id="43006-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="43006-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="43006-241">工作人员标识类型</span><span class="sxs-lookup"><span data-stu-id="43006-241">Worker Person Identification Type</span></span> | <span data-ttu-id="43006-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="43006-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="43006-243">工作日历</span><span class="sxs-lookup"><span data-stu-id="43006-243">Work Calendar</span></span> | <span data-ttu-id="43006-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="43006-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="43006-245">工作日历天</span><span class="sxs-lookup"><span data-stu-id="43006-245">Work Calendar Day</span></span> | <span data-ttu-id="43006-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="43006-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="43006-247">工作日历的假日</span><span class="sxs-lookup"><span data-stu-id="43006-247">Work Calendar Holiday</span></span> |<span data-ttu-id="43006-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="43006-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="43006-249">工作日历假期行</span><span class="sxs-lookup"><span data-stu-id="43006-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="43006-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="43006-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="43006-251">工作日历时间间隔</span><span class="sxs-lookup"><span data-stu-id="43006-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="43006-252">cdm_workcalendartimeinterval（未启用自定义字段支持）</span><span class="sxs-lookup"><span data-stu-id="43006-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="43006-253">工作人员银行帐户</span><span class="sxs-lookup"><span data-stu-id="43006-253">Worker Bank Account</span></span> | <span data-ttu-id="43006-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="43006-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="43006-255">工作人员设置表</span><span class="sxs-lookup"><span data-stu-id="43006-255">Worker setup tables</span></span>

| <span data-ttu-id="43006-256">姓名</span><span class="sxs-lookup"><span data-stu-id="43006-256">Name</span></span> | <span data-ttu-id="43006-257">表</span><span class="sxs-lookup"><span data-stu-id="43006-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43006-258">退伍军人状态</span><span class="sxs-lookup"><span data-stu-id="43006-258">Veteran Status</span></span> | <span data-ttu-id="43006-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="43006-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="43006-260">所属种族</span><span class="sxs-lookup"><span data-stu-id="43006-260">Ethnic Origin</span></span> | <span data-ttu-id="43006-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="43006-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="43006-262">原因代码</span><span class="sxs-lookup"><span data-stu-id="43006-262">Reason Code</span></span> | <span data-ttu-id="43006-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="43006-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="43006-264">人员身份证明签发机构</span><span class="sxs-lookup"><span data-stu-id="43006-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="43006-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="43006-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="43006-266">能力表</span><span class="sxs-lookup"><span data-stu-id="43006-266">Competency tables</span></span>

| <span data-ttu-id="43006-267">姓名</span><span class="sxs-lookup"><span data-stu-id="43006-267">Name</span></span> | <span data-ttu-id="43006-268">表</span><span class="sxs-lookup"><span data-stu-id="43006-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="43006-269">技能类型</span><span class="sxs-lookup"><span data-stu-id="43006-269">Skill Type</span></span> | <span data-ttu-id="43006-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="43006-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="43006-271">表关系模型</span><span class="sxs-lookup"><span data-stu-id="43006-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="43006-272">工作线程</span><span class="sxs-lookup"><span data-stu-id="43006-272">Worker</span></span>

![工作线程](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="43006-274">工作和工作职位</span><span class="sxs-lookup"><span data-stu-id="43006-274">Job and Job Position</span></span>

![工作和工作职位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="43006-276">福利</span><span class="sxs-lookup"><span data-stu-id="43006-276">Benefits</span></span>

![福利](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="43006-278">薪酬</span><span class="sxs-lookup"><span data-stu-id="43006-278">Compensation</span></span>

![薪酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="43006-280">离开</span><span class="sxs-lookup"><span data-stu-id="43006-280">Leave</span></span>

![离开](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="43006-282">工作日历</span><span class="sxs-lookup"><span data-stu-id="43006-282">Work Calendar</span></span>

![工作日历](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="43006-284">请参阅</span><span class="sxs-lookup"><span data-stu-id="43006-284">See also</span></span>

[<span data-ttu-id="43006-285">选择数据集成技术</span><span class="sxs-lookup"><span data-stu-id="43006-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="43006-286">配置 Dataverse 集成</span><span class="sxs-lookup"><span data-stu-id="43006-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="43006-287">配置 Dataverse 虚拟表</span><span class="sxs-lookup"><span data-stu-id="43006-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="43006-288">Human Resources 虚拟表常见问题解答</span><span class="sxs-lookup"><span data-stu-id="43006-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="43006-289">什么是 Microsoft Dataverse？</span><span class="sxs-lookup"><span data-stu-id="43006-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="43006-290">术语更新</span><span class="sxs-lookup"><span data-stu-id="43006-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]