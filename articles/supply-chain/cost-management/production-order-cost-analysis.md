---
title: "生产订单成本分析"
description: "本文提供有关可为已完成和当前生产订单执行的成本分析的信息。 您可以使用价格计算页或成本预估和成本计算报表分析估计成本和实际成本。 您可以查看有关每个组件物料的估计和实际成本（和数量）、工艺路线工序以及间接成本的信息。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 703070ae85f504cf204244b2197732dc6849abd6
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="production-order-cost-analysis"></a><span data-ttu-id="2aac3-105">生产订单成本分析</span><span class="sxs-lookup"><span data-stu-id="2aac3-105">Production order cost analysis</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2aac3-106">本文提供有关可为已完成和当前生产订单执行的成本分析的信息。</span><span class="sxs-lookup"><span data-stu-id="2aac3-106">This article provides information about the cost analysis that you can do for completed and current production orders.</span></span> <span data-ttu-id="2aac3-107">您可以使用价格计算页或成本预估和成本计算报表分析估计成本和实际成本。</span><span class="sxs-lookup"><span data-stu-id="2aac3-107">You can analyze the estimated costs and actual costs by using the Price calculation page or the Cost estimates and costings report.</span></span> <span data-ttu-id="2aac3-108">您可以查看有关每个组件物料的估计和实际成本（和数量）、工艺路线工序以及间接成本的信息。</span><span class="sxs-lookup"><span data-stu-id="2aac3-108">You can view information about the estimated and actual costs (and quantity) for each component item, the routing operation, and the indirect cost.</span></span>

<span data-ttu-id="2aac3-109">生产订单的实际成本基于报告的物料消耗量和工艺路线工序。</span><span class="sxs-lookup"><span data-stu-id="2aac3-109">The actual costs for a production order are based on the reported consumption of material and routing operations.</span></span> <span data-ttu-id="2aac3-110">您可以访问有关**生产过帐**页中生产订单的报告的物料消耗量、工艺路线工序和间接成本的详细交易记录。</span><span class="sxs-lookup"><span data-stu-id="2aac3-110">You can access detailed transactions about the reported consumption of material, routing operations, and indirect costs for a production order on the **Production posting** page.</span></span>

## <a name="variance-analysis-for-a-completed-production-order"></a><span data-ttu-id="2aac3-111">已完成生产订单的差异分析</span><span class="sxs-lookup"><span data-stu-id="2aac3-111">Variance analysis for a completed production order</span></span>
<span data-ttu-id="2aac3-112">差异反映生产物料的报告的生产活动和标准成本的计算之间的比较。</span><span class="sxs-lookup"><span data-stu-id="2aac3-112">The variances reflect a comparison of the reported production activities and the calculation of standard costs for the production item.</span></span> <span data-ttu-id="2aac3-113">该差异不反映与生产订单的估计成本的比较。</span><span class="sxs-lookup"><span data-stu-id="2aac3-113">The variances don't reflect a comparison to the production order's estimated costs.</span></span> <span data-ttu-id="2aac3-114">报告的生产活动包含物料消耗量和工艺路线工序，以及关联的直接成本和报告完成的数量。</span><span class="sxs-lookup"><span data-stu-id="2aac3-114">The production activities that are reported include the consumption of material and routing operations, together with the associated indirect costs, and the quantity that is reported as finished.</span></span> <span data-ttu-id="2aac3-115">计算差异的以下四种类型：</span><span class="sxs-lookup"><span data-stu-id="2aac3-115">The following four types of variance are calculated:</span></span>

-   <span data-ttu-id="2aac3-116">批次规模差异</span><span class="sxs-lookup"><span data-stu-id="2aac3-116">Lot size variance</span></span>
-   <span data-ttu-id="2aac3-117">生产数量差异</span><span class="sxs-lookup"><span data-stu-id="2aac3-117">Production quantity variance</span></span>
-   <span data-ttu-id="2aac3-118">生产价差异</span><span class="sxs-lookup"><span data-stu-id="2aac3-118">Production price variance</span></span>
-   <span data-ttu-id="2aac3-119">生产替代差异</span><span class="sxs-lookup"><span data-stu-id="2aac3-119">Production substitution variance</span></span>

<span data-ttu-id="2aac3-120">在该生产订单结束时，下图为物料的成本记录内生成订单的实际成本和计算的成本之间的差异显示帐户的四个差异。</span><span class="sxs-lookup"><span data-stu-id="2aac3-120">The following diagram shows the four variances that account for the difference between a production order's actual costs and the calculated costs within the item's cost record when the production order is ended.</span></span> 

![计入已完成生产订单差异的差异](./media/control.jpg) 

<span data-ttu-id="2aac3-122">可以通过使用**差异**页或**生产差异**报表分析生产差异。</span><span class="sxs-lookup"><span data-stu-id="2aac3-122">You can analyze the production variances by using the **Variance** page or the **Production variance** report.</span></span> <span data-ttu-id="2aac3-123">使用显示选项卡按物料和运营资源，或按成本组查看详细差异。</span><span class="sxs-lookup"><span data-stu-id="2aac3-123">Use the display options to view detailed variances by item and operations resource, or by cost group.</span></span> <span data-ttu-id="2aac3-124">库存参数中的成本细分策略确定是否按成本组跟踪差异。</span><span class="sxs-lookup"><span data-stu-id="2aac3-124">The policy for cost breakdown in the inventory parameters determines whether the variances are tracked by cost group.</span></span> <span data-ttu-id="2aac3-125">您还可以使用**单个**、**多个**和**总计**显示选项查看汇总的差异。</span><span class="sxs-lookup"><span data-stu-id="2aac3-125">You can also use the **single**, **multi**, and **total** display options to view summarized variances.</span></span> <span data-ttu-id="2aac3-126">有关详细差异的信息可以帮助您理解每个差异的来源。</span><span class="sxs-lookup"><span data-stu-id="2aac3-126">The information about detailed variances can help you understand the source of each variance.</span></span> <span data-ttu-id="2aac3-127">为了在结束生产订单前预测差异，应分析在**成本预估和成本计算**报表中提供的详细信息。</span><span class="sxs-lookup"><span data-stu-id="2aac3-127">To predict variances before you end a production order, analyze the detailed information that is provided on the **Cost estimates and costings** report.</span></span>

## <a name="cost-analysis-for-current-production-orders"></a><span data-ttu-id="2aac3-128">当前生产订单的成本分析</span><span class="sxs-lookup"><span data-stu-id="2aac3-128">Cost analysis for current production orders</span></span>
<span data-ttu-id="2aac3-129">单独的报表提供与各个交易记录类型有关的信息。</span><span class="sxs-lookup"><span data-stu-id="2aac3-129">Separate reports provide information about each type of transaction.</span></span> <span data-ttu-id="2aac3-130">使用这些报表可以分析报告的生产活动的成本。</span><span class="sxs-lookup"><span data-stu-id="2aac3-130">Use these reports to analyze costs for reported production activities.</span></span> <span data-ttu-id="2aac3-131">只为状态为**已开始**或**完工入库**的当前生产订单显示信息。</span><span class="sxs-lookup"><span data-stu-id="2aac3-131">Information is displayed only for current production orders that have a status of **Started** or **Reported as finished**.</span></span>

-   <span data-ttu-id="2aac3-132">**在途原材料** − 该报表列出根据截至指定交易记录日期的当前生产订单报告的领料单交易记录。</span><span class="sxs-lookup"><span data-stu-id="2aac3-132">**Materials in process** − This report lists the picking list transactions that are reported against the current production orders as of a specified transaction date.</span></span> <span data-ttu-id="2aac3-133">该报表指示发货的组件的数量以及各个交易记录的成本额。</span><span class="sxs-lookup"><span data-stu-id="2aac3-133">The report indicates the quantity of a component that was issued and the cost amount for each transaction.</span></span> <span data-ttu-id="2aac3-134">为单个组件物料使用选择条件。</span><span class="sxs-lookup"><span data-stu-id="2aac3-134">Use the selection criteria for a single component item.</span></span> <span data-ttu-id="2aac3-135">例如，您可以根据适用生产订单打印与组件的发货数量有关的信息。</span><span class="sxs-lookup"><span data-stu-id="2aac3-135">For example, you can print information about the component’s issued quantity against applicable production orders.</span></span> <span data-ttu-id="2aac3-136">发货数量不按照父物料的完工入库数量进行更新。</span><span class="sxs-lookup"><span data-stu-id="2aac3-136">The issued quantity isn't updated by the quantities that are reported as finished for the parent item.</span></span> <span data-ttu-id="2aac3-137">因此，进行中的原材料的实际数量可能会被高估。</span><span class="sxs-lookup"><span data-stu-id="2aac3-137">Therefore, the actual quantity of raw materials in process might be overstated.</span></span>
-   <span data-ttu-id="2aac3-138">**在制品** − 该报表列出根据截至指定交易记录日期的当前生产订单报告的工艺路线交易记录（或作业）。</span><span class="sxs-lookup"><span data-stu-id="2aac3-138">**Work in process** − This report lists route transactions (or job transactions) that are reported against the current production orders as of a specified transaction date.</span></span> <span data-ttu-id="2aac3-139">该报表指示为每个交易记录报告的工时、金额和数量（完好数量和残次数量）。</span><span class="sxs-lookup"><span data-stu-id="2aac3-139">The report indicates the hours, amount, and quantity (both good quantity and error quantity) that are reported for each transaction.</span></span> <span data-ttu-id="2aac3-140">它还包括诸如工序编号、工序 ID 和工序资源等信息。</span><span class="sxs-lookup"><span data-stu-id="2aac3-140">It also includes information such as the operation number, operation ID, and operations resource.</span></span> <span data-ttu-id="2aac3-141">而且，该报表还根据生产订单显示所有交易记录的总时间和金额，以及完工入库数量。</span><span class="sxs-lookup"><span data-stu-id="2aac3-141">Additionally, this report shows the total time and amount for all transactions against the production order, and the quantity that is reported as finished.</span></span>
-   <span data-ttu-id="2aac3-142">**未入帐间接成本** − 该报表针对生产订单列出了已发生的间接成本。</span><span class="sxs-lookup"><span data-stu-id="2aac3-142">**Indirect costs in process** − This report lists the indirect costs that have been incurred against production orders.</span></span> <span data-ttu-id="2aac3-143">此数据是基于工艺路线工序的已报告消耗和截止指定交易记录日期的组件。</span><span class="sxs-lookup"><span data-stu-id="2aac3-143">This data is based on reported consumption of routing operations and components as of a specified transaction date.</span></span> <span data-ttu-id="2aac3-144">该报表指示间接成本的类型（附加费或费用）、间接成本的成本计算单代码和每个交易记录的成本额。</span><span class="sxs-lookup"><span data-stu-id="2aac3-144">The report indicates the type of indirect cost (surcharge or rate), the costing sheet code for the indirect cost, and the cost amount for each transaction.</span></span> <span data-ttu-id="2aac3-145">该报表不提供有关导致间接成本的工艺卡或领料单交易记录的信息。</span><span class="sxs-lookup"><span data-stu-id="2aac3-145">This report doesn't provide information about the route card or pick list transaction that generated the indirect cost.</span></span>
-   <span data-ttu-id="2aac3-146">**进行中的生产的成本计算** − 该报表针对截至指定交易记录日期的生产订单，列出组合的物料消耗量、工艺路线工序和间接成本。</span><span class="sxs-lookup"><span data-stu-id="2aac3-146">**In process production costing** − This report lists the combined consumption of material, routing operations, and indirect cost against the production orders as of a specified transaction date.</span></span>
-   <span data-ttu-id="2aac3-147">**在制的成品** − 该报表列出截至指定的交易记录日期的当前生产订单和完工入库交易记录。</span><span class="sxs-lookup"><span data-stu-id="2aac3-147">**Finished items in process** − This report lists current production orders and the report-as-finished transactions as of a specified transaction date.</span></span>


<a name="see-also"></a><span data-ttu-id="2aac3-148">请参阅</span><span class="sxs-lookup"><span data-stu-id="2aac3-148">See also</span></span>
--------

[<span data-ttu-id="2aac3-149">生产差异的常见来源</span><span class="sxs-lookup"><span data-stu-id="2aac3-149">Common sources of production variances</span></span>](common-sources-of-production-variances.md)




