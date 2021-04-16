---
title: 重估与指数利率链接的租赁付款
description: 本主题描述了由于指数利率的变化而导致可变租赁付款发生变化时，对租赁使用权 (ROU) 负债进行的调整。
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
ms.openlocfilehash: 8d743bb51cfc1487e76ee46adfd59276f1c1b48b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819714"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a><span data-ttu-id="97e2b-103">重估与指数利率链接的租赁付款</span><span class="sxs-lookup"><span data-stu-id="97e2b-103">Revalue lease payments that are linked to an index rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97e2b-104">本主题描述了由于指数利率的变化而导致可变租赁付款发生变化时，对租赁使用权 (ROU) 负债进行的调整。</span><span class="sxs-lookup"><span data-stu-id="97e2b-104">This topic describes the adjustment that is made to the lease liability for a right-of-use (ROU) asset when variable lease payments change because of a change in the index rate.</span></span> <span data-ttu-id="97e2b-105">租赁负债和使用权资产将进行调整，以计入新的付款金额。</span><span class="sxs-lookup"><span data-stu-id="97e2b-105">The lease liability and ROU asset will be adjusted to account for the new payment amounts.</span></span> <span data-ttu-id="97e2b-106">根据会计准则编纂专题 842 (ASC 842)（这是美国公认会计准则 (US GAAP) 中的准则），除非现金流发生了更多变化，否则在由于指数利率改变导致付款增加或减少时，只有可变付款会改变。</span><span class="sxs-lookup"><span data-stu-id="97e2b-106">Under Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), only the variable payments change when payments increase or decrease because of a change in the index rate, unless there are additional changes to cash flows.</span></span> <span data-ttu-id="97e2b-107">这些其他变化可能包括与利率有关的租赁条款的变化。</span><span class="sxs-lookup"><span data-stu-id="97e2b-107">These additional changes might include a change in lease terms that is related to interest rates.</span></span> <span data-ttu-id="97e2b-108">有关详细信息，请参阅 ASC 842-10-55-225 和国际财务报告准则 16 (IFRS 16) 第 42(b) 段。</span><span class="sxs-lookup"><span data-stu-id="97e2b-108">For more information, see ASC 842-10-55-225 and paragraph 42(b) of International Financial Reporting Standard 16 (IFRS 16).</span></span>

## <a name="adjust-lease-payments"></a><span data-ttu-id="97e2b-109">调整租赁付款</span><span class="sxs-lookup"><span data-stu-id="97e2b-109">Adjust lease payments</span></span>

<span data-ttu-id="97e2b-110">按照以下步骤重估与指数利率链接的租赁付款。</span><span class="sxs-lookup"><span data-stu-id="97e2b-110">Follow these steps to revalue lease payments that are linked to an index rate.</span></span>

1. <span data-ttu-id="97e2b-111">要运行租赁指数重估流程，请转到 **资产租赁 \> 定期 \> 指数利率重估**。</span><span class="sxs-lookup"><span data-stu-id="97e2b-111">To run the lease index revaluation process, go to **Asset leasing \> Periodic \> Index rate revaluation**.</span></span>

    <span data-ttu-id="97e2b-112">将显示 **指数利率重估** 页，其中显示所有先前已运行的租赁指数重估流程。</span><span class="sxs-lookup"><span data-stu-id="97e2b-112">The **Index rate revaluation** page appears and shows all previous lease index revaluation processes that have been run.</span></span> <span data-ttu-id="97e2b-113">此页面上的信息包括从编号规则设置生成的流程 ID、法人、已调整的租赁帐簿数量、IFRS 16 租赁的总负债调整，以及针对 ASC 842 租赁调整的可变付款总额。</span><span class="sxs-lookup"><span data-stu-id="97e2b-113">The information on this page includes the process ID that was generated from the number sequence setup, the legal entity, the number of lease books that were adjusted, the total liability adjustment for IFRS 16 leases, and the total variable payments that were adjusted for ASC 842 leases.</span></span>

2. <span data-ttu-id="97e2b-114">要运行重估，请在操作窗格上选择 **租赁指数重估**。</span><span class="sxs-lookup"><span data-stu-id="97e2b-114">To run the revaluation, on the Action Pane, select **Lease index revaluation**.</span></span>

    <span data-ttu-id="97e2b-115">将显示 **指数重估参数** 对话框。</span><span class="sxs-lookup"><span data-stu-id="97e2b-115">The **Index revaluation parameters** dialog box appears.</span></span> <span data-ttu-id="97e2b-116">可在此处筛选并选择在选择要重估的租赁时应使用哪些租赁、租赁组或其他条件。</span><span class="sxs-lookup"><span data-stu-id="97e2b-116">Here, you can filter and select which leases, lease groups, or other criteria should be used when you select the leases to revalue.</span></span> <span data-ttu-id="97e2b-117">此外，还可以在 **后台运行** 选项卡上设置指数重估流程，以使其批量运行。</span><span class="sxs-lookup"><span data-stu-id="97e2b-117">Additionally, on the **Run in the background** tab, you can set up the index revaluation process so that it runs in a batch.</span></span>

4. <span data-ttu-id="97e2b-118">选择用于选择后台处理中应包括的租赁的筛选器，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="97e2b-118">Select the filters for selecting leases that should be included in the background processing, and then select **OK**.</span></span>

    <span data-ttu-id="97e2b-119">将显示 **指数利率重估预览** 对话框，其中显示将重估的租赁。</span><span class="sxs-lookup"><span data-stu-id="97e2b-119">The **Index Rate revaluation preview** dialog box appears and shows the leases that will be revalued.</span></span> <span data-ttu-id="97e2b-120">还显示资产和负债调整或可变付款调整。</span><span class="sxs-lookup"><span data-stu-id="97e2b-120">It also shows the asset and liability adjustments or the variable payment adjustments.</span></span>
    
5. <span data-ttu-id="97e2b-121">要防止重估租赁，请选择 **应该** 重估的租赁。</span><span class="sxs-lookup"><span data-stu-id="97e2b-121">To prevent leases from being revalued, select the leases that **should** be revalued.</span></span> <span data-ttu-id="97e2b-122">如果不选择任何租赁，将重估所有租赁。</span><span class="sxs-lookup"><span data-stu-id="97e2b-122">If you don't select any leases, all leases will be revalued.</span></span> <span data-ttu-id="97e2b-123">完成后，选择 **确定** 重估租赁付款。</span><span class="sxs-lookup"><span data-stu-id="97e2b-123">When you've finished, select **OK** to revalue the lease payments.</span></span>
6. <span data-ttu-id="97e2b-124">要查看为特定指数重估流程创建的交易，请选择流程 ID，然后选择 **交易**。</span><span class="sxs-lookup"><span data-stu-id="97e2b-124">To view the transactions that were created for a specific index revaluation process, select the process ID, and then select **Transactions**.</span></span>

    <span data-ttu-id="97e2b-125">将显示一个对话框，其中显示处理期间创建的交易的详细信息。</span><span class="sxs-lookup"><span data-stu-id="97e2b-125">A dialog box appears and shows the details of the transactions that were created during processing.</span></span>

> [!NOTE]
> <span data-ttu-id="97e2b-126">只能重估重估日期在系统日期当天或之前的租赁。</span><span class="sxs-lookup"><span data-stu-id="97e2b-126">Only leases that have a revaluation date that is on or before the system date can be revalued.</span></span> <span data-ttu-id="97e2b-127">系统将自动忽略重估日期晚于系统日期的所有租赁。</span><span class="sxs-lookup"><span data-stu-id="97e2b-127">The system automatically ignores all leases that have a revaluation date that is later than the system date.</span></span>

## <a name="asc-842-leases--index-revaluation"></a><span data-ttu-id="97e2b-128">ASC 842 租赁 – 指数重估</span><span class="sxs-lookup"><span data-stu-id="97e2b-128">ASC 842 leases – Index revaluation</span></span>

<span data-ttu-id="97e2b-129">要查看租赁重估过程对 ASC 842 租赁的影响，请打开租赁的付款计划。</span><span class="sxs-lookup"><span data-stu-id="97e2b-129">To view the effects of the lease revaluation process on ASC 842 leases, open the payment schedule for a lease.</span></span> <span data-ttu-id="97e2b-130">该页面仅显示由于指数重估而在重估日期更改之日或之后更改的可变付款。</span><span class="sxs-lookup"><span data-stu-id="97e2b-130">The page shows only the variable payments that have been made on or after the revaluation date was changed because of the index revaluation.</span></span> <span data-ttu-id="97e2b-131">摊销和折旧计划保持不变。</span><span class="sxs-lookup"><span data-stu-id="97e2b-131">The amortization and depreciation schedules remain unchanged.</span></span> <span data-ttu-id="97e2b-132">当您创建具有可变付款的发票时，可变付款会借记到可变付款过帐科目。</span><span class="sxs-lookup"><span data-stu-id="97e2b-132">When you create an invoice that has a variable payment, the variable payment is debited to the Variable payment posting account.</span></span> <span data-ttu-id="97e2b-133">此外，根据租赁帐簿的设置，可变付款金额还会添加到直接过帐到供应商或过帐到 Notes 应付帐款的贷方条目中。</span><span class="sxs-lookup"><span data-stu-id="97e2b-133">Also the variable payment amount is added to the credit entry that's posted directly to the vendor, or posted to Notes payable account, depending on the lease book setup.</span></span>

<span data-ttu-id="97e2b-134">租赁详细信息页面上的付款计划行会自动使用新行更新，该行指示新的指数利率。</span><span class="sxs-lookup"><span data-stu-id="97e2b-134">The payment schedule lines on the lease details page are automatically updated with a new line that indicates the new index rate.</span></span> <span data-ttu-id="97e2b-135">此外，还会有一列显示该行是手动创建的，还是通过指数重估流程创建的。</span><span class="sxs-lookup"><span data-stu-id="97e2b-135">Additionally, a column shows whether the line was created manually or through the index revaluation process.</span></span>

## <a name="ifrs-16-leases--index-revaluation"></a><span data-ttu-id="97e2b-136">IFRS 16 租赁 – 指数重估</span><span class="sxs-lookup"><span data-stu-id="97e2b-136">IFRS 16 leases – Index revaluation</span></span>

<span data-ttu-id="97e2b-137">要查看租赁重估过程对 IFRS 16 租赁的影响，请打开调整后租赁的租赁详细信息。</span><span class="sxs-lookup"><span data-stu-id="97e2b-137">To view the effects of the lease revaluation process on IFRS 16 leases, open the lease details for an adjusted lease.</span></span> <span data-ttu-id="97e2b-138">**租赁期** 和 **资产使用年限** 字段已更新，以反映从开始日期或修改日期到重估日期的过程。</span><span class="sxs-lookup"><span data-stu-id="97e2b-138">The **Lease term** and **Asset useful life** fields have been updated to reflect the passage of time from the commencement date or modification date to the revaluation date.</span></span> <span data-ttu-id="97e2b-139">此外，付款计划行已更新，以反映租赁中的新付款、新指数利率和行的创建方式。</span><span class="sxs-lookup"><span data-stu-id="97e2b-139">Additionally, the payment schedule lines have updated to reflect the new payments on the lease, the new index rate, and how the line was created.</span></span>

<span data-ttu-id="97e2b-140">您可以查看从重估日期开始新生成的付款计划，并显示更新后的付款总额。</span><span class="sxs-lookup"><span data-stu-id="97e2b-140">You can view the newly generated payment schedule that starts on the revaluation date and show the total updated payment amount.</span></span> <span data-ttu-id="97e2b-141">还创建了新的租赁负债摊销计划和资产折旧计划，以反映调整后的付款计划。</span><span class="sxs-lookup"><span data-stu-id="97e2b-141">A new lease liability amortization schedule and an asset depreciation schedule have also been created to reflect the adjusted payment schedule.</span></span>

<span data-ttu-id="97e2b-142">日记帐条目已将调整日记帐条目自动过帐到与指数重估相关的租赁付款变更的科目。</span><span class="sxs-lookup"><span data-stu-id="97e2b-142">The journal entry has automatically posted the adjustment journal entry to the account for the change in lease payments that are related to the index revaluation.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]