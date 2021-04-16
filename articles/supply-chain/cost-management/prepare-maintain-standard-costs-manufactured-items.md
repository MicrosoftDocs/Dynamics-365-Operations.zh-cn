---
title: 准备为制造物料维护标准成本
description: 本主题介绍准备维护制造物料成本的步骤。
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6944782ac236a3f414b1cadfb12b0f0d8c1115b9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821505"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="f484f-103">准备为制造物料维护标准成本</span><span class="sxs-lookup"><span data-stu-id="f484f-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f484f-104">本主题介绍准备维护制造物料成本的步骤。</span><span class="sxs-lookup"><span data-stu-id="f484f-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="f484f-105">制造物料的步骤与采购物料的步骤稍有不同。</span><span class="sxs-lookup"><span data-stu-id="f484f-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="f484f-106">分配给制造物料的策略可能会影响父级制造物料的成本计算。</span><span class="sxs-lookup"><span data-stu-id="f484f-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="f484f-107">若要准备维护制造物料的成本，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="f484f-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="f484f-108">将某一物料模型组分配给该制造物料。</span><span class="sxs-lookup"><span data-stu-id="f484f-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="f484f-109">该物料模型组标识将使用标准成本。</span><span class="sxs-lookup"><span data-stu-id="f484f-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="f484f-110">将某一物料组分配给制造物料。</span><span class="sxs-lookup"><span data-stu-id="f484f-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="f484f-111">该物料组包含应用于制造物料的会计科目。</span><span class="sxs-lookup"><span data-stu-id="f484f-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="f484f-112">具有标准成本库存模型的制造物料的会计科目包括若干生产差异、成本变化差异和库存成本重估。</span><span class="sxs-lookup"><span data-stu-id="f484f-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="f484f-113">将库存度量单位分配给该物料。</span><span class="sxs-lookup"><span data-stu-id="f484f-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="f484f-114">该物料的成本始终按其库存度量单位表示。</span><span class="sxs-lookup"><span data-stu-id="f484f-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="f484f-115">不用将某一成本组分配给制造物料，除非该物料将被视作采购物料。</span><span class="sxs-lookup"><span data-stu-id="f484f-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="f484f-116">将物料清单 (BOM) 计算组分配给制造物料。</span><span class="sxs-lookup"><span data-stu-id="f484f-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="f484f-117">物料的 BOM 计算组标识应用的警告条件。</span><span class="sxs-lookup"><span data-stu-id="f484f-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="f484f-118">这样，BOM 计算完成后，可生成有关计算错误可能原因的警告消息。</span><span class="sxs-lookup"><span data-stu-id="f484f-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="f484f-119">例如，某一警告消息可以标识有效物料清单或工艺路线何时不存在。</span><span class="sxs-lookup"><span data-stu-id="f484f-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="f484f-120">物料清单计算组包含停止分解策略，指示何时应将制造物料视作采购物料。</span><span class="sxs-lookup"><span data-stu-id="f484f-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="f484f-121">如果制造物料具有固定成本，请为其分配标准订单数量。</span><span class="sxs-lookup"><span data-stu-id="f484f-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="f484f-122">标准订单数量是摊销固定成本的会计批次规模。</span><span class="sxs-lookup"><span data-stu-id="f484f-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="f484f-123">固定成本的示例包括工艺路线工序的设置时间和 BOM 中的固定组件数量。</span><span class="sxs-lookup"><span data-stu-id="f484f-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="f484f-124">为制造物料定义物料清单。</span><span class="sxs-lookup"><span data-stu-id="f484f-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="f484f-125">可为制造物料定义一个或多个物料清单版本。</span><span class="sxs-lookup"><span data-stu-id="f484f-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="f484f-126">请确认您所需的版本已标记为已审核且活动的版本，并且它们具有所需的生效日期。</span><span class="sxs-lookup"><span data-stu-id="f484f-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="f484f-127">该物料清单版本可以是公司范围的或特定于站点的。</span><span class="sxs-lookup"><span data-stu-id="f484f-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="f484f-128">为制造物料定义工艺路线。</span><span class="sxs-lookup"><span data-stu-id="f484f-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="f484f-129">可为制造物料定义一个或多个工艺路线版本。</span><span class="sxs-lookup"><span data-stu-id="f484f-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="f484f-130">请确认您所需的版本已标记为已审核且活动的版本，并且它们具有所需的生效日期。</span><span class="sxs-lookup"><span data-stu-id="f484f-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="f484f-131">该工艺路线版本必须是特定于站点的。</span><span class="sxs-lookup"><span data-stu-id="f484f-131">The route version must be site-specific.</span></span>

<span data-ttu-id="f484f-132">如果要将工艺路线信息用于成本核算目的，需要执行更多的准备步骤。</span><span class="sxs-lookup"><span data-stu-id="f484f-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="f484f-133">例如，分配给工艺路线工序的成本类别必须正确且完整。</span><span class="sxs-lookup"><span data-stu-id="f484f-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="f484f-134">相关主题</span><span class="sxs-lookup"><span data-stu-id="f484f-134">Related topics</span></span>
--------

[<span data-ttu-id="f484f-135">为制造物料摊销固定成本</span><span class="sxs-lookup"><span data-stu-id="f484f-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="f484f-136">设置可以生产或采购的产品</span><span class="sxs-lookup"><span data-stu-id="f484f-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]