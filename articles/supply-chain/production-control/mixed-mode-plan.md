---
title: "混合模式计划 - 合并不同的流程和精益采购"
description: "文主题提供有关混合模式计划的信息。"
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 52931
ms.assetid: 2e8b5fd1-cee9-45da-a3ae-6961fb020b89
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 8e6a896b2a073e189b956ef189f63908f08606ed
ms.contentlocale: zh-cn
ms.lasthandoff: 08/07/2018

---

# <a name="mixed-mode-planning---combine-discrete-process-and-lean-sourcing"></a><span data-ttu-id="10fe8-103">混合模式计划 - 合并不同的流程和精益采购</span><span class="sxs-lookup"><span data-stu-id="10fe8-103">Mixed mode planning - Combine discrete, process, and lean sourcing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10fe8-104">文主题提供有关混合模式计划的信息。</span><span class="sxs-lookup"><span data-stu-id="10fe8-104">This topic provides information about mixed mode planning.</span></span> <span data-ttu-id="10fe8-105">在混合模式计划中，您可以基于物料流来模拟供应链。</span><span class="sxs-lookup"><span data-stu-id="10fe8-105">In mixed mode planning, you can model your supply chain based on the material flow.</span></span> <span data-ttu-id="10fe8-106">Microsoft Dynamics 365 for Finance and Operations 确保物料流遵循您的模型，不论您选择的是哪种供应策略（看板、生产订单、采购订单、批次订单或转移单）。</span><span class="sxs-lookup"><span data-stu-id="10fe8-106">Microsoft Dynamics 365 for Finance and Operations makes sure that the material flow follows your models, regardless of the supply policy that is selected (kanbans, production orders, purchase orders, batch orders, or transfer orders).</span></span> 

<span data-ttu-id="10fe8-107">无论产品结构如何，您都可以选择产品供应的总体策略。</span><span class="sxs-lookup"><span data-stu-id="10fe8-107">You can select your overall strategy for supplying a product, regardless of the product structure.</span></span>  

<span data-ttu-id="10fe8-108">例如，您可以在装配中实施看板控制，以便按生产订单、看板、转移、批次订单或适合供应链特性的任意组合来为装配区域采购物料，但您仍具有对多个供应的完全可见性。</span><span class="sxs-lookup"><span data-stu-id="10fe8-108">For example, you can have kanban control in the assembly, where materials are sourced for the assembly area by production orders, kanbans, transfers, batch orders, or any combination that is appropriate for the characteristics of your supply chain, but you can still have full visibility across supplies.</span></span> <span data-ttu-id="10fe8-109">此能力可实现优化的供应链流程并提高对供应链的可见性。</span><span class="sxs-lookup"><span data-stu-id="10fe8-109">This capability leads to optimized supply chain processes and enhanced visibility into your supply chain.</span></span>  

<span data-ttu-id="10fe8-110">主计划编制中使用的供应策略的粒度取决于作为覆盖范围维度启用的存储维度。</span><span class="sxs-lookup"><span data-stu-id="10fe8-110">The granularity of the supply policies that are used in master scheduling depends on the storage dimensions that are enabled as coverage dimensions.</span></span> <span data-ttu-id="10fe8-111">要启用主计划编制以控制不同类型的位置的补货和供应（例如，通过分离不同的生产单位的生产车间，或通过分离不同类型的物料和成品仓库），建议您将站点和仓库启用为覆盖范围维度。</span><span class="sxs-lookup"><span data-stu-id="10fe8-111">To enable master scheduling to control the replenishment and supply of different types of locations (for example, by separating the production floor for different production units, or by separating different types of material and finished goods warehouses), we recommend that you enable Site and Warehouse as coverage dimensions.</span></span> <span data-ttu-id="10fe8-112">或者，可以将仓库作为覆盖范围维度忽略。</span><span class="sxs-lookup"><span data-stu-id="10fe8-112">Alternatively, Warehouse can be omitted as a coverage dimension.</span></span> <span data-ttu-id="10fe8-113">在此情况下，当您使用高级仓库管理时，仓库内的所有转移将由仓库工作控制，而仓库间的所有转移可由取料看板控制。</span><span class="sxs-lookup"><span data-stu-id="10fe8-113">In that case, when you use advanced warehouse management, all movements inside a warehouse are controlled by warehouse work, whereas all movements across warehouses can be controlled by withdrawal kanbans.</span></span>

## <a name="supply-policies"></a><span data-ttu-id="10fe8-114">供应策略</span><span class="sxs-lookup"><span data-stu-id="10fe8-114">Supply policies</span></span>
<span data-ttu-id="10fe8-115">Finance and Operations 混合模式计划可控制产品的供应方式（基于供应）以及针对派生的需求（物料清单 \[BOM\] 中的物料消耗量）的发货方式。</span><span class="sxs-lookup"><span data-stu-id="10fe8-115">Finance and Operations mixed mode planning controls how a product is supplied and, based on the supply, how derived requirements (consumption of items from a bill of materials \[BOM\]) are issued.</span></span> <span data-ttu-id="10fe8-116">系统将基于订单类型自动采购物料以满足需求。</span><span class="sxs-lookup"><span data-stu-id="10fe8-116">Based on the order type, the system automatically sources materials to match the requirements.</span></span>  

<span data-ttu-id="10fe8-117">可在产品级别或以任何支持需求的粒度定义供应策略。</span><span class="sxs-lookup"><span data-stu-id="10fe8-117">Supply policies can be defined at the product level or at any granularity that supports your requirements.</span></span> <span data-ttu-id="10fe8-118">您在 **“默认订单设置”** 页面上定义供应策略的粒度。</span><span class="sxs-lookup"><span data-stu-id="10fe8-118">You define the granularity of supply policies on the **Default order settings** page.</span></span>  

<span data-ttu-id="10fe8-119">供应策略可按产品、物料维度（配置、颜色和大小）、站点和仓库控制。</span><span class="sxs-lookup"><span data-stu-id="10fe8-119">Supply policies can be controlled by product, item dimensions (configuration, color, and size), site, and warehouse.</span></span> <span data-ttu-id="10fe8-120">在 **“物料覆盖范围”** 页面上进行此设置。</span><span class="sxs-lookup"><span data-stu-id="10fe8-120">This setup is done on the **Item coverage** page.</span></span>  

<span data-ttu-id="10fe8-121">默认订单类型控制主计划生成的订单。</span><span class="sxs-lookup"><span data-stu-id="10fe8-121">The default order type controls what order master planning generates.</span></span>  

<span data-ttu-id="10fe8-122">不管供应链的建模方式如何，Finance and Operations 都支持供应策略的组合。</span><span class="sxs-lookup"><span data-stu-id="10fe8-122">Regardless of how the supply chain is modeled, Finance and Operations supports your mix of supply policies.</span></span> <span data-ttu-id="10fe8-123">您可以具有从看板采购的生产订单。</span><span class="sxs-lookup"><span data-stu-id="10fe8-123">You can have production orders that are sourced from kanbans.</span></span> <span data-ttu-id="10fe8-124">或者，您可以具有需要按转移或看板供应的产品的批次订单。</span><span class="sxs-lookup"><span data-stu-id="10fe8-124">Alternatively, you can have a batch order that requires a product that is supplied by transfers or by kanbans.</span></span>  

<span data-ttu-id="10fe8-125">Finance and Operations 确保物料流遵循该模型。</span><span class="sxs-lookup"><span data-stu-id="10fe8-125">Finance and Operations makes sure that the material flow follows the model.</span></span>  

<span data-ttu-id="10fe8-126">在定义供应策略后，将在运行时动态分配物料领取仓库。</span><span class="sxs-lookup"><span data-stu-id="10fe8-126">The warehouse for picking material is assigned dynamically at run time, after the supply policy has been defined.</span></span>  

<span data-ttu-id="10fe8-127">通常，不会为将来日期创建看板，因为看板的生命周期短。</span><span class="sxs-lookup"><span data-stu-id="10fe8-127">Typically, kanbans aren't created for future dates, because a kanban has a short life cycle.</span></span> <span data-ttu-id="10fe8-128">要保持对供应链的完全可见性，我们已引入“计划看板”这个新的计划概念，用于计算派生的需求并帮助确保基于在创建实际看板时使用的相同逻辑来满足需求。</span><span class="sxs-lookup"><span data-stu-id="10fe8-128">To maintain full visibility into the supply chain, we have introduced the new planning concept of a “planned kanban,” which is used to calculate derived requirements and helps guarantee that the requirements are sourced based on the same logic that is used when the actual kanban is created.</span></span>  

<span data-ttu-id="10fe8-129">为所有其他供应策略类型提供了相同的逻辑。</span><span class="sxs-lookup"><span data-stu-id="10fe8-129">The same logic is present for all other supply policy types.</span></span> <span data-ttu-id="10fe8-130">因此，在批准生产和供应后，将基于应与实际订单一起运行的相同逻辑进行长期物料计划。</span><span class="sxs-lookup"><span data-stu-id="10fe8-130">Therefore, long-term materials planning is based on the same logic that you expect to run with the actual orders after production and supply are approved.</span></span>

## <a name="materials-allocation-cross-supply-policy--resource-consumption-on-boms"></a><span data-ttu-id="10fe8-131">跨供应策略的物料分配 - 物料清单中的资源消耗量</span><span class="sxs-lookup"><span data-stu-id="10fe8-131">Materials allocation cross-supply policy – Resource consumption on BOMs</span></span>
<span data-ttu-id="10fe8-132">资源消耗量是一项重要功能。</span><span class="sxs-lookup"><span data-stu-id="10fe8-132">Resource consumption is an important functionality.</span></span> <span data-ttu-id="10fe8-133">利用资源消耗量，可基于供应策略（订单类型）动态选择物料领取仓库，并可更轻松地维护基础数据。</span><span class="sxs-lookup"><span data-stu-id="10fe8-133">Resource consumption enables a warehouse for picking materials to be selected dynamically, based on the supply policy (order type), and also makes maintenance of base data easier.</span></span>  

<span data-ttu-id="10fe8-134">资源消耗量要求基于产品的供应方式分配物料领取仓库。</span><span class="sxs-lookup"><span data-stu-id="10fe8-134">Resource consumption requires that the warehouse that materials are picked from be assigned based on the way that the product is supplied.</span></span> <span data-ttu-id="10fe8-135">换句话说，在运行时，系统将查找应用于制造的资源。</span><span class="sxs-lookup"><span data-stu-id="10fe8-135">In other words, at run time, the system finds the resources that should be used for manufacturing.</span></span> <span data-ttu-id="10fe8-136">随后，系统将基于这些资源查找领料仓库。</span><span class="sxs-lookup"><span data-stu-id="10fe8-136">Based on those resources, the system then finds the picking warehouse.</span></span>  

<span data-ttu-id="10fe8-137">对于与供应策略无关的工作，如果供应发生更改，您无需更改物料清单上的信息。</span><span class="sxs-lookup"><span data-stu-id="10fe8-137">For work that is independent of a supply policy, you don't have to change information on the BOM if the supply is changed.</span></span> <span data-ttu-id="10fe8-138">对于临时更改，Finance and Operations 可确保从正确的仓库领取物料。</span><span class="sxs-lookup"><span data-stu-id="10fe8-138">For ad-hoc changes, Finance and Operations makes sure that materials are sourced from the right warehouse.</span></span>

## <a name="process-manufacturing--the-production-type"></a><span data-ttu-id="10fe8-139">流程制造 – 生产类型</span><span class="sxs-lookup"><span data-stu-id="10fe8-139">Process manufacturing – The production type</span></span>
<span data-ttu-id="10fe8-140">对于混合模式中的完整灵活性，建议您对所有产品使用生产类型 BOM。</span><span class="sxs-lookup"><span data-stu-id="10fe8-140">For full flexibility in mixed mode, we recommend that you use production type BOMs for all products.</span></span> <span data-ttu-id="10fe8-141">随后，您可以使用生产订单、看板、转移单或采购订单来供应产品。</span><span class="sxs-lookup"><span data-stu-id="10fe8-141">You can then use production orders, kanbans, transfer orders, or purchase orders to supply a product.</span></span> <span data-ttu-id="10fe8-142">对于流程制造，您必须使用以下生产类型：**“配方”**、**“联产品”**、**“副产品”** 或 **“计划物料”**。</span><span class="sxs-lookup"><span data-stu-id="10fe8-142">For process manufacturing, you must use a production type of **Formula**, **Co-product**, **By-product**, or **Planning item**.</span></span> <span data-ttu-id="10fe8-143">看板和生产订单不能用于这些生产类型。</span><span class="sxs-lookup"><span data-stu-id="10fe8-143">Kanbans and production orders can't be used for these production types.</span></span>




