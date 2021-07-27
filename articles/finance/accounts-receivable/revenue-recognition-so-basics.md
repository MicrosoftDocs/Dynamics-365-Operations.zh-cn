---
title: 销售订单上的收入确认
description: 本主题介绍在销售订单和发票上确认收入的基本功能。 收入确认在销售订单和从销售订单创建的对应发票上可用。
author: kweekley
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: ce0879565babfbf526e1aa6864482e60cbabd377
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2021
ms.locfileid: "6345588"
---
# <a name="revenue-recognition-on-sales-orders"></a>销售订单上的收入确认

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 收入确认功能不能通过功能管理来启用。 目前，您必须使用 Configuration Key 启用该功能。

本主题介绍在销售订单和发票上确认收入的基本功能。 收入确认在销售订单和从销售订单创建的对应发票上可用。 销售订单也可通过时间和材料项目创建。

> [!NOTE]
> 在本主题的示意图中，列已隐藏或添加到网格，以便更好地说明概念。 因此，示意图中的页面和数据可能不同于您在产品中所看到的。

## <a name="enter-a-sales-order"></a>输入销售订单

输入了以下销售订单并且其包括为收入确认设置的三个物料。

[![输入销售订单。](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

收入确认有两个概念：

- **确定收入价格。** 收入价格基于已发布产品的设置进行计算。 收入价格不会对客户显示，仅用于销售订单发票的会计核算。 作为销售一部分打印的销售订单行和文档仍然显示单价/标价。
- **确定应进行收入确认的时间。** 收入计划用于确定应确认收入的时间。

    在此示例中，第一个物料 S0001 分配给了 **1O**（发生一次）收入计划。 此行表示里程碑类型方案，即将在未来进行安装之后确认收入的情况。 因此，收入将延期，直至安装完成。

    第二个物料 S0008 是设置为过帐合同支持 (PCS) 物料的服务物料。 在 12 个月的期间中为客户提供了持续的工程服务。 因此，为产品默认分配了 **12M** 收入计划。 由于该物料是 PCS 物料，必须定义合同开始日期和结束日期。 默认情况下，合同开始日期和结束日期可在“物料详细信息 - 设置”选项卡中找到。在收入计划中，定义了 **12M** 的设置，以便自动填写合同条款，如下图所示。

    [![收入计划。](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    第三个物料 S0012 是硬件，默认情况下未分配收入计划。 硬件的收入在对物料开票时确认。

## <a name="confirm-the-sales-order"></a>确认销售订单

若要查看有关收入价格和收入计划的其他详细信息，请使用销售订单操作窗格的 **管理** 选项卡的 **收入确认** 组中的按钮。 由于此时未确认销售订单，用于收入确认的按钮不可用。 随着销售订单进展到履行的各个阶段，这些按钮将变得可用或不可用。

[![销售订单头。](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

前三个按钮提供用于收入确认的销售订单设置中有关物料收入价格的详细信息。

- **收入价格分配** - 在确认销售订单或过帐发票之后，此按钮将变得可用。 销售订单确认和发票过帐都将计算收入，以确认将在会计条目中确认或延期的价格。 根据该设置，计算出的收入价格可能不同于对客户显示的单位价格。
- **使用新订单行重新分配价格** - 在确认销售订单或过帐发票之后，此按钮将变得可用。 开票后将新行添加到当前销售订单或添加到新销售订单之后，重新分配过程用于重新计算必须确认的收入。 在这两种方案中，添加新物料都会导致合同发生变化。 因此，必须重新分配收入价格。
- **更新收入价格分配** - 确认销售订单之后，此按钮将变得可用，但在对销售订单开票之后，它将变得不可用。 该更新用于重新运行收入价格分配，而无需确认销售订单。 在对销售订单开票后，无法重新计算收入价格。

后两个按钮提供具有收入计划的销售订单中有关这些物料的收入计划的详细信息。

- **预期的收入确认计划** - 确认销售订单之后，此按钮将变得可用，但在对销售订单开票之后，它将变得不可用。 将打开显示预期收入计划的页面。 最终计划可能会发生变化，因为预期计划使用要求装运日期，而最终计划使用实际的装运日期。
- **收入确认计划** - 在对销售订单开票之后，此按钮将变得可用。 进行确认或创建装箱单时，将不会创建最终收入确认计划。 仅当对销售订单开票时才会创建。

在以下示例中，确认销售订单时进行了收入价格分配。 请注意，即使以不同的方式分配了收入价格，**要确认的收入** 字段中的金额总计必须等于对客户开票的销售订单行的总和。 例如，销售订单行的总和除税后为 1,499 美元。 因此，**要确认的收入** 值的总和也必须为 1,499 美元。

[![收入价格分配。](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

此外，还将创建预期的收入确认计划。 收入计划使用 **要确认的收入** 值作为要延期的金额。 物料 S0001 延期 321.21 美元而不是 300 美元，物料 S0008 延期 160.61 美元而不是 100 美元。 物料 S0012 未显示在预期计划中，因为延期了收入。 进行过帐时，物料 S0012 将 1,017.18 美元直接过帐到收入会计科目。

[![预期的收入确认计划。](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>创建装箱单

接下来，可以为销售订单创建装箱单。 过帐装箱单时，不会确认收入。 如果未确认销售订单，则对装箱单过帐不会触发收入价格计算。 此外，也不会触发对预期或最终收入确认计划的创建。 如果物料模型组设置为在装箱单上延期收入，则将继续使用当前过帐模板会计科目而不是发票过帐中使用的新延期收入科目来进行过帐。

## <a name="create-the-invoice"></a>创建发票

最后一步是对销售订单开票。 如果查看发票的凭证，您会注意到物料 S0001 和 S0008 的收入已延期 ($321.21 + 160.61 = 481.82)，并且物料 S0012 的剩余金额已过帐到收入 (1,017.18)。 这些值之和为 1,499 美元，与销售订单行的总和一致。

[![凭证交易记录。](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

创建发票之后，用于收入确认的 **收入价格分配**、**使用新订单行重新分配价格** 和 **收入确认计划** 按钮将变得可用，但 **更新收入价格分配** 和 **预期收入确认计划** 按钮不可用。

[![可用收入确认按钮可用性。](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

**收入价格分配** 按钮仍然可用，以便您可以查看收入价格计算。 如果销售订单在确认之后未进行任何更改，则对发票过帐不会更改 **要确认的收入** 字段中的已计算金额。

预期收入确认计划将被移除并替换为最终收入确认计划。 每个销售订单行的收入计划详细信息均会得到保持，并会用于在履行合同义务的同时将延迟收入发布到实际收入中。

[![最终收入确认计划。](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]