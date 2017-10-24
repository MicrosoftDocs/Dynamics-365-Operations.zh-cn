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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6327d9cab1651d22cd411f718f6e3a2f8733e13e
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="centralized-payments-for-accounts-receivable"></a><span data-ttu-id="e61d3-105">应收账款的集中付款</span><span class="sxs-lookup"><span data-stu-id="e61d3-105">Centralized payments for Accounts receivable</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e61d3-106">包括多个法人的组织可以使用处理所有付款的单个法人创建和管理付款。</span><span class="sxs-lookup"><span data-stu-id="e61d3-106">Organizations that include multiple legal entities can create and manage payments by using a single legal entity that handles all payments.</span></span> <span data-ttu-id="e61d3-107">因此，不必在多个法人中输入同一交易记录。</span><span class="sxs-lookup"><span data-stu-id="e61d3-107">Therefore, the same transaction doesn't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="e61d3-108">本文提供显示集中付款过帐如何在不同环境中处理的示例。</span><span class="sxs-lookup"><span data-stu-id="e61d3-108">This article provides examples that show how posting for centralized payments is handled in various scenarios.</span></span>

<span data-ttu-id="e61d3-109">包括多个法人的组织可以使用处理所有付款的法人创建和管理付款。</span><span class="sxs-lookup"><span data-stu-id="e61d3-109">Organizations that include multiple legal entities can create and manage payments by using a legal entity that handles all payments.</span></span> <span data-ttu-id="e61d3-110">因此，不必在多个法人中输入同一交易记录。</span><span class="sxs-lookup"><span data-stu-id="e61d3-110">Therefore, the same transaction doesn't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="e61d3-111">此外，组织也节省时间，因为针对集中付款，付款方案、结算以及编辑未结和已结交易记录的流程已简化。</span><span class="sxs-lookup"><span data-stu-id="e61d3-111">Additionally, the organization saves time, because the processes for payment proposals, settlements, and editing open and closed transactions for centralized payments are streamlined.</span></span> 

<span data-ttu-id="e61d3-112">在集中式付款的组织中，有很多营业的法人，且每个营业的法人都管理自己的发票应收信息。</span><span class="sxs-lookup"><span data-stu-id="e61d3-112">In a centralized payment organization, there are many legal entities for operations, and each operating legal entity manages its own invoices receivable information.</span></span> <span data-ttu-id="e61d3-113">所有营业的法人的付款都是由称作付款的法人的单个法人接收的。</span><span class="sxs-lookup"><span data-stu-id="e61d3-113">Payments for all the operating legal entities are received by a single legal entity, which is known as the legal entity of the payment.</span></span> <span data-ttu-id="e61d3-114">在结算流程中，生成适用的应付和应收交易记录。</span><span class="sxs-lookup"><span data-stu-id="e61d3-114">During the settlement process, the applicable due-to and due-from transactions are generated.</span></span> <span data-ttu-id="e61d3-115">您可以指定组织内的哪个法人接收已有收益或已有损失交易记录，以及如何处理与集中式付款相关的现金折扣交易记录。</span><span class="sxs-lookup"><span data-stu-id="e61d3-115">You can specify which legal entity in the organization receives the realized gain or realized loss transactions, and how cash discount transactions that are related to a centralized payment are handled.</span></span> 

<span data-ttu-id="e61d3-116">以下示例说明如何在不同的环境中处理过帐。</span><span class="sxs-lookup"><span data-stu-id="e61d3-116">The following examples illustrate how posting is handled in various scenarios.</span></span> <span data-ttu-id="e61d3-117">假定所有这些示例都采用以下配置：</span><span class="sxs-lookup"><span data-stu-id="e61d3-117">The following configuration is assumed for all these examples:</span></span>

-   <span data-ttu-id="e61d3-118">法人分别为 Fabrikam、Fabrikam East 和 Fabrikam West。</span><span class="sxs-lookup"><span data-stu-id="e61d3-118">The legal entities are Fabrikam, Fabrikam East, and Fabrikam West.</span></span> <span data-ttu-id="e61d3-119">客户付款输入 Fabrikam。</span><span class="sxs-lookup"><span data-stu-id="e61d3-119">Customer payments are entered into Fabrikam.</span></span>
-   <span data-ttu-id="e61d3-120">**“内部公司”**页上的**“过帐现金折扣”**字段设置为**“发票法人”**。</span><span class="sxs-lookup"><span data-stu-id="e61d3-120">The **Post cash discount** field on the **Intercompany accounting** page is set to **Legal entity of the invoice**.</span></span>
-   <span data-ttu-id="e61d3-121">**“内部公司”**页上的**“过帐币种汇兑损益”**字段设置为**“付款法人”**。</span><span class="sxs-lookup"><span data-stu-id="e61d3-121">The **Post currency exchange gain or loss** field on the **Intercompany accounting** page is set to **Legal entity of the payment**.</span></span>
-   <span data-ttu-id="e61d3-122">客户 Northwind Traders 在每个法人中设置为一个客户。</span><span class="sxs-lookup"><span data-stu-id="e61d3-122">Customer Northwind Traders is set up as a customer in each legal entity.</span></span> <span data-ttu-id="e61d3-123">来自不同法人的客户被标识为同一客户，因为他们共享相同的全球通讯簿 ID。</span><span class="sxs-lookup"><span data-stu-id="e61d3-123">The customers from the various legal entities are identified as the same customer because they share the same global address book ID.</span></span>

| <span data-ttu-id="e61d3-124">通讯簿 ID</span><span class="sxs-lookup"><span data-stu-id="e61d3-124">Address book ID</span></span> | <span data-ttu-id="e61d3-125">客户帐户</span><span class="sxs-lookup"><span data-stu-id="e61d3-125">Customer account</span></span> | <span data-ttu-id="e61d3-126">姓名</span><span class="sxs-lookup"><span data-stu-id="e61d3-126">Name</span></span>              | <span data-ttu-id="e61d3-127">法人</span><span class="sxs-lookup"><span data-stu-id="e61d3-127">Legal entity</span></span>  |
|-----------------|------------------|-------------------|---------------|
| <span data-ttu-id="e61d3-128">4050</span><span class="sxs-lookup"><span data-stu-id="e61d3-128">4050</span></span>            | <span data-ttu-id="e61d3-129">4000</span><span class="sxs-lookup"><span data-stu-id="e61d3-129">4000</span></span>             | <span data-ttu-id="e61d3-130">Northwind Traders</span><span class="sxs-lookup"><span data-stu-id="e61d3-130">Northwind Traders</span></span> | <span data-ttu-id="e61d3-131">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e61d3-131">Fabrikam</span></span>      |
| <span data-ttu-id="e61d3-132">4050</span><span class="sxs-lookup"><span data-stu-id="e61d3-132">4050</span></span>            | <span data-ttu-id="e61d3-133">4000</span><span class="sxs-lookup"><span data-stu-id="e61d3-133">4000</span></span>             | <span data-ttu-id="e61d3-134">Northwind Traders</span><span class="sxs-lookup"><span data-stu-id="e61d3-134">Northwind Traders</span></span> | <span data-ttu-id="e61d3-135">Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="e61d3-135">Fabrikam East</span></span> |
| <span data-ttu-id="e61d3-136">4050</span><span class="sxs-lookup"><span data-stu-id="e61d3-136">4050</span></span>            | <span data-ttu-id="e61d3-137">10000</span><span class="sxs-lookup"><span data-stu-id="e61d3-137">10000</span></span>            | <span data-ttu-id="e61d3-138">Northwind Traders</span><span class="sxs-lookup"><span data-stu-id="e61d3-138">Northwind Traders</span></span> | <span data-ttu-id="e61d3-139">Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="e61d3-139">Fabrikam West</span></span> |

## <a name="example-1-customer-payment-of-invoice-from-another-legal-entity"></a><span data-ttu-id="e61d3-140">示例 1：来自其他法人的发票的客户付款</span><span class="sxs-lookup"><span data-stu-id="e61d3-140">Example 1: Customer payment of invoice from another legal entity</span></span>
<span data-ttu-id="e61d3-141">Fabrikam 为 Fabrikam 客户帐户 4000 (Northwind Traders) 收到了金额为 600.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="e61d3-141">Fabrikam receives a payment of 600.00 for Fabrikam customer account 4000, Northwind Traders.</span></span> <span data-ttu-id="e61d3-142">该付款用 Fabrikam East 中的客户帐户 4000 的未结发票结算。</span><span class="sxs-lookup"><span data-stu-id="e61d3-142">The payment is settled with an open invoice for customer account 4000 in Fabrikam East.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-customer-4000"></a><span data-ttu-id="e61d3-143">在 Fabrikam East 中为客户 4000 过帐发票</span><span class="sxs-lookup"><span data-stu-id="e61d3-143">Invoice is posted in Fabrikam East for customer 4000</span></span>

| <span data-ttu-id="e61d3-144">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-144">Account</span></span>                             | <span data-ttu-id="e61d3-145">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-145">Debit amount</span></span> | <span data-ttu-id="e61d3-146">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-146">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-147">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-147">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="e61d3-148">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-148">600.00</span></span>       |               |
| <span data-ttu-id="e61d3-149">销售 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-149">Sales (Fabrikam East)</span></span>               |              | <span data-ttu-id="e61d3-150">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-150">600.00</span></span>        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a><span data-ttu-id="e61d3-151">在 Fabrikam 中为客户 4000 接收和过帐付款</span><span class="sxs-lookup"><span data-stu-id="e61d3-151">Payment is received and posted in Fabrikam for customer 4000</span></span>

| <span data-ttu-id="e61d3-152">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-152">Account</span></span>                        | <span data-ttu-id="e61d3-153">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-153">Debit amount</span></span> | <span data-ttu-id="e61d3-154">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-154">Credit amount</span></span> |
|--------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-155">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-155">Cash (Fabrikam)</span></span>                | <span data-ttu-id="e61d3-156">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-156">600.00</span></span>       |               |
| <span data-ttu-id="e61d3-157">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-157">Accounts receivable (Fabrikam)</span></span> |              | <span data-ttu-id="e61d3-158">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-158">600.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="e61d3-159">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="e61d3-159">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="e61d3-160">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-160">**Fabrikam posting**</span></span>

| <span data-ttu-id="e61d3-161">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-161">Account</span></span>                         | <span data-ttu-id="e61d3-162">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-162">Debit amount</span></span> | <span data-ttu-id="e61d3-163">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-163">Credit amount</span></span> |
|---------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-164">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-164">Accounts receivable (Fabrikam)</span></span>  | <span data-ttu-id="e61d3-165">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-165">600.00</span></span>       |               |
| <span data-ttu-id="e61d3-166">向 Fabrikam East (Fabrikam) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-166">Due to Fabrikam East (Fabrikam)</span></span> |              | <span data-ttu-id="e61d3-167">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-167">600.00</span></span>        |

<span data-ttu-id="e61d3-168">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-168">**Fabrikam East posting**</span></span>

| <span data-ttu-id="e61d3-169">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-169">Account</span></span>                             | <span data-ttu-id="e61d3-170">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-170">Debit amount</span></span> | <span data-ttu-id="e61d3-171">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-171">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-172">从 Fabrikam (Fabrikam East) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-172">Due from Fabrikam (Fabrikam East)</span></span>   | <span data-ttu-id="e61d3-173">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-173">600.00</span></span>       |               |
| <span data-ttu-id="e61d3-174">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-174">Accounts receivable (Fabrikam East)</span></span> |              | <span data-ttu-id="e61d3-175">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-175">600.00</span></span>        |

## <a name="example-2-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a><span data-ttu-id="e61d3-176">示例 2：来自具有现金折扣的其他法人的发票的客户付款</span><span class="sxs-lookup"><span data-stu-id="e61d3-176">Example 2: Customer payment of invoice from another legal entity with cash discount</span></span>
<span data-ttu-id="e61d3-177">Fabrikam 为 Fabrikam 客户帐户 4000 (Northwind Traders) 收到了金额为 580.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="e61d3-177">Fabrikam receives a payment of 580.00 for Fabrikam customer 4000, Northwind Traders.</span></span> <span data-ttu-id="e61d3-178">Fabrikam East 为客户 4000 (Fourth Coffee) 具有一个未结发票。</span><span class="sxs-lookup"><span data-stu-id="e61d3-178">Fabrikam East has an open invoice for customer 4000.</span></span> <span data-ttu-id="e61d3-179">该发票具有 20.00 的可用现金折扣。</span><span class="sxs-lookup"><span data-stu-id="e61d3-179">The invoice has a 20.00 cash discount available.</span></span> <span data-ttu-id="e61d3-180">该付款用未结 Fabrikam East 发票结算。</span><span class="sxs-lookup"><span data-stu-id="e61d3-180">The payment is settled with the open Fabrikam East invoices.</span></span> <span data-ttu-id="e61d3-181">该现金折扣过帐到发票法人 Fabrikam East。</span><span class="sxs-lookup"><span data-stu-id="e61d3-181">The cash discount is posted to the legal entity of the invoice, Fabrikam East.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a><span data-ttu-id="e61d3-182">在 Fabrikam East 中为 Fabrikam East 客户 4000 过帐发票</span><span class="sxs-lookup"><span data-stu-id="e61d3-182">Invoice is posted in Fabrikam East for Fabrikam East customer 4000</span></span>

| <span data-ttu-id="e61d3-183">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-183">Account</span></span>                             | <span data-ttu-id="e61d3-184">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-184">Debit amount</span></span> | <span data-ttu-id="e61d3-185">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-185">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-186">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-186">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="e61d3-187">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-187">600.00</span></span>       |               |
| <span data-ttu-id="e61d3-188">销售 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-188">Sales (Fabrikam East)</span></span>               |              | <span data-ttu-id="e61d3-189">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-189">600.00</span></span>        |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a><span data-ttu-id="e61d3-190">在 Fabrikam 中为 Fabrikam 客户 4000 接收和过帐付款</span><span class="sxs-lookup"><span data-stu-id="e61d3-190">Payment is received and posted in Fabrikam for Fabrikam customer 4000</span></span>

| <span data-ttu-id="e61d3-191">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-191">Account</span></span>                        | <span data-ttu-id="e61d3-192">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-192">Debit amount</span></span> | <span data-ttu-id="e61d3-193">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-193">Credit amount</span></span> |
|--------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-194">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-194">Cash (Fabrikam)</span></span>                | <span data-ttu-id="e61d3-195">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-195">600.00</span></span>       |               |
| <span data-ttu-id="e61d3-196">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-196">Accounts receivable (Fabrikam)</span></span> |              | <span data-ttu-id="e61d3-197">600.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-197">600.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="e61d3-198">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="e61d3-198">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="e61d3-199">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-199">**Fabrikam posting**</span></span>

| <span data-ttu-id="e61d3-200">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-200">Account</span></span>                         | <span data-ttu-id="e61d3-201">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-201">Debit amount</span></span> | <span data-ttu-id="e61d3-202">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-202">Credit amount</span></span> |
|---------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-203">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-203">Accounts receivable (Fabrikam)</span></span>  | <span data-ttu-id="e61d3-204">580.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-204">580.00</span></span>       |               |
| <span data-ttu-id="e61d3-205">向 Fabrikam East (Fabrikam) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-205">Due to Fabrikam East (Fabrikam)</span></span> |              | <span data-ttu-id="e61d3-206">580.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-206">580.00</span></span>        |

<span data-ttu-id="e61d3-207">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-207">**Fabrikam East posting**</span></span>

| <span data-ttu-id="e61d3-208">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-208">Account</span></span>                             | <span data-ttu-id="e61d3-209">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-209">Debit amount</span></span> | <span data-ttu-id="e61d3-210">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-210">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-211">从 Fabrikam (Fabrikam East) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-211">Due from Fabrikam (Fabrikam East)</span></span>   | <span data-ttu-id="e61d3-212">580.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-212">580.00</span></span>       |               |
| <span data-ttu-id="e61d3-213">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-213">Accounts receivable (Fabrikam East)</span></span> |              | <span data-ttu-id="e61d3-214">580.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-214">580.00</span></span>        |
| <span data-ttu-id="e61d3-215">现金折扣 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-215">Cash discount (Fabrikam East)</span></span>       | <span data-ttu-id="e61d3-216">20.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-216">20.00</span></span>        |               |
| <span data-ttu-id="e61d3-217">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-217">Accounts receivable (Fabrikam East)</span></span> |              | <span data-ttu-id="e61d3-218">20.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-218">20.00</span></span>         |

## <a name="example-3-customer-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-gain"></a><span data-ttu-id="e61d3-219">示例 3：来自具有已有汇率收益的其他法人的发票的客户付款</span><span class="sxs-lookup"><span data-stu-id="e61d3-219">Example 3: Customer payment of invoice from another legal entity with realized exchange rate gain</span></span>
<span data-ttu-id="e61d3-220">Fabrikam 为 Fabrikam 客户帐户 4000 (Northwind Traders) 收到了金额为 600.00 欧元 (EUR) 的付款。</span><span class="sxs-lookup"><span data-stu-id="e61d3-220">Fabrikam receives a payment of 600.00 euros (EUR) for Fabrikam customer 4000, Northwind Traders.</span></span> <span data-ttu-id="e61d3-221">该付款用 Fabrikam East 中的客户 4000 的未结发票结算。</span><span class="sxs-lookup"><span data-stu-id="e61d3-221">The payment is settled with an open invoice for customer 4000 in Fabrikam East.</span></span> <span data-ttu-id="e61d3-222">在结算过程中将生成币种汇率收益交易记录。</span><span class="sxs-lookup"><span data-stu-id="e61d3-222">A currency exchange gain transaction is generated during the settlement process.</span></span>

-   <span data-ttu-id="e61d3-223">在发票日期的欧元 (EUR) 到美元 (USD) 的汇率：1.2062</span><span class="sxs-lookup"><span data-stu-id="e61d3-223">Exchange rate for EUR to U.S. dollars (USD) as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="e61d3-224">在付款日期的欧元到美元的汇率：1.2277</span><span class="sxs-lookup"><span data-stu-id="e61d3-224">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-customer-4000"></a><span data-ttu-id="e61d3-225">在 Fabrikam East 中为 Fabrikam East 客户 4000 过帐发票</span><span class="sxs-lookup"><span data-stu-id="e61d3-225">Invoice is posted in Fabrikam East for Fabrikam East customer 4000</span></span>

| <span data-ttu-id="e61d3-226">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-226">Account</span></span>                             | <span data-ttu-id="e61d3-227">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-227">Debit amount</span></span>            | <span data-ttu-id="e61d3-228">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-228">Credit amount</span></span>           |
|-------------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="e61d3-229">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-229">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="e61d3-230">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-230">600.00 EUR / 723.72 USD</span></span> |                         |
| <span data-ttu-id="e61d3-231">销售 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-231">Sales (Fabrikam East)</span></span>               |                         | <span data-ttu-id="e61d3-232">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-232">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-received-and-posted-in-fabrikam-for-fabrikam-customer-4000"></a><span data-ttu-id="e61d3-233">在 Fabrikam 中为 Fabrikam 客户 4000 接收和过帐付款</span><span class="sxs-lookup"><span data-stu-id="e61d3-233">Payment is received and posted in Fabrikam for Fabrikam customer 4000</span></span>

| <span data-ttu-id="e61d3-234">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-234">Account</span></span>                        | <span data-ttu-id="e61d3-235">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-235">Debit amount</span></span>            | <span data-ttu-id="e61d3-236">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-236">Credit amount</span></span>           |
|--------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="e61d3-237">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-237">Cash (Fabrikam)</span></span>                | <span data-ttu-id="e61d3-238">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-238">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="e61d3-239">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-239">Accounts receivable (Fabrikam)</span></span> |                         | <span data-ttu-id="e61d3-240">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-240">600.00 EUR / 736.62 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="e61d3-241">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="e61d3-241">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="e61d3-242">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-242">**Fabrikam posting**</span></span>

| <span data-ttu-id="e61d3-243">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-243">Account</span></span>                         | <span data-ttu-id="e61d3-244">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-244">Debit amount</span></span>            | <span data-ttu-id="e61d3-245">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-245">Credit amount</span></span>           |
|---------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="e61d3-246">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-246">Accounts receivable (Fabrikam)</span></span>  | <span data-ttu-id="e61d3-247">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-247">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="e61d3-248">向 Fabrikam East (Fabrikam) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-248">Due to Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="e61d3-249">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-249">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="e61d3-250">向 Fabrikam East (Fabrikam) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-250">Due to Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="e61d3-251">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-251">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="e61d3-252">已有收益 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-252">Realized gain (Fabrikam)</span></span>        |                         | <span data-ttu-id="e61d3-253">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-253">0.00 EUR / 12.90 USD</span></span>    |

<span data-ttu-id="e61d3-254">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-254">**Fabrikam East posting**</span></span>

| <span data-ttu-id="e61d3-255">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-255">Account</span></span>                             | <span data-ttu-id="e61d3-256">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-256">Debit amount</span></span>            | <span data-ttu-id="e61d3-257">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-257">Credit amount</span></span>           |
|-------------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="e61d3-258">从 Fabrikam (Fabrikam East) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-258">Due from Fabrikam (Fabrikam East)</span></span>   | <span data-ttu-id="e61d3-259">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-259">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="e61d3-260">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-260">Accounts receivable (Fabrikam East)</span></span> |                         | <span data-ttu-id="e61d3-261">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-261">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="e61d3-262">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-262">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="e61d3-263">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-263">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="e61d3-264">从 Fabrikam (Fabrikam East) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-264">Due from Fabrikam (Fabrikam East)</span></span>   |                         | <span data-ttu-id="e61d3-265">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-265">0.00 EUR / 12.90 USD</span></span>    |

## <a name="example-4-customer-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-gain"></a><span data-ttu-id="e61d3-266">示例 4：来自具有现金折扣和已有汇率收益的其他法人的发票的客户付款</span><span class="sxs-lookup"><span data-stu-id="e61d3-266">Example 4: Customer payment of invoice from another legal entity with cash discount and realized exchange rate gain</span></span>
<span data-ttu-id="e61d3-267">Fabrikam 为 Fabrikam East 中的未结发票，为 Fabrikam customer 4000 (Northwind Traders) 过帐付款。</span><span class="sxs-lookup"><span data-stu-id="e61d3-267">Fabrikam posts a payment for Fabrikam customer 4000, Northwind Traders, for an open invoice in Fabrikam East.</span></span> <span data-ttu-id="e61d3-268">该发票具有可用的现金折扣并且生成增值税交易记录。</span><span class="sxs-lookup"><span data-stu-id="e61d3-268">The invoice has a cash discount available, and a sales tax transaction is generated.</span></span> <span data-ttu-id="e61d3-269">该付款用未结 Fabrikam East 发票结算。</span><span class="sxs-lookup"><span data-stu-id="e61d3-269">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="e61d3-270">在结算过程中将生成币种汇率收益交易记录。</span><span class="sxs-lookup"><span data-stu-id="e61d3-270">A currency exchange gain transaction is generated during the settlement process.</span></span> <span data-ttu-id="e61d3-271">现金折扣过帐到发票法人 (Fabrikam East)，且币种汇率获得过帐到付款法人 (Fabrikam)。</span><span class="sxs-lookup"><span data-stu-id="e61d3-271">The cash discount is posted to the legal entity of the invoice (Fabrikam East), and the currency exchange gain is posted to the legal entity of the payment (Fabrikam).</span></span>

-   <span data-ttu-id="e61d3-272">在发票日期的欧元到美元的汇率：1.2062</span><span class="sxs-lookup"><span data-stu-id="e61d3-272">Exchange rate for EUR to USD as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="e61d3-273">在付款日期的欧元到美元的汇率：1.2277</span><span class="sxs-lookup"><span data-stu-id="e61d3-273">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="free-text-invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-customer-4000"></a><span data-ttu-id="e61d3-274">过帐普通发票，并且在 Fabrikam East 中为客户 4000 生成纳税交易记录</span><span class="sxs-lookup"><span data-stu-id="e61d3-274">Free text invoice is posted and a tax transaction is generated in Fabrikam East for customer 4000</span></span>

| <span data-ttu-id="e61d3-275">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-275">Account</span></span>                             | <span data-ttu-id="e61d3-276">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-276">Debit amount</span></span>            | <span data-ttu-id="e61d3-277">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-277">Credit amount</span></span>           |
|-------------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="e61d3-278">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-278">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="e61d3-279">638.22 EUR / 769.82 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-279">638.22 EUR / 769.82 USD</span></span> |                         |
| <span data-ttu-id="e61d3-280">销售 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-280">Sales (Fabrikam East)</span></span>               |                         | <span data-ttu-id="e61d3-281">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-281">600.00 EUR / 723.72 USD</span></span> |
| <span data-ttu-id="e61d3-282">增值税 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-282">Sales tax (Fabrikam East)</span></span>           |                         | <span data-ttu-id="e61d3-283">38.22 EUR / 46.10 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-283">38.22 EUR / 46.10 USD</span></span>   |

### <a name="payment-is-received-and-posted-in-fabrikam-for-customer-4000"></a><span data-ttu-id="e61d3-284">在 Fabrikam 中为客户 4000 接收和过帐付款</span><span class="sxs-lookup"><span data-stu-id="e61d3-284">Payment is received and posted in Fabrikam for customer 4000</span></span>

| <span data-ttu-id="e61d3-285">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-285">Account</span></span>                        | <span data-ttu-id="e61d3-286">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-286">Debit amount</span></span>            | <span data-ttu-id="e61d3-287">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-287">Credit amount</span></span>           |
|--------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="e61d3-288">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-288">Cash (Fabrikam)</span></span>                | <span data-ttu-id="e61d3-289">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-289">626.22 EUR / 768.81 USD</span></span> |                         |
| <span data-ttu-id="e61d3-290">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-290">Accounts receivable (Fabrikam)</span></span> |                         | <span data-ttu-id="e61d3-291">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-291">626.22 EUR / 768.81 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="e61d3-292">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="e61d3-292">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="e61d3-293">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-293">**Fabrikam posting**</span></span>

| <span data-ttu-id="e61d3-294">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-294">Account</span></span>                         | <span data-ttu-id="e61d3-295">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-295">Debit amount</span></span>            | <span data-ttu-id="e61d3-296">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-296">Credit amount</span></span>           |
|---------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="e61d3-297">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-297">Accounts receivable (Fabrikam)</span></span>  | <span data-ttu-id="e61d3-298">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-298">626.22 EUR / 768.81 USD</span></span> |                         |
| <span data-ttu-id="e61d3-299">向 Fabrikam East (Fabrikam) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-299">Due to Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="e61d3-300">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-300">626.22 EUR / 768.81 USD</span></span> |
| <span data-ttu-id="e61d3-301">向 Fabrikam East (Fabrikam) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-301">Due to Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="e61d3-302">0.00 EUR / 13.46 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-302">0.00 EUR / 13.46 USD</span></span>    |                         |
| <span data-ttu-id="e61d3-303">已有收益 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-303">Realized gain (Fabrikam)</span></span>        |                         | <span data-ttu-id="e61d3-304">0.00 EUR / 13.46 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-304">0.00 EUR / 13.46 USD</span></span>    |

<span data-ttu-id="e61d3-305">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-305">**Fabrikam East posting**</span></span>

| <span data-ttu-id="e61d3-306">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-306">Account</span></span>                             | <span data-ttu-id="e61d3-307">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-307">Debit amount</span></span>            | <span data-ttu-id="e61d3-308">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-308">Credit amount</span></span>           |
|-------------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="e61d3-309">从 Fabrikam (Fabrikam East) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-309">Due from Fabrikam (Fabrikam East)</span></span>   | <span data-ttu-id="e61d3-310">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-310">626.22 EUR / 768.81 USD</span></span> |                         |
| <span data-ttu-id="e61d3-311">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-311">Accounts receivable (Fabrikam East)</span></span> |                         | <span data-ttu-id="e61d3-312">626.22 EUR / 768.81 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-312">626.22 EUR / 768.81 USD</span></span> |
| <span data-ttu-id="e61d3-313">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-313">Accounts receivable (Fabrikam East</span></span>  | <span data-ttu-id="e61d3-314">0.00 EUR / 13.46 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-314">0.00 EUR / 13.46 USD</span></span>    |                         |
| <span data-ttu-id="e61d3-315">从 Fabrikam (Fabrikam East) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-315">Due from Fabrikam (Fabrikam East)</span></span>   |                         | <span data-ttu-id="e61d3-316">0.00 EUR / 13.46 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-316">0.00 EUR / 13.46 USD</span></span>    |
| <span data-ttu-id="e61d3-317">现金折扣 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-317">Cash discount (Fabrikam East)</span></span>       | <span data-ttu-id="e61d3-318">12.00 EUR / 14.47 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-318">12.00 EUR / 14.47 USD</span></span>   |                         |
| <span data-ttu-id="e61d3-319">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-319">Accounts receivable (Fabrikam East)</span></span> |                         | <span data-ttu-id="e61d3-320">12.00 EUR / 14.47 USD</span><span class="sxs-lookup"><span data-stu-id="e61d3-320">12.00 EUR / 14.47 USD</span></span>   |

## <a name="example-5-customer-credit-note-with-primary-payment"></a><span data-ttu-id="e61d3-321">示例 5：具有主付款的客户贷方通知单</span><span class="sxs-lookup"><span data-stu-id="e61d3-321">Example 5: Customer credit note with primary payment</span></span>
<span data-ttu-id="e61d3-322">Fabrikam 从客户 4000 (Northwind Traders) 接收 75.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="e61d3-322">Fabrikam receives a payment of 75.00 from customer 4000, Northwind Traders.</span></span> <span data-ttu-id="e61d3-323">该付款用针对 Fabrikam West 客户 10000 的未结发票和针对 Fabrikam East 客户 4000 的未结贷方通知单结算。</span><span class="sxs-lookup"><span data-stu-id="e61d3-323">The payment is settled with an open invoice for Fabrikam West customer 10000 and an open credit note for Fabrikam East customer 4000.</span></span> <span data-ttu-id="e61d3-324">该付款在**未结交易记录编辑**页中选择为主付款。</span><span class="sxs-lookup"><span data-stu-id="e61d3-324">The payment is selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a><span data-ttu-id="e61d3-325">发票为客户 10000 过帐到 Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="e61d3-325">Invoice is posted to Fabrikam West for customer 10000</span></span>

| <span data-ttu-id="e61d3-326">帐户</span><span class="sxs-lookup"><span data-stu-id="e61d3-326">Account</span></span>                             | <span data-ttu-id="e61d3-327">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-327">Debit amount</span></span> | <span data-ttu-id="e61d3-328">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-328">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-329">应收账款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="e61d3-329">Accounts receivable (Fabrikam West)</span></span> | <span data-ttu-id="e61d3-330">100.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-330">100.00</span></span>       |               |
| <span data-ttu-id="e61d3-331">销售 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="e61d3-331">Sales (Fabrikam West)</span></span>               |              | <span data-ttu-id="e61d3-332">100.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-332">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a><span data-ttu-id="e61d3-333">贷方通知单为客户 4000 过帐到 Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="e61d3-333">Credit note is posted to Fabrikam East for customer 4000</span></span>

| <span data-ttu-id="e61d3-334">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-334">Account</span></span>                             | <span data-ttu-id="e61d3-335">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-335">Debit amount</span></span> | <span data-ttu-id="e61d3-336">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-336">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-337">销售退货 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-337">Sales returns (Fabrikam East)</span></span>       | <span data-ttu-id="e61d3-338">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-338">25.00</span></span>        |               |
| <span data-ttu-id="e61d3-339">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-339">Accounts receivable (Fabrikam East)</span></span> |              | <span data-ttu-id="e61d3-340">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-340">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a><span data-ttu-id="e61d3-341">付款为客户 4000 过帐到 Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e61d3-341">Payment is posted to Fabrikam for customer 4000</span></span>

| <span data-ttu-id="e61d3-342">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-342">Account</span></span>                        | <span data-ttu-id="e61d3-343">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-343">Debit amount</span></span> | <span data-ttu-id="e61d3-344">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-344">Credit amount</span></span> |
|--------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-345">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-345">Cash (Fabrikam)</span></span>                | <span data-ttu-id="e61d3-346">75.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-346">75.00</span></span>        |               |
| <span data-ttu-id="e61d3-347">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-347">Accounts receivable (Fabrikam)</span></span> |              | <span data-ttu-id="e61d3-348">75.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-348">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="e61d3-349">Fabrikam 付款用 Fabrikam West 发票和 Fabrikam East 贷方通知单结算</span><span class="sxs-lookup"><span data-stu-id="e61d3-349">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="e61d3-350">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-350">**Fabrikam posting**</span></span>

| <span data-ttu-id="e61d3-351">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-351">Account</span></span>                           | <span data-ttu-id="e61d3-352">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-352">Debit amount</span></span> | <span data-ttu-id="e61d3-353">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-353">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-354">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-354">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="e61d3-355">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-355">25.00</span></span>        |               |
| <span data-ttu-id="e61d3-356">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-356">Accounts receivable (Fabrikam)</span></span>    |              | <span data-ttu-id="e61d3-357">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-357">25.00</span></span>         |
| <span data-ttu-id="e61d3-358">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-358">Accounts receivable (Fabrikam)</span></span>    | <span data-ttu-id="e61d3-359">100.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-359">100.00</span></span>       |               |
| <span data-ttu-id="e61d3-360">向 Fabrikam West (Fabrikam) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-360">Due to Fabrikam West (Fabrikam)</span></span>   |              | <span data-ttu-id="e61d3-361">100.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-361">100.00</span></span>        |

<span data-ttu-id="e61d3-362">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-362">**Fabrikam East posting**</span></span>

| <span data-ttu-id="e61d3-363">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-363">Account</span></span>                             | <span data-ttu-id="e61d3-364">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-364">Debit amount</span></span> | <span data-ttu-id="e61d3-365">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-365">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-366">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-366">Accounts receivable (Fabrikam East)</span></span> | <span data-ttu-id="e61d3-367">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-367">25.00</span></span>        |               |
| <span data-ttu-id="e61d3-368">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-368">Due to Fabrikam (Fabrikam East)</span></span>     |              | <span data-ttu-id="e61d3-369">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-369">25.00</span></span>         |

<span data-ttu-id="e61d3-370">**Fabrikam West 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-370">**Fabrikam West posting**</span></span>

| <span data-ttu-id="e61d3-371">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-371">Account</span></span>                             | <span data-ttu-id="e61d3-372">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-372">Debit amount</span></span> | <span data-ttu-id="e61d3-373">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-373">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-374">从 Fabrikam (Fabrikam West) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-374">Due from Fabrikam (Fabrikam West)</span></span>   | <span data-ttu-id="e61d3-375">100.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-375">100.00</span></span>       |               |
| <span data-ttu-id="e61d3-376">应收账款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="e61d3-376">Accounts receivable (Fabrikam West)</span></span> |              | <span data-ttu-id="e61d3-377">100.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-377">100.00</span></span>        |

## <a name="example-6-customer-credit-note-without-primary-payment"></a><span data-ttu-id="e61d3-378">示例 6：没有主付款的客户贷方通知单</span><span class="sxs-lookup"><span data-stu-id="e61d3-378">Example 6: Customer credit note without primary payment</span></span>
<span data-ttu-id="e61d3-379">Fabrikam 从客户 4000 (Northwind Traders) 接收 75.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="e61d3-379">Fabrikam receives a payment of 75.00 from customer 4000, Northwind Traders.</span></span> <span data-ttu-id="e61d3-380">该付款用针对 Fabrikam West 客户 10000 的未结发票和针对 Fabrikam East 客户 4000 的未结贷方通知单结算。</span><span class="sxs-lookup"><span data-stu-id="e61d3-380">The payment is settled with an open invoice for Fabrikam West customer 10000 and an open credit note for Fabrikam East customer 4000.</span></span> <span data-ttu-id="e61d3-381">该付款未在**未结交易记录编辑**页中选择为主付款。</span><span class="sxs-lookup"><span data-stu-id="e61d3-381">The payment isn't selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-customer-10000"></a><span data-ttu-id="e61d3-382">发票为客户 10000 过帐到 Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="e61d3-382">Invoice is posted to Fabrikam West for customer 10000</span></span>

| <span data-ttu-id="e61d3-383">帐户</span><span class="sxs-lookup"><span data-stu-id="e61d3-383">Account</span></span>                             | <span data-ttu-id="e61d3-384">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-384">Debit amount</span></span> | <span data-ttu-id="e61d3-385">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-385">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-386">应收账款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="e61d3-386">Accounts receivable (Fabrikam West)</span></span> | <span data-ttu-id="e61d3-387">100.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-387">100.00</span></span>       |               |
| <span data-ttu-id="e61d3-388">销售 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="e61d3-388">Sales (Fabrikam West)</span></span>               |              | <span data-ttu-id="e61d3-389">100.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-389">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-customer-4000"></a><span data-ttu-id="e61d3-390">贷方通知单为客户 4000 过帐到 Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="e61d3-390">Credit note is posted to Fabrikam East for customer 4000</span></span>

| <span data-ttu-id="e61d3-391">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-391">Account</span></span>                             | <span data-ttu-id="e61d3-392">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-392">Debit amount</span></span> | <span data-ttu-id="e61d3-393">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-393">Credit amount</span></span> |
|-------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-394">销售退货 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-394">Sales returns (Fabrikam East)</span></span>       | <span data-ttu-id="e61d3-395">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-395">25.00</span></span>        |               |
| <span data-ttu-id="e61d3-396">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-396">Accounts receivable (Fabrikam East)</span></span> |              | <span data-ttu-id="e61d3-397">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-397">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-customer-4000"></a><span data-ttu-id="e61d3-398">付款为客户 4000 过帐到 Fabrikam</span><span class="sxs-lookup"><span data-stu-id="e61d3-398">Payment is posted to Fabrikam for customer 4000</span></span>

| <span data-ttu-id="e61d3-399">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-399">Account</span></span>                        | <span data-ttu-id="e61d3-400">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-400">Debit amount</span></span> | <span data-ttu-id="e61d3-401">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-401">Credit amount</span></span> |
|--------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-402">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-402">Cash (Fabrikam)</span></span>                | <span data-ttu-id="e61d3-403">75.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-403">75.00</span></span>        |               |
| <span data-ttu-id="e61d3-404">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-404">Accounts receivable (Fabrikam)</span></span> |              | <span data-ttu-id="e61d3-405">75.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-405">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="e61d3-406">Fabrikam 付款用 Fabrikam West 发票和 Fabrikam East 贷方通知单结算</span><span class="sxs-lookup"><span data-stu-id="e61d3-406">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="e61d3-407">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-407">**Fabrikam posting**</span></span>

| <span data-ttu-id="e61d3-408">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-408">Account</span></span>                         | <span data-ttu-id="e61d3-409">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-409">Debit amount</span></span> | <span data-ttu-id="e61d3-410">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-410">Credit amount</span></span> |
|---------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-411">应收账款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="e61d3-411">Accounts receivable (Fabrikam)</span></span>  | <span data-ttu-id="e61d3-412">75.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-412">75.00</span></span>        |               |
| <span data-ttu-id="e61d3-413">向 Fabrikam West (Fabrikam) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-413">Due to Fabrikam West (Fabrikam)</span></span> |              | <span data-ttu-id="e61d3-414">75.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-414">75.00</span></span>         |

<span data-ttu-id="e61d3-415">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-415">**Fabrikam East posting**</span></span>

| <span data-ttu-id="e61d3-416">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-416">Account</span></span>                              | <span data-ttu-id="e61d3-417">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-417">Debit amount</span></span> | <span data-ttu-id="e61d3-418">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-418">Credit amount</span></span> |
|--------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-419">应收账款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="e61d3-419">Accounts receivable (Fabrikam East)</span></span>  | <span data-ttu-id="e61d3-420">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-420">25.00</span></span>        |               |
| <span data-ttu-id="e61d3-421">向 Fabrikam West (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-421">Due to Fabrikam West (Fabrikam East)</span></span> |              | <span data-ttu-id="e61d3-422">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-422">25.00</span></span>         |

<span data-ttu-id="e61d3-423">**Fabrikam West 过帐**</span><span class="sxs-lookup"><span data-stu-id="e61d3-423">**Fabrikam West posting**</span></span>

| <span data-ttu-id="e61d3-424">科目</span><span class="sxs-lookup"><span data-stu-id="e61d3-424">Account</span></span>                                | <span data-ttu-id="e61d3-425">借方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-425">Debit amount</span></span> | <span data-ttu-id="e61d3-426">贷方金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-426">Credit amount</span></span> |
|----------------------------------------|--------------|---------------|
| <span data-ttu-id="e61d3-427">从 Fabrikam (Fabrikam West) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-427">Due from Fabrikam (Fabrikam West)</span></span>      | <span data-ttu-id="e61d3-428">75.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-428">75.00</span></span>        |               |
| <span data-ttu-id="e61d3-429">应收账款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="e61d3-429">Accounts receivable (Fabrikam West)</span></span>    |              | <span data-ttu-id="e61d3-430">75.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-430">75.00</span></span>         |
| <span data-ttu-id="e61d3-431">从 Fabrikam East (Fabrikam West) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="e61d3-431">Due from Fabrikam East (Fabrikam West)</span></span> | <span data-ttu-id="e61d3-432">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-432">25.00</span></span>        |               |
| <span data-ttu-id="e61d3-433">应收账款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="e61d3-433">Accounts receivable (Fabrikam West)</span></span>    |              | <span data-ttu-id="e61d3-434">25.00</span><span class="sxs-lookup"><span data-stu-id="e61d3-434">25.00</span></span>         |






