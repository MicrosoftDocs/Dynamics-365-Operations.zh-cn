---
title: 与第三方制造执行系统集成
description: 本主题说明如何将 Microsoft Dynamics 365 Supply Chain Management 与第三方制造执行系统 (MES) 集成。
author: t-benebo
ms.date: 10/01/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-01
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 43814023474d44b8c95bae087c7b6a4d52d21471
ms.sourcegitcommit: 7cbd53617af179a0de74aae30c149edc95e86684
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2021
ms.locfileid: "7891918"
---
# <a name="integrate-with-third-party-manufacturing-execution-systems"></a>与第三方制造执行系统集成

[!include [banner](../includes/banner.md)]

一些使用 Microsoft Dynamics 365 Supply Chain Management 的制造组织使用 Dynamics 365 中的本地功能来控制机器、设备和人员的制造活动。 但是，其他制造组织，尤其是那些具有先进制造要求的制造组织，则改用第三方制造执行系统 (MES)。 组织可能会选择第三方 MES 解决方案，比如如果它是专门为其垂直行业量身定制的。

在集成解决方案中，数据交换是完全自动化的，几乎是实时发生。 因此，两个系统中的数据都会保持最新，不需要手动输入数据。 例如，当材料消耗在 MES 中登记时，集成将确保在 Dynamics 365 中也登记相同的消耗。 因此，最新的库存记录可用于其他重要流程，如计划和销售。

此解决方案使 Supply Chain Management 用户可以更快、更轻松、更便宜地与第三方 MES 集成。 它提供以下功能：

- 支持[关键制造执行流程](#processes-available-for-mes-integration)的业务事件和接口
- 一个集中式仪表板，您可以在其中跟踪事件处理历史记录，并对失败的流程进行故障排除和修复

下图显示了在集成解决方案中交换的业务事件、流程和消息的典型集合。

![典型集成场景。](media/3p-mes-scenario.png "典型集成场景。")

## <a name="turn-on-the-mes-integration-feature"></a>开启 MES 集成功能

此功能只有在系统中开启之后才能使用。 管理员可以使用[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*生产控制*
- **功能名称**：*制造执行系统集成*

## <a name="processes-available-for-mes-integration"></a>可用于 MES 集成的流程

您可以为集成启用以下任何或所有流程。

| 流程名称 | Description |
|---|---|
| 发布生产订单和生产订单状态更改业务事件 | 此流程提供了一个业务事件，MES 可以侦听该事件，以获取有关应生产的生产订单的信息。 与生产订单相关的参考数据会通过 Open Data Protocol (OData) 或数据实体从 Supply Chain Management 共享到 MES。 |
| 开始生产订单 | 此流程为 Supply Chain Management 提供有关使用 MES 启动的生产订单的信息。 它确保两个系统都有所有制造活动的最新视图。 |
| 报告产生或废品数量 | 此流程为 Supply Chain Management 提供有关使用 MES 报告的生产作业的良好和残次数量的信息。 它可确保车间主管对生产计划进度有最新的了解。 |
| 报告材料消耗量 | 此流程 Supply Chain Management 提供来自 MES 的有关消耗材料数量的信息。 它让最新的库存记录可用于其他重要流程，如计划和销售。 |
| 报告操作消耗的时间 | 此流程为 Supply Chain Management 提供有关用于特定操作的时间的信息。 |
| 结束生产订单 | 此流程通知 Supply Chain Management MES 已将生产订单更新为最终状态 *结束*。 此状态表示生产订单将不再生产更多数量。 |

## <a name="monitor-incoming-messages"></a>监视传入消息

要监视传入系统的消息，打开 **制造执行系统集成** 页面。 在那里，您可以查看、处理和排查问题。

## <a name="call-the-api"></a>调用 API

要调用 MES 集成 API，向以下终结点 URL 发送 `POST` 请求：

`/api/services/SysMessageServices/SysMessageService/SendMessage`

您发送的请求正文应类似于以下示例。 根据需要替换 `_companyId`、`_messageType` 和 `_messageContent` 值。 有关 API 支持的各种消息类型以及如何设计其内容的信息，请参阅下一节。

```json
{
    "_companyId": "USMF",
    "_messageQueue": "JmgMES3P",
    "_messageType": "ProdProductionOrderReportFinished",
    "_messageContent":
    "{\"ProductionOrderNumber\": \"P000123\", \"ReportFinishedLines\": [{\"ItemNumber\": \"A0001\", \"ReportedGoodQuantity\": 10, \"ReportAsFinishedDate\": \"2021-01-01\"}]}"
}
```

## <a name="api-message-types-and-content"></a>API 消息类型和内容

本节介绍了可以通过 MES 集成 API 交换的每种类型的消息。

### <a name="start-production-order-message"></a>开始生产订单消息

对于 *开始生产订单* 消息，`_messageType` 值是 `ProdProductionOrderStart`。 下表显示了此消息支持的字段。

| 字段名称 | Status | 类型 |
|---|---|---|
| `ProductionOrderNumber` | 强制 | 字符串 |
| `StartedQuantity` | 可选 | 实数 |
| `StartedDate` | 可选 | 日期 |
| `AutomaticBOMConsumptionRule` | 可选 | 枚举 (FlushingPrincip \| Always \| Never) |

### <a name="report-as-finished-message"></a>完工入库消息

对于 *完工入库* 消息，`_messageType` 值是 `ProdProductionOrderReportFinished`。 下表显示了此消息支持的字段。

| 字段名称 | Status | 类型 |
|---|---|---|
| `ProductionOrderNumber` | 强制 | 字符串 |
| `ReportFinishedLines` | 强制 | 行列表（至少一个），每个列表都包含下表中描述的有效负载 |

下表显示了 `ProdProductionOrderReportFinished` 消息的 `ReportFinishedLines` 部分中的每一行所支持的字段。

| 字段名称 | Status | 类型 |
|---|---|---|
| `LineNumber` | 可选 | 实数 |
| `ItemNumber` | 可选 | 字符串|
| `ProductionType` | 可选 | 枚举 (MainItem \| Formula \| BOM \| Co_Product \| By_Product \| None)，可扩展 |
| `ReportedErrorQuantity` | 可选 | 实数|
| `ReportedGoodQuantity` | 可选 | 实数|
| `ReportedErrorCatchWeightQuantity` | 可选 | 实数 |
| `ReportedGoodCatchWeightQuantity` | 可选 | 实数 |
| `AcceptError` | 可选 |布尔值 |
| `ErrorCause` | 可选 | 枚举 (None \| Material \| Machine \| OperatingStaff)，可扩展 |
| `ExecutedDateTime` | 可选 | 日期时间 |
| `ReportAsFinishedDate` | 可选 | 日期 |
| `AutomaticBOMConsumptionRule` | 可选 | 枚举 (FlushingPrincip \| Always \| Never) |
| `AutomaticRouteConsumptionRule` | 可选 |枚举 (RouteDependent \| Always \| Never) |
| `RespectFlushingPrincipleDuringOverproduction` | 可选 | 布尔值 |
| `ProductionJournalNameId` | 可选 | 字符串 |
| `PickingListProductionJournalNameId` | 可选 | 字符串|
| `RouteCardProductionJournalNameId` | 可选 | 字符串 |
| `FromOperationNumber` | 可选 | 整数|
| `ToOperationNumber` | 可选 | 整数|
| `InventoryLotId` | 可选 | 字符串 |
| `BaseValue` | 可选 | 字符串 |
| `EndJob` | 可选 | 布尔值 |
| `EndPickingList` | 可选 | 布尔值 |
| `EndRouteCard` | 可选 | 布尔值 |
| `PostNow` | 可选 | 布尔值 |
| `AutoUpdate` | 可选 | 布尔值 |
| `ProductColorId` | 可选 | 字符串|
| `ProductConfigurationId` | 可选 | 字符串 |
| `ProductSizeId` | 可选 | 字符串 |
| `ProductStyleId` | 可选 | 字符串 |
| `ProductVersionId` | 可选 | 字符串 |
| `ItemBatchNumber` | 可选 | 字符串 |
| `ProductSerialNumber` | 可选 | 字符串 |
| `LicensePlateNumber` | 可选 | 字符串 |
| `InventoryStatusId` | 可选 | 字符串 |
| `ProductionWarehouseId` | 可选 | 字符串 |
| `ProductionSiteId` | 可选 | 字符串 |
| `ProductionWarehouseLocationId` | 可选 | 字符串 |
| `InventoryDimension1` 到 `InventoryDimension12` | 可选 | 字符串 |

12 个可扩展维度（`InventoryDimension1` 到 `InventoryDimension12`）需要自定义，不总是使用。 有关详细信息，请参阅[通过扩展添加新库存维度](../../fin-ops-core/dev-itpro/extensibility/inventory-dimensions.md)。

### <a name="material-consumption-picking-list-message"></a>材料消耗（领料单）消息

对于 *材料消耗（领料单）* 消息，`_messageType` 值是 `ProdProductionOrderPickingList`。 下表显示了此消息支持的字段。

| 字段名称 | Status | 类型 |
|---|---|---|
| `ProductionOrderNumber` | 强制 | 字符串 |
| `JournalNameId` | 可选 | 字符串 |
| `PickingListLines` | 强制 | 行列表（至少一个），每个列表都包含下表中描述的有效负载 |

下表显示了 `ProdProductionOrderPickingList` 消息的 `PickingListLines` 部分中的每一行所支持的字段。

| 字段名称 | Status | 类型 |
|---|---|---|
| `ItemNumber` | 强制 | 字符串 |
| `ConsumptionBOMQuantity` | 可选 | 实数 |
| `ProposalBOMQuantity` | 可选 | 实数 |
| `ScrapBOMQuantity` | 可选 | 实数 |
| `BOMUnitSymbol` | 可选 | 字符串 |
| `ConsumptionInventoryQuantity` | 可选 | 实数 |
| `ProposalInventoryQuantity` | 可选 | 实数 |
| `ConsumptionCatchWeightQuantity` | 可选 | 实数 |
| `ProposalCatchWeightQuantity` | 可选 | 实数 |
| `ConsumptionDate` | 可选 | 日期 |
| `OperationNumber` | 可选 | 整数 |
| `LineNumber` | 可选 | 实数 |
| `PositionNumber` | 可选 | 字符串 |
| `IsConsumptionEnded` | 可选 | 布尔值 |
| `ErrorCause` | 可选 | 枚举 (None \| Material \| Machine \| OperatingStaff)，可扩展 |

### <a name="time-used-for-operation-route-card-message"></a>用于操作的时间（工艺卡）消息

对于 *用于操作的时间（工艺卡）* 消息，`_messageType` 值是 `ProdProductionOrderRouteCard`。 下表显示了此消息支持的字段。

| 字段名称 | Status | 类型 |
|---|---|---|
| `ProductionOrderNumber` | 强制 | 字符串 |
| `JournalNameId` | 可选 | 字符串 |
| `RouteCardLines` | 强制 | 行列表（至少一个），每个列表都包含下表中描述的有效负载 |

下表显示了 `ProdProductionOrderRouteCard` 消息的 `RouteCardLines` 部分中的每一行所支持的字段。

| 字段名称 | Status | 类型 |
|---|---|---|
| `OperationNumber` | 强制 | 整数 |
| `OperationPriority` | 可选 | 枚举 (Primary \| Secondary1 \| Secondary2 \| ... \| Secondary20) |
| `OperationId` | 可选 | 字符串 |
| `OperationsResourceId` | 可选 | 字符串 |
| `Worker` | 可选 | 字符串 |
| `HoursRouteCostCategoryId` | 可选 | 字符串 |
| `QuantityRouteCostCategoryId` | 可选 | 字符串 |
| `HourlyRate` | 可选 | 实数 |
| `Hours` | 可选 | 实数 |
| `GoodQuantity` | 可选 | 实数 |
| `ErrorQuantity` | 可选 | 实数 |
| `CatchWeightGoodQuantity` | 可选 | 实数 |
| `CatchWeightErrorQuantity` | 可选 | 实数 |
| `QuantityPrice` | 可选 | 实数 |
| `ProcessingPercentage` | 可选 | 实数 |
| `ConsumptionDate` | 可选 | 日期 |
| `TaskType` | 可选 | 枚举 (QueueBefore \| Setup \| Process \| Overlap \| Transport \| QueueAfter \| Burden) |
| `ErrorCause` | 可选 | 枚举 (None \| Material \| Machine \| OperatingStaff)，可扩展 |
| `OperationCompleted` | 可选 | 布尔值 |
| `BOMConsumption` | 可选 | 布尔值 |
| `ReportAsFinished` | 可选 | 布尔值 |

### <a name="end-production-order-message"></a>结束生产订单消息

对于 *结束生产订单* 消息，`_messageType` 值是 `ProdProductionOrderEnd`。 下表显示了此消息支持的字段。

| 字段名称 | Status | 类型 |
|---|---|---|
| `ProductionOrderNumber` | 强制 | 字符串 |
| `ExecutedDateTime` | 可选 | 日期时间 |
| `EndedDate` | 可选 | 日期 |
| `UseTimeAndAttendanceCost` | 可选 | 布尔值 |
| `AutoReportAsFinished` | 可选 | 布尔值 |
| `AutoUpdate` | 可选 | 布尔值 |

## <a name="receive-feedback-about-the-state-of-a-message"></a>接收有关消息状态的反馈

在 MES 向 Supply Chain Management 发送消息后，Supply Chain Management 可能需要返回有关消息状态的反馈。 以下是此行为可能相关的一些案例示例：

- 没有人负责持续监管 MES 集成。
- 负责监管 MES 集成的人员希望在消息失败时通过电子邮件收到通知，以便他们知道必须采取行动。
- MES 必须显示错误消息以通知车间操作员或 IT 部门的人员他们必须采取行动。
- MES 在收到失败消息后必须重新计算订单计划（例如，因为生产订单未能启动）。

在这些情况下，您可以利用 Supply Chain Management 中的标准预警功能。 有关标准预警如何工作的信息，请参阅以下资源：

- 帮助主题：[预警概述](../../fin-ops-core/fin-ops/get-started/alerts-overview.md)
- 视频：[Dynamics 365 for Finance and Operations 中的预警规则选项](https://www.youtube.com/watch?v=cpzimwOjicM&ab_channel=MicrosoftDynamics365)

例如，您可以设置以下预警来提供有关消息状态的反馈：

- 创建在消息 *失败* 时使用的业务事件（“外部发送”）。
- 向 IT 管理员或生产车间经理发送通知和电子邮件。
