---
title: 成本计算版本概览
description: 本文提供有关成本计算版本、如何维护它们以及可在其中包括的数据类型的信息。 成本计算版本主要用于包含与物料、成本类别和间接成本计算公式有关的成本记录。
author: AndersGirke
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 54532
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25d3abf177c1e420d1c97dc74891e1ac0d2c2546
ms.sourcegitcommit: e286572ce94a9442a5b3076c3ff5b429be0ed512
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2019
ms.locfileid: "1865512"
---
# <a name="costing-versions-overview"></a><span data-ttu-id="592b1-104">成本计算版本概览</span><span class="sxs-lookup"><span data-stu-id="592b1-104">Costing versions overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="592b1-105">本文提供有关成本计算版本、如何维护它们以及可在其中包括的数据类型的信息。</span><span class="sxs-lookup"><span data-stu-id="592b1-105">This article provides information about costing versions, how to maintain them, and the types of data that you can include in them.</span></span> <span data-ttu-id="592b1-106">成本计算版本主要用于包含与物料、成本类别和间接成本计算公式有关的成本记录。</span><span class="sxs-lookup"><span data-stu-id="592b1-106">The primary purpose of a costing version is to contain cost records about items, cost categories, and calculation formulas for indirect costs.</span></span>

<span data-ttu-id="592b1-107">一个成本计算版本可以服务于一种或多种目的，具体取决于在该成本计算版本内包含的数据。</span><span class="sxs-lookup"><span data-stu-id="592b1-107">A costing version can serve one or more purposes, depending on the data that the costing version contains.</span></span> <span data-ttu-id="592b1-108">成本计算版本主要用于包含与物料、成本类别和间接成本计算公式有关的成本记录。</span><span class="sxs-lookup"><span data-stu-id="592b1-108">The primary purpose of a costing version is to contain cost records about items, cost categories, and calculation formulas for indirect costs.</span></span> <span data-ttu-id="592b1-109">一个成本计算版本可以包含一组标准成本记录或一组计划成本记录（基于分配给该成本计算版本的成本计算类型）。</span><span class="sxs-lookup"><span data-stu-id="592b1-109">A costing version can contain a set of standard cost records or a set of planned cost records that are based on the costing type that is assigned to the costing version.</span></span>

## <a name="costing-versions-for-standard-or-planned-costs"></a><span data-ttu-id="592b1-110">标准或计划成本的成本计算版本</span><span class="sxs-lookup"><span data-stu-id="592b1-110">Costing versions for standard or planned costs</span></span>
### <a name="standard-costs"></a><span data-ttu-id="592b1-111">标准成本</span><span class="sxs-lookup"><span data-stu-id="592b1-111">Standard costs</span></span>

<span data-ttu-id="592b1-112">成本计算版本可以支持物料的标准成本库存模型，其中，成本计算版本包含与物料和制造过程有关的一组标准成本记录。</span><span class="sxs-lookup"><span data-stu-id="592b1-112">A costing version can support a standard cost inventory model for items, where the costing version contains a set of standard cost records about items and manufacturing processes.</span></span> <span data-ttu-id="592b1-113">根据用于工艺路线工序的成本类别以及用于制造开销的计算公式，表示与制造过程有关的成本数据。</span><span class="sxs-lookup"><span data-stu-id="592b1-113">Cost data about manufacturing processes is expressed in terms of the cost categories for routing operations and the calculation formulas for manufacturing overheads.</span></span>

### <a name="planned-costs"></a><span data-ttu-id="592b1-114">计划成本</span><span class="sxs-lookup"><span data-stu-id="592b1-114">Planned costs</span></span>

<span data-ttu-id="592b1-115">成本计算版本可以包含与物料和制造过程有关的一组计划的成本记录。</span><span class="sxs-lookup"><span data-stu-id="592b1-115">A costing version can contain a set of planned cost records about items and manufacturing processes.</span></span> <span data-ttu-id="592b1-116">具有计划成本的成本计算版本常用于支持成本计算模拟，例如模拟在制造物料的计算的成本上成本变化对采购物料或制造过程的影响。</span><span class="sxs-lookup"><span data-stu-id="592b1-116">A costing version that contains planned costs is often used to support cost calculation simulations, such as simulations of the effect that cost changes to purchased materials or manufacturing processes has on the calculated costs of manufactured items.</span></span> <span data-ttu-id="592b1-117">计划成本的物料成本记录还可用于通过提供物料成本的初始值来支持实际成本库存模型。</span><span class="sxs-lookup"><span data-stu-id="592b1-117">The item cost records for planned costs can also be used to support an actual cost inventory model by providing the initial values for item costs.</span></span> <span data-ttu-id="592b1-118">这些值包括计算制造物料的计划成本。</span><span class="sxs-lookup"><span data-stu-id="592b1-118">These values include the calculation of planned costs for manufactured items.</span></span>

## <a name="entering-costs"></a><span data-ttu-id="592b1-119">输入成本</span><span class="sxs-lookup"><span data-stu-id="592b1-119">Entering costs</span></span>
<span data-ttu-id="592b1-120">对成本计算版本内的成本记录进行数据维护涉及为采购物料和在各站点之间转移的物料输入成本。</span><span class="sxs-lookup"><span data-stu-id="592b1-120">Data maintenance for cost records in a costing version involves entering costs for purchased items and for items that are transferred between sites.</span></span> <span data-ttu-id="592b1-121">针对制造商的附加数据维护涉及为成本类别输入与工艺路线工序相关联的成本、为反映制造开销的间接成本输入计算公式，以及为制造物料计算成本。</span><span class="sxs-lookup"><span data-stu-id="592b1-121">Additional data maintenance for manufacturers involves entering costs for cost categories that are associated with routing operations, entering calculation formulas for the indirect costs that reflect manufacturing overhead, and calculating costs for manufactured items.</span></span> 

<span data-ttu-id="592b1-122">成本计算版本内的物料成本数据由针对各个物料的一个或多个成本记录构成。</span><span class="sxs-lookup"><span data-stu-id="592b1-122">The item cost data in a costing version consists of one or more cost records for each item.</span></span> <span data-ttu-id="592b1-123">当物料成本记录初次输入时，它具有**待定**状态和预期生效日期。</span><span class="sxs-lookup"><span data-stu-id="592b1-123">When an item cost record is first entered, it has **Pending** status and an intended effective date.</span></span> <span data-ttu-id="592b1-124">当您激活物料成本记录时，状态将更新为**有效**，生效日期将更新为激活日期。</span><span class="sxs-lookup"><span data-stu-id="592b1-124">When you activate the item cost record, the status is updated to **Active**, and the effective date is updated to the activation date.</span></span> <span data-ttu-id="592b1-125">不同的物料成本记录可以反应不同站点、生效日期、或状态。</span><span class="sxs-lookup"><span data-stu-id="592b1-125">Different item cost records can reflect different sites, effective dates, or statuses.</span></span> <span data-ttu-id="592b1-126">当您为将来日期计算制造物料的成本时，该物料清单计算将使用具有相关生效日期的成本记录，无论该状态是**待定**还是**有效**。</span><span class="sxs-lookup"><span data-stu-id="592b1-126">When you calculate costs for manufactured items for a future date, the bill of materials (BOM) calculation uses cost records that have the relevant effective date, regardless of whether the status is **Pending** or **Active**.</span></span> <span data-ttu-id="592b1-127">一个物料的当前活动成本记录用于评估生产订单成本和对标准成本计算库存模型下的库存交易记录求值。</span><span class="sxs-lookup"><span data-stu-id="592b1-127">An item's current active cost record is used to estimate production order costs and to value inventory transactions under a standard costing inventory model.</span></span> <span data-ttu-id="592b1-128">为成本类别和间接成本计算公式维护成本记录类似于维护物料成本记录。</span><span class="sxs-lookup"><span data-stu-id="592b1-128">The maintenance of cost records for cost categories and indirect cost calculation formulas resembles the maintenance of item cost records.</span></span> 

<span data-ttu-id="592b1-129">用于成本计算版本的两个冻结策略确定是否可维护未决成本以及是否可启用未决成本。</span><span class="sxs-lookup"><span data-stu-id="592b1-129">Two blocking policies for a costing version determine whether pending costs can be maintained and whether the pending cost can be activated.</span></span> <span data-ttu-id="592b1-130">使用冻结策略可以允许数据维护，然后使用它们为某一成本计算版本内的成本记录阻止数据维护。</span><span class="sxs-lookup"><span data-stu-id="592b1-130">Use the blocking policies to permit data maintenance, and then use them to prevent data maintenance for cost records in a costing version.</span></span> 

<span data-ttu-id="592b1-131">成本计算版本还可以出于物料清单计算目的，包含与物料销售价或采购价相关的数据。</span><span class="sxs-lookup"><span data-stu-id="592b1-131">A costing version can also contain data about item sales prices or purchase prices for BOM calculation purposes.</span></span>

## <a name="item-sales-prices-for-bom-calculations"></a><span data-ttu-id="592b1-132">物料清单计算的物料销售价</span><span class="sxs-lookup"><span data-stu-id="592b1-132">Item sales prices for BOM calculations</span></span>
<span data-ttu-id="592b1-133">包括有关销售价的数据的主要原因是保留制造物料的计算销售价。</span><span class="sxs-lookup"><span data-stu-id="592b1-133">The main reason for including data about sales prices is to retain a manufactured item’s calculated sales price.</span></span> <span data-ttu-id="592b1-134">然后可以分析计算出的销售价确定组件、工艺路线工序和开销有助于成本价和销售价。</span><span class="sxs-lookup"><span data-stu-id="592b1-134">The calculated sales price can then be analyzed to determine how components, routing operations, and overhead contribute to the cost and sales price.</span></span> 

<span data-ttu-id="592b1-135">包括有关销售价的数据的次要原因是定义构成物料的销售价记录。</span><span class="sxs-lookup"><span data-stu-id="592b1-135">A secondary reason for including data about sales prices is to define the sales price records for component items.</span></span> <span data-ttu-id="592b1-136">这些记录然后可用于计算制造物料的销售价。</span><span class="sxs-lookup"><span data-stu-id="592b1-136">These records can then be used to calculate the sales price of manufactured items.</span></span> <span data-ttu-id="592b1-137">您首先定义在物料清单计算组中嵌入的销售价模型，然后将该物料清单计算组分配给采购物料。</span><span class="sxs-lookup"><span data-stu-id="592b1-137">You first define the sales price model that is embedded in a BOM calculation group, and assign the BOM calculation group to purchased items.</span></span> <span data-ttu-id="592b1-138">然后，在您执行使用计划成本的物料清单计算时，选择物料清单计算组的成本价模型。</span><span class="sxs-lookup"><span data-stu-id="592b1-138">Then, when you perform BOM calculations that use planned costs, you select the cost price model of the BOM calculation group.</span></span> 

<span data-ttu-id="592b1-139">否则，无论是手动输入的还是计算出的记录，物料销售价记录仅用作参考信息。</span><span class="sxs-lookup"><span data-stu-id="592b1-139">Otherwise, the sales price records for items are used only as reference information, regardless of whether the records are manually entered or calculated.</span></span> <span data-ttu-id="592b1-140">通过激活物料的销售价记录，可以更新该物料的基本销售价。</span><span class="sxs-lookup"><span data-stu-id="592b1-140">By activating an item’s sales price record, you can update the item’s base sales price.</span></span> <span data-ttu-id="592b1-141">然而，基本销售价不是特定于站点的，并且可以手动覆盖。</span><span class="sxs-lookup"><span data-stu-id="592b1-141">However, the base sales price isn't site-specific and can be manually overridden.</span></span> <span data-ttu-id="592b1-142">该物料的基本销售价用作销售订单和销售报价单上的默认销售价。</span><span class="sxs-lookup"><span data-stu-id="592b1-142">The item’s base sales price is used as a default sales price on sales orders and sales quotations.</span></span>

## <a name="item-purchase-prices-for-bom-calculations"></a><span data-ttu-id="592b1-143">物料清单计算的物料采购价</span><span class="sxs-lookup"><span data-stu-id="592b1-143">Item purchase prices for BOM calculations</span></span>
<span data-ttu-id="592b1-144">启用采购价数据的主要原因是为构成物料定义采购价记录，然后使用该采购价记录计算制造物料的成本。</span><span class="sxs-lookup"><span data-stu-id="592b1-144">The main reason for enabling purchase price data is to define purchase price records for component items, so that these records can be used to calculate the costs of manufactured items.</span></span> <span data-ttu-id="592b1-145">物料采购价记录必须手动输入。</span><span class="sxs-lookup"><span data-stu-id="592b1-145">The item purchase price records must be manually entered.</span></span> 

<span data-ttu-id="592b1-146">若要启用采购价内容，必须先定义包含物料的采购价的成本价模型的物料清单计算组，然后将该物料清单计算组分配给采购物料。</span><span class="sxs-lookup"><span data-stu-id="592b1-146">To enable purchase price content, you first define a BOM calculation group that contains a cost price model for the item’s purchase price, and assign the BOM calculation group to purchased items.</span></span> <span data-ttu-id="592b1-147">然后，在您执行使用计划成本的物料清单计算来计算制造物料的销售价时，您将为物料清单计算组使用成本价模型。</span><span class="sxs-lookup"><span data-stu-id="592b1-147">You then use a cost price model for the BOM calculation group when you perform BOM calculations that use planned costs to calculate the sales price of manufactured items.</span></span> 

<span data-ttu-id="592b1-148">物料的采购价记录也用作参考信息。</span><span class="sxs-lookup"><span data-stu-id="592b1-148">The purchase price records for items are also used as reference information.</span></span> <span data-ttu-id="592b1-149">通过将物料的采购价记录的状态从**待定**更改为**有效**，您可以更新该物料的基本采购价。</span><span class="sxs-lookup"><span data-stu-id="592b1-149">By changing the status of an item’s purchase price record from **Pending** to **Active**, you can update the item’s base purchase price.</span></span> <span data-ttu-id="592b1-150">然而，基本采购价不是特定于站点的，并且可以手动覆盖。</span><span class="sxs-lookup"><span data-stu-id="592b1-150">However, the base purchase price isn't site-specific and can be manually overridden.</span></span> <span data-ttu-id="592b1-151">该物料的基本采购价将用作采购订单上的默认采购价。</span><span class="sxs-lookup"><span data-stu-id="592b1-151">The item's base purchase price is used as a default purchase price on purchase orders.</span></span>



