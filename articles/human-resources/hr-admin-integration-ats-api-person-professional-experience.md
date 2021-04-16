---
title: 人员专业经验
description: 本主题介绍 Dynamics 365 Human Resources 的“人员专业经验”实体。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1defaff8397c41feedbd85893766106338a28941
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798049"
---
# <a name="person-professional-experience"></a><span data-ttu-id="7f772-103">人员专业经验</span><span class="sxs-lookup"><span data-stu-id="7f772-103">Person professional experience</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7f772-104">本主题介绍 Dynamics 365 Human Resources 的“人员专业经验”实体。</span><span class="sxs-lookup"><span data-stu-id="7f772-104">This topic describes the Person professional experience entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7f772-105">物理名称：mshr_hcmpersonprofessionalexperienceentity</span><span class="sxs-lookup"><span data-stu-id="7f772-105">Physical name: mshr_hcmpersonprofessionalexperienceentity</span></span>

## <a name="description"></a><span data-ttu-id="7f772-106">说明</span><span class="sxs-lookup"><span data-stu-id="7f772-106">Description</span></span>

<span data-ttu-id="7f772-107">此实体描述应聘者的专业经验或工作经历。</span><span class="sxs-lookup"><span data-stu-id="7f772-107">This entity describes professional experience or work history of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7f772-108">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="7f772-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="7f772-109">属性</span><span class="sxs-lookup"><span data-stu-id="7f772-109">Properties</span></span>

| <span data-ttu-id="7f772-110">属性</span><span class="sxs-lookup"><span data-stu-id="7f772-110">Property</span></span><br><span data-ttu-id="7f772-111">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="7f772-111">**Physical name**</span></span><br><span data-ttu-id="7f772-112">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="7f772-112">**_Type_**</span></span> | <span data-ttu-id="7f772-113">使用</span><span class="sxs-lookup"><span data-stu-id="7f772-113">Use</span></span> | <span data-ttu-id="7f772-114">说明</span><span class="sxs-lookup"><span data-stu-id="7f772-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7f772-115">**人员专业经验实体 ID**</span><span class="sxs-lookup"><span data-stu-id="7f772-115">**Person Professional Experience Entity ID**</span></span><br><span data-ttu-id="7f772-116">mshr_hcmpersonprofessionalexperienceentityid</span><span class="sxs-lookup"><span data-stu-id="7f772-116">mshr_hcmpersonprofessionalexperienceentityid</span></span><br><span data-ttu-id="7f772-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7f772-117">*GUID*</span></span> | <span data-ttu-id="7f772-118">只读</span><span class="sxs-lookup"><span data-stu-id="7f772-118">Read-only</span></span><br><span data-ttu-id="7f772-119">必填</span><span class="sxs-lookup"><span data-stu-id="7f772-119">Required</span></span> | <span data-ttu-id="7f772-120">系统生成的实体记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="7f772-120">System-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="7f772-121">**当事方编号**</span><span class="sxs-lookup"><span data-stu-id="7f772-121">**Party Number**</span></span><br><span data-ttu-id="7f772-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="7f772-122">mshr_partynumber</span></span><br><span data-ttu-id="7f772-123">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7f772-123">*String*</span></span> | <span data-ttu-id="7f772-124">读/写</span><span class="sxs-lookup"><span data-stu-id="7f772-124">Read/write</span></span><br><span data-ttu-id="7f772-125">必填</span><span class="sxs-lookup"><span data-stu-id="7f772-125">Required</span></span> | <span data-ttu-id="7f772-126">应聘者的人员记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="7f772-126">Unique identifier of the person record for the candidate.</span></span> |
| <span data-ttu-id="7f772-127">**人员 ID 值**</span><span class="sxs-lookup"><span data-stu-id="7f772-127">**Person ID Value**</span></span><br><span data-ttu-id="7f772-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="7f772-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="7f772-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7f772-129">*GUID*</span></span> | <span data-ttu-id="7f772-130">只读</span><span class="sxs-lookup"><span data-stu-id="7f772-130">Read-only</span></span><br><span data-ttu-id="7f772-131">必填</span><span class="sxs-lookup"><span data-stu-id="7f772-131">Required</span></span><br><span data-ttu-id="7f772-132">外键：mshr_dirpersonentity 的 mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="7f772-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="7f772-133">系统生成的人员实体记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="7f772-133">System-generated unique identifier of the person entity record.</span></span> |
| <span data-ttu-id="7f772-134">**雇主职位**</span><span class="sxs-lookup"><span data-stu-id="7f772-134">**Employer Position**</span></span><br><span data-ttu-id="7f772-135">mshr_employerposition</span><span class="sxs-lookup"><span data-stu-id="7f772-135">mshr_employerposition</span></span><br><span data-ttu-id="7f772-136">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7f772-136">*String*</span></span> | <span data-ttu-id="7f772-137">读/写</span><span class="sxs-lookup"><span data-stu-id="7f772-137">Read/write</span></span><br><span data-ttu-id="7f772-138">必填</span><span class="sxs-lookup"><span data-stu-id="7f772-138">Required</span></span> | <span data-ttu-id="7f772-139">应聘者受雇期间担任的职务。</span><span class="sxs-lookup"><span data-stu-id="7f772-139">The position title held by the candidate while under employment.</span></span> |
| <span data-ttu-id="7f772-140">**雇主名称**</span><span class="sxs-lookup"><span data-stu-id="7f772-140">**Employer Name**</span></span><br><span data-ttu-id="7f772-141">mshr_employername</span><span class="sxs-lookup"><span data-stu-id="7f772-141">mshr_employername</span></span><br><span data-ttu-id="7f772-142">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7f772-142">*String*</span></span> | <span data-ttu-id="7f772-143">读/写</span><span class="sxs-lookup"><span data-stu-id="7f772-143">Read/write</span></span><br><span data-ttu-id="7f772-144">必填</span><span class="sxs-lookup"><span data-stu-id="7f772-144">Required</span></span> | <span data-ttu-id="7f772-145">雇主的名称。</span><span class="sxs-lookup"><span data-stu-id="7f772-145">The name of the employer.</span></span> |
| <span data-ttu-id="7f772-146">**雇主位置**</span><span class="sxs-lookup"><span data-stu-id="7f772-146">**Employer Location**</span></span><br><span data-ttu-id="7f772-147">mshr_employerlocation</span><span class="sxs-lookup"><span data-stu-id="7f772-147">mshr_employerlocation</span></span><br><span data-ttu-id="7f772-148">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7f772-148">*String*</span></span> | <span data-ttu-id="7f772-149">读/写</span><span class="sxs-lookup"><span data-stu-id="7f772-149">Read/write</span></span><br><span data-ttu-id="7f772-150">可选</span><span class="sxs-lookup"><span data-stu-id="7f772-150">Optional</span></span> | <span data-ttu-id="7f772-151">雇主所在的位置。</span><span class="sxs-lookup"><span data-stu-id="7f772-151">The employer’s location.</span></span> <span data-ttu-id="7f772-152">最大长度：60。</span><span class="sxs-lookup"><span data-stu-id="7f772-152">Max length: 60.</span></span> <span data-ttu-id="7f772-153">未定义或要求特定格式。</span><span class="sxs-lookup"><span data-stu-id="7f772-153">No specific format defined or required.</span></span> |
| <span data-ttu-id="7f772-154">**电话**</span><span class="sxs-lookup"><span data-stu-id="7f772-154">**Phone**</span></span><br><span data-ttu-id="7f772-155">mshr_phone</span><span class="sxs-lookup"><span data-stu-id="7f772-155">mshr_phone</span></span><br><span data-ttu-id="7f772-156">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7f772-156">*String*</span></span> | <span data-ttu-id="7f772-157">读/写</span><span class="sxs-lookup"><span data-stu-id="7f772-157">Read/write</span></span><br><span data-ttu-id="7f772-158">可选</span><span class="sxs-lookup"><span data-stu-id="7f772-158">Optional</span></span> | <span data-ttu-id="7f772-159">雇主的电话号码。</span><span class="sxs-lookup"><span data-stu-id="7f772-159">The employer’s phone number.</span></span> |
| <span data-ttu-id="7f772-160">**URL**</span><span class="sxs-lookup"><span data-stu-id="7f772-160">**URL**</span></span><br><span data-ttu-id="7f772-161">mshr_url</span><span class="sxs-lookup"><span data-stu-id="7f772-161">mshr_url</span></span><br><span data-ttu-id="7f772-162">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7f772-162">*String*</span></span> | <span data-ttu-id="7f772-163">读/写</span><span class="sxs-lookup"><span data-stu-id="7f772-163">Read/write</span></span><br><span data-ttu-id="7f772-164">可选</span><span class="sxs-lookup"><span data-stu-id="7f772-164">Optional</span></span> | <span data-ttu-id="7f772-165">雇主网站的 URL。</span><span class="sxs-lookup"><span data-stu-id="7f772-165">The URL of the employer’s website.</span></span> |
| <span data-ttu-id="7f772-166">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="7f772-166">**Start Date**</span></span><br><span data-ttu-id="7f772-167">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="7f772-167">mshr_startdate</span></span><br><span data-ttu-id="7f772-168">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="7f772-168">*Datetime*</span></span> | <span data-ttu-id="7f772-169">读/写</span><span class="sxs-lookup"><span data-stu-id="7f772-169">Read/write</span></span><br><span data-ttu-id="7f772-170">必填</span><span class="sxs-lookup"><span data-stu-id="7f772-170">Required</span></span> | <span data-ttu-id="7f772-171">应聘者受雇用的开始日期。</span><span class="sxs-lookup"><span data-stu-id="7f772-171">The start date of the candidate’s employment.</span></span> |
| <span data-ttu-id="7f772-172">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="7f772-172">**End Date**</span></span><br><span data-ttu-id="7f772-173">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="7f772-173">mshr_enddate</span></span><br><span data-ttu-id="7f772-174">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="7f772-174">*Datetime*</span></span> | <span data-ttu-id="7f772-175">读/写</span><span class="sxs-lookup"><span data-stu-id="7f772-175">Read/write</span></span><br><span data-ttu-id="7f772-176">可选</span><span class="sxs-lookup"><span data-stu-id="7f772-176">Optional</span></span> | <span data-ttu-id="7f772-177">应聘者受雇用的结束日期，如果应聘者仍在此工作，则为 null。</span><span class="sxs-lookup"><span data-stu-id="7f772-177">The end date of the candidate’s employment, or null if the candidate is still employed here.</span></span> |
| <span data-ttu-id="7f772-178">**允许联系雇主**</span><span class="sxs-lookup"><span data-stu-id="7f772-178">**Allow Contact Employer**</span></span><br><span data-ttu-id="7f772-179">mshr_allowcontactemployer</span><span class="sxs-lookup"><span data-stu-id="7f772-179">mshr_allowcontactemployer</span></span><br><span data-ttu-id="7f772-180">*mshr_hrmblankyesno 选项集*</span><span class="sxs-lookup"><span data-stu-id="7f772-180">*mshr_hrmblankyesno option set*</span></span> | <span data-ttu-id="7f772-181">读/写</span><span class="sxs-lookup"><span data-stu-id="7f772-181">Read/write</span></span><br><span data-ttu-id="7f772-182">可选</span><span class="sxs-lookup"><span data-stu-id="7f772-182">Optional</span></span> | <span data-ttu-id="7f772-183">表示应聘者是否允许与以前的雇主联系。</span><span class="sxs-lookup"><span data-stu-id="7f772-183">Signifies whether the candidate allows contacting the previous employer.</span></span> |
| <span data-ttu-id="7f772-184">**说明**</span><span class="sxs-lookup"><span data-stu-id="7f772-184">**Notes**</span></span><br><span data-ttu-id="7f772-185">mshr_note</span><span class="sxs-lookup"><span data-stu-id="7f772-185">mshr_note</span></span><br><span data-ttu-id="7f772-186">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7f772-186">*String*</span></span> | <span data-ttu-id="7f772-187">读/写</span><span class="sxs-lookup"><span data-stu-id="7f772-187">Read/write</span></span><br><span data-ttu-id="7f772-188">可选</span><span class="sxs-lookup"><span data-stu-id="7f772-188">Optional</span></span> | <span data-ttu-id="7f772-189">招聘人员和招聘经理使用的说明。</span><span class="sxs-lookup"><span data-stu-id="7f772-189">Notes for use by the recruiter or hiring manager.</span></span> |
| <span data-ttu-id="7f772-190">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="7f772-190">**Primary Field**</span></span><br><span data-ttu-id="7f772-191">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="7f772-191">mshr_primaryfield</span></span><br><span data-ttu-id="7f772-192">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7f772-192">*String*</span></span> | <span data-ttu-id="7f772-193">只读</span><span class="sxs-lookup"><span data-stu-id="7f772-193">Read-only</span></span><br><span data-ttu-id="7f772-194">必填</span><span class="sxs-lookup"><span data-stu-id="7f772-194">Required</span></span> | <span data-ttu-id="7f772-195">用作实体记录的主要标识符的字段。</span><span class="sxs-lookup"><span data-stu-id="7f772-195">Field used as a primary identifier of the entity record.</span></span> <span data-ttu-id="7f772-196">当事方编号、开始日期、雇主职位和雇主名称的组合。</span><span class="sxs-lookup"><span data-stu-id="7f772-196">Combination of party number, start date, employer position, and employer name.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7f772-197">请参阅</span><span class="sxs-lookup"><span data-stu-id="7f772-197">See also</span></span>

[<span data-ttu-id="7f772-198">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="7f772-198">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7f772-199">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="7f772-199">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]