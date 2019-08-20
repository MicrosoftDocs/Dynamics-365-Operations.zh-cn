---
title: Common Data Service 中的组织层次结构
description: 本主题介绍 Finance and Operations 与 Common Data Service 之间的组织数据集成。
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
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789158"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="efc80-103">Common Data Service 中的组织层次结构</span><span class="sxs-lookup"><span data-stu-id="efc80-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="efc80-104">因为 Microsoft Dynamics 365 for Finance and Operations 是财务系统，所以*组织*是核心概念，并且系统设置从确认组织层次结构开始。</span><span class="sxs-lookup"><span data-stu-id="efc80-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="efc80-105">然后可以在组织级别，还可以在组织层次结构中的任何级别跟踪企业的财务和运作。</span><span class="sxs-lookup"><span data-stu-id="efc80-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="efc80-106">尽管 Common Data Service 没有组织层次结构这个概念，但是的确有一些松散的概念，如总销售收入。</span><span class="sxs-lookup"><span data-stu-id="efc80-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="efc80-107">在 Common Data Service 集成中，组织层次结构数据结构添加到了 Common Data Service。</span><span class="sxs-lookup"><span data-stu-id="efc80-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="efc80-108">数据流</span><span class="sxs-lookup"><span data-stu-id="efc80-108">Data flow</span></span>

<span data-ttu-id="efc80-109">包含 Finance and Operations 和 Common Data Service 的业务生态系统将继续采用组织层次结构。</span><span class="sxs-lookup"><span data-stu-id="efc80-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="efc80-110">这种组织层次结构基于 Finance and Operations，并在 Common Data Service 中显示以实现参考和扩展性目的。</span><span class="sxs-lookup"><span data-stu-id="efc80-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="efc80-111">下图显示在 Common Data Service 中显示为从 Finance and Operations 到 Common Data Service 的单向数据流的组织层次结构信息。</span><span class="sxs-lookup"><span data-stu-id="efc80-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![体系结构图像](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="efc80-113">模板</span><span class="sxs-lookup"><span data-stu-id="efc80-113">Templates</span></span>

<span data-ttu-id="efc80-114">组织层次结构实体映射可用于从 Finance and Operations 到 Common Data Service 的单向数据同步。</span><span class="sxs-lookup"><span data-stu-id="efc80-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="efc80-115">内部组织层次结构目的</span><span class="sxs-lookup"><span data-stu-id="efc80-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="efc80-116">此模板提供组织层次结构目的实体从 Finance and Operations 到 Dynamics 365 for Customer Engagement 的单向同步。</span><span class="sxs-lookup"><span data-stu-id="efc80-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="efc80-117">源字段</span><span class="sxs-lookup"><span data-stu-id="efc80-117">Source field</span></span> | <span data-ttu-id="efc80-118">映射类型</span><span class="sxs-lookup"><span data-stu-id="efc80-118">Map type</span></span> | <span data-ttu-id="efc80-119">目标字段</span><span class="sxs-lookup"><span data-stu-id="efc80-119">Destination field</span></span>
---|---|---
<span data-ttu-id="efc80-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="efc80-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="efc80-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="efc80-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="efc80-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="efc80-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="efc80-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="efc80-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="efc80-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="efc80-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="efc80-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="efc80-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="efc80-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="efc80-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="efc80-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="efc80-127">msdyn\_immutable</span></span>
<span data-ttu-id="efc80-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="efc80-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="efc80-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="efc80-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="efc80-130">内部组织层次结构类型</span><span class="sxs-lookup"><span data-stu-id="efc80-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="efc80-131">此模板提供组织层次结构类型实体从 Finance and Operations 到 Customer Engagement 的单向同步。</span><span class="sxs-lookup"><span data-stu-id="efc80-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="efc80-132">源字段</span><span class="sxs-lookup"><span data-stu-id="efc80-132">Source field</span></span> | <span data-ttu-id="efc80-133">映射类型</span><span class="sxs-lookup"><span data-stu-id="efc80-133">Map type</span></span> | <span data-ttu-id="efc80-134">目标字段</span><span class="sxs-lookup"><span data-stu-id="efc80-134">Destination field</span></span>
---|---|---
<span data-ttu-id="efc80-135">名称</span><span class="sxs-lookup"><span data-stu-id="efc80-135">NAME</span></span> | \> | <span data-ttu-id="efc80-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="efc80-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="efc80-137">内部组织层次结构</span><span class="sxs-lookup"><span data-stu-id="efc80-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="efc80-138">此模板提供组织层次结构已发布实体从 Finance and Operations 到 Customer Engagement 的单向同步。</span><span class="sxs-lookup"><span data-stu-id="efc80-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="efc80-139">源字段</span><span class="sxs-lookup"><span data-stu-id="efc80-139">Source field</span></span> | <span data-ttu-id="efc80-140">映射类型</span><span class="sxs-lookup"><span data-stu-id="efc80-140">Map type</span></span> | <span data-ttu-id="efc80-141">目标字段</span><span class="sxs-lookup"><span data-stu-id="efc80-141">Destination field</span></span>
---|---|---
<span data-ttu-id="efc80-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="efc80-142">VALIDTO</span></span> | \> | <span data-ttu-id="efc80-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="efc80-143">msdyn\_validto</span></span>
<span data-ttu-id="efc80-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="efc80-144">VALIDFROM</span></span> | \> | <span data-ttu-id="efc80-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="efc80-145">msdyn\_validfrom</span></span>
<span data-ttu-id="efc80-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="efc80-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="efc80-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="efc80-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="efc80-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="efc80-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="efc80-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="efc80-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="efc80-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="efc80-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="efc80-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="efc80-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="efc80-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="efc80-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="efc80-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="efc80-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="efc80-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="efc80-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="efc80-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="efc80-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="efc80-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="efc80-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="efc80-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="efc80-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="efc80-158">内部组织</span><span class="sxs-lookup"><span data-stu-id="efc80-158">Internal Organization</span></span>

<span data-ttu-id="efc80-159">Common Data Service 中的内部组织信息来自两个 Finance and Operations 实体：**运营单位**和**法人**。</span><span class="sxs-lookup"><span data-stu-id="efc80-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="efc80-160">运营单位</span><span class="sxs-lookup"><span data-stu-id="efc80-160">Operating unit</span></span>

<span data-ttu-id="efc80-161">源字段</span><span class="sxs-lookup"><span data-stu-id="efc80-161">Source field</span></span> | <span data-ttu-id="efc80-162">映射类型</span><span class="sxs-lookup"><span data-stu-id="efc80-162">Map type</span></span> | <span data-ttu-id="efc80-163">目标字段</span><span class="sxs-lookup"><span data-stu-id="efc80-163">Destination field</span></span>
---|---|---
<span data-ttu-id="efc80-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="efc80-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="efc80-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="efc80-165">msdyn\_languageid</span></span>
<span data-ttu-id="efc80-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="efc80-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="efc80-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="efc80-167">msdyn\_namealias</span></span>
<span data-ttu-id="efc80-168">名称</span><span class="sxs-lookup"><span data-stu-id="efc80-168">NAME</span></span> | \> | <span data-ttu-id="efc80-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="efc80-169">msdyn\_name</span></span>
<span data-ttu-id="efc80-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="efc80-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="efc80-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="efc80-171">msdyn\_partynumber</span></span>
<span data-ttu-id="efc80-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="efc80-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="efc80-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="efc80-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="efc80-174">法人</span><span class="sxs-lookup"><span data-stu-id="efc80-174">Legal entity</span></span>

<span data-ttu-id="efc80-175">源字段</span><span class="sxs-lookup"><span data-stu-id="efc80-175">Source field</span></span> | <span data-ttu-id="efc80-176">映射类型</span><span class="sxs-lookup"><span data-stu-id="efc80-176">Map type</span></span> | <span data-ttu-id="efc80-177">目标字段</span><span class="sxs-lookup"><span data-stu-id="efc80-177">Destination field</span></span>
---|---|---
<span data-ttu-id="efc80-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="efc80-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="efc80-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="efc80-179">msdyn\_namealias</span></span>
<span data-ttu-id="efc80-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="efc80-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="efc80-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="efc80-181">msdyn\_languageid</span></span>
<span data-ttu-id="efc80-182">名称</span><span class="sxs-lookup"><span data-stu-id="efc80-182">NAME</span></span> | \> | <span data-ttu-id="efc80-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="efc80-183">msdyn\_name</span></span>
<span data-ttu-id="efc80-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="efc80-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="efc80-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="efc80-185">msdyn\_partynumber</span></span>
<span data-ttu-id="efc80-186">无</span><span class="sxs-lookup"><span data-stu-id="efc80-186">none</span></span> | \>\> | <span data-ttu-id="efc80-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="efc80-187">msdyn\_type</span></span>
<span data-ttu-id="efc80-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="efc80-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="efc80-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="efc80-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="efc80-190">公司</span><span class="sxs-lookup"><span data-stu-id="efc80-190">Company</span></span>

<span data-ttu-id="efc80-191">提供 Finance and Operations 与 Customer Engagement 之间法人（公司）信息的双向同步。</span><span class="sxs-lookup"><span data-stu-id="efc80-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="efc80-192">源字段</span><span class="sxs-lookup"><span data-stu-id="efc80-192">Source field</span></span> | <span data-ttu-id="efc80-193">映射类型</span><span class="sxs-lookup"><span data-stu-id="efc80-193">Map type</span></span> | <span data-ttu-id="efc80-194">目标字段</span><span class="sxs-lookup"><span data-stu-id="efc80-194">Destination field</span></span>
---|---|---
<span data-ttu-id="efc80-195">名称</span><span class="sxs-lookup"><span data-stu-id="efc80-195">NAME</span></span> | = | <span data-ttu-id="efc80-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="efc80-196">cdm\_name</span></span>
<span data-ttu-id="efc80-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="efc80-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="efc80-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="efc80-198">cdm\_companycode</span></span>
