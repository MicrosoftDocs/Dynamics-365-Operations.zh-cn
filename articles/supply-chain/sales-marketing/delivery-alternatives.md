---
title: "交货备选方案"
description: "销售订单处理人员可以使用交货备选方案页发现备选订单履行选项。"
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b2ecf2d5b14dac28a26fe172807ae2931cb4c3ca
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="delivery-alternatives"></a><span data-ttu-id="d5a2b-103">交货备选方案</span><span class="sxs-lookup"><span data-stu-id="d5a2b-103">Delivery alternatives</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d5a2b-104">销售订单处理人员可以使用交货备选方案页发现备选订单履行选项。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-104">Sales order takers can use the Delivery alternatives page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="d5a2b-105">在 Microsoft Dynamics 365 for Operations 版本 1611（2016 年 11 月）中，销售订单处理人员可以使用**交货备选方案**页发现备选订单履行选项。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-105">In Microsoft Dynamics 365 for Operations version 1611 (November 2016), sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span> <span data-ttu-id="d5a2b-106">经过重新设计的页面布局提供所有备选方案的更好概览。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-106">The redesigned page layout gives a better overview of all alternative options.</span></span> <span data-ttu-id="d5a2b-107">它还能让订单处理人员在当前公司以外寻找履行机会。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-107">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="d5a2b-108">他们现在可以查看内部公司机会和来自外部供应商的机会。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-108">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="d5a2b-109">通过按交货日期排序选项，销售订单处理人员可以查看交货备选方案的智能列表。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-109">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="d5a2b-110">此外，参数帮助他们更好地管理建议的交货。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-110">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="d5a2b-111">因为运输时间可以影响交货日期，销售订单处理人员可以探索承运人提供的各种运输选择。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-111">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="d5a2b-112">由于详细信息为每个建议显示，订单处理人员可以直接从**交货备选方案**页做出明智的决定。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-112">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="d5a2b-113">打开“交货备选方案”页</span><span class="sxs-lookup"><span data-stu-id="d5a2b-113">Open the Delivery alternatives page</span></span>
<span data-ttu-id="d5a2b-114">您可以从销售订单行打开**交货****备选方案**页。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-114">You can open the **Delivery** **alternatives** page from the sales order line.</span></span>

1.  <span data-ttu-id="d5a2b-115">单击**产品和供应**&gt;**交货备选方案**。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-115">Click **Products and supply** &gt; **Delivery alternatives**.</span></span>
2.  <span data-ttu-id="d5a2b-116">单击**行明细**&gt;**交货**&gt;**交货备选方案**。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-116">Click **Line details** &gt; **Delivery** &gt; **Delivery alternatives.**</span></span>

<span data-ttu-id="d5a2b-117">您还可以通过打开**销售订单处理和查询**工作区打开**交货备选方案**页，然后单击**订单和收藏**&gt;**延迟的订单行**&gt;**交货备选方案** **注意：**只有当同时满足以下两个条件时，您才能够打开**交货备选方案**页：</span><span class="sxs-lookup"><span data-stu-id="d5a2b-117">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then clicking **Orders and favorites** &gt; **Delayed order lines** &gt; **Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

-   <span data-ttu-id="d5a2b-118">所有必需销售订单行信息均已填写。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-118">All mandatory sales line information is filled in.</span></span>
-   <span data-ttu-id="d5a2b-119">**交货日期控制**字段设置为**无**以外的值。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-119">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="d5a2b-120">交货日期控制方法</span><span class="sxs-lookup"><span data-stu-id="d5a2b-120">Delivery date control methods</span></span>
<span data-ttu-id="d5a2b-121">交货日期控制方法确定系统如何确定交货日期，如何计算交货备选方案，以及显示哪些信息。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-121">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="d5a2b-122">请注意，交货数据控制考虑日历。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-122">Note that delivery data control takes calendars into consideration.</span></span> <span data-ttu-id="d5a2b-123">因此，以下日历可能影响建议的收货日期：仓库日历、运输日历、供应商日历和客户日历。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-123">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="d5a2b-124">下表描述交货日期控制的各个方法。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-124">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d5a2b-125"><strong>方法</strong></span><span class="sxs-lookup"><span data-stu-id="d5a2b-125"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="d5a2b-126"><strong>描述</strong></span><span class="sxs-lookup"><span data-stu-id="d5a2b-126"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a2b-127"><strong>无</strong></span><span class="sxs-lookup"><span data-stu-id="d5a2b-127"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="d5a2b-128">不支持销售订单行的交货备选方案。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-128">Delivery alternatives for sales lines aren't supported.</span></span> <span data-ttu-id="d5a2b-129">此选项关闭交货数据控制。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-129">This option turns off delivery data control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5a2b-130"><strong>销售提前期</strong></span><span class="sxs-lookup"><span data-stu-id="d5a2b-130"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="d5a2b-131">交货备选方案根据预定义的销售提前期计算。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-131">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="d5a2b-132">运输天数基于交货方式计算。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-132">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="d5a2b-133">交货备选方案包括具有现有库存量库存和供应/需求订单的仓库。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-133">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a2b-134"><strong>ATP</strong></span><span class="sxs-lookup"><span data-stu-id="d5a2b-134"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="d5a2b-135">交货备选方案根据可承诺 (ATP) 逻辑计算。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-135">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="d5a2b-136">考虑当前可用性以及预期的将来可用性。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-136">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="d5a2b-137">运输天数基于交货方式计算。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-137">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="d5a2b-138">交货备选方案包括具有现有库存量库存和供应/需求订单的仓库。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-138">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d5a2b-139"><strong>ATP + 发货宽限期</strong></span><span class="sxs-lookup"><span data-stu-id="d5a2b-139"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="d5a2b-140">交货备选方案针对 ATP 方法计算，但是，发货宽限期包括在计算中。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-140">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d5a2b-141"><strong>CTP</strong></span><span class="sxs-lookup"><span data-stu-id="d5a2b-141"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="d5a2b-142">交货备选方案根据可承诺量 (CTP) 逻辑计算。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-142">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="d5a2b-143">MRP 分解用于确定可用性。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-143">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="d5a2b-144">请注意，CTP 至少将交货日期偏移至销售提前期。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-144">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="d5a2b-145">运输天数基于交货方式计算。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-145">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="d5a2b-146">交货备选方案包括以下仓库的建议：</span><span class="sxs-lookup"><span data-stu-id="d5a2b-146">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="d5a2b-147">当前仓库</span><span class="sxs-lookup"><span data-stu-id="d5a2b-147">Current warehouse</span></span></li>
<li><span data-ttu-id="d5a2b-148">默认仓库</span><span class="sxs-lookup"><span data-stu-id="d5a2b-148">Default warehouse</span></span></li>
<li><span data-ttu-id="d5a2b-149">具有现有库存量的所有仓库</span><span class="sxs-lookup"><span data-stu-id="d5a2b-149">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="d5a2b-150">具有供应订单的所有仓库</span><span class="sxs-lookup"><span data-stu-id="d5a2b-150">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="d5a2b-151">具有有效物料清单 (BOM) 版本的所有仓库</span><span class="sxs-lookup"><span data-stu-id="d5a2b-151">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="d5a2b-152">查看有关交货备选方案的信息</span><span class="sxs-lookup"><span data-stu-id="d5a2b-152">View information about delivery alternatives</span></span>
<span data-ttu-id="d5a2b-153">此节介绍在**交货备选方案**页的每个选项卡上可用的交货备选方案的信息。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-153">This section describes the information about delivery alternatives that is available on each tab of the **Delivery alternatives** page.</span></span>

### <a name="products"></a><span data-ttu-id="d5a2b-154">产品</span><span class="sxs-lookup"><span data-stu-id="d5a2b-154">Products</span></span>

<span data-ttu-id="d5a2b-155">此选项卡显示当前销售订单行的产品和详细信息的汇总。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-155">This tab shows a summary of the product and details of the current sales line.</span></span>

### <a name="delivery-alternatives"></a><span data-ttu-id="d5a2b-156">交货备选方案</span><span class="sxs-lookup"><span data-stu-id="d5a2b-156">Delivery alternatives</span></span>

<span data-ttu-id="d5a2b-157">此选项卡显示按收货数据排序的交货备选方案的列表。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-157">This tab shows a list of delivery alternatives that is sorted by receipt data.</span></span> <span data-ttu-id="d5a2b-158">在列表上，您可以选择建议所基于的选项。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-158">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="d5a2b-159">您还可以选择某一交货方式，确定运输天数。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-159">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="d5a2b-160">选项如下：</span><span class="sxs-lookup"><span data-stu-id="d5a2b-160">The following options are available:</span></span>

-   <span data-ttu-id="d5a2b-161">**包括其他产品变型** - 此选项对于包含产品变型的产品可用。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-161">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="d5a2b-162">它将包括其他产品变型的交货备选方案。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-162">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="d5a2b-163">此选项对 CTP 不可用。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-163">This option isn't available for CTP.</span></span>
-   <span data-ttu-id="d5a2b-164">**包括部分数量** - 默认情况下，仅包括执行销售订单行的完整数量的建议。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-164">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="d5a2b-165">选择此选项可以包含行只部分执行订单的建议。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-165">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="d5a2b-166">当客户请求更早的交货日期并接受部分交货时，此选项很有用。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-166">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
-   <span data-ttu-id="d5a2b-167">**包括更晚的日期** - 默认情况下，只显示好于（早于）销售订单行上的当前日期的建议。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-167">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="d5a2b-168">选择此选项以包括更晚的日期。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-168">Select this option to include later dates.</span></span> <span data-ttu-id="d5a2b-169">此选项在日期之外的参数具有优先级的情况下很有用。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-169">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="d5a2b-170">例如，特定供应商或仓库可能是首选。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-170">For example, a specific vendor or warehouse might be preferred.</span></span>
-   <span data-ttu-id="d5a2b-171">**交货方式** - 选择首选交货方式来优化运输时间和成本。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-171">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="d5a2b-172">您将立即看到建议的交货备选方案的效果。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-172">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="d5a2b-173">因此，比较备选方案更轻松。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-173">Therefore, it's easy to compare the alternatives.</span></span>
-   <span data-ttu-id="d5a2b-174">**包括采购** - 在选择采购时，建议的交货备选方案包括从外部供应商和企业（内部公司）的其他公司采购的选项。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-174">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="d5a2b-175">**包括采购**选项支持 ATP 和 ATP + 发货宽限期交货日期控制。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-175">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="d5a2b-176">来自产品默认供采购应商以及产品所有已审核供应商的采购选项都将包括在内。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-176">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
-   <span data-ttu-id="d5a2b-177">对于外部供应商，计算基于采购提前期。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-177">For external vendors, the calculation is based on the purchase lead time.</span></span>
-   <span data-ttu-id="d5a2b-178">对于内部公司，计算考虑采购公司的可用量，基于采购公司的交货日期控制。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-178">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
-   <span data-ttu-id="d5a2b-179">**交货类型**（与采购相关）</span><span class="sxs-lookup"><span data-stu-id="d5a2b-179">**Delivery type** (Relevant for procurement)</span></span>
    -   <span data-ttu-id="d5a2b-180">**存货** - 产品从采购仓库装运到销售订单行的站点/仓库。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-180">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="d5a2b-181">然后从该仓库装运到客户。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-181">They are then shipped from that warehouse to the customer.</span></span>
    -   <span data-ttu-id="d5a2b-182">**直接交运** - 产品直接从采购仓库装运给客户。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-182">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="availability-information"></a><span data-ttu-id="d5a2b-183">可用信息</span><span class="sxs-lookup"><span data-stu-id="d5a2b-183">Availability information</span></span>

<span data-ttu-id="d5a2b-184">此选项卡上的信息与所选交货备选方案行相关。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-184">Information on this tab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="d5a2b-185">以下信息根据销售订单行的交货日期控制显示：</span><span class="sxs-lookup"><span data-stu-id="d5a2b-185">The following information is shown, depending on the delivery date control for the sales line:</span></span>

-   <span data-ttu-id="d5a2b-186">**销售提前期**</span><span class="sxs-lookup"><span data-stu-id="d5a2b-186">**Sales lead time**</span></span>
    -   <span data-ttu-id="d5a2b-187">**今天可用** - 显示当前实际现有量、实际预留和实际可用库存。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-187">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="d5a2b-188">**参数** - 显示库存单位和销售提前期。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-188">**Parameters** - Show the inventory unit and sales lead time.</span></span>

-   <span data-ttu-id="d5a2b-189">**ATP and ATP + 发货宽限期**</span><span class="sxs-lookup"><span data-stu-id="d5a2b-189">**ATP and ATP + Issue margin**</span></span>
    -   <span data-ttu-id="d5a2b-190">**今天可用** - 显示当前实际现有量、实际预留和实际可用库存。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-190">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="d5a2b-191">**参数** - 显示库存单位和销售提前期。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-191">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="d5a2b-192">**将来的可用性** - 显示**交货备选方案**下所选站点和仓库的当前和未来可用性的图形表示形式。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-192">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="d5a2b-193">您可单击图表列查看有关产品的将来可用性的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-193">You can click the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="d5a2b-194">此滑块显示 ATP 时限内相关需求和供应订单的列表。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-194">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

-   <span data-ttu-id="d5a2b-195">**CTP**</span><span class="sxs-lookup"><span data-stu-id="d5a2b-195">**CTP**</span></span>
    -   <span data-ttu-id="d5a2b-196">**今天可用** - 显示当前实际现有量、实际预留和实际可用库存。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-196">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="d5a2b-197">**参数** - 显示库存单位和销售提前期。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-197">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="d5a2b-198">**分解** - 显示所选交货备选方案的供应分解。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-198">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="d5a2b-199">您可以使用**设置**更改在分解中显示的字段和库存维度。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-199">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="impact-of-selected-alternative"></a><span data-ttu-id="d5a2b-200">选定替换的影响</span><span class="sxs-lookup"><span data-stu-id="d5a2b-200">Impact of selected alternative</span></span>

<span data-ttu-id="d5a2b-201">此选项卡突出显示所选交货备选方案的影响。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-201">This tab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="d5a2b-202">如果您单击**确定**，销售订单行更新为所选列中突出显示的值。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-202">If you click **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="d5a2b-203">请注意，如果所选交货备选方案的数量少于销售订单行的数量，将创建交货计划，并且销售订单行拆分为两行：一行为选择的数量，一行为剩余数量。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-203">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="d5a2b-204">您还可以更新业务行，以便其与计划行匹配并影响定价。</span><span class="sxs-lookup"><span data-stu-id="d5a2b-204">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

<a name="see-also"></a><span data-ttu-id="d5a2b-205">请参阅</span><span class="sxs-lookup"><span data-stu-id="d5a2b-205">See also</span></span>
--------

[<span data-ttu-id="d5a2b-206">订单承诺</span><span class="sxs-lookup"><span data-stu-id="d5a2b-206">Order promising</span></span>](delivery-dates-available-promise-calculations.md)





