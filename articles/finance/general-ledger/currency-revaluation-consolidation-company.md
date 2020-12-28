---
title: 合并公司中的币种重估
description: 此主题描述如何重估合并公司中的币种。
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33db12388c969b8dadb38bfacf4d9df333b78bd4
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/16/2020
ms.locfileid: "4440922"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="2d1fa-103">合并公司中的币种重估</span><span class="sxs-lookup"><span data-stu-id="2d1fa-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d1fa-104">将一个记帐币种的数据与另一个记帐币种的数据合并时，如果汇率发生更改，则仍必须运行币种重估，以便准确重估帐户余额。</span><span class="sxs-lookup"><span data-stu-id="2d1fa-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="2d1fa-105">在最初合并数据时，使用 **币种折算** 选项卡可选择合并过程中用于折算的初始汇率。</span><span class="sxs-lookup"><span data-stu-id="2d1fa-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="2d1fa-106">在输入新的汇率后（例如，在下一个月），您必须重估帐户余额。</span><span class="sxs-lookup"><span data-stu-id="2d1fa-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="2d1fa-107">随后，将根据新的汇率和日期更新或有利润或损失。</span><span class="sxs-lookup"><span data-stu-id="2d1fa-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="2d1fa-108">以下示例说明了该过程中创建的会计条目。</span><span class="sxs-lookup"><span data-stu-id="2d1fa-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="2d1fa-109">公司设置</span><span class="sxs-lookup"><span data-stu-id="2d1fa-109">Company setup</span></span>
-   <span data-ttu-id="2d1fa-110">**源/运营公司 (USMF)** – 美元 (USD) 用作会计和申报币种。</span><span class="sxs-lookup"><span data-stu-id="2d1fa-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="2d1fa-111">**合并的公司 (CON)** – 欧元 (EUR) 用作会计和申报币种。</span><span class="sxs-lookup"><span data-stu-id="2d1fa-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="2d1fa-112">**已实现利润** – 会计科目 801500</span><span class="sxs-lookup"><span data-stu-id="2d1fa-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="2d1fa-113">**已有损失** – 会计科目 801600</span><span class="sxs-lookup"><span data-stu-id="2d1fa-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="2d1fa-114">**或有利润** – 会计科目 801600</span><span class="sxs-lookup"><span data-stu-id="2d1fa-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="2d1fa-115">**或有损失** – 会计科目 801400</span><span class="sxs-lookup"><span data-stu-id="2d1fa-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="2d1fa-116">原始交易记录</span><span class="sxs-lookup"><span data-stu-id="2d1fa-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="2d1fa-117">USMF 中的现金收据交易记录</span><span class="sxs-lookup"><span data-stu-id="2d1fa-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="2d1fa-118">日期</span><span class="sxs-lookup"><span data-stu-id="2d1fa-118">Date</span></span>       | <span data-ttu-id="2d1fa-119">会计科目</span><span class="sxs-lookup"><span data-stu-id="2d1fa-119">Ledger account</span></span>               | <span data-ttu-id="2d1fa-120">货币</span><span class="sxs-lookup"><span data-stu-id="2d1fa-120">Currency</span></span> | <span data-ttu-id="2d1fa-121">金额</span><span class="sxs-lookup"><span data-stu-id="2d1fa-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="2d1fa-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="2d1fa-122">10/11/2015</span></span> | <span data-ttu-id="2d1fa-123">110110 – 现金</span><span class="sxs-lookup"><span data-stu-id="2d1fa-123">110110 – Cash</span></span>                | <span data-ttu-id="2d1fa-124">美元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-124">USD</span></span>      | <span data-ttu-id="2d1fa-125">500</span><span class="sxs-lookup"><span data-stu-id="2d1fa-125">500</span></span>    |
| <span data-ttu-id="2d1fa-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="2d1fa-126">10/11/2015</span></span> | <span data-ttu-id="2d1fa-127">130100 – 应收帐款</span><span class="sxs-lookup"><span data-stu-id="2d1fa-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="2d1fa-128">美元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-128">USD</span></span>      | <span data-ttu-id="2d1fa-129">-500</span><span class="sxs-lookup"><span data-stu-id="2d1fa-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="2d1fa-130">汇率</span><span class="sxs-lookup"><span data-stu-id="2d1fa-130">Exchange rates</span></span>

| <span data-ttu-id="2d1fa-131">原始币种</span><span class="sxs-lookup"><span data-stu-id="2d1fa-131">From currency</span></span> | <span data-ttu-id="2d1fa-132">目标币种</span><span class="sxs-lookup"><span data-stu-id="2d1fa-132">To currency</span></span> | <span data-ttu-id="2d1fa-133">开始日期</span><span class="sxs-lookup"><span data-stu-id="2d1fa-133">Start date</span></span> | <span data-ttu-id="2d1fa-134">汇率</span><span class="sxs-lookup"><span data-stu-id="2d1fa-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="2d1fa-135">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-135">EUR</span></span>           | <span data-ttu-id="2d1fa-136">美元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-136">USD</span></span>         | <span data-ttu-id="2d1fa-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="2d1fa-137">10/1/2015</span></span>  | <span data-ttu-id="2d1fa-138">200</span><span class="sxs-lookup"><span data-stu-id="2d1fa-138">200</span></span>           |
| <span data-ttu-id="2d1fa-139">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-139">EUR</span></span>           | <span data-ttu-id="2d1fa-140">美元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-140">USD</span></span>         | <span data-ttu-id="2d1fa-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="2d1fa-141">11/1/2015</span></span>  | <span data-ttu-id="2d1fa-142">150</span><span class="sxs-lookup"><span data-stu-id="2d1fa-142">150</span></span>           |
| <span data-ttu-id="2d1fa-143">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-143">EUR</span></span>           | <span data-ttu-id="2d1fa-144">美元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-144">USD</span></span>         | <span data-ttu-id="2d1fa-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="2d1fa-145">12/1/2012</span></span>  | <span data-ttu-id="2d1fa-146">100</span><span class="sxs-lookup"><span data-stu-id="2d1fa-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="2d1fa-147">执行合并（2015 年 10 月）</span><span class="sxs-lookup"><span data-stu-id="2d1fa-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2d1fa-148">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="2d1fa-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="2d1fa-149">会计科目</span><span class="sxs-lookup"><span data-stu-id="2d1fa-149">Ledger account</span></span> | <span data-ttu-id="2d1fa-150">货币</span><span class="sxs-lookup"><span data-stu-id="2d1fa-150">Currency</span></span> | <span data-ttu-id="2d1fa-151">金额</span><span class="sxs-lookup"><span data-stu-id="2d1fa-151">Amount</span></span> | <span data-ttu-id="2d1fa-152">计算</span><span class="sxs-lookup"><span data-stu-id="2d1fa-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="2d1fa-153">110110</span><span class="sxs-lookup"><span data-stu-id="2d1fa-153">110110</span></span>         | <span data-ttu-id="2d1fa-154">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-154">EUR</span></span>      | <span data-ttu-id="2d1fa-155">250</span><span class="sxs-lookup"><span data-stu-id="2d1fa-155">250</span></span>    | <span data-ttu-id="2d1fa-156">500 美元 × 50%</span><span class="sxs-lookup"><span data-stu-id="2d1fa-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="2d1fa-157">130100</span><span class="sxs-lookup"><span data-stu-id="2d1fa-157">130100</span></span>         | <span data-ttu-id="2d1fa-158">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-158">EUR</span></span>      | <span data-ttu-id="2d1fa-159">-250</span><span class="sxs-lookup"><span data-stu-id="2d1fa-159">-250</span></span>   | <span data-ttu-id="2d1fa-160">-500 美元 × 50%</span><span class="sxs-lookup"><span data-stu-id="2d1fa-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="2d1fa-161">执行科目的币种重估（2015 年 10 月 1 日 - 2015 年 11 月 30 日）</span><span class="sxs-lookup"><span data-stu-id="2d1fa-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2d1fa-162">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="2d1fa-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="2d1fa-163">会计科目</span><span class="sxs-lookup"><span data-stu-id="2d1fa-163">Ledger account</span></span> | <span data-ttu-id="2d1fa-164">货币</span><span class="sxs-lookup"><span data-stu-id="2d1fa-164">Currency</span></span> | <span data-ttu-id="2d1fa-165">金额</span><span class="sxs-lookup"><span data-stu-id="2d1fa-165">Amount</span></span>  | <span data-ttu-id="2d1fa-166">计算</span><span class="sxs-lookup"><span data-stu-id="2d1fa-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="2d1fa-167">110110</span><span class="sxs-lookup"><span data-stu-id="2d1fa-167">110110</span></span>         | <span data-ttu-id="2d1fa-168">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-168">EUR</span></span>      | <span data-ttu-id="2d1fa-169">333.33</span><span class="sxs-lookup"><span data-stu-id="2d1fa-169">333.33</span></span>  | <span data-ttu-id="2d1fa-170">原金额为 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="2d1fa-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="2d1fa-171">130100</span><span class="sxs-lookup"><span data-stu-id="2d1fa-171">130100</span></span>         | <span data-ttu-id="2d1fa-172">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-172">EUR</span></span>      | <span data-ttu-id="2d1fa-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="2d1fa-173">-333.33</span></span> | <span data-ttu-id="2d1fa-174">原金额为 -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="2d1fa-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="2d1fa-175">801400</span><span class="sxs-lookup"><span data-stu-id="2d1fa-175">801400</span></span>         | <span data-ttu-id="2d1fa-176">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-176">EUR</span></span>      | <span data-ttu-id="2d1fa-177">83.33</span><span class="sxs-lookup"><span data-stu-id="2d1fa-177">83.33</span></span>   | <span data-ttu-id="2d1fa-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="2d1fa-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="2d1fa-179">801600</span><span class="sxs-lookup"><span data-stu-id="2d1fa-179">801600</span></span>         | <span data-ttu-id="2d1fa-180">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-180">EUR</span></span>      | <span data-ttu-id="2d1fa-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="2d1fa-181">-83.33</span></span>  | <span data-ttu-id="2d1fa-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="2d1fa-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="2d1fa-183">您将看到申报币种金额的其他交易记录。</span><span class="sxs-lookup"><span data-stu-id="2d1fa-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="2d1fa-184">执行科目的币种重估（2015 年 10 月 1 日 - 2015 年 12 月 31 日）</span><span class="sxs-lookup"><span data-stu-id="2d1fa-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2d1fa-185">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="2d1fa-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="2d1fa-186">会计科目</span><span class="sxs-lookup"><span data-stu-id="2d1fa-186">Ledger account</span></span> | <span data-ttu-id="2d1fa-187">货币</span><span class="sxs-lookup"><span data-stu-id="2d1fa-187">Currency</span></span> | <span data-ttu-id="2d1fa-188">金额</span><span class="sxs-lookup"><span data-stu-id="2d1fa-188">Amount</span></span>  | <span data-ttu-id="2d1fa-189">计算</span><span class="sxs-lookup"><span data-stu-id="2d1fa-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="2d1fa-190">110110</span><span class="sxs-lookup"><span data-stu-id="2d1fa-190">110110</span></span>         | <span data-ttu-id="2d1fa-191">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-191">EUR</span></span>      | <span data-ttu-id="2d1fa-192">500.00</span><span class="sxs-lookup"><span data-stu-id="2d1fa-192">500.00</span></span>  | <span data-ttu-id="2d1fa-193">原金额为 500 × 1</span><span class="sxs-lookup"><span data-stu-id="2d1fa-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="2d1fa-194">130100</span><span class="sxs-lookup"><span data-stu-id="2d1fa-194">130100</span></span>         | <span data-ttu-id="2d1fa-195">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-195">EUR</span></span>      | <span data-ttu-id="2d1fa-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="2d1fa-196">-500.00</span></span> | <span data-ttu-id="2d1fa-197">原金额为 -500 × 1</span><span class="sxs-lookup"><span data-stu-id="2d1fa-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="2d1fa-198">801400</span><span class="sxs-lookup"><span data-stu-id="2d1fa-198">801400</span></span>         | <span data-ttu-id="2d1fa-199">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-199">EUR</span></span>      | <span data-ttu-id="2d1fa-200">250</span><span class="sxs-lookup"><span data-stu-id="2d1fa-200">250</span></span>     | <span data-ttu-id="2d1fa-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="2d1fa-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="2d1fa-202">801600</span><span class="sxs-lookup"><span data-stu-id="2d1fa-202">801600</span></span>         | <span data-ttu-id="2d1fa-203">欧元</span><span class="sxs-lookup"><span data-stu-id="2d1fa-203">EUR</span></span>      | <span data-ttu-id="2d1fa-204">-250</span><span class="sxs-lookup"><span data-stu-id="2d1fa-204">-250</span></span>    | <span data-ttu-id="2d1fa-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="2d1fa-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





