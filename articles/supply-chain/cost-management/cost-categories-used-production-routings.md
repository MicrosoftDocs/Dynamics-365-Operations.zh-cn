---
title: "在生产工艺路线中使用的成本类别"
description: "本文提供有关应用于使用工艺路线的制造环境的成本类别的信息。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory, RouteCostCategoryPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 78153
ms.assetid: a3fdc76c-0a27-4723-b1c7-4322f707d89e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1bda8d9d656f1760061599d100ca4af9186742ea
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="cost-categories-used-in-production-routing"></a><span data-ttu-id="e445d-103">在生产工艺路线中使用的成本类别</span><span class="sxs-lookup"><span data-stu-id="e445d-103">Cost categories used in production routing</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e445d-104">本文提供有关应用于使用工艺路线的制造环境的成本类别的信息。</span><span class="sxs-lookup"><span data-stu-id="e445d-104">This article provides information about cost categories that apply to manufacturing environments that use routing.</span></span>

<span data-ttu-id="e445d-105">成本类别应用于使用工艺路线的制造环境。</span><span class="sxs-lookup"><span data-stu-id="e445d-105">Cost categories apply to manufacturing environments that use routing.</span></span> <span data-ttu-id="e445d-106">将成本类别分配给运营资源和工艺路线工序，以便用于在制造物料的计算成本中定义每小时成本和对成本份额进行细分。</span><span class="sxs-lookup"><span data-stu-id="e445d-106">They are assigned to operations resources and routing operations to define hourly costs and to segment cost contributions in a manufactured item’s calculated costs.</span></span> <span data-ttu-id="e445d-107">分配给成本类别的成本组基于运营资源和活动类型（例如设置时间和运行时间）划分制造成本份额。</span><span class="sxs-lookup"><span data-stu-id="e445d-107">The cost groups that are assigned to cost categories classify manufacturing cost contributions, based on the operation resources and the type of activity, such as setup time and run time.</span></span> <span data-ttu-id="e445d-108">成本组分配的特性基于工艺路线信息启用要计算的制造开销。</span><span class="sxs-lookup"><span data-stu-id="e445d-108">The specificity of cost group assignments enables manufacturing overhead to be calculated based on routing information.</span></span> 

<span data-ttu-id="e445d-109">**注意：**在制造环境内成本类别具有若干同义词，例如人工费率代码或机器费率代码。</span><span class="sxs-lookup"><span data-stu-id="e445d-109">**Note:** In manufacturing environments, cost categories are known by several other names, such as labor rate codes or machine rate codes.</span></span> 

<span data-ttu-id="e445d-110">每个成本类别都有自己的关联成本记录和分配的成本组。</span><span class="sxs-lookup"><span data-stu-id="e445d-110">Each cost category has associated cost records and an assigned cost group.</span></span> <span data-ttu-id="e445d-111">需要使用不同的成本类别来用于不同的生产目的。</span><span class="sxs-lookup"><span data-stu-id="e445d-111">Different cost categories are required for different production purposes.</span></span>

-   <span data-ttu-id="e445d-112">根据运营资源分配不同的小时成本。</span><span class="sxs-lookup"><span data-stu-id="e445d-112">Assign different hourly costs, depending on the operations resource.</span></span> <span data-ttu-id="e445d-113">例如，成本可以因人工技能、机器或制造单元的不同类型而有所不同。</span><span class="sxs-lookup"><span data-stu-id="e445d-113">For example, the costs can differ for various types of labor skills, machines, or manufacturing cells.</span></span>
-   <span data-ttu-id="e445d-114">为与某一工艺路线工序相关联的设置时间或运行时间分配不同的每小时成本。</span><span class="sxs-lookup"><span data-stu-id="e445d-114">Assign different hourly costs for the setup time or run time that is associated with a routing operation.</span></span>
-   <span data-ttu-id="e445d-115">基于输出数量而非每小时成本分配运营资源成本，例如支付人工费用的计件费率。</span><span class="sxs-lookup"><span data-stu-id="e445d-115">Assign operations resource costs based on the output quantity instead of hourly costs, such as the piece rates for paying labor.</span></span>
-   <span data-ttu-id="e445d-116">为制造物料的计算的成本提供成本份额的成本组细分。</span><span class="sxs-lookup"><span data-stu-id="e445d-116">Provide cost group segmentation of cost contributions to a manufactured item’s calculated cost.</span></span> <span data-ttu-id="e445d-117">例如，您可以细分人工和机器成本。</span><span class="sxs-lookup"><span data-stu-id="e445d-117">For example, you can segment of labor and machine costs.</span></span>
-   <span data-ttu-id="e445d-118">为开销计算公式提供成本组基础，例如与人工相关的开销和与机器相关的开销或者与设置时间和运行时间相关的开销的公式。</span><span class="sxs-lookup"><span data-stu-id="e445d-118">Provide the cost group basis for overhead calculation formulas, such as formulas for labor-related and machine-related overhead, or overhead that is related to setup and run time.</span></span>

<span data-ttu-id="e445d-119">可以将某一成本类别分配给用于工艺路线工序的设置时间、处理时间和数量。</span><span class="sxs-lookup"><span data-stu-id="e445d-119">A cost category can be assigned to the setup time, the process time, and the quantity for a routing operation.</span></span> <span data-ttu-id="e445d-120">例如，当成本或成本组细分在设置时间和处理时间之间不同时，应定义不同的成本类别并将这些类别分配给设置时间和处理时间。</span><span class="sxs-lookup"><span data-stu-id="e445d-120">When, for example, costs or cost group segmentation differs between the setup time and the process time, different cost categories should be defined and assigned to the setup time and the process time.</span></span> <span data-ttu-id="e445d-121">选择使用哪一成本类别来用于设置时间、处理时间和数量将由分配给某一工序的工艺路线组确定。</span><span class="sxs-lookup"><span data-stu-id="e445d-121">The selective use of cost categories for setup time, process time, and quantity is determined by the route group that is assigned to an operation.</span></span> <span data-ttu-id="e445d-122">可以由在**生产控制参数**页定义的公司范围的策略规定如何向时间和数量分配成本类别。</span><span class="sxs-lookup"><span data-stu-id="e445d-122">The assignment of cost categories to time and quantity can be mandated by company-wide policies that are defined on the **Production control parameters** page.</span></span> 

<span data-ttu-id="e445d-123">每个成本类别都具有关联成本，这些关联成本基于某一成本计算版本内的成本记录的定义。</span><span class="sxs-lookup"><span data-stu-id="e445d-123">Each cost category has associated costs that are based on the definition of cost records in a costing version.</span></span> <span data-ttu-id="e445d-124">使用**成本类别价格**页可以针对指定的成本计算版本和站点定义成本记录。</span><span class="sxs-lookup"><span data-stu-id="e445d-124">Use the **Cost category price** page to define the cost records for a specified costing version and site.</span></span> <span data-ttu-id="e445d-125">当某一成本类别的成本记录在最初输入时，其具有**未决**状态和预期生效日期。</span><span class="sxs-lookup"><span data-stu-id="e445d-125">When the cost record for a cost category is first entered, it has a status of **Pending** and an intended effective date.</span></span> <span data-ttu-id="e445d-126">当您激活成本记录时，状态将更新为**当前有效**，生效日期将更新为激活日期。</span><span class="sxs-lookup"><span data-stu-id="e445d-126">When you activate the cost record, the status is updated to **Current active**, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="e445d-127">不同的成本记录可能反应不同站点、生效日期或状态。</span><span class="sxs-lookup"><span data-stu-id="e445d-127">Different cost records might reflect different sites, effective dates, or statuses.</span></span> <span data-ttu-id="e445d-128">将来或历史日期的物料清单 (BOM) 计算使用具有相关生效日期的成本记录。</span><span class="sxs-lookup"><span data-stu-id="e445d-128">Bills of materials (BOM) calculations for a future or historical date use cost records that have the relevant effective date.</span></span> <span data-ttu-id="e445d-129">当前有效成本记录将用于评估生产订单成本并针对生产订单确定报告的时间。</span><span class="sxs-lookup"><span data-stu-id="e445d-129">The current active cost record will be used to estimate production order costs and to value reported time against a production order.</span></span> 

<span data-ttu-id="e445d-130">成本类别的成本记录可以是特定站点或公司范围。</span><span class="sxs-lookup"><span data-stu-id="e445d-130">The cost record for a cost category can be site-specific or company-wide.</span></span> <span data-ttu-id="e445d-131">若要使成本记录是站点特定的，将一个站点分配给该成本记录。</span><span class="sxs-lookup"><span data-stu-id="e445d-131">To make a cost record site-specific, assign a site to it.</span></span> <span data-ttu-id="e445d-132">否则，空值指示该成本记录应用于该公司内的所有站点。</span><span class="sxs-lookup"><span data-stu-id="e445d-132">Otherwise, a blank value indicates that the cost record applies to all sites in the company.</span></span> <span data-ttu-id="e445d-133">例如，由于成本在不同站点之间可能不同，因此，成本记录必须定义为特定于站点的。</span><span class="sxs-lookup"><span data-stu-id="e445d-133">Because costs can differ between sites, for example, the cost records must be defined as site-specific.</span></span> 

<span data-ttu-id="e445d-134">某一工艺路线工序通常继承分配给该运营资源或主工序的成本类别。</span><span class="sxs-lookup"><span data-stu-id="e445d-134">A routing operation generally inherits the cost categories that are assigned to the operations resource or master operation.</span></span> <span data-ttu-id="e445d-135">在创建某一生产订单时，该生产工艺路线内的工艺路线工序将反映所选工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="e445d-135">When a production order is created, the routing operations in the production route reflect the selected route version.</span></span> <span data-ttu-id="e445d-136">您可以覆盖分配给生产工艺路线内的工序的成本类别。</span><span class="sxs-lookup"><span data-stu-id="e445d-136">You can override the cost categories that are assigned to the operations in the production route.</span></span> 

<span data-ttu-id="e445d-137">某些生产工作类型可以应用于项目时间评估和报告。</span><span class="sxs-lookup"><span data-stu-id="e445d-137">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="e445d-138">在这种情况下，成本类别需要用于生产和项目目的。</span><span class="sxs-lookup"><span data-stu-id="e445d-138">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="e445d-139">在将某一成本类别标记为用于项目时，必须定义附加的与项目相关的信息。</span><span class="sxs-lookup"><span data-stu-id="e445d-139">You must define additional project-related information when a cost category is flagged for use in projects.</span></span>




