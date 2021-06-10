---
title: 工资单固定薪酬计划
description: 本主题提供 Dynamics 365 Human Resources 中工资单固定薪酬计划实体的详细信息和示例查询。
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
ms.openlocfilehash: 227082358c59abddd63f4faa4536a8df270a4d80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059080"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="e000e-103">工资单固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="e000e-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e000e-104">本主题提供 Dynamics 365 Human Resources 中工资单固定薪酬计划实体的详细信息和示例查询。</span><span class="sxs-lookup"><span data-stu-id="e000e-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="e000e-105">属性</span><span class="sxs-lookup"><span data-stu-id="e000e-105">Properties</span></span>

| <span data-ttu-id="e000e-106">属性</span><span class="sxs-lookup"><span data-stu-id="e000e-106">Property</span></span><br><span data-ttu-id="e000e-107">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="e000e-107">**Physical name**</span></span><br><span data-ttu-id="e000e-108">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="e000e-108">**_Type_**</span></span> | <span data-ttu-id="e000e-109">使用</span><span class="sxs-lookup"><span data-stu-id="e000e-109">Use</span></span> | <span data-ttu-id="e000e-110">说明</span><span class="sxs-lookup"><span data-stu-id="e000e-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e000e-111">**员工 ID**</span><span class="sxs-lookup"><span data-stu-id="e000e-111">**Employee ID**</span></span><br><span data-ttu-id="e000e-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="e000e-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="e000e-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e000e-113">*GUID*</span></span> | <span data-ttu-id="e000e-114">只读</span><span class="sxs-lookup"><span data-stu-id="e000e-114">Read-only</span></span><br><span data-ttu-id="e000e-115">必填</span><span class="sxs-lookup"><span data-stu-id="e000e-115">Required</span></span><br><span data-ttu-id="e000e-116">外键：mshr_payrollemployeeentity entity 的 mshr_Employee_id</span><span class="sxs-lookup"><span data-stu-id="e000e-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="e000e-117">员工 ID</span><span class="sxs-lookup"><span data-stu-id="e000e-117">Employee ID</span></span> |
| <span data-ttu-id="e000e-118">**付薪比率**</span><span class="sxs-lookup"><span data-stu-id="e000e-118">**Pay rate**</span></span><br><span data-ttu-id="e000e-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="e000e-119">mshr_payrate</span></span><br><span data-ttu-id="e000e-120">*十进制*</span><span class="sxs-lookup"><span data-stu-id="e000e-120">*Decimal*</span></span> | <span data-ttu-id="e000e-121">只读</span><span class="sxs-lookup"><span data-stu-id="e000e-121">Read-only</span></span><br><span data-ttu-id="e000e-122">必填</span><span class="sxs-lookup"><span data-stu-id="e000e-122">Required</span></span> | <span data-ttu-id="e000e-123">在固定薪酬计划中定义的付薪比率。</span><span class="sxs-lookup"><span data-stu-id="e000e-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="e000e-124">**计划 ID**</span><span class="sxs-lookup"><span data-stu-id="e000e-124">**Plan ID**</span></span><br><span data-ttu-id="e000e-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="e000e-125">mshr_planid</span></span><br><span data-ttu-id="e000e-126">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e000e-126">*String*</span></span> | <span data-ttu-id="e000e-127">只读</span><span class="sxs-lookup"><span data-stu-id="e000e-127">Read-only</span></span><br><span data-ttu-id="e000e-128">必填</span><span class="sxs-lookup"><span data-stu-id="e000e-128">Required</span></span> |<span data-ttu-id="e000e-129">指定薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="e000e-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="e000e-130">**生效日期**</span><span class="sxs-lookup"><span data-stu-id="e000e-130">**Valid from**</span></span><br><span data-ttu-id="e000e-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="e000e-131">mshr_validfrom</span></span><br><span data-ttu-id="e000e-132">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="e000e-132">*Date Time Offset*</span></span> |  <span data-ttu-id="e000e-133">只读</span><span class="sxs-lookup"><span data-stu-id="e000e-133">Read-only</span></span><br><span data-ttu-id="e000e-134">必填</span><span class="sxs-lookup"><span data-stu-id="e000e-134">Required</span></span> |<span data-ttu-id="e000e-135">员工固定薪酬有效的开始日期。</span><span class="sxs-lookup"><span data-stu-id="e000e-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="e000e-136">**工资单固定薪酬计划实体**</span><span class="sxs-lookup"><span data-stu-id="e000e-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="e000e-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="e000e-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="e000e-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e000e-138">*GUID*</span></span> | <span data-ttu-id="e000e-139">必填</span><span class="sxs-lookup"><span data-stu-id="e000e-139">Required</span></span><br><span data-ttu-id="e000e-140">系统生成</span><span class="sxs-lookup"><span data-stu-id="e000e-140">Sytem generated</span></span> | <span data-ttu-id="e000e-141">系统生成的用于唯一标识薪酬计划的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="e000e-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="e000e-142">**付薪频率**</span><span class="sxs-lookup"><span data-stu-id="e000e-142">**Pay frequency**</span></span><br><span data-ttu-id="e000e-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="e000e-143">mshr_payfrequency</span></span><br><span data-ttu-id="e000e-144">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e000e-144">*String*</span></span> | <span data-ttu-id="e000e-145">只读</span><span class="sxs-lookup"><span data-stu-id="e000e-145">Read-only</span></span><br><span data-ttu-id="e000e-146">必填</span><span class="sxs-lookup"><span data-stu-id="e000e-146">Required</span></span> |<span data-ttu-id="e000e-147">将向员工支付工资的频率。</span><span class="sxs-lookup"><span data-stu-id="e000e-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="e000e-148">**失效日期**</span><span class="sxs-lookup"><span data-stu-id="e000e-148">**Valid to**</span></span><br><span data-ttu-id="e000e-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="e000e-149">mshr_validto</span></span><br><span data-ttu-id="e000e-150">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="e000e-150">*Date Time Offset*</span></span> | <span data-ttu-id="e000e-151">只读</span><span class="sxs-lookup"><span data-stu-id="e000e-151">Read-only</span></span> <br><span data-ttu-id="e000e-152">必填</span><span class="sxs-lookup"><span data-stu-id="e000e-152">Required</span></span> | <span data-ttu-id="e000e-153">员工固定薪酬有效的结束日期。</span><span class="sxs-lookup"><span data-stu-id="e000e-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="e000e-154">**职位 ID**</span><span class="sxs-lookup"><span data-stu-id="e000e-154">**Position ID**</span></span><br><span data-ttu-id="e000e-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="e000e-155">mshr_positionid</span></span><br><span data-ttu-id="e000e-156">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e000e-156">*String*</span></span> | <span data-ttu-id="e000e-157">只读</span><span class="sxs-lookup"><span data-stu-id="e000e-157">Read-only</span></span> <br><span data-ttu-id="e000e-158">必填</span><span class="sxs-lookup"><span data-stu-id="e000e-158">Required</span></span> | <span data-ttu-id="e000e-159">与员工和固定薪酬计划登记关联的职位 ID。</span><span class="sxs-lookup"><span data-stu-id="e000e-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="e000e-160">**货币**</span><span class="sxs-lookup"><span data-stu-id="e000e-160">**Currency**</span></span><br><span data-ttu-id="e000e-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="e000e-161">mshr_currency</span></span><br><span data-ttu-id="e000e-162">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e000e-162">*String*</span></span> | <span data-ttu-id="e000e-163">只读</span><span class="sxs-lookup"><span data-stu-id="e000e-163">Read-only</span></span> <br><span data-ttu-id="e000e-164">必填</span><span class="sxs-lookup"><span data-stu-id="e000e-164">Required</span></span> |<span data-ttu-id="e000e-165">针对固定薪酬计划定义的货币</span><span class="sxs-lookup"><span data-stu-id="e000e-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="e000e-166">**人员编号**</span><span class="sxs-lookup"><span data-stu-id="e000e-166">**Personnel number**</span></span><br><span data-ttu-id="e000e-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="e000e-167">mshr_personnelnumber</span></span><br><span data-ttu-id="e000e-168">*字符串*</span><span class="sxs-lookup"><span data-stu-id="e000e-168">*String*</span></span> | <span data-ttu-id="e000e-169">只读</span><span class="sxs-lookup"><span data-stu-id="e000e-169">Read-only</span></span><br><span data-ttu-id="e000e-170">必填</span><span class="sxs-lookup"><span data-stu-id="e000e-170">Required</span></span> |<span data-ttu-id="e000e-171">员工的唯一人员编号。</span><span class="sxs-lookup"><span data-stu-id="e000e-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="e000e-172">**查询**</span><span class="sxs-lookup"><span data-stu-id="e000e-172">**Query**</span></span>

<span data-ttu-id="e000e-173">**申请**</span><span class="sxs-lookup"><span data-stu-id="e000e-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="e000e-174">**响应**</span><span class="sxs-lookup"><span data-stu-id="e000e-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
