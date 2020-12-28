---
title: 减损使用权资产
description: 本主题描述用于记录减损和调整会计准则编纂专题 842 (ASC 842) 经营性租赁的资产折旧计划的功能。
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7a017cdbcbfa01d4dba383f2b6b7c742e54014e4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440964"
---
# <a name="impair-right-of-use-assets"></a><span data-ttu-id="c1d9f-103">减损使用权资产</span><span class="sxs-lookup"><span data-stu-id="c1d9f-103">Impair right-of-use assets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1d9f-104">如果使用权 (ROU) 资产的帐面金额无法收回，则可能必须测试该资产是否已减损。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-104">If a right-of-use (ROU) asset's carrying amount isn't recoverable, you might have to test whether the asset is impaired.</span></span> <span data-ttu-id="c1d9f-105">如果您确定资产已减损，资产租赁可以记录减损并相应地调整折旧计划。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-105">If you determine that the asset is impaired, Asset leasing can record the impairment and adjust the depreciation schedule accordingly.</span></span> <span data-ttu-id="c1d9f-106">本主题描述用于记录减损和调整会计准则编纂专题 842 (ASC 842) 经营性租赁的折旧计划的功能。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-106">This topic describes the functionality that records the impairment and adjusts the depreciation schedule of an Accounting Standards Codification Topic 842 (ASC 842) operating lease.</span></span> <span data-ttu-id="c1d9f-107">同样的方法也适用于国际财务报告准则 16 (IFRS 16) 租赁。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-107">The same method also applies to International Financial Reporting Standard 16 (IFRS 16) leases.</span></span>

<span data-ttu-id="c1d9f-108">使用权资产的剩余余额将按直线法在剩余期间内摊销，无论该租赁是根据 IFRS 16 归类为金融租赁还是根据 ASC 842 归类为经营性租赁。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-108">The remaining balance of the ROU asset will be amortized on a straight-line basis for the number of periods that remain, regardless of whether the lease was classified as a finance lease under IFRS 16 or an operating lease under ASC 842.</span></span>

## <a name="impair-an-rou-asset"></a><span data-ttu-id="c1d9f-109">减损使用权资产</span><span class="sxs-lookup"><span data-stu-id="c1d9f-109">Impair an ROU asset</span></span>

1. <span data-ttu-id="c1d9f-110">转到减损的租赁，然后选择 **帐簿**。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-110">Go to the impaired lease, and select **Books**.</span></span>
2. <span data-ttu-id="c1d9f-111">在操作窗格上，选择 **减损**。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-111">On the Action Pane, select **Impairment**.</span></span>
3. <span data-ttu-id="c1d9f-112">在出现的对话框的 **减损金额** 字段中，输入资产减损金额。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-112">In the dialog box that appears, in the **Impairment amount** field, enter the amount of the asset impairment.</span></span> <span data-ttu-id="c1d9f-113">要减少使用权资产，您应该输入一个正值。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-113">To decrease the ROU asset, you should enter a positive value.</span></span>
4. <span data-ttu-id="c1d9f-114">在 **交易日期** 字段中，输入应过帐减损条目的日期。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-114">In the **Transaction date** field, enter the date when the impairment entry should be posted.</span></span>
5. <span data-ttu-id="c1d9f-115">在 **剩余期间** 字段中，输入要摊销的剩余月数。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-115">In the **Periods remaining** field, enter the remaining number of months to amortize.</span></span>
6. <span data-ttu-id="c1d9f-116">如果希望系统自动过帐减损费用日记帐条目，请打开 **过帐** 参数。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-116">Turn on the **Post** parameter if you want the system to automatically post the impairment expense journal entry.</span></span> <span data-ttu-id="c1d9f-117">如果您将此参数保持关闭状态，则系统将创建条目，但不过帐。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-117">If you leave this parameter turned off, the system creates the entry but doesn't post it.</span></span> <span data-ttu-id="c1d9f-118">然后可以从 **资产租赁日记帐** 页过帐该条目。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-118">You can then post the entry from the **Asset lease journals** page.</span></span>
7. <span data-ttu-id="c1d9f-119">将 **过帐前预览** 选项设置为 **是** 以在创建或发布建议的条目之前查看。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-119">Set the **Preview before posting** option to **Yes** to view the proposed entry before it's created or posted.</span></span>
8. <span data-ttu-id="c1d9f-120">将 **关闭帐簿** 选项设置为 **是** 关闭租赁帐簿。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-120">Set the **Close book** option to **Yes** to close the lease book.</span></span> <span data-ttu-id="c1d9f-121">您无法撤消此操作。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-121">You can't undo this action.</span></span> <span data-ttu-id="c1d9f-122">不能针对已结租赁过帐条目，也不能调整已结租赁。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-122">Entries can't be posted against closed leases, and closed leases can't be adjusted.</span></span>
9. <span data-ttu-id="c1d9f-123">选择 **确定** 创建或过帐减损条目。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-123">Select **OK** to create or post the impairment entry.</span></span>
10. <span data-ttu-id="c1d9f-124">要查看减损的资产折旧计划，请打开该租赁帐簿的资产折旧计划。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-124">To view the impaired asset depreciation schedule, open the asset depreciation schedule for that lease book.</span></span> <span data-ttu-id="c1d9f-125">现在，将按直线法为资产折旧您在 **剩余期间** 字段中输入的月数。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-125">The asset will now be depreciated on a straight-line basis over the number of months that you entered in the **Periods remaining** field.</span></span>
11. <span data-ttu-id="c1d9f-126">要查看减损费用日记帐条目，请选择减损的租赁帐簿的操作窗格上的 **资产租赁日记帐**。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-126">To view the impairment expense journal entry, select **Asset leasing journal** on the Action Pane of the impaired lease book.</span></span> <span data-ttu-id="c1d9f-127">系统将创建一个日记帐条目，用于借记减损费用过帐科目和贷记租赁资产过帐科目。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-127">The system creates a journal entry that debits the impairment expense posting account and credits the lease asset posting account.</span></span>
12. <span data-ttu-id="c1d9f-128">要查看使用权资产的新帐面价值，请选择租赁帐簿的操作窗格上的 **资产交易**。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-128">To view the new carrying value of the ROU asset, select **Asset transactions** on the Action Pane of the lease book.</span></span>

## <a name="example-of-rou-asset-impairment"></a><span data-ttu-id="c1d9f-129">使用权资产减损的示例</span><span class="sxs-lookup"><span data-stu-id="c1d9f-129">Example of ROU asset impairment</span></span>

<span data-ttu-id="c1d9f-130">在此示例中，租赁是一种非专用资产，不会转移所有权或授予承租人购买选择权。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-130">For this example, the lease is a non-specialized asset that doesn't transfer ownership or grant the lessee the option to purchase.</span></span>

### <a name="setup"></a><span data-ttu-id="c1d9f-131">设置</span><span class="sxs-lookup"><span data-stu-id="c1d9f-131">Setup</span></span>

<span data-ttu-id="c1d9f-132">下面的表显示了在 **常规** 和 **付款计划行** 选项卡中为此示例中使用的租赁设置的值。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-132">The following tables show the values that are set on the **General** and **Payment schedule lines** tabs for the lease that is used in this example.</span></span>

<span data-ttu-id="c1d9f-133">**常规选项卡**</span><span class="sxs-lookup"><span data-stu-id="c1d9f-133">**General tab**</span></span>

| <span data-ttu-id="c1d9f-134">字段</span><span class="sxs-lookup"><span data-stu-id="c1d9f-134">Field</span></span>                      | <span data-ttu-id="c1d9f-135">值</span><span class="sxs-lookup"><span data-stu-id="c1d9f-135">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="c1d9f-136">资产的公平价值</span><span class="sxs-lookup"><span data-stu-id="c1d9f-136">Fair value of the asset</span></span>    | <span data-ttu-id="c1d9f-137">600,000</span><span class="sxs-lookup"><span data-stu-id="c1d9f-137">600,000</span></span>          |
| <span data-ttu-id="c1d9f-138">增量借贷利率</span><span class="sxs-lookup"><span data-stu-id="c1d9f-138">Incremental borrowing rate</span></span> | <span data-ttu-id="c1d9f-139">7%</span><span class="sxs-lookup"><span data-stu-id="c1d9f-139">7%</span></span>               |
| <span data-ttu-id="c1d9f-140">复合间隔</span><span class="sxs-lookup"><span data-stu-id="c1d9f-140">Compounding interval</span></span>       | <span data-ttu-id="c1d9f-141">每年</span><span class="sxs-lookup"><span data-stu-id="c1d9f-141">Annually</span></span>         |
| <span data-ttu-id="c1d9f-142">资产使用年限(月数)</span><span class="sxs-lookup"><span data-stu-id="c1d9f-142">Asset useful life (months)</span></span> | <span data-ttu-id="c1d9f-143">600</span><span class="sxs-lookup"><span data-stu-id="c1d9f-143">600</span></span>              |
| <span data-ttu-id="c1d9f-144">年金类型</span><span class="sxs-lookup"><span data-stu-id="c1d9f-144">Annuity type</span></span>               | <span data-ttu-id="c1d9f-145">普通年金</span><span class="sxs-lookup"><span data-stu-id="c1d9f-145">Ordinary annuity</span></span> |
| <span data-ttu-id="c1d9f-146">开始日期</span><span class="sxs-lookup"><span data-stu-id="c1d9f-146">Commencement date</span></span>          | <span data-ttu-id="c1d9f-147">01/01/2019</span><span class="sxs-lookup"><span data-stu-id="c1d9f-147">01/01/2019</span></span>       |

<span data-ttu-id="c1d9f-148">**付款计划行选项卡**</span><span class="sxs-lookup"><span data-stu-id="c1d9f-148">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="c1d9f-149">字段</span><span class="sxs-lookup"><span data-stu-id="c1d9f-149">Field</span></span>             | <span data-ttu-id="c1d9f-150">值</span><span class="sxs-lookup"><span data-stu-id="c1d9f-150">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="c1d9f-151">开始日期</span><span class="sxs-lookup"><span data-stu-id="c1d9f-151">Start date</span></span>        | <span data-ttu-id="c1d9f-152">1/1/2019</span><span class="sxs-lookup"><span data-stu-id="c1d9f-152">1/1/2019</span></span>   |
| <span data-ttu-id="c1d9f-153">期间间隔</span><span class="sxs-lookup"><span data-stu-id="c1d9f-153">Period interval</span></span>   | <span data-ttu-id="c1d9f-154">月度</span><span class="sxs-lookup"><span data-stu-id="c1d9f-154">Monthly</span></span>    |
| <span data-ttu-id="c1d9f-155">期间</span><span class="sxs-lookup"><span data-stu-id="c1d9f-155">Periods</span></span>           | <span data-ttu-id="c1d9f-156">120</span><span class="sxs-lookup"><span data-stu-id="c1d9f-156">120</span></span>        |
| <span data-ttu-id="c1d9f-157">结束日期</span><span class="sxs-lookup"><span data-stu-id="c1d9f-157">End date</span></span>          | <span data-ttu-id="c1d9f-158">12/31/2028</span><span class="sxs-lookup"><span data-stu-id="c1d9f-158">12/31/2028</span></span> |
| <span data-ttu-id="c1d9f-159">付款频率</span><span class="sxs-lookup"><span data-stu-id="c1d9f-159">Payment frequency</span></span> | <span data-ttu-id="c1d9f-160">每年</span><span class="sxs-lookup"><span data-stu-id="c1d9f-160">Annually</span></span>   |
| <span data-ttu-id="c1d9f-161">付款金额</span><span class="sxs-lookup"><span data-stu-id="c1d9f-161">Payment amount</span></span>    | <span data-ttu-id="c1d9f-162">10,000</span><span class="sxs-lookup"><span data-stu-id="c1d9f-162">10,000</span></span>     |

### <a name="steps"></a><span data-ttu-id="c1d9f-163">步骤</span><span class="sxs-lookup"><span data-stu-id="c1d9f-163">Steps</span></span>

1. <span data-ttu-id="c1d9f-164">按照本主题前面所述创建租赁后，转到租赁帐簿，并确认付款计划。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-164">After you create the lease as described earlier in this topic, go to the lease book, and confirm the payment schedule.</span></span> <span data-ttu-id="c1d9f-165">然后过帐初始确认日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-165">Then post the initial recognition journal entry.</span></span> <span data-ttu-id="c1d9f-166">初始使用权资产和租赁负债应为 70,235.81 美元。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-166">The initial ROU asset and lease liability should be $70,235.81.</span></span> <span data-ttu-id="c1d9f-167">对于此示例，根据 ASC 842，租赁被分类为经营性租赁。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-167">For this example, the lease was classified as an operating lease under ASC 842.</span></span>
2. <span data-ttu-id="c1d9f-168">运行批处理日记帐流程三遍，模拟三年的租赁付款、利息费用和折旧费用过程。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-168">Run the batch journal process three times to simulate the passage of three years for the lease payments, interest expenses, and depreciation expenses.</span></span>
3. <span data-ttu-id="c1d9f-169">运行完所有三个批处理作业后，回到租赁帐簿，然后打开负债和资产交易表以查看使用权资产和租赁负债的当前帐面价值。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-169">After you've finished running all three batch jobs, go back to the lease book, and open the liability and asset transactions tables to view the current carrying value of the ROU asset and lease liability.</span></span> <span data-ttu-id="c1d9f-170">三年后，负债的价值应该为大约 -53,893.00 美元，资产的价值应该大约为 53,893.00 美元。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-170">After three years, the value of the liability should be approximately $-53,893.00, and the value of the asset should be approximately $53,893.00.</span></span> 

    <span data-ttu-id="c1d9f-171">三年后，企业进行减损测试并确定使用权资产的减损为 35,000 美元。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-171">After three years, the business does impairment tests and determines that the ROU asset has an impairment of $35,000.</span></span> <span data-ttu-id="c1d9f-172">您现在必须记录此减损。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-172">You must now record this impairment.</span></span>
    
4. <span data-ttu-id="c1d9f-173">转到租赁帐簿，然后在“操作”窗格上，选择 **减损**。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-173">Go to the lease book, and then, on the Action Pane, select **Impairment**.</span></span>
5. <span data-ttu-id="c1d9f-174">在 **减损参数** 页面上，输入以下详细信息。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-174">On the **Impairment parameter** page, enter the following details.</span></span>

    | <span data-ttu-id="c1d9f-175">字段</span><span class="sxs-lookup"><span data-stu-id="c1d9f-175">Field</span></span>                  | <span data-ttu-id="c1d9f-176">值</span><span class="sxs-lookup"><span data-stu-id="c1d9f-176">Value</span></span>    |
    |------------------------|----------|
    | <span data-ttu-id="c1d9f-177">减损金额</span><span class="sxs-lookup"><span data-stu-id="c1d9f-177">Impairment amount</span></span>      | <span data-ttu-id="c1d9f-178">35,000</span><span class="sxs-lookup"><span data-stu-id="c1d9f-178">35,000</span></span>   |
    | <span data-ttu-id="c1d9f-179">交易日期</span><span class="sxs-lookup"><span data-stu-id="c1d9f-179">Transaction date</span></span>       | <span data-ttu-id="c1d9f-180">1/1/2022</span><span class="sxs-lookup"><span data-stu-id="c1d9f-180">1/1/2022</span></span> |
    | <span data-ttu-id="c1d9f-181">剩余期间</span><span class="sxs-lookup"><span data-stu-id="c1d9f-181">Periods remaining</span></span>      | <span data-ttu-id="c1d9f-182">84</span><span class="sxs-lookup"><span data-stu-id="c1d9f-182">84</span></span>       |
    | <span data-ttu-id="c1d9f-183">过帐</span><span class="sxs-lookup"><span data-stu-id="c1d9f-183">Post</span></span>                   | <span data-ttu-id="c1d9f-184">是</span><span class="sxs-lookup"><span data-stu-id="c1d9f-184">Yes</span></span>      |
    | <span data-ttu-id="c1d9f-185">在过帐前预览</span><span class="sxs-lookup"><span data-stu-id="c1d9f-185">Preview before posting</span></span> | <span data-ttu-id="c1d9f-186">不</span><span class="sxs-lookup"><span data-stu-id="c1d9f-186">No</span></span>       |
    | <span data-ttu-id="c1d9f-187">关闭帐簿</span><span class="sxs-lookup"><span data-stu-id="c1d9f-187">Close book</span></span>             | <span data-ttu-id="c1d9f-188">不</span><span class="sxs-lookup"><span data-stu-id="c1d9f-188">No</span></span>       |

6. <span data-ttu-id="c1d9f-189">已创建并过帐了减损费用日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-189">An impairment expense journal entry has been created and posted.</span></span> <span data-ttu-id="c1d9f-190">要查看，请转到租赁帐簿中的资产租赁日记帐。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-190">To view it, go to the asset's leasing journal in the lease book.</span></span> <span data-ttu-id="c1d9f-191">请注意，减损金额已记入减损费用过帐科目，而使用权资产过帐科目已贷记。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-191">Notice that the amount of the impairment was debited to the Impairment expense posting account, and the ROU asset posting account was credited.</span></span>
7. <span data-ttu-id="c1d9f-192">要查看减损的实际影响，请转到负债和资产交易表。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-192">To view the net effect of the impairment, go to the liability and asset transactions tables.</span></span> <span data-ttu-id="c1d9f-193">请注意，减损费用导致了使用权资产减少，但租赁负债的帐面价值未发生变化。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-193">Notice that the impairment expense has decreased the ROU asset, but the carrying amount of the lease liability hasn't changed.</span></span>

<span data-ttu-id="c1d9f-194">减损还有一项您应考虑的影响。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-194">The impairment has one other effect that you should consider.</span></span> <span data-ttu-id="c1d9f-195">由于使用权资产金额现在远小于租赁负债，因此折旧金额必须与以前不同。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-195">Because the ROU asset amount is now much less than the lease liability, the amount must be depreciated differently than it was before.</span></span> <span data-ttu-id="c1d9f-196">具体来说，现在从交易日期开始，在整个剩余的 84 个月的租赁中以直线法折旧资产。</span><span class="sxs-lookup"><span data-stu-id="c1d9f-196">Specifically, the asset is now depreciated in a straight-line manner throughout the remaining 84 months of the lease, beginning on the transaction date.</span></span>
