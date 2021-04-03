---
title: 人员专业经验
description: 本主题介绍 Dynamics 365 Human Resources 的“人员专业经验”实体。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5672e32b157b46b6863f06fea123fd3d6a3d96d2
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466416"
---
# <a name="person-professional-experience"></a><span data-ttu-id="3da69-103">人员专业经验</span><span class="sxs-lookup"><span data-stu-id="3da69-103">Person professional experience</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3da69-104">本主题介绍 Dynamics 365 Human Resources 的“人员专业经验”实体。</span><span class="sxs-lookup"><span data-stu-id="3da69-104">This topic describes the Person professional experience entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3da69-105">物理名称：mshr_hcmpersonprofessionalexperienceentity</span><span class="sxs-lookup"><span data-stu-id="3da69-105">Physical name: mshr_hcmpersonprofessionalexperienceentity</span></span>

## <a name="description"></a><span data-ttu-id="3da69-106">说明</span><span class="sxs-lookup"><span data-stu-id="3da69-106">Description</span></span>

<span data-ttu-id="3da69-107">此实体描述应聘者的专业经验或工作经历。</span><span class="sxs-lookup"><span data-stu-id="3da69-107">This entity describes professional experience or work history of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3da69-108">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="3da69-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="3da69-109">属性</span><span class="sxs-lookup"><span data-stu-id="3da69-109">Properties</span></span>

| <span data-ttu-id="3da69-110">属性</span><span class="sxs-lookup"><span data-stu-id="3da69-110">Property</span></span><br><span data-ttu-id="3da69-111">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="3da69-111">**Physical name**</span></span><br><span data-ttu-id="3da69-112">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="3da69-112">**_Type_**</span></span> | <span data-ttu-id="3da69-113">使用</span><span class="sxs-lookup"><span data-stu-id="3da69-113">Use</span></span> | <span data-ttu-id="3da69-114">说明</span><span class="sxs-lookup"><span data-stu-id="3da69-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3da69-115">**人员专业经验实体 ID**</span><span class="sxs-lookup"><span data-stu-id="3da69-115">**Person Professional Experience Entity ID**</span></span><br><span data-ttu-id="3da69-116">mshr_hcmpersonprofessionalexperienceentityid</span><span class="sxs-lookup"><span data-stu-id="3da69-116">mshr_hcmpersonprofessionalexperienceentityid</span></span><br><span data-ttu-id="3da69-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3da69-117">*GUID*</span></span> | <span data-ttu-id="3da69-118">只读</span><span class="sxs-lookup"><span data-stu-id="3da69-118">Read-only</span></span><br><span data-ttu-id="3da69-119">必填</span><span class="sxs-lookup"><span data-stu-id="3da69-119">Required</span></span> | <span data-ttu-id="3da69-120">系统生成的实体记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3da69-120">System-generated unique identifier for the entity record.</span></span> |
| <span data-ttu-id="3da69-121">**当事方编号**</span><span class="sxs-lookup"><span data-stu-id="3da69-121">**Party Number**</span></span><br><span data-ttu-id="3da69-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="3da69-122">mshr_partynumber</span></span><br><span data-ttu-id="3da69-123">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3da69-123">*String*</span></span> | <span data-ttu-id="3da69-124">读/写</span><span class="sxs-lookup"><span data-stu-id="3da69-124">Read/write</span></span><br><span data-ttu-id="3da69-125">必填</span><span class="sxs-lookup"><span data-stu-id="3da69-125">Required</span></span> | <span data-ttu-id="3da69-126">应聘者的人员记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3da69-126">Unique identifier of the person record for the candidate.</span></span> |
| <span data-ttu-id="3da69-127">**人员 ID 值**</span><span class="sxs-lookup"><span data-stu-id="3da69-127">**Person ID Value**</span></span><br><span data-ttu-id="3da69-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="3da69-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="3da69-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3da69-129">*GUID*</span></span> | <span data-ttu-id="3da69-130">只读</span><span class="sxs-lookup"><span data-stu-id="3da69-130">Read-only</span></span><br><span data-ttu-id="3da69-131">必填</span><span class="sxs-lookup"><span data-stu-id="3da69-131">Required</span></span><br><span data-ttu-id="3da69-132">外键：mshr_dirpersonentity 的 mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="3da69-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="3da69-133">系统生成的人员实体记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3da69-133">System-generated unique identifier of the person entity record.</span></span> |
| <span data-ttu-id="3da69-134">**雇主职位**</span><span class="sxs-lookup"><span data-stu-id="3da69-134">**Employer Position**</span></span><br><span data-ttu-id="3da69-135">mshr_employerposition</span><span class="sxs-lookup"><span data-stu-id="3da69-135">mshr_employerposition</span></span><br><span data-ttu-id="3da69-136">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3da69-136">*String*</span></span> | <span data-ttu-id="3da69-137">读/写</span><span class="sxs-lookup"><span data-stu-id="3da69-137">Read/write</span></span><br><span data-ttu-id="3da69-138">必填</span><span class="sxs-lookup"><span data-stu-id="3da69-138">Required</span></span> | <span data-ttu-id="3da69-139">应聘者受雇期间担任的职务。</span><span class="sxs-lookup"><span data-stu-id="3da69-139">The position title held by the candidate while under employment.</span></span> |
| <span data-ttu-id="3da69-140">**雇主名称**</span><span class="sxs-lookup"><span data-stu-id="3da69-140">**Employer Name**</span></span><br><span data-ttu-id="3da69-141">mshr_employername</span><span class="sxs-lookup"><span data-stu-id="3da69-141">mshr_employername</span></span><br><span data-ttu-id="3da69-142">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3da69-142">*String*</span></span> | <span data-ttu-id="3da69-143">读/写</span><span class="sxs-lookup"><span data-stu-id="3da69-143">Read/write</span></span><br><span data-ttu-id="3da69-144">必填</span><span class="sxs-lookup"><span data-stu-id="3da69-144">Required</span></span> | <span data-ttu-id="3da69-145">雇主的名称。</span><span class="sxs-lookup"><span data-stu-id="3da69-145">The name of the employer.</span></span> |
| <span data-ttu-id="3da69-146">**雇主位置**</span><span class="sxs-lookup"><span data-stu-id="3da69-146">**Employer Location**</span></span><br><span data-ttu-id="3da69-147">mshr_employerlocation</span><span class="sxs-lookup"><span data-stu-id="3da69-147">mshr_employerlocation</span></span><br><span data-ttu-id="3da69-148">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3da69-148">*String*</span></span> | <span data-ttu-id="3da69-149">读/写</span><span class="sxs-lookup"><span data-stu-id="3da69-149">Read/write</span></span><br><span data-ttu-id="3da69-150">可选</span><span class="sxs-lookup"><span data-stu-id="3da69-150">Optional</span></span> | <span data-ttu-id="3da69-151">雇主所在的位置。</span><span class="sxs-lookup"><span data-stu-id="3da69-151">The employer’s location.</span></span> <span data-ttu-id="3da69-152">最大长度：60。</span><span class="sxs-lookup"><span data-stu-id="3da69-152">Max length: 60.</span></span> <span data-ttu-id="3da69-153">未定义或要求特定格式。</span><span class="sxs-lookup"><span data-stu-id="3da69-153">No specific format defined or required.</span></span> |
| <span data-ttu-id="3da69-154">**电话**</span><span class="sxs-lookup"><span data-stu-id="3da69-154">**Phone**</span></span><br><span data-ttu-id="3da69-155">mshr_phone</span><span class="sxs-lookup"><span data-stu-id="3da69-155">mshr_phone</span></span><br><span data-ttu-id="3da69-156">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3da69-156">*String*</span></span> | <span data-ttu-id="3da69-157">读/写</span><span class="sxs-lookup"><span data-stu-id="3da69-157">Read/write</span></span><br><span data-ttu-id="3da69-158">可选</span><span class="sxs-lookup"><span data-stu-id="3da69-158">Optional</span></span> | <span data-ttu-id="3da69-159">雇主的电话号码。</span><span class="sxs-lookup"><span data-stu-id="3da69-159">The employer’s phone number.</span></span> |
| <span data-ttu-id="3da69-160">**URL**</span><span class="sxs-lookup"><span data-stu-id="3da69-160">**URL**</span></span><br><span data-ttu-id="3da69-161">mshr_url</span><span class="sxs-lookup"><span data-stu-id="3da69-161">mshr_url</span></span><br><span data-ttu-id="3da69-162">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3da69-162">*String*</span></span> | <span data-ttu-id="3da69-163">读/写</span><span class="sxs-lookup"><span data-stu-id="3da69-163">Read/write</span></span><br><span data-ttu-id="3da69-164">可选</span><span class="sxs-lookup"><span data-stu-id="3da69-164">Optional</span></span> | <span data-ttu-id="3da69-165">雇主网站的 URL。</span><span class="sxs-lookup"><span data-stu-id="3da69-165">The URL of the employer’s website.</span></span> |
| <span data-ttu-id="3da69-166">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="3da69-166">**Start Date**</span></span><br><span data-ttu-id="3da69-167">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="3da69-167">mshr_startdate</span></span><br><span data-ttu-id="3da69-168">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="3da69-168">*Datetime*</span></span> | <span data-ttu-id="3da69-169">读/写</span><span class="sxs-lookup"><span data-stu-id="3da69-169">Read/write</span></span><br><span data-ttu-id="3da69-170">必填</span><span class="sxs-lookup"><span data-stu-id="3da69-170">Required</span></span> | <span data-ttu-id="3da69-171">应聘者受雇用的开始日期。</span><span class="sxs-lookup"><span data-stu-id="3da69-171">The start date of the candidate’s employment.</span></span> |
| <span data-ttu-id="3da69-172">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="3da69-172">**End Date**</span></span><br><span data-ttu-id="3da69-173">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="3da69-173">mshr_enddate</span></span><br><span data-ttu-id="3da69-174">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="3da69-174">*Datetime*</span></span> | <span data-ttu-id="3da69-175">读/写</span><span class="sxs-lookup"><span data-stu-id="3da69-175">Read/write</span></span><br><span data-ttu-id="3da69-176">可选</span><span class="sxs-lookup"><span data-stu-id="3da69-176">Optional</span></span> | <span data-ttu-id="3da69-177">应聘者受雇用的结束日期，如果应聘者仍在此工作，则为 null。</span><span class="sxs-lookup"><span data-stu-id="3da69-177">The end date of the candidate’s employment, or null if the candidate is still employed here.</span></span> |
| <span data-ttu-id="3da69-178">**允许联系雇主**</span><span class="sxs-lookup"><span data-stu-id="3da69-178">**Allow Contact Employer**</span></span><br><span data-ttu-id="3da69-179">mshr_allowcontactemployer</span><span class="sxs-lookup"><span data-stu-id="3da69-179">mshr_allowcontactemployer</span></span><br><span data-ttu-id="3da69-180">*mshr_hrmblankyesno 选项集*</span><span class="sxs-lookup"><span data-stu-id="3da69-180">*mshr_hrmblankyesno option set*</span></span> | <span data-ttu-id="3da69-181">读/写</span><span class="sxs-lookup"><span data-stu-id="3da69-181">Read/write</span></span><br><span data-ttu-id="3da69-182">可选</span><span class="sxs-lookup"><span data-stu-id="3da69-182">Optional</span></span> | <span data-ttu-id="3da69-183">表示应聘者是否允许与以前的雇主联系。</span><span class="sxs-lookup"><span data-stu-id="3da69-183">Signifies whether the candidate allows contacting the previous employer.</span></span> |
| <span data-ttu-id="3da69-184">**说明**</span><span class="sxs-lookup"><span data-stu-id="3da69-184">**Notes**</span></span><br><span data-ttu-id="3da69-185">mshr_note</span><span class="sxs-lookup"><span data-stu-id="3da69-185">mshr_note</span></span><br><span data-ttu-id="3da69-186">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3da69-186">*String*</span></span> | <span data-ttu-id="3da69-187">读/写</span><span class="sxs-lookup"><span data-stu-id="3da69-187">Read/write</span></span><br><span data-ttu-id="3da69-188">可选</span><span class="sxs-lookup"><span data-stu-id="3da69-188">Optional</span></span> | <span data-ttu-id="3da69-189">招聘人员和招聘经理使用的说明。</span><span class="sxs-lookup"><span data-stu-id="3da69-189">Notes for use by the recruiter or hiring manager.</span></span> |
| <span data-ttu-id="3da69-190">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="3da69-190">**Primary Field**</span></span><br><span data-ttu-id="3da69-191">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3da69-191">mshr_primaryfield</span></span><br><span data-ttu-id="3da69-192">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3da69-192">*String*</span></span> | <span data-ttu-id="3da69-193">只读</span><span class="sxs-lookup"><span data-stu-id="3da69-193">Read-only</span></span><br><span data-ttu-id="3da69-194">必填</span><span class="sxs-lookup"><span data-stu-id="3da69-194">Required</span></span> | <span data-ttu-id="3da69-195">用作实体记录的主要标识符的字段。</span><span class="sxs-lookup"><span data-stu-id="3da69-195">Field used as a primary identifier of the entity record.</span></span> <span data-ttu-id="3da69-196">当事方编号、开始日期、雇主职位和雇主名称的组合。</span><span class="sxs-lookup"><span data-stu-id="3da69-196">Combination of party number, start date, employer position, and employer name.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3da69-197">请参阅</span><span class="sxs-lookup"><span data-stu-id="3da69-197">See also</span></span>

[<span data-ttu-id="3da69-198">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="3da69-198">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3da69-199">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="3da69-199">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]