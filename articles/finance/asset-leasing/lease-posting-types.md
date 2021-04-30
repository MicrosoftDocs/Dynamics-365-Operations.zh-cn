---
title: 租赁过帐类型
description: 本主题描述用于资产租赁交易的过帐类型。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1d76c7ea72346c432db04bbe7947dea0c2911ea8
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881124"
---
# <a name="lease-posting-types"></a><span data-ttu-id="5fcba-103">租赁过帐类型</span><span class="sxs-lookup"><span data-stu-id="5fcba-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fcba-104">本主题描述用于资产租赁交易的过帐类型。</span><span class="sxs-lookup"><span data-stu-id="5fcba-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="5fcba-105">租赁资产</span><span class="sxs-lookup"><span data-stu-id="5fcba-105">Lease asset</span></span>

<span data-ttu-id="5fcba-106">该科目与使用权 (ROU) 资产相关联。</span><span class="sxs-lookup"><span data-stu-id="5fcba-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="5fcba-107">当根据新的租赁会计标准、会计准则编纂专题 842 (ASC 842) 和国际财务报告准则 16 (IFRS 16) 最初确认租赁时，将从此科目借记。</span><span class="sxs-lookup"><span data-stu-id="5fcba-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="5fcba-108">对于修改后的租赁，根据修改是增加还是减少租赁负债，可以将该科目记入借方或贷方。</span><span class="sxs-lookup"><span data-stu-id="5fcba-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="5fcba-109">**示例日记帐条目：** 初始确认</span><span class="sxs-lookup"><span data-stu-id="5fcba-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="5fcba-110">**借记：** 租赁资产 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="5fcba-111">**贷记：** 租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="5fcba-112">租赁负债</span><span class="sxs-lookup"><span data-stu-id="5fcba-112">Lease liability</span></span>

<span data-ttu-id="5fcba-113">该科目与根据新的 IFRS 16 和 ASC 842 标准对付款进行折现时发生的租赁负债相关。</span><span class="sxs-lookup"><span data-stu-id="5fcba-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="5fcba-114">根据新准则最初确认租赁时，该科目会记入贷方。</span><span class="sxs-lookup"><span data-stu-id="5fcba-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="5fcba-115">它从租赁付款中扣除，并在应计利息中入帐。</span><span class="sxs-lookup"><span data-stu-id="5fcba-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="5fcba-116">**示例日记帐条目：** 初始确认</span><span class="sxs-lookup"><span data-stu-id="5fcba-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="5fcba-117">**借记：** 租赁资产 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="5fcba-118">**贷记：** 租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="5fcba-119">**示例日记帐条目：** 应计利息</span><span class="sxs-lookup"><span data-stu-id="5fcba-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="5fcba-120">**借记：** 利息费用 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="5fcba-121">**贷记：** 租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="5fcba-122">**示例日记帐条目：** 租赁付款</span><span class="sxs-lookup"><span data-stu-id="5fcba-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="5fcba-123">**贷记：** 租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="5fcba-124">**贷记：** 卖方应付/租赁付款 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="5fcba-125">短期租赁负债</span><span class="sxs-lookup"><span data-stu-id="5fcba-125">Short-term lease liability</span></span>

<span data-ttu-id="5fcba-126">过帐短期租赁负债重新分类日记帐条目时，该科目与短期租赁负债相关联。</span><span class="sxs-lookup"><span data-stu-id="5fcba-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="5fcba-127">该科目在每月的最后一天从摊销计划贷记短期负债。</span><span class="sxs-lookup"><span data-stu-id="5fcba-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="5fcba-128">但是，下个月的第一天将借记同一金额。</span><span class="sxs-lookup"><span data-stu-id="5fcba-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="5fcba-129">**示例日记帐条目：** 短期租赁负债重新分类</span><span class="sxs-lookup"><span data-stu-id="5fcba-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="5fcba-130">**贷记：** 租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="5fcba-131">**贷记：** 短期租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="5fcba-132">**借记：** 短期租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="5fcba-133">**贷记：** 租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="5fcba-134">折旧支出</span><span class="sxs-lookup"><span data-stu-id="5fcba-134">Depreciation expense</span></span>

<span data-ttu-id="5fcba-135">该科目与与 IFRS 16、ASC 842 和 IAS 17 与 ASC 840 下的财务租赁下折旧 使用权资产有关的费用关联。</span><span class="sxs-lookup"><span data-stu-id="5fcba-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="5fcba-136">每月对使用权资产进行折旧时会借记此科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="5fcba-137">**示例日记帐条目：** 应计折旧</span><span class="sxs-lookup"><span data-stu-id="5fcba-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="5fcba-138">**贷记：** 折旧费用 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="5fcba-139">**贷记：** 累计折旧 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="5fcba-140">租赁修改的损益</span><span class="sxs-lookup"><span data-stu-id="5fcba-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="5fcba-141">该科目与因租赁修改而产生的任何损益关联。</span><span class="sxs-lookup"><span data-stu-id="5fcba-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="5fcba-142">如果修改使租赁负债减少的金额超出使用权资产的帐面价值，则在租赁修改期间可能会产生收益。</span><span class="sxs-lookup"><span data-stu-id="5fcba-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="5fcba-143">例如，一个租赁的租赁负债当前帐面价值为 150,000 美元，而使用权资产的帐面价值为 100,000 美元。</span><span class="sxs-lookup"><span data-stu-id="5fcba-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="5fcba-144">修改租赁，并且此修改将产生 40,000 美元的未来最低租赁付款 (PVFMLP) 新现值。</span><span class="sxs-lookup"><span data-stu-id="5fcba-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="5fcba-145">因此，将在租赁负债中借记 110,000 美元 ($150,000 – $40,000)。</span><span class="sxs-lookup"><span data-stu-id="5fcba-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="5fcba-146">由于使用权资产仅为 100,000 美元，因此减少 110,000 美元将导致资产减少到低于 0（零）。</span><span class="sxs-lookup"><span data-stu-id="5fcba-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="5fcba-147">因此，会计指南说明应将余额记入收益科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="5fcba-148">在这种情况下，最终日记帐条目将为 110,000 美元的租赁负债的借方，100,000 美元的租赁资产的贷方，以及 10,000 美元的收益科目的贷方。</span><span class="sxs-lookup"><span data-stu-id="5fcba-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="5fcba-149">**示例日记帐条目：** 租赁修改</span><span class="sxs-lookup"><span data-stu-id="5fcba-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="5fcba-150">**贷记：** 租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="5fcba-151">**贷记：** 租赁资产 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="5fcba-152">**贷记：** 收益 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="5fcba-153">累计折旧</span><span class="sxs-lookup"><span data-stu-id="5fcba-153">Accumulated depreciation</span></span>

<span data-ttu-id="5fcba-154">该科目与使用权资产的对冲资产科目相关联。</span><span class="sxs-lookup"><span data-stu-id="5fcba-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="5fcba-155">在过帐折扣费用时贷记此科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="5fcba-156">**示例日记帐条目：** 应计折旧</span><span class="sxs-lookup"><span data-stu-id="5fcba-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="5fcba-157">**贷记：** 折旧费用 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="5fcba-158">**贷记：** 累计折旧 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="5fcba-159">可变付款</span><span class="sxs-lookup"><span data-stu-id="5fcba-159">Variable payment</span></span>

<span data-ttu-id="5fcba-160">该科目与根据 ASC 842，ASC 840 和 IAS 17 租赁的指数重估产生的可变租赁付款关联。</span><span class="sxs-lookup"><span data-stu-id="5fcba-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="5fcba-161">在租赁付款计划中，可变付款包含在 **可变付款** 列中。</span><span class="sxs-lookup"><span data-stu-id="5fcba-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="5fcba-162">当针对包含可变付款的付款计划行创建发票时，将借记此科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="5fcba-163">**示例日记帐条目：** 租赁付款</span><span class="sxs-lookup"><span data-stu-id="5fcba-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="5fcba-164">**贷记：** 租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="5fcba-165">**借记：** 可变付款 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="5fcba-166">**贷记：** 卖方应付/租赁付款 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="5fcba-167">延期租金资产(负债)</span><span class="sxs-lookup"><span data-stu-id="5fcba-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="5fcba-168">该科目与由延期租金处理租赁产生的延期租金资产或负债相关联。</span><span class="sxs-lookup"><span data-stu-id="5fcba-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="5fcba-169">如果发票付款金额大于该期间的直线租金费用，则在针对延期租金处理租赁过帐发票时借记该科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="5fcba-170">如果租赁付款额少于期间的直线租金费用，则贷记。</span><span class="sxs-lookup"><span data-stu-id="5fcba-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="5fcba-171">**示例日记帐条目：** 租赁付款（延期租金处理租赁）</span><span class="sxs-lookup"><span data-stu-id="5fcba-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="5fcba-172">**借记：** 租赁费用 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="5fcba-173">**贷记：** 延期租金负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="5fcba-174">**贷记：** 卖方应付/租赁付款 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="5fcba-175">租赁支出</span><span class="sxs-lookup"><span data-stu-id="5fcba-175">Lease expense</span></span>

<span data-ttu-id="5fcba-176">如果将租赁分类为延期租金租金处理租赁，则科目与租赁费用关联。</span><span class="sxs-lookup"><span data-stu-id="5fcba-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="5fcba-177">当针对延期租金处理租赁过帐发票时，将借记此科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="5fcba-178">**示例日记帐条目：** 租赁付款（延期租金处理租赁）</span><span class="sxs-lookup"><span data-stu-id="5fcba-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="5fcba-179">**借记：** 租赁费用 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="5fcba-180">**贷记：** 延期租金负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="5fcba-181">**贷记：** 卖方应付/租赁付款 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="5fcba-182">减损支出</span><span class="sxs-lookup"><span data-stu-id="5fcba-182">Impairment expense</span></span>

<span data-ttu-id="5fcba-183">在减损租赁时，将过帐科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="5fcba-184">将借记此科目，而使用权资产科目则直接贷记。</span><span class="sxs-lookup"><span data-stu-id="5fcba-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="5fcba-185">**示例日记帐条目：** 租赁付款</span><span class="sxs-lookup"><span data-stu-id="5fcba-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="5fcba-186">**借记：** 减损费用 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="5fcba-187">**贷记：** 使用权资产 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="5fcba-188">租赁付款</span><span class="sxs-lookup"><span data-stu-id="5fcba-188">Lease payment</span></span>

<span data-ttu-id="5fcba-189">如果 **向供应商付款** 参数已关闭，则过帐科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="5fcba-190">如果关闭该参数，则贷记该科目，而不是贷记供应商应付款。</span><span class="sxs-lookup"><span data-stu-id="5fcba-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="5fcba-191">**示例日记帐条目：** 租赁付款</span><span class="sxs-lookup"><span data-stu-id="5fcba-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="5fcba-192">**贷记：** 租赁负债 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="5fcba-193">**贷记：** 租赁付款 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="5fcba-194">费用类型过帐</span><span class="sxs-lookup"><span data-stu-id="5fcba-194">Expense type postings</span></span>

<span data-ttu-id="5fcba-195">为每种费用类型生成付款时，将借记为费用类型选择的科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="5fcba-196">例如，只要从执行成本计划为保险费用创建发票或付款日记帐条目，都将借记为 **保险** 费用类型指定的科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="5fcba-197">**示例日记帐条目：** 保险付款</span><span class="sxs-lookup"><span data-stu-id="5fcba-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="5fcba-198">**借方：** 保险费用类型科目 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="5fcba-199">**贷方：** 对方科目 XXX</span><span class="sxs-lookup"><span data-stu-id="5fcba-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="5fcba-200">将在执行成本付款计划的行中租赁级别选择对方科目。</span><span class="sxs-lookup"><span data-stu-id="5fcba-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="5fcba-201">此对方科目可以与供应商或分类帐科目关联。</span><span class="sxs-lookup"><span data-stu-id="5fcba-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
