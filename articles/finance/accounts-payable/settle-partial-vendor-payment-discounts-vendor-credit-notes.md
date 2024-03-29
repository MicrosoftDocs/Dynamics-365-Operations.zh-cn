---
title: 结算在贷方通知单上已折扣的部分供应商付款
description: 本文向您介绍根据发票结算贷项通知单的情况。
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
ms.openlocfilehash: b926d94059fb12b143b9c9b4b5c04cb7f39f8e99
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715929"
---
# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-credit-notes"></a>结算在贷方通知单上已折扣的部分供应商付款

[!include [banner](../includes/banner.md)]

本文向您介绍根据发票结算贷项通知单的情况。

Fabrikam 的供应商指定在贷方通知单的现金折扣。 如果 14 天内支付发票，供应商 3050 将给予 Fabrikam 1% 的现金折扣。

## <a name="invoice-and-credit-memo"></a>发票和贷项通知单
6 月 29 日，April 为供应商 3050 创建 1,000.00 的发票。 7 月 2 日，她为 200.00 创建贷方通知单。 从 **供应商** 页上，April 打开了 **结算交易记录** 页。 她可以使用 **结算交易记录** 页来标记贷方通知单和结算的发票。 在贷方通知单中计算 2.00 的折扣。 因此，贷方通知单的总值减为 198.00。

| 标记                     | 使用现金折扣 | 凭证   | 帐户 | 日期      | 到期日期  | 开票 | 交易记录币种金额 | 货币 | 要结算的金额 |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 已选择                 | 标准            | Inv-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070   | -1,000.00                      | 美元      | -990.00          |
| 已选择和突出显示 | 标准            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 |         | 200.00                         | 美元      | 198.00           |

贷方通知单的折扣信息显示在 **结算未结交易记录** 页的底部。

| 字段                        | 值     |
|------------------------------|-----------|
| 现金折扣日期           | 2015 年 7 月 13 日 |
| 现金折扣金额         | 2.00      |
| 使用现金折扣            | 标准    |
| 提取了现金折扣          | 0.00      |
| 要提取的现金折扣金额 | 2.00      |

April 单击了 **过帐**。 然后，她查看已完成的结算。 April 看到应用了 198.00 的贷方通知单，并执行了 2.00 的折扣。 因此，总计为 200.00。

| 标记                     | 使用现金折扣 | 凭证   | 帐户 | 日期      | 到期日期  | 开票  | 交易记录币种金额 | 货币 | 要结算的金额 |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| 已选择和突出显示 | 标准            | Inv-10070 | 3050    | 6/29/2015 | 7/29/2015 | 10070    | -1,000.00                      | 美元      | -200.00          |
| 选定                 | 标准            | CR-10070  | 3050    | 7/2/2015  | 7/29/2015 | CR-10070 | 200.00                         | 美元      | 198.00           |

April 可以通过选择 **所有供应商** 页上的供应商来查看 **供应商交易记录** 页上的供应商交易记录，然后在操作窗格上单击 **交易记录**。 在此页上，April 看到该发票具有 -800.00 的余额。 她还看到 198.00 的贷方通知单和 2.00 的折扣。

| 凭证    | 交易记录类型 | 日期      | 开票 | 交易币种借方金额 | 交易币种贷方金额 | 余额 | 货币 |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Inv-10070  | 开票          | 6/29/2015 | 10070   |                                      | 1,000.00                              | -800.00 | 美元      |
| Inv-10071  |                  | 7/2/2015  | CR10071 | 200.00                               |                                       | 0.00    | 美元      |
| DISC-10071 |  现金折扣   | 7/2/2015  |         | 2.00                                 |                                       | 0.00    | 美元      |
| DISC-10071 |  现金折扣   | 7/2/2015  |         |                                      | 2.00                                  | 0.00    | 美元      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
