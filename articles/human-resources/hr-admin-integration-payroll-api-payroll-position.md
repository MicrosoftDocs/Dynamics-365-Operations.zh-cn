---
title: 职位的工资单详细信息
description: 本主题提供 Dynamics 365 Human Resources 中职位实体的详细信息和工资单详细信息的示例查询。
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
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881932"
---
# <a name="payroll-position"></a><span data-ttu-id="45fb2-103">工资单职位</span><span class="sxs-lookup"><span data-stu-id="45fb2-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="45fb2-104">本主题提供 Dynamics 365 Human Resources 中职位实体的详细信息和工资单详细信息的示例查询。</span><span class="sxs-lookup"><span data-stu-id="45fb2-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="45fb2-105">属性</span><span class="sxs-lookup"><span data-stu-id="45fb2-105">Properties</span></span>

| <span data-ttu-id="45fb2-106">属性</span><span class="sxs-lookup"><span data-stu-id="45fb2-106">Property</span></span><br><span data-ttu-id="45fb2-107">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="45fb2-107">**Physical name**</span></span><br><span data-ttu-id="45fb2-108">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="45fb2-108">**_Type_**</span></span> | <span data-ttu-id="45fb2-109">使用</span><span class="sxs-lookup"><span data-stu-id="45fb2-109">Use</span></span> | <span data-ttu-id="45fb2-110">说明</span><span class="sxs-lookup"><span data-stu-id="45fb2-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="45fb2-111">**年度常规时间(小时)**</span><span class="sxs-lookup"><span data-stu-id="45fb2-111">**Annual regular hours**</span></span><br><span data-ttu-id="45fb2-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="45fb2-112">annualregularhours</span></span><br><span data-ttu-id="45fb2-113">*十进制*</span><span class="sxs-lookup"><span data-stu-id="45fb2-113">*Decimal*</span></span> | <span data-ttu-id="45fb2-114">只读</span><span class="sxs-lookup"><span data-stu-id="45fb2-114">Read-only</span></span><br><span data-ttu-id="45fb2-115">必填</span><span class="sxs-lookup"><span data-stu-id="45fb2-115">Required</span></span> | <span data-ttu-id="45fb2-116">在职位上定义的年度常规小时。</span><span class="sxs-lookup"><span data-stu-id="45fb2-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="45fb2-117">**工资单职位详细信息实体 ID**</span><span class="sxs-lookup"><span data-stu-id="45fb2-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="45fb2-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="45fb2-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="45fb2-119">*GUID*</span><span class="sxs-lookup"><span data-stu-id="45fb2-119">*Guid*</span></span> | <span data-ttu-id="45fb2-120">必填</span><span class="sxs-lookup"><span data-stu-id="45fb2-120">Required</span></span><br><span data-ttu-id="45fb2-121">系统生成。</span><span class="sxs-lookup"><span data-stu-id="45fb2-121">System generated.</span></span> | <span data-ttu-id="45fb2-122">系统生成的用于唯一标识职位的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="45fb2-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="45fb2-123">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="45fb2-123">**Primary field**</span></span><br><span data-ttu-id="45fb2-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="45fb2-124">mshr_primaryfield</span></span><br><span data-ttu-id="45fb2-125">*字符串*</span><span class="sxs-lookup"><span data-stu-id="45fb2-125">*String*</span></span> | <span data-ttu-id="45fb2-126">必填</span><span class="sxs-lookup"><span data-stu-id="45fb2-126">Required</span></span><br><span data-ttu-id="45fb2-127">系统生成的</span><span class="sxs-lookup"><span data-stu-id="45fb2-127">System generated</span></span> |  |
| <span data-ttu-id="45fb2-128">**职位工作 ID 值**</span><span class="sxs-lookup"><span data-stu-id="45fb2-128">**Position job ID value**</span></span><br><span data-ttu-id="45fb2-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="45fb2-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="45fb2-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="45fb2-130">*GUID*</span></span> | <span data-ttu-id="45fb2-131">只读</span><span class="sxs-lookup"><span data-stu-id="45fb2-131">Read-only</span></span><br><span data-ttu-id="45fb2-132">必填</span><span class="sxs-lookup"><span data-stu-id="45fb2-132">Required</span></span><br><span data-ttu-id="45fb2-133">外键：mshr_payrollpositionjobentity 的 mshr_PayrollPositionJobEntity</span><span class="sxs-lookup"><span data-stu-id="45fb2-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="45fb2-134">与职位关联的工作的 ID。</span><span class="sxs-lookup"><span data-stu-id="45fb2-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="45fb2-135">**固定薪酬计划 ID 值**</span><span class="sxs-lookup"><span data-stu-id="45fb2-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="45fb2-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="45fb2-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="45fb2-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="45fb2-137">*GUID*</span></span> | <span data-ttu-id="45fb2-138">只读</span><span class="sxs-lookup"><span data-stu-id="45fb2-138">Read-only</span></span><br><span data-ttu-id="45fb2-139">必填</span><span class="sxs-lookup"><span data-stu-id="45fb2-139">Required</span></span><br><span data-ttu-id="45fb2-140">外键：mshr_payrollfixedcompensationplanentity 的 mshr_FixedCompPlan_id</span><span class="sxs-lookup"><span data-stu-id="45fb2-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="45fb2-141">与职位关联的固定薪酬计划的 ID。</span><span class="sxs-lookup"><span data-stu-id="45fb2-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="45fb2-142">**付薪周期 ID**</span><span class="sxs-lookup"><span data-stu-id="45fb2-142">**Pay cycle ID**</span></span><br><span data-ttu-id="45fb2-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="45fb2-143">mshr_primaryfield</span></span><br><span data-ttu-id="45fb2-144">*字符串*</span><span class="sxs-lookup"><span data-stu-id="45fb2-144">*String*</span></span> | <span data-ttu-id="45fb2-145">只读</span><span class="sxs-lookup"><span data-stu-id="45fb2-145">Read-only</span></span><br><span data-ttu-id="45fb2-146">必填</span><span class="sxs-lookup"><span data-stu-id="45fb2-146">Required</span></span> | <span data-ttu-id="45fb2-147">在职位上定义的付薪周期。</span><span class="sxs-lookup"><span data-stu-id="45fb2-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="45fb2-148">**由法人支付**</span><span class="sxs-lookup"><span data-stu-id="45fb2-148">**Paid by legal entity**</span></span><br><span data-ttu-id="45fb2-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="45fb2-149">paidbylegalentity</span></span><br><span data-ttu-id="45fb2-150">*字符串*</span><span class="sxs-lookup"><span data-stu-id="45fb2-150">*String*</span></span> | <span data-ttu-id="45fb2-151">只读</span><span class="sxs-lookup"><span data-stu-id="45fb2-151">Read-only</span></span><br><span data-ttu-id="45fb2-152">必填</span><span class="sxs-lookup"><span data-stu-id="45fb2-152">Required</span></span> | <span data-ttu-id="45fb2-153">在负责签发付款的职位上定义的法人。</span><span class="sxs-lookup"><span data-stu-id="45fb2-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="45fb2-154">**职位 ID**</span><span class="sxs-lookup"><span data-stu-id="45fb2-154">**Position ID**</span></span><br><span data-ttu-id="45fb2-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="45fb2-155">mshr_positionid</span></span><br><span data-ttu-id="45fb2-156">*字符串*</span><span class="sxs-lookup"><span data-stu-id="45fb2-156">*String*</span></span> | <span data-ttu-id="45fb2-157">只读</span><span class="sxs-lookup"><span data-stu-id="45fb2-157">Read-only</span></span><br><span data-ttu-id="45fb2-158">必填</span><span class="sxs-lookup"><span data-stu-id="45fb2-158">Required</span></span> | <span data-ttu-id="45fb2-159">职位的 ID。</span><span class="sxs-lookup"><span data-stu-id="45fb2-159">The ID of the position.</span></span> |
| <span data-ttu-id="45fb2-160">**失效日期**</span><span class="sxs-lookup"><span data-stu-id="45fb2-160">**Valid to**</span></span><br><span data-ttu-id="45fb2-161">validto</span><span class="sxs-lookup"><span data-stu-id="45fb2-161">validto</span></span><br><span data-ttu-id="45fb2-162">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="45fb2-162">*Date Time Offset*</span></span> | <span data-ttu-id="45fb2-163">只读</span><span class="sxs-lookup"><span data-stu-id="45fb2-163">Read-only</span></span><br><span data-ttu-id="45fb2-164">必填</span><span class="sxs-lookup"><span data-stu-id="45fb2-164">Required</span></span> |<span data-ttu-id="45fb2-165">位置详细信息有效的开始日期。</span><span class="sxs-lookup"><span data-stu-id="45fb2-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="45fb2-166">**生效日期**</span><span class="sxs-lookup"><span data-stu-id="45fb2-166">**Valid from**</span></span><br><span data-ttu-id="45fb2-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="45fb2-167">validfrom</span></span><br><span data-ttu-id="45fb2-168">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="45fb2-168">*Date Time Offset*</span></span> | <span data-ttu-id="45fb2-169">只读</span><span class="sxs-lookup"><span data-stu-id="45fb2-169">Read-only</span></span><br><span data-ttu-id="45fb2-170">必填</span><span class="sxs-lookup"><span data-stu-id="45fb2-170">Required</span></span> |<span data-ttu-id="45fb2-171">位置详细信息有效的结束日期。</span><span class="sxs-lookup"><span data-stu-id="45fb2-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="45fb2-172">**查询**</span><span class="sxs-lookup"><span data-stu-id="45fb2-172">**Query**</span></span>

<span data-ttu-id="45fb2-173">**申请**</span><span class="sxs-lookup"><span data-stu-id="45fb2-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="45fb2-174">**响应**</span><span class="sxs-lookup"><span data-stu-id="45fb2-174">**Response**</span></span>

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
