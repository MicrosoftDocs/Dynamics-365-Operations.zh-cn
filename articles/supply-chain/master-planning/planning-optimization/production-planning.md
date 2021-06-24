---
title: 生产计划
description: 本主题介绍生产计划，并说明如何使用计划优化来修改计划的生产订单。
author: ChristianRytt
ms.date: 06/01/2021
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ffee79f152141297ceb24e2d7a40523eac18ffaf
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129745"
---
# <a name="production-planning"></a><span data-ttu-id="8a77b-103">生产计划</span><span class="sxs-lookup"><span data-stu-id="8a77b-103">Production planning</span></span>

<span data-ttu-id="8a77b-104">计划优化支持多个生产场景。</span><span class="sxs-lookup"><span data-stu-id="8a77b-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="8a77b-105">如果要从现有的内置主计划引擎迁移，请注意某些变更的行为，这一点很重要。</span><span class="sxs-lookup"><span data-stu-id="8a77b-105">If you're migrating from the existing, built-in master planning engine, it's important to be aware of some changed behavior.</span></span>

<span data-ttu-id="8a77b-106">以下视频简要介绍了本主题中讨论的一些概念：[Dynamics 365 Supply Chain Management：计划优化增强](https://youtu.be/u1pcmZuZBTw)。</span><span class="sxs-lookup"><span data-stu-id="8a77b-106">The following video gives a short introduction to some of the concepts discussed in this topic: [Dynamics 365 Supply Chain Management: Planning Optimization enhancements](https://youtu.be/u1pcmZuZBTw).</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="8a77b-107">为您的系统启用此功能</span><span class="sxs-lookup"><span data-stu-id="8a77b-107">Turn on this feature for your system</span></span>

<span data-ttu-id="8a77b-108">如果您的系统尚未包含本主题中所述的功能，请转到 [功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，打开 *计划优化的计划生产订单* 功能。</span><span class="sxs-lookup"><span data-stu-id="8a77b-108">If your system doesn't already include the features described in this topic, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Planned production orders for Planning Optimization* feature.</span></span>

## <a name="planned-production-orders"></a><span data-ttu-id="8a77b-109">计划生产订单</span><span class="sxs-lookup"><span data-stu-id="8a77b-109">Planned production orders</span></span>

<span data-ttu-id="8a77b-110">当主计划创建计划订单以满足要求时，订单类型由 **计划订单类型** 字段的值确定。</span><span class="sxs-lookup"><span data-stu-id="8a77b-110">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="8a77b-111">如果 **计划订单类型** 字段设置为 *生产*，将创建计划生产订单。</span><span class="sxs-lookup"><span data-stu-id="8a77b-111">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="8a77b-112">这些计划生产订单包括有关有效物料清单 (BOM) 和来自相关生产设置的工艺路线 ID 的信息。</span><span class="sxs-lookup"><span data-stu-id="8a77b-112">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="8a77b-113">BOM 的要求</span><span class="sxs-lookup"><span data-stu-id="8a77b-113">Requirements from BOMs</span></span>

<span data-ttu-id="8a77b-114">主计划过程中会采用 BOM 信息。</span><span class="sxs-lookup"><span data-stu-id="8a77b-114">BOM information is honored during master planning.</span></span> <span data-ttu-id="8a77b-115">计划输出包括材料供应，以满足生产的相关材料需求。</span><span class="sxs-lookup"><span data-stu-id="8a77b-115">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="8a77b-116">在主计划期间，当前有效的 BOM 用于确定生产所需的材料。</span><span class="sxs-lookup"><span data-stu-id="8a77b-116">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="8a77b-117">此步骤在与所需生产订单相关的 BOM 结构的所有级别完成。</span><span class="sxs-lookup"><span data-stu-id="8a77b-117">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="8a77b-118">材料要求通过使用可用的现有库存量、现有的按订购供应和经过审核的计划订单来满足。</span><span class="sxs-lookup"><span data-stu-id="8a77b-118">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="8a77b-119">如果有任何地方需要其他材料，将创建计划订单来满足需求。</span><span class="sxs-lookup"><span data-stu-id="8a77b-119">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="8a77b-120">确认期间的计划</span><span class="sxs-lookup"><span data-stu-id="8a77b-120">Scheduling during firming</span></span>

<span data-ttu-id="8a77b-121">计划生产订单包括生产计划所需的工艺路线 ID。</span><span class="sxs-lookup"><span data-stu-id="8a77b-121">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="8a77b-122">但是，计划运行期间对计划订单的计划支持还未确定。</span><span class="sxs-lookup"><span data-stu-id="8a77b-122">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="8a77b-123">工艺路线 ID 用于在确认期间对计划生产订单进行计划。</span><span class="sxs-lookup"><span data-stu-id="8a77b-123">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="8a77b-124">因此，计划生产订单的提前期可能不同于从其生成的相关的已确认计划生产订单的提前期，如下所述：</span><span class="sxs-lookup"><span data-stu-id="8a77b-124">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="8a77b-125">**计划生产订单** – 提前期基于已发布产品的静态提前期。</span><span class="sxs-lookup"><span data-stu-id="8a77b-125">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="8a77b-126">**已确认生产订单** – 提前期基于使用工艺路线信息和相关资源约束的计划。</span><span class="sxs-lookup"><span data-stu-id="8a77b-126">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="8a77b-127">有关预期功能可用性的详细信息，请参阅[计划优化适应分析](planning-optimization-fit-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="8a77b-127">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="8a77b-128">如果您依赖于计划优化还不可用的生产功能，您可以继续使用内置的主计划引擎。</span><span class="sxs-lookup"><span data-stu-id="8a77b-128">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="8a77b-129">不需要处理异常。</span><span class="sxs-lookup"><span data-stu-id="8a77b-129">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="8a77b-130">延迟</span><span class="sxs-lookup"><span data-stu-id="8a77b-130">Delays</span></span>

<span data-ttu-id="8a77b-131">如果所需材料的提前期长于今天的日期和材料要求日期之间的期间，所需材料的计划订单和相关生产订单将延迟。</span><span class="sxs-lookup"><span data-stu-id="8a77b-131">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="8a77b-132">对于计划订单，延迟（以天为单位）根据已发布产品的提前期计算。</span><span class="sxs-lookup"><span data-stu-id="8a77b-132">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="8a77b-133">延迟信息然后传播到 BOM 结构的所有级别。</span><span class="sxs-lookup"><span data-stu-id="8a77b-133">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="8a77b-134">因此，您可以一直关注延迟原材料对客户销售订单的影响。</span><span class="sxs-lookup"><span data-stu-id="8a77b-134">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="8a77b-135">修改计划订单</span><span class="sxs-lookup"><span data-stu-id="8a77b-135">Modifying planned orders</span></span>

<span data-ttu-id="8a77b-136">当您更改计划订单的信息时，您会收到以下消息：“请注意，在运行下一个主计划之前，对计划订单的手动更改的影响不会反映在计划的剩余部分中。”</span><span class="sxs-lookup"><span data-stu-id="8a77b-136">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="8a77b-137">如果要更改计划订单上的信息并查看对相关材料要求的影响，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="8a77b-137">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="8a77b-138">更新计划订单。</span><span class="sxs-lookup"><span data-stu-id="8a77b-138">Update the planned order.</span></span>
2. <span data-ttu-id="8a77b-139">审核计划订单。</span><span class="sxs-lookup"><span data-stu-id="8a77b-139">Approve the planned order.</span></span>
3. <span data-ttu-id="8a77b-140">运行主计划。</span><span class="sxs-lookup"><span data-stu-id="8a77b-140">Run master planning.</span></span>

<span data-ttu-id="8a77b-141">运行主计划时，如果包含计划生产订单，则不应使用筛选器。</span><span class="sxs-lookup"><span data-stu-id="8a77b-141">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="8a77b-142">有关详细信息，请参阅本主题后面的[筛选器](#filters)一节。</span><span class="sxs-lookup"><span data-stu-id="8a77b-142">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="8a77b-143">如果计划订单的交货日期更改为以后的日期，可能会根据新计划订单对需求加以限定。</span><span class="sxs-lookup"><span data-stu-id="8a77b-143">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="8a77b-144">当新供应日期导致限定需求出现延迟，但是根据提前期设置，可以避免这一延迟，这时会发生此行为。</span><span class="sxs-lookup"><span data-stu-id="8a77b-144">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="8a77b-145">分解页</span><span class="sxs-lookup"><span data-stu-id="8a77b-145">Explosion page</span></span>

<span data-ttu-id="8a77b-146">您可以使用 **分解** 页分析特定生产订单或计划生产订单所需的需求、相关的覆盖范围以及限定标准信息。</span><span class="sxs-lookup"><span data-stu-id="8a77b-146">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="8a77b-147">**分解** 页上的信息在主计划期间更新。</span><span class="sxs-lookup"><span data-stu-id="8a77b-147">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="8a77b-148">您不能直接从 **分解** 页更新信息。</span><span class="sxs-lookup"><span data-stu-id="8a77b-148">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="8a77b-149">筛选器</span><span class="sxs-lookup"><span data-stu-id="8a77b-149">Filters</span></span>

<span data-ttu-id="8a77b-150">若要确保计划优化具有计算正确结果所需的信息，您必须在计划订单的整个 BOM 结构中包括与产品有任何关系的所有产品。</span><span class="sxs-lookup"><span data-stu-id="8a77b-150">To ensure that Planning Optimization has the information that it needs to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span> <span data-ttu-id="8a77b-151">对于包含生产的计划场景，我们建议您不要筛选主计划运行。</span><span class="sxs-lookup"><span data-stu-id="8a77b-151">For planning scenarios that include production, we therefore recommend that you avoid filtered master planning runs.</span></span>

<span data-ttu-id="8a77b-152">虽然使用内置的主计划引擎时会自动检测到依赖子项并将其包括在主计划运行中，但是计划优化当前不会执行此操作。</span><span class="sxs-lookup"><span data-stu-id="8a77b-152">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't currently perform this action.</span></span>

<span data-ttu-id="8a77b-153">例如，如果产品 A 的 BOM 结构中的单个螺栓还用于生产产品 B，产品 A 和 B 的 BOM 结构中的所有产品都必须包含在筛选器中。</span><span class="sxs-lookup"><span data-stu-id="8a77b-153">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="8a77b-154">因为要确保所有产品都是筛选器的一部分可能非常复杂，所以我们建议在涉及生产订单时避免发生筛选后的主计划运行。</span><span class="sxs-lookup"><span data-stu-id="8a77b-154">Because it can be complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span> <span data-ttu-id="8a77b-155">否则，主计划将产生不需要的结果。</span><span class="sxs-lookup"><span data-stu-id="8a77b-155">Otherwise, master planning will provide undesired results.</span></span>

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a><span data-ttu-id="8a77b-156">避免发生筛选后的主计划运行的原因</span><span class="sxs-lookup"><span data-stu-id="8a77b-156">Reasons to avoid filtered master planning runs</span></span>

<span data-ttu-id="8a77b-157">当您为产品运行筛选的主计划时，计划优化（与内置的主计划引擎不同）不会检测到该产品的 BOM 结构中的所有子产品和原材料，因此不会将它们包括在主计划运行中。</span><span class="sxs-lookup"><span data-stu-id="8a77b-157">When you run filtered master planning for a product, Planning Optimization (unlike the built-in master planning engine) doesn't detect all the subproducts and raw materials in the BOM structure of that product, and therefore doesn't include them in the master planning run.</span></span> <span data-ttu-id="8a77b-158">即使计划优化标识产品的 BOM 结构中的第一级，它也不会从数据库加载任何产品设置（例如，默认订单类型或物料范围）。</span><span class="sxs-lookup"><span data-stu-id="8a77b-158">Even though Planning Optimization identifies the first level in the BOM structure of the product, it doesn't load any product settings (such as the default order type or item coverage) from the database.</span></span>

<span data-ttu-id="8a77b-159">在计划优化中，运行的数据将预先加载并应用筛选器。</span><span class="sxs-lookup"><span data-stu-id="8a77b-159">In Planning Optimization, data for the run is loaded beforehand and applies the filters.</span></span> <span data-ttu-id="8a77b-160">这意味着，如果包含在特定产品中的子产品或原材料不是筛选器的一部分，则不会为运行捕获与之相关的信息。</span><span class="sxs-lookup"><span data-stu-id="8a77b-160">This means that if a subproduct or raw material included in a specific product isn't part of the filter, information about it won't be captured for the run.</span></span> <span data-ttu-id="8a77b-161">此外，如果子产品或原材料也包含在另一个产品中，则仅包含原始产品及其组件的筛选后运行将删除为该其他产品创建的现有计划需求。</span><span class="sxs-lookup"><span data-stu-id="8a77b-161">Additionally, if the subproduct or raw material is also included in another product, then a filtered run that includes only the original product and its components would remove existing planned demand that was created for that other product.</span></span>

<span data-ttu-id="8a77b-162">此逻辑可能会导致筛选后的主计划运行产生意外结果。</span><span class="sxs-lookup"><span data-stu-id="8a77b-162">This logic may cause filtered master planning runs to produce unexpected results.</span></span> <span data-ttu-id="8a77b-163">以下部分提供了说明可能发生的意外结果的示例。</span><span class="sxs-lookup"><span data-stu-id="8a77b-163">The following sections provide examples that illustrate the unexpected results that could occur.</span></span>

### <a name="example-1"></a><span data-ttu-id="8a77b-164">示例 1</span><span class="sxs-lookup"><span data-stu-id="8a77b-164">Example 1</span></span>

<span data-ttu-id="8a77b-165">成品 *FG* 由以下组件组成：</span><span class="sxs-lookup"><span data-stu-id="8a77b-165">Finished good *FG* consists of following components:</span></span>

- <span data-ttu-id="8a77b-166">原材料 *R*</span><span class="sxs-lookup"><span data-stu-id="8a77b-166">Raw material *R*</span></span>
- <span data-ttu-id="8a77b-167">子产品 *S1*，由子产品 *S2* 组成</span><span class="sxs-lookup"><span data-stu-id="8a77b-167">Subproduct *S1*, which consists of subproduct *S2*</span></span>

<span data-ttu-id="8a77b-168">原材料 *R* 具有现有库存，而子产品 *S1* 没有库存。</span><span class="sxs-lookup"><span data-stu-id="8a77b-168">There is inventory on-hand for the raw material *R*, while subproduct *S1* isn't present in the inventory.</span></span>

<span data-ttu-id="8a77b-169">当您为成品 *FG* 执行筛选后的主计划运行时，您将获得成品 *FG* 的计划生产订单、原材料 *R* 的计划采购订单和子产品 *S1* 的计划采购订单。</span><span class="sxs-lookup"><span data-stu-id="8a77b-169">When you do a filtered master planning run for finished good *FG*, you will get a planned production order for the finished good *FG*, a planned purchase order for the raw material *R*, and a planned purchase order for the subproduct *S1*.</span></span> <span data-ttu-id="8a77b-170">这是一个不想要的结果，因为计划优化忽略了需要使用 *S2* 而不是直接订购生产的原材料 *R* 和子产品 *S1* 的现有供应。</span><span class="sxs-lookup"><span data-stu-id="8a77b-170">This is an undesirable result because Planning Optimization has ignored existing supply for raw material *R* and subproduct *S1* needs to be produced using *S2* rather than ordered directly.</span></span> <span data-ttu-id="8a77b-171">发生这种情况是因为计划优化只有成品 *FG* 的组件列表，而没有任何相关信息，例如其组件或其默认订单设置的现有供应。</span><span class="sxs-lookup"><span data-stu-id="8a77b-171">This happened because Planning Optimization only has the list of components for the finished good *FG* without any related information, such as the existing supply of its components or their default order settings.</span></span>

### <a name="example-2"></a><span data-ttu-id="8a77b-172">示例 2</span><span class="sxs-lookup"><span data-stu-id="8a77b-172">Example 2</span></span>

<span data-ttu-id="8a77b-173">基于前面的示例，一个额外的成品 *FG2* 也使用子产品 *S1*。</span><span class="sxs-lookup"><span data-stu-id="8a77b-173">Building on the previous example, an additional finished good, *FG2*, also uses subproduct *S1*.</span></span> <span data-ttu-id="8a77b-174">成品 *FG2* 存在计划的订单，其所有组件（包括 *S1*）存在计划的需求。</span><span class="sxs-lookup"><span data-stu-id="8a77b-174">A planned order exists for finished good *FG2* and planned demand exists for all of its components, including *S1*.</span></span>

<span data-ttu-id="8a77b-175">您决定通过将成品 *FG* 的 BOM 结构中的所有子产品和原材料添加到筛选器，然后运行完全重新生成，克服前面示例中筛选后的主计划运行产生的不想要结果。</span><span class="sxs-lookup"><span data-stu-id="8a77b-175">You decide to overcome the undesired results of the filtered master planning run from the previous example by adding all the subproducts and raw materials from the BOM structure of finished good *FG* to the filter and then running full regeneration.</span></span>

<span data-ttu-id="8a77b-176">当您运行完全重新生成时，系统会删除所有包含产品的所有现有结果，然后根据新计算重新创建结果。</span><span class="sxs-lookup"><span data-stu-id="8a77b-176">When you run the full regeneration, the system deletes all existing results for all the included products and then recreates results based on the new calculations.</span></span> <span data-ttu-id="8a77b-177">这意味着产品 *S1* 的现有计划需求将删除，然后考虑仅重新创建成品 *FG* 需求，而成品 *FG2* 需求将忽略。</span><span class="sxs-lookup"><span data-stu-id="8a77b-177">This means that existing planned demand for product *S1* is deleted and then recreated taking into account finished good *FG* requirements only, while finished good *FG2* requirements are disregarded.</span></span> <span data-ttu-id="8a77b-178">发生这种情况是因为当您运行计划优化时，它不包括其他计划生产订单的计划需求&mdash;仅使用运行期间生成的计划需求。</span><span class="sxs-lookup"><span data-stu-id="8a77b-178">This happens because when you run Planning Optimization, it doesn't include the planned demand of other planned production orders&mdash;only the planned demand generated during the run is used.</span></span>

> [!NOTE]
> <span data-ttu-id="8a77b-179">如果成品 *FG2* 的现有计划订单处于状态 *已批准* 下，将包括批准的计划需求，即使未将父产品添加到筛选器。</span><span class="sxs-lookup"><span data-stu-id="8a77b-179">If the existing planned order for finished good *FG2* is in status *Approved*, then the approved planned demand will be included, even when the parent product isn't added to the filter.</span></span>

<span data-ttu-id="8a77b-180">因此，除非您添加成品 *FG*、成品 *FG2* 和这些组件所属的所有其他产品（连同其组件）的所有组件，否则筛选后的主计划运行将提供不想要的结果。</span><span class="sxs-lookup"><span data-stu-id="8a77b-180">Therefore, unless you add all the components of the finished good *FG*, finished good *FG2*, and all other products that these components are part of (together with their components), the filtered master planning run will provide undesired results.</span></span>

<span data-ttu-id="8a77b-181">因为要确保所有产品都是筛选器的一部分可能非常复杂，所以我们建议在涉及生产订单时避免发生筛选后的主计划运行。</span><span class="sxs-lookup"><span data-stu-id="8a77b-181">Because it can be complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
