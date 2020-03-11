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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087338"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="2f724-103">Common Data Service 实体</span><span class="sxs-lookup"><span data-stu-id="2f724-103">Common Data Service entities</span></span>

<span data-ttu-id="2f724-104">Microsoft Dynamics 365 Human Resources 使用 Common Data Service 实现可扩展性和集成方案。</span><span class="sxs-lookup"><span data-stu-id="2f724-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="2f724-105">有关 Common Data Service 的详细信息，请参阅[什么是 Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)。</span><span class="sxs-lookup"><span data-stu-id="2f724-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="2f724-106">Common Data Service 中提供以下 Human Resources 实体。</span><span class="sxs-lookup"><span data-stu-id="2f724-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="2f724-107">福利实体</span><span class="sxs-lookup"><span data-stu-id="2f724-107">Benefit entities</span></span>

| <span data-ttu-id="2f724-108">姓名</span><span class="sxs-lookup"><span data-stu-id="2f724-108">Name</span></span> | <span data-ttu-id="2f724-109">实体</span><span class="sxs-lookup"><span data-stu-id="2f724-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2f724-110">福利计算频率</span><span class="sxs-lookup"><span data-stu-id="2f724-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="2f724-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="2f724-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="2f724-112">福利计算频率付薪期间</span><span class="sxs-lookup"><span data-stu-id="2f724-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="2f724-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="2f724-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="2f724-114">福利计算比率</span><span class="sxs-lookup"><span data-stu-id="2f724-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="2f724-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="2f724-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="2f724-116">福利计算比率详细信息</span><span class="sxs-lookup"><span data-stu-id="2f724-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="2f724-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="2f724-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="2f724-118">福利选项</span><span class="sxs-lookup"><span data-stu-id="2f724-118">Benefit Option</span></span> | <span data-ttu-id="2f724-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="2f724-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="2f724-120">福利计划</span><span class="sxs-lookup"><span data-stu-id="2f724-120">Benefit Plan</span></span> | <span data-ttu-id="2f724-121">cdm_benefitplan（未启用自定义字段支持）</span><span class="sxs-lookup"><span data-stu-id="2f724-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="2f724-122">福利类型</span><span class="sxs-lookup"><span data-stu-id="2f724-122">Benefit Type</span></span> | <span data-ttu-id="2f724-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="2f724-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="2f724-124">业务流程任务实体</span><span class="sxs-lookup"><span data-stu-id="2f724-124">Business process tasks entities</span></span>

| <span data-ttu-id="2f724-125">姓名</span><span class="sxs-lookup"><span data-stu-id="2f724-125">Name</span></span> | <span data-ttu-id="2f724-126">实体</span><span class="sxs-lookup"><span data-stu-id="2f724-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2f724-127">业务流程日历</span><span class="sxs-lookup"><span data-stu-id="2f724-127">Business Process Calendar</span></span> | <span data-ttu-id="2f724-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="2f724-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="2f724-129">业务流程组分配</span><span class="sxs-lookup"><span data-stu-id="2f724-129">Business Process Group Assignment</span></span> | <span data-ttu-id="2f724-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="2f724-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="2f724-131">业务流程库任务组</span><span class="sxs-lookup"><span data-stu-id="2f724-131">Business Process Library Task Group</span></span> | <span data-ttu-id="2f724-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="2f724-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="2f724-133">业务流程阶段</span><span class="sxs-lookup"><span data-stu-id="2f724-133">Business Process Stage</span></span> | <span data-ttu-id="2f724-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="2f724-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="2f724-135">核对清单模板标题</span><span class="sxs-lookup"><span data-stu-id="2f724-135">Checklist Template Header</span></span> | <span data-ttu-id="2f724-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="2f724-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="2f724-137">核对清单模板任务</span><span class="sxs-lookup"><span data-stu-id="2f724-137">Checklist Template Task</span></span> | <span data-ttu-id="2f724-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="2f724-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="2f724-139">薪酬实体</span><span class="sxs-lookup"><span data-stu-id="2f724-139">Compensation entities</span></span>

| <span data-ttu-id="2f724-140">姓名</span><span class="sxs-lookup"><span data-stu-id="2f724-140">Name</span></span> | <span data-ttu-id="2f724-141">实体</span><span class="sxs-lookup"><span data-stu-id="2f724-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2f724-142">薪酬固定计划</span><span class="sxs-lookup"><span data-stu-id="2f724-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="2f724-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="2f724-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="2f724-144">薪酬网格</span><span class="sxs-lookup"><span data-stu-id="2f724-144">Compensation Grid</span></span> | <span data-ttu-id="2f724-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="2f724-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="2f724-146">薪酬级别</span><span class="sxs-lookup"><span data-stu-id="2f724-146">Compensation Level</span></span> | <span data-ttu-id="2f724-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="2f724-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="2f724-148">薪酬付薪频率</span><span class="sxs-lookup"><span data-stu-id="2f724-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="2f724-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="2f724-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="2f724-150">薪酬参考点设置</span><span class="sxs-lookup"><span data-stu-id="2f724-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="2f724-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="2f724-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="2f724-152">薪酬参考点设置行</span><span class="sxs-lookup"><span data-stu-id="2f724-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="2f724-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="2f724-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="2f724-154">薪酬区域</span><span class="sxs-lookup"><span data-stu-id="2f724-154">Compensation Region</span></span> | <span data-ttu-id="2f724-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="2f724-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="2f724-156">薪酬结构</span><span class="sxs-lookup"><span data-stu-id="2f724-156">Compensation Structure</span></span> | <span data-ttu-id="2f724-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="2f724-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="2f724-158">可变薪酬计划</span><span class="sxs-lookup"><span data-stu-id="2f724-158">Compensation Variable Plan</span></span> | <span data-ttu-id="2f724-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="2f724-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="2f724-160">可变薪酬计划级别</span><span class="sxs-lookup"><span data-stu-id="2f724-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="2f724-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="2f724-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="2f724-162">可变薪酬计划类型</span><span class="sxs-lookup"><span data-stu-id="2f724-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="2f724-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="2f724-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="2f724-164">固定薪酬事件</span><span class="sxs-lookup"><span data-stu-id="2f724-164">Fixed Compensation Event</span></span> | <span data-ttu-id="2f724-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="2f724-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="2f724-166">股份行权规则</span><span class="sxs-lookup"><span data-stu-id="2f724-166">Vesting Rule</span></span> | <span data-ttu-id="2f724-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="2f724-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="2f724-168">工作人员固定薪酬</span><span class="sxs-lookup"><span data-stu-id="2f724-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="2f724-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="2f724-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="2f724-170">组织实体</span><span class="sxs-lookup"><span data-stu-id="2f724-170">Organization entities</span></span>

| <span data-ttu-id="2f724-171">姓名</span><span class="sxs-lookup"><span data-stu-id="2f724-171">Name</span></span> | <span data-ttu-id="2f724-172">实体</span><span class="sxs-lookup"><span data-stu-id="2f724-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2f724-173">部门</span><span class="sxs-lookup"><span data-stu-id="2f724-173">Department</span></span> | <span data-ttu-id="2f724-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="2f724-174">cdm_department</span></span> |
| <span data-ttu-id="2f724-175">雇用</span><span class="sxs-lookup"><span data-stu-id="2f724-175">Employment</span></span> | <span data-ttu-id="2f724-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="2f724-176">cdm_employment</span></span> |
| <span data-ttu-id="2f724-177">公司</span><span class="sxs-lookup"><span data-stu-id="2f724-177">Company</span></span> | <span data-ttu-id="2f724-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="2f724-178">cdm_company</span></span> |
| <span data-ttu-id="2f724-179">职位</span><span class="sxs-lookup"><span data-stu-id="2f724-179">Job</span></span> | <span data-ttu-id="2f724-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="2f724-180">cdm_job</span></span> |
| <span data-ttu-id="2f724-181">工作职能</span><span class="sxs-lookup"><span data-stu-id="2f724-181">Job Function</span></span> | <span data-ttu-id="2f724-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="2f724-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="2f724-183">工作职位</span><span class="sxs-lookup"><span data-stu-id="2f724-183">Job Position</span></span> | <span data-ttu-id="2f724-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="2f724-184">cdm_jobposition</span></span> |
| <span data-ttu-id="2f724-185">职位类型</span><span class="sxs-lookup"><span data-stu-id="2f724-185">Position Type</span></span> | <span data-ttu-id="2f724-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="2f724-186">cdm_positiontype</span></span> |
| <span data-ttu-id="2f724-187">职位工作人员分配</span><span class="sxs-lookup"><span data-stu-id="2f724-187">Position Worker Assignment</span></span> | <span data-ttu-id="2f724-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="2f724-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="2f724-189">工作类型</span><span class="sxs-lookup"><span data-stu-id="2f724-189">Job Type</span></span> | <span data-ttu-id="2f724-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="2f724-190">cdm_jobtype</span></span> |
| <span data-ttu-id="2f724-191">语言</span><span class="sxs-lookup"><span data-stu-id="2f724-191">Language</span></span> | <span data-ttu-id="2f724-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="2f724-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="2f724-193">休假和缺勤实体</span><span class="sxs-lookup"><span data-stu-id="2f724-193">Leave and absence entities</span></span>

| <span data-ttu-id="2f724-194">姓名</span><span class="sxs-lookup"><span data-stu-id="2f724-194">Name</span></span> | <span data-ttu-id="2f724-195">实体</span><span class="sxs-lookup"><span data-stu-id="2f724-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2f724-196">休假银行交易记录</span><span class="sxs-lookup"><span data-stu-id="2f724-196">Leave Bank Transaction</span></span> | <span data-ttu-id="2f724-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="2f724-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="2f724-198">休假登记</span><span class="sxs-lookup"><span data-stu-id="2f724-198">Leave Enrollment</span></span> | <span data-ttu-id="2f724-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="2f724-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="2f724-200">休假计划</span><span class="sxs-lookup"><span data-stu-id="2f724-200">Leave Plan</span></span> | <span data-ttu-id="2f724-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="2f724-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="2f724-202">休假请求</span><span class="sxs-lookup"><span data-stu-id="2f724-202">Leave Request</span></span> | <span data-ttu-id="2f724-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="2f724-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="2f724-204">休假请求详细信息</span><span class="sxs-lookup"><span data-stu-id="2f724-204">Leave Request Detail</span></span> | <span data-ttu-id="2f724-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="2f724-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="2f724-206">休假类型</span><span class="sxs-lookup"><span data-stu-id="2f724-206">Leave Type</span></span> | <span data-ttu-id="2f724-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="2f724-207">cdm_leavetype</span></span> |
| <span data-ttu-id="2f724-208">休假类型原因代码</span><span class="sxs-lookup"><span data-stu-id="2f724-208">Leave Type Reason Code</span></span> | <span data-ttu-id="2f724-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="2f724-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="2f724-210">工资单实体</span><span class="sxs-lookup"><span data-stu-id="2f724-210">Payroll entities</span></span>

| <span data-ttu-id="2f724-211">姓名</span><span class="sxs-lookup"><span data-stu-id="2f724-211">Name</span></span> | <span data-ttu-id="2f724-212">实体</span><span class="sxs-lookup"><span data-stu-id="2f724-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2f724-213">付薪周期</span><span class="sxs-lookup"><span data-stu-id="2f724-213">Pay Cycle</span></span> | <span data-ttu-id="2f724-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="2f724-214">cdm_paycycle</span></span> |
| <span data-ttu-id="2f724-215">付薪期间</span><span class="sxs-lookup"><span data-stu-id="2f724-215">Pay Period</span></span> | <span data-ttu-id="2f724-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="2f724-216">cdm_payperiod</span></span> |
| <span data-ttu-id="2f724-217">工资单收入代码</span><span class="sxs-lookup"><span data-stu-id="2f724-217">Payroll Earning Code</span></span> | <span data-ttu-id="2f724-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="2f724-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="2f724-219">银行帐户付款</span><span class="sxs-lookup"><span data-stu-id="2f724-219">Bank Account Disbursement</span></span> | <span data-ttu-id="2f724-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="2f724-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="2f724-221">税区</span><span class="sxs-lookup"><span data-stu-id="2f724-221">Tax Region</span></span> | <span data-ttu-id="2f724-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="2f724-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="2f724-223">工作人员实体</span><span class="sxs-lookup"><span data-stu-id="2f724-223">Worker entities</span></span>

| <span data-ttu-id="2f724-224">姓名</span><span class="sxs-lookup"><span data-stu-id="2f724-224">Name</span></span> | <span data-ttu-id="2f724-225">实体</span><span class="sxs-lookup"><span data-stu-id="2f724-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2f724-226">工作线程</span><span class="sxs-lookup"><span data-stu-id="2f724-226">Worker</span></span> | <span data-ttu-id="2f724-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="2f724-227">cdm_worker</span></span> |
| <span data-ttu-id="2f724-228">工作人员地址</span><span class="sxs-lookup"><span data-stu-id="2f724-228">Worker Address</span></span> | <span data-ttu-id="2f724-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="2f724-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="2f724-230">工作人员个人详细信息</span><span class="sxs-lookup"><span data-stu-id="2f724-230">Worker Personal Detail</span></span> | <span data-ttu-id="2f724-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="2f724-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="2f724-232">工作人员标识号</span><span class="sxs-lookup"><span data-stu-id="2f724-232">Worker Person Identification Number</span></span> | <span data-ttu-id="2f724-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="2f724-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="2f724-234">工作人员标识类型</span><span class="sxs-lookup"><span data-stu-id="2f724-234">Worker Person Identification Type</span></span> | <span data-ttu-id="2f724-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="2f724-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="2f724-236">工作日历</span><span class="sxs-lookup"><span data-stu-id="2f724-236">Work Calendar</span></span> | <span data-ttu-id="2f724-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="2f724-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="2f724-238">工作日历天</span><span class="sxs-lookup"><span data-stu-id="2f724-238">Work Calendar Day</span></span> | <span data-ttu-id="2f724-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="2f724-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="2f724-240">工作日历的假日</span><span class="sxs-lookup"><span data-stu-id="2f724-240">Work Calendar Holiday</span></span> |<span data-ttu-id="2f724-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="2f724-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="2f724-242">工作日历假期行</span><span class="sxs-lookup"><span data-stu-id="2f724-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="2f724-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="2f724-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="2f724-244">工作日历时间间隔</span><span class="sxs-lookup"><span data-stu-id="2f724-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="2f724-245">cdm_workcalendartimeinterval（未启用自定义字段支持）</span><span class="sxs-lookup"><span data-stu-id="2f724-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="2f724-246">工作人员银行帐户</span><span class="sxs-lookup"><span data-stu-id="2f724-246">Worker Bank Account</span></span> | <span data-ttu-id="2f724-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="2f724-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="2f724-248">工作人员设置实体</span><span class="sxs-lookup"><span data-stu-id="2f724-248">Worker setup entities</span></span>

| <span data-ttu-id="2f724-249">姓名</span><span class="sxs-lookup"><span data-stu-id="2f724-249">Name</span></span> | <span data-ttu-id="2f724-250">实体</span><span class="sxs-lookup"><span data-stu-id="2f724-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2f724-251">退伍军人身份</span><span class="sxs-lookup"><span data-stu-id="2f724-251">Veteran Status</span></span> | <span data-ttu-id="2f724-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="2f724-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="2f724-253">所属种族</span><span class="sxs-lookup"><span data-stu-id="2f724-253">Ethnic Origin</span></span> | <span data-ttu-id="2f724-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="2f724-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="2f724-255">原因代码</span><span class="sxs-lookup"><span data-stu-id="2f724-255">Reason Code</span></span> | <span data-ttu-id="2f724-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="2f724-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="2f724-257">人员标识颁发机构</span><span class="sxs-lookup"><span data-stu-id="2f724-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="2f724-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="2f724-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="2f724-259">能力实体</span><span class="sxs-lookup"><span data-stu-id="2f724-259">Competency entities</span></span>

| <span data-ttu-id="2f724-260">姓名</span><span class="sxs-lookup"><span data-stu-id="2f724-260">Name</span></span> | <span data-ttu-id="2f724-261">实体</span><span class="sxs-lookup"><span data-stu-id="2f724-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="2f724-262">技能类型</span><span class="sxs-lookup"><span data-stu-id="2f724-262">Skill Type</span></span> | <span data-ttu-id="2f724-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="2f724-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="2f724-264">实体关系模型</span><span class="sxs-lookup"><span data-stu-id="2f724-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="2f724-265">工作线程</span><span class="sxs-lookup"><span data-stu-id="2f724-265">Worker</span></span>

![工作线程](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="2f724-267">工作和工作职位</span><span class="sxs-lookup"><span data-stu-id="2f724-267">Job and Job Position</span></span>

![工作和工作职位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="2f724-269">福利</span><span class="sxs-lookup"><span data-stu-id="2f724-269">Benefits</span></span>

![福利](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="2f724-271">薪酬</span><span class="sxs-lookup"><span data-stu-id="2f724-271">Compensation</span></span>

![薪酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="2f724-273">离开</span><span class="sxs-lookup"><span data-stu-id="2f724-273">Leave</span></span>

![离开](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="2f724-275">工作日历</span><span class="sxs-lookup"><span data-stu-id="2f724-275">Work Calendar</span></span>

![工作日历](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="2f724-277">请参阅</span><span class="sxs-lookup"><span data-stu-id="2f724-277">See also</span></span>

[<span data-ttu-id="2f724-278">选择数据集成技术</span><span class="sxs-lookup"><span data-stu-id="2f724-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="2f724-279">配置 Common Data Service 集成</span><span class="sxs-lookup"><span data-stu-id="2f724-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)