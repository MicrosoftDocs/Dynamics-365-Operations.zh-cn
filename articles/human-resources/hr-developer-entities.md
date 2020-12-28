---
title: Common Data Service 实体
description: Microsoft Dynamics 365 Human Resources 使用 Common Data Service 实现可扩展性和集成方案。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529998"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="f6378-103">Common Data Service 实体</span><span class="sxs-lookup"><span data-stu-id="f6378-103">Common Data Service entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f6378-104">Microsoft Dynamics 365 Human Resources 使用 Common Data Service 实现可扩展性和集成方案。</span><span class="sxs-lookup"><span data-stu-id="f6378-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="f6378-105">有关 Common Data Service 的详细信息，请参阅[什么是 Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)。</span><span class="sxs-lookup"><span data-stu-id="f6378-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="f6378-106">Common Data Service 中提供以下 Human Resources 实体。</span><span class="sxs-lookup"><span data-stu-id="f6378-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="f6378-107">福利实体</span><span class="sxs-lookup"><span data-stu-id="f6378-107">Benefit entities</span></span>

| <span data-ttu-id="f6378-108">姓名</span><span class="sxs-lookup"><span data-stu-id="f6378-108">Name</span></span> | <span data-ttu-id="f6378-109">实体</span><span class="sxs-lookup"><span data-stu-id="f6378-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f6378-110">福利计算频率</span><span class="sxs-lookup"><span data-stu-id="f6378-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="f6378-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="f6378-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="f6378-112">福利计算频率付薪期间</span><span class="sxs-lookup"><span data-stu-id="f6378-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="f6378-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="f6378-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="f6378-114">福利计算比率</span><span class="sxs-lookup"><span data-stu-id="f6378-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="f6378-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="f6378-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="f6378-116">福利计算比率详细信息</span><span class="sxs-lookup"><span data-stu-id="f6378-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="f6378-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="f6378-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="f6378-118">福利选项</span><span class="sxs-lookup"><span data-stu-id="f6378-118">Benefit Option</span></span> | <span data-ttu-id="f6378-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="f6378-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="f6378-120">福利计划</span><span class="sxs-lookup"><span data-stu-id="f6378-120">Benefit Plan</span></span> | <span data-ttu-id="f6378-121">cdm_benefitplan（未启用自定义字段支持）</span><span class="sxs-lookup"><span data-stu-id="f6378-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="f6378-122">福利类型</span><span class="sxs-lookup"><span data-stu-id="f6378-122">Benefit Type</span></span> | <span data-ttu-id="f6378-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="f6378-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="f6378-124">业务流程任务实体</span><span class="sxs-lookup"><span data-stu-id="f6378-124">Business process tasks entities</span></span>

| <span data-ttu-id="f6378-125">姓名</span><span class="sxs-lookup"><span data-stu-id="f6378-125">Name</span></span> | <span data-ttu-id="f6378-126">实体</span><span class="sxs-lookup"><span data-stu-id="f6378-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f6378-127">业务流程日历</span><span class="sxs-lookup"><span data-stu-id="f6378-127">Business Process Calendar</span></span> | <span data-ttu-id="f6378-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="f6378-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="f6378-129">业务流程组分配</span><span class="sxs-lookup"><span data-stu-id="f6378-129">Business Process Group Assignment</span></span> | <span data-ttu-id="f6378-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="f6378-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="f6378-131">业务流程库任务组</span><span class="sxs-lookup"><span data-stu-id="f6378-131">Business Process Library Task Group</span></span> | <span data-ttu-id="f6378-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="f6378-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="f6378-133">业务流程阶段</span><span class="sxs-lookup"><span data-stu-id="f6378-133">Business Process Stage</span></span> | <span data-ttu-id="f6378-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="f6378-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="f6378-135">核对清单模板标题</span><span class="sxs-lookup"><span data-stu-id="f6378-135">Checklist Template Header</span></span> | <span data-ttu-id="f6378-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="f6378-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="f6378-137">核对清单模板任务</span><span class="sxs-lookup"><span data-stu-id="f6378-137">Checklist Template Task</span></span> | <span data-ttu-id="f6378-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="f6378-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="f6378-139">薪酬实体</span><span class="sxs-lookup"><span data-stu-id="f6378-139">Compensation entities</span></span>

| <span data-ttu-id="f6378-140">姓名</span><span class="sxs-lookup"><span data-stu-id="f6378-140">Name</span></span> | <span data-ttu-id="f6378-141">实体</span><span class="sxs-lookup"><span data-stu-id="f6378-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f6378-142">薪酬固定计划</span><span class="sxs-lookup"><span data-stu-id="f6378-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="f6378-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="f6378-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="f6378-144">薪酬网格</span><span class="sxs-lookup"><span data-stu-id="f6378-144">Compensation Grid</span></span> | <span data-ttu-id="f6378-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="f6378-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="f6378-146">薪酬级别</span><span class="sxs-lookup"><span data-stu-id="f6378-146">Compensation Level</span></span> | <span data-ttu-id="f6378-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="f6378-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="f6378-148">薪酬付薪频率</span><span class="sxs-lookup"><span data-stu-id="f6378-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="f6378-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="f6378-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="f6378-150">薪酬参考点设置</span><span class="sxs-lookup"><span data-stu-id="f6378-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="f6378-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="f6378-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="f6378-152">薪酬参考点设置行</span><span class="sxs-lookup"><span data-stu-id="f6378-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="f6378-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="f6378-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="f6378-154">薪酬区域</span><span class="sxs-lookup"><span data-stu-id="f6378-154">Compensation Region</span></span> | <span data-ttu-id="f6378-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="f6378-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="f6378-156">薪酬结构</span><span class="sxs-lookup"><span data-stu-id="f6378-156">Compensation Structure</span></span> | <span data-ttu-id="f6378-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="f6378-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="f6378-158">可变薪酬计划</span><span class="sxs-lookup"><span data-stu-id="f6378-158">Compensation Variable Plan</span></span> | <span data-ttu-id="f6378-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="f6378-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="f6378-160">可变薪酬计划级别</span><span class="sxs-lookup"><span data-stu-id="f6378-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="f6378-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="f6378-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="f6378-162">可变薪酬计划类型</span><span class="sxs-lookup"><span data-stu-id="f6378-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="f6378-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="f6378-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="f6378-164">固定薪酬事件</span><span class="sxs-lookup"><span data-stu-id="f6378-164">Fixed Compensation Event</span></span> | <span data-ttu-id="f6378-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="f6378-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="f6378-166">股份行权规则</span><span class="sxs-lookup"><span data-stu-id="f6378-166">Vesting Rule</span></span> | <span data-ttu-id="f6378-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="f6378-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="f6378-168">工作人员固定薪酬</span><span class="sxs-lookup"><span data-stu-id="f6378-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="f6378-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="f6378-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="f6378-170">组织实体</span><span class="sxs-lookup"><span data-stu-id="f6378-170">Organization entities</span></span>

| <span data-ttu-id="f6378-171">姓名</span><span class="sxs-lookup"><span data-stu-id="f6378-171">Name</span></span> | <span data-ttu-id="f6378-172">实体</span><span class="sxs-lookup"><span data-stu-id="f6378-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f6378-173">部门</span><span class="sxs-lookup"><span data-stu-id="f6378-173">Department</span></span> | <span data-ttu-id="f6378-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="f6378-174">cdm_department</span></span> |
| <span data-ttu-id="f6378-175">雇用</span><span class="sxs-lookup"><span data-stu-id="f6378-175">Employment</span></span> | <span data-ttu-id="f6378-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="f6378-176">cdm_employment</span></span> |
| <span data-ttu-id="f6378-177">公司</span><span class="sxs-lookup"><span data-stu-id="f6378-177">Company</span></span> | <span data-ttu-id="f6378-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="f6378-178">cdm_company</span></span> |
| <span data-ttu-id="f6378-179">职位</span><span class="sxs-lookup"><span data-stu-id="f6378-179">Job</span></span> | <span data-ttu-id="f6378-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="f6378-180">cdm_job</span></span> |
| <span data-ttu-id="f6378-181">工作职能</span><span class="sxs-lookup"><span data-stu-id="f6378-181">Job Function</span></span> | <span data-ttu-id="f6378-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="f6378-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="f6378-183">工作职位</span><span class="sxs-lookup"><span data-stu-id="f6378-183">Job Position</span></span> | <span data-ttu-id="f6378-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="f6378-184">cdm_jobposition</span></span> |
| <span data-ttu-id="f6378-185">职位类型</span><span class="sxs-lookup"><span data-stu-id="f6378-185">Position Type</span></span> | <span data-ttu-id="f6378-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="f6378-186">cdm_positiontype</span></span> |
| <span data-ttu-id="f6378-187">职位工作人员分配</span><span class="sxs-lookup"><span data-stu-id="f6378-187">Position Worker Assignment</span></span> | <span data-ttu-id="f6378-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="f6378-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="f6378-189">工作职位维度</span><span class="sxs-lookup"><span data-stu-id="f6378-189">Job Position Dimension</span></span> | <span data-ttu-id="f6378-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="f6378-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="f6378-191">工作类型</span><span class="sxs-lookup"><span data-stu-id="f6378-191">Job Type</span></span> | <span data-ttu-id="f6378-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="f6378-192">cdm_jobtype</span></span> |
| <span data-ttu-id="f6378-193">语言</span><span class="sxs-lookup"><span data-stu-id="f6378-193">Language</span></span> | <span data-ttu-id="f6378-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="f6378-194">cdm_language</span></span> |
| <span data-ttu-id="f6378-195">职位</span><span class="sxs-lookup"><span data-stu-id="f6378-195">Title</span></span> | <span data-ttu-id="f6378-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="f6378-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="f6378-197">**职位类型**、**职位工作人员分配** 和 **雇用** 的财务维度提供到 Common Data Service 的单向集成。</span><span class="sxs-lookup"><span data-stu-id="f6378-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="f6378-198">财务维度更新现在不能从 Common Data Service 同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="f6378-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="f6378-199">休假和缺勤实体</span><span class="sxs-lookup"><span data-stu-id="f6378-199">Leave and absence entities</span></span>

| <span data-ttu-id="f6378-200">姓名</span><span class="sxs-lookup"><span data-stu-id="f6378-200">Name</span></span> | <span data-ttu-id="f6378-201">实体</span><span class="sxs-lookup"><span data-stu-id="f6378-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f6378-202">休假银行交易记录</span><span class="sxs-lookup"><span data-stu-id="f6378-202">Leave Bank Transaction</span></span> | <span data-ttu-id="f6378-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="f6378-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="f6378-204">休假登记</span><span class="sxs-lookup"><span data-stu-id="f6378-204">Leave Enrollment</span></span> | <span data-ttu-id="f6378-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="f6378-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="f6378-206">休假计划</span><span class="sxs-lookup"><span data-stu-id="f6378-206">Leave Plan</span></span> | <span data-ttu-id="f6378-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="f6378-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="f6378-208">休假请求</span><span class="sxs-lookup"><span data-stu-id="f6378-208">Leave Request</span></span> | <span data-ttu-id="f6378-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="f6378-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="f6378-210">休假请求详细信息</span><span class="sxs-lookup"><span data-stu-id="f6378-210">Leave Request Detail</span></span> | <span data-ttu-id="f6378-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="f6378-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="f6378-212">休假类型</span><span class="sxs-lookup"><span data-stu-id="f6378-212">Leave Type</span></span> | <span data-ttu-id="f6378-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="f6378-213">cdm_leavetype</span></span> |
| <span data-ttu-id="f6378-214">休假类型原因代码</span><span class="sxs-lookup"><span data-stu-id="f6378-214">Leave Type Reason Code</span></span> | <span data-ttu-id="f6378-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="f6378-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="f6378-216">工资单实体</span><span class="sxs-lookup"><span data-stu-id="f6378-216">Payroll entities</span></span>

| <span data-ttu-id="f6378-217">姓名</span><span class="sxs-lookup"><span data-stu-id="f6378-217">Name</span></span> | <span data-ttu-id="f6378-218">实体</span><span class="sxs-lookup"><span data-stu-id="f6378-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f6378-219">付薪周期</span><span class="sxs-lookup"><span data-stu-id="f6378-219">Pay Cycle</span></span> | <span data-ttu-id="f6378-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="f6378-220">cdm_paycycle</span></span> |
| <span data-ttu-id="f6378-221">付薪期间</span><span class="sxs-lookup"><span data-stu-id="f6378-221">Pay Period</span></span> | <span data-ttu-id="f6378-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="f6378-222">cdm_payperiod</span></span> |
| <span data-ttu-id="f6378-223">工资单收入代码</span><span class="sxs-lookup"><span data-stu-id="f6378-223">Payroll Earning Code</span></span> | <span data-ttu-id="f6378-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="f6378-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="f6378-225">银行帐户付款</span><span class="sxs-lookup"><span data-stu-id="f6378-225">Bank Account Disbursement</span></span> | <span data-ttu-id="f6378-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="f6378-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="f6378-227">税区</span><span class="sxs-lookup"><span data-stu-id="f6378-227">Tax Region</span></span> | <span data-ttu-id="f6378-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="f6378-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="f6378-229">工作人员实体</span><span class="sxs-lookup"><span data-stu-id="f6378-229">Worker entities</span></span>

| <span data-ttu-id="f6378-230">姓名</span><span class="sxs-lookup"><span data-stu-id="f6378-230">Name</span></span> | <span data-ttu-id="f6378-231">实体</span><span class="sxs-lookup"><span data-stu-id="f6378-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f6378-232">工作线程</span><span class="sxs-lookup"><span data-stu-id="f6378-232">Worker</span></span> | <span data-ttu-id="f6378-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="f6378-233">cdm_worker</span></span> |
| <span data-ttu-id="f6378-234">工作人员地址</span><span class="sxs-lookup"><span data-stu-id="f6378-234">Worker Address</span></span> | <span data-ttu-id="f6378-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="f6378-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="f6378-236">工作人员个人详细信息</span><span class="sxs-lookup"><span data-stu-id="f6378-236">Worker Personal Detail</span></span> | <span data-ttu-id="f6378-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="f6378-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="f6378-238">工作人员标识号</span><span class="sxs-lookup"><span data-stu-id="f6378-238">Worker Person Identification Number</span></span> | <span data-ttu-id="f6378-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="f6378-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="f6378-240">工作人员标识类型</span><span class="sxs-lookup"><span data-stu-id="f6378-240">Worker Person Identification Type</span></span> | <span data-ttu-id="f6378-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="f6378-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="f6378-242">工作日历</span><span class="sxs-lookup"><span data-stu-id="f6378-242">Work Calendar</span></span> | <span data-ttu-id="f6378-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="f6378-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="f6378-244">工作日历天</span><span class="sxs-lookup"><span data-stu-id="f6378-244">Work Calendar Day</span></span> | <span data-ttu-id="f6378-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="f6378-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="f6378-246">工作日历的假日</span><span class="sxs-lookup"><span data-stu-id="f6378-246">Work Calendar Holiday</span></span> |<span data-ttu-id="f6378-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="f6378-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="f6378-248">工作日历假期行</span><span class="sxs-lookup"><span data-stu-id="f6378-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="f6378-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="f6378-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="f6378-250">工作日历时间间隔</span><span class="sxs-lookup"><span data-stu-id="f6378-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="f6378-251">cdm_workcalendartimeinterval（未启用自定义字段支持）</span><span class="sxs-lookup"><span data-stu-id="f6378-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="f6378-252">工作人员银行帐户</span><span class="sxs-lookup"><span data-stu-id="f6378-252">Worker Bank Account</span></span> | <span data-ttu-id="f6378-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="f6378-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="f6378-254">工作人员设置实体</span><span class="sxs-lookup"><span data-stu-id="f6378-254">Worker setup entities</span></span>

| <span data-ttu-id="f6378-255">姓名</span><span class="sxs-lookup"><span data-stu-id="f6378-255">Name</span></span> | <span data-ttu-id="f6378-256">实体</span><span class="sxs-lookup"><span data-stu-id="f6378-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f6378-257">退伍军人身份</span><span class="sxs-lookup"><span data-stu-id="f6378-257">Veteran Status</span></span> | <span data-ttu-id="f6378-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="f6378-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="f6378-259">所属种族</span><span class="sxs-lookup"><span data-stu-id="f6378-259">Ethnic Origin</span></span> | <span data-ttu-id="f6378-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="f6378-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="f6378-261">原因代码</span><span class="sxs-lookup"><span data-stu-id="f6378-261">Reason Code</span></span> | <span data-ttu-id="f6378-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="f6378-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="f6378-263">人员标识颁发机构</span><span class="sxs-lookup"><span data-stu-id="f6378-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="f6378-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="f6378-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="f6378-265">能力实体</span><span class="sxs-lookup"><span data-stu-id="f6378-265">Competency entities</span></span>

| <span data-ttu-id="f6378-266">姓名</span><span class="sxs-lookup"><span data-stu-id="f6378-266">Name</span></span> | <span data-ttu-id="f6378-267">实体</span><span class="sxs-lookup"><span data-stu-id="f6378-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f6378-268">技能类型</span><span class="sxs-lookup"><span data-stu-id="f6378-268">Skill Type</span></span> | <span data-ttu-id="f6378-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="f6378-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="f6378-270">实体关系模型</span><span class="sxs-lookup"><span data-stu-id="f6378-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="f6378-271">工作线程</span><span class="sxs-lookup"><span data-stu-id="f6378-271">Worker</span></span>

![工作线程](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="f6378-273">工作和工作职位</span><span class="sxs-lookup"><span data-stu-id="f6378-273">Job and Job Position</span></span>

![工作和工作职位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="f6378-275">福利</span><span class="sxs-lookup"><span data-stu-id="f6378-275">Benefits</span></span>

![福利](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="f6378-277">薪酬</span><span class="sxs-lookup"><span data-stu-id="f6378-277">Compensation</span></span>

![薪酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="f6378-279">离开</span><span class="sxs-lookup"><span data-stu-id="f6378-279">Leave</span></span>

![离开](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="f6378-281">工作日历</span><span class="sxs-lookup"><span data-stu-id="f6378-281">Work Calendar</span></span>

![工作日历](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="f6378-283">请参阅</span><span class="sxs-lookup"><span data-stu-id="f6378-283">See also</span></span>

[<span data-ttu-id="f6378-284">选择数据集成技术</span><span class="sxs-lookup"><span data-stu-id="f6378-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="f6378-285">配置 Common Data Service 集成</span><span class="sxs-lookup"><span data-stu-id="f6378-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
