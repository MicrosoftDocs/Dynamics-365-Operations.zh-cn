---
title: 应付帐款的集中付款
description: 包括多个法人的组织可以使用处理所有付款的单个法人创建和管理付款。 因此，不必在多个法人中输入同一付款。 本文提供显示集中付款过帐如何在不同环境中处理的示例。
author: abruer
manager: AnnBe
ms.date: 02/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a8ec6fa1515b179b0cf1df034d8217b926cc5a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003545"
---
# <a name="centralized-payments-for-accounts-payable"></a>应付帐款的集中付款

[!include [banner](../includes/banner.md)]

包括多个法人的组织可以使用处理所有付款的单个法人创建和管理付款。 因此，不必在多个法人中输入同一付款。 本文提供显示集中付款过帐如何在不同环境中处理的示例。

包括多个法人的组织可以使用处理所有付款的法人创建和管理付款。 因此，不必在多个法人中输入同一付款。 此外，组织节省时间，因为付款流程简化。

在集中付款的组织中，有很多营业的法人，且每个营业的法人都管理自己的供应商发票。 所有营业的法人的付款都是从称作付款的法人的单个法人中生成的。 在结算流程中，生成适用的应付和应收交易记录。 您可以指定组织内的哪个法人接收已有收益或已有损失交易记录，以及如何处理与跨公司付款相关的现金折扣交易记录。 在集中支付日记帐行中，**科目类型** 应设置为“供应商”。 **对方科目类型** 应设置为“银行”或“分类帐”。 银行科目应在当前公司中。 

以下示例说明如何在不同的环境中处理过帐。 假定所有这些示例都采用以下配置：

-   法人分别为 Fabrikam、Fabrikam East 和 Fabrikam West。 从 Fabrikam 进行付款。
-   **内部公司** 页上的 **过帐现金折扣** 字段设置为 **发票法人**。
-   **内部公司** 页上的 **过帐币种汇兑损益** 字段设置为 **付款法人**。
-   客户 Fourth Coffee 在每个法人中设置为一个供应商。 来自不同法人的供应商被标识为同一供应商，因为他们共享相同的全球通讯簿 ID。

| 名录 ID | 供应商帐户 | 姓名          | 法人  |
|--------------|----------------|---------------|---------------|
| 1050         | 3004           | Fourth Coffee | Fabrikam      |
| 1050         | 100            | Fourth Coffee | Fabrikam East |
| 1050         | 3004           | Fourth Coffee | Fabrikam West |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a>示例 1：来自其他法人的发票的供应商付款
Fabrikam East 为供应商帐户 100 (Fourth Coffee) 具有一个未结发票。 Fabrikam 输入付款并将付款过帐到 Fabrikam 供应商帐户 3004 (Fourth Coffee)。 该付款用该未结发票结算。

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a>在 Fabrikam East 中为供应商 100 过帐发票

| 科目                          | 借方金额 | 贷方金额 |
|----------------------------------|--------------|---------------|
| 支出 (Fabrikam East)          | 600.00       |               |
| 应付帐款 (Fabrikam East) |              | 600.00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>在 Fabrikam 中为供应商 3004 生成和过帐付款

| 科目                     | 借方金额 | 贷方金额 |
|-----------------------------|--------------|---------------|
| 应付帐款 (Fabrikam) | 600.00       |               |
| 现金 (Fabrikam)             |              | 600.00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam 付款用 Fabrikam East 发票结算

**Fabrikam 过帐**

| 科目                           | 借方金额 | 贷方金额 |
|-----------------------------------|--------------|---------------|
| 从 Fabrikam East (Fabrikam) 的应收金额 | 600.00       |               |
| 应付帐款 (Fabrikam)       |              | 600.00        |

**Fabrikam East 过帐**

| 科目                          | 借方金额 | 贷方金额 |
|----------------------------------|--------------|---------------|
| 应付帐款 (Fabrikam East) | 600.00       |               |
| 向 Fabrikam (Fabrikam East) 的应付金额  |              | 600.00        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>示例 2：来自具有现金折扣的其他法人的发票的供应商付款
Fabrikam East 为供应商 100 (Fourth Coffee) 具有一个未结发票。 该发票具有 20.00 的可用现金折扣。 Fabrikam 为 Fabrikam 供应商 3004 (Fourth Coffee) 输入并过帐了 580.00 的付款。 该付款用未结 Fabrikam East 发票结算。 该现金折扣过帐到发票法人 Fabrikam East。

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>在 Fabrikam East 中为 Fabrikam East 供应商 100 过帐发票

| 科目                          | 借方金额 | 贷方金额 |
|----------------------------------|--------------|---------------|
| 支出 (Fabrikam East)          | 600.00       |               |
| 应付帐款 (Fabrikam East) |              | 600.00        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>在 Fabrikam 中为 Fabrikam 供应商 3004 生成和过帐付款

| 科目                     | 借方金额 | 贷方金额 |
|-----------------------------|--------------|---------------|
| 应付帐款 (Fabrikam) | 580.00       |               |
| 现金 (Fabrikam)             |              | 580.00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam 付款用 Fabrikam East 发票结算

**Fabrikam 过帐**

| 科目                           | 借方金额 | 贷方金额 |
|-----------------------------------|--------------|---------------|
| 从 Fabrikam East (Fabrikam) 的应收金额 | 580.00       |               |
| 应付帐款 (Fabrikam)       |              | 580.00        |

**Fabrikam East 过帐**

| 科目                          | 借方金额 | 贷方金额 |
|----------------------------------|--------------|---------------|
| 应付帐款 (Fabrikam East) | 580.00       |               |
| 向 Fabrikam (Fabrikam East) 的应付金额  |              | 580.00        |
| 应付帐款 (Fabrikam East) | 20.00        |               |
| 现金折扣 (Fabrikam East)    |              | 20.00         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a>示例 3：来自具有已有汇率损失的其他法人的发票的供应商付款
Fabrikam East 为供应商 100 (Fourth Coffee) 具有一个未结发票。 Fabrikam 输入并过帐 Fabrikam 供应商 3004 (Fourth Coffee) 的付款。 该付款用未结 Fabrikam East 发票结算。 在结算过程中将生成币种汇率损失交易记录。

-   在发票日期的欧元 (EUR) 到美元 (USD) 的汇率：1.2062
-   在付款日期的欧元到美元的汇率：1.2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a>在 Fabrikam East 中为 Fabrikam East 供应商 100 过帐发票

| 科目                          | 借方金额            | 贷方金额           |
|----------------------------------|-------------------------|-------------------------|
| 支出 (Fabrikam East)          | 600.00 EUR / 723.72 USD |                         |
| 应付帐款 (Fabrikam East) |                         | 600.00 EUR / 723.72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a>在 Fabrikam 中为 Fabrikam 供应商 3004 生成和过帐付款

| 科目                     | 借方金额            | 贷方金额           |
|-----------------------------|-------------------------|-------------------------|
| 应付帐款 (Fabrikam) | 600.00 EUR / 736.62 USD |                         |
| 现金 (Fabrikam)             |                         | 600.00 EUR / 736.62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam 付款用 Fabrikam East 发票结算

**Fabrikam 过帐**

| 科目                           | 借方金额            | 贷方金额           |
|-----------------------------------|-------------------------|-------------------------|
| 从 Fabrikam East (Fabrikam) 的应收金额 | 600.00 EUR / 736.62 USD |                         |
| 应付帐款 (Fabrikam)       |                         | 600.00 EUR / 736.62 USD |
| 已有损失 (Fabrikam)          | 0.00 EUR / 12.90 USD    |                         |
| 从 Fabrikam East (Fabrikam) 的应收金额 |                         | 0.00 EUR / 12.90 USD    |

**Fabrikam East 过帐**

| 科目                          | 借方金额            | 贷方金额           |
|----------------------------------|-------------------------|-------------------------|
| 应付帐款 (Fabrikam East) | 600.00 EUR / 736.62 USD |                         |
| 向 Fabrikam (Fabrikam East) 的应付金额  |                         | 600.00 EUR / 736.62 USD |
| 向 Fabrikam (Fabrikam East) 的应付金额  | 0.00 EUR / 12.90 USD    |                         |
| 应付帐款 (Fabrikam East) |                         | 0.00 EUR / 12.90 USD    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a>示例 4：来自具有现金折扣和已有汇率损失的其他法人的发票的供应商付款
Fabrikam East 为供应商 100 (Fourth Coffee) 具有一个未结发票。 该发票具有可用的现金折扣并且生成增值税交易记录。 Fabrikam 过帐 Fabrikam 供应商 3004 (Fourth Coffee) 的付款。 该付款用未结 Fabrikam East 发票结算。 在结算过程中将生成币种汇率损失交易记录。 现金折扣过帐到发票法人 (Fabrikam East)，且币种汇率损失过帐到付款法人 (Fabrikam)。

-   在发票日期的欧元到美元的汇率：1.2062
-   在付款日期的欧元到美元的汇率：1.2277

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a>过帐发票，并且在 Fabrikam East 中为供应商 100 生成纳税交易记录

| 科目                          | 借方金额            | 贷方金额           |
|----------------------------------|-------------------------|-------------------------|
| 支出 (Fabrikam East)          | 564.07 EUR / 680.38 USD |                         |
| 增值税 (Fabrikam East)        | 35.93 EUR / 43.34 USD   |                         |
| 应付帐款 (Fabrikam East) |                         | 600.00 EUR / 723.72 USD |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a>在 Fabrikam 中为供应商 3004 生成和过帐付款

| 科目                     | 借方金额            | 贷方金额           |
|-----------------------------|-------------------------|-------------------------|
| 应付帐款 (Fabrikam) | 588.72 EUR / 722.77 USD |                         |
| 现金 (Fabrikam East)        |                         | 588.72 EUR / 722.77 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam 付款用 Fabrikam East 发票结算

**Fabrikam 过帐**

| 科目                           | 借方金额            | 贷方金额           |
|-----------------------------------|-------------------------|-------------------------|
| 从 Fabrikam East (Fabrikam) 的应收金额 | 588.72 EUR / 722.77 USD |                         |
| 应付帐款 (Fabrikam)       |                         | 588.72 EUR / 722.77 USD |
| 已有损失 (Fabrikam)          | 0.00 EUR / 12.66 USD    |                         |
| 从 Fabrikam East (Fabrikam) 的应收金额 |                         | 0.00 EUR / 12.66 USD    |

**Fabrikam East 过帐**

| 科目                          | 借方金额            | 贷方金额           |
|----------------------------------|-------------------------|-------------------------|
| 应付帐款 (Fabrikam East) | 588.72 EUR / 722.77 USD |                         |
| 向 Fabrikam (Fabrikam East) 的应付金额  |                         | 588.72 EUR / 722.77 USD |
| 向 Fabrikam (Fabrikam East) 的应付金额   | 0.00 EUR / 12.66 USD    |                         |
| 应付帐款 (Fabrikam East) |                         | 0.00 EUR / 12.66 USD    |
| 应付帐款 (Fabrikam East) | 11.28 EUR / 13.61 USD   |                         |
| 现金折扣 (Fabrikam East)    |                         | 11.28 EUR / 13.61 USD   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a>示例 5：具有主付款的供应商贷方通知单
Fabrikam 为供应商 3004 (Fourth Coffee) 生成 75.00 的付款。 该付款用针对 Fabrikam West 供应商 3004 的未结发票和针对 Fabrikam East 供应商 100 的未结贷方通知单结算。 该付款在 **未结交易记录编辑** 页中选择为主付款。

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>发票为供应商 3004 过帐到 Fabrikam West

| 帐户                          | 借方金额 | 贷方金额 |
|----------------------------------|--------------|---------------|
| 支出 (Fabrikam West)          | 100.00       |               |
| 应付帐款 (Fabrikam West) |              | 100.00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>贷方通知单为供应商 100 过帐到 Fabrikam East

| 科目                          | 借方金额 | 贷方金额 |
|----------------------------------|--------------|---------------|
| 应付帐款 (Fabrikam East) | 25.00        |               |
| 采购退货 (Fabrikam East) |              | 25.00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>付款为供应商 3004 过帐到 Fabrikam

| 科目                     | 借方金额 | 贷方金额 |
|-----------------------------|--------------|---------------|
| 应付帐款 (Fabrikam) | 75.00        |               |
| 现金 (Fabrikam)             |              | 75.00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam 付款用 Fabrikam West 发票和 Fabrikam East 贷方通知单结算

**Fabrikam 过帐**

| 科目                           | 借方金额 | 贷方金额 |
|-----------------------------------|--------------|---------------|
| 应付帐款 (Fabrikam)       | 25.00        |               |
| 向 Fabrikam East (Fabrikam) 的应付金额   |              | 25.00         |
| 从 Fabrikam West (Fabrikam) 的应收金额 | 100.00       |               |
| 应付帐款 (Fabrikam)       |              | 100.00        |

**Fabrikam East 过帐**

| 科目                           | 借方金额 | 贷方金额 |
|-----------------------------------|--------------|---------------|
| 从 Fabrikam (Fabrikam East) 的应收金额 | 25.00        |               |
| 应付帐款 (Fabrikam East)  |              | 25.00         |

**Fabrikam West 过帐**

| 科目                          | 借方金额 | 贷方金额 |
|----------------------------------|--------------|---------------|
| 应付帐款 (Fabrikam West) | 100.00       |               |
| 向 Fabrikam (Fabrikam West) 的应付金额  |              | 100.00        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a>示例 6：不具有主付款的供应商贷方通知单
Fabrikam 为供应商 3004 (Fourth Coffee) 生成 75.00 的付款。 该付款用针对 Fabrikam West 供应商 3004 的未结发票和针对 Fabrikam East 供应商 100 的未结贷方通知单结算。 该付款未在 **未结交易记录编辑** 页中选择为主付款。

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a>发票为供应商 3004 过帐到 Fabrikam West

| 帐户                          | 借方金额 | 贷方金额 |
|----------------------------------|--------------|---------------|
| 支出 (Fabrikam West)          | 100.00       |               |
| 应付帐款 (Fabrikam West) |              | 100.00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a>贷方通知单为供应商 100 过帐到 Fabrikam East

| 科目                          | 借方金额 | 贷方金额 |
|----------------------------------|--------------|---------------|
| 应付帐款 (Fabrikam East) | 25.00        |               |
| 采购退货 (Fabrikam East) |              | 25.00         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a>付款为供应商 3004 过帐到 Fabrikam

| 科目                     | 借方金额 | 贷方金额 |
|-----------------------------|--------------|---------------|
| 应付帐款 (Fabrikam) | 75.00        |               |
| 现金 (Fabrikam)             |              | 75.00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam 付款用 Fabrikam West 发票和 Fabrikam East 贷方通知单结算

**Fabrikam 过帐**

| 科目                           | 借方金额 | 贷方金额 |
|-----------------------------------|--------------|---------------|
| 从 Fabrikam West (Fabrikam) 的应收金额 | 75.00        |               |
| 应付帐款 (Fabrikam)       |              | 75.00         |

**Fabrikam East 过帐**

| 科目                                | 借方金额 | 贷方金额 |
|----------------------------------------|--------------|---------------|
| 从 Fabrikam West (Fabrikam East) 的应收金额 | 25.00        |               |
| 应付帐款 (Fabrikam East)       |              | 25.00         |

**Fabrikam West 过帐**

| 科目                              | 借方金额 | 贷方金额 |
|--------------------------------------|--------------|---------------|
| 应付帐款 (Fabrikam West)     | 75.00        |               |
| 向 Fabrikam (Fabrikam West) 的应付金额      |              | 75.00         |
| 应付帐款 (Fabrikam West)     | 25.00        |               |
| 向 Fabrikam East (Fabrikam West) 的应付金额 |              | 25.00         |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]