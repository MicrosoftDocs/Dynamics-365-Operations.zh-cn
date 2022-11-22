---
title: WMS 物料的 Inventory Visibility 支持
description: 本文介绍针对为仓库管理流程（WHS 物料）启用的物料的库存可见性支持。
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: bed402ecf20c19e81b2687efd90dba600460971a
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762731"
---
# <a name="inventory-visibility-support-for-wms-items"></a>WMS 物料的 Inventory Visibility 支持

[!include [banner](../includes/banner.md)]

本文介绍针对为仓库管理流程 (WMS) 启用的物料的库存可见性支持。 将此功能添加到库存可见性的功能被命名为 *高级 WMS*。

## <a name="wms-items"></a>WMS 物料

WMS 物料是为 WMS 启用并且在也启用了 WMS 的仓库中处理的物料。

有关 Microsoft Dynamics 365 Supply Chain Management 中的 WMS 和 **Warehouse Management** 模块的详细信息，请参阅 [Warehouse Management 概览](../warehousing/warehouse-management-overview.md)。

## <a name="scope-of-the-feature"></a>功能的范围

库存可见性的高级 WMS 功能侧重于基于现有查询的现有数量计算。 该功能通常并非旨在让您使用库存可见性来管理仓库处理活动。 库存可见性不会向其用户公开特定于仓库的概念。 以下是这些概念的一些示例：

- 预留层次结构
- 是否对物料或仓库启用了 WMS
- 单位序列组 ID
- 特定于仓库的流程，如装运、装载、波次和工作

库存可见性根据从 Supply Chain Management 发送的数据推断此信息。 特定于 WMS 的数据（即 `WHSInventReserve` 表中的数据）对用户不可见。

当您对库存可见性使用高级 WMS 功能时，所有查询结果将与直接在 Supply Chain Management 中进行的查询的结果相同。 但是，它们与使用 Warehouse Management 移动应用进行的查询的结果不同，因为此移动应用使用的计算逻辑略有不同。

## <a name="when-to-use-the-feature"></a>何时使用此功能

我们建议您在满足以下所有条件的情况下针对库存可见性使用 WMS 功能：

- 您正在将 Supply Chain Management 数据与库存可见性同步。
- 您正在 Supply Chain Management 中使用 WMS。
- 用户在低于仓库级别的级别（例如，在牌照级别，因为您在处理仓库工作）对 WMS 物料进行预留。

在其他情况下，无论是否启用库存可见性的高级 WMS 功能，现有查询结果都相同。 此外，如果您在这些情况下未启用该功能，则性能会更好，因为计算更少，开销也更少。

## <a name="enable-the-wms-feature-for-inventory-visibility"></a>启用库存可见性的 WMS 功能

要启用库存可见性的 WMS 功能，请执行以下步骤。

1. 以管理员身份登录到 Supply Chain Management 环境
1. 打开[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区，按此顺序启用以下功能：

    1. *库存可见性集成*
    1. *在库存可见性中启用仓库物料*

1. 转到 **库存管理 \> 设置 \> 库存可见性集成参数**。
1. 在 **启用 WMS 物料** 选项卡上，将 **启用 WMS 物料** 选项设置为 *是*。
1. 登录您的 Power Apps 环境，然后打开 **库存可见性**。
1. 打开 **配置** 页，然后在 **功能管理** 选项卡上，打开 *AdvancedWHS* 功能。
1. 在 Supply Chain Management 中，转到 **库存管理 \> 定期任务 \> 库存可见性集成**。
1. 在操作窗格上，选择 **禁用** 以暂时禁用库存可见性。
1. 在操作窗格上，选择 **启用** 以重新启用库存可见性。 加载项已重新加载，新功能现已启用。 您的 WMS 相关数据会开始同步到库存可见性。

## <a name="query-on-hand-quantities-of-wms-items"></a>查询 WMS 物料的现有数量

要查询 WMS 物料，可使用用于非 WMS 物料的相同[应用程序编程接口 (API) 和消息语法](inventory-visibility-api.md)。 您不必指定物料是 WMS 物料还是非 WMS 物料。 库存可见性功能根据存储的数据自动区分物料。

WMS 物料的查询结果与非 WMS 物料的结果基本相同。 唯一的区别是，来自 `fno` 数据源的以下物理度量是根据 Supply Chain Management 中的 WMS 逻辑计算的：

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

所有其他物理度量的计算方式与禁用库存可见性的 WMS 功能时完全一样。

有关 WMS 物料的现有计算的工作原理的详细信息，请参阅 [Warehouse Management 中的预留](https://www.microsoft.com/download/details.aspx?id=43284)白皮书。

## <a name="on-hand-list-view-and-data-entity-for-wms-items"></a>WMS 物料的现有量列表视图和数据实体

**预加载库存可见性摘要** 页面提供了 *现有库存索引查询预加载结果* 实体的视图。 与 *库存摘要* 实体不同，*现有库存索引查询预加载结果* 实体提供产品的现有库存量列表以及选定的维度。 库存可见性每 15 分钟同步一次预加载的摘要数据。

如果您对 WMS 物料使用库存可见性，想要查看 WMS 物料的现有量列表，建议您启用 *预加载库存可见性摘要* 功能（另请参阅[预加载简化的现有量查询](inventory-visibility-power-platform.md#preload-streamlined-onhand-query)）。 Dataverse 中的相应数据实体存储您的查询预加载结果，结果每 15 分钟更新一次。 数据实体的名称是 `Onhand Index Query Preload Result`。

> [!IMPORTANT]
> Dataverse 实体是只读的。 您可以在库存可见性实体中查看和导出数据，但 **不要进行修改**。

禁止更改存储在 Supply Chain Management 数据源 (`fno`) 中的 WMS 物料数量。 此行为与库存可见性的其他功能的行为一致。 强制执行此限制可以帮助防止冲突。

## <a name="wms-item-compatibility-for-other-functions-in-inventory-visibility"></a>WMS 物料与库存可见性中其他功能的兼容性

支持 WMS 物料的[软预留](inventory-visibility-reservations.md)和[库存分配](inventory-visibility-allocation.md)。 您可以在软预留和分配计算中包括与 WMS 相关的实际度量。

## <a name="calculate-available-to-promise-quantities"></a>计算可承诺数量

对于 WMS 物料，该解决方案完全支持[可承诺 (ATP)](inventory-visibility-available-to-promise.md)。 您可以定义 ATP 计算，而无需担心 WMS 特定的详细信息。
