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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9960af8c4961a42e7e829077da40bcbbf3bc71c2
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="cash-discounts"></a><span data-ttu-id="d3a1d-104">现金折扣</span><span class="sxs-lookup"><span data-stu-id="d3a1d-104">Cash discounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d3a1d-105">为应付账款和应收账款设置和共享现金折扣。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="d3a1d-106">可用现金折扣可以在客户发票或供应商发票上定义，并在现金折扣日期内支付发票时执行。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

<a name="cash-discounts"></a><span data-ttu-id="d3a1d-107">现金折扣</span><span class="sxs-lookup"><span data-stu-id="d3a1d-107">Cash discounts</span></span>
--------------

<span data-ttu-id="d3a1d-108">客户或供应商的现金折扣可以在“现金折扣”页中创建。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="d3a1d-109">通过使用“下一折扣代码”字段，您还可以定义随以前的现金折扣到期而彼此交替的一系列现金折扣。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="d3a1d-110">有关详细信息，请参见本节中后面部分的“示例：现金折扣系列”。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="d3a1d-111">如果发票和/或货方交易记录（付款或货方通知单）是按法人的记帐币种以外的币种输入的，则现金折扣将使用付款或货方通知单的日期计算。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="d3a1d-112">如果发票和信用卡文档登录到不同的法人中，而且如果法人的记账币种不同、汇率将从该发票的法人处获取，就像从信用卡文档的日期的法人处获取一样。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="d3a1d-113">有关详细信息，请参见本节中后面部分的“示例：现金折扣的汇率”。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>
<span data-ttu-id="d3a1d-114">现金折扣主科目的默认订单</span><span class="sxs-lookup"><span data-stu-id="d3a1d-114">Defaulting order of cash discount main account</span></span>
----------------------------------------------

<span data-ttu-id="d3a1d-115">如果因及时结算发票而得到了现金折扣，该现金折扣将根据下面的默认优先级自动过帐到现金折扣主科目：</span><span class="sxs-lookup"><span data-stu-id="d3a1d-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="d3a1d-116">在客户“结算未结交易记录”页或供应商“结算未结交易记录”页上的“备选现金折扣帐户”字段中指定的主科目。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="d3a1d-117">在分配到发票增值税代码的分类帐记帐组的“客户现金折扣”字段或“供应商现金折扣”字段中指定的主科目。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="d3a1d-118">在“分类帐记帐组”页上设置分类帐记帐组，并将其分配给“销售税代码”页中的销售税代码。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="d3a1d-119">“现金折扣”页上的主记帐科目，在位于已结算发票上的现金折扣代码的“客户折扣的主科目”字段或“供应商折扣的主科目”字段中。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="d3a1d-120">现金折扣的主科目，如在“自动交易记录帐户”中定义。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="d3a1d-121">示例：现金折扣系列</span><span class="sxs-lookup"><span data-stu-id="d3a1d-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="d3a1d-122">按照下列说明设置三个现金折扣代码：</span><span class="sxs-lookup"><span data-stu-id="d3a1d-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="d3a1d-123">代码 5D10% – 若 5 天内付款，则有 10% 的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="d3a1d-124">代码 10D5% – 在 10 天内付款可获得 5% 的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="d3a1d-125">代码 14D2% – 在 14 天内付款可获得 2% 的现金折扣。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="d3a1d-126">在“下一折扣代码”字段中：</span><span class="sxs-lookup"><span data-stu-id="d3a1d-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="d3a1d-127">对于 5D10% 代码，选择 10D5%。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="d3a1d-128">对于 10D5% 代码，选择 14D2%。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="d3a1d-129">对于 14D2% 代码，将“下一折扣代码”字段保留为空。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="d3a1d-130">三个现金折扣随付款日期超过发票上的前一个现金折扣日期而彼此交替。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="d3a1d-131">根据在现金折扣序列中哪个现金折扣日期被满足，当对发票付款时，只能保证一个现金折扣。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="d3a1d-132">示例：现金折扣的汇率</span><span class="sxs-lookup"><span data-stu-id="d3a1d-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="d3a1d-133">您的法人的记账币种是 EUR，以下汇率是为 USD 指定的：</span><span class="sxs-lookup"><span data-stu-id="d3a1d-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="d3a1d-134">2 月 1 日 = 110</span><span class="sxs-lookup"><span data-stu-id="d3a1d-134">February 1 = 110</span></span>
-   <span data-ttu-id="d3a1d-135">3 月 1 日 = 80</span><span class="sxs-lookup"><span data-stu-id="d3a1d-135">March 1 = 80</span></span>

<span data-ttu-id="d3a1d-136">2 月 15 日按照现金折扣条例 20D2% 过账 1000 USD 的发票。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="d3a1d-137">该发票的记账币种金额为 1100 EUR。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="d3a1d-138">3 月 1 日使用发票结算 980 USD 的付款。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="d3a1d-139">现金折扣金额为 20 USD。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="d3a1d-140">付款的记账币种金额为 784 EUR。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="d3a1d-141">使用汇率（3 月 1 日：20 \* 80 / 100 = 16 EUR）计算现金折扣的记账币种金额。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>
| <span data-ttu-id="d3a1d-142">**注释**</span><span class="sxs-lookup"><span data-stu-id="d3a1d-142">**Note**</span></span>                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3a1d-143">如果“计算部分付款的现金折扣”选项在“应收账款参数”或“应付账款参数”页中被选定时，会使用在每个部分付款的日期有效的汇率。</span><span class="sxs-lookup"><span data-stu-id="d3a1d-143">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> |

 
=

 




