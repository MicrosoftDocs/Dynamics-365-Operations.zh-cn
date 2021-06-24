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
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187239"
---
# <a name="view-plan-history-and-planning-logs"></a>查看计划历史记录和计划日志

[!include [banner](../../includes/banner.md)]

本主题说明如何在 Microsoft Dynamics 365 Supply Chain Management 中查看由计划优化功能触发的计划作业的历史记录。

要查看计划的历史记录，请依次转到 **主计划** \> **设置** \> **计划** \> **主计划** 并选择 **历史记录** 打开计划。 历史记录列出了所选计划的所有作业。 该列表包括已完成和活动的作业。

计划优化主计划运行的作业历史记录最多只能为每个主计划保留 60 条记录。 每当您运行新的主计划计算时，该计划的最早历史记录都会删除。

除了查看作业的开始时间和状态之外，您还可以查看特定作业的日志。 日志包含其他信息和警告。 并非所有作业都有日志。 要查看作业的日志，请选择 **日志**。 日志条目仅在作业完成之日起存储 30 天，之后它们将自动删除。

## <a name="related-resources"></a>相关资源

- [计划优化概览](planning-optimization-overview.md)
- [开始使用计划优化](get-started.md)
- [计划优化拟合分析](planning-optimization-fit-analysis.md)
- [将筛选器应用于计划](plan-filters.md)
- [取消计划作业](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]