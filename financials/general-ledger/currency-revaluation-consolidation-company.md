---
title: "合并公司中的币种重估"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: zh-cn
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="19a3c-102">合并公司中的币种重估</span><span class="sxs-lookup"><span data-stu-id="19a3c-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="19a3c-103">将一个记帐币种的数据与另一个记帐币种的数据合并时，如果汇率发生更改，则仍必须运行币种重估，以便准确重估帐户余额。</span><span class="sxs-lookup"><span data-stu-id="19a3c-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="19a3c-104">在最初合并数据时，使用**“币种折算”**选项卡可选择合并过程中用于折算的初始汇率。</span><span class="sxs-lookup"><span data-stu-id="19a3c-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="19a3c-105">在输入新的汇率后（例如，在下一个月），您必须重估帐户余额。</span><span class="sxs-lookup"><span data-stu-id="19a3c-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="19a3c-106">随后，将根据新的汇率和日期更新或有利润或损失。</span><span class="sxs-lookup"><span data-stu-id="19a3c-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="19a3c-107">以下示例说明了该过程中创建的会计条目。</span><span class="sxs-lookup"><span data-stu-id="19a3c-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="19a3c-108">公司设置</span><span class="sxs-lookup"><span data-stu-id="19a3c-108">Company setup</span></span>
-   <span data-ttu-id="19a3c-109">**源/运营公司 (USMF)** – 美元 (USD) 用作会计和申报币种。</span><span class="sxs-lookup"><span data-stu-id="19a3c-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="19a3c-110">**合并的公司 (CON)** – 欧元 (EUR) 用作会计和申报币种。</span><span class="sxs-lookup"><span data-stu-id="19a3c-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="19a3c-111">**已实现利润** – 会计科目 801500</span><span class="sxs-lookup"><span data-stu-id="19a3c-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="19a3c-112">**已有损失** – 会计科目 801600</span><span class="sxs-lookup"><span data-stu-id="19a3c-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="19a3c-113">**或有利润** – 会计科目 801600</span><span class="sxs-lookup"><span data-stu-id="19a3c-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="19a3c-114">**或有损失** – 会计科目 801400</span><span class="sxs-lookup"><span data-stu-id="19a3c-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="19a3c-115">原始交易记录</span><span class="sxs-lookup"><span data-stu-id="19a3c-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="19a3c-116">USMF 中的现金收据交易记录</span><span class="sxs-lookup"><span data-stu-id="19a3c-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="19a3c-117">日期</span><span class="sxs-lookup"><span data-stu-id="19a3c-117">Date</span></span>       | <span data-ttu-id="19a3c-118">会计科目</span><span class="sxs-lookup"><span data-stu-id="19a3c-118">Ledger account</span></span>               | <span data-ttu-id="19a3c-119">货币</span><span class="sxs-lookup"><span data-stu-id="19a3c-119">Currency</span></span> | <span data-ttu-id="19a3c-120">金额</span><span class="sxs-lookup"><span data-stu-id="19a3c-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="19a3c-121">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="19a3c-121">10/11/2015</span></span> | <span data-ttu-id="19a3c-122">110110 – 现金</span><span class="sxs-lookup"><span data-stu-id="19a3c-122">110110 – Cash</span></span>                | <span data-ttu-id="19a3c-123">美元</span><span class="sxs-lookup"><span data-stu-id="19a3c-123">USD</span></span>      | <span data-ttu-id="19a3c-124">500</span><span class="sxs-lookup"><span data-stu-id="19a3c-124">500</span></span>    |
| <span data-ttu-id="19a3c-125">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="19a3c-125">10/11/2015</span></span> | <span data-ttu-id="19a3c-126">130100 – 应收帐款</span><span class="sxs-lookup"><span data-stu-id="19a3c-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="19a3c-127">美元</span><span class="sxs-lookup"><span data-stu-id="19a3c-127">USD</span></span>      | <span data-ttu-id="19a3c-128">-500</span><span class="sxs-lookup"><span data-stu-id="19a3c-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="19a3c-129">汇率</span><span class="sxs-lookup"><span data-stu-id="19a3c-129">Exchange rates</span></span>
| <span data-ttu-id="19a3c-130">原始币种</span><span class="sxs-lookup"><span data-stu-id="19a3c-130">From currency</span></span> | <span data-ttu-id="19a3c-131">目标币种</span><span class="sxs-lookup"><span data-stu-id="19a3c-131">To currency</span></span> | <span data-ttu-id="19a3c-132">开始日期</span><span class="sxs-lookup"><span data-stu-id="19a3c-132">Start date</span></span> | <span data-ttu-id="19a3c-133">汇率</span><span class="sxs-lookup"><span data-stu-id="19a3c-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="19a3c-134">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-134">EUR</span></span>           | <span data-ttu-id="19a3c-135">美元</span><span class="sxs-lookup"><span data-stu-id="19a3c-135">USD</span></span>         | <span data-ttu-id="19a3c-136">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="19a3c-136">10/1/2015</span></span>  | <span data-ttu-id="19a3c-137">200</span><span class="sxs-lookup"><span data-stu-id="19a3c-137">200</span></span>           |
| <span data-ttu-id="19a3c-138">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-138">EUR</span></span>           | <span data-ttu-id="19a3c-139">美元</span><span class="sxs-lookup"><span data-stu-id="19a3c-139">USD</span></span>         | <span data-ttu-id="19a3c-140">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="19a3c-140">11/1/2015</span></span>  | <span data-ttu-id="19a3c-141">150</span><span class="sxs-lookup"><span data-stu-id="19a3c-141">150</span></span>           |
| <span data-ttu-id="19a3c-142">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-142">EUR</span></span>           | <span data-ttu-id="19a3c-143">美元</span><span class="sxs-lookup"><span data-stu-id="19a3c-143">USD</span></span>         | <span data-ttu-id="19a3c-144">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="19a3c-144">12/1/2012</span></span>  | <span data-ttu-id="19a3c-145">100</span><span class="sxs-lookup"><span data-stu-id="19a3c-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="19a3c-146">执行合并（2015 年 10 月）</span><span class="sxs-lookup"><span data-stu-id="19a3c-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="19a3c-147">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="19a3c-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="19a3c-148">会计科目</span><span class="sxs-lookup"><span data-stu-id="19a3c-148">Ledger account</span></span> | <span data-ttu-id="19a3c-149">货币</span><span class="sxs-lookup"><span data-stu-id="19a3c-149">Currency</span></span> | <span data-ttu-id="19a3c-150">金额</span><span class="sxs-lookup"><span data-stu-id="19a3c-150">Amount</span></span> | <span data-ttu-id="19a3c-151">计算</span><span class="sxs-lookup"><span data-stu-id="19a3c-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="19a3c-152">110110</span><span class="sxs-lookup"><span data-stu-id="19a3c-152">110110</span></span>         | <span data-ttu-id="19a3c-153">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-153">EUR</span></span>      | <span data-ttu-id="19a3c-154">250</span><span class="sxs-lookup"><span data-stu-id="19a3c-154">250</span></span>    | <span data-ttu-id="19a3c-155">500 美元 × 50%</span><span class="sxs-lookup"><span data-stu-id="19a3c-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="19a3c-156">130100</span><span class="sxs-lookup"><span data-stu-id="19a3c-156">130100</span></span>         | <span data-ttu-id="19a3c-157">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-157">EUR</span></span>      | <span data-ttu-id="19a3c-158">-250</span><span class="sxs-lookup"><span data-stu-id="19a3c-158">-250</span></span>   | <span data-ttu-id="19a3c-159">-500 美元 × 50%</span><span class="sxs-lookup"><span data-stu-id="19a3c-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="19a3c-160">执行科目的币种重估（2015 年 10 月 1 日 - 2015 年 11 月 30 日）</span><span class="sxs-lookup"><span data-stu-id="19a3c-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="19a3c-161">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="19a3c-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="19a3c-162">会计科目</span><span class="sxs-lookup"><span data-stu-id="19a3c-162">Ledger account</span></span> | <span data-ttu-id="19a3c-163">货币</span><span class="sxs-lookup"><span data-stu-id="19a3c-163">Currency</span></span> | <span data-ttu-id="19a3c-164">金额</span><span class="sxs-lookup"><span data-stu-id="19a3c-164">Amount</span></span>  | <span data-ttu-id="19a3c-165">计算</span><span class="sxs-lookup"><span data-stu-id="19a3c-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="19a3c-166">110110</span><span class="sxs-lookup"><span data-stu-id="19a3c-166">110110</span></span>         | <span data-ttu-id="19a3c-167">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-167">EUR</span></span>      | <span data-ttu-id="19a3c-168">333.33</span><span class="sxs-lookup"><span data-stu-id="19a3c-168">333.33</span></span>  | <span data-ttu-id="19a3c-169">原金额为 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="19a3c-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="19a3c-170">130100</span><span class="sxs-lookup"><span data-stu-id="19a3c-170">130100</span></span>         | <span data-ttu-id="19a3c-171">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-171">EUR</span></span>      | <span data-ttu-id="19a3c-172">-333.33</span><span class="sxs-lookup"><span data-stu-id="19a3c-172">-333.33</span></span> | <span data-ttu-id="19a3c-173">原金额为 -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="19a3c-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="19a3c-174">801400</span><span class="sxs-lookup"><span data-stu-id="19a3c-174">801400</span></span>         | <span data-ttu-id="19a3c-175">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-175">EUR</span></span>      | <span data-ttu-id="19a3c-176">83.33</span><span class="sxs-lookup"><span data-stu-id="19a3c-176">83.33</span></span>   | <span data-ttu-id="19a3c-177">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="19a3c-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="19a3c-178">801600</span><span class="sxs-lookup"><span data-stu-id="19a3c-178">801600</span></span>         | <span data-ttu-id="19a3c-179">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-179">EUR</span></span>      | <span data-ttu-id="19a3c-180">-83.33</span><span class="sxs-lookup"><span data-stu-id="19a3c-180">-83.33</span></span>  | <span data-ttu-id="19a3c-181">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="19a3c-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="19a3c-182">您将看到申报币种金额的其他交易记录。</span><span class="sxs-lookup"><span data-stu-id="19a3c-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="19a3c-183">执行科目的币种重估（2015 年 10 月 1 日 - 2015 年 12 月 31 日）</span><span class="sxs-lookup"><span data-stu-id="19a3c-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="19a3c-184">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="19a3c-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="19a3c-185">会计科目</span><span class="sxs-lookup"><span data-stu-id="19a3c-185">Ledger account</span></span> | <span data-ttu-id="19a3c-186">货币</span><span class="sxs-lookup"><span data-stu-id="19a3c-186">Currency</span></span> | <span data-ttu-id="19a3c-187">金额</span><span class="sxs-lookup"><span data-stu-id="19a3c-187">Amount</span></span>  | <span data-ttu-id="19a3c-188">计算</span><span class="sxs-lookup"><span data-stu-id="19a3c-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="19a3c-189">110110</span><span class="sxs-lookup"><span data-stu-id="19a3c-189">110110</span></span>         | <span data-ttu-id="19a3c-190">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-190">EUR</span></span>      | <span data-ttu-id="19a3c-191">500.00</span><span class="sxs-lookup"><span data-stu-id="19a3c-191">500.00</span></span>  | <span data-ttu-id="19a3c-192">原金额为 500 × 1</span><span class="sxs-lookup"><span data-stu-id="19a3c-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="19a3c-193">130100</span><span class="sxs-lookup"><span data-stu-id="19a3c-193">130100</span></span>         | <span data-ttu-id="19a3c-194">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-194">EUR</span></span>      | <span data-ttu-id="19a3c-195">-500.00</span><span class="sxs-lookup"><span data-stu-id="19a3c-195">-500.00</span></span> | <span data-ttu-id="19a3c-196">原金额为 -500 × 1</span><span class="sxs-lookup"><span data-stu-id="19a3c-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="19a3c-197">801400</span><span class="sxs-lookup"><span data-stu-id="19a3c-197">801400</span></span>         | <span data-ttu-id="19a3c-198">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-198">EUR</span></span>      | <span data-ttu-id="19a3c-199">250</span><span class="sxs-lookup"><span data-stu-id="19a3c-199">250</span></span>     | <span data-ttu-id="19a3c-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="19a3c-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="19a3c-201">801600</span><span class="sxs-lookup"><span data-stu-id="19a3c-201">801600</span></span>         | <span data-ttu-id="19a3c-202">欧元</span><span class="sxs-lookup"><span data-stu-id="19a3c-202">EUR</span></span>      | <span data-ttu-id="19a3c-203">-250</span><span class="sxs-lookup"><span data-stu-id="19a3c-203">-250</span></span>    | <span data-ttu-id="19a3c-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="19a3c-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






