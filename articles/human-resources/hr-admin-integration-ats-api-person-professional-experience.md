---
title: 人员专业经验
description: 本主题介绍 Dynamics 365 Human Resources 的“人员专业经验”实体。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7cb728a29ccf6c23a227e63edd6bb5226d2ffdd0
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053699"
---
# <a name="person-professional-experience"></a><span data-ttu-id="81b36-103">人员专业经验</span><span class="sxs-lookup"><span data-stu-id="81b36-103">Person professional experience</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="81b36-104">本主题介绍 Dynamics 365 Human Resources 的“人员专业经验”实体。</span><span class="sxs-lookup"><span data-stu-id="81b36-104">This topic describes the Person professional experience entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="81b36-105">物理名称：mshr_hcmpersonprofessionalexperienceentity</span><span class="sxs-lookup"><span data-stu-id="81b36-105">Physical name: mshr_hcmpersonprofessionalexperienceentity</span></span>

## <a name="description"></a><span data-ttu-id="81b36-106">说明</span><span class="sxs-lookup"><span data-stu-id="81b36-106">Description</span></span>

<span data-ttu-id="81b36-107">此实体描述应聘者的专业经验或工作经历。</span><span class="sxs-lookup"><span data-stu-id="81b36-107">This entity describes professional experience or work history of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="81b36-108">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="81b36-108">JSON representation</span></span>

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="81b36-109">属性</span><span class="sxs-lookup"><span data-stu-id="81b36-109">Properties</span></span>

| <span data-ttu-id="81b36-110">属性</span><span class="sxs-lookup"><span data-stu-id="81b36-110">Property</span></span><br><span data-ttu-id="81b36-111">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="81b36-111">**Physical name**</span></span><br><span data-ttu-id="81b36-112">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="81b36-112">**_Type_**</span></span> | <span data-ttu-id="81b36-113">使用</span><span class="sxs-lookup"><span data-stu-id="81b36-113">Use</span></span> | <span data-ttu-id="81b36-114">说明</span><span class="sxs-lookup"><span data-stu-id="81b36-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="81b36-115">**人员专业经验实体 ID**</span><span class="sxs-lookup"><span data-stu-id="81b36-115">**Person Professional Experience Entity ID**</span></span><br><span data-ttu-id="81b36-116">mshr_hcmpersonprofessionalexperienceentityid</span><span class="sxs-lookup"><span data-stu-id="81b36-116">mshr_hcmpersonprofessionalexperienceentityid</span></span><br><span data-ttu-id="81b36-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="81b36-117">*GUID*</span></span> | <span data-ttu-id="81b36-118">只读</span><span class="sxs-lookup"><span data-stu-id="81b36-118">Read-only</span></span><br><span data-ttu-id="81b36-119">必填</span><span class="sxs-lookup"><span data-stu-id="81b36-119">Required</span></span> | <span data-ttu-id="81b36-120">系统生成的实体记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="81b36-120">System-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="81b36-121">**当事方编号**</span><span class="sxs-lookup"><span data-stu-id="81b36-121">**Party Number**</span></span><br><span data-ttu-id="81b36-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="81b36-122">mshr_partynumber</span></span><br><span data-ttu-id="81b36-123">*字符串*</span><span class="sxs-lookup"><span data-stu-id="81b36-123">*String*</span></span> | <span data-ttu-id="81b36-124">读/写</span><span class="sxs-lookup"><span data-stu-id="81b36-124">Read/write</span></span><br><span data-ttu-id="81b36-125">必填</span><span class="sxs-lookup"><span data-stu-id="81b36-125">Required</span></span> | <span data-ttu-id="81b36-126">应聘者的人员记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="81b36-126">Unique identifier of the person record for the candidate.</span></span> |
| <span data-ttu-id="81b36-127">**人员 ID 值**</span><span class="sxs-lookup"><span data-stu-id="81b36-127">**Person ID Value**</span></span><br><span data-ttu-id="81b36-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="81b36-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="81b36-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="81b36-129">*GUID*</span></span> | <span data-ttu-id="81b36-130">只读</span><span class="sxs-lookup"><span data-stu-id="81b36-130">Read-only</span></span><br><span data-ttu-id="81b36-131">必填</span><span class="sxs-lookup"><span data-stu-id="81b36-131">Required</span></span><br><span data-ttu-id="81b36-132">外键：mshr_dirpersonentity 的 mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="81b36-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="81b36-133">系统生成的人员实体记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="81b36-133">System-generated unique identifier of the person entity record.</span></span> |
| <span data-ttu-id="81b36-134">**雇主职位**</span><span class="sxs-lookup"><span data-stu-id="81b36-134">**Employer Position**</span></span><br><span data-ttu-id="81b36-135">mshr_employerposition</span><span class="sxs-lookup"><span data-stu-id="81b36-135">mshr_employerposition</span></span><br><span data-ttu-id="81b36-136">*字符串*</span><span class="sxs-lookup"><span data-stu-id="81b36-136">*String*</span></span> | <span data-ttu-id="81b36-137">读/写</span><span class="sxs-lookup"><span data-stu-id="81b36-137">Read/write</span></span><br><span data-ttu-id="81b36-138">必填</span><span class="sxs-lookup"><span data-stu-id="81b36-138">Required</span></span> | <span data-ttu-id="81b36-139">应聘者受雇期间担任的职务。</span><span class="sxs-lookup"><span data-stu-id="81b36-139">The position title held by the candidate while under employment.</span></span> |
| <span data-ttu-id="81b36-140">**雇主名称**</span><span class="sxs-lookup"><span data-stu-id="81b36-140">**Employer Name**</span></span><br><span data-ttu-id="81b36-141">mshr_employername</span><span class="sxs-lookup"><span data-stu-id="81b36-141">mshr_employername</span></span><br><span data-ttu-id="81b36-142">*字符串*</span><span class="sxs-lookup"><span data-stu-id="81b36-142">*String*</span></span> | <span data-ttu-id="81b36-143">读/写</span><span class="sxs-lookup"><span data-stu-id="81b36-143">Read/write</span></span><br><span data-ttu-id="81b36-144">必填</span><span class="sxs-lookup"><span data-stu-id="81b36-144">Required</span></span> | <span data-ttu-id="81b36-145">雇主的名称。</span><span class="sxs-lookup"><span data-stu-id="81b36-145">The name of the employer.</span></span> |
| <span data-ttu-id="81b36-146">**雇主位置**</span><span class="sxs-lookup"><span data-stu-id="81b36-146">**Employer Location**</span></span><br><span data-ttu-id="81b36-147">mshr_employerlocation</span><span class="sxs-lookup"><span data-stu-id="81b36-147">mshr_employerlocation</span></span><br><span data-ttu-id="81b36-148">*字符串*</span><span class="sxs-lookup"><span data-stu-id="81b36-148">*String*</span></span> | <span data-ttu-id="81b36-149">读/写</span><span class="sxs-lookup"><span data-stu-id="81b36-149">Read/write</span></span><br><span data-ttu-id="81b36-150">可选</span><span class="sxs-lookup"><span data-stu-id="81b36-150">Optional</span></span> | <span data-ttu-id="81b36-151">雇主所在的位置。</span><span class="sxs-lookup"><span data-stu-id="81b36-151">The employer’s location.</span></span> <span data-ttu-id="81b36-152">最大长度：60。</span><span class="sxs-lookup"><span data-stu-id="81b36-152">Max length: 60.</span></span> <span data-ttu-id="81b36-153">未定义或要求特定格式。</span><span class="sxs-lookup"><span data-stu-id="81b36-153">No specific format defined or required.</span></span> |
| <span data-ttu-id="81b36-154">**电话**</span><span class="sxs-lookup"><span data-stu-id="81b36-154">**Phone**</span></span><br><span data-ttu-id="81b36-155">mshr_phone</span><span class="sxs-lookup"><span data-stu-id="81b36-155">mshr_phone</span></span><br><span data-ttu-id="81b36-156">*字符串*</span><span class="sxs-lookup"><span data-stu-id="81b36-156">*String*</span></span> | <span data-ttu-id="81b36-157">读/写</span><span class="sxs-lookup"><span data-stu-id="81b36-157">Read/write</span></span><br><span data-ttu-id="81b36-158">可选</span><span class="sxs-lookup"><span data-stu-id="81b36-158">Optional</span></span> | <span data-ttu-id="81b36-159">雇主的电话号码。</span><span class="sxs-lookup"><span data-stu-id="81b36-159">The employer’s phone number.</span></span> |
| <span data-ttu-id="81b36-160">**URL**</span><span class="sxs-lookup"><span data-stu-id="81b36-160">**URL**</span></span><br><span data-ttu-id="81b36-161">mshr_url</span><span class="sxs-lookup"><span data-stu-id="81b36-161">mshr_url</span></span><br><span data-ttu-id="81b36-162">*字符串*</span><span class="sxs-lookup"><span data-stu-id="81b36-162">*String*</span></span> | <span data-ttu-id="81b36-163">读/写</span><span class="sxs-lookup"><span data-stu-id="81b36-163">Read/write</span></span><br><span data-ttu-id="81b36-164">可选</span><span class="sxs-lookup"><span data-stu-id="81b36-164">Optional</span></span> | <span data-ttu-id="81b36-165">雇主网站的 URL。</span><span class="sxs-lookup"><span data-stu-id="81b36-165">The URL of the employer’s website.</span></span> |
| <span data-ttu-id="81b36-166">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="81b36-166">**Start Date**</span></span><br><span data-ttu-id="81b36-167">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="81b36-167">mshr_startdate</span></span><br><span data-ttu-id="81b36-168">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="81b36-168">*Datetime*</span></span> | <span data-ttu-id="81b36-169">读/写</span><span class="sxs-lookup"><span data-stu-id="81b36-169">Read/write</span></span><br><span data-ttu-id="81b36-170">必填</span><span class="sxs-lookup"><span data-stu-id="81b36-170">Required</span></span> | <span data-ttu-id="81b36-171">应聘者受雇用的开始日期。</span><span class="sxs-lookup"><span data-stu-id="81b36-171">The start date of the candidate’s employment.</span></span> |
| <span data-ttu-id="81b36-172">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="81b36-172">**End Date**</span></span><br><span data-ttu-id="81b36-173">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="81b36-173">mshr_enddate</span></span><br><span data-ttu-id="81b36-174">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="81b36-174">*Datetime*</span></span> | <span data-ttu-id="81b36-175">读/写</span><span class="sxs-lookup"><span data-stu-id="81b36-175">Read/write</span></span><br><span data-ttu-id="81b36-176">可选</span><span class="sxs-lookup"><span data-stu-id="81b36-176">Optional</span></span> | <span data-ttu-id="81b36-177">应聘者受雇用的结束日期，如果应聘者仍在此工作，则为 null。</span><span class="sxs-lookup"><span data-stu-id="81b36-177">The end date of the candidate’s employment, or null if the candidate is still employed here.</span></span> |
| <span data-ttu-id="81b36-178">**允许联系雇主**</span><span class="sxs-lookup"><span data-stu-id="81b36-178">**Allow Contact Employer**</span></span><br><span data-ttu-id="81b36-179">mshr_allowcontactemployer</span><span class="sxs-lookup"><span data-stu-id="81b36-179">mshr_allowcontactemployer</span></span><br><span data-ttu-id="81b36-180">*mshr_hrmblankyesno 选项集*</span><span class="sxs-lookup"><span data-stu-id="81b36-180">*mshr_hrmblankyesno option set*</span></span> | <span data-ttu-id="81b36-181">读/写</span><span class="sxs-lookup"><span data-stu-id="81b36-181">Read/write</span></span><br><span data-ttu-id="81b36-182">可选</span><span class="sxs-lookup"><span data-stu-id="81b36-182">Optional</span></span> | <span data-ttu-id="81b36-183">表示应聘者是否允许与以前的雇主联系。</span><span class="sxs-lookup"><span data-stu-id="81b36-183">Signifies whether the candidate allows contacting the previous employer.</span></span> |
| <span data-ttu-id="81b36-184">**说明**</span><span class="sxs-lookup"><span data-stu-id="81b36-184">**Notes**</span></span><br><span data-ttu-id="81b36-185">mshr_note</span><span class="sxs-lookup"><span data-stu-id="81b36-185">mshr_note</span></span><br><span data-ttu-id="81b36-186">*字符串*</span><span class="sxs-lookup"><span data-stu-id="81b36-186">*String*</span></span> | <span data-ttu-id="81b36-187">读/写</span><span class="sxs-lookup"><span data-stu-id="81b36-187">Read/write</span></span><br><span data-ttu-id="81b36-188">可选</span><span class="sxs-lookup"><span data-stu-id="81b36-188">Optional</span></span> | <span data-ttu-id="81b36-189">招聘人员和招聘经理使用的说明。</span><span class="sxs-lookup"><span data-stu-id="81b36-189">Notes for use by the recruiter or hiring manager.</span></span> |
| <span data-ttu-id="81b36-190">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="81b36-190">**Primary Field**</span></span><br><span data-ttu-id="81b36-191">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="81b36-191">mshr_primaryfield</span></span><br><span data-ttu-id="81b36-192">*字符串*</span><span class="sxs-lookup"><span data-stu-id="81b36-192">*String*</span></span> | <span data-ttu-id="81b36-193">只读</span><span class="sxs-lookup"><span data-stu-id="81b36-193">Read-only</span></span><br><span data-ttu-id="81b36-194">必填</span><span class="sxs-lookup"><span data-stu-id="81b36-194">Required</span></span> | <span data-ttu-id="81b36-195">用作实体记录的主要标识符的字段。</span><span class="sxs-lookup"><span data-stu-id="81b36-195">Field used as a primary identifier of the entity record.</span></span> <span data-ttu-id="81b36-196">当事方编号、开始日期、雇主职位和雇主名称的组合。</span><span class="sxs-lookup"><span data-stu-id="81b36-196">Combination of party number, start date, employer position, and employer name.</span></span> |

## <a name="see-also"></a><span data-ttu-id="81b36-197">请参阅</span><span class="sxs-lookup"><span data-stu-id="81b36-197">See also</span></span>

[<span data-ttu-id="81b36-198">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="81b36-198">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="81b36-199">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="81b36-199">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]