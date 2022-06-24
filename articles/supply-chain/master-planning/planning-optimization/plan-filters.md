---
title: 为计划应用筛选器
description: 本文说明使用计划优化功能时如何对计划使用筛选器。
author: t-benebo
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: c2df379be0876225bc7b0301d21f4e6660b04eb6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875295"
---
# <a name="apply-filters-to-a-plan"></a>将筛选器应用于计划

[!include [banner](../../includes/banner.md)]

使用计划优化功能时，可以将筛选器应用于计划。 **计划筛选器** 将始终在主计划运行期间应用。 当您要将计划限制为特定的项目组并确保没有其他项目作为生成的主计划的一部分包含时，**计划筛选器** 很有用。

如果应用了 **计划筛选器**，并且在主计划运行期间也应用了运行时筛选器，则计划运行中仅包括两个筛选器的交集。

使用计划优化时，可以从 **主计划** 访问 **计划筛选器**。

## <a name="example-scenario"></a>示例场景

设置了一个包含项目 A、B 和 C 的计划筛选器。然后为同一计划运行主计划运行，但是应用了不同的运行时筛选器：

- **包含项目 D 的运行时筛选器：** 未计划项目，因为计划筛选器和运行时筛选器之间没有交集。
- **包含项目 A 和 D 的运行时筛选器：** 在计划运行中仅包含项目 A，因为项目 D 不是计划筛选器的一部分。
- **包含物料 B 的运行时筛选器：** 在计划运行中仅包含物料 B，保留物料 A 的先前计划输出。
- **包含所有物料的运行时筛选器（空筛选器）：** 计划运行中包含物料 A、B 和 C，物料 A 和 B 的先前计划输出将被覆盖。

> [!NOTE]
> 如果您在 **主计划参数** 页面上选择为 **当前动态主计划** 的计划上设置计划筛选器，动态主计划功能将仅限于筛选出的物料。 例如，如果针对不是计划筛选器一部分的物料更新了净需求，则不会生成结果。

## <a name="related-resources"></a>相关资源

[计划优化概述](planning-optimization-overview.md)

[开始使用计划优化](get-started.md)

[计划优化拟合分析](planning-optimization-fit-analysis.md)

[查看计划历史记录和计划日志](plan-history-logs.md)

[取消计划作业](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
