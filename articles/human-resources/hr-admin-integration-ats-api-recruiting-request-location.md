---
title: 招聘请求位置
description: 本主题介绍 Dynamics 365 Human Resources 的“招聘请求位置”实体。
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
ms.openlocfilehash: 9a3b47c76094adb6c601daf2f9583116255b0a99
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465934"
---
# <a name="recruiting-request-location"></a><span data-ttu-id="f794a-103">招聘请求位置</span><span class="sxs-lookup"><span data-stu-id="f794a-103">Recruiting request location</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="f794a-104">本主题介绍 Dynamics 365 Human Resources 的“招聘请求位置”实体。</span><span class="sxs-lookup"><span data-stu-id="f794a-104">This topic describes the Recruiting request location entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="f794a-105">物理名称：mshr_hcmrecruitingrequestlocationentity</span><span class="sxs-lookup"><span data-stu-id="f794a-105">Physical name: mshr_hcmrecruitingrequestlocationentity</span></span>

### <a name="description"></a><span data-ttu-id="f794a-106">说明</span><span class="sxs-lookup"><span data-stu-id="f794a-106">Description</span></span>

<span data-ttu-id="f794a-107">定义为招聘的员工雇用后的工作位置的位置列表。</span><span class="sxs-lookup"><span data-stu-id="f794a-107">The list of locations defined as locations where recruited employees will work upon hiring.</span></span> <span data-ttu-id="f794a-108">这些是跨法人创建的位置。</span><span class="sxs-lookup"><span data-stu-id="f794a-108">These are locations created across legal entities.</span></span>

### <a name="json-representation"></a><span data-ttu-id="f794a-109">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="f794a-109">JSON representation</span></span>

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a><span data-ttu-id="f794a-110">属性</span><span class="sxs-lookup"><span data-stu-id="f794a-110">Properties</span></span>

| <span data-ttu-id="f794a-111">属性</span><span class="sxs-lookup"><span data-stu-id="f794a-111">Property</span></span><br><span data-ttu-id="f794a-112">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="f794a-112">**Physical name**</span></span><br><span data-ttu-id="f794a-113">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="f794a-113">**_Type_**</span></span> | <span data-ttu-id="f794a-114">使用</span><span class="sxs-lookup"><span data-stu-id="f794a-114">Use</span></span> | <span data-ttu-id="f794a-115">说明</span><span class="sxs-lookup"><span data-stu-id="f794a-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="f794a-116">**位置 ID**</span><span class="sxs-lookup"><span data-stu-id="f794a-116">**Location ID**</span></span><br><span data-ttu-id="f794a-117">mshr_locationid</span><span class="sxs-lookup"><span data-stu-id="f794a-117">mshr_locationid</span></span><br><span data-ttu-id="f794a-118">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-118">*String*</span></span> | <span data-ttu-id="f794a-119">写入一次</span><span class="sxs-lookup"><span data-stu-id="f794a-119">Write-once</span></span><br><span data-ttu-id="f794a-120">必填</span><span class="sxs-lookup"><span data-stu-id="f794a-120">Required</span></span> | <span data-ttu-id="f794a-121">系统生成的用户可读的招聘位置的标识符。</span><span class="sxs-lookup"><span data-stu-id="f794a-121">The system-generated, user-readable identifier for the recruiting location.</span></span> |
| <span data-ttu-id="f794a-122">**招聘请求位置**</span><span class="sxs-lookup"><span data-stu-id="f794a-122">**Recruiting Request Location**</span></span><br><span data-ttu-id="f794a-123">mshr_recruitingrequestlocationid</span><span class="sxs-lookup"><span data-stu-id="f794a-123">mshr_recruitingrequestlocationid</span></span><br><span data-ttu-id="f794a-124">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-124">*String*</span></span> | <span data-ttu-id="f794a-125">写入一次</span><span class="sxs-lookup"><span data-stu-id="f794a-125">Write-once</span></span><br><span data-ttu-id="f794a-126">必填</span><span class="sxs-lookup"><span data-stu-id="f794a-126">Required</span></span> | <span data-ttu-id="f794a-127">用户定义的招聘位置的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="f794a-127">User-defined unique identifier for the recruiting location.</span></span> |
| <span data-ttu-id="f794a-128">**招聘请求位置实体 ID**</span><span class="sxs-lookup"><span data-stu-id="f794a-128">**Recruiting Request Location Entity ID**</span></span><br><span data-ttu-id="f794a-129">mshr_hcmrecruitingrequestlocationentityid</span><span class="sxs-lookup"><span data-stu-id="f794a-129">mshr_hcmrecruitingrequestlocationentityid</span></span><br><span data-ttu-id="f794a-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f794a-130">*GUID*</span></span> | <span data-ttu-id="f794a-131">只读</span><span class="sxs-lookup"><span data-stu-id="f794a-131">Read-only</span></span><br><span data-ttu-id="f794a-132">必填</span><span class="sxs-lookup"><span data-stu-id="f794a-132">Required</span></span> | <span data-ttu-id="f794a-133">系统生成的招聘请求位置记录的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="f794a-133">System-generated unique identifier for the recruiting request location record.</span></span> |
| <span data-ttu-id="f794a-134">**说明**</span><span class="sxs-lookup"><span data-stu-id="f794a-134">**Description**</span></span><br><span data-ttu-id="f794a-135">mshr_description</span><span class="sxs-lookup"><span data-stu-id="f794a-135">mshr_description</span></span><br><span data-ttu-id="f794a-136">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-136">*String*</span></span> | <span data-ttu-id="f794a-137">读/写</span><span class="sxs-lookup"><span data-stu-id="f794a-137">Read/write</span></span><br><span data-ttu-id="f794a-138">必填</span><span class="sxs-lookup"><span data-stu-id="f794a-138">Required</span></span> | <span data-ttu-id="f794a-139">位置的描述。</span><span class="sxs-lookup"><span data-stu-id="f794a-139">Description of the location.</span></span> |
| <span data-ttu-id="f794a-140">**国家/地区 ID**</span><span class="sxs-lookup"><span data-stu-id="f794a-140">**Country/Region ID**</span></span><br><span data-ttu-id="f794a-141">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="f794a-141">mshr_countryregionid</span></span><br><span data-ttu-id="f794a-142">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-142">*String*</span></span> | <span data-ttu-id="f794a-143">只读</span><span class="sxs-lookup"><span data-stu-id="f794a-143">Read-only</span></span><br><span data-ttu-id="f794a-144">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-144">Optional</span></span> | <span data-ttu-id="f794a-145">指定应聘者的国籍国家或地区。</span><span class="sxs-lookup"><span data-stu-id="f794a-145">Specifies the country or region where the candidate has citizenship.</span></span> |
| <span data-ttu-id="f794a-146">**国家/地区 ID 值**</span><span class="sxs-lookup"><span data-stu-id="f794a-146">**Country/Region ID Value**</span></span><br><span data-ttu-id="f794a-147">_mshr_fk_countriregion_id_value</span><span class="sxs-lookup"><span data-stu-id="f794a-147">_mshr_fk_countriregion_id_value</span></span><br><span data-ttu-id="f794a-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f794a-148">*GUID*</span></span> | <span data-ttu-id="f794a-149">只读</span><span class="sxs-lookup"><span data-stu-id="f794a-149">Read-only</span></span><br><span data-ttu-id="f794a-150">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-150">Optional</span></span><br><span data-ttu-id="f794a-151">外键：mshr_logisticsaddresscountryregionentity 的 mshr_logisticaddresscountryregionentityid</span><span class="sxs-lookup"><span data-stu-id="f794a-151">Foreign key: mshr_logisticaddresscountryregionentityid of mshr_logisticsaddresscountryregionentity</span></span> | <span data-ttu-id="f794a-152">系统生成的地址中国家/地区的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="f794a-152">System-generated unique identifier of the country/region of the address.</span></span> |
| <span data-ttu-id="f794a-153">**邮政编码**</span><span class="sxs-lookup"><span data-stu-id="f794a-153">**ZipCode**</span></span><br><span data-ttu-id="f794a-154">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="f794a-154">mshr_zipcode</span></span><br><span data-ttu-id="f794a-155">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-155">*String*</span></span> | <span data-ttu-id="f794a-156">只读</span><span class="sxs-lookup"><span data-stu-id="f794a-156">Read-only</span></span><br><span data-ttu-id="f794a-157">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-157">Optional</span></span> | <span data-ttu-id="f794a-158">邮政编码。</span><span class="sxs-lookup"><span data-stu-id="f794a-158">Zip/postal code.</span></span> |
| <span data-ttu-id="f794a-159">**街道**</span><span class="sxs-lookup"><span data-stu-id="f794a-159">**Street**</span></span><br><span data-ttu-id="f794a-160">mshr_street</span><span class="sxs-lookup"><span data-stu-id="f794a-160">mshr_street</span></span><br><span data-ttu-id="f794a-161">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-161">*String*</span></span> | <span data-ttu-id="f794a-162">只读</span><span class="sxs-lookup"><span data-stu-id="f794a-162">Read-only</span></span><br><span data-ttu-id="f794a-163">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-163">Optional</span></span> | <span data-ttu-id="f794a-164">街道地址。</span><span class="sxs-lookup"><span data-stu-id="f794a-164">Street address.</span></span> |
| <span data-ttu-id="f794a-165">**市**</span><span class="sxs-lookup"><span data-stu-id="f794a-165">**City**</span></span><br><span data-ttu-id="f794a-166">mshr_city</span><span class="sxs-lookup"><span data-stu-id="f794a-166">mshr_city</span></span><br><span data-ttu-id="f794a-167">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-167">*String*</span></span> | <span data-ttu-id="f794a-168">只读</span><span class="sxs-lookup"><span data-stu-id="f794a-168">Read-only</span></span><br><span data-ttu-id="f794a-169">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-169">Optional</span></span> | <span data-ttu-id="f794a-170">城市。</span><span class="sxs-lookup"><span data-stu-id="f794a-170">City.</span></span> |
| <span data-ttu-id="f794a-171">**州或省/自治区/直辖市**</span><span class="sxs-lookup"><span data-stu-id="f794a-171">**State**</span></span><br><span data-ttu-id="f794a-172">mshr_state</span><span class="sxs-lookup"><span data-stu-id="f794a-172">mshr_state</span></span><br><span data-ttu-id="f794a-173">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-173">*String*</span></span> | <span data-ttu-id="f794a-174">只读</span><span class="sxs-lookup"><span data-stu-id="f794a-174">Read-only</span></span><br><span data-ttu-id="f794a-175">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-175">Optional</span></span> | <span data-ttu-id="f794a-176">州或省/自治区/直辖市。</span><span class="sxs-lookup"><span data-stu-id="f794a-176">State or province.</span></span> |
| <span data-ttu-id="f794a-177">**县**</span><span class="sxs-lookup"><span data-stu-id="f794a-177">**County**</span></span><br><span data-ttu-id="f794a-178">mshr_county</span><span class="sxs-lookup"><span data-stu-id="f794a-178">mshr_county</span></span><br><span data-ttu-id="f794a-179">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-179">*String*</span></span> | <span data-ttu-id="f794a-180">只读</span><span class="sxs-lookup"><span data-stu-id="f794a-180">Read-only</span></span><br><span data-ttu-id="f794a-181">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-181">Optional</span></span> | <span data-ttu-id="f794a-182">县。</span><span class="sxs-lookup"><span data-stu-id="f794a-182">County.</span></span> |
| <span data-ttu-id="f794a-183">**电话**</span><span class="sxs-lookup"><span data-stu-id="f794a-183">**Telephone**</span></span><br><span data-ttu-id="f794a-184">mshr_telephone</span><span class="sxs-lookup"><span data-stu-id="f794a-184">mshr_telephone</span></span><br><span data-ttu-id="f794a-185">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-185">*String*</span></span> | <span data-ttu-id="f794a-186">读/写</span><span class="sxs-lookup"><span data-stu-id="f794a-186">Read/write</span></span><br><span data-ttu-id="f794a-187">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-187">Optional</span></span> | <span data-ttu-id="f794a-188">位置的电话号码。</span><span class="sxs-lookup"><span data-stu-id="f794a-188">Telephone number for the location.</span></span> |
| <span data-ttu-id="f794a-189">**电子邮件**</span><span class="sxs-lookup"><span data-stu-id="f794a-189">**Email**</span></span><br><span data-ttu-id="f794a-190">mshr_email</span><span class="sxs-lookup"><span data-stu-id="f794a-190">mshr_email</span></span><br><span data-ttu-id="f794a-191">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-191">*String*</span></span> | <span data-ttu-id="f794a-192">读/写</span><span class="sxs-lookup"><span data-stu-id="f794a-192">Read/write</span></span><br><span data-ttu-id="f794a-193">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-193">Optional</span></span> | <span data-ttu-id="f794a-194">电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="f794a-194">Email address.</span></span> |
| <span data-ttu-id="f794a-195">**InternetAddress**</span><span class="sxs-lookup"><span data-stu-id="f794a-195">**InternetAddress**</span></span><br><span data-ttu-id="f794a-196">mshr_internetaddress</span><span class="sxs-lookup"><span data-stu-id="f794a-196">mshr_internetaddress</span></span><br><span data-ttu-id="f794a-197">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-197">*String*</span></span> | <span data-ttu-id="f794a-198">读/写</span><span class="sxs-lookup"><span data-stu-id="f794a-198">Read/write</span></span><br><span data-ttu-id="f794a-199">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-199">Optional</span></span> | <span data-ttu-id="f794a-200">位置网站的 URL。</span><span class="sxs-lookup"><span data-stu-id="f794a-200">URL for the location website.</span></span> |
| <span data-ttu-id="f794a-201">**数据区域 ID**</span><span class="sxs-lookup"><span data-stu-id="f794a-201">**Data Area ID**</span></span><br><span data-ttu-id="f794a-202">mshr_dataareaid</span><span class="sxs-lookup"><span data-stu-id="f794a-202">mshr_dataareaid</span></span><br><span data-ttu-id="f794a-203">*字符串*</span><span class="sxs-lookup"><span data-stu-id="f794a-203">*String*</span></span> | <span data-ttu-id="f794a-204">读/写</span><span class="sxs-lookup"><span data-stu-id="f794a-204">Read/write</span></span><br><span data-ttu-id="f794a-205">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-205">Optional</span></span> | <span data-ttu-id="f794a-206">指定法人（公司）。</span><span class="sxs-lookup"><span data-stu-id="f794a-206">Specifies the legal entity (company).</span></span> |
| <span data-ttu-id="f794a-207">**数据区域 ID 值**</span><span class="sxs-lookup"><span data-stu-id="f794a-207">**Data Area ID Value**</span></span><br><span data-ttu-id="f794a-208">_mshr_dataareaid_id_value</span><span class="sxs-lookup"><span data-stu-id="f794a-208">_mshr_dataareaid_id_value</span></span><br><span data-ttu-id="f794a-209">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f794a-209">*GUID*</span></span> | <span data-ttu-id="f794a-210">只读</span><span class="sxs-lookup"><span data-stu-id="f794a-210">Read-only</span></span><br><span data-ttu-id="f794a-211">可选</span><span class="sxs-lookup"><span data-stu-id="f794a-211">Optional</span></span><br><span data-ttu-id="f794a-212">外键：cdm_company 实体的 cdm_companyid</span><span class="sxs-lookup"><span data-stu-id="f794a-212">Foreign key: cdm_companyid of cdm_company entity</span></span> | <span data-ttu-id="f794a-213">系统生成的标识法人（公司）的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="f794a-213">System-generated GUID value identifying the legal entity (company).</span></span> |

## <a name="see-also"></a><span data-ttu-id="f794a-214">请参阅</span><span class="sxs-lookup"><span data-stu-id="f794a-214">See also</span></span>

[<span data-ttu-id="f794a-215">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="f794a-215">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="f794a-216">招聘请求的查询示例</span><span class="sxs-lookup"><span data-stu-id="f794a-216">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]