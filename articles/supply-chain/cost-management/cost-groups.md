---
title: 成本组
description: 在对制造物料的计算成本中的成本份额（例如针对材料、人工和开销的成本份额）进行细分和分析时，可将成本组作为基础。 成本组细分在制造环境中有若干同义词，例如成本细分、成本分解或成本分类。
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCostGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dee8e40de43480cd010b5acc41a3d87611c2ab6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423141"
---
# <a name="cost-groups"></a><span data-ttu-id="5d9ec-104">成本组</span><span class="sxs-lookup"><span data-stu-id="5d9ec-104">Cost groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d9ec-105">在对制造物料的计算成本中的成本份额（例如针对材料、人工和开销的成本份额）进行细分和分析时，可将成本组作为基础。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-105">Cost groups provide the basis for segmenting and analyzing cost contributions in a manufactured item’s calculated cost, such as the cost contributions for material, labor, and overhead.</span></span> <span data-ttu-id="5d9ec-106">成本组细分在制造环境中有若干同义词，例如成本细分、成本分解或成本分类。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-106">Cost group segmentation has several synonyms within manufacturing environments, such as cost breakdown, cost decomposition, or cost classification.</span></span> 

<span data-ttu-id="5d9ec-107">成本组细分在制造环境中有若干同义词，例如成本细分、成本分解或成本分类。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-107">Cost group segmentation has several synonyms within manufacturing environments, such as cost breakdown, cost decomposition, or cost classification.</span></span> <span data-ttu-id="5d9ec-108">成本组细分可用于若干目的。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-108">Cost group segmentation can serve several purposes.</span></span> <span data-ttu-id="5d9ec-109">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="5d9ec-109">Here are some examples:</span></span>

-   <span data-ttu-id="5d9ec-110">可以基于分配给物料的成本组，为不同类型的材料（例如罐装货物产品的成分和包装）对成本进行细分。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-110">It can segment costs for different types of material, such as ingredients and packaging material for a canned goods product, based on the cost groups that are assigned to items.</span></span>
-   <span data-ttu-id="5d9ec-111">可以基于分配给与运营资源和工艺路线工序相关的成本类别的成本组，针对不同类型的运营资源（如不同的人工或机器类型），对成本进行细分。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-111">It can segment costs for different types of operations resources, such as different types of labor or machines, based on the cost groups that are assigned to cost categories that are related to operations resources and routing operations.</span></span>
-   <span data-ttu-id="5d9ec-112">可以基于分配给与工艺路线工序相关的成本类别的成本组，为工艺路线工序中的设置时间和运行时间对成本进行细分。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-112">It can segment costs for setup time and run time in routing operations, based on the cost groups that are assigned to cost categories that are related to the routing operations.</span></span>
-   <span data-ttu-id="5d9ec-113">可以基于分配给成本计算单设置中的间接成本的成本组，为不同类型的开销（例如与人工相关的开销和与机器相关的开销）对成本进行细分。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-113">It can segment costs for different types of overhead, such as labor-related and machine-related overhead, based on cost groups that are assigned to indirect costs in the costing sheet setup.</span></span>
-   <span data-ttu-id="5d9ec-114">可以在成本计算单设置中作为计算各种制造开销类型的基础。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-114">It can act as the basis for calculating various types of manufacturing overhead in the costing sheet setup.</span></span> <span data-ttu-id="5d9ec-115">此开销可以包括与有关运营资源或有关设置时间和运行时间的工艺路线信息相关的不同开销类型。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-115">This overhead can include different types of overhead that are related to routing information about operations resources, or information about setup time and run time.</span></span> <span data-ttu-id="5d9ec-116">制造开销还可与组件材料的成本份额相关，从而反映无需工艺路线信息的精益制造理念。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-116">Manufacturing overhead can also be related to cost contributions of component material, reflecting a lean manufacturing philosophy that eliminates the need for routing information.</span></span>

<span data-ttu-id="5d9ec-117">成本组细分应用于制造物料的计算成本，无论该成本是基于标准成本还是计划成本。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-117">Cost group segmentation applies to a manufactured item’s calculated cost, regardless of whether that cost was based on standard costs or planned costs.</span></span> <span data-ttu-id="5d9ec-118">**汇总** 页按成本组、级别或按成本组和级别显示此细分。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-118">The **Summary** page displays this segmentation by cost group, by level, or by both cost group and level.</span></span> 

<span data-ttu-id="5d9ec-119">在产品结构中的多个级别上保留成本组细分的能力也称为 *分解*。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-119">The ability to retain cost group segmentation across multiple levels in a product structure is known as *splitting*.</span></span> <span data-ttu-id="5d9ec-120">分解仅适用于使用标准成本库存模型的制造物料。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-120">Splitting applies only to manufactured items that use a standard cost inventory model.</span></span> <span data-ttu-id="5d9ec-121">如果不使用分解，则制造组件的成本被视作材料成本份额。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-121">If splitting isn't used, the cost of a manufactured component is treated as a material cost contribution.</span></span> <span data-ttu-id="5d9ec-122">按子分类细分的成本的库存参数指示成本组细分将在标准成本计算中的多个级别上被保留。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-122">The inventory parameter for cost breakdown by subledger indicates that cost group segmentation will be retained across multiple levels in standard cost calculations.</span></span> <span data-ttu-id="5d9ec-123">相反，如果策略无级别，成本组细分只应用于单级别计算。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-123">By contrast, if a policy has no levels, cost group segmentation applies only to a single-level calculation.</span></span> <span data-ttu-id="5d9ec-124">例如，**按成本组的成本累积** 页显示标准成本物料的多个级别上的成本组细分。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-124">For example, the **Cost rollup by cost group** page displays the cost group segmentation across multiple levels for standard cost items.</span></span> 

<span data-ttu-id="5d9ec-125">成本组细分还可以应用于标准成本物料差异上。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-125">Cost group segmentation can also apply to variances for a standard cost item.</span></span> <span data-ttu-id="5d9ec-126">第二个库存参数定义了差异将按成本组被标识或仅被汇总。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-126">A second inventory parameter defines whether variances are identified by cost group or just summarized.</span></span> 

<span data-ttu-id="5d9ec-127">可以出于补充细分目的，向成本组分配某一成本组类型和行为。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-127">A cost group can be assigned a cost group type and a behavior for supplemental segmentation purposes.</span></span>

-   <span data-ttu-id="5d9ec-128">**成本组类型** − 每个成本组都必须分配有一个成本组类型，以指示成本组适用于直接材料、直接制造或直接外包，或将其指定为间接或未定义。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-128">**Cost group type** − Each cost group must be assigned a cost group type to indicate that the cost group applies to direct material, direct manufacturing, or direct outsourcing, or to designate it as indirect or undefined.</span></span> <span data-ttu-id="5d9ec-129">指定为直接材料的成本组可分配给物料。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-129">A cost group that is designated as direct material can be assigned to items.</span></span> <span data-ttu-id="5d9ec-130">直接制造成本组可分配给各成本类别。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-130">A direct manufacturing cost group can be assigned to cost categories.</span></span> <span data-ttu-id="5d9ec-131">直接业务外包成本组可分配给服务的产品类型，以便您可以对与服务采购到转包活动相关的成本进行分类。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-131">A direct outsourcing cost group can be assigned to a product type of service, so that you can classify costs that are associated with the service purchase to subcontracting activities.</span></span> <span data-ttu-id="5d9ec-132">间接成本组可分配给间接成本以用于附加费和费率。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-132">An indirect cost group can be assigned to indirect costs for surcharges or rates.</span></span> <span data-ttu-id="5d9ec-133">指定为未定义的成本组可分配给物料、各成本类别或间接成本。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-133">A cost group that is designated as undefined can be assigned to items, cost categories, or indirect costs.</span></span> <span data-ttu-id="5d9ec-134">成本组类型的分配出于若干目的。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-134">The assignment of a cost group type serves several purposes.</span></span> <span data-ttu-id="5d9ec-135">首先，它限制分配成本组和查看适用的成本组的列表的能力。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-135">First, it constrains the ability to assign a cost group and to view a list of applicable cost groups.</span></span> <span data-ttu-id="5d9ec-136">其次，它为报告目的提供补充细分。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-136">Second, it provides supplemental segmentation for reporting purposes.</span></span> <span data-ttu-id="5d9ec-137">第三，它可用于为差异分配会计科目。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-137">Third, it can be used to assign ledger accounts for variances.</span></span>
-   <span data-ttu-id="5d9ec-138">**行为** − 每个成本组都可以选择分配有某一行为，以指示该成本组适用于固定成本或可变成本。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-138">**Behavior** − Each cost group can optionally be assigned a behavior to indicate that the cost group applies to fixed costs or variable costs.</span></span> <span data-ttu-id="5d9ec-139">行为是空值的成本组被视为可变成本。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-139">A cost group that has a null value for behavior is treated as a variable cost.</span></span> <span data-ttu-id="5d9ec-140">行为的分配只出于报告目的。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-140">The assignment of a behavior serves only a reporting purpose.</span></span> <span data-ttu-id="5d9ec-141">例如，成本可以在成本计算单上和 **按成本组的成本累积** 页中随固定成本和可变成本的细分显示。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-141">For example, costs can be displayed with segmentation of fixed and variable costs on the costing sheet and on the **Cost rollup by cost group** page.</span></span> <span data-ttu-id="5d9ec-142">如果您将利润设置百分比分配到每个成本组，物料清单 (BOM) 计算将提供基于成本加上加价方法的建议销售价。</span><span class="sxs-lookup"><span data-stu-id="5d9ec-142">If you assign a profit setting percentage to each cost group, the bill of materials (BOM) calculation provides a suggested sales price, based on a cost-plus-markup approach.</span></span>




