---
title: 在波次期间计划波次标签打印
description: 本主题介绍了如何设置和使用基于任务的波次标签打印功能。
author: MSFTGarm
ms.date: 06/09/2021
ms.topic: article
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-obaranov
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 652e6fb3f586fc873ffabf2c741e5c99216931461f159a42f08f9922e756280f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735888"
---
# <a name="schedule-wave-label-printing-during-wave"></a>在波次期间计划波次标签打印

[!include [banner](../../includes/banner.md)]

使用 *基于任务的波次标签打印* 功能作为波次流程的一部分，以帮助提高效率，并使系统创建波次标签并在单独的任务中工作。

配置波次标签打印的流程很复杂，并且依赖于准确的配置和主数据。 生成波次标签记录失败的情况并不少见，当失败时，整个波次处理都会回滚。 *基于任务的波次标签打印* 功能帮助您避免在每次错误打印波次标签时都必须重新创建工作和工作行。

使用 *基于任务的波次标签打印* 功能时，系统首先创建工作和工作行。 然后，创建并打印波次标签。 最后，如果正确创建了波次标签，将发放工作和波次以供领料。

## <a name="turn-on-the-task-based-wave-label-printing-feature-in-feature-management"></a>在功能管理中打开“基于任务的波次标签打印”功能

若要使用本主题中描述的功能，必须为您的系统打开这些功能。 使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区按以下顺序打开功能：

1. *波次标签打印* – 为波次标签打印启用波次流程方法时需要此功能。
1. *组织范围内的工作锁定* - 手动和自动配置计划的工作创建时需要此功能。
1. *基于任务的波次标签打印* – 将波次标签打印拆分为单独的交易范围时需要此功能。

## <a name="manually-enable-the-new-wave-step-method"></a>手动启用新的波次步骤方法

必须首先创建新的波次步骤方法并启用它来进行并行异步任务处理。

1. 转到 **仓库管理 \> 设置 \> 波次 \> 波次流程方法**。
1. 在操作窗格上，选择 **重新生成方法**。 请注意，*waveLabelPrinting* 将添加到可在装运波次模板中使用的波次流程方法列表中。
1. 选择 **方法名称** 字段设置为 *waveLabelPrinting* 的记录，然后在操作窗格上，选择 **任务配置**。
1. 在操作窗格上，选择 **新建** 向网格添加一行。 然后，针对新行设置以下字段：

    - **仓库** – 选择用于计划工作创建处理的仓库。 （如果您使用演示数据进行测试，可以选择仓库 *24*。）
    - **最大批处理任务数** – 指定最大批处理任务数。 在大多数情况下，该值应介于 *8* 至 *16* 之间。 但是，我们建议您尝试为您的场景找到最佳设置。
    - **波次处理批处理组** – 选择专用的波次处理批处理组以优化批处理队列处理。

您现在可以更新现有的波次模板，以便它使用 *波次标签打印* 波次处理方法。 或者，您可以创建一个使用它的新波次模板。

1. 转到 **仓库管理 \> 设置 \> 波次 \> 波次模板**。
1. 在操作窗格上，选择 **编辑**。
1. 在列表窗格中，选择要更新的波次模板。 （如果您使用演示数据进行测试，可以选择仓库 *24 装运默认*。）
1. 在 **方法** 快速选项卡上的 **其余方法** 列中，选择 **名称** 字段设置为 *waveLabelPrinting* 的行。
1. 选择 **添加**（向右箭头按钮）以将选定行添加到 **选定方法** 列。
1. 在 **波次步骤代码** 字段中，输入将用于使波次模板与波次标签模板连接的波次步骤代码。

## <a name="set-wave-task-processing-threshold-data"></a>设置波次任务处理阈值数据

首次使用任何基于任务的处理运行波次流程时，系统将创建默认的波次任务处理阈值数据。 此数据用于控制波次处理是异步运行还是基于任务，以便它可以并行处理和创建波次标签。

默认数据最初会为最小工作 ID 数 (`MinimumWorkThresholdForLabelPrinting`) 使用阈值 *1*。 因此，当系统处理具有多个工作 ID 的波次时，它将在单独的交易中使用基于任务的波次标签处理。 您可以在测试环境中手动插入或更新 `WHSWaveTaskProcessingThresholdParameters` 表中的此数据。 若要在生产环境中更改此设置，必须联系 Microsoft 支持部门以请求更新。

## <a name="changes-to-the-wave-processing-logic-when-task-based-wave-label-printing-is-used"></a>使用基于任务的波次标签打印时波次处理逻辑的变化

如果波次标签处理超过波次任务处理阈值，将启动基于任务的处理。 在下一个适合波次模板的波次处理中，波次标签打印将在工作创建后立即在单独的 *ttsbegin*/*ttscommit* 交易中运行。 如果工作发放（解锁）在波次模板上配置为自动运行，将仅在波次标签打印流程成功完成后进行。

如果波次标签生成失败（例如，如果将工作数量转换为波次标签数量失败并引发错误），仅相应的交易失败。 先前创建的工作保持冻结状态。 若要更正错误并打印波次标签，请按照以下步骤操作。

1. 转到 **仓库管理 \> 出站波次 \> 装运波次 \> 所有波次**。
1. 在网格中选择相关波次。
1. 在“操作窗格”的 **波次** 选项卡上，在 **打印** 组中，选择 **波次标签**。
1. 按照屏幕上的说明发送标签进行打印。
1. 在操作窗格上的 **波次** 选项卡上，在 **波次** 组中，选择 **发放** 以手动发放选定波次的工作。

## <a name="additional-resources"></a>其他资源

- [波次标签打印](configure-wave-label-printing.md)
- [波次期间安排工作创建](configure-wave-schedule-work-creation.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
