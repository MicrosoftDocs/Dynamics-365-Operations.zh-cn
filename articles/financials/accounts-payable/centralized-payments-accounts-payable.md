---
title: 应付账款的集中付款
description: 包括多个法人的组织可以使用处理所有付款的单个法人创建和管理付款。 因此，不必在多个法人中输入同一付款。 本文提供显示集中付款过帐如何在不同环境中处理的示例。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6744aae97499385405e192cd6d6cb8590dd79b7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "327059"
---
# <a name="centralized-payments-for-accounts-payable"></a><span data-ttu-id="86f12-105">应付账款的集中付款</span><span class="sxs-lookup"><span data-stu-id="86f12-105">Centralized payments for Accounts payable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86f12-106">包括多个法人的组织可以使用处理所有付款的单个法人创建和管理付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-106">Organizations that include multiple legal entities can create and manage payments by using a single legal entity that handles all payments.</span></span> <span data-ttu-id="86f12-107">因此，不必在多个法人中输入同一付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-107">Therefore, the same payments don't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="86f12-108">本文提供显示集中付款过帐如何在不同环境中处理的示例。</span><span class="sxs-lookup"><span data-stu-id="86f12-108">This article provides examples that show how posting for centralized payments is handled in various scenarios.</span></span>

<span data-ttu-id="86f12-109">包括多个法人的组织可以使用处理所有付款的法人创建和管理付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-109">Organizations that include multiple legal entities can create and manage payments by using a legal entity that handles all payments.</span></span> <span data-ttu-id="86f12-110">因此，不必在多个法人中输入同一付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-110">Therefore, the same payments don't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="86f12-111">此外，组织节省时间，因为付款流程简化。</span><span class="sxs-lookup"><span data-stu-id="86f12-111">Additionally, the organization saves time, because the payment process is streamlined.</span></span>

<span data-ttu-id="86f12-112">在集中付款的组织中，有很多营业的法人，且每个营业的法人都管理自己的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="86f12-112">In a centralized payments organization, there are many legal entities for operations, and each operating legal entity manages its own vendor invoices.</span></span> <span data-ttu-id="86f12-113">所有营业的法人的付款都是从称作付款的法人的单个法人中生成的。</span><span class="sxs-lookup"><span data-stu-id="86f12-113">Payments for all the operating legal entities are generated from a single legal entity, which is known as the legal entity of the payment.</span></span> <span data-ttu-id="86f12-114">在结算流程中，生成适用的应付和应收交易记录。</span><span class="sxs-lookup"><span data-stu-id="86f12-114">During the settlement process, the applicable due-to and due-from transactions are generated.</span></span> <span data-ttu-id="86f12-115">您可以指定组织内的哪个法人接收已有收益或已有损失交易记录，以及如何处理与跨公司付款相关的现金折扣交易记录。</span><span class="sxs-lookup"><span data-stu-id="86f12-115">You can specify which legal entity in the organization receives the realized gain or realized loss transactions, and how cash discount transactions that are related to a cross-company payment are handled.</span></span> 

<span data-ttu-id="86f12-116">以下示例说明如何在不同的环境中处理过帐。</span><span class="sxs-lookup"><span data-stu-id="86f12-116">The following examples illustrate how posting is handled in various scenarios.</span></span> <span data-ttu-id="86f12-117">假定所有这些示例都采用以下配置：</span><span class="sxs-lookup"><span data-stu-id="86f12-117">The following configuration is assumed for all these examples:</span></span>

-   <span data-ttu-id="86f12-118">法人分别为 Fabrikam、Fabrikam East 和 Fabrikam West。</span><span class="sxs-lookup"><span data-stu-id="86f12-118">The legal entities are Fabrikam, Fabrikam East, and Fabrikam West.</span></span> <span data-ttu-id="86f12-119">从 Fabrikam 进行付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-119">Payments are made from Fabrikam.</span></span>
-   <span data-ttu-id="86f12-120">**内部公司**页上的**过帐现金折扣**字段设置为**发票法人**。</span><span class="sxs-lookup"><span data-stu-id="86f12-120">The **Post cash discount** field on the **Intercompany accounting** page is set to **Legal entity of the invoice**.</span></span>
-   <span data-ttu-id="86f12-121">**内部公司**页上的**过帐币种汇兑损益**字段设置为**付款法人**。</span><span class="sxs-lookup"><span data-stu-id="86f12-121">The **Post currency exchange gain or loss** field on the **Intercompany accounting** page is set to **Legal entity of the payment**.</span></span>
-   <span data-ttu-id="86f12-122">客户 Fourth Coffee 在每个法人中设置为一个供应商。</span><span class="sxs-lookup"><span data-stu-id="86f12-122">The vendor Fourth Coffee is set up as a vendor in each legal entity.</span></span> <span data-ttu-id="86f12-123">来自不同法人的供应商被标识为同一供应商，因为他们共享相同的全球通讯簿 ID。</span><span class="sxs-lookup"><span data-stu-id="86f12-123">The vendors from the various legal entities are identified as the same vendor because they share the same global address book ID.</span></span>

| <span data-ttu-id="86f12-124">名录 ID</span><span class="sxs-lookup"><span data-stu-id="86f12-124">Directory ID</span></span> | <span data-ttu-id="86f12-125">供应商帐户</span><span class="sxs-lookup"><span data-stu-id="86f12-125">Vendor account</span></span> | <span data-ttu-id="86f12-126">姓名</span><span class="sxs-lookup"><span data-stu-id="86f12-126">Name</span></span>          | <span data-ttu-id="86f12-127">法人</span><span class="sxs-lookup"><span data-stu-id="86f12-127">Legal entity</span></span>  |
|--------------|----------------|---------------|---------------|
| <span data-ttu-id="86f12-128">1050</span><span class="sxs-lookup"><span data-stu-id="86f12-128">1050</span></span>         | <span data-ttu-id="86f12-129">3004</span><span class="sxs-lookup"><span data-stu-id="86f12-129">3004</span></span>           | <span data-ttu-id="86f12-130">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="86f12-130">Fourth Coffee</span></span> | <span data-ttu-id="86f12-131">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="86f12-131">Fabrikam</span></span>      |
| <span data-ttu-id="86f12-132">1050</span><span class="sxs-lookup"><span data-stu-id="86f12-132">1050</span></span>         | <span data-ttu-id="86f12-133">100</span><span class="sxs-lookup"><span data-stu-id="86f12-133">100</span></span>            | <span data-ttu-id="86f12-134">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="86f12-134">Fourth Coffee</span></span> | <span data-ttu-id="86f12-135">Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="86f12-135">Fabrikam East</span></span> |
| <span data-ttu-id="86f12-136">1050</span><span class="sxs-lookup"><span data-stu-id="86f12-136">1050</span></span>         | <span data-ttu-id="86f12-137">3004</span><span class="sxs-lookup"><span data-stu-id="86f12-137">3004</span></span>           | <span data-ttu-id="86f12-138">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="86f12-138">Fourth Coffee</span></span> | <span data-ttu-id="86f12-139">Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="86f12-139">Fabrikam West</span></span> |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a><span data-ttu-id="86f12-140">示例 1：来自其他法人的发票的供应商付款</span><span class="sxs-lookup"><span data-stu-id="86f12-140">Example 1: Vendor payment of invoice from another legal entity</span></span>
<span data-ttu-id="86f12-141">Fabrikam East 为供应商帐户 100 (Fourth Coffee) 具有一个未结发票。</span><span class="sxs-lookup"><span data-stu-id="86f12-141">Fabrikam East has an open invoice for vendor account 100, Fourth Coffee.</span></span> <span data-ttu-id="86f12-142">Fabrikam 输入付款并将付款过帐到 Fabrikam 供应商帐户 3004 (Fourth Coffee)。</span><span class="sxs-lookup"><span data-stu-id="86f12-142">Fabrikam enters and posts a payment to Fabrikam vendor account 3004, Fourth Coffee.</span></span> <span data-ttu-id="86f12-143">该付款用该未结发票结算。</span><span class="sxs-lookup"><span data-stu-id="86f12-143">The payment is settled with the open invoice.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a><span data-ttu-id="86f12-144">在 Fabrikam East 中为供应商 100 过帐发票</span><span class="sxs-lookup"><span data-stu-id="86f12-144">Invoice is posted in Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="86f12-145">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-145">Account</span></span>                          | <span data-ttu-id="86f12-146">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-146">Debit amount</span></span> | <span data-ttu-id="86f12-147">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-147">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-148">支出 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-148">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="86f12-149">600.00</span><span class="sxs-lookup"><span data-stu-id="86f12-149">600.00</span></span>       |               |
| <span data-ttu-id="86f12-150">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-150">Accounts payable (Fabrikam East)</span></span> |              | <span data-ttu-id="86f12-151">600.00</span><span class="sxs-lookup"><span data-stu-id="86f12-151">600.00</span></span>        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a><span data-ttu-id="86f12-152">在 Fabrikam 中为供应商 3004 生成和过帐付款</span><span class="sxs-lookup"><span data-stu-id="86f12-152">Payment is generated and posted in Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="86f12-153">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-153">Account</span></span>                     | <span data-ttu-id="86f12-154">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-154">Debit amount</span></span> | <span data-ttu-id="86f12-155">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-155">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="86f12-156">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-156">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="86f12-157">600.00</span><span class="sxs-lookup"><span data-stu-id="86f12-157">600.00</span></span>       |               |
| <span data-ttu-id="86f12-158">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-158">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="86f12-159">600.00</span><span class="sxs-lookup"><span data-stu-id="86f12-159">600.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="86f12-160">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="86f12-160">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="86f12-161">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-161">**Fabrikam posting**</span></span>

| <span data-ttu-id="86f12-162">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-162">Account</span></span>                           | <span data-ttu-id="86f12-163">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-163">Debit amount</span></span> | <span data-ttu-id="86f12-164">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-164">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-165">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="86f12-165">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="86f12-166">600.00</span><span class="sxs-lookup"><span data-stu-id="86f12-166">600.00</span></span>       |               |
| <span data-ttu-id="86f12-167">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-167">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="86f12-168">600.00</span><span class="sxs-lookup"><span data-stu-id="86f12-168">600.00</span></span>        |

<span data-ttu-id="86f12-169">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-169">**Fabrikam East posting**</span></span>

| <span data-ttu-id="86f12-170">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-170">Account</span></span>                          | <span data-ttu-id="86f12-171">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-171">Debit amount</span></span> | <span data-ttu-id="86f12-172">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-172">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-173">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-173">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="86f12-174">600.00</span><span class="sxs-lookup"><span data-stu-id="86f12-174">600.00</span></span>       |               |
| <span data-ttu-id="86f12-175">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="86f12-175">Due to Fabrikam (Fabrikam East)</span></span>  |              | <span data-ttu-id="86f12-176">600.00</span><span class="sxs-lookup"><span data-stu-id="86f12-176">600.00</span></span>        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a><span data-ttu-id="86f12-177">示例 2：来自具有现金折扣的其他法人的发票的供应商付款</span><span class="sxs-lookup"><span data-stu-id="86f12-177">Example 2: Vendor payment of invoice from another legal entity with cash discount</span></span>
<span data-ttu-id="86f12-178">Fabrikam East 为供应商 100 (Fourth Coffee) 具有一个未结发票。</span><span class="sxs-lookup"><span data-stu-id="86f12-178">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="86f12-179">该发票具有 20.00 的可用现金折扣。</span><span class="sxs-lookup"><span data-stu-id="86f12-179">The invoice has a 20.00 cash discount available.</span></span> <span data-ttu-id="86f12-180">Fabrikam 为 Fabrikam 供应商 3004 (Fourth Coffee) 输入并过帐了 580.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-180">Fabrikam enters and posts a payment of 580.00 for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="86f12-181">该付款用未结 Fabrikam East 发票结算。</span><span class="sxs-lookup"><span data-stu-id="86f12-181">The payment is settled with the open Fabrikam East invoices.</span></span> <span data-ttu-id="86f12-182">该现金折扣过帐到发票法人 Fabrikam East。</span><span class="sxs-lookup"><span data-stu-id="86f12-182">The cash discount is posted to the legal entity of the invoice, Fabrikam East.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a><span data-ttu-id="86f12-183">在 Fabrikam East 中为 Fabrikam East 供应商 100 过帐发票</span><span class="sxs-lookup"><span data-stu-id="86f12-183">Invoice is posted in Fabrikam East for Fabrikam East vendor 100</span></span>

| <span data-ttu-id="86f12-184">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-184">Account</span></span>                          | <span data-ttu-id="86f12-185">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-185">Debit amount</span></span> | <span data-ttu-id="86f12-186">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-186">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-187">支出 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-187">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="86f12-188">600.00</span><span class="sxs-lookup"><span data-stu-id="86f12-188">600.00</span></span>       |               |
| <span data-ttu-id="86f12-189">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-189">Accounts payable (Fabrikam East)</span></span> |              | <span data-ttu-id="86f12-190">600.00</span><span class="sxs-lookup"><span data-stu-id="86f12-190">600.00</span></span>        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a><span data-ttu-id="86f12-191">在 Fabrikam 中为 Fabrikam 供应商 3004 生成和过帐付款</span><span class="sxs-lookup"><span data-stu-id="86f12-191">Payment is generated and posted in Fabrikam for Fabrikam vendor 3004</span></span>

| <span data-ttu-id="86f12-192">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-192">Account</span></span>                     | <span data-ttu-id="86f12-193">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-193">Debit amount</span></span> | <span data-ttu-id="86f12-194">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-194">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="86f12-195">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-195">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="86f12-196">580.00</span><span class="sxs-lookup"><span data-stu-id="86f12-196">580.00</span></span>       |               |
| <span data-ttu-id="86f12-197">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-197">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="86f12-198">580.00</span><span class="sxs-lookup"><span data-stu-id="86f12-198">580.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="86f12-199">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="86f12-199">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="86f12-200">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-200">**Fabrikam posting**</span></span>

| <span data-ttu-id="86f12-201">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-201">Account</span></span>                           | <span data-ttu-id="86f12-202">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-202">Debit amount</span></span> | <span data-ttu-id="86f12-203">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-203">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-204">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="86f12-204">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="86f12-205">580.00</span><span class="sxs-lookup"><span data-stu-id="86f12-205">580.00</span></span>       |               |
| <span data-ttu-id="86f12-206">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-206">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="86f12-207">580.00</span><span class="sxs-lookup"><span data-stu-id="86f12-207">580.00</span></span>        |

<span data-ttu-id="86f12-208">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-208">**Fabrikam East posting**</span></span>

| <span data-ttu-id="86f12-209">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-209">Account</span></span>                          | <span data-ttu-id="86f12-210">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-210">Debit amount</span></span> | <span data-ttu-id="86f12-211">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-211">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-212">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-212">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="86f12-213">580.00</span><span class="sxs-lookup"><span data-stu-id="86f12-213">580.00</span></span>       |               |
| <span data-ttu-id="86f12-214">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="86f12-214">Due to Fabrikam (Fabrikam East)</span></span>  |              | <span data-ttu-id="86f12-215">580.00</span><span class="sxs-lookup"><span data-stu-id="86f12-215">580.00</span></span>        |
| <span data-ttu-id="86f12-216">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-216">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="86f12-217">20.00</span><span class="sxs-lookup"><span data-stu-id="86f12-217">20.00</span></span>        |               |
| <span data-ttu-id="86f12-218">现金折扣 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-218">Cash discount (Fabrikam East)</span></span>    |              | <span data-ttu-id="86f12-219">20.00</span><span class="sxs-lookup"><span data-stu-id="86f12-219">20.00</span></span>         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a><span data-ttu-id="86f12-220">示例 3：来自具有已有汇率损失的其他法人的发票的供应商付款</span><span class="sxs-lookup"><span data-stu-id="86f12-220">Example 3: Vendor payment of invoice from another legal entity with realized exchange rate loss</span></span>
<span data-ttu-id="86f12-221">Fabrikam East 为供应商 100 (Fourth Coffee) 具有一个未结发票。</span><span class="sxs-lookup"><span data-stu-id="86f12-221">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="86f12-222">Fabrikam 输入并过帐 Fabrikam 供应商 3004 (Fourth Coffee) 的付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-222">Fabrikam enters and posts a payment for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="86f12-223">该付款用未结 Fabrikam East 发票结算。</span><span class="sxs-lookup"><span data-stu-id="86f12-223">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="86f12-224">在结算过程中将生成币种汇率损失交易记录。</span><span class="sxs-lookup"><span data-stu-id="86f12-224">A currency exchange loss transaction is generated during the settlement process.</span></span>

-   <span data-ttu-id="86f12-225">在发票日期的欧元 (EUR) 到美元 (USD) 的汇率：1.2062</span><span class="sxs-lookup"><span data-stu-id="86f12-225">Exchange rate for euros (EUR) to U.S. dollars (USD) as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="86f12-226">在付款日期的欧元到美元的汇率：1.2277</span><span class="sxs-lookup"><span data-stu-id="86f12-226">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a><span data-ttu-id="86f12-227">在 Fabrikam East 中为 Fabrikam East 供应商 100 过帐发票</span><span class="sxs-lookup"><span data-stu-id="86f12-227">Invoice is posted in Fabrikam East for Fabrikam East vendor 100</span></span>

| <span data-ttu-id="86f12-228">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-228">Account</span></span>                          | <span data-ttu-id="86f12-229">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-229">Debit amount</span></span>            | <span data-ttu-id="86f12-230">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-230">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="86f12-231">支出 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-231">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="86f12-232">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-232">600.00 EUR / 723.72 USD</span></span> |                         |
| <span data-ttu-id="86f12-233">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-233">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="86f12-234">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-234">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a><span data-ttu-id="86f12-235">在 Fabrikam 中为 Fabrikam 供应商 3004 生成和过帐付款</span><span class="sxs-lookup"><span data-stu-id="86f12-235">Payment is generated and posted in Fabrikam for Fabrikam vendor 3004</span></span>

| <span data-ttu-id="86f12-236">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-236">Account</span></span>                     | <span data-ttu-id="86f12-237">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-237">Debit amount</span></span>            | <span data-ttu-id="86f12-238">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-238">Credit amount</span></span>           |
|-----------------------------|-------------------------|-------------------------|
| <span data-ttu-id="86f12-239">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-239">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="86f12-240">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-240">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="86f12-241">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-241">Cash (Fabrikam)</span></span>             |                         | <span data-ttu-id="86f12-242">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-242">600.00 EUR / 736.62 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="86f12-243">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="86f12-243">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="86f12-244">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-244">**Fabrikam posting**</span></span>

| <span data-ttu-id="86f12-245">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-245">Account</span></span>                           | <span data-ttu-id="86f12-246">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-246">Debit amount</span></span>            | <span data-ttu-id="86f12-247">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-247">Credit amount</span></span>           |
|-----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="86f12-248">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="86f12-248">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="86f12-249">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-249">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="86f12-250">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-250">Accounts payable (Fabrikam)</span></span>       |                         | <span data-ttu-id="86f12-251">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-251">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="86f12-252">已有损失 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-252">Realized loss (Fabrikam)</span></span>          | <span data-ttu-id="86f12-253">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-253">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="86f12-254">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="86f12-254">Due from Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="86f12-255">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-255">0.00 EUR / 12.90 USD</span></span>    |

<span data-ttu-id="86f12-256">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-256">**Fabrikam East posting**</span></span>

| <span data-ttu-id="86f12-257">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-257">Account</span></span>                          | <span data-ttu-id="86f12-258">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-258">Debit amount</span></span>            | <span data-ttu-id="86f12-259">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-259">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="86f12-260">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-260">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="86f12-261">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-261">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="86f12-262">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="86f12-262">Due to Fabrikam (Fabrikam East)</span></span>  |                         | <span data-ttu-id="86f12-263">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-263">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="86f12-264">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="86f12-264">Due to Fabrikam (Fabrikam East)</span></span>  | <span data-ttu-id="86f12-265">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-265">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="86f12-266">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-266">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="86f12-267">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-267">0.00 EUR / 12.90 USD</span></span>    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a><span data-ttu-id="86f12-268">示例 4：来自具有现金折扣和已有汇率损失的其他法人的发票的供应商付款</span><span class="sxs-lookup"><span data-stu-id="86f12-268">Example 4: Vendor payment of invoice from another legal entity with cash discount and realized exchange rate loss</span></span>
<span data-ttu-id="86f12-269">Fabrikam East 为供应商 100 (Fourth Coffee) 具有一个未结发票。</span><span class="sxs-lookup"><span data-stu-id="86f12-269">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="86f12-270">该发票具有可用的现金折扣并且生成增值税交易记录。</span><span class="sxs-lookup"><span data-stu-id="86f12-270">The invoice has a cash discount available, and a sales tax transaction is generated.</span></span> <span data-ttu-id="86f12-271">Fabrikam 过帐 Fabrikam 供应商 3004 (Fourth Coffee) 的付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-271">Fabrikam posts a payment for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="86f12-272">该付款用未结 Fabrikam East 发票结算。</span><span class="sxs-lookup"><span data-stu-id="86f12-272">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="86f12-273">在结算过程中将生成币种汇率损失交易记录。</span><span class="sxs-lookup"><span data-stu-id="86f12-273">A currency exchange loss transaction is generated during the settlement process.</span></span> <span data-ttu-id="86f12-274">现金折扣过帐到发票法人 (Fabrikam East)，且币种汇率损失过帐到付款法人 (Fabrikam)。</span><span class="sxs-lookup"><span data-stu-id="86f12-274">The cash discount is posted to the legal entity of the invoice (Fabrikam East), and the currency exchange loss is posted to the legal entity of the payment (Fabrikam).</span></span>

-   <span data-ttu-id="86f12-275">在发票日期的欧元到美元的汇率：1.2062</span><span class="sxs-lookup"><span data-stu-id="86f12-275">Exchange rate for EUR to USD as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="86f12-276">在付款日期的欧元到美元的汇率：1.2277</span><span class="sxs-lookup"><span data-stu-id="86f12-276">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a><span data-ttu-id="86f12-277">过帐发票，并且在 Fabrikam East 中为供应商 100 生成纳税交易记录</span><span class="sxs-lookup"><span data-stu-id="86f12-277">Invoice is posted and a tax transaction is generated in Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="86f12-278">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-278">Account</span></span>                          | <span data-ttu-id="86f12-279">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-279">Debit amount</span></span>            | <span data-ttu-id="86f12-280">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-280">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="86f12-281">支出 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-281">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="86f12-282">564.07 EUR / 680.38 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-282">564.07 EUR / 680.38 USD</span></span> |                         |
| <span data-ttu-id="86f12-283">增值税 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-283">Sales tax (Fabrikam East)</span></span>        | <span data-ttu-id="86f12-284">35.93 EUR / 43.34 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-284">35.93 EUR / 43.34 USD</span></span>   |                         |
| <span data-ttu-id="86f12-285">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-285">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="86f12-286">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-286">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a><span data-ttu-id="86f12-287">在 Fabrikam 中为供应商 3004 生成和过帐付款</span><span class="sxs-lookup"><span data-stu-id="86f12-287">Payment is generated and posted in Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="86f12-288">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-288">Account</span></span>                     | <span data-ttu-id="86f12-289">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-289">Debit amount</span></span>            | <span data-ttu-id="86f12-290">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-290">Credit amount</span></span>           |
|-----------------------------|-------------------------|-------------------------|
| <span data-ttu-id="86f12-291">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-291">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="86f12-292">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-292">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="86f12-293">现金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-293">Cash (Fabrikam East)</span></span>        |                         | <span data-ttu-id="86f12-294">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-294">588.72 EUR / 722.77 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="86f12-295">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="86f12-295">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="86f12-296">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-296">**Fabrikam posting**</span></span>

| <span data-ttu-id="86f12-297">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-297">Account</span></span>                           | <span data-ttu-id="86f12-298">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-298">Debit amount</span></span>            | <span data-ttu-id="86f12-299">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-299">Credit amount</span></span>           |
|-----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="86f12-300">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="86f12-300">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="86f12-301">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-301">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="86f12-302">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-302">Accounts payable (Fabrikam)</span></span>       |                         | <span data-ttu-id="86f12-303">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-303">588.72 EUR / 722.77 USD</span></span> |
| <span data-ttu-id="86f12-304">已有损失 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-304">Realized loss (Fabrikam)</span></span>          | <span data-ttu-id="86f12-305">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-305">0.00 EUR / 12.66 USD</span></span>    |                         |
| <span data-ttu-id="86f12-306">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="86f12-306">Due from Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="86f12-307">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-307">0.00 EUR / 12.66 USD</span></span>    |

<span data-ttu-id="86f12-308">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-308">**Fabrikam East posting**</span></span>

| <span data-ttu-id="86f12-309">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-309">Account</span></span>                          | <span data-ttu-id="86f12-310">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-310">Debit amount</span></span>            | <span data-ttu-id="86f12-311">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-311">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="86f12-312">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-312">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="86f12-313">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-313">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="86f12-314">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="86f12-314">Due to Fabrikam (Fabrikam East)</span></span>  |                         | <span data-ttu-id="86f12-315">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-315">588.72 EUR / 722.77 USD</span></span> |
| <span data-ttu-id="86f12-316">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="86f12-316">Due to Fabrikam (Fabrikam East</span></span>   | <span data-ttu-id="86f12-317">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-317">0.00 EUR / 12.66 USD</span></span>    |                         |
| <span data-ttu-id="86f12-318">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-318">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="86f12-319">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-319">0.00 EUR / 12.66 USD</span></span>    |
| <span data-ttu-id="86f12-320">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-320">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="86f12-321">11.28 EUR / 13.61 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-321">11.28 EUR / 13.61 USD</span></span>   |                         |
| <span data-ttu-id="86f12-322">现金折扣 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-322">Cash discount (Fabrikam East)</span></span>    |                         | <span data-ttu-id="86f12-323">11.28 EUR / 13.61 USD</span><span class="sxs-lookup"><span data-stu-id="86f12-323">11.28 EUR / 13.61 USD</span></span>   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a><span data-ttu-id="86f12-324">示例 5：具有主付款的供应商贷方通知单</span><span class="sxs-lookup"><span data-stu-id="86f12-324">Example 5: Vendor credit note with primary payment</span></span>
<span data-ttu-id="86f12-325">Fabrikam 为供应商 3004 (Fourth Coffee) 生成 75.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-325">Fabrikam generates a payment of 75.00 for vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="86f12-326">该付款用针对 Fabrikam West 供应商 3004 的未结发票和针对 Fabrikam East 供应商 100 的未结贷方通知单结算。</span><span class="sxs-lookup"><span data-stu-id="86f12-326">The payment is settled with an open invoice for Fabrikam West vendor 3004 and an open credit note for Fabrikam East vendor 100.</span></span> <span data-ttu-id="86f12-327">该付款在**未结交易记录编辑**页中选择为主付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-327">The payment is selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a><span data-ttu-id="86f12-328">发票为供应商 3004 过帐到 Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="86f12-328">Invoice is posted to Fabrikam West for vendor 3004</span></span>

| <span data-ttu-id="86f12-329">帐户</span><span class="sxs-lookup"><span data-stu-id="86f12-329">Account</span></span>                          | <span data-ttu-id="86f12-330">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-330">Debit amount</span></span> | <span data-ttu-id="86f12-331">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-331">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-332">支出 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="86f12-332">Expense (Fabrikam West)</span></span>          | <span data-ttu-id="86f12-333">100.00</span><span class="sxs-lookup"><span data-stu-id="86f12-333">100.00</span></span>       |               |
| <span data-ttu-id="86f12-334">应付帐款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="86f12-334">Accounts payable (Fabrikam West)</span></span> |              | <span data-ttu-id="86f12-335">100.00</span><span class="sxs-lookup"><span data-stu-id="86f12-335">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a><span data-ttu-id="86f12-336">贷方通知单为供应商 100 过帐到 Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="86f12-336">Credit note is posted to Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="86f12-337">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-337">Account</span></span>                          | <span data-ttu-id="86f12-338">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-338">Debit amount</span></span> | <span data-ttu-id="86f12-339">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-339">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-340">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-340">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="86f12-341">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-341">25.00</span></span>        |               |
| <span data-ttu-id="86f12-342">采购退货 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-342">Purchase returns (Fabrikam East)</span></span> |              | <span data-ttu-id="86f12-343">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-343">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a><span data-ttu-id="86f12-344">付款为供应商 3004 过帐到 Fabrikam</span><span class="sxs-lookup"><span data-stu-id="86f12-344">Payment is posted to Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="86f12-345">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-345">Account</span></span>                     | <span data-ttu-id="86f12-346">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-346">Debit amount</span></span> | <span data-ttu-id="86f12-347">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-347">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="86f12-348">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-348">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="86f12-349">75.00</span><span class="sxs-lookup"><span data-stu-id="86f12-349">75.00</span></span>        |               |
| <span data-ttu-id="86f12-350">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-350">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="86f12-351">75.00</span><span class="sxs-lookup"><span data-stu-id="86f12-351">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="86f12-352">Fabrikam 付款用 Fabrikam West 发票和 Fabrikam East 贷方通知单结算</span><span class="sxs-lookup"><span data-stu-id="86f12-352">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="86f12-353">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-353">**Fabrikam posting**</span></span>

| <span data-ttu-id="86f12-354">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-354">Account</span></span>                           | <span data-ttu-id="86f12-355">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-355">Debit amount</span></span> | <span data-ttu-id="86f12-356">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-356">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-357">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-357">Accounts payable (Fabrikam)</span></span>       | <span data-ttu-id="86f12-358">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-358">25.00</span></span>        |               |
| <span data-ttu-id="86f12-359">向 Fabrikam East (Fabrikam) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="86f12-359">Due to Fabrikam East (Fabrikam)</span></span>   |              | <span data-ttu-id="86f12-360">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-360">25.00</span></span>         |
| <span data-ttu-id="86f12-361">从 Fabrikam West (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="86f12-361">Due from Fabrikam West (Fabrikam)</span></span> | <span data-ttu-id="86f12-362">100.00</span><span class="sxs-lookup"><span data-stu-id="86f12-362">100.00</span></span>       |               |
| <span data-ttu-id="86f12-363">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-363">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="86f12-364">100.00</span><span class="sxs-lookup"><span data-stu-id="86f12-364">100.00</span></span>        |

<span data-ttu-id="86f12-365">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-365">**Fabrikam East posting**</span></span>

| <span data-ttu-id="86f12-366">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-366">Account</span></span>                           | <span data-ttu-id="86f12-367">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-367">Debit amount</span></span> | <span data-ttu-id="86f12-368">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-368">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-369">从 Fabrikam (Fabrikam East) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="86f12-369">Due from Fabrikam (Fabrikam East)</span></span> | <span data-ttu-id="86f12-370">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-370">25.00</span></span>        |               |
| <span data-ttu-id="86f12-371">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-371">Accounts payable (Fabrikam East)</span></span>  |              | <span data-ttu-id="86f12-372">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-372">25.00</span></span>         |

<span data-ttu-id="86f12-373">**Fabrikam West 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-373">**Fabrikam West posting**</span></span>

| <span data-ttu-id="86f12-374">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-374">Account</span></span>                          | <span data-ttu-id="86f12-375">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-375">Debit amount</span></span> | <span data-ttu-id="86f12-376">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-376">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-377">应付帐款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="86f12-377">Accounts payable (Fabrikam West)</span></span> | <span data-ttu-id="86f12-378">100.00</span><span class="sxs-lookup"><span data-stu-id="86f12-378">100.00</span></span>       |               |
| <span data-ttu-id="86f12-379">向 Fabrikam (Fabrikam West) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="86f12-379">Due to Fabrikam (Fabrikam West)</span></span>  |              | <span data-ttu-id="86f12-380">100.00</span><span class="sxs-lookup"><span data-stu-id="86f12-380">100.00</span></span>        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a><span data-ttu-id="86f12-381">示例 6：不具有主付款的供应商贷方通知单</span><span class="sxs-lookup"><span data-stu-id="86f12-381">Example 6: Vendor credit note without primary payment</span></span>
<span data-ttu-id="86f12-382">Fabrikam 为供应商 3004 (Fourth Coffee) 生成 75.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-382">Fabrikam generates a payment of 75.00 for vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="86f12-383">该付款用针对 Fabrikam West 供应商 3004 的未结发票和针对 Fabrikam East 供应商 100 的未结贷方通知单结算。</span><span class="sxs-lookup"><span data-stu-id="86f12-383">The payment is settled with an open invoice for Fabrikam West vendor 3004 and an open credit note for Fabrikam East vendor 100.</span></span> <span data-ttu-id="86f12-384">该付款未在**未结交易记录编辑**页中选择为主付款。</span><span class="sxs-lookup"><span data-stu-id="86f12-384">The payment isn't selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a><span data-ttu-id="86f12-385">发票为供应商 3004 过帐到 Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="86f12-385">Invoice is posted to Fabrikam West for vendor 3004</span></span>

| <span data-ttu-id="86f12-386">帐户</span><span class="sxs-lookup"><span data-stu-id="86f12-386">Account</span></span>                          | <span data-ttu-id="86f12-387">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-387">Debit amount</span></span> | <span data-ttu-id="86f12-388">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-388">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-389">支出 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="86f12-389">Expense (Fabrikam West)</span></span>          | <span data-ttu-id="86f12-390">100.00</span><span class="sxs-lookup"><span data-stu-id="86f12-390">100.00</span></span>       |               |
| <span data-ttu-id="86f12-391">应付帐款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="86f12-391">Accounts payable (Fabrikam West)</span></span> |              | <span data-ttu-id="86f12-392">100.00</span><span class="sxs-lookup"><span data-stu-id="86f12-392">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a><span data-ttu-id="86f12-393">贷方通知单为供应商 100 过帐到 Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="86f12-393">Credit note is posted to Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="86f12-394">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-394">Account</span></span>                          | <span data-ttu-id="86f12-395">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-395">Debit amount</span></span> | <span data-ttu-id="86f12-396">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-396">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-397">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-397">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="86f12-398">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-398">25.00</span></span>        |               |
| <span data-ttu-id="86f12-399">采购退货 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-399">Purchase returns (Fabrikam East)</span></span> |              | <span data-ttu-id="86f12-400">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-400">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a><span data-ttu-id="86f12-401">付款为供应商 3004 过帐到 Fabrikam</span><span class="sxs-lookup"><span data-stu-id="86f12-401">Payment is posted to Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="86f12-402">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-402">Account</span></span>                     | <span data-ttu-id="86f12-403">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-403">Debit amount</span></span> | <span data-ttu-id="86f12-404">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-404">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="86f12-405">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-405">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="86f12-406">75.00</span><span class="sxs-lookup"><span data-stu-id="86f12-406">75.00</span></span>        |               |
| <span data-ttu-id="86f12-407">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-407">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="86f12-408">75.00</span><span class="sxs-lookup"><span data-stu-id="86f12-408">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="86f12-409">Fabrikam 付款用 Fabrikam West 发票和 Fabrikam East 贷方通知单结算</span><span class="sxs-lookup"><span data-stu-id="86f12-409">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="86f12-410">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-410">**Fabrikam posting**</span></span>

| <span data-ttu-id="86f12-411">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-411">Account</span></span>                           | <span data-ttu-id="86f12-412">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-412">Debit amount</span></span> | <span data-ttu-id="86f12-413">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-413">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-414">从 Fabrikam West (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="86f12-414">Due from Fabrikam West (Fabrikam)</span></span> | <span data-ttu-id="86f12-415">75.00</span><span class="sxs-lookup"><span data-stu-id="86f12-415">75.00</span></span>        |               |
| <span data-ttu-id="86f12-416">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="86f12-416">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="86f12-417">75.00</span><span class="sxs-lookup"><span data-stu-id="86f12-417">75.00</span></span>         |

<span data-ttu-id="86f12-418">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-418">**Fabrikam East posting**</span></span>

| <span data-ttu-id="86f12-419">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-419">Account</span></span>                                | <span data-ttu-id="86f12-420">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-420">Debit amount</span></span> | <span data-ttu-id="86f12-421">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-421">Credit amount</span></span> |
|----------------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-422">从 Fabrikam West (Fabrikam East) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="86f12-422">Due from Fabrikam West (Fabrikam East)</span></span> | <span data-ttu-id="86f12-423">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-423">25.00</span></span>        |               |
| <span data-ttu-id="86f12-424">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="86f12-424">Accounts payable (Fabrikam East)</span></span>       |              | <span data-ttu-id="86f12-425">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-425">25.00</span></span>         |

<span data-ttu-id="86f12-426">**Fabrikam West 过帐**</span><span class="sxs-lookup"><span data-stu-id="86f12-426">**Fabrikam West posting**</span></span>

| <span data-ttu-id="86f12-427">科目</span><span class="sxs-lookup"><span data-stu-id="86f12-427">Account</span></span>                              | <span data-ttu-id="86f12-428">借方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-428">Debit amount</span></span> | <span data-ttu-id="86f12-429">贷方金额</span><span class="sxs-lookup"><span data-stu-id="86f12-429">Credit amount</span></span> |
|--------------------------------------|--------------|---------------|
| <span data-ttu-id="86f12-430">应付帐款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="86f12-430">Accounts payable (Fabrikam West)</span></span>     | <span data-ttu-id="86f12-431">75.00</span><span class="sxs-lookup"><span data-stu-id="86f12-431">75.00</span></span>        |               |
| <span data-ttu-id="86f12-432">向 Fabrikam (Fabrikam West) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="86f12-432">Due to Fabrikam (Fabrikam West)</span></span>      |              | <span data-ttu-id="86f12-433">75.00</span><span class="sxs-lookup"><span data-stu-id="86f12-433">75.00</span></span>         |
| <span data-ttu-id="86f12-434">应付账款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="86f12-434">Accounts payable (Fabrikam West)</span></span>     | <span data-ttu-id="86f12-435">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-435">25.00</span></span>        |               |
| <span data-ttu-id="86f12-436">向 Fabrikam East (Fabrikam West) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="86f12-436">Due to Fabrikam East (Fabrikam West)</span></span> |              | <span data-ttu-id="86f12-437">25.00</span><span class="sxs-lookup"><span data-stu-id="86f12-437">25.00</span></span>         |





