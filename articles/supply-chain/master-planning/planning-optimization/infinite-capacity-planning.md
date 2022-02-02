---
title: 无限容量计划
description: 本主题提供有关计划优化的无限容量计划的信息。 它还介绍当前的功能限制。
author: ChristianRytt
ms.date: 09/21/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6ea27f4e38697d517b1520176eb5dfeee651a598
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982142"
---
# <a name="scheduling-with-infinite-capacity"></a>无限容量计划

[!include [banner](../../includes/banner.md)]

*计划优化的无限容量计划* 功能引入基于工艺路线信息的计划。 它允许您基于各种工艺路线设置计划作业。 计划优化的计划涵盖常用的工艺路线设置，包括工艺路线工序顺序或工艺路线工序资源的要求。

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>打开无限容量计划功能

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*主计划*
- **功能名称**：*计划优化的无限产能计划*

有关此功能的详细信息，请参阅[基于能力选择资源的计划](capability-based-scheduling.md)。

## <a name="added-functionality"></a>添加的功能

*计划优化的无限容量计划* 功能启用基于工艺路线信息的作业计划。 因此，工艺路线设置可用于计划生产流程。 虽然此功能具有一些内置主计划没有的限制，但它支持制造方案所需的最常见功能。

该功能同时考虑 *简单工艺路线* 和 *工艺路线网络*。 通过使用工艺路线工序上的 **下一个** 字段，您可以设置具有并行运行的多个起点和多个工序的复杂工艺路线。 系统将在计划期间考虑此类型的复杂工艺路线结构。

此外，该功能还在工艺路线中支持 *并行工序*。 通过使用工艺路线工序上 **优先级** 字段中的 *主要* 和 *辅助* 选项，您可以定义一个工艺路线结构，其中一个工艺路线工序是主要工序，另一个工序是辅助工序。 在这种情况下，系统将在计划期间考虑工艺路线结构。

在计划流程期间，系统还考虑为工序指定的 *资源要求*。 系统使用资源要求来确定执行工序所需的资源。 当前，*计划优化的无限容量计划* 功能支持以下类型的资源要求：

- 资源类型
- 资源
- 资源组
- 能力（有关详细信息，请参阅[基于能力选择资源的计划](capability-based-scheduling.md)。）

> [!NOTE]
>
> - 如果资源和/或资源组设置为无限产能，则主计划会将它们视为无限产能。
> - 尚不支持与 Human Resources 相关的要求（例如技能或证书要求）。

该功能还支持 **设置时间** 和 **运行时间** 操作属性。 当您在工艺路线工序上设置这些属性时，计划流程将创建适当的设置和处理作业。

总之，计划优化的计划支持最常用的方案。 您可以创建工艺路线，添加主要和辅助工序，定义下一个工序，添加资源要求，以及添加设置时间和运行时间。 然后，系统将在计划期间考虑此信息。

## <a name="limitations"></a>限制

当您使用计划优化的计划时，以下限制适用：

- 该功能仅支持无限容量。
- 该功能不支持资源负荷功能。
- 该功能不考虑工艺路线废料。
- 在选择主要资源时，该功能仅支持 *持续时间*。

请注意，*计划优化的无限容量计划* 功能在不断改进。 Microsoft 预计在未来版本中引入对其他计划设置的支持。
