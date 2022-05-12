---
title: WHS 物料的 Inventory Visibility 支持
description: 本主题介绍针对为高级仓库流程（WHS 物料）启用的物料的库存可见性支持。
author: yufeihuang
ms.date: 03/10/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-03-10
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: cfbff05697f4159cb74d110887b8029f28fbf96b
ms.sourcegitcommit: 1050e58e621d9a0454895ed07c286936f8c03320
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/21/2022
ms.locfileid: "8625376"
---
# <a name="inventory-visibility-support-for-whs-items"></a>WHS 物料的 Inventory Visibility 支持

[!include [banner](../includes/banner.md)]

本主题介绍针对为高级仓库流程（WHS 物料）启用的物料的库存可见性支持。 将此功能添加到库存可见性的功能被命名为 *高级 WHS*。

## <a name="whs-items"></a>WHS 物料

WHS 物料是为高级仓库流程 (WHS) 启用并且在也启用了 WHS 的仓库中处理的物料。

有关 Microsoft Dynamics 365 Supply Chain Management 中的 WHS 和 **Warehouse Management** 模块的详细信息，请参阅 [Warehouse Management 概览](../warehousing/warehouse-management-overview.md)。

## <a name="scope-of-the-feature"></a>功能的范围

库存可见性的高级 WHS 功能侧重于基于现有查询的现有数量计算。 该功能通常并非旨在让您使用库存可见性来管理仓库处理活动。 库存可见性不会向其用户公开特定于仓库的概念。 以下是这些概念的一些示例：

- 预留层次结构
- 是否对物料或仓库启用了 WHS
- 单位序列组 ID
- 特定于仓库的流程，如装运、装载、波次和工作

库存可见性根据从 Supply Chain Management 发送的数据推断此信息。 特定于 WHS 的数据（即 `WHSInventReserve` 表中的数据）对用户不可见。

当您对库存可见性使用高级 WHS 功能时，所有查询结果将与直接在 Supply Chain Management 中进行的查询的结果相同。 但是，它们与使用 Warehouse Management 移动应用进行的查询的结果不同，因为此移动应用使用的计算逻辑略有不同。

## <a name="when-to-use-the-feature"></a>何时使用此功能

我们建议您在满足以下所有条件的情况下针对库存可见性使用高级 WHS 功能：

- 您正在将 Supply Chain Management 数据与库存可见性同步。
- 您正在 Supply Chain Management 中使用 WHS。
- 用户在仓库级别之外的级别对 WHS 物料进行预留（例如，因为您正在进行仓库工作）。

在其他情况下，无论是否启用库存可见性的高级 WHS 功能，现有查询结果都相同。 此外，如果您在这些情况下未启用该功能，则性能会更好，因为计算更少，开销也更少。

## <a name="enable-the-advanced-whs-feature-for-inventory-visibility"></a>启用库存可见性的高级 WHS 功能

要启用库存可见性的高级 WHS 功能，请执行以下步骤。

1. 以管理员身份登录到 Supply Chain Management 环境
1. 打开[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)工作区，按此顺序启用以下功能：

    1. *库存可见性集成*
    1. *在库存可见性中启用仓库物料*

1. 转到 **库存管理 \> 设置 \> 库存可见性集成参数**。
1. 在 **启用 WHS 物料** 选项卡上，将 **启用 WHS 物料** 选项设置为 *是*。
1. 登录到 Power Apps。
1. 打开 **配置** 页，然后在 **功能管理** 选项卡上，打开 *AdvancedWHS* 功能。
1. 在 Supply Chain Management 中，转到 **库存管理 \> 定期任务 \> 库存可见性集成**。
1. 在操作窗格上，选择 **禁用** 以暂时禁用库存可见性。
1. 在操作窗格上，选择 **启用** 以重新启用库存可见性。 加载项已重新加载，新功能现已启用。 您的 WHS 相关数据会开始同步到库存可见性。

## <a name="query-on-hand-quantities-of-whs-items"></a>查询 WHS 物料的现有数量

要查询 WHS 物料，可使用用于非 WHS 物料的相同[应用程序编程接口 (API) 和消息语法](inventory-visibility-api.md)。 您不必指定物料是 WHS 物料还是非 WHS 物料。 库存可见性功能根据存储的数据自动区分物料。

WHS 物料的查询结果与非 WHS 物料的结果基本相同。 唯一的区别是，来自 `fno` 数据源的以下物理度量是根据 Supply Chain Management 中的 WHS 逻辑计算的：

- `AvailOrdered`
- `AvailPhysical`
- `ReservOrdered`
- `ReservPhysical`

所有其他物理度量的计算方式与禁用库存可见性的高级 WHS 功能时完全一样。

有关 WHS 物料的现有计算的工作原理的详细信息，请参阅 [Warehouse Management 中的预留](https://www.microsoft.com/download/details.aspx?id=43284)白皮书。

导出到 Dataverse 的数据实体还不能更新 WHS 物料的数量。 数据实体中显示的数量对于非 WHS 物料和不受 WHS 逻辑影响的数量（即，除了 `fno` 数据源中的 `AvailPhysical`, `AvailOrdered`, `ReservPhysical` 和 `ReservOrdered` 以外的其他度量）均正确。

禁止更改存储在 Supply Chain Management 数据源中的 WHS 物料数量。 对于库存可见性的其他功能，强制执行了此限制以帮助防止冲突。

## <a name="soft-reservations-on-whs-items-in-inventory-visibility"></a>库存可见性中 WHS 物料的软预留

一般情况下，支持对 WHS 物料进行[软预留](inventory-visibility-reservations.md)。 您可以在软预留计算中包括与 WHS 相关的物理度量。 

在一个已知限制中，WHS 物料目前不支持 *可供预留* 计算。 因此，如果在发生软预留的当前维度之上存在预留，则 *可供预留* 计算不正确。 在 [软预留 API](inventory-visibility-api.md#create-one-reservation-event) 中禁用 **ifCheckAvailForReserv** 选项时，将不会影响软预留。

此约束也适用于基于软预留（例如分配）的功能和自定义。

## <a name="calculate-available-to-promise-quantities"></a>计算可承诺数量

对于 WHS 物料，该解决方案完全支持[可承诺 (ATP)](inventory-visibility-available-to-promise.md)。 您可以定义 ATP 计算，而无需担心 WHS 特定的详细信息。
