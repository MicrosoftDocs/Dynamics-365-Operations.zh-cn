---
title: 使用冲销的折旧影响
description: 本文讨论冲销固定资产交易记录的潜在影响。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd4c4a9e7e89b34b1311b38310877b45e4d95b22
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840593"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="18284-103">使用冲销的折旧影响</span><span class="sxs-lookup"><span data-stu-id="18284-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18284-104">本文讨论冲销固定资产交易记录的潜在影响。</span><span class="sxs-lookup"><span data-stu-id="18284-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="18284-105">您可以冲销固定资产交易记录，以及与某一固定资产相关联的应付账款和应收账款交易记录。</span><span class="sxs-lookup"><span data-stu-id="18284-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="18284-106">您还可以撤消某一已冲销的交易记录。</span><span class="sxs-lookup"><span data-stu-id="18284-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="18284-107">您可以冲销或取消不是最近交易记录过帐到资产的帐簿交易记录。</span><span class="sxs-lookup"><span data-stu-id="18284-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="18284-108">您应该首先确定任何折旧交易记录是否在您冲销的交易记录后过帐。</span><span class="sxs-lookup"><span data-stu-id="18284-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="18284-109">原因在于，并不重新计算折旧，在您冲销交易记录时。</span><span class="sxs-lookup"><span data-stu-id="18284-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="18284-110">因此，如以下示例中所示，折旧在冲销后常常被高估或低估，。</span><span class="sxs-lookup"><span data-stu-id="18284-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="18284-111">为了在您冲销某一交易记录时确保折旧正确，如果您在该过程中收到一条消息，说明将不重新计算折旧，则不要继续进行冲销。</span><span class="sxs-lookup"><span data-stu-id="18284-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="18284-112">而是首先冲销在您尝试冲销的交易记录后已过帐的折旧交易记录，然后继续进行冲销。</span><span class="sxs-lookup"><span data-stu-id="18284-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="18284-113">您将不会收到有关折旧重新计算的警告，并且您可以继续冲销。</span><span class="sxs-lookup"><span data-stu-id="18284-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="18284-114">以下示例显示在您选择不理睬警告消息而继续冲销（而不是首先冲销折旧交易记录）的情况下发生的计算。</span><span class="sxs-lookup"><span data-stu-id="18284-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="18284-115">示例 1：折旧被高估</span><span class="sxs-lookup"><span data-stu-id="18284-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="18284-116">使用 5 年的使用寿命和直线法折旧（60 个折旧期间）设置某一资产。</span><span class="sxs-lookup"><span data-stu-id="18284-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="18284-117">在此示例中，折旧被高估。</span><span class="sxs-lookup"><span data-stu-id="18284-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="18284-118">资产交易历史记录</span><span class="sxs-lookup"><span data-stu-id="18284-118">Asset transaction history</span></span>

| <span data-ttu-id="18284-119">日期</span><span class="sxs-lookup"><span data-stu-id="18284-119">Date</span></span>       | <span data-ttu-id="18284-120">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="18284-120">Transaction type</span></span>                                                          | <span data-ttu-id="18284-121">金额</span><span class="sxs-lookup"><span data-stu-id="18284-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="18284-122">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="18284-122">January 1</span></span>  | <span data-ttu-id="18284-123">购置</span><span class="sxs-lookup"><span data-stu-id="18284-123">Acquisition</span></span>                                                               | <span data-ttu-id="18284-124">59,000.00</span><span class="sxs-lookup"><span data-stu-id="18284-124">59,000.00</span></span>                                 |
| <span data-ttu-id="18284-125">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="18284-125">January 1</span></span>  | <span data-ttu-id="18284-126">购置调整</span><span class="sxs-lookup"><span data-stu-id="18284-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="18284-127">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18284-127">1,000.00</span></span>                                  |
| <span data-ttu-id="18284-128">1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="18284-128">January 31</span></span> | <span data-ttu-id="18284-129">折旧（使用针对一个折旧期间的方案创建）</span><span class="sxs-lookup"><span data-stu-id="18284-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="18284-130">1,000.00 计算：帐面净值 (59,000 + 1,000) / 剩余折旧期间数目 (60)</span><span class="sxs-lookup"><span data-stu-id="18284-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="18284-131">冲销操作</span><span class="sxs-lookup"><span data-stu-id="18284-131">Reversal action</span></span>

| <span data-ttu-id="18284-132">日期</span><span class="sxs-lookup"><span data-stu-id="18284-132">Date</span></span>      | <span data-ttu-id="18284-133">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="18284-133">Transaction type</span></span>                | <span data-ttu-id="18284-134">金额</span><span class="sxs-lookup"><span data-stu-id="18284-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="18284-135">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="18284-135">January 1</span></span> | <span data-ttu-id="18284-136">购置调整冲销</span><span class="sxs-lookup"><span data-stu-id="18284-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="18284-137">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="18284-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="18284-138">折旧影响</span><span class="sxs-lookup"><span data-stu-id="18284-138">Depreciation effect</span></span>

| <span data-ttu-id="18284-139">日期</span><span class="sxs-lookup"><span data-stu-id="18284-139">Date</span></span>        | <span data-ttu-id="18284-140">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="18284-140">Transaction type</span></span>        | <span data-ttu-id="18284-141">金额</span><span class="sxs-lookup"><span data-stu-id="18284-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18284-142">2 月 28 日</span><span class="sxs-lookup"><span data-stu-id="18284-142">February 28</span></span> | <span data-ttu-id="18284-143">折旧（方案）</span><span class="sxs-lookup"><span data-stu-id="18284-143">Depreciation (proposal)</span></span> | <span data-ttu-id="18284-144">983.05 计算：帐面净值 (59,000 - 1,000 折旧) / 剩余折旧期间数目 (59)</span><span class="sxs-lookup"><span data-stu-id="18284-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="18284-145">折旧被高估 16.95 (1000 - 983.05)。</span><span class="sxs-lookup"><span data-stu-id="18284-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="18284-146">示例 2：折旧被低估</span><span class="sxs-lookup"><span data-stu-id="18284-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="18284-147">使用 5 年的使用寿命和直线法折旧（60 个折旧期间）设置某一资产。</span><span class="sxs-lookup"><span data-stu-id="18284-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="18284-148">在此示例中，折旧被低估。</span><span class="sxs-lookup"><span data-stu-id="18284-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="18284-149">资产交易历史记录</span><span class="sxs-lookup"><span data-stu-id="18284-149">Asset transaction history</span></span>

| <span data-ttu-id="18284-150">日期</span><span class="sxs-lookup"><span data-stu-id="18284-150">Date</span></span>       | <span data-ttu-id="18284-151">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="18284-151">Transaction type</span></span>                                                          | <span data-ttu-id="18284-152">金额</span><span class="sxs-lookup"><span data-stu-id="18284-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="18284-153">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="18284-153">January 1</span></span>  | <span data-ttu-id="18284-154">购置</span><span class="sxs-lookup"><span data-stu-id="18284-154">Acquisition</span></span>                                                               | <span data-ttu-id="18284-155">59,000.00</span><span class="sxs-lookup"><span data-stu-id="18284-155">59,000.00</span></span>                                   |
| <span data-ttu-id="18284-156">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="18284-156">January 1</span></span>  | <span data-ttu-id="18284-157">调低</span><span class="sxs-lookup"><span data-stu-id="18284-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="18284-158">1,000.00</span><span class="sxs-lookup"><span data-stu-id="18284-158">1,000.00</span></span>                                    |
| <span data-ttu-id="18284-159">1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="18284-159">January 31</span></span> | <span data-ttu-id="18284-160">折旧（使用针对一个折旧期间的方案创建）</span><span class="sxs-lookup"><span data-stu-id="18284-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="18284-161">966.67 计算：帐面净值 (59,000 - 1,000) / 剩余折旧期间数目 (60)</span><span class="sxs-lookup"><span data-stu-id="18284-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="18284-162">冲销操作</span><span class="sxs-lookup"><span data-stu-id="18284-162">Reversal action</span></span>

| <span data-ttu-id="18284-163">日期</span><span class="sxs-lookup"><span data-stu-id="18284-163">Date</span></span>      | <span data-ttu-id="18284-164">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="18284-164">Transaction type</span></span>               | <span data-ttu-id="18284-165">金额</span><span class="sxs-lookup"><span data-stu-id="18284-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="18284-166">1 月 1 日</span><span class="sxs-lookup"><span data-stu-id="18284-166">January 1</span></span> | <span data-ttu-id="18284-167">调低冲销</span><span class="sxs-lookup"><span data-stu-id="18284-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="18284-168">-1,000.00</span><span class="sxs-lookup"><span data-stu-id="18284-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="18284-169">折旧影响</span><span class="sxs-lookup"><span data-stu-id="18284-169">Depreciation effect</span></span>

| <span data-ttu-id="18284-170">日期</span><span class="sxs-lookup"><span data-stu-id="18284-170">Date</span></span>        | <span data-ttu-id="18284-171">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="18284-171">Transaction type</span></span>        | <span data-ttu-id="18284-172">金额</span><span class="sxs-lookup"><span data-stu-id="18284-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="18284-173">2 月 28 日</span><span class="sxs-lookup"><span data-stu-id="18284-173">February 28</span></span> | <span data-ttu-id="18284-174">折旧（方案）</span><span class="sxs-lookup"><span data-stu-id="18284-174">Depreciation (proposal)</span></span> | <span data-ttu-id="18284-175">983.62 计算：帐面净值 (59,000 - 966.67 折旧) / 剩余折旧期间数目 (59)</span><span class="sxs-lookup"><span data-stu-id="18284-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="18284-176">折旧被低估 16.95 (983.62 - 966.67)。</span><span class="sxs-lookup"><span data-stu-id="18284-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="18284-177">其他资源</span><span class="sxs-lookup"><span data-stu-id="18284-177">Additional resources</span></span>
--------

[<span data-ttu-id="18284-178">固定资产折旧</span><span class="sxs-lookup"><span data-stu-id="18284-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



