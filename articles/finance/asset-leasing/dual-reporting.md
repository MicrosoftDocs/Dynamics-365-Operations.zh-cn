---
title: 双重申报
description: 本主题通过一个示例指导您如何在资产租赁中同时满足国际财务申报标准 (IFRS) 申报和法定申报的要求。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003173"
---
# <a name="dual-reporting"></a><span data-ttu-id="8e2ae-103">双重申报</span><span class="sxs-lookup"><span data-stu-id="8e2ae-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e2ae-104">本主题通过一个示例指导您如何在资产租赁中同时满足国际财务申报标准 (IFRS) 申报和法定申报的要求。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="8e2ae-105">需要熟悉 Microsoft Dynamics 365 Finance中的过帐层，这一可以让示例更容易理解。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="8e2ae-106">示例</span><span class="sxs-lookup"><span data-stu-id="8e2ae-106">Example</span></span>

<span data-ttu-id="8e2ae-107">以下示例使用现金基础法和 IFRS 申报法介绍意大利法定申报下的租赁。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="8e2ae-108">公司必须建立三本帐簿，以同时满足意大利的法定要求和 IFRS 16 的要求。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="8e2ae-109">IFRS 16 需要一本帐簿，法规要求需要一本帐簿，并且还需要一本帐簿来自动撤消法定过帐。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="8e2ae-110">下面的表中显示了这些帐簿的设置。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="8e2ae-111">**IFRS 16 帐簿**</span><span class="sxs-lookup"><span data-stu-id="8e2ae-111">**IFRS 16 book**</span></span>

<span data-ttu-id="8e2ae-112">IFRS 16 帐簿设置为遵守 IFRS 16 会计标准。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="8e2ae-113">此帐簿中过帐的所有条目都将过帐到自定义层。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="8e2ae-114">姓名</span><span class="sxs-lookup"><span data-stu-id="8e2ae-114">Name</span></span>                                    | <span data-ttu-id="8e2ae-115">说明</span><span class="sxs-lookup"><span data-stu-id="8e2ae-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="8e2ae-116">帐簿类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-116">Book type</span></span>                               | <span data-ttu-id="8e2ae-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="8e2ae-117">IFRS 16</span></span>        |
| <span data-ttu-id="8e2ae-118">帐簿描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-118">Book description</span></span>                        | <span data-ttu-id="8e2ae-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="8e2ae-119">IFRS 16</span></span>        |
| <span data-ttu-id="8e2ae-120">过帐层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-120">Posting Layer</span></span>                           | <span data-ttu-id="8e2ae-121">自定义层 1</span><span class="sxs-lookup"><span data-stu-id="8e2ae-121">Custom layer 1</span></span> |
| <span data-ttu-id="8e2ae-122">租赁类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-122">Lease Type</span></span>                              | <span data-ttu-id="8e2ae-123">Finance</span><span class="sxs-lookup"><span data-stu-id="8e2ae-123">Finance</span></span>        |
| <span data-ttu-id="8e2ae-124">会计框架</span><span class="sxs-lookup"><span data-stu-id="8e2ae-124">Accounting Framework</span></span>                    | <span data-ttu-id="8e2ae-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="8e2ae-125">IFRS 16</span></span>        |
| <span data-ttu-id="8e2ae-126">租赁期/使用年限设置</span><span class="sxs-lookup"><span data-stu-id="8e2ae-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="8e2ae-127">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-127">0.00</span></span>           |
| <span data-ttu-id="8e2ae-128">现值/资产的公平价值设置</span><span class="sxs-lookup"><span data-stu-id="8e2ae-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="8e2ae-129">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-129">0.00</span></span>           |
| <span data-ttu-id="8e2ae-130">短期阈值</span><span class="sxs-lookup"><span data-stu-id="8e2ae-130">Short-term threshold</span></span>                    | <span data-ttu-id="8e2ae-131">12</span><span class="sxs-lookup"><span data-stu-id="8e2ae-131">12</span></span>             |
| <span data-ttu-id="8e2ae-132">低价值阈值</span><span class="sxs-lookup"><span data-stu-id="8e2ae-132">Low Value Threshold</span></span>                     | <span data-ttu-id="8e2ae-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-133">5,000.00</span></span>       |
| <span data-ttu-id="8e2ae-134">向供应商付款</span><span class="sxs-lookup"><span data-stu-id="8e2ae-134">Pay to Vendor</span></span>                           | <span data-ttu-id="8e2ae-135">不</span><span class="sxs-lookup"><span data-stu-id="8e2ae-135">No</span></span>             |

<span data-ttu-id="8e2ae-136">**法定帐簿**</span><span class="sxs-lookup"><span data-stu-id="8e2ae-136">**Statutory book**</span></span>

<span data-ttu-id="8e2ae-137">法定帐簿是一种现金基础帐簿，在这种帐簿中，公司将把租赁费用作为每月支付的租金现金金额入帐。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="8e2ae-138">这种帐簿不会产生使用权 (ROU) 资产或租赁负债。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="8e2ae-139">姓名</span><span class="sxs-lookup"><span data-stu-id="8e2ae-139">Name</span></span>                                    | <span data-ttu-id="8e2ae-140">说明</span><span class="sxs-lookup"><span data-stu-id="8e2ae-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="8e2ae-141">帐簿类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-141">Book type</span></span>                               | <span data-ttu-id="8e2ae-142">法定</span><span class="sxs-lookup"><span data-stu-id="8e2ae-142">Statutory</span></span>   |
| <span data-ttu-id="8e2ae-143">帐簿描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-143">Book description</span></span>                        | <span data-ttu-id="8e2ae-144">本地 GAAP</span><span class="sxs-lookup"><span data-stu-id="8e2ae-144">Local GAAP</span></span>  |
| <span data-ttu-id="8e2ae-145">过帐层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-145">Posting Layer</span></span>                           | <span data-ttu-id="8e2ae-146">当前</span><span class="sxs-lookup"><span data-stu-id="8e2ae-146">Current</span></span>     |
| <span data-ttu-id="8e2ae-147">租赁类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-147">Lease Type</span></span>                              | <span data-ttu-id="8e2ae-148">自动</span><span class="sxs-lookup"><span data-stu-id="8e2ae-148">Automatic</span></span>   |
| <span data-ttu-id="8e2ae-149">会计框架</span><span class="sxs-lookup"><span data-stu-id="8e2ae-149">Accounting Framework</span></span>                    | <span data-ttu-id="8e2ae-150">现金基数</span><span class="sxs-lookup"><span data-stu-id="8e2ae-150">Cash basis</span></span>  |
| <span data-ttu-id="8e2ae-151">租赁期/使用年限设置</span><span class="sxs-lookup"><span data-stu-id="8e2ae-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="8e2ae-152">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-152">0.00</span></span>        |
| <span data-ttu-id="8e2ae-153">现值/资产的公平价值设置</span><span class="sxs-lookup"><span data-stu-id="8e2ae-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="8e2ae-154">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-154">0.00</span></span>        |
| <span data-ttu-id="8e2ae-155">短期阈值</span><span class="sxs-lookup"><span data-stu-id="8e2ae-155">Short-term threshold</span></span>                    | <span data-ttu-id="8e2ae-156">0</span><span class="sxs-lookup"><span data-stu-id="8e2ae-156">0</span></span>           |
| <span data-ttu-id="8e2ae-157">低价值阈值</span><span class="sxs-lookup"><span data-stu-id="8e2ae-157">Low Value Threshold</span></span>                     | <span data-ttu-id="8e2ae-158">0</span><span class="sxs-lookup"><span data-stu-id="8e2ae-158">0</span></span>           |
| <span data-ttu-id="8e2ae-159">向供应商付款</span><span class="sxs-lookup"><span data-stu-id="8e2ae-159">Pay to Vendor</span></span>                           | <span data-ttu-id="8e2ae-160">不</span><span class="sxs-lookup"><span data-stu-id="8e2ae-160">No</span></span>          |

<span data-ttu-id="8e2ae-161">**法定冲销帐簿**</span><span class="sxs-lookup"><span data-stu-id="8e2ae-161">**Statutory reversal book**</span></span>

<span data-ttu-id="8e2ae-162">法定冲销帐簿的建立方式与法定帐簿相同。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="8e2ae-163">姓名</span><span class="sxs-lookup"><span data-stu-id="8e2ae-163">Name</span></span>                                    | <span data-ttu-id="8e2ae-164">说明</span><span class="sxs-lookup"><span data-stu-id="8e2ae-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="8e2ae-165">帐簿类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-165">Book type</span></span>                               | <span data-ttu-id="8e2ae-166">法定 – 冲销</span><span class="sxs-lookup"><span data-stu-id="8e2ae-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="8e2ae-167">帐簿描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-167">Book description</span></span>                        | <span data-ttu-id="8e2ae-168">用于冲销法定帐簿的帐簿</span><span class="sxs-lookup"><span data-stu-id="8e2ae-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="8e2ae-169">过帐层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-169">Posting Layer</span></span>                           | <span data-ttu-id="8e2ae-170">自定义层 1</span><span class="sxs-lookup"><span data-stu-id="8e2ae-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="8e2ae-171">租赁类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-171">Lease Type</span></span>                              | <span data-ttu-id="8e2ae-172">自动</span><span class="sxs-lookup"><span data-stu-id="8e2ae-172">Automatic</span></span>                      |
| <span data-ttu-id="8e2ae-173">会计框架</span><span class="sxs-lookup"><span data-stu-id="8e2ae-173">Accounting Framework</span></span>                    | <span data-ttu-id="8e2ae-174">现金基数</span><span class="sxs-lookup"><span data-stu-id="8e2ae-174">Cash basis</span></span>                     |
| <span data-ttu-id="8e2ae-175">租赁期/使用年限设置</span><span class="sxs-lookup"><span data-stu-id="8e2ae-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="8e2ae-176">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-176">0.00</span></span>                           |
| <span data-ttu-id="8e2ae-177">现值/资产的公平价值设置</span><span class="sxs-lookup"><span data-stu-id="8e2ae-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="8e2ae-178">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-178">0.00</span></span>                           |
| <span data-ttu-id="8e2ae-179">短期阈值</span><span class="sxs-lookup"><span data-stu-id="8e2ae-179">Short-term threshold</span></span>                    | <span data-ttu-id="8e2ae-180">0</span><span class="sxs-lookup"><span data-stu-id="8e2ae-180">0</span></span>                              |
| <span data-ttu-id="8e2ae-181">低价值阈值</span><span class="sxs-lookup"><span data-stu-id="8e2ae-181">Low Value Threshold</span></span>                     | <span data-ttu-id="8e2ae-182">0</span><span class="sxs-lookup"><span data-stu-id="8e2ae-182">0</span></span>                              |
| <span data-ttu-id="8e2ae-183">向供应商付款</span><span class="sxs-lookup"><span data-stu-id="8e2ae-183">Pay to Vendor</span></span>                           | <span data-ttu-id="8e2ae-184">不</span><span class="sxs-lookup"><span data-stu-id="8e2ae-184">No</span></span>                             |

<span data-ttu-id="8e2ae-185">在此示例中，创建了一个租赁，该租赁在 **常规** 和 **付款计划行** 选项卡上的设置如下。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="8e2ae-186">**常规选项卡**</span><span class="sxs-lookup"><span data-stu-id="8e2ae-186">**General tab**</span></span>

| <span data-ttu-id="8e2ae-187">字段</span><span class="sxs-lookup"><span data-stu-id="8e2ae-187">Field</span></span>                      | <span data-ttu-id="8e2ae-188">值</span><span class="sxs-lookup"><span data-stu-id="8e2ae-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="8e2ae-189">增量借贷利率</span><span class="sxs-lookup"><span data-stu-id="8e2ae-189">Incremental borrowing rate</span></span> | <span data-ttu-id="8e2ae-190">5%</span><span class="sxs-lookup"><span data-stu-id="8e2ae-190">5%</span></span>               |
| <span data-ttu-id="8e2ae-191">开始日期</span><span class="sxs-lookup"><span data-stu-id="8e2ae-191">Commencement date</span></span>          | <span data-ttu-id="8e2ae-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="8e2ae-192">1/1/2020</span></span>         |
| <span data-ttu-id="8e2ae-193">租赁组</span><span class="sxs-lookup"><span data-stu-id="8e2ae-193">Lease group</span></span>                | <span data-ttu-id="8e2ae-194">建筑物</span><span class="sxs-lookup"><span data-stu-id="8e2ae-194">Buildings</span></span>        |
| <span data-ttu-id="8e2ae-195">供应商</span><span class="sxs-lookup"><span data-stu-id="8e2ae-195">Vendor</span></span>                     | <span data-ttu-id="8e2ae-196">1001</span><span class="sxs-lookup"><span data-stu-id="8e2ae-196">1001</span></span>             |
| <span data-ttu-id="8e2ae-197">资产的公平价值</span><span class="sxs-lookup"><span data-stu-id="8e2ae-197">Fair value of the asset</span></span>    | <span data-ttu-id="8e2ae-198">245,000</span><span class="sxs-lookup"><span data-stu-id="8e2ae-198">245,000</span></span>          |
| <span data-ttu-id="8e2ae-199">资产使用年限</span><span class="sxs-lookup"><span data-stu-id="8e2ae-199">Asset useful life</span></span>          | <span data-ttu-id="8e2ae-200">120</span><span class="sxs-lookup"><span data-stu-id="8e2ae-200">120</span></span>              |
| <span data-ttu-id="8e2ae-201">年金类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-201">Annuity type</span></span>               | <span data-ttu-id="8e2ae-202">普通年金</span><span class="sxs-lookup"><span data-stu-id="8e2ae-202">Ordinary annuity</span></span> |
| <span data-ttu-id="8e2ae-203">复合间隔</span><span class="sxs-lookup"><span data-stu-id="8e2ae-203">Compounding interval</span></span>       | <span data-ttu-id="8e2ae-204">月度</span><span class="sxs-lookup"><span data-stu-id="8e2ae-204">Monthly</span></span>          |

<span data-ttu-id="8e2ae-205">**付款计划行选项卡**</span><span class="sxs-lookup"><span data-stu-id="8e2ae-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="8e2ae-206">字段</span><span class="sxs-lookup"><span data-stu-id="8e2ae-206">Field</span></span>             | <span data-ttu-id="8e2ae-207">值</span><span class="sxs-lookup"><span data-stu-id="8e2ae-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="8e2ae-208">开始日期</span><span class="sxs-lookup"><span data-stu-id="8e2ae-208">Start date</span></span>        | <span data-ttu-id="8e2ae-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="8e2ae-209">1/1/2020</span></span>   |
| <span data-ttu-id="8e2ae-210">期间间隔</span><span class="sxs-lookup"><span data-stu-id="8e2ae-210">Period interval</span></span>   | <span data-ttu-id="8e2ae-211">月数</span><span class="sxs-lookup"><span data-stu-id="8e2ae-211">Months</span></span>     |
| <span data-ttu-id="8e2ae-212">期间</span><span class="sxs-lookup"><span data-stu-id="8e2ae-212">Periods</span></span>           | <span data-ttu-id="8e2ae-213">24</span><span class="sxs-lookup"><span data-stu-id="8e2ae-213">24</span></span>         |
| <span data-ttu-id="8e2ae-214">结束日期</span><span class="sxs-lookup"><span data-stu-id="8e2ae-214">End date</span></span>          | <span data-ttu-id="8e2ae-215">12/31/2020</span><span class="sxs-lookup"><span data-stu-id="8e2ae-215">12/31/2020</span></span> |
| <span data-ttu-id="8e2ae-216">付款频率</span><span class="sxs-lookup"><span data-stu-id="8e2ae-216">Payment frequency</span></span> | <span data-ttu-id="8e2ae-217">月度</span><span class="sxs-lookup"><span data-stu-id="8e2ae-217">Monthly</span></span>    |
| <span data-ttu-id="8e2ae-218">付款金额</span><span class="sxs-lookup"><span data-stu-id="8e2ae-218">Payment amount</span></span>    | <span data-ttu-id="8e2ae-219">1,000</span><span class="sxs-lookup"><span data-stu-id="8e2ae-219">1,000</span></span>      |

<span data-ttu-id="8e2ae-220">要在两个框架下考虑此租赁，请使用当前过帐层和自定义过帐层。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="8e2ae-221">下表显示了各种申报标准下公平地代表财务状况所需的每个日记帐条目的示例。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="8e2ae-222">后面提供了租赁首月各日记帐条目的详细说明。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="8e2ae-223">帐号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="8e2ae-224">说明</span><span class="sxs-lookup"><span data-stu-id="8e2ae-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="8e2ae-225">法定帐簿（当前层）</span><span class="sxs-lookup"><span data-stu-id="8e2ae-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="8e2ae-226">当前层总计</span><span class="sxs-lookup"><span data-stu-id="8e2ae-226">Current layer total</span></span></th>
<th><span data-ttu-id="8e2ae-227">冲销帐簿（自定义层）</span><span class="sxs-lookup"><span data-stu-id="8e2ae-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="8e2ae-228">IFRS 16 帐簿（自定义层）</span><span class="sxs-lookup"><span data-stu-id="8e2ae-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="8e2ae-229">当前层 + 自定义层总计</span><span class="sxs-lookup"><span data-stu-id="8e2ae-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e2ae-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="8e2ae-230">JE-100</span></span></th>
<th><span data-ttu-id="8e2ae-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="8e2ae-231">JE-110</span></span></th>
<th><span data-ttu-id="8e2ae-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="8e2ae-232">JE-120</span></span></th>
<th><span data-ttu-id="8e2ae-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="8e2ae-233">JE-130</span></span></th>
<th><span data-ttu-id="8e2ae-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="8e2ae-234">JE-140</span></span></th>
<th><span data-ttu-id="8e2ae-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="8e2ae-235">JE-150</span></span></th>
<th><span data-ttu-id="8e2ae-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="8e2ae-236">JE-160</span></span></th>
<th><span data-ttu-id="8e2ae-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="8e2ae-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e2ae-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e2ae-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e2ae-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e2ae-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e2ae-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e2ae-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e2ae-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e2ae-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e2ae-246">1</span><span class="sxs-lookup"><span data-stu-id="8e2ae-246">1</span></span></td>
<td><span data-ttu-id="8e2ae-247">租赁费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-247">Lease expense</span></span></td>
<td><span data-ttu-id="8e2ae-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-249">1,000.00</span></span></td>
<td><span data-ttu-id="8e2ae-250">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-251">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-252">2</span><span class="sxs-lookup"><span data-stu-id="8e2ae-252">2</span></span></td>
<td><span data-ttu-id="8e2ae-253">银行手续费</span><span class="sxs-lookup"><span data-stu-id="8e2ae-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-254">3.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-255">3.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-256">3.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-257">3</span><span class="sxs-lookup"><span data-stu-id="8e2ae-257">3</span></span></td>
<td><span data-ttu-id="8e2ae-258">增值税费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-259">5.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-260">5.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-261">5.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-262">4</span><span class="sxs-lookup"><span data-stu-id="8e2ae-262">4</span></span></td>
<td><span data-ttu-id="8e2ae-263">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e2ae-263">Clearing account</span></span></td>
<td><span data-ttu-id="8e2ae-264">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-264">-1,000.00</span></span></td>
<td><span data-ttu-id="8e2ae-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-266">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-266">0.00</span></span></td>
<td><span data-ttu-id="8e2ae-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-268">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-269">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-270">5</span><span class="sxs-lookup"><span data-stu-id="8e2ae-270">5</span></span></td>
<td><span data-ttu-id="8e2ae-271">应付帐款</span><span class="sxs-lookup"><span data-stu-id="8e2ae-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-272">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-272">-1,008.00</span></span></td>
<td><span data-ttu-id="8e2ae-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-273">1,008.00</span></span></td>
<td><span data-ttu-id="8e2ae-274">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-275">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-276">6</span><span class="sxs-lookup"><span data-stu-id="8e2ae-276">6</span></span></td>
<td><span data-ttu-id="8e2ae-277">使用权资产</span><span class="sxs-lookup"><span data-stu-id="8e2ae-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-278">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="8e2ae-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-281">7</span><span class="sxs-lookup"><span data-stu-id="8e2ae-281">7</span></span></td>
<td><span data-ttu-id="8e2ae-282">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e2ae-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-283">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-284">-22,794.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-284">-22,794.00</span></span></td>
<td><span data-ttu-id="8e2ae-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-285">1,000.00</span></span></td>
<td><span data-ttu-id="8e2ae-286">-94.97</span><span class="sxs-lookup"><span data-stu-id="8e2ae-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-287">-21,888.87</span><span class="sxs-lookup"><span data-stu-id="8e2ae-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-288">8</span><span class="sxs-lookup"><span data-stu-id="8e2ae-288">8</span></span></td>
<td><span data-ttu-id="8e2ae-289">利息费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-290">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-291">94.97</span><span class="sxs-lookup"><span data-stu-id="8e2ae-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-292">94.97</span><span class="sxs-lookup"><span data-stu-id="8e2ae-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-293">9</span><span class="sxs-lookup"><span data-stu-id="8e2ae-293">9</span></span></td>
<td><span data-ttu-id="8e2ae-294">现金</span><span class="sxs-lookup"><span data-stu-id="8e2ae-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-295">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-295">-1,008.00</span></span></td>
<td><span data-ttu-id="8e2ae-296">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-297">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-298">10</span><span class="sxs-lookup"><span data-stu-id="8e2ae-298">10</span></span></td>
<td><span data-ttu-id="8e2ae-299">折旧费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-300">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-301">949.75</span><span class="sxs-lookup"><span data-stu-id="8e2ae-301">949.75</span></span></td>
<td><span data-ttu-id="8e2ae-302">949.75</span><span class="sxs-lookup"><span data-stu-id="8e2ae-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-303">11</span><span class="sxs-lookup"><span data-stu-id="8e2ae-303">11</span></span></td>
<td><span data-ttu-id="8e2ae-304">累计折旧</span><span class="sxs-lookup"><span data-stu-id="8e2ae-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-305">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-306">-949.75</span><span class="sxs-lookup"><span data-stu-id="8e2ae-306">-949.75</span></span></td>
<td><span data-ttu-id="8e2ae-307">-949.75</span><span class="sxs-lookup"><span data-stu-id="8e2ae-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e2ae-308">如上表所示，根据法定申报和 IFRS 申报，需要申报三本帐簿。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="8e2ae-309">法定帐簿根据当前层下基于现金的记帐记录租赁付款。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="8e2ae-310">法定冲销帐簿冲销法定日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="8e2ae-311">IFRS 16 帐簿创建按照 IFRS 16 所需的日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="8e2ae-312">一次只能输入一个租赁。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-312">You must enter a lease only one time.</span></span> <span data-ttu-id="8e2ae-313">然后可以打开 **帐簿** 页以查看与租赁关联的所有帐簿。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="8e2ae-314">创建帐簿时，所有三本帐簿都必须与同一个租赁记录关联。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="8e2ae-315">第一个日记帐条目将租赁费用记录在法定帐簿下。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="8e2ae-316">您可以批量创建付款，也可以通过在法定帐簿中选择付款计划来创建付款。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="8e2ae-317">对于此示例，将从付款计划为法定帐簿生成以下日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="8e2ae-318">租赁付款 – 1/31/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="8e2ae-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="8e2ae-319">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-319">Account type</span></span> | <span data-ttu-id="8e2ae-320">帐号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-320">Account number</span></span> | <span data-ttu-id="8e2ae-321">层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-321">Layer</span></span>   | <span data-ttu-id="8e2ae-322">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-322">Account description</span></span> | <span data-ttu-id="8e2ae-323">借记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-323">Debit</span></span>    | <span data-ttu-id="8e2ae-324">贷记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="8e2ae-325">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-325">Ledger</span></span>       | <span data-ttu-id="8e2ae-326">1</span><span class="sxs-lookup"><span data-stu-id="8e2ae-326">1</span></span>              | <span data-ttu-id="8e2ae-327">当前</span><span class="sxs-lookup"><span data-stu-id="8e2ae-327">Current</span></span> | <span data-ttu-id="8e2ae-328">租赁费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-328">Lease expense</span></span>       | <span data-ttu-id="8e2ae-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-329">1,000.00</span></span> |          |
| <span data-ttu-id="8e2ae-330">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-330">Ledger</span></span>       | <span data-ttu-id="8e2ae-331">4</span><span class="sxs-lookup"><span data-stu-id="8e2ae-331">4</span></span>              | <span data-ttu-id="8e2ae-332">当前</span><span class="sxs-lookup"><span data-stu-id="8e2ae-332">Current</span></span> | <span data-ttu-id="8e2ae-333">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e2ae-333">Clearing account</span></span>    |          | <span data-ttu-id="8e2ae-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-334">1,000.00</span></span> |

<span data-ttu-id="8e2ae-335">应付帐款业务员使用标准 Dynamics 365 功能创建发票以支付资产租赁以外的租赁费用。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="8e2ae-336">但是，应付帐款业务员不是选择 **租赁费用** 作为借方科目，而是选择清算科目以生成以下条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="8e2ae-337">AP 流程 – 1/31/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="8e2ae-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="8e2ae-338">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-338">Account type</span></span> | <span data-ttu-id="8e2ae-339">帐号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-339">Account number</span></span> | <span data-ttu-id="8e2ae-340">层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-340">Layer</span></span>   | <span data-ttu-id="8e2ae-341">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-341">Account description</span></span> | <span data-ttu-id="8e2ae-342">借记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-342">Debit</span></span>    | <span data-ttu-id="8e2ae-343">贷记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="8e2ae-344">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-344">Ledger</span></span>       | <span data-ttu-id="8e2ae-345">4</span><span class="sxs-lookup"><span data-stu-id="8e2ae-345">4</span></span>              | <span data-ttu-id="8e2ae-346">当前</span><span class="sxs-lookup"><span data-stu-id="8e2ae-346">Current</span></span> | <span data-ttu-id="8e2ae-347">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e2ae-347">Clearing account</span></span>    | <span data-ttu-id="8e2ae-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-348">1,000.00</span></span> |          |
| <span data-ttu-id="8e2ae-349">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-349">Ledger</span></span>       | <span data-ttu-id="8e2ae-350">2</span><span class="sxs-lookup"><span data-stu-id="8e2ae-350">2</span></span>              | <span data-ttu-id="8e2ae-351">当前</span><span class="sxs-lookup"><span data-stu-id="8e2ae-351">Current</span></span> | <span data-ttu-id="8e2ae-352">银行手续费</span><span class="sxs-lookup"><span data-stu-id="8e2ae-352">Bank fee</span></span>            | <span data-ttu-id="8e2ae-353">3.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-353">3.00</span></span>     |          |
| <span data-ttu-id="8e2ae-354">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-354">Ledger</span></span>       | <span data-ttu-id="8e2ae-355">3</span><span class="sxs-lookup"><span data-stu-id="8e2ae-355">3</span></span>              | <span data-ttu-id="8e2ae-356">当前</span><span class="sxs-lookup"><span data-stu-id="8e2ae-356">Current</span></span> | <span data-ttu-id="8e2ae-357">增值税费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-357">VAT expense</span></span>         | <span data-ttu-id="8e2ae-358">5.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-358">5.00</span></span>     |          |
| <span data-ttu-id="8e2ae-359">供应商</span><span class="sxs-lookup"><span data-stu-id="8e2ae-359">Vendor</span></span>       | <span data-ttu-id="8e2ae-360">5</span><span class="sxs-lookup"><span data-stu-id="8e2ae-360">5</span></span>              | <span data-ttu-id="8e2ae-361">当前</span><span class="sxs-lookup"><span data-stu-id="8e2ae-361">Current</span></span> | <span data-ttu-id="8e2ae-362">应付帐款</span><span class="sxs-lookup"><span data-stu-id="8e2ae-362">Accounts payable</span></span>    |          | <span data-ttu-id="8e2ae-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-363">1,008.00</span></span> |

<span data-ttu-id="8e2ae-364">将对帐单发给供应商时，请执行常规付款流程。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="8e2ae-365">在此流程中，将生成以下日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="8e2ae-366">现金付款 – 1/31/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="8e2ae-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="8e2ae-367">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-367">Account type</span></span> | <span data-ttu-id="8e2ae-368">帐号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-368">Account number</span></span> | <span data-ttu-id="8e2ae-369">层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-369">Layer</span></span>   | <span data-ttu-id="8e2ae-370">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-370">Account description</span></span> | <span data-ttu-id="8e2ae-371">借记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-371">Debit</span></span>    | <span data-ttu-id="8e2ae-372">贷记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="8e2ae-373">供应商</span><span class="sxs-lookup"><span data-stu-id="8e2ae-373">Vendor</span></span>       | <span data-ttu-id="8e2ae-374">5</span><span class="sxs-lookup"><span data-stu-id="8e2ae-374">5</span></span>              | <span data-ttu-id="8e2ae-375">当前</span><span class="sxs-lookup"><span data-stu-id="8e2ae-375">Current</span></span> | <span data-ttu-id="8e2ae-376">应付帐款</span><span class="sxs-lookup"><span data-stu-id="8e2ae-376">Accounts Payable</span></span>    | <span data-ttu-id="8e2ae-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-377">1,008.00</span></span> |          |
| <span data-ttu-id="8e2ae-378">银行</span><span class="sxs-lookup"><span data-stu-id="8e2ae-378">Bank</span></span>         | <span data-ttu-id="8e2ae-379">9</span><span class="sxs-lookup"><span data-stu-id="8e2ae-379">9</span></span>              | <span data-ttu-id="8e2ae-380">当前</span><span class="sxs-lookup"><span data-stu-id="8e2ae-380">Current</span></span> | <span data-ttu-id="8e2ae-381">现金</span><span class="sxs-lookup"><span data-stu-id="8e2ae-381">Cash</span></span>                |          | <span data-ttu-id="8e2ae-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-382">1,008.00</span></span> |

<span data-ttu-id="8e2ae-383">至此，您已经按照法定申报要求充分考虑了此租赁，因此可以通过使用当前层来生成试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="8e2ae-384">系统将返回包含以下数据的试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="8e2ae-385">帐号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="8e2ae-386">说明</span><span class="sxs-lookup"><span data-stu-id="8e2ae-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="8e2ae-387">法定帐簿（当前层）</span><span class="sxs-lookup"><span data-stu-id="8e2ae-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="8e2ae-388">当前层总计</span><span class="sxs-lookup"><span data-stu-id="8e2ae-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e2ae-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="8e2ae-389">JE-100</span></span></th>
<th><span data-ttu-id="8e2ae-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="8e2ae-390">JE-110</span></span></th>
<th><span data-ttu-id="8e2ae-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="8e2ae-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e2ae-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e2ae-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e2ae-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e2ae-395">1</span><span class="sxs-lookup"><span data-stu-id="8e2ae-395">1</span></span></td>
<td><span data-ttu-id="8e2ae-396">租赁费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-396">Lease expense</span></span></td>
<td><span data-ttu-id="8e2ae-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-399">2</span><span class="sxs-lookup"><span data-stu-id="8e2ae-399">2</span></span></td>
<td><span data-ttu-id="8e2ae-400">银行手续费</span><span class="sxs-lookup"><span data-stu-id="8e2ae-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-401">3.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-402">3.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-403">3</span><span class="sxs-lookup"><span data-stu-id="8e2ae-403">3</span></span></td>
<td><span data-ttu-id="8e2ae-404">增值税费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-405">5.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-406">5.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-407">4</span><span class="sxs-lookup"><span data-stu-id="8e2ae-407">4</span></span></td>
<td><span data-ttu-id="8e2ae-408">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e2ae-408">Clearing account</span></span></td>
<td><span data-ttu-id="8e2ae-409">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-409">-1,000.00</span></span></td>
<td><span data-ttu-id="8e2ae-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-411">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-412">5</span><span class="sxs-lookup"><span data-stu-id="8e2ae-412">5</span></span></td>
<td><span data-ttu-id="8e2ae-413">应付帐款</span><span class="sxs-lookup"><span data-stu-id="8e2ae-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="8e2ae-414">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-414">-1,008.00</span></span></td>
<td><span data-ttu-id="8e2ae-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-415">1,008.00</span></span></td>
<td><span data-ttu-id="8e2ae-416">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-417">6</span><span class="sxs-lookup"><span data-stu-id="8e2ae-417">6</span></span></td>
<td><span data-ttu-id="8e2ae-418">使用权资产</span><span class="sxs-lookup"><span data-stu-id="8e2ae-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-419">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-420">7</span><span class="sxs-lookup"><span data-stu-id="8e2ae-420">7</span></span></td>
<td><span data-ttu-id="8e2ae-421">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e2ae-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-422">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-423">8</span><span class="sxs-lookup"><span data-stu-id="8e2ae-423">8</span></span></td>
<td><span data-ttu-id="8e2ae-424">利息费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-425">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-426">9</span><span class="sxs-lookup"><span data-stu-id="8e2ae-426">9</span></span></td>
<td><span data-ttu-id="8e2ae-427">现金</span><span class="sxs-lookup"><span data-stu-id="8e2ae-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-428">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-428">-1,008.00</span></span></td>
<td><span data-ttu-id="8e2ae-429">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-430">10</span><span class="sxs-lookup"><span data-stu-id="8e2ae-430">10</span></span></td>
<td><span data-ttu-id="8e2ae-431">折旧费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-432">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e2ae-433">11</span><span class="sxs-lookup"><span data-stu-id="8e2ae-433">11</span></span></td>
<td><span data-ttu-id="8e2ae-434">累计折旧</span><span class="sxs-lookup"><span data-stu-id="8e2ae-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e2ae-435">0.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e2ae-436">如果要使用 IFRS 16 数据来运行同一个试算平衡表，则必须冲销法定会计日记帐条目，并且必须过帐 IFRS 16 日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="8e2ae-437">为了冲销法定日记帐条目，此示例中包括一个法定冲销帐簿，该帐簿与法定帐簿具有相同的设置，但相反的过帐配置文件。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="8e2ae-438">例如，法定帐簿 *借记* 租赁费用科目，但冲销帐簿则 *贷记* 此科目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="8e2ae-439">这些关系很容易在 **资产租赁参数** 页面（**资产租赁 \> 设置 \> 资产租赁参数**）中的资产租赁过帐科目中定义。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="8e2ae-440">如果对冲销帐簿使用用于法定帐簿的相同流程，将生成以下日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="8e2ae-441">区别在于冲销帐簿记录法定帐簿中的冲销条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="8e2ae-442">还将为自定义层创建冲销条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="8e2ae-443">在当前层运行试算平衡表时，不包括冲销日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="8e2ae-444">租赁付款 – 1/31/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="8e2ae-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="8e2ae-445">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-445">Account type</span></span> | <span data-ttu-id="8e2ae-446">帐号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-446">Account number</span></span> | <span data-ttu-id="8e2ae-447">层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-447">Layer</span></span>  | <span data-ttu-id="8e2ae-448">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-448">Account description</span></span> | <span data-ttu-id="8e2ae-449">借记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-449">Debit</span></span>    | <span data-ttu-id="8e2ae-450">贷记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="8e2ae-451">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-451">Ledger</span></span>       | <span data-ttu-id="8e2ae-452">4</span><span class="sxs-lookup"><span data-stu-id="8e2ae-452">4</span></span>              | <span data-ttu-id="8e2ae-453">自定义</span><span class="sxs-lookup"><span data-stu-id="8e2ae-453">Custom</span></span> | <span data-ttu-id="8e2ae-454">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e2ae-454">Clearing account</span></span>    | <span data-ttu-id="8e2ae-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-455">1,000.00</span></span> |          |
| <span data-ttu-id="8e2ae-456">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-456">Ledger</span></span>       | <span data-ttu-id="8e2ae-457">1</span><span class="sxs-lookup"><span data-stu-id="8e2ae-457">1</span></span>              | <span data-ttu-id="8e2ae-458">自定义</span><span class="sxs-lookup"><span data-stu-id="8e2ae-458">Custom</span></span> | <span data-ttu-id="8e2ae-459">租赁费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-459">Lease expense</span></span>       |          | <span data-ttu-id="8e2ae-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-460">1,000.00</span></span> |

<span data-ttu-id="8e2ae-461">现在，您已经删除了法定日记帐条目，您将在 IFRS 16 帐簿中预订 IFRS 16 所需的所有日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="8e2ae-462">这些条目包括对 ROU 资产和负债的初始确认，以及利息和折旧的记录。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="8e2ae-463">初始确认 – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="8e2ae-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="8e2ae-464">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-464">Account type</span></span> | <span data-ttu-id="8e2ae-465">帐号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-465">Account number</span></span> | <span data-ttu-id="8e2ae-466">层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-466">Layer</span></span>  | <span data-ttu-id="8e2ae-467">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-467">Account description</span></span>      | <span data-ttu-id="8e2ae-468">借记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-468">Debit</span></span>     | <span data-ttu-id="8e2ae-469">贷记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="8e2ae-470">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-470">Ledger</span></span>       | <span data-ttu-id="8e2ae-471">6</span><span class="sxs-lookup"><span data-stu-id="8e2ae-471">6</span></span>              | <span data-ttu-id="8e2ae-472">自定义</span><span class="sxs-lookup"><span data-stu-id="8e2ae-472">Custom</span></span> | <span data-ttu-id="8e2ae-473">使用权资产</span><span class="sxs-lookup"><span data-stu-id="8e2ae-473">ROU Asset</span></span>                | <span data-ttu-id="8e2ae-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="8e2ae-474">22,793.90</span></span> |           |
| <span data-ttu-id="8e2ae-475">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-475">Ledger</span></span>       | <span data-ttu-id="8e2ae-476">7</span><span class="sxs-lookup"><span data-stu-id="8e2ae-476">7</span></span>              | <span data-ttu-id="8e2ae-477">自定义</span><span class="sxs-lookup"><span data-stu-id="8e2ae-477">Custom</span></span> | <span data-ttu-id="8e2ae-478">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e2ae-478">Finance lease obligation</span></span> |           | <span data-ttu-id="8e2ae-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="8e2ae-479">22,793.90</span></span> |

<span data-ttu-id="8e2ae-480">租赁付款与其他租赁付款一样过帐。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="8e2ae-481">使用清算科目的原因是为了确保只将现金记入一次。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="8e2ae-482">租赁付款 – 1/31/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="8e2ae-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="8e2ae-483">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-483">Account type</span></span> | <span data-ttu-id="8e2ae-484">帐号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-484">Account number</span></span> | <span data-ttu-id="8e2ae-485">层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-485">Layer</span></span>  | <span data-ttu-id="8e2ae-486">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-486">Account description</span></span>      | <span data-ttu-id="8e2ae-487">借记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-487">Debit</span></span>    | <span data-ttu-id="8e2ae-488">贷记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="8e2ae-489">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-489">Ledger</span></span>       | <span data-ttu-id="8e2ae-490">7</span><span class="sxs-lookup"><span data-stu-id="8e2ae-490">7</span></span>              | <span data-ttu-id="8e2ae-491">自定义</span><span class="sxs-lookup"><span data-stu-id="8e2ae-491">Custom</span></span> | <span data-ttu-id="8e2ae-492">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e2ae-492">Finance lease obligation</span></span> | <span data-ttu-id="8e2ae-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-493">1,000.00</span></span> |          |
| <span data-ttu-id="8e2ae-494">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-494">Ledger</span></span>       | <span data-ttu-id="8e2ae-495">4</span><span class="sxs-lookup"><span data-stu-id="8e2ae-495">4</span></span>              | <span data-ttu-id="8e2ae-496">自定义</span><span class="sxs-lookup"><span data-stu-id="8e2ae-496">Custom</span></span> | <span data-ttu-id="8e2ae-497">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e2ae-497">Clearing account</span></span>         |          | <span data-ttu-id="8e2ae-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-498">1,000.00</span></span> |

<span data-ttu-id="8e2ae-499">利息费用日记帐条目从负债摊销计划中生成。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="8e2ae-500">利息费用 – 1/31/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="8e2ae-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="8e2ae-501">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-501">Account type</span></span> | <span data-ttu-id="8e2ae-502">帐号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-502">Account number</span></span> | <span data-ttu-id="8e2ae-503">层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-503">Layer</span></span>  | <span data-ttu-id="8e2ae-504">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-504">Account description</span></span>      | <span data-ttu-id="8e2ae-505">借记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-505">Debit</span></span> | <span data-ttu-id="8e2ae-506">贷记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="8e2ae-507">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-507">Ledger</span></span>       | <span data-ttu-id="8e2ae-508">8</span><span class="sxs-lookup"><span data-stu-id="8e2ae-508">8</span></span>              | <span data-ttu-id="8e2ae-509">自定义</span><span class="sxs-lookup"><span data-stu-id="8e2ae-509">Custom</span></span> | <span data-ttu-id="8e2ae-510">利息费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-510">Interest expense</span></span>         | <span data-ttu-id="8e2ae-511">94.97</span><span class="sxs-lookup"><span data-stu-id="8e2ae-511">94.97</span></span> |        |
| <span data-ttu-id="8e2ae-512">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-512">Ledger</span></span>       | <span data-ttu-id="8e2ae-513">7</span><span class="sxs-lookup"><span data-stu-id="8e2ae-513">7</span></span>              | <span data-ttu-id="8e2ae-514">自定义</span><span class="sxs-lookup"><span data-stu-id="8e2ae-514">Custom</span></span> | <span data-ttu-id="8e2ae-515">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e2ae-515">Finance lease obligation</span></span> |       | <span data-ttu-id="8e2ae-516">94.97</span><span class="sxs-lookup"><span data-stu-id="8e2ae-516">94.97</span></span>  |

<span data-ttu-id="8e2ae-517">折旧费用日记帐条目从资产折旧计划中生成。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="8e2ae-518">折旧费用 – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="8e2ae-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="8e2ae-519">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e2ae-519">Account type</span></span> | <span data-ttu-id="8e2ae-520">帐号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-520">Account number</span></span> | <span data-ttu-id="8e2ae-521">层</span><span class="sxs-lookup"><span data-stu-id="8e2ae-521">Layer</span></span>  | <span data-ttu-id="8e2ae-522">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e2ae-522">Account description</span></span>      | <span data-ttu-id="8e2ae-523">借记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-523">Debit</span></span>  | <span data-ttu-id="8e2ae-524">贷记</span><span class="sxs-lookup"><span data-stu-id="8e2ae-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="8e2ae-525">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-525">Ledger</span></span>       | <span data-ttu-id="8e2ae-526">10</span><span class="sxs-lookup"><span data-stu-id="8e2ae-526">10</span></span>             | <span data-ttu-id="8e2ae-527">自定义</span><span class="sxs-lookup"><span data-stu-id="8e2ae-527">Custom</span></span> | <span data-ttu-id="8e2ae-528">折旧费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-528">Depreciation expense</span></span>     | <span data-ttu-id="8e2ae-529">949.75</span><span class="sxs-lookup"><span data-stu-id="8e2ae-529">949.75</span></span> |        |
| <span data-ttu-id="8e2ae-530">总帐</span><span class="sxs-lookup"><span data-stu-id="8e2ae-530">Ledger</span></span>       | <span data-ttu-id="8e2ae-531">11</span><span class="sxs-lookup"><span data-stu-id="8e2ae-531">11</span></span>             | <span data-ttu-id="8e2ae-532">自定义</span><span class="sxs-lookup"><span data-stu-id="8e2ae-532">Custom</span></span> | <span data-ttu-id="8e2ae-533">累计折旧</span><span class="sxs-lookup"><span data-stu-id="8e2ae-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="8e2ae-534">949.75</span><span class="sxs-lookup"><span data-stu-id="8e2ae-534">949.75</span></span> |

<span data-ttu-id="8e2ae-535">创建并过帐所有这些日记帐条目后，您将看到以下“自定义层 1”值。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="8e2ae-536">请注意，最后一列包括银行手续费、增值税 (VAT) 费用和上一层的现金减少额，但不包括法定申报日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="8e2ae-537">因此，您可以实现真正的双重申报功能。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="8e2ae-538">此时，公司仅需运行其试算平衡表，并将当前层和自定义层结合起来即可创建 IFRS 试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="8e2ae-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="8e2ae-539">科目编号</span><span class="sxs-lookup"><span data-stu-id="8e2ae-539">Account No</span></span> | <span data-ttu-id="8e2ae-540">说明</span><span class="sxs-lookup"><span data-stu-id="8e2ae-540">Description</span></span>              | <span data-ttu-id="8e2ae-541">法定帐簿\-当前层\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e2ae-542">法定帐簿\-当前层\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e2ae-543">法定帐簿\-当前层\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e2ae-544">当前层 \- 总计</span><span class="sxs-lookup"><span data-stu-id="8e2ae-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="8e2ae-545">冲销帐簿\-自定义层\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e2ae-546">IFRS 16 帐簿\-自定义层\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e2ae-547">IFRS 16 帐簿\-自定义层\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e2ae-548">IFRS 16 帐簿\-自定义层\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e2ae-549">IFRS 16 帐簿\-自定义层\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e2ae-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e2ae-550">自定义层 \+ 当前层 \- 总计</span><span class="sxs-lookup"><span data-stu-id="8e2ae-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="8e2ae-551">1</span><span class="sxs-lookup"><span data-stu-id="8e2ae-551">1</span></span>          | <span data-ttu-id="8e2ae-552">租赁费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-552">Lease expense</span></span>            | <span data-ttu-id="8e2ae-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="8e2ae-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-554">1,000\.00</span></span>               |   | <span data-ttu-id="8e2ae-555">\-1,000</span><span class="sxs-lookup"><span data-stu-id="8e2ae-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="8e2ae-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-556">0\.00</span></span>                                   |
| <span data-ttu-id="8e2ae-557">2</span><span class="sxs-lookup"><span data-stu-id="8e2ae-557">2</span></span>          | <span data-ttu-id="8e2ae-558">银行手续费</span><span class="sxs-lookup"><span data-stu-id="8e2ae-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="8e2ae-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="8e2ae-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8e2ae-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-561">3\.00</span></span>                                   |
| <span data-ttu-id="8e2ae-562">3</span><span class="sxs-lookup"><span data-stu-id="8e2ae-562">3</span></span>          | <span data-ttu-id="8e2ae-563">增值税费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="8e2ae-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="8e2ae-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8e2ae-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-566">5\.00</span></span>                                   |
| <span data-ttu-id="8e2ae-567">4</span><span class="sxs-lookup"><span data-stu-id="8e2ae-567">4</span></span>          | <span data-ttu-id="8e2ae-568">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e2ae-568">Clearing account</span></span>         | <span data-ttu-id="8e2ae-569">\-1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="8e2ae-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="8e2ae-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-571">0\.00</span></span>                   |   | <span data-ttu-id="8e2ae-572">1,000</span><span class="sxs-lookup"><span data-stu-id="8e2ae-572">1,000</span></span>                                           |                                                | <span data-ttu-id="8e2ae-573">\-1,000</span><span class="sxs-lookup"><span data-stu-id="8e2ae-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="8e2ae-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-574">0\.00</span></span>                                   |
| <span data-ttu-id="8e2ae-575">5</span><span class="sxs-lookup"><span data-stu-id="8e2ae-575">5</span></span>          | <span data-ttu-id="8e2ae-576">应付帐款</span><span class="sxs-lookup"><span data-stu-id="8e2ae-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="8e2ae-577">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="8e2ae-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-578">1,008\.00</span></span>                                         | <span data-ttu-id="8e2ae-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8e2ae-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-580">0\.00</span></span>                                   |
| <span data-ttu-id="8e2ae-581">6</span><span class="sxs-lookup"><span data-stu-id="8e2ae-581">6</span></span>          | <span data-ttu-id="8e2ae-582">使用权资产</span><span class="sxs-lookup"><span data-stu-id="8e2ae-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="8e2ae-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="8e2ae-584">22,794</span><span class="sxs-lookup"><span data-stu-id="8e2ae-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="8e2ae-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="8e2ae-585">22,793\.90</span></span>                              |
| <span data-ttu-id="8e2ae-586">7</span><span class="sxs-lookup"><span data-stu-id="8e2ae-586">7</span></span>          | <span data-ttu-id="8e2ae-587">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e2ae-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="8e2ae-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="8e2ae-589">\-22,794</span><span class="sxs-lookup"><span data-stu-id="8e2ae-589">\-22,794</span></span>                                       | <span data-ttu-id="8e2ae-590">1,000</span><span class="sxs-lookup"><span data-stu-id="8e2ae-590">1,000</span></span>                                          | <span data-ttu-id="8e2ae-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="8e2ae-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="8e2ae-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="8e2ae-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="8e2ae-593">8</span><span class="sxs-lookup"><span data-stu-id="8e2ae-593">8</span></span>          | <span data-ttu-id="8e2ae-594">利息费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="8e2ae-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="8e2ae-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="8e2ae-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="8e2ae-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="8e2ae-597">94\.97</span></span>                                  |
| <span data-ttu-id="8e2ae-598">9</span><span class="sxs-lookup"><span data-stu-id="8e2ae-598">9</span></span>          | <span data-ttu-id="8e2ae-599">现金</span><span class="sxs-lookup"><span data-stu-id="8e2ae-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="8e2ae-600">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="8e2ae-601">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8e2ae-602">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="8e2ae-603">10</span><span class="sxs-lookup"><span data-stu-id="8e2ae-603">10</span></span>         | <span data-ttu-id="8e2ae-604">折旧费用</span><span class="sxs-lookup"><span data-stu-id="8e2ae-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="8e2ae-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="8e2ae-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="8e2ae-606">949\.75</span></span>                                        | <span data-ttu-id="8e2ae-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="8e2ae-607">949\.75</span></span>                                 |
| <span data-ttu-id="8e2ae-608">11</span><span class="sxs-lookup"><span data-stu-id="8e2ae-608">11</span></span>         | <span data-ttu-id="8e2ae-609">累计折旧</span><span class="sxs-lookup"><span data-stu-id="8e2ae-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="8e2ae-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e2ae-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="8e2ae-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="8e2ae-611">\-949\.75</span></span>                                      | <span data-ttu-id="8e2ae-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="8e2ae-612">\-949\.75</span></span>                               |


