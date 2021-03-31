---
title: 主计划疑难解答
description: 本主题介绍如何解决在使用主计划时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: db336946873fa1b5cc3f669823541af8cab4115b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216097"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="296c0-103">主计划疑难解答</span><span class="sxs-lookup"><span data-stu-id="296c0-103">Troubleshoot master planning</span></span>

<span data-ttu-id="296c0-104">本主题介绍如何解决在使用主计划时可能遇到的问题。</span><span class="sxs-lookup"><span data-stu-id="296c0-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="296c0-105">物料清单分解行为对于确定的生产订单和人工创建工作的估计生产订单是不同的。</span><span class="sxs-lookup"><span data-stu-id="296c0-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="296c0-106">问题描述</span><span class="sxs-lookup"><span data-stu-id="296c0-106">Issue description</span></span>

<span data-ttu-id="296c0-107">生产订单确定后，物料在您分解物料清单 (BOM) 时不会分解。</span><span class="sxs-lookup"><span data-stu-id="296c0-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="296c0-108">但是，当您手动创建工作订单然后估计生产订单时，物料将被分解。</span><span class="sxs-lookup"><span data-stu-id="296c0-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="296c0-109">解决问题</span><span class="sxs-lookup"><span data-stu-id="296c0-109">Issue resolution</span></span>

<span data-ttu-id="296c0-110">系统按预期运行。</span><span class="sxs-lookup"><span data-stu-id="296c0-110">The system is working as expected.</span></span> <span data-ttu-id="296c0-111">确定生产订单时发生的分解将指向计划订单，但似乎计划订单在这种情况下目前不会确定。</span><span class="sxs-lookup"><span data-stu-id="296c0-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="296c0-112">但是，如果已经估计了生产订单，分解将从不存在计划订单的已下达生产订单触发。</span><span class="sxs-lookup"><span data-stu-id="296c0-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="296c0-113">当我重新计划计划订单时，延迟值不更新。</span><span class="sxs-lookup"><span data-stu-id="296c0-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="296c0-114">要更新计划订单的延迟，请打开计划订单的 **重新计划** 对话框。</span><span class="sxs-lookup"><span data-stu-id="296c0-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="296c0-115">在 **分解** 快速选项卡上，确保将 **重新计划后执行分解** 选项设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="296c0-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="296c0-116">生产计划不会考虑在限定供应的物料覆盖范围上设置的安全宽限期。</span><span class="sxs-lookup"><span data-stu-id="296c0-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="296c0-117">问题描述</span><span class="sxs-lookup"><span data-stu-id="296c0-117">Issue description</span></span>

<span data-ttu-id="296c0-118">主计划会考虑安全宽限期。</span><span class="sxs-lookup"><span data-stu-id="296c0-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="296c0-119">但是，安全宽限期会在计划生产订单时被忽略。</span><span class="sxs-lookup"><span data-stu-id="296c0-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="296c0-120">解决问题</span><span class="sxs-lookup"><span data-stu-id="296c0-120">Issue resolution</span></span>

<span data-ttu-id="296c0-121">仅在主计划期间考虑宽限期，手动计划期间不会考虑。</span><span class="sxs-lookup"><span data-stu-id="296c0-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="296c0-122">宽限期的目的是在计划阶段充当缓冲，为实际流程提供一定的“余地”。</span><span class="sxs-lookup"><span data-stu-id="296c0-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="296c0-123">要获得所需的结果，您可以删除宽限期。</span><span class="sxs-lookup"><span data-stu-id="296c0-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="296c0-124">然后必须更新工艺路线，使其包含所需的时间（例如，排队时间）。</span><span class="sxs-lookup"><span data-stu-id="296c0-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="296c0-125">然后，主计划和手动计划应该都会产生相同的结果。</span><span class="sxs-lookup"><span data-stu-id="296c0-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="296c0-126">计划订单将生成，即使我们在库存中有物料，并且它们已经存在生产订单。</span><span class="sxs-lookup"><span data-stu-id="296c0-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="296c0-127">您可以通过在 **覆盖范围组** 页上为相关组增加 **正天数** 值来解决此问题。</span><span class="sxs-lookup"><span data-stu-id="296c0-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="296c0-128">此更改会让系统确定现有库存量是否可用于需求。</span><span class="sxs-lookup"><span data-stu-id="296c0-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="296c0-129">之后就不会为库存中的物料生成新的计划订单。</span><span class="sxs-lookup"><span data-stu-id="296c0-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="296c0-130">主计划似乎不遵守产能限制，计划的产能超过可用产能。</span><span class="sxs-lookup"><span data-stu-id="296c0-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="296c0-131">问题描述</span><span class="sxs-lookup"><span data-stu-id="296c0-131">Issue description</span></span>

<span data-ttu-id="296c0-132">当您使用存在有限产能且工艺路线指定资源组和单个资源的混合需要的工序计划编制时，由于算法验证产能冲突的方式，超额预订的可能性较小。</span><span class="sxs-lookup"><span data-stu-id="296c0-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="296c0-133">当您使用帮助程序运行主计划时，可能会发生这种超额预订情况。</span><span class="sxs-lookup"><span data-stu-id="296c0-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="296c0-134">如果有很多作业的运行时间相对较短，最有可能发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="296c0-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="296c0-135">解决问题</span><span class="sxs-lookup"><span data-stu-id="296c0-135">Issue resolution</span></span>

<span data-ttu-id="296c0-136">如果必须确保工序计划编制不会发生超额预订，可以打开 **主计划参数** 页上的 **工序计划编制的准确有限产能** 选项，让主计划的计划编制部分变为单线程。</span><span class="sxs-lookup"><span data-stu-id="296c0-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="296c0-137">此选项默认不可用。</span><span class="sxs-lookup"><span data-stu-id="296c0-137">This option isn't available by default.</span></span> <span data-ttu-id="296c0-138">您必须使用个性化功能将其手动添加到页面。</span><span class="sxs-lookup"><span data-stu-id="296c0-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="296c0-139">使用此选项时，由于缺少并行处理，计划编制会运行得更慢。</span><span class="sxs-lookup"><span data-stu-id="296c0-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="296c0-140">计划订单需要很长时间来更新。</span><span class="sxs-lookup"><span data-stu-id="296c0-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="296c0-141">问题描述</span><span class="sxs-lookup"><span data-stu-id="296c0-141">Issue description</span></span>

<span data-ttu-id="296c0-142">更新计划订单上的需求数量和/或交货日期时，每个订单保存更新通常至少需要 30 秒。</span><span class="sxs-lookup"><span data-stu-id="296c0-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="296c0-143">解决问题</span><span class="sxs-lookup"><span data-stu-id="296c0-143">Issue resolution</span></span>

<span data-ttu-id="296c0-144">这是内置的主计划引擎的一个已知问题。</span><span class="sxs-lookup"><span data-stu-id="296c0-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="296c0-145">它是由编辑期间物料清单结构的基础自动分解引起的。</span><span class="sxs-lookup"><span data-stu-id="296c0-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="296c0-146">此问题在计划优化中得到了解决，规划员可以在其中更新和审核相关订单，并可以在需要时触发计划运行来更新基础物料清单结构的计划订单。</span><span class="sxs-lookup"><span data-stu-id="296c0-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="296c0-147">使用内置的主计划引擎提高性能的一种方法是执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="296c0-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="296c0-148">转到 **主计划 \> 设置 \> 计划 \> 主计划**。</span><span class="sxs-lookup"><span data-stu-id="296c0-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="296c0-149">选择一个计划。</span><span class="sxs-lookup"><span data-stu-id="296c0-149">Select a plan.</span></span>
1. <span data-ttu-id="296c0-150">展开 **按天计算的时限** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="296c0-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="296c0-151">将 **分解** 设置为 *是*，将将此设置下方的字段设置为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="296c0-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="296c0-152">这会将为这个主计划执行的分解的期间限制为一天。</span><span class="sxs-lookup"><span data-stu-id="296c0-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]