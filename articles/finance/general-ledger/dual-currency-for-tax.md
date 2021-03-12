---
title: 纳税的双币种支持
description: 此主题介绍如何扩展税域的双币种记帐功能和对税额计算与过帐的影响
author: EricWang
manager: Ann Beebe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 2e3e7ff93ca3c6a2266ba0f33c8eac7ceade0d4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978584"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="1c7a5-103">销售税的双币种支持</span><span class="sxs-lookup"><span data-stu-id="1c7a5-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c7a5-104">此主题介绍如何扩展销售税的双币种记帐功能和对销售税计算、过帐与结算的影响。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="1c7a5-105">版本 8.1（2018 年 10 月）中引入了适用于 Dynamics 365 Finance 的双币种功能。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="1c7a5-106">该功能改变了计算采用申报币种的会计条目的方式。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="1c7a5-107">在早期版本中，交易记录按以下顺序转换为申报币种：</span><span class="sxs-lookup"><span data-stu-id="1c7a5-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="1c7a5-108">使用交易币种计算交易记录合计 > 交易记录金额转换为记帐币种 > 记帐币种金额转换为申报币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="1c7a5-109">启用双币种功能之后，交易记录按照以下顺序转换为申报币种：</span><span class="sxs-lookup"><span data-stu-id="1c7a5-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="1c7a5-110">交易币种金额 > 申报币种金额</span><span class="sxs-lookup"><span data-stu-id="1c7a5-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="1c7a5-111">有关双币种的详细信息，请参阅[双币种](dual-currency.md)。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="1c7a5-112">由于支持双币种，所以功能管理中增加了两项新功能：</span><span class="sxs-lookup"><span data-stu-id="1c7a5-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="1c7a5-113">销售税转换（版本 10.0.13 中的新增功能）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="1c7a5-114">销售税的双币种支持确保使用税金币种准确计算税额，以及同时使用记帐币种和申报币种准确计算销售税结算余额。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="1c7a5-115">销售税换算</span><span class="sxs-lookup"><span data-stu-id="1c7a5-115">Sales tax conversion</span></span>

<span data-ttu-id="1c7a5-116">**销售税转换** 参数提供两个选项，用于将税额从交易币种转换为税金币种。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="1c7a5-117">记帐币种：路径将为“交易币种的金额 > 记帐币种的金额 > 税金币种的金额”。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="1c7a5-118">将把记帐币种汇率类型（在分类帐设置中配置）用于币种转换。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="1c7a5-119">申报币种：路径将为“交易币种的金额 > 申报币种的金额 > 税金币种的金额”。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="1c7a5-120">将把申报币种汇率类型（在分类帐设置中配置）用于币种转换。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="1c7a5-121">示例</span><span class="sxs-lookup"><span data-stu-id="1c7a5-121">Example</span></span>

<span data-ttu-id="1c7a5-122">下面是一个简单示例，用于介绍此功能：</span><span class="sxs-lookup"><span data-stu-id="1c7a5-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="1c7a5-123">分类帐和税金的币种设置</span><span class="sxs-lookup"><span data-stu-id="1c7a5-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="1c7a5-124">交易币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-124">Transaction currency</span></span> | <span data-ttu-id="1c7a5-125">记帐币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-125">Accounting currency</span></span> | <span data-ttu-id="1c7a5-126">申报币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-126">Reporting currency</span></span> | <span data-ttu-id="1c7a5-127">税金币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="1c7a5-128">欧元</span><span class="sxs-lookup"><span data-stu-id="1c7a5-128">EUR</span></span>                  | <span data-ttu-id="1c7a5-129">美元</span><span class="sxs-lookup"><span data-stu-id="1c7a5-129">USD</span></span>                 | <span data-ttu-id="1c7a5-130">GBP</span><span class="sxs-lookup"><span data-stu-id="1c7a5-130">GBP</span></span>                | <span data-ttu-id="1c7a5-131">GBP</span><span class="sxs-lookup"><span data-stu-id="1c7a5-131">GBP</span></span>          |

<span data-ttu-id="1c7a5-132">汇率</span><span class="sxs-lookup"><span data-stu-id="1c7a5-132">Exchange rate</span></span>

| <span data-ttu-id="1c7a5-133">原始币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-133">From currency</span></span> | <span data-ttu-id="1c7a5-134">目标币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-134">To currency</span></span> | <span data-ttu-id="1c7a5-135">系数</span><span class="sxs-lookup"><span data-stu-id="1c7a5-135">Factor</span></span> | <span data-ttu-id="1c7a5-136">汇率</span><span class="sxs-lookup"><span data-stu-id="1c7a5-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="1c7a5-137">欧元</span><span class="sxs-lookup"><span data-stu-id="1c7a5-137">EUR</span></span>           | <span data-ttu-id="1c7a5-138">美元</span><span class="sxs-lookup"><span data-stu-id="1c7a5-138">USD</span></span>         | <span data-ttu-id="1c7a5-139">1</span><span class="sxs-lookup"><span data-stu-id="1c7a5-139">1</span></span>      | <span data-ttu-id="1c7a5-140">1.11</span><span class="sxs-lookup"><span data-stu-id="1c7a5-140">1.11</span></span>          |
| <span data-ttu-id="1c7a5-141">欧元</span><span class="sxs-lookup"><span data-stu-id="1c7a5-141">EUR</span></span>           | <span data-ttu-id="1c7a5-142">GBP</span><span class="sxs-lookup"><span data-stu-id="1c7a5-142">GBP</span></span>         | <span data-ttu-id="1c7a5-143">1</span><span class="sxs-lookup"><span data-stu-id="1c7a5-143">1</span></span>      | <span data-ttu-id="1c7a5-144">0.83</span><span class="sxs-lookup"><span data-stu-id="1c7a5-144">0.83</span></span>          |
| <span data-ttu-id="1c7a5-145">美元</span><span class="sxs-lookup"><span data-stu-id="1c7a5-145">USD</span></span>           | <span data-ttu-id="1c7a5-146">GBP</span><span class="sxs-lookup"><span data-stu-id="1c7a5-146">GBP</span></span>         | <span data-ttu-id="1c7a5-147">1</span><span class="sxs-lookup"><span data-stu-id="1c7a5-147">1</span></span>      | <span data-ttu-id="1c7a5-148">0.75</span><span class="sxs-lookup"><span data-stu-id="1c7a5-148">0.75</span></span>          |

<span data-ttu-id="1c7a5-149">不同参数选项中的税额计算</span><span class="sxs-lookup"><span data-stu-id="1c7a5-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="1c7a5-150">税额 = 100 欧元</span><span class="sxs-lookup"><span data-stu-id="1c7a5-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="1c7a5-151">销售税转换参数</span><span class="sxs-lookup"><span data-stu-id="1c7a5-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="1c7a5-152">交易币种（欧元）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="1c7a5-153">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-153">Accounting currency (USD)</span></span> | <span data-ttu-id="1c7a5-154">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="1c7a5-155">税金币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="1c7a5-156">记帐币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-156">Accounting currency</span></span>             | <span data-ttu-id="1c7a5-157">100</span><span class="sxs-lookup"><span data-stu-id="1c7a5-157">100</span></span>                        | <span data-ttu-id="1c7a5-158">111</span><span class="sxs-lookup"><span data-stu-id="1c7a5-158">111</span></span>                       | <span data-ttu-id="1c7a5-159">83</span><span class="sxs-lookup"><span data-stu-id="1c7a5-159">83</span></span>                       | <span data-ttu-id="1c7a5-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="1c7a5-160">**83.25**</span></span>          |
| <span data-ttu-id="1c7a5-161">申报币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-161">Reporting currency</span></span>              | <span data-ttu-id="1c7a5-162">100</span><span class="sxs-lookup"><span data-stu-id="1c7a5-162">100</span></span>                        | <span data-ttu-id="1c7a5-163">111</span><span class="sxs-lookup"><span data-stu-id="1c7a5-163">111</span></span>                       | <span data-ttu-id="1c7a5-164">83</span><span class="sxs-lookup"><span data-stu-id="1c7a5-164">83</span></span>                       | <span data-ttu-id="1c7a5-165">**83**</span><span class="sxs-lookup"><span data-stu-id="1c7a5-165">**83**</span></span>             |

<span data-ttu-id="1c7a5-166">可以根据税务部门的合规性要求配置此参数。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="1c7a5-167">升级注意事项</span><span class="sxs-lookup"><span data-stu-id="1c7a5-167">Upgrade Consideration</span></span>

<span data-ttu-id="1c7a5-168">此功能仅适用于新交易记录。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="1c7a5-169">对于已经使用 TAXTRANS 表保存，但尚未结算的税务交易记录，系统不会使用税金币种重新计算税额，因为已经错过了过帐税时的汇率。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="1c7a5-170">为了避免前面的这种情况，我们建议在不包含任何未结算税务交易记录的新（干净）税务结算期间更改此参数值。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="1c7a5-171">若要在税务结算期间中途更改此值，请在更改此参数值之前，对当前税务结算期间运行“结算并过帐销售税”程序。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="1c7a5-172">跟踪申报币种税额</span><span class="sxs-lookup"><span data-stu-id="1c7a5-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="1c7a5-173">已向与税务有关的表添加了三个新字段，用于跟踪申报币种的金额。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="1c7a5-174">这些字段在 TAXUNCOMMITTED 和 TAXTRANS 表中：</span><span class="sxs-lookup"><span data-stu-id="1c7a5-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="1c7a5-175">TaxAmountRep：申报币种的税额</span><span class="sxs-lookup"><span data-stu-id="1c7a5-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="1c7a5-176">TaxBaseAmountRep：申报币种的基准额</span><span class="sxs-lookup"><span data-stu-id="1c7a5-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="1c7a5-177">TaxInCostPriceRep：申报币种的不可扣除金额</span><span class="sxs-lookup"><span data-stu-id="1c7a5-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="1c7a5-178">对于仅在 TAXUNCOMMITTED 表中保存，但尚未过帐的税金，系统将在过帐时使用申报币种重新计算税额，然后在 TAXTRANS 表中保存。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="1c7a5-179">此版本中不包含对使用申报币种显示税额的报表和窗体的更改。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="1c7a5-180">将在将来的版本中发布对报表和窗体的更改。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="1c7a5-181">税务结算自动平衡采用申报币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="1c7a5-182">如果因为某种原因（如销售税转换路径为“申报币种”或汇率在单个税金结算期间内改变），未使用申报币种平衡税金结算，系统将自动生成会计条目以调整税额差异，并针对实现的汇兑损益金额进行补偿，这在分类帐设置中配置。</span><span class="sxs-lookup"><span data-stu-id="1c7a5-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="1c7a5-183">使用前面的示例说明此功能时，假设过帐时 TAXTRANS 表中的数据如下所示：</span><span class="sxs-lookup"><span data-stu-id="1c7a5-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="1c7a5-184">销售税转换参数</span><span class="sxs-lookup"><span data-stu-id="1c7a5-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="1c7a5-185">交易币种（欧元）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="1c7a5-186">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-186">Accounting currency (USD)</span></span> | <span data-ttu-id="1c7a5-187">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="1c7a5-188">税金币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="1c7a5-189">记帐币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-189">Accounting currency</span></span>             | <span data-ttu-id="1c7a5-190">100</span><span class="sxs-lookup"><span data-stu-id="1c7a5-190">100</span></span>                        | <span data-ttu-id="1c7a5-191">111</span><span class="sxs-lookup"><span data-stu-id="1c7a5-191">111</span></span>                       | <span data-ttu-id="1c7a5-192">83</span><span class="sxs-lookup"><span data-stu-id="1c7a5-192">83</span></span>                       | <span data-ttu-id="1c7a5-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="1c7a5-193">**83.25**</span></span>          |
| <span data-ttu-id="1c7a5-194">申报币种</span><span class="sxs-lookup"><span data-stu-id="1c7a5-194">Reporting currency</span></span>              | <span data-ttu-id="1c7a5-195">100</span><span class="sxs-lookup"><span data-stu-id="1c7a5-195">100</span></span>                        | <span data-ttu-id="1c7a5-196">111</span><span class="sxs-lookup"><span data-stu-id="1c7a5-196">111</span></span>                       | <span data-ttu-id="1c7a5-197">83</span><span class="sxs-lookup"><span data-stu-id="1c7a5-197">83</span></span>                       | <span data-ttu-id="1c7a5-198">**83**</span><span class="sxs-lookup"><span data-stu-id="1c7a5-198">**83**</span></span>             |

<span data-ttu-id="1c7a5-199">月末运行销售税结算程序时，会计条目将如下所示：</span><span class="sxs-lookup"><span data-stu-id="1c7a5-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="1c7a5-200">方案：销售税转换 =“记帐币种”</span><span class="sxs-lookup"><span data-stu-id="1c7a5-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="1c7a5-201">主科目</span><span class="sxs-lookup"><span data-stu-id="1c7a5-201">Main account</span></span>           | <span data-ttu-id="1c7a5-202">交易币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="1c7a5-203">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-203">Accounting currency (USD)</span></span> | <span data-ttu-id="1c7a5-204">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="1c7a5-205">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="1c7a5-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="1c7a5-206">-83.25</span><span class="sxs-lookup"><span data-stu-id="1c7a5-206">-83.25</span></span>                     | <span data-ttu-id="1c7a5-207">-111</span><span class="sxs-lookup"><span data-stu-id="1c7a5-207">-111</span></span>                      | <span data-ttu-id="1c7a5-208">-83.25</span><span class="sxs-lookup"><span data-stu-id="1c7a5-208">-83.25</span></span>                   |
| <span data-ttu-id="1c7a5-209">税务结算</span><span class="sxs-lookup"><span data-stu-id="1c7a5-209">Tax Settlement</span></span>         | <span data-ttu-id="1c7a5-210">83.25</span><span class="sxs-lookup"><span data-stu-id="1c7a5-210">83.25</span></span>                      | <span data-ttu-id="1c7a5-211">111</span><span class="sxs-lookup"><span data-stu-id="1c7a5-211">111</span></span>                       | <span data-ttu-id="1c7a5-212">83.25</span><span class="sxs-lookup"><span data-stu-id="1c7a5-212">83.25</span></span>                    |
| <span data-ttu-id="1c7a5-213">实现的损益</span><span class="sxs-lookup"><span data-stu-id="1c7a5-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="1c7a5-214">0</span><span class="sxs-lookup"><span data-stu-id="1c7a5-214">0</span></span>                          | <span data-ttu-id="1c7a5-215">0</span><span class="sxs-lookup"><span data-stu-id="1c7a5-215">0</span></span>                         | <span data-ttu-id="1c7a5-216">-0.25</span><span class="sxs-lookup"><span data-stu-id="1c7a5-216">-0.25</span></span>                    |
| <span data-ttu-id="1c7a5-217">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="1c7a5-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="1c7a5-218">0</span><span class="sxs-lookup"><span data-stu-id="1c7a5-218">0</span></span>                          | <span data-ttu-id="1c7a5-219">0</span><span class="sxs-lookup"><span data-stu-id="1c7a5-219">0</span></span>                         | <span data-ttu-id="1c7a5-220">0.25</span><span class="sxs-lookup"><span data-stu-id="1c7a5-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="1c7a5-221">方案：销售税转换 =“申报币种”</span><span class="sxs-lookup"><span data-stu-id="1c7a5-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="1c7a5-222">主科目</span><span class="sxs-lookup"><span data-stu-id="1c7a5-222">Main account</span></span>           | <span data-ttu-id="1c7a5-223">交易币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="1c7a5-224">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-224">Accounting currency (USD)</span></span> | <span data-ttu-id="1c7a5-225">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="1c7a5-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="1c7a5-226">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="1c7a5-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="1c7a5-227">-83</span><span class="sxs-lookup"><span data-stu-id="1c7a5-227">-83</span></span>                        | <span data-ttu-id="1c7a5-228">-110.67</span><span class="sxs-lookup"><span data-stu-id="1c7a5-228">-110.67</span></span>                   | <span data-ttu-id="1c7a5-229">-83</span><span class="sxs-lookup"><span data-stu-id="1c7a5-229">-83</span></span>                      |
| <span data-ttu-id="1c7a5-230">税务结算</span><span class="sxs-lookup"><span data-stu-id="1c7a5-230">Tax Settlement</span></span>         | <span data-ttu-id="1c7a5-231">83</span><span class="sxs-lookup"><span data-stu-id="1c7a5-231">83</span></span>                         | <span data-ttu-id="1c7a5-232">110.67</span><span class="sxs-lookup"><span data-stu-id="1c7a5-232">110.67</span></span>                    | <span data-ttu-id="1c7a5-233">83</span><span class="sxs-lookup"><span data-stu-id="1c7a5-233">83</span></span>                       |
| <span data-ttu-id="1c7a5-234">实现的损益</span><span class="sxs-lookup"><span data-stu-id="1c7a5-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="1c7a5-235">0</span><span class="sxs-lookup"><span data-stu-id="1c7a5-235">0</span></span>                          | <span data-ttu-id="1c7a5-236">0.33</span><span class="sxs-lookup"><span data-stu-id="1c7a5-236">0.33</span></span>                      | <span data-ttu-id="1c7a5-237">0</span><span class="sxs-lookup"><span data-stu-id="1c7a5-237">0</span></span>                        |
| <span data-ttu-id="1c7a5-238">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="1c7a5-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="1c7a5-239">0</span><span class="sxs-lookup"><span data-stu-id="1c7a5-239">0</span></span>                          | <span data-ttu-id="1c7a5-240">-0.33</span><span class="sxs-lookup"><span data-stu-id="1c7a5-240">-0.33</span></span>                     | <span data-ttu-id="1c7a5-241">0</span><span class="sxs-lookup"><span data-stu-id="1c7a5-241">0</span></span>                        |



<span data-ttu-id="1c7a5-242">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="1c7a5-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="1c7a5-243">双货币</span><span class="sxs-lookup"><span data-stu-id="1c7a5-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="1c7a5-244">销售税概览</span><span class="sxs-lookup"><span data-stu-id="1c7a5-244">Sales tax overview</span></span>](indirect-taxes-overview.md)

