---
title: 年终结算缺少期初余额
description: 本主题介绍了进行年终结算时为什么可能会缺少期初余额，以及缺少期初余额时如何重新生成这些余额。
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028551"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="9f06d-103">年终结算缺少期初余额</span><span class="sxs-lookup"><span data-stu-id="9f06d-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f06d-104">本主题介绍了进行年终结算时为什么可能会缺少期初余额，以及缺少期初余额时如何重新生成这些余额。</span><span class="sxs-lookup"><span data-stu-id="9f06d-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="9f06d-105">问题</span><span class="sxs-lookup"><span data-stu-id="9f06d-105">Symptom</span></span>

<span data-ttu-id="9f06d-106">为什么运行总帐年终结算之后没有期初余额？</span><span class="sxs-lookup"><span data-stu-id="9f06d-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="9f06d-107">解决方法</span><span class="sxs-lookup"><span data-stu-id="9f06d-107">Resolution</span></span>

<span data-ttu-id="9f06d-108">如果您进行总帐年终结算，但生成的试算平衡表未显示下一会计年度的期初余额，可以检查下面几个方面：</span><span class="sxs-lookup"><span data-stu-id="9f06d-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="9f06d-109">如果 **撤消上一次结算** 字段设置为 **是**，将冲销同一会计年度的上一次年终结算。</span><span class="sxs-lookup"><span data-stu-id="9f06d-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="9f06d-110">运行冲销年终结算的流程时，将删除有关期末余额和期初余额的所有条目，好像从未进行年终结算一样。</span><span class="sxs-lookup"><span data-stu-id="9f06d-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="9f06d-111">此外，还将删除凭证。</span><span class="sxs-lookup"><span data-stu-id="9f06d-111">The vouchers are also deleted.</span></span> <span data-ttu-id="9f06d-112">将不会自动重新运行年终结算流程。</span><span class="sxs-lookup"><span data-stu-id="9f06d-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="9f06d-113">您必须重新启动该流程，此时会将 **撤消上一次结算** 选项更新为 **否**。</span><span class="sxs-lookup"><span data-stu-id="9f06d-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="9f06d-114">年终结算常见问题解答主题中介绍了此情况。</span><span class="sxs-lookup"><span data-stu-id="9f06d-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="9f06d-115">有关详细信息，请参阅[年终活动常见问题解答](faq-year-end-activities.md)。</span><span class="sxs-lookup"><span data-stu-id="9f06d-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="9f06d-116">问题</span><span class="sxs-lookup"><span data-stu-id="9f06d-116">Symptom</span></span>

<span data-ttu-id="9f06d-117">我在 **撤消上一次结算** 选项设置为 **否** 的情况下运行了年终结算，但我的会计年度仍没有期初余额。</span><span class="sxs-lookup"><span data-stu-id="9f06d-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="9f06d-118">解决方法</span><span class="sxs-lookup"><span data-stu-id="9f06d-118">Resolution</span></span>

<span data-ttu-id="9f06d-119">请首先检查批处理作业的状态。</span><span class="sxs-lookup"><span data-stu-id="9f06d-119">First check the status of the batch job.</span></span> <span data-ttu-id="9f06d-120">年终结算包括多项单独的任务，但是最关键的步骤是批处理任务，**步骤 5.0.0** 中提供了相关任务说明。</span><span class="sxs-lookup"><span data-stu-id="9f06d-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="9f06d-121">在此步骤期间中，会将期初交易记录和可选的期末交易记录过帐到总帐。</span><span class="sxs-lookup"><span data-stu-id="9f06d-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="9f06d-122">[![批处理历史记录列表](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="9f06d-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="9f06d-123">如果此步骤成功完成，但您在 **试算平衡表查询** 页面上看不到期初余额（**总帐 > 查询和报表 > 试算平衡表**），请查看年终结算批处理作业的结果，以了解是否已成功完成“重新生成余额”步骤。</span><span class="sxs-lookup"><span data-stu-id="9f06d-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="9f06d-124">[![年终结算批处理作业的结果](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="9f06d-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="9f06d-125">如果此步骤由于任何原因而失败，则可能已成功过帐期初（和可选的期末）交易记录。</span><span class="sxs-lookup"><span data-stu-id="9f06d-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="9f06d-126">您可以使用 **凭证交易记录查询** 页面来验证是否已成功过帐总帐交易记录，方法是为所结算的年份指定年终结算对话框上提供的凭证编号和日期（**总帐 > 查询和报表 > 凭证交易记录**）。</span><span class="sxs-lookup"><span data-stu-id="9f06d-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="9f06d-127">[![凭证交易记录查询](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="9f06d-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="9f06d-128">如果存在期初（和可选的期末）凭证，则无需再次运行年终结算。</span><span class="sxs-lookup"><span data-stu-id="9f06d-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="9f06d-129">请参阅下一部分了解有关如何继续的信息。</span><span class="sxs-lookup"><span data-stu-id="9f06d-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="9f06d-130">问题</span><span class="sxs-lookup"><span data-stu-id="9f06d-130">Symptom</span></span>

<span data-ttu-id="9f06d-131">年终结算中的“重新生成余额”步骤失败，我是否需要重新运行整个年终结算流程？</span><span class="sxs-lookup"><span data-stu-id="9f06d-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="9f06d-132">解决方法</span><span class="sxs-lookup"><span data-stu-id="9f06d-132">Resolution</span></span>

<span data-ttu-id="9f06d-133">“重新生成余额”步骤会更新在生成试算平衡表查询时使用的总帐余额。</span><span class="sxs-lookup"><span data-stu-id="9f06d-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="9f06d-134">这是年终结算流程中的最后一步。</span><span class="sxs-lookup"><span data-stu-id="9f06d-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="9f06d-135">如果此步骤是唯一失败的步骤，则说明已成功过帐总帐交易记录。</span><span class="sxs-lookup"><span data-stu-id="9f06d-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="9f06d-136">无需再次运行年终结算。</span><span class="sxs-lookup"><span data-stu-id="9f06d-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="9f06d-137">您可以运行该流程以使用 **财务维度集** 页面（**总帐 > 会计科目表 > 维度 > 财务维度集**）手动重新生成余额。</span><span class="sxs-lookup"><span data-stu-id="9f06d-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="9f06d-138">[![“财务维度集”页面上的“重新生成余额”按钮](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="9f06d-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="9f06d-139">如果此步骤需要较长的时间才能完成，我们建议您按照[更新财务维度集的最佳实践](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets)中所述查看财务维度集的最佳实践。</span><span class="sxs-lookup"><span data-stu-id="9f06d-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

