---
title: 分配的订单管理 (DOM) 的成本配置
description: 本主题将介绍 Dynamics 365 Commerce 中分配的订单管理 (DOM) 功能的成本配置。
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458498"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="b6a6d-103">分配的订单管理 (DOM) 的成本配置</span><span class="sxs-lookup"><span data-stu-id="b6a6d-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6a6d-104">组织需要考虑多个成本构成以确定履行订单的最佳位置。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="b6a6d-105">其中一些成本构成是装运成本、处理成本和包装成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="b6a6d-106">通过计算这些成本的组合来确定履行位置。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="b6a6d-107">Dynamics 365 Commerce 中分布的订单管理 (DOM) 的第一次迭代在优化履行位置的订单分配时，只考虑距离因素。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="b6a6d-108">虽然距离与成本相关，但不同于成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="b6a6d-109">例如，对于相同距离，连夜装运方式的成本要高于三日装运或七日装运。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="b6a6d-110">成本配置功能让零售商可以定义和配置其他需要计算并考虑在内的成本构成，用于确定履行订单行的最佳位置。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="b6a6d-111">在配置了成本构成时，DOM 求解器仅使用这些成本定义来确定订单履行的最佳位置。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="b6a6d-112">它不将距离构成视为成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="b6a6d-113">但是，如果没有配置成本构成，DOM 求解器就会使用距离构成作为成本，用于确定订单履行的最佳位置。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="b6a6d-114">设置成本构成</span><span class="sxs-lookup"><span data-stu-id="b6a6d-114">Set up cost components</span></span>

<span data-ttu-id="b6a6d-115">在系统中可以定义两个主要成本构成类型：**装运** 和 **其他**。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="b6a6d-116">两个成本构成类型均支持多个计算依据，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b6a6d-117">成本构成类型</span><span class="sxs-lookup"><span data-stu-id="b6a6d-117">Cost component type</span></span></th>
<th><span data-ttu-id="b6a6d-118">计算依据</span><span class="sxs-lookup"><span data-stu-id="b6a6d-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b6a6d-119">装运</span><span class="sxs-lookup"><span data-stu-id="b6a6d-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b6a6d-120">简单</span><span class="sxs-lookup"><span data-stu-id="b6a6d-120">Simple</span></span></li>
<li><span data-ttu-id="b6a6d-121">分层</span><span class="sxs-lookup"><span data-stu-id="b6a6d-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="b6a6d-122">其他</span><span class="sxs-lookup"><span data-stu-id="b6a6d-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="b6a6d-123">销售订单</span><span class="sxs-lookup"><span data-stu-id="b6a6d-123">Sales order</span></span></li>
<li><span data-ttu-id="b6a6d-124">销售行</span><span class="sxs-lookup"><span data-stu-id="b6a6d-124">Sales line</span></span></li>
<li><span data-ttu-id="b6a6d-125">位置</span><span class="sxs-lookup"><span data-stu-id="b6a6d-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="b6a6d-126">装运成本构成类型</span><span class="sxs-lookup"><span data-stu-id="b6a6d-126">Shipping cost component type</span></span>

<span data-ttu-id="b6a6d-127">本节说明如何设置 **装运** 成本构成类型与装运成本计算依据的各种组合。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="b6a6d-128">它还介绍了 DOM 求解器如何使用各个组合。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="b6a6d-129">成本构成类型 = 装运，计算依据 = 简单</span><span class="sxs-lookup"><span data-stu-id="b6a6d-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="b6a6d-130">如果使用 **装运** 成本构成类型和 **简单** 计算依据组合，则交货方式的装运成本基于净成本或距离。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="b6a6d-131">您必须为此组合设置下列字段：</span><span class="sxs-lookup"><span data-stu-id="b6a6d-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="b6a6d-132">**成本系数** - 输入成本系数的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="b6a6d-133">**描述** - 输入成本系数的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="b6a6d-134">**开始日期** 和 **结束日期** - 您可以使用这些字段限制特定日期范围的成本系数。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="b6a6d-135">如果将这些字段留空，则成本系数将无限期有效。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="b6a6d-136">**有效** - 指示成本系数是否有效。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="b6a6d-137">DOM 仅考虑与履行配置文件关联的有效成本系数。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="b6a6d-138">**公司** - 指定为其配置成本系数的法人。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="b6a6d-139">计算条件的所有行必须针对相同法人。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="b6a6d-140">**交货方式** - 指定为其配置成本的交货方式。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="b6a6d-141">**计算类型** - 指定应该如何为特定交货方式计算成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="b6a6d-142">支持两种计算类型：</span><span class="sxs-lookup"><span data-stu-id="b6a6d-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="b6a6d-143">**固定** - 为交货方式使用净成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="b6a6d-144">如果选择此计算类型，**成本** 字段定义净成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="b6a6d-145">**每距离单位** - 交货方式成本的计算方式为，在 **成本** 字段中指定的成本值乘以交货地址与交货位置之间的距离。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="b6a6d-146">**成本** - 指定与 **计算类型** 字段一起用于计算交货方式成本的成本值。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="b6a6d-147">成本构成类型 = 装运，计算依据 = 分层</span><span class="sxs-lookup"><span data-stu-id="b6a6d-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="b6a6d-148">如果使用 **装运** 成本构成类型和 **分层** 计算依据组合，则交货方式的装运成本基于净成本或距离。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="b6a6d-149">但是，在此组合中，距离基于分层的距离范围。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="b6a6d-150">您必须为此组合设置下列字段：</span><span class="sxs-lookup"><span data-stu-id="b6a6d-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="b6a6d-151">**成本系数** - 输入成本系数的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="b6a6d-152">**描述** - 输入成本系数的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="b6a6d-153">**默认成本** - 指定在交货地址与交货位置之间的距离不在交货方式的任意分层距离之内时，应该为交货方式使用的成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="b6a6d-154">**开始日期** 和 **结束日期** - 您可以使用这些字段限制特定日期范围的成本系数。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="b6a6d-155">如果将这些字段留空，则成本系数将无限期有效。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="b6a6d-156">**有效** - 指示成本系数是否有效。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="b6a6d-157">DOM 仅考虑与履行配置文件关联的有效成本系数。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="b6a6d-158">**公司** - 指定为其配置成本系数的法人。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="b6a6d-159">计算条件的所有行必须针对相同法人。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="b6a6d-160">**交货方式** - 指定为其配置成本的交货方式。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="b6a6d-161">**距离类型** - 指定分层距离定义是航空距离还是公路距离。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="b6a6d-162">**距离单位** - 指定衡量分层距离所用的单位。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="b6a6d-163">**起始距离** - 指定分层距离的开始范围。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="b6a6d-164">**结束距离** - 指定分层距离的结束范围。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="b6a6d-165">**计算类型** - 指定应该如何为特定交货方式和分层距离计算成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="b6a6d-166">支持两种计算类型：</span><span class="sxs-lookup"><span data-stu-id="b6a6d-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="b6a6d-167">**固定** - 为交货方式使用净成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="b6a6d-168">如果选择此计算类型，**成本** 字段定义净成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="b6a6d-169">**每距离单位** - 交货方式和分层距离成本的计算方式为，在 **成本** 字段中指定的成本值乘以交货地址与交货位置之间的距离。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="b6a6d-170">**成本** - 指定与 **计算类型** 字段一起用于计算交货方式成本的成本值。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="b6a6d-171">在您定义分层距离时，系统会验证没有缺少或重叠的距离。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="b6a6d-172">为交货方式使用的距离类型必须在所有分层距离中相同。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="b6a6d-173">其他成本构成类型</span><span class="sxs-lookup"><span data-stu-id="b6a6d-173">Other cost component type</span></span>

<span data-ttu-id="b6a6d-174">本节说明如何设置 **其他** 成本构成类型与非装运成本的其他成本类型的各种组合。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="b6a6d-175">它还介绍了 DOM 求解器如何使用各个组合。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="b6a6d-176">成本构成类型 = 其他，其他成本类型 = 销售订单</span><span class="sxs-lookup"><span data-stu-id="b6a6d-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="b6a6d-177">**其他** 成本构成类型与 **销售订单** 其他成本类型的组合用于在销售订单级别定义非装运成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="b6a6d-178">您必须为此组合设置下列字段：</span><span class="sxs-lookup"><span data-stu-id="b6a6d-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="b6a6d-179">**成本系数** - 输入成本系数的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="b6a6d-180">**描述** - 输入成本系数的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="b6a6d-181">**开始日期** 和 **结束日期** - 您可以使用这些字段限制特定日期范围的成本系数。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="b6a6d-182">如果将这些字段留空，则成本系数将无限期有效。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="b6a6d-183">**有效** - 指示成本系数是否有效。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="b6a6d-184">DOM 仅考虑与履行配置文件关联的有效成本系数。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="b6a6d-185">**成本** - 在销售订单级别指定非装运成本的成本值。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="b6a6d-186">成本构成类型 = 其他，其他成本类型 = 销售行</span><span class="sxs-lookup"><span data-stu-id="b6a6d-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="b6a6d-187">**其他** 成本构成类型与 **销售行** 其他成本类型的组合用于在销售订单行级别定义非装运成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="b6a6d-188">您必须为此组合设置下列字段：</span><span class="sxs-lookup"><span data-stu-id="b6a6d-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="b6a6d-189">**成本系数** - 输入成本系数的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="b6a6d-190">**描述** - 输入成本系数的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="b6a6d-191">**开始日期** 和 **结束日期** - 您可以使用这些字段限制特定日期范围的成本系数。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="b6a6d-192">如果将这些字段留空，则成本系数将无限期有效。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="b6a6d-193">**有效** - 指示成本系数是否有效。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="b6a6d-194">DOM 仅考虑与履行配置文件关联的有效成本系数。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="b6a6d-195">**成本** - 在销售订单行级别指定非装运成本的成本值。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="b6a6d-196">成本构成类型 = 其他，其他成本类型 = 位置</span><span class="sxs-lookup"><span data-stu-id="b6a6d-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="b6a6d-197">**其他** 成本构成类型与 **位置** 其他成本类型的组合用于定义一组位置或单个位置的非装运成本。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="b6a6d-198">您必须为此组合设置下列字段：</span><span class="sxs-lookup"><span data-stu-id="b6a6d-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="b6a6d-199">**成本系数** - 输入成本系数的唯一标识符。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="b6a6d-200">**描述** - 输入成本系数的名称和描述。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="b6a6d-201">**开始日期** 和 **结束日期** - 您可以使用这些字段限制特定日期范围的成本系数。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="b6a6d-202">如果将这些字段留空，则成本系数将无限期有效。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="b6a6d-203">**有效** - 指示成本系数是否有效。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="b6a6d-204">DOM 仅考虑与履行配置文件关联的有效成本系数。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="b6a6d-205">**履行组** - 指定为其定义非装运成本的一组位置。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="b6a6d-206">**履行位置** - 指定为其定义非装运成本的位置。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b6a6d-207">您不能为基于位置的计算标准在同一行上指定履行组和履行位置。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="b6a6d-208">**成本** - 在履行组级别或履行位置级别为非装运成本指定成本值。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6a6d-209">要在运行时使 DOM 考虑这些成本，您必须将成本系数添加到相关履行配置文件。</span><span class="sxs-lookup"><span data-stu-id="b6a6d-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
