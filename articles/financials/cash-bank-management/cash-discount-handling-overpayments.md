---
title: 处理超额支付的现金折扣
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
ms.openlocfilehash: 803cb478bb7631439ebde66ad96182193d3dd1ae
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842513"
---
# <a name="handling-cash-discounts-for-overpayments"></a><span data-ttu-id="d7d6b-103">处理超额支付的现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-103">Handling cash discounts for overpayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7d6b-104">本文提供显示在客户执行现金折扣同时超额支付时如何处理付款的情况。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-104">This article provides scenarios that show how a payment is handled when the customer takes a cash discount but also overpays.</span></span> 

<span data-ttu-id="d7d6b-105">当付款金额高于发票金额减去现金折扣后的金额时，应被视为超额支付。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-105">An invoice is considered overpaid when the payment amount is more than the invoice amount minus the cash discount.</span></span> <span data-ttu-id="d7d6b-106">要指定在超额支付发票时处理可获得的现金折扣差额的方式，请使用**应收账款参数**页面上的**现金折扣管理**和**最大超额支付或支付不足**。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-106">To specify how an obtainable cash discount difference is handled when an invoice is overpaid, use the **Cash discount administration** and **Maximum overpayment or underpayment** fields on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="d7d6b-107">在以下示例中，客户对发票超额支付了 0.50。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-107">In the following example, the customer has overpaid the invoice by 0.50.</span></span>

| <span data-ttu-id="d7d6b-108">发票合计</span><span class="sxs-lookup"><span data-stu-id="d7d6b-108">Invoice total</span></span> | <span data-ttu-id="d7d6b-109">可用的现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-109">Cash discount available</span></span> | <span data-ttu-id="d7d6b-110">要支付的金额，其中包括现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-110">Amount to be paid, which includes the cash discount</span></span> | <span data-ttu-id="d7d6b-111">客户实际支付金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-111">Amount the customer actually pays</span></span> |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="d7d6b-112">105.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-112">105.00</span></span>        | <span data-ttu-id="d7d6b-113">1050</span><span class="sxs-lookup"><span data-stu-id="d7d6b-113">10.50</span></span>                   | <span data-ttu-id="d7d6b-114">94.50</span><span class="sxs-lookup"><span data-stu-id="d7d6b-114">94.50</span></span>                                               | <span data-ttu-id="d7d6b-115">95.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-115">95.00</span></span>                             |

## <a name="cash-discount-administration--specific"></a><span data-ttu-id="d7d6b-116">现金折扣管理 = 特定</span><span class="sxs-lookup"><span data-stu-id="d7d6b-116">Cash discount administration = Specific</span></span>
<span data-ttu-id="d7d6b-117">当在**自动交易记录帐户**页面上的**现金折扣管理**字段中选择看**特定**时，将获得完全现金折扣。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-117">When **Specific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the full cash discount is taken.</span></span> <span data-ttu-id="d7d6b-118">超额支付金额或者被过帐到现金折扣差额分类帐帐户或作为余额留在客户帐户上。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-118">The overpayment amount either is posted to a cash discount difference ledger account or remains a balance on the customer’s account.</span></span> <span data-ttu-id="d7d6b-119">该行为取决于超额支付金额是否介于 0.00 和在**最大超额支付或支付不足**字段中输入的金额之间，或者超额支付金额是否大于**最大超额支付或支付不足**。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-119">The behavior depends on whether the overpayment amount is between 0.00 and the amount that is entered in the **Maximum overpayment or underpayment** field, or whether the overpayment amount is more than the **Maximum overpayment or underpayment** amount.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="d7d6b-120">方案 1</span><span class="sxs-lookup"><span data-stu-id="d7d6b-120">Scenario 1</span></span>

<span data-ttu-id="d7d6b-121">在此方案中，超额支付金额介于 0.00 和最大超额支付或支付不足之间。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-121">In this scenario, the overpayment amount is between 0.00 and the maximum overpayment or underpayment.</span></span> <span data-ttu-id="d7d6b-122">如果在七日内支付发票款项，则开具面额为 105.00 的发票，且提供现金折扣。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-122">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="d7d6b-123">发票合计</span><span class="sxs-lookup"><span data-stu-id="d7d6b-123">Invoice total</span></span> | <span data-ttu-id="d7d6b-124">可用的现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-124">Cash discount available</span></span> | <span data-ttu-id="d7d6b-125">要支付的金额，其中包括现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-125">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="d7d6b-126">105.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-126">105.00</span></span>        | <span data-ttu-id="d7d6b-127">1050</span><span class="sxs-lookup"><span data-stu-id="d7d6b-127">10.50</span></span>                   | <span data-ttu-id="d7d6b-128">94.50</span><span class="sxs-lookup"><span data-stu-id="d7d6b-128">94.50</span></span>                                               |

<span data-ttu-id="d7d6b-129">客户在现金折扣期间内提交 95.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-129">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="d7d6b-130">付款结算到面额为 105.00 的发票。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-130">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="d7d6b-131">在发票和付款结算后，会在客户的应收账款中创建以下交易记录。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-131">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="d7d6b-132">事务</span><span class="sxs-lookup"><span data-stu-id="d7d6b-132">Transaction</span></span>   | <span data-ttu-id="d7d6b-133">金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-133">Amount</span></span> | <span data-ttu-id="d7d6b-134">余额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-134">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="d7d6b-135">开票</span><span class="sxs-lookup"><span data-stu-id="d7d6b-135">Invoice</span></span>       | <span data-ttu-id="d7d6b-136">105.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-136">105.00</span></span> | <span data-ttu-id="d7d6b-137">0.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-137">0.00</span></span>    |
| <span data-ttu-id="d7d6b-138">付款</span><span class="sxs-lookup"><span data-stu-id="d7d6b-138">Payment</span></span>       | <span data-ttu-id="d7d6b-139">-95.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-139">-95.00</span></span> | <span data-ttu-id="d7d6b-140">0.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-140">0.00</span></span>    |
| <span data-ttu-id="d7d6b-141">现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-141">Cash discount</span></span> | <span data-ttu-id="d7d6b-142">-10.50</span><span class="sxs-lookup"><span data-stu-id="d7d6b-142">-10.50</span></span> | <span data-ttu-id="d7d6b-143">0.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-143">0.00</span></span>    |

<span data-ttu-id="d7d6b-144">将为付款和结算下列以下会计条目。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-144">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="d7d6b-145">**付款**</span><span class="sxs-lookup"><span data-stu-id="d7d6b-145">**Payment**</span></span>

| <span data-ttu-id="d7d6b-146">帐户</span><span class="sxs-lookup"><span data-stu-id="d7d6b-146">Account</span></span>             | <span data-ttu-id="d7d6b-147">借方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-147">Debit amount</span></span> | <span data-ttu-id="d7d6b-148">贷方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-148">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="d7d6b-149">现金</span><span class="sxs-lookup"><span data-stu-id="d7d6b-149">Cash</span></span>                | <span data-ttu-id="d7d6b-150">95.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-150">95.00</span></span>        |               |
| <span data-ttu-id="d7d6b-151">应收账款</span><span class="sxs-lookup"><span data-stu-id="d7d6b-151">Accounts receivable</span></span> |              | <span data-ttu-id="d7d6b-152">95.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-152">95.00</span></span>         |

<span data-ttu-id="d7d6b-153">**结算**</span><span class="sxs-lookup"><span data-stu-id="d7d6b-153">**Settlement**</span></span>

| <span data-ttu-id="d7d6b-154">帐户</span><span class="sxs-lookup"><span data-stu-id="d7d6b-154">Account</span></span>                                                                                                          | <span data-ttu-id="d7d6b-155">借方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-155">Debit amount</span></span> | <span data-ttu-id="d7d6b-156">贷方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-156">Credit amount</span></span> |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="d7d6b-157">现金折扣（**现金折扣**页面上的**客户折扣的主科目**字段）</span><span class="sxs-lookup"><span data-stu-id="d7d6b-157">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span>                 | <span data-ttu-id="d7d6b-158">1050</span><span class="sxs-lookup"><span data-stu-id="d7d6b-158">10.50</span></span>        |               |
| <span data-ttu-id="d7d6b-159">应收账款</span><span class="sxs-lookup"><span data-stu-id="d7d6b-159">Accounts receivable</span></span>                                                                                              |              | <span data-ttu-id="d7d6b-160">1050</span><span class="sxs-lookup"><span data-stu-id="d7d6b-160">10.50</span></span>         |
| <span data-ttu-id="d7d6b-161">客户现金折扣（**自动交易记录帐户**页面上的**客户现金折扣**字段）</span><span class="sxs-lookup"><span data-stu-id="d7d6b-161">Customer cash discount (the **Customer cash discount** field on the **Account for automatic transactions** page)</span></span> |              | <span data-ttu-id="d7d6b-162">0.50</span><span class="sxs-lookup"><span data-stu-id="d7d6b-162">0.50</span></span>          |
| <span data-ttu-id="d7d6b-163">应收账款</span><span class="sxs-lookup"><span data-stu-id="d7d6b-163">Accounts receivable</span></span>                                                                                              | <span data-ttu-id="d7d6b-164">0.50</span><span class="sxs-lookup"><span data-stu-id="d7d6b-164">0.50</span></span>         |               |

### <a name="scenario-2"></a><span data-ttu-id="d7d6b-165">方案 2</span><span class="sxs-lookup"><span data-stu-id="d7d6b-165">Scenario 2</span></span>

<span data-ttu-id="d7d6b-166">在此方案中，超额支付金额高于最大超额支付或支付不足金额。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-166">In this scenario, the overpayment amount exceeds the maximum overpayment or underpayment amount.</span></span> <span data-ttu-id="d7d6b-167">如果在七日内支付发票款项，则开具面额为 105.00 的发票，且提供现金折扣。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-167">An invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="d7d6b-168">发票合计</span><span class="sxs-lookup"><span data-stu-id="d7d6b-168">Invoice total</span></span> | <span data-ttu-id="d7d6b-169">可用的现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-169">Cash discount available</span></span> | <span data-ttu-id="d7d6b-170">要支付的金额，其中包括现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-170">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="d7d6b-171">105.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-171">105.00</span></span>        | <span data-ttu-id="d7d6b-172">1050</span><span class="sxs-lookup"><span data-stu-id="d7d6b-172">10.50</span></span>                   | <span data-ttu-id="d7d6b-173">94.50</span><span class="sxs-lookup"><span data-stu-id="d7d6b-173">94.50</span></span>                                               |

<span data-ttu-id="d7d6b-174">客户在现金折扣期间内提交 95.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-174">The customer submits a payment for 95.00 within the cash discount period.</span></span> <span data-ttu-id="d7d6b-175">付款结算到面额为 105.00 的发票。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-175">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="d7d6b-176">在发票和付款结算后，会在客户的应收账款中创建以下交易记录。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-176">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="d7d6b-177">事务</span><span class="sxs-lookup"><span data-stu-id="d7d6b-177">Transaction</span></span>   | <span data-ttu-id="d7d6b-178">金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-178">Amount</span></span> | <span data-ttu-id="d7d6b-179">余额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-179">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="d7d6b-180">开票</span><span class="sxs-lookup"><span data-stu-id="d7d6b-180">Invoice</span></span>       | <span data-ttu-id="d7d6b-181">105.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-181">105.00</span></span> | <span data-ttu-id="d7d6b-182">0.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-182">0.00</span></span>    |
| <span data-ttu-id="d7d6b-183">付款</span><span class="sxs-lookup"><span data-stu-id="d7d6b-183">Payment</span></span>       | <span data-ttu-id="d7d6b-184">-95.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-184">-95.00</span></span> | <span data-ttu-id="d7d6b-185">-0.50</span><span class="sxs-lookup"><span data-stu-id="d7d6b-185">-0.50</span></span>   |
| <span data-ttu-id="d7d6b-186">现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-186">Cash discount</span></span> | <span data-ttu-id="d7d6b-187">-10.50</span><span class="sxs-lookup"><span data-stu-id="d7d6b-187">-10.50</span></span> | <span data-ttu-id="d7d6b-188">0.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-188">0.00</span></span>    |

<span data-ttu-id="d7d6b-189">超额付款金额 0.50，将作为未结余额留在付款中，可以结算到另一张发票。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-189">The overpayment amount of 0.50 will remain as an open balance on the payment and can be settled against another invoice.</span></span> <span data-ttu-id="d7d6b-190">将为付款和结算下列以下会计条目。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-190">The following accounting entries are generated for the payment and the settlement.</span></span> <span data-ttu-id="d7d6b-191">**付款**</span><span class="sxs-lookup"><span data-stu-id="d7d6b-191">**Payment**</span></span>

| <span data-ttu-id="d7d6b-192">帐户</span><span class="sxs-lookup"><span data-stu-id="d7d6b-192">Account</span></span>             | <span data-ttu-id="d7d6b-193">借方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-193">Debit amount</span></span> | <span data-ttu-id="d7d6b-194">贷方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-194">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="d7d6b-195">现金</span><span class="sxs-lookup"><span data-stu-id="d7d6b-195">Cash</span></span>                | <span data-ttu-id="d7d6b-196">95.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-196">95.00</span></span>        |               |
| <span data-ttu-id="d7d6b-197">应收账款</span><span class="sxs-lookup"><span data-stu-id="d7d6b-197">Accounts receivable</span></span> |              | <span data-ttu-id="d7d6b-198">95.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-198">95.00</span></span>         |

<span data-ttu-id="d7d6b-199">**结算**</span><span class="sxs-lookup"><span data-stu-id="d7d6b-199">**Settlement**</span></span>

| <span data-ttu-id="d7d6b-200">帐户</span><span class="sxs-lookup"><span data-stu-id="d7d6b-200">Account</span></span>                                                                                          | <span data-ttu-id="d7d6b-201">借方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-201">Debit amount</span></span> | <span data-ttu-id="d7d6b-202">贷方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-202">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="d7d6b-203">现金折扣（**现金折扣**页面上的**客户折扣的主科目**字段）</span><span class="sxs-lookup"><span data-stu-id="d7d6b-203">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="d7d6b-204">1050</span><span class="sxs-lookup"><span data-stu-id="d7d6b-204">10.50</span></span>        |               |
| <span data-ttu-id="d7d6b-205">应收账款</span><span class="sxs-lookup"><span data-stu-id="d7d6b-205">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="d7d6b-206">1050</span><span class="sxs-lookup"><span data-stu-id="d7d6b-206">10.50</span></span>         |

## <a name="cash-discount-administration--unspecific"></a><span data-ttu-id="d7d6b-207">现金折扣管理 = 非特定</span><span class="sxs-lookup"><span data-stu-id="d7d6b-207">Cash discount administration = Unspecific</span></span>
<span data-ttu-id="d7d6b-208">当在**自动交易记录帐户**页面上的**现金折扣管理**字段中选择看**非特定**时，应将现金折扣金额减去超额支付金额。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-208">When **Unspecific** is selected in the **Cash discount administration** field on the **Accounts for automatic transactions** page, the cash discount amount is reduced by the overpayment amount.</span></span> <span data-ttu-id="d7d6b-209">此行为始终适用，无论超额支付金额高于还是低于在**最大超额支付或支付不足**字段中输入的金额。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-209">This behavior always applies, regardless of whether the overpayment amount is over or under the amount that is entered in the **Maximum overpayment or underpayment** field.</span></span>

### <a name="scenario-3"></a><span data-ttu-id="d7d6b-210">方案 3</span><span class="sxs-lookup"><span data-stu-id="d7d6b-210">Scenario 3</span></span>

<span data-ttu-id="d7d6b-211">在此方案中，如果在七日内支付发票款项，则开具面额为 105.00 的发票，且提供现金折扣。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-211">In this scenario, an invoice for 105.00 is entered, and a cash discount is available if the invoice is paid within seven days.</span></span>

| <span data-ttu-id="d7d6b-212">发票合计</span><span class="sxs-lookup"><span data-stu-id="d7d6b-212">Invoice total</span></span> | <span data-ttu-id="d7d6b-213">可用的现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-213">Cash discount available</span></span> | <span data-ttu-id="d7d6b-214">要支付的金额，其中包括现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-214">Amount to be paid, which includes the cash discount</span></span> |
|---------------|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="d7d6b-215">105.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-215">105.00</span></span>        | <span data-ttu-id="d7d6b-216">1050</span><span class="sxs-lookup"><span data-stu-id="d7d6b-216">10.50</span></span>                   | <span data-ttu-id="d7d6b-217">94.50</span><span class="sxs-lookup"><span data-stu-id="d7d6b-217">94.50</span></span>                                               |

<span data-ttu-id="d7d6b-218">客户在现金折扣期间内提交 95.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-218">The customer submits a payment for 95.00 within the cash discount date.</span></span> <span data-ttu-id="d7d6b-219">付款结算到面额为 105.00 的发票。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-219">The payment is settled against the invoice for 105.00.</span></span> <span data-ttu-id="d7d6b-220">在发票和付款结算后，会在客户的应收账款中创建以下交易记录。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-220">After the invoice and payment are settled, the following transactions are created for the customer in Accounts receivable.</span></span>

| <span data-ttu-id="d7d6b-221">事务</span><span class="sxs-lookup"><span data-stu-id="d7d6b-221">Transaction</span></span>   | <span data-ttu-id="d7d6b-222">金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-222">Amount</span></span> | <span data-ttu-id="d7d6b-223">余额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-223">Balance</span></span> |
|---------------|--------|---------|
| <span data-ttu-id="d7d6b-224">开票</span><span class="sxs-lookup"><span data-stu-id="d7d6b-224">Invoice</span></span>       | <span data-ttu-id="d7d6b-225">105.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-225">105.00</span></span> | <span data-ttu-id="d7d6b-226">0.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-226">0.00</span></span>    |
| <span data-ttu-id="d7d6b-227">付款</span><span class="sxs-lookup"><span data-stu-id="d7d6b-227">Payment</span></span>       | <span data-ttu-id="d7d6b-228">-95.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-228">-95.00</span></span> | <span data-ttu-id="d7d6b-229">-0.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-229">-0.00</span></span>   |
| <span data-ttu-id="d7d6b-230">现金折扣</span><span class="sxs-lookup"><span data-stu-id="d7d6b-230">Cash discount</span></span> | <span data-ttu-id="d7d6b-231">-10.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-231">-10.00</span></span> | <span data-ttu-id="d7d6b-232">0.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-232">0.00</span></span>    |

<span data-ttu-id="d7d6b-233">现金折扣金额由 10.50 降到 10.00。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-233">The cash discount amount is reduced from 10.50 to 10.00.</span></span> <span data-ttu-id="d7d6b-234">付款和发票被视为已结算。</span><span class="sxs-lookup"><span data-stu-id="d7d6b-234">The payment and invoice are considered settled.</span></span> <span data-ttu-id="d7d6b-235">**付款**</span><span class="sxs-lookup"><span data-stu-id="d7d6b-235">**Payment**</span></span>

| <span data-ttu-id="d7d6b-236">帐户</span><span class="sxs-lookup"><span data-stu-id="d7d6b-236">Account</span></span>             | <span data-ttu-id="d7d6b-237">借方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-237">Debit amount</span></span> | <span data-ttu-id="d7d6b-238">贷方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-238">Credit amount</span></span> |
|---------------------|--------------|---------------|
| <span data-ttu-id="d7d6b-239">现金</span><span class="sxs-lookup"><span data-stu-id="d7d6b-239">Cash</span></span>                | <span data-ttu-id="d7d6b-240">95.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-240">95.00</span></span>        |               |
| <span data-ttu-id="d7d6b-241">应收账款</span><span class="sxs-lookup"><span data-stu-id="d7d6b-241">Accounts receivable</span></span> |              | <span data-ttu-id="d7d6b-242">95.00</span><span class="sxs-lookup"><span data-stu-id="d7d6b-242">95.00</span></span>         |

<span data-ttu-id="d7d6b-243">**结算**</span><span class="sxs-lookup"><span data-stu-id="d7d6b-243">**Settlement**</span></span>

| <span data-ttu-id="d7d6b-244">帐户</span><span class="sxs-lookup"><span data-stu-id="d7d6b-244">Account</span></span>                                                                                          | <span data-ttu-id="d7d6b-245">借方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-245">Debit amount</span></span> | <span data-ttu-id="d7d6b-246">贷方金额</span><span class="sxs-lookup"><span data-stu-id="d7d6b-246">Credit amount</span></span> |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| <span data-ttu-id="d7d6b-247">现金折扣（**现金折扣**页面上的**客户折扣的主科目**字段）</span><span class="sxs-lookup"><span data-stu-id="d7d6b-247">Cash discount (the **Main account for customer discounts** field on the **Cash discounts** page)</span></span> | <span data-ttu-id="d7d6b-248">1050</span><span class="sxs-lookup"><span data-stu-id="d7d6b-248">10.50</span></span>        |               |
| <span data-ttu-id="d7d6b-249">应收账款</span><span class="sxs-lookup"><span data-stu-id="d7d6b-249">Accounts receivable</span></span>                                                                              |              | <span data-ttu-id="d7d6b-250">1050</span><span class="sxs-lookup"><span data-stu-id="d7d6b-250">10.50</span></span>         |





