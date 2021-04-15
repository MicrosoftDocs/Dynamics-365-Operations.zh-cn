---
title: 评级级别
description: 本主题介绍 Dynamics 365 Human Resources 的“评级级别”实体。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800325"
---
# <a name="rating-level"></a><span data-ttu-id="4ab3f-103">评级级别</span><span class="sxs-lookup"><span data-stu-id="4ab3f-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4ab3f-104">本主题介绍 Dynamics 365 Human Resources 的“评级级别”实体。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4ab3f-105">物理名称：mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="4ab3f-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="4ab3f-106">说明</span><span class="sxs-lookup"><span data-stu-id="4ab3f-106">Description</span></span>

<span data-ttu-id="4ab3f-107">此实体提供可用的技能评级级别。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="4ab3f-108">评级级别在所有法人中应用。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4ab3f-109">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="4ab3f-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="4ab3f-110">属性</span><span class="sxs-lookup"><span data-stu-id="4ab3f-110">Properties</span></span>

| <span data-ttu-id="4ab3f-111">属性</span><span class="sxs-lookup"><span data-stu-id="4ab3f-111">Property</span></span><br><span data-ttu-id="4ab3f-112">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="4ab3f-112">**Physical name**</span></span><br><span data-ttu-id="4ab3f-113">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="4ab3f-113">**_Type_**</span></span> | <span data-ttu-id="4ab3f-114">使用</span><span class="sxs-lookup"><span data-stu-id="4ab3f-114">Use</span></span> | <span data-ttu-id="4ab3f-115">说明</span><span class="sxs-lookup"><span data-stu-id="4ab3f-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4ab3f-116">**评级级别实体 ID**</span><span class="sxs-lookup"><span data-stu-id="4ab3f-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="4ab3f-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="4ab3f-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="4ab3f-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4ab3f-118">*GUID*</span></span> | <span data-ttu-id="4ab3f-119">只读</span><span class="sxs-lookup"><span data-stu-id="4ab3f-119">Read-only</span></span><br><span data-ttu-id="4ab3f-120">必填</span><span class="sxs-lookup"><span data-stu-id="4ab3f-120">Required</span></span><br><span data-ttu-id="4ab3f-121">系统生成</span><span class="sxs-lookup"><span data-stu-id="4ab3f-121">System-generated</span></span> | <span data-ttu-id="4ab3f-122">系统生成的级别的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="4ab3f-123">**评级级别 ID**</span><span class="sxs-lookup"><span data-stu-id="4ab3f-123">**Rating Level ID**</span></span><br><span data-ttu-id="4ab3f-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="4ab3f-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="4ab3f-125">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4ab3f-125">*String*</span></span> | <span data-ttu-id="4ab3f-126">读/写</span><span class="sxs-lookup"><span data-stu-id="4ab3f-126">Read/write</span></span><br><span data-ttu-id="4ab3f-127">必填</span><span class="sxs-lookup"><span data-stu-id="4ab3f-127">Required</span></span> | <span data-ttu-id="4ab3f-128">级别的用户可读的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="4ab3f-129">**评级模型 ID**</span><span class="sxs-lookup"><span data-stu-id="4ab3f-129">**Rating Model ID**</span></span><br><span data-ttu-id="4ab3f-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="4ab3f-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="4ab3f-131">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4ab3f-131">*String*</span></span> | <span data-ttu-id="4ab3f-132">读/写</span><span class="sxs-lookup"><span data-stu-id="4ab3f-132">Read/write</span></span><br><span data-ttu-id="4ab3f-133">必填</span><span class="sxs-lookup"><span data-stu-id="4ab3f-133">Required</span></span> | <span data-ttu-id="4ab3f-134">评级级别所属的评级模型。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="4ab3f-135">**评级模型实体 ID**</span><span class="sxs-lookup"><span data-stu-id="4ab3f-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="4ab3f-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="4ab3f-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="4ab3f-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4ab3f-137">*GUID*</span></span> | <span data-ttu-id="4ab3f-138">只读</span><span class="sxs-lookup"><span data-stu-id="4ab3f-138">Read-only</span></span><br><span data-ttu-id="4ab3f-139">必填</span><span class="sxs-lookup"><span data-stu-id="4ab3f-139">Required</span></span><br><span data-ttu-id="4ab3f-140">外键：mshr_hcmratingmodelentity 的 mshr_hcmratingmodelentityid</span><span class="sxs-lookup"><span data-stu-id="4ab3f-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="4ab3f-141">系统生成的评级级别所属的评级模型的标识符。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="4ab3f-142">**说明**</span><span class="sxs-lookup"><span data-stu-id="4ab3f-142">**Description**</span></span><br><span data-ttu-id="4ab3f-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="4ab3f-143">mshr_description</span></span><br><span data-ttu-id="4ab3f-144">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4ab3f-144">*String*</span></span> | <span data-ttu-id="4ab3f-145">读/写</span><span class="sxs-lookup"><span data-stu-id="4ab3f-145">Read/write</span></span><br><span data-ttu-id="4ab3f-146">必填</span><span class="sxs-lookup"><span data-stu-id="4ab3f-146">Required</span></span> | <span data-ttu-id="4ab3f-147">评级级别的描述。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-147">The description of the rating level.</span></span> |
| <span data-ttu-id="4ab3f-148">**系数**</span><span class="sxs-lookup"><span data-stu-id="4ab3f-148">**Factor**</span></span><br><span data-ttu-id="4ab3f-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="4ab3f-149">mshr_factor</span></span><br><span data-ttu-id="4ab3f-150">*整数*</span><span class="sxs-lookup"><span data-stu-id="4ab3f-150">*Integer*</span></span> | <span data-ttu-id="4ab3f-151">读/写</span><span class="sxs-lookup"><span data-stu-id="4ab3f-151">Read/write</span></span><br><span data-ttu-id="4ab3f-152">必填</span><span class="sxs-lookup"><span data-stu-id="4ab3f-152">Required</span></span> | <span data-ttu-id="4ab3f-153">评级级别的系数。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-153">The factor for the rating level.</span></span> <span data-ttu-id="4ab3f-154">在比较具有不同评级级别数的项时，系数用于使分数标准化。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="4ab3f-155">此值必须是 0 到 9 之间的一个整数。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="4ab3f-156">**注意**</span><span class="sxs-lookup"><span data-stu-id="4ab3f-156">**Note**</span></span><br><span data-ttu-id="4ab3f-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="4ab3f-157">mshr_note</span></span><br><span data-ttu-id="4ab3f-158">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4ab3f-158">*String*</span></span> | <span data-ttu-id="4ab3f-159">读/写</span><span class="sxs-lookup"><span data-stu-id="4ab3f-159">Read/write</span></span><br><span data-ttu-id="4ab3f-160">可选</span><span class="sxs-lookup"><span data-stu-id="4ab3f-160">Optional</span></span> | <span data-ttu-id="4ab3f-161">与评级级别关联的所有说明。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="4ab3f-162">**主要字段**</span><span class="sxs-lookup"><span data-stu-id="4ab3f-162">**Primary Field**</span></span><br><span data-ttu-id="4ab3f-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="4ab3f-163">mshr_primaryfield</span></span><br><span data-ttu-id="4ab3f-164">*字符串*</span><span class="sxs-lookup"><span data-stu-id="4ab3f-164">*String*</span></span> | <span data-ttu-id="4ab3f-165">只读</span><span class="sxs-lookup"><span data-stu-id="4ab3f-165">Read-only</span></span><br><span data-ttu-id="4ab3f-166">必填</span><span class="sxs-lookup"><span data-stu-id="4ab3f-166">Required</span></span> | <span data-ttu-id="4ab3f-167">用作实体记录的标识符的字段。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="4ab3f-168">评级级别 ID 和评级模型 ID 的组合。</span><span class="sxs-lookup"><span data-stu-id="4ab3f-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4ab3f-169">请参阅</span><span class="sxs-lookup"><span data-stu-id="4ab3f-169">See also</span></span>

[<span data-ttu-id="4ab3f-170">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="4ab3f-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4ab3f-171">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="4ab3f-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]