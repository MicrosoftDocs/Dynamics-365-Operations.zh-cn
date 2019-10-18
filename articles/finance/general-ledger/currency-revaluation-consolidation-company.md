---
title: 合并公司中的币种重估
description: 此主题描述如何重估合并公司中的币种。
author: ShylaThompson
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
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7f0a18910cbaed382971e47eb688c075e7e6a5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176564"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="2b6af-103">合并公司中的币种重估</span><span class="sxs-lookup"><span data-stu-id="2b6af-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b6af-104">将一个记帐币种的数据与另一个记帐币种的数据合并时，如果汇率发生更改，则仍必须运行币种重估，以便准确重估帐户余额。</span><span class="sxs-lookup"><span data-stu-id="2b6af-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="2b6af-105">在最初合并数据时，使用**币种折算**选项卡可选择合并过程中用于折算的初始汇率。</span><span class="sxs-lookup"><span data-stu-id="2b6af-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="2b6af-106">在输入新的汇率后（例如，在下一个月），您必须重估帐户余额。</span><span class="sxs-lookup"><span data-stu-id="2b6af-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="2b6af-107">随后，将根据新的汇率和日期更新或有利润或损失。</span><span class="sxs-lookup"><span data-stu-id="2b6af-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="2b6af-108">以下示例说明了该过程中创建的会计条目。</span><span class="sxs-lookup"><span data-stu-id="2b6af-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="2b6af-109">公司设置</span><span class="sxs-lookup"><span data-stu-id="2b6af-109">Company setup</span></span>
-   <span data-ttu-id="2b6af-110">**源/运营公司 (USMF)** – 美元 (USD) 用作会计和申报币种。</span><span class="sxs-lookup"><span data-stu-id="2b6af-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="2b6af-111">**合并的公司 (CON)** – 欧元 (EUR) 用作会计和申报币种。</span><span class="sxs-lookup"><span data-stu-id="2b6af-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="2b6af-112">**已实现利润** – 会计科目 801500</span><span class="sxs-lookup"><span data-stu-id="2b6af-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="2b6af-113">**已有损失** – 会计科目 801600</span><span class="sxs-lookup"><span data-stu-id="2b6af-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="2b6af-114">**或有利润** – 会计科目 801600</span><span class="sxs-lookup"><span data-stu-id="2b6af-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="2b6af-115">**或有损失** – 会计科目 801400</span><span class="sxs-lookup"><span data-stu-id="2b6af-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="2b6af-116">原始交易记录</span><span class="sxs-lookup"><span data-stu-id="2b6af-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="2b6af-117">USMF 中的现金收据交易记录</span><span class="sxs-lookup"><span data-stu-id="2b6af-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="2b6af-118">日期</span><span class="sxs-lookup"><span data-stu-id="2b6af-118">Date</span></span>       | <span data-ttu-id="2b6af-119">会计科目</span><span class="sxs-lookup"><span data-stu-id="2b6af-119">Ledger account</span></span>               | <span data-ttu-id="2b6af-120">货币</span><span class="sxs-lookup"><span data-stu-id="2b6af-120">Currency</span></span> | <span data-ttu-id="2b6af-121">金额</span><span class="sxs-lookup"><span data-stu-id="2b6af-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="2b6af-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="2b6af-122">10/11/2015</span></span> | <span data-ttu-id="2b6af-123">110110 – 现金</span><span class="sxs-lookup"><span data-stu-id="2b6af-123">110110 – Cash</span></span>                | <span data-ttu-id="2b6af-124">美元</span><span class="sxs-lookup"><span data-stu-id="2b6af-124">USD</span></span>      | <span data-ttu-id="2b6af-125">500</span><span class="sxs-lookup"><span data-stu-id="2b6af-125">500</span></span>    |
| <span data-ttu-id="2b6af-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="2b6af-126">10/11/2015</span></span> | <span data-ttu-id="2b6af-127">130100 – 应收账款</span><span class="sxs-lookup"><span data-stu-id="2b6af-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="2b6af-128">美元</span><span class="sxs-lookup"><span data-stu-id="2b6af-128">USD</span></span>      | <span data-ttu-id="2b6af-129">-500</span><span class="sxs-lookup"><span data-stu-id="2b6af-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="2b6af-130">汇率</span><span class="sxs-lookup"><span data-stu-id="2b6af-130">Exchange rates</span></span>

| <span data-ttu-id="2b6af-131">原始币种</span><span class="sxs-lookup"><span data-stu-id="2b6af-131">From currency</span></span> | <span data-ttu-id="2b6af-132">目标币种</span><span class="sxs-lookup"><span data-stu-id="2b6af-132">To currency</span></span> | <span data-ttu-id="2b6af-133">开始日期</span><span class="sxs-lookup"><span data-stu-id="2b6af-133">Start date</span></span> | <span data-ttu-id="2b6af-134">汇率</span><span class="sxs-lookup"><span data-stu-id="2b6af-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="2b6af-135">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-135">EUR</span></span>           | <span data-ttu-id="2b6af-136">美元</span><span class="sxs-lookup"><span data-stu-id="2b6af-136">USD</span></span>         | <span data-ttu-id="2b6af-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="2b6af-137">10/1/2015</span></span>  | <span data-ttu-id="2b6af-138">200</span><span class="sxs-lookup"><span data-stu-id="2b6af-138">200</span></span>           |
| <span data-ttu-id="2b6af-139">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-139">EUR</span></span>           | <span data-ttu-id="2b6af-140">美元</span><span class="sxs-lookup"><span data-stu-id="2b6af-140">USD</span></span>         | <span data-ttu-id="2b6af-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="2b6af-141">11/1/2015</span></span>  | <span data-ttu-id="2b6af-142">150</span><span class="sxs-lookup"><span data-stu-id="2b6af-142">150</span></span>           |
| <span data-ttu-id="2b6af-143">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-143">EUR</span></span>           | <span data-ttu-id="2b6af-144">美元</span><span class="sxs-lookup"><span data-stu-id="2b6af-144">USD</span></span>         | <span data-ttu-id="2b6af-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="2b6af-145">12/1/2012</span></span>  | <span data-ttu-id="2b6af-146">100</span><span class="sxs-lookup"><span data-stu-id="2b6af-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="2b6af-147">执行合并（2015 年 10 月）</span><span class="sxs-lookup"><span data-stu-id="2b6af-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2b6af-148">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="2b6af-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="2b6af-149">会计科目</span><span class="sxs-lookup"><span data-stu-id="2b6af-149">Ledger account</span></span> | <span data-ttu-id="2b6af-150">货币</span><span class="sxs-lookup"><span data-stu-id="2b6af-150">Currency</span></span> | <span data-ttu-id="2b6af-151">金额</span><span class="sxs-lookup"><span data-stu-id="2b6af-151">Amount</span></span> | <span data-ttu-id="2b6af-152">计算</span><span class="sxs-lookup"><span data-stu-id="2b6af-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="2b6af-153">110110</span><span class="sxs-lookup"><span data-stu-id="2b6af-153">110110</span></span>         | <span data-ttu-id="2b6af-154">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-154">EUR</span></span>      | <span data-ttu-id="2b6af-155">250</span><span class="sxs-lookup"><span data-stu-id="2b6af-155">250</span></span>    | <span data-ttu-id="2b6af-156">500 美元 × 50%</span><span class="sxs-lookup"><span data-stu-id="2b6af-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="2b6af-157">130100</span><span class="sxs-lookup"><span data-stu-id="2b6af-157">130100</span></span>         | <span data-ttu-id="2b6af-158">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-158">EUR</span></span>      | <span data-ttu-id="2b6af-159">-250</span><span class="sxs-lookup"><span data-stu-id="2b6af-159">-250</span></span>   | <span data-ttu-id="2b6af-160">-500 美元 × 50%</span><span class="sxs-lookup"><span data-stu-id="2b6af-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="2b6af-161">执行科目的币种重估（2015 年 10 月 1 日 - 2015 年 11 月 30 日）</span><span class="sxs-lookup"><span data-stu-id="2b6af-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2b6af-162">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="2b6af-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="2b6af-163">会计科目</span><span class="sxs-lookup"><span data-stu-id="2b6af-163">Ledger account</span></span> | <span data-ttu-id="2b6af-164">货币</span><span class="sxs-lookup"><span data-stu-id="2b6af-164">Currency</span></span> | <span data-ttu-id="2b6af-165">金额</span><span class="sxs-lookup"><span data-stu-id="2b6af-165">Amount</span></span>  | <span data-ttu-id="2b6af-166">计算</span><span class="sxs-lookup"><span data-stu-id="2b6af-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="2b6af-167">110110</span><span class="sxs-lookup"><span data-stu-id="2b6af-167">110110</span></span>         | <span data-ttu-id="2b6af-168">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-168">EUR</span></span>      | <span data-ttu-id="2b6af-169">333.33</span><span class="sxs-lookup"><span data-stu-id="2b6af-169">333.33</span></span>  | <span data-ttu-id="2b6af-170">原金额为 500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="2b6af-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="2b6af-171">130100</span><span class="sxs-lookup"><span data-stu-id="2b6af-171">130100</span></span>         | <span data-ttu-id="2b6af-172">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-172">EUR</span></span>      | <span data-ttu-id="2b6af-173">-333.33</span><span class="sxs-lookup"><span data-stu-id="2b6af-173">-333.33</span></span> | <span data-ttu-id="2b6af-174">原金额为 -500 × 66.6667%</span><span class="sxs-lookup"><span data-stu-id="2b6af-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="2b6af-175">801400</span><span class="sxs-lookup"><span data-stu-id="2b6af-175">801400</span></span>         | <span data-ttu-id="2b6af-176">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-176">EUR</span></span>      | <span data-ttu-id="2b6af-177">83.33</span><span class="sxs-lookup"><span data-stu-id="2b6af-177">83.33</span></span>   | <span data-ttu-id="2b6af-178">333.33 – 250</span><span class="sxs-lookup"><span data-stu-id="2b6af-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="2b6af-179">801600</span><span class="sxs-lookup"><span data-stu-id="2b6af-179">801600</span></span>         | <span data-ttu-id="2b6af-180">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-180">EUR</span></span>      | <span data-ttu-id="2b6af-181">-83.33</span><span class="sxs-lookup"><span data-stu-id="2b6af-181">-83.33</span></span>  | <span data-ttu-id="2b6af-182">-333.33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="2b6af-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="2b6af-183">您将看到申报币种金额的其他交易记录。</span><span class="sxs-lookup"><span data-stu-id="2b6af-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="2b6af-184">执行科目的币种重估（2015 年 10 月 1 日 - 2015 年 12 月 31 日）</span><span class="sxs-lookup"><span data-stu-id="2b6af-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2b6af-185">合并公司中的余额</span><span class="sxs-lookup"><span data-stu-id="2b6af-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="2b6af-186">会计科目</span><span class="sxs-lookup"><span data-stu-id="2b6af-186">Ledger account</span></span> | <span data-ttu-id="2b6af-187">货币</span><span class="sxs-lookup"><span data-stu-id="2b6af-187">Currency</span></span> | <span data-ttu-id="2b6af-188">金额</span><span class="sxs-lookup"><span data-stu-id="2b6af-188">Amount</span></span>  | <span data-ttu-id="2b6af-189">计算</span><span class="sxs-lookup"><span data-stu-id="2b6af-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="2b6af-190">110110</span><span class="sxs-lookup"><span data-stu-id="2b6af-190">110110</span></span>         | <span data-ttu-id="2b6af-191">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-191">EUR</span></span>      | <span data-ttu-id="2b6af-192">500.00</span><span class="sxs-lookup"><span data-stu-id="2b6af-192">500.00</span></span>  | <span data-ttu-id="2b6af-193">原金额为 500 × 1</span><span class="sxs-lookup"><span data-stu-id="2b6af-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="2b6af-194">130100</span><span class="sxs-lookup"><span data-stu-id="2b6af-194">130100</span></span>         | <span data-ttu-id="2b6af-195">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-195">EUR</span></span>      | <span data-ttu-id="2b6af-196">-500.00</span><span class="sxs-lookup"><span data-stu-id="2b6af-196">-500.00</span></span> | <span data-ttu-id="2b6af-197">原金额为 -500 × 1</span><span class="sxs-lookup"><span data-stu-id="2b6af-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="2b6af-198">801400</span><span class="sxs-lookup"><span data-stu-id="2b6af-198">801400</span></span>         | <span data-ttu-id="2b6af-199">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-199">EUR</span></span>      | <span data-ttu-id="2b6af-200">250</span><span class="sxs-lookup"><span data-stu-id="2b6af-200">250</span></span>     | <span data-ttu-id="2b6af-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="2b6af-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="2b6af-202">801600</span><span class="sxs-lookup"><span data-stu-id="2b6af-202">801600</span></span>         | <span data-ttu-id="2b6af-203">欧元</span><span class="sxs-lookup"><span data-stu-id="2b6af-203">EUR</span></span>      | <span data-ttu-id="2b6af-204">-250</span><span class="sxs-lookup"><span data-stu-id="2b6af-204">-250</span></span>    | <span data-ttu-id="2b6af-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="2b6af-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





