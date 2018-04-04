---
title: "计划具有多个停止点的货运运输路线"
description: "本文介绍用于在 Dynamics 365 for Finance and Operations 中计划运输路线的各种元素。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 16255e812773ed35c0e34ec26a8a689ea09632bd
ms.contentlocale: zh-cn
ms.lasthandoff: 03/26/2018

---

# <a name="plan-freight-transportation-routes-with-multiple-stops"></a><span data-ttu-id="f4875-103">计划具有多个停止点的货运运输路线</span><span class="sxs-lookup"><span data-stu-id="f4875-103">Plan freight transportation routes with multiple stops</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f4875-104">本文介绍用于在 Microsoft Dynamics 365 for Finance and Operations 中计划运输路线的各种元素。</span><span class="sxs-lookup"><span data-stu-id="f4875-104">This article describes the various elements that you use to plan transportation routes in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="f4875-105">可以使用路线计划和路线指南计划具有多个停止点的复杂交通路线。</span><span class="sxs-lookup"><span data-stu-id="f4875-105">You can use route plans and route guides for complex transportation routes that have multiple stops.</span></span> <span data-ttu-id="f4875-106">如果将定期使用同一个路线，您可以设置计划路线。</span><span class="sxs-lookup"><span data-stu-id="f4875-106">If the same route will be used on a regular basis, you can set up a scheduled route.</span></span>

## <a name="route-plans"></a><span data-ttu-id="f4875-107">路线计划</span><span class="sxs-lookup"><span data-stu-id="f4875-107">Route plans</span></span>
<span data-ttu-id="f4875-108">路线计划包含提供有关在路线中访问的停止点和用于每个段的运营商的信息。</span><span class="sxs-lookup"><span data-stu-id="f4875-108">A route plan contains route segments that provide information about the stops that are visited on the route and the carriers that are used for each segment.</span></span> <span data-ttu-id="f4875-109">必须在路线上将停止点定义为枢纽。</span><span class="sxs-lookup"><span data-stu-id="f4875-109">You must define the stops on the route as hubs.</span></span> <span data-ttu-id="f4875-110">枢纽可以是供应商、仓库、客户或甚至只是一个再装货位置（您可在其中更改承运人）。</span><span class="sxs-lookup"><span data-stu-id="f4875-110">A hub can be a vendor, a warehouse, a customer, or even just a reloading place where you change carrier.</span></span> <span data-ttu-id="f4875-111">对于每个段，您可以定义各种费用的“即期费率”。</span><span class="sxs-lookup"><span data-stu-id="f4875-111">For each segment, you can define “spot rates” for various charges.</span></span> <span data-ttu-id="f4875-112">下面举了一些示例加以说明：</span><span class="sxs-lookup"><span data-stu-id="f4875-112">Here are some examples:</span></span>

-   <span data-ttu-id="f4875-113">往返于给定段的费用</span><span class="sxs-lookup"><span data-stu-id="f4875-113">Charges for travelling to the given segments</span></span>
-   <span data-ttu-id="f4875-114">领取货物的费用</span><span class="sxs-lookup"><span data-stu-id="f4875-114">Charges for a picking up the goods</span></span>
-   <span data-ttu-id="f4875-115">邮寄货物的费用</span><span class="sxs-lookup"><span data-stu-id="f4875-115">Charges for dropping off the goods</span></span>

<span data-ttu-id="f4875-116">每个路线计划必须与路线指南关联。</span><span class="sxs-lookup"><span data-stu-id="f4875-116">Each route plan must be associated with a route guide.</span></span>

## <a name="route-guides"></a><span data-ttu-id="f4875-117">路线指南</span><span class="sxs-lookup"><span data-stu-id="f4875-117">Route guides</span></span>
<span data-ttu-id="f4875-118">路线指南定义将负荷与特定路线计划匹配的条件。</span><span class="sxs-lookup"><span data-stu-id="f4875-118">A route guide defines the criteria for matching a load to a specific route plan.</span></span> <span data-ttu-id="f4875-119">例如，您可以指定起始枢纽和目标枢纽，容器体积或重量限制，以及配送承运人、服务或组。</span><span class="sxs-lookup"><span data-stu-id="f4875-119">For example, you can specify an origin hub and a destination hub, limits for the container volume or weight, and a shipping carrier, service, or group.</span></span> <span data-ttu-id="f4875-120">路线指南在**费率路线工作台**页面提供，在此页面上，负荷可以手动或自动与路线匹配。</span><span class="sxs-lookup"><span data-stu-id="f4875-120">Route guides are available on the **Rate route workbench** page, where loads can be matched to routes either manually or automatically.</span></span> <span data-ttu-id="f4875-121">如果路线指南针对计划路线，它也在**装载计划工作台**页提供。</span><span class="sxs-lookup"><span data-stu-id="f4875-121">If the route guide is for a scheduled route, it's also available on the **Load building workbench** page.</span></span>

## <a name="scheduled-routes"></a><span data-ttu-id="f4875-122">计划的路线</span><span class="sxs-lookup"><span data-stu-id="f4875-122">Scheduled routes</span></span>
<span data-ttu-id="f4875-123">计划路线是具有装运日期计划的预定义路线计划。</span><span class="sxs-lookup"><span data-stu-id="f4875-123">A scheduled route is a predefined route plan that has a schedule for the shipping dates.</span></span> <span data-ttu-id="f4875-124">计划路线和非计划路线在负荷分配的方式方面不同。</span><span class="sxs-lookup"><span data-stu-id="f4875-124">Scheduled routes and non-scheduled routes differ in the way that loads are assigned to them.</span></span> <span data-ttu-id="f4875-125">如果通过使用费率路线工作台分配非计划路线，则仅负荷和路线指南进行验证。</span><span class="sxs-lookup"><span data-stu-id="f4875-125">If you assign a non-scheduled route by using the Rate route workbench, only the load and the route guide are validated.</span></span> <span data-ttu-id="f4875-126">如果分配计划路线，还考虑订单和枢纽的日期和地址，以及路线计划的日期。</span><span class="sxs-lookup"><span data-stu-id="f4875-126">If you assign a scheduled route, the dates and addresses from the orders and the hubs, and the date on the route plan, are also considered.</span></span> <span data-ttu-id="f4875-127">您不必使用费率路线工作台页面手动将负荷分配到计划路线。</span><span class="sxs-lookup"><span data-stu-id="f4875-127">You don't have to use the Rate route workbench page to manually assign loads to a scheduled route.</span></span> <span data-ttu-id="f4875-128">相反，可以使用装载计划工作台建议基于给定计划路线的销售订单的客户地址和交货日期构建。</span><span class="sxs-lookup"><span data-stu-id="f4875-128">Instead, you can use the Load building workbench to suggest that loads be built based on the customer addresses and delivery dates from sales orders for a given scheduled route.</span></span> <span data-ttu-id="f4875-129">对于计划路线，路线计划将具有固定的起始和目标枢纽。</span><span class="sxs-lookup"><span data-stu-id="f4875-129">For scheduled routes, the route plan will have fixed origin and destination hubs.</span></span> <span data-ttu-id="f4875-130">通常情况下，装运承运人和服务对所有段将是相同的，但它们可以有区别。</span><span class="sxs-lookup"><span data-stu-id="f4875-130">Typically, the shipping carrier and service will be the same for all segments, but they can differ.</span></span> <span data-ttu-id="f4875-131">目标枢纽使用在路线访问的客户的邮政编码创建。</span><span class="sxs-lookup"><span data-stu-id="f4875-131">The destination hubs are created by using the postal codes of the customers that are visited on the route.</span></span> <span data-ttu-id="f4875-132">可以为一个路线计划定义几种路线计划。</span><span class="sxs-lookup"><span data-stu-id="f4875-132">Several route schedules can be defined for one route plan.</span></span> <span data-ttu-id="f4875-133">路线计划必须与路线指南关联。</span><span class="sxs-lookup"><span data-stu-id="f4875-133">The route plan must be associated with a route guide.</span></span> <span data-ttu-id="f4875-134">不过，对于计划路线，计划可只与一个路线指南关联。</span><span class="sxs-lookup"><span data-stu-id="f4875-134">However, for scheduled routes, the plan can be associated with only one route guide.</span></span> <span data-ttu-id="f4875-135">路线计划只能用于在**路线计划**页创建实际路线。</span><span class="sxs-lookup"><span data-stu-id="f4875-135">The route schedule is used only to create the actual routes on the **Route schedule** page.</span></span> <span data-ttu-id="f4875-136">在装载计划工作台建议负荷时，可以使用默认的负荷模板。</span><span class="sxs-lookup"><span data-stu-id="f4875-136">You can use the default load template when you propose loads on the Load building workbench.</span></span>

## <a name="load-building-workbench"></a><span data-ttu-id="f4875-137">装载计划工作台</span><span class="sxs-lookup"><span data-stu-id="f4875-137">Load building workbench</span></span>
<span data-ttu-id="f4875-138">装载计划工作台使用销售订单的客户地址和交货日期以及可用的计划路线建议负荷。</span><span class="sxs-lookup"><span data-stu-id="f4875-138">The Load building workbench uses the customer addresses and delivery dates from sales orders, and the scheduled routes that are available, to propose a load.</span></span> <span data-ttu-id="f4875-139">默认情况下，在工作台上输入路线的值。</span><span class="sxs-lookup"><span data-stu-id="f4875-139">By default, the values from the route are entered on the workbench.</span></span> <span data-ttu-id="f4875-140">但是，您可以选择早于路线上的“起始”日期的“起始”日期。</span><span class="sxs-lookup"><span data-stu-id="f4875-140">However, you can select a "from" date that is earlier than the "from" date on the route.</span></span> <span data-ttu-id="f4875-141">当建议负荷时，将检查所有未结销售订单的交货地址和交货日期。</span><span class="sxs-lookup"><span data-stu-id="f4875-141">When a load is proposed, the delivery address and delivery date of all open sales orders are checked.</span></span> <span data-ttu-id="f4875-142">如果交货地址的邮政编码与路线计划中的枢纽邮政编码匹配，且如果交货日期是在条件中选择的范围内，将为负荷建议销售订单。</span><span class="sxs-lookup"><span data-stu-id="f4875-142">If the postal code of the delivery address matches the postal code of a hub in the route plan, and if the delivery date is within the range that is selected in the criteria, the sales order is proposed for the load.</span></span> <span data-ttu-id="f4875-143">此外还考虑负荷模板的产能。</span><span class="sxs-lookup"><span data-stu-id="f4875-143">The capacity of the load template is also considered.</span></span> <span data-ttu-id="f4875-144">一次只建议一个负荷。</span><span class="sxs-lookup"><span data-stu-id="f4875-144">Only one load is proposed at a time.</span></span> <span data-ttu-id="f4875-145">如果您有不包含的销售订单，您可能必须使用不同的负荷模板（例如，更大的卡车或集装箱的负荷模板），或者计划额外交货。</span><span class="sxs-lookup"><span data-stu-id="f4875-145">If you have a sales order that isn't included, you might have to use a different load template (for example, a load template for a bigger truck or container) or plan an extra delivery.</span></span>




