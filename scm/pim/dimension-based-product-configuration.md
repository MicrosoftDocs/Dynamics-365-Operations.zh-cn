---
title: "基于维度的产品配置"
description: "基于维度的产品配置表示从单个基础产品和物料清单创建多个产品变型的简单解决方案。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 89f01401f1d937a72ae7e59b784cf034b48aaf1f
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="16ab2-103">基于维度的产品配置</span><span class="sxs-lookup"><span data-stu-id="16ab2-103">Dimension-based product configuration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="16ab2-104">基于维度的产品配置表示从单个基础产品和物料清单创建多个产品变型的简单解决方案。</span><span class="sxs-lookup"><span data-stu-id="16ab2-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="16ab2-105">基于维度的产品配置是三项内置产品配置技术之一。</span><span class="sxs-lookup"><span data-stu-id="16ab2-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="16ab2-106">其他两项技术是预定义的变型和基于约束的配置。</span><span class="sxs-lookup"><span data-stu-id="16ab2-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="16ab2-107">全部三项技术使用基础产品作为起点，并允许用户为一个基础产品创建许多产品变型。</span><span class="sxs-lookup"><span data-stu-id="16ab2-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="16ab2-108">重要概念</span><span class="sxs-lookup"><span data-stu-id="16ab2-108">Key concepts</span></span>
<span data-ttu-id="16ab2-109">基于维度的产品配置基于以下重要概念：</span><span class="sxs-lookup"><span data-stu-id="16ab2-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="16ab2-110">基础产品</span><span class="sxs-lookup"><span data-stu-id="16ab2-110">Product masters</span></span>
-   <span data-ttu-id="16ab2-111">配置产品维度</span><span class="sxs-lookup"><span data-stu-id="16ab2-111">Configuration product dimension</span></span>
-   <span data-ttu-id="16ab2-112">配置组</span><span class="sxs-lookup"><span data-stu-id="16ab2-112">Configuration groups</span></span>
-   <span data-ttu-id="16ab2-113">物料清单 (BOM)</span><span class="sxs-lookup"><span data-stu-id="16ab2-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="16ab2-114">配置流程</span><span class="sxs-lookup"><span data-stu-id="16ab2-114">Configuration route</span></span>
-   <span data-ttu-id="16ab2-115">配置规则</span><span class="sxs-lookup"><span data-stu-id="16ab2-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="16ab2-116">基础产品</span><span class="sxs-lookup"><span data-stu-id="16ab2-116">Product masters</span></span>

<span data-ttu-id="16ab2-117">基础产品是所有产品配置流程的起点。</span><span class="sxs-lookup"><span data-stu-id="16ab2-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="16ab2-118">对于基于维度的产品配置，您需要具有此特定配置技术的基础产品和包括配置产品维度的产品维度组。</span><span class="sxs-lookup"><span data-stu-id="16ab2-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="16ab2-119">配置产品维度</span><span class="sxs-lookup"><span data-stu-id="16ab2-119">Configuration product dimension</span></span>

<span data-ttu-id="16ab2-120">配置产品维度用于确定具有基于维度的配置技术的基础产品的产品变型。</span><span class="sxs-lookup"><span data-stu-id="16ab2-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="16ab2-121">配置维度值由用户输入，应帮助确定各个产品变型。</span><span class="sxs-lookup"><span data-stu-id="16ab2-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="16ab2-122">配置组</span><span class="sxs-lookup"><span data-stu-id="16ab2-122">Configuration groups</span></span>

<span data-ttu-id="16ab2-123">配置组在中央存储库定义，并且可以用于所有基于维度的产品配置模型。</span><span class="sxs-lookup"><span data-stu-id="16ab2-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="16ab2-124">配置组与各个物料清单行关联，并包含一组相互排斥的行。</span><span class="sxs-lookup"><span data-stu-id="16ab2-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="16ab2-125">这意味着只能为单个产品变型选择组中的一个行。</span><span class="sxs-lookup"><span data-stu-id="16ab2-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="16ab2-126">物料清单 (BOM)</span><span class="sxs-lookup"><span data-stu-id="16ab2-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="16ab2-127">物料清单表示基于维度的产品配置的构建基块。</span><span class="sxs-lookup"><span data-stu-id="16ab2-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="16ab2-128">它必须包括可用于所有产品变型的所有不同的产品。</span><span class="sxs-lookup"><span data-stu-id="16ab2-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="16ab2-129">物料清单中的每一行均可以引用配置组。</span><span class="sxs-lookup"><span data-stu-id="16ab2-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="16ab2-130">如果行不引用配置组，它将包括在所有产品变型中。</span><span class="sxs-lookup"><span data-stu-id="16ab2-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="16ab2-131">配置流程</span><span class="sxs-lookup"><span data-stu-id="16ab2-131">Configuration route</span></span>

<span data-ttu-id="16ab2-132">因为配置组将在产品配置流程中显示给用户，配置流程确定配置组的顺序。</span><span class="sxs-lookup"><span data-stu-id="16ab2-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="16ab2-133">配置规则</span><span class="sxs-lookup"><span data-stu-id="16ab2-133">Configuration rules</span></span>

<span data-ttu-id="16ab2-134">配置规则表示，确保包括在物料清单的一个配置组中的产品在同一物料清单的不同配置组中强制包含或排除某一产品的机制。</span><span class="sxs-lookup"><span data-stu-id="16ab2-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="16ab2-135">产品建模流程</span><span class="sxs-lookup"><span data-stu-id="16ab2-135">Product modeling process</span></span>
<span data-ttu-id="16ab2-136">为基于维度的产品构建产品模型的自然顺序从定义相关配置组开始。</span><span class="sxs-lookup"><span data-stu-id="16ab2-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="16ab2-137">请务必确保物料清单中使用的所有产品已发布到已为其构建产品模型的公司。</span><span class="sxs-lookup"><span data-stu-id="16ab2-137">It is important to ensure that all products which will be used in the BOM have been relased to the company that the product model is built for.</span></span> <span data-ttu-id="16ab2-138">这些构建基块在位后，用户可以创建物料清单并将配置组分配到所有相关物料清单行。</span><span class="sxs-lookup"><span data-stu-id="16ab2-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="16ab2-139">在物料清单完成后，配置流程可为在适当序列中订购配置组定义。</span><span class="sxs-lookup"><span data-stu-id="16ab2-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="16ab2-140">\[caption id="attachment\_282671" align="alignnone" width="1187"\][![基于维度的产品建模流程](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) 基于维度的产品建模流程\[/caption\] 如果存在来自必须或禁止一起使用的不同配置组的某些产品，您可以创建将强制这些产品关系的配置规则。</span><span class="sxs-lookup"><span data-stu-id="16ab2-140">\[caption id="attachment\_282671" align="alignnone" width="1187"\][![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimension-based product modeling process\[/caption\] If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="16ab2-141">在物料清单通过物料清单版本与基于维度的基础产品关联，并且二者均已审核和激活后，您可以创建产品配置并为每个配置输入一个名称。</span><span class="sxs-lookup"><span data-stu-id="16ab2-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="16ab2-142">配置可以在所有交易记录生成前定义，或者可以在某些配置需求发生前进行。</span><span class="sxs-lookup"><span data-stu-id="16ab2-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="16ab2-143">建议的使用</span><span class="sxs-lookup"><span data-stu-id="16ab2-143">Suggested use</span></span>

<span data-ttu-id="16ab2-144">基于维度配置的技术最适合用于具有有限可变性的产品，标准产品维度尺寸、颜色、样式和配置的组合不适合确定特定的产品变型。</span><span class="sxs-lookup"><span data-stu-id="16ab2-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="16ab2-145">示例可以是具有框架高度、车轮大小、闸类型和不同齿轮的自行车。</span><span class="sxs-lookup"><span data-stu-id="16ab2-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>




