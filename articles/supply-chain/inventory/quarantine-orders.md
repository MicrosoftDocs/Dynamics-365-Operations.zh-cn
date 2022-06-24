---
title: 检验单
description: 本文介绍如何使用隔离订单锁定库存。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ee1ba338d90c6ee9cdc37948061f518040ae1a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869653"
---
# <a name="quarantine-orders"></a>检验单

[!include [banner](../includes/banner.md)]

本文介绍如何使用隔离订单锁定库存。

隔离订单可让您锁定库存。 例如，您可能要检验质量控制原因的物料。 将把已检验的库存转移到检验仓库。

> [!NOTE]
> 如果您使用高级仓库管理流程（在仓库管理中），隔离订单处理仅用于退货销售订单。

## <a name="quarantine-on-hand-inventory-items"></a>检验现有库存物料

隔离物料时，可以手动创建隔离订单，也可以将系统设置为在入站处理期间自动创建订单。

要将系统设置为自动生成隔离订单，请按照以下步骤操作。

1. 转到 **库存管理 \> 设置 \> 库存 \> 物料模型组**。
1. 在列表窗格中选择一个相关模型组，或创建一个新模型组。
1. 在 **库存策略** 快速选项卡上，选中 **隔离管理** 复选框。
1. 关闭该页面。
1. 在接收仓库的 **隔离仓库** 字段中，指定默认隔离仓库。

当在仓库登记为已接收的物料属于已选中 **隔离管理** 复选框的模型组时，系统将为其生成隔离订单。 隔离订单指示工作人员将物料移至隔离仓库。

当您在 **隔离订单** 页上手动创建隔离订单时，不必在关联的物料模型组中对物料进行隔离管理设置。 对于此流程，必须指定应检验的现有库存量和应使用的检验仓库。 您可以使用检验单状态来帮助计划流程。

## <a name="quarantine-order-statuses"></a>检验单状态

检验单可以有下列状态：

- 已创建
- 已开始
- 完工入库
- 已结束

### <a name="created"></a>创建时间

如果检验单已手动创建，但物料不在检验仓库中，则检验单具有 **已创建** 状态。 生成两个库存交易记录。 一个交易记录是可具有 **在单**、**实际预留** 或 **已领料** 状态的发货交易记录。 另一个交易记录是可在检验仓库中具有 **已订购** 或 **已登记** 状态的收货交易记录。 可使用一般流程预留、领取和登记库存更新。

### <a name="started"></a>已开始

当检验单已具有 **已开始** 状态时，库存将从常规仓库转移到检验仓库，并且会生成两个库存交易记录。 一个交易记录具有 **已扣除** 状态，另一个交易记录具有 **已接收** 状态。 同时，创建两个库存交易记录以处理退货转移。 这些交易记录未到期。 一个交易记录具有 **实际预留** 状态，另一个交易记录具有 **已订购** 状态。

### <a name="reported-as-finished"></a>完工入库

要将开始的隔离订单报告为完工入库，打开该订单，然后在操作窗格上选择 **完工入库**。 物料将从隔离区释放，但尚未移回常规仓库。 移回常规仓库可以通过可在完工入库流程中初始化的物料到达日记帐进行处理。

### <a name="ended"></a>已结束

当检验单结束后，物料将从检验仓库移回常规仓库。 物料交易记录的状态在检验仓库中设置为 *已售出*，在常规仓库中设置为 *已采购*。

## <a name="quarantine-order-scrap"></a>检验单报废

作为检验单流程的一部分，可以报废库存。 当处理报废时，库存状态将按隔离仓库中的发货交易设置为 *已售出*。

## <a name="additional-resources"></a>其他资源

- [库存锁定](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
