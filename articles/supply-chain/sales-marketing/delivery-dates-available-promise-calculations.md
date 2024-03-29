---
title: 订单承诺
description: 本文提供有关订单承诺的信息。 订单承诺帮助您向客户确切承诺交货日期，并给予您履行这些日期的灵活性。
author: Henrikan
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesATP, SalesAvailableDlvDates, SalesCarrier
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c835e25348b937c1dd68d8fa45b0264bd6815c23
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228256"
---
# <a name="order-promising"></a>订单承诺

[!include [banner](../includes/banner.md)]

本文提供有关订单承诺的信息。 订单承诺帮助您向客户确切承诺交货日期，并给予您履行这些日期的灵活性。

订单承诺计算最早的装运日期和接收日期，它是基于交货日期控制方法和运输天数的。 您可以在以下交货日期控制方法中进行选择：

- **销售提前期** - 销售提前期是创建销售订单和装运物料之间的时间。 交货日期计算基于默认天数，不考虑库存可用性、已知需求或计划供应。
- **ATP（可承诺）**– ATP 是可用的且可对某一客户在特定日期承诺的物料数量。 ATP 计算包括未承诺库存、提前期、计划收货和发货。
- **ATP + 发货宽限期**– 装运日期等于 ATP 日期加上物料的发货宽限期。 发货宽限期是准备物料以进行装运所需的时间。
- **CTP（可承诺量）**– 通过分解计算可用性。 如果您正在使用计划优化，则不允许使用 *CTP* 交货日期控制方法，如果选中此方法，则在计算运行时将产生错误。 有关如何设置和使用 CTP 的详细信息，请参阅[使用 CTP 计算销售订单交货日期](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md)。
- **用于计划优化的 CTP** - 使用由计划优化提供的 CTP 计算。 如果您正在使用内置主计划引擎，则此选项无效。 有关如何设置和使用 CTP 的详细信息，请参阅[使用 CTP 计算销售订单交货日期](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md)。

> [!NOTE]
> 更新销售订单时，仅在无法满足现有订单承诺日期的情况下才更新订单承诺信息，如以下示例所示：
>
> - **示例 1**：当前订单承诺日期是 7 月 20 日，但是由于数量增加，您要到 7 月 25 日才能交货。 由于无法再满足当前日期，因此触发了订单承诺。
> - **示例 2**：当前订单承诺日期是 7 月 20 日，但是由于数量减少，现在可能在 7 月 15 日就能交货。 但是，由于仍然可以满足当前日期，因此不会触发订单承诺，并且 7 月 20 日仍然是订单承诺日期。

## <a name="atp-calculations"></a>ATP 计算

通过使用“含预期的累积 ATP”方法计算 ATP 数量。 这一计算 ATP 的方法的主要优点在于，它可以在收货之间的发货总和大于最新收货时（例如，必须使用来自更早收货的数量来满足需求时）处理案例。 “含预期的累积 ATP”计算方法包括所有发货，直到累积收货数量超过累积发货数量。 因此，该 ATP 计算方法评估更早期间的某些数量是否可用于以后的期间。

该 ATP 数量是第一个期间中的未承诺库存余额。 通常，会为计划收货的每个期间计算它。 程序将按天数计算 ATP 期间，并且将当前日期计算为该 ATP 数量的第一个日期。 在第一个期间中，ATP 将包括现有库存量减去到期和逾期的客户订单。

ATP 使用以下公式计算：

ATP = 前一期间的 ATP + 当前期间的收货 - 当前期间的发货 - 截至以下期间前的各个将来期间的净发货数量：在所有将来期间（直到并且包括该将来期间）的收货之和超过发货之和（直到并且包括该将来期间）时的期间。

请注意，ATP 计算不包括有关到期日期以及可以承诺任何数量时超出系统预期的 ATP 时间范围之外的信息。

在没有要考虑的更多发货或收货时，用于以下日期的 ATP 数量与最新计算的 ATP 数量相同。

如果在执行 ATP 检查时未提供用于某一物料的所有维度，则在发货和收货时仍可以指定它们。 在此情况下，在 ATP 计算中，收货和发货必须聚合到现有维度中，以便减少在 ATP 计算中使用的收货行和发货行的数目。

显示的 ATP 数量始终大于或等于 0（零）。 如果该计算返回负的 ATP 数量（例如，如果以前承诺的数量超出可用数量），数量会自动设置为 0。

### <a name="example"></a>示例

**ATP 后向需求时限** 字段控制向后多长时间查找延期需求订单或库存发货。 **ATP 后向供应时限** 字段控制向后多长时间查找延期供应订单或库存收货。 例如，如果只延迟七天的订单应被考虑到 ATP 计算中，则两个字段都应设置为 **7**。

**ATP 延迟需求偏移时间** 和 **ATP 延迟供应偏移时间** 字段控制何时将延期需求或供应考虑到 ATP 计算中。 例如，如果延期供应和需求应被考虑到 ATP 计算中，则两个字段都应设置为 **2**。 值为 **2** 表示应被考虑到 ATP 计算中的延期采购订单的物料数量将在当前日期之后两天可供查看。

对于以下示例，在 **ATP 后向需求时限** 和 **ATP 后向供应时限** 字段中输入了 **7**，在 **ATP 延迟需求偏移时间** 和 **ATP 延迟供应偏移时间** 字段中输入了 **1**。

应在三天之前收到的 200 件产品的采购订单尚未接收。 因此，昨天应装运的 75件 相同产品的销售订单行尚未装运。

客户致电并要订购 150 件同一产品。 在您确认产品的可用性时，您会发现将在 10 天交货的其他 100 件产品的采购订单。

您为该产品创建销售订单行并输入 **150** 的数量。

由于交货日期控制方法是 ATP，所以会计算 ATP 数据以找到最早的可能装运日期。 基于设置，延期采购订单和销售订单会被考虑，并且当前日期生成的 ATP 数量是 0。 明天，当预计会收到延期采购订单时，会将 ATP 数量计算为大于 0（在这种情况下，它被计算为 125）。 但是，从现在起 10 天，当预期接收 100 件的其他采购订单时，ATP 数量将变为超过 150。

因此，基于 ATP 计算，装运日期被设置为从现在起 10 天。 因此，您告知客户请求数量的可以为从现在起的 10 天交货。

## <a name="ctp-calculations"></a>CTP 计算

利用 CTP 功能，您可以为客户提供可承诺特定商品的实际日期。 对于每个销售行，您可以提供一个考虑到现有库存量、产能和运输时间的日期。

CTP 通过考虑产能信息来扩展 ATP 功能。 虽然 ATP 仅考虑物料可用性并假定有无限产能资源，但 CTP 会考虑物料和产能的可用性。 因此，它可以让用户更真实地了解是否可以在给定期限内满足需求。

CTP 的工作方式略有不同，具体取决于您使用的主计划引擎（计划优化或内置引擎）。 用于计划优化的 CTP 当前仅支持内置引擎所支持的 CTP 方案的一部分。

有关如何针对每个引擎设置和使用 CTP 的详细信息，请参阅[使用 CTP 计算销售订单交货日期](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md)。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
