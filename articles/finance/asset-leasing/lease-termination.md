---
title: 租赁终止方案
description: 本主题说明如何建议要终止的租赁。
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 144559b14878a44afd8a77648bb5ce1d3ba17832
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131272"
---
# <a name="propose-a-lease-for-termination"></a><span data-ttu-id="937df-103">建议要终止的租赁</span><span class="sxs-lookup"><span data-stu-id="937df-103">Propose a lease for termination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="937df-104">如果租赁提前终止，“资产租赁”可以记录终止日记帐条目，以勾销租赁负债、使用权 (ROU) 资产和累计折旧，并计入损益。</span><span class="sxs-lookup"><span data-stu-id="937df-104">If a lease is terminated early, Asset leasing can record a termination journal entry to write off the lease liability, right-of-use (ROU) asset, and accumulated depreciation, and book a gain or loss.</span></span> <span data-ttu-id="937df-105">提前终止流程将终止租赁及其关联的租赁帐簿。</span><span class="sxs-lookup"><span data-stu-id="937df-105">The early termination process terminates a lease and its associated lease books.</span></span> <span data-ttu-id="937df-106">不会终止单个租赁帐簿。</span><span class="sxs-lookup"><span data-stu-id="937df-106">It doesn't terminate individual lease books.</span></span> <span data-ttu-id="937df-107">本主题介绍让您可以建议要终止的租赁并处理租赁终止日记帐条目的功能。</span><span class="sxs-lookup"><span data-stu-id="937df-107">This topic describes the functionality that lets you propose a lease for termination and process the lease termination journal entry.</span></span>

<span data-ttu-id="937df-108">如果租赁未分类为延期租金处理租赁且未与固定资产关联，资产租赁将生成以下终止日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="937df-108">If a lease isn't classified as a deferred rent treatment lease and isn't associated with a fixed asset, Asset leasing produces the following termination journal entry.</span></span>

| <span data-ttu-id="937df-109">交易</span><span class="sxs-lookup"><span data-stu-id="937df-109">Transaction</span></span>                           | <span data-ttu-id="937df-110">借记（借）</span><span class="sxs-lookup"><span data-stu-id="937df-110">Debit (Dr.)</span></span> | <span data-ttu-id="937df-111">贷记（贷）</span><span class="sxs-lookup"><span data-stu-id="937df-111">Credit (Cr.)</span></span> |
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="937df-112">借记租赁负债</span><span class="sxs-lookup"><span data-stu-id="937df-112">Dr. Lease liability</span></span>                   | <span data-ttu-id="937df-113">X</span><span class="sxs-lookup"><span data-stu-id="937df-113">X</span></span>           |              |
| <span data-ttu-id="937df-114">借记累计折旧</span><span class="sxs-lookup"><span data-stu-id="937df-114">Dr. Accumulated depreciation</span></span>          | <span data-ttu-id="937df-115">X</span><span class="sxs-lookup"><span data-stu-id="937df-115">X</span></span>           |              |
| <span data-ttu-id="937df-116">借记租赁修改的损（益）</span><span class="sxs-lookup"><span data-stu-id="937df-116">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="937df-117">X</span><span class="sxs-lookup"><span data-stu-id="937df-117">X</span></span>           |              |
| <span data-ttu-id="937df-118">贷记租赁资产</span><span class="sxs-lookup"><span data-stu-id="937df-118">Cr. Lease asset</span></span>                       |             | <span data-ttu-id="937df-119">X</span><span class="sxs-lookup"><span data-stu-id="937df-119">X</span></span>            |
| <span data-ttu-id="937df-120">贷记租赁修改的损（益）</span><span class="sxs-lookup"><span data-stu-id="937df-120">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="937df-121">X</span><span class="sxs-lookup"><span data-stu-id="937df-121">X</span></span>            |

<span data-ttu-id="937df-122">如果租赁帐簿被分类为延期租金帐簿，条目会将终止之前延期租金的余额勾销到收益科目或损失科目，如此处所示。</span><span class="sxs-lookup"><span data-stu-id="937df-122">If the lease book is classified as a deferred rent book, the entry writes off the balance of the deferred rent before the termination to the gain or loss account, as shown here.</span></span>

| <span data-ttu-id="937df-123">交易</span><span class="sxs-lookup"><span data-stu-id="937df-123">Transaction</span></span>                           | <span data-ttu-id="937df-124">借记（借）</span><span class="sxs-lookup"><span data-stu-id="937df-124">Debit (Dr.)</span></span> | <span data-ttu-id="937df-125">贷记（贷）</span><span class="sxs-lookup"><span data-stu-id="937df-125">Credit (Cr.)</span></span> | 
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="937df-126">借记延期租金</span><span class="sxs-lookup"><span data-stu-id="937df-126">Dr. Deferred rent</span></span>                     | <span data-ttu-id="937df-127">X</span><span class="sxs-lookup"><span data-stu-id="937df-127">X</span></span>           |              |
| <span data-ttu-id="937df-128">贷记租赁修改的损（益）</span><span class="sxs-lookup"><span data-stu-id="937df-128">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="937df-129">X</span><span class="sxs-lookup"><span data-stu-id="937df-129">X</span></span>            |
| <span data-ttu-id="937df-130">贷记延期租金</span><span class="sxs-lookup"><span data-stu-id="937df-130">Cr. Deferred rent</span></span>                     |             | <span data-ttu-id="937df-131">X</span><span class="sxs-lookup"><span data-stu-id="937df-131">X</span></span>            |
| <span data-ttu-id="937df-132">借记租赁修改的损（益）</span><span class="sxs-lookup"><span data-stu-id="937df-132">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="937df-133">X</span><span class="sxs-lookup"><span data-stu-id="937df-133">X</span></span>           |              |

<span data-ttu-id="937df-134">如果租赁帐簿连接到固定资产，使用权资产将计入固定资产。</span><span class="sxs-lookup"><span data-stu-id="937df-134">If the lease book is connected to a fixed asset, the ROU asset is accounted for in Fixed assets.</span></span> <span data-ttu-id="937df-135">此会计包括要提前终止的会计。</span><span class="sxs-lookup"><span data-stu-id="937df-135">This accounting includes the accounting for early terminations.</span></span> <span data-ttu-id="937df-136">资产租赁生成以下日记帐条目以勾销租赁负债。</span><span class="sxs-lookup"><span data-stu-id="937df-136">Asset leasing produces the following journal entry to write off the lease liability.</span></span>

| <span data-ttu-id="937df-137">交易</span><span class="sxs-lookup"><span data-stu-id="937df-137">Transaction</span></span>                           | <span data-ttu-id="937df-138">借记（借）</span><span class="sxs-lookup"><span data-stu-id="937df-138">Debit (Dr.)</span></span> | <span data-ttu-id="937df-139">贷记（贷）</span><span class="sxs-lookup"><span data-stu-id="937df-139">Credit (Cr.)</span></span> |
|---------------------------------------|-------------|--------------|
| <span data-ttu-id="937df-140">借记租赁负债</span><span class="sxs-lookup"><span data-stu-id="937df-140">Dr. Lease liability</span></span>                   | <span data-ttu-id="937df-141">X</span><span class="sxs-lookup"><span data-stu-id="937df-141">X</span></span>           |              |
| <span data-ttu-id="937df-142">贷记租赁修改的损（益）</span><span class="sxs-lookup"><span data-stu-id="937df-142">Cr. Gain (loss) on lease modification</span></span> |             | <span data-ttu-id="937df-143">X</span><span class="sxs-lookup"><span data-stu-id="937df-143">X</span></span>            |

<span data-ttu-id="937df-144">有关处置使用权资产的正确方法的信息，请参阅[将固定资产作为废料处置](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md)。</span><span class="sxs-lookup"><span data-stu-id="937df-144">For information about the correct way to dispose of an ROU asset, see [Dispose of a fixed asset as scrap](../fixed-assets/dispose-of-a-fixed-asset-as-scrap.md).</span></span>

## <a name="propose-a-lease-for-termination"></a><span data-ttu-id="937df-145">建议要终止的租赁</span><span class="sxs-lookup"><span data-stu-id="937df-145">Propose a lease for termination</span></span>

1. <span data-ttu-id="937df-146">转到必须终止的租赁，然后在操作窗格上，选择 **终止方案**。</span><span class="sxs-lookup"><span data-stu-id="937df-146">Go to the lease that must be terminated, and then, on the Action Pane, select **Termination proposal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="937df-147">如果针对任何帐簿有任何未过帐的日记帐条目，**终止方案** 按钮将不可用。</span><span class="sxs-lookup"><span data-stu-id="937df-147">The **Termination proposal** button is unavailable if there are any unposted journal entries against any book.</span></span> <span data-ttu-id="937df-148">您必须先过帐或删除针对租赁创建的所有日记帐条目，然后才能够终止租赁。</span><span class="sxs-lookup"><span data-stu-id="937df-148">Before you can terminate the lease, you must post or delete any journal entries that have been created against the lease.</span></span>

2. <span data-ttu-id="937df-149">在出现的对话框中，为终止日记帐条目设置 **生效日期** 和 **过帐日期** 字段。</span><span class="sxs-lookup"><span data-stu-id="937df-149">In the dialog box that appears, set the **Effective date** and **Posting date** fields for the termination journal entry.</span></span>
3. <span data-ttu-id="937df-150">选择 **终止方案** 可以建议要终止的租赁。</span><span class="sxs-lookup"><span data-stu-id="937df-150">Select **Termination proposal** to propose the lease for termination.</span></span>
4. <span data-ttu-id="937df-151">选择 **过帐租赁终止** 可以自动过帐租赁终止日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="937df-151">Select **Post lease termination** to automatically post the lease termination journal entry.</span></span>
5. <span data-ttu-id="937df-152">在 **租赁终止** 页上，选择您建议终止的租赁的租赁 ID 来查看终止行。</span><span class="sxs-lookup"><span data-stu-id="937df-152">On the **Lease terminations** page, select the lease ID of the lease that you proposed for termination to view the termination lines.</span></span> <span data-ttu-id="937df-153">终止行显示使用权资产、租赁负债、累计折旧、延期租金（如果适用）以及在租赁终止时必须确认的损益的结转值。</span><span class="sxs-lookup"><span data-stu-id="937df-153">The termination lines show the carrying values of the ROU asset, lease liability, accumulated depreciation, deferred rent (if applicable), and gain or loss that must be recognized on the termination of the lease.</span></span>

<span data-ttu-id="937df-154">租赁现在可以终止了。</span><span class="sxs-lookup"><span data-stu-id="937df-154">The lease is now ready for termination.</span></span> <span data-ttu-id="937df-155">租赁帐簿的 **终止状态** 字段的值将更改为 **可以终止**。</span><span class="sxs-lookup"><span data-stu-id="937df-155">The value of the **Termination status** field for the lease book is changed to **Ready for termination**.</span></span> <span data-ttu-id="937df-156">此时，您不能再针对该租赁过帐日记帐条目，也不能对其进行调整或减损。</span><span class="sxs-lookup"><span data-stu-id="937df-156">At this point, you can no longer post journal entries against the lease, or adjust or impair it.</span></span> 

## <a name="process-leases-that-are-ready-for-termination"></a><span data-ttu-id="937df-157">处理准备好终止的租赁</span><span class="sxs-lookup"><span data-stu-id="937df-157">Process leases that are ready for termination</span></span>

<span data-ttu-id="937df-158">要处理准备好终止的租赁并过帐终止日记帐条目，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="937df-158">To process leases that are ready for termination and post the termination journal entry, follow these steps.</span></span>

1. <span data-ttu-id="937df-159">在 **租赁终止** 页上，选择要处理的租赁，然后选择 **终止**。</span><span class="sxs-lookup"><span data-stu-id="937df-159">On the **Lease terminations** page, select the lease to process, and then select **Terminate**.</span></span>
2. <span data-ttu-id="937df-160">在显示的对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="937df-160">In the dialog box that appears, select **OK**.</span></span>

<span data-ttu-id="937df-161">系统将过帐终止日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="937df-161">The system posts the termination journal entry.</span></span> <span data-ttu-id="937df-162">租赁帐簿的 **租赁状态** 字段将设置为 **已终止**，**终止方案状态** 字段将设置为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="937df-162">The **Lease status** field for the lease book is set to **Terminated**, and the **Termination proposal status** field is set to **Completed**.</span></span>

## <a name="reverse-a-lease-termination"></a><span data-ttu-id="937df-163">冲销租赁终止</span><span class="sxs-lookup"><span data-stu-id="937df-163">Reverse a lease termination</span></span>

<span data-ttu-id="937df-164">要冲销租赁终止日记帐条目并打开终止的租赁，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="937df-164">To reverse a lease termination journal entry and open a terminated lease, follow this step.</span></span>

- <span data-ttu-id="937df-165">在 **租赁终止** 页上，选择要冲销的终止的租赁，然后选择 **冲销终止**。</span><span class="sxs-lookup"><span data-stu-id="937df-165">On the **Lease terminations** page, select the terminated lease to reverse, and then select **Reverse termination**.</span></span>

<span data-ttu-id="937df-166">系统将冲销终止日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="937df-166">The system reverses the termination journal entry.</span></span> <span data-ttu-id="937df-167">租赁帐簿的 **租赁状态** 字段将设置为 **打开**。</span><span class="sxs-lookup"><span data-stu-id="937df-167">The **Lease status** field for the lease book is set to **Open**.</span></span> <span data-ttu-id="937df-168">此租赁不会再出现在 **租赁终止** 页上，可以再次建议终止。</span><span class="sxs-lookup"><span data-stu-id="937df-168">The lease no longer appears on the **Lease terminations** page and can be proposed again for termination.</span></span>

## <a name="example-of-a-lease-termination"></a><span data-ttu-id="937df-169">租赁终止示例</span><span class="sxs-lookup"><span data-stu-id="937df-169">Example of a lease termination</span></span>

<span data-ttu-id="937df-170">在此示例中，租赁与非专用资产关联，不会转移资产所有权或授予承租人购买资产的选择权。</span><span class="sxs-lookup"><span data-stu-id="937df-170">For this example, the lease is associated with a non-specialized asset, and it doesn't transfer ownership of the asset or grant the lessee the option to purchase the asset.</span></span>

### <a name="setup"></a><span data-ttu-id="937df-171">设置</span><span class="sxs-lookup"><span data-stu-id="937df-171">Setup</span></span>

<span data-ttu-id="937df-172">下面的表显示了在 **常规** 和 **付款计划行** 选项卡中为此示例中使用的租赁设置的值。</span><span class="sxs-lookup"><span data-stu-id="937df-172">The following tables show the values that are set on the **General** and **Payment schedule lines** tabs for the lease that is used in this example.</span></span>

<span data-ttu-id="937df-173">**常规选项卡**</span><span class="sxs-lookup"><span data-stu-id="937df-173">**General tab**</span></span>

| <span data-ttu-id="937df-174">字段</span><span class="sxs-lookup"><span data-stu-id="937df-174">Field</span></span>                      | <span data-ttu-id="937df-175">值</span><span class="sxs-lookup"><span data-stu-id="937df-175">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="937df-176">资产的公平价值</span><span class="sxs-lookup"><span data-stu-id="937df-176">Fair value of the asset</span></span>    | <span data-ttu-id="937df-177">600,000</span><span class="sxs-lookup"><span data-stu-id="937df-177">600,000</span></span>          |
| <span data-ttu-id="937df-178">货币</span><span class="sxs-lookup"><span data-stu-id="937df-178">Currency</span></span>                   | <span data-ttu-id="937df-179">USD</span><span class="sxs-lookup"><span data-stu-id="937df-179">USD</span></span>              |
| <span data-ttu-id="937df-180">初始直接成本</span><span class="sxs-lookup"><span data-stu-id="937df-180">Initial direct costs</span></span>       | <span data-ttu-id="937df-181">1,000</span><span class="sxs-lookup"><span data-stu-id="937df-181">1,000</span></span>            |
| <span data-ttu-id="937df-182">增量借贷利率</span><span class="sxs-lookup"><span data-stu-id="937df-182">Incremental borrowing rate</span></span> | <span data-ttu-id="937df-183">7%</span><span class="sxs-lookup"><span data-stu-id="937df-183">7%</span></span>               |
| <span data-ttu-id="937df-184">复合间隔</span><span class="sxs-lookup"><span data-stu-id="937df-184">Compounding interval</span></span>       | <span data-ttu-id="937df-185">每年</span><span class="sxs-lookup"><span data-stu-id="937df-185">Annually</span></span>         |
| <span data-ttu-id="937df-186">资产使用年限(月数)</span><span class="sxs-lookup"><span data-stu-id="937df-186">Asset useful life (months)</span></span> | <span data-ttu-id="937df-187">600</span><span class="sxs-lookup"><span data-stu-id="937df-187">600</span></span>              |
| <span data-ttu-id="937df-188">年金类型</span><span class="sxs-lookup"><span data-stu-id="937df-188">Annuity type</span></span>               | <span data-ttu-id="937df-189">普通年金</span><span class="sxs-lookup"><span data-stu-id="937df-189">Ordinary annuity</span></span> |
| <span data-ttu-id="937df-190">开始日期</span><span class="sxs-lookup"><span data-stu-id="937df-190">Commencement date</span></span>          | <span data-ttu-id="937df-191">1/1/2019</span><span class="sxs-lookup"><span data-stu-id="937df-191">1/1/2019</span></span>         |

<span data-ttu-id="937df-192">**付款计划行选项卡**</span><span class="sxs-lookup"><span data-stu-id="937df-192">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="937df-193">字段</span><span class="sxs-lookup"><span data-stu-id="937df-193">Field</span></span>             | <span data-ttu-id="937df-194">值</span><span class="sxs-lookup"><span data-stu-id="937df-194">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="937df-195">开始日期</span><span class="sxs-lookup"><span data-stu-id="937df-195">Start date</span></span>        | <span data-ttu-id="937df-196">1/1/2019</span><span class="sxs-lookup"><span data-stu-id="937df-196">1/1/2019</span></span>   |
| <span data-ttu-id="937df-197">期间间隔</span><span class="sxs-lookup"><span data-stu-id="937df-197">Period interval</span></span>   | <span data-ttu-id="937df-198">月度</span><span class="sxs-lookup"><span data-stu-id="937df-198">Monthly</span></span>    |
| <span data-ttu-id="937df-199">期间</span><span class="sxs-lookup"><span data-stu-id="937df-199">Periods</span></span>           | <span data-ttu-id="937df-200">120</span><span class="sxs-lookup"><span data-stu-id="937df-200">120</span></span>        |
| <span data-ttu-id="937df-201">结束日期</span><span class="sxs-lookup"><span data-stu-id="937df-201">End date</span></span>          | <span data-ttu-id="937df-202">12/31/2028</span><span class="sxs-lookup"><span data-stu-id="937df-202">12/31/2028</span></span> |
| <span data-ttu-id="937df-203">付款频率</span><span class="sxs-lookup"><span data-stu-id="937df-203">Payment frequency</span></span> | <span data-ttu-id="937df-204">每年</span><span class="sxs-lookup"><span data-stu-id="937df-204">Annually</span></span>   |
| <span data-ttu-id="937df-205">付款金额</span><span class="sxs-lookup"><span data-stu-id="937df-205">Payment amount</span></span>    | <span data-ttu-id="937df-206">10,000</span><span class="sxs-lookup"><span data-stu-id="937df-206">10,000</span></span>     |

### <a name="steps-for-terminating-the-lease"></a><span data-ttu-id="937df-207">终止租赁的步骤</span><span class="sxs-lookup"><span data-stu-id="937df-207">Steps for terminating the lease</span></span>

1. <span data-ttu-id="937df-208">按照本主题前面所述创建租赁后，转到租赁帐簿，并确认付款计划。</span><span class="sxs-lookup"><span data-stu-id="937df-208">After you create the lease as described earlier in this topic, go to the lease book, and confirm the payment schedule.</span></span> <span data-ttu-id="937df-209">然后过帐初始确认日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="937df-209">Then post the initial recognition journal entry.</span></span> <span data-ttu-id="937df-210">初始使用权资产为 71,235.81 美元，租赁负债应为 70,235.81 美元。</span><span class="sxs-lookup"><span data-stu-id="937df-210">The initial ROU asset is $71,235.81, and lease liability should be $70,235.81.</span></span> <span data-ttu-id="937df-211">对于此示例，根据会计准则编纂专题 842 (ASC 842)，租赁被分类为经营性租赁。</span><span class="sxs-lookup"><span data-stu-id="937df-211">For this example, the lease was classified as an operating lease under Accounting Standards Codification Topic 842 (ASC 842).</span></span>
2. <span data-ttu-id="937df-212">运行批处理日记帐流程三遍，模拟三年的租赁付款、利息费用和折旧费用过程。</span><span class="sxs-lookup"><span data-stu-id="937df-212">Run the batch journal process three times to simulate the passage of three years for the lease payments, interest expenses, and depreciation expenses.</span></span>
3. <span data-ttu-id="937df-213">运行完所有三个批处理作业后，回到租赁帐簿，然后打开负债和资产交易表以查看使用权资产和租赁负债的当前帐面价值。</span><span class="sxs-lookup"><span data-stu-id="937df-213">After you've finished running all three batch jobs, go back to the lease book, and open the Liability and Asset transactions tables to view the current carrying value of the ROU asset and lease liability.</span></span> <span data-ttu-id="937df-214">三年后，负债的价值应该为大约 -53,893.00 美元，资产的价值应该大约为 54,593.00 美元。</span><span class="sxs-lookup"><span data-stu-id="937df-214">After three years, the value of the liability should be approximately $-53,893.00, and the value of the asset should be approximately $54,593.00.</span></span>

    <span data-ttu-id="937df-215">三年过去后，企业和出租人相互同意终止租赁。</span><span class="sxs-lookup"><span data-stu-id="937df-215">After the three years have passed, the business and lessor mutually agree to terminate the lease.</span></span> <span data-ttu-id="937df-216">因此，您现在必须终止租赁。</span><span class="sxs-lookup"><span data-stu-id="937df-216">Therefore, you must now terminate the lease.</span></span>

4. <span data-ttu-id="937df-217">转到必须终止的租赁，然后在操作窗格上，选择 **终止方案**。</span><span class="sxs-lookup"><span data-stu-id="937df-217">Go to the lease that must be terminated, and then, on the Action Pane, select **Termination proposal**.</span></span> 
5. <span data-ttu-id="937df-218">在出现的对话框中，在 **生效日期** 和 **过帐日期** 字段中，输入 **1/1/2021**。</span><span class="sxs-lookup"><span data-stu-id="937df-218">In the dialog box that appears, in the **Effective date** and **Posting date** field, enter **1/1/2021**.</span></span>
6. <span data-ttu-id="937df-219">选择 **终止方案** 可以建议要终止的租赁。</span><span class="sxs-lookup"><span data-stu-id="937df-219">Select **Termination proposal** to propose the lease for termination.</span></span>

    <span data-ttu-id="937df-220">**租赁终止** 页将出现，显示将要终止的租赁。</span><span class="sxs-lookup"><span data-stu-id="937df-220">The **Lease terminations** page appears and shows the lease that will be terminated.</span></span>

7. <span data-ttu-id="937df-221">要查看终止行，选择您建议终止的租赁的租赁 ID。</span><span class="sxs-lookup"><span data-stu-id="937df-221">To view the termination lines, select the lease ID of the lease that you proposed for termination.</span></span> <span data-ttu-id="937df-222">终止行显示租赁的结转值。</span><span class="sxs-lookup"><span data-stu-id="937df-222">The termination lines show the carrying values of the lease.</span></span> <span data-ttu-id="937df-223">下表显示了这些值在此示例中会呈现的值。</span><span class="sxs-lookup"><span data-stu-id="937df-223">The following table shows what these values should be for this example.</span></span> 

    | <span data-ttu-id="937df-224">字段</span><span class="sxs-lookup"><span data-stu-id="937df-224">Field</span></span>                                                 | <span data-ttu-id="937df-225">值</span><span class="sxs-lookup"><span data-stu-id="937df-225">Value</span></span>      |
    |-------------------------------------------------------|------------|
    | <span data-ttu-id="937df-226">以交易货币表示的负债结转余额</span><span class="sxs-lookup"><span data-stu-id="937df-226">Carrying balance of liability in transaction currency</span></span> | <span data-ttu-id="937df-227">53,892.89 美元</span><span class="sxs-lookup"><span data-stu-id="937df-227">$53,892.89</span></span> |
    | <span data-ttu-id="937df-228">以交易货币表示的使用权资产</span><span class="sxs-lookup"><span data-stu-id="937df-228">Right-of-use asset in transaction currency</span></span>            | <span data-ttu-id="937df-229">71,235.81 美元</span><span class="sxs-lookup"><span data-stu-id="937df-229">$71,235.81</span></span> |
    | <span data-ttu-id="937df-230">以交易货币表示的累计折旧</span><span class="sxs-lookup"><span data-stu-id="937df-230">Accumulated depreciation in transaction currency</span></span>      | <span data-ttu-id="937df-231">16,642.92 美元</span><span class="sxs-lookup"><span data-stu-id="937df-231">$16,642.92</span></span> |
    | <span data-ttu-id="937df-232">以交易货币表示的损（益）</span><span class="sxs-lookup"><span data-stu-id="937df-232">Gain (loss) in transaction currency</span></span>                   | <span data-ttu-id="937df-233">700.00 美元</span><span class="sxs-lookup"><span data-stu-id="937df-233">$-700.00</span></span>   |

8. <span data-ttu-id="937df-234">要过帐终止日记帐条目，在 **租赁终止** 页上选择租赁，然后选择 **终止**。</span><span class="sxs-lookup"><span data-stu-id="937df-234">To post the termination journal entry, select the lease on the **Lease terminations** page, and then select **Terminate**.</span></span>
9. <span data-ttu-id="937df-235">在显示的对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="937df-235">In the dialog box that appears, select **OK**.</span></span>
10. <span data-ttu-id="937df-236">要查看已创建并过帐的终止日记帐条目，转到租赁帐簿中资产的租赁日记帐。</span><span class="sxs-lookup"><span data-stu-id="937df-236">To view the termination journal entry that has been created and posted, go to the asset's leasing journal in the lease book.</span></span> <span data-ttu-id="937df-237">下表显示了此条目在此示例中会呈现的样子。</span><span class="sxs-lookup"><span data-stu-id="937df-237">The following table shows what this entry should look like for this example.</span></span>

    | <span data-ttu-id="937df-238">交易</span><span class="sxs-lookup"><span data-stu-id="937df-238">Transaction</span></span>                           | <span data-ttu-id="937df-239">借记（借）</span><span class="sxs-lookup"><span data-stu-id="937df-239">Debit (Dr.)</span></span> | <span data-ttu-id="937df-240">贷记（贷）</span><span class="sxs-lookup"><span data-stu-id="937df-240">Credit (Cr.)</span></span> |
    |---------------------------------------|-------------|--------------|
    | <span data-ttu-id="937df-241">借记租赁负债</span><span class="sxs-lookup"><span data-stu-id="937df-241">Dr. Lease liability</span></span>                   | <span data-ttu-id="937df-242">53,892.89</span><span class="sxs-lookup"><span data-stu-id="937df-242">53,892.89</span></span>   |              |
    | <span data-ttu-id="937df-243">借记累计折旧</span><span class="sxs-lookup"><span data-stu-id="937df-243">Dr. Accumulated depreciation</span></span>          | <span data-ttu-id="937df-244">16,642.92</span><span class="sxs-lookup"><span data-stu-id="937df-244">16,642.92</span></span>   |              |
    | <span data-ttu-id="937df-245">借记租赁修改的损（益）</span><span class="sxs-lookup"><span data-stu-id="937df-245">Dr. Gain (loss) on lease modification</span></span> | <span data-ttu-id="937df-246">700.00</span><span class="sxs-lookup"><span data-stu-id="937df-246">700.00</span></span>      |              |
    | <span data-ttu-id="937df-247">贷记租赁资产</span><span class="sxs-lookup"><span data-stu-id="937df-247">Cr. Lease asset</span></span>                       |             | <span data-ttu-id="937df-248">71,235.81</span><span class="sxs-lookup"><span data-stu-id="937df-248">71,235.81</span></span>    |

11. <span data-ttu-id="937df-249">要查看使用权资产和租赁负债为 0（零）的终止的实际影响，打开负债和资产交易表。</span><span class="sxs-lookup"><span data-stu-id="937df-249">To view the net effect of the termination, where the ROU asset and lease liability will be 0 (zero), open the Liability and Asset transactions tables.</span></span>

<span data-ttu-id="937df-250">租赁状态现在应为 **已终止**。</span><span class="sxs-lookup"><span data-stu-id="937df-250">The lease status should now be **Terminated**.</span></span> <span data-ttu-id="937df-251">除非终止被冲销，否则不会针对此租赁过帐其他日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="937df-251">No additional journal entries will be posted against this lease unless the termination is reversed.</span></span>
