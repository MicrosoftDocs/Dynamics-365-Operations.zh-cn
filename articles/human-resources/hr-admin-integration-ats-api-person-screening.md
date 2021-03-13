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
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125369"
---
# <a name="person-screening"></a><span data-ttu-id="b7565-103">人员筛选</span><span class="sxs-lookup"><span data-stu-id="b7565-103">Person screening</span></span>

<span data-ttu-id="b7565-104">本主题介绍 Dynamics 365 Human Resources 的“人员筛选”实体。</span><span class="sxs-lookup"><span data-stu-id="b7565-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b7565-105">物理名称：mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="b7565-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="b7565-106">说明</span><span class="sxs-lookup"><span data-stu-id="b7565-106">Description</span></span>

<span data-ttu-id="b7565-107">此实体描述应聘者已通过或必须通过才能被雇用的筛选。</span><span class="sxs-lookup"><span data-stu-id="b7565-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b7565-108">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="b7565-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="b7565-109">属性</span><span class="sxs-lookup"><span data-stu-id="b7565-109">Properties</span></span>

| <span data-ttu-id="b7565-110">属性</span><span class="sxs-lookup"><span data-stu-id="b7565-110">Property</span></span><br><span data-ttu-id="b7565-111">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="b7565-111">**Physical name**</span></span><br><span data-ttu-id="b7565-112">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="b7565-112">**_Type_**</span></span> | <span data-ttu-id="b7565-113">使用</span><span class="sxs-lookup"><span data-stu-id="b7565-113">Use</span></span> | <span data-ttu-id="b7565-114">说明</span><span class="sxs-lookup"><span data-stu-id="b7565-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b7565-115">**人员筛选实体 ID**</span><span class="sxs-lookup"><span data-stu-id="b7565-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="b7565-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="b7565-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="b7565-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b7565-117">*GUID*</span></span> | <span data-ttu-id="b7565-118">只读</span><span class="sxs-lookup"><span data-stu-id="b7565-118">Read-only</span></span><br><span data-ttu-id="b7565-119">必填</span><span class="sxs-lookup"><span data-stu-id="b7565-119">Required</span></span><br><span data-ttu-id="b7565-120">系统生成</span><span class="sxs-lookup"><span data-stu-id="b7565-120">System-generated</span></span> | <span data-ttu-id="b7565-121">人员筛选记录的唯一主要标识符。</span><span class="sxs-lookup"><span data-stu-id="b7565-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="b7565-122">**当事方编号**</span><span class="sxs-lookup"><span data-stu-id="b7565-122">**Party Number**</span></span><br><span data-ttu-id="b7565-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="b7565-123">mshr_partynumber</span></span><br><span data-ttu-id="b7565-124">*字符串*</span><span class="sxs-lookup"><span data-stu-id="b7565-124">*String*</span></span> | <span data-ttu-id="b7565-125">读/写</span><span class="sxs-lookup"><span data-stu-id="b7565-125">Read/write</span></span><br><span data-ttu-id="b7565-126">必填</span><span class="sxs-lookup"><span data-stu-id="b7565-126">Required</span></span> | <span data-ttu-id="b7565-127">与应聘者关联的当事方（人员）编号。</span><span class="sxs-lookup"><span data-stu-id="b7565-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="b7565-128">**人员 ID 值**</span><span class="sxs-lookup"><span data-stu-id="b7565-128">**Person ID Value**</span></span><br><span data-ttu-id="b7565-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="b7565-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="b7565-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b7565-130">*GUID*</span></span> | <span data-ttu-id="b7565-131">只读</span><span class="sxs-lookup"><span data-stu-id="b7565-131">Read-only</span></span><br><span data-ttu-id="b7565-132">必填</span><span class="sxs-lookup"><span data-stu-id="b7565-132">Required</span></span><br><span data-ttu-id="b7565-133">外键：mshr_dirpersonentity 的 mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="b7565-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="b7565-134">系统生成的当事方（人员）实体记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="b7565-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="b7565-135">**筛选类型 ID**</span><span class="sxs-lookup"><span data-stu-id="b7565-135">**Screening Type ID**</span></span><br><span data-ttu-id="b7565-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="b7565-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="b7565-137">*字符串*</span><span class="sxs-lookup"><span data-stu-id="b7565-137">*String*</span></span> | <span data-ttu-id="b7565-138">读/写</span><span class="sxs-lookup"><span data-stu-id="b7565-138">Read/write</span></span><br><span data-ttu-id="b7565-139">必填</span><span class="sxs-lookup"><span data-stu-id="b7565-139">Required</span></span><br><span data-ttu-id="b7565-140">外键：ScreeningType</span><span class="sxs-lookup"><span data-stu-id="b7565-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="b7565-141">Human Resources 中定义的筛选类型的标识符。</span><span class="sxs-lookup"><span data-stu-id="b7565-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="b7565-142">**筛选类型 ID 值**</span><span class="sxs-lookup"><span data-stu-id="b7565-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="b7565-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="b7565-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="b7565-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b7565-144">*GUID*</span></span> | <span data-ttu-id="b7565-145">只读</span><span class="sxs-lookup"><span data-stu-id="b7565-145">Read-only</span></span><br><span data-ttu-id="b7565-146">必填</span><span class="sxs-lookup"><span data-stu-id="b7565-146">Required</span></span><br><span data-ttu-id="b7565-147">外键：mshr_hcmscreeningtypeentity 的 mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="b7565-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="b7565-148">系统生成的关联实体中筛选类型记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="b7565-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="b7565-149">**需求截止日期**</span><span class="sxs-lookup"><span data-stu-id="b7565-149">**Required By**</span></span><br><span data-ttu-id="b7565-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="b7565-150">mshr_requiredby</span></span><br><span data-ttu-id="b7565-151">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="b7565-151">*Datetime*</span></span> | <span data-ttu-id="b7565-152">读/写</span><span class="sxs-lookup"><span data-stu-id="b7565-152">Read/write</span></span><br><span data-ttu-id="b7565-153">可选</span><span class="sxs-lookup"><span data-stu-id="b7565-153">Optional</span></span> | <span data-ttu-id="b7565-154">要求在此之前完成筛选的日期。</span><span class="sxs-lookup"><span data-stu-id="b7565-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="b7565-155">**状态**</span><span class="sxs-lookup"><span data-stu-id="b7565-155">**Status**</span></span><br><span data-ttu-id="b7565-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="b7565-156">mshr_status</span></span><br><span data-ttu-id="b7565-157">*mshr_hcmcompletionstatus 选项集*</span><span class="sxs-lookup"><span data-stu-id="b7565-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="b7565-158">读/写</span><span class="sxs-lookup"><span data-stu-id="b7565-158">Read/write</span></span><br><span data-ttu-id="b7565-159">必填</span><span class="sxs-lookup"><span data-stu-id="b7565-159">Required</span></span> | <span data-ttu-id="b7565-160">提供用于筛选的应聘者状态。</span><span class="sxs-lookup"><span data-stu-id="b7565-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="b7565-161">**完成日期**</span><span class="sxs-lookup"><span data-stu-id="b7565-161">**Completed Date**</span></span><br><span data-ttu-id="b7565-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="b7565-162">mshr_completeddate</span></span><br><span data-ttu-id="b7565-163">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="b7565-163">*Datetime*</span></span> | <span data-ttu-id="b7565-164">读/写</span><span class="sxs-lookup"><span data-stu-id="b7565-164">Read/write</span></span><br><span data-ttu-id="b7565-165">可选</span><span class="sxs-lookup"><span data-stu-id="b7565-165">Optional</span></span> | <span data-ttu-id="b7565-166">筛选完成的日期。</span><span class="sxs-lookup"><span data-stu-id="b7565-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="b7565-167">**说明**</span><span class="sxs-lookup"><span data-stu-id="b7565-167">**Notes**</span></span><br><span data-ttu-id="b7565-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="b7565-168">mshr_note</span></span><br><span data-ttu-id="b7565-169">*字符串*</span><span class="sxs-lookup"><span data-stu-id="b7565-169">*String*</span></span> | <span data-ttu-id="b7565-170">读/写</span><span class="sxs-lookup"><span data-stu-id="b7565-170">Read/write</span></span><br><span data-ttu-id="b7565-171">可选</span><span class="sxs-lookup"><span data-stu-id="b7565-171">Optional</span></span> | <span data-ttu-id="b7565-172">招聘经理和招聘人员使用的说明。</span><span class="sxs-lookup"><span data-stu-id="b7565-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b7565-173">请参阅</span><span class="sxs-lookup"><span data-stu-id="b7565-173">See also</span></span>

[<span data-ttu-id="b7565-174">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="b7565-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="b7565-175">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="b7565-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

