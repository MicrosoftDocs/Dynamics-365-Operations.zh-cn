---
title: 在波次期间计划工作创建
description: 本主题介绍如何设置和使用计划工作创建波次处理方法。
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e4258c03b12a80a5bd81328ae7418835d68f82e7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835694"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="b1d4b-103">在波次期间计划工作创建</span><span class="sxs-lookup"><span data-stu-id="b1d4b-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b1d4b-104">将 *计划工作创建* 功能用作波次流程的一部分，通过让系统使用并行处理创建工作来帮助提高波浪处理的吞吐量。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="b1d4b-105">启用此功能后，将自动创建计划的工作，系统最终将对其进行处理以创建实际工作。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="b1d4b-106">如果波次负荷行的数量达到预先确定的阈值，系统将通过应用并行的异步处理来更快地创建实际工作。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a><span data-ttu-id="b1d4b-107">在功能管理中打开计划的工作创建功能</span><span class="sxs-lookup"><span data-stu-id="b1d4b-107">Turn on the scheduled work creation features in feature management</span></span>

<span data-ttu-id="b1d4b-108">若要使用本主题中描述的功能，必须为您的系统打开这些功能。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-108">To use the features described in this topic, they must be turned on for your system.</span></span> <span data-ttu-id="b1d4b-109">使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区以按以下顺序打开以下功能：</span><span class="sxs-lookup"><span data-stu-id="b1d4b-109">Use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to turn on the following features in the following order:</span></span>

1. <span data-ttu-id="b1d4b-110">**组织范围内的工作锁定** - 手动和自动配置计划的工作创建时所必需。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-110">**Organization-wide work blocking** - Required for both manual and automatic configuration of scheduled work creation.</span></span>
1. <span data-ttu-id="b1d4b-111">**计划工作创建** - 手动和自动配置计划的工作创建时所必需。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-111">**Schedule work creation** - Required for both manual and automatic configuration of scheduled work creation.</span></span>
1. <span data-ttu-id="b1d4b-112">**组织范围内的“计划工作创建”波次方法** - 自动配置计划的工作创建时所必需。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-112">**Organization-wide "Schedule work creation" wave method** - Required for automatic configuration of scheduled work creation.</span></span> <span data-ttu-id="b1d4b-113">如果仅使用手动配置，则不需要此功能。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-113">You don't need this feature if you will only use manual configuration.</span></span>

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a><span data-ttu-id="b1d4b-114">自动配置计划的工作创建</span><span class="sxs-lookup"><span data-stu-id="b1d4b-114">Automatically configure scheduled work creation</span></span>

<span data-ttu-id="b1d4b-115">如果启用 *组织范围内的“计划工作创建”波次方法* 功能，您的系统将自动发生以下情况：</span><span class="sxs-lookup"><span data-stu-id="b1d4b-115">If you enable the *Organization-wide "Schedule work creation" wave method* feature, the following automatically occurs on your system:</span></span>

- <span data-ttu-id="b1d4b-116">添加和配置 *计划工作创建* 波次方法 (`WHSScheduleWorkCreationWaveStepMethod`) 以在所有法人上并行运行。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-116">The *Schedule work creation* wave method (`WHSScheduleWorkCreationWaveStepMethod`) is added and configured to run in parallel across all legal entities.</span></span>
- <span data-ttu-id="b1d4b-117">所有法人中 **波次模板类型** 设置为 *装运* 并且 **模板状态** 设置为 *有效* 的波次模板将 *创建工作* 方法替换为 *计划工作创建* 方法。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-117">Wave templates from all legal entities that have **Wave template type** set to *Shipping* and **Template status** set to *Valid* will have the *Create work* method replaced by the *Schedule work creation* method.</span></span> <span data-ttu-id="b1d4b-118">但是，将不会修改法人中允许 *创建工作* 方法重复的波次模板。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-118">However, wave templates from legal entities where the *Create work* method is allowed to be repeatable will not be modified.</span></span>
- <span data-ttu-id="b1d4b-119">将为所有法人中启用了 **使用仓库管理流程** 的所有仓库创建 *计划工作创建* 方法的任务配置。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-119">Task configurations for the *Schedule work creation* method will be created for all warehouses from all legal entities that have **Use warehouse management processes** enabled.</span></span> <span data-ttu-id="b1d4b-120">这意味着，默认情况下，*计划工作创建* 方法现在将并行运行。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-120">This means that the *Schedule work creation* method will now run in parallel by default.</span></span> <span data-ttu-id="b1d4b-121">将 **使用仓库管理流程** 从 *否* 更改为 *是* 的现有仓库默认情况下也将并行运行此方法。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-121">Existing warehouses for which you change **Use warehouse management processes** from *No* to *Yes* will also run this method in parallel by default.</span></span>
- <span data-ttu-id="b1d4b-122">所有法人将分批处理波次，如果 **等待锁定（毫秒）** 之前设置为 *0* 毫秒，现在将设置为默认值 *60,000* 毫秒。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-122">All legal entities will process waves in batches and **Wait for lock (ms)** will be set to a default value of *60,000* ms if it was previously set to *0* ms.</span></span>
- <span data-ttu-id="b1d4b-123">您创建的所有新波次模板都将具有 *计划工作创建* 波次方法，而不是 *创建工作* 方法。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-123">All the new wave templates that you create will have the *Schedule work creation* wave method instead of the *Create Work* method.</span></span>

<span data-ttu-id="b1d4b-124">对于已配置为分批处理波次的所有法人以及已配置为并行使用 *计划工作创建* 方法的所有仓库，也将保留现有任务和波次处理配置。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-124">The existing task and wave processing configurations will also be kept for all legal entities that are already configured to process waves in batches, and for all warehouses that are already configured to use the *Schedule work creation* method in parallel.</span></span>

<span data-ttu-id="b1d4b-125">如有必要，您可以通过执行以下操作手动还原在启用 *组织范围内的计划工作创建波次方法* 功能时自动进行的任何或所有设置：</span><span class="sxs-lookup"><span data-stu-id="b1d4b-125">If necessary, you can manually revert any or all of the settings made automatically when you enabled the *Organization-wide Schedule work creation wave method* feature by doing the following:</span></span>

- <span data-ttu-id="b1d4b-126">对于波次模板，转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-126">For wave templates, go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span> <span data-ttu-id="b1d4b-127">将 *计划工作创建* 方法替换为 *创建工作*。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-127">Replace *Schedule work creation* method with *Create work*.</span></span>
- <span data-ttu-id="b1d4b-128">对于仓库参数，转到 **仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-128">For warehouse parameters, go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span> <span data-ttu-id="b1d4b-129">在 **波次处理** 选项卡上，应用 **分批处理波次** 和 **等待锁定(毫秒)** 的首选值。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-129">On the **Wave processing** tab, apply your preferred values for **Process waves in batch** and **Wait for lock (ms)**.</span></span>
- <span data-ttu-id="b1d4b-130">对于波次方法，转到 **仓库管理 \> 设置 \> 波次 \> 波次处理方法**。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-130">For the wave methods, go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span> <span data-ttu-id="b1d4b-131">选择 `WHSScheduleWorkCreationWaveStepMethod`，然后在操作窗格上，选择 **任务配置**。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-131">Select `WHSScheduleWorkCreationWaveStepMethod` and, on the Action Pane, select **Task configuration**.</span></span> <span data-ttu-id="b1d4b-132">根据需要修改或删除每个列出的仓库的批处理任务数和分配的波次组。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-132">Modify or delete the number of batch tasks and the assigned wave group for each listed warehouse as needed.</span></span>

## <a name="manually-configure-scheduled-work-creation"></a><span data-ttu-id="b1d4b-133">手动配置计划的工作创建</span><span class="sxs-lookup"><span data-stu-id="b1d4b-133">Manually configure scheduled work creation</span></span>

<span data-ttu-id="b1d4b-134">如果未启用 [*组织范围内的“计划工作创建”波次方法* 功能](#Auto-enable-schedule-work-creation)，您可以使用本部分中提供的过程来根据需要手动配置计划的工作创建。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-134">If you didn't enable the [*Organization-wide "Schedule work creation" wave method* feature](#Auto-enable-schedule-work-creation), then you can use the procedures provided in this section to manually configure scheduled work creation as needed.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="b1d4b-135">手动启用波次的批处理</span><span class="sxs-lookup"><span data-stu-id="b1d4b-135">Manually enable batch processing of waves</span></span>

<span data-ttu-id="b1d4b-136">要利用并行异步方法创建仓库工作，您的波次流程必须批量运行。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-136">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="b1d4b-137">要进行设置：</span><span class="sxs-lookup"><span data-stu-id="b1d4b-137">To set this up:</span></span>

1. <span data-ttu-id="b1d4b-138">转到 **仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-138">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="b1d4b-139">在 **常规** 选项卡上，将 **批量处理波次** 设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-139">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="b1d4b-140">或者，您还可以选择专用的 **波次处理批处理组**，来阻止批处理队列处理与其他流程同时运行。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-140">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>
1. <span data-ttu-id="b1d4b-141">设置 **等待锁定(毫秒)时间**，此值在系统同时处理多个波次时应用。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-141">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="b1d4b-142">对于大多数较大的波次流程，我们建议值为 *60000*。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-142">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="b1d4b-143">手动为现有波次模板启用新的波次步骤方法</span><span class="sxs-lookup"><span data-stu-id="b1d4b-143">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="b1d4b-144">首先创建新的波次步骤方法并启用它来进行并行异步任务处理。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-144">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="b1d4b-145">转到 **仓库管理 \> 设置 \> 波次 \> 波次流程方法**。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-145">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>
1. <span data-ttu-id="b1d4b-146">选择  **重新生成方法**，注意 *WHSScheduleWorkCreationWaveStepMethod* 已被添加到您可以在装运波次模板中使用的波次流程方法列表中。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-146">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>
1. <span data-ttu-id="b1d4b-147">选择带有 **方法** 名称 *WHSScheduleWorkCreationWaveStepMethod* 的记录，然后选择 **任务配置**。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-147">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>
1. <span data-ttu-id="b1d4b-148">要将新行添加到网格中，在操作窗格上选择 **新建**，使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="b1d4b-148">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="b1d4b-149">**仓库** - 选择用于计划工作创建处理的仓库。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-149">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>
    - <span data-ttu-id="b1d4b-150">**最大批处理任务数** - 指定最大批处理任务数。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-150">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="b1d4b-151">在大多数情况下，此值应在 8-16 之间，但是我们建议您根据您的方案尝试最佳设置。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-151">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>
    - <span data-ttu-id="b1d4b-152">**波次处理批处理组** - 选择专用的波次处理批处理组以优化您的批处理队列处理。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-152">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="b1d4b-153">现在，您可以更新现有波次模板（或创建新模板）来使用 *计划工作创建* 波次处理方法了。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-153">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="b1d4b-154">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-154">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="b1d4b-155">在操作窗格上选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-155">Select **Edit** on the Action Pane.</span></span>
1. <span data-ttu-id="b1d4b-156">在列表窗格中，选择要更新的波次模板（如果您使用演示数据进行测试，可以使用 *24 装运默认*）。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-156">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>
1. <span data-ttu-id="b1d4b-157">展开 **方法** 快速选项卡，在 **其余方法** 网格中选择带有 **名** 称 *计划工作创建* 的行。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-157">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>
1. <span data-ttu-id="b1d4b-158">选择指向 **选定方法** 列的箭头，将选定的行移到该列。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-158">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="b1d4b-159">（您一次只能选择一个使用 `WHSScheduleWorkCreationWaveStepMethod` 或 `createWork` 的方法，因此带有 **方法名称** `createWork` 的现有行将自动移到 **其余方法** 网格。）</span><span class="sxs-lookup"><span data-stu-id="b1d4b-159">(You can only have one selected method at a time that uses either `WHSScheduleWorkCreationWaveStepMethod` or `createWork`, so the existing row with **Method name** `createWork` is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="b1d4b-160">设置波次任务处理阈值数据</span><span class="sxs-lookup"><span data-stu-id="b1d4b-160">Set wave task processing threshold data</span></span>

<span data-ttu-id="b1d4b-161">首次使用任何基于任务的处理运行波次流程时，系统将创建默认的波次任务处理阈值数据。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-161">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="b1d4b-162">此数据用于控制波次处理何时异步运行以及何时基于任务，让其能够并行处理和创建工作。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-162">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="b1d4b-163">默认数据最初会为最小负荷行数 (`MINIMUMWAVELOADLINES`) 使用阈值 15。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-163">The default data will initially use a threshold value of 15 for the minimum number of load lines (`MINIMUMWAVELOADLINES`).</span></span> <span data-ttu-id="b1d4b-164">这意味着，当系统处理的波次有超过 15 个负荷行时，将使用异步任务处理。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-164">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="b1d4b-165">您可以在测试环境中手动插入/更新 `WHSWaveTaskProcessingThresholdParameters` 表中的此数据。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-165">You can manually insert/update this data in the `WHSWaveTaskProcessingThresholdParameters` table in your test environments.</span></span> <span data-ttu-id="b1d4b-166">如果需要在生产环境中更改此设置，则必须联系 Microsoft 支持部门以请求更新。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-166">If you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-scheduled-work-creation"></a><span data-ttu-id="b1d4b-167">使用计划工作创建</span><span class="sxs-lookup"><span data-stu-id="b1d4b-167">Work with the scheduled work creation</span></span>

<span data-ttu-id="b1d4b-168">有关如何处理计划的工作创建的详细信息，请参阅[波次创建和处理](wave-processing.md)。</span><span class="sxs-lookup"><span data-stu-id="b1d4b-168">For details about how to work with scheduled work creation, see [Wave creation and processing](wave-processing.md).</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
