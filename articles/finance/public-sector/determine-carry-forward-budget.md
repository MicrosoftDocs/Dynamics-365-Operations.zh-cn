---
title: 在采购订单和发票减少后更新结转预算
description: 本文描述了在取消或减少采购订单以及减少发票时如何控制结转预算的情况。
author: TaylorVH
ms.date: 02/11/2022
ms.topic: article
ms.search.form: LedgerFund
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-savanh
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2022-02-01
ms.openlocfilehash: 7f0ef0ffdf697609e811f754b4378b1f7a81c494
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897949"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>在采购订单和发票减少后更新结转预算

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

本文描述了在取消或减少采购订单以及减少发票时如何控制结转预算的情况。

有关如何在年终处理采购订单的信息，请参阅[在年终处理采购订单](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)。

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>打开或关闭发票差异的结转预算减少

当采购订单被取消或减少时，系统总是可以更新结转预算。 但是，如果您想在发票减少时更新结转预算，您必须打开 *当采购订单发票因差异而减小时缩减结转预算* 功能。 管理员可以通过在 **[功能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** 工作区搜索此功能来打开或关闭此功能。

## <a name="purchase-order-reductions-and-cancellations"></a>采购订单缩减和取消

无论是否开启了 *当采购订单发票因差异而减小时缩减结转预算* 功能，当合格采购订单被取消或减少时，结转预算都将更新。 您可以设置每个总帐资金以按以下方式之一进行响应：

- 保留创建时的结转预算。
- 自动调整结转预算以删除取消或减少的金额。

只有具有包含资金的分配的采购订单行可用于自动预算调整。 完成采购订单或确认采购订单减少时，会发生自动预算调整。

## <a name="invoice-reductions"></a>发票缩减

如果开启了 *当采购订单发票因差异而减小时缩减结转预算* 功能，您可以指定每笔资金在发票减少时是否应减少结转预算，以及何时减少或取消采购订单。 发票必须针对具有结转预算的采购订单。 减少包括价格差异、费用差异和税收差异。 在开票期间减少结转采购订单时，会产生差异。 过帐发票时，采购订单保留款将减去差异金额。 该功能还将为差异金额创建自动预算调整。

如果您关闭了 *当采购订单发票因差异而减小时缩减结转预算* 功能，则在这种情况下不会减少结转预算。 因此，会留下差异金额的剩余结转预算。

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>为每笔资金配置结转预算选项

当采购订单或发票减少时，对应该能够减少结转预算的每个总帐资金执行这些步骤。

1. 转到 **总帐 \> 会计科目表 \> 资金 \> 资金**。
1. 选择要设置的资金。
1. 在 **采购订单年终流程** 下面，确保 **覆盖所选的年终选项** 选项设置为 *是*。
1. 在 **结转预算状态** 下面，根据需要设置 **当取消或减少结转采购订单时复征预算** 字段。 这些设置的效果略有不同，具体取决于您的系统中是否启用了 *当采购订单发票因差异而减小时缩减结转预算* 功能。

    - 当该功能关闭时，系统仅对取消或减少的采购订单作出反应。 选项设置按以下方式工作：

        - *否* - 系统为已取消或减少的采购订单的余额创建预算登记分录。
        - *是* - 系统允许取消或减少采购订单，但不创建预算登记分录。 结转预算仍可供其他单据使用。

    - 启用该功能后，系统会同时对发票差异以及取消或减少的采购订单作出反应。 选项设置按以下方式工作：

        - *否* - 对于发票差异，系统会根据采购订单为差异减少金额创建预算登记分录。 对于取消或减少的采购订单，此设置与关闭该功能时的效果相同。
        - *是* - 对于发票差异，系统允许减少发票，但不创建预算登记分录。 结转预算仍可供其他单据使用。 对于取消或减少的采购订单，此设置与关闭该功能时的效果相同。

## <a name="additional-resources"></a>其他资源

- [在年底处理采购订单](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [维护常规预算预留](general-budget-reservation-tasks.md)
- [公共部门中的资金](funds-public-sector.md)
- [设置公共部门中的资金](tasks/set-up-fund-public-sector.md)
