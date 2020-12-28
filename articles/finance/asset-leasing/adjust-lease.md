---
title: 调整租赁
description: 此主题说明如何调整租赁。 如果修改了租赁条款，延长了租赁期限或其他情况发生了变化，可能需要进行调整。
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
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/28/2020
ms.locfileid: "4440966"
---
# <a name="adjust-leases"></a><span data-ttu-id="31ef9-104">调整租赁</span><span class="sxs-lookup"><span data-stu-id="31ef9-104">Adjust leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31ef9-105">此主题说明如何调整租赁。</span><span class="sxs-lookup"><span data-stu-id="31ef9-105">The topic explains how to adjust a lease.</span></span> <span data-ttu-id="31ef9-106">如果修改了租赁条款，延长了租赁期限或其他情况发生了变化，可能需要进行调整。</span><span class="sxs-lookup"><span data-stu-id="31ef9-106">Adjustment might be required if the lease terms are modified, the lease is extended, or other circumstances change.</span></span> <span data-ttu-id="31ef9-107">资产租赁应该遵守会计准则编纂专题 842 (ASC 842) 和国际财务报告准则 16 (IFRS 16) 提供的有关租赁修改的指导。</span><span class="sxs-lookup"><span data-stu-id="31ef9-107">Asset leasing complies with the guidance that Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16) provide about lease modifications.</span></span> <span data-ttu-id="31ef9-108">ASC 842-20-15-1 将租赁修改定义为对合同的条款和条件进行的任何会导致租赁的范围或注意事项改变的更改。</span><span class="sxs-lookup"><span data-stu-id="31ef9-108">ASC 842-20-15-1 defines a lease modification as any change to the terms and conditions of a contract that causes a change in the scope of, or the consideration for, a lease.</span></span> <span data-ttu-id="31ef9-109">IFRS 16 第 39 段规定，承租人必须对租赁负债进行重估，以反映租赁付款的变化。</span><span class="sxs-lookup"><span data-stu-id="31ef9-109">Paragraph 39 of IFRS 16 states that a lessee must revalue the lease liability so that it reflects changes to the lease payments.</span></span>

<span data-ttu-id="31ef9-110">对于遵守 ASC 842 或 IFRS 16 的组织，将重新度量租赁以反映未来最低租赁付款 (PVFMLP) 的现值变化。</span><span class="sxs-lookup"><span data-stu-id="31ef9-110">For organizations that adhere to ASC 842 or IFRS 16, a lease is remeasured to reflect a change in the present value of the future minimum lease payments (PVFMLP).</span></span> <span data-ttu-id="31ef9-111">如果 PVFMLP 增加，则创建的日记帐条目将是使用权 (ROU) 资产的借方，是新 PVFMLP 与先前 PVFMLP 之间的差额的租赁负债的贷方。</span><span class="sxs-lookup"><span data-stu-id="31ef9-111">If the PVFMLP increases, the journal entry that is created will be a debit to the right-of-use (ROU) asset and a credit to the lease liability for the difference between the new PVFMLP and the previous PVFMLP.</span></span> <span data-ttu-id="31ef9-112">如果 PVFMLP 减少，则日记帐条目将是租赁负债的借方，是差额的使用权资产的贷方。</span><span class="sxs-lookup"><span data-stu-id="31ef9-112">If the PVFMLP decreases, the journal entry will be a debit to the lease liability and a credit to the ROU asset for the difference.</span></span>

<span data-ttu-id="31ef9-113">如果调整将使用权资产减少到低于 0（零），则剩余部分将记入在 **租赁过帐科目** 页指定的租赁修改过帐科目中的收益。</span><span class="sxs-lookup"><span data-stu-id="31ef9-113">If the adjustment decreases the ROU asset past 0 (zero), the remainder will be credited to the gain on lease modification posting account that is specified on the **Lease posting accounts** page.</span></span> <span data-ttu-id="31ef9-114">系统将考虑这些交易和其他调整条目，如因租赁修改而产生的分类变更、初始直接成本、租赁奖励、预付款和拆除成本。</span><span class="sxs-lookup"><span data-stu-id="31ef9-114">The system accounts for these transactions and other adjustment entries, such as classification changes, initial direct costs, lease incentives, prepayments, and dismantling costs that arise from lease modifications.</span></span>

<span data-ttu-id="31ef9-115">有关租赁调整交易的具体指导，我们建议您参阅 IFRS 16 和 ASC 842。</span><span class="sxs-lookup"><span data-stu-id="31ef9-115">For specific guidance about lease adjustment transactions, we recommend that you see IFRS 16 and ASC 842.</span></span>

<span data-ttu-id="31ef9-116">若要调整租赁，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="31ef9-116">To adjust a lease, follow these steps.</span></span> <span data-ttu-id="31ef9-117">运行创建计划流程后，修改后的数据将更新租赁计划。</span><span class="sxs-lookup"><span data-stu-id="31ef9-117">The modified data will update lease schedules after the Create schedule process is run.</span></span>

1. <span data-ttu-id="31ef9-118">转到 **资产租赁 \> 租赁 \> 租赁摘要**。</span><span class="sxs-lookup"><span data-stu-id="31ef9-118">Go to **Asset leasing \> Leases \> Lease summary**.</span></span>
2. <span data-ttu-id="31ef9-119">在 **租赁摘要** 页上，选择要调整的租赁，然后选择 **调整租赁**。</span><span class="sxs-lookup"><span data-stu-id="31ef9-119">On the **Lease summary** page, select the lease to adjust, and then select **Adjust lease**.</span></span>
3. <span data-ttu-id="31ef9-120">在 **调整租赁** 页上，输入调整后租赁的新信息。</span><span class="sxs-lookup"><span data-stu-id="31ef9-120">On the **Adjust lease** page, enter the new information for the adjusted lease.</span></span>

    <span data-ttu-id="31ef9-121">请注意，**调整租赁** 页面与 **添加租赁** 页相似。</span><span class="sxs-lookup"><span data-stu-id="31ef9-121">Notice that the **Adjust lease** page resembles the **Add lease** page.</span></span> <span data-ttu-id="31ef9-122">此外，正如您在添加租赁时指定的开始日期确定新租赁的开始时间一样，**调整租赁** 页面上的 **修改日期** 字段决定修改后的租赁何时开始。</span><span class="sxs-lookup"><span data-stu-id="31ef9-122">Additionally, just as the commencement date that you specify when you add a lease determines when the new lease starts, the **Modification date** field on the **Adjust lease** page determines when the modified lease starts.</span></span> <span data-ttu-id="31ef9-123">该日期不能晚于付款计划行中的开始日期。</span><span class="sxs-lookup"><span data-stu-id="31ef9-123">This date can't be after the start date on the payment schedule lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="31ef9-124">**使用权注意事项** 字段将应用于租赁调整。</span><span class="sxs-lookup"><span data-stu-id="31ef9-124">The **ROU considerations** fields apply to the lease adjustment.</span></span> <span data-ttu-id="31ef9-125">如果没有初始直接成本、租赁奖励、预付款或拆除成本与修改后的租赁相关联，则应将这些字段留空。</span><span class="sxs-lookup"><span data-stu-id="31ef9-125">If no initial direct costs, lease incentives, prepayments, or dismantling costs are associated with the modified lease, you should leave these fields blank.</span></span> <span data-ttu-id="31ef9-126">原始金额将不应用于更新后的租赁。</span><span class="sxs-lookup"><span data-stu-id="31ef9-126">The original amounts won't apply to the updated lease.</span></span> <span data-ttu-id="31ef9-127">应在 **调整租赁** 页中输入修改租赁时产生的任何其他费用。</span><span class="sxs-lookup"><span data-stu-id="31ef9-127">Any additional costs that are incurred when the lease is modified should be entered on the **Adjust lease** page.</span></span>
    > 
    > <span data-ttu-id="31ef9-128">例如，出租人对同意延长租赁提供 1,000 美元的奖励。</span><span class="sxs-lookup"><span data-stu-id="31ef9-128">For example, a lessor provides a $1,000 incentive for agreeing to a lease extension.</span></span> <span data-ttu-id="31ef9-129">在这种情况下，当您调整租赁以延长期限时，请在 **租赁奖励** 字段中输入 **1,000**。</span><span class="sxs-lookup"><span data-stu-id="31ef9-129">In this case, when you adjust the lease to account for the extension, you enter **1,000** in the **Lease incentives** field.</span></span> <span data-ttu-id="31ef9-130">如果没有任何与租赁调整相关的奖励措施，则应清除以前在此字段中输入的所有值。</span><span class="sxs-lookup"><span data-stu-id="31ef9-130">If no incentives are associated with the lease adjustment, you should clear any value that was previously entered in this field.</span></span> <span data-ttu-id="31ef9-131">相同的逻辑适用于其他使用权注意事项。</span><span class="sxs-lookup"><span data-stu-id="31ef9-131">The same logic is applied to other ROU considerations.</span></span>

    <span data-ttu-id="31ef9-132">应基于预期创建调整后租赁的付款计划行。</span><span class="sxs-lookup"><span data-stu-id="31ef9-132">The payment schedule lines of the adjusted lease should be created on a prospective basis.</span></span> <span data-ttu-id="31ef9-133">在租赁修改生效之前，不能启动按预期创建的付款计划行。</span><span class="sxs-lookup"><span data-stu-id="31ef9-133">Payment schedule lines that are created on a prospective basis can't start before the lease modifications take effect.</span></span>

    <span data-ttu-id="31ef9-134">以下步骤与最初确认租赁的步骤几乎相同。</span><span class="sxs-lookup"><span data-stu-id="31ef9-134">The following steps are almost identical to the steps for initially recognizing a lease.</span></span>

4. <span data-ttu-id="31ef9-135">选择 **创建计划** 生成调整后的付款计划。</span><span class="sxs-lookup"><span data-stu-id="31ef9-135">Select **Create schedules** to generate the adjusted payment schedule.</span></span> <span data-ttu-id="31ef9-136">您将收到一条消息，指出已为租赁创建付款计划。</span><span class="sxs-lookup"><span data-stu-id="31ef9-136">You receive a message that states that the payment schedule has been created for the lease.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="31ef9-137">选择 **创建计划** 之前，请确保修改日期和付款计划行正确无误。</span><span class="sxs-lookup"><span data-stu-id="31ef9-137">Before you select **Create schedules**, make sure that the modification date and payment schedule lines are accurate.</span></span> <span data-ttu-id="31ef9-138">还应确保所有初始直接成本、租赁奖励、预付款或拆除成本仅与调整产生的成本相对应。</span><span class="sxs-lookup"><span data-stu-id="31ef9-138">Also make sure that all initial direct costs, lease incentives, prepayments, or dismantling costs correspond only to those costs that arise from the adjustment.</span></span>

5. <span data-ttu-id="31ef9-139">要查看新创建的付款计划，请选择 **帐簿**，然后打开 **付款计划** 页。</span><span class="sxs-lookup"><span data-stu-id="31ef9-139">To view the newly created payment schedule, select **Books**, and open the **Payment schedule** page.</span></span>
6. <span data-ttu-id="31ef9-140">在 **付款计划** 页上，您可以在确认付款计划之前编辑调整后的付款金额。</span><span class="sxs-lookup"><span data-stu-id="31ef9-140">On the **Payment schedule** page, you can edit the adjusted payment amounts before you confirm the payment schedule.</span></span> <span data-ttu-id="31ef9-141">要确认计划，请选择 **确认计划**。</span><span class="sxs-lookup"><span data-stu-id="31ef9-141">To confirm the schedule, select **Confirm schedule**.</span></span>

    <span data-ttu-id="31ef9-142">确认付款计划后，将创建新资产折旧和新租赁负债计划。</span><span class="sxs-lookup"><span data-stu-id="31ef9-142">When the payment schedule is confirmed, the new asset depreciation and new lease liability schedules are created.</span></span>

7. <span data-ttu-id="31ef9-143">要查看从新输入生成的新租赁负债摊销计划，请关闭 **付款计划** 页，然后打开 **负债摊销计划** 页。</span><span class="sxs-lookup"><span data-stu-id="31ef9-143">To view the new lease liability amortization schedule that is generated from the new inputs, close the **Payment schedule** page, and open the **Liability amortization schedule** page.</span></span>
8. <span data-ttu-id="31ef9-144">要查看新生成的资产折旧计划，请从 **帐簿详细信息** 页打开 **资产折旧计划** 页。</span><span class="sxs-lookup"><span data-stu-id="31ef9-144">To view the newly generated asset depreciation schedule, open the **Asset depreciation schedule** page from the **Book details** page.</span></span>
9. <span data-ttu-id="31ef9-145">要生成调整日记帐条目，请选择 **功能 \> 租赁调整**。</span><span class="sxs-lookup"><span data-stu-id="31ef9-145">To generate the adjustment journal entry, select **Function \> Lease adjustment**.</span></span> <span data-ttu-id="31ef9-146">您将收到一条消息，指出已创建调整日记帐条目。</span><span class="sxs-lookup"><span data-stu-id="31ef9-146">You receive a message that states that the adjustment journal entry has been created.</span></span> 
10. <span data-ttu-id="31ef9-147">要查看日记帐条目，请选择 **日记帐 \> 资产租赁日记帐**。</span><span class="sxs-lookup"><span data-stu-id="31ef9-147">To view the journal entry, select **Journals \> Asset leasing journal**.</span></span>
11. <span data-ttu-id="31ef9-148">要过帐日记帐条目，请选择行，然后选择 **过帐**。</span><span class="sxs-lookup"><span data-stu-id="31ef9-148">To post the journal entry, select the line, and then select **Post**.</span></span>

## <a name="view-lease-versions"></a><span data-ttu-id="31ef9-149">查看租赁版本</span><span class="sxs-lookup"><span data-stu-id="31ef9-149">View lease versions</span></span>

<span data-ttu-id="31ef9-150">如果已修改租赁，则可以查看其不同版本。</span><span class="sxs-lookup"><span data-stu-id="31ef9-150">If a lease has been modified, you can view the different versions of it.</span></span> <span data-ttu-id="31ef9-151">您还可以查看历史计划和过去的租赁详细信息。</span><span class="sxs-lookup"><span data-stu-id="31ef9-151">You can also view the historical schedules and past lease details.</span></span>

1. <span data-ttu-id="31ef9-152">在 **租赁摘要** 页面上，选择租赁，然后在“操作”窗格上选择 **租赁版本历史记录**。</span><span class="sxs-lookup"><span data-stu-id="31ef9-152">On the **Lease summary** page, select the lease, and then, on the Action Pane, select **Lease version history**.</span></span>

    <span data-ttu-id="31ef9-153">如果已调整所选租赁，**租赁版本历史** 页将显示它的不同版本。</span><span class="sxs-lookup"><span data-stu-id="31ef9-153">If the selected lease has been adjusted, the **Lease version history** page shows the different versions of it.</span></span> <span data-ttu-id="31ef9-154">原始租赁带有标签 **1个**，后续版本采用升序数字顺序。</span><span class="sxs-lookup"><span data-stu-id="31ef9-154">The original lease is labeled **1**, and subsequent versions have ascending numerical order.</span></span>

    <span data-ttu-id="31ef9-155">对于选定的租赁版本，您可以查看财务维度、合同明细、位置和付款计划行。</span><span class="sxs-lookup"><span data-stu-id="31ef9-155">For a selected lease version, you can view the financial dimensions, contract details, location, and payment schedule lines.</span></span>

2. <span data-ttu-id="31ef9-156">要查看历史计划，请从 **租赁摘要** 页上选择所需帐簿，然后在“操作窗格”上选择 **帐簿版本历史记录**。</span><span class="sxs-lookup"><span data-stu-id="31ef9-156">To view historical schedules, open the modified lease from the **Lease summary** page, select the desired book, and then, on the Action Pane, select **Book version history**.</span></span>
3. <span data-ttu-id="31ef9-157">在 **帐簿版本** 页面上，选择所需版本和所需计划进行查看。</span><span class="sxs-lookup"><span data-stu-id="31ef9-157">On the **Book version** page, select the desired version and the desired schedule to view.</span></span>
