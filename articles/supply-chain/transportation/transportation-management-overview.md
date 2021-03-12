---
title: 运输管理概览
description: 本主题提供 Supply Chain Management 中运输管理功能的概览。
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30251
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fca83ef2c80ed6df9cfbdedd2805e453df3f737a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006483"
---
# <a name="transportation-management-overview"></a><span data-ttu-id="402b5-103">运输管理概览</span><span class="sxs-lookup"><span data-stu-id="402b5-103">Transportation management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="402b5-104">本主题提供 Supply Chain Management 中运输管理功能的概览。</span><span class="sxs-lookup"><span data-stu-id="402b5-104">This topic gives an overview of the transportation management functionality in Supply Chain Management.</span></span>

<span data-ttu-id="402b5-105">“运输管理”能让您使用公司的运输，还能让您为进货和出货订单标识供应商和路线解决方法。</span><span class="sxs-lookup"><span data-stu-id="402b5-105">Transportation management lets you use your company’s transportation, and also lets you identify vendor and routing solutions for inbound and outbound orders.</span></span> <span data-ttu-id="402b5-106">例如，您可以标识装运的最快路线或最便宜费率。</span><span class="sxs-lookup"><span data-stu-id="402b5-106">For example, you can identify the fastest route or the least expensive rate for a shipment.</span></span> <span data-ttu-id="402b5-107">下表描述使用运输管理的主要情况。</span><span class="sxs-lookup"><span data-stu-id="402b5-107">The following table describes the main scenarios for using Transportation management.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="402b5-108">场景</span><span class="sxs-lookup"><span data-stu-id="402b5-108">Scenario</span></span></th>
<th><span data-ttu-id="402b5-109">运输管理如何提供帮助</span><span class="sxs-lookup"><span data-stu-id="402b5-109">How Transportation management can help</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="402b5-110">为运输活动使用外部物流提供商。</span><span class="sxs-lookup"><span data-stu-id="402b5-110">Use external logistics providers for transportation activities.</span></span></td>
<td><span data-ttu-id="402b5-111">为入站和/或出站运使用运输管理。</span><span class="sxs-lookup"><span data-stu-id="402b5-111">Use Transportation management for inbound and/or outbound transportation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="402b5-112">公司自己的车队可用于交货/装货，交货费用向客户收取。</span><span class="sxs-lookup"><span data-stu-id="402b5-112">The company&#39;s own fleet is available for delivery/pickup, and delivery charges are passed on to customers.</span></span></td>
<td><span data-ttu-id="402b5-113">对于出站流程，您可以使用运输管理来确定运输费用并将费用传递给客户。</span><span class="sxs-lookup"><span data-stu-id="402b5-113">For the outbound processes, you can use Transportation management to determine the transportation charges and pass them on to customers.</span></span> <span data-ttu-id="402b5-114">不过，不需要承运人发票对帐流程。</span><span class="sxs-lookup"><span data-stu-id="402b5-114">However, the carrier invoice reconciliation process isn&#39;t required.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="402b5-115">公司自己的车队可用于交货/装货，但交货费用不由客户承担，因为产品价格包括运输费用。</span><span class="sxs-lookup"><span data-stu-id="402b5-115">The company&#39;s own fleet is available for delivery/pickup, but delivery charges aren&#39;t passed on to customers, because product prices include transportation.</span></span></td>
<td><span data-ttu-id="402b5-116">不需要大量运输管理功能。</span><span class="sxs-lookup"><span data-stu-id="402b5-116">A lot of the Transportation management functionality isn&#39;t required.</span></span> <span data-ttu-id="402b5-117">但是，您可以使用运输管理来确定运输费率和相应调整销售价格。</span><span class="sxs-lookup"><span data-stu-id="402b5-117">However, you can use Transportation management to determine the transportation rates and adjust the sales price accordingly.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="402b5-118">物流服务由同一公司的另一法人提供。</span><span class="sxs-lookup"><span data-stu-id="402b5-118">Logistics service is provided by another legal entity in the same company.</span></span></td>
<td><ul>
<li><span data-ttu-id="402b5-119">您可以通过将其他法人视为任何其他装运承运人来使用运输管理。</span><span class="sxs-lookup"><span data-stu-id="402b5-119">You can use Transportation management by treating the other legal entity like any other shipping carrier.</span></span> <span data-ttu-id="402b5-120">您不能将法人之间的经济交易记录自动化。</span><span class="sxs-lookup"><span data-stu-id="402b5-120">You can&#39;t automate the economic transactions between legal entities.</span></span> <span data-ttu-id="402b5-121">因此，您必须手动处理这些交易记录（例如，通过创建采购订单）。</span><span class="sxs-lookup"><span data-stu-id="402b5-121">Therefore, you must handle these transactions manually (for example, by creating a purchase order).</span></span></li>
<li><span data-ttu-id="402b5-122">在提供物流服务的法人中，运输管理可用于确定运输费用。</span><span class="sxs-lookup"><span data-stu-id="402b5-122">In the legal entity that provides the logistics services, Transportation management can be used to determine transportation rates.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a><span data-ttu-id="402b5-123">在 Supply Chain Management 中计划运输</span><span class="sxs-lookup"><span data-stu-id="402b5-123">Planning transportation in Supply Chain Management</span></span>
<span data-ttu-id="402b5-124">在运输管理中， 运输计划可以基于订单或基于根据这些订单创建的装运。</span><span class="sxs-lookup"><span data-stu-id="402b5-124">In Transportation management, transportation planning can be based either on orders or on the shipments that are created based on those orders.</span></span> <span data-ttu-id="402b5-125">装运在某个时间点上始终存在，但对运输计划不是必需的。</span><span class="sxs-lookup"><span data-stu-id="402b5-125">The shipments always exist at some point in time but aren't required for transportation planning.</span></span> <span data-ttu-id="402b5-126">转移单是出站方案的一部分，并且可以与销售订单一起计划。</span><span class="sxs-lookup"><span data-stu-id="402b5-126">Transfer orders are part of the outbound scenario and can be planned together with sales orders.</span></span> 

![装载图](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a><span data-ttu-id="402b5-128">入站运输</span><span class="sxs-lookup"><span data-stu-id="402b5-128">Inbound transportation</span></span>
<span data-ttu-id="402b5-129">当您从供应商订购物料，且物料必须交付至您的仓库，您可能想要亲自安排物料的运输。</span><span class="sxs-lookup"><span data-stu-id="402b5-129">When you order items from a vendor, and the items must be delivered to your warehouse, you might want to arrange the transport of the items yourself.</span></span> <span data-ttu-id="402b5-130">您可以使用 Supply Chain Management 来计划运输和入站负荷的收货。</span><span class="sxs-lookup"><span data-stu-id="402b5-130">You can use Supply Chain Management to plan the transportation and receipt of the inbound load.</span></span> <span data-ttu-id="402b5-131">下图显示了计划入站负荷的运输的业务流程。</span><span class="sxs-lookup"><span data-stu-id="402b5-131">The following illustration shows the business process flow for planning transportation for an inbound load.</span></span> 

![入站装载运输的业务流程](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a><span data-ttu-id="402b5-133">出站运输</span><span class="sxs-lookup"><span data-stu-id="402b5-133">Outbound transportation</span></span>
<span data-ttu-id="402b5-134">您可以计划和处理一个出站负荷来将指定物料从公司仓库装运至客户。</span><span class="sxs-lookup"><span data-stu-id="402b5-134">You can plan and process an outbound load to ship specific items from a company’s warehouse to a customer.</span></span> <span data-ttu-id="402b5-135">您可以使用 Supply Chain Management 来计划运输和出站负荷的装运。</span><span class="sxs-lookup"><span data-stu-id="402b5-135">You can use Supply Chain Management to plan the transportation and shipping of an outbound load.</span></span> <span data-ttu-id="402b5-136">下图显示了计划和处理装运的出站负荷的业务流程。</span><span class="sxs-lookup"><span data-stu-id="402b5-136">The following illustration shows the business process flow for planning and processing outbound loads for shipping.</span></span> 

![计划和处理出站装载](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a><span data-ttu-id="402b5-138">装载计划</span><span class="sxs-lookup"><span data-stu-id="402b5-138">Load building</span></span>
<span data-ttu-id="402b5-139">Supply Chain Management 提供称作“基于容量的装载计划策略”的装载计划策略。</span><span class="sxs-lookup"><span data-stu-id="402b5-139">Supply Chain Management provides a load building strategy that is named the Volume-based load building strategy.</span></span> <span data-ttu-id="402b5-140">此策略允许您在装载模板上为高度和重量指定最大值，或您可以通过输入新的值来覆盖设置。</span><span class="sxs-lookup"><span data-stu-id="402b5-140">This strategy lets you use the maximum values that are specified for height and weight in the load template, or you can override the settings by entering new values.</span></span> <span data-ttu-id="402b5-141">若要使用此策略，请在 **装载计划工作台** 页中 **设置** 快速选项卡上的 **装载计划策略** 字段中选择。</span><span class="sxs-lookup"><span data-stu-id="402b5-141">To use this strategy, select it in the **Load building strategy** field on the **Setup** FastTab on the **Load building workbench** page.</span></span> <span data-ttu-id="402b5-142">此外，可以在应用程序对象树 (AOT) 中创建新类添加您自己的负荷创建策略。</span><span class="sxs-lookup"><span data-stu-id="402b5-142">In addition, you can add your own load-building strategies by creating a new class in the Application Object Tree (AOT).</span></span>



