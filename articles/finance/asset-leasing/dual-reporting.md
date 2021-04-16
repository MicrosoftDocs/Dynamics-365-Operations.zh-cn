---
title: 双重申报
description: 本主题通过一个示例指导您如何在资产租赁中同时满足国际财务申报标准 (IFRS) 申报和法定申报的要求。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c9f2bae330e688e1e941277d46ddcbd38916f8c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815972"
---
# <a name="dual-reporting"></a><span data-ttu-id="e4c44-103">双重申报</span><span class="sxs-lookup"><span data-stu-id="e4c44-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4c44-104">本主题通过一个示例指导您如何在资产租赁中同时满足国际财务申报标准 (IFRS) 申报和法定申报的要求。</span><span class="sxs-lookup"><span data-stu-id="e4c44-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="e4c44-105">需要熟悉 Microsoft Dynamics 365 Finance中的过帐层，这一可以让示例更容易理解。</span><span class="sxs-lookup"><span data-stu-id="e4c44-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="e4c44-106">示例</span><span class="sxs-lookup"><span data-stu-id="e4c44-106">Example</span></span>

<span data-ttu-id="e4c44-107">以下示例使用现金基础法和 IFRS 申报法介绍意大利法定申报下的租赁。</span><span class="sxs-lookup"><span data-stu-id="e4c44-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="e4c44-108">公司必须建立三本帐簿，以同时满足意大利的法定要求和 IFRS 16 的要求。</span><span class="sxs-lookup"><span data-stu-id="e4c44-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="e4c44-109">IFRS 16 需要一本帐簿，法规要求需要一本帐簿，并且还需要一本帐簿来自动撤消法定过帐。</span><span class="sxs-lookup"><span data-stu-id="e4c44-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="e4c44-110">下面的表中显示了这些帐簿的设置。</span><span class="sxs-lookup"><span data-stu-id="e4c44-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="e4c44-111">**IFRS 16 帐簿**</span><span class="sxs-lookup"><span data-stu-id="e4c44-111">**IFRS 16 book**</span></span>

<span data-ttu-id="e4c44-112">IFRS 16 帐簿设置为遵守 IFRS 16 会计标准。</span><span class="sxs-lookup"><span data-stu-id="e4c44-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="e4c44-113">此帐簿中过帐的所有条目都将过帐到自定义层。</span><span class="sxs-lookup"><span data-stu-id="e4c44-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="e4c44-114">姓名</span><span class="sxs-lookup"><span data-stu-id="e4c44-114">Name</span></span>                                    | <span data-ttu-id="e4c44-115">说明</span><span class="sxs-lookup"><span data-stu-id="e4c44-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="e4c44-116">帐簿类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-116">Book type</span></span>                               | <span data-ttu-id="e4c44-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="e4c44-117">IFRS 16</span></span>        |
| <span data-ttu-id="e4c44-118">帐簿描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-118">Book description</span></span>                        | <span data-ttu-id="e4c44-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="e4c44-119">IFRS 16</span></span>        |
| <span data-ttu-id="e4c44-120">过帐层</span><span class="sxs-lookup"><span data-stu-id="e4c44-120">Posting Layer</span></span>                           | <span data-ttu-id="e4c44-121">自定义层 1</span><span class="sxs-lookup"><span data-stu-id="e4c44-121">Custom layer 1</span></span> |
| <span data-ttu-id="e4c44-122">租赁类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-122">Lease Type</span></span>                              | <span data-ttu-id="e4c44-123">Finance</span><span class="sxs-lookup"><span data-stu-id="e4c44-123">Finance</span></span>        |
| <span data-ttu-id="e4c44-124">会计框架</span><span class="sxs-lookup"><span data-stu-id="e4c44-124">Accounting Framework</span></span>                    | <span data-ttu-id="e4c44-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="e4c44-125">IFRS 16</span></span>        |
| <span data-ttu-id="e4c44-126">租赁期/使用年限设置</span><span class="sxs-lookup"><span data-stu-id="e4c44-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="e4c44-127">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-127">0.00</span></span>           |
| <span data-ttu-id="e4c44-128">现值/资产的公平价值设置</span><span class="sxs-lookup"><span data-stu-id="e4c44-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="e4c44-129">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-129">0.00</span></span>           |
| <span data-ttu-id="e4c44-130">短期阈值</span><span class="sxs-lookup"><span data-stu-id="e4c44-130">Short-term threshold</span></span>                    | <span data-ttu-id="e4c44-131">12</span><span class="sxs-lookup"><span data-stu-id="e4c44-131">12</span></span>             |
| <span data-ttu-id="e4c44-132">低价值阈值</span><span class="sxs-lookup"><span data-stu-id="e4c44-132">Low Value Threshold</span></span>                     | <span data-ttu-id="e4c44-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-133">5,000.00</span></span>       |
| <span data-ttu-id="e4c44-134">向供应商付款</span><span class="sxs-lookup"><span data-stu-id="e4c44-134">Pay to Vendor</span></span>                           | <span data-ttu-id="e4c44-135">不</span><span class="sxs-lookup"><span data-stu-id="e4c44-135">No</span></span>             |

<span data-ttu-id="e4c44-136">**法定帐簿**</span><span class="sxs-lookup"><span data-stu-id="e4c44-136">**Statutory book**</span></span>

<span data-ttu-id="e4c44-137">法定帐簿是一种现金基础帐簿，在这种帐簿中，公司将把租赁费用作为每月支付的租金现金金额入帐。</span><span class="sxs-lookup"><span data-stu-id="e4c44-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="e4c44-138">这种帐簿不会产生使用权 (ROU) 资产或租赁负债。</span><span class="sxs-lookup"><span data-stu-id="e4c44-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="e4c44-139">姓名</span><span class="sxs-lookup"><span data-stu-id="e4c44-139">Name</span></span>                                    | <span data-ttu-id="e4c44-140">说明</span><span class="sxs-lookup"><span data-stu-id="e4c44-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="e4c44-141">帐簿类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-141">Book type</span></span>                               | <span data-ttu-id="e4c44-142">法定</span><span class="sxs-lookup"><span data-stu-id="e4c44-142">Statutory</span></span>   |
| <span data-ttu-id="e4c44-143">帐簿描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-143">Book description</span></span>                        | <span data-ttu-id="e4c44-144">本地 GAAP</span><span class="sxs-lookup"><span data-stu-id="e4c44-144">Local GAAP</span></span>  |
| <span data-ttu-id="e4c44-145">过帐层</span><span class="sxs-lookup"><span data-stu-id="e4c44-145">Posting Layer</span></span>                           | <span data-ttu-id="e4c44-146">当前</span><span class="sxs-lookup"><span data-stu-id="e4c44-146">Current</span></span>     |
| <span data-ttu-id="e4c44-147">租赁类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-147">Lease Type</span></span>                              | <span data-ttu-id="e4c44-148">自动</span><span class="sxs-lookup"><span data-stu-id="e4c44-148">Automatic</span></span>   |
| <span data-ttu-id="e4c44-149">会计框架</span><span class="sxs-lookup"><span data-stu-id="e4c44-149">Accounting Framework</span></span>                    | <span data-ttu-id="e4c44-150">现金基数</span><span class="sxs-lookup"><span data-stu-id="e4c44-150">Cash basis</span></span>  |
| <span data-ttu-id="e4c44-151">租赁期/使用年限设置</span><span class="sxs-lookup"><span data-stu-id="e4c44-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="e4c44-152">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-152">0.00</span></span>        |
| <span data-ttu-id="e4c44-153">现值/资产的公平价值设置</span><span class="sxs-lookup"><span data-stu-id="e4c44-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="e4c44-154">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-154">0.00</span></span>        |
| <span data-ttu-id="e4c44-155">短期阈值</span><span class="sxs-lookup"><span data-stu-id="e4c44-155">Short-term threshold</span></span>                    | <span data-ttu-id="e4c44-156">0</span><span class="sxs-lookup"><span data-stu-id="e4c44-156">0</span></span>           |
| <span data-ttu-id="e4c44-157">低价值阈值</span><span class="sxs-lookup"><span data-stu-id="e4c44-157">Low Value Threshold</span></span>                     | <span data-ttu-id="e4c44-158">0</span><span class="sxs-lookup"><span data-stu-id="e4c44-158">0</span></span>           |
| <span data-ttu-id="e4c44-159">向供应商付款</span><span class="sxs-lookup"><span data-stu-id="e4c44-159">Pay to Vendor</span></span>                           | <span data-ttu-id="e4c44-160">不</span><span class="sxs-lookup"><span data-stu-id="e4c44-160">No</span></span>          |

<span data-ttu-id="e4c44-161">**法定冲销帐簿**</span><span class="sxs-lookup"><span data-stu-id="e4c44-161">**Statutory reversal book**</span></span>

<span data-ttu-id="e4c44-162">法定冲销帐簿的建立方式与法定帐簿相同。</span><span class="sxs-lookup"><span data-stu-id="e4c44-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="e4c44-163">姓名</span><span class="sxs-lookup"><span data-stu-id="e4c44-163">Name</span></span>                                    | <span data-ttu-id="e4c44-164">说明</span><span class="sxs-lookup"><span data-stu-id="e4c44-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="e4c44-165">帐簿类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-165">Book type</span></span>                               | <span data-ttu-id="e4c44-166">法定 – 冲销</span><span class="sxs-lookup"><span data-stu-id="e4c44-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="e4c44-167">帐簿描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-167">Book description</span></span>                        | <span data-ttu-id="e4c44-168">用于冲销法定帐簿的帐簿</span><span class="sxs-lookup"><span data-stu-id="e4c44-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="e4c44-169">过帐层</span><span class="sxs-lookup"><span data-stu-id="e4c44-169">Posting Layer</span></span>                           | <span data-ttu-id="e4c44-170">自定义层 1</span><span class="sxs-lookup"><span data-stu-id="e4c44-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="e4c44-171">租赁类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-171">Lease Type</span></span>                              | <span data-ttu-id="e4c44-172">自动</span><span class="sxs-lookup"><span data-stu-id="e4c44-172">Automatic</span></span>                      |
| <span data-ttu-id="e4c44-173">会计框架</span><span class="sxs-lookup"><span data-stu-id="e4c44-173">Accounting Framework</span></span>                    | <span data-ttu-id="e4c44-174">现金基数</span><span class="sxs-lookup"><span data-stu-id="e4c44-174">Cash basis</span></span>                     |
| <span data-ttu-id="e4c44-175">租赁期/使用年限设置</span><span class="sxs-lookup"><span data-stu-id="e4c44-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="e4c44-176">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-176">0.00</span></span>                           |
| <span data-ttu-id="e4c44-177">现值/资产的公平价值设置</span><span class="sxs-lookup"><span data-stu-id="e4c44-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="e4c44-178">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-178">0.00</span></span>                           |
| <span data-ttu-id="e4c44-179">短期阈值</span><span class="sxs-lookup"><span data-stu-id="e4c44-179">Short-term threshold</span></span>                    | <span data-ttu-id="e4c44-180">0</span><span class="sxs-lookup"><span data-stu-id="e4c44-180">0</span></span>                              |
| <span data-ttu-id="e4c44-181">低价值阈值</span><span class="sxs-lookup"><span data-stu-id="e4c44-181">Low Value Threshold</span></span>                     | <span data-ttu-id="e4c44-182">0</span><span class="sxs-lookup"><span data-stu-id="e4c44-182">0</span></span>                              |
| <span data-ttu-id="e4c44-183">向供应商付款</span><span class="sxs-lookup"><span data-stu-id="e4c44-183">Pay to Vendor</span></span>                           | <span data-ttu-id="e4c44-184">不</span><span class="sxs-lookup"><span data-stu-id="e4c44-184">No</span></span>                             |

<span data-ttu-id="e4c44-185">在此示例中，创建了一个租赁，该租赁在 **常规** 和 **付款计划行** 选项卡上的设置如下。</span><span class="sxs-lookup"><span data-stu-id="e4c44-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="e4c44-186">**常规选项卡**</span><span class="sxs-lookup"><span data-stu-id="e4c44-186">**General tab**</span></span>

| <span data-ttu-id="e4c44-187">字段</span><span class="sxs-lookup"><span data-stu-id="e4c44-187">Field</span></span>                      | <span data-ttu-id="e4c44-188">值</span><span class="sxs-lookup"><span data-stu-id="e4c44-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="e4c44-189">增量借贷利率</span><span class="sxs-lookup"><span data-stu-id="e4c44-189">Incremental borrowing rate</span></span> | <span data-ttu-id="e4c44-190">5%</span><span class="sxs-lookup"><span data-stu-id="e4c44-190">5%</span></span>               |
| <span data-ttu-id="e4c44-191">开始日期</span><span class="sxs-lookup"><span data-stu-id="e4c44-191">Commencement date</span></span>          | <span data-ttu-id="e4c44-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="e4c44-192">1/1/2020</span></span>         |
| <span data-ttu-id="e4c44-193">租赁组</span><span class="sxs-lookup"><span data-stu-id="e4c44-193">Lease group</span></span>                | <span data-ttu-id="e4c44-194">建筑物</span><span class="sxs-lookup"><span data-stu-id="e4c44-194">Buildings</span></span>        |
| <span data-ttu-id="e4c44-195">供应商</span><span class="sxs-lookup"><span data-stu-id="e4c44-195">Vendor</span></span>                     | <span data-ttu-id="e4c44-196">1001</span><span class="sxs-lookup"><span data-stu-id="e4c44-196">1001</span></span>             |
| <span data-ttu-id="e4c44-197">资产的公平价值</span><span class="sxs-lookup"><span data-stu-id="e4c44-197">Fair value of the asset</span></span>    | <span data-ttu-id="e4c44-198">245,000</span><span class="sxs-lookup"><span data-stu-id="e4c44-198">245,000</span></span>          |
| <span data-ttu-id="e4c44-199">资产使用年限</span><span class="sxs-lookup"><span data-stu-id="e4c44-199">Asset useful life</span></span>          | <span data-ttu-id="e4c44-200">120</span><span class="sxs-lookup"><span data-stu-id="e4c44-200">120</span></span>              |
| <span data-ttu-id="e4c44-201">年金类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-201">Annuity type</span></span>               | <span data-ttu-id="e4c44-202">普通年金</span><span class="sxs-lookup"><span data-stu-id="e4c44-202">Ordinary annuity</span></span> |
| <span data-ttu-id="e4c44-203">复合间隔</span><span class="sxs-lookup"><span data-stu-id="e4c44-203">Compounding interval</span></span>       | <span data-ttu-id="e4c44-204">月度</span><span class="sxs-lookup"><span data-stu-id="e4c44-204">Monthly</span></span>          |

<span data-ttu-id="e4c44-205">**付款计划行选项卡**</span><span class="sxs-lookup"><span data-stu-id="e4c44-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="e4c44-206">字段</span><span class="sxs-lookup"><span data-stu-id="e4c44-206">Field</span></span>             | <span data-ttu-id="e4c44-207">值</span><span class="sxs-lookup"><span data-stu-id="e4c44-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="e4c44-208">开始日期</span><span class="sxs-lookup"><span data-stu-id="e4c44-208">Start date</span></span>        | <span data-ttu-id="e4c44-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="e4c44-209">1/1/2020</span></span>   |
| <span data-ttu-id="e4c44-210">期间间隔</span><span class="sxs-lookup"><span data-stu-id="e4c44-210">Period interval</span></span>   | <span data-ttu-id="e4c44-211">月数</span><span class="sxs-lookup"><span data-stu-id="e4c44-211">Months</span></span>     |
| <span data-ttu-id="e4c44-212">期间</span><span class="sxs-lookup"><span data-stu-id="e4c44-212">Periods</span></span>           | <span data-ttu-id="e4c44-213">24</span><span class="sxs-lookup"><span data-stu-id="e4c44-213">24</span></span>         |
| <span data-ttu-id="e4c44-214">结束日期</span><span class="sxs-lookup"><span data-stu-id="e4c44-214">End date</span></span>          | <span data-ttu-id="e4c44-215">12/31/2020</span><span class="sxs-lookup"><span data-stu-id="e4c44-215">12/31/2020</span></span> |
| <span data-ttu-id="e4c44-216">付款频率</span><span class="sxs-lookup"><span data-stu-id="e4c44-216">Payment frequency</span></span> | <span data-ttu-id="e4c44-217">月度</span><span class="sxs-lookup"><span data-stu-id="e4c44-217">Monthly</span></span>    |
| <span data-ttu-id="e4c44-218">付款金额</span><span class="sxs-lookup"><span data-stu-id="e4c44-218">Payment amount</span></span>    | <span data-ttu-id="e4c44-219">1,000</span><span class="sxs-lookup"><span data-stu-id="e4c44-219">1,000</span></span>      |

<span data-ttu-id="e4c44-220">要在两个框架下考虑此租赁，请使用当前过帐层和自定义过帐层。</span><span class="sxs-lookup"><span data-stu-id="e4c44-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="e4c44-221">下表显示了各种申报标准下公平地代表财务状况所需的每个日记帐条目的示例。</span><span class="sxs-lookup"><span data-stu-id="e4c44-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="e4c44-222">后面提供了租赁首月各日记帐条目的详细说明。</span><span class="sxs-lookup"><span data-stu-id="e4c44-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="e4c44-223">帐号</span><span class="sxs-lookup"><span data-stu-id="e4c44-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="e4c44-224">说明</span><span class="sxs-lookup"><span data-stu-id="e4c44-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="e4c44-225">法定帐簿（当前层）</span><span class="sxs-lookup"><span data-stu-id="e4c44-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="e4c44-226">当前层总计</span><span class="sxs-lookup"><span data-stu-id="e4c44-226">Current layer total</span></span></th>
<th><span data-ttu-id="e4c44-227">冲销帐簿（自定义层）</span><span class="sxs-lookup"><span data-stu-id="e4c44-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="e4c44-228">IFRS 16 帐簿（自定义层）</span><span class="sxs-lookup"><span data-stu-id="e4c44-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="e4c44-229">当前层 + 自定义层总计</span><span class="sxs-lookup"><span data-stu-id="e4c44-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e4c44-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="e4c44-230">JE-100</span></span></th>
<th><span data-ttu-id="e4c44-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="e4c44-231">JE-110</span></span></th>
<th><span data-ttu-id="e4c44-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="e4c44-232">JE-120</span></span></th>
<th><span data-ttu-id="e4c44-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="e4c44-233">JE-130</span></span></th>
<th><span data-ttu-id="e4c44-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="e4c44-234">JE-140</span></span></th>
<th><span data-ttu-id="e4c44-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="e4c44-235">JE-150</span></span></th>
<th><span data-ttu-id="e4c44-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="e4c44-236">JE-160</span></span></th>
<th><span data-ttu-id="e4c44-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="e4c44-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e4c44-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="e4c44-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="e4c44-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="e4c44-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="e4c44-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="e4c44-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="e4c44-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="e4c44-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4c44-246">1</span><span class="sxs-lookup"><span data-stu-id="e4c44-246">1</span></span></td>
<td><span data-ttu-id="e4c44-247">租赁费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-247">Lease expense</span></span></td>
<td><span data-ttu-id="e4c44-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-249">1,000.00</span></span></td>
<td><span data-ttu-id="e4c44-250">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-251">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-252">2</span><span class="sxs-lookup"><span data-stu-id="e4c44-252">2</span></span></td>
<td><span data-ttu-id="e4c44-253">银行手续费</span><span class="sxs-lookup"><span data-stu-id="e4c44-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-254">3.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-255">3.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-256">3.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-257">3</span><span class="sxs-lookup"><span data-stu-id="e4c44-257">3</span></span></td>
<td><span data-ttu-id="e4c44-258">增值税费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-259">5.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-260">5.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-261">5.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-262">4</span><span class="sxs-lookup"><span data-stu-id="e4c44-262">4</span></span></td>
<td><span data-ttu-id="e4c44-263">结算科目</span><span class="sxs-lookup"><span data-stu-id="e4c44-263">Clearing account</span></span></td>
<td><span data-ttu-id="e4c44-264">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-264">-1,000.00</span></span></td>
<td><span data-ttu-id="e4c44-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-266">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-266">0.00</span></span></td>
<td><span data-ttu-id="e4c44-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-268">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-269">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-270">5</span><span class="sxs-lookup"><span data-stu-id="e4c44-270">5</span></span></td>
<td><span data-ttu-id="e4c44-271">应付帐款</span><span class="sxs-lookup"><span data-stu-id="e4c44-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-272">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-272">-1,008.00</span></span></td>
<td><span data-ttu-id="e4c44-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-273">1,008.00</span></span></td>
<td><span data-ttu-id="e4c44-274">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-275">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-276">6</span><span class="sxs-lookup"><span data-stu-id="e4c44-276">6</span></span></td>
<td><span data-ttu-id="e4c44-277">使用权资产</span><span class="sxs-lookup"><span data-stu-id="e4c44-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-278">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="e4c44-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-281">7</span><span class="sxs-lookup"><span data-stu-id="e4c44-281">7</span></span></td>
<td><span data-ttu-id="e4c44-282">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="e4c44-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-283">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-284">-22,794.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-284">-22,794.00</span></span></td>
<td><span data-ttu-id="e4c44-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-285">1,000.00</span></span></td>
<td><span data-ttu-id="e4c44-286">-94.97</span><span class="sxs-lookup"><span data-stu-id="e4c44-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-287">-21,888.87</span><span class="sxs-lookup"><span data-stu-id="e4c44-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-288">8</span><span class="sxs-lookup"><span data-stu-id="e4c44-288">8</span></span></td>
<td><span data-ttu-id="e4c44-289">利息费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-290">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-291">94.97</span><span class="sxs-lookup"><span data-stu-id="e4c44-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-292">94.97</span><span class="sxs-lookup"><span data-stu-id="e4c44-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-293">9</span><span class="sxs-lookup"><span data-stu-id="e4c44-293">9</span></span></td>
<td><span data-ttu-id="e4c44-294">现金</span><span class="sxs-lookup"><span data-stu-id="e4c44-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-295">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-295">-1,008.00</span></span></td>
<td><span data-ttu-id="e4c44-296">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-297">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-298">10</span><span class="sxs-lookup"><span data-stu-id="e4c44-298">10</span></span></td>
<td><span data-ttu-id="e4c44-299">折旧费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-300">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-301">949.75</span><span class="sxs-lookup"><span data-stu-id="e4c44-301">949.75</span></span></td>
<td><span data-ttu-id="e4c44-302">949.75</span><span class="sxs-lookup"><span data-stu-id="e4c44-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-303">11</span><span class="sxs-lookup"><span data-stu-id="e4c44-303">11</span></span></td>
<td><span data-ttu-id="e4c44-304">累计折旧</span><span class="sxs-lookup"><span data-stu-id="e4c44-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-305">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-306">-949.75</span><span class="sxs-lookup"><span data-stu-id="e4c44-306">-949.75</span></span></td>
<td><span data-ttu-id="e4c44-307">-949.75</span><span class="sxs-lookup"><span data-stu-id="e4c44-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4c44-308">如上表所示，根据法定申报和 IFRS 申报，需要申报三本帐簿。</span><span class="sxs-lookup"><span data-stu-id="e4c44-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="e4c44-309">法定帐簿根据当前层下基于现金的记帐记录租赁付款。</span><span class="sxs-lookup"><span data-stu-id="e4c44-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="e4c44-310">法定冲销帐簿冲销法定日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="e4c44-311">IFRS 16 帐簿创建按照 IFRS 16 所需的日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="e4c44-312">一次只能输入一个租赁。</span><span class="sxs-lookup"><span data-stu-id="e4c44-312">You must enter a lease only one time.</span></span> <span data-ttu-id="e4c44-313">然后可以打开 **帐簿** 页以查看与租赁关联的所有帐簿。</span><span class="sxs-lookup"><span data-stu-id="e4c44-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="e4c44-314">创建帐簿时，所有三本帐簿都必须与同一个租赁记录关联。</span><span class="sxs-lookup"><span data-stu-id="e4c44-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="e4c44-315">第一个日记帐条目将租赁费用记录在法定帐簿下。</span><span class="sxs-lookup"><span data-stu-id="e4c44-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="e4c44-316">您可以批量创建付款，也可以通过在法定帐簿中选择付款计划来创建付款。</span><span class="sxs-lookup"><span data-stu-id="e4c44-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="e4c44-317">对于此示例，将从付款计划为法定帐簿生成以下日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="e4c44-318">租赁付款 – 1/31/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="e4c44-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="e4c44-319">科目类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-319">Account type</span></span> | <span data-ttu-id="e4c44-320">帐号</span><span class="sxs-lookup"><span data-stu-id="e4c44-320">Account number</span></span> | <span data-ttu-id="e4c44-321">层</span><span class="sxs-lookup"><span data-stu-id="e4c44-321">Layer</span></span>   | <span data-ttu-id="e4c44-322">科目描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-322">Account description</span></span> | <span data-ttu-id="e4c44-323">借记</span><span class="sxs-lookup"><span data-stu-id="e4c44-323">Debit</span></span>    | <span data-ttu-id="e4c44-324">贷记</span><span class="sxs-lookup"><span data-stu-id="e4c44-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="e4c44-325">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-325">Ledger</span></span>       | <span data-ttu-id="e4c44-326">1</span><span class="sxs-lookup"><span data-stu-id="e4c44-326">1</span></span>              | <span data-ttu-id="e4c44-327">当前</span><span class="sxs-lookup"><span data-stu-id="e4c44-327">Current</span></span> | <span data-ttu-id="e4c44-328">租赁费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-328">Lease expense</span></span>       | <span data-ttu-id="e4c44-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-329">1,000.00</span></span> |          |
| <span data-ttu-id="e4c44-330">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-330">Ledger</span></span>       | <span data-ttu-id="e4c44-331">4</span><span class="sxs-lookup"><span data-stu-id="e4c44-331">4</span></span>              | <span data-ttu-id="e4c44-332">当前</span><span class="sxs-lookup"><span data-stu-id="e4c44-332">Current</span></span> | <span data-ttu-id="e4c44-333">结算科目</span><span class="sxs-lookup"><span data-stu-id="e4c44-333">Clearing account</span></span>    |          | <span data-ttu-id="e4c44-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-334">1,000.00</span></span> |

<span data-ttu-id="e4c44-335">应付帐款业务员使用标准 Dynamics 365 功能创建发票以支付资产租赁以外的租赁费用。</span><span class="sxs-lookup"><span data-stu-id="e4c44-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="e4c44-336">但是，应付帐款业务员不是选择 **租赁费用** 作为借方科目，而是选择清算科目以生成以下条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="e4c44-337">AP 流程 – 1/31/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="e4c44-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="e4c44-338">科目类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-338">Account type</span></span> | <span data-ttu-id="e4c44-339">帐号</span><span class="sxs-lookup"><span data-stu-id="e4c44-339">Account number</span></span> | <span data-ttu-id="e4c44-340">层</span><span class="sxs-lookup"><span data-stu-id="e4c44-340">Layer</span></span>   | <span data-ttu-id="e4c44-341">科目描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-341">Account description</span></span> | <span data-ttu-id="e4c44-342">借记</span><span class="sxs-lookup"><span data-stu-id="e4c44-342">Debit</span></span>    | <span data-ttu-id="e4c44-343">贷记</span><span class="sxs-lookup"><span data-stu-id="e4c44-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="e4c44-344">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-344">Ledger</span></span>       | <span data-ttu-id="e4c44-345">4</span><span class="sxs-lookup"><span data-stu-id="e4c44-345">4</span></span>              | <span data-ttu-id="e4c44-346">当前</span><span class="sxs-lookup"><span data-stu-id="e4c44-346">Current</span></span> | <span data-ttu-id="e4c44-347">结算科目</span><span class="sxs-lookup"><span data-stu-id="e4c44-347">Clearing account</span></span>    | <span data-ttu-id="e4c44-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-348">1,000.00</span></span> |          |
| <span data-ttu-id="e4c44-349">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-349">Ledger</span></span>       | <span data-ttu-id="e4c44-350">2</span><span class="sxs-lookup"><span data-stu-id="e4c44-350">2</span></span>              | <span data-ttu-id="e4c44-351">当前</span><span class="sxs-lookup"><span data-stu-id="e4c44-351">Current</span></span> | <span data-ttu-id="e4c44-352">银行手续费</span><span class="sxs-lookup"><span data-stu-id="e4c44-352">Bank fee</span></span>            | <span data-ttu-id="e4c44-353">3.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-353">3.00</span></span>     |          |
| <span data-ttu-id="e4c44-354">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-354">Ledger</span></span>       | <span data-ttu-id="e4c44-355">3</span><span class="sxs-lookup"><span data-stu-id="e4c44-355">3</span></span>              | <span data-ttu-id="e4c44-356">当前</span><span class="sxs-lookup"><span data-stu-id="e4c44-356">Current</span></span> | <span data-ttu-id="e4c44-357">增值税费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-357">VAT expense</span></span>         | <span data-ttu-id="e4c44-358">5.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-358">5.00</span></span>     |          |
| <span data-ttu-id="e4c44-359">供应商</span><span class="sxs-lookup"><span data-stu-id="e4c44-359">Vendor</span></span>       | <span data-ttu-id="e4c44-360">5</span><span class="sxs-lookup"><span data-stu-id="e4c44-360">5</span></span>              | <span data-ttu-id="e4c44-361">当前</span><span class="sxs-lookup"><span data-stu-id="e4c44-361">Current</span></span> | <span data-ttu-id="e4c44-362">应付帐款</span><span class="sxs-lookup"><span data-stu-id="e4c44-362">Accounts payable</span></span>    |          | <span data-ttu-id="e4c44-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-363">1,008.00</span></span> |

<span data-ttu-id="e4c44-364">将对帐单发给供应商时，请执行常规付款流程。</span><span class="sxs-lookup"><span data-stu-id="e4c44-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="e4c44-365">在此流程中，将生成以下日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="e4c44-366">现金付款 – 1/31/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="e4c44-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="e4c44-367">科目类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-367">Account type</span></span> | <span data-ttu-id="e4c44-368">帐号</span><span class="sxs-lookup"><span data-stu-id="e4c44-368">Account number</span></span> | <span data-ttu-id="e4c44-369">层</span><span class="sxs-lookup"><span data-stu-id="e4c44-369">Layer</span></span>   | <span data-ttu-id="e4c44-370">科目描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-370">Account description</span></span> | <span data-ttu-id="e4c44-371">借记</span><span class="sxs-lookup"><span data-stu-id="e4c44-371">Debit</span></span>    | <span data-ttu-id="e4c44-372">贷记</span><span class="sxs-lookup"><span data-stu-id="e4c44-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="e4c44-373">供应商</span><span class="sxs-lookup"><span data-stu-id="e4c44-373">Vendor</span></span>       | <span data-ttu-id="e4c44-374">5</span><span class="sxs-lookup"><span data-stu-id="e4c44-374">5</span></span>              | <span data-ttu-id="e4c44-375">当前</span><span class="sxs-lookup"><span data-stu-id="e4c44-375">Current</span></span> | <span data-ttu-id="e4c44-376">应付帐款</span><span class="sxs-lookup"><span data-stu-id="e4c44-376">Accounts Payable</span></span>    | <span data-ttu-id="e4c44-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-377">1,008.00</span></span> |          |
| <span data-ttu-id="e4c44-378">银行</span><span class="sxs-lookup"><span data-stu-id="e4c44-378">Bank</span></span>         | <span data-ttu-id="e4c44-379">9</span><span class="sxs-lookup"><span data-stu-id="e4c44-379">9</span></span>              | <span data-ttu-id="e4c44-380">当前</span><span class="sxs-lookup"><span data-stu-id="e4c44-380">Current</span></span> | <span data-ttu-id="e4c44-381">现金</span><span class="sxs-lookup"><span data-stu-id="e4c44-381">Cash</span></span>                |          | <span data-ttu-id="e4c44-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-382">1,008.00</span></span> |

<span data-ttu-id="e4c44-383">至此，您已经按照法定申报要求充分考虑了此租赁，因此可以通过使用当前层来生成试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="e4c44-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="e4c44-384">系统将返回包含以下数据的试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="e4c44-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="e4c44-385">帐号</span><span class="sxs-lookup"><span data-stu-id="e4c44-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="e4c44-386">说明</span><span class="sxs-lookup"><span data-stu-id="e4c44-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="e4c44-387">法定帐簿（当前层）</span><span class="sxs-lookup"><span data-stu-id="e4c44-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="e4c44-388">当前层总计</span><span class="sxs-lookup"><span data-stu-id="e4c44-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e4c44-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="e4c44-389">JE-100</span></span></th>
<th><span data-ttu-id="e4c44-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="e4c44-390">JE-110</span></span></th>
<th><span data-ttu-id="e4c44-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="e4c44-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="e4c44-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="e4c44-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="e4c44-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="e4c44-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e4c44-395">1</span><span class="sxs-lookup"><span data-stu-id="e4c44-395">1</span></span></td>
<td><span data-ttu-id="e4c44-396">租赁费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-396">Lease expense</span></span></td>
<td><span data-ttu-id="e4c44-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-399">2</span><span class="sxs-lookup"><span data-stu-id="e4c44-399">2</span></span></td>
<td><span data-ttu-id="e4c44-400">银行手续费</span><span class="sxs-lookup"><span data-stu-id="e4c44-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-401">3.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-402">3.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-403">3</span><span class="sxs-lookup"><span data-stu-id="e4c44-403">3</span></span></td>
<td><span data-ttu-id="e4c44-404">增值税费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-405">5.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-406">5.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-407">4</span><span class="sxs-lookup"><span data-stu-id="e4c44-407">4</span></span></td>
<td><span data-ttu-id="e4c44-408">结算科目</span><span class="sxs-lookup"><span data-stu-id="e4c44-408">Clearing account</span></span></td>
<td><span data-ttu-id="e4c44-409">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-409">-1,000.00</span></span></td>
<td><span data-ttu-id="e4c44-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-411">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-412">5</span><span class="sxs-lookup"><span data-stu-id="e4c44-412">5</span></span></td>
<td><span data-ttu-id="e4c44-413">应付帐款</span><span class="sxs-lookup"><span data-stu-id="e4c44-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="e4c44-414">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-414">-1,008.00</span></span></td>
<td><span data-ttu-id="e4c44-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-415">1,008.00</span></span></td>
<td><span data-ttu-id="e4c44-416">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-417">6</span><span class="sxs-lookup"><span data-stu-id="e4c44-417">6</span></span></td>
<td><span data-ttu-id="e4c44-418">使用权资产</span><span class="sxs-lookup"><span data-stu-id="e4c44-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-419">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-420">7</span><span class="sxs-lookup"><span data-stu-id="e4c44-420">7</span></span></td>
<td><span data-ttu-id="e4c44-421">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="e4c44-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-422">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-423">8</span><span class="sxs-lookup"><span data-stu-id="e4c44-423">8</span></span></td>
<td><span data-ttu-id="e4c44-424">利息费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-425">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-426">9</span><span class="sxs-lookup"><span data-stu-id="e4c44-426">9</span></span></td>
<td><span data-ttu-id="e4c44-427">现金</span><span class="sxs-lookup"><span data-stu-id="e4c44-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-428">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-428">-1,008.00</span></span></td>
<td><span data-ttu-id="e4c44-429">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-430">10</span><span class="sxs-lookup"><span data-stu-id="e4c44-430">10</span></span></td>
<td><span data-ttu-id="e4c44-431">折旧费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-432">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e4c44-433">11</span><span class="sxs-lookup"><span data-stu-id="e4c44-433">11</span></span></td>
<td><span data-ttu-id="e4c44-434">累计折旧</span><span class="sxs-lookup"><span data-stu-id="e4c44-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="e4c44-435">0.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e4c44-436">如果要使用 IFRS 16 数据来运行同一个试算平衡表，则必须冲销法定会计日记帐条目，并且必须过帐 IFRS 16 日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="e4c44-437">为了冲销法定日记帐条目，此示例中包括一个法定冲销帐簿，该帐簿与法定帐簿具有相同的设置，但相反的过帐配置文件。</span><span class="sxs-lookup"><span data-stu-id="e4c44-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="e4c44-438">例如，法定帐簿 *借记* 租赁费用科目，但冲销帐簿则 *贷记* 此科目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="e4c44-439">这些关系很容易在 **资产租赁参数** 页面（**资产租赁 \> 设置 \> 资产租赁参数**）中的资产租赁过帐科目中定义。</span><span class="sxs-lookup"><span data-stu-id="e4c44-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="e4c44-440">如果对冲销帐簿使用用于法定帐簿的相同流程，将生成以下日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="e4c44-441">区别在于冲销帐簿记录法定帐簿中的冲销条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="e4c44-442">还将为自定义层创建冲销条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="e4c44-443">在当前层运行试算平衡表时，不包括冲销日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="e4c44-444">租赁付款 – 1/31/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="e4c44-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="e4c44-445">科目类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-445">Account type</span></span> | <span data-ttu-id="e4c44-446">帐号</span><span class="sxs-lookup"><span data-stu-id="e4c44-446">Account number</span></span> | <span data-ttu-id="e4c44-447">层</span><span class="sxs-lookup"><span data-stu-id="e4c44-447">Layer</span></span>  | <span data-ttu-id="e4c44-448">科目描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-448">Account description</span></span> | <span data-ttu-id="e4c44-449">借记</span><span class="sxs-lookup"><span data-stu-id="e4c44-449">Debit</span></span>    | <span data-ttu-id="e4c44-450">贷记</span><span class="sxs-lookup"><span data-stu-id="e4c44-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="e4c44-451">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-451">Ledger</span></span>       | <span data-ttu-id="e4c44-452">4</span><span class="sxs-lookup"><span data-stu-id="e4c44-452">4</span></span>              | <span data-ttu-id="e4c44-453">自定义</span><span class="sxs-lookup"><span data-stu-id="e4c44-453">Custom</span></span> | <span data-ttu-id="e4c44-454">结算科目</span><span class="sxs-lookup"><span data-stu-id="e4c44-454">Clearing account</span></span>    | <span data-ttu-id="e4c44-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-455">1,000.00</span></span> |          |
| <span data-ttu-id="e4c44-456">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-456">Ledger</span></span>       | <span data-ttu-id="e4c44-457">1</span><span class="sxs-lookup"><span data-stu-id="e4c44-457">1</span></span>              | <span data-ttu-id="e4c44-458">自定义</span><span class="sxs-lookup"><span data-stu-id="e4c44-458">Custom</span></span> | <span data-ttu-id="e4c44-459">租赁费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-459">Lease expense</span></span>       |          | <span data-ttu-id="e4c44-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-460">1,000.00</span></span> |

<span data-ttu-id="e4c44-461">现在，您已经删除了法定日记帐条目，您将在 IFRS 16 帐簿中预订 IFRS 16 所需的所有日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="e4c44-462">这些条目包括对 ROU 资产和负债的初始确认，以及利息和折旧的记录。</span><span class="sxs-lookup"><span data-stu-id="e4c44-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="e4c44-463">初始确认 – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="e4c44-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="e4c44-464">科目类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-464">Account type</span></span> | <span data-ttu-id="e4c44-465">帐号</span><span class="sxs-lookup"><span data-stu-id="e4c44-465">Account number</span></span> | <span data-ttu-id="e4c44-466">层</span><span class="sxs-lookup"><span data-stu-id="e4c44-466">Layer</span></span>  | <span data-ttu-id="e4c44-467">科目描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-467">Account description</span></span>      | <span data-ttu-id="e4c44-468">借记</span><span class="sxs-lookup"><span data-stu-id="e4c44-468">Debit</span></span>     | <span data-ttu-id="e4c44-469">贷记</span><span class="sxs-lookup"><span data-stu-id="e4c44-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="e4c44-470">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-470">Ledger</span></span>       | <span data-ttu-id="e4c44-471">6</span><span class="sxs-lookup"><span data-stu-id="e4c44-471">6</span></span>              | <span data-ttu-id="e4c44-472">自定义</span><span class="sxs-lookup"><span data-stu-id="e4c44-472">Custom</span></span> | <span data-ttu-id="e4c44-473">使用权资产</span><span class="sxs-lookup"><span data-stu-id="e4c44-473">ROU Asset</span></span>                | <span data-ttu-id="e4c44-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="e4c44-474">22,793.90</span></span> |           |
| <span data-ttu-id="e4c44-475">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-475">Ledger</span></span>       | <span data-ttu-id="e4c44-476">7</span><span class="sxs-lookup"><span data-stu-id="e4c44-476">7</span></span>              | <span data-ttu-id="e4c44-477">自定义</span><span class="sxs-lookup"><span data-stu-id="e4c44-477">Custom</span></span> | <span data-ttu-id="e4c44-478">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="e4c44-478">Finance lease obligation</span></span> |           | <span data-ttu-id="e4c44-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="e4c44-479">22,793.90</span></span> |

<span data-ttu-id="e4c44-480">租赁付款与其他租赁付款一样过帐。</span><span class="sxs-lookup"><span data-stu-id="e4c44-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="e4c44-481">使用清算科目的原因是为了确保只将现金记入一次。</span><span class="sxs-lookup"><span data-stu-id="e4c44-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="e4c44-482">租赁付款 – 1/31/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="e4c44-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="e4c44-483">科目类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-483">Account type</span></span> | <span data-ttu-id="e4c44-484">帐号</span><span class="sxs-lookup"><span data-stu-id="e4c44-484">Account number</span></span> | <span data-ttu-id="e4c44-485">层</span><span class="sxs-lookup"><span data-stu-id="e4c44-485">Layer</span></span>  | <span data-ttu-id="e4c44-486">科目描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-486">Account description</span></span>      | <span data-ttu-id="e4c44-487">借记</span><span class="sxs-lookup"><span data-stu-id="e4c44-487">Debit</span></span>    | <span data-ttu-id="e4c44-488">贷记</span><span class="sxs-lookup"><span data-stu-id="e4c44-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="e4c44-489">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-489">Ledger</span></span>       | <span data-ttu-id="e4c44-490">7</span><span class="sxs-lookup"><span data-stu-id="e4c44-490">7</span></span>              | <span data-ttu-id="e4c44-491">自定义</span><span class="sxs-lookup"><span data-stu-id="e4c44-491">Custom</span></span> | <span data-ttu-id="e4c44-492">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="e4c44-492">Finance lease obligation</span></span> | <span data-ttu-id="e4c44-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-493">1,000.00</span></span> |          |
| <span data-ttu-id="e4c44-494">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-494">Ledger</span></span>       | <span data-ttu-id="e4c44-495">4</span><span class="sxs-lookup"><span data-stu-id="e4c44-495">4</span></span>              | <span data-ttu-id="e4c44-496">自定义</span><span class="sxs-lookup"><span data-stu-id="e4c44-496">Custom</span></span> | <span data-ttu-id="e4c44-497">结算科目</span><span class="sxs-lookup"><span data-stu-id="e4c44-497">Clearing account</span></span>         |          | <span data-ttu-id="e4c44-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-498">1,000.00</span></span> |

<span data-ttu-id="e4c44-499">利息费用日记帐条目从负债摊销计划中生成。</span><span class="sxs-lookup"><span data-stu-id="e4c44-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="e4c44-500">利息费用 – 1/31/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="e4c44-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="e4c44-501">科目类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-501">Account type</span></span> | <span data-ttu-id="e4c44-502">帐号</span><span class="sxs-lookup"><span data-stu-id="e4c44-502">Account number</span></span> | <span data-ttu-id="e4c44-503">层</span><span class="sxs-lookup"><span data-stu-id="e4c44-503">Layer</span></span>  | <span data-ttu-id="e4c44-504">科目描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-504">Account description</span></span>      | <span data-ttu-id="e4c44-505">借记</span><span class="sxs-lookup"><span data-stu-id="e4c44-505">Debit</span></span> | <span data-ttu-id="e4c44-506">贷记</span><span class="sxs-lookup"><span data-stu-id="e4c44-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="e4c44-507">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-507">Ledger</span></span>       | <span data-ttu-id="e4c44-508">8</span><span class="sxs-lookup"><span data-stu-id="e4c44-508">8</span></span>              | <span data-ttu-id="e4c44-509">自定义</span><span class="sxs-lookup"><span data-stu-id="e4c44-509">Custom</span></span> | <span data-ttu-id="e4c44-510">利息费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-510">Interest expense</span></span>         | <span data-ttu-id="e4c44-511">94.97</span><span class="sxs-lookup"><span data-stu-id="e4c44-511">94.97</span></span> |        |
| <span data-ttu-id="e4c44-512">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-512">Ledger</span></span>       | <span data-ttu-id="e4c44-513">7</span><span class="sxs-lookup"><span data-stu-id="e4c44-513">7</span></span>              | <span data-ttu-id="e4c44-514">自定义</span><span class="sxs-lookup"><span data-stu-id="e4c44-514">Custom</span></span> | <span data-ttu-id="e4c44-515">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="e4c44-515">Finance lease obligation</span></span> |       | <span data-ttu-id="e4c44-516">94.97</span><span class="sxs-lookup"><span data-stu-id="e4c44-516">94.97</span></span>  |

<span data-ttu-id="e4c44-517">折旧费用日记帐条目从资产折旧计划中生成。</span><span class="sxs-lookup"><span data-stu-id="e4c44-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="e4c44-518">折旧费用 – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="e4c44-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="e4c44-519">科目类型</span><span class="sxs-lookup"><span data-stu-id="e4c44-519">Account type</span></span> | <span data-ttu-id="e4c44-520">帐号</span><span class="sxs-lookup"><span data-stu-id="e4c44-520">Account number</span></span> | <span data-ttu-id="e4c44-521">层</span><span class="sxs-lookup"><span data-stu-id="e4c44-521">Layer</span></span>  | <span data-ttu-id="e4c44-522">科目描述</span><span class="sxs-lookup"><span data-stu-id="e4c44-522">Account description</span></span>      | <span data-ttu-id="e4c44-523">借记</span><span class="sxs-lookup"><span data-stu-id="e4c44-523">Debit</span></span>  | <span data-ttu-id="e4c44-524">贷记</span><span class="sxs-lookup"><span data-stu-id="e4c44-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="e4c44-525">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-525">Ledger</span></span>       | <span data-ttu-id="e4c44-526">10</span><span class="sxs-lookup"><span data-stu-id="e4c44-526">10</span></span>             | <span data-ttu-id="e4c44-527">自定义</span><span class="sxs-lookup"><span data-stu-id="e4c44-527">Custom</span></span> | <span data-ttu-id="e4c44-528">折旧费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-528">Depreciation expense</span></span>     | <span data-ttu-id="e4c44-529">949.75</span><span class="sxs-lookup"><span data-stu-id="e4c44-529">949.75</span></span> |        |
| <span data-ttu-id="e4c44-530">总帐</span><span class="sxs-lookup"><span data-stu-id="e4c44-530">Ledger</span></span>       | <span data-ttu-id="e4c44-531">11</span><span class="sxs-lookup"><span data-stu-id="e4c44-531">11</span></span>             | <span data-ttu-id="e4c44-532">自定义</span><span class="sxs-lookup"><span data-stu-id="e4c44-532">Custom</span></span> | <span data-ttu-id="e4c44-533">累计折旧</span><span class="sxs-lookup"><span data-stu-id="e4c44-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="e4c44-534">949.75</span><span class="sxs-lookup"><span data-stu-id="e4c44-534">949.75</span></span> |

<span data-ttu-id="e4c44-535">创建并过帐所有这些日记帐条目后，您将看到以下“自定义层 1”值。</span><span class="sxs-lookup"><span data-stu-id="e4c44-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="e4c44-536">请注意，最后一列包括银行手续费、增值税 (VAT) 费用和上一层的现金减少额，但不包括法定申报日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="e4c44-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="e4c44-537">因此，您可以实现真正的双重申报功能。</span><span class="sxs-lookup"><span data-stu-id="e4c44-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="e4c44-538">此时，公司仅需运行其试算平衡表，并将当前层和自定义层结合起来即可创建 IFRS 试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="e4c44-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="e4c44-539">科目编号</span><span class="sxs-lookup"><span data-stu-id="e4c44-539">Account No</span></span> | <span data-ttu-id="e4c44-540">说明</span><span class="sxs-lookup"><span data-stu-id="e4c44-540">Description</span></span>              | <span data-ttu-id="e4c44-541">法定帐簿\-当前层\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="e4c44-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="e4c44-542">法定帐簿\-当前层\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="e4c44-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="e4c44-543">法定帐簿\-当前层\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="e4c44-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="e4c44-544">当前层 \- 总计</span><span class="sxs-lookup"><span data-stu-id="e4c44-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="e4c44-545">冲销帐簿\-自定义层\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="e4c44-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="e4c44-546">IFRS 16 帐簿\-自定义层\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="e4c44-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="e4c44-547">IFRS 16 帐簿\-自定义层\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="e4c44-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="e4c44-548">IFRS 16 帐簿\-自定义层\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="e4c44-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="e4c44-549">IFRS 16 帐簿\-自定义层\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="e4c44-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="e4c44-550">自定义层 \+ 当前层 \- 总计</span><span class="sxs-lookup"><span data-stu-id="e4c44-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="e4c44-551">1</span><span class="sxs-lookup"><span data-stu-id="e4c44-551">1</span></span>          | <span data-ttu-id="e4c44-552">租赁费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-552">Lease expense</span></span>            | <span data-ttu-id="e4c44-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="e4c44-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-554">1,000\.00</span></span>               |   | <span data-ttu-id="e4c44-555">\-1,000</span><span class="sxs-lookup"><span data-stu-id="e4c44-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="e4c44-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-556">0\.00</span></span>                                   |
| <span data-ttu-id="e4c44-557">2</span><span class="sxs-lookup"><span data-stu-id="e4c44-557">2</span></span>          | <span data-ttu-id="e4c44-558">银行手续费</span><span class="sxs-lookup"><span data-stu-id="e4c44-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="e4c44-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="e4c44-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="e4c44-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-561">3\.00</span></span>                                   |
| <span data-ttu-id="e4c44-562">3</span><span class="sxs-lookup"><span data-stu-id="e4c44-562">3</span></span>          | <span data-ttu-id="e4c44-563">增值税费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="e4c44-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="e4c44-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="e4c44-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-566">5\.00</span></span>                                   |
| <span data-ttu-id="e4c44-567">4</span><span class="sxs-lookup"><span data-stu-id="e4c44-567">4</span></span>          | <span data-ttu-id="e4c44-568">结算科目</span><span class="sxs-lookup"><span data-stu-id="e4c44-568">Clearing account</span></span>         | <span data-ttu-id="e4c44-569">\-1,000\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="e4c44-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="e4c44-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-571">0\.00</span></span>                   |   | <span data-ttu-id="e4c44-572">1,000</span><span class="sxs-lookup"><span data-stu-id="e4c44-572">1,000</span></span>                                           |                                                | <span data-ttu-id="e4c44-573">\-1,000</span><span class="sxs-lookup"><span data-stu-id="e4c44-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="e4c44-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-574">0\.00</span></span>                                   |
| <span data-ttu-id="e4c44-575">5</span><span class="sxs-lookup"><span data-stu-id="e4c44-575">5</span></span>          | <span data-ttu-id="e4c44-576">应付帐款</span><span class="sxs-lookup"><span data-stu-id="e4c44-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="e4c44-577">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="e4c44-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-578">1,008\.00</span></span>                                         | <span data-ttu-id="e4c44-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="e4c44-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-580">0\.00</span></span>                                   |
| <span data-ttu-id="e4c44-581">6</span><span class="sxs-lookup"><span data-stu-id="e4c44-581">6</span></span>          | <span data-ttu-id="e4c44-582">使用权资产</span><span class="sxs-lookup"><span data-stu-id="e4c44-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="e4c44-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="e4c44-584">22,794</span><span class="sxs-lookup"><span data-stu-id="e4c44-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="e4c44-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="e4c44-585">22,793\.90</span></span>                              |
| <span data-ttu-id="e4c44-586">7</span><span class="sxs-lookup"><span data-stu-id="e4c44-586">7</span></span>          | <span data-ttu-id="e4c44-587">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="e4c44-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="e4c44-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="e4c44-589">\-22,794</span><span class="sxs-lookup"><span data-stu-id="e4c44-589">\-22,794</span></span>                                       | <span data-ttu-id="e4c44-590">1,000</span><span class="sxs-lookup"><span data-stu-id="e4c44-590">1,000</span></span>                                          | <span data-ttu-id="e4c44-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="e4c44-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="e4c44-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="e4c44-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="e4c44-593">8</span><span class="sxs-lookup"><span data-stu-id="e4c44-593">8</span></span>          | <span data-ttu-id="e4c44-594">利息费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="e4c44-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="e4c44-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="e4c44-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="e4c44-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="e4c44-597">94\.97</span></span>                                  |
| <span data-ttu-id="e4c44-598">9</span><span class="sxs-lookup"><span data-stu-id="e4c44-598">9</span></span>          | <span data-ttu-id="e4c44-599">现金</span><span class="sxs-lookup"><span data-stu-id="e4c44-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="e4c44-600">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="e4c44-601">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="e4c44-602">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="e4c44-603">10</span><span class="sxs-lookup"><span data-stu-id="e4c44-603">10</span></span>         | <span data-ttu-id="e4c44-604">折旧费用</span><span class="sxs-lookup"><span data-stu-id="e4c44-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="e4c44-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="e4c44-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="e4c44-606">949\.75</span></span>                                        | <span data-ttu-id="e4c44-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="e4c44-607">949\.75</span></span>                                 |
| <span data-ttu-id="e4c44-608">11</span><span class="sxs-lookup"><span data-stu-id="e4c44-608">11</span></span>         | <span data-ttu-id="e4c44-609">累计折旧</span><span class="sxs-lookup"><span data-stu-id="e4c44-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="e4c44-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="e4c44-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="e4c44-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="e4c44-611">\-949\.75</span></span>                                      | <span data-ttu-id="e4c44-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="e4c44-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]