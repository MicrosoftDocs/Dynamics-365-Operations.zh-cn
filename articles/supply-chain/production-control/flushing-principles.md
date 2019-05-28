---
title: 耗用原则
description: 本主题描述为原材料消耗量使用的四个耗用原则。
author: johanhoffmann
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgShopSupervisorReleaseOrders
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e4b9cd918bec9a094744b208821285c57f01798a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547432"
---
# <a name="controlling-raw-material-consumption-by-using-flushing-principles"></a>使用耗用原则控制原材料消耗量

[!include [banner](../includes/banner.md)]

耗用原则反映用于生产流程中使用的原材料的不同的消耗策略。 消耗是从现有库存量中扣减物料并为生产订单和批次订单将已消耗物料的值设置为**在制品** (WIP) 的流程。 原材料通常从为使用物料的流程配置的位置使用。 此位置称作生产输入位置。

在物料消耗前，物料移至输入位置。 下图显示了此流程。

[![scenario4a](./media/scenario4a.png)](./media/scenario4a.png)

1. 物料仓库
2. 原材料领取
3. 生产输入地点
4. 原材料消耗量
5. 生产流程

原材料消耗量通过以下四个耗用原则进行控制：

- 手动
- 启动
- 完成
- 在库位可用

耗用原则在默认值层次结构中进行配置。 层次结构从已发放的产品开始，此时耗用原则的值为**开始**。 在物料清单 (BOM) 或配方行上，可以覆盖来自产品的耗用原则。 在生产 BOM 行或批次订单配方行上的默认耗用原则从产品或 BOM 或配方上被覆盖的值提取。

## <a name="description-of-the-flushing-principles"></a>耗用原则的描述

### <a name="manual"></a>手动
手动耗用原则指示物料消耗量的登记由人工操作。 例如，如果你希望能够跟踪时间，且因为跟踪目的而必须说明已使用的批号或序列号的数量，则与此原则有关。 手动消耗量在生产领料单日志中登记。 对于已启用高级仓库流程的物料，可以应用手持流。

### <a name="start"></a>启动
“开始”耗用原则指示在开始执行生产订单时将自动使用物料。 使用的物料量与开始的数量成比例。 当“开始”耗用原则与制造执行系统一起使用时，它也可以用于在开始操作或处理作业时耗用物料。 例如，如果消耗量中的差异很小、物料为低价值物料、无跟踪需要或操作运行时间较短时，则与此原则有关。 

### <a name="finish"></a>完成
“完成”耗用原则指示当生产订单报告完工入库时，或当设置为使用物料的操作登记为已完成时将自动使用物料。 使用的物料量与报告完工入库的数量成比例。 当“完成”耗用原则与制造执行系统一起使用时，它也可以用于在完成操作或处理作业时耗用物料。 此原则的适用情况与“开始”原则相同。 但是，“完成”原则适用于运行时间更长，且在操作完成前不应将物料设置为 WIP 的操作。 

### <a name="available-at-location"></a>在库位可用
“在库位可用”耗用原则指示当物料登记为生产领料时自动使用物料。 当原材料领料工作完成时，或当物料在生产输入库位可用且物料行被发放到仓库时，该物料登记为从库位领料。 在批处理作业中对流程进行过帐期间生成领料单。 例如，如果一个生产订单有多个领料活动，则与此原则有关。 在这种情况下，你不必手动更新领料单，而且可以获得 WIP 余额的当前视图。
