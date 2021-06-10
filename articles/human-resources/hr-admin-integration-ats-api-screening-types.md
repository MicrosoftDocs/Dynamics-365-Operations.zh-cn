---
title: 筛选类型
description: 本主题介绍 Dynamics 365 Human Resources 的“筛选类型”实体。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb99c2fb57df883ab376c7f6aab547073bd0ff
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058288"
---
# <a name="screening-types"></a><span data-ttu-id="7b976-103">筛选类型</span><span class="sxs-lookup"><span data-stu-id="7b976-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7b976-104">本主题介绍 Dynamics 365 Human Resources 的“筛选类型”实体。</span><span class="sxs-lookup"><span data-stu-id="7b976-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7b976-105">物理名称：mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="7b976-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="7b976-106">说明</span><span class="sxs-lookup"><span data-stu-id="7b976-106">Description</span></span>

<span data-ttu-id="7b976-107">此实体描述公司为入职前和持续的员工筛选流程设置的筛选类型。</span><span class="sxs-lookup"><span data-stu-id="7b976-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7b976-108">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="7b976-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="7b976-109">属性</span><span class="sxs-lookup"><span data-stu-id="7b976-109">Properties</span></span>

| <span data-ttu-id="7b976-110">属性</span><span class="sxs-lookup"><span data-stu-id="7b976-110">Property</span></span><br><span data-ttu-id="7b976-111">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="7b976-111">**Physical name**</span></span><br><span data-ttu-id="7b976-112">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="7b976-112">**_Type_**</span></span> | <span data-ttu-id="7b976-113">使用</span><span class="sxs-lookup"><span data-stu-id="7b976-113">Use</span></span> | <span data-ttu-id="7b976-114">说明</span><span class="sxs-lookup"><span data-stu-id="7b976-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7b976-115">**筛选类型实体 ID**</span><span class="sxs-lookup"><span data-stu-id="7b976-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="7b976-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="7b976-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="7b976-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7b976-117">*GUID*</span></span> | <span data-ttu-id="7b976-118">只读</span><span class="sxs-lookup"><span data-stu-id="7b976-118">Read-only</span></span><br><span data-ttu-id="7b976-119">必填</span><span class="sxs-lookup"><span data-stu-id="7b976-119">Required</span></span><br><span data-ttu-id="7b976-120">系统生成</span><span class="sxs-lookup"><span data-stu-id="7b976-120">System-generated</span></span> | <span data-ttu-id="7b976-121">筛选类型记录的唯一主要标识符。</span><span class="sxs-lookup"><span data-stu-id="7b976-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="7b976-122">**筛选类型 ID**</span><span class="sxs-lookup"><span data-stu-id="7b976-122">**Screening Type ID**</span></span><br><span data-ttu-id="7b976-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="7b976-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="7b976-124">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7b976-124">*String*</span></span> | <span data-ttu-id="7b976-125">读/写</span><span class="sxs-lookup"><span data-stu-id="7b976-125">Read/write</span></span><br><span data-ttu-id="7b976-126">必填</span><span class="sxs-lookup"><span data-stu-id="7b976-126">Required</span></span> | <span data-ttu-id="7b976-127">用户定义的筛选类型的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="7b976-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="7b976-128">**说明**</span><span class="sxs-lookup"><span data-stu-id="7b976-128">**Description**</span></span><br><span data-ttu-id="7b976-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="7b976-129">mshr_description</span></span><br><span data-ttu-id="7b976-130">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7b976-130">*String*</span></span> | <span data-ttu-id="7b976-131">读/写</span><span class="sxs-lookup"><span data-stu-id="7b976-131">Read/write</span></span><br><span data-ttu-id="7b976-132">必填</span><span class="sxs-lookup"><span data-stu-id="7b976-132">Required</span></span> | <span data-ttu-id="7b976-133">筛选类型的描述。</span><span class="sxs-lookup"><span data-stu-id="7b976-133">The description of the screening type.</span></span> |
| <span data-ttu-id="7b976-134">**频率单位**</span><span class="sxs-lookup"><span data-stu-id="7b976-134">**Frequency Unit**</span></span><br><span data-ttu-id="7b976-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="7b976-135">mshr_frequencyunit</span></span><br><span data-ttu-id="7b976-136">*mshr_hcmfrequencyunit 选项集*</span><span class="sxs-lookup"><span data-stu-id="7b976-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="7b976-137">读/写</span><span class="sxs-lookup"><span data-stu-id="7b976-137">Read/write</span></span><br><span data-ttu-id="7b976-138">必填</span><span class="sxs-lookup"><span data-stu-id="7b976-138">Required</span></span> | <span data-ttu-id="7b976-139">描述必须为分配的人员完成的筛选的频率。</span><span class="sxs-lookup"><span data-stu-id="7b976-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="7b976-140">**生成来源**</span><span class="sxs-lookup"><span data-stu-id="7b976-140">**Generate From**</span></span><br><span data-ttu-id="7b976-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="7b976-141">mshr_generatefrom</span></span><br><span data-ttu-id="7b976-142">*mshr_hcmfrequencygeneratefrom 选项集*</span><span class="sxs-lookup"><span data-stu-id="7b976-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="7b976-143">读/写</span><span class="sxs-lookup"><span data-stu-id="7b976-143">Read-write</span></span><br><span data-ttu-id="7b976-144">必填</span><span class="sxs-lookup"><span data-stu-id="7b976-144">Required</span></span> | <span data-ttu-id="7b976-145">如果频率值是“一次性”以外的任何值，GenerateFrom 值将确定开始计算下一个筛选事件的日期。</span><span class="sxs-lookup"><span data-stu-id="7b976-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="7b976-146">**频率间隔**</span><span class="sxs-lookup"><span data-stu-id="7b976-146">**Frequency Interval**</span></span><br><span data-ttu-id="7b976-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="7b976-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="7b976-148">*整数*</span><span class="sxs-lookup"><span data-stu-id="7b976-148">*Integer*</span></span> | <span data-ttu-id="7b976-149">读/写</span><span class="sxs-lookup"><span data-stu-id="7b976-149">Read-write</span></span><br><span data-ttu-id="7b976-150">必填</span><span class="sxs-lookup"><span data-stu-id="7b976-150">Required</span></span> | <span data-ttu-id="7b976-151">如果频率值是“一次性”以外的任何值，您必须为每个筛选事件之间的时间单位定义一个间隔。</span><span class="sxs-lookup"><span data-stu-id="7b976-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7b976-152">请参阅</span><span class="sxs-lookup"><span data-stu-id="7b976-152">See also</span></span>

[<span data-ttu-id="7b976-153">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="7b976-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7b976-154">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="7b976-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]