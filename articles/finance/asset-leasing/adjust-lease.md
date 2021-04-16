---
title: 调整租赁
description: 此主题说明如何调整租赁。 如果修改了租赁条款，延长了租赁期限或其他情况发生了变化，可能需要进行调整。
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
ms.openlocfilehash: 1dce99e9fb553cce8de9cefc7e01c8755e9d2090
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825763"
---
# <a name="adjust-leases"></a><span data-ttu-id="36e1b-104">调整租赁</span><span class="sxs-lookup"><span data-stu-id="36e1b-104">Adjust leases</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="36e1b-105">此主题说明如何调整租赁。</span><span class="sxs-lookup"><span data-stu-id="36e1b-105">The topic explains how to adjust a lease.</span></span> <span data-ttu-id="36e1b-106">如果修改了租赁条款，延长了租赁期限或其他情况发生了变化，可能需要进行调整。</span><span class="sxs-lookup"><span data-stu-id="36e1b-106">Adjustment might be required if the lease terms are modified, the lease is extended, or other circumstances change.</span></span> <span data-ttu-id="36e1b-107">资产租赁应该遵守会计准则编纂专题 842 (ASC 842) 和国际财务报告准则 16 (IFRS 16) 提供的有关租赁修改的指导。</span><span class="sxs-lookup"><span data-stu-id="36e1b-107">Asset leasing complies with the guidance that Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16) provide about lease modifications.</span></span> <span data-ttu-id="36e1b-108">ASC 842-20-15-1 将租赁修改定义为对合同的条款和条件进行的任何会导致租赁的范围或注意事项改变的更改。</span><span class="sxs-lookup"><span data-stu-id="36e1b-108">ASC 842-20-15-1 defines a lease modification as any change to the terms and conditions of a contract that causes a change in the scope of, or the consideration for, a lease.</span></span> <span data-ttu-id="36e1b-109">IFRS 16 第 39 段规定，承租人必须对租赁负债进行重估，以反映租赁付款的变化。</span><span class="sxs-lookup"><span data-stu-id="36e1b-109">Paragraph 39 of IFRS 16 states that a lessee must revalue the lease liability so that it reflects changes to the lease payments.</span></span>

<span data-ttu-id="36e1b-110">对于遵守 ASC 842 或 IFRS 16 的组织，将重新度量租赁以反映未来最低租赁付款 (PVFMLP) 的现值变化。</span><span class="sxs-lookup"><span data-stu-id="36e1b-110">For organizations that adhere to ASC 842 or IFRS 16, a lease is remeasured to reflect a change in the present value of the future minimum lease payments (PVFMLP).</span></span> <span data-ttu-id="36e1b-111">如果 PVFMLP 增加，则创建的日记帐条目将是使用权 (ROU) 资产科目的借方，是新 PVFMLP 与先前 PVFMLP 之间的差额的租赁负债科目的贷方。</span><span class="sxs-lookup"><span data-stu-id="36e1b-111">If the PVFMLP increases, the journal entry that is created will be a debit to the right-of-use (ROU) asset account and a credit to the lease liability account for the difference between the new PVFMLP and the previous PVFMLP.</span></span> <span data-ttu-id="36e1b-112">如果 PVFMLP 减少，则日记帐条目将是租赁负债科目的借方，是差额的使用权资产科目的贷方。</span><span class="sxs-lookup"><span data-stu-id="36e1b-112">If the PVFMLP decreases, the journal entry will be a debit to the lease liability account and a credit to the ROU asset account for the difference.</span></span>

<span data-ttu-id="36e1b-113">如果调整将使用权资产减少到低于 0（零），则剩余部分将记入在 **租赁过帐科目** 页指定的租赁修改过帐科目中的收益。</span><span class="sxs-lookup"><span data-stu-id="36e1b-113">If the adjustment decreases the ROU asset past 0 (zero), the remainder will be credited to the gain on lease modification posting account that is specified on the **Lease posting accounts** page.</span></span> <span data-ttu-id="36e1b-114">系统将考虑这些交易和其他调整条目，如因租赁修改而产生的分类变更、初始直接成本、租赁奖励、预付款和拆除成本。</span><span class="sxs-lookup"><span data-stu-id="36e1b-114">The system accounts for these transactions and other adjustment entries, such as classification changes, initial direct costs, lease incentives, prepayments, and dismantling costs that arise from lease modifications.</span></span>

<span data-ttu-id="36e1b-115">有关租赁调整交易的具体指导，我们建议您参阅 IFRS 16 和 ASC 842。</span><span class="sxs-lookup"><span data-stu-id="36e1b-115">For specific guidance about lease adjustment transactions, we recommend that you see IFRS 16 and ASC 842.</span></span>

## <a name="lease-adjustment-wizard"></a><span data-ttu-id="36e1b-116">租赁调整向导</span><span class="sxs-lookup"><span data-stu-id="36e1b-116">Lease adjustment wizard</span></span>

<span data-ttu-id="36e1b-117">要调整租赁，请完成以下步骤。</span><span class="sxs-lookup"><span data-stu-id="36e1b-117">To adjust a lease, complete the following steps.</span></span> <span data-ttu-id="36e1b-118">修改后的数据将在您从 **租赁调整** 向导发布后更新租赁计划。</span><span class="sxs-lookup"><span data-stu-id="36e1b-118">The modified data will update lease schedules after you post from the **Lease adjustment** wizard.</span></span> <span data-ttu-id="36e1b-119">您可以随时保存工作并关闭向导，然后在以后返回继续工作。</span><span class="sxs-lookup"><span data-stu-id="36e1b-119">You can save your work and close the wizard at any time, and then come back later to resume your work.</span></span>

<span data-ttu-id="36e1b-120">要从租赁摘要打开 **租赁调整** 向导，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="36e1b-120">To open the **Lease adjustment** wizard from the lease summary, follow these steps.</span></span>

1. <span data-ttu-id="36e1b-121">转到 **资产租赁 \> 租赁 \> 租赁摘要**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-121">Go to **Asset leasing \> Leases \> Lease summary**.</span></span> 
2. <span data-ttu-id="36e1b-122">选择要调整的租赁，然后选择 **调整向导**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-122">Select the lease to adjust, and then select **Adjustment wizard**.</span></span>
3. <span data-ttu-id="36e1b-123">按照向导中的提示输入所需的更改。</span><span class="sxs-lookup"><span data-stu-id="36e1b-123">Follow the prompts in the wizard to enter the required changes.</span></span>

<span data-ttu-id="36e1b-124">要从 **租赁调整** 页打开 **租赁调整** 向导，对于已经进行的调整，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="36e1b-124">To open the **Lease adjustment** wizard from the **Lease adjustments** page, for an adjustment that is already in progress, follow these steps.</span></span>

1.  <span data-ttu-id="36e1b-125">转到 **租赁 \> 租赁 \> 租赁调整**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-125">Go to **Lease \> Leases \> Lease adjustments**.</span></span>
2.  <span data-ttu-id="36e1b-126">选择调整状态为 **进行中** 的租赁，然后选择 **调整向导**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-126">Select a lease that has an adjustment status of **In progress**, and then select **Adjustment wizard**.</span></span>
3.  <span data-ttu-id="36e1b-127">在 **修改开始日期** 和 **发布日期** 字段中，输入适当的日期。</span><span class="sxs-lookup"><span data-stu-id="36e1b-127">In the **Modification start date** and **Posting date** fields, enter the appropriate dates.</span></span>
4.  <span data-ttu-id="36e1b-128">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-128">Select **Next**.</span></span>

    <span data-ttu-id="36e1b-129">租赁现在已被添加到 **租赁调整** 页，您可以在页面中输入有关它的新信息。</span><span class="sxs-lookup"><span data-stu-id="36e1b-129">The lease is now added to the **Lease adjustments** page, where you can enter the new information about it.</span></span>

    <span data-ttu-id="36e1b-130">租赁调整后，将应用使用权注意事项字段。</span><span class="sxs-lookup"><span data-stu-id="36e1b-130">After the lease has been adjusted, the right-of-use considerations fields apply to it.</span></span> <span data-ttu-id="36e1b-131">如果没有初始直接成本、租赁奖励、预付款或拆除成本与修改后的租赁相关联，应将相应字段留空。</span><span class="sxs-lookup"><span data-stu-id="36e1b-131">If no initial direct costs, lease incentives, prepayments, or dismantling costs are associated with the modified lease, leave the corresponding fields blank.</span></span> <span data-ttu-id="36e1b-132">原始金额将不应用于更新后的租赁。</span><span class="sxs-lookup"><span data-stu-id="36e1b-132">The original amounts won't apply to the updated lease.</span></span> 

    <span data-ttu-id="36e1b-133">例如，出租人对同意延长租赁提供 1,000 美元的奖励。</span><span class="sxs-lookup"><span data-stu-id="36e1b-133">For example, a lessor provides a $1,000 incentive for agreeing to a lease extension.</span></span> <span data-ttu-id="36e1b-134">在这种情况下，当您调整租赁以延长期限时，请在 **调整产生的租赁奖励** 字段中输入 **1,000**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-134">In this case, when you adjust the lease to account for the extension, enter **1,000** in the **Lease incentives arising from adjustment** field.</span></span>

    <span data-ttu-id="36e1b-135">现在，付款计划行会在 **修改开始日期** 字段中显示当月及以后月份的所有付款。</span><span class="sxs-lookup"><span data-stu-id="36e1b-135">The payment schedule lines now show all payments from the month, and later months, in the **Modification start date** field.</span></span> <span data-ttu-id="36e1b-136">由于预期会进行修改，因此付款计划行不能在修改开始之前开始。</span><span class="sxs-lookup"><span data-stu-id="36e1b-136">Because modifications are prospective, payment schedule lines can't start before the modification starts.</span></span> <span data-ttu-id="36e1b-137">要查看修改开始日期之前的付款计划行，请转到 **租赁版本历史记** 页。</span><span class="sxs-lookup"><span data-stu-id="36e1b-137">To view payment schedule lines from before the modification start date, go to the **Lease version history** page.</span></span>

8.  <span data-ttu-id="36e1b-138">选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-138">Select **Next**.</span></span>

    <span data-ttu-id="36e1b-139">下一页将显示有关预期租赁调整的关键详细信息，如修改前的租赁负债和修改后的新的预期租赁负债的结转值。</span><span class="sxs-lookup"><span data-stu-id="36e1b-139">The next page shows key details about the expected lease adjustment, such as the carrying values of the lease liability before the modification and the new expected lease liability after the modification.</span></span> <span data-ttu-id="36e1b-140">此页面还将显示预期租赁调整的日记帐条目的预览。</span><span class="sxs-lookup"><span data-stu-id="36e1b-140">The page also shows a preview of the journal entry for the expected lease adjustment.</span></span>

9.  <span data-ttu-id="36e1b-141">如果赁调整工作流处于活动状态且调整尚未批准，请选择 **提交到工作流** 将租赁调整提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="36e1b-141">Select **Submit to workflow** to submit the lease adjustment to the workflow system if the lease adjustment workflow is active and the adjustment hasn't yet been approved.</span></span> <span data-ttu-id="36e1b-142">有关如何使用租赁调整工作流的详细信息，请参阅[使用租赁调整工作流](use-create-lease-wrkflw.md)。</span><span class="sxs-lookup"><span data-stu-id="36e1b-142">For more information about how to use the lease adjustment workflow, see [Use lease adjustments workflows](use-create-lease-wrkflw.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="36e1b-143">此时，系统将重新计算调整变量，以验证自首次计算调整概览和调整日记帐条目以来，没有针对租赁发布任何交易。</span><span class="sxs-lookup"><span data-stu-id="36e1b-143">At this point, the system recalculates the adjustment variables to verify that no transactions have been posted against the lease since the adjustment overview and adjustment journal entry were first calculated.</span></span> <span data-ttu-id="36e1b-144">如果任何值发生更改，调整概览网格将更新，您可以查看信息，然后再将租赁调整提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="36e1b-144">If any values change, the adjustment overview grid is updated, and you can review the information before you resubmit the lease adjustments to the workflow system.</span></span>

10. <span data-ttu-id="36e1b-145">如果工作流不是活动状态，或者租赁调整已获批准，请选择 **完成** 处理更改并发布调整日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="36e1b-145">If a workflow isn't active, or if the lease adjustment has been approved, select **Finish** to process the changes and post the adjustment journal entry.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="36e1b-146">此时，系统将重新计算调整变量，以验证自首次计算调整概览和调整日记帐条目以来，没有针对租赁发布任何交易。</span><span class="sxs-lookup"><span data-stu-id="36e1b-146">At this point, the system recalculates the adjustment variables to verify that no transactions have been posted against the lease since the adjustment overview and adjustment journal entry were first calculated.</span></span> <span data-ttu-id="36e1b-147">如果有任何值更改，调整概览网格将更新，您可以在选择 **完成** 之前查看更改。</span><span class="sxs-lookup"><span data-stu-id="36e1b-147">If any values change, the adjustment overview grid is updated, and you can review the changes before you select **Finish**.</span></span> <span data-ttu-id="36e1b-148">如果工作流处于活动状态并且租赁调整已获批准，对调整概览的任何更改都将导致将审批状态重新设置为 **未提交**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-148">If the workflow is active and the lease adjustment has been approved, any changes to the adjustment overview will cause the approval status to be set back to **Not submitted**.</span></span> <span data-ttu-id="36e1b-149">在这种情况下，您应该将租赁调整重新提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="36e1b-149">In this case, you should resubmit the lease adjustment to the workflow system.</span></span>

    <span data-ttu-id="36e1b-150">在 **租赁调整** 页上，调整状态现在将设置为 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-150">On the **Lease adjustments** page, the adjustment status is now set to **Completed**.</span></span>

    <span data-ttu-id="36e1b-151">在 **租赁调整** 页上，您仍然可以查看 **调整概览** 和 **调整条目预览** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="36e1b-151">On the **Lease adjustments** page, you can still view the **Adjustment overview** and **Adjustment entry preview** FastTabs.</span></span> <span data-ttu-id="36e1b-152">租赁详细信息和日期信息显示在该租赁的版本历史记录中。</span><span class="sxs-lookup"><span data-stu-id="36e1b-152">The lease details and date information are shown in the version history of that lease.</span></span>

    <span data-ttu-id="36e1b-153">新租赁版本和新计划集现在可以使用修改后的信息创建。</span><span class="sxs-lookup"><span data-stu-id="36e1b-153">A new lease version and a new set of schedules are now created by using the modified information.</span></span> 

13. <span data-ttu-id="36e1b-154">要查看新计划，请转到租赁，然后选择 **帐簿**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-154">To view the new schedules, go to the lease, and then select **Books**.</span></span>
14. <span data-ttu-id="36e1b-155">要查看新生成的付款计划，请选择 **付款计划**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-155">To view the newly generated payment schedule, select **Payment schedule**.</span></span>
15. <span data-ttu-id="36e1b-156">要查看从新信息生成的新租赁负债摊销计划，请关闭 **付款计划** 页，然后打开 **负债摊销计划** 页。</span><span class="sxs-lookup"><span data-stu-id="36e1b-156">To view the new lease liability amortization schedule that is generated from the new information, close the **Payment schedule** page, and open the **Liability amortization schedule** page.</span></span>
16. <span data-ttu-id="36e1b-157">要查看新生成的资产折旧计划，请从 **帐簿详细信息** 页打开 **资产折旧计划** 页。</span><span class="sxs-lookup"><span data-stu-id="36e1b-157">To view the newly generated asset depreciation schedule, open the **Asset depreciation schedule** page from the **Book details** page.</span></span>
17. <span data-ttu-id="36e1b-158">要查看调整日记帐条目，请选择 **日记帐 \> 资产租赁日记帐**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-158">To view the adjustment journal entry, select **Journals \> Asset leasing journal**.</span></span>

## <a name="cancel-a-lease-adjustment"></a><span data-ttu-id="36e1b-159">取消租赁调整</span><span class="sxs-lookup"><span data-stu-id="36e1b-159">Cancel a lease adjustment</span></span>

<span data-ttu-id="36e1b-160">要删除正在进行的租赁调整，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="36e1b-160">To delete a lease adjustment that is in progress, follow these steps.</span></span>

1.  <span data-ttu-id="36e1b-161">转到 **租赁 \> 租赁 \> 租赁调整**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-161">Go to **Lease \> Leases \> Lease adjustments**.</span></span>
2.  <span data-ttu-id="36e1b-162">选择要取消的正在进行的租赁调整。</span><span class="sxs-lookup"><span data-stu-id="36e1b-162">Select that in-progress lease adjustment to cancel.</span></span>
3.  <span data-ttu-id="36e1b-163">选择 **取消调整**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-163">Select **Cancel adjustment**.</span></span> 
4.  <span data-ttu-id="36e1b-164">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-164">Select **OK**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="36e1b-165">如果您在 **租赁调整** 向导中选择 **取消**，将回滚您在向导中完成的最新更改，但不会删除正在进行的调整。</span><span class="sxs-lookup"><span data-stu-id="36e1b-165">If you select **Cancel** in the **Lease adjustment** wizard, you roll back the most recent change that you completed in the wizard, but you don't remove an adjustment that is in progress.</span></span>

## <a name="use-the-lease-adjustment-workflow"></a><span data-ttu-id="36e1b-166">使用租赁调整工作流</span><span class="sxs-lookup"><span data-stu-id="36e1b-166">Use the lease adjustment workflow</span></span>

<span data-ttu-id="36e1b-167">本节说明如何使用租赁调整工作流。</span><span class="sxs-lookup"><span data-stu-id="36e1b-167">This section explains how to use the lease adjustment workflow.</span></span> <span data-ttu-id="36e1b-168">租赁调整工作流通过提供一组审批步骤并将其分配给在调整最终确定前审批租赁调整的特定用户，来帮助您以一致的方式管理租赁调整。</span><span class="sxs-lookup"><span data-stu-id="36e1b-168">The lease adjustment workflow helps you manage lease adjustments in a consistent manner by providing a set of approval steps and assigning them to specific users who approve a lease adjustment before it becomes final.</span></span> <span data-ttu-id="36e1b-169">租赁调整在工作流中获得批准后，您可以使用 **租赁调整** 向导完成租赁调整。</span><span class="sxs-lookup"><span data-stu-id="36e1b-169">After the lease adjustment is approved in the workflow, you can use the **Lease adjustment** wizard to complete the lease adjustment.</span></span>

1.  <span data-ttu-id="36e1b-170">要提交租赁调整以进行审批，转到 **租赁 \> 租赁 \> 租赁调整**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-170">To submit a lease adjustment for approval, go to **Lease \> Leases \> Lease adjustments**.</span></span>
2.  <span data-ttu-id="36e1b-171">选择租赁调整的租赁 ID，然后选择 **调整向导**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-171">Select the lease ID of the lease adjustment, and then select **Adjustment wizard**.</span></span>
3.  <span data-ttu-id="36e1b-172">在向导的最后一页上，选择 **提交以供审批**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-172">On the last page of the wizard, select **Submit for approval**.</span></span>
4.  <span data-ttu-id="36e1b-173">输入有关调整的注释，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-173">Enter a comment about the adjustment, and then select **OK**.</span></span>

    <span data-ttu-id="36e1b-174">工作流状态将更改为 **等待审批**，向导中的所有字段都将被锁定，无法进行编辑。</span><span class="sxs-lookup"><span data-stu-id="36e1b-174">The workflow status is changed to **Pending approval**, and all the fields in the wizard are locked for editing.</span></span>

5.  <span data-ttu-id="36e1b-175">要审批租赁调整，转到 **租赁 \> 租赁 \> 租赁调整**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-175">To approve the lease adjustment, go to **Lease \> Leases \> Lease adjustments**.</span></span>
6.  <span data-ttu-id="36e1b-176">选择租赁调整的租赁 ID，查看 **调整概览** 和 **调整条目预览** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="36e1b-176">Select the lease ID of the lease adjustment, and review the **Adjustment overview** and **Adjustment entry preview** FastTabs.</span></span>
7.  <span data-ttu-id="36e1b-177">选择 **工作流 \> 已批准**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-177">Select **Workflow \> Approved**.</span></span>

    <span data-ttu-id="36e1b-178">在 **租赁调整** 页上，工作流状态现在将设置为 **已批准**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-178">On the **Lease adjustments** page, the workflow status is now set to **Approved**.</span></span> <span data-ttu-id="36e1b-179">此时，租赁调整已经准备好通过调整日记帐条目发布。</span><span class="sxs-lookup"><span data-stu-id="36e1b-179">At this point, the lease adjustment is ready to be posted through the adjustment journal entry.</span></span>

8.  <span data-ttu-id="36e1b-180">要继续处理租赁调整和发布调整条目，请转到 **租赁 \> 租赁 \> 租赁调整**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-180">To continue to process the lease adjustment and post the adjustment entry, go to **Lease \> Leases \> Lease adjustments**.</span></span>
9.  <span data-ttu-id="36e1b-181">选择租赁调整的租赁 ID，然后选择 **调整向导**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-181">Select the lease ID of the lease adjustment, and then select **Adjustment wizard**.</span></span>
10. <span data-ttu-id="36e1b-182">选择 **下一步** 直到到达向导的最后一页，然后选择 **完成**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-182">Select **Next** until you reach the last page of the wizard, and then select **Finish**.</span></span>

<span data-ttu-id="36e1b-183">系统将重新计算租赁的结转值，以确保批准的调整变量是最新的。</span><span class="sxs-lookup"><span data-stu-id="36e1b-183">The system recalculates the carrying values of the lease to ensure that the adjustment variables that were approved are current.</span></span> <span data-ttu-id="36e1b-184">如果有任何更改，审批状态将重新设置为 **草稿**，您应该将租赁调整重新提交到工作流系统。</span><span class="sxs-lookup"><span data-stu-id="36e1b-184">If there are any changes, the approval status is set back to **Draft**, and you should resubmit the lease adjustment to the workflow system.</span></span>

## <a name="view-lease-versions"></a><span data-ttu-id="36e1b-185">查看租赁版本</span><span class="sxs-lookup"><span data-stu-id="36e1b-185">View lease versions</span></span>

<span data-ttu-id="36e1b-186">如果已调整租赁，则可以查看其不同版本。</span><span class="sxs-lookup"><span data-stu-id="36e1b-186">If a lease has been adjusted, you can view the different versions of it.</span></span> <span data-ttu-id="36e1b-187">您还可以查看历史计划和过去的租赁详细信息。</span><span class="sxs-lookup"><span data-stu-id="36e1b-187">You can also view the historical schedules and past lease details.</span></span>

1. <span data-ttu-id="36e1b-188">在 **租赁摘要** 页面上，选择租赁，然后在“操作”窗格上选择 **租赁版本历史记录**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-188">On the **Lease summary** page, select the lease, and then, on the Action Pane, select **Lease version history**.</span></span>

    <span data-ttu-id="36e1b-189">如果已调整所选租赁，**租赁版本历史记录** 页将显示其他版本。</span><span class="sxs-lookup"><span data-stu-id="36e1b-189">If the selected lease has been adjusted, the **Lease version history** page shows the different versions.</span></span> <span data-ttu-id="36e1b-190">原始租赁带有标签 **1个**，后续版本采用升序数字顺序。</span><span class="sxs-lookup"><span data-stu-id="36e1b-190">The original lease is labeled **1**, and subsequent versions have ascending numerical order.</span></span>

    <span data-ttu-id="36e1b-191">对于选定的租赁版本，您可以查看财务维度、合同明细、位置和付款计划行。</span><span class="sxs-lookup"><span data-stu-id="36e1b-191">For a selected lease version, you can view the financial dimensions, contract details, location, and payment schedule lines.</span></span>

2. <span data-ttu-id="36e1b-192">要查看历史计划，请从 **租赁摘要** 页上选择所需帐簿，然后在“操作窗格”上选择 **帐簿版本历史记录**。</span><span class="sxs-lookup"><span data-stu-id="36e1b-192">To view historical schedules, open the modified lease from the **Lease summary** page, select the desired book, and then, on the Action Pane, select **Book version history**.</span></span>
3. <span data-ttu-id="36e1b-193">在 **帐簿版本** 页上，选择要查看的版本和计划。</span><span class="sxs-lookup"><span data-stu-id="36e1b-193">On the **Book version** page, select a version and a schedule to view.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]