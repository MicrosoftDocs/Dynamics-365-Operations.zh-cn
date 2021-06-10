---
title: 工资单工作人员地址
description: 本主题提供 Dynamics 365 Human Resources 中工资单工作人员地址实体的详细信息和示例查询。
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3407128b0172f0e253d51bcfa23a894f981e21e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052281"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="46320-103">工资单工作人员地址</span><span class="sxs-lookup"><span data-stu-id="46320-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="46320-104">本主题提供 Dynamics 365 Human Resources 中工资单工作人员地址实体的详细信息和示例查询。</span><span class="sxs-lookup"><span data-stu-id="46320-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="46320-105">属性</span><span class="sxs-lookup"><span data-stu-id="46320-105">Properties</span></span>

| <span data-ttu-id="46320-106">属性</span><span class="sxs-lookup"><span data-stu-id="46320-106">Property</span></span><br><span data-ttu-id="46320-107">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="46320-107">**Physical name**</span></span><br><span data-ttu-id="46320-108">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="46320-108">**_Type_**</span></span> | <span data-ttu-id="46320-109">使用</span><span class="sxs-lookup"><span data-stu-id="46320-109">Use</span></span> | <span data-ttu-id="46320-110">说明</span><span class="sxs-lookup"><span data-stu-id="46320-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="46320-111">**市**</span><span class="sxs-lookup"><span data-stu-id="46320-111">**City**</span></span><br><span data-ttu-id="46320-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="46320-112">mshr_city</span></span><br><span data-ttu-id="46320-113">*字符串*</span><span class="sxs-lookup"><span data-stu-id="46320-113">*String*</span></span> | <span data-ttu-id="46320-114">只读</span><span class="sxs-lookup"><span data-stu-id="46320-114">Read-only</span></span><br><span data-ttu-id="46320-115">必填</span><span class="sxs-lookup"><span data-stu-id="46320-115">Required</span></span> | <span data-ttu-id="46320-116">针对地址定义的城市。</span><span class="sxs-lookup"><span data-stu-id="46320-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="46320-117">**人员编号**</span><span class="sxs-lookup"><span data-stu-id="46320-117">**Personnel number**</span></span><br><span data-ttu-id="46320-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="46320-118">mshr_personnelnumber</span></span><br><span data-ttu-id="46320-119">*字符串*</span><span class="sxs-lookup"><span data-stu-id="46320-119">*String*</span></span> | <span data-ttu-id="46320-120">只读</span><span class="sxs-lookup"><span data-stu-id="46320-120">Read-only</span></span><br><span data-ttu-id="46320-121">必填</span><span class="sxs-lookup"><span data-stu-id="46320-121">Required</span></span> | <span data-ttu-id="46320-122">员工的唯一人员编号。</span><span class="sxs-lookup"><span data-stu-id="46320-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="46320-123">**国家/地区**</span><span class="sxs-lookup"><span data-stu-id="46320-123">**Country region**</span></span><br><span data-ttu-id="46320-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="46320-124">mshr_countryregionid</span></span><br><span data-ttu-id="46320-125">*字符串*</span><span class="sxs-lookup"><span data-stu-id="46320-125">*String*</span></span> | <span data-ttu-id="46320-126">只读</span><span class="sxs-lookup"><span data-stu-id="46320-126">Read-only</span></span><br><span data-ttu-id="46320-127">必填</span><span class="sxs-lookup"><span data-stu-id="46320-127">Required</span></span> | <span data-ttu-id="46320-128">针对地址定义的国家/地区</span><span class="sxs-lookup"><span data-stu-id="46320-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="46320-129">**生效日期**</span><span class="sxs-lookup"><span data-stu-id="46320-129">**Valid from**</span></span><br><span data-ttu-id="46320-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="46320-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="46320-131">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="46320-131">*Date Time Offset*</span></span> | <span data-ttu-id="46320-132">只读</span><span class="sxs-lookup"><span data-stu-id="46320-132">Read-only</span></span> <br><span data-ttu-id="46320-133">必填</span><span class="sxs-lookup"><span data-stu-id="46320-133">Required</span></span> | <span data-ttu-id="46320-134">地址有效的开始日期。</span><span class="sxs-lookup"><span data-stu-id="46320-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="46320-135">**工作地址**</span><span class="sxs-lookup"><span data-stu-id="46320-135">**Worked in address**</span></span><br><span data-ttu-id="46320-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="46320-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="46320-137">只读</span><span class="sxs-lookup"><span data-stu-id="46320-137">Read-only</span></span><br><span data-ttu-id="46320-138">必填</span><span class="sxs-lookup"><span data-stu-id="46320-138">Required</span></span> | <span data-ttu-id="46320-139">表示地址是否是员工的工作地址。</span><span class="sxs-lookup"><span data-stu-id="46320-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="46320-140">**县**</span><span class="sxs-lookup"><span data-stu-id="46320-140">**County**</span></span><br><span data-ttu-id="46320-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="46320-141">mshr_county</span></span><br><span data-ttu-id="46320-142">*字符串*</span><span class="sxs-lookup"><span data-stu-id="46320-142">*String*</span></span> | <span data-ttu-id="46320-143">只读</span><span class="sxs-lookup"><span data-stu-id="46320-143">Read-only</span></span><br><span data-ttu-id="46320-144">必填</span><span class="sxs-lookup"><span data-stu-id="46320-144">Required</span></span> | <span data-ttu-id="46320-145">针对地址定义的县。</span><span class="sxs-lookup"><span data-stu-id="46320-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="46320-146">**工资单工作人员地址 ID**</span><span class="sxs-lookup"><span data-stu-id="46320-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="46320-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="46320-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="46320-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="46320-148">*GUID*</span></span> | <span data-ttu-id="46320-149">必填</span><span class="sxs-lookup"><span data-stu-id="46320-149">Required</span></span><br><span data-ttu-id="46320-150">系统生成的</span><span class="sxs-lookup"><span data-stu-id="46320-150">System generated</span></span> | <span data-ttu-id="46320-151">系统生成的用于唯一标识地址的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="46320-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="46320-152">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="46320-152">**Primary field**</span></span><br><span data-ttu-id="46320-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="46320-153">mshr_primaryfield</span></span><br><span data-ttu-id="46320-154">*字符串*</span><span class="sxs-lookup"><span data-stu-id="46320-154">*String*</span></span> | <span data-ttu-id="46320-155">只读</span><span class="sxs-lookup"><span data-stu-id="46320-155">Read-only</span></span><br><span data-ttu-id="46320-156">必填</span><span class="sxs-lookup"><span data-stu-id="46320-156">Required</span></span> |  |
| <span data-ttu-id="46320-157">**街道**</span><span class="sxs-lookup"><span data-stu-id="46320-157">**Street**</span></span><br><span data-ttu-id="46320-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="46320-158">mshr_street</span></span><br><span data-ttu-id="46320-159">*字符串*</span><span class="sxs-lookup"><span data-stu-id="46320-159">*String*</span></span> | <span data-ttu-id="46320-160">只读</span><span class="sxs-lookup"><span data-stu-id="46320-160">Read-only</span></span><br><span data-ttu-id="46320-161">必填</span><span class="sxs-lookup"><span data-stu-id="46320-161">Required</span></span> | <span data-ttu-id="46320-162">针对地址定义的街道。</span><span class="sxs-lookup"><span data-stu-id="46320-162">The street defined for the address.</span></span> |
| <span data-ttu-id="46320-163">**失效日期**</span><span class="sxs-lookup"><span data-stu-id="46320-163">**Valid to**</span></span><br><span data-ttu-id="46320-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="46320-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="46320-165">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="46320-165">*Date Time Offset*</span></span> | <span data-ttu-id="46320-166">只读</span><span class="sxs-lookup"><span data-stu-id="46320-166">Read-only</span></span> <br><span data-ttu-id="46320-167">必填</span><span class="sxs-lookup"><span data-stu-id="46320-167">Required</span></span> | <span data-ttu-id="46320-168">地址有效的结束日期。</span><span class="sxs-lookup"><span data-stu-id="46320-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="46320-169">**位置 ID**</span><span class="sxs-lookup"><span data-stu-id="46320-169">**Location ID**</span></span><br><span data-ttu-id="46320-170">mshr_locationidbr>*String*</span><span class="sxs-lookup"><span data-stu-id="46320-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="46320-171">只读</span><span class="sxs-lookup"><span data-stu-id="46320-171">Read-only</span></span> <br><span data-ttu-id="46320-172">必填</span><span class="sxs-lookup"><span data-stu-id="46320-172">Required</span></span> | <span data-ttu-id="46320-173">地址的 ID。</span><span class="sxs-lookup"><span data-stu-id="46320-173">The ID for the address.</span></span>  |
| <span data-ttu-id="46320-174">**邮政编码**</span><span class="sxs-lookup"><span data-stu-id="46320-174">**Postal code**</span></span><br><span data-ttu-id="46320-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="46320-175">mshr_zipcode</span></span><br><span data-ttu-id="46320-176">*字符串*</span><span class="sxs-lookup"><span data-stu-id="46320-176">*String*</span></span> | <span data-ttu-id="46320-177">只读</span><span class="sxs-lookup"><span data-stu-id="46320-177">Read-only</span></span> <br><span data-ttu-id="46320-178">必填</span><span class="sxs-lookup"><span data-stu-id="46320-178">Required</span></span> |<span data-ttu-id="46320-179">针对员工定义的标识号。</span><span class="sxs-lookup"><span data-stu-id="46320-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="46320-180">**家庭地址**</span><span class="sxs-lookup"><span data-stu-id="46320-180">**Lived in address**</span></span><br><span data-ttu-id="46320-181">mshr_islivedinaddressbr>*String*</span><span class="sxs-lookup"><span data-stu-id="46320-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="46320-182">只读</span><span class="sxs-lookup"><span data-stu-id="46320-182">Read-only</span></span><br><span data-ttu-id="46320-183">必填</span><span class="sxs-lookup"><span data-stu-id="46320-183">Required</span></span> | <span data-ttu-id="46320-184">表示地址是否是员工的家庭地址。</span><span class="sxs-lookup"><span data-stu-id="46320-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="46320-185">**州或省/自治区/直辖市**</span><span class="sxs-lookup"><span data-stu-id="46320-185">**State**</span></span><br><span data-ttu-id="46320-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="46320-186">mshr_state</span></span><br><span data-ttu-id="46320-187">*字符串*</span><span class="sxs-lookup"><span data-stu-id="46320-187">*String*</span></span> | <span data-ttu-id="46320-188">只读</span><span class="sxs-lookup"><span data-stu-id="46320-188">Read-only</span></span><br><span data-ttu-id="46320-189">必填</span><span class="sxs-lookup"><span data-stu-id="46320-189">Required</span></span> | <span data-ttu-id="46320-190">针对地址定义的省/自治区/直辖市。</span><span class="sxs-lookup"><span data-stu-id="46320-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="46320-191">示例查询</span><span class="sxs-lookup"><span data-stu-id="46320-191">Example query</span></span>

<span data-ttu-id="46320-192">**申请**</span><span class="sxs-lookup"><span data-stu-id="46320-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="46320-193">**响应**</span><span class="sxs-lookup"><span data-stu-id="46320-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
