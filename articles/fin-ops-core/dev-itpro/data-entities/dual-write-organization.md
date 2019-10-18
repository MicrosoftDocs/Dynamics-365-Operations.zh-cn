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
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182017"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="a3d9b-103">Common Data Service 中的组织层次结构</span><span class="sxs-lookup"><span data-stu-id="a3d9b-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="a3d9b-104">因为 Dynamics 365 Finance 是财务系统，所以*组织*是核心概念，并且系统设置从确认组织层次结构开始。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="a3d9b-105">然后可以在组织级别，还可以在组织层次结构中的任何级别跟踪企业的财务。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="a3d9b-106">尽管 Common Data Service 没有组织层次结构这个概念，但是的确有一些松散的概念，如总销售收入。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="a3d9b-107">在 Common Data Service 集成中，组织层次结构数据结构添加到了 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="a3d9b-108">数据流</span><span class="sxs-lookup"><span data-stu-id="a3d9b-108">Data flow</span></span>

<span data-ttu-id="a3d9b-109">包含 Finance and Operations 应用和 Common Data Service 的业务生态系统将继续采用组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="a3d9b-110">这种组织层次结构基于 Finance and Operations 应用，并在 Common Data Service 中显示以实现参考和扩展性目的。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="a3d9b-111">下图显示在 Common Data Service 中显示为从 Finance and Operations 应用到 Common Data Service 的单向数据流的组织层次结构信息。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![体系结构图像](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="a3d9b-113">模板</span><span class="sxs-lookup"><span data-stu-id="a3d9b-113">Templates</span></span>

<span data-ttu-id="a3d9b-114">组织层次结构实体映射可用于从 Finance and Operations 应用到 Common Data Service 的单向数据同步。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="a3d9b-115">内部组织层次结构目的</span><span class="sxs-lookup"><span data-stu-id="a3d9b-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="a3d9b-116">此模板提供组织层次结构目的实体从 Finance and Operations 到其他 Dynamics 365 应用的单向同步。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="a3d9b-117">源字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-117">Source field</span></span> | <span data-ttu-id="a3d9b-118">映射类型</span><span class="sxs-lookup"><span data-stu-id="a3d9b-118">Map type</span></span> | <span data-ttu-id="a3d9b-119">目标字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-119">Destination field</span></span>
---|---|---
<span data-ttu-id="a3d9b-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="a3d9b-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="a3d9b-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="a3d9b-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="a3d9b-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="a3d9b-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="a3d9b-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="a3d9b-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="a3d9b-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="a3d9b-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="a3d9b-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="a3d9b-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="a3d9b-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="a3d9b-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="a3d9b-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="a3d9b-127">msdyn\_immutable</span></span>
<span data-ttu-id="a3d9b-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="a3d9b-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="a3d9b-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="a3d9b-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="a3d9b-130">内部组织层次结构类型</span><span class="sxs-lookup"><span data-stu-id="a3d9b-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="a3d9b-131">此模板提供组织层次结构类型实体从 Finance and Operations 到其他 Dynamics 365 应用的单向同步。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="a3d9b-132">源字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-132">Source field</span></span> | <span data-ttu-id="a3d9b-133">映射类型</span><span class="sxs-lookup"><span data-stu-id="a3d9b-133">Map type</span></span> | <span data-ttu-id="a3d9b-134">目标字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-134">Destination field</span></span>
---|---|---
<span data-ttu-id="a3d9b-135">名称</span><span class="sxs-lookup"><span data-stu-id="a3d9b-135">NAME</span></span> | \> | <span data-ttu-id="a3d9b-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="a3d9b-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="a3d9b-137">内部组织层次结构</span><span class="sxs-lookup"><span data-stu-id="a3d9b-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="a3d9b-138">此模板提供组织层次结构已发布实体从 Finance and Operations 到其他 Dynamics 365 应用的单向同步。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="a3d9b-139">源字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-139">Source field</span></span> | <span data-ttu-id="a3d9b-140">映射类型</span><span class="sxs-lookup"><span data-stu-id="a3d9b-140">Map type</span></span> | <span data-ttu-id="a3d9b-141">目标字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-141">Destination field</span></span>
---|---|---
<span data-ttu-id="a3d9b-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="a3d9b-142">VALIDTO</span></span> | \> | <span data-ttu-id="a3d9b-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="a3d9b-143">msdyn\_validto</span></span>
<span data-ttu-id="a3d9b-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="a3d9b-144">VALIDFROM</span></span> | \> | <span data-ttu-id="a3d9b-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="a3d9b-145">msdyn\_validfrom</span></span>
<span data-ttu-id="a3d9b-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="a3d9b-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="a3d9b-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="a3d9b-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="a3d9b-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3d9b-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="a3d9b-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="a3d9b-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="a3d9b-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3d9b-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="a3d9b-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="a3d9b-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="a3d9b-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="a3d9b-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="a3d9b-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="a3d9b-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="a3d9b-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3d9b-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="a3d9b-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="a3d9b-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="a3d9b-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3d9b-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="a3d9b-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="a3d9b-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="a3d9b-158">内部组织</span><span class="sxs-lookup"><span data-stu-id="a3d9b-158">Internal Organization</span></span>

<span data-ttu-id="a3d9b-159">Common Data Service 中的内部组织信息来自两个实体：**运营单位**和**法人**。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="a3d9b-160">运营单位</span><span class="sxs-lookup"><span data-stu-id="a3d9b-160">Operating unit</span></span>

<span data-ttu-id="a3d9b-161">源字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-161">Source field</span></span> | <span data-ttu-id="a3d9b-162">映射类型</span><span class="sxs-lookup"><span data-stu-id="a3d9b-162">Map type</span></span> | <span data-ttu-id="a3d9b-163">目标字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-163">Destination field</span></span>
---|---|---
<span data-ttu-id="a3d9b-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="a3d9b-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="a3d9b-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="a3d9b-165">msdyn\_languageid</span></span>
<span data-ttu-id="a3d9b-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="a3d9b-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="a3d9b-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="a3d9b-167">msdyn\_namealias</span></span>
<span data-ttu-id="a3d9b-168">名称</span><span class="sxs-lookup"><span data-stu-id="a3d9b-168">NAME</span></span> | \> | <span data-ttu-id="a3d9b-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="a3d9b-169">msdyn\_name</span></span>
<span data-ttu-id="a3d9b-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3d9b-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="a3d9b-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="a3d9b-171">msdyn\_partynumber</span></span>
<span data-ttu-id="a3d9b-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="a3d9b-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="a3d9b-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="a3d9b-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="a3d9b-174">法人</span><span class="sxs-lookup"><span data-stu-id="a3d9b-174">Legal entity</span></span>

<span data-ttu-id="a3d9b-175">源字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-175">Source field</span></span> | <span data-ttu-id="a3d9b-176">映射类型</span><span class="sxs-lookup"><span data-stu-id="a3d9b-176">Map type</span></span> | <span data-ttu-id="a3d9b-177">目标字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-177">Destination field</span></span>
---|---|---
<span data-ttu-id="a3d9b-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="a3d9b-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="a3d9b-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="a3d9b-179">msdyn\_namealias</span></span>
<span data-ttu-id="a3d9b-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="a3d9b-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="a3d9b-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="a3d9b-181">msdyn\_languageid</span></span>
<span data-ttu-id="a3d9b-182">名称</span><span class="sxs-lookup"><span data-stu-id="a3d9b-182">NAME</span></span> | \> | <span data-ttu-id="a3d9b-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="a3d9b-183">msdyn\_name</span></span>
<span data-ttu-id="a3d9b-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="a3d9b-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="a3d9b-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="a3d9b-185">msdyn\_partynumber</span></span>
<span data-ttu-id="a3d9b-186">无</span><span class="sxs-lookup"><span data-stu-id="a3d9b-186">none</span></span> | \>\> | <span data-ttu-id="a3d9b-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="a3d9b-187">msdyn\_type</span></span>
<span data-ttu-id="a3d9b-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="a3d9b-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="a3d9b-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="a3d9b-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="a3d9b-190">公司</span><span class="sxs-lookup"><span data-stu-id="a3d9b-190">Company</span></span>

<span data-ttu-id="a3d9b-191">提供 Finance and Operations 与其他 Dynamics 365 应用之间法人（公司）信息的双向同步。</span><span class="sxs-lookup"><span data-stu-id="a3d9b-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="a3d9b-192">源字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-192">Source field</span></span> | <span data-ttu-id="a3d9b-193">映射类型</span><span class="sxs-lookup"><span data-stu-id="a3d9b-193">Map type</span></span> | <span data-ttu-id="a3d9b-194">目标字段</span><span class="sxs-lookup"><span data-stu-id="a3d9b-194">Destination field</span></span>
---|---|---
<span data-ttu-id="a3d9b-195">名称</span><span class="sxs-lookup"><span data-stu-id="a3d9b-195">NAME</span></span> | = | <span data-ttu-id="a3d9b-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="a3d9b-196">cdm\_name</span></span>
<span data-ttu-id="a3d9b-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="a3d9b-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="a3d9b-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="a3d9b-198">cdm\_companycode</span></span>
