---
title: Cloud Scale Unit 和 Edge Scale Unit 的制造执行工作负荷
description: 本主题介绍制造执行工作负荷如何使用 Cloud Scale Unit 和 Edge Scale Unit。
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08c46655d3966ad1433935318c5e60667dd10bb6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967751"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Cloud Scale Unit 和 Edge Scale Unit 的制造执行工作负荷

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> 当使用工作负荷缩放单元时，公开预览版中不完全支持某些业务功能。

在制造执行中，Cloud Scale Unit 和 Edge Scale Unit 提供以下功能，即使 Edge 单元未连接到中心：

- 机器操作员和车间主管可以访问操作生产计划。
- 机器操作员可以通过运行离散和流程制造作业来使计划保持最新状态。
- 车间主管可以调整操作计划。
- 工作人员可以访问在 Edge 中上下班打卡的考勤管理，以确保正确计算工作人员工资。

本主题介绍制造执行工作负荷如何使用 Cloud Scale Unit 和 Edge Scale Unit。

## <a name="the-manufacturing-lifecycle"></a>制造生命周期

如下图所示，制造生命周期分为三个阶段：*计划*、*执行* 和 *完成*。

[![使用单个环境时的制造执行阶段](media/mes-phases.png "使用单个环境时的制造执行阶段")](media/mes-phases-large.png)

_计划_ 阶段包括产品定义、计划、订单创建和计划编制以及发放。 发放步骤指示从 _计划_ 阶段转换为 _执行_ 阶段。 发放生产订单后，生产订单作业将在生产车间可见并准备好执行。

当生产作业标记为已完成时，它将从 _执行_ 阶段移动到 _完成_ 阶段。 在 _完成_ 阶段中，*执行* 阶段中的登记将完成审批工作流，在该工作流中计算、批准和传输它们。 此时，生产订单已完成。 因此，将生成工作人员工资的基础。

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>将执行阶段拆分为单独的工作负荷

如下图所示，使用缩放单元时，_执行_ 阶段将拆分为单独的工作负荷。

[![使用缩放单元时的制造执行阶段](media/mes-phases-workloads.png "使用缩放单元时的制造执行阶段")](media/mes-phases-workloads-large.png)

现在，该模型将从单实例安装变为基于中心和缩放单元的模型。 _计划_ 和 _完成_ 阶段在中心上作为后台操作运行，制造执行工作负荷在缩放单元上运行。 在中心和缩放单元之间异步传输数据。

在中心上发放生产订单后，处理生产作业所需的所有数据都将传输到缩放单元。 此数据包括生产订单、生产工艺路线、物料清单和产品。 与生产订单无关的数据（例如间接活动、缺勤代码和生产参数）也将从中心传输到缩放单元。 通常，只能在中心上创建或更新源自中心且传输到缩放单元的数据。 例如，不能在缩放单元上创建新的缺勤代码或间接活动&mdash;它们只能用于登记。 然后，在执行过程中在缩放单元上进行的登记将传输到中心，可在该中心上处理考勤管理审批、库存和财务更新。

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>可在工作负荷上运行的制造执行任务

使用缩放单元时，以下制造执行任务当前可以在工作负荷上运行：

- 上班打卡、登录、下班打卡和缺勤
- 开始作业
- 捆绑作业
- 报告进度
- 报告报废物料
- 间接活动
- 休息

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>在中心上使用制造执行工作负荷

通常，运行制造执行工作负荷所需的流程会自动运行，以根据需要使中心和所有缩放单元保持同步。 但是，如果遇到问题，可以手动触发从工作负荷收到的原始登记的处理和/或查看登记处理日志。

### <a name="manually-process-raw-registrations"></a>手动处理原始登记

Supply Chain Management 中的批处理作业会自动运行，以处理从工作负荷收到的所有登记。 在针对工作负荷上的已完成作业处理登记时，此作业将创建所需的生产日记帐和日志条目。

尽管作业通常会自动运行，但您可以通过登录到中心并转到 **生产控制 \> 定期任务 \> 后台工作负荷管理 \> 处理原始登记** 随时手动运行它。

### <a name="check-the-raw-registration-processing-log"></a>查看原始登记处理日志

若要查看登记处理日志，请登录到中心，然后转到 **生产控制 \> 定期任务 \> 后台工作负荷管理 \> 原始登记处理日志**。 **原始登记处理日志** 页面显示已处理的原始登记的列表以及每个登记的状态。

![原始登记处理日志页面](media/mes-processing-log.png "原始登记处理日志页面")

您可以通过选择列表中的任何登记，然后选择操作窗格上的以下按钮之一来处理登记：

- **处理** – 手动处理选定的登记。 如果 _处理原始登记_ 作业未运行或者已失败，此操作可能有用。
- **取消** – 取消选定的登记。

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>在缩放单元上使用制造执行工作负荷

通常，运行制造执行工作负荷所需的流程会自动运行，以根据需要使中心和所有缩放单元保持同步。 但是，如果遇到问题，您可以查看缩放单元上已处理的订单历史记录或手动运行 _制造中心到缩放单元消息处理器_ 作业。

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>查看缩放单元上已处理的制造作业的历史记录

若要查看缩放单元上已处理的制造作业的历史记录，然后转到 **生产控制 \> 定期任务 \> 后台工作负荷管理 \> 制造作业处理历史记录**。 **制造作业处理历史记录** 页面显示缩放单元上生产订单的处理历史记录。 您可以通过选择列表中的任何生产订单，然后选择操作窗格上的以下按钮之一来处理生产订单：

- **处理** – 手动处理选定的生产订单。
- **取消** – 取消选定的生产订单。

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>制造中心到缩放单元消息处理器作业

_制造中心到缩放单元消息处理器_ 作业处理从中心到缩放单元的数据。 在部署制造执行工作负荷时将自动启动此作业。 但是，您可以通过转到 **生产控制 \> 定期任务 \> 后台工作负荷管理 \> 制造中心到缩放单元消息处理器** 随时手动运行它。
