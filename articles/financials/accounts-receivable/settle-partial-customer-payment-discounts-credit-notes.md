---
title: "结算在贷方通知单上已折扣的部分客户付款"
description: "本文向您介绍当原始发票也具有现金折扣时，在贷方通知单中执行的现金折扣的情况。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5402aa886d7194c4dcfad329aa30eb19bae3bc84
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>结算在贷方通知单上已折扣的部分客户付款

[!include[banner](../includes/banner.md)]


本文向您介绍当原始发票也具有现金折扣时，在贷方通知单中执行的现金折扣的情况。 

Fabrikam 允许客户在部分付款以及贷方通知单上获得现金折扣。 当为客户在其上获得现金折扣的发票签发贷方通知单时，可以在贷方通知单上获得现金折扣。 不是提供贷方用于全部金额，您可以为排除客户获得的现金折扣百分比的金额贷记客户的余额。 结算参数位于**应付账款参数**页上。

## <a name="invoice-and-credit-note"></a>发票和贷方通知单
客户 4035 具有 1.000.00 的发票和 100.00 的贷方通知单。 如果在 14 天内支付，则每个单据具有 1 的折扣。 Arnie 可以在**“客户交易记录”**页上查看该信息。

| 凭证    | 交易记录类型 | 日期      | 开票  | 交易币种借方金额 | 交易币种贷方金额 | 余额  | 货币 |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | 开票          | 6/28/2015 | 10050    | 1,000.00                             |                                       | 1,000.00 | 美元      |
| CCRN-10050 | 贷方通知单      | 6/28/2015 | CR-10050 |                                      | 100.00                                | -100.00  | 美元      |

## <a name="settle-a-credit-note-with-an-invoice"></a>结算使用发票的贷方通知单
从**“客户交易记录”**页上，Arnie 打开**“结算交易记录”**页。 他可以使用 **“结算交易记录”**页来结算发票和贷方通知单。 作为结算流程的一部分，他查看现金折扣日期和金额。 他标记两个单据，然后单击“**过帐**”结算该交易记录。 这里有贷方通知单上的 -1.00 的折扣，因为 Fabrikam 允许贷方通知单上的折扣。

| 标记     | 使用现金折扣 | 凭证    | 帐户 | 日期      | 到期日期  | 开票  | 交易记录币种金额 | 货币 | 要结算的金额 |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| 已选择 | 标准            | FTI-10050  | 4035    | 6/28/2015 | 7/28/2015 | 10050    | 1,000.00                       | 美元      | 990.00           |
| 选定 | 标准            | CCRN-10050 | 4035    | 6/28/2015 | 7/28/2015 | CR-10050 | -100.00                        | 美元      | -99.00           |

折扣信息显示在**“结算交易记录”**页的底部。

|                              |           |
|------------------------------|-----------|
| 现金折扣日期           | 7/12/2015 |
| 现金折扣金额         | -1.00     |
| 使用现金折扣            | 标准    |
| 提取了现金折扣          | 0.00      |
| 要提取的现金折扣金额 | -1.00     |

结算将为 100.00，并将包括 99.00 的付款和 1.00 的折扣。




