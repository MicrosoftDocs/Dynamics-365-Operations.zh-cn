---
title: 计划优化使用的日期和时间参数
description: 本主题提供有关计划优化在运行期间使用的日期和时间参数的信息。
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0708404f286253449e0400fc65680e903f6d1e9b
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468823"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>计划优化使用的日期和时间参数

[!include [banner](../../includes/banner.md)]

本主题提供有关计划优化在运行期间使用的日期和时间参数的信息。

内置主计划引擎在所有计算中使用交易日期，但计划优化使用转换为日期的日期和时间值。 此行为差异可能导致以下情况：未包括在运行主计划当天午夜创建的预测交易，因为计划优化认为是在当前日期之前创建的，此为举例。

## <a name="parameters-for-issue-and-demand-transactions"></a>发货和需求交易的参数

下表列出了计划优化在处理发货和需求交易时使用的参数。

| 参数 | 计划优化中的参数名称 | 说明 | Microsoft Dynamics 365 Supply Chain Management 中的等效字段（在 ReqTrans 表中） |
|---|---|---|---|
| 计划发货时间 | `PlannedIssueTime` | 当前计划要发货的日期。 | **结束日期** (`FuturesDate`) 和 **延迟时间** (`FuturesTime`) |
| 请求的发货时间 | `RequestedIssueTime` | 用户请求并在 Supply Chain Management 中设置的发货日期。 此参数仅适用于已发布或已批准的计划订单。 对于计划订单，默认情况下为空。 | **请求日期** (`ReqDateDlvOrig`) |
| 要求发货时间 | `RequiredIssueTime` | 经计划优化调整的要求发货日期。 如果运行计划优化时请求的发货时间在过去，要求发货时间将调整为第一个不早于今天日期的开放日期。 如果请求的发货时间在日历中标记为锁定，要求发货时间将调整为该日期之前的第一个开放日期。 | **要求日期** (`ReqDate`) 和 **要求时间** (`ReqTime`) |
| 发货时间延迟 | `IssueTimeDelay` | 计划发货时间与已批次和已发布订单的请求发货时间或要求发货时间之间的时间差。 | **延迟(天)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>收货和供应交易的参数

下表列出了计划优化在处理收货和供应交易时使用的参数。

| 参数 | 计划优化中的参数名称 | 说明 | Supply Chain Management 中的等效字段（在 ReqTrans 或 ReqPO 表中） |
|---|---|---|---|
| 计划供应时间 | `PlannedAvailabilityTime` | 计划可以收货的日期。 | **要求日期** (`ReqDate`) 和 **要求时间** (`ReqTime`) |
| 计划收货时间 | `PlannedReceiptTime` | 收货货物到达位置的日期。 | 如果订单尚未下达，为 **结束日期** (`FuturesDate`)、**延迟时间** (`FuturesTime`) 和 **交货日期** (`ReqDateDlv`) 或 **请求日期** (`ReqDateDlvOrig`)。 |
| 要求供应时间 | `RequiredAvailabilityTime` | 经计划优化调整的要求供应日期。 | **要求日期** (`ReqDate`) 和 **要求时间** (`ReqTime`) |
| 预期收货时间 | `ExpectedReceiptTime` | 已发放收货的预期收货日期。 此值由用户在 Supply Chain Management 中设置，不由计划优化调整。 此参数仅适用于已发放收货。 | **请求日期** (`ReqDateDlvOrig`) |
| 要求收货时间 | `RequiredReceiptTime` | 经计划优化调整的要求收货日期。 | **要求日期** (`ReqDate`) 和 **要求时间** (`ReqTime`) |
| 计划订购时间 | `PlannedOrderingTime` | 由计划优化计算的订购日期。 | **订单日期** (`ReqDateOrder`) 和 **订单时间** (`ReqTimeOrder`) |
| 计划活动开始时间 | `PlannedActivityStartTime` | 此收货的活动应开始的日期。 | **开始日期** (`SchedFromDate`) |
| 收货时间延迟 | `ReceiptTimeDelay` | 计划收货时间与要求收货时间之间的时间差。 | **延迟(天)** (`FuturesDays`) 和 **延迟时间** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>计划优化使用的日期参数的示例

下图中的计划位于天级别，但计划优化在更细化的级别运行。 例如，由于宽限期可以按小时计，因此计划订购时间可以是 2021 年 1 月 22 日 11：35，等等。

### <a name="example-1-simple-scenario"></a>示例 1：简单场景

在 1 月 22 日具有请求发货时间的一个销售订单被一个采购订单覆盖。 使用以下设置：

- 无提前期
- 无日历（所有日期均为开放日期。）
- 无宽限期

下图显示了此场景。 （选择插图以打开更大的版本。）

[![简单场景。](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>示例 2：提前期场景

在 1 月 22 日具有请求发货时间的一个销售订单被一个采购订单覆盖。 使用以下设置：

- 提前期为三天
- 无日历（所有日期均为开放日期。）
- 无宽限期

下图显示了此场景。 （选择插图以打开更大的版本。）

[![提前期场景。](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>示例 3：宽限期场景

在 1 月 22 日具有请求发货时间的一个销售订单被一个采购订单覆盖。 使用以下设置：

- 提前期为三天
- 四天订购宽限期
- 五天供应宽限期
- 无日历（所有日期均为开放日期。）

下图显示了此场景。 （选择插图以打开更大的版本。）

[![宽限期场景。](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>示例 4：延迟场景

在 1 月 22 日具有请求发货时间的一个销售订单被一个采购订单覆盖。 此示例使用与示例 3 相同的设置，但计划日期移至 1 月 15 日。 倒推排产（红色标记）失败，因为计划订购时间必须早于今天的日期。 因此，主计划必须正推排产，延迟发生。

下图显示了此场景。 （选择插图以打开更大的版本。）

[![延迟场景。](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>示例 5：转移场景

在 1 月 22 日具有请求发货时间的仓库 1 中的一个销售订单被计划采购订单覆盖的仓库 2 中的一个转移单覆盖。 使用以下设置：

- 转移提前期为三天（仓库 1）
- 采购提前期为两天（仓库 2）
- 无日历（所有日期均为开放日期。）

下图显示了此场景。 （选择插图以打开更大的版本。）

[![转移场景。](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>示例 6：带日历的提前期场景

在 1 月 22 日具有请求发货时间的一个销售订单被一个采购订单覆盖。 使用以下设置：

- 提前期为三天
- 发货日历（星期五关闭）
- 供应日历（星期四和星期五关闭）
- 收货日历（星期二、星期三和星期日关闭）
- 提前期日历（星期四和星期五关闭）
- 订购日历（星期一和星期六开放）

下图显示了此场景。 （选择插图以打开更大的版本。）

[![带日历的提前期场景。](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>示例 7：带日历的延迟场景

在 1 月 22 日具有请求发货时间的一个销售订单被一个采购订单覆盖。 此示例使用与示例 6 相同的设置，但计划日期移至 1 月 13 日。 倒推排产（红色标记）失败，因为计划订购时间必须早于今天的日期。 因此，主计划必须正推排产，延迟发生。

下图显示了此场景。 （选择插图以打开更大的版本。）

[![带日历的延迟场景。](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
