---
title: "应付帐款的集中付款"
description: "包括多个法人的组织可以使用处理所有付款的单个法人创建和管理付款。 因此，不必在多个法人中输入同一付款。 本文提供显示集中付款过帐如何在不同环境中处理的示例。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14341
ms.assetid: 7bd02e32-2416-4ac6-8a60-85525267fdb7
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 49d5242168cd43e78dd4b0c63da363f91f680904
ms.contentlocale: zh-cn
ms.lasthandoff: 08/29/2017

---

# <a name="centralized-payments-for-accounts-payable"></a><span data-ttu-id="ede41-105">应付帐款的集中付款</span><span class="sxs-lookup"><span data-stu-id="ede41-105">Centralized payments for Accounts payable</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ede41-106">包括多个法人的组织可以使用处理所有付款的单个法人创建和管理付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-106">Organizations that include multiple legal entities can create and manage payments by using a single legal entity that handles all payments.</span></span> <span data-ttu-id="ede41-107">因此，不必在多个法人中输入同一付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-107">Therefore, the same payments don't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="ede41-108">本文提供显示集中付款过帐如何在不同环境中处理的示例。</span><span class="sxs-lookup"><span data-stu-id="ede41-108">This article provides examples that show how posting for centralized payments is handled in various scenarios.</span></span>

<span data-ttu-id="ede41-109">包括多个法人的组织可以使用处理所有付款的法人创建和管理付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-109">Organizations that include multiple legal entities can create and manage payments by using a legal entity that handles all payments.</span></span> <span data-ttu-id="ede41-110">因此，不必在多个法人中输入同一付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-110">Therefore, the same payments don't have to be entered in multiple legal entities.</span></span> <span data-ttu-id="ede41-111">此外，组织节省时间，因为付款流程简化。</span><span class="sxs-lookup"><span data-stu-id="ede41-111">Additionally, the organization saves time, because the payment process is streamlined.</span></span>

<span data-ttu-id="ede41-112">在集中付款的组织中，有很多营业的法人，且每个营业的法人都管理自己的供应商发票。</span><span class="sxs-lookup"><span data-stu-id="ede41-112">In a centralized payments organization, there are many legal entities for operations, and each operating legal entity manages its own vendor invoices.</span></span> <span data-ttu-id="ede41-113">所有营业的法人的付款都是从称作付款的法人的单个法人中生成的。</span><span class="sxs-lookup"><span data-stu-id="ede41-113">Payments for all the operating legal entities are generated from a single legal entity, which is known as the legal entity of the payment.</span></span> <span data-ttu-id="ede41-114">在结算流程中，生成适用的应付和应收交易记录。</span><span class="sxs-lookup"><span data-stu-id="ede41-114">During the settlement process, the applicable due-to and due-from transactions are generated.</span></span> <span data-ttu-id="ede41-115">您可以指定组织内的哪个法人接收已有收益或已有损失交易记录，以及如何处理与跨公司付款相关的现金折扣交易记录。</span><span class="sxs-lookup"><span data-stu-id="ede41-115">You can specify which legal entity in the organization receives the realized gain or realized loss transactions, and how cash discount transactions that are related to a cross-company payment are handled.</span></span> 

<span data-ttu-id="ede41-116">以下示例说明如何在不同的环境中处理过帐。</span><span class="sxs-lookup"><span data-stu-id="ede41-116">The following examples illustrate how posting is handled in various scenarios.</span></span> <span data-ttu-id="ede41-117">假定所有这些示例都采用以下配置：</span><span class="sxs-lookup"><span data-stu-id="ede41-117">The following configuration is assumed for all these examples:</span></span>

-   <span data-ttu-id="ede41-118">法人分别为 Fabrikam、Fabrikam East 和 Fabrikam West。</span><span class="sxs-lookup"><span data-stu-id="ede41-118">The legal entities are Fabrikam, Fabrikam East, and Fabrikam West.</span></span> <span data-ttu-id="ede41-119">从 Fabrikam 进行付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-119">Payments are made from Fabrikam.</span></span>
-   <span data-ttu-id="ede41-120">**“内部公司”**页上的**“过帐现金折扣”**字段设置为**“发票法人”**。</span><span class="sxs-lookup"><span data-stu-id="ede41-120">The **Post cash discount** field on the **Intercompany accounting** page is set to **Legal entity of the invoice**.</span></span>
-   <span data-ttu-id="ede41-121">**“内部公司”**页上的**“过帐币种汇兑损益”**字段设置为**“付款法人”**。</span><span class="sxs-lookup"><span data-stu-id="ede41-121">The **Post currency exchange gain or loss** field on the **Intercompany accounting** page is set to **Legal entity of the payment**.</span></span>
-   <span data-ttu-id="ede41-122">客户 Fourth Coffee 在每个法人中设置为一个供应商。</span><span class="sxs-lookup"><span data-stu-id="ede41-122">The vendor Fourth Coffee is set up as a vendor in each legal entity.</span></span> <span data-ttu-id="ede41-123">来自不同法人的供应商被标识为同一供应商，因为他们共享相同的全球通讯簿 ID。</span><span class="sxs-lookup"><span data-stu-id="ede41-123">The vendors from the various legal entities are identified as the same vendor because they share the same global address book ID.</span></span>

| <span data-ttu-id="ede41-124">名录 ID</span><span class="sxs-lookup"><span data-stu-id="ede41-124">Directory ID</span></span> | <span data-ttu-id="ede41-125">供应商帐户</span><span class="sxs-lookup"><span data-stu-id="ede41-125">Vendor account</span></span> | <span data-ttu-id="ede41-126">姓名</span><span class="sxs-lookup"><span data-stu-id="ede41-126">Name</span></span>          | <span data-ttu-id="ede41-127">法人</span><span class="sxs-lookup"><span data-stu-id="ede41-127">Legal entity</span></span>  |
|--------------|----------------|---------------|---------------|
| <span data-ttu-id="ede41-128">1050</span><span class="sxs-lookup"><span data-stu-id="ede41-128">1050</span></span>         | <span data-ttu-id="ede41-129">3004</span><span class="sxs-lookup"><span data-stu-id="ede41-129">3004</span></span>           | <span data-ttu-id="ede41-130">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="ede41-130">Fourth Coffee</span></span> | <span data-ttu-id="ede41-131">Fabrikam</span><span class="sxs-lookup"><span data-stu-id="ede41-131">Fabrikam</span></span>      |
| <span data-ttu-id="ede41-132">1050</span><span class="sxs-lookup"><span data-stu-id="ede41-132">1050</span></span>         | <span data-ttu-id="ede41-133">100</span><span class="sxs-lookup"><span data-stu-id="ede41-133">100</span></span>            | <span data-ttu-id="ede41-134">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="ede41-134">Fourth Coffee</span></span> | <span data-ttu-id="ede41-135">Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="ede41-135">Fabrikam East</span></span> |
| <span data-ttu-id="ede41-136">1050</span><span class="sxs-lookup"><span data-stu-id="ede41-136">1050</span></span>         | <span data-ttu-id="ede41-137">3004</span><span class="sxs-lookup"><span data-stu-id="ede41-137">3004</span></span>           | <span data-ttu-id="ede41-138">Fourth Coffee</span><span class="sxs-lookup"><span data-stu-id="ede41-138">Fourth Coffee</span></span> | <span data-ttu-id="ede41-139">Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="ede41-139">Fabrikam West</span></span> |

## <a name="example-1-vendor-payment-of-invoice-from-another-legal-entity"></a><span data-ttu-id="ede41-140">示例 1：来自其他法人的发票的供应商付款</span><span class="sxs-lookup"><span data-stu-id="ede41-140">Example 1: Vendor payment of invoice from another legal entity</span></span>
<span data-ttu-id="ede41-141">Fabrikam East 为供应商帐户 100 (Fourth Coffee) 具有一个未结发票。</span><span class="sxs-lookup"><span data-stu-id="ede41-141">Fabrikam East has an open invoice for vendor account 100, Fourth Coffee.</span></span> <span data-ttu-id="ede41-142">Fabrikam 输入付款并将付款过帐到 Fabrikam 供应商帐户 3004 (Fourth Coffee)。</span><span class="sxs-lookup"><span data-stu-id="ede41-142">Fabrikam enters and posts a payment to Fabrikam vendor account 3004, Fourth Coffee.</span></span> <span data-ttu-id="ede41-143">该付款用该未结发票结算。</span><span class="sxs-lookup"><span data-stu-id="ede41-143">The payment is settled with the open invoice.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-vendor-100"></a><span data-ttu-id="ede41-144">在 Fabrikam East 中为供应商 100 过帐发票</span><span class="sxs-lookup"><span data-stu-id="ede41-144">Invoice is posted in Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="ede41-145">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-145">Account</span></span>                          | <span data-ttu-id="ede41-146">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-146">Debit amount</span></span> | <span data-ttu-id="ede41-147">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-147">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-148">支出 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-148">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="ede41-149">600.00</span><span class="sxs-lookup"><span data-stu-id="ede41-149">600.00</span></span>       |               |
| <span data-ttu-id="ede41-150">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-150">Accounts payable (Fabrikam East)</span></span> |              | <span data-ttu-id="ede41-151">600.00</span><span class="sxs-lookup"><span data-stu-id="ede41-151">600.00</span></span>        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a><span data-ttu-id="ede41-152">在 Fabrikam 中为供应商 3004 生成和过帐付款</span><span class="sxs-lookup"><span data-stu-id="ede41-152">Payment is generated and posted in Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="ede41-153">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-153">Account</span></span>                     | <span data-ttu-id="ede41-154">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-154">Debit amount</span></span> | <span data-ttu-id="ede41-155">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-155">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="ede41-156">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-156">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="ede41-157">600.00</span><span class="sxs-lookup"><span data-stu-id="ede41-157">600.00</span></span>       |               |
| <span data-ttu-id="ede41-158">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-158">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="ede41-159">600.00</span><span class="sxs-lookup"><span data-stu-id="ede41-159">600.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="ede41-160">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="ede41-160">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="ede41-161">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-161">**Fabrikam posting**</span></span>

| <span data-ttu-id="ede41-162">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-162">Account</span></span>                           | <span data-ttu-id="ede41-163">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-163">Debit amount</span></span> | <span data-ttu-id="ede41-164">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-164">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-165">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="ede41-165">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="ede41-166">600.00</span><span class="sxs-lookup"><span data-stu-id="ede41-166">600.00</span></span>       |               |
| <span data-ttu-id="ede41-167">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-167">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="ede41-168">600.00</span><span class="sxs-lookup"><span data-stu-id="ede41-168">600.00</span></span>        |

<span data-ttu-id="ede41-169">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-169">**Fabrikam East posting**</span></span>

| <span data-ttu-id="ede41-170">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-170">Account</span></span>                          | <span data-ttu-id="ede41-171">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-171">Debit amount</span></span> | <span data-ttu-id="ede41-172">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-172">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-173">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-173">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="ede41-174">600.00</span><span class="sxs-lookup"><span data-stu-id="ede41-174">600.00</span></span>       |               |
| <span data-ttu-id="ede41-175">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="ede41-175">Due to Fabrikam (Fabrikam East)</span></span>  |              | <span data-ttu-id="ede41-176">600.00</span><span class="sxs-lookup"><span data-stu-id="ede41-176">600.00</span></span>        |

## <a name="example-2-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount"></a><span data-ttu-id="ede41-177">示例 2：来自具有现金折扣的其他法人的发票的供应商付款</span><span class="sxs-lookup"><span data-stu-id="ede41-177">Example 2: Vendor payment of invoice from another legal entity with cash discount</span></span>
<span data-ttu-id="ede41-178">Fabrikam East 为供应商 100 (Fourth Coffee) 具有一个未结发票。</span><span class="sxs-lookup"><span data-stu-id="ede41-178">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="ede41-179">该发票具有 20.00 的可用现金折扣。</span><span class="sxs-lookup"><span data-stu-id="ede41-179">The invoice has a 20.00 cash discount available.</span></span> <span data-ttu-id="ede41-180">Fabrikam 为 Fabrikam 供应商 3004 (Fourth Coffee) 输入并过帐了 580.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-180">Fabrikam enters and posts a payment of 580.00 for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="ede41-181">该付款用未结 Fabrikam East 发票结算。</span><span class="sxs-lookup"><span data-stu-id="ede41-181">The payment is settled with the open Fabrikam East invoices.</span></span> <span data-ttu-id="ede41-182">该现金折扣过帐到发票法人 Fabrikam East。</span><span class="sxs-lookup"><span data-stu-id="ede41-182">The cash discount is posted to the legal entity of the invoice, Fabrikam East.</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a><span data-ttu-id="ede41-183">在 Fabrikam East 中为 Fabrikam East 供应商 100 过帐发票</span><span class="sxs-lookup"><span data-stu-id="ede41-183">Invoice is posted in Fabrikam East for Fabrikam East vendor 100</span></span>

| <span data-ttu-id="ede41-184">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-184">Account</span></span>                          | <span data-ttu-id="ede41-185">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-185">Debit amount</span></span> | <span data-ttu-id="ede41-186">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-186">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-187">支出 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-187">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="ede41-188">600.00</span><span class="sxs-lookup"><span data-stu-id="ede41-188">600.00</span></span>       |               |
| <span data-ttu-id="ede41-189">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-189">Accounts payable (Fabrikam East)</span></span> |              | <span data-ttu-id="ede41-190">600.00</span><span class="sxs-lookup"><span data-stu-id="ede41-190">600.00</span></span>        |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a><span data-ttu-id="ede41-191">在 Fabrikam 中为 Fabrikam 供应商 3004 生成和过帐付款</span><span class="sxs-lookup"><span data-stu-id="ede41-191">Payment is generated and posted in Fabrikam for Fabrikam vendor 3004</span></span>

| <span data-ttu-id="ede41-192">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-192">Account</span></span>                     | <span data-ttu-id="ede41-193">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-193">Debit amount</span></span> | <span data-ttu-id="ede41-194">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-194">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="ede41-195">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-195">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="ede41-196">580.00</span><span class="sxs-lookup"><span data-stu-id="ede41-196">580.00</span></span>       |               |
| <span data-ttu-id="ede41-197">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-197">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="ede41-198">580.00</span><span class="sxs-lookup"><span data-stu-id="ede41-198">580.00</span></span>        |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="ede41-199">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="ede41-199">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="ede41-200">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-200">**Fabrikam posting**</span></span>

| <span data-ttu-id="ede41-201">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-201">Account</span></span>                           | <span data-ttu-id="ede41-202">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-202">Debit amount</span></span> | <span data-ttu-id="ede41-203">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-203">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-204">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="ede41-204">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="ede41-205">580.00</span><span class="sxs-lookup"><span data-stu-id="ede41-205">580.00</span></span>       |               |
| <span data-ttu-id="ede41-206">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-206">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="ede41-207">580.00</span><span class="sxs-lookup"><span data-stu-id="ede41-207">580.00</span></span>        |

<span data-ttu-id="ede41-208">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-208">**Fabrikam East posting**</span></span>

| <span data-ttu-id="ede41-209">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-209">Account</span></span>                          | <span data-ttu-id="ede41-210">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-210">Debit amount</span></span> | <span data-ttu-id="ede41-211">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-211">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-212">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-212">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="ede41-213">580.00</span><span class="sxs-lookup"><span data-stu-id="ede41-213">580.00</span></span>       |               |
| <span data-ttu-id="ede41-214">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="ede41-214">Due to Fabrikam (Fabrikam East)</span></span>  |              | <span data-ttu-id="ede41-215">580.00</span><span class="sxs-lookup"><span data-stu-id="ede41-215">580.00</span></span>        |
| <span data-ttu-id="ede41-216">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-216">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="ede41-217">20.00</span><span class="sxs-lookup"><span data-stu-id="ede41-217">20.00</span></span>        |               |
| <span data-ttu-id="ede41-218">现金折扣 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-218">Cash discount (Fabrikam East)</span></span>    |              | <span data-ttu-id="ede41-219">20.00</span><span class="sxs-lookup"><span data-stu-id="ede41-219">20.00</span></span>         |

## <a name="example-3-vendor-payment-of-invoice-from-another-legal-entity-with-realized-exchange-rate-loss"></a><span data-ttu-id="ede41-220">示例 3：来自具有已有汇率损失的其他法人的发票的供应商付款</span><span class="sxs-lookup"><span data-stu-id="ede41-220">Example 3: Vendor payment of invoice from another legal entity with realized exchange rate loss</span></span>
<span data-ttu-id="ede41-221">Fabrikam East 为供应商 100 (Fourth Coffee) 具有一个未结发票。</span><span class="sxs-lookup"><span data-stu-id="ede41-221">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="ede41-222">Fabrikam 输入并过帐 Fabrikam 供应商 3004 (Fourth Coffee) 的付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-222">Fabrikam enters and posts a payment for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="ede41-223">该付款用未结 Fabrikam East 发票结算。</span><span class="sxs-lookup"><span data-stu-id="ede41-223">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="ede41-224">在结算过程中将生成币种汇率损失交易记录。</span><span class="sxs-lookup"><span data-stu-id="ede41-224">A currency exchange loss transaction is generated during the settlement process.</span></span>

-   <span data-ttu-id="ede41-225">在发票日期的欧元 (EUR) 到美元 (USD) 的汇率：1.2062</span><span class="sxs-lookup"><span data-stu-id="ede41-225">Exchange rate for euros (EUR) to U.S. dollars (USD) as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="ede41-226">在付款日期的欧元到美元的汇率：1.2277</span><span class="sxs-lookup"><span data-stu-id="ede41-226">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-in-fabrikam-east-for-fabrikam-east-vendor-100"></a><span data-ttu-id="ede41-227">在 Fabrikam East 中为 Fabrikam East 供应商 100 过帐发票</span><span class="sxs-lookup"><span data-stu-id="ede41-227">Invoice is posted in Fabrikam East for Fabrikam East vendor 100</span></span>

| <span data-ttu-id="ede41-228">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-228">Account</span></span>                          | <span data-ttu-id="ede41-229">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-229">Debit amount</span></span>            | <span data-ttu-id="ede41-230">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-230">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="ede41-231">支出 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-231">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="ede41-232">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-232">600.00 EUR / 723.72 USD</span></span> |                         |
| <span data-ttu-id="ede41-233">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-233">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="ede41-234">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-234">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-fabrikam-vendor-3004"></a><span data-ttu-id="ede41-235">在 Fabrikam 中为 Fabrikam 供应商 3004 生成和过帐付款</span><span class="sxs-lookup"><span data-stu-id="ede41-235">Payment is generated and posted in Fabrikam for Fabrikam vendor 3004</span></span>

| <span data-ttu-id="ede41-236">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-236">Account</span></span>                     | <span data-ttu-id="ede41-237">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-237">Debit amount</span></span>            | <span data-ttu-id="ede41-238">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-238">Credit amount</span></span>           |
|-----------------------------|-------------------------|-------------------------|
| <span data-ttu-id="ede41-239">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-239">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="ede41-240">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-240">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="ede41-241">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-241">Cash (Fabrikam)</span></span>             |                         | <span data-ttu-id="ede41-242">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-242">600.00 EUR / 736.62 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="ede41-243">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="ede41-243">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="ede41-244">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-244">**Fabrikam posting**</span></span>

| <span data-ttu-id="ede41-245">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-245">Account</span></span>                           | <span data-ttu-id="ede41-246">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-246">Debit amount</span></span>            | <span data-ttu-id="ede41-247">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-247">Credit amount</span></span>           |
|-----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="ede41-248">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="ede41-248">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="ede41-249">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-249">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="ede41-250">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-250">Accounts payable (Fabrikam)</span></span>       |                         | <span data-ttu-id="ede41-251">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-251">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="ede41-252">已有损失 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-252">Realized loss (Fabrikam)</span></span>          | <span data-ttu-id="ede41-253">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-253">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="ede41-254">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="ede41-254">Due from Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="ede41-255">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-255">0.00 EUR / 12.90 USD</span></span>    |

<span data-ttu-id="ede41-256">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-256">**Fabrikam East posting**</span></span>

| <span data-ttu-id="ede41-257">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-257">Account</span></span>                          | <span data-ttu-id="ede41-258">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-258">Debit amount</span></span>            | <span data-ttu-id="ede41-259">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-259">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="ede41-260">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-260">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="ede41-261">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-261">600.00 EUR / 736.62 USD</span></span> |                         |
| <span data-ttu-id="ede41-262">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="ede41-262">Due to Fabrikam (Fabrikam East)</span></span>  |                         | <span data-ttu-id="ede41-263">600.00 EUR / 736.62 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-263">600.00 EUR / 736.62 USD</span></span> |
| <span data-ttu-id="ede41-264">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="ede41-264">Due to Fabrikam (Fabrikam East)</span></span>  | <span data-ttu-id="ede41-265">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-265">0.00 EUR / 12.90 USD</span></span>    |                         |
| <span data-ttu-id="ede41-266">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-266">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="ede41-267">0.00 EUR / 12.90 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-267">0.00 EUR / 12.90 USD</span></span>    |

## <a name="example-4-vendor-payment-of-invoice-from-another-legal-entity-with-cash-discount-and-realized-exchange-rate-loss"></a><span data-ttu-id="ede41-268">示例 4：来自具有现金折扣和已有汇率损失的其他法人的发票的供应商付款</span><span class="sxs-lookup"><span data-stu-id="ede41-268">Example 4: Vendor payment of invoice from another legal entity with cash discount and realized exchange rate loss</span></span>
<span data-ttu-id="ede41-269">Fabrikam East 为供应商 100 (Fourth Coffee) 具有一个未结发票。</span><span class="sxs-lookup"><span data-stu-id="ede41-269">Fabrikam East has an open invoice for vendor 100, Fourth Coffee.</span></span> <span data-ttu-id="ede41-270">该发票具有可用的现金折扣并且生成增值税交易记录。</span><span class="sxs-lookup"><span data-stu-id="ede41-270">The invoice has a cash discount available, and a sales tax transaction is generated.</span></span> <span data-ttu-id="ede41-271">Fabrikam 过帐 Fabrikam 供应商 3004 (Fourth Coffee) 的付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-271">Fabrikam posts a payment for Fabrikam vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="ede41-272">该付款用未结 Fabrikam East 发票结算。</span><span class="sxs-lookup"><span data-stu-id="ede41-272">The payment is settled with the open Fabrikam East invoice.</span></span> <span data-ttu-id="ede41-273">在结算过程中将生成币种汇率损失交易记录。</span><span class="sxs-lookup"><span data-stu-id="ede41-273">A currency exchange loss transaction is generated during the settlement process.</span></span> <span data-ttu-id="ede41-274">现金折扣过帐到发票法人 (Fabrikam East)，且币种汇率损失过帐到付款法人 (Fabrikam)。</span><span class="sxs-lookup"><span data-stu-id="ede41-274">The cash discount is posted to the legal entity of the invoice (Fabrikam East), and the currency exchange loss is posted to the legal entity of the payment (Fabrikam).</span></span>

-   <span data-ttu-id="ede41-275">在发票日期的欧元到美元的汇率：1.2062</span><span class="sxs-lookup"><span data-stu-id="ede41-275">Exchange rate for EUR to USD as of the invoice date: 1.2062</span></span>
-   <span data-ttu-id="ede41-276">在付款日期的欧元到美元的汇率：1.2277</span><span class="sxs-lookup"><span data-stu-id="ede41-276">Exchange rate for EUR to USD as of the payment date: 1.2277</span></span>

### <a name="invoice-is-posted-and-a-tax-transaction-is-generated-in-fabrikam-east-for-vendor-100"></a><span data-ttu-id="ede41-277">过帐发票，并且在 Fabrikam East 中为供应商 100 生成纳税交易记录</span><span class="sxs-lookup"><span data-stu-id="ede41-277">Invoice is posted and a tax transaction is generated in Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="ede41-278">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-278">Account</span></span>                          | <span data-ttu-id="ede41-279">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-279">Debit amount</span></span>            | <span data-ttu-id="ede41-280">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-280">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="ede41-281">支出 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-281">Expense (Fabrikam East)</span></span>          | <span data-ttu-id="ede41-282">564.07 EUR / 680.38 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-282">564.07 EUR / 680.38 USD</span></span> |                         |
| <span data-ttu-id="ede41-283">增值税 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-283">Sales tax (Fabrikam East)</span></span>        | <span data-ttu-id="ede41-284">35.93 EUR / 43.34 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-284">35.93 EUR / 43.34 USD</span></span>   |                         |
| <span data-ttu-id="ede41-285">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-285">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="ede41-286">600.00 EUR / 723.72 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-286">600.00 EUR / 723.72 USD</span></span> |

### <a name="payment-is-generated-and-posted-in-fabrikam-for-vendor-3004"></a><span data-ttu-id="ede41-287">在 Fabrikam 中为供应商 3004 生成和过帐付款</span><span class="sxs-lookup"><span data-stu-id="ede41-287">Payment is generated and posted in Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="ede41-288">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-288">Account</span></span>                     | <span data-ttu-id="ede41-289">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-289">Debit amount</span></span>            | <span data-ttu-id="ede41-290">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-290">Credit amount</span></span>           |
|-----------------------------|-------------------------|-------------------------|
| <span data-ttu-id="ede41-291">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-291">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="ede41-292">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-292">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="ede41-293">现金 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-293">Cash (Fabrikam East)</span></span>        |                         | <span data-ttu-id="ede41-294">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-294">588.72 EUR / 722.77 USD</span></span> |

### <a name="fabrikam-payment-is-settled-with-fabrikam-east-invoice"></a><span data-ttu-id="ede41-295">Fabrikam 付款用 Fabrikam East 发票结算</span><span class="sxs-lookup"><span data-stu-id="ede41-295">Fabrikam payment is settled with Fabrikam East invoice</span></span>

<span data-ttu-id="ede41-296">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-296">**Fabrikam posting**</span></span>

| <span data-ttu-id="ede41-297">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-297">Account</span></span>                           | <span data-ttu-id="ede41-298">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-298">Debit amount</span></span>            | <span data-ttu-id="ede41-299">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-299">Credit amount</span></span>           |
|-----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="ede41-300">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="ede41-300">Due from Fabrikam East (Fabrikam)</span></span> | <span data-ttu-id="ede41-301">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-301">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="ede41-302">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-302">Accounts payable (Fabrikam)</span></span>       |                         | <span data-ttu-id="ede41-303">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-303">588.72 EUR / 722.77 USD</span></span> |
| <span data-ttu-id="ede41-304">已有损失 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-304">Realized loss (Fabrikam)</span></span>          | <span data-ttu-id="ede41-305">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-305">0.00 EUR / 12.66 USD</span></span>    |                         |
| <span data-ttu-id="ede41-306">从 Fabrikam East (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="ede41-306">Due from Fabrikam East (Fabrikam)</span></span> |                         | <span data-ttu-id="ede41-307">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-307">0.00 EUR / 12.66 USD</span></span>    |

<span data-ttu-id="ede41-308">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-308">**Fabrikam East posting**</span></span>

| <span data-ttu-id="ede41-309">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-309">Account</span></span>                          | <span data-ttu-id="ede41-310">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-310">Debit amount</span></span>            | <span data-ttu-id="ede41-311">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-311">Credit amount</span></span>           |
|----------------------------------|-------------------------|-------------------------|
| <span data-ttu-id="ede41-312">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-312">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="ede41-313">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-313">588.72 EUR / 722.77 USD</span></span> |                         |
| <span data-ttu-id="ede41-314">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="ede41-314">Due to Fabrikam (Fabrikam East)</span></span>  |                         | <span data-ttu-id="ede41-315">588.72 EUR / 722.77 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-315">588.72 EUR / 722.77 USD</span></span> |
| <span data-ttu-id="ede41-316">向 Fabrikam (Fabrikam East) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="ede41-316">Due to Fabrikam (Fabrikam East</span></span>   | <span data-ttu-id="ede41-317">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-317">0.00 EUR / 12.66 USD</span></span>    |                         |
| <span data-ttu-id="ede41-318">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-318">Accounts payable (Fabrikam East)</span></span> |                         | <span data-ttu-id="ede41-319">0.00 EUR / 12.66 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-319">0.00 EUR / 12.66 USD</span></span>    |
| <span data-ttu-id="ede41-320">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-320">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="ede41-321">11.28 EUR / 13.61 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-321">11.28 EUR / 13.61 USD</span></span>   |                         |
| <span data-ttu-id="ede41-322">现金折扣 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-322">Cash discount (Fabrikam East)</span></span>    |                         | <span data-ttu-id="ede41-323">11.28 EUR / 13.61 USD</span><span class="sxs-lookup"><span data-stu-id="ede41-323">11.28 EUR / 13.61 USD</span></span>   |

## <a name="example-5-vendor-credit-note-with-primary-payment"></a><span data-ttu-id="ede41-324">示例 5：具有主付款的供应商贷方通知单</span><span class="sxs-lookup"><span data-stu-id="ede41-324">Example 5: Vendor credit note with primary payment</span></span>
<span data-ttu-id="ede41-325">Fabrikam 为供应商 3004 (Fourth Coffee) 生成 75.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-325">Fabrikam generates a payment of 75.00 for vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="ede41-326">该付款用针对 Fabrikam West 供应商 3004 的未结发票和针对 Fabrikam East 供应商 100 的未结贷方通知单结算。</span><span class="sxs-lookup"><span data-stu-id="ede41-326">The payment is settled with an open invoice for Fabrikam West vendor 3004 and an open credit note for Fabrikam East vendor 100.</span></span> <span data-ttu-id="ede41-327">该付款在**未结交易记录编辑**页中选择为主付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-327">The payment is selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a><span data-ttu-id="ede41-328">发票为供应商 3004 过帐到 Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="ede41-328">Invoice is posted to Fabrikam West for vendor 3004</span></span>

| <span data-ttu-id="ede41-329">帐户</span><span class="sxs-lookup"><span data-stu-id="ede41-329">Account</span></span>                          | <span data-ttu-id="ede41-330">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-330">Debit amount</span></span> | <span data-ttu-id="ede41-331">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-331">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-332">支出 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="ede41-332">Expense (Fabrikam West)</span></span>          | <span data-ttu-id="ede41-333">100.00</span><span class="sxs-lookup"><span data-stu-id="ede41-333">100.00</span></span>       |               |
| <span data-ttu-id="ede41-334">应付帐款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="ede41-334">Accounts payable (Fabrikam West)</span></span> |              | <span data-ttu-id="ede41-335">100.00</span><span class="sxs-lookup"><span data-stu-id="ede41-335">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a><span data-ttu-id="ede41-336">贷方通知单为供应商 100 过帐到 Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="ede41-336">Credit note is posted to Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="ede41-337">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-337">Account</span></span>                          | <span data-ttu-id="ede41-338">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-338">Debit amount</span></span> | <span data-ttu-id="ede41-339">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-339">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-340">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-340">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="ede41-341">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-341">25.00</span></span>        |               |
| <span data-ttu-id="ede41-342">采购退货 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-342">Purchase returns (Fabrikam East)</span></span> |              | <span data-ttu-id="ede41-343">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-343">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a><span data-ttu-id="ede41-344">付款为供应商 3004 过帐到 Fabrikam</span><span class="sxs-lookup"><span data-stu-id="ede41-344">Payment is posted to Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="ede41-345">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-345">Account</span></span>                     | <span data-ttu-id="ede41-346">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-346">Debit amount</span></span> | <span data-ttu-id="ede41-347">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-347">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="ede41-348">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-348">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="ede41-349">75.00</span><span class="sxs-lookup"><span data-stu-id="ede41-349">75.00</span></span>        |               |
| <span data-ttu-id="ede41-350">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-350">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="ede41-351">75.00</span><span class="sxs-lookup"><span data-stu-id="ede41-351">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="ede41-352">Fabrikam 付款用 Fabrikam West 发票和 Fabrikam East 贷方通知单结算</span><span class="sxs-lookup"><span data-stu-id="ede41-352">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="ede41-353">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-353">**Fabrikam posting**</span></span>

| <span data-ttu-id="ede41-354">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-354">Account</span></span>                           | <span data-ttu-id="ede41-355">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-355">Debit amount</span></span> | <span data-ttu-id="ede41-356">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-356">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-357">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-357">Accounts payable (Fabrikam)</span></span>       | <span data-ttu-id="ede41-358">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-358">25.00</span></span>        |               |
| <span data-ttu-id="ede41-359">向 Fabrikam East (Fabrikam) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="ede41-359">Due to Fabrikam East (Fabrikam)</span></span>   |              | <span data-ttu-id="ede41-360">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-360">25.00</span></span>         |
| <span data-ttu-id="ede41-361">从 Fabrikam West (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="ede41-361">Due from Fabrikam West (Fabrikam)</span></span> | <span data-ttu-id="ede41-362">100.00</span><span class="sxs-lookup"><span data-stu-id="ede41-362">100.00</span></span>       |               |
| <span data-ttu-id="ede41-363">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-363">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="ede41-364">100.00</span><span class="sxs-lookup"><span data-stu-id="ede41-364">100.00</span></span>        |

<span data-ttu-id="ede41-365">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-365">**Fabrikam East posting**</span></span>

| <span data-ttu-id="ede41-366">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-366">Account</span></span>                           | <span data-ttu-id="ede41-367">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-367">Debit amount</span></span> | <span data-ttu-id="ede41-368">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-368">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-369">从 Fabrikam (Fabrikam East) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="ede41-369">Due from Fabrikam (Fabrikam East)</span></span> | <span data-ttu-id="ede41-370">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-370">25.00</span></span>        |               |
| <span data-ttu-id="ede41-371">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-371">Accounts payable (Fabrikam East)</span></span>  |              | <span data-ttu-id="ede41-372">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-372">25.00</span></span>         |

<span data-ttu-id="ede41-373">**Fabrikam West 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-373">**Fabrikam West posting**</span></span>

| <span data-ttu-id="ede41-374">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-374">Account</span></span>                          | <span data-ttu-id="ede41-375">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-375">Debit amount</span></span> | <span data-ttu-id="ede41-376">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-376">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-377">应付帐款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="ede41-377">Accounts payable (Fabrikam West)</span></span> | <span data-ttu-id="ede41-378">100.00</span><span class="sxs-lookup"><span data-stu-id="ede41-378">100.00</span></span>       |               |
| <span data-ttu-id="ede41-379">向 Fabrikam (Fabrikam West) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="ede41-379">Due to Fabrikam (Fabrikam West)</span></span>  |              | <span data-ttu-id="ede41-380">100.00</span><span class="sxs-lookup"><span data-stu-id="ede41-380">100.00</span></span>        |

## <a name="example-6-vendor-credit-note-without-primary-payment"></a><span data-ttu-id="ede41-381">示例 6：不具有主付款的供应商贷方通知单</span><span class="sxs-lookup"><span data-stu-id="ede41-381">Example 6: Vendor credit note without primary payment</span></span>
<span data-ttu-id="ede41-382">Fabrikam 为供应商 3004 (Fourth Coffee) 生成 75.00 的付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-382">Fabrikam generates a payment of 75.00 for vendor 3004, Fourth Coffee.</span></span> <span data-ttu-id="ede41-383">该付款用针对 Fabrikam West 供应商 3004 的未结发票和针对 Fabrikam East 供应商 100 的未结贷方通知单结算。</span><span class="sxs-lookup"><span data-stu-id="ede41-383">The payment is settled with an open invoice for Fabrikam West vendor 3004 and an open credit note for Fabrikam East vendor 100.</span></span> <span data-ttu-id="ede41-384">该付款未在**未结交易记录编辑**页中选择为主付款。</span><span class="sxs-lookup"><span data-stu-id="ede41-384">The payment isn't selected as the primary payment on the **Settle transactions** page.</span></span>

### <a name="invoice-is-posted-to-fabrikam-west-for-vendor-3004"></a><span data-ttu-id="ede41-385">发票为供应商 3004 过帐到 Fabrikam West</span><span class="sxs-lookup"><span data-stu-id="ede41-385">Invoice is posted to Fabrikam West for vendor 3004</span></span>

| <span data-ttu-id="ede41-386">帐户</span><span class="sxs-lookup"><span data-stu-id="ede41-386">Account</span></span>                          | <span data-ttu-id="ede41-387">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-387">Debit amount</span></span> | <span data-ttu-id="ede41-388">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-388">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-389">支出 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="ede41-389">Expense (Fabrikam West)</span></span>          | <span data-ttu-id="ede41-390">100.00</span><span class="sxs-lookup"><span data-stu-id="ede41-390">100.00</span></span>       |               |
| <span data-ttu-id="ede41-391">应付帐款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="ede41-391">Accounts payable (Fabrikam West)</span></span> |              | <span data-ttu-id="ede41-392">100.00</span><span class="sxs-lookup"><span data-stu-id="ede41-392">100.00</span></span>        |

### <a name="credit-note-is-posted-to-fabrikam-east-for-vendor-100"></a><span data-ttu-id="ede41-393">贷方通知单为供应商 100 过帐到 Fabrikam East</span><span class="sxs-lookup"><span data-stu-id="ede41-393">Credit note is posted to Fabrikam East for vendor 100</span></span>

| <span data-ttu-id="ede41-394">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-394">Account</span></span>                          | <span data-ttu-id="ede41-395">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-395">Debit amount</span></span> | <span data-ttu-id="ede41-396">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-396">Credit amount</span></span> |
|----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-397">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-397">Accounts payable (Fabrikam East)</span></span> | <span data-ttu-id="ede41-398">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-398">25.00</span></span>        |               |
| <span data-ttu-id="ede41-399">采购退货 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-399">Purchase returns (Fabrikam East)</span></span> |              | <span data-ttu-id="ede41-400">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-400">25.00</span></span>         |

### <a name="payment-is-posted-to-fabrikam-for-vendor-3004"></a><span data-ttu-id="ede41-401">付款为供应商 3004 过帐到 Fabrikam</span><span class="sxs-lookup"><span data-stu-id="ede41-401">Payment is posted to Fabrikam for vendor 3004</span></span>

| <span data-ttu-id="ede41-402">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-402">Account</span></span>                     | <span data-ttu-id="ede41-403">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-403">Debit amount</span></span> | <span data-ttu-id="ede41-404">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-404">Credit amount</span></span> |
|-----------------------------|--------------|---------------|
| <span data-ttu-id="ede41-405">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-405">Accounts payable (Fabrikam)</span></span> | <span data-ttu-id="ede41-406">75.00</span><span class="sxs-lookup"><span data-stu-id="ede41-406">75.00</span></span>        |               |
| <span data-ttu-id="ede41-407">现金 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-407">Cash (Fabrikam)</span></span>             |              | <span data-ttu-id="ede41-408">75.00</span><span class="sxs-lookup"><span data-stu-id="ede41-408">75.00</span></span>         |

### <a name="fabrikam-payment-is-settled-with-fabrikam-west-invoice-and-fabrikam-east-credit-note"></a><span data-ttu-id="ede41-409">Fabrikam 付款用 Fabrikam West 发票和 Fabrikam East 贷方通知单结算</span><span class="sxs-lookup"><span data-stu-id="ede41-409">Fabrikam payment is settled with Fabrikam West invoice and Fabrikam East credit note</span></span>

<span data-ttu-id="ede41-410">**Fabrikam 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-410">**Fabrikam posting**</span></span>

| <span data-ttu-id="ede41-411">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-411">Account</span></span>                           | <span data-ttu-id="ede41-412">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-412">Debit amount</span></span> | <span data-ttu-id="ede41-413">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-413">Credit amount</span></span> |
|-----------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-414">从 Fabrikam West (Fabrikam) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="ede41-414">Due from Fabrikam West (Fabrikam)</span></span> | <span data-ttu-id="ede41-415">75.00</span><span class="sxs-lookup"><span data-stu-id="ede41-415">75.00</span></span>        |               |
| <span data-ttu-id="ede41-416">应付帐款 (Fabrikam)</span><span class="sxs-lookup"><span data-stu-id="ede41-416">Accounts payable (Fabrikam)</span></span>       |              | <span data-ttu-id="ede41-417">75.00</span><span class="sxs-lookup"><span data-stu-id="ede41-417">75.00</span></span>         |

<span data-ttu-id="ede41-418">**Fabrikam East 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-418">**Fabrikam East posting**</span></span>

| <span data-ttu-id="ede41-419">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-419">Account</span></span>                                | <span data-ttu-id="ede41-420">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-420">Debit amount</span></span> | <span data-ttu-id="ede41-421">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-421">Credit amount</span></span> |
|----------------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-422">从 Fabrikam West (Fabrikam East) 的应收金额</span><span class="sxs-lookup"><span data-stu-id="ede41-422">Due from Fabrikam West (Fabrikam East)</span></span> | <span data-ttu-id="ede41-423">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-423">25.00</span></span>        |               |
| <span data-ttu-id="ede41-424">应付帐款 (Fabrikam East)</span><span class="sxs-lookup"><span data-stu-id="ede41-424">Accounts payable (Fabrikam East)</span></span>       |              | <span data-ttu-id="ede41-425">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-425">25.00</span></span>         |

<span data-ttu-id="ede41-426">**Fabrikam West 过帐**</span><span class="sxs-lookup"><span data-stu-id="ede41-426">**Fabrikam West posting**</span></span>

| <span data-ttu-id="ede41-427">科目</span><span class="sxs-lookup"><span data-stu-id="ede41-427">Account</span></span>                              | <span data-ttu-id="ede41-428">借方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-428">Debit amount</span></span> | <span data-ttu-id="ede41-429">贷方金额</span><span class="sxs-lookup"><span data-stu-id="ede41-429">Credit amount</span></span> |
|--------------------------------------|--------------|---------------|
| <span data-ttu-id="ede41-430">应付帐款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="ede41-430">Accounts payable (Fabrikam West)</span></span>     | <span data-ttu-id="ede41-431">75.00</span><span class="sxs-lookup"><span data-stu-id="ede41-431">75.00</span></span>        |               |
| <span data-ttu-id="ede41-432">向 Fabrikam (Fabrikam West) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="ede41-432">Due to Fabrikam (Fabrikam West)</span></span>      |              | <span data-ttu-id="ede41-433">75.00</span><span class="sxs-lookup"><span data-stu-id="ede41-433">75.00</span></span>         |
| <span data-ttu-id="ede41-434">应付帐款 (Fabrikam West)</span><span class="sxs-lookup"><span data-stu-id="ede41-434">Accounts payable (Fabrikam West)</span></span>     | <span data-ttu-id="ede41-435">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-435">25.00</span></span>        |               |
| <span data-ttu-id="ede41-436">向 Fabrikam East (Fabrikam West) 的应付金额</span><span class="sxs-lookup"><span data-stu-id="ede41-436">Due to Fabrikam East (Fabrikam West)</span></span> |              | <span data-ttu-id="ede41-437">25.00</span><span class="sxs-lookup"><span data-stu-id="ede41-437">25.00</span></span>         |






