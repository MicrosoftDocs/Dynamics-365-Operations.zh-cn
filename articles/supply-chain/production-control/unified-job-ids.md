---
title: 统一作业 ID 编号规则
description: 此功能提供一个统一的编号规则，可为生产控制、制造执行和考勤管理模块生成作业 ID。
author: johanhoffmann
ms.date: 03/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 00212803c46d898a39eafbc5c62016eb829535e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824933"
---
# <a name="unified-number-sequence-for-job-ids"></a>统一作业 ID 编号规则

[!include [banner](../includes/banner.md)]

此功能提供一个统一的编号规则，可为生产控制、制造执行和考勤管理模块生成作业 ID。 之前，您能够为每个模块选择不同的编号规则，如果其中两个或多个规则使用相同的格式，可能会导致作业 ID 冲突。 此类冲突可能导致数据损坏。

## <a name="turn-on-this-feature-for-your-system"></a>为您的系统启用此功能

如果您的系统尚未包含本主题中所述的功能，请转到 [功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，打开 *统一作业 ID 编号规则* 功能。

## <a name="set-up-the-unified-number-sequence-for-job-ids"></a>设置统一作业 ID 编号规则

启用此功能后，将弃用生产控制、制造执行和考勤管理模块的参数页面上的现有 **作业标识** 编号规则设置，并将添加新的 **统一作业 ID** 字段。 **统一作业 ID** 值由全部三个模块共享，从而确保所有模块引用相同的编号规则。 因此，作业 ID 在全部三个模块中都是唯一的，并且永远不会发生冲突。

若要设置统一作业 ID 编号规则：

1. 如上一部分所述打开功能。
1. 确定要用于统一作业 ID 的编号规则，或创建新的编号规则。 有关详细信息，请参阅[编号规则概述](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)。
1. 转到 **生产控制参数**、**制造执行参数** 或 **考勤管理参数** 页面。 选择哪个页面都没有关系，因为在其中任何页面上进行此设置时，所有其他页面都将自动更新。
1. 在选定的参数页面上打开 **编号规则** 选项卡。
1. 将之前标识的 **编号规则代码** 分配到网格的 **统一作业 ID**。
