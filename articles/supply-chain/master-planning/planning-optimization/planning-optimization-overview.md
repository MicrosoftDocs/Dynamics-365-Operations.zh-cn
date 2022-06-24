---
title: 计划优化概述
description: 本文提供计划优化功能的概述。
author: t-benebo
ms.date: 10/31/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 302c92c48765d1c2faddd65c6c6a18ddfd56c71e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890993"
---
# <a name="planning-optimization-overview"></a>计划优化概述

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management 的计划优化加载项使主计划计算可以在 Dynamics 365 Supply Chain Management 和相关的 SQL 数据库之外进行。 与计划优化功能相关的好处包括在主计划运行期间改进的性能以及对 SQL 数据库的影响最小。 即使在工作时间内也可以进行快速的计划运行，因此规划员可以立即对需求或参数更改做出反应。

若要使用计划优化，必须从 Microsoft Dynamics Lifecycle Services (LCS) 中的项目安装计划优化加载项，并在 Supply Chain Management 中启用计划优化功能。 有关详细信息，请参阅[开始使用计划优化](get-started.md)。

下图显示了在工作时间内运行计划优化的好处。

![在工作时间内运行计划优化的好处。](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>性能提升

计划优化可用于涉及长期运行的主计划的场景。 它是专门为涉及大量数据的快速计算而设计的。 由于它是作为超级可扩展的多租户服务构建的，因此多个实例可以同时协同工作来计算计划。 此外，计划服务还可以从系统中删除主计划的负荷，并使用可最大程度减少服务器负荷的数据流。

计划优化可以帮助您实现以下目标：

- 通过缩短运行时间来提高计划性能。
- 减少主计划运行期间对其他流程的影响。
- 进行更频繁的计划运行。 （不限于日常运行。）
- 放心未来的业务增长不会使计划系统超负荷。

## <a name="architecture-and-data-flow"></a>体系结构和数据流

从 LCS 安装计划优化加载项后，将建立到计划优化服务的安全连接。 服务与相关的 Supply Chain Management 实例位于相同的数据中心国家或地区。 设置计划优化后，运行主计划时，主数据和交易记录数据将从 Supply Chain Management 发送到计划优化服务。

如果卸载了计划优化加载项，则会删除计划优化服务中的所有相关数据。

### <a name="high-level-data-flow-for-regeneration-runs"></a>用于重新生成运行的高级数据流

1. Supply Chain Management 客户端发送信号从“计划优化”请求计划运行。
2. “计划优化”通过集成的连接器请求所需的数据。
3. SQL 数据库通过连接器将请求的有关设置、主数据和交易记录数据的信息发送到“计划优化”。 连接器在 Supply Chain Management 和计划优化服务之间转换信息。
4. 计划优化服务将与计划相关的数据保存在内存中，并进行所需的计算。
5. 计划结果通过连接器发送到 Supply Chain Management 数据库。 结果包括计划订单和限定标准信息等信息。 “计划优化”向 Supply Chain Management 发送信号，指示计划运行已完成。 它还发送任何相关的消息和警告。

下图显示数据流。

![用于重新生成运行的数据流。](media/PlanningOptimization2.png)

## <a name="related-resources"></a>相关资源

[开始使用计划优化](get-started.md)

[计划优化拟合分析](planning-optimization-fit-analysis.md)

[查看计划历史记录和计划日志](plan-history-logs.md)

[将筛选器应用于计划](plan-filters.md)

[取消计划作业](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]