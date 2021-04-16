---
title: 人员筛选
description: 本主题介绍 Dynamics 365 Human Resources 的“人员筛选”实体。
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
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798025"
---
# <a name="person-screening"></a><span data-ttu-id="9a35c-103">人员筛选</span><span class="sxs-lookup"><span data-stu-id="9a35c-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9a35c-104">本主题介绍 Dynamics 365 Human Resources 的“人员筛选”实体。</span><span class="sxs-lookup"><span data-stu-id="9a35c-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="9a35c-105">物理名称：mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="9a35c-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="9a35c-106">说明</span><span class="sxs-lookup"><span data-stu-id="9a35c-106">Description</span></span>

<span data-ttu-id="9a35c-107">此实体描述应聘者已通过或必须通过才能被雇用的筛选。</span><span class="sxs-lookup"><span data-stu-id="9a35c-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9a35c-108">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="9a35c-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="9a35c-109">属性</span><span class="sxs-lookup"><span data-stu-id="9a35c-109">Properties</span></span>

| <span data-ttu-id="9a35c-110">属性</span><span class="sxs-lookup"><span data-stu-id="9a35c-110">Property</span></span><br><span data-ttu-id="9a35c-111">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="9a35c-111">**Physical name**</span></span><br><span data-ttu-id="9a35c-112">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="9a35c-112">**_Type_**</span></span> | <span data-ttu-id="9a35c-113">使用</span><span class="sxs-lookup"><span data-stu-id="9a35c-113">Use</span></span> | <span data-ttu-id="9a35c-114">说明</span><span class="sxs-lookup"><span data-stu-id="9a35c-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9a35c-115">**人员筛选实体 ID**</span><span class="sxs-lookup"><span data-stu-id="9a35c-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="9a35c-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="9a35c-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="9a35c-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9a35c-117">*GUID*</span></span> | <span data-ttu-id="9a35c-118">只读</span><span class="sxs-lookup"><span data-stu-id="9a35c-118">Read-only</span></span><br><span data-ttu-id="9a35c-119">必填</span><span class="sxs-lookup"><span data-stu-id="9a35c-119">Required</span></span><br><span data-ttu-id="9a35c-120">系统生成</span><span class="sxs-lookup"><span data-stu-id="9a35c-120">System-generated</span></span> | <span data-ttu-id="9a35c-121">人员筛选记录的唯一主要标识符。</span><span class="sxs-lookup"><span data-stu-id="9a35c-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="9a35c-122">**当事方编号**</span><span class="sxs-lookup"><span data-stu-id="9a35c-122">**Party Number**</span></span><br><span data-ttu-id="9a35c-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="9a35c-123">mshr_partynumber</span></span><br><span data-ttu-id="9a35c-124">*字符串*</span><span class="sxs-lookup"><span data-stu-id="9a35c-124">*String*</span></span> | <span data-ttu-id="9a35c-125">读/写</span><span class="sxs-lookup"><span data-stu-id="9a35c-125">Read/write</span></span><br><span data-ttu-id="9a35c-126">必填</span><span class="sxs-lookup"><span data-stu-id="9a35c-126">Required</span></span> | <span data-ttu-id="9a35c-127">与应聘者关联的当事方（人员）编号。</span><span class="sxs-lookup"><span data-stu-id="9a35c-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="9a35c-128">**人员 ID 值**</span><span class="sxs-lookup"><span data-stu-id="9a35c-128">**Person ID Value**</span></span><br><span data-ttu-id="9a35c-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="9a35c-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="9a35c-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9a35c-130">*GUID*</span></span> | <span data-ttu-id="9a35c-131">只读</span><span class="sxs-lookup"><span data-stu-id="9a35c-131">Read-only</span></span><br><span data-ttu-id="9a35c-132">必填</span><span class="sxs-lookup"><span data-stu-id="9a35c-132">Required</span></span><br><span data-ttu-id="9a35c-133">外键：mshr_dirpersonentity 的 mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="9a35c-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="9a35c-134">系统生成的当事方（人员）实体记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="9a35c-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="9a35c-135">**筛选类型 ID**</span><span class="sxs-lookup"><span data-stu-id="9a35c-135">**Screening Type ID**</span></span><br><span data-ttu-id="9a35c-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="9a35c-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="9a35c-137">*字符串*</span><span class="sxs-lookup"><span data-stu-id="9a35c-137">*String*</span></span> | <span data-ttu-id="9a35c-138">读/写</span><span class="sxs-lookup"><span data-stu-id="9a35c-138">Read/write</span></span><br><span data-ttu-id="9a35c-139">必填</span><span class="sxs-lookup"><span data-stu-id="9a35c-139">Required</span></span><br><span data-ttu-id="9a35c-140">外键：ScreeningType</span><span class="sxs-lookup"><span data-stu-id="9a35c-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="9a35c-141">Human Resources 中定义的筛选类型的标识符。</span><span class="sxs-lookup"><span data-stu-id="9a35c-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="9a35c-142">**筛选类型 ID 值**</span><span class="sxs-lookup"><span data-stu-id="9a35c-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="9a35c-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="9a35c-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="9a35c-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9a35c-144">*GUID*</span></span> | <span data-ttu-id="9a35c-145">只读</span><span class="sxs-lookup"><span data-stu-id="9a35c-145">Read-only</span></span><br><span data-ttu-id="9a35c-146">必填</span><span class="sxs-lookup"><span data-stu-id="9a35c-146">Required</span></span><br><span data-ttu-id="9a35c-147">外键：mshr_hcmscreeningtypeentity 的 mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="9a35c-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="9a35c-148">系统生成的关联实体中筛选类型记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="9a35c-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="9a35c-149">**需求截止日期**</span><span class="sxs-lookup"><span data-stu-id="9a35c-149">**Required By**</span></span><br><span data-ttu-id="9a35c-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="9a35c-150">mshr_requiredby</span></span><br><span data-ttu-id="9a35c-151">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="9a35c-151">*Datetime*</span></span> | <span data-ttu-id="9a35c-152">读/写</span><span class="sxs-lookup"><span data-stu-id="9a35c-152">Read/write</span></span><br><span data-ttu-id="9a35c-153">可选</span><span class="sxs-lookup"><span data-stu-id="9a35c-153">Optional</span></span> | <span data-ttu-id="9a35c-154">要求在此之前完成筛选的日期。</span><span class="sxs-lookup"><span data-stu-id="9a35c-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="9a35c-155">**状态**</span><span class="sxs-lookup"><span data-stu-id="9a35c-155">**Status**</span></span><br><span data-ttu-id="9a35c-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="9a35c-156">mshr_status</span></span><br><span data-ttu-id="9a35c-157">*mshr_hcmcompletionstatus 选项集*</span><span class="sxs-lookup"><span data-stu-id="9a35c-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="9a35c-158">读/写</span><span class="sxs-lookup"><span data-stu-id="9a35c-158">Read/write</span></span><br><span data-ttu-id="9a35c-159">必填</span><span class="sxs-lookup"><span data-stu-id="9a35c-159">Required</span></span> | <span data-ttu-id="9a35c-160">提供用于筛选的应聘者状态。</span><span class="sxs-lookup"><span data-stu-id="9a35c-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="9a35c-161">**完成日期**</span><span class="sxs-lookup"><span data-stu-id="9a35c-161">**Completed Date**</span></span><br><span data-ttu-id="9a35c-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="9a35c-162">mshr_completeddate</span></span><br><span data-ttu-id="9a35c-163">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="9a35c-163">*Datetime*</span></span> | <span data-ttu-id="9a35c-164">读/写</span><span class="sxs-lookup"><span data-stu-id="9a35c-164">Read/write</span></span><br><span data-ttu-id="9a35c-165">可选</span><span class="sxs-lookup"><span data-stu-id="9a35c-165">Optional</span></span> | <span data-ttu-id="9a35c-166">筛选完成的日期。</span><span class="sxs-lookup"><span data-stu-id="9a35c-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="9a35c-167">**说明**</span><span class="sxs-lookup"><span data-stu-id="9a35c-167">**Notes**</span></span><br><span data-ttu-id="9a35c-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="9a35c-168">mshr_note</span></span><br><span data-ttu-id="9a35c-169">*字符串*</span><span class="sxs-lookup"><span data-stu-id="9a35c-169">*String*</span></span> | <span data-ttu-id="9a35c-170">读/写</span><span class="sxs-lookup"><span data-stu-id="9a35c-170">Read/write</span></span><br><span data-ttu-id="9a35c-171">可选</span><span class="sxs-lookup"><span data-stu-id="9a35c-171">Optional</span></span> | <span data-ttu-id="9a35c-172">招聘经理和招聘人员使用的说明。</span><span class="sxs-lookup"><span data-stu-id="9a35c-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="9a35c-173">请参阅</span><span class="sxs-lookup"><span data-stu-id="9a35c-173">See also</span></span>

[<span data-ttu-id="9a35c-174">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="9a35c-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="9a35c-175">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="9a35c-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]