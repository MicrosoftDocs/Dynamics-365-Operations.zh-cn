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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125705"
---
# <a name="certificate-type"></a><span data-ttu-id="5fe79-103">证书类型</span><span class="sxs-lookup"><span data-stu-id="5fe79-103">Certificate type</span></span>

<span data-ttu-id="5fe79-104">本主题介绍 Dynamics 365 Human Resources 的“证书类型”实体。</span><span class="sxs-lookup"><span data-stu-id="5fe79-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="5fe79-105">物理名称：mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="5fe79-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="5fe79-106">说明</span><span class="sxs-lookup"><span data-stu-id="5fe79-106">Description</span></span>

<span data-ttu-id="5fe79-107">此实体定义在 Human Resources 中设置的专业证书类型列表。</span><span class="sxs-lookup"><span data-stu-id="5fe79-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="5fe79-108">此实体不特定于法人（公司）。</span><span class="sxs-lookup"><span data-stu-id="5fe79-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="5fe79-109">JSON 表示</span><span class="sxs-lookup"><span data-stu-id="5fe79-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="5fe79-110">属性</span><span class="sxs-lookup"><span data-stu-id="5fe79-110">Properties</span></span>

| <span data-ttu-id="5fe79-111">属性</span><span class="sxs-lookup"><span data-stu-id="5fe79-111">Property</span></span><br><span data-ttu-id="5fe79-112">**物理名称**</span><span class="sxs-lookup"><span data-stu-id="5fe79-112">**Physical name**</span></span><br><span data-ttu-id="5fe79-113">**_类型_**</span><span class="sxs-lookup"><span data-stu-id="5fe79-113">**_Type_**</span></span> | <span data-ttu-id="5fe79-114">使用</span><span class="sxs-lookup"><span data-stu-id="5fe79-114">Use</span></span> | <span data-ttu-id="5fe79-115">说明</span><span class="sxs-lookup"><span data-stu-id="5fe79-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5fe79-116">**证书类型实体 ID**</span><span class="sxs-lookup"><span data-stu-id="5fe79-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="5fe79-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="5fe79-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="5fe79-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="5fe79-118">*GUID*</span></span> | <span data-ttu-id="5fe79-119">只读</span><span class="sxs-lookup"><span data-stu-id="5fe79-119">Read-only</span></span><br><span data-ttu-id="5fe79-120">必填</span><span class="sxs-lookup"><span data-stu-id="5fe79-120">Required</span></span> 
<span data-ttu-id="5fe79-121">系统生成</span><span class="sxs-lookup"><span data-stu-id="5fe79-121">System-generated</span></span> | <span data-ttu-id="5fe79-122">证书类型的唯一主要标识符。</span><span class="sxs-lookup"><span data-stu-id="5fe79-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="5fe79-123">**证书类型**</span><span class="sxs-lookup"><span data-stu-id="5fe79-123">**Certificate Type**</span></span><br><span data-ttu-id="5fe79-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="5fe79-124">mshr_certificatetype</span></span><br><span data-ttu-id="5fe79-125">*字符串*</span><span class="sxs-lookup"><span data-stu-id="5fe79-125">*String*</span></span> | <span data-ttu-id="5fe79-126">读/写</span><span class="sxs-lookup"><span data-stu-id="5fe79-126">Read/write</span></span><br><span data-ttu-id="5fe79-127">必填</span><span class="sxs-lookup"><span data-stu-id="5fe79-127">Required</span></span> | <span data-ttu-id="5fe79-128">证书类型的唯一用户可读标识符。</span><span class="sxs-lookup"><span data-stu-id="5fe79-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="5fe79-129">**说明**</span><span class="sxs-lookup"><span data-stu-id="5fe79-129">**Description**</span></span><br><span data-ttu-id="5fe79-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="5fe79-130">mshr_description</span></span><br><span data-ttu-id="5fe79-131">*字符串*</span><span class="sxs-lookup"><span data-stu-id="5fe79-131">*String*</span></span> | <span data-ttu-id="5fe79-132">读/写</span><span class="sxs-lookup"><span data-stu-id="5fe79-132">Read/write</span></span><br><span data-ttu-id="5fe79-133">必填</span><span class="sxs-lookup"><span data-stu-id="5fe79-133">Required</span></span> | <span data-ttu-id="5fe79-134">证书类型的描述。</span><span class="sxs-lookup"><span data-stu-id="5fe79-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="5fe79-135">**需要续订**</span><span class="sxs-lookup"><span data-stu-id="5fe79-135">**Require Renewal**</span></span><br><span data-ttu-id="5fe79-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="5fe79-136">mshr_requirerenewal</span></span><br><span data-ttu-id="5fe79-137">*mshr_noyes 选项集*</span><span class="sxs-lookup"><span data-stu-id="5fe79-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="5fe79-138">读/写</span><span class="sxs-lookup"><span data-stu-id="5fe79-138">Read/write</span></span><br><span data-ttu-id="5fe79-139">可选</span><span class="sxs-lookup"><span data-stu-id="5fe79-139">Optional</span></span> | <span data-ttu-id="5fe79-140">指示证书是否需要续订。</span><span class="sxs-lookup"><span data-stu-id="5fe79-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5fe79-141">请参阅</span><span class="sxs-lookup"><span data-stu-id="5fe79-141">See also</span></span>

[<span data-ttu-id="5fe79-142">申请人跟踪系统集成 API 简介</span><span class="sxs-lookup"><span data-stu-id="5fe79-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="5fe79-143">可雇用的应聘者的查询示例</span><span class="sxs-lookup"><span data-stu-id="5fe79-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

