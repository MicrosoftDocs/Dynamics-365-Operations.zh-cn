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
# <a name="schedule-work-creation-during-wave"></a>在波次期间计划工作创建

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

将 *计划工作创建* 功能用作波次流程的一部分，通过让系统使用并行处理创建工作来帮助提高波浪处理的吞吐量。

启用此功能后，将自动创建计划的工作，系统最终将对其进行处理以创建实际工作。 如果波次负荷行的数量达到预先确定的阈值，系统将通过应用并行的异步处理来更快地创建实际工作。

## <a name="enable-the-schedule-work-creation-feature"></a>启用计划工作创建功能

### <a name="enable-the-feature-in-feature-management"></a>在功能管理中启用功能

*计划工作创建* 功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区检查功能状态和开启功能（如果需要）。 在那里，此功能以以下方式列出：

- **模块**：*仓库管理*
- **功能名称**：*计划工作创建*

> [!NOTE]
> 必须先启用 *组织范围内的工作锁定* 功能，然后才能启用 *计划工作创建*。

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

1. 选择指向 **选定方法** 列的箭头，将选定的行移到该列。 （您一次只能选择一个使用 *WHSScheduleWorkCreationWaveStepMethod* 或 *createWork* 的方法，因此带有 **方法** 名称 *createWork* 的现有行将自动移到 **其余方法** 网格。）

## <a name="set-wave-task-processing-threshold-data"></a>设置波次任务处理阈值数据

首次使用任何基于任务的处理运行波次流程时，系统将创建默认的波次任务处理阈值数据。 此数据用于控制波次处理何时异步运行以及何时基于任务，让其能够并行处理和创建工作。

默认数据最初会为最小负荷行数 (MINIMUMWAVELOADLINES) 使用阈值 15。 这意味着，当系统处理的波次有超过 15 个负荷行时，将使用异步任务处理。 您可以在测试环境中在 **WHSWaveTaskProcessingThresholdParameters** 表中手动插入/更新此数据，但是如果您需要在生产环境中更改此设置，则必须联系 Microsoft 支持部门请求更新。

## <a name="work-with-the-feature"></a>使用功能

启用 *计划工作创建* 功能后，波次处理将创建计划工作，其最终将由新工作创建流程使用。 在创建工作期间，将使用 *组织范围内的工作锁定* 功能来阻止工作。

以下流程图显示了波次处理期间计划工作是如何创建的。

![计划工作创建](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>计划的工作

**计划工作详细信息** 页面（**仓库管理 \> 工作 \> 计划工作详细信息**）显示有关计划工作的信息，此信息最初在波次处理期间创建。 提供以下 **流程状态** 值：

- **已排队** - 计划工作正在等待用于创建工作。
- **已完成** - 计划工作已用于创建工作。
- **失败** – 波次处理失败。 请注意，无论是否有相关的实际工作，计划工作都可能处于 **失败** 状态。 当实际工作创建流程失败时，实际工作保持 *已取消* 状态。

### <a name="batch-job-for-the-work-creation-process"></a>工作创建流程的批处理作业

要查看处理波次的批处理作业，在 **所有波次** 页上的操作窗格中选择 **批处理作业**。

从这里，您可以查看每个批处理作业 ID 的所有批处理任务详细信息。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]