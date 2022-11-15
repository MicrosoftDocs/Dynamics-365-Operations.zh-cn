---
title: 使用 CTP 计算销售订单交货日期
description: 利用可承诺 (CTP) 功能，您可以为客户提供可承诺特定商品的实际日期。 本文介绍如何针对每个计划引擎（计划优化和已弃用的主计划引擎）设置和使用 CTP。
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 4a3b8ba89d9fb224026cf32cad89d7f28321ee79
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741195"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>使用 CTP 计算销售订单交货日期

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->
<!-- KFN: Split into two topics, one for PO and one for classic. -->

利用可承诺 (CTP) 功能，您可以为客户提供可承诺特定商品的实际日期。 对于每个销售行，您可以提供一个考虑到现有库存量、产能和运输时间的日期。

CTP 通过考虑产能信息来扩展[可承诺](../../sales-marketing/delivery-dates-available-promise-calculations.md) (ATP) 功能。 虽然 ATP 仅考虑物料可用性并假定有无限产能资源，但 CTP 会考虑物料和产能的可用性。 因此，它可以让用户更真实地了解是否可以在给定期限内满足需求。

CTP 的工作方式略有不同，具体取决于您使用的主计划引擎（计划优化或已弃用的主计划引擎）。 本文介绍如何针对每个引擎设置它。 用于计划优化的 CTP 当前仅支持已弃用的主计划引擎所支持的 CTP 方案的一部分。

## <a name="turn-on-ctp-for-planning-optimization"></a>打开用于计划优化的 CTP

用于已弃用的主计划引擎的 CTP 始终可用。 但是，如果您要使用用于计划优化的 CTP，则必须为您的系统启用它。 管理员可以使用[功能管理](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)设置检查功能状态和开启功能。 在 **功能管理** 工作区中，此功能按照下面的方式列出：

- **模块**：*主计划*
- **功能名称**：*（预览版）用于计划优化的 CTP*

## <a name="how-ctp-compares-to-atp"></a>CTP 与 ATP 的区别

CTP 和 ATP 相似，但 CTP 通常可以提供更准确的结果，如以下示例所示。

物料 A 由物料 B 和 C 组成，物料 A 的现有数量为 0（零）。 如果执行仅考虑物料的 ATP 检查，则 ATP 数量也将为 0（零）。 但是，如果您执行 CTP 检查，则系统将检查物料 B 和 C 的可用性，检查将其制作成物料 A 所需的资源，并计算可生产出的物料 A 数量。 此外，CTP 计算可以检查制造更多物料 B 和 C 并使用它们制作更多物料 A 所需的资源和材料。

考虑材料和资源的 CTP 计算所显示的数量可能大于仅检查材料的计算，尤其是当正在检查的物料是按订单装配的物料时。 换言之，CTP 功能基于分解函数，可以为所选销售订单行运行以计算预期交货日期。

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>CTP 的差别取决于您使用的主计划引擎

下表总结了用于计划优化的 CTP 与用于已弃用的主计划引擎的 CTP 之间的差异。

| 分项指标 | 计划优化 | 已弃用的主计划引擎 |
|---|---|---|
| 订单、订单行和产品的 **交货日期控制** 设置 | *用于计划优化的 CTP* | *CTP* |
| 计算时间 | 通过将动态计划作为计划任务运行来触发此计算。 | 每次输入或更新销售订单行时，都会立即触发此计算。 |
| **用于计划优化的 CTP 状态** 字段值 | <p>对于自从创建或上次更新订单和行以来尚未运行动态计划的订单和订单行，显示了 *未就绪* 值。</p><p>对于已使用 CTP 通过运行动态计划计算确认交货日期的订单和行，显示了 *就绪* 值。</p> | 始终显示了 *就绪* 值。 |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a>设置默认交货日期控制方法

系统可以使用多种方法中的任意方法来计算每个订单和订单行的交货日期估计值。 您应设置最常用作全局默认方法的交货日期控制方法。 您还可以为每个产品设置单独的覆盖。 稍后，您将能够根据需要覆盖每个订单和/或订单行的默认方法。

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a>设置全局默认交货日期控制

默认交货日期控制方法将应用于所有不应用覆盖的新订单行。 要选择一个，请按照以下步骤操作。

1. 转至 **应收帐款 \> 设置 \> 应收帐款参数**。
1. 在 **装运** 选项卡上，在 **交货控制** 快速选项卡上的 **交货日期控制** 字段中，选择要用作公司默认方法的方法：

    - *无* - 不计算交货日期。
    - *销售提前期* - 销售提前期是创建销售订单和装运物料之间的时间。 交货日期计算基于默认天数，不考虑库存可用性、已知需求或计划供应。
    - *ATP* - ATP 是可向客户承诺的特定日期可提供的物料数量。 ATP 计算包括未承诺库存、提前期、计划收货和发货。
    - *ATP + 发货宽限期* - 装运日期等于 ATP 日期加上物料的发货宽限期。 发货宽限期是准备物料以进行装运所需的时间。
    - *CTP* – 使用已弃用的主计划引擎提供的 CTP 计算。 如果您正在使用计划优化，则不允许使用 *CTP* 交货日期控制方法，如果选中此方法，则在计算运行时将产生错误。
    - *用于计划优化的 CTP* - 使用由计划优化提供的 CTP 计算。 如果您正在使用已弃用的主计划引擎，则此选项无效。

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>设置单个产品的交货日期控制覆盖

如果您希望使用交货日期控制方法，而不是使用设置为全局默认方法的某种方法，则您可以为特定产品分配覆盖。

1. 转到 **产品信息管理 \> 产品 \> 已发布产品**。
1. 选择要设置的产品。
1. 在操作窗格上，在 **管理库存** 选项卡上的 **订单设置** 组中，选择 **默认订单设置**。
1. 在 **默认订单设置** 页面上的 **销售订单** 快速选项上，将 **覆盖交货控制** 选项设置为 *是*。
1. 在 **交货日期控制** 字段中，选择要用于所选产品的方法。 [设置全局默认交货日期控制](#global-default)部分中描述的相同选项可用。

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a>计划用于计划优化的 CTP 计算

当您使用用于计划优化的 CTP 时，必须运行动态计划以触发系统执行 CTP 计算，然后为所有相关订单设置已确认的装运和收货日期。 计划必须包括所有需要确认的装运日期和收货日期的物料。 （当您使用用于已弃用的主计划引擎的 CTP 时，CTP 计算将立即在本地完成。 因此，您不必运行动态计划来查看 CTP 结果。）

为确保所有用户都能及时使用这些日期，我们建议您设置批处理作业以定期运行相关计划。 例如，设置为每 30 分钟运行一次动态计划的批处理作业将设置已确认的装运并每 30 分钟接收一次日期。 因此，输入和导入订单的用户最多需要等待 30 分钟才能获取已确认的装运和接收日期。

若要将批处理作业设置为按定期时间表运行动态计划，请按照以下步骤操作。

1. 转到 **主计划 \> 主计划 \> 运行 \> 主计划**。
1. 在 **主计划** 对话框中的 **参数** 快速选项卡上，将 **主计划** 字段设置为要运行的动态计划。
1. 在 **在后台运行** 快速选项卡上，将 **批处理** 选项设置为 *是*。
1. 选择 **定期**，并根据需要设置计划。
1. 选择 **确定** 以保存此计划。
1. 选择 **确定** 创建批处理作业，然后关闭对话框。

## <a name="use-ctp-for-the-deprecated-master-planning-engine"></a>使用用于已弃用的主计划引擎的 CTP

### <a name="create-a-new-order-by-using-ctp-for-the-deprecated-master-planning-engine"></a>使用用于已弃用的主计划引擎的 CTP 创建新订单

每次添加新的销售订单或订单行时，系统都会向其分配默认交货日期控制方法。 订单标题始终以全局默认方法开头。 如果将覆盖分配给已订购物料，则新订单行将使用该覆盖。 否则，新订单行还将使用全局默认方法。 因此，您应该设置默认方法，使其与您最常使用的交货日期控制方法相匹配。 创建订单后，您可以根据需要在订单标头和/或订单行级别覆盖默认方法。 有关详细信息，请参阅[设置默认交货日期控制方法](#default-methods)和[更改现有销售订单以使用 CTP](#change-orders)。

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-the-deprecated-master-planning-engine"></a>在使用用于已弃用的主计划引擎的 CTP 时查看已确认的交货日期

如果您使用的是已弃用的主计划引擎，则 CTP 计算将应用于 **交货日期控制** 字段设置为 *CTP* 的订单和/或订单行。

对于使用用于已弃用的主计划引擎的 CTP 的销售行，每次保存销售行时，系统都会自动设置 **已确认的装运日期** 和 **已确认的接收日期** 字段。 如果您稍后对销售行进行相关更改（例如，通过更改其数量或站点），则将立即重新计算日期。

- 若要查看销售订单行的已确认交货日期，请打开销售订单并选择销售行。 然后，在 **行明细** 快速选项卡上的 **交货** 选项卡中，查看 **已确认的装运日期** 和 **已确认的接收日期** 值。
- 若要查看整个订单的已确认交货日期，请打开销售订单并选择 **标头** 视图。 然后，在 **交货** 快速选项卡上，查看 **已确认的装运日期** 和 **已确认的接收日期** 值。

## <a name="use-ctp-for-planning-optimization"></a>使用用于计划优化的 CTP

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>使用用于计划优化的 CTP 创建新订单

每次添加新的销售订单或订单行时，系统都会向其分配默认交货日期控制方法。 订单标题始终以全局默认方法开头。 如果将覆盖分配给已订购物料，则新订单行将使用该覆盖。 否则，新订单行还将使用全局默认方法。 因此，您应该设置默认方法，使其与您最常使用的交货日期控制方法相匹配。 创建订单后，您可以根据需要在订单标头和/或订单行级别覆盖默认方法。 有关详细信息，请参阅[设置默认交货日期控制方法](#default-methods)和[更改现有销售订单以使用 CTP](#change-orders)。

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>使用用于计划优化的 CTP 时查看已确认的交货日期

如果您使用的是计划优化，则 CTP 计算将应用于 **交货日期控制** 字段设置为 *用于计划优化的 CTP* 的订单和/或订单行。

对于使用用于计划优化的 CTP 的销售行，在您运行适当的动态计划（通常使用定期批处理作业）之前，**已确认的装运日期** 和 **已确认的接收日期** 字段将为空白。 然后系统会自动设置它们。 有关详细信息，请参阅[计划用于计划优化的 CTP 计算](#batch-job)。

**用于计划优化的 CTP 状态** 字段指示是否已针对使用用于计划优化的 CTP 的每个行计算了已确认的日期。 对于确认的交货日期尚未计算或由于其他更改而不再有效的行和订单，该字段显示的值为 *未就绪*。 对于已计算的行和订单，它显示的值为 *就绪*。 您可以查看每个行和整个订单的状态。

- 若要查看每个销售订单行的状态，请打开销售订单并选择销售行。 然后，在 **行明细** 快速选项卡上，在 **交货** 选项卡上，查看 **用于计划优化的 CTP 状态** 值。 该行的 **已确认的装运日期** 和 **已确认的接收日期** 字段在计算后也会显示在此选项卡上。
- 若要查看整个订单的状态，请打开销售订单并选择 **标头** 视图。 然后，在 **交货** 快速选项卡上，查看 **用于计划优化的 CTP 状态** 值。 该订单的 **已确认的装运日期** 和 **已确认的接收日期** 在计算后也会显示在此选项卡上。

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - 如果您在用于计划优化的 CTP 计算了销售订单行的确认日期后更新此销售订单行，则系统将清除这些日期，直至下次运行适当的动态计划。
> - 如果您编辑可能会影响现有确认日期的相关设置（例如，通过更改提前期、预留或标记），您应该清除相关现有订单的确认日期。 此操作将导致每个相关行的状态更改为 *未就绪*。 反过来，此更改将导致系统在下次运行动态计划时重新计算确认的日期。

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a>更改现有销售订单以便它们使用 CTP

您可以随时更改任何未结订单的 **交货日期控制** 值。 您可以根据需要在标头级别和/或针对每行更改值。

### <a name="change-to-ctp-at-the-order-header-level"></a>在订单标头级别更改 CTP

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

若要更改订单以便在订单标头级别使用 CTP，请按照以下步骤进行操作。

1. 转到 **应收帐款 \> 订单 \> 全部采购订单**。
1. 打开要设置的销售订单或创建新销售订单。
1. 选择 **标头** 以在 **销售订单详细信息** 页面上打开标头信息。
1. 在 **交货** 快速选项卡上，根据您使用的计划引擎，将 **交货日期控制** 字段设置为以下值之一：

    - *CTP* – 使用已弃用的主计划引擎提供的 CTP 计算。 如果您正在使用计划优化，则不允许使用 *CTP* 交货日期控制方法。 因此，如果选择此值，则计算运行时将出错。
    - *用于计划优化的 CTP* - 使用由计划优化提供的 CTP 计算。 如果您正在使用已弃用的主计划引擎，则此设置无效。

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. 选择 **确定** 以应用更改。

### <a name="change-to-ctp-at-the-order-line-level"></a>在订单行级别更改 CTP

如果您使用其他交货日期控制方法创建了订单行，则可以随时更改 CTP。 您在行级别所做的更改不会影响任何其他行。 但是，这可能会导致整个订单交货日期向前或向后移动，具体取决于每个更新的行计算的更改方式。 <!-- KFM: Confirm this intro at next revision -->

若要更改订单以便在行级别使用用于已弃用的主计划引擎的 CTP，请按照以下步骤进行操作。

1. 转到 **应收帐款 \> 订单 \> 全部采购订单**。
1. 打开要设置的销售订单或创建新销售订单。
1. 在 **销售订单详细信息** 页上，在 **销售订单行** 快速选项卡上，选择要设置的销售订单行。
1. 在 **行明细** 快速选项卡上，在 **交货** 选项卡上，根据您使用的计划引擎，将 **交货日期控制** 字段设置为以下值之一：

    - *CTP* – 使用已弃用的主计划引擎提供的 CTP 计算。 如果您正在使用计划优化，则不允许使用 *CTP* 交货日期控制方法。 因此，如果选择此值，则计算运行时将出错。
    - *用于计划优化的 CTP* - 使用由计划优化提供的 CTP 计算。 如果您正在使用已弃用的主计划引擎，则此设置无效。

    此时会显示 **可用的装运日期和接收日期** 对话框，并显示可用的装运日期和接收日期。 如上一节所述，此对话框对订单行的工作方式与对订单标头的工作方式相同。

1. 在操作窗格上，选择 **保存**。
