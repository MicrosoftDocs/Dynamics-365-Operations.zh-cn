---
title: "生产订单成本估计"
description: "本文提供有关生产成本估计的信息。 生产成本估计提供按计划的生产订单数量生产一个物料的预计材料和产能消耗成本。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 172bb55358c20ba80b1c32b05f1ae8e6aff8901f
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="production-order-cost-estimation"></a><span data-ttu-id="3018e-104">生产订单成本估计</span><span class="sxs-lookup"><span data-stu-id="3018e-104">Production order cost estimation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3018e-105">本文提供有关生产成本估计的信息。</span><span class="sxs-lookup"><span data-stu-id="3018e-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="3018e-106">生产成本估计提供按计划的生产订单数量生产一个物料的预计材料和产能消耗成本。</span><span class="sxs-lookup"><span data-stu-id="3018e-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="3018e-107">在您创建生产订单后，必须估计生产成本。</span><span class="sxs-lookup"><span data-stu-id="3018e-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="3018e-108">目的是估计生产流程的物料和工艺路线消耗量，因为这些预估用作后续的排产和生产流程的基础。</span><span class="sxs-lookup"><span data-stu-id="3018e-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="3018e-109">生产成本估计</span><span class="sxs-lookup"><span data-stu-id="3018e-109">Production cost estimation</span></span>
<span data-ttu-id="3018e-110">生产成本估计基于以下信息：</span><span class="sxs-lookup"><span data-stu-id="3018e-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="3018e-111">生产订单中的数量</span><span class="sxs-lookup"><span data-stu-id="3018e-111">The quantity on the production order</span></span>
-   <span data-ttu-id="3018e-112">生产物料清单 (BOM) 的组件</span><span class="sxs-lookup"><span data-stu-id="3018e-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="3018e-113">生产工艺路线中的工艺路线工序</span><span class="sxs-lookup"><span data-stu-id="3018e-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="3018e-114">应用于组件和工序的间接成本</span><span class="sxs-lookup"><span data-stu-id="3018e-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="3018e-115">截至计算日期的有效成本数据</span><span class="sxs-lookup"><span data-stu-id="3018e-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="3018e-116">如果生产物料清单中存在虚拟行物料，这些计算反映虚拟的组件和工艺路线工序。</span><span class="sxs-lookup"><span data-stu-id="3018e-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="3018e-117">您可以使用估计任务重新计算估计成本，以便它们反映更新的信息。</span><span class="sxs-lookup"><span data-stu-id="3018e-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="3018e-118">例如，更新后的信息可以更改为生产订单数量、生产物料清单中的组件、生产工艺路线中的工艺路线工序、适用于这些组件和工序的间接成本或者截至重新计算日期的有效成本数据中的变化。</span><span class="sxs-lookup"><span data-stu-id="3018e-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="3018e-119">计算估计成本还基于成本加上加价方法为生产物流建议销售价格。</span><span class="sxs-lookup"><span data-stu-id="3018e-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="3018e-120">估计成本计算可选择是否应用于参考订单，参考订单反映链接到该生产订单的其他生产订单。</span><span class="sxs-lookup"><span data-stu-id="3018e-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="3018e-121">查看估计成本</span><span class="sxs-lookup"><span data-stu-id="3018e-121">View the estimated costs</span></span>
<span data-ttu-id="3018e-122">在运行估计后，您可以查看**价格计算**页上的结果。</span><span class="sxs-lookup"><span data-stu-id="3018e-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="3018e-123">估计将计算以下值：</span><span class="sxs-lookup"><span data-stu-id="3018e-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="3018e-124">**生产成本** – 生产成本是估计的顶行。</span><span class="sxs-lookup"><span data-stu-id="3018e-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="3018e-125">它显示执行生产订单的整个成本以及生产的总销售价。</span><span class="sxs-lookup"><span data-stu-id="3018e-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="3018e-126">它是预估上的所有成本行之和。</span><span class="sxs-lookup"><span data-stu-id="3018e-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="3018e-127">**工艺路线或资源成本** – 工艺路线或资源成本是生产工序的成本。</span><span class="sxs-lookup"><span data-stu-id="3018e-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="3018e-128">它们包括诸如设置时间、运行时间和开销等元素成本。</span><span class="sxs-lookup"><span data-stu-id="3018e-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="3018e-129">**材料成本** – 材料成本是需要用于生产物料的物料清单组件的成本和价格。</span><span class="sxs-lookup"><span data-stu-id="3018e-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="3018e-130">这些成本以前已确立并输入到系统中。</span><span class="sxs-lookup"><span data-stu-id="3018e-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="3018e-131">成本估计的其他用途</span><span class="sxs-lookup"><span data-stu-id="3018e-131">Other uses of cost estimation</span></span>
<span data-ttu-id="3018e-132">成本估计还提供以下信息：</span><span class="sxs-lookup"><span data-stu-id="3018e-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="3018e-133">有意义的报价单</span><span class="sxs-lookup"><span data-stu-id="3018e-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="3018e-134">订单利润的估计</span><span class="sxs-lookup"><span data-stu-id="3018e-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="3018e-135">原材料使用的估计</span><span class="sxs-lookup"><span data-stu-id="3018e-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="3018e-136">来自以前生产的成本信息的比较</span><span class="sxs-lookup"><span data-stu-id="3018e-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="3018e-137">预算和预测信息</span><span class="sxs-lookup"><span data-stu-id="3018e-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="3018e-138">维持特定成本所需的生产规模的估计</span><span class="sxs-lookup"><span data-stu-id="3018e-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>





