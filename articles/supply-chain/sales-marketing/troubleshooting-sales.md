---
title: 销售订单故障排除
description: 本主题介绍如何解决在使用销售订单时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c9a5b7a5e8cac7f8816233dd2d7ff1a7f84ea480
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974777"
---
# <a name="troubleshoot-sales-orders"></a>销售订单故障排除

本主题介绍如何解决在使用销售订单时可能遇到的问题。

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>如果更改销售订单标题上的位置，税务信息不会更新。

### <a name="issue-description"></a>问题描述

如果在销售订单标题或行级别更改了站点、仓库或交货地址，不会自动更新行的案例税务信息。

### <a name="issue-resolution"></a>解决问题

此为有意行为。 发生此问题是因为交货地址、站点和仓库也未在生级别自动更改。 您必须手动更新它们。

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>如果在同一期间或重叠期间有两个贸易协议，将始终选择同一协议行。

### <a name="issue-description"></a>问题描述

如果为同一期间或重叠期间定义了两个贸易协议，每次创建包含这些物料的销售订单行时，似乎会选择同一个贸易协议。

### <a name="issue-resolution"></a>解决问题

如果给定日期有多个贸易协议，将始终选择价格最低的贸易协议。 有关详细信息，请下载以下白皮书：[Microsoft Dynamics AX 2012 中的贸易协议](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90)。

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>我可以将采购订单链接到销售订单以满足需求吗？

您可以从销售订单创建采购订单。 有关详细信息，请参阅[基于销售订单创建采购订单](tasks/create-purchase-order-sales-order.md)。

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>我无法取消或删除退货单或销售订单。

您只能取消处于 *已创建* 状态的销售订单和退货单。 有关详细信息，请参阅[取消退货单](../service-management/cancel-return-order.md)。

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>当我尝试取消销售订单时，我收到“已创建了依赖预留的工作，因此无法删除这些预留”错误。

错误代码：WAX4661

如果工作与销售订单相关联，在取消和冲销工作之前，您不能取消销售订单。 即使与销售订单关联的工作已关闭，此要求也适用。

若要解决此问题，请按照以下步骤操作。

1. 取消工作，然后将库存放回所需的位置。 转到销售订单的相关负荷，然后在负荷行上选择 **减少领料数量** 或在操作窗格上选择 **冲销工作**。

    现在，工作的状态为 *已取消*，并且已自动创建和处理新的库存变动工作，以在冲销时将库存放回到所述位置。

2. 删除负荷。 装运也会被删除。
3. 您现在应该能够转到销售订单并取消订单。

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>我无法取消链接到销售订单的内部公司采购订单。

### <a name="issue-description"></a>问题描述

如果您尝试取消链接到销售订单的内部公司采购订单，您可能会收到以下错误消息：“数量无法减少，因为剩余的更新数量会更改符号。”

### <a name="issue-resolution"></a>解决问题

此问题已在 Microsoft Dynamics 365 Supply Chain Management 版本 10.0.13 中修复。 在该版本和更高版本中，您现在可以取消链接到销售订单的内部公司采购订单。

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>我可以恢复删除的已开票销售订单吗？

### <a name="issue-description"></a>问题描述

开票的销售订单被误删除，您想要恢复它或查看它的详细信息。

### <a name="issue-resolution"></a>解决问题

如果删除的销售订单已开票，请转到 **客户帐户 \> 交易记录 \> 原始单据 \> 查看详细信息**。 找到您要查找的发票，然后选择它查看详细信息。 这些详细信息包括销售订单引用。 您还应该能够从该页面访问销售订单详细信息。

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>在 SalesOrderHeaderV2Entity 数据实体中找不到销售订单标题的截止日期。

截止日期字段不在 *SalesOrderHeaderV2Entity* 实体中。

## <a name="i-must-delete-orphaned-sales-order-records"></a>我必须删除孤立的销售订单记录。

要清除孤立的销售订单记录，请转到以下任一位置运行 *销售订单删除* 定期作业：

- 销售和市场营销 \> 定期任务 \> 清除 \> 删除销售订单
- 零售和商业 \> 零售和商业 IT \> 清除 \> 删除销售订单

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>是否有方法可以计算已经过帐的发票上的佣金？

Supply Chain Management 当前不支持已过帐发票的佣金计算。

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>内部公司流程不支持捆绑物料。

捆绑物料不能用于采购订单，因为如果检查捆绑物料的销售订单行，您会注意到数量为 *0*（零），状态为 *已取消*。 此为有意行为。 销售订单仅购买捆绑物料的组件。 不购买捆绑物料本身。

如果必须购买捆绑，请考虑是否必须将其标记为捆绑物料，因为此功能是为收入确认场景设计的。 有关捆绑物料的详细信息，请参阅[捆绑销售](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles)。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]