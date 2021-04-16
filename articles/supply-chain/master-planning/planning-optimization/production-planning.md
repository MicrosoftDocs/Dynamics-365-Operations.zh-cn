---
title: 生产计划
description: 本主题介绍生产计划，并说明如何使用计划优化来修改计划的生产订单。
author: ChristianRytt
ms.date: 12/15/2020
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
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 22b78f44940f71097ca8b1cdb74edb06274bba75
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839215"
---
# <a name="production-planning"></a>生产计划

计划优化支持多个生产场景。 如果要从现有的内置主计划引擎迁移，请注意某些变更的行为，这一点很重要。

以下视频简要介绍了本主题中讨论的一些概念：[Dynamics 365 Supply Chain Management：计划优化增强](https://youtu.be/u1pcmZuZBTw)。

## <a name="turn-on-this-feature-for-your-system"></a>为您的系统启用此功能

如果您的系统尚未包含本主题中所述的功能，请转到 [功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)，打开 *计划优化的计划生产订单* 功能。

## <a name="planned-production-orders"></a>计划生产订单

当主计划创建计划订单以满足要求时，订单类型由 **计划订单类型** 字段的值确定。 如果 **计划订单类型** 字段设置为 *生产*，将创建计划生产订单。 这些计划生产订单包括有关有效物料清单 (BOM) 和来自相关生产设置的工艺路线 ID 的信息。

## <a name="requirements-from-boms"></a>BOM 的要求

主计划过程中会采用 BOM 信息。 计划输出包括材料供应，以满足生产的相关材料需求。

在主计划期间，当前有效的 BOM 用于确定生产所需的材料。 此步骤在与所需生产订单相关的 BOM 结构的所有级别完成。 材料要求通过使用可用的现有库存量、现有的按订购供应和经过审核的计划订单来满足。 如果有任何地方需要其他材料，将创建计划订单来满足需求。

## <a name="scheduling-during-firming"></a>确认期间的计划

计划生产订单包括生产计划所需的工艺路线 ID。 但是，计划运行期间对计划订单的计划支持还未确定。 工艺路线 ID 用于在确认期间对计划生产订单进行计划。 因此，计划生产订单的提前期可能不同于从其生成的相关的已确认计划生产订单的提前期，如下所述：

- **计划生产订单** – 提前期基于已发布产品的静态提前期。
- **已确认生产订单** – 提前期基于使用工艺路线信息和相关资源约束的计划。

有关预期功能可用性的详细信息，请参阅[计划优化适应分析](planning-optimization-fit-analysis.md)。

如果您依赖于计划优化还不可用的生产功能，您可以继续使用内置的主计划引擎。 不需要处理异常。

## <a name="delays"></a>延迟

如果所需材料的提前期长于今天的日期和材料要求日期之间的期间，所需材料的计划订单和相关生产订单将延迟。 对于计划订单，延迟（以天为单位）根据已发布产品的提前期计算。 延迟信息然后传播到 BOM 结构的所有级别。 因此，您可以一直关注延迟原材料对客户销售订单的影响。

## <a name="modifying-planned-orders"></a>修改计划订单

当您更改计划订单的信息时，您会收到以下消息：“请注意，在运行下一个主计划之前，对计划订单的手动更改的影响不会反映在计划的剩余部分中。”

如果要更改计划订单上的信息并查看对相关材料要求的影响，请按照以下步骤操作。

1. 更新计划订单。
2. 审核计划订单。
3. 运行主计划。

运行主计划时，如果包含计划生产订单，则不应使用筛选器。 有关详细信息，请参阅本主题后面的[筛选器](#filters)一节。

> [!NOTE]
> 如果计划订单的交货日期更改为以后的日期，可能会根据新计划订单对需求加以限定。 当新供应日期导致限定需求出现延迟，但是根据提前期设置，可以避免这一延迟，这时会发生此行为。

## <a name="explosion-page"></a>分解页

您可以使用 **分解** 页分析特定生产订单或计划生产订单所需的需求、相关的覆盖范围以及限定标准信息。 **分解** 页上的信息在主计划期间更新。 您不能直接从 **分解** 页更新信息。

## <a name="filters"></a><a name="filters"></a>筛选器

对于包含生产的计划场景，我们建议您不要筛选主计划运行。 为确保计划优化具有计算正确结果所需的信息，您必须在计划订单的整个 BOM 结构中包括与产品有任何关系的所有产品。

虽然使用内置的主计划引擎时会自动检测到依赖子项并将其包括在主计划运行中，但是计划优化不会执行此操作。

例如，如果产品 A 的 BOM 结构中的单个螺栓还用于生产产品 B，产品 A 和 B 的 BOM 结构中的所有产品都必须包含在筛选器中。 因为要确保所有产品都是筛选器的一部分可能非常复杂，所以我们建议在涉及生产订单时避免发生筛选后的主计划运行。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]