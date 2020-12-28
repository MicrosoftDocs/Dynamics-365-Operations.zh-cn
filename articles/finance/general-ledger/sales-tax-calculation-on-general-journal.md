---
title: 普通日记帐行的销售税计算
description: 此主题介绍如何计算普通日记帐行中不同类型的科目（供应商、客户、分类帐和项目）的销售税。
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 51d43c8e6d16201e1f8c392c13ead20287782dcc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440607"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="a8dbd-103">普通日记帐行的销售税计算</span><span class="sxs-lookup"><span data-stu-id="a8dbd-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8dbd-104">此主题介绍如何计算普通日记帐行中不同类型的科目（供应商、客户、分类帐和项目）的销售税。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="a8dbd-105">此流程可以分为三个步骤：</span><span class="sxs-lookup"><span data-stu-id="a8dbd-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="a8dbd-106">确定税金方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="a8dbd-107">确定将存储到临时销售税表中的销售税金额。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="a8dbd-108">确定凭证中的销售税金额和科目。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="a8dbd-109">确定税金方向</span><span class="sxs-lookup"><span data-stu-id="a8dbd-109">Determine the sales tax direction</span></span>

<span data-ttu-id="a8dbd-110">税金方向的确定方法取决于凭证中的科目类型。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="a8dbd-111">税金方向由科目类型和销售税代码的组合决定。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="a8dbd-112">以下部分更详细地介绍可能情况。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="a8dbd-113">科目类型为“项目”</span><span class="sxs-lookup"><span data-stu-id="a8dbd-113">Account type is Project</span></span>

<span data-ttu-id="a8dbd-114">如果凭证中的日记帐行内科目类型为 **项目**，则该凭证中的所有日记帐行采用相同税金方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="a8dbd-115">下图显示规则。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-115">The following illustration shows the rule.</span></span> <span data-ttu-id="a8dbd-116">以下点显示项目科目可能的税金方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="a8dbd-117">•   如果销售税代码为销项税，则税金方向为“销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="a8dbd-118">•   如果销售税代码为免税，则税金方向为“免税采购”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="a8dbd-119">•   如果销售税代码为集团内部增值税，则税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a8dbd-120">•   如果销售税代码为冲销费用，则税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a8dbd-121">否则，税金方向为“应收销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="a8dbd-122">下图以图形方式演示规则。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-122">The following diagram illustrates the rule graphically.</span></span>

![项目科目的税金方向可能情况](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="a8dbd-124">科目类型为“供应商”</span><span class="sxs-lookup"><span data-stu-id="a8dbd-124">Account type is Vendor</span></span>

<span data-ttu-id="a8dbd-125">如果凭证中的日记帐行内科目类型为 **供应商**，则该凭证中的所有日记帐行采用相同税金方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="a8dbd-126">以下点显示供应商科目可能的税金方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="a8dbd-127">•   如果销售税代码为销项税，则税金方向为“销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="a8dbd-128">•   如果销售税代码为免税，则税金方向为“免税采购”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="a8dbd-129">•   如果销售税代码为集团内部增值税，则税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a8dbd-130">•   如果销售税代码为冲销费用，则税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a8dbd-131">否则，税金方向为“应收销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="a8dbd-132">下图以图形方式演示规则。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-132">The following diagram illustrates the rule graphically.</span></span>

![供应商科目的税金方向可能情况](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="a8dbd-134">科目类型为“客户”</span><span class="sxs-lookup"><span data-stu-id="a8dbd-134">Account type is Customer</span></span>

<span data-ttu-id="a8dbd-135">如果凭证中的日记帐行内科目类型为 **客户**，则该凭证中的所有日记帐行采用相同税金方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="a8dbd-136">以下点显示客户科目可能的税金方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="a8dbd-137">•   如果销售税代码为免税，则税金方向为“免税采购”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="a8dbd-138">•   如果销售税代码为集团内部增值税，则税金方向为“应收销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="a8dbd-139">•   如果销售税代码为冲销费用，则税金方向为“应收销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="a8dbd-140">否则，税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a8dbd-141">下图以图形方式演示规则。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-141">The following diagram illustrates the rule graphically.</span></span>

![客户科目的税金方向可能情况](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="a8dbd-143">科目类型为“分类帐”</span><span class="sxs-lookup"><span data-stu-id="a8dbd-143">Account type is Ledger</span></span>

<span data-ttu-id="a8dbd-144">下图显示当凭证中只有其科目类型为 **分类帐** 的日记帐行时应用的规则。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="a8dbd-145">以下点显示分类帐科目可能的税金方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="a8dbd-146">•   如果销售税代码为销项税，则税金方向为“销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="a8dbd-147">•   如果销售税代码为免税，则税金方向为“免税采购”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="a8dbd-148">否则，如果日记帐科目为借记（整数），则税金方向为“应收销售税”；如果日记帐科目为贷项（复数），则税金方向为“应付销售税”。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="a8dbd-149">下图以图形方式演示规则。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-149">The following diagram illustrates the rule graphically.</span></span>

![分类帐科目的税金方向可能情况](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="a8dbd-151">覆盖税金方向</span><span class="sxs-lookup"><span data-stu-id="a8dbd-151">Override the sales tax direction</span></span>

<span data-ttu-id="a8dbd-152">如果凭证中仅包含其科目类型为 **分类帐** 的行，则可覆盖税金方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="a8dbd-153">转到 **总帐 \> 会计科目表 \> 科目 \> 主科目**，然后选择 **法人覆盖** 快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="a8dbd-154">确定销售税金额</span><span class="sxs-lookup"><span data-stu-id="a8dbd-154">Determine the sales tax amount</span></span>

<span data-ttu-id="a8dbd-155">此部分介绍如何计算销售税金额符号。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-155">This section describes how the sales tax amount sign is calculated.</span></span>

![销售税交易记录页面](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="a8dbd-157">下表显示用于确定临时销售税表中的销售税金额符号的一般规则。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="a8dbd-158">日记帐行金额</span><span class="sxs-lookup"><span data-stu-id="a8dbd-158">Journal line amount</span></span> | <span data-ttu-id="a8dbd-159">税金方向</span><span class="sxs-lookup"><span data-stu-id="a8dbd-159">Sales tax direction</span></span>  | <span data-ttu-id="a8dbd-160">销售税金额符号</span><span class="sxs-lookup"><span data-stu-id="a8dbd-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="a8dbd-161">正</span><span class="sxs-lookup"><span data-stu-id="a8dbd-161">Positive</span></span>            | <span data-ttu-id="a8dbd-162">应收销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-162">Sales Tax Receivable</span></span> | <span data-ttu-id="a8dbd-163">正</span><span class="sxs-lookup"><span data-stu-id="a8dbd-163">Positive</span></span>              |
| <span data-ttu-id="a8dbd-164">正</span><span class="sxs-lookup"><span data-stu-id="a8dbd-164">Positive</span></span>            | <span data-ttu-id="a8dbd-165">应付销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-165">Sales Tax Payable</span></span>    | <span data-ttu-id="a8dbd-166">负</span><span class="sxs-lookup"><span data-stu-id="a8dbd-166">Negative</span></span>              |
| <span data-ttu-id="a8dbd-167">负</span><span class="sxs-lookup"><span data-stu-id="a8dbd-167">Negative</span></span>            | <span data-ttu-id="a8dbd-168">应收销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-168">Sales Tax Receivable</span></span> | <span data-ttu-id="a8dbd-169">负</span><span class="sxs-lookup"><span data-stu-id="a8dbd-169">Negative</span></span>              |
| <span data-ttu-id="a8dbd-170">负</span><span class="sxs-lookup"><span data-stu-id="a8dbd-170">Negative</span></span>            | <span data-ttu-id="a8dbd-171">应付销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-171">Sales Tax Payable</span></span>    | <span data-ttu-id="a8dbd-172">正</span><span class="sxs-lookup"><span data-stu-id="a8dbd-172">Positive</span></span>              |

<span data-ttu-id="a8dbd-173">在 **分类帐** 行中选择了销售税组或物料销售税组时，只有 **项目** 或 **分类帐** 行的凭证具有特殊规则。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="a8dbd-174">此规则由普通日记帐的“启用独立销售税计算”功能控制。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="a8dbd-175">如果关闭了此功能，则 **分类帐** 行的税额使用 **项目** 行的借记/贷记方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="a8dbd-176">如果开启了此功能，则 **分类帐** 行的税额使用自己的借记/贷记方向。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="a8dbd-177">下表显示各方案的规则。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="a8dbd-178">**开启此功能后的规则**</span><span class="sxs-lookup"><span data-stu-id="a8dbd-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="a8dbd-179">项目的日记帐行金额</span><span class="sxs-lookup"><span data-stu-id="a8dbd-179">Journal line amount of project</span></span> | <span data-ttu-id="a8dbd-180">税金方向</span><span class="sxs-lookup"><span data-stu-id="a8dbd-180">Sales tax direction</span></span>  | <span data-ttu-id="a8dbd-181">销售税金额符号</span><span class="sxs-lookup"><span data-stu-id="a8dbd-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="a8dbd-182">正</span><span class="sxs-lookup"><span data-stu-id="a8dbd-182">Positive</span></span>                       | <span data-ttu-id="a8dbd-183">应收销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-183">Sales Tax Receivable</span></span> | <span data-ttu-id="a8dbd-184">正</span><span class="sxs-lookup"><span data-stu-id="a8dbd-184">Positive</span></span>              |
| <span data-ttu-id="a8dbd-185">负</span><span class="sxs-lookup"><span data-stu-id="a8dbd-185">Negative</span></span>                       | <span data-ttu-id="a8dbd-186">应收销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-186">Sales Tax Receivable</span></span> | <span data-ttu-id="a8dbd-187">负</span><span class="sxs-lookup"><span data-stu-id="a8dbd-187">Negative</span></span>              |

<span data-ttu-id="a8dbd-188">**关闭此功能后的规则**</span><span class="sxs-lookup"><span data-stu-id="a8dbd-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="a8dbd-189">分类帐的日记帐行金额</span><span class="sxs-lookup"><span data-stu-id="a8dbd-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="a8dbd-190">税金方向</span><span class="sxs-lookup"><span data-stu-id="a8dbd-190">Sales tax direction</span></span>  | <span data-ttu-id="a8dbd-191">销售税金额符号</span><span class="sxs-lookup"><span data-stu-id="a8dbd-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="a8dbd-192">正</span><span class="sxs-lookup"><span data-stu-id="a8dbd-192">Positive</span></span>                       | <span data-ttu-id="a8dbd-193">应收销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-193">Sales Tax Receivable</span></span> | <span data-ttu-id="a8dbd-194">正</span><span class="sxs-lookup"><span data-stu-id="a8dbd-194">Positive</span></span>              |
| <span data-ttu-id="a8dbd-195">负</span><span class="sxs-lookup"><span data-stu-id="a8dbd-195">Negative</span></span>                       | <span data-ttu-id="a8dbd-196">应收销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-196">Sales Tax Receivable</span></span> | <span data-ttu-id="a8dbd-197">负</span><span class="sxs-lookup"><span data-stu-id="a8dbd-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="a8dbd-198">确定凭证中的销售税金额和科目</span><span class="sxs-lookup"><span data-stu-id="a8dbd-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="a8dbd-199">过帐销售税时，将从分类帐过帐组模板检索主科目。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="a8dbd-200">如果销售税为应收销售税，则系统使用在该模板中指定的“应收销售税”科目。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="a8dbd-201">对于应付销售税，则系统使用在该模板中指定的“应付销售税”科目。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="a8dbd-202">下表显示一般规则。</span><span class="sxs-lookup"><span data-stu-id="a8dbd-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="a8dbd-203">税金方向</span><span class="sxs-lookup"><span data-stu-id="a8dbd-203">Sales tax direction</span></span>  | <span data-ttu-id="a8dbd-204">销售税金额符号</span><span class="sxs-lookup"><span data-stu-id="a8dbd-204">Sales tax amount sign</span></span> | <span data-ttu-id="a8dbd-205">增值税帐户</span><span class="sxs-lookup"><span data-stu-id="a8dbd-205">Sales tax account</span></span>      | <span data-ttu-id="a8dbd-206">凭证中的金额</span><span class="sxs-lookup"><span data-stu-id="a8dbd-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="a8dbd-207">应收销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-207">Sales Tax Receivable</span></span> | <span data-ttu-id="a8dbd-208">正</span><span class="sxs-lookup"><span data-stu-id="a8dbd-208">Positive</span></span>              | <span data-ttu-id="a8dbd-209">应收税金科目</span><span class="sxs-lookup"><span data-stu-id="a8dbd-209">Tax Receivable Account</span></span> | <span data-ttu-id="a8dbd-210">正数（借记）</span><span class="sxs-lookup"><span data-stu-id="a8dbd-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="a8dbd-211">应收销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-211">Sales Tax Receivable</span></span> | <span data-ttu-id="a8dbd-212">负</span><span class="sxs-lookup"><span data-stu-id="a8dbd-212">Negative</span></span>              | <span data-ttu-id="a8dbd-213">应收税金科目</span><span class="sxs-lookup"><span data-stu-id="a8dbd-213">Tax Receivable Account</span></span> | <span data-ttu-id="a8dbd-214">负数（贷记）</span><span class="sxs-lookup"><span data-stu-id="a8dbd-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="a8dbd-215">应付销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-215">Sales Tax Payable</span></span>    | <span data-ttu-id="a8dbd-216">正</span><span class="sxs-lookup"><span data-stu-id="a8dbd-216">Positive</span></span>              | <span data-ttu-id="a8dbd-217">应付税金科目</span><span class="sxs-lookup"><span data-stu-id="a8dbd-217">Tax Payable Account</span></span>    | <span data-ttu-id="a8dbd-218">负数（贷记）</span><span class="sxs-lookup"><span data-stu-id="a8dbd-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="a8dbd-219">应付销售税</span><span class="sxs-lookup"><span data-stu-id="a8dbd-219">Sales Tax Payable</span></span>    | <span data-ttu-id="a8dbd-220">负</span><span class="sxs-lookup"><span data-stu-id="a8dbd-220">Negative</span></span>              | <span data-ttu-id="a8dbd-221">应付税金科目</span><span class="sxs-lookup"><span data-stu-id="a8dbd-221">Tax Payable Account</span></span>    | <span data-ttu-id="a8dbd-222">正数（借记）</span><span class="sxs-lookup"><span data-stu-id="a8dbd-222">Positive (Debit)</span></span>  |
