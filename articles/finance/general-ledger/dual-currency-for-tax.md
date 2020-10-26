---
title: 纳税的双币种支持
description: 此主题介绍如何扩展税域的双币种记帐功能和对税额计算与过帐的影响
author: EricWang
manager: Ann Beebe
ms.date: 12/16/2019
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
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 9e5db8e4bbd14aa30196e3be617cdfcb72c091fd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977159"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="caf91-103">销售税的双币种支持</span><span class="sxs-lookup"><span data-stu-id="caf91-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="caf91-104">此主题介绍如何扩展销售税的双币种记帐功能和对销售税计算、过帐与结算的影响。</span><span class="sxs-lookup"><span data-stu-id="caf91-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="caf91-105">版本 8.1（2018 年 10 月）中引入了适用于 Dynamics 365 Finance 的双币种功能。</span><span class="sxs-lookup"><span data-stu-id="caf91-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="caf91-106">该功能改变了计算采用申报币种的会计条目的方式。</span><span class="sxs-lookup"><span data-stu-id="caf91-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="caf91-107">在早期版本中，交易记录按以下顺序转换为申报币种：</span><span class="sxs-lookup"><span data-stu-id="caf91-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="caf91-108">使用交易币种计算交易记录合计 > 交易记录金额转换为记帐币种 > 记帐币种金额转换为申报币种</span><span class="sxs-lookup"><span data-stu-id="caf91-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="caf91-109">启用双币种功能之后，交易记录按照以下顺序转换为申报币种：</span><span class="sxs-lookup"><span data-stu-id="caf91-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="caf91-110">交易币种金额 > 申报币种金额</span><span class="sxs-lookup"><span data-stu-id="caf91-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="caf91-111">有关双币种的详细信息，请参阅[双币种](dual-currency.md)。</span><span class="sxs-lookup"><span data-stu-id="caf91-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="caf91-112">由于支持双币种，所以功能管理中增加了两项新功能：</span><span class="sxs-lookup"><span data-stu-id="caf91-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="caf91-113">销售税转换（版本 10.0.9 中发布）</span><span class="sxs-lookup"><span data-stu-id="caf91-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="caf91-114">税务结算自动平衡采用申报币种（版本 10.0.11 中发布）</span><span class="sxs-lookup"><span data-stu-id="caf91-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="caf91-115">销售税的双币种支持确保使用税金币种准确计算税额，以及同时使用记帐币种和申报币种准确计算销售税结算余额。</span><span class="sxs-lookup"><span data-stu-id="caf91-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="caf91-116">销售税换算</span><span class="sxs-lookup"><span data-stu-id="caf91-116">Sales tax conversion</span></span>

<span data-ttu-id="caf91-117">**销售税转换**参数提供两个选项，用于将税额从交易币种转换为税金币种。</span><span class="sxs-lookup"><span data-stu-id="caf91-117">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="caf91-118">记帐币种：路径将为“交易币种的金额 > 记帐币种的金额 > 税金币种的金额”。</span><span class="sxs-lookup"><span data-stu-id="caf91-118">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="caf91-119">将把记帐币种汇率类型（在分类帐设置中配置）用于币种转换。</span><span class="sxs-lookup"><span data-stu-id="caf91-119">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="caf91-120">申报币种：路径将为“交易币种的金额 > 申报币种的金额 > 税金币种的金额”。</span><span class="sxs-lookup"><span data-stu-id="caf91-120">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="caf91-121">将把申报币种汇率类型（在分类帐设置中配置）用于币种转换。</span><span class="sxs-lookup"><span data-stu-id="caf91-121">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="caf91-122">示例</span><span class="sxs-lookup"><span data-stu-id="caf91-122">Example</span></span>

<span data-ttu-id="caf91-123">下面是一个简单示例，用于介绍此功能：</span><span class="sxs-lookup"><span data-stu-id="caf91-123">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="caf91-124">分类帐和税金的币种设置</span><span class="sxs-lookup"><span data-stu-id="caf91-124">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="caf91-125">交易币种</span><span class="sxs-lookup"><span data-stu-id="caf91-125">Transaction currency</span></span> | <span data-ttu-id="caf91-126">记帐币种</span><span class="sxs-lookup"><span data-stu-id="caf91-126">Accounting currency</span></span> | <span data-ttu-id="caf91-127">申报币种</span><span class="sxs-lookup"><span data-stu-id="caf91-127">Reporting currency</span></span> | <span data-ttu-id="caf91-128">税金币种</span><span class="sxs-lookup"><span data-stu-id="caf91-128">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="caf91-129">欧元</span><span class="sxs-lookup"><span data-stu-id="caf91-129">EUR</span></span>                  | <span data-ttu-id="caf91-130">美元</span><span class="sxs-lookup"><span data-stu-id="caf91-130">USD</span></span>                 | <span data-ttu-id="caf91-131">GBP</span><span class="sxs-lookup"><span data-stu-id="caf91-131">GBP</span></span>                | <span data-ttu-id="caf91-132">GBP</span><span class="sxs-lookup"><span data-stu-id="caf91-132">GBP</span></span>          |

<span data-ttu-id="caf91-133">汇率</span><span class="sxs-lookup"><span data-stu-id="caf91-133">Exchange rate</span></span>

| <span data-ttu-id="caf91-134">原始币种</span><span class="sxs-lookup"><span data-stu-id="caf91-134">From currency</span></span> | <span data-ttu-id="caf91-135">目标币种</span><span class="sxs-lookup"><span data-stu-id="caf91-135">To currency</span></span> | <span data-ttu-id="caf91-136">系数</span><span class="sxs-lookup"><span data-stu-id="caf91-136">Factor</span></span> | <span data-ttu-id="caf91-137">汇率</span><span class="sxs-lookup"><span data-stu-id="caf91-137">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="caf91-138">欧元</span><span class="sxs-lookup"><span data-stu-id="caf91-138">EUR</span></span>           | <span data-ttu-id="caf91-139">美元</span><span class="sxs-lookup"><span data-stu-id="caf91-139">USD</span></span>         | <span data-ttu-id="caf91-140">1</span><span class="sxs-lookup"><span data-stu-id="caf91-140">1</span></span>      | <span data-ttu-id="caf91-141">1.11</span><span class="sxs-lookup"><span data-stu-id="caf91-141">1.11</span></span>          |
| <span data-ttu-id="caf91-142">欧元</span><span class="sxs-lookup"><span data-stu-id="caf91-142">EUR</span></span>           | <span data-ttu-id="caf91-143">GBP</span><span class="sxs-lookup"><span data-stu-id="caf91-143">GBP</span></span>         | <span data-ttu-id="caf91-144">1</span><span class="sxs-lookup"><span data-stu-id="caf91-144">1</span></span>      | <span data-ttu-id="caf91-145">0.83</span><span class="sxs-lookup"><span data-stu-id="caf91-145">0.83</span></span>          |
| <span data-ttu-id="caf91-146">美元</span><span class="sxs-lookup"><span data-stu-id="caf91-146">USD</span></span>           | <span data-ttu-id="caf91-147">GBP</span><span class="sxs-lookup"><span data-stu-id="caf91-147">GBP</span></span>         | <span data-ttu-id="caf91-148">1</span><span class="sxs-lookup"><span data-stu-id="caf91-148">1</span></span>      | <span data-ttu-id="caf91-149">0.75</span><span class="sxs-lookup"><span data-stu-id="caf91-149">0.75</span></span>          |

<span data-ttu-id="caf91-150">不同参数选项中的税额计算</span><span class="sxs-lookup"><span data-stu-id="caf91-150">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="caf91-151">税额 = 100 欧元</span><span class="sxs-lookup"><span data-stu-id="caf91-151">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="caf91-152">销售税转换参数</span><span class="sxs-lookup"><span data-stu-id="caf91-152">Sales tax conversion parameters</span></span> | <span data-ttu-id="caf91-153">交易币种（欧元）</span><span class="sxs-lookup"><span data-stu-id="caf91-153">Transaction currency (EUR)</span></span> | <span data-ttu-id="caf91-154">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="caf91-154">Accounting currency (USD)</span></span> | <span data-ttu-id="caf91-155">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="caf91-155">Reporting currency (GBP)</span></span> | <span data-ttu-id="caf91-156">税金币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="caf91-156">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="caf91-157">记帐币种</span><span class="sxs-lookup"><span data-stu-id="caf91-157">Accounting currency</span></span>             | <span data-ttu-id="caf91-158">100</span><span class="sxs-lookup"><span data-stu-id="caf91-158">100</span></span>                        | <span data-ttu-id="caf91-159">111</span><span class="sxs-lookup"><span data-stu-id="caf91-159">111</span></span>                       | <span data-ttu-id="caf91-160">83</span><span class="sxs-lookup"><span data-stu-id="caf91-160">83</span></span>                       | <span data-ttu-id="caf91-161">**83.25**</span><span class="sxs-lookup"><span data-stu-id="caf91-161">**83.25**</span></span>          |
| <span data-ttu-id="caf91-162">申报币种</span><span class="sxs-lookup"><span data-stu-id="caf91-162">Reporting currency</span></span>              | <span data-ttu-id="caf91-163">100</span><span class="sxs-lookup"><span data-stu-id="caf91-163">100</span></span>                        | <span data-ttu-id="caf91-164">111</span><span class="sxs-lookup"><span data-stu-id="caf91-164">111</span></span>                       | <span data-ttu-id="caf91-165">83</span><span class="sxs-lookup"><span data-stu-id="caf91-165">83</span></span>                       | <span data-ttu-id="caf91-166">**83**</span><span class="sxs-lookup"><span data-stu-id="caf91-166">**83**</span></span>             |

<span data-ttu-id="caf91-167">可以根据税务部门的合规性要求配置此参数。</span><span class="sxs-lookup"><span data-stu-id="caf91-167">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="caf91-168">升级注意事项</span><span class="sxs-lookup"><span data-stu-id="caf91-168">Upgrade Consideration</span></span>

<span data-ttu-id="caf91-169">此功能仅适用于新交易记录。</span><span class="sxs-lookup"><span data-stu-id="caf91-169">This feature will only apply for new transactions.</span></span> <span data-ttu-id="caf91-170">对于已经使用 TAXTRANS 表保存，但尚未结算的税务交易记录，系统不会使用税金币种重新计算税额，因为已经错过了过帐税时的汇率。</span><span class="sxs-lookup"><span data-stu-id="caf91-170">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="caf91-171">为了避免前面的这种情况，我们建议在不包含任何未结算税务交易记录的新（干净）税务结算期间更改此参数值。</span><span class="sxs-lookup"><span data-stu-id="caf91-171">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="caf91-172">若要在税务结算期间中途更改此值，请在更改此参数值之前，对当前税务结算期间运行“结算并过帐销售税”程序。</span><span class="sxs-lookup"><span data-stu-id="caf91-172">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="caf91-173">跟踪申报币种税额</span><span class="sxs-lookup"><span data-stu-id="caf91-173">Track reporting currency tax amount</span></span>

<span data-ttu-id="caf91-174">已向与税务有关的表添加了三个新字段，用于跟踪申报币种的金额。</span><span class="sxs-lookup"><span data-stu-id="caf91-174">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="caf91-175">这些字段在 TAXUNCOMMITTED 和 TAXTRANS 表中：</span><span class="sxs-lookup"><span data-stu-id="caf91-175">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="caf91-176">TaxAmountRep：申报币种的税额</span><span class="sxs-lookup"><span data-stu-id="caf91-176">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="caf91-177">TaxBaseAmountRep：申报币种的基准额</span><span class="sxs-lookup"><span data-stu-id="caf91-177">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="caf91-178">TaxInCostPriceRep：申报币种的不可扣除金额</span><span class="sxs-lookup"><span data-stu-id="caf91-178">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="caf91-179">对于仅在 TAXUNCOMMITTED 表中保存，但尚未过帐的税金，系统将在过帐时使用申报币种重新计算税额，然后在 TAXTRANS 表中保存。</span><span class="sxs-lookup"><span data-stu-id="caf91-179">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="caf91-180">此版本中不包含对使用申报币种显示税额的报表和窗体的更改。</span><span class="sxs-lookup"><span data-stu-id="caf91-180">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="caf91-181">将在将来的版本中发布对报表和窗体的更改。</span><span class="sxs-lookup"><span data-stu-id="caf91-181">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="caf91-182">税务结算自动平衡采用申报币种</span><span class="sxs-lookup"><span data-stu-id="caf91-182">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="caf91-183">如果因为某种原因（如销售税转换路径为“申报币种”或汇率在单个税金结算期间内改变），未使用申报币种平衡税金结算，系统将自动生成会计条目以调整税额差异，并针对实现的汇兑损益金额进行补偿，这在分类帐设置中配置。</span><span class="sxs-lookup"><span data-stu-id="caf91-183">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="caf91-184">使用前面的示例说明此功能时，假设过帐时 TAXTRANS 表中的数据如下所示：</span><span class="sxs-lookup"><span data-stu-id="caf91-184">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="caf91-185">销售税转换参数</span><span class="sxs-lookup"><span data-stu-id="caf91-185">Sales tax conversion parameters</span></span> | <span data-ttu-id="caf91-186">交易币种（欧元）</span><span class="sxs-lookup"><span data-stu-id="caf91-186">Transaction currency (EUR)</span></span> | <span data-ttu-id="caf91-187">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="caf91-187">Accounting currency (USD)</span></span> | <span data-ttu-id="caf91-188">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="caf91-188">Reporting currency (GBP)</span></span> | <span data-ttu-id="caf91-189">税金币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="caf91-189">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="caf91-190">记帐币种</span><span class="sxs-lookup"><span data-stu-id="caf91-190">Accounting currency</span></span>             | <span data-ttu-id="caf91-191">100</span><span class="sxs-lookup"><span data-stu-id="caf91-191">100</span></span>                        | <span data-ttu-id="caf91-192">111</span><span class="sxs-lookup"><span data-stu-id="caf91-192">111</span></span>                       | <span data-ttu-id="caf91-193">83</span><span class="sxs-lookup"><span data-stu-id="caf91-193">83</span></span>                       | <span data-ttu-id="caf91-194">**83.25**</span><span class="sxs-lookup"><span data-stu-id="caf91-194">**83.25**</span></span>          |
| <span data-ttu-id="caf91-195">申报币种</span><span class="sxs-lookup"><span data-stu-id="caf91-195">Reporting currency</span></span>              | <span data-ttu-id="caf91-196">100</span><span class="sxs-lookup"><span data-stu-id="caf91-196">100</span></span>                        | <span data-ttu-id="caf91-197">111</span><span class="sxs-lookup"><span data-stu-id="caf91-197">111</span></span>                       | <span data-ttu-id="caf91-198">83</span><span class="sxs-lookup"><span data-stu-id="caf91-198">83</span></span>                       | <span data-ttu-id="caf91-199">**83**</span><span class="sxs-lookup"><span data-stu-id="caf91-199">**83**</span></span>             |

<span data-ttu-id="caf91-200">月末运行销售税结算程序时，会计条目将如下所示：</span><span class="sxs-lookup"><span data-stu-id="caf91-200">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="caf91-201">方案：销售税转换 =“记帐币种”</span><span class="sxs-lookup"><span data-stu-id="caf91-201">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="caf91-202">主科目</span><span class="sxs-lookup"><span data-stu-id="caf91-202">Main account</span></span>           | <span data-ttu-id="caf91-203">交易币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="caf91-203">Transaction currency (GBP)</span></span> | <span data-ttu-id="caf91-204">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="caf91-204">Accounting currency (USD)</span></span> | <span data-ttu-id="caf91-205">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="caf91-205">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="caf91-206">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="caf91-206">Tax Payable/Receivable</span></span> | <span data-ttu-id="caf91-207">-83.25</span><span class="sxs-lookup"><span data-stu-id="caf91-207">-83.25</span></span>                     | <span data-ttu-id="caf91-208">-111</span><span class="sxs-lookup"><span data-stu-id="caf91-208">-111</span></span>                      | <span data-ttu-id="caf91-209">-83.25</span><span class="sxs-lookup"><span data-stu-id="caf91-209">-83.25</span></span>                   |
| <span data-ttu-id="caf91-210">税务结算</span><span class="sxs-lookup"><span data-stu-id="caf91-210">Tax Settlement</span></span>         | <span data-ttu-id="caf91-211">83.25</span><span class="sxs-lookup"><span data-stu-id="caf91-211">83.25</span></span>                      | <span data-ttu-id="caf91-212">111</span><span class="sxs-lookup"><span data-stu-id="caf91-212">111</span></span>                       | <span data-ttu-id="caf91-213">83.25</span><span class="sxs-lookup"><span data-stu-id="caf91-213">83.25</span></span>                    |
| <span data-ttu-id="caf91-214">实现的损益</span><span class="sxs-lookup"><span data-stu-id="caf91-214">Realized Gain/Loss</span></span>     | <span data-ttu-id="caf91-215">0</span><span class="sxs-lookup"><span data-stu-id="caf91-215">0</span></span>                          | <span data-ttu-id="caf91-216">0</span><span class="sxs-lookup"><span data-stu-id="caf91-216">0</span></span>                         | <span data-ttu-id="caf91-217">-0.25</span><span class="sxs-lookup"><span data-stu-id="caf91-217">-0.25</span></span>                    |
| <span data-ttu-id="caf91-218">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="caf91-218">Tax Payable/Receivable</span></span> | <span data-ttu-id="caf91-219">0</span><span class="sxs-lookup"><span data-stu-id="caf91-219">0</span></span>                          | <span data-ttu-id="caf91-220">0</span><span class="sxs-lookup"><span data-stu-id="caf91-220">0</span></span>                         | <span data-ttu-id="caf91-221">0.25</span><span class="sxs-lookup"><span data-stu-id="caf91-221">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="caf91-222">方案：销售税转换 =“申报币种”</span><span class="sxs-lookup"><span data-stu-id="caf91-222">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="caf91-223">主科目</span><span class="sxs-lookup"><span data-stu-id="caf91-223">Main account</span></span>           | <span data-ttu-id="caf91-224">交易币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="caf91-224">Transaction currency (GBP)</span></span> | <span data-ttu-id="caf91-225">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="caf91-225">Accounting currency (USD)</span></span> | <span data-ttu-id="caf91-226">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="caf91-226">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="caf91-227">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="caf91-227">Tax Payable/Receivable</span></span> | <span data-ttu-id="caf91-228">-83</span><span class="sxs-lookup"><span data-stu-id="caf91-228">-83</span></span>                        | <span data-ttu-id="caf91-229">-110.67</span><span class="sxs-lookup"><span data-stu-id="caf91-229">-110.67</span></span>                   | <span data-ttu-id="caf91-230">-83</span><span class="sxs-lookup"><span data-stu-id="caf91-230">-83</span></span>                      |
| <span data-ttu-id="caf91-231">税务结算</span><span class="sxs-lookup"><span data-stu-id="caf91-231">Tax Settlement</span></span>         | <span data-ttu-id="caf91-232">83</span><span class="sxs-lookup"><span data-stu-id="caf91-232">83</span></span>                         | <span data-ttu-id="caf91-233">110.67</span><span class="sxs-lookup"><span data-stu-id="caf91-233">110.67</span></span>                    | <span data-ttu-id="caf91-234">83</span><span class="sxs-lookup"><span data-stu-id="caf91-234">83</span></span>                       |
| <span data-ttu-id="caf91-235">实现的损益</span><span class="sxs-lookup"><span data-stu-id="caf91-235">Realized Gain/Loss</span></span>     | <span data-ttu-id="caf91-236">0</span><span class="sxs-lookup"><span data-stu-id="caf91-236">0</span></span>                          | <span data-ttu-id="caf91-237">0.33</span><span class="sxs-lookup"><span data-stu-id="caf91-237">0.33</span></span>                      | <span data-ttu-id="caf91-238">0</span><span class="sxs-lookup"><span data-stu-id="caf91-238">0</span></span>                        |
| <span data-ttu-id="caf91-239">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="caf91-239">Tax Payable/Receivable</span></span> | <span data-ttu-id="caf91-240">0</span><span class="sxs-lookup"><span data-stu-id="caf91-240">0</span></span>                          | <span data-ttu-id="caf91-241">-0.33</span><span class="sxs-lookup"><span data-stu-id="caf91-241">-0.33</span></span>                     | <span data-ttu-id="caf91-242">0</span><span class="sxs-lookup"><span data-stu-id="caf91-242">0</span></span>                        |



<span data-ttu-id="caf91-243">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="caf91-243">For more information, see the following topics:</span></span>

- [<span data-ttu-id="caf91-244">双货币</span><span class="sxs-lookup"><span data-stu-id="caf91-244">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="caf91-245">销售税概览</span><span class="sxs-lookup"><span data-stu-id="caf91-245">Sales tax overview</span></span>](indirect-taxes-overview.md)

