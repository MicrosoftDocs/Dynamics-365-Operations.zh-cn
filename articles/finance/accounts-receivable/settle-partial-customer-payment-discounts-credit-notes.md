---
title: 结算在贷方通知单上已折扣的部分客户付款
description: 本文向您介绍当原始发票也具有现金折扣时，在贷方通知单中执行的现金折扣的情况。
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14564
ms.assetid: d9984cef-ddcf-46bd-816d-c01b8cc5cf48
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44f64b9b9cd4fa65d17ba30fb87a688411becd5a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780436"
---
# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a>结算在贷方通知单上已折扣的部分客户付款

[!include [banner](../includes/banner.md)]

本文向您介绍当原始发票也具有现金折扣时，在贷方通知单中执行的现金折扣的情况。 

Fabrikam 允许客户在部分付款以及贷方通知单上获得现金折扣。 当为客户在其上获得现金折扣的发票签发贷方通知单时，可以在贷方通知单上获得现金折扣。 不是提供贷方用于全部金额，您可以为排除客户获得的现金折扣百分比的金额贷记客户的余额。 结算参数位于 **应付帐款参数** 页上。

## <a name="invoice-and-credit-note"></a>发票和贷方通知单
客户 4035 具有 1.000.00 的发票和 100.00 的贷方通知单。 如果在 14 天内支付，则每个单据具有 1 的折扣。 Arnie 可以在 **客户交易记录** 页上查看该信息。

| 凭证    | 交易记录类型 | 日期      | 开票  | 交易币种借方金额 | 交易币种贷方金额 | 平  | 货币 |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| FTI-10050  | 发票          | 2020 年 6 月 28 日 | 10050    | 1,000.00                             |                                       | 1,000.00 | USD      |
| CCRN-10050 | 贷方通知单      | 2020 年 6 月 28 日 | CR-10050 |                                      | 100.00                                | -100.00  | USD      |

## <a name="settle-a-credit-note-with-an-invoice"></a>结算使用发票的贷方通知单
从 **客户交易记录** 页上，Arnie 打开 **结算交易记录** 页。 Arnie 可以使用 **结算交易记录** 页来结算发票和贷方通知单。 作为结算流程的一部分，Arnie 查看现金折扣日期和金额。 Arnie 标记两个单据，然后单击 **过帐** 结算该交易记录。 这里有贷方通知单上的 -1.00 的折扣，因为 Fabrikam 允许贷方通知单上的折扣。

| 标记     | 使用现金折扣 | 凭证    | 帐户 | 日期      | 到期日期  | 开票  | 交易记录币种金额 | 货币 | 要结算的金额 |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| 已选择 | 标准            | FTI-10050  | 4035    | 2020 年 6 月 28 日 | 2020 年 7 月 28 日 | 10050    | 1,000.00                       | USD      | 990.00           |
| 已选择 | 标准            | CCRN-10050 | 4035    | 2020 年 6 月 28 日 | 2020 年 7 月 28 日 | CR-10050 | -100.00                        | USD      | -99.00           |

折扣信息显示在 **结算交易记录** 页的底部。

- **现金折扣日期**：2020 年 7 月 12 日 
- **现金折扣金额**：-1.00     
- **使用现金折扣**：标准    
- **提取的现金折扣**：0.00      
- **要提取的现金折扣金额**：-1.00     

结算将为 100.00，并将包括 99.00 的付款和 1.00 的折扣。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
