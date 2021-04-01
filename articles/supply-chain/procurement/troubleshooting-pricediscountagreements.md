---
title: 价格、折扣、协议和返点故障排除
description: 本主题介绍如何解决在使用价格、折扣、协议和返点时可能遇到的问题。
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 5d17f2ec594901404fcd251e463f293258af051c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237147"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a>价格、折扣、协议和返点故障排除

本主题介绍如何解决在使用价格、折扣、协议和返点时可能遇到的问题。

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a>创建采购订单后，我无法将采购协议链接到采购订单行。

创建采购订单时，必须将采购协议与采购订单关联。 否则，采购订单行无法与采购协议行关联。

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>哪项检查会触发“请更新手动输入的价格和折扣或外部单据”消息？

更改装运日期时，您可能会收到一条消息，显示“请更新手动输入的价格和折扣或外部单据”。 您收到此消息的原因是，如果更改了装运日期，其他贸易或销售协议可能会被触发，导致价格更改。 装运日期的更改还会影响仓库计划和其他相关信息。

每当更改日期或另外一些参数都会触发此消息。 此消息的目的是确保您知道由于这些更改，可能发生价格更改。

此消息是贸易协议评估 (TAE) 提示。 有关完整说明，请参阅[贸易协议评估政策](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper)。

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>采购订单收货不包括所有费用。

### <a name="reproduce-the-issue"></a>重现问题

以下过程显示了一种重现此问题的方法。

1. 在 **采购参数** 页上的 **交货** 选项卡上，确保将 **在产品收货时生成费用** 选项设置为 *是*。
1. 创建包含费用的采购订单。
1. 确认采购订单。
1. 接收采购订单。
1. 查看收货总计，并将其与预期总计进行比较。
1. 请注意，并非所有费用都包含在采购订单收货中。

### <a name="issue-resolution"></a>解决问题

解决方法取决于设置杂项费用的方式。 有关如何设置杂项费用以满足您的要求的信息，请参阅以下博客文章：[在产品收货时过帐杂项费用](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/)。

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a>贸易协议价格和折扣不应用于通过数据管理导入的销售或采购订单行。

### <a name="issue-description"></a>问题描述

适用于销售或采购订单行的贸易协议不应用于通过数据管理导入的行。 但是，相同的贸易协议应用于手动创建的销售或采购订单行。

### <a name="reason-for-the-issue"></a>问题原因

如果通过数据管理导入的采购订单行已经包含价格信息，将不会重新评估这些行的贸易协议。 例如，如果 **单行折扣率** 或为某行设置了价格和折扣值，则不会查找该行的贸易协议。

### <a name="issue-workaround"></a>问题解决方法

此行为是预期的，对于销售订单和采购订单是相似的。

解决方法是，导入采购订单行而不设置任何价格信息。 然后将应用贸易协议，并将基于定义的贸易协议更新采购订单行。

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>不会根据发票累计供应商返点。

### <a name="issue-description"></a>问题描述

如果过帐的发票具有不同的截止日期，这些发票不会反映在从它们生成的供应商返点中。

### <a name="issue-resolution"></a>解决问题

根据设计，在计算供应商返点时不考虑截止日期。 考虑自定义系统，以使截止日期和与发票的关系相对于实际的供应商返点更加明显。

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a>采购订单上的单位价格不是基于单位转换来计算的。

### <a name="issue-description"></a>问题描述

在采购订单上更改单位时，不会根据单位转换定义重新计算贸易协议价格。

### <a name="issue-resolution"></a>解决问题

价格始终从贸易协议（或系统中的其他价格设置，如销售协议或物料价格）获取，它们是针对单位设置的。

如果在订单行上更改了单位，系统将为新单位查找价格并应用该价格。 如果未为该单位找到价格，系统不会应用价格。 单位转换不能用于将价格重新计算为另一个单位。 从理论上讲，一盒十个的价格可能不等于一盒价格的十倍。

### <a name="issue-workaround"></a>问题解决方法

解决此问题的一种方法是，确保有您预期的单位的贸易协议将用于物料的订单行。

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a>贸易协议中会发生货币转换问题。

当采购订单上的货币不同时，不会根据货币重新计算贸易协议价格。

*通用货币* 功能可让您仅使用一种货币定义价格和折扣。 然后，您可以根据需要转换为其他货币。 而且，转换完成后，此功能还可以自动应用智能舍入。

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a>当我以行视图模式打开“采购协议”页时，我无法通过在该行的概览中添加“计价单位”字段来个性化该页面。

协议框架中的某些共享字段不能包含在个性化设置中。 由于实现了数据模型，因此会出现此限制。 因此，您无法个性化 **计价单位** 字段。

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a>采购协议的最大限制对采购申请无效。

### <a name="issue-description"></a>问题描述

当采购申请链接到采购协议时，采购协议的最大限制对采购申请无效。 默认价格信息已正确输入，但可以在采购申请中订购超过采购协议最大限制的量。

### <a name="issue-resolution"></a>解决问题

此行为是预期的。 由于采购申请不一定总是得到批准，因此不应在采购协议上保留数量或金额。 因此，您不会达到采购协议的最大限制。

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a>贸易协议可以从拒绝的询价创建。 因此，如果询价行未被接受，系统不会阻止创建贸易协议日记帐。

您可以为询价 (RFQ) 的任何回复创建贸易协议，无论它们是被接受还是被拒绝。 有关详细信息，请参阅[询价 (RFQ) 概述](request-quotations.md)。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]