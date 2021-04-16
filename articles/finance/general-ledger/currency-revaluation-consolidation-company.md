---
title: 合并公司中的币种重估
description: 此主题描述如何重估合并公司中的币种。
author: roschlom
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c901d5ccd8c8b2146daa49752b7d8b70bbfca722
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818408"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="17785-103">合并公司中的币种重估</span><span class="sxs-lookup"><span data-stu-id="17785-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17785-104">将一个记帐币种的数据与另一个记帐币种的数据合并时，如果汇率发生更改，则仍必须运行币种重估，以便准确重估帐户余额。</span><span class="sxs-lookup"><span data-stu-id="17785-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="17785-105">在最初合并数据时，使用 **币种折算** 选项卡可选择合并过程中用于折算的初始汇率。</span><span class="sxs-lookup"><span data-stu-id="17785-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="17785-106">在输入新的汇率后（例如，在下一个月），您必须重估帐户余额。</span><span class="sxs-lookup"><span data-stu-id="17785-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="17785-107">随后，将根据新的汇率和日期更新或有利润或损失。</span><span class="sxs-lookup"><span data-stu-id="17785-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="17785-108">以下示例说明了该过程中创建的会计条目。</span><span class="sxs-lookup"><span data-stu-id="17785-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="17785-109">公司设置</span><span class="sxs-lookup"><span data-stu-id="17785-109">Company setup</span></span>
-   <span data-ttu-id="17785-110">**源/运营公司 (USMF)** – 美元 (USD) 用作会计和申报币种。</span><span class="sxs-lookup"><span data-stu-id="17785-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="17785-111">**合并的公司 (CON)** – 欧元 (EUR) 用作会计和申报币种。</span><span class="sxs-lookup"><span data-stu-id="17785-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="17785-112">**已实现利润** – 会计科目 801500</span><span class="sxs-lookup"><span data-stu-id="17785-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="17785-113">**已有损失** – 会计科目 801600</span><span class="sxs-lookup"><span data-stu-id="17785-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="17785-114">**或有利润** – 会计科目 801600</span><span class="sxs-lookup"><span data-stu-id="17785-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="17785-115">**或有损失** – 会计科目 801400</span><span class="sxs-lookup"><span data-stu-id="17785-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="17785-116">原始交易记录</span><span class="sxs-lookup"><span data-stu-id="17785-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="17785-117">USMF 中的现金收据交易记录</span><span class="sxs-lookup"><span data-stu-id="17785-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="17785-118">日期</span><span class="sxs-lookup"><span data-stu-id="17785-118">Date</span></span>       | <span data-ttu-id="17785-119">会计科目</span><span class="sxs-lookup"><span data-stu-id="17785-119">Ledger account</span></span>               | <span data-ttu-id="17785-120">货币</span><span class="sxs-lookup"><span data-stu-id="17785-120">Currency</span></span> | <span data-ttu-id="17785-121">金额</span><span class="sxs-lookup"><span data-stu-id="17785-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="17785-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="17785-122">10/11/2015</span></span> | <span data-ttu-id="17785-123">110110 – 现金</span><span class="sxs-lookup"><span data-stu-id="17785-123">110110 – Cash</span></span>                | <span data-ttu-id="17785-124">美元</span><span class="sxs-lookup"><span data-stu-id="17785-124">USD</span></span>      | <span data-ttu-id="17785-125">500</span><span class="sxs-lookup"><span data-stu-id="17785-125">500</span></span>    |
| <span data-ttu-id="17785-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="17785-126">10/11/2015</span></span> | <span data-ttu-id="17785-127">130100 – 应收帐款</span><span class="sxs-lookup"><span data-stu-id="17785-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="17785-128">美元</span><span class="sxs-lookup"><span data-stu-id="17785-128">USD</span></span>      | <span data-ttu-id="17785-129">-500</span><span class="sxs-lookup"><span data-stu-id="17785-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="17785-130">汇率</span><span class="sxs-lookup"><span data-stu-id="17785-130">Exchange rates</span></span>

| <span data-ttu-id="17785-131">原始币种</span><span class="sxs-lookup"><span data-stu-id="17785-131">From currency</span></span> | <span data-ttu-id="17785-132">目标币种</span><span class="sxs-lookup"><span data-stu-id="17785-132">To currency</span></span> | <span data-ttu-id="17785-133">开始日期</span><span class="sxs-lookup"><span data-stu-id="17785-133">Start date</span></span> | <span data-ttu-id="17785-134">汇率</span><span class="sxs-lookup"><span data-stu-id="17785-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="17785-135">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-135">EUR</span></span>           | <span data-ttu-id="17785-136">美元</span><span class="sxs-lookup"><span data-stu-id="17785-136">USD</span></span>         | <span data-ttu-id="17785-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="17785-137">10/1/2015</span></span>  | <span data-ttu-id="17785-138">200</span><span class="sxs-lookup"><span data-stu-id="17785-138">200</span></span>           |
| <span data-ttu-id="17785-139">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-139">EUR</span></span>           | <span data-ttu-id="17785-140">美元</span><span class="sxs-lookup"><span data-stu-id="17785-140">USD</span></span>         | <span data-ttu-id="17785-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="17785-141">11/1/2015</span></span>  | <span data-ttu-id="17785-142">150</span><span class="sxs-lookup"><span data-stu-id="17785-142">150</span></span>           |
| <span data-ttu-id="17785-143">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-143">EUR</span></span>           | <span data-ttu-id="17785-144">美元</span><span class="sxs-lookup"><span data-stu-id="17785-144">USD</span></span>         | <span data-ttu-id="17785-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="17785-145">12/1/2012</span></span>  | <span data-ttu-id="17785-146">100</span><span class="sxs-lookup"><span data-stu-id="17785-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="17785-147">执行合并（2015 年 10 月）</span><span class="sxs-lookup"><span data-stu-id="17785-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="17785-148">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="17785-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="17785-149">会计科目</span><span class="sxs-lookup"><span data-stu-id="17785-149">Ledger account</span></span> | <span data-ttu-id="17785-150">货币</span><span class="sxs-lookup"><span data-stu-id="17785-150">Currency</span></span> | <span data-ttu-id="17785-151">金额</span><span class="sxs-lookup"><span data-stu-id="17785-151">Amount</span></span> | <span data-ttu-id="17785-152">计算</span><span class="sxs-lookup"><span data-stu-id="17785-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="17785-153">110110</span><span class="sxs-lookup"><span data-stu-id="17785-153">110110</span></span>         | <span data-ttu-id="17785-154">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-154">EUR</span></span>      | <span data-ttu-id="17785-155">250</span><span class="sxs-lookup"><span data-stu-id="17785-155">250</span></span>    | <span data-ttu-id="17785-156">500 美元 × 50%</span><span class="sxs-lookup"><span data-stu-id="17785-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="17785-157">130100</span><span class="sxs-lookup"><span data-stu-id="17785-157">130100</span></span>         | <span data-ttu-id="17785-158">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-158">EUR</span></span>      | <span data-ttu-id="17785-159">-250</span><span class="sxs-lookup"><span data-stu-id="17785-159">-250</span></span>   | <span data-ttu-id="17785-160">-500 美元 × 50%</span><span class="sxs-lookup"><span data-stu-id="17785-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="17785-161">执行科目的币种重估（2015 年 10 月 1 日 - 2015 年 11 月 30 日）</span><span class="sxs-lookup"><span data-stu-id="17785-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="17785-162">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="17785-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="17785-163">会计科目</span><span class="sxs-lookup"><span data-stu-id="17785-163">Ledger account</span></span> | <span data-ttu-id="17785-164">货币</span><span class="sxs-lookup"><span data-stu-id="17785-164">Currency</span></span> | <span data-ttu-id="17785-165">金额</span><span class="sxs-lookup"><span data-stu-id="17785-165">Amount</span></span>  | <span data-ttu-id="17785-166">计算</span><span class="sxs-lookup"><span data-stu-id="17785-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="17785-167">110110</span><span class="sxs-lookup"><span data-stu-id="17785-167">110110</span></span>         | <span data-ttu-id="17785-168">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-168">EUR</span></span>      | <span data-ttu-id="17785-169">333.33</span><span class="sxs-lookup"><span data-stu-id="17785-169">333.33</span></span>  | <span data-ttu-id="17785-170">原金额为 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="17785-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="17785-171">130100</span><span class="sxs-lookup"><span data-stu-id="17785-171">130100</span></span>         | <span data-ttu-id="17785-172">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-172">EUR</span></span>      | <span data-ttu-id="17785-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="17785-173">-333.33</span></span> | <span data-ttu-id="17785-174">原金额为 -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="17785-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="17785-175">801400</span><span class="sxs-lookup"><span data-stu-id="17785-175">801400</span></span>         | <span data-ttu-id="17785-176">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-176">EUR</span></span>      | <span data-ttu-id="17785-177">83.33</span><span class="sxs-lookup"><span data-stu-id="17785-177">83.33</span></span>   | <span data-ttu-id="17785-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="17785-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="17785-179">801600</span><span class="sxs-lookup"><span data-stu-id="17785-179">801600</span></span>         | <span data-ttu-id="17785-180">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-180">EUR</span></span>      | <span data-ttu-id="17785-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="17785-181">-83.33</span></span>  | <span data-ttu-id="17785-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="17785-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="17785-183">您将看到申报币种金额的其他交易记录。</span><span class="sxs-lookup"><span data-stu-id="17785-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="17785-184">执行科目的币种重估（2015 年 10 月 1 日 - 2015 年 12 月 31 日）</span><span class="sxs-lookup"><span data-stu-id="17785-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="17785-185">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="17785-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="17785-186">会计科目</span><span class="sxs-lookup"><span data-stu-id="17785-186">Ledger account</span></span> | <span data-ttu-id="17785-187">货币</span><span class="sxs-lookup"><span data-stu-id="17785-187">Currency</span></span> | <span data-ttu-id="17785-188">金额</span><span class="sxs-lookup"><span data-stu-id="17785-188">Amount</span></span>  | <span data-ttu-id="17785-189">计算</span><span class="sxs-lookup"><span data-stu-id="17785-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="17785-190">110110</span><span class="sxs-lookup"><span data-stu-id="17785-190">110110</span></span>         | <span data-ttu-id="17785-191">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-191">EUR</span></span>      | <span data-ttu-id="17785-192">500.00</span><span class="sxs-lookup"><span data-stu-id="17785-192">500.00</span></span>  | <span data-ttu-id="17785-193">原金额为 500 × 1</span><span class="sxs-lookup"><span data-stu-id="17785-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="17785-194">130100</span><span class="sxs-lookup"><span data-stu-id="17785-194">130100</span></span>         | <span data-ttu-id="17785-195">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-195">EUR</span></span>      | <span data-ttu-id="17785-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="17785-196">-500.00</span></span> | <span data-ttu-id="17785-197">原金额为 -500 × 1</span><span class="sxs-lookup"><span data-stu-id="17785-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="17785-198">801400</span><span class="sxs-lookup"><span data-stu-id="17785-198">801400</span></span>         | <span data-ttu-id="17785-199">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-199">EUR</span></span>      | <span data-ttu-id="17785-200">250</span><span class="sxs-lookup"><span data-stu-id="17785-200">250</span></span>     | <span data-ttu-id="17785-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="17785-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="17785-202">801600</span><span class="sxs-lookup"><span data-stu-id="17785-202">801600</span></span>         | <span data-ttu-id="17785-203">欧元</span><span class="sxs-lookup"><span data-stu-id="17785-203">EUR</span></span>      | <span data-ttu-id="17785-204">-250</span><span class="sxs-lookup"><span data-stu-id="17785-204">-250</span></span>    | <span data-ttu-id="17785-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="17785-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]