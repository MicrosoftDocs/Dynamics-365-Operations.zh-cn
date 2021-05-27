---
title: 工资单固定薪酬计划
description: 本主题提供 Dynamics 365 Human Resources 中工资单固定薪酬计划实体的详细信息和示例查询。
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
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021288"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="9b30a-103">工资单固定薪酬计划</span><span class="sxs-lookup"><span data-stu-id="9b30a-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9b30a-104">本主题提供 Dynamics 365 Human Resources 中工资单固定薪酬计划实体的详细信息和示例查询。</span><span class="sxs-lookup"><span data-stu-id="9b30a-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="9b30a-105">属性</span><span class="sxs-lookup"><span data-stu-id="9b30a-105">Properties</span></span>

| <span data-ttu-id="9b30a-106">属性</span><span class="sxs-lookup"><span data-stu-id="9b30a-106">Property</span></span><br><span data-ttu-id="9b30a-107">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="9b30a-107">**Physical name**</span></span><br><span data-ttu-id="9b30a-108">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="9b30a-108">**_Type_**</span></span> | <span data-ttu-id="9b30a-109">使用</span><span class="sxs-lookup"><span data-stu-id="9b30a-109">Use</span></span> | <span data-ttu-id="9b30a-110">说明</span><span class="sxs-lookup"><span data-stu-id="9b30a-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="9b30a-111">**员工 ID**</span><span class="sxs-lookup"><span data-stu-id="9b30a-111">**Employee ID**</span></span><br><span data-ttu-id="9b30a-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="9b30a-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="9b30a-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9b30a-113">*GUID*</span></span> | <span data-ttu-id="9b30a-114">只读</span><span class="sxs-lookup"><span data-stu-id="9b30a-114">Read-only</span></span><br><span data-ttu-id="9b30a-115">必填</span><span class="sxs-lookup"><span data-stu-id="9b30a-115">Required</span></span><br><span data-ttu-id="9b30a-116">外键：mshr_payrollemployeeentity entity 的 mshr_Employee_id</span><span class="sxs-lookup"><span data-stu-id="9b30a-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="9b30a-117">员工 ID</span><span class="sxs-lookup"><span data-stu-id="9b30a-117">Employee ID</span></span> |
| <span data-ttu-id="9b30a-118">**付薪比率**</span><span class="sxs-lookup"><span data-stu-id="9b30a-118">**Pay rate**</span></span><br><span data-ttu-id="9b30a-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="9b30a-119">mshr_payrate</span></span><br><span data-ttu-id="9b30a-120">*十进制*</span><span class="sxs-lookup"><span data-stu-id="9b30a-120">*Decimal*</span></span> | <span data-ttu-id="9b30a-121">只读</span><span class="sxs-lookup"><span data-stu-id="9b30a-121">Read-only</span></span><br><span data-ttu-id="9b30a-122">必填</span><span class="sxs-lookup"><span data-stu-id="9b30a-122">Required</span></span> | <span data-ttu-id="9b30a-123">在固定薪酬计划中定义的付薪比率。</span><span class="sxs-lookup"><span data-stu-id="9b30a-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="9b30a-124">**计划 ID**</span><span class="sxs-lookup"><span data-stu-id="9b30a-124">**Plan ID**</span></span><br><span data-ttu-id="9b30a-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="9b30a-125">mshr_planid</span></span><br><span data-ttu-id="9b30a-126">*字符串*</span><span class="sxs-lookup"><span data-stu-id="9b30a-126">*String*</span></span> | <span data-ttu-id="9b30a-127">只读</span><span class="sxs-lookup"><span data-stu-id="9b30a-127">Read-only</span></span><br><span data-ttu-id="9b30a-128">必填</span><span class="sxs-lookup"><span data-stu-id="9b30a-128">Required</span></span> |<span data-ttu-id="9b30a-129">指定薪酬计划。</span><span class="sxs-lookup"><span data-stu-id="9b30a-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="9b30a-130">**生效日期**</span><span class="sxs-lookup"><span data-stu-id="9b30a-130">**Valid from**</span></span><br><span data-ttu-id="9b30a-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="9b30a-131">mshr_validfrom</span></span><br><span data-ttu-id="9b30a-132">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="9b30a-132">*Date Time Offset*</span></span> |  <span data-ttu-id="9b30a-133">只读</span><span class="sxs-lookup"><span data-stu-id="9b30a-133">Read-only</span></span><br><span data-ttu-id="9b30a-134">必填</span><span class="sxs-lookup"><span data-stu-id="9b30a-134">Required</span></span> |<span data-ttu-id="9b30a-135">员工固定薪酬有效的开始日期。</span><span class="sxs-lookup"><span data-stu-id="9b30a-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="9b30a-136">**工资单固定薪酬计划实体**</span><span class="sxs-lookup"><span data-stu-id="9b30a-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="9b30a-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="9b30a-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="9b30a-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="9b30a-138">*GUID*</span></span> | <span data-ttu-id="9b30a-139">必填</span><span class="sxs-lookup"><span data-stu-id="9b30a-139">Required</span></span><br><span data-ttu-id="9b30a-140">系统生成</span><span class="sxs-lookup"><span data-stu-id="9b30a-140">Sytem generated</span></span> | <span data-ttu-id="9b30a-141">系统生成的用于唯一标识薪酬计划的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="9b30a-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="9b30a-142">**付薪频率**</span><span class="sxs-lookup"><span data-stu-id="9b30a-142">**Pay frequency**</span></span><br><span data-ttu-id="9b30a-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="9b30a-143">mshr_payfrequency</span></span><br><span data-ttu-id="9b30a-144">*字符串*</span><span class="sxs-lookup"><span data-stu-id="9b30a-144">*String*</span></span> | <span data-ttu-id="9b30a-145">只读</span><span class="sxs-lookup"><span data-stu-id="9b30a-145">Read-only</span></span><br><span data-ttu-id="9b30a-146">必填</span><span class="sxs-lookup"><span data-stu-id="9b30a-146">Required</span></span> |<span data-ttu-id="9b30a-147">将向员工支付工资的频率。</span><span class="sxs-lookup"><span data-stu-id="9b30a-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="9b30a-148">**失效日期**</span><span class="sxs-lookup"><span data-stu-id="9b30a-148">**Valid to**</span></span><br><span data-ttu-id="9b30a-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="9b30a-149">mshr_validto</span></span><br><span data-ttu-id="9b30a-150">*日期/时间偏移*</span><span class="sxs-lookup"><span data-stu-id="9b30a-150">*Date Time Offset*</span></span> | <span data-ttu-id="9b30a-151">只读</span><span class="sxs-lookup"><span data-stu-id="9b30a-151">Read-only</span></span> <br><span data-ttu-id="9b30a-152">必填</span><span class="sxs-lookup"><span data-stu-id="9b30a-152">Required</span></span> | <span data-ttu-id="9b30a-153">员工固定薪酬有效的结束日期。</span><span class="sxs-lookup"><span data-stu-id="9b30a-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="9b30a-154">**职位 ID**</span><span class="sxs-lookup"><span data-stu-id="9b30a-154">**Position ID**</span></span><br><span data-ttu-id="9b30a-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="9b30a-155">mshr_positionid</span></span><br><span data-ttu-id="9b30a-156">*字符串*</span><span class="sxs-lookup"><span data-stu-id="9b30a-156">*String*</span></span> | <span data-ttu-id="9b30a-157">只读</span><span class="sxs-lookup"><span data-stu-id="9b30a-157">Read-only</span></span> <br><span data-ttu-id="9b30a-158">必填</span><span class="sxs-lookup"><span data-stu-id="9b30a-158">Required</span></span> | <span data-ttu-id="9b30a-159">与员工和固定薪酬计划登记关联的职位 ID。</span><span class="sxs-lookup"><span data-stu-id="9b30a-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="9b30a-160">**货币**</span><span class="sxs-lookup"><span data-stu-id="9b30a-160">**Currency**</span></span><br><span data-ttu-id="9b30a-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="9b30a-161">mshr_currency</span></span><br><span data-ttu-id="9b30a-162">*字符串*</span><span class="sxs-lookup"><span data-stu-id="9b30a-162">*String*</span></span> | <span data-ttu-id="9b30a-163">只读</span><span class="sxs-lookup"><span data-stu-id="9b30a-163">Read-only</span></span> <br><span data-ttu-id="9b30a-164">必填</span><span class="sxs-lookup"><span data-stu-id="9b30a-164">Required</span></span> |<span data-ttu-id="9b30a-165">针对固定薪酬计划定义的货币</span><span class="sxs-lookup"><span data-stu-id="9b30a-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="9b30a-166">**人员编号**</span><span class="sxs-lookup"><span data-stu-id="9b30a-166">**Personnel number**</span></span><br><span data-ttu-id="9b30a-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="9b30a-167">mshr_personnelnumber</span></span><br><span data-ttu-id="9b30a-168">*字符串*</span><span class="sxs-lookup"><span data-stu-id="9b30a-168">*String*</span></span> | <span data-ttu-id="9b30a-169">只读</span><span class="sxs-lookup"><span data-stu-id="9b30a-169">Read-only</span></span><br><span data-ttu-id="9b30a-170">必填</span><span class="sxs-lookup"><span data-stu-id="9b30a-170">Required</span></span> |<span data-ttu-id="9b30a-171">员工的唯一人员编号。</span><span class="sxs-lookup"><span data-stu-id="9b30a-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="9b30a-172">**查询**</span><span class="sxs-lookup"><span data-stu-id="9b30a-172">**Query**</span></span>

<span data-ttu-id="9b30a-173">**申请**</span><span class="sxs-lookup"><span data-stu-id="9b30a-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="9b30a-174">**响应**</span><span class="sxs-lookup"><span data-stu-id="9b30a-174">**Response**</span></span>

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
