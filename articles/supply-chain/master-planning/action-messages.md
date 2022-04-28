---
title: 行动消息
description: 行动消息是系统生成的关于更改现有计划订单或确定订单的建议。
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570245"
---
# <a name="action-messages"></a>行动消息

[!include [banner](../includes/banner.md)]

操作消息是系统生成的关于更改现有计划订单、批准订单或确定订单的建议。

行动消息由主计划计算生成，以响应变化的需求。 例如，在您创建采购订单以满足销售订单的需求后，装运日期或数量在该销售订单上发生更改。 在这种情况下，主计划计算会生成一条或多条建议您更新采购订单的操作消息。 您决定是否进行所建议的更改。

您可以设置如何为附加到物料的覆盖范围组计算行动消息。

## <a name="select-action-messages"></a>选择行动消息

在 **覆盖范围组** 页上，您可以选择您希望系统生成的行动消息和消息适用的覆盖范围组或物料。 下表列出了您可以选择的操作消息。

| 消息 | Description |
|---|---|
| 提前 | 系统将根据需要生成操作消息，以将订单移至更早的日期。 在 **提前宽限期** 字段中，您可以指定无提前操作的收货与发货之间可以经过的最大天数。 |
| 推迟 | 系统将根据需要生成操作消息，以将订单移至更晚的日期。 在 **延长宽限期** 字段中，您还可以指定无推迟操作的收货与发货之间可以经过的最大天数。 |
| 减少 | 当生产订单、采购订单或其他收货交易记录应减少以避免超出库存水平时，系统将生成操作消息。 |
| 增加 | 当生产订单、采购订单或其他收货交易记录应增加以避免库存出现短缺时，系统将生成操作消息。 |
| 派生的行动 | 为收货交易记录创建的操作消息将传播到任何派生的要求，同时将为满足这些要求的收货交易记录生成必要的操作消息。 |

以下几节提供了一些详细的场景。

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>使用产品默认订单数量增加和减少操作

在物料的 **默认订单设置** 页面，您可以设置最小订单数量、最大订单数量和多个值。 然后，系统在建议操作时会考虑这些设置，以确保建议永远不会导致供应不足。

例如，您的物料在 **默认订单设置** 页面上有以下设置：

- **最小订单数量**：*0*
- **最大订单数量**：*90*
- **倍数**：*20*

如果此物料的需求数量为 60，主计划将创建数量为 60 的计划采购订单。 如果需求增加 30，主计划会建议增加 40，因为它会采用 20 的倍数，不会导致供应不足。

## <a name="action-messages-for-orders-related-to-safety-stock"></a>与安全存货相关的订单的操作消息

供应安全存货的订单的操作消息永远不会建议将数量减少到低于安全存货所需的数量。 换言之，如果有一个订单供应安全存货和客户需求，当需求降低或取消时，主计划会建议将计划订单减少降低的需求量。 但是，永远不会建议低于所需安全存货的值。

系统不会建议推迟供应安全存货的操作，因为它假定安全存货必须在规定时间和规定日期供应。

### <a name="advance-and-postpone-actions-related-to-boms"></a>提前和推迟与 BOM 相关的操作

与物料清单 (BOM) 组件相关的操作必须在其父项的操作之前应用，因为与更高级别 BOM 相关的进一步订单可能会受到影响。 然后，您必须再次运行主计划以重新计算并建议适当的操作。

例如，您有以下情况：

- *生产* 类型的最终产品 *FG* 的 BOM 包含原材料 *RM*。
- 今天的日期是 1 月 21 日。
- *FG* 的现有已下达生产订单计划于 1 月 25 日下达。
- 为支持现有生产订单，主计划为所需原材料 *RM* 创建了计划采购订单。 此订单的要求日期为 1 月 25 日。
- 今天创建了 *FG* 的新销售订单。 它的要求日期为今天（1 月 21 日）。
- 1 月 21 日在 *RM* 日历上对交付是关闭的，但 1 月 22 日是开放的。

主计划运行时，它会生成提前操作消息，建议将先前计划的生产向上移动，让您可以履行今天的订单。

- 为满足新的需求，建议将 *FG* 的生产订单上移到 1 月 21 日。 （给出此建议时未考虑 *RM* 的关闭日期。）
- 由于生产订单仍需要 *RM*，因此建议同时将计划采购订单上移。 但是，这一次将检查 *RM* 日历。 因此，建议将 *RM* 的计划采购订单移至 1 月 22 日（因为 1 月 21 日已关闭）。

如您所见，对于 *FG* 的计划生产，所需的原材料 *RM* 现在会到货太晚。 因此，您必须首先将提前操作应用于 *RM* 的计划采购订单，然后再次运行主计划。 这时，主计划将生成一条新的操作消息，建议将 *FG* 的生产订单移至 1 月 22 日。
