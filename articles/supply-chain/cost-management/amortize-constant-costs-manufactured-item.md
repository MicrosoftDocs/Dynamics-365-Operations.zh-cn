---
title: "为制造物料摊销固定成本"
description: "制造物料的固定成本反映工序设置时间以及具有固定数量或固定残值金额的组件。"
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 1f3c837d601877142ac6708287a434f5afe088e6
ms.contentlocale: zh-cn
ms.lasthandoff: 01/17/2018

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="f8588-103">为制造物料摊销固定成本</span><span class="sxs-lookup"><span data-stu-id="f8588-103">Amortize constant costs for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f8588-104">制造物料的固定成本反映工序设置时间以及具有固定数量或固定残值金额的组件。</span><span class="sxs-lookup"><span data-stu-id="f8588-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="f8588-105">成本计算批次规模的概念用于在制造物料的计算成本中摊销这些固定成本。</span><span class="sxs-lookup"><span data-stu-id="f8588-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="f8588-106">此概念具有若干同义词，其中之一是会计批次规模。</span><span class="sxs-lookup"><span data-stu-id="f8588-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="f8588-107">摊销固定成本的概念也具有若干同义词，其中之一是成比例固定成本。</span><span class="sxs-lookup"><span data-stu-id="f8588-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>

<span data-ttu-id="f8588-108">制造物料的成本计算批次规模数量用于物料清单 (BOM) 计算中。</span><span class="sxs-lookup"><span data-stu-id="f8588-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="f8588-109">该数量取决于您是如何启动和执行物料清单计算的，如下所示：</span><span class="sxs-lookup"><span data-stu-id="f8588-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>

-   <span data-ttu-id="f8588-110">物料的物料清单计算中的默认计算数量 − 该物料的标准订单数量（用于库存）充当成本计算批次规模，但该默认值可以是更高的数量，以便反映该物料的订单数量倍数。</span><span class="sxs-lookup"><span data-stu-id="f8588-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="f8588-111">可以在该物料的默认订单设置或特定于站点的订单设置内定义其标准订单数量和倍数。</span><span class="sxs-lookup"><span data-stu-id="f8588-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="f8588-112">物料的物料清单计算中的指定计算数量 − 该指定的计算数量充当物料的成本计算批次规模。</span><span class="sxs-lookup"><span data-stu-id="f8588-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="f8588-113">该计算数量最初使用该物料的标准订单数量，但默认值可被手动覆盖。</span><span class="sxs-lookup"><span data-stu-id="f8588-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="f8588-114">指定的计算数量为指定的物料和具有生产的一种物料清单行类型的制造组件显示成本计算批次规模。</span><span class="sxs-lookup"><span data-stu-id="f8588-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="f8588-115">原因在于，假定精确数量生产制造组件。</span><span class="sxs-lookup"><span data-stu-id="f8588-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="f8588-116">具有物料的物料清单行类型的其他制造组件的成本计算批次规模将反映其标准订单数量。</span><span class="sxs-lookup"><span data-stu-id="f8588-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="f8588-117">物料的物料清单计算中指定的按订单生产计算数量 − 该指定的计算数量在物料清单计算使用按订单生产分解模式时充当该物料及其制造组件的成本计算批次规模。</span><span class="sxs-lookup"><span data-stu-id="f8588-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="f8588-118">假定按精确数量生产制造组件，就像具有生产的物料清单行类型的制造组件。</span><span class="sxs-lookup"><span data-stu-id="f8588-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="f8588-119">特定于订单的物料清单计算中的指定计算数量 − 可为销售订单、销售报价单或服务订单上的行项执行特定于订单的物料清单计算。</span><span class="sxs-lookup"><span data-stu-id="f8588-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="f8588-120">该指定的计算数量使用原始行项上的数量，但是可以覆盖该默认数量。</span><span class="sxs-lookup"><span data-stu-id="f8588-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="f8588-121">您可以选择特定于订单的物料清单计算是使用按订单生产还是多级分解模式。</span><span class="sxs-lookup"><span data-stu-id="f8588-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="f8588-122">制造物料的摊销固定成本的计算出的金额称作费用。</span><span class="sxs-lookup"><span data-stu-id="f8588-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>






