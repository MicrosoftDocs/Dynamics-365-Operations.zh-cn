---
title: 招聘请求教育
description: 本主题介绍 Dynamics 365 Human Resources 的“招聘请求教育”实体。
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
ms.openlocfilehash: 4976e51dbe0cb7f50290b40d6342bcc18044cd52
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057422"
---
# <a name="recruiting-request-education"></a><span data-ttu-id="e9662-103">招聘请求教育</span><span class="sxs-lookup"><span data-stu-id="e9662-103">Recruiting request education</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e9662-104">本主题介绍 Dynamics 365 Human Resources 的“招聘请求教育”实体。</span><span class="sxs-lookup"><span data-stu-id="e9662-104">This topic describes the Recruiting request education entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="e9662-105">物理名称：mshr_hcmrecruitingrequesteducationentity</span><span class="sxs-lookup"><span data-stu-id="e9662-105">Physical name: mshr_hcmrecruitingrequesteducationentity</span></span>

### <a name="description"></a><span data-ttu-id="e9662-106">说明</span><span class="sxs-lookup"><span data-stu-id="e9662-106">Description</span></span>

<span data-ttu-id="e9662-107">描述 RecruitingRequest 的教育要求。</span><span class="sxs-lookup"><span data-stu-id="e9662-107">Describes educational requirements for a RecruitingRequest.</span></span>

### <a name="json-representation"></a><span data-ttu-id="e9662-108">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="e9662-108">JSON representation</span></span>

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a><span data-ttu-id="e9662-109">属性</span><span class="sxs-lookup"><span data-stu-id="e9662-109">Properties</span></span>

| <span data-ttu-id="e9662-110">属性</span><span class="sxs-lookup"><span data-stu-id="e9662-110">Property</span></span><br><span data-ttu-id="e9662-111">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="e9662-111">**Physical name**</span></span><br><span data-ttu-id="e9662-112">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="e9662-112">**_Type_**</span></span> | <span data-ttu-id="e9662-113">使用</span><span class="sxs-lookup"><span data-stu-id="e9662-113">Use</span></span> | <span data-ttu-id="e9662-114">说明</span><span class="sxs-lookup"><span data-stu-id="e9662-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e9662-115">**招聘请求教育实体 ID**</span><span class="sxs-lookup"><span data-stu-id="e9662-115">**Recruiting Request Education Entity ID**</span></span><br><span data-ttu-id="e9662-116">mshr_hcmrecruitingrequesteducationentityid</span><span class="sxs-lookup"><span data-stu-id="e9662-116">mshr_hcmrecruitingrequesteducationentityid</span></span><br><span data-ttu-id="e9662-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e9662-117">*GUID*</span></span> | <span data-ttu-id="e9662-118">只读</span><span class="sxs-lookup"><span data-stu-id="e9662-118">Read-only</span></span><br><span data-ttu-id="e9662-119">必填</span><span class="sxs-lookup"><span data-stu-id="e9662-119">Required</span></span> | <span data-ttu-id="e9662-120">系统生成的招聘请求教育记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e9662-120">System-generated unique identifier for the Recruiting Request Education record.</span></span> |
| <span data-ttu-id="e9662-121">**招聘请求 ID**</span><span class="sxs-lookup"><span data-stu-id="e9662-121">**Recruiting Request ID**</span></span><br><span data-ttu-id="e9662-122">mshr_recruitingrequestid</span><span class="sxs-lookup"><span data-stu-id="e9662-122">mshr_recruitingrequestid</span></span><br><span data-ttu-id="e9662-123">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e9662-123">*String*</span></span> | <span data-ttu-id="e9662-124">写入一次</span><span class="sxs-lookup"><span data-stu-id="e9662-124">Write-once</span></span><br><span data-ttu-id="e9662-125">必填</span><span class="sxs-lookup"><span data-stu-id="e9662-125">Required</span></span> | <span data-ttu-id="e9662-126">相关招聘请求的用户可读的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e9662-126">The user-readable unique identifier of the related recruiting request.</span></span> |
| <span data-ttu-id="e9662-127">**招聘请求 ID 值**</span><span class="sxs-lookup"><span data-stu-id="e9662-127">**Recruiting Request ID Value**</span></span><br><span data-ttu-id="e9662-128">_mshr_fk_recruitingrequest_id_value</span><span class="sxs-lookup"><span data-stu-id="e9662-128">_mshr_fk_recruitingrequest_id_value</span></span><br><span data-ttu-id="e9662-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e9662-129">*GUID*</span></span> | <span data-ttu-id="e9662-130">只读</span><span class="sxs-lookup"><span data-stu-id="e9662-130">Read-only</span></span><br><span data-ttu-id="e9662-131">必填</span><span class="sxs-lookup"><span data-stu-id="e9662-131">Required</span></span><br><span data-ttu-id="e9662-132">外键：mshr_hcmrecruitingrequestentity 的 mshr_hcmrecruitingrequestentityid</span><span class="sxs-lookup"><span data-stu-id="e9662-132">Foreign key: mshr_hcmrecruitingrequestentityid of mshr_hcmrecruitingrequestentity</span></span> | <span data-ttu-id="e9662-133">系统生成的相关招聘请求的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e9662-133">System-generated unique identifier of the related recruiting request.</span></span> |
| <span data-ttu-id="e9662-134">**教育程度 ID**</span><span class="sxs-lookup"><span data-stu-id="e9662-134">**Education Level ID**</span></span><br><span data-ttu-id="e9662-135">mshr_educationlevelid</span><span class="sxs-lookup"><span data-stu-id="e9662-135">mshr_educationlevelid</span></span><br><span data-ttu-id="e9662-136">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e9662-136">*String*</span></span> | <span data-ttu-id="e9662-137">写入一次</span><span class="sxs-lookup"><span data-stu-id="e9662-137">Write-once</span></span><br><span data-ttu-id="e9662-138">必填</span><span class="sxs-lookup"><span data-stu-id="e9662-138">Required</span></span> | <span data-ttu-id="e9662-139">所需教育程度。</span><span class="sxs-lookup"><span data-stu-id="e9662-139">The level of education required.</span></span> |
| <span data-ttu-id="e9662-140">**教育程度 ID 值**</span><span class="sxs-lookup"><span data-stu-id="e9662-140">**Educational Level ID Value**</span></span><br><span data-ttu-id="e9662-141">_mshr_fk_educationlevel_id_value</span><span class="sxs-lookup"><span data-stu-id="e9662-141">_mshr_fk_educationlevel_id_value</span></span><br><span data-ttu-id="e9662-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e9662-142">*GUID*</span></span> | <span data-ttu-id="e9662-143">只读</span><span class="sxs-lookup"><span data-stu-id="e9662-143">Read-only</span></span><br><span data-ttu-id="e9662-144">必填</span><span class="sxs-lookup"><span data-stu-id="e9662-144">Required</span></span><br><span data-ttu-id="e9662-145">外键：mshr_hcmeducationlevelentity 的 mshr_hcmeducationlevelentityid</span><span class="sxs-lookup"><span data-stu-id="e9662-145">Foreign key: mshr_hcmeducationlevelentityid of mshr_hcmeducationlevelentity</span></span> | <span data-ttu-id="e9662-146">系统生成的所需教育程度的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e9662-146">System-generated unique identifier of the level of education required.</span></span> |
| <span data-ttu-id="e9662-147">**教育程度描述**</span><span class="sxs-lookup"><span data-stu-id="e9662-147">**Education Level Description**</span></span><br><span data-ttu-id="e9662-148">mshr_educationleveldescription</span><span class="sxs-lookup"><span data-stu-id="e9662-148">mshr_educationleveldescription</span></span><br><span data-ttu-id="e9662-149">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e9662-149">*String*</span></span> | <span data-ttu-id="e9662-150">只读</span><span class="sxs-lookup"><span data-stu-id="e9662-150">Read-only</span></span><br><span data-ttu-id="e9662-151">必填</span><span class="sxs-lookup"><span data-stu-id="e9662-151">Required</span></span> | <span data-ttu-id="e9662-152">技能所需的教育程度的描述。</span><span class="sxs-lookup"><span data-stu-id="e9662-152">The description of the level required for the skill.</span></span> |
| <span data-ttu-id="e9662-153">**教育学科 ID**</span><span class="sxs-lookup"><span data-stu-id="e9662-153">**Education Discipline ID**</span></span><br><span data-ttu-id="e9662-154">mshr_educationdisciplinedescription</span><span class="sxs-lookup"><span data-stu-id="e9662-154">mshr_educationdisciplinedescription</span></span><br><span data-ttu-id="e9662-155">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e9662-155">*String*</span></span> | <span data-ttu-id="e9662-156">写入一次</span><span class="sxs-lookup"><span data-stu-id="e9662-156">Write-once</span></span><br><span data-ttu-id="e9662-157">必填</span><span class="sxs-lookup"><span data-stu-id="e9662-157">Required</span></span> | <span data-ttu-id="e9662-158">教育学科所在的领域。</span><span class="sxs-lookup"><span data-stu-id="e9662-158">The area of educational discipline.</span></span> |
| <span data-ttu-id="e9662-159">**教育学科 ID 值**</span><span class="sxs-lookup"><span data-stu-id="e9662-159">**Education Discipline ID Value**</span></span><br><span data-ttu-id="e9662-160">_mshr_fk_educationdiscipline_id_value</span><span class="sxs-lookup"><span data-stu-id="e9662-160">_mshr_fk_educationdiscipline_id_value</span></span><br><span data-ttu-id="e9662-161">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e9662-161">*GUID*</span></span> | <span data-ttu-id="e9662-162">只读</span><span class="sxs-lookup"><span data-stu-id="e9662-162">Read-only</span></span><br><span data-ttu-id="e9662-163">必填</span><span class="sxs-lookup"><span data-stu-id="e9662-163">Required</span></span><br><span data-ttu-id="e9662-164">外键：mshr_hcmeducationdisciplineentity 的 mshr_hcmeducationdisciplineentityid</span><span class="sxs-lookup"><span data-stu-id="e9662-164">Foreign key: mshr_hcmeducationdisciplineentityid of mshr_hcmeducationdisciplineentity</span></span> | <span data-ttu-id="e9662-165">系统生成的教育学科所在领域的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="e9662-165">System-generated unique identifier of the area of educational discipline.</span></span> |
| <span data-ttu-id="e9662-166">**教育学科描述**</span><span class="sxs-lookup"><span data-stu-id="e9662-166">**Education Discipline Description**</span></span><br><span data-ttu-id="e9662-167">mshr_educationdisciplinedescription</span><span class="sxs-lookup"><span data-stu-id="e9662-167">mshr_educationdisciplinedescription</span></span><br><span data-ttu-id="e9662-168">字符串</span><span class="sxs-lookup"><span data-stu-id="e9662-168">String</span></span> | <span data-ttu-id="e9662-169">只读</span><span class="sxs-lookup"><span data-stu-id="e9662-169">Read-only</span></span><br><span data-ttu-id="e9662-170">必填</span><span class="sxs-lookup"><span data-stu-id="e9662-170">Required</span></span> | <span data-ttu-id="e9662-171">教育学科所在领域的描述。</span><span class="sxs-lookup"><span data-stu-id="e9662-171">The description of the area of educational discipline.</span></span> |
| <span data-ttu-id="e9662-172">**数据区域 ID**</span><span class="sxs-lookup"><span data-stu-id="e9662-172">**Data Area ID**</span></span><br><span data-ttu-id="e9662-173">mshr_dataareaid</span><span class="sxs-lookup"><span data-stu-id="e9662-173">mshr_dataareaid</span></span><br><span data-ttu-id="e9662-174">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e9662-174">*String*</span></span> | <span data-ttu-id="e9662-175">读/写</span><span class="sxs-lookup"><span data-stu-id="e9662-175">Read/write</span></span><br><span data-ttu-id="e9662-176">可选</span><span class="sxs-lookup"><span data-stu-id="e9662-176">Optional</span></span> | <span data-ttu-id="e9662-177">指定法人（公司）。</span><span class="sxs-lookup"><span data-stu-id="e9662-177">Specifies the legal entity (company).</span></span>|
| <span data-ttu-id="e9662-178">**数据区域 ID 值**</span><span class="sxs-lookup"><span data-stu-id="e9662-178">**Data Area ID Value**</span></span><br><span data-ttu-id="e9662-179">_mshr_dataareaid_id_value</span><span class="sxs-lookup"><span data-stu-id="e9662-179">_mshr_dataareaid_id_value</span></span><br><span data-ttu-id="e9662-180">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e9662-180">*GUID*</span></span> | <span data-ttu-id="e9662-181">只读</span><span class="sxs-lookup"><span data-stu-id="e9662-181">Read-only</span></span><br><span data-ttu-id="e9662-182">可选</span><span class="sxs-lookup"><span data-stu-id="e9662-182">Optional</span></span><br><span data-ttu-id="e9662-183">外键：cdm_company 实体的 cdm_companyid</span><span class="sxs-lookup"><span data-stu-id="e9662-183">Foreign key: cdm_companyid of cdm_company entity</span></span> | <span data-ttu-id="e9662-184">系统生成的标识法人（公司）的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="e9662-184">System-generated GUID value identifying the legal entity (company).</span></span> |
| <span data-ttu-id="e9662-185">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="e9662-185">**Primary Field**</span></span><br><span data-ttu-id="e9662-186">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="e9662-186">mshr_primaryfield</span></span><br><span data-ttu-id="e9662-187">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e9662-187">*String*</span></span> | <span data-ttu-id="e9662-188">只读</span><span class="sxs-lookup"><span data-stu-id="e9662-188">Read-only</span></span><br><span data-ttu-id="e9662-189">必填</span><span class="sxs-lookup"><span data-stu-id="e9662-189">Required</span></span> | <span data-ttu-id="e9662-190">招聘请求值、教育程度 ID 和教育学科 ID 的串联，作为唯一标识记录的另一种方法。</span><span class="sxs-lookup"><span data-stu-id="e9662-190">Concatenation of Recruiting Request value, Education Level ID, and Education Discipline ID as another method to uniquely identify the record.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e9662-191">请参阅</span><span class="sxs-lookup"><span data-stu-id="e9662-191">See also</span></span>

[<span data-ttu-id="e9662-192">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="e9662-192">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="e9662-193">招聘请求的查询示例</span><span class="sxs-lookup"><span data-stu-id="e9662-193">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]