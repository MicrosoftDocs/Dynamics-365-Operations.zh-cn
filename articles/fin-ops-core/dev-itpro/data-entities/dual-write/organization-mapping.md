---
title: Common Data Service 中的组织层次结构
description: 本主题介绍 Finance and Operations 应用与 Common Data Service 之间的组织数据集成。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fbf7cc33d12fb54d2ff02acc46ba2e284b2a2b3f
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019658"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="756a7-103">Common Data Service 中的组织层次结构</span><span class="sxs-lookup"><span data-stu-id="756a7-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="756a7-104">因为 Dynamics 365 Finance 是财务系统，所以*组织*是核心概念，并且系统设置从确认组织层次结构开始。</span><span class="sxs-lookup"><span data-stu-id="756a7-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="756a7-105">然后可以在组织级别，还可以在组织层次结构中的任何级别跟踪企业的财务。</span><span class="sxs-lookup"><span data-stu-id="756a7-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="756a7-106">尽管 Common Data Service 没有组织层次结构这个概念，但是的确有一些松散的概念，如总销售收入。</span><span class="sxs-lookup"><span data-stu-id="756a7-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="756a7-107">在 Common Data Service 集成中，组织层次结构数据结构添加到了 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="756a7-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="756a7-108">数据流</span><span class="sxs-lookup"><span data-stu-id="756a7-108">Data flow</span></span>

<span data-ttu-id="756a7-109">包含 Finance and Operations 应用和 Common Data Service 的业务生态系统将继续采用组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="756a7-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="756a7-110">这种组织层次结构基于 Finance and Operations 应用，并在 Common Data Service 中显示以实现参考和扩展性目的。</span><span class="sxs-lookup"><span data-stu-id="756a7-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="756a7-111">下图显示在 Common Data Service 中显示为从 Finance and Operations 应用到 Common Data Service 的单向数据流的组织层次结构信息。</span><span class="sxs-lookup"><span data-stu-id="756a7-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![体系结构图像](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="756a7-113">模板</span><span class="sxs-lookup"><span data-stu-id="756a7-113">Templates</span></span>

<span data-ttu-id="756a7-114">组织层次结构实体映射可用于从 Finance and Operations 应用到 Common Data Service 的单向数据同步。</span><span class="sxs-lookup"><span data-stu-id="756a7-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="756a7-115">模板</span><span class="sxs-lookup"><span data-stu-id="756a7-115">Templates</span></span>

<span data-ttu-id="756a7-116">产品信息包含与产品及其定义有关的所有信息，例如产品维度或跟踪维度和存储维度。</span><span class="sxs-lookup"><span data-stu-id="756a7-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="756a7-117">如下表所示，将创建实体映射的集合以同步产品和相关信息。</span><span class="sxs-lookup"><span data-stu-id="756a7-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="756a7-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="756a7-118">Finance and Operations</span></span> | <span data-ttu-id="756a7-119">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="756a7-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="756a7-120">说明</span><span class="sxs-lookup"><span data-stu-id="756a7-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="756a7-121">组织层次结构目的</span><span class="sxs-lookup"><span data-stu-id="756a7-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="756a7-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="756a7-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="756a7-123">此模板提供组织层次结构目的实体的单向同步。</span><span class="sxs-lookup"><span data-stu-id="756a7-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="756a7-124">组织层次结构类型</span><span class="sxs-lookup"><span data-stu-id="756a7-124">Organization hierarchy type</span></span> | <span data-ttu-id="756a7-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="756a7-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="756a7-126">此模板提供组织层次结构类型实体的单向同步。</span><span class="sxs-lookup"><span data-stu-id="756a7-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="756a7-127">组织层次结构 - 已发布</span><span class="sxs-lookup"><span data-stu-id="756a7-127">Organization hierarchy - published</span></span> | <span data-ttu-id="756a7-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="756a7-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="756a7-129">此模板提供组织层次结构已发布实体的单向同步。</span><span class="sxs-lookup"><span data-stu-id="756a7-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="756a7-130">运营单位</span><span class="sxs-lookup"><span data-stu-id="756a7-130">Operating unit</span></span> | <span data-ttu-id="756a7-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="756a7-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="756a7-132">法人</span><span class="sxs-lookup"><span data-stu-id="756a7-132">Legal entities</span></span> | <span data-ttu-id="756a7-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="756a7-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="756a7-134">法人</span><span class="sxs-lookup"><span data-stu-id="756a7-134">Legal entities</span></span> | <span data-ttu-id="756a7-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="756a7-135">cdm_companies</span></span> | <span data-ttu-id="756a7-136">提供法人实体（公司）信息的双向同步。</span><span class="sxs-lookup"><span data-stu-id="756a7-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="756a7-137">内部组织</span><span class="sxs-lookup"><span data-stu-id="756a7-137">Internal Organization</span></span>

<span data-ttu-id="756a7-138">Common Data Service 中的内部组织信息来自两个实体：**运营单位**和**法人**。</span><span class="sxs-lookup"><span data-stu-id="756a7-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

