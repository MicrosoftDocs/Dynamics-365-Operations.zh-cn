---
title: "Lean manufacturing 概述"
description: "本文提供 Dynamics 365 for Finance and Operations 中的 lean manufacturing 功能的概览和描述。"
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19371
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2964083ec6cb8792e3c67722c68b038939933cbc
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="lean-manufacturing-overview"></a>精益生产概览

[!include[banner](../includes/banner.md)]


本文提供 Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 中的 lean manufacturing 功能的概览和描述。

精益制造提供您可以使用建模精益工序的工具。 这些工具支持和促进以下概念和业务活动：
-   通过建模制造和物流流程创建基础精益制造为生产流程。
-   通过使用看板符号的需求需求实施下拉精益系统。
-   监控和维护看板作业。

Finance and Operations 中的 lean manufacturing 体系结构由生产流程、活动和种规则组成。 这些结构完全由 Finance and Operations 流程集成。 在混合模式的制造环境可以使用精益制造合并各种供应来源、生产和采购策略。 这些策略包括生产订单、批次订单、流程工业、采购订单和转移单。
| **重要**                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 您可以通过看板使用 Finance and Operations 支持 lean manufacturing 的执行。 但是，原则的精益一个成功的部署取决于您使用实际生产条件和环境的内部业务流程。 |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a>建模为生产流程的制造和物流流程
如要创建建模制造、模型制造和物流流程为生产流程。 此活动包括以下任务：
1.  标识要实现补货精益战略的流程，然后建模这些进程作为生产流程。 然后可以分析和优化流程。 精益实现的目标之一是通过减少浪费提高材料和信息流。
2.  定义生产流描述物料流程活动的规则。 转移活动定义从一个位置到另一个产品或产品的变动。 处理活动定义应用于产品的增值工序。
3.  创建定义单位产品生产时间的要求生产流程的版本。 这些要求用于计算在生产流程时间周期的每个活动。 您可以创建生产流程的多个版本，然后使用这些版本提高流程。

## <a name="using-kanbans-to-signal-demand-requirements"></a>使用看板标记需求的要求
货物在需要的情况下，系统下拉生产物料。 此操作将减少交货提前期和额外库存。 您可以使用看板计划、跟踪和处理基于生产流程的需求。 若要创建看板结构，创建看板时，创建看板规则定义，并且要求如何执行。 您可以创建规则的两种类型。 制造规则创建处理看板作业，并且，提领看板的规则创建转移看板作业。 可以设置以下补货策略：
-   **“固定数量”**看板规则与处理单位的固定编号相关，这意味着，活动看板的数量是固定的。 只要使用了看板中的所有产品并手动清空了处理单元，将创建同一类型的新看板。 在创建固定数量看板规则时，您可以计算最佳看板数量和使用的产品数量。 该计算考虑到预测、未结订单的实际需求、补货物料的提前期以及历史需求。
-   **“计划”**的看板规则由主计划计算的补货需求。 主计划生成可以确定到看板的计划看板。
-   **“事件”**看板规则源自销售订单行、生产物料清单行的行或最小库存量设置的补货要求。 在生成事件看板时，这些限定为源需求。

在创建看板时，基于定义在看板规则中的看板流活动中将生成一个或多个看板作业。

## <a name="monitoring-and-maintaining-kanban-jobs"></a> 监控和维护看板作业。
Lean manufacturing 提供由看板规则管理的可见性到制造和物流活动的当前状态。 因此，您可以计划和优先以下任务：

-   获取当前看板作业计划的概览。
-   计划并重新计划看板作业。
-   跟踪和登记看板作业的状态。

下表描述专门的看板面板：
-   看板作业计划 – 提供看板作业的概览。 该板显示一个或多个工作单元的看板作业及其状态。 此作业根据定义在生产流程模型的计划周期（天数或周数）列出。 该板还显示每个计划期间产能消耗量，因此，您可以监控计划的负荷。 您可以更改看板作业的状态，重新计划看板作业到不同的计划期间和执行其他任务。
-   看板面板转移作业–此板提供转移作业当前的概览。 可以更新和登记领料单，开始并完成转移作业，以及执行其他任务。
-   用于处理作业的看板面板 – 此板专用于支持常规生产流程并提供一个或多个工作单元中的当前情况的概览。 从该板中，可以对看板设置优先级、领料和制造。 此板还装用于支持看板报告的条码扫描。

## <a name="kanban-jobs-and-integration-with-finance-and-operations-processes"></a>看板作业和集成 Finance and Operations 流程
看板作业在 Finance and Operations 中完全集成库存交易记录的当前流程。
-   您可以执行领料活动用于完成看板作业的要求的补货物料。
-   您可以打印看板卡、循环看板卡和领料单以支持看板的使用。 这些文件在仓库中和在生产车间上用于表示、跟踪和登记看板作业。
-   您可以通过在库存中扫描条码登记领料和转移活动。

此外，lean manufacturing 支持转包的活动引用的服务的采购和开票的过程。
-   您可以将采购协议行和服务分配到已转包活动。
-   您可以创建期间采购订单和收货通知支持采购和发票的服务。






