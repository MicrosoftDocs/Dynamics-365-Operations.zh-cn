---
title: "用于精益生产的可视排产"
description: "本主题提供关于看板计划板的信息，生产规划人员可以使用看板计划板控制和优化看板作业的生产计划。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
keywords: "KanbanBoard，KanbanJobSchedulingListPage，LeanProductionFlowVisulaization"
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: johanhoffmann
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 1a3f43c2812cdf1c9f5c564bc86abe4fcc90b8a3
ms.contentlocale: zh-cn
ms.lasthandoff: 06/20/2017

---

# <a name="visual-scheduling-for-lean-manufacturing"></a>用于精益生产的可视排产

[!include[banner](../includes/banner.md)]


本主题提供关于看板计划板的信息，生产规划人员可以使用看板计划板控制和优化看板作业的生产计划。

本主题提供关于看板计划板的信息，生产规划人员可以使用看板计划板控制和优化看板作业的生产计划。

看板计划板使生产规划人员可以控制和优化看板作业的生产计划。 它使看板作业流透明，且为生产规划人员提供优化和调整 lean manufacturing 工作单元生产计划的工具。

## <a name="visual-scheduling-of-kanban-jobs"></a>看板作业的可视排产
看板作业可以包括一个或多个看板作业。 有以下两种类型的看板作业：

-   进程
-   转移

您仅可以计划**流程**类型的作业。 看板作业及其属性（例如活动时间）在生产看板流中进行定义。 在生产看板流，看板作业还被分配到工作单元。 工作单元的每日产能基于在资源组上设置的工作单元产能进行计算。 在相关日历中按每日工作时间进行调整。 计划看板作业后，该作业加载工作单元的产能。 看板计划板提供以下主要功能：

-   精益工作单元中的生产计划的图形概览。 此概览显示在定义的期间的已计划的看板流程作业。
-   让您计划未计划的看板作业和重新计划之前已计划的作业的工具。

## <a name="kanban-schedule-board"></a>看板计划板
如下图中所示，**看板计划板**页包含七个主要元素。 

![看板计划板](./media/kanban-schedule-board-1024x554.png)
1.  操作窗格
2.  筛选器字段
3.  用于未计划的作业的按钮
4.  时间段节点
5.  看板作业
6.  产能条
7.  时间刻度

### <a name="view-the-time-scale"></a>查看时间刻度

该板划分为多个时间段，每个时间段表示为一个节点 (4)。 时间段节点列在垂直轴上，水平访问表示显示时间段长度的时间刻度 (7)。 时间段的长度为一天或一周。 时间段长度由为看板计划板 (2) 选择的工作单元的配置确定。 对于每个时间段节点，看板计划板指示有多少已计划的看板计划加载此时间段。 此外还存在该时间段最大生产量的指示。 如果已计划的生产量超出最大生产量，则该时间段被视为超负荷，并且显示红色警告符号。 已计划的看板作业显示在已计划了开始和结束时间 (5) 的时间段中。 作业的长度与活动时间相等。 如果看板作业的活动时间超出工作单元的单位产品生产时间，则该看板作业在时间段中显示为重叠。

### <a name="view-job-status"></a>查看作业状态

将指针悬停在作业上时显示的工具提示中提供有关看板作业的详细信息。 符号提供有关作业的状态的信息。 例如，时钟符号表示看板作业逾期。

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>使用颜色查看看板计划板

要增强看板计划板提供的概览，可以使用颜色来区分看板作业。 看板作业的颜色在精益计划组中进行配置，您可以在精益计划组中聚合应在相同序列中生产的产品。 操作窗格**看板**选项卡上的**使用主题颜色**按钮让您能够在应用程序主题颜色与在精益计划组中配置的颜色之间切换。 对于每个时间段，产能条 (6) 表示该时间段有多少个可用小时数已加载看板作业。 如果时间段超负荷，产能条变厚且显示红色。 所有这些功能都在**看板计划板**页顶部的操作窗格 (1) 的**看板**选项卡上提供。

## <a name="plan-unplanned-jobs"></a>计划未计划的作业
您可以从**计划未计划的作业**对话框计划未计划的看板作业。 要打开此对话框，单击**未计划的作业**按钮，此时将显示当前未计划作业的数量。 或者单击操作窗格**看板**选项卡上的**计划未计划的作业**。 对话框显示工作单元的未计划的看板作业的列表。 您可以使用**筛选器**字段筛选网格中的所有字段。 例如，您可以筛选特定产品的看板作业。 筛选您要计划的作业的列表后，在列表中进行选择，然后单击**确定**。 要使用自动规划来计划作业，将**自动规划**选项设置为**是**。 在这种情况下，将根据作业的到期日期将作业计划到一个时间段。 您可以按时间段计划作业。 只需在**时间段**字段中选择一个时间段。 下图显示**计划未计划的作业**对话框的示例。 

![计划未计划的作业对话框](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>在相同时间段中为看板作业排序
您可以更改一个时间段内的一个或多个所选作业的序列。 如果您要确定一些作业在时间段内的优先级，此功能很有用。 或者，您可能要对具有相同产品属性的作业排序，以优化作业执行。 您可以通过拖放操作，或者使用操作窗格**看板**选项卡上的**后退**和**前进**菜单项更改序列。

## <a name="reassign-kanban-jobs-across-periods"></a>跨时间段重新分配看板作业
作业可以从一个时间段重新分配到另一个时间段。 如果一个时间段超负荷，且您要将负荷平衡到具有备用产能的时间段，此功能很有用。 您可以通过拖放操作，或者使用操作窗格**看板**选项卡上的**下一个时间段**和**上一个时间段**菜单项重新分配作业。

## <a name="open-the-kanban-schedule-board"></a>打开看板计划板
您可以使用以下页面上的菜单项打开看板计划板：

-   **生产区域**页
-   **看板作业计划**页
-   **生产流可视化**页


<a name="see-also"></a>请参阅
--------

[Lean manufacturing – 看板作业计划](lean-manufacturing-kanban-job-scheduling.md)


