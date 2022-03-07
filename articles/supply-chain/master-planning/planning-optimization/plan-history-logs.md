---
title: 查看计划历史记录和计划日志
description: 本主题说明如何查看由计划优化功能触发的计划作业的历史记录。
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 757d2103bd629c0107a3f29599196a56ea56d431a66cf1e69c7b3cf3d817c087
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6724812"
---
# <a name="view-plan-history-and-planning-logs"></a>查看计划历史记录和计划日志

[!include [banner](../../includes/banner.md)]

本主题说明如何在 Microsoft Dynamics 365 Supply Chain Management 中查看由计划优化功能触发的计划作业的历史记录。

要查看计划的历史记录，请依次转到 **主计划** \> **设置** \> **计划** \> **主计划** 并选择 **历史记录** 打开计划。 历史记录列出了所选计划的所有作业。 该列表包括已完成和活动的作业。

计划优化主计划运行的作业历史记录最多只能为每个主计划保留 60 条记录。 每当您运行新的主计划计算时，该计划的最早历史记录都会删除。

除了查看作业的开始时间和状态之外，您还可以查看特定作业的日志。 日志包含其他信息和警告。 并非所有作业都有日志。 要查看作业的日志，请选择 **日志**。 日志条目仅在作业完成之日起存储 30 天，之后它们将自动删除。

如果在设置主计划处理时启用了 **在后台运行** 快速选项卡上的 **批处理** 选项，批处理作业日志将显示有关主计划运行期间生成的任何警告和错误的详细信息。 例如，仅在批处理作业日志中捕获自动确认错误。 它们不会显示在 **历史记录** 页上的日志中。

要查看主计划运行期间发生的自动确认错误和其他警告或错误，请执行以下步骤。

1. 转到 **系统管理 \> 查询 \> 批处理作业**。
1. 查找并选择代表您感兴趣的主计划运行的记录。 （例如，**作业描述** 字段的值可能以 *主计划* 开头。）
1. 执行以下步骤之一，具体取决于您对 **批处理作业** 页使用的是 *增强窗体* 还是 *旧（未增强）窗体*：

    - 如果您使用的是增强窗体：在操作窗格上，选择 **批处理作业历史记录**。 然后，在 **批处理作业历史记录** 页上的操作窗格上，选择 **日志**。
    - 如果您使用的是旧窗体：在操作窗格上，在 **批处理作业** 选项卡上，选择 **日志**。

1. 选择 **消息详细信息** 打开 **消息详细信息** 窗格，您可以在其中查看处理过程中捕获的所有警告和错误。

## <a name="related-resources"></a>相关资源

- [计划优化概览](planning-optimization-overview.md)
- [开始使用计划优化](get-started.md)
- [计划优化拟合分析](planning-optimization-fit-analysis.md)
- [将筛选器应用于计划](plan-filters.md)
- [取消计划作业](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
