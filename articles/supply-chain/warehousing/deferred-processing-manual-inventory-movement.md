---
title: 延期处理手动库存变动
description: 本主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中使用延期处理手动库存变动。
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 21dd01448fcf6c2b3ca90a5476fad061bb0f55e4
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102731"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>延期处理手动库存变动

[!include [banner](../includes/banner.md)]

本主题介绍如何在 Microsoft Dynamics 365 Supply Chain Management 中使用延期处理手动库存变动。

延期处理让仓库工作人员可以在后台处理放置操作期间继续执行其他工作。 当服务器的处理时间临时或意外增加，并且增加的处理时间可能影响工作人员的生产率时，延期处理非常有用。 *库存变动* 工作类型现已添加到此功能支持的工作类型集中。

后台处理通过使用[处理仓库应用事件功能](warehouse-app-events.md)实现。

## <a name="turn-on-this-feature-for-your-system"></a>为您的系统启用此功能

若要使此功能可用，请在[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)中打开以下功能。 您必须按以下顺序打开它们：

1. *组织范围内的工作阻止*<br>（从 Supply Chain Management 版本 10.0.21 开始，此功能是强制性的，因此默认情况下处于开启状态，无法再次关闭。）
1. *处理仓库应用事件*<br>（从 Supply Chain Management 版本 10.0.25 开始，此功能默认开启。）
1. *延迟 PUT 操作*
1. *延迟处理手动库存变动操作*<br>（从 Supply Chain Management 版本 10.0.25 开始，此功能是强制性的，因此默认情况下处于开启状态，无法再次关闭。）

## <a name="configure-the-work-processing-policies"></a>配置工作处理策略

若要使用推迟处理，必须设置并使用工作处理策略。 对于延期放置处理，[延期处理仓库工作功能](deferred-put.md)支持以下工作类型：*销售订单*、*转移单发货* 和 *补货*。 *延期处理手动库存变动操作* 功能添加了新的工作类型：*库存变动*。

要设置工作处理策略，请按照下列步骤操作。

1. 转到 **仓库管理 \> 设置 \> 工作 \> 工作处理策略**。
1. 在列表中选择一个现有策略，或者在操作窗格上选择 **新建** 创建一个新策略。 每个策略的标头都有以下字段：

    - **工作处理策略名称** – 工作处理策略的名称。
    - **描述** – 工作处理策略的描述。

1. 在 **处理规则** 快速选项卡上，设置将应用策略的规则集合。 使用工具栏上的按钮可以根据需要添加或删除规则。 对于每个规则，设置以下字段：

    - **工作订单类型** – 选择策略应用的工作类型。
    - **操作** – 选择策略用于处理的操作。 如果您在 **工作订单类型** 字段中选择了 *库存变动*，则不必设置此字段，因为领料操作和放置操作都将作为单个事件处理。
    - **工作处理方法** – 选择用于处理工作行的方法。 如果选择 *立即*，行为类似未使用任何工作处理策略来处理行时的行为。 如果选择 *延期*，系统将应用使用批处理框架的延期处理。
    - **延期处理阈值** – 如果将此字段设置为 *0*（零），将没有阈值。 在这种情况下，如果可能，会使用 *延期* 处理方法。 如果阈值的具体计算结果低于阈值，则使用 *立即* 方法。 否则，如果可能，则使用 *延期* 方法。 对于与销售和运输有关的工作，计算出的阈值是正在为工作处理的关联源负荷行的数量。 对于补货工作，计算出的阈值是工作正在补货的工作行的数量。 例如，如果将销售的阈值设置为 *5*，您将确保初始源负荷行少于五个的较小工作不使用延期处理，但是大量工作则会使用。 仅当 **工作处理方法** 字段设置为 *延期* 时，此阈值才有效。
    - **延期处理批处理组** – 指定用于处理的批处理组。 如果您在 **工作订单类型** 字段中选择了 *库存变动*，则不必设置此字段，因为已在 **处理仓库应用事件** 对话框中选择了批处理组。

## <a name="assign-the-work-creation-policy"></a>分配工作创建策略

有关如何分配作品创建策略的详细信息，请参阅[延期处理仓库工作](deferred-put.md)。

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>设置批处理作业以处理仓库应用事件

要使用 *延期处理手动库存变动操作* 流程，需要设置计划的批处理作业。

1. 转到 **仓库管理 \> 定期任务 \> 处理仓库应用事件**。
1. 在 **处理仓库应用事件** 对话框中，在 **在后台运行** 快速选项卡上，将 **批处理** 选项设置为 *是*。
1. 选择 **定期**，设置符合您的业务要求的运行计划。
1. 在每个对话框中选择 **确定**。

## <a name="inquire-about-the-warehouse-app-events"></a>查询仓库应用事件

您可以通过转到 **仓库管理 \> 查询和报表 \> 移动设备日志 \> 仓库应用事件** 查看仓库应用生成的事件队列和事件消息。

首次创建时，*库存变动* 事件消息的状态为 *已排队*。 此状态指示 **处理仓库应用事件** 批处理作业将选取事件消息并进行处理。 当状态更新为 *已完成* 时，所有相关事件将从队列中删除。

所有 *库存变动* 事件按事件类型和仓库在一个集合下累积。

批处理作业将根据在 **处理仓库应用事件** 对话框中设置的定期处理仓库应用事件。 因此，在消息被处理之前，您可以通过在 **标识符** 字段中查找来查找仓库 ID。

消息的详细信息包含变动详细信息（例如，“起始”和“目标”位置）。

有关详细信息，请参阅[仓库应用事件处理](warehouse-app-events.md)。

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>配置移动设备菜单以跳过推迟处理策略

有关如何配置移动设备菜单以跳过延期处理策略的详细信息，请参阅[延期处理仓库工作](deferred-put.md)。

## <a name="impact-on-closed-work-dates"></a>对工作关闭日期的影响

有关对已关闭工作日期的影响的详细信息，请参阅[延期处理仓库工作](deferred-put.md)。

## <a name="additional-resources"></a>其他资源

- [仓库工作延期处理](deferred-put.md)
- [仓库应用事件处理](warehouse-app-events.md)
- [设置移动设备以执行仓库工作](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
