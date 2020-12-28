---
title: Dataverse 中的组织层次结构
description: 本主题介绍 Finance and Operations 应用与 Dataverse 之间的组织数据集成。
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680064"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="ab84e-103">Dataverse 中的组织层次结构</span><span class="sxs-lookup"><span data-stu-id="ab84e-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ab84e-104">因为 Dynamics 365 Finance 是财务系统，所以 *组织* 是核心概念，并且系统设置从确认组织层次结构开始。</span><span class="sxs-lookup"><span data-stu-id="ab84e-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="ab84e-105">然后可以在组织级别，还可以在组织层次结构中的任何级别跟踪企业的财务。</span><span class="sxs-lookup"><span data-stu-id="ab84e-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="ab84e-106">尽管 Dataverse 没有组织层次结构这个概念，但是的确有一些松散的概念，如总销售收入。</span><span class="sxs-lookup"><span data-stu-id="ab84e-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="ab84e-107">在 Dataverse 集成中，组织层次结构数据结构添加到了 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="ab84e-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="ab84e-108">数据流</span><span class="sxs-lookup"><span data-stu-id="ab84e-108">Data flow</span></span>

<span data-ttu-id="ab84e-109">包含 Finance and Operations 应用和 Dataverse 的业务生态系统将继续采用组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="ab84e-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="ab84e-110">这种组织层次结构基于 Finance and Operations 应用，并在 Dataverse 中显示以实现参考和扩展性目的。</span><span class="sxs-lookup"><span data-stu-id="ab84e-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="ab84e-111">下图显示在 Dataverse 中显示为从 Finance and Operations 应用到 Dataverse 的单向数据流的组织层次结构信息。</span><span class="sxs-lookup"><span data-stu-id="ab84e-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![体系结构图像](media/dual-write-data-flow.png)

<span data-ttu-id="ab84e-113">组织层次结构表映射可用于从 Finance and Operations 应用到 Dataverse 的单向数据同步。</span><span class="sxs-lookup"><span data-stu-id="ab84e-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="ab84e-114">模板</span><span class="sxs-lookup"><span data-stu-id="ab84e-114">Templates</span></span>

<span data-ttu-id="ab84e-115">产品信息包含与产品及其定义有关的所有信息，例如产品维度或跟踪维度和存储维度。</span><span class="sxs-lookup"><span data-stu-id="ab84e-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="ab84e-116">如下表所示，将创建表映射的集合以同步产品和相关信息。</span><span class="sxs-lookup"><span data-stu-id="ab84e-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="ab84e-117">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="ab84e-117">Finance and Operations apps</span></span> | <span data-ttu-id="ab84e-118">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="ab84e-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="ab84e-119">说明</span><span class="sxs-lookup"><span data-stu-id="ab84e-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="ab84e-120">组织层次结构目的</span><span class="sxs-lookup"><span data-stu-id="ab84e-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="ab84e-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="ab84e-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="ab84e-122">此模板提供组织层次结构目的实体的单向同步。</span><span class="sxs-lookup"><span data-stu-id="ab84e-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="ab84e-123">组织层次结构类型</span><span class="sxs-lookup"><span data-stu-id="ab84e-123">Organization hierarchy type</span></span> | <span data-ttu-id="ab84e-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="ab84e-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="ab84e-125">此模板提供组织层次结构类型实体的单向同步。</span><span class="sxs-lookup"><span data-stu-id="ab84e-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="ab84e-126">组织层次结构 - 已发布</span><span class="sxs-lookup"><span data-stu-id="ab84e-126">Organization hierarchy - published</span></span> | <span data-ttu-id="ab84e-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="ab84e-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="ab84e-128">此模板提供组织层次结构已发布实体的单向同步。</span><span class="sxs-lookup"><span data-stu-id="ab84e-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="ab84e-129">运营单位</span><span class="sxs-lookup"><span data-stu-id="ab84e-129">Operating unit</span></span> | <span data-ttu-id="ab84e-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="ab84e-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="ab84e-131">法人</span><span class="sxs-lookup"><span data-stu-id="ab84e-131">Legal entities</span></span> | <span data-ttu-id="ab84e-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="ab84e-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="ab84e-133">法人</span><span class="sxs-lookup"><span data-stu-id="ab84e-133">Legal entities</span></span> | <span data-ttu-id="ab84e-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="ab84e-134">cdm_companies</span></span> | <span data-ttu-id="ab84e-135">提供法人实体（公司）信息的双向同步。</span><span class="sxs-lookup"><span data-stu-id="ab84e-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="ab84e-136">内部组织</span><span class="sxs-lookup"><span data-stu-id="ab84e-136">Internal Organization</span></span>

<span data-ttu-id="ab84e-137">Dataverse 中的内部组织信息来自两个表：**运营单位** 和 **法人**。</span><span class="sxs-lookup"><span data-stu-id="ab84e-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
