---
title: "Lean manufacturing 的 看板作业计划"
description: "文本提供有关看板作业计划和各种看板作业计划方法的可视化控制的信息。"
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 27db57170ccc23c2ea18a49c1a3e5950c870fa13
ms.contentlocale: zh-cn
ms.lasthandoff: 05/25/2017

---

# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Lean manufacturing 的 看板作业计划

[!include[banner](../includes/banner.md)]


文本提供有关看板作业计划和各种看板作业计划方法的可视化控制的信息。  

**“看板作业计划”**页提供了对 lean manufacturing 工作单元的计划的可视化控制。 它概述了所有看板作业并提供了多种筛选功能。 您可以从该页移至所有其他与看板配置和执行相关的页面。

## <a name="automatic-scheduling-of-kanban-jobs"></a>自动计划看板作业
如果您在看板规则上设置**自动计划数量**参数，则会自动触发计划。 如果您将**自动计划数量**设置为 <**1**，则会在创建每个看板作业后立即计划该作业。 该结果为一系列先拉先运行操作。 如果您将**“自动计划数量”**设置为一个大于 1 的值，则会先对看板作业进行分组，然后再计划这些看板作业。 

此概念支持减小看板大小，直至其小于实际经济批次大小。 例如，某个特定物料（或物料系列）的经济批次大小为 30。 您可以配置看板规则，使其产品数量为 10 且**自动计划数量**值为 **3**，而不是创建使用产品数量 30 的看板。 虽然自动计划仅在存在 3 个未计划的作业时为工作单元计划看板作业，但规划员或车间经理可以很清楚地知道，两个未计划的作业可能正在等待执行。 随后，规划员或车间经理可通过手动计划这两个作业或创建附加看板来将二者投入生产中。

## <a name="manual-scheduling"></a>手动计划
对于手动计划，Microsoft Dynamics AX 2012 引入了看板计划板。 手动计划可与自动计划结合使用。 利用看板计划板，您可以计划和取消计划作业、按顺序移动作业或在各个期间之间移动作业。 可手动取消计划基于看板规则（其中，**“自动计划”**值大于 **0**）的作业。 但是，在下一个自动计划事件发生时（即，在创建新的看板时），将重新计划这些作业。 以下选项可用于手动计划：

-   **计划** 根据所选作业的到期日期计划这些作业。 （此选项与自动计划类似。）
-   **从某一日期正推时间表** 尝试根据所选作业的到期日期计划这些作业，但会使用指定的最早开始日期来约束结果。
-   **延后** 在期间内序列中将所选计划作业移后。
-   **向前** 在期间内序列中将所选计划作业移前。
-   **上一期间** 将所选计划作业移到上一期间的开始日期或结束日期。
-   **下一期间** 将所选计划作业移到下一期间的开始日期或结束日期。
-   **计划** &gt; **恢复作业状态**可让您取消计划已计划的作业。

## <a name="lean-scheduling-groups"></a>精益计划组
每种颜色均代表一个精益计划组。 可随意将精益计划组定义为通用组或属于单个工作单元的组。 可随意将物料和维度分配给计划组。 例如，在“上漆”单元中，一个计划组可代表一种产品颜色。 在由特定的工具要求驱动的工作中，可按工具要求对物料分组，并且包装工作单元可按包装模板对物料进行分组。 虽然对精益计划组使用颜色是一项可选操作，但建议执行此操作。 它将提高计划状态的可见性。 例如，可以很轻松地看到哪些颜色在哪一天生成，并且您可以快速说明此工作的优化方式。

## <a name="work-cell-capacity-and-period-capacity"></a>工作单元产能和期间产能
精益工作单元的产能始终是并发产能。 换句话说，多个作业可在一个工作单元中同时处于活动状态。 可在两种模式中跟踪产能：吞吐量和工时数。

### <a name="throughput"></a>吞吐量

工作单元的产能由引用期间（标准工作日、周或月）的平均吞吐量定义。 随后，根据分配给工作单元的日历的工作时间来按天或周计算实际产能。 按作业加载的产能为作业的数量，并已按照工作单元中物料的吞吐率进行调整。

### <a name="hours"></a>工时数

按天或周的可用产能由分配给工作单元的日历定义。 按作业加载的产能为活动的周期时间，并已按照工作单元中物料的数量（默认活动数量和实际作业数量）和吞吐率进行调整。

#### <a name="period-capacity-factbox"></a>期间产能速见表

**“看板作业计划”**列表页包含一个速见表，此表显示所选工作单元的可用和预订的期间产能。 根据生产流模型中的所选计划期间，期间将显示天数或周数。

<a name="see-also"></a>请参阅
--------




