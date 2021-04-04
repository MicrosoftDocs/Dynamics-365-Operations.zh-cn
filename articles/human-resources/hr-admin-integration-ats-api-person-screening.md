---
title: 人员筛选
description: 本主题介绍 Dynamics 365 Human Resources 的“人员筛选”实体。
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
ms.openlocfilehash: c6287f30aaa008ea77b91fd46a8dfb2b7c905036
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467233"
---
# <a name="person-screening"></a><span data-ttu-id="4eb11-103">人员筛选</span><span class="sxs-lookup"><span data-stu-id="4eb11-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4eb11-104">本主题介绍 Dynamics 365 Human Resources 的“人员筛选”实体。</span><span class="sxs-lookup"><span data-stu-id="4eb11-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4eb11-105">物理名称：mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="4eb11-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="4eb11-106">说明</span><span class="sxs-lookup"><span data-stu-id="4eb11-106">Description</span></span>

<span data-ttu-id="4eb11-107">此实体描述应聘者已通过或必须通过才能被雇用的筛选。</span><span class="sxs-lookup"><span data-stu-id="4eb11-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4eb11-108">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="4eb11-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="4eb11-109">属性</span><span class="sxs-lookup"><span data-stu-id="4eb11-109">Properties</span></span>

| <span data-ttu-id="4eb11-110">属性</span><span class="sxs-lookup"><span data-stu-id="4eb11-110">Property</span></span><br><span data-ttu-id="4eb11-111">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="4eb11-111">**Physical name**</span></span><br><span data-ttu-id="4eb11-112">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="4eb11-112">**_Type_**</span></span> | <span data-ttu-id="4eb11-113">使用</span><span class="sxs-lookup"><span data-stu-id="4eb11-113">Use</span></span> | <span data-ttu-id="4eb11-114">说明</span><span class="sxs-lookup"><span data-stu-id="4eb11-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4eb11-115">**人员筛选实体 ID**</span><span class="sxs-lookup"><span data-stu-id="4eb11-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="4eb11-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="4eb11-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="4eb11-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4eb11-117">*GUID*</span></span> | <span data-ttu-id="4eb11-118">只读</span><span class="sxs-lookup"><span data-stu-id="4eb11-118">Read-only</span></span><br><span data-ttu-id="4eb11-119">必填</span><span class="sxs-lookup"><span data-stu-id="4eb11-119">Required</span></span><br><span data-ttu-id="4eb11-120">系统生成</span><span class="sxs-lookup"><span data-stu-id="4eb11-120">System-generated</span></span> | <span data-ttu-id="4eb11-121">人员筛选记录的唯一主要标识符。</span><span class="sxs-lookup"><span data-stu-id="4eb11-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="4eb11-122">**当事方编号**</span><span class="sxs-lookup"><span data-stu-id="4eb11-122">**Party Number**</span></span><br><span data-ttu-id="4eb11-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="4eb11-123">mshr_partynumber</span></span><br><span data-ttu-id="4eb11-124">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4eb11-124">*String*</span></span> | <span data-ttu-id="4eb11-125">读/写</span><span class="sxs-lookup"><span data-stu-id="4eb11-125">Read/write</span></span><br><span data-ttu-id="4eb11-126">必填</span><span class="sxs-lookup"><span data-stu-id="4eb11-126">Required</span></span> | <span data-ttu-id="4eb11-127">与应聘者关联的当事方（人员）编号。</span><span class="sxs-lookup"><span data-stu-id="4eb11-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="4eb11-128">**人员 ID 值**</span><span class="sxs-lookup"><span data-stu-id="4eb11-128">**Person ID Value**</span></span><br><span data-ttu-id="4eb11-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="4eb11-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="4eb11-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4eb11-130">*GUID*</span></span> | <span data-ttu-id="4eb11-131">只读</span><span class="sxs-lookup"><span data-stu-id="4eb11-131">Read-only</span></span><br><span data-ttu-id="4eb11-132">必填</span><span class="sxs-lookup"><span data-stu-id="4eb11-132">Required</span></span><br><span data-ttu-id="4eb11-133">外键：mshr_dirpersonentity 的 mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="4eb11-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="4eb11-134">系统生成的当事方（人员）实体记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="4eb11-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="4eb11-135">**筛选类型 ID**</span><span class="sxs-lookup"><span data-stu-id="4eb11-135">**Screening Type ID**</span></span><br><span data-ttu-id="4eb11-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="4eb11-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="4eb11-137">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4eb11-137">*String*</span></span> | <span data-ttu-id="4eb11-138">读/写</span><span class="sxs-lookup"><span data-stu-id="4eb11-138">Read/write</span></span><br><span data-ttu-id="4eb11-139">必填</span><span class="sxs-lookup"><span data-stu-id="4eb11-139">Required</span></span><br><span data-ttu-id="4eb11-140">外键：ScreeningType</span><span class="sxs-lookup"><span data-stu-id="4eb11-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="4eb11-141">Human Resources 中定义的筛选类型的标识符。</span><span class="sxs-lookup"><span data-stu-id="4eb11-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="4eb11-142">**筛选类型 ID 值**</span><span class="sxs-lookup"><span data-stu-id="4eb11-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="4eb11-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="4eb11-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="4eb11-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4eb11-144">*GUID*</span></span> | <span data-ttu-id="4eb11-145">只读</span><span class="sxs-lookup"><span data-stu-id="4eb11-145">Read-only</span></span><br><span data-ttu-id="4eb11-146">必填</span><span class="sxs-lookup"><span data-stu-id="4eb11-146">Required</span></span><br><span data-ttu-id="4eb11-147">外键：mshr_hcmscreeningtypeentity 的 mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="4eb11-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="4eb11-148">系统生成的关联实体中筛选类型记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="4eb11-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="4eb11-149">**需求截止日期**</span><span class="sxs-lookup"><span data-stu-id="4eb11-149">**Required By**</span></span><br><span data-ttu-id="4eb11-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="4eb11-150">mshr_requiredby</span></span><br><span data-ttu-id="4eb11-151">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="4eb11-151">*Datetime*</span></span> | <span data-ttu-id="4eb11-152">读/写</span><span class="sxs-lookup"><span data-stu-id="4eb11-152">Read/write</span></span><br><span data-ttu-id="4eb11-153">可选</span><span class="sxs-lookup"><span data-stu-id="4eb11-153">Optional</span></span> | <span data-ttu-id="4eb11-154">要求在此之前完成筛选的日期。</span><span class="sxs-lookup"><span data-stu-id="4eb11-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="4eb11-155">**状态**</span><span class="sxs-lookup"><span data-stu-id="4eb11-155">**Status**</span></span><br><span data-ttu-id="4eb11-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="4eb11-156">mshr_status</span></span><br><span data-ttu-id="4eb11-157">*mshr_hcmcompletionstatus 选项集*</span><span class="sxs-lookup"><span data-stu-id="4eb11-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="4eb11-158">读/写</span><span class="sxs-lookup"><span data-stu-id="4eb11-158">Read/write</span></span><br><span data-ttu-id="4eb11-159">必填</span><span class="sxs-lookup"><span data-stu-id="4eb11-159">Required</span></span> | <span data-ttu-id="4eb11-160">提供用于筛选的应聘者状态。</span><span class="sxs-lookup"><span data-stu-id="4eb11-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="4eb11-161">**完成日期**</span><span class="sxs-lookup"><span data-stu-id="4eb11-161">**Completed Date**</span></span><br><span data-ttu-id="4eb11-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="4eb11-162">mshr_completeddate</span></span><br><span data-ttu-id="4eb11-163">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="4eb11-163">*Datetime*</span></span> | <span data-ttu-id="4eb11-164">读/写</span><span class="sxs-lookup"><span data-stu-id="4eb11-164">Read/write</span></span><br><span data-ttu-id="4eb11-165">可选</span><span class="sxs-lookup"><span data-stu-id="4eb11-165">Optional</span></span> | <span data-ttu-id="4eb11-166">筛选完成的日期。</span><span class="sxs-lookup"><span data-stu-id="4eb11-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="4eb11-167">**说明**</span><span class="sxs-lookup"><span data-stu-id="4eb11-167">**Notes**</span></span><br><span data-ttu-id="4eb11-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="4eb11-168">mshr_note</span></span><br><span data-ttu-id="4eb11-169">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4eb11-169">*String*</span></span> | <span data-ttu-id="4eb11-170">读/写</span><span class="sxs-lookup"><span data-stu-id="4eb11-170">Read/write</span></span><br><span data-ttu-id="4eb11-171">可选</span><span class="sxs-lookup"><span data-stu-id="4eb11-171">Optional</span></span> | <span data-ttu-id="4eb11-172">招聘经理和招聘人员使用的说明。</span><span class="sxs-lookup"><span data-stu-id="4eb11-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4eb11-173">请参阅</span><span class="sxs-lookup"><span data-stu-id="4eb11-173">See also</span></span>

[<span data-ttu-id="4eb11-174">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="4eb11-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4eb11-175">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="4eb11-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]