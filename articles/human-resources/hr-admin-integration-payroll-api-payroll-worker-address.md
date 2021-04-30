---
title: 工资单工作人员地址
description: 本主题提供 Dynamics 365 Human Resources 中工资单工作人员地址实体的详细信息和示例查询。
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881934"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="0a433-103">工资单工作人员地址</span><span class="sxs-lookup"><span data-stu-id="0a433-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0a433-104">本主题提供 Dynamics 365 Human Resources 中工资单工作人员地址实体的详细信息和示例查询。</span><span class="sxs-lookup"><span data-stu-id="0a433-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="0a433-105">属性</span><span class="sxs-lookup"><span data-stu-id="0a433-105">Properties</span></span>

| <span data-ttu-id="0a433-106">属性</span><span class="sxs-lookup"><span data-stu-id="0a433-106">Property</span></span><br><span data-ttu-id="0a433-107">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="0a433-107">**Physical name**</span></span><br><span data-ttu-id="0a433-108">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="0a433-108">**_Type_**</span></span> | <span data-ttu-id="0a433-109">使用</span><span class="sxs-lookup"><span data-stu-id="0a433-109">Use</span></span> | <span data-ttu-id="0a433-110">说明</span><span class="sxs-lookup"><span data-stu-id="0a433-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0a433-111">**市**</span><span class="sxs-lookup"><span data-stu-id="0a433-111">**City**</span></span><br><span data-ttu-id="0a433-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="0a433-112">mshr_city</span></span><br><span data-ttu-id="0a433-113">*字符串*</span><span class="sxs-lookup"><span data-stu-id="0a433-113">*String*</span></span> | <span data-ttu-id="0a433-114">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-114">Read-only</span></span><br><span data-ttu-id="0a433-115">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-115">Required</span></span> | <span data-ttu-id="0a433-116">针对地址定义的城市。</span><span class="sxs-lookup"><span data-stu-id="0a433-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="0a433-117">**人员编号**</span><span class="sxs-lookup"><span data-stu-id="0a433-117">**Personnel number**</span></span><br><span data-ttu-id="0a433-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="0a433-118">mshr_personnelnumber</span></span><br><span data-ttu-id="0a433-119">*字符串*</span><span class="sxs-lookup"><span data-stu-id="0a433-119">*String*</span></span> | <span data-ttu-id="0a433-120">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-120">Read-only</span></span><br><span data-ttu-id="0a433-121">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-121">Required</span></span> | <span data-ttu-id="0a433-122">员工的唯一人员编号。</span><span class="sxs-lookup"><span data-stu-id="0a433-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="0a433-123">**国家/地区**</span><span class="sxs-lookup"><span data-stu-id="0a433-123">**Country region**</span></span><br><span data-ttu-id="0a433-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="0a433-124">mshr_countryregionid</span></span><br><span data-ttu-id="0a433-125">*字符串*</span><span class="sxs-lookup"><span data-stu-id="0a433-125">*String*</span></span> | <span data-ttu-id="0a433-126">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-126">Read-only</span></span><br><span data-ttu-id="0a433-127">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-127">Required</span></span> | <span data-ttu-id="0a433-128">针对地址定义的国家/地区</span><span class="sxs-lookup"><span data-stu-id="0a433-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="0a433-129">**生效日期**</span><span class="sxs-lookup"><span data-stu-id="0a433-129">**Valid from**</span></span><br><span data-ttu-id="0a433-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="0a433-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="0a433-131">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="0a433-131">*Date Time Offset*</span></span> | <span data-ttu-id="0a433-132">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-132">Read-only</span></span> <br><span data-ttu-id="0a433-133">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-133">Required</span></span> | <span data-ttu-id="0a433-134">地址有效的开始日期。</span><span class="sxs-lookup"><span data-stu-id="0a433-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="0a433-135">**工作地址**</span><span class="sxs-lookup"><span data-stu-id="0a433-135">**Worked in address**</span></span><br><span data-ttu-id="0a433-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="0a433-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="0a433-137">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-137">Read-only</span></span><br><span data-ttu-id="0a433-138">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-138">Required</span></span> | <span data-ttu-id="0a433-139">表示地址是否是员工的工作地址。</span><span class="sxs-lookup"><span data-stu-id="0a433-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="0a433-140">**县**</span><span class="sxs-lookup"><span data-stu-id="0a433-140">**County**</span></span><br><span data-ttu-id="0a433-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="0a433-141">mshr_county</span></span><br><span data-ttu-id="0a433-142">*字符串*</span><span class="sxs-lookup"><span data-stu-id="0a433-142">*String*</span></span> | <span data-ttu-id="0a433-143">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-143">Read-only</span></span><br><span data-ttu-id="0a433-144">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-144">Required</span></span> | <span data-ttu-id="0a433-145">针对地址定义的县。</span><span class="sxs-lookup"><span data-stu-id="0a433-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="0a433-146">**工资单工作人员地址 ID**</span><span class="sxs-lookup"><span data-stu-id="0a433-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="0a433-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="0a433-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="0a433-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="0a433-148">*GUID*</span></span> | <span data-ttu-id="0a433-149">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-149">Required</span></span><br><span data-ttu-id="0a433-150">系统生成的</span><span class="sxs-lookup"><span data-stu-id="0a433-150">System generated</span></span> | <span data-ttu-id="0a433-151">系统生成的用于唯一标识地址的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="0a433-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="0a433-152">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="0a433-152">**Primary field**</span></span><br><span data-ttu-id="0a433-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="0a433-153">mshr_primaryfield</span></span><br><span data-ttu-id="0a433-154">*字符串*</span><span class="sxs-lookup"><span data-stu-id="0a433-154">*String*</span></span> | <span data-ttu-id="0a433-155">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-155">Read-only</span></span><br><span data-ttu-id="0a433-156">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-156">Required</span></span> |  |
| <span data-ttu-id="0a433-157">**街道**</span><span class="sxs-lookup"><span data-stu-id="0a433-157">**Street**</span></span><br><span data-ttu-id="0a433-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="0a433-158">mshr_street</span></span><br><span data-ttu-id="0a433-159">*字符串*</span><span class="sxs-lookup"><span data-stu-id="0a433-159">*String*</span></span> | <span data-ttu-id="0a433-160">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-160">Read-only</span></span><br><span data-ttu-id="0a433-161">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-161">Required</span></span> | <span data-ttu-id="0a433-162">针对地址定义的街道。</span><span class="sxs-lookup"><span data-stu-id="0a433-162">The street defined for the address.</span></span> |
| <span data-ttu-id="0a433-163">**失效日期**</span><span class="sxs-lookup"><span data-stu-id="0a433-163">**Valid to**</span></span><br><span data-ttu-id="0a433-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="0a433-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="0a433-165">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="0a433-165">*Date Time Offset*</span></span> | <span data-ttu-id="0a433-166">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-166">Read-only</span></span> <br><span data-ttu-id="0a433-167">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-167">Required</span></span> | <span data-ttu-id="0a433-168">地址有效的结束日期。</span><span class="sxs-lookup"><span data-stu-id="0a433-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="0a433-169">**位置 ID**</span><span class="sxs-lookup"><span data-stu-id="0a433-169">**Location ID**</span></span><br><span data-ttu-id="0a433-170">mshr_locationidbr>*String*</span><span class="sxs-lookup"><span data-stu-id="0a433-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="0a433-171">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-171">Read-only</span></span> <br><span data-ttu-id="0a433-172">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-172">Required</span></span> | <span data-ttu-id="0a433-173">地址的 ID。</span><span class="sxs-lookup"><span data-stu-id="0a433-173">The ID for the address.</span></span>  |
| <span data-ttu-id="0a433-174">**邮政编码**</span><span class="sxs-lookup"><span data-stu-id="0a433-174">**Postal code**</span></span><br><span data-ttu-id="0a433-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="0a433-175">mshr_zipcode</span></span><br><span data-ttu-id="0a433-176">*字符串*</span><span class="sxs-lookup"><span data-stu-id="0a433-176">*String*</span></span> | <span data-ttu-id="0a433-177">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-177">Read-only</span></span> <br><span data-ttu-id="0a433-178">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-178">Required</span></span> |<span data-ttu-id="0a433-179">针对员工定义的标识号。</span><span class="sxs-lookup"><span data-stu-id="0a433-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="0a433-180">**家庭地址**</span><span class="sxs-lookup"><span data-stu-id="0a433-180">**Lived in address**</span></span><br><span data-ttu-id="0a433-181">mshr_islivedinaddressbr>*String*</span><span class="sxs-lookup"><span data-stu-id="0a433-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="0a433-182">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-182">Read-only</span></span><br><span data-ttu-id="0a433-183">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-183">Required</span></span> | <span data-ttu-id="0a433-184">表示地址是否是员工的家庭地址。</span><span class="sxs-lookup"><span data-stu-id="0a433-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="0a433-185">**州或省/自治区/直辖市**</span><span class="sxs-lookup"><span data-stu-id="0a433-185">**State**</span></span><br><span data-ttu-id="0a433-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="0a433-186">mshr_state</span></span><br><span data-ttu-id="0a433-187">*字符串*</span><span class="sxs-lookup"><span data-stu-id="0a433-187">*String*</span></span> | <span data-ttu-id="0a433-188">只读</span><span class="sxs-lookup"><span data-stu-id="0a433-188">Read-only</span></span><br><span data-ttu-id="0a433-189">必填</span><span class="sxs-lookup"><span data-stu-id="0a433-189">Required</span></span> | <span data-ttu-id="0a433-190">针对地址定义的省/自治区/直辖市。</span><span class="sxs-lookup"><span data-stu-id="0a433-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="0a433-191">示例查询</span><span class="sxs-lookup"><span data-stu-id="0a433-191">Example query</span></span>

<span data-ttu-id="0a433-192">**申请**</span><span class="sxs-lookup"><span data-stu-id="0a433-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="0a433-193">**响应**</span><span class="sxs-lookup"><span data-stu-id="0a433-193">**Response**</span></span>

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
