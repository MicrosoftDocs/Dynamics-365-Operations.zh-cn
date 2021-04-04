---
title: 仓库应用事件
description: 本主题介绍了作为批处理作业一部分的用于处理仓库应用事件消息的仓库应用事件处理。
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0bafcbd5306860cb80d6e813aabf83853a9011c1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248635"
---
# <a name="warehouse-app-event-processing"></a>仓库应用事件处理

[!include [banner](../includes/banner.md)]

在 Supply Chain Management 中运行的批处理作业可以使用队列中的数据来处理仓库应用发出的事件，以根据需要对发出信号的事件做出反应。 此功能将相关事件添加到队列中，以响应工作人员使用该应用执行的某些类型的操作。 例如，当使用 **通过仓库应用创建和处理转移单** 功能时，如果系统在运行 **处理仓库应用事件** 批处理作业，将在后端创建和更新转移单标题和行。

## <a name="enable-the-process-warehouse-app-events-feature"></a>启用处理仓库应用事件功能

此功能只有在系统中启用了之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)页面检查功能状态，并在需要时启用。 处理仓库应用事件功能列出为：

- **模块** - 仓库管理
- **功能名称** - 处理仓库应用事件

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>设置批处理作业以处理仓库应用事件

### <a name="process-warehouse-app-events"></a>处理仓库应用事件

设置计划的批处理作业以处理用于转移单创建和行更新的仓库应用事件。

1. 转到 **仓库管理 \> 定期任务 \> 处理仓库应用事件**。
1. “处理仓库应用事件”对话框将打开。 展开 **在后台运行** 快速选项卡并将 **批处理** 设置为 **是**。
1. 在 **在后台运行** 快速选项卡上，选择 **重复执行**。
1. **定义重复执行** 对话框将打开。 根据业务需要设置运行计划。
1. 选择 **确定** 以返回到 **处理仓库应用事件** 对话框。
1. 在 **处理仓库应用事件** 对话框中选择 **确定**，将批处理作业添加到批处理队列中。

## <a name="query-warehouse-app-events"></a>查询仓库应用事件

您可以通过转到 **仓库管理 \> 查询和报表 \> 移动设备日志 \> 仓库应用事件** 查看仓库应用生成的事件队列和事件消息。

## <a name="the-standard-event-queue-process"></a>标准事件队列流程

仓库应用事件队列通常将与下面描述的流一起使用：

1. 一个事件随事件消息一起添加到队列中。 新消息最初的事件状态为 **等待**，这意味着 **处理仓库应用事件** 批处理作业将不会接收并处理此消息。
1. 一旦消息状态更新为 **已排队**，**流程仓库应用** 事件批处理作业将会接收并处理事件。
1. 批处理作业将事件状态更新为 **已完成** 或 **失败**，具体取决于请求的流程是否可行。
1. 当所有相关事件消息都是 **已完成** 时，该事件将从队列中删除。

 有关详细示例，请参阅[通过仓库应用创建转移单流程](create-transfer-order-from-warehouse-app.md)。

## <a name="handle-event-errors"></a>处理事件错误

作为仓库事件处理的一部分，所请求的消息活动可能未从批处理作业接收流程。 在这种情况下，事件消息将更改为 **失败**。 您可以使用 **批处理日志** 信息以了解原因并采取必要的措施纠正任何问题。

有关详细示例，请参阅[通过仓库应用创建转移单](create-transfer-order-from-warehouse-app.md)。

若要重置失败的仓库应用事件消息：

1. 转到 **仓库管理 \> 查询和报表 \> 移动设备日志 \> 仓库应用事件**。
1. 在 **仓库应用事件消息** 快速选项卡上，找到并选择在 **事件状态** 列中显示 **失败** 的相关事件。
1. 从 **仓库应用事件消息** 工具栏中选择 **重置**。
1. 继续工作，直到所有相关消息都已重置。

您也可以通过使用 **仓库应用事件消息** 工具栏上的 **删除** 选项删除 **失败** 事件消息。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]