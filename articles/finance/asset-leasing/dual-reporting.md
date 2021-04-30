---
title: 双重申报
description: 本主题通过一个示例指导您如何在资产租赁中同时满足国际财务申报标准 (IFRS) 申报和法定申报的要求。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseBookMaster
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 86f42f8db707f3b8c62b9ec4c39ad6464f080748
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881148"
---
# <a name="dual-reporting"></a><span data-ttu-id="8e9b1-103">双重申报</span><span class="sxs-lookup"><span data-stu-id="8e9b1-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8e9b1-104">本主题通过一个示例指导您如何在资产租赁中同时满足国际财务申报标准 (IFRS) 申报和法定申报的要求。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="8e9b1-105">需要熟悉 Microsoft Dynamics 365 Finance中的过帐层，这一可以让示例更容易理解。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="8e9b1-106">示例</span><span class="sxs-lookup"><span data-stu-id="8e9b1-106">Example</span></span>

<span data-ttu-id="8e9b1-107">以下示例使用现金基础法和 IFRS 申报法介绍意大利法定申报下的租赁。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="8e9b1-108">公司必须建立三本帐簿，以同时满足意大利的法定要求和 IFRS 16 的要求。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="8e9b1-109">IFRS 16 需要一本帐簿，法规要求需要一本帐簿，并且还需要一本帐簿来自动撤消法定过帐。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="8e9b1-110">下面的表中显示了这些帐簿的设置。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="8e9b1-111">**IFRS 16 帐簿**</span><span class="sxs-lookup"><span data-stu-id="8e9b1-111">**IFRS 16 book**</span></span>

<span data-ttu-id="8e9b1-112">IFRS 16 帐簿设置为遵守 IFRS 16 会计标准。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="8e9b1-113">此帐簿中过帐的所有条目都将过帐到自定义层。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="8e9b1-114">姓名</span><span class="sxs-lookup"><span data-stu-id="8e9b1-114">Name</span></span>                                    | <span data-ttu-id="8e9b1-115">说明</span><span class="sxs-lookup"><span data-stu-id="8e9b1-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="8e9b1-116">帐簿类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-116">Book type</span></span>                               | <span data-ttu-id="8e9b1-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="8e9b1-117">IFRS 16</span></span>        |
| <span data-ttu-id="8e9b1-118">帐簿描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-118">Book description</span></span>                        | <span data-ttu-id="8e9b1-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="8e9b1-119">IFRS 16</span></span>        |
| <span data-ttu-id="8e9b1-120">过帐层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-120">Posting Layer</span></span>                           | <span data-ttu-id="8e9b1-121">自定义层 1</span><span class="sxs-lookup"><span data-stu-id="8e9b1-121">Custom layer 1</span></span> |
| <span data-ttu-id="8e9b1-122">租赁类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-122">Lease Type</span></span>                              | <span data-ttu-id="8e9b1-123">Finance</span><span class="sxs-lookup"><span data-stu-id="8e9b1-123">Finance</span></span>        |
| <span data-ttu-id="8e9b1-124">会计框架</span><span class="sxs-lookup"><span data-stu-id="8e9b1-124">Accounting Framework</span></span>                    | <span data-ttu-id="8e9b1-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="8e9b1-125">IFRS 16</span></span>        |
| <span data-ttu-id="8e9b1-126">租赁期/使用年限设置</span><span class="sxs-lookup"><span data-stu-id="8e9b1-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="8e9b1-127">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-127">0.00</span></span>           |
| <span data-ttu-id="8e9b1-128">现值/资产的公平价值设置</span><span class="sxs-lookup"><span data-stu-id="8e9b1-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="8e9b1-129">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-129">0.00</span></span>           |
| <span data-ttu-id="8e9b1-130">短期阈值</span><span class="sxs-lookup"><span data-stu-id="8e9b1-130">Short-term threshold</span></span>                    | <span data-ttu-id="8e9b1-131">12</span><span class="sxs-lookup"><span data-stu-id="8e9b1-131">12</span></span>             |
| <span data-ttu-id="8e9b1-132">低价值阈值</span><span class="sxs-lookup"><span data-stu-id="8e9b1-132">Low Value Threshold</span></span>                     | <span data-ttu-id="8e9b1-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-133">5,000.00</span></span>       |
| <span data-ttu-id="8e9b1-134">向供应商付款</span><span class="sxs-lookup"><span data-stu-id="8e9b1-134">Pay to Vendor</span></span>                           | <span data-ttu-id="8e9b1-135">不</span><span class="sxs-lookup"><span data-stu-id="8e9b1-135">No</span></span>             |

<span data-ttu-id="8e9b1-136">**法定帐簿**</span><span class="sxs-lookup"><span data-stu-id="8e9b1-136">**Statutory book**</span></span>

<span data-ttu-id="8e9b1-137">法定帐簿是一种现金基础帐簿，在这种帐簿中，公司将把租赁费用作为每月支付的租金现金金额入帐。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="8e9b1-138">这种帐簿不会产生使用权 (ROU) 资产或租赁负债。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="8e9b1-139">姓名</span><span class="sxs-lookup"><span data-stu-id="8e9b1-139">Name</span></span>                                    | <span data-ttu-id="8e9b1-140">说明</span><span class="sxs-lookup"><span data-stu-id="8e9b1-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="8e9b1-141">帐簿类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-141">Book type</span></span>                               | <span data-ttu-id="8e9b1-142">法定</span><span class="sxs-lookup"><span data-stu-id="8e9b1-142">Statutory</span></span>   |
| <span data-ttu-id="8e9b1-143">帐簿描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-143">Book description</span></span>                        | <span data-ttu-id="8e9b1-144">本地 GAAP</span><span class="sxs-lookup"><span data-stu-id="8e9b1-144">Local GAAP</span></span>  |
| <span data-ttu-id="8e9b1-145">过帐层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-145">Posting Layer</span></span>                           | <span data-ttu-id="8e9b1-146">当前</span><span class="sxs-lookup"><span data-stu-id="8e9b1-146">Current</span></span>     |
| <span data-ttu-id="8e9b1-147">租赁类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-147">Lease Type</span></span>                              | <span data-ttu-id="8e9b1-148">自动</span><span class="sxs-lookup"><span data-stu-id="8e9b1-148">Automatic</span></span>   |
| <span data-ttu-id="8e9b1-149">会计框架</span><span class="sxs-lookup"><span data-stu-id="8e9b1-149">Accounting Framework</span></span>                    | <span data-ttu-id="8e9b1-150">现金基数</span><span class="sxs-lookup"><span data-stu-id="8e9b1-150">Cash basis</span></span>  |
| <span data-ttu-id="8e9b1-151">租赁期/使用年限设置</span><span class="sxs-lookup"><span data-stu-id="8e9b1-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="8e9b1-152">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-152">0.00</span></span>        |
| <span data-ttu-id="8e9b1-153">现值/资产的公平价值设置</span><span class="sxs-lookup"><span data-stu-id="8e9b1-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="8e9b1-154">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-154">0.00</span></span>        |
| <span data-ttu-id="8e9b1-155">短期阈值</span><span class="sxs-lookup"><span data-stu-id="8e9b1-155">Short-term threshold</span></span>                    | <span data-ttu-id="8e9b1-156">0</span><span class="sxs-lookup"><span data-stu-id="8e9b1-156">0</span></span>           |
| <span data-ttu-id="8e9b1-157">低价值阈值</span><span class="sxs-lookup"><span data-stu-id="8e9b1-157">Low Value Threshold</span></span>                     | <span data-ttu-id="8e9b1-158">0</span><span class="sxs-lookup"><span data-stu-id="8e9b1-158">0</span></span>           |
| <span data-ttu-id="8e9b1-159">向供应商付款</span><span class="sxs-lookup"><span data-stu-id="8e9b1-159">Pay to Vendor</span></span>                           | <span data-ttu-id="8e9b1-160">不</span><span class="sxs-lookup"><span data-stu-id="8e9b1-160">No</span></span>          |

<span data-ttu-id="8e9b1-161">**法定冲销帐簿**</span><span class="sxs-lookup"><span data-stu-id="8e9b1-161">**Statutory reversal book**</span></span>

<span data-ttu-id="8e9b1-162">法定冲销帐簿的建立方式与法定帐簿相同。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="8e9b1-163">姓名</span><span class="sxs-lookup"><span data-stu-id="8e9b1-163">Name</span></span>                                    | <span data-ttu-id="8e9b1-164">说明</span><span class="sxs-lookup"><span data-stu-id="8e9b1-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="8e9b1-165">帐簿类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-165">Book type</span></span>                               | <span data-ttu-id="8e9b1-166">法定 – 冲销</span><span class="sxs-lookup"><span data-stu-id="8e9b1-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="8e9b1-167">帐簿描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-167">Book description</span></span>                        | <span data-ttu-id="8e9b1-168">用于冲销法定帐簿的帐簿</span><span class="sxs-lookup"><span data-stu-id="8e9b1-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="8e9b1-169">过帐层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-169">Posting Layer</span></span>                           | <span data-ttu-id="8e9b1-170">自定义层 1</span><span class="sxs-lookup"><span data-stu-id="8e9b1-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="8e9b1-171">租赁类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-171">Lease Type</span></span>                              | <span data-ttu-id="8e9b1-172">自动</span><span class="sxs-lookup"><span data-stu-id="8e9b1-172">Automatic</span></span>                      |
| <span data-ttu-id="8e9b1-173">会计框架</span><span class="sxs-lookup"><span data-stu-id="8e9b1-173">Accounting Framework</span></span>                    | <span data-ttu-id="8e9b1-174">现金基数</span><span class="sxs-lookup"><span data-stu-id="8e9b1-174">Cash basis</span></span>                     |
| <span data-ttu-id="8e9b1-175">租赁期/使用年限设置</span><span class="sxs-lookup"><span data-stu-id="8e9b1-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="8e9b1-176">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-176">0.00</span></span>                           |
| <span data-ttu-id="8e9b1-177">现值/资产的公平价值设置</span><span class="sxs-lookup"><span data-stu-id="8e9b1-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="8e9b1-178">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-178">0.00</span></span>                           |
| <span data-ttu-id="8e9b1-179">短期阈值</span><span class="sxs-lookup"><span data-stu-id="8e9b1-179">Short-term threshold</span></span>                    | <span data-ttu-id="8e9b1-180">0</span><span class="sxs-lookup"><span data-stu-id="8e9b1-180">0</span></span>                              |
| <span data-ttu-id="8e9b1-181">低价值阈值</span><span class="sxs-lookup"><span data-stu-id="8e9b1-181">Low Value Threshold</span></span>                     | <span data-ttu-id="8e9b1-182">0</span><span class="sxs-lookup"><span data-stu-id="8e9b1-182">0</span></span>                              |
| <span data-ttu-id="8e9b1-183">向供应商付款</span><span class="sxs-lookup"><span data-stu-id="8e9b1-183">Pay to Vendor</span></span>                           | <span data-ttu-id="8e9b1-184">不</span><span class="sxs-lookup"><span data-stu-id="8e9b1-184">No</span></span>                             |

<span data-ttu-id="8e9b1-185">在此示例中，创建了一个租赁，该租赁在 **常规** 和 **付款计划行** 选项卡上的设置如下。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="8e9b1-186">**常规选项卡**</span><span class="sxs-lookup"><span data-stu-id="8e9b1-186">**General tab**</span></span>

| <span data-ttu-id="8e9b1-187">字段</span><span class="sxs-lookup"><span data-stu-id="8e9b1-187">Field</span></span>                      | <span data-ttu-id="8e9b1-188">值</span><span class="sxs-lookup"><span data-stu-id="8e9b1-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="8e9b1-189">增量借贷利率</span><span class="sxs-lookup"><span data-stu-id="8e9b1-189">Incremental borrowing rate</span></span> | <span data-ttu-id="8e9b1-190">5%</span><span class="sxs-lookup"><span data-stu-id="8e9b1-190">5%</span></span>               |
| <span data-ttu-id="8e9b1-191">开始日期</span><span class="sxs-lookup"><span data-stu-id="8e9b1-191">Commencement date</span></span>          | <span data-ttu-id="8e9b1-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="8e9b1-192">1/1/2020</span></span>         |
| <span data-ttu-id="8e9b1-193">租赁组</span><span class="sxs-lookup"><span data-stu-id="8e9b1-193">Lease group</span></span>                | <span data-ttu-id="8e9b1-194">建筑物</span><span class="sxs-lookup"><span data-stu-id="8e9b1-194">Buildings</span></span>        |
| <span data-ttu-id="8e9b1-195">供应商</span><span class="sxs-lookup"><span data-stu-id="8e9b1-195">Vendor</span></span>                     | <span data-ttu-id="8e9b1-196">1001</span><span class="sxs-lookup"><span data-stu-id="8e9b1-196">1001</span></span>             |
| <span data-ttu-id="8e9b1-197">资产的公平价值</span><span class="sxs-lookup"><span data-stu-id="8e9b1-197">Fair value of the asset</span></span>    | <span data-ttu-id="8e9b1-198">245,000</span><span class="sxs-lookup"><span data-stu-id="8e9b1-198">245,000</span></span>          |
| <span data-ttu-id="8e9b1-199">资产使用年限</span><span class="sxs-lookup"><span data-stu-id="8e9b1-199">Asset useful life</span></span>          | <span data-ttu-id="8e9b1-200">120</span><span class="sxs-lookup"><span data-stu-id="8e9b1-200">120</span></span>              |
| <span data-ttu-id="8e9b1-201">年金类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-201">Annuity type</span></span>               | <span data-ttu-id="8e9b1-202">普通年金</span><span class="sxs-lookup"><span data-stu-id="8e9b1-202">Ordinary annuity</span></span> |
| <span data-ttu-id="8e9b1-203">复合间隔</span><span class="sxs-lookup"><span data-stu-id="8e9b1-203">Compounding interval</span></span>       | <span data-ttu-id="8e9b1-204">月度</span><span class="sxs-lookup"><span data-stu-id="8e9b1-204">Monthly</span></span>          |

<span data-ttu-id="8e9b1-205">**付款计划行选项卡**</span><span class="sxs-lookup"><span data-stu-id="8e9b1-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="8e9b1-206">字段</span><span class="sxs-lookup"><span data-stu-id="8e9b1-206">Field</span></span>             | <span data-ttu-id="8e9b1-207">值</span><span class="sxs-lookup"><span data-stu-id="8e9b1-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="8e9b1-208">开始日期</span><span class="sxs-lookup"><span data-stu-id="8e9b1-208">Start date</span></span>        | <span data-ttu-id="8e9b1-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="8e9b1-209">1/1/2020</span></span>   |
| <span data-ttu-id="8e9b1-210">期间间隔</span><span class="sxs-lookup"><span data-stu-id="8e9b1-210">Period interval</span></span>   | <span data-ttu-id="8e9b1-211">月数</span><span class="sxs-lookup"><span data-stu-id="8e9b1-211">Months</span></span>     |
| <span data-ttu-id="8e9b1-212">期间</span><span class="sxs-lookup"><span data-stu-id="8e9b1-212">Periods</span></span>           | <span data-ttu-id="8e9b1-213">24</span><span class="sxs-lookup"><span data-stu-id="8e9b1-213">24</span></span>         |
| <span data-ttu-id="8e9b1-214">结束日期</span><span class="sxs-lookup"><span data-stu-id="8e9b1-214">End date</span></span>          | <span data-ttu-id="8e9b1-215">12/31/2020</span><span class="sxs-lookup"><span data-stu-id="8e9b1-215">12/31/2020</span></span> |
| <span data-ttu-id="8e9b1-216">付款频率</span><span class="sxs-lookup"><span data-stu-id="8e9b1-216">Payment frequency</span></span> | <span data-ttu-id="8e9b1-217">月度</span><span class="sxs-lookup"><span data-stu-id="8e9b1-217">Monthly</span></span>    |
| <span data-ttu-id="8e9b1-218">付款金额</span><span class="sxs-lookup"><span data-stu-id="8e9b1-218">Payment amount</span></span>    | <span data-ttu-id="8e9b1-219">1,000</span><span class="sxs-lookup"><span data-stu-id="8e9b1-219">1,000</span></span>      |

<span data-ttu-id="8e9b1-220">要在两个框架下考虑此租赁，请使用当前过帐层和自定义过帐层。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="8e9b1-221">下表显示了各种申报标准下公平地代表财务状况所需的每个日记帐条目的示例。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="8e9b1-222">后面提供了租赁首月各日记帐条目的详细说明。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="8e9b1-223">帐号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="8e9b1-224">说明</span><span class="sxs-lookup"><span data-stu-id="8e9b1-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="8e9b1-225">法定帐簿（当前层）</span><span class="sxs-lookup"><span data-stu-id="8e9b1-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="8e9b1-226">当前层总计</span><span class="sxs-lookup"><span data-stu-id="8e9b1-226">Current layer total</span></span></th>
<th><span data-ttu-id="8e9b1-227">冲销帐簿（自定义层）</span><span class="sxs-lookup"><span data-stu-id="8e9b1-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="8e9b1-228">IFRS 16 帐簿（自定义层）</span><span class="sxs-lookup"><span data-stu-id="8e9b1-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="8e9b1-229">当前层 + 自定义层总计</span><span class="sxs-lookup"><span data-stu-id="8e9b1-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e9b1-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="8e9b1-230">JE-100</span></span></th>
<th><span data-ttu-id="8e9b1-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="8e9b1-231">JE-110</span></span></th>
<th><span data-ttu-id="8e9b1-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="8e9b1-232">JE-120</span></span></th>
<th><span data-ttu-id="8e9b1-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="8e9b1-233">JE-130</span></span></th>
<th><span data-ttu-id="8e9b1-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="8e9b1-234">JE-140</span></span></th>
<th><span data-ttu-id="8e9b1-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="8e9b1-235">JE-150</span></span></th>
<th><span data-ttu-id="8e9b1-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="8e9b1-236">JE-160</span></span></th>
<th><span data-ttu-id="8e9b1-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="8e9b1-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e9b1-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e9b1-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e9b1-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e9b1-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e9b1-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e9b1-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e9b1-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e9b1-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e9b1-246">1</span><span class="sxs-lookup"><span data-stu-id="8e9b1-246">1</span></span></td>
<td><span data-ttu-id="8e9b1-247">租赁费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-247">Lease expense</span></span></td>
<td><span data-ttu-id="8e9b1-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-249">1,000.00</span></span></td>
<td><span data-ttu-id="8e9b1-250">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-251">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-252">2</span><span class="sxs-lookup"><span data-stu-id="8e9b1-252">2</span></span></td>
<td><span data-ttu-id="8e9b1-253">银行手续费</span><span class="sxs-lookup"><span data-stu-id="8e9b1-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-254">3.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-255">3.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-256">3.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-257">3</span><span class="sxs-lookup"><span data-stu-id="8e9b1-257">3</span></span></td>
<td><span data-ttu-id="8e9b1-258">增值税费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-259">5.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-260">5.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-261">5.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-262">4</span><span class="sxs-lookup"><span data-stu-id="8e9b1-262">4</span></span></td>
<td><span data-ttu-id="8e9b1-263">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e9b1-263">Clearing account</span></span></td>
<td><span data-ttu-id="8e9b1-264">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-264">-1,000.00</span></span></td>
<td><span data-ttu-id="8e9b1-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-266">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-266">0.00</span></span></td>
<td><span data-ttu-id="8e9b1-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-268">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-269">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-270">5</span><span class="sxs-lookup"><span data-stu-id="8e9b1-270">5</span></span></td>
<td><span data-ttu-id="8e9b1-271">应付帐款</span><span class="sxs-lookup"><span data-stu-id="8e9b1-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-272">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-272">-1,008.00</span></span></td>
<td><span data-ttu-id="8e9b1-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-273">1,008.00</span></span></td>
<td><span data-ttu-id="8e9b1-274">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-275">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-276">6</span><span class="sxs-lookup"><span data-stu-id="8e9b1-276">6</span></span></td>
<td><span data-ttu-id="8e9b1-277">使用权资产</span><span class="sxs-lookup"><span data-stu-id="8e9b1-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-278">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="8e9b1-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-281">7</span><span class="sxs-lookup"><span data-stu-id="8e9b1-281">7</span></span></td>
<td><span data-ttu-id="8e9b1-282">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e9b1-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-283">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-284">-22,794.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-284">-22,794.00</span></span></td>
<td><span data-ttu-id="8e9b1-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-285">1,000.00</span></span></td>
<td><span data-ttu-id="8e9b1-286">-94.97</span><span class="sxs-lookup"><span data-stu-id="8e9b1-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-287">-21,888.87</span><span class="sxs-lookup"><span data-stu-id="8e9b1-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-288">8</span><span class="sxs-lookup"><span data-stu-id="8e9b1-288">8</span></span></td>
<td><span data-ttu-id="8e9b1-289">利息费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-290">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-291">94.97</span><span class="sxs-lookup"><span data-stu-id="8e9b1-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-292">94.97</span><span class="sxs-lookup"><span data-stu-id="8e9b1-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-293">9</span><span class="sxs-lookup"><span data-stu-id="8e9b1-293">9</span></span></td>
<td><span data-ttu-id="8e9b1-294">现金</span><span class="sxs-lookup"><span data-stu-id="8e9b1-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-295">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-295">-1,008.00</span></span></td>
<td><span data-ttu-id="8e9b1-296">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-297">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-298">10</span><span class="sxs-lookup"><span data-stu-id="8e9b1-298">10</span></span></td>
<td><span data-ttu-id="8e9b1-299">折旧费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-300">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-301">949.75</span><span class="sxs-lookup"><span data-stu-id="8e9b1-301">949.75</span></span></td>
<td><span data-ttu-id="8e9b1-302">949.75</span><span class="sxs-lookup"><span data-stu-id="8e9b1-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-303">11</span><span class="sxs-lookup"><span data-stu-id="8e9b1-303">11</span></span></td>
<td><span data-ttu-id="8e9b1-304">累计折旧</span><span class="sxs-lookup"><span data-stu-id="8e9b1-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-305">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-306">-949.75</span><span class="sxs-lookup"><span data-stu-id="8e9b1-306">-949.75</span></span></td>
<td><span data-ttu-id="8e9b1-307">-949.75</span><span class="sxs-lookup"><span data-stu-id="8e9b1-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e9b1-308">如上表所示，根据法定申报和 IFRS 申报，需要申报三本帐簿。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="8e9b1-309">法定帐簿根据当前层下基于现金的记帐记录租赁付款。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="8e9b1-310">法定冲销帐簿冲销法定日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="8e9b1-311">IFRS 16 帐簿创建按照 IFRS 16 所需的日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="8e9b1-312">一次只能输入一个租赁。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-312">You must enter a lease only one time.</span></span> <span data-ttu-id="8e9b1-313">然后可以打开 **帐簿** 页以查看与租赁关联的所有帐簿。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="8e9b1-314">创建帐簿时，所有三本帐簿都必须与同一个租赁记录关联。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="8e9b1-315">第一个日记帐条目将租赁费用记录在法定帐簿下。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="8e9b1-316">您可以批量创建付款，也可以通过在法定帐簿中选择付款计划来创建付款。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="8e9b1-317">对于此示例，将从付款计划为法定帐簿生成以下日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="8e9b1-318">租赁付款 – 1/31/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="8e9b1-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="8e9b1-319">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-319">Account type</span></span> | <span data-ttu-id="8e9b1-320">帐号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-320">Account number</span></span> | <span data-ttu-id="8e9b1-321">层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-321">Layer</span></span>   | <span data-ttu-id="8e9b1-322">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-322">Account description</span></span> | <span data-ttu-id="8e9b1-323">借记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-323">Debit</span></span>    | <span data-ttu-id="8e9b1-324">贷记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="8e9b1-325">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-325">Ledger</span></span>       | <span data-ttu-id="8e9b1-326">1</span><span class="sxs-lookup"><span data-stu-id="8e9b1-326">1</span></span>              | <span data-ttu-id="8e9b1-327">当前</span><span class="sxs-lookup"><span data-stu-id="8e9b1-327">Current</span></span> | <span data-ttu-id="8e9b1-328">租赁费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-328">Lease expense</span></span>       | <span data-ttu-id="8e9b1-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-329">1,000.00</span></span> |          |
| <span data-ttu-id="8e9b1-330">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-330">Ledger</span></span>       | <span data-ttu-id="8e9b1-331">4</span><span class="sxs-lookup"><span data-stu-id="8e9b1-331">4</span></span>              | <span data-ttu-id="8e9b1-332">当前</span><span class="sxs-lookup"><span data-stu-id="8e9b1-332">Current</span></span> | <span data-ttu-id="8e9b1-333">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e9b1-333">Clearing account</span></span>    |          | <span data-ttu-id="8e9b1-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-334">1,000.00</span></span> |

<span data-ttu-id="8e9b1-335">应付帐款业务员使用标准 Dynamics 365 功能创建发票以支付资产租赁以外的租赁费用。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="8e9b1-336">但是，应付帐款业务员不是选择 **租赁费用** 作为借方科目，而是选择清算科目以生成以下条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="8e9b1-337">AP 流程 – 1/31/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="8e9b1-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="8e9b1-338">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-338">Account type</span></span> | <span data-ttu-id="8e9b1-339">帐号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-339">Account number</span></span> | <span data-ttu-id="8e9b1-340">层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-340">Layer</span></span>   | <span data-ttu-id="8e9b1-341">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-341">Account description</span></span> | <span data-ttu-id="8e9b1-342">借记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-342">Debit</span></span>    | <span data-ttu-id="8e9b1-343">贷记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="8e9b1-344">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-344">Ledger</span></span>       | <span data-ttu-id="8e9b1-345">4</span><span class="sxs-lookup"><span data-stu-id="8e9b1-345">4</span></span>              | <span data-ttu-id="8e9b1-346">当前</span><span class="sxs-lookup"><span data-stu-id="8e9b1-346">Current</span></span> | <span data-ttu-id="8e9b1-347">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e9b1-347">Clearing account</span></span>    | <span data-ttu-id="8e9b1-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-348">1,000.00</span></span> |          |
| <span data-ttu-id="8e9b1-349">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-349">Ledger</span></span>       | <span data-ttu-id="8e9b1-350">2</span><span class="sxs-lookup"><span data-stu-id="8e9b1-350">2</span></span>              | <span data-ttu-id="8e9b1-351">当前</span><span class="sxs-lookup"><span data-stu-id="8e9b1-351">Current</span></span> | <span data-ttu-id="8e9b1-352">银行手续费</span><span class="sxs-lookup"><span data-stu-id="8e9b1-352">Bank fee</span></span>            | <span data-ttu-id="8e9b1-353">3.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-353">3.00</span></span>     |          |
| <span data-ttu-id="8e9b1-354">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-354">Ledger</span></span>       | <span data-ttu-id="8e9b1-355">3</span><span class="sxs-lookup"><span data-stu-id="8e9b1-355">3</span></span>              | <span data-ttu-id="8e9b1-356">当前</span><span class="sxs-lookup"><span data-stu-id="8e9b1-356">Current</span></span> | <span data-ttu-id="8e9b1-357">增值税费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-357">VAT expense</span></span>         | <span data-ttu-id="8e9b1-358">5.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-358">5.00</span></span>     |          |
| <span data-ttu-id="8e9b1-359">供应商</span><span class="sxs-lookup"><span data-stu-id="8e9b1-359">Vendor</span></span>       | <span data-ttu-id="8e9b1-360">5</span><span class="sxs-lookup"><span data-stu-id="8e9b1-360">5</span></span>              | <span data-ttu-id="8e9b1-361">当前</span><span class="sxs-lookup"><span data-stu-id="8e9b1-361">Current</span></span> | <span data-ttu-id="8e9b1-362">应付帐款</span><span class="sxs-lookup"><span data-stu-id="8e9b1-362">Accounts payable</span></span>    |          | <span data-ttu-id="8e9b1-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-363">1,008.00</span></span> |

<span data-ttu-id="8e9b1-364">将对帐单发给供应商时，请执行常规付款流程。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="8e9b1-365">在此流程中，将生成以下日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="8e9b1-366">现金付款 – 1/31/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="8e9b1-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="8e9b1-367">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-367">Account type</span></span> | <span data-ttu-id="8e9b1-368">帐号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-368">Account number</span></span> | <span data-ttu-id="8e9b1-369">层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-369">Layer</span></span>   | <span data-ttu-id="8e9b1-370">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-370">Account description</span></span> | <span data-ttu-id="8e9b1-371">借记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-371">Debit</span></span>    | <span data-ttu-id="8e9b1-372">贷记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="8e9b1-373">供应商</span><span class="sxs-lookup"><span data-stu-id="8e9b1-373">Vendor</span></span>       | <span data-ttu-id="8e9b1-374">5</span><span class="sxs-lookup"><span data-stu-id="8e9b1-374">5</span></span>              | <span data-ttu-id="8e9b1-375">当前</span><span class="sxs-lookup"><span data-stu-id="8e9b1-375">Current</span></span> | <span data-ttu-id="8e9b1-376">应付帐款</span><span class="sxs-lookup"><span data-stu-id="8e9b1-376">Accounts Payable</span></span>    | <span data-ttu-id="8e9b1-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-377">1,008.00</span></span> |          |
| <span data-ttu-id="8e9b1-378">银行</span><span class="sxs-lookup"><span data-stu-id="8e9b1-378">Bank</span></span>         | <span data-ttu-id="8e9b1-379">9</span><span class="sxs-lookup"><span data-stu-id="8e9b1-379">9</span></span>              | <span data-ttu-id="8e9b1-380">当前</span><span class="sxs-lookup"><span data-stu-id="8e9b1-380">Current</span></span> | <span data-ttu-id="8e9b1-381">现金</span><span class="sxs-lookup"><span data-stu-id="8e9b1-381">Cash</span></span>                |          | <span data-ttu-id="8e9b1-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-382">1,008.00</span></span> |

<span data-ttu-id="8e9b1-383">至此，您已经按照法定申报要求充分考虑了此租赁，因此可以通过使用当前层来生成试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="8e9b1-384">系统将返回包含以下数据的试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="8e9b1-385">帐号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="8e9b1-386">说明</span><span class="sxs-lookup"><span data-stu-id="8e9b1-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="8e9b1-387">法定帐簿（当前层）</span><span class="sxs-lookup"><span data-stu-id="8e9b1-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="8e9b1-388">当前层总计</span><span class="sxs-lookup"><span data-stu-id="8e9b1-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e9b1-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="8e9b1-389">JE-100</span></span></th>
<th><span data-ttu-id="8e9b1-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="8e9b1-390">JE-110</span></span></th>
<th><span data-ttu-id="8e9b1-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="8e9b1-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e9b1-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e9b1-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="8e9b1-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e9b1-395">1</span><span class="sxs-lookup"><span data-stu-id="8e9b1-395">1</span></span></td>
<td><span data-ttu-id="8e9b1-396">租赁费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-396">Lease expense</span></span></td>
<td><span data-ttu-id="8e9b1-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-399">2</span><span class="sxs-lookup"><span data-stu-id="8e9b1-399">2</span></span></td>
<td><span data-ttu-id="8e9b1-400">银行手续费</span><span class="sxs-lookup"><span data-stu-id="8e9b1-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-401">3.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-402">3.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-403">3</span><span class="sxs-lookup"><span data-stu-id="8e9b1-403">3</span></span></td>
<td><span data-ttu-id="8e9b1-404">增值税费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-405">5.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-406">5.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-407">4</span><span class="sxs-lookup"><span data-stu-id="8e9b1-407">4</span></span></td>
<td><span data-ttu-id="8e9b1-408">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e9b1-408">Clearing account</span></span></td>
<td><span data-ttu-id="8e9b1-409">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-409">-1,000.00</span></span></td>
<td><span data-ttu-id="8e9b1-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-411">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-412">5</span><span class="sxs-lookup"><span data-stu-id="8e9b1-412">5</span></span></td>
<td><span data-ttu-id="8e9b1-413">应付帐款</span><span class="sxs-lookup"><span data-stu-id="8e9b1-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="8e9b1-414">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-414">-1,008.00</span></span></td>
<td><span data-ttu-id="8e9b1-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-415">1,008.00</span></span></td>
<td><span data-ttu-id="8e9b1-416">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-417">6</span><span class="sxs-lookup"><span data-stu-id="8e9b1-417">6</span></span></td>
<td><span data-ttu-id="8e9b1-418">使用权资产</span><span class="sxs-lookup"><span data-stu-id="8e9b1-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-419">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-420">7</span><span class="sxs-lookup"><span data-stu-id="8e9b1-420">7</span></span></td>
<td><span data-ttu-id="8e9b1-421">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e9b1-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-422">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-423">8</span><span class="sxs-lookup"><span data-stu-id="8e9b1-423">8</span></span></td>
<td><span data-ttu-id="8e9b1-424">利息费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-425">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-426">9</span><span class="sxs-lookup"><span data-stu-id="8e9b1-426">9</span></span></td>
<td><span data-ttu-id="8e9b1-427">现金</span><span class="sxs-lookup"><span data-stu-id="8e9b1-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-428">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-428">-1,008.00</span></span></td>
<td><span data-ttu-id="8e9b1-429">-1,008.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-430">10</span><span class="sxs-lookup"><span data-stu-id="8e9b1-430">10</span></span></td>
<td><span data-ttu-id="8e9b1-431">折旧费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-432">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e9b1-433">11</span><span class="sxs-lookup"><span data-stu-id="8e9b1-433">11</span></span></td>
<td><span data-ttu-id="8e9b1-434">累计折旧</span><span class="sxs-lookup"><span data-stu-id="8e9b1-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="8e9b1-435">0.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e9b1-436">如果要使用 IFRS 16 数据来运行同一个试算平衡表，则必须冲销法定会计日记帐条目，并且必须过帐 IFRS 16 日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="8e9b1-437">为了冲销法定日记帐条目，此示例中包括一个法定冲销帐簿，该帐簿与法定帐簿具有相同的设置，但相反的过帐配置文件。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="8e9b1-438">例如，法定帐簿 *借记* 租赁费用科目，但冲销帐簿则 *贷记* 此科目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="8e9b1-439">这些关系很容易在 **资产租赁参数** 页面（**资产租赁 \> 设置 \> 资产租赁参数**）中的资产租赁过帐科目中定义。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="8e9b1-440">如果对冲销帐簿使用用于法定帐簿的相同流程，将生成以下日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="8e9b1-441">区别在于冲销帐簿记录法定帐簿中的冲销条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="8e9b1-442">还将为自定义层创建冲销条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="8e9b1-443">在当前层运行试算平衡表时，不包括冲销日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="8e9b1-444">租赁付款 – 1/31/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="8e9b1-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="8e9b1-445">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-445">Account type</span></span> | <span data-ttu-id="8e9b1-446">帐号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-446">Account number</span></span> | <span data-ttu-id="8e9b1-447">层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-447">Layer</span></span>  | <span data-ttu-id="8e9b1-448">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-448">Account description</span></span> | <span data-ttu-id="8e9b1-449">借记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-449">Debit</span></span>    | <span data-ttu-id="8e9b1-450">贷记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="8e9b1-451">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-451">Ledger</span></span>       | <span data-ttu-id="8e9b1-452">4</span><span class="sxs-lookup"><span data-stu-id="8e9b1-452">4</span></span>              | <span data-ttu-id="8e9b1-453">自定义</span><span class="sxs-lookup"><span data-stu-id="8e9b1-453">Custom</span></span> | <span data-ttu-id="8e9b1-454">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e9b1-454">Clearing account</span></span>    | <span data-ttu-id="8e9b1-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-455">1,000.00</span></span> |          |
| <span data-ttu-id="8e9b1-456">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-456">Ledger</span></span>       | <span data-ttu-id="8e9b1-457">1</span><span class="sxs-lookup"><span data-stu-id="8e9b1-457">1</span></span>              | <span data-ttu-id="8e9b1-458">自定义</span><span class="sxs-lookup"><span data-stu-id="8e9b1-458">Custom</span></span> | <span data-ttu-id="8e9b1-459">租赁费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-459">Lease expense</span></span>       |          | <span data-ttu-id="8e9b1-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-460">1,000.00</span></span> |

<span data-ttu-id="8e9b1-461">现在，您已经删除了法定日记帐条目，您将在 IFRS 16 帐簿中预订 IFRS 16 所需的所有日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="8e9b1-462">这些条目包括对 ROU 资产和负债的初始确认，以及利息和折旧的记录。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="8e9b1-463">初始确认 – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="8e9b1-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="8e9b1-464">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-464">Account type</span></span> | <span data-ttu-id="8e9b1-465">帐号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-465">Account number</span></span> | <span data-ttu-id="8e9b1-466">层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-466">Layer</span></span>  | <span data-ttu-id="8e9b1-467">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-467">Account description</span></span>      | <span data-ttu-id="8e9b1-468">借记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-468">Debit</span></span>     | <span data-ttu-id="8e9b1-469">贷记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="8e9b1-470">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-470">Ledger</span></span>       | <span data-ttu-id="8e9b1-471">6</span><span class="sxs-lookup"><span data-stu-id="8e9b1-471">6</span></span>              | <span data-ttu-id="8e9b1-472">自定义</span><span class="sxs-lookup"><span data-stu-id="8e9b1-472">Custom</span></span> | <span data-ttu-id="8e9b1-473">使用权资产</span><span class="sxs-lookup"><span data-stu-id="8e9b1-473">ROU Asset</span></span>                | <span data-ttu-id="8e9b1-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="8e9b1-474">22,793.90</span></span> |           |
| <span data-ttu-id="8e9b1-475">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-475">Ledger</span></span>       | <span data-ttu-id="8e9b1-476">7</span><span class="sxs-lookup"><span data-stu-id="8e9b1-476">7</span></span>              | <span data-ttu-id="8e9b1-477">自定义</span><span class="sxs-lookup"><span data-stu-id="8e9b1-477">Custom</span></span> | <span data-ttu-id="8e9b1-478">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e9b1-478">Finance lease obligation</span></span> |           | <span data-ttu-id="8e9b1-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="8e9b1-479">22,793.90</span></span> |

<span data-ttu-id="8e9b1-480">租赁付款与其他租赁付款一样过帐。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="8e9b1-481">使用清算科目的原因是为了确保只将现金记入一次。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="8e9b1-482">租赁付款 – 1/31/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="8e9b1-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="8e9b1-483">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-483">Account type</span></span> | <span data-ttu-id="8e9b1-484">帐号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-484">Account number</span></span> | <span data-ttu-id="8e9b1-485">层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-485">Layer</span></span>  | <span data-ttu-id="8e9b1-486">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-486">Account description</span></span>      | <span data-ttu-id="8e9b1-487">借记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-487">Debit</span></span>    | <span data-ttu-id="8e9b1-488">贷记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="8e9b1-489">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-489">Ledger</span></span>       | <span data-ttu-id="8e9b1-490">7</span><span class="sxs-lookup"><span data-stu-id="8e9b1-490">7</span></span>              | <span data-ttu-id="8e9b1-491">自定义</span><span class="sxs-lookup"><span data-stu-id="8e9b1-491">Custom</span></span> | <span data-ttu-id="8e9b1-492">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e9b1-492">Finance lease obligation</span></span> | <span data-ttu-id="8e9b1-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-493">1,000.00</span></span> |          |
| <span data-ttu-id="8e9b1-494">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-494">Ledger</span></span>       | <span data-ttu-id="8e9b1-495">4</span><span class="sxs-lookup"><span data-stu-id="8e9b1-495">4</span></span>              | <span data-ttu-id="8e9b1-496">自定义</span><span class="sxs-lookup"><span data-stu-id="8e9b1-496">Custom</span></span> | <span data-ttu-id="8e9b1-497">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e9b1-497">Clearing account</span></span>         |          | <span data-ttu-id="8e9b1-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-498">1,000.00</span></span> |

<span data-ttu-id="8e9b1-499">利息费用日记帐条目从负债摊销计划中生成。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="8e9b1-500">利息费用 – 1/31/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="8e9b1-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="8e9b1-501">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-501">Account type</span></span> | <span data-ttu-id="8e9b1-502">帐号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-502">Account number</span></span> | <span data-ttu-id="8e9b1-503">层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-503">Layer</span></span>  | <span data-ttu-id="8e9b1-504">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-504">Account description</span></span>      | <span data-ttu-id="8e9b1-505">借记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-505">Debit</span></span> | <span data-ttu-id="8e9b1-506">贷记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="8e9b1-507">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-507">Ledger</span></span>       | <span data-ttu-id="8e9b1-508">8</span><span class="sxs-lookup"><span data-stu-id="8e9b1-508">8</span></span>              | <span data-ttu-id="8e9b1-509">自定义</span><span class="sxs-lookup"><span data-stu-id="8e9b1-509">Custom</span></span> | <span data-ttu-id="8e9b1-510">利息费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-510">Interest expense</span></span>         | <span data-ttu-id="8e9b1-511">94.97</span><span class="sxs-lookup"><span data-stu-id="8e9b1-511">94.97</span></span> |        |
| <span data-ttu-id="8e9b1-512">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-512">Ledger</span></span>       | <span data-ttu-id="8e9b1-513">7</span><span class="sxs-lookup"><span data-stu-id="8e9b1-513">7</span></span>              | <span data-ttu-id="8e9b1-514">自定义</span><span class="sxs-lookup"><span data-stu-id="8e9b1-514">Custom</span></span> | <span data-ttu-id="8e9b1-515">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e9b1-515">Finance lease obligation</span></span> |       | <span data-ttu-id="8e9b1-516">94.97</span><span class="sxs-lookup"><span data-stu-id="8e9b1-516">94.97</span></span>  |

<span data-ttu-id="8e9b1-517">折旧费用日记帐条目从资产折旧计划中生成。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="8e9b1-518">折旧费用 – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="8e9b1-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="8e9b1-519">科目类型</span><span class="sxs-lookup"><span data-stu-id="8e9b1-519">Account type</span></span> | <span data-ttu-id="8e9b1-520">帐号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-520">Account number</span></span> | <span data-ttu-id="8e9b1-521">层</span><span class="sxs-lookup"><span data-stu-id="8e9b1-521">Layer</span></span>  | <span data-ttu-id="8e9b1-522">科目描述</span><span class="sxs-lookup"><span data-stu-id="8e9b1-522">Account description</span></span>      | <span data-ttu-id="8e9b1-523">借记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-523">Debit</span></span>  | <span data-ttu-id="8e9b1-524">贷记</span><span class="sxs-lookup"><span data-stu-id="8e9b1-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="8e9b1-525">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-525">Ledger</span></span>       | <span data-ttu-id="8e9b1-526">10</span><span class="sxs-lookup"><span data-stu-id="8e9b1-526">10</span></span>             | <span data-ttu-id="8e9b1-527">自定义</span><span class="sxs-lookup"><span data-stu-id="8e9b1-527">Custom</span></span> | <span data-ttu-id="8e9b1-528">折旧费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-528">Depreciation expense</span></span>     | <span data-ttu-id="8e9b1-529">949.75</span><span class="sxs-lookup"><span data-stu-id="8e9b1-529">949.75</span></span> |        |
| <span data-ttu-id="8e9b1-530">总帐</span><span class="sxs-lookup"><span data-stu-id="8e9b1-530">Ledger</span></span>       | <span data-ttu-id="8e9b1-531">11</span><span class="sxs-lookup"><span data-stu-id="8e9b1-531">11</span></span>             | <span data-ttu-id="8e9b1-532">自定义</span><span class="sxs-lookup"><span data-stu-id="8e9b1-532">Custom</span></span> | <span data-ttu-id="8e9b1-533">累计折旧</span><span class="sxs-lookup"><span data-stu-id="8e9b1-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="8e9b1-534">949.75</span><span class="sxs-lookup"><span data-stu-id="8e9b1-534">949.75</span></span> |

<span data-ttu-id="8e9b1-535">创建并过帐所有这些日记帐条目后，您将看到以下“自定义层 1”值。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="8e9b1-536">请注意，最后一列包括银行手续费、增值税 (VAT) 费用和上一层的现金减少额，但不包括法定申报日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="8e9b1-537">因此，您可以实现真正的双重申报功能。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="8e9b1-538">此时，公司仅需运行其试算平衡表，并将当前层和自定义层结合起来即可创建 IFRS 试算平衡表。</span><span class="sxs-lookup"><span data-stu-id="8e9b1-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="8e9b1-539">科目编号</span><span class="sxs-lookup"><span data-stu-id="8e9b1-539">Account No</span></span> | <span data-ttu-id="8e9b1-540">说明</span><span class="sxs-lookup"><span data-stu-id="8e9b1-540">Description</span></span>              | <span data-ttu-id="8e9b1-541">法定帐簿\-当前层\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e9b1-542">法定帐簿\-当前层\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e9b1-543">法定帐簿\-当前层\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e9b1-544">当前层 \- 总计</span><span class="sxs-lookup"><span data-stu-id="8e9b1-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="8e9b1-545">冲销帐簿\-自定义层\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e9b1-546">IFRS 16 帐簿\-自定义层\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e9b1-547">IFRS 16 帐簿\-自定义层\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e9b1-548">IFRS 16 帐簿\-自定义层\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e9b1-549">IFRS 16 帐簿\-自定义层\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="8e9b1-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="8e9b1-550">自定义层 \+ 当前层 \- 总计</span><span class="sxs-lookup"><span data-stu-id="8e9b1-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="8e9b1-551">1</span><span class="sxs-lookup"><span data-stu-id="8e9b1-551">1</span></span>          | <span data-ttu-id="8e9b1-552">租赁费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-552">Lease expense</span></span>            | <span data-ttu-id="8e9b1-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="8e9b1-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-554">1,000\.00</span></span>               |   | <span data-ttu-id="8e9b1-555">\-1,000</span><span class="sxs-lookup"><span data-stu-id="8e9b1-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="8e9b1-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-556">0\.00</span></span>                                   |
| <span data-ttu-id="8e9b1-557">2</span><span class="sxs-lookup"><span data-stu-id="8e9b1-557">2</span></span>          | <span data-ttu-id="8e9b1-558">银行手续费</span><span class="sxs-lookup"><span data-stu-id="8e9b1-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="8e9b1-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="8e9b1-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8e9b1-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-561">3\.00</span></span>                                   |
| <span data-ttu-id="8e9b1-562">3</span><span class="sxs-lookup"><span data-stu-id="8e9b1-562">3</span></span>          | <span data-ttu-id="8e9b1-563">增值税费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="8e9b1-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="8e9b1-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8e9b1-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-566">5\.00</span></span>                                   |
| <span data-ttu-id="8e9b1-567">4</span><span class="sxs-lookup"><span data-stu-id="8e9b1-567">4</span></span>          | <span data-ttu-id="8e9b1-568">结算科目</span><span class="sxs-lookup"><span data-stu-id="8e9b1-568">Clearing account</span></span>         | <span data-ttu-id="8e9b1-569">\-1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="8e9b1-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="8e9b1-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-571">0\.00</span></span>                   |   | <span data-ttu-id="8e9b1-572">1,000</span><span class="sxs-lookup"><span data-stu-id="8e9b1-572">1,000</span></span>                                           |                                                | <span data-ttu-id="8e9b1-573">\-1,000</span><span class="sxs-lookup"><span data-stu-id="8e9b1-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="8e9b1-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-574">0\.00</span></span>                                   |
| <span data-ttu-id="8e9b1-575">5</span><span class="sxs-lookup"><span data-stu-id="8e9b1-575">5</span></span>          | <span data-ttu-id="8e9b1-576">应付帐款</span><span class="sxs-lookup"><span data-stu-id="8e9b1-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="8e9b1-577">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="8e9b1-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-578">1,008\.00</span></span>                                         | <span data-ttu-id="8e9b1-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8e9b1-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-580">0\.00</span></span>                                   |
| <span data-ttu-id="8e9b1-581">6</span><span class="sxs-lookup"><span data-stu-id="8e9b1-581">6</span></span>          | <span data-ttu-id="8e9b1-582">使用权资产</span><span class="sxs-lookup"><span data-stu-id="8e9b1-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="8e9b1-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="8e9b1-584">22,794</span><span class="sxs-lookup"><span data-stu-id="8e9b1-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="8e9b1-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="8e9b1-585">22,793\.90</span></span>                              |
| <span data-ttu-id="8e9b1-586">7</span><span class="sxs-lookup"><span data-stu-id="8e9b1-586">7</span></span>          | <span data-ttu-id="8e9b1-587">金融租赁义务</span><span class="sxs-lookup"><span data-stu-id="8e9b1-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="8e9b1-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="8e9b1-589">\-22,794</span><span class="sxs-lookup"><span data-stu-id="8e9b1-589">\-22,794</span></span>                                       | <span data-ttu-id="8e9b1-590">1,000</span><span class="sxs-lookup"><span data-stu-id="8e9b1-590">1,000</span></span>                                          | <span data-ttu-id="8e9b1-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="8e9b1-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="8e9b1-592">\-21,888\.87</span><span class="sxs-lookup"><span data-stu-id="8e9b1-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="8e9b1-593">8</span><span class="sxs-lookup"><span data-stu-id="8e9b1-593">8</span></span>          | <span data-ttu-id="8e9b1-594">利息费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="8e9b1-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="8e9b1-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="8e9b1-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="8e9b1-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="8e9b1-597">94\.97</span></span>                                  |
| <span data-ttu-id="8e9b1-598">9</span><span class="sxs-lookup"><span data-stu-id="8e9b1-598">9</span></span>          | <span data-ttu-id="8e9b1-599">现金</span><span class="sxs-lookup"><span data-stu-id="8e9b1-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="8e9b1-600">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="8e9b1-601">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="8e9b1-602">\-1,008\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="8e9b1-603">10</span><span class="sxs-lookup"><span data-stu-id="8e9b1-603">10</span></span>         | <span data-ttu-id="8e9b1-604">折旧费用</span><span class="sxs-lookup"><span data-stu-id="8e9b1-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="8e9b1-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="8e9b1-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="8e9b1-606">949\.75</span></span>                                        | <span data-ttu-id="8e9b1-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="8e9b1-607">949\.75</span></span>                                 |
| <span data-ttu-id="8e9b1-608">11</span><span class="sxs-lookup"><span data-stu-id="8e9b1-608">11</span></span>         | <span data-ttu-id="8e9b1-609">累计折旧</span><span class="sxs-lookup"><span data-stu-id="8e9b1-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="8e9b1-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="8e9b1-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="8e9b1-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="8e9b1-611">\-949\.75</span></span>                                      | <span data-ttu-id="8e9b1-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="8e9b1-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
