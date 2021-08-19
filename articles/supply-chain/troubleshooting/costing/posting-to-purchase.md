---
title: 为零值产品收货过帐了具有零金额的采购应计
description: 过帐具有零值的产品收货时，系统会创建一个金额为 0（零）的采购应计的过帐。
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: LedgerTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 304609e065389d4f56913ae3f2f7fc562de2eadc9f0885ddbe2c8f4747081c66
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722167"
---
# <a name="purchase-accrual-that-has-a-zero-amount-is-posted-for-a-zero-value-product-receipt"></a>为零值产品收货过帐了具有零金额的采购应计

知识库编号：4612588

## <a name="symptoms"></a>故障特征

过帐具有零值的产品收货时，系统会创建一个金额为 0（零）的采购应计的过帐。

## <a name="resolution"></a>解决方法

默认情况下，对于 *采购、应计* 类型的分类帐过帐，子分类帐交易中的 `IsTransferredIndetail` 字段始终设置为 *Summary*。 因此，即使金额为 0（零），系统也会创建相关的凭证条目。

要在金额为 0（零）时跳过此过帐类型，扩展 `subledgerJournalizer.markDoNotTransferEntries` 方法，让它包括 `ledgerPostingType = PurchPckSlpPurchaseOffsetAccount`，如以下示例所示。

```xpp
update_recordset existingSubledgerJournalAccountEntry
setting
    IsTransferredInDetail = TransferPolicy::DoNotTransfer
where existingSubledgerJournalAccountEntry.SubledgerJournalEntry == _subledgerJournalEntryRecId
    && (existingSubledgerJournalAccountEntry.AccountingCurrencyAmount == 0 && existingSubledgerJournalAccountEntry.ReportingCurrencyAmount == 0)
    && existingSubledgerJournalAccountEntry.PostingType == LedgerPostingType::PurchPckSlpPurchaseOffsetAccount;
```
