---
title: "工序级排产选项"
description: "本主题介绍工序级排产的选项。 您可以使用工序级排产以提供生产流程的持续时间的粗略估计。"
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 198123
ms.assetid: d680d7be-da64-4132-89fe-ad2fa59afb77
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 56eeb2b56261dc3e576192c0ede405996d82b2b7
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="operations-scheduling-options"></a><span data-ttu-id="876a9-104">工序级排产选项</span><span class="sxs-lookup"><span data-stu-id="876a9-104">Operations scheduling options</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="876a9-105">本主题介绍工序级排产的选项。</span><span class="sxs-lookup"><span data-stu-id="876a9-105">This topic describes the options for operations scheduling.</span></span> <span data-ttu-id="876a9-106">您可以使用工序级排产以提供生产流程的持续时间的粗略估计。</span><span class="sxs-lookup"><span data-stu-id="876a9-106">You can use operations scheduling to provide a general estimate of the production process over time.</span></span>

<span data-ttu-id="876a9-107">工序级排产是计算某个生产订单的以下信息：</span><span class="sxs-lookup"><span data-stu-id="876a9-107">Operations scheduling calculates the following information for a production order:</span></span>

-   <span data-ttu-id="876a9-108">为生产订单和每个工序设置开始日期和结束日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-108">Start and end dates are set for the production order and each operation.</span></span>
-   <span data-ttu-id="876a9-109">将资源分配给这些工序。</span><span class="sxs-lookup"><span data-stu-id="876a9-109">Resources are assigned to operations.</span></span>

<span data-ttu-id="876a9-110">有几项确定计算生产计划的方式的设置。</span><span class="sxs-lookup"><span data-stu-id="876a9-110">Several settings determine how production schedules are calculated.</span></span> <span data-ttu-id="876a9-111">您可以在“**工序级排产**”页面上定义这些设置。</span><span class="sxs-lookup"><span data-stu-id="876a9-111">You define these settings on the **Operations scheduling** page.</span></span> <span data-ttu-id="876a9-112">以下信息描述了排产选项。</span><span class="sxs-lookup"><span data-stu-id="876a9-112">The following information describes the scheduling options.</span></span>

## <a name="operations-scheduling"></a><span data-ttu-id="876a9-113">工序级排产</span><span class="sxs-lookup"><span data-stu-id="876a9-113">Operations scheduling</span></span>
### <a name="scheduling-direction"></a><span data-ttu-id="876a9-114">计划的方向</span><span class="sxs-lookup"><span data-stu-id="876a9-114">Scheduling direction</span></span>

<span data-ttu-id="876a9-115">计划编制说明对计划编制进程至关重要。</span><span class="sxs-lookup"><span data-stu-id="876a9-115">The scheduling direction is fundamental to the scheduling process.</span></span> <span data-ttu-id="876a9-116">生产可以根据时间和排产的要求，从任意日期正推或倒推。</span><span class="sxs-lookup"><span data-stu-id="876a9-116">A production can be scheduled forward or backward from any date, depending on timing and scheduling requirements.</span></span>

-   <span data-ttu-id="876a9-117">**前导式排产** – 尽可能早地开始计划生产。</span><span class="sxs-lookup"><span data-stu-id="876a9-117">**Forward scheduling** – You can schedule a production to start as early as possible.</span></span> <span data-ttu-id="876a9-118">可以在今天、明天或将来任何特定日期开始生产。</span><span class="sxs-lookup"><span data-stu-id="876a9-118">The production can be started today, tomorrow, or on any specific date in the future.</span></span> <span data-ttu-id="876a9-119">对生产进行排产以便尽可能早地开始，从而安排可能最早的结束日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-119">The production is scheduled to start on the earliest possible date and is planned forward in time to the earliest possible end date.</span></span>
-   <span data-ttu-id="876a9-120">**后导式排产** – 尽可能晚地开始计划生产。</span><span class="sxs-lookup"><span data-stu-id="876a9-120">**Backward scheduling** – You can schedule a production to start as late as possible.</span></span> <span data-ttu-id="876a9-121">它基于生产必须完成的日期，倒推在不会影响其目标截止时间的前提下可以开始生产的最晚可能日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-121">The schedule is based on the date when the production must be completed and counts backward to the latest possible date that the production can be started without missing its target deadline.</span></span>

<span data-ttu-id="876a9-122">选项如下：</span><span class="sxs-lookup"><span data-stu-id="876a9-122">The following options are available:</span></span>

-   <span data-ttu-id="876a9-123">**从今天正推** - 计划从当前日期正推。</span><span class="sxs-lookup"><span data-stu-id="876a9-123">**Forward from today** – Schedule forward from the current date.</span></span> <span data-ttu-id="876a9-124">（当前日期是系统日期。）</span><span class="sxs-lookup"><span data-stu-id="876a9-124">(The current date is the system date.)</span></span>
-   <span data-ttu-id="876a9-125">**从计划开始时间正推** - 计划从以前的开始日期正推。</span><span class="sxs-lookup"><span data-stu-id="876a9-125">**Forward from planned start** – Schedule forward from an earlier start date.</span></span> <span data-ttu-id="876a9-126">如果以前没有排产，则排产方向从当前日期往前推。</span><span class="sxs-lookup"><span data-stu-id="876a9-126">If there is no previous scheduling, the scheduling direction is forward from the current date.</span></span>
-   <span data-ttu-id="876a9-127">**从排产日期正推** - 计划从“**排产日期**”字段中指定的日期正推。</span><span class="sxs-lookup"><span data-stu-id="876a9-127">**Forward from scheduling date** – Schedule forward from the date that is specified in the **Scheduling date** field.</span></span> <span data-ttu-id="876a9-128">如果没指定排产日期，则排产方向从当前日期往前推。</span><span class="sxs-lookup"><span data-stu-id="876a9-128">If you don't specify a scheduling date, the scheduling direction is forward from the current date.</span></span>
-   <span data-ttu-id="876a9-129">**从交货日期倒推** - 计划从为生产订单指定的交货日期倒推。</span><span class="sxs-lookup"><span data-stu-id="876a9-129">**Backward from delivery date** – Schedule backward from the delivery date that is specified for the production order.</span></span> <span data-ttu-id="876a9-130">如果选择了此选项，但未指定交货日期，则交货日期为当前日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-130">If you select this option, but no delivery date is specified, the delivery date is the current date.</span></span>
-   <span data-ttu-id="876a9-131">**从计划结束日期倒推** - 计划从以前计算出的结束日期倒推。</span><span class="sxs-lookup"><span data-stu-id="876a9-131">**Backward from planned end** – Schedule backward from a previously calculated end date.</span></span> <span data-ttu-id="876a9-132">如果以前没有排产，则结束日期为当前日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-132">If there is no previous scheduling, the end date is the current date.</span></span>
-   <span data-ttu-id="876a9-133">**从排产日期后推** - 计划从“**排产日期**”字段中指定的日期后推。</span><span class="sxs-lookup"><span data-stu-id="876a9-133">**Backward from scheduling date** – Schedule backward from the date that is specified in the **Scheduling date** field.</span></span> <span data-ttu-id="876a9-134">如果没有指定排产日期，将使用当前日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-134">If you don't specify a scheduling date, the current date is used.</span></span> <span data-ttu-id="876a9-135">在最后一次计算需求时为生产订单计算从排产日期倒推。</span><span class="sxs-lookup"><span data-stu-id="876a9-135">Backward from scheduling date is calculated for the production order the last time that a requirement was calculated.</span></span> <span data-ttu-id="876a9-136">如果没有为生产订单指定日期，则使用当前系统日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-136">If no date is specified for the production order, the current system date is used.</span></span>
-   <span data-ttu-id="876a9-137">**从将来日期倒推** - 计划从将来日期倒推，在计算最后一次需求时为生产订单计算该将来日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-137">**Backward from futures date** – Schedule backward from the futures date that was calculated for the production order the last time that a requirement was calculated.</span></span> <span data-ttu-id="876a9-138">如果没有为生产订单指定将来日期，则使用当前系统日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-138">If no futures date is specified for the production order, the current system date is used.</span></span>
-   <span data-ttu-id="876a9-139">**与上一个排产相同** - 就工序级排产和作业级排产而言，将保存所选的排产方向和日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-139">**As last scheduling** – For operations scheduling and job scheduling, the selected scheduling direction and date are saved.</span></span> <span data-ttu-id="876a9-140">因此，您可以为后续排产选择此选项。</span><span class="sxs-lookup"><span data-stu-id="876a9-140">Therefore, you can select this option for subsequent scheduling.</span></span> <span data-ttu-id="876a9-141">如果生产订单以前没有排产，则排产将从当前系统日期倒推。</span><span class="sxs-lookup"><span data-stu-id="876a9-141">If there is no previous scheduling of the production order, scheduling is backward from the current system date.</span></span>
-   <span data-ttu-id="876a9-142">**从明天正推** - 计划从当前日期再加上一天的日期正推。</span><span class="sxs-lookup"><span data-stu-id="876a9-142">**Forward from tomorrow** – Schedule forward from the current date plus one day.</span></span>
-   <span data-ttu-id="876a9-143">**从上一个作业正推** - 只在作业级排产中使用此选项。</span><span class="sxs-lookup"><span data-stu-id="876a9-143">**Forward from previous job** – This option is relevant only in job scheduling.</span></span> <span data-ttu-id="876a9-144">如果为工序级排产选择此排产方向，则安排将生产订单从当前日期正推。</span><span class="sxs-lookup"><span data-stu-id="876a9-144">If you select this scheduling direction for operations scheduling, the production order is scheduled forward from the current date.</span></span> <span data-ttu-id="876a9-145">在作业级排产中，为一个作业建立排产，然后基于该作业计划生产的所有其他作业。</span><span class="sxs-lookup"><span data-stu-id="876a9-145">In job scheduling, scheduling is established for one job, and all other jobs for the production are scheduled based on that job.</span></span>
-   <span data-ttu-id="876a9-146">**从上一个作业倒推** - 只在作业级排产中使用此选项。</span><span class="sxs-lookup"><span data-stu-id="876a9-146">**Backward from previous job** – This option is relevant only in job scheduling.</span></span> <span data-ttu-id="876a9-147">如果为工序级排产选择此排产方向，则安排将生产订单从当前日期倒推。</span><span class="sxs-lookup"><span data-stu-id="876a9-147">If you select this scheduling direction for operations scheduling, planned orders are scheduled backward from the current date.</span></span> <span data-ttu-id="876a9-148">在作业级排产中，为一个作业建立排产，然后基于该作业计划生产的所有其他作业。</span><span class="sxs-lookup"><span data-stu-id="876a9-148">In job scheduling, scheduling is established for one job, and all other jobs for the production are scheduled based on that job.</span></span>

### <a name="scheduling-date"></a><span data-ttu-id="876a9-149">计划编制日期</span><span class="sxs-lookup"><span data-stu-id="876a9-149">Scheduling date</span></span>

<span data-ttu-id="876a9-150">用于“**从排产日期正推**”和“**从排产日期倒推**”排产方向的日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-150">This date is used for the **Forward from scheduling date** and **Backward from scheduling date** scheduling directions.</span></span> <span data-ttu-id="876a9-151">从此日期正推或倒推计划。</span><span class="sxs-lookup"><span data-stu-id="876a9-151">Scheduling is backward or forward from this date.</span></span> <span data-ttu-id="876a9-152">有关详细信息，请参阅上一节“排产方向”。</span><span class="sxs-lookup"><span data-stu-id="876a9-152">For more information, see the previous section, "Scheduling direction."</span></span>

### <a name="recalculate-bom-levels"></a><span data-ttu-id="876a9-153">重新计算物料清单层</span><span class="sxs-lookup"><span data-stu-id="876a9-153">Recalculate BOM levels</span></span>

<span data-ttu-id="876a9-154">您选择“**重新计算物料清单级别**”后，要重新计算所选物料清单 (BOM) 级别，以保障正确的排产顺序。</span><span class="sxs-lookup"><span data-stu-id="876a9-154">When you select **Recalculate BOM levels**, the selected bill of materials (BOM) levels will be recalculated to help guarantee the correct scheduling order.</span></span>

## <a name="limitations"></a><span data-ttu-id="876a9-155">限制</span><span class="sxs-lookup"><span data-stu-id="876a9-155">Limitations</span></span>
### <a name="finite-capacity"></a><span data-ttu-id="876a9-156">有限产能</span><span class="sxs-lookup"><span data-stu-id="876a9-156">Finite capacity</span></span>

<span data-ttu-id="876a9-157">排产取决于完成生产所需的资源的可用性。</span><span class="sxs-lookup"><span data-stu-id="876a9-157">Scheduling depends on the availability of the resources that are required in order to complete production.</span></span> <span data-ttu-id="876a9-158">如果没有足够的产能，生产订单可能延误甚至停止。</span><span class="sxs-lookup"><span data-stu-id="876a9-158">If there isn't enough capacity, production orders can be delayed or even stopped.</span></span> <span data-ttu-id="876a9-159">如果将有限产能应用于工序级排产，将考虑该资源上进行预留的现有产能，另外该产能被视为不可用。</span><span class="sxs-lookup"><span data-stu-id="876a9-159">If finite capacity is applied to operations scheduling, existing capacity reservations that are made on the resources are considered, and that capacity is seen as unavailable.</span></span> <span data-ttu-id="876a9-160">根据资源所需的产能的可用性计划生产订单。</span><span class="sxs-lookup"><span data-stu-id="876a9-160">The production order is scheduled based on the availability of capacity on the resources that are required.</span></span> <span data-ttu-id="876a9-161">工序级排产使用了指定的工序顺序以确定生产工艺路线中的工序顺序。</span><span class="sxs-lookup"><span data-stu-id="876a9-161">Operations scheduling uses the specified sequence of operations to determine the order of operations in the production route.</span></span> <span data-ttu-id="876a9-162">工序级排产基于在生产工艺路线上定义的工序时间在资源组预留产能。</span><span class="sxs-lookup"><span data-stu-id="876a9-162">Operations scheduling reserves capacity on the resource groups, based on the operation times that are defined on the production route.</span></span> <span data-ttu-id="876a9-163">资源组的产能是资源组中所有资源的可用产能的总和。</span><span class="sxs-lookup"><span data-stu-id="876a9-163">The capacity of the resource groups is the sum of available capacity on all the resources in the resource groups.</span></span>

### <a name="finite-material"></a><span data-ttu-id="876a9-164">有限物料</span><span class="sxs-lookup"><span data-stu-id="876a9-164">Finite material</span></span>

<span data-ttu-id="876a9-165">排产也取决于生产所需的物料的可用性。</span><span class="sxs-lookup"><span data-stu-id="876a9-165">Scheduling also depends on the availability of the materials that are required for production.</span></span> <span data-ttu-id="876a9-166">不足组件的可用性也可能导致生产延误。</span><span class="sxs-lookup"><span data-stu-id="876a9-166">Insufficient component availability can also cause production delays.</span></span> <span data-ttu-id="876a9-167">也可以基于物料的使用进行排产。</span><span class="sxs-lookup"><span data-stu-id="876a9-167">Scheduling can also be based on the use of materials.</span></span> <span data-ttu-id="876a9-168">仅指定必须对生产可用的物料（而不是不重要的物料）。</span><span class="sxs-lookup"><span data-stu-id="876a9-168">Just specify the materials that must be available for production instead of the materials that aren't critical.</span></span> <span data-ttu-id="876a9-169">此类排产被称作使用有限物料进行排产。</span><span class="sxs-lookup"><span data-stu-id="876a9-169">This type of scheduling is known as scheduling with finite material.</span></span> <span data-ttu-id="876a9-170">当您指定有限物料时，基于材料是否可用进行排产。</span><span class="sxs-lookup"><span data-stu-id="876a9-170">When you specify finite materials, production is scheduled based on whether materials are available.</span></span> <span data-ttu-id="876a9-171">**注意：**同时基于产能和物料进行优化时，计算生产以同时满足这两种限制。</span><span class="sxs-lookup"><span data-stu-id="876a9-171">**Note:** When you optimize on both capacity and materials, production is calculated to meet both restrictions.</span></span> <span data-ttu-id="876a9-172">考虑产能和材料的可用性，另外，直到产能和材料以所需的数量在相同时间可用，生产订单的工序不能被安排开始。</span><span class="sxs-lookup"><span data-stu-id="876a9-172">The availability of capacity and materials is considered, and the production order’s operations can't be scheduled to start until capacity and materials are available at the same time and in the required quantities.</span></span> <span data-ttu-id="876a9-173">如果在编制计划期间应将物料视为有限，则选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="876a9-173">Select this check box if materials should be considered limited during scheduling.</span></span> <span data-ttu-id="876a9-174">如果物料有限，则将考虑这些物料当时的覆盖范围。</span><span class="sxs-lookup"><span data-stu-id="876a9-174">If the materials are limited, the material's coverage for that time will be considered.</span></span> <span data-ttu-id="876a9-175">换言之，编制计划时将考虑为这些物料计算的将来日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-175">In other words, scheduling considers the futures dates that are calculated for the items.</span></span> <span data-ttu-id="876a9-176">编制计划时将预留原材料并分解当前生产。</span><span class="sxs-lookup"><span data-stu-id="876a9-176">Scheduling reserves raw materials and explodes the current production.</span></span> <span data-ttu-id="876a9-177">如果多次执行了计划编制，则只有第一次编制计划时才运行分解过程并执行预留。</span><span class="sxs-lookup"><span data-stu-id="876a9-177">If scheduling occurs several times, only the first scheduling runs an explosion and makes reservations.</span></span> <span data-ttu-id="876a9-178">如果在生产物料清单或工艺路线中进行了更改，则下一次编制计划时将运行分解过程。</span><span class="sxs-lookup"><span data-stu-id="876a9-178">If you make changes in the production BOM or route, the next scheduling runs an explosion.</span></span> <span data-ttu-id="876a9-179">该分解假定在当天需要物料。</span><span class="sxs-lookup"><span data-stu-id="876a9-179">For the explosion, it's assumed that the materials are required on the same day.</span></span> <span data-ttu-id="876a9-180">由于生产不是在分解主计划时计划的，因此当前日期为物料变得可用的时间的最佳估计。</span><span class="sxs-lookup"><span data-stu-id="876a9-180">Because the production isn't scheduled at the time of the master schedule explosion, the current date is the best estimate of when the items will be available.</span></span> <span data-ttu-id="876a9-181">然后，分解过程将检查物料是否可用。</span><span class="sxs-lookup"><span data-stu-id="876a9-181">The explosion then checks whether the items are available.</span></span> <span data-ttu-id="876a9-182">如果物料可用，则可以满足生产要求。</span><span class="sxs-lookup"><span data-stu-id="876a9-182">If the items are available, the production requirement can be fulfilled.</span></span> <span data-ttu-id="876a9-183">如果到当前日期物料不可用，则将生成一个计划订单并为该计划订单进行抵销选择。</span><span class="sxs-lookup"><span data-stu-id="876a9-183">If the items aren't available by the current date, a planned order is generated, and an offset selection is made for the planned order.</span></span> <span data-ttu-id="876a9-184">如果为该计划订单设置了自动确定，则将为采购或生产自动确定该计划订单。</span><span class="sxs-lookup"><span data-stu-id="876a9-184">If automatic firming is set for the planned order, the planned order is firmed automatically for purchase or production.</span></span> <span data-ttu-id="876a9-185">生产状态将自动更改为“**覆盖范围组**”对话框的“**请求的生产状态**”字段中所指定的状态。</span><span class="sxs-lookup"><span data-stu-id="876a9-185">The production status is automatically changed to the status that is specified in the **Requested production status** field in the **Coverage groups** dialog box.</span></span> <span data-ttu-id="876a9-186">如果清除该复选框，则始终认为物料是可用的。</span><span class="sxs-lookup"><span data-stu-id="876a9-186">If the check box is cleared, the materials are always considered available.</span></span> <span data-ttu-id="876a9-187">因此，排产时不考虑物料在有需求时是否可用。</span><span class="sxs-lookup"><span data-stu-id="876a9-187">Therefore, scheduling doesn't consider whether the materials are available at the time of requirement.</span></span>

### <a name="finite-property"></a><span data-ttu-id="876a9-188">有限属性</span><span class="sxs-lookup"><span data-stu-id="876a9-188">Finite property</span></span>

<span data-ttu-id="876a9-189">如果作业级排产应包括属性要求，则选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="876a9-189">Select this check box if the job scheduling should include property requirements.</span></span>

### <a name="keep-production-unit"></a><span data-ttu-id="876a9-190">保持生产单位</span><span class="sxs-lookup"><span data-stu-id="876a9-190">Keep production unit</span></span>

<span data-ttu-id="876a9-191">选择排产引擎是否应仅计划生产单位上已经指定的资源。</span><span class="sxs-lookup"><span data-stu-id="876a9-191">Select whether the scheduling engine should schedule only resources that are already specified on the production unit.</span></span>

### <a name="keep-warehouse-from-resource"></a><span data-ttu-id="876a9-192">保留资源仓库</span><span class="sxs-lookup"><span data-stu-id="876a9-192">Keep warehouse from resource</span></span>

<span data-ttu-id="876a9-193">选择排产引擎是否应仅计划与资源上指定的输入仓库相关联的资源。</span><span class="sxs-lookup"><span data-stu-id="876a9-193">Select whether the scheduling engine should schedule only resources that are associated with the input warehouse that is specified on the resource.</span></span>

## <a name="references"></a><span data-ttu-id="876a9-194">参考</span><span class="sxs-lookup"><span data-stu-id="876a9-194">References</span></span>
### <a name="schedule-references"></a><span data-ttu-id="876a9-195">编制参考计划</span><span class="sxs-lookup"><span data-stu-id="876a9-195">Schedule references</span></span>

<span data-ttu-id="876a9-196">当参考取决于生产订单时，也称为子生产。</span><span class="sxs-lookup"><span data-stu-id="876a9-196">When references depend on production orders, they are also known as subproductions.</span></span> <span data-ttu-id="876a9-197">子生产也可以作为生产订单计划编制的一部分编制计划。</span><span class="sxs-lookup"><span data-stu-id="876a9-197">Subproductions can be scheduled as part of the scheduling of a production order.</span></span> <span data-ttu-id="876a9-198">如果应基于主生产计划编制对子生产编制计划，则选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="876a9-198">Select this check box if the scheduling of subproductions should be based on the scheduling of the main production.</span></span> <span data-ttu-id="876a9-199">就主生产而言，过量生产将计划正推，而欠量生产将计划倒推。</span><span class="sxs-lookup"><span data-stu-id="876a9-199">In relation to the main production, overlying productions are scheduled forward, and underlying productions are scheduled backward.</span></span> <span data-ttu-id="876a9-200">您可以在“**生产订单**”页中的“**参考级别**”字段中查看生产订单参考。</span><span class="sxs-lookup"><span data-stu-id="876a9-200">You can view production order references can be viewed in the **Reference level** field on the **Production orders** page.</span></span>

### <a name="synchronize-references"></a><span data-ttu-id="876a9-201">同步参考</span><span class="sxs-lookup"><span data-stu-id="876a9-201">Synchronize references</span></span>

<span data-ttu-id="876a9-202">您可以将参考和生产订单同步。</span><span class="sxs-lookup"><span data-stu-id="876a9-202">You can synchronize references with the production order.</span></span> <span data-ttu-id="876a9-203">如果选择了此选项，对生产订单计划进行更改时将更改并对齐子生产的日期。</span><span class="sxs-lookup"><span data-stu-id="876a9-203">If this option is selected, the dates of the subproductions are moved and aligned when changes are made to the production order’s schedule.</span></span> <span data-ttu-id="876a9-204">如果一个生产订单具有一个或多个子生产，您可能要将子生产和主生产一起计划。</span><span class="sxs-lookup"><span data-stu-id="876a9-204">If a production order has one or more subproductions, you might want to schedule the subproductions together with the main production.</span></span> <span data-ttu-id="876a9-205">在此情况下，直到完成了相关的子生产才能开始主生产。</span><span class="sxs-lookup"><span data-stu-id="876a9-205">In this case, the main production can't be started until the related subproductions have been completed.</span></span> <span data-ttu-id="876a9-206">因此，如果应基于所选生产的开始和结束日期对子生产编制计划，则选中此复选框。</span><span class="sxs-lookup"><span data-stu-id="876a9-206">Therefore, select this check box if the scheduling of subproductions should be based on the start and end times of the selected production.</span></span> <span data-ttu-id="876a9-207">仅当同时选中“**编制参考计划**”复选框时，您才可以选择此复选框。</span><span class="sxs-lookup"><span data-stu-id="876a9-207">You can select this check box only if the **Schedule references** check box is also selected.</span></span>

## <a name="cancellation"></a><span data-ttu-id="876a9-208">取消</span><span class="sxs-lookup"><span data-stu-id="876a9-208">Cancellation</span></span>
### <a name="cancel-queue-time"></a><span data-ttu-id="876a9-209">取消排队时间</span><span class="sxs-lookup"><span data-stu-id="876a9-209">Cancel queue time</span></span>

<span data-ttu-id="876a9-210">选中此复选框可将排队时间从计划编制中排除。</span><span class="sxs-lookup"><span data-stu-id="876a9-210">Select this check box to exclude queue time from the scheduling.</span></span>

### <a name="cancel-setup"></a><span data-ttu-id="876a9-211">取消设置</span><span class="sxs-lookup"><span data-stu-id="876a9-211">Cancel setup</span></span>

<span data-ttu-id="876a9-212">选中此复选框可将设置时间从计划编制中排除。</span><span class="sxs-lookup"><span data-stu-id="876a9-212">Select this check box to exclude setup time from the scheduling.</span></span>

### <a name="cancel-process"></a><span data-ttu-id="876a9-213">取消进程</span><span class="sxs-lookup"><span data-stu-id="876a9-213">Cancel process</span></span>

<span data-ttu-id="876a9-214">选中此复选框可将运行时间从计划编制中排除。</span><span class="sxs-lookup"><span data-stu-id="876a9-214">Select this check box to exclude run time from the scheduling.</span></span>

### <a name="cancel-overlap"></a><span data-ttu-id="876a9-215">取消重叠</span><span class="sxs-lookup"><span data-stu-id="876a9-215">Cancel overlap</span></span>

<span data-ttu-id="876a9-216">选中此复选框可将重叠时间从计划编制中排除。</span><span class="sxs-lookup"><span data-stu-id="876a9-216">Select this check box to exclude overlap time from the scheduling.</span></span>

### <a name="cancel-transport"></a><span data-ttu-id="876a9-217">取消运输</span><span class="sxs-lookup"><span data-stu-id="876a9-217">Cancel transport</span></span>

<span data-ttu-id="876a9-218">选中此复选框可将过渡时间从计划编制中排除。</span><span class="sxs-lookup"><span data-stu-id="876a9-218">Select this check box to exclude transit time from the scheduling.</span></span>

## <a name="set-default"></a><span data-ttu-id="876a9-219">设置默认值</span><span class="sxs-lookup"><span data-stu-id="876a9-219">Set default</span></span>
<span data-ttu-id="876a9-220">您可以将当前值保存为默认值。</span><span class="sxs-lookup"><span data-stu-id="876a9-220">You can save the current values as default values.</span></span> <span data-ttu-id="876a9-221">有两个选项：</span><span class="sxs-lookup"><span data-stu-id="876a9-221">There are two options:</span></span>

-   <span data-ttu-id="876a9-222">设置为我的默认值</span><span class="sxs-lookup"><span data-stu-id="876a9-222">Set as my default</span></span>
-   <span data-ttu-id="876a9-223">对所有人设置为默认值</span><span class="sxs-lookup"><span data-stu-id="876a9-223">Set as default for everyone</span></span>


<a name="see-also"></a><span data-ttu-id="876a9-224">请参阅</span><span class="sxs-lookup"><span data-stu-id="876a9-224">See also</span></span>
--------

[<span data-ttu-id="876a9-225">工序级排产</span><span class="sxs-lookup"><span data-stu-id="876a9-225">Operations scheduling</span></span>](operations-scheduling.md)




