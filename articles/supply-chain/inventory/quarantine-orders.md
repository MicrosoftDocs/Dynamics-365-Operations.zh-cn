---
title: "检验单"
description: "本主题介绍检验单如何用于锁定库存。"
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9a05c35d2e4a9e3ad81421eac863d182e8a6b499
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="quarantine-orders"></a>检验单

[!include [banner](../includes/banner.md)]

本主题介绍检验单如何用于锁定库存。

检验单可用于锁定库存。 例如，您可能要检验质量控制原因的物料。 将把已检验的库存转移到检验仓库。 **注意：** 如果您使用高级仓库管理流程（在仓库管理中），仅为退货销售订单使用检验单。

## <a name="quarantine-on-hand-inventory-items"></a>检验现有库存物料
在检验物料时，您可以手动创建检验单或设置该系统以在收货处理期间自动创建检验单。 若要自动创建检验单，请在**物料模型组**页的**库存策略**选项卡上选择**检验管理**选项。 您还必须在**检验仓库**字段中为接收仓库指定默认检验仓库。 当实际现有库存量在采购订单或生产订单中记录时，检验物料会自动移至 Microsoft Dynamics 365 for Finance and Operations 中的检验仓库中。 因为检验单的状态改为**已开始**，所以发生此移动。 当您手动创建检验单时，则不必需在相关的物料模型组中为检验管理设置物料。 对于此流程，必须指定应检验的现有库存量和应使用的检验仓库。 您可以使用检验单状态来帮助计划流程。

## <a name="quarantine-order-statuses"></a>检验单状态
检验单可以有下列状态：

-   已创建
-   已开始
-   完工入库
-   已结束

### <a name="created"></a>创建时间

如果检验单已手动创建，但物料不在检验仓库中，则检验单具有**已创建**状态。 生成两个库存交易记录。 一个交易记录是可具有**在单**、**实际预留**或**已领料**状态的发货交易记录。 另一个交易记录是可在检验仓库中具有**已订购**或**已登记**状态的收货交易记录。 可使用一般流程预留、领取和登记库存更新。

### <a name="started"></a>已开始

当检验单已具有**已开始**状态时，库存将从常规仓库转移到检验仓库，并且会生成两个库存交易记录。 一个交易记录具有**已扣除**状态，另一个交易记录具有**已接收**状态。 同时，创建两个库存交易记录以处理退货转移。 这些交易记录未到期。 一个交易记录具有**实际预留**状态，另一个交易记录具有**已订购**状态。

### <a name="reported-as-finished"></a>完工入库

通过单击**完工入库**，您可以将已开始的检验单报告为完工入库。 物料从检验仓库中取出，但尚未移回常规仓库。 移回常规仓库可以通过可在完工入库流程中初始化的物料到达日记帐进行处理。

### <a name="ended"></a>已结束

当检验单结束后，物料将从检验仓库移回常规仓库。 物料交易记录的状态在检验仓库中设置为**已售出**，在常规仓库中设置为**已采购**。

## <a name="quarantine-order-scrap"></a>检验单报废
作为检验单流程的一部分，可以报废库存。 当处理报废时，库存状态将按检验仓库中的发货交易记录设置为**售出**。

<a name="additional-resources"></a>其他资源
--------

[库存锁定](inventory-blocking.md)

