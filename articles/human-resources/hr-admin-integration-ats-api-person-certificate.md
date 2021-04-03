---
title: 人员证书
description: 本主题介绍 Dynamics 365 Human Resources 的“人员证书”实体。
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
ms.openlocfilehash: 4587337d8fd52828309826f3301b6f053b267819
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466512"
---
# <a name="person-certificate"></a><span data-ttu-id="4a970-103">人员证书</span><span class="sxs-lookup"><span data-stu-id="4a970-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4a970-104">本主题介绍 Dynamics 365 Human Resources 的“人员证书”实体。</span><span class="sxs-lookup"><span data-stu-id="4a970-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4a970-105">物理名称：mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="4a970-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="4a970-106">说明</span><span class="sxs-lookup"><span data-stu-id="4a970-106">Description</span></span>

<span data-ttu-id="4a970-107">此实体描述应聘者的专业证书。</span><span class="sxs-lookup"><span data-stu-id="4a970-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4a970-108">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="4a970-108">JSON representation</span></span>

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="4a970-109">属性</span><span class="sxs-lookup"><span data-stu-id="4a970-109">Properties</span></span>

| <span data-ttu-id="4a970-110">属性</span><span class="sxs-lookup"><span data-stu-id="4a970-110">Property</span></span><br><span data-ttu-id="4a970-111">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="4a970-111">**Physical name**</span></span><br><span data-ttu-id="4a970-112">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="4a970-112">**_Type_**</span></span> | <span data-ttu-id="4a970-113">使用</span><span class="sxs-lookup"><span data-stu-id="4a970-113">Use</span></span> | <span data-ttu-id="4a970-114">说明</span><span class="sxs-lookup"><span data-stu-id="4a970-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4a970-115">**人员证书实体 ID**</span><span class="sxs-lookup"><span data-stu-id="4a970-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="4a970-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="4a970-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="4a970-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4a970-117">*GUID*</span></span> | <span data-ttu-id="4a970-118">只读</span><span class="sxs-lookup"><span data-stu-id="4a970-118">Read-only</span></span><br><span data-ttu-id="4a970-119">必填</span><span class="sxs-lookup"><span data-stu-id="4a970-119">Required</span></span> | <span data-ttu-id="4a970-120">系统生成的人员证书实体记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="4a970-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="4a970-121">**当事方编号**</span><span class="sxs-lookup"><span data-stu-id="4a970-121">**Party Number**</span></span><br><span data-ttu-id="4a970-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="4a970-122">mshr_partynumber</span></span><br><span data-ttu-id="4a970-123">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4a970-123">*String*</span></span> | <span data-ttu-id="4a970-124">读/写</span><span class="sxs-lookup"><span data-stu-id="4a970-124">Read/write</span></span><br><span data-ttu-id="4a970-125">必填</span><span class="sxs-lookup"><span data-stu-id="4a970-125">Required</span></span> | <span data-ttu-id="4a970-126">应聘者的当事方（人员）ID。</span><span class="sxs-lookup"><span data-stu-id="4a970-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="4a970-127">**人员 ID 值**</span><span class="sxs-lookup"><span data-stu-id="4a970-127">**Person ID Value**</span></span><br><span data-ttu-id="4a970-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="4a970-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="4a970-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4a970-129">*GUID*</span></span> | <span data-ttu-id="4a970-130">只读</span><span class="sxs-lookup"><span data-stu-id="4a970-130">Read-only</span></span><br><span data-ttu-id="4a970-131">必填</span><span class="sxs-lookup"><span data-stu-id="4a970-131">Required</span></span><br><span data-ttu-id="4a970-132">外键：mshr_dirpersonentity 的 mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="4a970-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="4a970-133">系统生成的当事方（人员）实体记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="4a970-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="4a970-134">**证书类型 ID**</span><span class="sxs-lookup"><span data-stu-id="4a970-134">**Certificate Type ID**</span></span><br><span data-ttu-id="4a970-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="4a970-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="4a970-136">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4a970-136">*String*</span></span> | <span data-ttu-id="4a970-137">读/写</span><span class="sxs-lookup"><span data-stu-id="4a970-137">Read/write</span></span><br><span data-ttu-id="4a970-138">必填</span><span class="sxs-lookup"><span data-stu-id="4a970-138">Required</span></span> |  <span data-ttu-id="4a970-139">Human Resources 中定义的证书类型的标识符。</span><span class="sxs-lookup"><span data-stu-id="4a970-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="4a970-140">**证书类型 ID 值**</span><span class="sxs-lookup"><span data-stu-id="4a970-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="4a970-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="4a970-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="4a970-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4a970-142">*GUID*</span></span> | <span data-ttu-id="4a970-143">只读</span><span class="sxs-lookup"><span data-stu-id="4a970-143">Read-only</span></span><br><span data-ttu-id="4a970-144">必填</span><span class="sxs-lookup"><span data-stu-id="4a970-144">Required</span></span><br><span data-ttu-id="4a970-145">外键：mshr_hcmcertificatetypeentity 的 mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="4a970-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="4a970-146">系统生成的关联实体中证书类型的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="4a970-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="4a970-147">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="4a970-147">**Start Date**</span></span><br><span data-ttu-id="4a970-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="4a970-148">mshr_startdate</span></span><br><span data-ttu-id="4a970-149">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="4a970-149">*Datetime*</span></span> | <span data-ttu-id="4a970-150">读/写</span><span class="sxs-lookup"><span data-stu-id="4a970-150">Read/write</span></span><br><span data-ttu-id="4a970-151">必填</span><span class="sxs-lookup"><span data-stu-id="4a970-151">Required</span></span> | <span data-ttu-id="4a970-152">颁发证书的日期。</span><span class="sxs-lookup"><span data-stu-id="4a970-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="4a970-153">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="4a970-153">**End Date**</span></span><br><span data-ttu-id="4a970-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="4a970-154">mshr_enddate</span></span><br><span data-ttu-id="4a970-155">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="4a970-155">*Datetime*</span></span> | <span data-ttu-id="4a970-156">读/写</span><span class="sxs-lookup"><span data-stu-id="4a970-156">Read/write</span></span><br><span data-ttu-id="4a970-157">可选</span><span class="sxs-lookup"><span data-stu-id="4a970-157">Optional</span></span> | <span data-ttu-id="4a970-158">证书到期的日期。</span><span class="sxs-lookup"><span data-stu-id="4a970-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="4a970-159">**说明**</span><span class="sxs-lookup"><span data-stu-id="4a970-159">**Notes**</span></span><br><span data-ttu-id="4a970-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="4a970-160">mshr_notes</span></span><br><span data-ttu-id="4a970-161">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4a970-161">*String*</span></span> | <span data-ttu-id="4a970-162">读/写</span><span class="sxs-lookup"><span data-stu-id="4a970-162">Read/write</span></span><br><span data-ttu-id="4a970-163">可选</span><span class="sxs-lookup"><span data-stu-id="4a970-163">Optional</span></span> | <span data-ttu-id="4a970-164">招聘经理和招聘人员使用的说明。</span><span class="sxs-lookup"><span data-stu-id="4a970-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="4a970-165">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="4a970-165">**Primary Field**</span></span><br><span data-ttu-id="4a970-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="4a970-166">mshr_primaryfield</span></span><br><span data-ttu-id="4a970-167">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4a970-167">*String*</span></span> | <span data-ttu-id="4a970-168">只读</span><span class="sxs-lookup"><span data-stu-id="4a970-168">Read-only</span></span><br><span data-ttu-id="4a970-169">必填</span><span class="sxs-lookup"><span data-stu-id="4a970-169">Required</span></span> |  <span data-ttu-id="4a970-170">用作实体记录的标识符的字段。</span><span class="sxs-lookup"><span data-stu-id="4a970-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="4a970-171">当事方编号、证书类型 ID 和开始日期的组合。</span><span class="sxs-lookup"><span data-stu-id="4a970-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4a970-172">请参阅</span><span class="sxs-lookup"><span data-stu-id="4a970-172">See also</span></span>

[<span data-ttu-id="4a970-173">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="4a970-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4a970-174">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="4a970-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]