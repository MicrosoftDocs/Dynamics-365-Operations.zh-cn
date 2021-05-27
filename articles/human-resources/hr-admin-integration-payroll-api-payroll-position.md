---
title: 职位的工资单详细信息
description: 本主题提供 Dynamics 365 Human Resources 中职位实体的详细信息和工资单详细信息的示例查询。
author: jcart
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
ms.openlocfilehash: 7b23ac5d11b18c77109be21afe1570755dccba20
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019314"
---
# <a name="payroll-position"></a><span data-ttu-id="31ddc-103">工资单职位</span><span class="sxs-lookup"><span data-stu-id="31ddc-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="31ddc-104">本主题提供 Dynamics 365 Human Resources 中职位实体的详细信息和工资单详细信息的示例查询。</span><span class="sxs-lookup"><span data-stu-id="31ddc-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="31ddc-105">属性</span><span class="sxs-lookup"><span data-stu-id="31ddc-105">Properties</span></span>

| <span data-ttu-id="31ddc-106">属性</span><span class="sxs-lookup"><span data-stu-id="31ddc-106">Property</span></span><br><span data-ttu-id="31ddc-107">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="31ddc-107">**Physical name**</span></span><br><span data-ttu-id="31ddc-108">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="31ddc-108">**_Type_**</span></span> | <span data-ttu-id="31ddc-109">使用</span><span class="sxs-lookup"><span data-stu-id="31ddc-109">Use</span></span> | <span data-ttu-id="31ddc-110">说明</span><span class="sxs-lookup"><span data-stu-id="31ddc-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="31ddc-111">**年度常规时间(小时)**</span><span class="sxs-lookup"><span data-stu-id="31ddc-111">**Annual regular hours**</span></span><br><span data-ttu-id="31ddc-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="31ddc-112">annualregularhours</span></span><br><span data-ttu-id="31ddc-113">*十进制*</span><span class="sxs-lookup"><span data-stu-id="31ddc-113">*Decimal*</span></span> | <span data-ttu-id="31ddc-114">只读</span><span class="sxs-lookup"><span data-stu-id="31ddc-114">Read-only</span></span><br><span data-ttu-id="31ddc-115">必填</span><span class="sxs-lookup"><span data-stu-id="31ddc-115">Required</span></span> | <span data-ttu-id="31ddc-116">在职位上定义的年度常规小时。</span><span class="sxs-lookup"><span data-stu-id="31ddc-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="31ddc-117">**工资单职位详细信息实体 ID**</span><span class="sxs-lookup"><span data-stu-id="31ddc-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="31ddc-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="31ddc-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="31ddc-119">*GUID*</span><span class="sxs-lookup"><span data-stu-id="31ddc-119">*Guid*</span></span> | <span data-ttu-id="31ddc-120">必填</span><span class="sxs-lookup"><span data-stu-id="31ddc-120">Required</span></span><br><span data-ttu-id="31ddc-121">系统生成。</span><span class="sxs-lookup"><span data-stu-id="31ddc-121">System generated.</span></span> | <span data-ttu-id="31ddc-122">系统生成的用于唯一标识职位的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="31ddc-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="31ddc-123">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="31ddc-123">**Primary field**</span></span><br><span data-ttu-id="31ddc-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="31ddc-124">mshr_primaryfield</span></span><br><span data-ttu-id="31ddc-125">*字符串*</span><span class="sxs-lookup"><span data-stu-id="31ddc-125">*String*</span></span> | <span data-ttu-id="31ddc-126">必填</span><span class="sxs-lookup"><span data-stu-id="31ddc-126">Required</span></span><br><span data-ttu-id="31ddc-127">系统生成的</span><span class="sxs-lookup"><span data-stu-id="31ddc-127">System generated</span></span> |  |
| <span data-ttu-id="31ddc-128">**职位工作 ID 值**</span><span class="sxs-lookup"><span data-stu-id="31ddc-128">**Position job ID value**</span></span><br><span data-ttu-id="31ddc-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="31ddc-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="31ddc-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="31ddc-130">*GUID*</span></span> | <span data-ttu-id="31ddc-131">只读</span><span class="sxs-lookup"><span data-stu-id="31ddc-131">Read-only</span></span><br><span data-ttu-id="31ddc-132">必填</span><span class="sxs-lookup"><span data-stu-id="31ddc-132">Required</span></span><br><span data-ttu-id="31ddc-133">外键：mshr_payrollpositionjobentity 的 mshr_PayrollPositionJobEntity</span><span class="sxs-lookup"><span data-stu-id="31ddc-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="31ddc-134">与职位关联的工作的 ID。</span><span class="sxs-lookup"><span data-stu-id="31ddc-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="31ddc-135">**固定薪酬计划 ID 值**</span><span class="sxs-lookup"><span data-stu-id="31ddc-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="31ddc-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="31ddc-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="31ddc-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="31ddc-137">*GUID*</span></span> | <span data-ttu-id="31ddc-138">只读</span><span class="sxs-lookup"><span data-stu-id="31ddc-138">Read-only</span></span><br><span data-ttu-id="31ddc-139">必填</span><span class="sxs-lookup"><span data-stu-id="31ddc-139">Required</span></span><br><span data-ttu-id="31ddc-140">外键：mshr_payrollfixedcompensationplanentity 的 mshr_FixedCompPlan_id</span><span class="sxs-lookup"><span data-stu-id="31ddc-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="31ddc-141">与职位关联的固定薪酬计划的 ID。</span><span class="sxs-lookup"><span data-stu-id="31ddc-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="31ddc-142">**付薪周期 ID**</span><span class="sxs-lookup"><span data-stu-id="31ddc-142">**Pay cycle ID**</span></span><br><span data-ttu-id="31ddc-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="31ddc-143">mshr_primaryfield</span></span><br><span data-ttu-id="31ddc-144">*字符串*</span><span class="sxs-lookup"><span data-stu-id="31ddc-144">*String*</span></span> | <span data-ttu-id="31ddc-145">只读</span><span class="sxs-lookup"><span data-stu-id="31ddc-145">Read-only</span></span><br><span data-ttu-id="31ddc-146">必填</span><span class="sxs-lookup"><span data-stu-id="31ddc-146">Required</span></span> | <span data-ttu-id="31ddc-147">在职位上定义的付薪周期。</span><span class="sxs-lookup"><span data-stu-id="31ddc-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="31ddc-148">**由法人支付**</span><span class="sxs-lookup"><span data-stu-id="31ddc-148">**Paid by legal entity**</span></span><br><span data-ttu-id="31ddc-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="31ddc-149">paidbylegalentity</span></span><br><span data-ttu-id="31ddc-150">*字符串*</span><span class="sxs-lookup"><span data-stu-id="31ddc-150">*String*</span></span> | <span data-ttu-id="31ddc-151">只读</span><span class="sxs-lookup"><span data-stu-id="31ddc-151">Read-only</span></span><br><span data-ttu-id="31ddc-152">必填</span><span class="sxs-lookup"><span data-stu-id="31ddc-152">Required</span></span> | <span data-ttu-id="31ddc-153">在负责签发付款的职位上定义的法人。</span><span class="sxs-lookup"><span data-stu-id="31ddc-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="31ddc-154">**职位 ID**</span><span class="sxs-lookup"><span data-stu-id="31ddc-154">**Position ID**</span></span><br><span data-ttu-id="31ddc-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="31ddc-155">mshr_positionid</span></span><br><span data-ttu-id="31ddc-156">*字符串*</span><span class="sxs-lookup"><span data-stu-id="31ddc-156">*String*</span></span> | <span data-ttu-id="31ddc-157">只读</span><span class="sxs-lookup"><span data-stu-id="31ddc-157">Read-only</span></span><br><span data-ttu-id="31ddc-158">必填</span><span class="sxs-lookup"><span data-stu-id="31ddc-158">Required</span></span> | <span data-ttu-id="31ddc-159">职位的 ID。</span><span class="sxs-lookup"><span data-stu-id="31ddc-159">The ID of the position.</span></span> |
| <span data-ttu-id="31ddc-160">**失效日期**</span><span class="sxs-lookup"><span data-stu-id="31ddc-160">**Valid to**</span></span><br><span data-ttu-id="31ddc-161">validto</span><span class="sxs-lookup"><span data-stu-id="31ddc-161">validto</span></span><br><span data-ttu-id="31ddc-162">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="31ddc-162">*Date Time Offset*</span></span> | <span data-ttu-id="31ddc-163">只读</span><span class="sxs-lookup"><span data-stu-id="31ddc-163">Read-only</span></span><br><span data-ttu-id="31ddc-164">必填</span><span class="sxs-lookup"><span data-stu-id="31ddc-164">Required</span></span> |<span data-ttu-id="31ddc-165">位置详细信息有效的开始日期。</span><span class="sxs-lookup"><span data-stu-id="31ddc-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="31ddc-166">**生效日期**</span><span class="sxs-lookup"><span data-stu-id="31ddc-166">**Valid from**</span></span><br><span data-ttu-id="31ddc-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="31ddc-167">validfrom</span></span><br><span data-ttu-id="31ddc-168">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="31ddc-168">*Date Time Offset*</span></span> | <span data-ttu-id="31ddc-169">只读</span><span class="sxs-lookup"><span data-stu-id="31ddc-169">Read-only</span></span><br><span data-ttu-id="31ddc-170">必填</span><span class="sxs-lookup"><span data-stu-id="31ddc-170">Required</span></span> |<span data-ttu-id="31ddc-171">位置详细信息有效的结束日期。</span><span class="sxs-lookup"><span data-stu-id="31ddc-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="31ddc-172">**查询**</span><span class="sxs-lookup"><span data-stu-id="31ddc-172">**Query**</span></span>

<span data-ttu-id="31ddc-173">**申请**</span><span class="sxs-lookup"><span data-stu-id="31ddc-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="31ddc-174">**响应**</span><span class="sxs-lookup"><span data-stu-id="31ddc-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
