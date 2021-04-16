---
title: 纳税的双币种支持
description: 此主题介绍如何扩展税域的双币种记帐功能和对税额计算与过帐的影响
author: EricWang
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0a3245febe31857181d17bba42e12b65f4ebb40f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832962"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="de5b1-103">销售税的双币种支持</span><span class="sxs-lookup"><span data-stu-id="de5b1-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="de5b1-104">此主题介绍如何扩展销售税的双币种记帐功能和对销售税计算、过帐与结算的影响。</span><span class="sxs-lookup"><span data-stu-id="de5b1-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="de5b1-105">版本 8.1（2018 年 10 月）中引入了适用于 Dynamics 365 Finance 的双币种功能。</span><span class="sxs-lookup"><span data-stu-id="de5b1-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="de5b1-106">该功能改变了计算采用申报币种的会计条目的方式。</span><span class="sxs-lookup"><span data-stu-id="de5b1-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="de5b1-107">在早期版本中，交易记录按以下顺序转换为申报币种：</span><span class="sxs-lookup"><span data-stu-id="de5b1-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="de5b1-108">使用交易币种计算交易记录合计 > 交易记录金额转换为记帐币种 > 记帐币种金额转换为申报币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="de5b1-109">启用双币种功能之后，交易记录按照以下顺序转换为申报币种：</span><span class="sxs-lookup"><span data-stu-id="de5b1-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="de5b1-110">交易币种金额 > 申报币种金额</span><span class="sxs-lookup"><span data-stu-id="de5b1-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="de5b1-111">有关双币种的详细信息，请参阅[双币种](dual-currency.md)。</span><span class="sxs-lookup"><span data-stu-id="de5b1-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="de5b1-112">由于支持双币种，所以功能管理中增加了两项新功能：</span><span class="sxs-lookup"><span data-stu-id="de5b1-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="de5b1-113">销售税转换（版本 10.0.13 中的新增功能）</span><span class="sxs-lookup"><span data-stu-id="de5b1-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="de5b1-114">销售税的双币种支持确保使用税金币种准确计算税额，以及同时使用记帐币种和申报币种准确计算销售税结算余额。</span><span class="sxs-lookup"><span data-stu-id="de5b1-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="de5b1-115">销售税换算</span><span class="sxs-lookup"><span data-stu-id="de5b1-115">Sales tax conversion</span></span>

<span data-ttu-id="de5b1-116">**销售税转换** 参数提供两个选项，用于将税额从交易币种转换为税金币种。</span><span class="sxs-lookup"><span data-stu-id="de5b1-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="de5b1-117">记帐币种：路径将为“交易币种的金额 > 记帐币种的金额 > 税金币种的金额”。</span><span class="sxs-lookup"><span data-stu-id="de5b1-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="de5b1-118">将把记帐币种汇率类型（在分类帐设置中配置）用于币种转换。</span><span class="sxs-lookup"><span data-stu-id="de5b1-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="de5b1-119">申报币种：路径将为“交易币种的金额 > 申报币种的金额 > 税金币种的金额”。</span><span class="sxs-lookup"><span data-stu-id="de5b1-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="de5b1-120">将把申报币种汇率类型（在分类帐设置中配置）用于币种转换。</span><span class="sxs-lookup"><span data-stu-id="de5b1-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="de5b1-121">示例</span><span class="sxs-lookup"><span data-stu-id="de5b1-121">Example</span></span>

<span data-ttu-id="de5b1-122">下面是一个简单示例，用于介绍此功能：</span><span class="sxs-lookup"><span data-stu-id="de5b1-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="de5b1-123">分类帐和税金的币种设置</span><span class="sxs-lookup"><span data-stu-id="de5b1-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="de5b1-124">交易币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-124">Transaction currency</span></span> | <span data-ttu-id="de5b1-125">记帐币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-125">Accounting currency</span></span> | <span data-ttu-id="de5b1-126">申报币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-126">Reporting currency</span></span> | <span data-ttu-id="de5b1-127">税金币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="de5b1-128">欧元</span><span class="sxs-lookup"><span data-stu-id="de5b1-128">EUR</span></span>                  | <span data-ttu-id="de5b1-129">美元</span><span class="sxs-lookup"><span data-stu-id="de5b1-129">USD</span></span>                 | <span data-ttu-id="de5b1-130">GBP</span><span class="sxs-lookup"><span data-stu-id="de5b1-130">GBP</span></span>                | <span data-ttu-id="de5b1-131">GBP</span><span class="sxs-lookup"><span data-stu-id="de5b1-131">GBP</span></span>          |

<span data-ttu-id="de5b1-132">汇率</span><span class="sxs-lookup"><span data-stu-id="de5b1-132">Exchange rate</span></span>

| <span data-ttu-id="de5b1-133">原始币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-133">From currency</span></span> | <span data-ttu-id="de5b1-134">目标币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-134">To currency</span></span> | <span data-ttu-id="de5b1-135">系数</span><span class="sxs-lookup"><span data-stu-id="de5b1-135">Factor</span></span> | <span data-ttu-id="de5b1-136">汇率</span><span class="sxs-lookup"><span data-stu-id="de5b1-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="de5b1-137">欧元</span><span class="sxs-lookup"><span data-stu-id="de5b1-137">EUR</span></span>           | <span data-ttu-id="de5b1-138">美元</span><span class="sxs-lookup"><span data-stu-id="de5b1-138">USD</span></span>         | <span data-ttu-id="de5b1-139">1</span><span class="sxs-lookup"><span data-stu-id="de5b1-139">1</span></span>      | <span data-ttu-id="de5b1-140">1.11</span><span class="sxs-lookup"><span data-stu-id="de5b1-140">1.11</span></span>          |
| <span data-ttu-id="de5b1-141">欧元</span><span class="sxs-lookup"><span data-stu-id="de5b1-141">EUR</span></span>           | <span data-ttu-id="de5b1-142">GBP</span><span class="sxs-lookup"><span data-stu-id="de5b1-142">GBP</span></span>         | <span data-ttu-id="de5b1-143">1</span><span class="sxs-lookup"><span data-stu-id="de5b1-143">1</span></span>      | <span data-ttu-id="de5b1-144">0.83</span><span class="sxs-lookup"><span data-stu-id="de5b1-144">0.83</span></span>          |
| <span data-ttu-id="de5b1-145">美元</span><span class="sxs-lookup"><span data-stu-id="de5b1-145">USD</span></span>           | <span data-ttu-id="de5b1-146">GBP</span><span class="sxs-lookup"><span data-stu-id="de5b1-146">GBP</span></span>         | <span data-ttu-id="de5b1-147">1</span><span class="sxs-lookup"><span data-stu-id="de5b1-147">1</span></span>      | <span data-ttu-id="de5b1-148">0.75</span><span class="sxs-lookup"><span data-stu-id="de5b1-148">0.75</span></span>          |

<span data-ttu-id="de5b1-149">不同参数选项中的税额计算</span><span class="sxs-lookup"><span data-stu-id="de5b1-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="de5b1-150">税额 = 100 欧元</span><span class="sxs-lookup"><span data-stu-id="de5b1-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="de5b1-151">销售税转换参数</span><span class="sxs-lookup"><span data-stu-id="de5b1-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="de5b1-152">交易币种（欧元）</span><span class="sxs-lookup"><span data-stu-id="de5b1-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="de5b1-153">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="de5b1-153">Accounting currency (USD)</span></span> | <span data-ttu-id="de5b1-154">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="de5b1-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="de5b1-155">税金币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="de5b1-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="de5b1-156">记帐币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-156">Accounting currency</span></span>             | <span data-ttu-id="de5b1-157">100</span><span class="sxs-lookup"><span data-stu-id="de5b1-157">100</span></span>                        | <span data-ttu-id="de5b1-158">111</span><span class="sxs-lookup"><span data-stu-id="de5b1-158">111</span></span>                       | <span data-ttu-id="de5b1-159">83</span><span class="sxs-lookup"><span data-stu-id="de5b1-159">83</span></span>                       | <span data-ttu-id="de5b1-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="de5b1-160">**83.25**</span></span>          |
| <span data-ttu-id="de5b1-161">申报币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-161">Reporting currency</span></span>              | <span data-ttu-id="de5b1-162">100</span><span class="sxs-lookup"><span data-stu-id="de5b1-162">100</span></span>                        | <span data-ttu-id="de5b1-163">111</span><span class="sxs-lookup"><span data-stu-id="de5b1-163">111</span></span>                       | <span data-ttu-id="de5b1-164">83</span><span class="sxs-lookup"><span data-stu-id="de5b1-164">83</span></span>                       | <span data-ttu-id="de5b1-165">**83**</span><span class="sxs-lookup"><span data-stu-id="de5b1-165">**83**</span></span>             |

<span data-ttu-id="de5b1-166">可以根据税务部门的合规性要求配置此参数。</span><span class="sxs-lookup"><span data-stu-id="de5b1-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="de5b1-167">升级注意事项</span><span class="sxs-lookup"><span data-stu-id="de5b1-167">Upgrade Consideration</span></span>

<span data-ttu-id="de5b1-168">此功能仅适用于新交易记录。</span><span class="sxs-lookup"><span data-stu-id="de5b1-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="de5b1-169">对于已经使用 TAXTRANS 表保存，但尚未结算的税务交易记录，系统不会使用税金币种重新计算税额，因为已经错过了过帐税时的汇率。</span><span class="sxs-lookup"><span data-stu-id="de5b1-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="de5b1-170">为了避免前面的这种情况，我们建议在不包含任何未结算税务交易记录的新（干净）税务结算期间更改此参数值。</span><span class="sxs-lookup"><span data-stu-id="de5b1-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="de5b1-171">若要在税务结算期间中途更改此值，请在更改此参数值之前，对当前税务结算期间运行“结算并过帐销售税”程序。</span><span class="sxs-lookup"><span data-stu-id="de5b1-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="de5b1-172">跟踪申报币种税额</span><span class="sxs-lookup"><span data-stu-id="de5b1-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="de5b1-173">已向与税务有关的表添加了三个新字段，用于跟踪申报币种的金额。</span><span class="sxs-lookup"><span data-stu-id="de5b1-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="de5b1-174">这些字段在 TAXUNCOMMITTED 和 TAXTRANS 表中：</span><span class="sxs-lookup"><span data-stu-id="de5b1-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="de5b1-175">TaxAmountRep：申报币种的税额</span><span class="sxs-lookup"><span data-stu-id="de5b1-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="de5b1-176">TaxBaseAmountRep：申报币种的基准额</span><span class="sxs-lookup"><span data-stu-id="de5b1-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="de5b1-177">TaxInCostPriceRep：申报币种的不可扣除金额</span><span class="sxs-lookup"><span data-stu-id="de5b1-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="de5b1-178">对于仅在 TAXUNCOMMITTED 表中保存，但尚未过帐的税金，系统将在过帐时使用申报币种重新计算税额，然后在 TAXTRANS 表中保存。</span><span class="sxs-lookup"><span data-stu-id="de5b1-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="de5b1-179">此版本中不包含对使用申报币种显示税额的报表和窗体的更改。</span><span class="sxs-lookup"><span data-stu-id="de5b1-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="de5b1-180">将在将来的版本中发布对报表和窗体的更改。</span><span class="sxs-lookup"><span data-stu-id="de5b1-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="de5b1-181">税务结算自动平衡采用申报币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="de5b1-182">如果因为某种原因（如销售税转换路径为“申报币种”或汇率在单个税金结算期间内改变），未使用申报币种平衡税金结算，系统将自动生成会计条目以调整税额差异，并针对实现的汇兑损益金额进行补偿，这在分类帐设置中配置。</span><span class="sxs-lookup"><span data-stu-id="de5b1-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="de5b1-183">使用前面的示例说明此功能时，假设过帐时 TAXTRANS 表中的数据如下所示：</span><span class="sxs-lookup"><span data-stu-id="de5b1-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="de5b1-184">销售税转换参数</span><span class="sxs-lookup"><span data-stu-id="de5b1-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="de5b1-185">交易币种（欧元）</span><span class="sxs-lookup"><span data-stu-id="de5b1-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="de5b1-186">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="de5b1-186">Accounting currency (USD)</span></span> | <span data-ttu-id="de5b1-187">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="de5b1-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="de5b1-188">税金币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="de5b1-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="de5b1-189">记帐币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-189">Accounting currency</span></span>             | <span data-ttu-id="de5b1-190">100</span><span class="sxs-lookup"><span data-stu-id="de5b1-190">100</span></span>                        | <span data-ttu-id="de5b1-191">111</span><span class="sxs-lookup"><span data-stu-id="de5b1-191">111</span></span>                       | <span data-ttu-id="de5b1-192">83</span><span class="sxs-lookup"><span data-stu-id="de5b1-192">83</span></span>                       | <span data-ttu-id="de5b1-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="de5b1-193">**83.25**</span></span>          |
| <span data-ttu-id="de5b1-194">申报币种</span><span class="sxs-lookup"><span data-stu-id="de5b1-194">Reporting currency</span></span>              | <span data-ttu-id="de5b1-195">100</span><span class="sxs-lookup"><span data-stu-id="de5b1-195">100</span></span>                        | <span data-ttu-id="de5b1-196">111</span><span class="sxs-lookup"><span data-stu-id="de5b1-196">111</span></span>                       | <span data-ttu-id="de5b1-197">83</span><span class="sxs-lookup"><span data-stu-id="de5b1-197">83</span></span>                       | <span data-ttu-id="de5b1-198">**83**</span><span class="sxs-lookup"><span data-stu-id="de5b1-198">**83**</span></span>             |

<span data-ttu-id="de5b1-199">月末运行销售税结算程序时，会计条目将如下所示：</span><span class="sxs-lookup"><span data-stu-id="de5b1-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="de5b1-200">方案：销售税转换 =“记帐币种”</span><span class="sxs-lookup"><span data-stu-id="de5b1-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="de5b1-201">主科目</span><span class="sxs-lookup"><span data-stu-id="de5b1-201">Main account</span></span>           | <span data-ttu-id="de5b1-202">交易币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="de5b1-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="de5b1-203">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="de5b1-203">Accounting currency (USD)</span></span> | <span data-ttu-id="de5b1-204">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="de5b1-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="de5b1-205">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="de5b1-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="de5b1-206">-83.25</span><span class="sxs-lookup"><span data-stu-id="de5b1-206">-83.25</span></span>                     | <span data-ttu-id="de5b1-207">-111</span><span class="sxs-lookup"><span data-stu-id="de5b1-207">-111</span></span>                      | <span data-ttu-id="de5b1-208">-83.25</span><span class="sxs-lookup"><span data-stu-id="de5b1-208">-83.25</span></span>                   |
| <span data-ttu-id="de5b1-209">税务结算</span><span class="sxs-lookup"><span data-stu-id="de5b1-209">Tax Settlement</span></span>         | <span data-ttu-id="de5b1-210">83.25</span><span class="sxs-lookup"><span data-stu-id="de5b1-210">83.25</span></span>                      | <span data-ttu-id="de5b1-211">111</span><span class="sxs-lookup"><span data-stu-id="de5b1-211">111</span></span>                       | <span data-ttu-id="de5b1-212">83.25</span><span class="sxs-lookup"><span data-stu-id="de5b1-212">83.25</span></span>                    |
| <span data-ttu-id="de5b1-213">实现的损益</span><span class="sxs-lookup"><span data-stu-id="de5b1-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="de5b1-214">0</span><span class="sxs-lookup"><span data-stu-id="de5b1-214">0</span></span>                          | <span data-ttu-id="de5b1-215">0</span><span class="sxs-lookup"><span data-stu-id="de5b1-215">0</span></span>                         | <span data-ttu-id="de5b1-216">-0.25</span><span class="sxs-lookup"><span data-stu-id="de5b1-216">-0.25</span></span>                    |
| <span data-ttu-id="de5b1-217">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="de5b1-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="de5b1-218">0</span><span class="sxs-lookup"><span data-stu-id="de5b1-218">0</span></span>                          | <span data-ttu-id="de5b1-219">0</span><span class="sxs-lookup"><span data-stu-id="de5b1-219">0</span></span>                         | <span data-ttu-id="de5b1-220">0.25</span><span class="sxs-lookup"><span data-stu-id="de5b1-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="de5b1-221">方案：销售税转换 =“申报币种”</span><span class="sxs-lookup"><span data-stu-id="de5b1-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="de5b1-222">主科目</span><span class="sxs-lookup"><span data-stu-id="de5b1-222">Main account</span></span>           | <span data-ttu-id="de5b1-223">交易币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="de5b1-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="de5b1-224">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="de5b1-224">Accounting currency (USD)</span></span> | <span data-ttu-id="de5b1-225">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="de5b1-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="de5b1-226">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="de5b1-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="de5b1-227">-83</span><span class="sxs-lookup"><span data-stu-id="de5b1-227">-83</span></span>                        | <span data-ttu-id="de5b1-228">-110.67</span><span class="sxs-lookup"><span data-stu-id="de5b1-228">-110.67</span></span>                   | <span data-ttu-id="de5b1-229">-83</span><span class="sxs-lookup"><span data-stu-id="de5b1-229">-83</span></span>                      |
| <span data-ttu-id="de5b1-230">税务结算</span><span class="sxs-lookup"><span data-stu-id="de5b1-230">Tax Settlement</span></span>         | <span data-ttu-id="de5b1-231">83</span><span class="sxs-lookup"><span data-stu-id="de5b1-231">83</span></span>                         | <span data-ttu-id="de5b1-232">110.67</span><span class="sxs-lookup"><span data-stu-id="de5b1-232">110.67</span></span>                    | <span data-ttu-id="de5b1-233">83</span><span class="sxs-lookup"><span data-stu-id="de5b1-233">83</span></span>                       |
| <span data-ttu-id="de5b1-234">实现的损益</span><span class="sxs-lookup"><span data-stu-id="de5b1-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="de5b1-235">0</span><span class="sxs-lookup"><span data-stu-id="de5b1-235">0</span></span>                          | <span data-ttu-id="de5b1-236">0.33</span><span class="sxs-lookup"><span data-stu-id="de5b1-236">0.33</span></span>                      | <span data-ttu-id="de5b1-237">0</span><span class="sxs-lookup"><span data-stu-id="de5b1-237">0</span></span>                        |
| <span data-ttu-id="de5b1-238">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="de5b1-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="de5b1-239">0</span><span class="sxs-lookup"><span data-stu-id="de5b1-239">0</span></span>                          | <span data-ttu-id="de5b1-240">-0.33</span><span class="sxs-lookup"><span data-stu-id="de5b1-240">-0.33</span></span>                     | <span data-ttu-id="de5b1-241">0</span><span class="sxs-lookup"><span data-stu-id="de5b1-241">0</span></span>                        |



<span data-ttu-id="de5b1-242">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="de5b1-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="de5b1-243">双货币</span><span class="sxs-lookup"><span data-stu-id="de5b1-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="de5b1-244">销售税概览</span><span class="sxs-lookup"><span data-stu-id="de5b1-244">Sales tax overview</span></span>](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]