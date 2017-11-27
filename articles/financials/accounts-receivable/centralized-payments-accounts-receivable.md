---
title: "应收账款的集中付款"
description: "包括多个法人的组织可以使用处理所有付款的单个法人创建和管理付款。 因此，不必在多个法人中输入同一交易记录。 本文提供显示集中付款过帐如何在不同环境中处理的示例。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7208acc35e656d12b3c4f88a090f36ecfdd4fdfb
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="centralized-payments-for-accounts-receivable"></a>应收账款的集中付款

[!include[banner](../includes/banner.md)]


包括多个法人的组织可以使用处理所有付款的单个法人创建和管理付款。 因此，不必在多个法人中输入同一交易记录。 本文提供显示集中付款过帐如何在不同环境中处理的示例。

包括多个法人的组织可以使用处理所有付款的法人创建和管理付款。 因此，不必在多个法人中输入同一交易记录。 此外，组织也节省时间，因为针对集中付款，付款方案、结算以及编辑未结和已结交易记录的流程已简化。 

在集中式付款的组织中，有很多营业的法人，且每个营业的法人都管理自己的发票应收信息。 所有营业的法人的付款都是由称作付款的法人的单个法人接收的。 在结算流程中，生成适用的应付和应收交易记录。 您可以指定组织内的哪个法人接收已有收益或已有损失交易记录，以及如何处理与集中式付款相关的现金折扣交易记录。 

以下示例说明如何在不同的环境中处理过帐。 假定所有这些示例都采用以下配置：

-   法人分别为 Fabrikam、Fabrikam East 和 Fabrikam West。 客户付款输入 Fabrikam。
-   **“内部公司”**页上的**“过帐现金折扣”**字段设置为**“发票法人”**。
-   **“内部公司”**页上的**“过帐币种汇兑损益”**字段设置为**“付款法人”**。
-   客户 Northwind Traders 在每个法人中设置为一个客户。 来自不同法人的客户被标识为同一客户，因为他们共享相同的全球通讯簿 ID。

| 通讯簿 ID | 客户帐户 | 姓名              | 法人  |
|-----------------|------------------|-------------------|---------------|
| 4050            | 4000             | Northwind Traders | Fabrikam      |
| 4050            | 4000             | Northwind Traders | Fabrikam East |
| 4050            | 10000            | Northwind Traders | Fabrikam West |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a>示例 1：来自其他法人的发票的客户付款
Fabrikam 为 Fabrikam 客户帐户 4000 (Northwind Traders) 收到了金额为 600.00 的付款。 该付款用 Fabrikam East 中的客户帐户 4000 的未结发票结算。

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a>在 Fabrikam East 中为客户 4000 过帐发票

| 科目                             | 借方金额 | 贷方金额 |
|-------------------------------------|--------------|---------------|
| 应收帐款 (Fabrikam East) | 600.00       |               |
| 销售 (Fabrikam East)               |              | 600.00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>在 Fabrikam 中为客户 4000 接收和过帐付款

| 科目                        | 借方金额 | 贷方金额 |
|--------------------------------|--------------|---------------|
| 现金 (Fabrikam)                | 600.00       |               |
| 应收帐款 (Fabrikam) |              | 600.00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam 付款用 Fabrikam East 发票结算

**Fabrikam 过帐**

| 科目                         | 借方金额 | 贷方金额 |
|---------------------------------|--------------|---------------|
| 应收帐款 (Fabrikam)  | 600.00       |               |
| 向 Fabrikam East (Fabrikam) 的应付金额 |              | 600.00        |

**Fabrikam East 过帐**

| 科目                             | 借方金额 | 贷方金额 |
|-------------------------------------|--------------|---------------|
| 从 Fabrikam (Fabrikam East) 的应收金额   | 600.00       |               |
| 应收帐款 (Fabrikam East) |              | 600.00        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a>示例 2：来自具有现金折扣的其他法人的发票的客户付款
Fabrikam 为 Fabrikam 客户帐户 4000 (Northwind Traders) 收到了金额为 580.00 的付款。 Fabrikam East 为客户 4000 (Fourth Coffee) 具有一个未结发票。 该发票具有 20.00 的可用现金折扣。 该付款用未结 Fabrikam East 发票结算。 该现金折扣过帐到发票法人 Fabrikam East。

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>在 Fabrikam East 中为 Fabrikam East 客户 4000 过帐发票

| 科目                             | 借方金额 | 贷方金额 |
|-------------------------------------|--------------|---------------|
| 应收帐款 (Fabrikam East) | 600.00       |               |
| 销售 (Fabrikam East)               |              | 600.00        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>在 Fabrikam 中为 Fabrikam 客户 4000 接收和过帐付款

| 科目                        | 借方金额 | 贷方金额 |
|--------------------------------|--------------|---------------|
| 现金 (Fabrikam)                | 600.00       |               |
| 应收帐款 (Fabrikam) |              | 600.00        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam 付款用 Fabrikam East 发票结算

**Fabrikam 过帐**

| 科目                         | 借方金额 | 贷方金额 |
|---------------------------------|--------------|---------------|
| 应收帐款 (Fabrikam)  | 580.00       |               |
| 向 Fabrikam East (Fabrikam) 的应付金额 |              | 580.00        |

**Fabrikam East 过帐**

| 科目                             | 借方金额 | 贷方金额 |
|-------------------------------------|--------------|---------------|
| 从 Fabrikam (Fabrikam East) 的应收金额   | 580.00       |               |
| 应收帐款 (Fabrikam East) |              | 580.00        |
| 现金折扣 (Fabrikam East)       | 20.00        |               |
| 应收账款 (Fabrikam East) |              | 20.00         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a>示例 3：来自具有已有汇率收益的其他法人的发票的客户付款
Fabrikam 为 Fabrikam 客户帐户 4000 (Northwind Traders) 收到了金额为 600.00 欧元 (EUR) 的付款。 该付款用 Fabrikam East 中的客户 4000 的未结发票结算。 在结算过程中将生成币种汇率收益交易记录。

-   在发票日期的欧元 (EUR) 到美元 (USD) 的汇率：1.2062
-   在付款日期的欧元到美元的汇率：1.2277

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a>在 Fabrikam East 中为 Fabrikam East 客户 4000 过帐发票

| 科目                             | 借方金额            | 贷方金额           |
|-------------------------------------|-------------------------|-------------------------|
| 应收帐款 (Fabrikam East) | 600.00 EUR / 723.72 USD |                         |
| 销售 (Fabrikam East)               |                         | 600.00 EUR / 723.72 USD |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a>在 Fabrikam 中为 Fabrikam 客户 4000 接收和过帐付款

| 科目                        | 借方金额            | 贷方金额           |
|--------------------------------|-------------------------|-------------------------|
| 现金 (Fabrikam)                | 600.00 EUR / 736.62 USD |                         |
| 应收帐款 (Fabrikam) |                         | 600.00 EUR / 736.62 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam 付款用 Fabrikam East 发票结算

**Fabrikam 过帐**

| 科目                         | 借方金额            | 贷方金额           |
|---------------------------------|-------------------------|-------------------------|
| 应收帐款 (Fabrikam)  | 600.00 EUR / 736.62 USD |                         |
| 向 Fabrikam East (Fabrikam) 的应付金额 |                         | 600.00 EUR / 736.62 USD |
| 向 Fabrikam East (Fabrikam) 的应付金额 | 0.00 EUR / 12.90 USD    |                         |
| 已有收益 (Fabrikam)        |                         | 0.00 EUR / 12.90 USD    |

**Fabrikam East 过帐**

| 科目                             | 借方金额            | 贷方金额           |
|-------------------------------------|-------------------------|-------------------------|
| 从 Fabrikam (Fabrikam East) 的应收金额   | 600.00 EUR / 736.62 USD |                         |
| 应收帐款 (Fabrikam East) |                         | 600.00 EUR / 736.62 USD |
| 应收帐款 (Fabrikam East) | 0.00 EUR / 12.90 USD    |                         |
| 从 Fabrikam (Fabrikam East) 的应收金额   |                         | 0.00 EUR / 12.90 USD    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a>示例 4：来自具有现金折扣和已有汇率收益的其他法人的发票的客户付款
Fabrikam 为 Fabrikam East 中的未结发票，为 Fabrikam customer 4000 (Northwind Traders) 过帐付款。 该发票具有可用的现金折扣并且生成增值税交易记录。 该付款用未结 Fabrikam East 发票结算。 在结算过程中将生成币种汇率收益交易记录。 现金折扣过帐到发票法人 (Fabrikam East)，且币种汇率获得过帐到付款法人 (Fabrikam)。

-   在发票日期的欧元到美元的汇率：1.2062
-   在付款日期的欧元到美元的汇率：1.2277

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a>过帐普通发票，并且在 Fabrikam East 中为客户 4000 生成纳税交易记录

| 科目                             | 借方金额            | 贷方金额           |
|-------------------------------------|-------------------------|-------------------------|
| 应收帐款 (Fabrikam East) | 638.22 EUR / 769.82 USD |                         |
| 销售 (Fabrikam East)               |                         | 600.00 EUR / 723.72 USD |
| 增值税 (Fabrikam East)           |                         | 38.22 EUR / 46.10 USD   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a>在 Fabrikam 中为客户 4000 接收和过帐付款

| 科目                        | 借方金额            | 贷方金额           |
|--------------------------------|-------------------------|-------------------------|
| 现金 (Fabrikam)                | 626.22 EUR / 768.81 USD |                         |
| 应收帐款 (Fabrikam) |                         | 626.22 EUR / 768.81 USD |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a>Fabrikam 付款用 Fabrikam East 发票结算

**Fabrikam 过帐**

| 科目                         | 借方金额            | 贷方金额           |
|---------------------------------|-------------------------|-------------------------|
| 应收帐款 (Fabrikam)  | 626.22 EUR / 768.81 USD |                         |
| 向 Fabrikam East (Fabrikam) 的应付金额 |                         | 626.22 EUR / 768.81 USD |
| 向 Fabrikam East (Fabrikam) 的应付金额 | 0.00 EUR / 13.46 USD    |                         |
| 已有收益 (Fabrikam)        |                         | 0.00 EUR / 13.46 USD    |

**Fabrikam East 过帐**

| 科目                             | 借方金额            | 贷方金额           |
|-------------------------------------|-------------------------|-------------------------|
| 从 Fabrikam (Fabrikam East) 的应收金额   | 626.22 EUR / 768.81 USD |                         |
| 应收帐款 (Fabrikam East) |                         | 626.22 EUR / 768.81 USD |
| 应收帐款 (Fabrikam East)  | 0.00 EUR / 13.46 USD    |                         |
| 从 Fabrikam (Fabrikam East) 的应收金额   |                         | 0.00 EUR / 13.46 USD    |
| 现金折扣 (Fabrikam East)       | 12.00 EUR / 14.47 USD   |                         |
| 应收帐款 (Fabrikam East) |                         | 12.00 EUR / 14.47 USD   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a>示例 5：具有主付款的客户贷方通知单
Fabrikam 从客户 4000 (Northwind Traders) 接收 75.00 的付款。 该付款用针对 Fabrikam West 客户 10000 的未结发票和针对 Fabrikam East 客户 4000 的未结贷方通知单结算。 该付款在**未结交易记录编辑**页中选择为主付款。

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>发票为客户 10000 过帐到 Fabrikam West

| 帐户                             | 借方金额 | 贷方金额 |
|-------------------------------------|--------------|---------------|
| 应收帐款 (Fabrikam West) | 100.00       |               |
| 销售 (Fabrikam West)               |              | 100.00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>贷方通知单为客户 4000 过帐到 Fabrikam East

| 科目                             | 借方金额 | 贷方金额 |
|-------------------------------------|--------------|---------------|
| 销售退货 (Fabrikam East)       | 25.00        |               |
| 应收帐款 (Fabrikam East) |              | 25.00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>付款为客户 4000 过帐到 Fabrikam

| 科目                        | 借方金额 | 贷方金额 |
|--------------------------------|--------------|---------------|
| 现金 (Fabrikam)                | 75.00        |               |
| 应收帐款 (Fabrikam) |              | 75.00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam 付款用 Fabrikam West 发票和 Fabrikam East 贷方通知单结算

**Fabrikam 过帐**

| 科目                           | 借方金额 | 贷方金额 |
|-----------------------------------|--------------|---------------|
| 从 Fabrikam East (Fabrikam) 的应收金额 | 25.00        |               |
| 应收帐款 (Fabrikam)    |              | 25.00         |
| 应收帐款 (Fabrikam)    | 100.00       |               |
| 向 Fabrikam West (Fabrikam) 的应付金额   |              | 100.00        |

**Fabrikam East 过帐**

| 科目                             | 借方金额 | 贷方金额 |
|-------------------------------------|--------------|---------------|
| 应收帐款 (Fabrikam East) | 25.00        |               |
| 向 Fabrikam (Fabrikam East) 的应付金额     |              | 25.00         |

**Fabrikam West 过帐**

| 科目                             | 借方金额 | 贷方金额 |
|-------------------------------------|--------------|---------------|
| 从 Fabrikam (Fabrikam West) 的应收金额   | 100.00       |               |
| 应收帐款 (Fabrikam West) |              | 100.00        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a>示例 6：没有主付款的客户贷方通知单
Fabrikam 从客户 4000 (Northwind Traders) 接收 75.00 的付款。 该付款用针对 Fabrikam West 客户 10000 的未结发票和针对 Fabrikam East 客户 4000 的未结贷方通知单结算。 该付款未在**未结交易记录编辑**页中选择为主付款。

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a>发票为客户 10000 过帐到 Fabrikam West

| 帐户                             | 借方金额 | 贷方金额 |
|-------------------------------------|--------------|---------------|
| 应收帐款 (Fabrikam West) | 100.00       |               |
| 销售 (Fabrikam West)               |              | 100.00        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a>贷方通知单为客户 4000 过帐到 Fabrikam East

| 科目                             | 借方金额 | 贷方金额 |
|-------------------------------------|--------------|---------------|
| 销售退货 (Fabrikam East)       | 25.00        |               |
| 应收帐款 (Fabrikam East) |              | 25.00         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a>付款为客户 4000 过帐到 Fabrikam

| 科目                        | 借方金额 | 贷方金额 |
|--------------------------------|--------------|---------------|
| 现金 (Fabrikam)                | 75.00        |               |
| 应收帐款 (Fabrikam) |              | 75.00         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a>Fabrikam 付款用 Fabrikam West 发票和 Fabrikam East 贷方通知单结算

**Fabrikam 过帐**

| 科目                         | 借方金额 | 贷方金额 |
|---------------------------------|--------------|---------------|
| 应收帐款 (Fabrikam)  | 75.00        |               |
| 向 Fabrikam West (Fabrikam) 的应付金额 |              | 75.00         |

**Fabrikam East 过帐**

| 科目                              | 借方金额 | 贷方金额 |
|--------------------------------------|--------------|---------------|
| 应收帐款 (Fabrikam East)  | 25.00        |               |
| 向 Fabrikam West (Fabrikam East) 的应付金额 |              | 25.00         |

**Fabrikam West 过帐**

| 科目                                | 借方金额 | 贷方金额 |
|----------------------------------------|--------------|---------------|
| 从 Fabrikam (Fabrikam West) 的应收金额      | 75.00        |               |
| 应收帐款 (Fabrikam West)    |              | 75.00         |
| 从 Fabrikam East (Fabrikam West) 的应收金额 | 25.00        |               |
| 应收账款 (Fabrikam West)    |              | 25.00         |






