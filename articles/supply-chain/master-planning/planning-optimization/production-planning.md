---
title: 生产计划
description: 本主题介绍生产计划，并说明如何使用计划优化来修改计划的生产订单。
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: eda22aa6f1e8d665d8ef390f24b247a76d4c2956
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992387"
---
# <a name="production-planning"></a><span data-ttu-id="1c42a-103">生产计划</span><span class="sxs-lookup"><span data-stu-id="1c42a-103">Production planning</span></span>

<span data-ttu-id="1c42a-104">计划优化支持多个生产场景。</span><span class="sxs-lookup"><span data-stu-id="1c42a-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="1c42a-105">如果要从现有的内置主计划引擎迁移，请注意某些变更的行为，这一点很重要。</span><span class="sxs-lookup"><span data-stu-id="1c42a-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<!-- The following video gives a short introduction to some of the current capabilities. 
KFM: Link to video for production functionality, coming soon... -->

## <a name="planned-production-orders"></a><span data-ttu-id="1c42a-106">计划生产订单</span><span class="sxs-lookup"><span data-stu-id="1c42a-106">Planned production orders</span></span>

<span data-ttu-id="1c42a-107">当主计划创建计划订单以满足要求时，订单类型由 **计划订单类型** 字段的值确定。</span><span class="sxs-lookup"><span data-stu-id="1c42a-107">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="1c42a-108">如果 **计划订单类型** 字段设置为 *生产*，将创建计划生产订单。</span><span class="sxs-lookup"><span data-stu-id="1c42a-108">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="1c42a-109">这些计划生产订单包括有关有效物料清单 (BOM) 和来自相关生产设置的工艺路线 ID 的信息。</span><span class="sxs-lookup"><span data-stu-id="1c42a-109">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="1c42a-110">BOM 的要求</span><span class="sxs-lookup"><span data-stu-id="1c42a-110">Requirements from BOMs</span></span>

<span data-ttu-id="1c42a-111">主计划过程中会采用 BOM 信息。</span><span class="sxs-lookup"><span data-stu-id="1c42a-111">BOM information is honored during master planning.</span></span> <span data-ttu-id="1c42a-112">计划输出包括材料供应，以满足生产的相关材料需求。</span><span class="sxs-lookup"><span data-stu-id="1c42a-112">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="1c42a-113">在主计划期间，当前有效的 BOM 用于确定生产所需的材料。</span><span class="sxs-lookup"><span data-stu-id="1c42a-113">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="1c42a-114">此步骤在与所需生产订单相关的 BOM 结构的所有级别完成。</span><span class="sxs-lookup"><span data-stu-id="1c42a-114">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="1c42a-115">材料要求通过使用可用的现有库存量、现有的按订购供应和经过审核的计划订单来满足。</span><span class="sxs-lookup"><span data-stu-id="1c42a-115">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="1c42a-116">如果有任何地方需要其他材料，将创建计划订单来满足需求。</span><span class="sxs-lookup"><span data-stu-id="1c42a-116">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="1c42a-117">确认期间的计划</span><span class="sxs-lookup"><span data-stu-id="1c42a-117">Scheduling during firming</span></span>

<span data-ttu-id="1c42a-118">计划生产订单包括生产计划所需的工艺路线 ID。</span><span class="sxs-lookup"><span data-stu-id="1c42a-118">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="1c42a-119">但是，计划运行期间对计划订单的计划支持还未确定。</span><span class="sxs-lookup"><span data-stu-id="1c42a-119">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="1c42a-120">工艺路线 ID 用于在确认期间对计划生产订单进行计划。</span><span class="sxs-lookup"><span data-stu-id="1c42a-120">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="1c42a-121">因此，计划生产订单的提前期可能不同于从其生成的相关的已确认计划生产订单的提前期，如下所述：</span><span class="sxs-lookup"><span data-stu-id="1c42a-121">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="1c42a-122">**计划生产订单** – 提前期基于已发布产品的静态提前期。</span><span class="sxs-lookup"><span data-stu-id="1c42a-122">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="1c42a-123">**已确认生产订单** – 提前期基于使用工艺路线信息和相关资源约束的计划。</span><span class="sxs-lookup"><span data-stu-id="1c42a-123">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="1c42a-124">有关预期功能可用性的详细信息，请参阅[计划优化适应分析](planning-optimization-fit-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="1c42a-124">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="1c42a-125">如果您依赖于计划优化还不可用的生产功能，您可以继续使用内置的主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="1c42a-125">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="1c42a-126">不需要处理异常。</span><span class="sxs-lookup"><span data-stu-id="1c42a-126">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="1c42a-127">延迟</span><span class="sxs-lookup"><span data-stu-id="1c42a-127">Delays</span></span>

<span data-ttu-id="1c42a-128">如果所需材料的提前期长于今天的日期和材料要求日期之间的期间，所需材料的计划订单和相关生产订单将延迟。</span><span class="sxs-lookup"><span data-stu-id="1c42a-128">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="1c42a-129">对于计划订单，延迟（以天为单位）根据已发布产品的提前期计算。</span><span class="sxs-lookup"><span data-stu-id="1c42a-129">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="1c42a-130">延迟信息然后传播到 BOM 结构的所有级别。</span><span class="sxs-lookup"><span data-stu-id="1c42a-130">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="1c42a-131">因此，您可以一直关注延迟原材料对客户销售订单的影响。</span><span class="sxs-lookup"><span data-stu-id="1c42a-131">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="1c42a-132">修改计划订单</span><span class="sxs-lookup"><span data-stu-id="1c42a-132">Modifying planned orders</span></span>

<span data-ttu-id="1c42a-133">当您更改计划订单的信息时，您会收到以下消息：“请注意，在运行下一个主计划之前，对计划订单的手动更改的影响不会反映在计划的剩余部分中。”</span><span class="sxs-lookup"><span data-stu-id="1c42a-133">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="1c42a-134">如果要更改计划订单上的信息并查看对相关材料要求的影响，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="1c42a-134">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="1c42a-135">更新计划订单。</span><span class="sxs-lookup"><span data-stu-id="1c42a-135">Update the planned order.</span></span>
2. <span data-ttu-id="1c42a-136">审核计划订单。</span><span class="sxs-lookup"><span data-stu-id="1c42a-136">Approve the planned order.</span></span>
3. <span data-ttu-id="1c42a-137">运行主计划。</span><span class="sxs-lookup"><span data-stu-id="1c42a-137">Run master planning.</span></span>

<span data-ttu-id="1c42a-138">运行主计划时，如果包含计划生产订单，则不应使用筛选器。</span><span class="sxs-lookup"><span data-stu-id="1c42a-138">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="1c42a-139">有关详细信息，请参阅本主题后面的[筛选器](#filters)一节。</span><span class="sxs-lookup"><span data-stu-id="1c42a-139">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="1c42a-140">如果计划订单的交货日期更改为以后的日期，可能会根据新计划订单对需求加以限定。</span><span class="sxs-lookup"><span data-stu-id="1c42a-140">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="1c42a-141">当新供应日期导致限定需求出现延迟，但是根据提前期设置，可以避免这一延迟，这时会发生此行为。</span><span class="sxs-lookup"><span data-stu-id="1c42a-141">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="1c42a-142">分解页</span><span class="sxs-lookup"><span data-stu-id="1c42a-142">Explosion page</span></span>

<span data-ttu-id="1c42a-143">您可以使用 **分解** 页分析特定生产订单或计划生产订单所需的需求、相关的覆盖范围以及限定标准信息。</span><span class="sxs-lookup"><span data-stu-id="1c42a-143">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="1c42a-144">**分解** 页上的信息在主计划期间更新。</span><span class="sxs-lookup"><span data-stu-id="1c42a-144">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="1c42a-145">您不能直接从 **分解** 页更新信息。</span><span class="sxs-lookup"><span data-stu-id="1c42a-145">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="1c42a-146">筛选器</span><span class="sxs-lookup"><span data-stu-id="1c42a-146">Filters</span></span>

<span data-ttu-id="1c42a-147">对于包含生产的计划场景，我们建议您不要筛选主计划运行。</span><span class="sxs-lookup"><span data-stu-id="1c42a-147">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="1c42a-148">为确保计划优化具有计算正确结果所需的信息，您必须在计划订单的整个 BOM 结构中包括与产品有任何关系的所有产品。</span><span class="sxs-lookup"><span data-stu-id="1c42a-148">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="1c42a-149">虽然使用内置的主计划引擎时会自动检测到依赖子项并将其包括在主计划运行中，但是计划优化不会执行此操作。</span><span class="sxs-lookup"><span data-stu-id="1c42a-149">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="1c42a-150">例如，如果产品 A 的 BOM 结构中的单个螺栓还用于生产产品 B，产品 A 和 B 的 BOM 结构中的所有产品都必须包含在筛选器中。</span><span class="sxs-lookup"><span data-stu-id="1c42a-150">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="1c42a-151">因为要确保所有产品都是筛选器的一部分可能非常复杂，所以我们建议在涉及生产订单时避免发生筛选后的主计划运行。</span><span class="sxs-lookup"><span data-stu-id="1c42a-151">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>
