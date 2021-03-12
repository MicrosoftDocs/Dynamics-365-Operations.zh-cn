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
ms.openlocfilehash: 5132fd85fdf2c08ccded9db590328c394a2f984e
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744685"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="d3df1-103">Dataverse 中的组织层次结构</span><span class="sxs-lookup"><span data-stu-id="d3df1-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d3df1-104">因为 Dynamics 365 Finance 是财务系统，所以 *组织* 是核心概念，并且系统设置从确认组织层次结构开始。</span><span class="sxs-lookup"><span data-stu-id="d3df1-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="d3df1-105">然后可以在组织级别，还可以在组织层次结构中的任何级别跟踪企业的财务。</span><span class="sxs-lookup"><span data-stu-id="d3df1-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="d3df1-106">尽管 Dataverse 没有组织层次结构这个概念，但是的确有一些松散的概念，如总销售收入。</span><span class="sxs-lookup"><span data-stu-id="d3df1-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="d3df1-107">在 Dataverse 集成中，组织层次结构数据结构添加到了 Dataverse。</span><span class="sxs-lookup"><span data-stu-id="d3df1-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="d3df1-108">数据流</span><span class="sxs-lookup"><span data-stu-id="d3df1-108">Data flow</span></span>

<span data-ttu-id="d3df1-109">包含 Finance and Operations 应用和 Dataverse 的业务生态系统将继续采用组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="d3df1-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="d3df1-110">这种组织层次结构基于 Finance and Operations 应用，并在 Dataverse 中显示以实现参考和扩展性目的。</span><span class="sxs-lookup"><span data-stu-id="d3df1-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="d3df1-111">下图显示在 Dataverse 中显示为从 Finance and Operations 应用到 Dataverse 的单向数据流的组织层次结构信息。</span><span class="sxs-lookup"><span data-stu-id="d3df1-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![体系结构图像](media/dual-write-data-flow.png)

<span data-ttu-id="d3df1-113">组织层次结构表映射可用于从 Finance and Operations 应用到 Dataverse 的单向数据同步。</span><span class="sxs-lookup"><span data-stu-id="d3df1-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="d3df1-114">模板</span><span class="sxs-lookup"><span data-stu-id="d3df1-114">Templates</span></span>

<span data-ttu-id="d3df1-115">产品信息包含与产品及其定义有关的所有信息，例如产品维度或跟踪维度和存储维度。</span><span class="sxs-lookup"><span data-stu-id="d3df1-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="d3df1-116">如下表所示，将创建表映射的集合以同步产品和相关信息。</span><span class="sxs-lookup"><span data-stu-id="d3df1-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="d3df1-117">Finance and Operations 应用</span><span class="sxs-lookup"><span data-stu-id="d3df1-117">Finance and Operations apps</span></span> | <span data-ttu-id="d3df1-118">其他 Dynamics 365 应用</span><span class="sxs-lookup"><span data-stu-id="d3df1-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="d3df1-119">说明</span><span class="sxs-lookup"><span data-stu-id="d3df1-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="d3df1-120">组织层次结构目的</span><span class="sxs-lookup"><span data-stu-id="d3df1-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="d3df1-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="d3df1-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="d3df1-122">此模板提供组织层次结构目的表的单向同步。</span><span class="sxs-lookup"><span data-stu-id="d3df1-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="d3df1-123">组织层次结构类型</span><span class="sxs-lookup"><span data-stu-id="d3df1-123">Organization hierarchy type</span></span> | <span data-ttu-id="d3df1-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="d3df1-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="d3df1-125">此模板提供组织层次结构类型表的单向同步。</span><span class="sxs-lookup"><span data-stu-id="d3df1-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="d3df1-126">组织层次结构 - 已发布</span><span class="sxs-lookup"><span data-stu-id="d3df1-126">Organization hierarchy - published</span></span> | <span data-ttu-id="d3df1-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="d3df1-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="d3df1-128">此模板提供组织层次结构已发布表的单向同步。</span><span class="sxs-lookup"><span data-stu-id="d3df1-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="d3df1-129">运营单位</span><span class="sxs-lookup"><span data-stu-id="d3df1-129">Operating unit</span></span> | <span data-ttu-id="d3df1-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="d3df1-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="d3df1-131">法人</span><span class="sxs-lookup"><span data-stu-id="d3df1-131">Legal entities</span></span> | <span data-ttu-id="d3df1-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="d3df1-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="d3df1-133">法人</span><span class="sxs-lookup"><span data-stu-id="d3df1-133">Legal entities</span></span> | <span data-ttu-id="d3df1-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="d3df1-134">cdm_companies</span></span> | <span data-ttu-id="d3df1-135">提供法人实体（公司）信息的双向同步。</span><span class="sxs-lookup"><span data-stu-id="d3df1-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="d3df1-136">内部组织</span><span class="sxs-lookup"><span data-stu-id="d3df1-136">Internal Organization</span></span>

<span data-ttu-id="d3df1-137">Dataverse 中的内部组织信息来自两个表：**运营单位** 和 **法人**。</span><span class="sxs-lookup"><span data-stu-id="d3df1-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
