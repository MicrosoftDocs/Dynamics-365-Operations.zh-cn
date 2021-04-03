---
title: 证书类型
description: 本主题介绍 Dynamics 365 Human Resources 的“证书类型”实体。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 962bccb3aaab16322d072417660ec3aac821183b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467473"
---
# <a name="certificate-type"></a><span data-ttu-id="7c04f-103">证书类型</span><span class="sxs-lookup"><span data-stu-id="7c04f-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7c04f-104">本主题介绍 Dynamics 365 Human Resources 的“证书类型”实体。</span><span class="sxs-lookup"><span data-stu-id="7c04f-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="7c04f-105">物理名称：mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="7c04f-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="7c04f-106">说明</span><span class="sxs-lookup"><span data-stu-id="7c04f-106">Description</span></span>

<span data-ttu-id="7c04f-107">此实体定义在 Human Resources 中设置的专业证书类型列表。</span><span class="sxs-lookup"><span data-stu-id="7c04f-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="7c04f-108">此实体不特定于法人（公司）。</span><span class="sxs-lookup"><span data-stu-id="7c04f-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="7c04f-109">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="7c04f-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="7c04f-110">属性</span><span class="sxs-lookup"><span data-stu-id="7c04f-110">Properties</span></span>

| <span data-ttu-id="7c04f-111">属性</span><span class="sxs-lookup"><span data-stu-id="7c04f-111">Property</span></span><br><span data-ttu-id="7c04f-112">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="7c04f-112">**Physical name**</span></span><br><span data-ttu-id="7c04f-113">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="7c04f-113">**_Type_**</span></span> | <span data-ttu-id="7c04f-114">使用</span><span class="sxs-lookup"><span data-stu-id="7c04f-114">Use</span></span> | <span data-ttu-id="7c04f-115">说明</span><span class="sxs-lookup"><span data-stu-id="7c04f-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="7c04f-116">**证书类型实体 ID**</span><span class="sxs-lookup"><span data-stu-id="7c04f-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="7c04f-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="7c04f-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="7c04f-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7c04f-118">*GUID*</span></span> | <span data-ttu-id="7c04f-119">只读</span><span class="sxs-lookup"><span data-stu-id="7c04f-119">Read-only</span></span><br><span data-ttu-id="7c04f-120">必填</span><span class="sxs-lookup"><span data-stu-id="7c04f-120">Required</span></span> 
<span data-ttu-id="7c04f-121">系统生成</span><span class="sxs-lookup"><span data-stu-id="7c04f-121">System-generated</span></span> | <span data-ttu-id="7c04f-122">证书类型的唯一主要标识符。</span><span class="sxs-lookup"><span data-stu-id="7c04f-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="7c04f-123">**证书类型**</span><span class="sxs-lookup"><span data-stu-id="7c04f-123">**Certificate Type**</span></span><br><span data-ttu-id="7c04f-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="7c04f-124">mshr_certificatetype</span></span><br><span data-ttu-id="7c04f-125">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7c04f-125">*String*</span></span> | <span data-ttu-id="7c04f-126">读/写</span><span class="sxs-lookup"><span data-stu-id="7c04f-126">Read/write</span></span><br><span data-ttu-id="7c04f-127">必填</span><span class="sxs-lookup"><span data-stu-id="7c04f-127">Required</span></span> | <span data-ttu-id="7c04f-128">证书类型的唯一用户可读标识符。</span><span class="sxs-lookup"><span data-stu-id="7c04f-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="7c04f-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="7c04f-129">**Description**</span></span><br><span data-ttu-id="7c04f-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="7c04f-130">mshr_description</span></span><br><span data-ttu-id="7c04f-131">*字符串*</span><span class="sxs-lookup"><span data-stu-id="7c04f-131">*String*</span></span> | <span data-ttu-id="7c04f-132">读/写</span><span class="sxs-lookup"><span data-stu-id="7c04f-132">Read/write</span></span><br><span data-ttu-id="7c04f-133">必填</span><span class="sxs-lookup"><span data-stu-id="7c04f-133">Required</span></span> | <span data-ttu-id="7c04f-134">证书类型的描述。</span><span class="sxs-lookup"><span data-stu-id="7c04f-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="7c04f-135">**需要续订**</span><span class="sxs-lookup"><span data-stu-id="7c04f-135">**Require Renewal**</span></span><br><span data-ttu-id="7c04f-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="7c04f-136">mshr_requirerenewal</span></span><br><span data-ttu-id="7c04f-137">*mshr_noyes 选项集*</span><span class="sxs-lookup"><span data-stu-id="7c04f-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="7c04f-138">读/写</span><span class="sxs-lookup"><span data-stu-id="7c04f-138">Read/write</span></span><br><span data-ttu-id="7c04f-139">可选</span><span class="sxs-lookup"><span data-stu-id="7c04f-139">Optional</span></span> | <span data-ttu-id="7c04f-140">指示证书是否需要续订。</span><span class="sxs-lookup"><span data-stu-id="7c04f-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7c04f-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="7c04f-141">See also</span></span>

[<span data-ttu-id="7c04f-142">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="7c04f-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="7c04f-143">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="7c04f-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]