---
title: 评级级别
description: 本主题介绍 Dynamics 365 Human Resources 的“评级级别”实体。
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
ms.openlocfilehash: 8bbd10bcc47a928070da7cd82e6d996f71c65698
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054828"
---
# <a name="rating-level"></a><span data-ttu-id="3bdf9-103">评级级别</span><span class="sxs-lookup"><span data-stu-id="3bdf9-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="3bdf9-104">本主题介绍 Dynamics 365 Human Resources 的“评级级别”实体。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="3bdf9-105">物理名称：mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="3bdf9-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="3bdf9-106">说明</span><span class="sxs-lookup"><span data-stu-id="3bdf9-106">Description</span></span>

<span data-ttu-id="3bdf9-107">此实体提供可用的技能评级级别。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="3bdf9-108">评级级别在所有法人中应用。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3bdf9-109">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="3bdf9-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="3bdf9-110">属性</span><span class="sxs-lookup"><span data-stu-id="3bdf9-110">Properties</span></span>

| <span data-ttu-id="3bdf9-111">属性</span><span class="sxs-lookup"><span data-stu-id="3bdf9-111">Property</span></span><br><span data-ttu-id="3bdf9-112">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="3bdf9-112">**Physical name**</span></span><br><span data-ttu-id="3bdf9-113">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="3bdf9-113">**_Type_**</span></span> | <span data-ttu-id="3bdf9-114">使用</span><span class="sxs-lookup"><span data-stu-id="3bdf9-114">Use</span></span> | <span data-ttu-id="3bdf9-115">说明</span><span class="sxs-lookup"><span data-stu-id="3bdf9-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="3bdf9-116">**评级级别实体 ID**</span><span class="sxs-lookup"><span data-stu-id="3bdf9-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="3bdf9-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="3bdf9-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="3bdf9-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3bdf9-118">*GUID*</span></span> | <span data-ttu-id="3bdf9-119">只读</span><span class="sxs-lookup"><span data-stu-id="3bdf9-119">Read-only</span></span><br><span data-ttu-id="3bdf9-120">必填</span><span class="sxs-lookup"><span data-stu-id="3bdf9-120">Required</span></span><br><span data-ttu-id="3bdf9-121">系统生成</span><span class="sxs-lookup"><span data-stu-id="3bdf9-121">System-generated</span></span> | <span data-ttu-id="3bdf9-122">系统生成的级别的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="3bdf9-123">**评级级别 ID**</span><span class="sxs-lookup"><span data-stu-id="3bdf9-123">**Rating Level ID**</span></span><br><span data-ttu-id="3bdf9-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="3bdf9-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="3bdf9-125">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3bdf9-125">*String*</span></span> | <span data-ttu-id="3bdf9-126">读/写</span><span class="sxs-lookup"><span data-stu-id="3bdf9-126">Read/write</span></span><br><span data-ttu-id="3bdf9-127">必填</span><span class="sxs-lookup"><span data-stu-id="3bdf9-127">Required</span></span> | <span data-ttu-id="3bdf9-128">级别的用户可读的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="3bdf9-129">**评级模型 ID**</span><span class="sxs-lookup"><span data-stu-id="3bdf9-129">**Rating Model ID**</span></span><br><span data-ttu-id="3bdf9-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="3bdf9-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="3bdf9-131">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3bdf9-131">*String*</span></span> | <span data-ttu-id="3bdf9-132">读/写</span><span class="sxs-lookup"><span data-stu-id="3bdf9-132">Read/write</span></span><br><span data-ttu-id="3bdf9-133">必填</span><span class="sxs-lookup"><span data-stu-id="3bdf9-133">Required</span></span> | <span data-ttu-id="3bdf9-134">评级级别所属的评级模型。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="3bdf9-135">**评级模型实体 ID**</span><span class="sxs-lookup"><span data-stu-id="3bdf9-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="3bdf9-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="3bdf9-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="3bdf9-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="3bdf9-137">*GUID*</span></span> | <span data-ttu-id="3bdf9-138">只读</span><span class="sxs-lookup"><span data-stu-id="3bdf9-138">Read-only</span></span><br><span data-ttu-id="3bdf9-139">必填</span><span class="sxs-lookup"><span data-stu-id="3bdf9-139">Required</span></span><br><span data-ttu-id="3bdf9-140">外键：mshr_hcmratingmodelentity 的 mshr_hcmratingmodelentityid</span><span class="sxs-lookup"><span data-stu-id="3bdf9-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="3bdf9-141">系统生成的评级级别所属的评级模型的标识符。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="3bdf9-142">**说明**</span><span class="sxs-lookup"><span data-stu-id="3bdf9-142">**Description**</span></span><br><span data-ttu-id="3bdf9-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="3bdf9-143">mshr_description</span></span><br><span data-ttu-id="3bdf9-144">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3bdf9-144">*String*</span></span> | <span data-ttu-id="3bdf9-145">读/写</span><span class="sxs-lookup"><span data-stu-id="3bdf9-145">Read/write</span></span><br><span data-ttu-id="3bdf9-146">必填</span><span class="sxs-lookup"><span data-stu-id="3bdf9-146">Required</span></span> | <span data-ttu-id="3bdf9-147">评级级别的描述。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-147">The description of the rating level.</span></span> |
| <span data-ttu-id="3bdf9-148">**系数**</span><span class="sxs-lookup"><span data-stu-id="3bdf9-148">**Factor**</span></span><br><span data-ttu-id="3bdf9-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="3bdf9-149">mshr_factor</span></span><br><span data-ttu-id="3bdf9-150">*整数*</span><span class="sxs-lookup"><span data-stu-id="3bdf9-150">*Integer*</span></span> | <span data-ttu-id="3bdf9-151">读/写</span><span class="sxs-lookup"><span data-stu-id="3bdf9-151">Read/write</span></span><br><span data-ttu-id="3bdf9-152">必填</span><span class="sxs-lookup"><span data-stu-id="3bdf9-152">Required</span></span> | <span data-ttu-id="3bdf9-153">评级级别的系数。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-153">The factor for the rating level.</span></span> <span data-ttu-id="3bdf9-154">在比较具有不同评级级别数的项时，系数用于使分数标准化。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="3bdf9-155">此值必须是 0 到 9 之间的一个整数。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="3bdf9-156">**注意**</span><span class="sxs-lookup"><span data-stu-id="3bdf9-156">**Note**</span></span><br><span data-ttu-id="3bdf9-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="3bdf9-157">mshr_note</span></span><br><span data-ttu-id="3bdf9-158">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3bdf9-158">*String*</span></span> | <span data-ttu-id="3bdf9-159">读/写</span><span class="sxs-lookup"><span data-stu-id="3bdf9-159">Read/write</span></span><br><span data-ttu-id="3bdf9-160">可选</span><span class="sxs-lookup"><span data-stu-id="3bdf9-160">Optional</span></span> | <span data-ttu-id="3bdf9-161">与评级级别关联的所有说明。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="3bdf9-162">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="3bdf9-162">**Primary Field**</span></span><br><span data-ttu-id="3bdf9-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="3bdf9-163">mshr_primaryfield</span></span><br><span data-ttu-id="3bdf9-164">*字符串*</span><span class="sxs-lookup"><span data-stu-id="3bdf9-164">*String*</span></span> | <span data-ttu-id="3bdf9-165">只读</span><span class="sxs-lookup"><span data-stu-id="3bdf9-165">Read-only</span></span><br><span data-ttu-id="3bdf9-166">必填</span><span class="sxs-lookup"><span data-stu-id="3bdf9-166">Required</span></span> | <span data-ttu-id="3bdf9-167">用作实体记录的标识符的字段。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="3bdf9-168">评级级别 ID 和评级模型 ID 的组合。</span><span class="sxs-lookup"><span data-stu-id="3bdf9-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="3bdf9-169">请参阅</span><span class="sxs-lookup"><span data-stu-id="3bdf9-169">See also</span></span>

[<span data-ttu-id="3bdf9-170">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="3bdf9-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="3bdf9-171">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="3bdf9-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]