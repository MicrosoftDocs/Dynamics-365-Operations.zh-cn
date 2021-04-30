---
title: 工资单员工
description: 本主题提供 Dynamics 365 Human Resources 中工资单员工实体的详细信息和示例查询。
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
ms.openlocfilehash: d3977b758f65875a36749a49459c2a81459a7b69
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881938"
---
# <a name="payroll-employee"></a><span data-ttu-id="a9723-103">工资单员工</span><span class="sxs-lookup"><span data-stu-id="a9723-103">Payroll employee</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a9723-104">本主题提供 Dynamics 365 Human Resources 中工资单员工实体的详细信息和示例查询。</span><span class="sxs-lookup"><span data-stu-id="a9723-104">This topic provides details and an example query for the Payroll employee entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="a9723-105">属性</span><span class="sxs-lookup"><span data-stu-id="a9723-105">Properties</span></span>

| <span data-ttu-id="a9723-106">属性</span><span class="sxs-lookup"><span data-stu-id="a9723-106">Property</span></span><br><span data-ttu-id="a9723-107">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="a9723-107">**Physical name**</span></span><br><span data-ttu-id="a9723-108">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="a9723-108">**_Type_**</span></span> | <span data-ttu-id="a9723-109">使用</span><span class="sxs-lookup"><span data-stu-id="a9723-109">Use</span></span> | <span data-ttu-id="a9723-110">说明</span><span class="sxs-lookup"><span data-stu-id="a9723-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a9723-111">**人员编号**</span><span class="sxs-lookup"><span data-stu-id="a9723-111">**Personnel number**</span></span><br><span data-ttu-id="a9723-112">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="a9723-112">mshr_personnelnumber</span></span><br><span data-ttu-id="a9723-113">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a9723-113">*String*</span></span> | <span data-ttu-id="a9723-114">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-114">Read-only</span></span><br><span data-ttu-id="a9723-115">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-115">Required</span></span> | <span data-ttu-id="a9723-116">员工的唯一人员编号。</span><span class="sxs-lookup"><span data-stu-id="a9723-116">The employee's unique personnel number.</span></span> |
| <span data-ttu-id="a9723-117">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="a9723-117">**Primary field**</span></span><br><span data-ttu-id="a9723-118">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="a9723-118">mshr_primaryfield</span></span><br><span data-ttu-id="a9723-119">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a9723-119">*String*</span></span> | <span data-ttu-id="a9723-120">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-120">Required</span></span><br><span data-ttu-id="a9723-121">系统生成的</span><span class="sxs-lookup"><span data-stu-id="a9723-121">System generated</span></span> |  |
| <span data-ttu-id="a9723-122">**姓**</span><span class="sxs-lookup"><span data-stu-id="a9723-122">**Last name**</span></span><br><span data-ttu-id="a9723-123">mshr_lastname</span><span class="sxs-lookup"><span data-stu-id="a9723-123">mshr_lastname</span></span><br><span data-ttu-id="a9723-124">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a9723-124">*String*</span></span> | <span data-ttu-id="a9723-125">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-125">Read only</span></span><br><span data-ttu-id="a9723-126">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-126">Required</span></span> | <span data-ttu-id="a9723-127">员工姓氏。</span><span class="sxs-lookup"><span data-stu-id="a9723-127">Employee last name.</span></span> |
| <span data-ttu-id="a9723-128">**法人 ID**</span><span class="sxs-lookup"><span data-stu-id="a9723-128">**Legal entity ID**</span></span><br><span data-ttu-id="a9723-129">mshr_legalentityID</span><span class="sxs-lookup"><span data-stu-id="a9723-129">mshr_legalentityID</span></span><br><span data-ttu-id="a9723-130">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a9723-130">*String*</span></span> | <span data-ttu-id="a9723-131">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-131">Read-only</span></span><br><span data-ttu-id="a9723-132">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-132">Required</span></span> | <span data-ttu-id="a9723-133">指定法人（公司）。</span><span class="sxs-lookup"><span data-stu-id="a9723-133">Specifies the legal entity (company).</span></span> |
| <span data-ttu-id="a9723-134">**生效日期**</span><span class="sxs-lookup"><span data-stu-id="a9723-134">**Valid from**</span></span><br><span data-ttu-id="a9723-135">mshr_namevalidfrom</span><span class="sxs-lookup"><span data-stu-id="a9723-135">mshr_namevalidfrom</span></span><br><span data-ttu-id="a9723-136">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="a9723-136">*Date Time Offset*</span></span> | <span data-ttu-id="a9723-137">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-137">Read-only</span></span> <br><span data-ttu-id="a9723-138">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-138">Required</span></span> | <span data-ttu-id="a9723-139">员工信息有效的开始日期。</span><span class="sxs-lookup"><span data-stu-id="a9723-139">Date the employee information is valid from.</span></span>  |
| <span data-ttu-id="a9723-140">**性**</span><span class="sxs-lookup"><span data-stu-id="a9723-140">**Gender**</span></span><br><span data-ttu-id="a9723-141">mshr_gender</span><span class="sxs-lookup"><span data-stu-id="a9723-141">mshr_gender</span></span><br><span data-ttu-id="a9723-142">*Int32*</span><span class="sxs-lookup"><span data-stu-id="a9723-142">*Int32*</span></span> | <span data-ttu-id="a9723-143">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-143">Read-only</span></span><br><span data-ttu-id="a9723-144">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-144">Required</span></span> | <span data-ttu-id="a9723-145">员工的性别。</span><span class="sxs-lookup"><span data-stu-id="a9723-145">The employee's gender.</span></span> |
| <span data-ttu-id="a9723-146">**工资单员工实体 ID**</span><span class="sxs-lookup"><span data-stu-id="a9723-146">**Payroll employee entity ID**</span></span><br><span data-ttu-id="a9723-147">mshr_payrollemployeeentityid</span><span class="sxs-lookup"><span data-stu-id="a9723-147">mshr_payrollemployeeentityid</span></span><br><span data-ttu-id="a9723-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a9723-148">*GUID*</span></span> | <span data-ttu-id="a9723-149">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-149">Required</span></span><br><span data-ttu-id="a9723-150">系统生成的</span><span class="sxs-lookup"><span data-stu-id="a9723-150">System generated</span></span> | <span data-ttu-id="a9723-151">系统生成的用于唯一标识员工的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="a9723-151">A system-generated GUID value to uniquely identify the employee.</span></span> |
| <span data-ttu-id="a9723-152">**雇用开始日期**</span><span class="sxs-lookup"><span data-stu-id="a9723-152">**Employment start date**</span></span><br><span data-ttu-id="a9723-153">mshr_employmentstartdate</span><span class="sxs-lookup"><span data-stu-id="a9723-153">mshr_employmentstartdate</span></span><br><span data-ttu-id="a9723-154">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="a9723-154">*Date time offset*</span></span> | <span data-ttu-id="a9723-155">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-155">Read-only</span></span><br><span data-ttu-id="a9723-156">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-156">Required</span></span> | <span data-ttu-id="a9723-157">员工受雇用的开始日期。</span><span class="sxs-lookup"><span data-stu-id="a9723-157">The start date of the employee's employment.</span></span> |
| <span data-ttu-id="a9723-158">**标识类型 ID**</span><span class="sxs-lookup"><span data-stu-id="a9723-158">**Identification type ID**</span></span><br><span data-ttu-id="a9723-159">mshr_identificationtypeid</span><span class="sxs-lookup"><span data-stu-id="a9723-159">mshr_identificationtypeid</span></span><br><span data-ttu-id="a9723-160">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a9723-160">*String*</span></span> |<span data-ttu-id="a9723-161">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-161">Read-only</span></span><br><span data-ttu-id="a9723-162">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-162">Required</span></span> | <span data-ttu-id="a9723-163">针对员工定义的标识类型。</span><span class="sxs-lookup"><span data-stu-id="a9723-163">The identification type defined for the employee.</span></span> |
| <span data-ttu-id="a9723-164">**雇佣结束日期**</span><span class="sxs-lookup"><span data-stu-id="a9723-164">**Employment end date**</span></span><br><span data-ttu-id="a9723-165">mshr_employmentenddate</span><span class="sxs-lookup"><span data-stu-id="a9723-165">mshr_employmentenddate</span></span><br><span data-ttu-id="a9723-166">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="a9723-166">*Date time offset*</span></span> | <span data-ttu-id="a9723-167">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-167">Read-only</span></span><br><span data-ttu-id="a9723-168">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-168">Required</span></span> |<span data-ttu-id="a9723-169">员工受雇用的结束日期。</span><span class="sxs-lookup"><span data-stu-id="a9723-169">The end of the employee's employment.</span></span>  |
| <span data-ttu-id="a9723-170">**数据区域 ID**</span><span class="sxs-lookup"><span data-stu-id="a9723-170">**Data area ID**</span></span><br><span data-ttu-id="a9723-171">mshr_dataareaid_id</span><span class="sxs-lookup"><span data-stu-id="a9723-171">mshr_dataareaid_id</span></span><br><span data-ttu-id="a9723-172">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a9723-172">*GUID*</span></span> | <span data-ttu-id="a9723-173">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-173">Required</span></span> <br><span data-ttu-id="a9723-174">系统生成的</span><span class="sxs-lookup"><span data-stu-id="a9723-174">System generated</span></span> | <span data-ttu-id="a9723-175">系统生成的标识法人（公司）的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="a9723-175">System-generated GUID value identifying the legal entity (company).</span></span> |
| <span data-ttu-id="a9723-176">**失效日期**</span><span class="sxs-lookup"><span data-stu-id="a9723-176">**Valid to**</span></span><br><span data-ttu-id="a9723-177">mshr_namevalidto</span><span class="sxs-lookup"><span data-stu-id="a9723-177">mshr_namevalidto</span></span><br><span data-ttu-id="a9723-178">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="a9723-178">*Date Time Offset*</span></span> |  <span data-ttu-id="a9723-179">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-179">Read-only</span></span><br><span data-ttu-id="a9723-180">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-180">Required</span></span> | <span data-ttu-id="a9723-181">员工信息有效的结束日期。</span><span class="sxs-lookup"><span data-stu-id="a9723-181">Date the employee information is valid to.</span></span> |
| <span data-ttu-id="a9723-182">**出生日期**</span><span class="sxs-lookup"><span data-stu-id="a9723-182">**Birth date**</span></span><br><span data-ttu-id="a9723-183">mshr_birthdate</span><span class="sxs-lookup"><span data-stu-id="a9723-183">mshr_birthdate</span></span><br><span data-ttu-id="a9723-184">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="a9723-184">*Date Time Offset*</span></span> | <span data-ttu-id="a9723-185">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-185">Read-only</span></span> <br><span data-ttu-id="a9723-186">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-186">Required</span></span> | <span data-ttu-id="a9723-187">员工的出生日期</span><span class="sxs-lookup"><span data-stu-id="a9723-187">The employee's birth date</span></span> |
| <span data-ttu-id="a9723-188">**标识号**</span><span class="sxs-lookup"><span data-stu-id="a9723-188">**Identification number to**</span></span><br><span data-ttu-id="a9723-189">mshr_identificationnumber</span><span class="sxs-lookup"><span data-stu-id="a9723-189">mshr_identificationnumber</span></span><br><span data-ttu-id="a9723-190">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a9723-190">*String*</span></span> | <span data-ttu-id="a9723-191">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-191">Read-only</span></span> <br><span data-ttu-id="a9723-192">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-192">Required</span></span> |<span data-ttu-id="a9723-193">针对员工定义的标识号。</span><span class="sxs-lookup"><span data-stu-id="a9723-193">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="a9723-194">**名**</span><span class="sxs-lookup"><span data-stu-id="a9723-194">**First name**</span></span><br><span data-ttu-id="a9723-195">mshr_firstname</span><span class="sxs-lookup"><span data-stu-id="a9723-195">mshr_firstname</span></span><br><span data-ttu-id="a9723-196">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a9723-196">*String*</span></span> | <span data-ttu-id="a9723-197">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-197">Read-only</span></span><br><span data-ttu-id="a9723-198">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-198">Required</span></span> | <span data-ttu-id="a9723-199">员工名字。</span><span class="sxs-lookup"><span data-stu-id="a9723-199">Employee first name.</span></span> |
| <span data-ttu-id="a9723-200">**中间名**</span><span class="sxs-lookup"><span data-stu-id="a9723-200">**Middle name**</span></span><br><span data-ttu-id="a9723-201">mshr_middlename</span><span class="sxs-lookup"><span data-stu-id="a9723-201">mshr_middlename</span></span><br><span data-ttu-id="a9723-202">*字符串*</span><span class="sxs-lookup"><span data-stu-id="a9723-202">*String*</span></span> | <span data-ttu-id="a9723-203">只读</span><span class="sxs-lookup"><span data-stu-id="a9723-203">Read-only</span></span><br><span data-ttu-id="a9723-204">必填</span><span class="sxs-lookup"><span data-stu-id="a9723-204">Required</span></span> |<span data-ttu-id="a9723-205">员工中间名。</span><span class="sxs-lookup"><span data-stu-id="a9723-205">Employee middle name.</span></span>  |

## <a name="example-query-for-payroll-employee"></a><span data-ttu-id="a9723-206">工资单员工的示例查询</span><span class="sxs-lookup"><span data-stu-id="a9723-206">Example query for Payroll employee</span></span>

<span data-ttu-id="a9723-207">**申请**</span><span class="sxs-lookup"><span data-stu-id="a9723-207">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

<span data-ttu-id="a9723-208">**响应**</span><span class="sxs-lookup"><span data-stu-id="a9723-208">**Response**</span></span>

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```
