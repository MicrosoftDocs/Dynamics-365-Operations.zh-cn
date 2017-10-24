---
title: "物料清单和配方"
description: "本文提供有关物料清单 (BOM) 和配方的信息，物料清单和配方是产品和产品变型定义的核心部分。 物料清单和配方指定特定产品必需的成分或材料。 配方还指定特定生产环境中接收的联产品和副产品。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, EcoResProductProcessManufacturingWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19331
ms.assetid: c19b437a-2de2-4728-9477-2bcb0c2b1f5e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3137d93dd91ec3e58937e97bdddb5ca51ec4084c
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="bills-of-materials-and-formulas"></a><span data-ttu-id="2c1d9-105">物料清单和配方</span><span class="sxs-lookup"><span data-stu-id="2c1d9-105">Bills of materials and formulas</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2c1d9-106">本文提供有关物料清单 (BOM) 和配方的信息，物料清单和配方是产品和产品变型定义的核心部分。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-106">This article provides information about bills of materials (BOMs) and formulas, which are a central part of the definition of products and product variants.</span></span> <span data-ttu-id="2c1d9-107">物料清单和配方指定特定产品必需的成分或材料。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-107">BOMs and formulas specify the required materials or ingredients for a specific product.</span></span> <span data-ttu-id="2c1d9-108">配方还指定特定生产环境中接收的联产品和副产品。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-108">Formulas also specify the co-products and by-products that are received in a specific production context.</span></span> 

<a name="bills-of-materials"></a><span data-ttu-id="2c1d9-109">物料清单</span><span class="sxs-lookup"><span data-stu-id="2c1d9-109">Bills of materials</span></span>
------------------

<span data-ttu-id="2c1d9-110">物料清单 (BOM) 用于定义生产产品所需的组件。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-110">A bill of materials (BOM) defines the components that are required in order to produce a product.</span></span> <span data-ttu-id="2c1d9-111">这些组件可以是原材料、半成品或成分。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-111">The components can be raw materials, semifinished products, or ingredients.</span></span> <span data-ttu-id="2c1d9-112">在某些情况下，服务可以在物料清单中引用。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-112">In some cases, services can be referenced in a BOM.</span></span> <span data-ttu-id="2c1d9-113">但是，物料清单通常描述的是所需的*材料资源*。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-113">However, BOMs typically describe the *material resources* that are required.</span></span>  

<span data-ttu-id="2c1d9-114">当与描述制作产品所需的工序和资源的工艺路线或生产流相结合时，物料清单将构成计算产品的估计成本的基础。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-114">When it's combined with a route or production flow that describes the operations and resources that are required in order to build a product, the BOM forms the foundation for calculating the estimated cost of the product.</span></span>  

<span data-ttu-id="2c1d9-115">物料清单是由以下信息说明的单个实体：</span><span class="sxs-lookup"><span data-stu-id="2c1d9-115">A BOM is an individual entity that is described by the following information:</span></span>

-   <span data-ttu-id="2c1d9-116">物料清单 ID</span><span class="sxs-lookup"><span data-stu-id="2c1d9-116">BOM ID</span></span>
-   <span data-ttu-id="2c1d9-117">物料清单名称</span><span class="sxs-lookup"><span data-stu-id="2c1d9-117">BOM name</span></span>
-   <span data-ttu-id="2c1d9-118">描述组件和成分的物料清单行</span><span class="sxs-lookup"><span data-stu-id="2c1d9-118">The BOM lines that describe the components and ingredients</span></span>
-   <span data-ttu-id="2c1d9-119">物料清单版本，定义物料清单适用的产品和期间</span><span class="sxs-lookup"><span data-stu-id="2c1d9-119">The BOM versions, which define the product and period that the BOM can be used for</span></span>

<span data-ttu-id="2c1d9-120">单个物料清单描述由唯一 ID 标识的单个级别。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-120">A single BOM describes a single level that is identified by a unique ID.</span></span> <span data-ttu-id="2c1d9-121">组件可能有自己的由物料清单版本引用的 BOM。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-121">Components might have their own BOMs that are referenced by BOM versions.</span></span> <span data-ttu-id="2c1d9-122">您可以在物料清单设计器中显示和编辑特定产品的物料清单的完整层次结构。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-122">You can display and edit the complete hierarchy of BOMs for a specific product in the BOM designer.</span></span>

### <a name="formulas-co-products-and-by-products"></a><span data-ttu-id="2c1d9-123">配方、联产品和副产品</span><span class="sxs-lookup"><span data-stu-id="2c1d9-123">Formulas, co-products, and by-products</span></span>

<span data-ttu-id="2c1d9-124">配方是通常用于流程制造的物料清单的子类型。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-124">A formula is a subtype of BOM that is typically used for process manufacturing.</span></span> <span data-ttu-id="2c1d9-125">除了组件和成分，配方还描述了联产品和副产品。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-125">In addition to components and ingredients, a formula describes co-products and by-products.</span></span> <span data-ttu-id="2c1d9-126">在实际版本中，配方的联产品和副产品的定义需要配方版本。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-126">In the actual version, the definition of co-products and by-products for the formula requires the formula version.</span></span> <span data-ttu-id="2c1d9-127">配方通常是为某个特定成品（配方或计划物料）定义的。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-127">A formula is typically defined for one specific finished product (a formula or planning item) that is defined in the formula version.</span></span>

### <a name="boms-in-the-product-lifecycle"></a><span data-ttu-id="2c1d9-128">产品生命周期中的物料清单</span><span class="sxs-lookup"><span data-stu-id="2c1d9-128">BOMs in the product lifecycle</span></span>

<span data-ttu-id="2c1d9-129">在产品生命周期中，可能出于各种原因创建很多类型的物料清单：</span><span class="sxs-lookup"><span data-stu-id="2c1d9-129">In the product lifecycle, many types of BOM might be created for various reasons:</span></span>

-   <span data-ttu-id="2c1d9-130">**草案物料清单** - 此物料清单提供了早期设计阶段中需要的材料的草案估计，并帮助您进行成本和预计产品属性的粗略估计。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-130">**Sketching/Draft BOM** – This BOM gives a draft estimation of required materials in an early design phase and helps you do a rough estimate of cost and estimated product attributes.</span></span> <span data-ttu-id="2c1d9-131">此物料清单通常不在企业资源规划 (ERP) 中使用。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-131">This BOM isn't usually used in enterprise resource planning (ERP).</span></span>
-   <span data-ttu-id="2c1d9-132">**工程物料清单** - 此物料清单通常在您设计基于现有产品组合的产品时使用。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-132">**Engineering BOM** – This BOM is typically used when you design products that are based on existing product portfolios.</span></span> <span data-ttu-id="2c1d9-133">工程物料清单在结构上可简化设计流程并将复杂的产品分为若干个工程模块。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-133">Engineering BOMs are structured to simplify the design process and group complex products into engineering modules.</span></span> <span data-ttu-id="2c1d9-134">对于简单的产品，可以将工程物料清单用于实际的生产流程。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-134">For simple products, it might be possible to engineering BOMs for the actual production process.</span></span> <span data-ttu-id="2c1d9-135">但是，对于其他产品，必须将工程物料清单物料转换为实际生产物料清单。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-135">However, for other products, the engineering BOM must be converted to an actual production BOM.</span></span> <span data-ttu-id="2c1d9-136">工程物料清单在物料清单层次结构中通常由虚拟表示。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-136">Engineering BOMS are typically represented by phantoms in the BOM hierarchy.</span></span> <span data-ttu-id="2c1d9-137">尽管工程物料清单可用于工序的规划和执行，但此方法可能导致效率低下，尤其是在创建了很多订单的重复性工序中。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-137">Although engineering BOMs can be used for the planning and execution of manufacturing operations, this approach can lead to inefficiencies, especially in repetitive operations where many orders are created.</span></span>
-   <span data-ttu-id="2c1d9-138">**计划物料清单** - 此物料清单用于执行物料需求的规划。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-138">**Planning BOM** – This BOM is used to do planning for material requirements.</span></span> <span data-ttu-id="2c1d9-139">组件和成分的需求根据成品的需求来计算。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-139">The demand of components and ingredients is calculated based on the demand of the finished products.</span></span> <span data-ttu-id="2c1d9-140">与成本计算物料清单相似，计划物料清单可能表示某个期间内使用的特定物料组合。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-140">Like costing BOMs, planning BOMs might represent a specific mix of material that is used in a period.</span></span>
-   <span data-ttu-id="2c1d9-141">**生产物料清单** - 这是用于特定生产的实际物料清单。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-141">**Production BOM** – This is the actual BOM that is used for a specific production.</span></span> <span data-ttu-id="2c1d9-142">生产物料清单必须考虑用于生产产品的实际资源。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-142">A production BOM must take into account the actual resources that are used to produce the product.</span></span> <span data-ttu-id="2c1d9-143">创建生产订单、批次订单或看板后，由虚拟表示的多个级别的物料清单将折叠为一个级别并分配到该订单的各个工序。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-143">When a production order, batch order, or kanban is created, the multiple levels of BOMs that are represented by phantoms are collapsed into one level and distributed over the operations for the order.</span></span>
-   <span data-ttu-id="2c1d9-144">**成本计算物料清单** - 此物料清单用于计算产品的估计成本。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-144">**Costing BOM** – This BOM is used to calculated the estimated cost of a product.</span></span> <span data-ttu-id="2c1d9-145">例如，您可以在使用标准成本或计算给定产品的估计计划成本后使用成本计算物料清单。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-145">For example, you can use a costing BOM when standard cost is used or the estimated planned cost of a given product is calculated.</span></span> <span data-ttu-id="2c1d9-146">成本计算物料清单可能引用应使用的物料和资源的特定组合。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-146">Costing BOMs can refer to a specific mix of materials and resources that is expected to be used.</span></span> <span data-ttu-id="2c1d9-147">因此，您可以使用成本计算物料清单为某个期间创建一个代表性估计成本并帮助避免日后出现差异。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-147">Therefore, you can use the costing BOM to create a representative estimated cost for a period and help avoid variances over time.</span></span>

<span data-ttu-id="2c1d9-148">实际用于某个实施的物料清单的类型取决于该实施以及业务方案和要求。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-148">The types of BOM that are actually used in an implementation depend on the implementation, and also on the business scenarios and requirements.</span></span> <span data-ttu-id="2c1d9-149">在简单实施中，计划物料清单、生产物料清单和成本计算物料清单可作为一个物料清单进行建模。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-149">In simple implementations, a planning BOM, production BOM, and costing BOM can be modeled as one BOM.</span></span> <span data-ttu-id="2c1d9-150">在工程变更频繁并具有多条备用工艺路线的环境中，可能需要更大的一组物料清单。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-150">In environments that have frequent engineering changes and multiple alternative routes, a larger set of BOM types will probably be required.</span></span>

### <a name="approval-of-boms-and-formulas"></a><span data-ttu-id="2c1d9-151">物料清单和配方的审核</span><span class="sxs-lookup"><span data-stu-id="2c1d9-151">Approval of BOMs and formulas</span></span>

<span data-ttu-id="2c1d9-152">每个物料清单和配方可以单独地获得批准或取消批准。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-152">Each BOM and formula can be separately approved or unapproved.</span></span> <span data-ttu-id="2c1d9-153">通常，物料清单或配方的审核在第一个相关物料清单版本获得批准时进行。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-153">Typically, approval of a BOM or formula occurs when the first relevant BOM version is approved.</span></span> <span data-ttu-id="2c1d9-154">但是，在某些企业方案中，这些审核可能是流程中的不同步骤，并可能涉及不同的流程负责人。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-154">However, in some business scenarios, these approvals might be different steps in the process and might involve different process owners.</span></span>  

<span data-ttu-id="2c1d9-155">请注意，如果物料清单未获得批准，所有相关物料清单版本也将未获得批准。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-155">Note that, if a BOM is unapproved, all related BOM versions are also unapproved.</span></span>

## <a name="bom-and-formula-versions"></a><span data-ttu-id="2c1d9-156">物料清单和配方版本</span><span class="sxs-lookup"><span data-stu-id="2c1d9-156">BOM and formula versions</span></span>
<span data-ttu-id="2c1d9-157">要将特定物料清单或配方与可生产的产品变型关联，您必须创建物料清单版本或配方版本。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-157">To relate a specific BOM or formula to a product variant that can be produced, you must create a BOM version or formula version.</span></span> <span data-ttu-id="2c1d9-158">物料清单版本和配方版本的有效性可能受到期间、数量、站点、特定物料维度和其他条件的约束。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-158">The validity of BOM versions and formula versions can be constrained by period, quantity, site, specific product dimensions, and other criteria.</span></span> <span data-ttu-id="2c1d9-159">配方版本具有其他重要属性，如产出、联产品和副产品定义以及配方的成本分配说明。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-159">Formula versions have additional important attributes, such as yield, co-product and by-product definitions, and the cost distribution instructions for the formula.</span></span>

### <a name="approval-of-bom-and-formula-versions"></a><span data-ttu-id="2c1d9-160">物料清单和配方版本的审核</span><span class="sxs-lookup"><span data-stu-id="2c1d9-160">Approval of BOM and formula versions</span></span>

<span data-ttu-id="2c1d9-161">必须先审核物料清单版本，然后才能在计划或制造流程中使用它。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-161">Before a BOM version can be used in the planning or manufacturing process, it must be approved.</span></span> <span data-ttu-id="2c1d9-162">在审核物料清单版本后，也可以审核相关物料清单，版本具体取决于用户的选择和身份验证权利。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-162">When a BOM version is approved, the related BOM can also be approved, depending on the user's selection and authentication rights.</span></span> <span data-ttu-id="2c1d9-163">请注意，仅在审核相关物料清单后才能审核物料清单版本。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-163">Note that a BOM version can be approved only if the related BOM itself is approved.</span></span>

### <a name="activation-of-the-default-bom-or-formula-version"></a><span data-ttu-id="2c1d9-164">默认物料清单或配方版本的启用</span><span class="sxs-lookup"><span data-stu-id="2c1d9-164">Activation of the default BOM or formula version</span></span>

<span data-ttu-id="2c1d9-165">要将特定物料清单或配方设置为将由主计划使用的或用于创建生产订单的默认物料清单版本或配方版本，您必须启用该版本。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-165">To set a specific BOM or formula as the default BOM version or formula version that will be used by master planning or used to create of production orders, you must activate the version.</span></span> <span data-ttu-id="2c1d9-166">在启用某个版本后，将验证该版本针对给定约束（例如，期间、站点或数量）的唯一性。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-166">When a version is activated, the uniqueness of the version for the given constraints (for example, period, site, or quantity) is verified.</span></span> <span data-ttu-id="2c1d9-167">如果您尝试启用的版本与已生效的版本相冲突，您将收到一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-167">You receive an error message if the version that you're trying to activate conflicts with a version that is already active.</span></span> <span data-ttu-id="2c1d9-168">您随后必须停用冲突的版本或修改版本约束（通常是期间）以防止不明确的启用。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-168">You must then either inactivate the conflicting version or modify the version constraints (usually the period) to prevent an ambiguous activation.</span></span>

### <a name="product-change-with-case-management"></a><span data-ttu-id="2c1d9-169">带案例管理的产品变更</span><span class="sxs-lookup"><span data-stu-id="2c1d9-169">Product change with case management</span></span>

<span data-ttu-id="2c1d9-170">适用于新的或已更改的物料清单和物料清单版本的产品变更案例提供了一个查看物料清单版本约束的简单方法。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-170">The product change case for approval and activation of new or changed BOMs and BOM versions provides an easy way to see an overview of the BOM version constraints.</span></span> <span data-ttu-id="2c1d9-171">您还可以审核和启用与一个启用日期的特定更改相关的所有物料清单和配方。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-171">You can also approve and activate all BOMs and formulas that are related to a specific change for one activation date.</span></span>

### <a name="alternative-bom-versions"></a><span data-ttu-id="2c1d9-172">备用物料清单版本</span><span class="sxs-lookup"><span data-stu-id="2c1d9-172">Alternative BOM versions</span></span>

<span data-ttu-id="2c1d9-173">有时候，有效的物料清单版本或配方版本不应在预测、销售或父产品中使用。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-173">Sometimes, the active BOM version or formula version should not be used in forecasts, sales, or a parent product.</span></span> <span data-ttu-id="2c1d9-174">在这种情况下，如果备用物料清单或配方已存在获得批准的物料清单版本和配方版本，您可以选择特定的获得批准的物料清单作为需求（预测行、销售行或物料清单行）的一部分。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-174">In this case, you can select a specific approved BOM as part of the requirement (forecast line, sales line, or BOM line) if an approved BOM version or formula version exists for the alternative BOM or formula.</span></span>  

<span data-ttu-id="2c1d9-175">在创建计划订单、生产订单或看板后，规划员或车间主管可使用在请求的计划生产日期生效的任何获得批准的物料清单版本来计划或生产特定产品。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-175">When planned orders, production orders, or kanbans are created, the planner or shop floor supervisor can use any approved BOM version that is valid on the requested planned production date to plan for or produce a specific product.</span></span> <span data-ttu-id="2c1d9-176">所使用的物料清单版本不必作为默认物料清单版本启用。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-176">The BOM version that is used doesn't have to be activated as the default BOM version.</span></span>

## <a name="bom-and-formula-lines"></a><span data-ttu-id="2c1d9-177">物料清单和配方行</span><span class="sxs-lookup"><span data-stu-id="2c1d9-177">BOM and formula lines</span></span>
<span data-ttu-id="2c1d9-178">将为每个物料、服务或成分创建物料清单行。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-178">A BOM line is created for each material, service, or ingredient.</span></span> <span data-ttu-id="2c1d9-179">该行定义了指定产品变型的计划消耗量，还定义了与计划消耗量相关的各种属性。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-179">The line defines the planned consumption of the specified product variant and also defines the various attributes that are related to the planned consumption.</span></span>  

<span data-ttu-id="2c1d9-180">物料清单行可以具有以下行类型：**“物料”**、**“虚拟”**、**“限定供应”**、**“供应商”**。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-180">BOM lines can have the following line types: **Item**, **Phantom**, **Pegged supply**, **Vendor**.</span></span>

### <a name="item"></a><span data-ttu-id="2c1d9-181">物料</span><span class="sxs-lookup"><span data-stu-id="2c1d9-181">Item</span></span>

<span data-ttu-id="2c1d9-182">为直接消耗但不需要进一步分解或限定供应的物料和服务选择**“物料”**行类型。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-182">Select the **Item** line type for materials or services that are directly consumed, and that don't require further explosion or pegged supply.</span></span>

### <a name="phantom"></a><span data-ttu-id="2c1d9-183">虚拟</span><span class="sxs-lookup"><span data-stu-id="2c1d9-183">Phantom</span></span>

<span data-ttu-id="2c1d9-184">当您要分解在物料清单行上包含的任何更低级别的物料清单物料时，请选择**“虚拟”**。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-184">Select the **Phantom** line type when you want to explode any lower-level BOM items that are contained on the BOM line.</span></span> <span data-ttu-id="2c1d9-185">在主计划编制中，在计划成本计算中，或者在使用**“虚拟”**类型的物料清单行的生产订单的估计中，引用具有虚拟物料清单的产品变型的父物料清单行将替换为在该物料清单中作为物料清单行列出的构成物料（由该产品变型的适用的有效物料清单版本确定）。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-185">In Master scheduling, in planned cost calculation, or on estimation of a production order that uses BOM lines of the **Phantom** type, the parent BOM line that refers to a product variant that has a phantom BOM is replaced by the component items that are listed as BOM lines in that BOM, as determined by the applicable active BOM version of that product variant.</span></span> <span data-ttu-id="2c1d9-186">如果产品变型具有适用的有效工艺路线，该工艺路线的工序将合并到父工艺路线中。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-186">If the product variant has an applicable active route, the operations of that route are merged into the parent route.</span></span>  

<span data-ttu-id="2c1d9-187">请注意，虚拟通常用于简化工程流程。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-187">Note that phantoms are typically used to simplify the engineering process.</span></span> <span data-ttu-id="2c1d9-188">在多个级别广泛使用虚拟物料清单会影响性能，尤其是在高度重复的制造方案中。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-188">Extensive use of phantom BOMs in many levels has an effect on performance, especially in highly repetitive manufacturing scenarios.</span></span> <span data-ttu-id="2c1d9-189">为了提高性能，您应该避免为虚拟设置较深的层次结构。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-189">To improve performance, you should avoid deep hierarchies of phantoms.</span></span> <span data-ttu-id="2c1d9-190">相反，您应使用预先分解的生产物料清单和工艺路线。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-190">Instead, use pre-exploded production BOMs and routes.</span></span>

### <a name="pegged-supply"></a><span data-ttu-id="2c1d9-191">限定供应</span><span class="sxs-lookup"><span data-stu-id="2c1d9-191">Pegged supply</span></span>

<span data-ttu-id="2c1d9-192">当您要创建子生产、创建物料清单行事件看板或创建物料清单行引用的任何产品变型的直接采购订单时，请选择**“限定供应“**。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-192">Select the **Pegged supply** line type when you want to create a subproduction, a BOM line event kanban, or a direct purchase order for any product variant that the BOM line references.</span></span> <span data-ttu-id="2c1d9-193">子生产、事件看板或采购订单在您估计生产订单时创建。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-193">The subproduction, event kanban, or purchase order is created when you estimate the production order.</span></span> <span data-ttu-id="2c1d9-194">将自动为消耗生产订单预留所需的物料数量。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-194">The required item quantities are automatically reserved for the consuming production order.</span></span>

### <a name="vendor"></a><span data-ttu-id="2c1d9-195">供应商</span><span class="sxs-lookup"><span data-stu-id="2c1d9-195">Vendor</span></span>

<span data-ttu-id="2c1d9-196">如果生产流程利用了某个转包商，并且您想要自动为该转包商创建子生产或采购订单，请选择**“供应商”**行类型。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-196">Select the **Vendor** line type if the production process uses a subcontractor, and you want a subproduction or purchase order to be created automatically for the subcontractor.</span></span>  

<span data-ttu-id="2c1d9-197">**有关物料清单中的转包工序的注释：**由转包商执行的服务或工作必须作为在库存中跟踪的服务项创建。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-197">**Note about subcontracted operations in a BOM:** The service or work that is performed by the subcontractor must be created as service item that is tracked in inventory.</span></span> <span data-ttu-id="2c1d9-198">您必须将服务项作为物料清单行附加到父项。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-198">You must attach the service item to the parent item as a BOM line.</span></span> <span data-ttu-id="2c1d9-199">工艺路线必须包含分配给转包商的运营资源。</span><span class="sxs-lookup"><span data-stu-id="2c1d9-199">The route must contain an operation that is assigned to the subcontractor's operations resource.</span></span>




