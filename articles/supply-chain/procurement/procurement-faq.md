---
title: 采购常见问题解答
description: 本主题提供有关 Supply Chain Management 的采购功能的常见问题 (FAQ) 的解答
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 718108447dcb5cec488b7fa626feb551808e8dd8
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669339"
---
# <a name="procurement-faq"></a>采购常见问题解答

[!include [banner](../includes/banner.md)]

本主题提供有关 Supply Chain Management 的采购功能的常见问题 (FAQ) 的解答。

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>我可以只显示我创建的采购订单吗？

此功能当前不可用。

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>我可以针对采购订单上的已登记库存预留库存和创建交易吗？

### <a name="issue-description"></a>问题描述

即使物料在采购订单上处于 *已登记* 状态，您仍然可以预留库存。 换言之，您可以针对已登记的库存创建交易记录。

### <a name="reproduce-the-issue"></a>重现问题

以下过程显示了一种重现此问题的方法。

1. 创建采购订单。
2. 登记采购订单行。
3. 请注意，您可以针对已登记的库存生成预留或交易。

### <a name="issue-resolution"></a>解决问题

此为有意行为。 预期是已登记的物料已实际到达仓库或库存，因此可以预留。

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>我可以找到取消采购订单的用户吗？

仅当采购订单接受更改管理时，才会跟踪此信息。 如果使用更改管理，您可以查看谁提交了更改（取消）以及谁批准了更改。

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>为什么我无法将采购协议链接到现有采购订单？

创建采购订单时，必须将采购协议与采购订单关联。 否则，采购订单行无法与采购协议行关联。

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>哪项检查会触发“请更新手动输入的价格和折扣或外部单据”消息？

更改装运日期时，您可能会收到一条消息，显示“请更新手动输入的价格和折扣或外部单据”。 您收到此消息的原因是，如果更改了装运日期，其他贸易或销售协议可能会被触发，导致价格更改。 装运日期的更改还会影响仓库计划和其他相关信息。

每当更改日期或另外一些参数都会触发此消息。 此消息的目的是确保您知道由于这些更改，可能发生价格更改。

此消息是贸易协议评估 (TAE) 提示。 有关完整说明，请参阅[贸易协议评估政策](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper)。

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>为什么我无法为有基于类别的物料的采购订单行过帐多个发票？

如果要过帐发票，数量是必填项。 因此，如果仅对一行的全部数量开具了部分金额的发票，您将无法为另一个发票上的其余金额开票。
