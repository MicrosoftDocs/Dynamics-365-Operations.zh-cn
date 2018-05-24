---
title: "现金折扣"
description: "为应付账款和应收账款设置和共享现金折扣。  可用现金折扣可以在客户发票或供应商发票上定义，并在现金折扣日期内支付发票时执行。"
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5ccf41d1184280d3c4a000db13847733fd2cf4d2
ms.contentlocale: zh-cn
ms.lasthandoff: 05/08/2018

---

# <a name="cash-discounts"></a>现金折扣

[!include [banner](../includes/banner.md)]

为应付账款和应收账款设置和共享现金折扣。  可用现金折扣可以在客户发票或供应商发票上定义，并在现金折扣日期内支付发票时执行。 

## <a name="cash-discounts"></a>现金折扣

客户或供应商的现金折扣可以在“现金折扣”页中创建。 通过使用“下一折扣代码”字段，您还可以定义随以前的现金折扣到期而彼此交替的一系列现金折扣。 有关详细信息，请参见本节中后面部分的“示例：现金折扣系列”。 如果发票和/或货方交易记录（付款或货方通知单）是按法人的记帐币种以外的币种输入的，则现金折扣将使用付款或货方通知单的日期计算。 如果发票和信用卡文档登录到不同的法人中，而且如果法人的记账币种不同、汇率将从该发票的法人处获取，就像从信用卡文档的日期的法人处获取一样。 有关详细信息，请参见本节中后面部分的“示例：现金折扣的汇率”。

## <a name="defaulting-order-of-cash-discount-main-account"></a>现金折扣主科目的默认订单

如果因及时结算发票而得到了现金折扣，该现金折扣将根据下面的默认优先级自动过帐到现金折扣主科目：
1.  在客户“结算未结交易记录”页或供应商“结算未结交易记录”页上的“备选现金折扣帐户”字段中指定的主科目。
2.  在分配到发票增值税代码的分类帐记帐组的“客户现金折扣”字段或“供应商现金折扣”字段中指定的主科目。 在“分类帐记帐组”页上设置分类帐记帐组，并将其分配给“销售税代码”页中的销售税代码。
3.  “现金折扣”页上的主记帐科目，在位于已结算发票上的现金折扣代码的“客户折扣的主科目”字段或“供应商折扣的主科目”字段中。
4.  现金折扣的主科目，如在“自动交易记录帐户”中定义。

## <a name="example-series-of-cash-discounts"></a>示例：现金折扣系列
按照下列说明设置三个现金折扣代码：
-   代码 5D10% – 若 5 天内付款，则有 10% 的现金折扣。
-   代码 10D5% – 在 10 天内付款可获得 5% 的现金折扣。
-   代码 14D2% – 在 14 天内付款可获得 2% 的现金折扣。

在“下一折扣代码”字段中：
-   对于 5D10% 代码，选择 10D5%。
-   对于 10D5% 代码，选择 14D2%。
-   对于 14D2% 代码，将“下一折扣代码”字段保留为空。

三个现金折扣随付款日期超过发票上的前一个现金折扣日期而彼此交替。 根据在现金折扣序列中哪个现金折扣日期被满足，当对发票付款时，只能保证一个现金折扣。

## <a name="example-exchange-rates-for-cash-discounts"></a>示例：现金折扣的汇率
您的法人的记账币种是 EUR，以下汇率是为 USD 指定的：
-   2 月 1 日 = 110
-   3 月 1 日 = 80

2 月 15 日按照现金折扣条例 20D2% 过账 1000 USD 的发票。 该发票的记账币种金额为 1100 EUR。 3 月 1 日使用发票结算 980 USD 的付款。 现金折扣金额为 20 USD。 付款的记账币种金额为 784 EUR。 使用汇率（3 月 1 日：20 \* 80 / 100 = 16 EUR）计算现金折扣的记账币种金额。

> [!NOTE]
> 如果“计算部分付款的现金折扣”选项在“应收账款参数”或“应付账款参数”页中被选定时，会使用在每个部分付款的日期有效的汇率。 


