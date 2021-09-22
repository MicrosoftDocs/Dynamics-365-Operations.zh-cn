---
title: 计划优化发布流程和发布历史记录
description: 本主题提供有关计划优化的发布流程和发布历史记录的信息。
author: crytt
ms.date: 09/02/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d0f7a9f59d1034451c5c2dec1150c017bda27ad4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474692"
---
# <a name="planning-optimization-release-process-and-release-history"></a>计划优化发布流程和发布历史记录

[!include [banner](../../includes/banner.md)]

Microsoft 每月都会更新计划优化。 但是，根据业务要求，我们偶尔会在计划发布之间发布其他更新。

每个发布都将发布到计划优化可用的各个区域。 该流程通常需要三天时间。

在更新计划优化时，主计划运行速度可能比平时慢一些。

使用计划优化的环境会自动接收最新发布。 无需用户操作：系统将自动更新此服务。 但是，从未将中断性变更功能自动推送到环境中。 默认情况下，任何被视为中断性变更的更改都将被禁用，并且必须使用[功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)来显式启用。 因此，在您选择启用这些更改之前，这些更改不会显示在环境中。

由于在您的环境中更新计划优化时未显示通知，因此您可以查看以下表中的发布说明，以确定何时发布更改及其引入的功能。 此表显示为计划优化发布的更改、这些更改是否与功能管理中的功能相关联，以及发布日期。

| 更改 | 功能管理详细信息 | 发布日期 |
|---|---|---|
| 一般性能、质量和稳定性改进。 | 无需功能管理。 | 2021 年 8 月 25 日到 30 日 |
| <p>已将 **提前期** 字段添加到了计划订单。</p><p>一般性能、质量和稳定性改进。</p> | 无需功能管理。 | 2021 年 8 月 12 日到 17 日 |
| <p>添加了无限产能计划的资源类型要求。</p><p>提高了无限产能计划的资源效率和日历效率。</p><p>有关详细信息，请参阅[具有无限容量的计划](infinite-capacity-planning.md)。 | <p>自 10.0.20 版起在功能管理中发布。</p><p>功能名称：*计划优化的无限容量计划*</p> | 2021 年 7 月 6 日到 12 日 |
| 常规质量改进。 | 无需功能管理。 | 2021 年 7 月 6 日到 12 日 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
