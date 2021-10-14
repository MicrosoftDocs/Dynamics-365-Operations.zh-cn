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
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 358f5a87cdb42f0ff646948da8d38475cf49e3f2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577904"
---
# <a name="schedule-work-creation-during-wave"></a>在波次期间计划工作创建

[!include [banner](../../includes/banner.md)]

将 *计划工作创建* 功能用作波次流程的一部分，通过让系统使用并行处理创建工作来帮助提高波浪处理的吞吐量。

启用此功能后，将自动创建计划的工作，系统最终将对其进行处理以创建实际工作。 如果波次负荷行的数量达到预先确定的阈值，系统将通过应用并行的异步处理来更快地创建实际工作。

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>在功能管理中打开计划的工作创建功能

若要使用本主题中描述的功能，必须为您的系统打开这些功能。 使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区以按以下顺序打开以下功能：

1. **组织范围内的工作锁定** - 手动和自动配置计划的工作创建时所必需。
1. **计划工作创建** - 手动和自动配置计划的工作创建时所必需。
1. **组织范围内的“计划工作创建”波次方法** - 自动配置计划的工作创建时所必需。 如果仅使用手动配置，则不需要此功能。

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>自动配置计划的工作创建

如果启用 *组织范围内的“计划工作创建”波次方法* 功能，您的系统将自动发生以下情况：

- 添加和配置 *计划工作创建* 波次方法 (`WHSScheduleWorkCreationWaveStepMethod`) 以在所有法人上并行运行。
- 所有法人中 **波次模板类型** 设置为 *装运* 并且 **模板状态** 设置为 *有效* 的波次模板将 *创建工作* 方法替换为 *计划工作创建* 方法。 但是，将不会修改法人中允许 *创建工作* 方法重复的波次模板。
- 将为所有法人中启用了 **使用仓库管理流程** 的所有仓库创建 *计划工作创建* 方法的任务配置。 这意味着，默认情况下，*计划工作创建* 方法现在将并行运行。 将 **使用仓库管理流程** 从 *否* 更改为 *是* 的现有仓库默认情况下也将并行运行此方法。
- 所有法人将分批处理波次，如果 **等待锁定（毫秒）** 之前设置为 *0* 毫秒，现在将设置为默认值 *60,000* 毫秒。
- 您创建的所有新波次模板都将具有 *计划工作创建* 波次方法，而不是 *创建工作* 方法。

对于已配置为分批处理波次的所有法人以及已配置为并行使用 *计划工作创建* 方法的所有仓库，也将保留现有任务和波次处理配置。

如有必要，您可以通过执行以下操作手动还原在启用 *组织范围内的计划工作创建波次方法* 功能时自动进行的任何或所有设置：

- 对于波次模板，转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。 将 *计划工作创建* 方法替换为 *创建工作*。
- 对于仓库参数，转到 **仓库管理 \> 设置 \> 仓库管理参数**。 在 **波次处理** 选项卡上，应用 **分批处理波次** 和 **等待锁定(毫秒)** 的首选值。
- 对于波次方法，转到 **仓库管理 \> 设置 \> 波次 \> 波次处理方法**。 选择 `WHSScheduleWorkCreationWaveStepMethod`，然后在操作窗格上，选择 **任务配置**。 根据需要修改或删除每个列出的仓库的批处理任务数和分配的波次组。

## <a name="manually-configure-scheduled-work-creation"></a>手动配置计划的工作创建

如果未启用 [*组织范围内的“计划工作创建”波次方法* 功能](#Auto-enable-schedule-work-creation)，您可以使用本部分中提供的过程来根据需要手动配置计划的工作创建。

### <a name="manually-enable-batch-processing-of-waves"></a>手动启用波次的批处理

要利用并行异步方法创建仓库工作，您的波次流程必须批量运行。 要进行设置：

1. 转到 **仓库管理 \> 设置 \> 仓库管理参数**。
1. 在 **常规** 选项卡上，将 **批量处理波次** 设置为 *是*。 或者，您还可以选择专用的 **波次处理批处理组**，来阻止批处理队列处理与其他流程同时运行。
1. 设置 **等待锁定(毫秒)时间**，此值在系统同时处理多个波次时应用。 对于大多数较大的波次流程，我们建议值为 *60000*。

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>手动为现有波次模板启用新的波次步骤方法

首先创建新的波次步骤方法并启用它来进行并行异步任务处理。

1. 转到 **仓库管理 \> 设置 \> 波次 \> 波次流程方法**。
1. 选择  **重新生成方法**，注意 *WHSScheduleWorkCreationWaveStepMethod* 已被添加到您可以在装运波次模板中使用的波次流程方法列表中。
1. 选择带有 **方法** 名称 *WHSScheduleWorkCreationWaveStepMethod* 的记录，然后选择 **任务配置**。
1. 要将新行添加到网格中，在操作窗格上选择 **新建**，使用以下设置：

    - **仓库** - 选择用于计划工作创建处理的仓库。
    - **最大批处理任务数** - 指定最大批处理任务数。 在大多数情况下，此值应在 8-16 之间，但是我们建议您根据您的方案尝试最佳设置。
    - **波次处理批处理组** - 选择专用的波次处理批处理组以优化您的批处理队列处理。

现在，您可以更新现有波次模板（或创建新模板）来使用 *计划工作创建* 波次处理方法了。

1. 转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。
1. 在操作窗格上选择 **编辑**。
1. 在列表窗格中，选择要更新的波次模板（如果您使用演示数据进行测试，可以使用 *24 装运默认*）。
1. 展开 **方法** 快速选项卡，在 **其余方法** 网格中选择带有 **名** 称 *计划工作创建* 的行。
1. 选择指向 **选定方法** 列的箭头，将选定的行移到该列。 （您一次只能选择一个使用 `WHSScheduleWorkCreationWaveStepMethod` 或 `createWork` 的方法，因此带有 **方法名称** `createWork` 的现有行将自动移到 **其余方法** 网格。）

## <a name="set-wave-task-processing-threshold-data"></a>设置波次任务处理阈值数据

首次使用任何基于任务的处理运行波次流程时，系统将创建默认的波次任务处理阈值数据。 此数据用于控制波次处理何时异步运行以及何时基于任务，让其能够并行处理和创建工作。

默认数据最初会为最小负荷行数 (`MINIMUMWAVELOADLINES`) 使用阈值 15。 这意味着，当系统处理的波次有超过 15 个负荷行时，将使用异步任务处理。 您可以在测试环境中手动插入/更新 `WHSWaveTaskProcessingThresholdParameters` 表中的此数据。 如果需要在生产环境中更改此设置，则必须联系 Microsoft 支持部门以请求更新。

## <a name="work-with-the-scheduled-work-creation"></a>使用计划工作创建

有关如何处理计划的工作创建的详细信息，请参阅[波次创建和处理](wave-processing.md)。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
