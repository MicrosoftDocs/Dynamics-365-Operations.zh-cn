---
title: 超额支付的现金折扣
description: 本文提供显示在客户执行现金折扣同时超额支付时如何处理付款的情况。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2fafe2fba9dd71fc09c60bfa20d72fa59510b7f
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154148"
---
# <a name="cash-discounts-for-overpayments"></a><span data-ttu-id="7f9a2-103">超额支付的现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-103">Cash discounts for overpayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f9a2-104">本文提供显示在客户执行现金折扣同时超额支付时如何处理付款的情况。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-104">This article provides scenarios that show how a payment is handled when the customer takes a cash discount but also overpays.</span></span> 

<span data-ttu-id="7f9a2-105">当付款金额高于发票金额减去现金折扣后的金额时，应被视为超额支付。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-105">An invoice is considered overpaid when the payment amount is more than the invoice amount minus the cash discount.</span></span> <span data-ttu-id="7f9a2-106">要指定在超额支付发票时处理可获得的现金折扣差额的方式，请使用**应收账款参数**页面上的**现金折扣管理**和**最大超额支付或支付不足**。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-106">To specify how an obtainable cash discount difference is handled when an invoice is overpaid, use the **Cash discount administration** and **Maximum overpayment or underpayment** fields on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="7f9a2-107">在以下示例中，客户对发票超额支付了 0.50。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-107">In the following example, the customer has overpaid the invoice by 0.50.</span></span>

| <span data-ttu-id="7f9a2-108">发票合计</span><span class="sxs-lookup"><span data-stu-id="7f9a2-108">Invoice total</span></span> | <span data-ttu-id="7f9a2-109">可用的现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-109">Cash discount available</span></span> | <span data-ttu-id="7f9a2-110">要支付的金额，其中包括现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-110">Amount to be paid, which includes the cash discount</span></span> | <span data-ttu-id="7f9a2-111">客户实际支付金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-111">Amount the customer actually pays</span></span> |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="7f9a2-112">105.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-112">105.00</span></span>        | <span data-ttu-id="7f9a2-113">1050</span><span class="sxs-lookup"><span data-stu-id="7f9a2-113">10.50</span></span>                   | <span data-ttu-id="7f9a2-114">94.50</span><span class="sxs-lookup"><span data-stu-id="7f9a2-114">94.50</span></span>                                               | <span data-ttu-id="7f9a2-115">95.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-115">95.00</span></span>                             |

## <a name="cash-discount-administration--specific"></a><span data-ttu-id="7f9a2-116">现金折扣管理 = 特定</span><span class="sxs-lookup"><span data-stu-id="7f9a2-116">Cash discount administration = Specific</span></span>
<span data-ttu-id="7f9a2-117">当在**自动交易记录帐户**页面上的**现金折扣管理**字段中选择看**特定**时，将获得完全现金折扣。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-117">When **Specific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the full cash discount is taken.</span></span> <span data-ttu-id="7f9a2-118">超额支付金额或者被过帐到现金折扣差额分类帐帐户或作为余额留在客户帐户上。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-118">The overpayment amount either is posted to a cash discount difference ledger account or remains a balance on the customer’s account.</span></span> <span data-ttu-id="7f9a2-119">该行为取决于超额支付金额是否介于 0.00 和在**最大超额支付或支付不足**字段中输入的金额之间，或者超额支付金额是否大于**最大超额支付或支付不足**。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-119">The behavior depends on whether the overpayment amount is between 0.00 and the amount that is entered in the **Maximum overpayment or underpayment** field, or whether the overpayment amount is more than the **Maximum overpayment or underpayment** amount.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="7f9a2-120">方案 1</span><span class="sxs-lookup"><span data-stu-id="7f9a2-120">Scenario 1</span></span>

<span data-ttu-id="7f9a2-121">在此方案中，超额支付金额介于 0.00 和最大超额支付或支付不足之间。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-121">In this scenario, the overpayment amount is between 0.00 and the maximum overpayment or underpayment.</span></span> <span data-ttu-id="7f9a2-122">如果在七日内支付发票款项，则开具面额为 105.00 的发票，且提供现金折扣。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-122">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="7f9a2-123">发票合计</span><span class="sxs-lookup"><span data-stu-id="7f9a2-123">Invoice total</span></span> | <span data-ttu-id="7f9a2-124">可用的现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-124">Cash discount available</span></span> | <span data-ttu-id="7f9a2-125">要支付的金额，其中包括现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-125">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="7f9a2-126">105.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-126">105.00</span></span>        | <span data-ttu-id="7f9a2-127">1050</span><span class="sxs-lookup"><span data-stu-id="7f9a2-127">10.50</span></span>                   | <span data-ttu-id="7f9a2-128">94.50</span><span class="sxs-lookup"><span data-stu-id="7f9a2-128">94.50</span></span>                                               |

<span data-ttu-id="7f9a2-129">客户在现金折扣期间内提交 95.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-129">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="7f9a2-130">付款结算到面额为 105.00 的发票。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-130">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="7f9a2-131">在发票和付款结算后，会在客户的应收账款中创建以下交易记录。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-131">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="7f9a2-132">事务</span><span class="sxs-lookup"><span data-stu-id="7f9a2-132">Transaction</span></span>   | <span data-ttu-id="7f9a2-133">金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-133">Amount</span></span> | <span data-ttu-id="7f9a2-134">余额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-134">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="7f9a2-135">开票</span><span class="sxs-lookup"><span data-stu-id="7f9a2-135">Invoice</span></span>       | <span data-ttu-id="7f9a2-136">105.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-136">105.00</span></span> | <span data-ttu-id="7f9a2-137">0.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-137">0.00</span></span>    |
| <span data-ttu-id="7f9a2-138">付款</span><span class="sxs-lookup"><span data-stu-id="7f9a2-138">Payment</span></span>       | <span data-ttu-id="7f9a2-139">-95.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-139">-95.00</span></span> | <span data-ttu-id="7f9a2-140">0.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-140">0.00</span></span>    |
| <span data-ttu-id="7f9a2-141">现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-141">Cash discount</span></span> | <span data-ttu-id="7f9a2-142">-10.50</span><span class="sxs-lookup"><span data-stu-id="7f9a2-142">-10.50</span></span> | <span data-ttu-id="7f9a2-143">0.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-143">0.00</span></span>    |

<span data-ttu-id="7f9a2-144">将为付款和结算下列以下会计条目。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-144">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="7f9a2-145">**付款**</span><span class="sxs-lookup"><span data-stu-id="7f9a2-145">**Payment**</span></span>

| <span data-ttu-id="7f9a2-146">帐户</span><span class="sxs-lookup"><span data-stu-id="7f9a2-146">Account</span></span>             | <span data-ttu-id="7f9a2-147">借方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-147">Debit amount</span></span> | <span data-ttu-id="7f9a2-148">贷方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-148">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="7f9a2-149">现金</span><span class="sxs-lookup"><span data-stu-id="7f9a2-149">Cash</span></span>                | <span data-ttu-id="7f9a2-150">95.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-150">95.00</span></span>        |               |
| <span data-ttu-id="7f9a2-151">应收账款</span><span class="sxs-lookup"><span data-stu-id="7f9a2-151">Accounts receivable</span></span> |              | <span data-ttu-id="7f9a2-152">95.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-152">95.00</span></span>         |

<span data-ttu-id="7f9a2-153">**结算**</span><span class="sxs-lookup"><span data-stu-id="7f9a2-153">**Settlement**</span></span>

| <span data-ttu-id="7f9a2-154">帐户</span><span class="sxs-lookup"><span data-stu-id="7f9a2-154">Account</span></span>                                                                                                          | <span data-ttu-id="7f9a2-155">借方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-155">Debit amount</span></span> | <span data-ttu-id="7f9a2-156">贷方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-156">Credit amount</span></span> |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="7f9a2-157">现金折扣（**现金折扣**页面上的**客户折扣的主科目**字段）</span><span class="sxs-lookup"><span data-stu-id="7f9a2-157">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span>                 | <span data-ttu-id="7f9a2-158">1050</span><span class="sxs-lookup"><span data-stu-id="7f9a2-158">10.50</span></span>        |               |
| <span data-ttu-id="7f9a2-159">应收账款</span><span class="sxs-lookup"><span data-stu-id="7f9a2-159">Accounts receivable</span></span>                                                                                              |              | <span data-ttu-id="7f9a2-160">1050</span><span class="sxs-lookup"><span data-stu-id="7f9a2-160">10.50</span></span>         |
| <span data-ttu-id="7f9a2-161">客户现金折扣（**自动交易记录帐户**页面上的**客户现金折扣**字段）</span><span class="sxs-lookup"><span data-stu-id="7f9a2-161">Customer cash discount (the **Customer cash discount** field on the **Account for automatic transactions** page)</span></span> |              | <span data-ttu-id="7f9a2-162">0.50</span><span class="sxs-lookup"><span data-stu-id="7f9a2-162">0.50</span></span>          |
| <span data-ttu-id="7f9a2-163">应收账款</span><span class="sxs-lookup"><span data-stu-id="7f9a2-163">Accounts receivable</span></span>                                                                                              | <span data-ttu-id="7f9a2-164">0.50</span><span class="sxs-lookup"><span data-stu-id="7f9a2-164">0.50</span></span>         |               |

### <a name="scenario-2"></a><span data-ttu-id="7f9a2-165">方案 2</span><span class="sxs-lookup"><span data-stu-id="7f9a2-165">Scenario 2</span></span>

<span data-ttu-id="7f9a2-166">在此方案中，超额支付金额高于最大超额支付或支付不足金额。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-166">In this scenario, the overpayment amount exceeds the maximum overpayment or underpayment amount.</span></span> <span data-ttu-id="7f9a2-167">如果在七日内支付发票款项，则开具面额为 105.00 的发票，且提供现金折扣。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-167">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="7f9a2-168">发票合计</span><span class="sxs-lookup"><span data-stu-id="7f9a2-168">Invoice total</span></span> | <span data-ttu-id="7f9a2-169">可用的现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-169">Cash discount available</span></span> | <span data-ttu-id="7f9a2-170">要支付的金额，其中包括现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-170">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="7f9a2-171">105.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-171">105.00</span></span>        | <span data-ttu-id="7f9a2-172">1050</span><span class="sxs-lookup"><span data-stu-id="7f9a2-172">10.50</span></span>                   | <span data-ttu-id="7f9a2-173">94.50</span><span class="sxs-lookup"><span data-stu-id="7f9a2-173">94.50</span></span>                                               |

<span data-ttu-id="7f9a2-174">客户在现金折扣期间内提交 95.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-174">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="7f9a2-175">付款结算到面额为 105.00 的发票。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-175">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="7f9a2-176">在发票和付款结算后，会在客户的应收账款中创建以下交易记录。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-176">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="7f9a2-177">事务</span><span class="sxs-lookup"><span data-stu-id="7f9a2-177">Transaction</span></span>   | <span data-ttu-id="7f9a2-178">金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-178">Amount</span></span> | <span data-ttu-id="7f9a2-179">余额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-179">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="7f9a2-180">开票</span><span class="sxs-lookup"><span data-stu-id="7f9a2-180">Invoice</span></span>       | <span data-ttu-id="7f9a2-181">105.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-181">105.00</span></span> | <span data-ttu-id="7f9a2-182">0.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-182">0.00</span></span>    |
| <span data-ttu-id="7f9a2-183">付款</span><span class="sxs-lookup"><span data-stu-id="7f9a2-183">Payment</span></span>       | <span data-ttu-id="7f9a2-184">-95.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-184">-95.00</span></span> | <span data-ttu-id="7f9a2-185">-0.50</span><span class="sxs-lookup"><span data-stu-id="7f9a2-185">-0.50</span></span>   |
| <span data-ttu-id="7f9a2-186">现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-186">Cash discount</span></span> | <span data-ttu-id="7f9a2-187">-10.50</span><span class="sxs-lookup"><span data-stu-id="7f9a2-187">-10.50</span></span> | <span data-ttu-id="7f9a2-188">0.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-188">0.00</span></span>    |

<span data-ttu-id="7f9a2-189">超额付款金额 0.50，将作为未结余额留在付款中，可以结算到另一张发票。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-189">The overpayment amount of 0.50 will remain as an open balance on the payment and can be settled against another invoice.</span></span> <span data-ttu-id="7f9a2-190">将为付款和结算下列以下会计条目。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-190">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="7f9a2-191">**付款**</span><span class="sxs-lookup"><span data-stu-id="7f9a2-191">**Payment**</span></span>

| <span data-ttu-id="7f9a2-192">帐户</span><span class="sxs-lookup"><span data-stu-id="7f9a2-192">Account</span></span>             | <span data-ttu-id="7f9a2-193">借方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-193">Debit amount</span></span> | <span data-ttu-id="7f9a2-194">贷方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-194">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="7f9a2-195">现金</span><span class="sxs-lookup"><span data-stu-id="7f9a2-195">Cash</span></span>                | <span data-ttu-id="7f9a2-196">95.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-196">95.00</span></span>        |               |
| <span data-ttu-id="7f9a2-197">应收账款</span><span class="sxs-lookup"><span data-stu-id="7f9a2-197">Accounts receivable</span></span> |              | <span data-ttu-id="7f9a2-198">95.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-198">95.00</span></span>         |

<span data-ttu-id="7f9a2-199">**结算**</span><span class="sxs-lookup"><span data-stu-id="7f9a2-199">**Settlement**</span></span>

| <span data-ttu-id="7f9a2-200">帐户</span><span class="sxs-lookup"><span data-stu-id="7f9a2-200">Account</span></span>                                                                                          | <span data-ttu-id="7f9a2-201">借方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-201">Debit amount</span></span> | <span data-ttu-id="7f9a2-202">贷方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-202">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="7f9a2-203">现金折扣（**现金折扣**页面上的**客户折扣的主科目**字段）</span><span class="sxs-lookup"><span data-stu-id="7f9a2-203">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="7f9a2-204">1050</span><span class="sxs-lookup"><span data-stu-id="7f9a2-204">10.50</span></span>        |               |
| <span data-ttu-id="7f9a2-205">应收账款</span><span class="sxs-lookup"><span data-stu-id="7f9a2-205">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="7f9a2-206">1050</span><span class="sxs-lookup"><span data-stu-id="7f9a2-206">10.50</span></span>         |

## <a name="cash-discount-administration--unspecific"></a><span data-ttu-id="7f9a2-207">现金折扣管理 = 非特定</span><span class="sxs-lookup"><span data-stu-id="7f9a2-207">Cash discount administration = Unspecific</span></span>
<span data-ttu-id="7f9a2-208">当在**自动交易记录帐户**页面上的**现金折扣管理**字段中选择看**非特定**时，应将现金折扣金额减去超额支付金额。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-208">When **Unspecific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the cash discount amount is reduced by the overpayment amount.</span></span> <span data-ttu-id="7f9a2-209">此行为始终适用，无论超额支付金额高于还是低于在**最大超额支付或支付不足**字段中输入的金额。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-209">This behavior always applies, regardless of whether the overpayment amount is over or under the amount that is entered in the **Maximum overpayment or underpayment** field.</span></span>

### <a name="scenario-3"></a><span data-ttu-id="7f9a2-210">方案 3</span><span class="sxs-lookup"><span data-stu-id="7f9a2-210">Scenario 3</span></span>

<span data-ttu-id="7f9a2-211">在此方案中，如果在七日内支付发票款项，则开具面额为 105.00 的发票，且提供现金折扣。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-211">In this scenario, an invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="7f9a2-212">发票合计</span><span class="sxs-lookup"><span data-stu-id="7f9a2-212">Invoice total</span></span> | <span data-ttu-id="7f9a2-213">可用的现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-213">Cash discount available</span></span> | <span data-ttu-id="7f9a2-214">要支付的金额，其中包括现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-214">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="7f9a2-215">105.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-215">105.00</span></span>        | <span data-ttu-id="7f9a2-216">1050</span><span class="sxs-lookup"><span data-stu-id="7f9a2-216">10.50</span></span>                   | <span data-ttu-id="7f9a2-217">94.50</span><span class="sxs-lookup"><span data-stu-id="7f9a2-217">94.50</span></span>                                               |

<span data-ttu-id="7f9a2-218">客户在现金折扣期间内提交 95.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-218">The customer submits a payment for 95.00 within the cash discount date.</span></span> <span data-ttu-id="7f9a2-219">付款结算到面额为 105.00 的发票。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-219">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="7f9a2-220">在发票和付款结算后，会在客户的应收账款中创建以下交易记录。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-220">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="7f9a2-221">事务</span><span class="sxs-lookup"><span data-stu-id="7f9a2-221">Transaction</span></span>   | <span data-ttu-id="7f9a2-222">金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-222">Amount</span></span> | <span data-ttu-id="7f9a2-223">余额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-223">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="7f9a2-224">开票</span><span class="sxs-lookup"><span data-stu-id="7f9a2-224">Invoice</span></span>       | <span data-ttu-id="7f9a2-225">105.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-225">105.00</span></span> | <span data-ttu-id="7f9a2-226">0.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-226">0.00</span></span>    |
| <span data-ttu-id="7f9a2-227">付款</span><span class="sxs-lookup"><span data-stu-id="7f9a2-227">Payment</span></span>       | <span data-ttu-id="7f9a2-228">-95.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-228">-95.00</span></span> | <span data-ttu-id="7f9a2-229">-0.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-229">-0.00</span></span>   |
| <span data-ttu-id="7f9a2-230">现金折扣</span><span class="sxs-lookup"><span data-stu-id="7f9a2-230">Cash discount</span></span> | <span data-ttu-id="7f9a2-231">-10.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-231">-10.00</span></span> | <span data-ttu-id="7f9a2-232">0.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-232">0.00</span></span>    |

<span data-ttu-id="7f9a2-233">现金折扣金额由 10.50 降到 10.00。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-233">The cash discount amount is reduced from 10.50 to 10.00.</span></span> <span data-ttu-id="7f9a2-234">付款和发票被视为已结算。</span><span class="sxs-lookup"><span data-stu-id="7f9a2-234">The payment and invoice are considered settled.</span></span> <span data-ttu-id="7f9a2-235">**付款**</span><span class="sxs-lookup"><span data-stu-id="7f9a2-235">**Payment**</span></span>

| <span data-ttu-id="7f9a2-236">帐户</span><span class="sxs-lookup"><span data-stu-id="7f9a2-236">Account</span></span>             | <span data-ttu-id="7f9a2-237">借方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-237">Debit amount</span></span> | <span data-ttu-id="7f9a2-238">贷方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-238">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="7f9a2-239">现金</span><span class="sxs-lookup"><span data-stu-id="7f9a2-239">Cash</span></span>                | <span data-ttu-id="7f9a2-240">95.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-240">95.00</span></span>        |               |
| <span data-ttu-id="7f9a2-241">应收账款</span><span class="sxs-lookup"><span data-stu-id="7f9a2-241">Accounts receivable</span></span> |              | <span data-ttu-id="7f9a2-242">95.00</span><span class="sxs-lookup"><span data-stu-id="7f9a2-242">95.00</span></span>         |

<span data-ttu-id="7f9a2-243">**结算**</span><span class="sxs-lookup"><span data-stu-id="7f9a2-243">**Settlement**</span></span>

| <span data-ttu-id="7f9a2-244">帐户</span><span class="sxs-lookup"><span data-stu-id="7f9a2-244">Account</span></span>                                                                                          | <span data-ttu-id="7f9a2-245">借方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-245">Debit amount</span></span> | <span data-ttu-id="7f9a2-246">贷方金额</span><span class="sxs-lookup"><span data-stu-id="7f9a2-246">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="7f9a2-247">现金折扣（**现金折扣**页面上的**客户折扣的主科目**字段）</span><span class="sxs-lookup"><span data-stu-id="7f9a2-247">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="7f9a2-248">1050</span><span class="sxs-lookup"><span data-stu-id="7f9a2-248">10.50</span></span>        |               |
| <span data-ttu-id="7f9a2-249">应收账款</span><span class="sxs-lookup"><span data-stu-id="7f9a2-249">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="7f9a2-250">1050</span><span class="sxs-lookup"><span data-stu-id="7f9a2-250">10.50</span></span>         |





