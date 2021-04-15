---
title: 人员证书
description: 本主题介绍 Dynamics 365 Human Resources 的“人员证书”实体。
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
ms.openlocfilehash: 796a57a5f97de08ff8c8440bc00d4dc5ced18f58
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798121"
---
# <a name="person-certificate"></a><span data-ttu-id="53af1-103">人员证书</span><span class="sxs-lookup"><span data-stu-id="53af1-103">Person certificate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="53af1-104">本主题介绍 Dynamics 365 Human Resources 的“人员证书”实体。</span><span class="sxs-lookup"><span data-stu-id="53af1-104">This topic describes the Person certificate entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="53af1-105">物理名称：mshr_hcmpersoncertificateentity</span><span class="sxs-lookup"><span data-stu-id="53af1-105">Physical name: mshr_hcmpersoncertificateentity</span></span>

## <a name="description"></a><span data-ttu-id="53af1-106">说明</span><span class="sxs-lookup"><span data-stu-id="53af1-106">Description</span></span>

<span data-ttu-id="53af1-107">此实体描述应聘者的专业证书。</span><span class="sxs-lookup"><span data-stu-id="53af1-107">This entity describes the professional certificates of a candidate.</span></span>

## <a name="json-representation"></a><span data-ttu-id="53af1-108">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="53af1-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="53af1-109">属性</span><span class="sxs-lookup"><span data-stu-id="53af1-109">Properties</span></span>

| <span data-ttu-id="53af1-110">属性</span><span class="sxs-lookup"><span data-stu-id="53af1-110">Property</span></span><br><span data-ttu-id="53af1-111">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="53af1-111">**Physical name**</span></span><br><span data-ttu-id="53af1-112">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="53af1-112">**_Type_**</span></span> | <span data-ttu-id="53af1-113">使用</span><span class="sxs-lookup"><span data-stu-id="53af1-113">Use</span></span> | <span data-ttu-id="53af1-114">说明</span><span class="sxs-lookup"><span data-stu-id="53af1-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="53af1-115">**人员证书实体 ID**</span><span class="sxs-lookup"><span data-stu-id="53af1-115">**Person Certificate Entity ID**</span></span><br><span data-ttu-id="53af1-116">mshr_hcmpersoncertificateentityid</span><span class="sxs-lookup"><span data-stu-id="53af1-116">mshr_hcmpersoncertificateentityid</span></span><br><span data-ttu-id="53af1-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="53af1-117">*GUID*</span></span> | <span data-ttu-id="53af1-118">只读</span><span class="sxs-lookup"><span data-stu-id="53af1-118">Read-only</span></span><br><span data-ttu-id="53af1-119">必填</span><span class="sxs-lookup"><span data-stu-id="53af1-119">Required</span></span> | <span data-ttu-id="53af1-120">系统生成的人员证书实体记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="53af1-120">System-generated unique identifier for the person certificate entity record.</span></span> |
| <span data-ttu-id="53af1-121">**当事方编号**</span><span class="sxs-lookup"><span data-stu-id="53af1-121">**Party Number**</span></span><br><span data-ttu-id="53af1-122">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="53af1-122">mshr_partynumber</span></span><br><span data-ttu-id="53af1-123">*字符串*</span><span class="sxs-lookup"><span data-stu-id="53af1-123">*String*</span></span> | <span data-ttu-id="53af1-124">读/写</span><span class="sxs-lookup"><span data-stu-id="53af1-124">Read/write</span></span><br><span data-ttu-id="53af1-125">必填</span><span class="sxs-lookup"><span data-stu-id="53af1-125">Required</span></span> | <span data-ttu-id="53af1-126">应聘者的当事方（人员）ID。</span><span class="sxs-lookup"><span data-stu-id="53af1-126">The party (person) ID of the candidate.</span></span> |
| <span data-ttu-id="53af1-127">**人员 ID 值**</span><span class="sxs-lookup"><span data-stu-id="53af1-127">**Person ID Value**</span></span><br><span data-ttu-id="53af1-128">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="53af1-128">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="53af1-129">*GUID*</span><span class="sxs-lookup"><span data-stu-id="53af1-129">*GUID*</span></span> | <span data-ttu-id="53af1-130">只读</span><span class="sxs-lookup"><span data-stu-id="53af1-130">Read-only</span></span><br><span data-ttu-id="53af1-131">必填</span><span class="sxs-lookup"><span data-stu-id="53af1-131">Required</span></span><br><span data-ttu-id="53af1-132">外键：mshr_dirpersonentity 的 mshr_dirpersonentityid</span><span class="sxs-lookup"><span data-stu-id="53af1-132">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="53af1-133">系统生成的当事方（人员）实体记录的标识符。</span><span class="sxs-lookup"><span data-stu-id="53af1-133">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="53af1-134">**证书类型 ID**</span><span class="sxs-lookup"><span data-stu-id="53af1-134">**Certificate Type ID**</span></span><br><span data-ttu-id="53af1-135">mshr_certificatetypeid</span><span class="sxs-lookup"><span data-stu-id="53af1-135">mshr_certificatetypeid</span></span><br><span data-ttu-id="53af1-136">*字符串*</span><span class="sxs-lookup"><span data-stu-id="53af1-136">*String*</span></span> | <span data-ttu-id="53af1-137">读/写</span><span class="sxs-lookup"><span data-stu-id="53af1-137">Read/write</span></span><br><span data-ttu-id="53af1-138">必填</span><span class="sxs-lookup"><span data-stu-id="53af1-138">Required</span></span> |  <span data-ttu-id="53af1-139">Human Resources 中定义的证书类型的标识符。</span><span class="sxs-lookup"><span data-stu-id="53af1-139">The identifier of the certificate type defined in Human Resources.</span></span> |
| <span data-ttu-id="53af1-140">**证书类型 ID 值**</span><span class="sxs-lookup"><span data-stu-id="53af1-140">**Certificate Type ID Value**</span></span><br><span data-ttu-id="53af1-141">_mshr_fk_certificatetype_id_value</span><span class="sxs-lookup"><span data-stu-id="53af1-141">_mshr_fk_certificatetype_id_value</span></span><br><span data-ttu-id="53af1-142">*GUID*</span><span class="sxs-lookup"><span data-stu-id="53af1-142">*GUID*</span></span> | <span data-ttu-id="53af1-143">只读</span><span class="sxs-lookup"><span data-stu-id="53af1-143">Read-only</span></span><br><span data-ttu-id="53af1-144">必填</span><span class="sxs-lookup"><span data-stu-id="53af1-144">Required</span></span><br><span data-ttu-id="53af1-145">外键：mshr_hcmcertificatetypeentity 的 mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="53af1-145">Foreign key: mshr_hcmcertificatetypeentityid of mshr_hcmcertificatetypeentity</span></span> | <span data-ttu-id="53af1-146">系统生成的关联实体中证书类型的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="53af1-146">System-generated unique identifier of the certificate type in the associated entity.</span></span> |
| <span data-ttu-id="53af1-147">**开始日期**</span><span class="sxs-lookup"><span data-stu-id="53af1-147">**Start Date**</span></span><br><span data-ttu-id="53af1-148">mshr_startdate</span><span class="sxs-lookup"><span data-stu-id="53af1-148">mshr_startdate</span></span><br><span data-ttu-id="53af1-149">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="53af1-149">*Datetime*</span></span> | <span data-ttu-id="53af1-150">读/写</span><span class="sxs-lookup"><span data-stu-id="53af1-150">Read/write</span></span><br><span data-ttu-id="53af1-151">必填</span><span class="sxs-lookup"><span data-stu-id="53af1-151">Required</span></span> | <span data-ttu-id="53af1-152">颁发证书的日期。</span><span class="sxs-lookup"><span data-stu-id="53af1-152">The date at which the certificate was issued.</span></span> |
| <span data-ttu-id="53af1-153">**结束日期**</span><span class="sxs-lookup"><span data-stu-id="53af1-153">**End Date**</span></span><br><span data-ttu-id="53af1-154">mshr_enddate</span><span class="sxs-lookup"><span data-stu-id="53af1-154">mshr_enddate</span></span><br><span data-ttu-id="53af1-155">*日期/时间*</span><span class="sxs-lookup"><span data-stu-id="53af1-155">*Datetime*</span></span> | <span data-ttu-id="53af1-156">读/写</span><span class="sxs-lookup"><span data-stu-id="53af1-156">Read/write</span></span><br><span data-ttu-id="53af1-157">可选</span><span class="sxs-lookup"><span data-stu-id="53af1-157">Optional</span></span> | <span data-ttu-id="53af1-158">证书到期的日期。</span><span class="sxs-lookup"><span data-stu-id="53af1-158">The date at which the certificate will expire.</span></span> |
| <span data-ttu-id="53af1-159">**说明**</span><span class="sxs-lookup"><span data-stu-id="53af1-159">**Notes**</span></span><br><span data-ttu-id="53af1-160">mshr_notes</span><span class="sxs-lookup"><span data-stu-id="53af1-160">mshr_notes</span></span><br><span data-ttu-id="53af1-161">*字符串*</span><span class="sxs-lookup"><span data-stu-id="53af1-161">*String*</span></span> | <span data-ttu-id="53af1-162">读/写</span><span class="sxs-lookup"><span data-stu-id="53af1-162">Read/write</span></span><br><span data-ttu-id="53af1-163">可选</span><span class="sxs-lookup"><span data-stu-id="53af1-163">Optional</span></span> | <span data-ttu-id="53af1-164">招聘经理和招聘人员使用的说明。</span><span class="sxs-lookup"><span data-stu-id="53af1-164">Notes for use by hiring managers and recruiters.</span></span> |
| <span data-ttu-id="53af1-165">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="53af1-165">**Primary Field**</span></span><br><span data-ttu-id="53af1-166">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="53af1-166">mshr_primaryfield</span></span><br><span data-ttu-id="53af1-167">*字符串*</span><span class="sxs-lookup"><span data-stu-id="53af1-167">*String*</span></span> | <span data-ttu-id="53af1-168">只读</span><span class="sxs-lookup"><span data-stu-id="53af1-168">Read-only</span></span><br><span data-ttu-id="53af1-169">必填</span><span class="sxs-lookup"><span data-stu-id="53af1-169">Required</span></span> |  <span data-ttu-id="53af1-170">用作实体记录的标识符的字段。</span><span class="sxs-lookup"><span data-stu-id="53af1-170">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="53af1-171">当事方编号、证书类型 ID 和开始日期的组合。</span><span class="sxs-lookup"><span data-stu-id="53af1-171">Combination of party number, certificate type ID, and start date.</span></span> |

## <a name="see-also"></a><span data-ttu-id="53af1-172">请参阅</span><span class="sxs-lookup"><span data-stu-id="53af1-172">See also</span></span>

[<span data-ttu-id="53af1-173">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="53af1-173">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="53af1-174">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="53af1-174">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]