---
title: 普通日记帐行的销售税计算
description: 此主题介绍如何计算普通日记帐行中不同类型的科目（供应商、客户、分类帐和项目）的销售税。
author: EricWang
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: EricWang
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: d0cb4b282fe2bd5c68af17c741787c4caca98003
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937298"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="13282-103">普通日记帐行的销售税计算</span><span class="sxs-lookup"><span data-stu-id="13282-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="13282-104">此主题介绍如何计算普通日记帐行中不同类型的科目（供应商、客户、分类帐和项目）的销售税。</span><span class="sxs-lookup"><span data-stu-id="13282-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="13282-105">此流程可以分为三个步骤：</span><span class="sxs-lookup"><span data-stu-id="13282-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="13282-106">确定税金方向。</span><span class="sxs-lookup"><span data-stu-id="13282-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="13282-107">确定将存储到临时销售税表中的销售税金额。</span><span class="sxs-lookup"><span data-stu-id="13282-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="13282-108">确定凭证中的销售税金额和科目。</span><span class="sxs-lookup"><span data-stu-id="13282-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="13282-109">确定税金方向</span><span class="sxs-lookup"><span data-stu-id="13282-109">Determine the sales tax direction</span></span>

<span data-ttu-id="13282-110">税金方向的确定方法取决于凭证中的科目类型。</span><span class="sxs-lookup"><span data-stu-id="13282-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="13282-111">税金方向由科目类型和销售税代码的组合决定。</span><span class="sxs-lookup"><span data-stu-id="13282-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="13282-112">以下部分更详细地介绍可能情况。</span><span class="sxs-lookup"><span data-stu-id="13282-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="13282-113">科目类型为“项目”</span><span class="sxs-lookup"><span data-stu-id="13282-113">Account type is Project</span></span>

<span data-ttu-id="13282-114">如果凭证中的日记帐行内科目类型为 **项目**，则该凭证中的所有日记帐行采用相同税金方向。</span><span class="sxs-lookup"><span data-stu-id="13282-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="13282-115">下图显示规则。</span><span class="sxs-lookup"><span data-stu-id="13282-115">The following illustration shows the rule.</span></span> <span data-ttu-id="13282-116">以下点显示项目科目可能的税金方向。</span><span class="sxs-lookup"><span data-stu-id="13282-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="13282-117">•   如果销售税代码为销项税，则税金方向为“销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="13282-118">•   如果销售税代码为免税，则税金方向为“免税采购”。</span><span class="sxs-lookup"><span data-stu-id="13282-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="13282-119">•   如果销售税代码为集团内部增值税，则税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="13282-120">•   如果销售税代码为冲销费用，则税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="13282-121">否则，税金方向为“应收销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="13282-122">下图以图形方式演示规则。</span><span class="sxs-lookup"><span data-stu-id="13282-122">The following diagram illustrates the rule graphically.</span></span>

![项目科目的税金方向可能情况](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="13282-124">科目类型为“供应商”</span><span class="sxs-lookup"><span data-stu-id="13282-124">Account type is Vendor</span></span>

<span data-ttu-id="13282-125">如果凭证中的日记帐行内科目类型为 **供应商**，则该凭证中的所有日记帐行采用相同税金方向。</span><span class="sxs-lookup"><span data-stu-id="13282-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="13282-126">以下点显示供应商科目可能的税金方向。</span><span class="sxs-lookup"><span data-stu-id="13282-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="13282-127">•   如果销售税代码为销项税，则税金方向为“销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="13282-128">•   如果销售税代码为免税，则税金方向为“免税采购”。</span><span class="sxs-lookup"><span data-stu-id="13282-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="13282-129">•   如果销售税代码为集团内部增值税，则税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="13282-130">•   如果销售税代码为冲销费用，则税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="13282-131">否则，税金方向为“应收销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="13282-132">下图以图形方式演示规则。</span><span class="sxs-lookup"><span data-stu-id="13282-132">The following diagram illustrates the rule graphically.</span></span>

![供应商科目的税金方向可能情况](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="13282-134">科目类型为“客户”</span><span class="sxs-lookup"><span data-stu-id="13282-134">Account type is Customer</span></span>

<span data-ttu-id="13282-135">如果凭证中的日记帐行内科目类型为 **客户**，则该凭证中的所有日记帐行采用相同税金方向。</span><span class="sxs-lookup"><span data-stu-id="13282-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="13282-136">以下点显示客户科目可能的税金方向。</span><span class="sxs-lookup"><span data-stu-id="13282-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="13282-137">•   如果销售税代码为免税，则税金方向为“免税采购”。</span><span class="sxs-lookup"><span data-stu-id="13282-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="13282-138">•   如果销售税代码为集团内部增值税，则税金方向为“应收销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="13282-139">•   如果销售税代码为冲销费用，则税金方向为“应收销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="13282-140">否则，税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="13282-141">下图以图形方式演示规则。</span><span class="sxs-lookup"><span data-stu-id="13282-141">The following diagram illustrates the rule graphically.</span></span>

![客户科目的税金方向可能情况](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="13282-143">科目类型为“分类帐”</span><span class="sxs-lookup"><span data-stu-id="13282-143">Account type is Ledger</span></span>

<span data-ttu-id="13282-144">下图显示当凭证中只有其科目类型为 **分类帐** 的日记帐行时应用的规则。</span><span class="sxs-lookup"><span data-stu-id="13282-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="13282-145">以下点显示分类帐科目可能的税金方向。</span><span class="sxs-lookup"><span data-stu-id="13282-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="13282-146">•   如果销售税代码为销项税，则税金方向为“销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="13282-147">•   如果销售税代码为免税，则税金方向为“免税采购”。</span><span class="sxs-lookup"><span data-stu-id="13282-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="13282-148">否则，如果日记帐科目为借记（整数），则税金方向为“应收销售税”；如果日记帐科目为贷项（复数），则税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="13282-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="13282-149">下图以图形方式演示规则。</span><span class="sxs-lookup"><span data-stu-id="13282-149">The following diagram illustrates the rule graphically.</span></span>

![分类帐科目的税金方向可能情况](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="13282-151">覆盖税金方向</span><span class="sxs-lookup"><span data-stu-id="13282-151">Override the sales tax direction</span></span>

<span data-ttu-id="13282-152">如果凭证中仅包含其科目类型为 **分类帐** 的行，则可覆盖税金方向。</span><span class="sxs-lookup"><span data-stu-id="13282-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="13282-153">转到 **总帐 \> 会计科目表 \> 科目 \> 主科目**，然后选择 **法人覆盖** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="13282-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="13282-154">确定销售税金额</span><span class="sxs-lookup"><span data-stu-id="13282-154">Determine the sales tax amount</span></span>

<span data-ttu-id="13282-155">此部分介绍如何计算销售税金额符号。</span><span class="sxs-lookup"><span data-stu-id="13282-155">This section describes how the sales tax amount sign is calculated.</span></span>

![销售税交易记录页面](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="13282-157">下表显示用于确定临时销售税表中的销售税方向和销售税金额符号的一般规则。</span><span class="sxs-lookup"><span data-stu-id="13282-157">The following table shows the generic rule for determining the sales tax direction and sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="13282-158">日记帐行金额</span><span class="sxs-lookup"><span data-stu-id="13282-158">Journal line amount</span></span> | <span data-ttu-id="13282-159">税金方向</span><span class="sxs-lookup"><span data-stu-id="13282-159">Sales tax direction</span></span>  | <span data-ttu-id="13282-160">销售税金额符号</span><span class="sxs-lookup"><span data-stu-id="13282-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="13282-161">正</span><span class="sxs-lookup"><span data-stu-id="13282-161">Positive</span></span>            | <span data-ttu-id="13282-162">应收销售税</span><span class="sxs-lookup"><span data-stu-id="13282-162">Sales Tax Receivable</span></span> | <span data-ttu-id="13282-163">正</span><span class="sxs-lookup"><span data-stu-id="13282-163">Positive</span></span>              |
| <span data-ttu-id="13282-164">正</span><span class="sxs-lookup"><span data-stu-id="13282-164">Positive</span></span>            | <span data-ttu-id="13282-165">应付销售税</span><span class="sxs-lookup"><span data-stu-id="13282-165">Sales Tax Payable</span></span>    | <span data-ttu-id="13282-166">负</span><span class="sxs-lookup"><span data-stu-id="13282-166">Negative</span></span>              |
| <span data-ttu-id="13282-167">负</span><span class="sxs-lookup"><span data-stu-id="13282-167">Negative</span></span>            | <span data-ttu-id="13282-168">应收销售税</span><span class="sxs-lookup"><span data-stu-id="13282-168">Sales Tax Receivable</span></span> | <span data-ttu-id="13282-169">负</span><span class="sxs-lookup"><span data-stu-id="13282-169">Negative</span></span>              |
| <span data-ttu-id="13282-170">负</span><span class="sxs-lookup"><span data-stu-id="13282-170">Negative</span></span>            | <span data-ttu-id="13282-171">应付销售税</span><span class="sxs-lookup"><span data-stu-id="13282-171">Sales Tax Payable</span></span>    | <span data-ttu-id="13282-172">正</span><span class="sxs-lookup"><span data-stu-id="13282-172">Positive</span></span>              |

<span data-ttu-id="13282-173">在 **分类帐** 行中选择了销售税组或物料销售税组时，只有 **项目** 或 **分类帐** 行的凭证具有特殊规则。</span><span class="sxs-lookup"><span data-stu-id="13282-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="13282-174">此规则由 **为普通日记帐启用独立销售税计算** 功能控制。</span><span class="sxs-lookup"><span data-stu-id="13282-174">This rule is controlled by the feature, **Enable independent sales tax calculation feature for general journals**.</span></span> <span data-ttu-id="13282-175">如果关闭了此功能，则 **分类帐** 行的税额使用 **项目** 行的借记/贷记方向。</span><span class="sxs-lookup"><span data-stu-id="13282-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="13282-176">如果开启了此功能，则 **分类帐** 行的税额使用自己的借记/贷记方向。</span><span class="sxs-lookup"><span data-stu-id="13282-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="13282-177">下表显示各方案的规则。</span><span class="sxs-lookup"><span data-stu-id="13282-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="13282-178">**开启此功能后的规则**</span><span class="sxs-lookup"><span data-stu-id="13282-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="13282-179">项目的日记帐行金额</span><span class="sxs-lookup"><span data-stu-id="13282-179">Journal line amount of project</span></span> | <span data-ttu-id="13282-180">税金方向</span><span class="sxs-lookup"><span data-stu-id="13282-180">Sales tax direction</span></span>  | <span data-ttu-id="13282-181">销售税金额符号</span><span class="sxs-lookup"><span data-stu-id="13282-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="13282-182">正</span><span class="sxs-lookup"><span data-stu-id="13282-182">Positive</span></span>                       | <span data-ttu-id="13282-183">应收销售税</span><span class="sxs-lookup"><span data-stu-id="13282-183">Sales Tax Receivable</span></span> | <span data-ttu-id="13282-184">正</span><span class="sxs-lookup"><span data-stu-id="13282-184">Positive</span></span>              |
| <span data-ttu-id="13282-185">负</span><span class="sxs-lookup"><span data-stu-id="13282-185">Negative</span></span>                       | <span data-ttu-id="13282-186">应收销售税</span><span class="sxs-lookup"><span data-stu-id="13282-186">Sales Tax Receivable</span></span> | <span data-ttu-id="13282-187">负</span><span class="sxs-lookup"><span data-stu-id="13282-187">Negative</span></span>              |

<span data-ttu-id="13282-188">**关闭此功能后的规则**</span><span class="sxs-lookup"><span data-stu-id="13282-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="13282-189">分类帐的日记帐行金额</span><span class="sxs-lookup"><span data-stu-id="13282-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="13282-190">税金方向</span><span class="sxs-lookup"><span data-stu-id="13282-190">Sales tax direction</span></span>  | <span data-ttu-id="13282-191">销售税金额符号</span><span class="sxs-lookup"><span data-stu-id="13282-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="13282-192">正</span><span class="sxs-lookup"><span data-stu-id="13282-192">Positive</span></span>                       | <span data-ttu-id="13282-193">应收销售税</span><span class="sxs-lookup"><span data-stu-id="13282-193">Sales Tax Receivable</span></span> | <span data-ttu-id="13282-194">正</span><span class="sxs-lookup"><span data-stu-id="13282-194">Positive</span></span>              |
| <span data-ttu-id="13282-195">负</span><span class="sxs-lookup"><span data-stu-id="13282-195">Negative</span></span>                       | <span data-ttu-id="13282-196">应收销售税</span><span class="sxs-lookup"><span data-stu-id="13282-196">Sales Tax Receivable</span></span> | <span data-ttu-id="13282-197">负</span><span class="sxs-lookup"><span data-stu-id="13282-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="13282-198">确定凭证中的销售税金额和科目</span><span class="sxs-lookup"><span data-stu-id="13282-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="13282-199">过帐销售税时，将从分类帐过帐组模板检索主科目。</span><span class="sxs-lookup"><span data-stu-id="13282-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="13282-200">如果销售税为应收销售税，则系统使用在该模板中指定的“应收销售税”科目。</span><span class="sxs-lookup"><span data-stu-id="13282-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="13282-201">对于应付销售税，则系统使用在该模板中指定的“应付销售税”科目。</span><span class="sxs-lookup"><span data-stu-id="13282-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="13282-202">下表显示一般规则。</span><span class="sxs-lookup"><span data-stu-id="13282-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="13282-203">税金方向</span><span class="sxs-lookup"><span data-stu-id="13282-203">Sales tax direction</span></span>  | <span data-ttu-id="13282-204">销售税金额符号</span><span class="sxs-lookup"><span data-stu-id="13282-204">Sales tax amount sign</span></span> | <span data-ttu-id="13282-205">增值税帐户</span><span class="sxs-lookup"><span data-stu-id="13282-205">Sales tax account</span></span>      | <span data-ttu-id="13282-206">凭证中的金额</span><span class="sxs-lookup"><span data-stu-id="13282-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="13282-207">应收销售税</span><span class="sxs-lookup"><span data-stu-id="13282-207">Sales Tax Receivable</span></span> | <span data-ttu-id="13282-208">正</span><span class="sxs-lookup"><span data-stu-id="13282-208">Positive</span></span>              | <span data-ttu-id="13282-209">应收税金科目</span><span class="sxs-lookup"><span data-stu-id="13282-209">Tax Receivable Account</span></span> | <span data-ttu-id="13282-210">正数（借记）</span><span class="sxs-lookup"><span data-stu-id="13282-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="13282-211">应收销售税</span><span class="sxs-lookup"><span data-stu-id="13282-211">Sales Tax Receivable</span></span> | <span data-ttu-id="13282-212">负</span><span class="sxs-lookup"><span data-stu-id="13282-212">Negative</span></span>              | <span data-ttu-id="13282-213">应收税金科目</span><span class="sxs-lookup"><span data-stu-id="13282-213">Tax Receivable Account</span></span> | <span data-ttu-id="13282-214">负数（贷记）</span><span class="sxs-lookup"><span data-stu-id="13282-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="13282-215">应付销售税</span><span class="sxs-lookup"><span data-stu-id="13282-215">Sales Tax Payable</span></span>    | <span data-ttu-id="13282-216">正</span><span class="sxs-lookup"><span data-stu-id="13282-216">Positive</span></span>              | <span data-ttu-id="13282-217">应付税金科目</span><span class="sxs-lookup"><span data-stu-id="13282-217">Tax Payable Account</span></span>    | <span data-ttu-id="13282-218">负数（贷记）</span><span class="sxs-lookup"><span data-stu-id="13282-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="13282-219">应付销售税</span><span class="sxs-lookup"><span data-stu-id="13282-219">Sales Tax Payable</span></span>    | <span data-ttu-id="13282-220">负</span><span class="sxs-lookup"><span data-stu-id="13282-220">Negative</span></span>              | <span data-ttu-id="13282-221">应付税金科目</span><span class="sxs-lookup"><span data-stu-id="13282-221">Tax Payable Account</span></span>    | <span data-ttu-id="13282-222">正数（借记）</span><span class="sxs-lookup"><span data-stu-id="13282-222">Positive (Debit)</span></span>  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
