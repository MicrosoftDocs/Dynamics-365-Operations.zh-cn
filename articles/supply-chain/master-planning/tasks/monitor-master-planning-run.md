---
title: 监控主计划运行
description: 本主题说明生产规划员如何查看主计划运行是否正在进行。
author: ChristianRytt
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4db1173b35cd196ab39fae3cac3754439fab84d0
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103155"
---
# <a name="monitor-a-master-planning-run"></a>监控主计划运行

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>使用甘特图可视化主计划进度

在 **查看主计划进度** 页面上，您可以甘特图形式查看历史主计划运行的详细信息。 此功能可以帮助您了解在主计划的各个阶段花费的时间。 对于当前的活动计划作业，可以使用 **查看主计划进度** 页面来跟踪进度并查看估计的剩余时间。

### <a name="turn-the-master-plan-progress-visualization-feature-on-or-off"></a>打开或关闭主计划进度可视化功能

从 Supply Chain Management 版本 10.0.21 开始，此功能默认开启。 从 Supply Chain Management 10.0.25 开始，此功能是强制性的，无法关闭。 如果您运行的版本早于 10.0.25，管理员可以通过在 [功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区中搜索 *主计划进度可视化* 功能来打开或关闭此功能。

### <a name="use-the-master-plan-progress-visualization-feature"></a>使用主计划进度可视化功能

**查看主计划进度** 页面可以显示历史计划作业和活动计划作业。 

要查看历史计划作业，有两个选项。 

1. 转到 **主计划 \> 设置 \> 计划 \> 主计划**，然后在操作窗格上选择 **历史记录**。 选择所需作业后，选择 **查询**，然后选择 **查看进度**
1. 转到 **主计划 \> 工作区 \> 主计划**，在主计划磁贴上，单击 **历史记录**。 选择所需作业后，选择 **查询**，然后选择 **查看进度**

要查看活动计划作业，有两个选项。 
1. 转到 **主计划 \> 工作区 \> 主计划**，在操作窗格上，选择 **未完成的计划流程**。 选择所需的作业后，选择 **查询**，然后选择 **查看进度**。
1. 转到 **主计划 \> 工作区 \> 主计划**，在主计划磁贴上，单击 **查看进度**。 选择所需作业后，选择 **查询**，然后选择 **查看进度**

请注意，仅当正在处理计划作业时，才能查看活动作业。

### <a name="analyze-a-master-planning-job"></a>分析主计划作业

在甘特图中，您可以展开以下每个计划流程以查看所花费时间的其他详细信息：

- 正在初始化
- 正在删除和删除数据
- 覆盖范围计划
- 延迟
- 行动消息
- 最终完成
- 自动固定

如果要查看使用操作消息的影响，甘特图是一个有用的工具。

#### <a name="navigation-in-the-gantt-chart"></a>甘特图中的导航

- 要展开所选组并显示详细信息，请在树视图中选择加号 (**+**)。
- 要折叠选定的组，请在树视图中选择减号 (**–**)。
- 您可以使用键盘进行导航。 使用 **向上箭头** 和 **向下箭头** 键在行之间移动。 使用 **向右箭头** 和 **向左箭头** 键展开和折叠组。
- 要打开或关闭甘特图中的所有级别，请选择 **全部展开** 或 **全部折叠**。
- 要查看相关的处理时间，将鼠标悬停在任务上。 （任务是甘特图中的最低级别。）

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>查看其他主计划运行以比较作业

通过在 **显示其他主计划运行** 字段上选择一个主计划作业，您可以在甘特图中查看其他主计划运行并比较两个作业。

#### <a name="bom-level-display"></a>BOM 级别显示

物料清单 (BOM) 级别对于覆盖范围计划、延迟、操作和确认的显示不同。

- **覆盖范围计划** – BOM 级别按预期显示。 它们从上到下计算。

    **示例：** BOM 级别 0、1、2

- **延迟** – BOM 级别显示为覆盖范围计划 BOM 级别乘以 –1。 （换句话说，它们有一个负号。）

    **示例：** BOM 级别 –2、–1、0

- **操作消息** – BOM 级别按预期显示。 它们从上到下计算。

    **示例：** BOM 级别 0、1、2

- **自动确认** – BOM 级别显示为 999 减去覆盖范围计划 BOM 级别。

    **示例：** BOM 级别 999、998、997

下表汇总了此行为。

| 显示的 BOM 级别 | 成品 | 子组件 | 原材料 |
|---|---|---|---|
| 覆盖范围计划 | 0 | 1 | 2 |
| 延迟 | 0 | –1 | –2 |
| 行动消息 | 0 | 1 | 2 |
| 自动固定 | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>可视化进度

如果查看当前正在运行的主计划作业，进度将通过甘特图中的颜色显示。 以下颜色适用于蓝色主题。 对于其他颜色主题，颜色将不同。

- **深蓝色** – 完成的计划任务。
- **橙色** – 当前正在进行的任务。
- **浅蓝色** – 剩余任务的估计值。

颜色仅在甘特图的最低级别上显示。 选择 **全部展开** 可以查看主计划作业中的所有任务。 剩余任务的估计基于历史主计划作业。

## <a name="run-master-planning-and-track-processing-time"></a>运行主计划和跟踪处理时间

1. 在默认仪表板上，选择 **主计划**。
1. 在 **计划** 字段中，输入或选择一个值。
1. 选择 **运行**。
1. 将 **跟踪处理时间** 选项设置为 **是**。
1. 在 **线程数** 字段中，输入一个数字。
1. 在 **要包括的记录** 快速选项卡中，选择 **筛选**。
1. 在网格中，选择将 **现场** 字段设置为 **物料编号** 的行。
1. 在 **条件** 字段中，输入一个值。
1. 选择 **确定**。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]