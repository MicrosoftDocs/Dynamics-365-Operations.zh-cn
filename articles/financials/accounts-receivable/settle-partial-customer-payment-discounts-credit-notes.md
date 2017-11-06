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

# <a name="settle-a-partial-customer-payment-that-has-discounts-on-credit-notes"></a><span data-ttu-id="96a5a-103">结算在贷方通知单上已折扣的部分客户付款</span><span class="sxs-lookup"><span data-stu-id="96a5a-103">Settle a partial customer payment that has discounts on credit notes</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="96a5a-104">本文向您介绍当原始发票也具有现金折扣时，在贷方通知单中执行的现金折扣的情况。</span><span class="sxs-lookup"><span data-stu-id="96a5a-104">This article walks you through a scenario where a cash discount is taken on a credit note when the original invoice also had a cash discount.</span></span> 

<span data-ttu-id="96a5a-105">Fabrikam 允许客户在部分付款以及贷方通知单上获得现金折扣。</span><span class="sxs-lookup"><span data-stu-id="96a5a-105">Fabrikam allows customers to take cash discounts on partial payments and also on credit notes (credit memos).</span></span> <span data-ttu-id="96a5a-106">当为客户在其上获得现金折扣的发票签发贷方通知单时，可以在贷方通知单上获得现金折扣。</span><span class="sxs-lookup"><span data-stu-id="96a5a-106">A cash discount can be taken on a credit note when the credit note is issued for an invoice that the customer took a cash discount on.</span></span> <span data-ttu-id="96a5a-107">不是提供贷方用于全部金额，您可以为排除客户获得的现金折扣百分比的金额贷记客户的余额。</span><span class="sxs-lookup"><span data-stu-id="96a5a-107">Instead of providing a credit for the full amount, you can credit the customer's balance for an amount that excludes the cash discount percent that the customer took.</span></span> <span data-ttu-id="96a5a-108">结算参数位于**应付账款参数**页上。</span><span class="sxs-lookup"><span data-stu-id="96a5a-108">The settlement parameters are located on the **Accounts receivable parameters** page.</span></span>

## <a name="invoice-and-credit-note"></a><span data-ttu-id="96a5a-109">发票和贷方通知单</span><span class="sxs-lookup"><span data-stu-id="96a5a-109">Invoice and credit note</span></span>
<span data-ttu-id="96a5a-110">客户 4035 具有 1.000.00 的发票和 100.00 的贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="96a5a-110">Customer 4035 has an invoice for 1,000.00 and a credit note for 100.00.</span></span> <span data-ttu-id="96a5a-111">如果在 14 天内支付，则每个单据具有 1 的折扣。</span><span class="sxs-lookup"><span data-stu-id="96a5a-111">Each document has a 1 percent discount if it's paid in 14 days.</span></span> <span data-ttu-id="96a5a-112">Arnie 可以在**“客户交易记录”**页上查看该信息。</span><span class="sxs-lookup"><span data-stu-id="96a5a-112">Arnie can view this information on the **Customer transactions** page.</span></span>

| <span data-ttu-id="96a5a-113">凭证</span><span class="sxs-lookup"><span data-stu-id="96a5a-113">Voucher</span></span>    | <span data-ttu-id="96a5a-114">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="96a5a-114">Transaction type</span></span> | <span data-ttu-id="96a5a-115">日期</span><span class="sxs-lookup"><span data-stu-id="96a5a-115">Date</span></span>      | <span data-ttu-id="96a5a-116">开票</span><span class="sxs-lookup"><span data-stu-id="96a5a-116">Invoice</span></span>  | <span data-ttu-id="96a5a-117">交易币种借方金额</span><span class="sxs-lookup"><span data-stu-id="96a5a-117">Amount in transaction currency debit</span></span> | <span data-ttu-id="96a5a-118">交易币种贷方金额</span><span class="sxs-lookup"><span data-stu-id="96a5a-118">Amount in transaction currency credit</span></span> | <span data-ttu-id="96a5a-119">余额</span><span class="sxs-lookup"><span data-stu-id="96a5a-119">Balance</span></span>  | <span data-ttu-id="96a5a-120">货币</span><span class="sxs-lookup"><span data-stu-id="96a5a-120">Currency</span></span> |
|------------|------------------|-----------|----------|--------------------------------------|---------------------------------------|----------|----------|
| <span data-ttu-id="96a5a-121">FTI-10050</span><span class="sxs-lookup"><span data-stu-id="96a5a-121">FTI-10050</span></span>  | <span data-ttu-id="96a5a-122">开票</span><span class="sxs-lookup"><span data-stu-id="96a5a-122">Invoice</span></span>          | <span data-ttu-id="96a5a-123">6/28/2015</span><span class="sxs-lookup"><span data-stu-id="96a5a-123">6/28/2015</span></span> | <span data-ttu-id="96a5a-124">10050</span><span class="sxs-lookup"><span data-stu-id="96a5a-124">10050</span></span>    | <span data-ttu-id="96a5a-125">1,000.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-125">1,000.00</span></span>                             |                                       | <span data-ttu-id="96a5a-126">1,000.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-126">1,000.00</span></span> | <span data-ttu-id="96a5a-127">美元</span><span class="sxs-lookup"><span data-stu-id="96a5a-127">USD</span></span>      |
| <span data-ttu-id="96a5a-128">CCRN-10050</span><span class="sxs-lookup"><span data-stu-id="96a5a-128">CCRN-10050</span></span> | <span data-ttu-id="96a5a-129">贷方通知单</span><span class="sxs-lookup"><span data-stu-id="96a5a-129">Credit note</span></span>      | <span data-ttu-id="96a5a-130">6/28/2015</span><span class="sxs-lookup"><span data-stu-id="96a5a-130">6/28/2015</span></span> | <span data-ttu-id="96a5a-131">CR-10050</span><span class="sxs-lookup"><span data-stu-id="96a5a-131">CR-10050</span></span> |                                      | <span data-ttu-id="96a5a-132">100.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-132">100.00</span></span>                                | <span data-ttu-id="96a5a-133">-100.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-133">-100.00</span></span>  | <span data-ttu-id="96a5a-134">美元</span><span class="sxs-lookup"><span data-stu-id="96a5a-134">USD</span></span>      |

## <a name="settle-a-credit-note-with-an-invoice"></a><span data-ttu-id="96a5a-135">结算使用发票的贷方通知单</span><span class="sxs-lookup"><span data-stu-id="96a5a-135">Settle a credit note with an invoice</span></span>
<span data-ttu-id="96a5a-136">从**“客户交易记录”**页上，Arnie 打开**“结算交易记录”**页。</span><span class="sxs-lookup"><span data-stu-id="96a5a-136">From the **Customer transactions** page, Arnie opens the **Settle transactions** page.</span></span> <span data-ttu-id="96a5a-137">他可以使用 **“结算交易记录”**页来结算发票和贷方通知单。</span><span class="sxs-lookup"><span data-stu-id="96a5a-137">He can use the **Settle transactions** page to settle the invoice and credit note.</span></span> <span data-ttu-id="96a5a-138">作为结算流程的一部分，他查看现金折扣日期和金额。</span><span class="sxs-lookup"><span data-stu-id="96a5a-138">As part of the settlement process, he views the cash discount dates and amounts.</span></span> <span data-ttu-id="96a5a-139">他标记两个单据，然后单击“**过帐**”结算该交易记录。</span><span class="sxs-lookup"><span data-stu-id="96a5a-139">He marks the two documents and then clicks **Post** to settle the transactions.</span></span> <span data-ttu-id="96a5a-140">这里有贷方通知单上的 -1.00 的折扣，因为 Fabrikam 允许贷方通知单上的折扣。</span><span class="sxs-lookup"><span data-stu-id="96a5a-140">There is a discount of -1.00 on the credit note, because Fabrikam allows for discounts on credit notes.</span></span>

| <span data-ttu-id="96a5a-141">标记</span><span class="sxs-lookup"><span data-stu-id="96a5a-141">Mark</span></span>     | <span data-ttu-id="96a5a-142">使用现金折扣</span><span class="sxs-lookup"><span data-stu-id="96a5a-142">Use cash discount</span></span> | <span data-ttu-id="96a5a-143">凭证</span><span class="sxs-lookup"><span data-stu-id="96a5a-143">Voucher</span></span>    | <span data-ttu-id="96a5a-144">帐户</span><span class="sxs-lookup"><span data-stu-id="96a5a-144">Account</span></span> | <span data-ttu-id="96a5a-145">日期</span><span class="sxs-lookup"><span data-stu-id="96a5a-145">Date</span></span>      | <span data-ttu-id="96a5a-146">到期日期</span><span class="sxs-lookup"><span data-stu-id="96a5a-146">Due date</span></span>  | <span data-ttu-id="96a5a-147">开票</span><span class="sxs-lookup"><span data-stu-id="96a5a-147">Invoice</span></span>  | <span data-ttu-id="96a5a-148">交易记录币种金额</span><span class="sxs-lookup"><span data-stu-id="96a5a-148">Amount in transaction currency</span></span> | <span data-ttu-id="96a5a-149">货币</span><span class="sxs-lookup"><span data-stu-id="96a5a-149">Currency</span></span> | <span data-ttu-id="96a5a-150">要结算的金额</span><span class="sxs-lookup"><span data-stu-id="96a5a-150">Amount to settle</span></span> |
|----------|-------------------|------------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| <span data-ttu-id="96a5a-151">已选择</span><span class="sxs-lookup"><span data-stu-id="96a5a-151">Selected</span></span> | <span data-ttu-id="96a5a-152">标准</span><span class="sxs-lookup"><span data-stu-id="96a5a-152">Normal</span></span>            | <span data-ttu-id="96a5a-153">FTI-10050</span><span class="sxs-lookup"><span data-stu-id="96a5a-153">FTI-10050</span></span>  | <span data-ttu-id="96a5a-154">4035</span><span class="sxs-lookup"><span data-stu-id="96a5a-154">4035</span></span>    | <span data-ttu-id="96a5a-155">6/28/2015</span><span class="sxs-lookup"><span data-stu-id="96a5a-155">6/28/2015</span></span> | <span data-ttu-id="96a5a-156">7/28/2015</span><span class="sxs-lookup"><span data-stu-id="96a5a-156">7/28/2015</span></span> | <span data-ttu-id="96a5a-157">10050</span><span class="sxs-lookup"><span data-stu-id="96a5a-157">10050</span></span>    | <span data-ttu-id="96a5a-158">1,000.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-158">1,000.00</span></span>                       | <span data-ttu-id="96a5a-159">美元</span><span class="sxs-lookup"><span data-stu-id="96a5a-159">USD</span></span>      | <span data-ttu-id="96a5a-160">990.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-160">990.00</span></span>           |
| <span data-ttu-id="96a5a-161">选定</span><span class="sxs-lookup"><span data-stu-id="96a5a-161">Selected</span></span> | <span data-ttu-id="96a5a-162">标准</span><span class="sxs-lookup"><span data-stu-id="96a5a-162">Normal</span></span>            | <span data-ttu-id="96a5a-163">CCRN-10050</span><span class="sxs-lookup"><span data-stu-id="96a5a-163">CCRN-10050</span></span> | <span data-ttu-id="96a5a-164">4035</span><span class="sxs-lookup"><span data-stu-id="96a5a-164">4035</span></span>    | <span data-ttu-id="96a5a-165">6/28/2015</span><span class="sxs-lookup"><span data-stu-id="96a5a-165">6/28/2015</span></span> | <span data-ttu-id="96a5a-166">7/28/2015</span><span class="sxs-lookup"><span data-stu-id="96a5a-166">7/28/2015</span></span> | <span data-ttu-id="96a5a-167">CR-10050</span><span class="sxs-lookup"><span data-stu-id="96a5a-167">CR-10050</span></span> | <span data-ttu-id="96a5a-168">-100.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-168">-100.00</span></span>                        | <span data-ttu-id="96a5a-169">美元</span><span class="sxs-lookup"><span data-stu-id="96a5a-169">USD</span></span>      | <span data-ttu-id="96a5a-170">-99.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-170">-99.00</span></span>           |

<span data-ttu-id="96a5a-171">折扣信息显示在**“结算交易记录”**页的底部。</span><span class="sxs-lookup"><span data-stu-id="96a5a-171">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="96a5a-172">现金折扣日期</span><span class="sxs-lookup"><span data-stu-id="96a5a-172">Cash discount date</span></span>           | <span data-ttu-id="96a5a-173">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="96a5a-173">7/12/2015</span></span> |
| <span data-ttu-id="96a5a-174">现金折扣金额</span><span class="sxs-lookup"><span data-stu-id="96a5a-174">Cash discount amount</span></span>         | <span data-ttu-id="96a5a-175">-1.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-175">-1.00</span></span>     |
| <span data-ttu-id="96a5a-176">使用现金折扣</span><span class="sxs-lookup"><span data-stu-id="96a5a-176">Use cash discount</span></span>            | <span data-ttu-id="96a5a-177">标准</span><span class="sxs-lookup"><span data-stu-id="96a5a-177">Normal</span></span>    |
| <span data-ttu-id="96a5a-178">提取了现金折扣</span><span class="sxs-lookup"><span data-stu-id="96a5a-178">Cash discount taken</span></span>          | <span data-ttu-id="96a5a-179">0.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-179">0.00</span></span>      |
| <span data-ttu-id="96a5a-180">要提取的现金折扣金额</span><span class="sxs-lookup"><span data-stu-id="96a5a-180">Cash discount amount to take</span></span> | <span data-ttu-id="96a5a-181">-1.00</span><span class="sxs-lookup"><span data-stu-id="96a5a-181">-1.00</span></span>     |

<span data-ttu-id="96a5a-182">结算将为 100.00，并将包括 99.00 的付款和 1.00 的折扣。</span><span class="sxs-lookup"><span data-stu-id="96a5a-182">The settlement will be 100.00, and will include a payment of 99.00 and a discount of 1.00.</span></span>




