---
title: 获取比供应商付款的计算折扣更多的折扣
description: 本主题向您展示为超过发票上最初可用折扣的金额执行现金折扣的情况。 如果组织履行协议，供应商支付发票上的较小金额，可能发生此情况。
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd8fd2fcbc56a91c0bcabfd2fc51e9ff62fe3994
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716627"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>获取比供应商付款的计算折扣更多的折扣

[!include [banner](../includes/banner.md)]

本主题向您展示为超过发票上最初可用折扣的金额执行现金折扣的情况。 如果组织履行协议，供应商支付发票上的较小金额，可能发生此情况。 

如果七天内支付发票，供应商 3051 将给予 Fabrikam 4% 的现金折扣。 April 在 6 月 29 日为发票输入 1,000.00。 供应商让 April 执行对此发票可用的 60.00 的折扣，而不是默认折扣 40.00。 通过使用应付帐款付款日记帐，April 记录一次性付款。 她为付款输入供应商，然后打开 **结算交易记录** 页。 她标记发票并在 **现金折扣金额** 字段中将值更改为 **60.00**。

| 标记     | 使用现金折扣 | 凭证   | 帐户 | 日期      | 到期日期  | 开票 | 交易记录币种金额 | 货币 | 要结算的金额 |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| 已选择 | 标准            | Inv-10040 | 3051    | 6/29/2015 | 7/29/2015 | 10040   | 1,000.00                       | 美元      | 940.00           |

折扣信息显示在 **结算交易记录** 页的底部。

| 字段                        | 值     |
|------------------------------|-----------|
| 现金折扣日期           | 7/12/2015 |
| 现金折扣金额         | 60.00     |
| 使用现金折扣            | 标准    |
| 提取了现金折扣          | 0.00      |
| 要提取的现金折扣金额 | 60.00     |

April 过帐付款日志。 使用付款 940.00 和 60.00 折扣完全结算发票。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
