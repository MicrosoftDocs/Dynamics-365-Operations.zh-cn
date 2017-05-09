---
title: "部分金额的供应商付款"
description: "有时您可以向低于发票金额的供应商付款。 本文介绍处理此情况不同的选项。 可供您使用的选项取决于您的业务要求和配置。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: 4d243e6a9a68b69a6b32748344fc606ff3f2d965
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-payments-for-a-partial-amount"></a>部分金额的供应商付款

[!include[banner](../includes/banner.md)]


有时您可以向低于发票金额的供应商付款。 本文介绍处理此情况不同的选项。 可供您使用的选项取决于您的业务要求和配置。 

<a name="cash-discount-amounts"></a>现金折扣金额
---------------------

供应商可以在到期日期前提供您支付的发票一个现金折扣。 例如，如果发票在 10 天内支付，您输入金额为 100.00 的发票，指定 2% 现金折扣。 到期期限为 30 天。 如果付款方案使用现金折扣作为选择发票的条件，并且，如果该方案在现金折扣日期或之前运行，为付款选择发票，付款创建为 98.00。 现金折扣还可以为手动创建的一次性付款获取。

## <a name="partial-payments-with-cash-discounts"></a>使用现金折扣的部分付款
在进行部分付款时，您可以计划进行部分付款以完全结算发票。 要为部分付款获取现金折扣，则必须设置**应付帐款参数**页上的 **计算部分付款的现金折扣** 选项为**是**。 

例如，如果发票在发出的 10 天内付款，您收到 2% 的现金折扣。 100.00 的发票已过帐。 如果您在 10 天内付款 49.00，则在付款日志中将输入借出 49.00。 在您在**结算未结交易记录**页面上结算部分付款时，**1.00** 将出现在**要提取的现金折扣金额**字段中。 

> [!NOTE] 
> 如果您输入部分付款并在**要结算的金额**字段中保留完整的发票金额，则在您过帐交易记录时，**要提取的现金折扣金额**字段将自动重新计算。

## <a name="credit-notes-with-cash-discounts"></a>使用现金折扣的贷方通知单
您可能要退回某些发票上的物料，并且接收贷方通知单。 如果现金折扣已在原始发票上执行，则可以减去折扣的值和接收退回的正确金额。 如果**应付帐款参数**页上的 **计算贷方通知单的现金折扣** 选项设置为**是**，则将自动计算贷方通知单的折扣。 

例如，如果发票在发出的 10 天内付款，您收到 2% 的现金折扣。 100.00 的发票已过帐。 如果您要退回货物，并且您接受贷方通知单，您可以为原始发票的全部金额 100.00 输入贷方通知单，以及同样在贷项通知单上定义的 2% 现金折扣。  当您在**结算交易记录**页面上查看贷方通知单时，**98.00** 将出现在**要结算的金额**字段中，并且 **-2.00** 将出现在**现金折扣金额**字段中。 折扣金额过帐到现金折扣帐户。

## <a name="overpaymentunderpayment-amounts"></a>超额支付/支付不足金额
仍必须结算的金额非常小时，您可以进行部分付款。 例如，供应商发票为 1,000.00，您 支付 999.90。 如果余额少于为**应付帐款参数**页的超额支付或支付不足指定的金额，差额将自动过帐到超额支付/支付不足会计科目。




