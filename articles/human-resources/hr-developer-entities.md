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
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166490"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="7cb1b-103">Common Data Service 实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-103">Common Data Service entities</span></span>

<span data-ttu-id="7cb1b-104">Microsoft Dynamics 365 Human Resources 使用 Common Data Service 实现可扩展性和集成方案。</span><span class="sxs-lookup"><span data-stu-id="7cb1b-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="7cb1b-105">有关 Common Data Service 的详细信息，请参阅[什么是 Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)。</span><span class="sxs-lookup"><span data-stu-id="7cb1b-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="7cb1b-106">Common Data Service 中提供以下 Human Resources 实体。</span><span class="sxs-lookup"><span data-stu-id="7cb1b-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="7cb1b-107">福利实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-107">Benefit entities</span></span>

| <span data-ttu-id="7cb1b-108">姓名</span><span class="sxs-lookup"><span data-stu-id="7cb1b-108">Name</span></span> | <span data-ttu-id="7cb1b-109">实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7cb1b-110">福利计算频率</span><span class="sxs-lookup"><span data-stu-id="7cb1b-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="7cb1b-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="7cb1b-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="7cb1b-112">福利计算频率付薪期间</span><span class="sxs-lookup"><span data-stu-id="7cb1b-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="7cb1b-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="7cb1b-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="7cb1b-114">福利计算比率</span><span class="sxs-lookup"><span data-stu-id="7cb1b-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="7cb1b-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="7cb1b-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="7cb1b-116">福利计算比率详细信息</span><span class="sxs-lookup"><span data-stu-id="7cb1b-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="7cb1b-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="7cb1b-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="7cb1b-118">福利选项</span><span class="sxs-lookup"><span data-stu-id="7cb1b-118">Benefit Option</span></span> | <span data-ttu-id="7cb1b-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="7cb1b-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="7cb1b-120">福利计划</span><span class="sxs-lookup"><span data-stu-id="7cb1b-120">Benefit Plan</span></span> | <span data-ttu-id="7cb1b-121">cdm_benefitplan（未启用自定义字段支持）</span><span class="sxs-lookup"><span data-stu-id="7cb1b-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="7cb1b-122">福利类型</span><span class="sxs-lookup"><span data-stu-id="7cb1b-122">Benefit Type</span></span> | <span data-ttu-id="7cb1b-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="7cb1b-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="7cb1b-124">业务流程任务实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-124">Business process tasks entities</span></span>

| <span data-ttu-id="7cb1b-125">姓名</span><span class="sxs-lookup"><span data-stu-id="7cb1b-125">Name</span></span> | <span data-ttu-id="7cb1b-126">实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7cb1b-127">业务流程日历</span><span class="sxs-lookup"><span data-stu-id="7cb1b-127">Business Process Calendar</span></span> | <span data-ttu-id="7cb1b-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="7cb1b-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="7cb1b-129">业务流程组分配</span><span class="sxs-lookup"><span data-stu-id="7cb1b-129">Business Process Group Assignment</span></span> | <span data-ttu-id="7cb1b-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="7cb1b-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="7cb1b-131">业务流程库任务组</span><span class="sxs-lookup"><span data-stu-id="7cb1b-131">Business Process Library Task Group</span></span> | <span data-ttu-id="7cb1b-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="7cb1b-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="7cb1b-133">业务流程阶段</span><span class="sxs-lookup"><span data-stu-id="7cb1b-133">Business Process Stage</span></span> | <span data-ttu-id="7cb1b-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="7cb1b-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="7cb1b-135">核对清单模板标题</span><span class="sxs-lookup"><span data-stu-id="7cb1b-135">Checklist Template Header</span></span> | <span data-ttu-id="7cb1b-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="7cb1b-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="7cb1b-137">核对清单模板任务</span><span class="sxs-lookup"><span data-stu-id="7cb1b-137">Checklist Template Task</span></span> | <span data-ttu-id="7cb1b-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="7cb1b-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="7cb1b-139">薪酬实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-139">Compensation entities</span></span>

| <span data-ttu-id="7cb1b-140">姓名</span><span class="sxs-lookup"><span data-stu-id="7cb1b-140">Name</span></span> | <span data-ttu-id="7cb1b-141">实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7cb1b-142">薪酬固定计划</span><span class="sxs-lookup"><span data-stu-id="7cb1b-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="7cb1b-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="7cb1b-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="7cb1b-144">薪酬网格</span><span class="sxs-lookup"><span data-stu-id="7cb1b-144">Compensation Grid</span></span> | <span data-ttu-id="7cb1b-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="7cb1b-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="7cb1b-146">薪酬级别</span><span class="sxs-lookup"><span data-stu-id="7cb1b-146">Compensation Level</span></span> | <span data-ttu-id="7cb1b-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="7cb1b-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="7cb1b-148">薪酬付薪频率</span><span class="sxs-lookup"><span data-stu-id="7cb1b-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="7cb1b-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="7cb1b-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="7cb1b-150">薪酬参考点设置</span><span class="sxs-lookup"><span data-stu-id="7cb1b-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="7cb1b-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="7cb1b-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="7cb1b-152">薪酬参考点设置行</span><span class="sxs-lookup"><span data-stu-id="7cb1b-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="7cb1b-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="7cb1b-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="7cb1b-154">薪酬区域</span><span class="sxs-lookup"><span data-stu-id="7cb1b-154">Compensation Region</span></span> | <span data-ttu-id="7cb1b-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="7cb1b-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="7cb1b-156">薪酬结构</span><span class="sxs-lookup"><span data-stu-id="7cb1b-156">Compensation Structure</span></span> | <span data-ttu-id="7cb1b-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="7cb1b-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="7cb1b-158">可变薪酬计划</span><span class="sxs-lookup"><span data-stu-id="7cb1b-158">Compensation Variable Plan</span></span> | <span data-ttu-id="7cb1b-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="7cb1b-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="7cb1b-160">可变薪酬计划级别</span><span class="sxs-lookup"><span data-stu-id="7cb1b-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="7cb1b-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="7cb1b-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="7cb1b-162">可变薪酬计划类型</span><span class="sxs-lookup"><span data-stu-id="7cb1b-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="7cb1b-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="7cb1b-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="7cb1b-164">固定薪酬事件</span><span class="sxs-lookup"><span data-stu-id="7cb1b-164">Fixed Compensation Event</span></span> | <span data-ttu-id="7cb1b-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="7cb1b-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="7cb1b-166">股份行权规则</span><span class="sxs-lookup"><span data-stu-id="7cb1b-166">Vesting Rule</span></span> | <span data-ttu-id="7cb1b-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="7cb1b-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="7cb1b-168">工作人员固定薪酬</span><span class="sxs-lookup"><span data-stu-id="7cb1b-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="7cb1b-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="7cb1b-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="7cb1b-170">组织实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-170">Organization entities</span></span>

| <span data-ttu-id="7cb1b-171">姓名</span><span class="sxs-lookup"><span data-stu-id="7cb1b-171">Name</span></span> | <span data-ttu-id="7cb1b-172">实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7cb1b-173">部门</span><span class="sxs-lookup"><span data-stu-id="7cb1b-173">Department</span></span> | <span data-ttu-id="7cb1b-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="7cb1b-174">cdm_department</span></span> |
| <span data-ttu-id="7cb1b-175">雇用</span><span class="sxs-lookup"><span data-stu-id="7cb1b-175">Employment</span></span> | <span data-ttu-id="7cb1b-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="7cb1b-176">cdm_employment</span></span> |
| <span data-ttu-id="7cb1b-177">公司</span><span class="sxs-lookup"><span data-stu-id="7cb1b-177">Company</span></span> | <span data-ttu-id="7cb1b-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="7cb1b-178">cdm_company</span></span> |
| <span data-ttu-id="7cb1b-179">职位</span><span class="sxs-lookup"><span data-stu-id="7cb1b-179">Job</span></span> | <span data-ttu-id="7cb1b-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="7cb1b-180">cdm_job</span></span> |
| <span data-ttu-id="7cb1b-181">工作职能</span><span class="sxs-lookup"><span data-stu-id="7cb1b-181">Job Function</span></span> | <span data-ttu-id="7cb1b-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="7cb1b-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="7cb1b-183">工作职位</span><span class="sxs-lookup"><span data-stu-id="7cb1b-183">Job Position</span></span> | <span data-ttu-id="7cb1b-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="7cb1b-184">cdm_jobposition</span></span> |
| <span data-ttu-id="7cb1b-185">职位类型</span><span class="sxs-lookup"><span data-stu-id="7cb1b-185">Position Type</span></span> | <span data-ttu-id="7cb1b-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="7cb1b-186">cdm_positiontype</span></span> |
| <span data-ttu-id="7cb1b-187">职位工作人员分配</span><span class="sxs-lookup"><span data-stu-id="7cb1b-187">Position Worker Assignment</span></span> | <span data-ttu-id="7cb1b-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="7cb1b-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="7cb1b-189">工作职位维度</span><span class="sxs-lookup"><span data-stu-id="7cb1b-189">Job Position Dimension</span></span> | <span data-ttu-id="7cb1b-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="7cb1b-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="7cb1b-191">工作类型</span><span class="sxs-lookup"><span data-stu-id="7cb1b-191">Job Type</span></span> | <span data-ttu-id="7cb1b-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="7cb1b-192">cdm_jobtype</span></span> |
| <span data-ttu-id="7cb1b-193">语言</span><span class="sxs-lookup"><span data-stu-id="7cb1b-193">Language</span></span> | <span data-ttu-id="7cb1b-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="7cb1b-194">cdm_language</span></span> |
| <span data-ttu-id="7cb1b-195">职位</span><span class="sxs-lookup"><span data-stu-id="7cb1b-195">Title</span></span> | <span data-ttu-id="7cb1b-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="7cb1b-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="7cb1b-197">**职位类型**、**职位工作人员分配**和**雇用**的财务维度提供到 Common Data Service 的单向集成。</span><span class="sxs-lookup"><span data-stu-id="7cb1b-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="7cb1b-198">财务维度更新现在不能从 Common Data Service 同步到 Human Resources。</span><span class="sxs-lookup"><span data-stu-id="7cb1b-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="7cb1b-199">休假和缺勤实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-199">Leave and absence entities</span></span>

| <span data-ttu-id="7cb1b-200">姓名</span><span class="sxs-lookup"><span data-stu-id="7cb1b-200">Name</span></span> | <span data-ttu-id="7cb1b-201">实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7cb1b-202">休假银行交易记录</span><span class="sxs-lookup"><span data-stu-id="7cb1b-202">Leave Bank Transaction</span></span> | <span data-ttu-id="7cb1b-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="7cb1b-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="7cb1b-204">休假登记</span><span class="sxs-lookup"><span data-stu-id="7cb1b-204">Leave Enrollment</span></span> | <span data-ttu-id="7cb1b-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="7cb1b-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="7cb1b-206">休假计划</span><span class="sxs-lookup"><span data-stu-id="7cb1b-206">Leave Plan</span></span> | <span data-ttu-id="7cb1b-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="7cb1b-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="7cb1b-208">休假请求</span><span class="sxs-lookup"><span data-stu-id="7cb1b-208">Leave Request</span></span> | <span data-ttu-id="7cb1b-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="7cb1b-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="7cb1b-210">休假请求详细信息</span><span class="sxs-lookup"><span data-stu-id="7cb1b-210">Leave Request Detail</span></span> | <span data-ttu-id="7cb1b-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="7cb1b-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="7cb1b-212">休假类型</span><span class="sxs-lookup"><span data-stu-id="7cb1b-212">Leave Type</span></span> | <span data-ttu-id="7cb1b-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="7cb1b-213">cdm_leavetype</span></span> |
| <span data-ttu-id="7cb1b-214">休假类型原因代码</span><span class="sxs-lookup"><span data-stu-id="7cb1b-214">Leave Type Reason Code</span></span> | <span data-ttu-id="7cb1b-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="7cb1b-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="7cb1b-216">工资单实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-216">Payroll entities</span></span>

| <span data-ttu-id="7cb1b-217">姓名</span><span class="sxs-lookup"><span data-stu-id="7cb1b-217">Name</span></span> | <span data-ttu-id="7cb1b-218">实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7cb1b-219">付薪周期</span><span class="sxs-lookup"><span data-stu-id="7cb1b-219">Pay Cycle</span></span> | <span data-ttu-id="7cb1b-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="7cb1b-220">cdm_paycycle</span></span> |
| <span data-ttu-id="7cb1b-221">付薪期间</span><span class="sxs-lookup"><span data-stu-id="7cb1b-221">Pay Period</span></span> | <span data-ttu-id="7cb1b-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="7cb1b-222">cdm_payperiod</span></span> |
| <span data-ttu-id="7cb1b-223">工资单收入代码</span><span class="sxs-lookup"><span data-stu-id="7cb1b-223">Payroll Earning Code</span></span> | <span data-ttu-id="7cb1b-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="7cb1b-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="7cb1b-225">银行帐户付款</span><span class="sxs-lookup"><span data-stu-id="7cb1b-225">Bank Account Disbursement</span></span> | <span data-ttu-id="7cb1b-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="7cb1b-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="7cb1b-227">税区</span><span class="sxs-lookup"><span data-stu-id="7cb1b-227">Tax Region</span></span> | <span data-ttu-id="7cb1b-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="7cb1b-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="7cb1b-229">工作人员实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-229">Worker entities</span></span>

| <span data-ttu-id="7cb1b-230">姓名</span><span class="sxs-lookup"><span data-stu-id="7cb1b-230">Name</span></span> | <span data-ttu-id="7cb1b-231">实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7cb1b-232">工作线程</span><span class="sxs-lookup"><span data-stu-id="7cb1b-232">Worker</span></span> | <span data-ttu-id="7cb1b-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="7cb1b-233">cdm_worker</span></span> |
| <span data-ttu-id="7cb1b-234">工作人员地址</span><span class="sxs-lookup"><span data-stu-id="7cb1b-234">Worker Address</span></span> | <span data-ttu-id="7cb1b-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="7cb1b-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="7cb1b-236">工作人员个人详细信息</span><span class="sxs-lookup"><span data-stu-id="7cb1b-236">Worker Personal Detail</span></span> | <span data-ttu-id="7cb1b-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="7cb1b-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="7cb1b-238">工作人员标识号</span><span class="sxs-lookup"><span data-stu-id="7cb1b-238">Worker Person Identification Number</span></span> | <span data-ttu-id="7cb1b-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="7cb1b-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="7cb1b-240">工作人员标识类型</span><span class="sxs-lookup"><span data-stu-id="7cb1b-240">Worker Person Identification Type</span></span> | <span data-ttu-id="7cb1b-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="7cb1b-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="7cb1b-242">工作日历</span><span class="sxs-lookup"><span data-stu-id="7cb1b-242">Work Calendar</span></span> | <span data-ttu-id="7cb1b-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="7cb1b-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="7cb1b-244">工作日历天</span><span class="sxs-lookup"><span data-stu-id="7cb1b-244">Work Calendar Day</span></span> | <span data-ttu-id="7cb1b-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="7cb1b-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="7cb1b-246">工作日历的假日</span><span class="sxs-lookup"><span data-stu-id="7cb1b-246">Work Calendar Holiday</span></span> |<span data-ttu-id="7cb1b-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="7cb1b-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="7cb1b-248">工作日历假期行</span><span class="sxs-lookup"><span data-stu-id="7cb1b-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="7cb1b-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="7cb1b-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="7cb1b-250">工作日历时间间隔</span><span class="sxs-lookup"><span data-stu-id="7cb1b-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="7cb1b-251">cdm_workcalendartimeinterval（未启用自定义字段支持）</span><span class="sxs-lookup"><span data-stu-id="7cb1b-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="7cb1b-252">工作人员银行帐户</span><span class="sxs-lookup"><span data-stu-id="7cb1b-252">Worker Bank Account</span></span> | <span data-ttu-id="7cb1b-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="7cb1b-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="7cb1b-254">工作人员设置实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-254">Worker setup entities</span></span>

| <span data-ttu-id="7cb1b-255">姓名</span><span class="sxs-lookup"><span data-stu-id="7cb1b-255">Name</span></span> | <span data-ttu-id="7cb1b-256">实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7cb1b-257">退伍军人身份</span><span class="sxs-lookup"><span data-stu-id="7cb1b-257">Veteran Status</span></span> | <span data-ttu-id="7cb1b-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="7cb1b-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="7cb1b-259">所属种族</span><span class="sxs-lookup"><span data-stu-id="7cb1b-259">Ethnic Origin</span></span> | <span data-ttu-id="7cb1b-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="7cb1b-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="7cb1b-261">原因代码</span><span class="sxs-lookup"><span data-stu-id="7cb1b-261">Reason Code</span></span> | <span data-ttu-id="7cb1b-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="7cb1b-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="7cb1b-263">人员标识颁发机构</span><span class="sxs-lookup"><span data-stu-id="7cb1b-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="7cb1b-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="7cb1b-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="7cb1b-265">能力实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-265">Competency entities</span></span>

| <span data-ttu-id="7cb1b-266">姓名</span><span class="sxs-lookup"><span data-stu-id="7cb1b-266">Name</span></span> | <span data-ttu-id="7cb1b-267">实体</span><span class="sxs-lookup"><span data-stu-id="7cb1b-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="7cb1b-268">技能类型</span><span class="sxs-lookup"><span data-stu-id="7cb1b-268">Skill Type</span></span> | <span data-ttu-id="7cb1b-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="7cb1b-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="7cb1b-270">实体关系模型</span><span class="sxs-lookup"><span data-stu-id="7cb1b-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="7cb1b-271">工作线程</span><span class="sxs-lookup"><span data-stu-id="7cb1b-271">Worker</span></span>

![工作线程](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="7cb1b-273">工作和工作职位</span><span class="sxs-lookup"><span data-stu-id="7cb1b-273">Job and Job Position</span></span>

![工作和工作职位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="7cb1b-275">福利</span><span class="sxs-lookup"><span data-stu-id="7cb1b-275">Benefits</span></span>

![福利](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="7cb1b-277">薪酬</span><span class="sxs-lookup"><span data-stu-id="7cb1b-277">Compensation</span></span>

![薪酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="7cb1b-279">离开</span><span class="sxs-lookup"><span data-stu-id="7cb1b-279">Leave</span></span>

![离开](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="7cb1b-281">工作日历</span><span class="sxs-lookup"><span data-stu-id="7cb1b-281">Work Calendar</span></span>

![工作日历](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="7cb1b-283">请参阅</span><span class="sxs-lookup"><span data-stu-id="7cb1b-283">See also</span></span>

[<span data-ttu-id="7cb1b-284">选择数据集成技术</span><span class="sxs-lookup"><span data-stu-id="7cb1b-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="7cb1b-285">配置 Common Data Service 集成</span><span class="sxs-lookup"><span data-stu-id="7cb1b-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
