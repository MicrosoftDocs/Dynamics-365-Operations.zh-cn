---
title: 在波次期间计划工作创建
description: 本主题介绍如何设置和使用计划工作创建波次处理方法。
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 36a450f78695f617056875f8d236fe46bc66aaaf
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501214"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="ca0d3-103">在波次期间计划工作创建</span><span class="sxs-lookup"><span data-stu-id="ca0d3-103">Schedule work creation during wave</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ca0d3-104">将 *计划工作创建* 功能用作波次流程的一部分，通过让系统使用并行处理创建工作来帮助提高波浪处理的吞吐量。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="ca0d3-105">启用此功能后，将自动创建计划的工作，系统最终将对其进行处理以创建实际工作。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="ca0d3-106">如果波次负荷行的数量达到预先确定的阈值，系统将通过应用并行的异步处理来更快地创建实际工作。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="ca0d3-107">启用计划工作创建功能</span><span class="sxs-lookup"><span data-stu-id="ca0d3-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="ca0d3-108">在功能管理中启用功能</span><span class="sxs-lookup"><span data-stu-id="ca0d3-108">Enable the feature in feature management</span></span>

<span data-ttu-id="ca0d3-109">*计划工作创建* 功能只有在系统中开启之后才能使用。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="ca0d3-110">管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ca0d3-111">在那里，此功能以以下方式列出：</span><span class="sxs-lookup"><span data-stu-id="ca0d3-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ca0d3-112">**模块**：*仓库管理*</span><span class="sxs-lookup"><span data-stu-id="ca0d3-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ca0d3-113">**功能名称**：*计划工作创建*</span><span class="sxs-lookup"><span data-stu-id="ca0d3-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="ca0d3-114">必须先启用 *组织范围内的工作锁定* 功能，然后才能启用 *计划工作创建*。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="ca0d3-115">手动启用波次的批处理</span><span class="sxs-lookup"><span data-stu-id="ca0d3-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="ca0d3-116">要利用并行异步方法创建仓库工作，您的波次流程必须批量运行。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="ca0d3-117">要进行设置：</span><span class="sxs-lookup"><span data-stu-id="ca0d3-117">To set this up:</span></span>

1. <span data-ttu-id="ca0d3-118">转到 **仓库管理 \> 设置 \> 仓库管理参数**。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="ca0d3-119">在 **常规** 选项卡上，将 **批量处理波次** 设置为 *是*。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="ca0d3-120">或者，您还可以选择专用的 **波次处理批处理组**，来阻止批处理队列处理与其他流程同时运行。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="ca0d3-121">设置 **等待锁定(毫秒)时间**，此值在系统同时处理多个波次时应用。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="ca0d3-122">对于大多数较大的波次流程，我们建议值为 *60000*。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="ca0d3-123">手动为现有波次模板启用新的波次步骤方法</span><span class="sxs-lookup"><span data-stu-id="ca0d3-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="ca0d3-124">首先创建新的波次步骤方法并启用它来进行并行异步任务处理。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="ca0d3-125">转到 **仓库管理 \> 设置 \> 波次 \> 波次流程方法**。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="ca0d3-126">选择  **重新生成方法**，注意 *WHSScheduleWorkCreationWaveStepMethod* 已被添加到您可以在装运波次模板中使用的波次流程方法列表中。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="ca0d3-127">选择带有 **方法** 名称 *WHSScheduleWorkCreationWaveStepMethod* 的记录，然后选择 **任务配置**。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="ca0d3-128">要将新行添加到网格中，在操作窗格上选择 **新建**，使用以下设置：</span><span class="sxs-lookup"><span data-stu-id="ca0d3-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="ca0d3-129">**仓库** - 选择用于计划工作创建处理的仓库。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="ca0d3-130">**最大批处理任务数** - 指定最大批处理任务数。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="ca0d3-131">在大多数情况下，此值应在 8-16 之间，但是我们建议您根据您的方案尝试最佳设置。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="ca0d3-132">**波次处理批处理组** - 选择专用的波次处理批处理组以优化您的批处理队列处理。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="ca0d3-133">现在，您可以更新现有波次模板（或创建新模板）来使用 *计划工作创建* 波次处理方法了。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="ca0d3-134">转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="ca0d3-135">在操作窗格上选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="ca0d3-136">在列表窗格中，选择要更新的波次模板（如果您使用演示数据进行测试，可以使用 *24 装运默认*）。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="ca0d3-137">展开 **方法** 快速选项卡，在 **其余方法** 网格中选择带有 **名** 称 *计划工作创建* 的行。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="ca0d3-138">选择指向 **选定方法** 列的箭头，将选定的行移到该列。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="ca0d3-139">（您一次只能选择一个使用 *WHSScheduleWorkCreationWaveStepMethod* 或 *createWork* 的方法，因此带有 **方法** 名称 *createWork* 的现有行将自动移到 **其余方法** 网格。）</span><span class="sxs-lookup"><span data-stu-id="ca0d3-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="ca0d3-140">设置波次任务处理阈值数据</span><span class="sxs-lookup"><span data-stu-id="ca0d3-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="ca0d3-141">首次使用任何基于任务的处理运行波次流程时，系统将创建默认的波次任务处理阈值数据。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="ca0d3-142">此数据用于控制波次处理何时异步运行以及何时基于任务，让其能够并行处理和创建工作。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="ca0d3-143">默认数据最初会为最小负荷行数 (MINIMUMWAVELOADLINES) 使用阈值 15。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="ca0d3-144">这意味着，当系统处理的波次有超过 15 个负荷行时，将使用异步任务处理。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="ca0d3-145">您可以在测试环境中在 **WHSWaveTaskProcessingThresholdParameters** 表中手动插入/更新此数据，但是如果您需要在生产环境中更改此设置，则必须联系 Microsoft 支持部门请求更新。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="ca0d3-146">使用功能</span><span class="sxs-lookup"><span data-stu-id="ca0d3-146">Work with the feature</span></span>

<span data-ttu-id="ca0d3-147">启用 *计划工作创建* 功能后，波次处理将创建计划工作，其最终将由新工作创建流程使用。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="ca0d3-148">在创建工作期间，将使用 *组织范围内的工作锁定* 功能来阻止工作。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="ca0d3-149">以下流程图显示了波次处理期间计划工作是如何创建的。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![计划工作创建](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="ca0d3-151">计划的工作</span><span class="sxs-lookup"><span data-stu-id="ca0d3-151">Planned work</span></span>

<span data-ttu-id="ca0d3-152">**计划工作详细信息** 页面（**仓库管理 \> 工作 \> 计划工作详细信息**）显示有关计划工作的信息，此信息最初在波次处理期间创建。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="ca0d3-153">提供以下 **流程状态** 值：</span><span class="sxs-lookup"><span data-stu-id="ca0d3-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="ca0d3-154">**已排队** - 计划工作正在等待用于创建工作。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="ca0d3-155">**已完成** - 计划工作已用于创建工作。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="ca0d3-156">**失败** – 波次处理失败。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="ca0d3-157">请注意，无论是否有相关的实际工作，计划工作都可能处于 **失败** 状态。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="ca0d3-158">当实际工作创建流程失败时，实际工作保持 *已取消* 状态。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="ca0d3-159">工作创建流程的批处理作业</span><span class="sxs-lookup"><span data-stu-id="ca0d3-159">Batch job for the work creation process</span></span>

<span data-ttu-id="ca0d3-160">要查看处理波次的批处理作业，在 **所有波次** 页上的操作窗格中选择 **批处理作业**。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="ca0d3-161">从这里，您可以查看每个批处理作业 ID 的所有批处理任务详细信息。</span><span class="sxs-lookup"><span data-stu-id="ca0d3-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]