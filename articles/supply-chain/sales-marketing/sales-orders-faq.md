---
title: 有关销售订单的常见问题
description: 此页解答在 Dynamics 365 Supply Chain Management 中处理销售订单时遇到的常见问题。
author: Henrikan
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cee75b1d740e7cb414c674157dde0146e8faa50
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571609"
---
# <a name="sales-order-faqs"></a>销售订单常见问题解答

此页解答在 Dynamics 365 Supply Chain Management 中处理销售订单时遇到的常见问题。

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>我可以将采购订单链接到销售订单以满足需求吗？

您可以从销售订单创建采购订单。 有关详细信息，请参阅[基于销售订单创建采购订单](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order)。

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>是否不能取消或删除销售订单或退货单？

您只能取消处于 *已创建* 状态的销售订单和退货单。 有关详细信息，请参阅[取消退货单](/dynamics365/supply-chain/service-management/cancel-return-order)。

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>我可以恢复删除的已开票销售订单吗？

如果开票的销售订单被误删除，您可以恢复它或查看它的详细信息。

转到 **客户帐户 \> 交易记录 \> 原始单据 \> 查看详细信息**。 找到您要查找的发票，然后选择它查看详细信息。 这些详细信息包括销售订单引用。 您还应该能够从该页面访问销售订单详细信息。

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>如何删除孤立的销售订单记录？

要清除孤立的销售订单记录，请转到以下任一位置运行 *销售订单删除* 定期作业：

- 销售和市场营销 \> 定期任务 \> 清除 \> 删除销售订单
- 零售和商业 \> 零售和商业 IT \> 清除 \> 删除销售订单

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>是否有方法可以计算已经过帐的发票上的佣金？

Supply Chain Management 当前不支持已过帐发票的佣金计算。
