---
title: "运输管理概览"
description: "本主题概述 Microsoft Dynamics 365 for Finance and Operations 中的运输管理功能。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8cea065ca07a19a50a0a22b124788a2ab745f17b
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="transportation-management-overview"></a><span data-ttu-id="68727-103">运输管理概览</span><span class="sxs-lookup"><span data-stu-id="68727-103">Transportation management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="68727-104">本主题概述 Microsoft Dynamics 365 for Finance and Operations 中的运输管理功能。</span><span class="sxs-lookup"><span data-stu-id="68727-104">This topic gives an overview of the transportation management functionality in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="68727-105">“运输管理”能让您使用公司的运输，还能让您为进货和出货订单标识供应商和路线解决方法。</span><span class="sxs-lookup"><span data-stu-id="68727-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="68727-106">例如，您可以标识装运的最快路线或最便宜费率。</span><span class="sxs-lookup"><span data-stu-id="68727-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="68727-107">下表描述在 Microsoft Dynamics 365 for Finance and Operations 中使用运输管理的主要情况。</span><span class="sxs-lookup"><span data-stu-id="68727-107">The following table describes the main scenarios for using Transportation management in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68727-108">方案</span><span class="sxs-lookup"><span data-stu-id="68727-108">Scenario</span></span></th>
<th><span data-ttu-id="68727-109">运输管理如何提供帮助</span><span class="sxs-lookup"><span data-stu-id="68727-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="68727-110">为运输活动使用外部物流提供商。</span><span class="sxs-lookup"><span data-stu-id="68727-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="68727-111">为入站和/或出站运使用运输管理。</span><span class="sxs-lookup"><span data-stu-id="68727-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68727-112">公司自己的车队可用于交货/装货，交货费用向客户收取。</span><span class="sxs-lookup"><span data-stu-id="68727-112">The company's own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="68727-113">对于出站流程，您可以使用运输管理来确定运输费用并将费用传递给客户。</span><span class="sxs-lookup"><span data-stu-id="68727-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="68727-114">不过，不需要承运人发票对帐流程。</span><span class="sxs-lookup"><span data-stu-id="68727-114">However, the carrier invoice reconciliation process isn't required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="68727-115">公司自己的车队可用于交货/装货，但交货费用不由客户承担，因为产品价格包括运输费用。</span><span class="sxs-lookup"><span data-stu-id="68727-115">The company's own fleet is available for delivery/pickup, but delivery charges aren't passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="68727-116">不需要大量运输管理功能。</span><span class="sxs-lookup"><span data-stu-id="68727-116">A lot of the Transportation management functionality isn't required.</span></span> <span data-ttu-id="68727-117">但是，您可以使用运输管理来确定运输费率和相应调整销售价格。</span><span class="sxs-lookup"><span data-stu-id="68727-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="68727-118">物流服务由同一公司的另一法人提供。</span><span class="sxs-lookup"><span data-stu-id="68727-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="68727-119">您可以通过将其他法人视为任何其他装运承运人来使用运输管理。</span><span class="sxs-lookup"><span data-stu-id="68727-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="68727-120">您不能将法人之间的经济交易记录自动化。</span><span class="sxs-lookup"><span data-stu-id="68727-120">You can't automate the economic transactions between legal entities.</span></span> <span data-ttu-id="68727-121">因此，您必须手动处理这些交易记录（例如，通过创建采购订单）。</span><span class="sxs-lookup"><span data-stu-id="68727-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="68727-122">在提供物流服务的法人中，运输管理可用于确定运输费用。</span><span class="sxs-lookup"><span data-stu-id="68727-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-finance-and-operations"></a><span data-ttu-id="68727-123">在 Finance and Operations 中规划运输</span><span class="sxs-lookup"><span data-stu-id="68727-123">Planning transportation in Finance and Operations</span></span>
<span data-ttu-id="68727-124">在运输管理中， 运输计划可以基于订单或基于根据这些订单创建的装运。</span><span class="sxs-lookup"><span data-stu-id="68727-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="68727-125">装运在某个时间点上始终存在，但对运输计划不是必需的。</span><span class="sxs-lookup"><span data-stu-id="68727-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="68727-126">转移单是出站方案的一部分，并且可以与销售订单一起计划。</span><span class="sxs-lookup"><span data-stu-id="68727-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![装载图](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="68727-128">入站运输</span><span class="sxs-lookup"><span data-stu-id="68727-128">Inbound transportation</span></span>
<span data-ttu-id="68727-129">当您从供应商订购物料，且物料必须交付至您的仓库，您可能想要亲自安排物料的运输。</span><span class="sxs-lookup"><span data-stu-id="68727-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="68727-130">您可以使用 Finance and Operations 来计划运输和入站装载的收货。</span><span class="sxs-lookup"><span data-stu-id="68727-130">You can use Finance and Operations to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="68727-131">下图显示了计划入站负荷的运输的业务流程。</span><span class="sxs-lookup"><span data-stu-id="68727-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![入站装载运输的业务流程](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="68727-133">出站运输</span><span class="sxs-lookup"><span data-stu-id="68727-133">Outbound transportation</span></span>
<span data-ttu-id="68727-134">您可以计划和处理一个出站负荷来将指定物料从公司仓库装运至客户。</span><span class="sxs-lookup"><span data-stu-id="68727-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="68727-135">您可以使用 Finance and Operations 来计划运输和出站装载的装运。</span><span class="sxs-lookup"><span data-stu-id="68727-135">You can use Finance and Operations to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="68727-136">下图显示了计划和处理装运的出站负荷的业务流程。</span><span class="sxs-lookup"><span data-stu-id="68727-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![计划和处理出站装载](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="68727-138">装载计划</span><span class="sxs-lookup"><span data-stu-id="68727-138">Load building</span></span>
<span data-ttu-id="68727-139">Finance and Operations 提供称作“基于容量的装载计划策略”的装载计划策略。</span><span class="sxs-lookup"><span data-stu-id="68727-139">Finance and Operations provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="68727-140">此策略允许您在装载模板上为高度和重量指定最大值，或您可以通过输入新的值来覆盖设置。</span><span class="sxs-lookup"><span data-stu-id="68727-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="68727-141">若要使用此策略，请在**装载计划工作台**页中**设置**快速选项卡上的**装载计划策略**字段中选择。</span><span class="sxs-lookup"><span data-stu-id="68727-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="68727-142">此外，可以在应用程序对象树 (AOT) 中创建新类添加您自己的负荷创建策略。</span><span class="sxs-lookup"><span data-stu-id="68727-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>




