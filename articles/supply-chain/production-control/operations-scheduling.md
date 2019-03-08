---
title: 工序级排产
description: 本主题提供了有关工序级排产的信息。 您可以使用工序级排产以提供生产流程的持续时间的粗略估计。
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 298c07346427a949ffa544e66eb6b01995dadc38
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "356936"
---
# <a name="operations-scheduling"></a><span data-ttu-id="105da-104">工序级排产</span><span class="sxs-lookup"><span data-stu-id="105da-104">Operations scheduling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="105da-105">本主题提供了有关工序级排产的信息。</span><span class="sxs-lookup"><span data-stu-id="105da-105">This topic provides information about operations scheduling.</span></span> <span data-ttu-id="105da-106">您可以使用工序级排产以提供生产流程的持续时间的粗略估计。</span><span class="sxs-lookup"><span data-stu-id="105da-106">You can use operations scheduling to provide a general estimate of the production process over time.</span></span>

<span data-ttu-id="105da-107">您可以在工序级别和作业级别计划生产。</span><span class="sxs-lookup"><span data-stu-id="105da-107">You can schedule production at the operation level and the job level.</span></span> <span data-ttu-id="105da-108">不同于作业级排产，工序级排产不将该生产工艺路线中的工序分解为作业。</span><span class="sxs-lookup"><span data-stu-id="105da-108">Unlike job scheduling, operations scheduling doesn't explode the operations for the production route into jobs.</span></span> <span data-ttu-id="105da-109">如果您要在计划中包括详细信息，如有关当前产能的信息，则可以在工序级排产后运行作业级排产。</span><span class="sxs-lookup"><span data-stu-id="105da-109">If you want to include more detail in the scheduling, such as information about current capacity, you can run job scheduling after you run operations scheduling.</span></span> <span data-ttu-id="105da-110">您还可以只运行作业级排产。</span><span class="sxs-lookup"><span data-stu-id="105da-110">You can also run job scheduling only.</span></span> <span data-ttu-id="105da-111">作业级排产通常用于即刻发生或在短期内发生的车间单个作业。</span><span class="sxs-lookup"><span data-stu-id="105da-111">Job scheduling is typically used to schedule individual jobs on the shop floor for an immediate or short-term time frame.</span></span>

## <a name="components-of-operations-scheduling"></a><span data-ttu-id="105da-112">工序级排产的组成部分</span><span class="sxs-lookup"><span data-stu-id="105da-112">Components of operations scheduling</span></span>
<span data-ttu-id="105da-113">工序级排产的主要组成部分是计划方向、资源产能和物料优化。</span><span class="sxs-lookup"><span data-stu-id="105da-113">The main components of operations scheduling are the scheduling direction, the capacity of resources, and materials optimization.</span></span> <span data-ttu-id="105da-114">通过使用工序级排产，可以达到以下目标：</span><span class="sxs-lookup"><span data-stu-id="105da-114">By using operations scheduling, you can achieve the following goals:</span></span>

-   <span data-ttu-id="105da-115">通过对某一给定日期正推或倒推排产控制计划方法。</span><span class="sxs-lookup"><span data-stu-id="105da-115">Control the planning method by scheduling forward or backward from a given date.</span></span>
-   <span data-ttu-id="105da-116">通过计划基于资源产能的生产优化资源的使用。</span><span class="sxs-lookup"><span data-stu-id="105da-116">Optimize the use of resources by scheduling productions based on the capacity of the resources.</span></span> <span data-ttu-id="105da-117">此方法有助于标识使用备选资源的时间。</span><span class="sxs-lookup"><span data-stu-id="105da-117">This approach also helps identify when alternative resources should be used.</span></span>
-   <span data-ttu-id="105da-118">通过计划基于所需物料的可用性的生产优化物料的使用。</span><span class="sxs-lookup"><span data-stu-id="105da-118">Optimize the use of materials by scheduling productions based on the availability of the required materials.</span></span>
-   <span data-ttu-id="105da-119">计划和同步参考生产。</span><span class="sxs-lookup"><span data-stu-id="105da-119">Schedule and synchronize reference productions.</span></span> <span data-ttu-id="105da-120">在更改该生产订单的计划时，调整参考生产日期。</span><span class="sxs-lookup"><span data-stu-id="105da-120">The dates of the reference productions are adjusted when the production order’s schedule is changed.</span></span>

<span data-ttu-id="105da-121">在您可以运行工序级排产之前，必须评估生产订单的成本。</span><span class="sxs-lookup"><span data-stu-id="105da-121">You must estimate the cost of a production order before you can run operations scheduling.</span></span> <span data-ttu-id="105da-122">如果还未运行估计，则在启动工序级排产流程之前自动运行。</span><span class="sxs-lookup"><span data-stu-id="105da-122">If you haven't run an estimate, it's automatically run before operations scheduling is started.</span></span> <span data-ttu-id="105da-123">工序级排产指定以下信息：</span><span class="sxs-lookup"><span data-stu-id="105da-123">An operations schedule specifies the following information:</span></span>

-   <span data-ttu-id="105da-124">为生产计划的产品</span><span class="sxs-lookup"><span data-stu-id="105da-124">The product that is planned for production</span></span>
-   <span data-ttu-id="105da-125">产品配置</span><span class="sxs-lookup"><span data-stu-id="105da-125">The configuration of the product</span></span>
-   <span data-ttu-id="105da-126">在生产中涉及的数量</span><span class="sxs-lookup"><span data-stu-id="105da-126">The quantities that are involved in the production</span></span>
-   <span data-ttu-id="105da-127">将开始和结束生产的日期</span><span class="sxs-lookup"><span data-stu-id="105da-127">The dates when the production will start and end</span></span>
-   <span data-ttu-id="105da-128">执行生产活动的资源的产能预留</span><span class="sxs-lookup"><span data-stu-id="105da-128">The capacity reservations for the resources that perform the production activities</span></span>

<span data-ttu-id="105da-129">为生产中的工序设置设置时间、处理时间和运行时间。</span><span class="sxs-lookup"><span data-stu-id="105da-129">The setup time, process time, and run time are set for operations in the production.</span></span> <span data-ttu-id="105da-130">在运行工序级排产后，生产订单的状态为**已排产**，并且所有工序都按生产工艺路线中指定的顺序排产。</span><span class="sxs-lookup"><span data-stu-id="105da-130">After you run operations scheduling, the status of the production order is **Scheduled**, and all operations are scheduled in the order that is specified by the production route.</span></span> <span data-ttu-id="105da-131">但是，只考虑工序的持续时间。</span><span class="sxs-lookup"><span data-stu-id="105da-131">However, only the duration of the operation is considered.</span></span> <span data-ttu-id="105da-132">未计划开始时间和结束时间。</span><span class="sxs-lookup"><span data-stu-id="105da-132">Start times and end times aren't scheduled.</span></span>

## <a name="scheduling-direction-and-date"></a><span data-ttu-id="105da-133">计划编制说明和日期</span><span class="sxs-lookup"><span data-stu-id="105da-133">Scheduling direction and date</span></span>
<span data-ttu-id="105da-134">计划编制说明对计划编制进程至关重要。</span><span class="sxs-lookup"><span data-stu-id="105da-134">The scheduling direction is fundamental to the scheduling process.</span></span> <span data-ttu-id="105da-135">生产将根据时间和计划编制的要求，从任意日期正推或倒推。</span><span class="sxs-lookup"><span data-stu-id="105da-135">Production can be scheduled forward or backward from any date, depending on timing and scheduling requirements.</span></span>

-   <span data-ttu-id="105da-136">**从排产日期正推** – 尽可能早地开始计划生产。</span><span class="sxs-lookup"><span data-stu-id="105da-136">**Forward from the scheduling date** – You can schedule production to start as early as possible.</span></span> <span data-ttu-id="105da-137">可以在今天、明天或将来的任何日期开始生产。</span><span class="sxs-lookup"><span data-stu-id="105da-137">Production can be started today, tomorrow, or on any date in the future.</span></span> <span data-ttu-id="105da-138">生产计划正推最早可能结束的日期。</span><span class="sxs-lookup"><span data-stu-id="105da-138">The production is scheduled forward in time to the earliest possible end date.</span></span>
-   <span data-ttu-id="105da-139">**从排产日期倒推** – 尽可能晚地开始计划生产。</span><span class="sxs-lookup"><span data-stu-id="105da-139">**Backward from the scheduling date** – You can schedule production to start as late as possible.</span></span> <span data-ttu-id="105da-140">必须完成基于该生产日期的倒推排产。</span><span class="sxs-lookup"><span data-stu-id="105da-140">Backward scheduling is based on the date when the production must be completed.</span></span> <span data-ttu-id="105da-141">从计划日期倒推到生产可以按时开始并完成的可能的最晚日期。</span><span class="sxs-lookup"><span data-stu-id="105da-141">The schedule counts backward from that date to the latest possible date that the production can be started and still be completed on time.</span></span>

## <a name="resource-scheduling"></a><span data-ttu-id="105da-142">资源计划编制</span><span class="sxs-lookup"><span data-stu-id="105da-142">Resource scheduling</span></span>
<span data-ttu-id="105da-143">在运行工序计划表时，生产工艺路线中的每道工序都是针对为其指定的资源来计划日期。</span><span class="sxs-lookup"><span data-stu-id="105da-143">When you run an operations schedule, each operation in the production route is scheduled for the resource that is specified for the operation.</span></span> <span data-ttu-id="105da-144">此外，每道工序的持续时间在生产工艺路线上指定。</span><span class="sxs-lookup"><span data-stu-id="105da-144">Additionally, the duration of each operation is specified on the production route.</span></span> <span data-ttu-id="105da-145">如果为工序指定了资源组，排产就会为该组预留产能。</span><span class="sxs-lookup"><span data-stu-id="105da-145">If a resource group is specified for an operation, the scheduling reserves capacity on the group.</span></span> <span data-ttu-id="105da-146">但是，与作业级排产不同，工序级排产不选择该组中的特定资源。</span><span class="sxs-lookup"><span data-stu-id="105da-146">However, unlike job scheduling, operations scheduling doesn't select the specific resources in the group.</span></span> <span data-ttu-id="105da-147">如果您使用有限产能，该排产取决于完成生产所需资源的可用性。</span><span class="sxs-lookup"><span data-stu-id="105da-147">If you're working with finite capacity, the schedule depends on the availability of the resources that are required in order to complete production.</span></span> <span data-ttu-id="105da-148">工序级排产按照在生产工艺路线中指定的工序顺序执行。</span><span class="sxs-lookup"><span data-stu-id="105da-148">Operations scheduling follows the sequence of operations that is specified on the production route.</span></span> <span data-ttu-id="105da-149">排产基于在生产工艺路线上定义的工序时间在资源组预留产能。</span><span class="sxs-lookup"><span data-stu-id="105da-149">The scheduling reserves capacity on the resource groups, based on the operation times that are defined on the production route.</span></span> <span data-ttu-id="105da-150">所涉及的资源可用产能的总和确定资源组的产能。</span><span class="sxs-lookup"><span data-stu-id="105da-150">The sum of available capacity on the resources that are involved determines the capacity for the resource group.</span></span> <span data-ttu-id="105da-151">为资源已存在的预留产能视作不可用产能。</span><span class="sxs-lookup"><span data-stu-id="105da-151">Capacity reservations that already exist for the resources are considered unavailable capacity.</span></span> <span data-ttu-id="105da-152">如果没有足够的产能可用于生产，这些生产订单可能延误或甚至停止。</span><span class="sxs-lookup"><span data-stu-id="105da-152">If there isn't enough available capacity for the production, the production orders can be delayed or even stopped.</span></span> <span data-ttu-id="105da-153">您还可以指定您希望在生产中涉及的资源的效率。</span><span class="sxs-lookup"><span data-stu-id="105da-153">You can also specify the efficiency that you expect from the resources that are involved in the production.</span></span> <span data-ttu-id="105da-154">您指定该效率作为资源中的百分比。</span><span class="sxs-lookup"><span data-stu-id="105da-154">You specify the efficiency as a percentage on the resource.</span></span> <span data-ttu-id="105da-155">效率百分比调整资源的生产量。</span><span class="sxs-lookup"><span data-stu-id="105da-155">The efficiency percentage adjusts the throughput of the resource.</span></span> <span data-ttu-id="105da-156">调整影响为资源预留的时间。</span><span class="sxs-lookup"><span data-stu-id="105da-156">This adjustment affects the time that is reserved for the resource.</span></span> <span data-ttu-id="105da-157">还相应调整使用该资源工序的提前期。</span><span class="sxs-lookup"><span data-stu-id="105da-157">The lead times for the operations that use the resource are also adjusted accordingly.</span></span>

## <a name="operations-scheduling-and-master-planning"></a><span data-ttu-id="105da-158">工序级排产和主计划</span><span class="sxs-lookup"><span data-stu-id="105da-158">Operations scheduling and master planning</span></span>
<span data-ttu-id="105da-159">工序级排产还驱动主计划，确定所有物料需求的计算。</span><span class="sxs-lookup"><span data-stu-id="105da-159">The operations schedule also drives master planning and determines calculations for material requirements.</span></span> <span data-ttu-id="105da-160">工序级排产将考虑以下信息：</span><span class="sxs-lookup"><span data-stu-id="105da-160">Operations scheduling considers the following information:</span></span>

-   <span data-ttu-id="105da-161">**订货生产** – 计划、下达或开始的产品</span><span class="sxs-lookup"><span data-stu-id="105da-161">**Backlogged productions** – Products that are planned, released, or started</span></span>
-   <span data-ttu-id="105da-162">**物料可用性** – 库存、子生产、供应商和提供商</span><span class="sxs-lookup"><span data-stu-id="105da-162">**Material availability** – Inventory, subproductions, suppliers, and vendors</span></span>
-   <span data-ttu-id="105da-163">**产能可用性** – 生产所需的资源</span><span class="sxs-lookup"><span data-stu-id="105da-163">**Capacity availability** – Resources that are required for production</span></span>

## <a name="cancellations"></a><span data-ttu-id="105da-164">取消</span><span class="sxs-lookup"><span data-stu-id="105da-164">Cancellations</span></span>
<span data-ttu-id="105da-165">在您运行工序级排产时，您可以取消该工艺路线的特定部分。</span><span class="sxs-lookup"><span data-stu-id="105da-165">When you run operations scheduling, you can cancel specific parts of the routing.</span></span> <span data-ttu-id="105da-166">其中包括排队时间、设置时间、处理时间、重叠时间和运输时间。</span><span class="sxs-lookup"><span data-stu-id="105da-166">These parts include the queue time, setup time, process time, overlap time, and transport times.</span></span>

## <a name="finite-materials"></a><span data-ttu-id="105da-167">有限物料</span><span class="sxs-lookup"><span data-stu-id="105da-167">Finite materials</span></span>
<span data-ttu-id="105da-168">如果您使用有限物料，该排产还取决于生产所需物料的可用性。</span><span class="sxs-lookup"><span data-stu-id="105da-168">If you're working with finite materials, scheduling also depends on the availability of the materials that are required for production.</span></span> <span data-ttu-id="105da-169">如果可用组件无法满足生产，生成可能延误。</span><span class="sxs-lookup"><span data-stu-id="105da-169">If there aren't enough available components for the production, production can be delayed.</span></span> <span data-ttu-id="105da-170">您可以根据指定必须可用于生产的物料的使用编制计划。</span><span class="sxs-lookup"><span data-stu-id="105da-170">You can base scheduling on the use of materials by specifying the materials that must be available for production.</span></span> <span data-ttu-id="105da-171">在您对资源产能和物料的可用性同时进行优化生产时，根据这些限制计算生产。</span><span class="sxs-lookup"><span data-stu-id="105da-171">When you optimize on both resource capacity and the availability of materials, production is calculated according to these restrictions.</span></span> <span data-ttu-id="105da-172">在产能和物料按所需数量同时可用前，生产订单不能计划开始。</span><span class="sxs-lookup"><span data-stu-id="105da-172">A production order can't be scheduled to start until capacity and materials are available at the same time and in the required quantities.</span></span>

<a name="additional-resources"></a><span data-ttu-id="105da-173">其他资源</span><span class="sxs-lookup"><span data-stu-id="105da-173">Additional resources</span></span>
--------

[<span data-ttu-id="105da-174">工序级排产选项</span><span class="sxs-lookup"><span data-stu-id="105da-174">Operation scheduling options</span></span>](operation-scheduling-options.md)



