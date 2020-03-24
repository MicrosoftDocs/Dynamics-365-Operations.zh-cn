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
ms.author: vstehman
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 1ba4d09240888f0c533fb07614e75ffecea0742c
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124085"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="24189-103">销售税的双币种支持</span><span class="sxs-lookup"><span data-stu-id="24189-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="24189-104">此主题介绍如何扩展销售税的双币种记帐功能和对销售税计算、过帐与结算的影响。</span><span class="sxs-lookup"><span data-stu-id="24189-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="24189-105">版本 8.1（2018 年 10 月）中引入了适用于 Dynamics 365 Finance 的双币种功能。</span><span class="sxs-lookup"><span data-stu-id="24189-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="24189-106">该功能改变了计算采用申报币种的会计条目的方式。</span><span class="sxs-lookup"><span data-stu-id="24189-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="24189-107">在早期版本中，交易记录按以下顺序转换为申报币种：</span><span class="sxs-lookup"><span data-stu-id="24189-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

<span data-ttu-id="24189-108">使用交易币种计算交易记录合计 > 交易记录金额转换为记帐币种 > 记帐币种金额转换为申报币种</span><span class="sxs-lookup"><span data-stu-id="24189-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="24189-109">启用双币种功能之后，交易记录按照以下顺序转换为申报币种：</span><span class="sxs-lookup"><span data-stu-id="24189-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="24189-110">交易币种金额 > 申报币种金额</span><span class="sxs-lookup"><span data-stu-id="24189-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="24189-111">有关双币种的详细信息，请参阅[双币种](dual-currency.md)。</span><span class="sxs-lookup"><span data-stu-id="24189-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="24189-112">由于支持双币种，所以功能管理中增加了两项新功能：</span><span class="sxs-lookup"><span data-stu-id="24189-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="24189-113">销售税转换（版本 10.0.9 中发布）</span><span class="sxs-lookup"><span data-stu-id="24189-113">Sales tax conversion (Release in version 10.0.9)</span></span>
- <span data-ttu-id="24189-114">税务结算自动平衡采用申报币种（版本 10.0.11 中发布）</span><span class="sxs-lookup"><span data-stu-id="24189-114">Tax settlement auto balance in reporting currency (Release in version 10.0.11)</span></span>

<span data-ttu-id="24189-115">销售税的双币种支持确保使用税金币种准确计算税额，以及同时使用记帐币种和申报币种准确计算销售税结算余额。</span><span class="sxs-lookup"><span data-stu-id="24189-115">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

<span data-ttu-id="24189-116">这些新功能现在对专用预览客户启用。</span><span class="sxs-lookup"><span data-stu-id="24189-116">The new features are currently enabled for private preview customers.</span></span> <span data-ttu-id="24189-117">若要启用这些功能，请通过相应渠道向 Microsoft 提出服务请求。</span><span class="sxs-lookup"><span data-stu-id="24189-117">To enable the features, raise a service request through corresponding channels to Microsoft.</span></span>

## <a name="sales-tax-conversion"></a><span data-ttu-id="24189-118">销售税换算</span><span class="sxs-lookup"><span data-stu-id="24189-118">Sales tax conversion</span></span>

<span data-ttu-id="24189-119">**销售税转换**参数提供两个选项，用于将税额从交易币种转换为税金币种。</span><span class="sxs-lookup"><span data-stu-id="24189-119">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="24189-120">记帐币种：路径将为“交易币种的金额 > 记帐币种的金额 > 税金币种的金额”。</span><span class="sxs-lookup"><span data-stu-id="24189-120">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="24189-121">将把记帐币种汇率类型（在分类帐设置中配置）用于币种转换。</span><span class="sxs-lookup"><span data-stu-id="24189-121">The accounting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="24189-122">申报币种：路径将为“交易币种的金额 > 申报币种的金额 > 税金币种的金额”。</span><span class="sxs-lookup"><span data-stu-id="24189-122">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="24189-123">将把申报币种汇率类型（在分类帐设置中配置）用于币种转换。</span><span class="sxs-lookup"><span data-stu-id="24189-123">The reporting currency exhange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="24189-124">示例</span><span class="sxs-lookup"><span data-stu-id="24189-124">Example</span></span>

<span data-ttu-id="24189-125">下面是一个简单示例，用于介绍此功能：</span><span class="sxs-lookup"><span data-stu-id="24189-125">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="24189-126">分类帐和税金的币种设置</span><span class="sxs-lookup"><span data-stu-id="24189-126">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="24189-127">交易币种</span><span class="sxs-lookup"><span data-stu-id="24189-127">Transaction currency</span></span> | <span data-ttu-id="24189-128">记帐币种</span><span class="sxs-lookup"><span data-stu-id="24189-128">Accounting currency</span></span> | <span data-ttu-id="24189-129">申报币种</span><span class="sxs-lookup"><span data-stu-id="24189-129">Reporting currency</span></span> | <span data-ttu-id="24189-130">税金币种</span><span class="sxs-lookup"><span data-stu-id="24189-130">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="24189-131">欧元</span><span class="sxs-lookup"><span data-stu-id="24189-131">EUR</span></span>                  | <span data-ttu-id="24189-132">美元</span><span class="sxs-lookup"><span data-stu-id="24189-132">USD</span></span>                 | <span data-ttu-id="24189-133">GBP</span><span class="sxs-lookup"><span data-stu-id="24189-133">GBP</span></span>                | <span data-ttu-id="24189-134">GBP</span><span class="sxs-lookup"><span data-stu-id="24189-134">GBP</span></span>          |

<span data-ttu-id="24189-135">汇率</span><span class="sxs-lookup"><span data-stu-id="24189-135">Exchange rate</span></span>

| <span data-ttu-id="24189-136">原始币种</span><span class="sxs-lookup"><span data-stu-id="24189-136">From currency</span></span> | <span data-ttu-id="24189-137">目标币种</span><span class="sxs-lookup"><span data-stu-id="24189-137">To currency</span></span> | <span data-ttu-id="24189-138">系数</span><span class="sxs-lookup"><span data-stu-id="24189-138">Factor</span></span> | <span data-ttu-id="24189-139">汇率</span><span class="sxs-lookup"><span data-stu-id="24189-139">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="24189-140">欧元</span><span class="sxs-lookup"><span data-stu-id="24189-140">EUR</span></span>           | <span data-ttu-id="24189-141">美元</span><span class="sxs-lookup"><span data-stu-id="24189-141">USD</span></span>         | <span data-ttu-id="24189-142">1</span><span class="sxs-lookup"><span data-stu-id="24189-142">1</span></span>      | <span data-ttu-id="24189-143">1.11</span><span class="sxs-lookup"><span data-stu-id="24189-143">1.11</span></span>          |
| <span data-ttu-id="24189-144">欧元</span><span class="sxs-lookup"><span data-stu-id="24189-144">EUR</span></span>           | <span data-ttu-id="24189-145">GBP</span><span class="sxs-lookup"><span data-stu-id="24189-145">GBP</span></span>         | <span data-ttu-id="24189-146">1</span><span class="sxs-lookup"><span data-stu-id="24189-146">1</span></span>      | <span data-ttu-id="24189-147">0.83</span><span class="sxs-lookup"><span data-stu-id="24189-147">0.83</span></span>          |
| <span data-ttu-id="24189-148">美元</span><span class="sxs-lookup"><span data-stu-id="24189-148">USD</span></span>           | <span data-ttu-id="24189-149">GBP</span><span class="sxs-lookup"><span data-stu-id="24189-149">GBP</span></span>         | <span data-ttu-id="24189-150">1</span><span class="sxs-lookup"><span data-stu-id="24189-150">1</span></span>      | <span data-ttu-id="24189-151">0.75</span><span class="sxs-lookup"><span data-stu-id="24189-151">0.75</span></span>          |

<span data-ttu-id="24189-152">不同参数选项中的税额计算</span><span class="sxs-lookup"><span data-stu-id="24189-152">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="24189-153">税额 = 100 欧元</span><span class="sxs-lookup"><span data-stu-id="24189-153">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="24189-154">销售税转换参数</span><span class="sxs-lookup"><span data-stu-id="24189-154">Sales tax conversion parameters</span></span> | <span data-ttu-id="24189-155">交易币种（欧元）</span><span class="sxs-lookup"><span data-stu-id="24189-155">Transaction currency (EUR)</span></span> | <span data-ttu-id="24189-156">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="24189-156">Accounting currency (USD)</span></span> | <span data-ttu-id="24189-157">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="24189-157">Reporting currency (GBP)</span></span> | <span data-ttu-id="24189-158">税金币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="24189-158">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="24189-159">记帐币种</span><span class="sxs-lookup"><span data-stu-id="24189-159">Accounting currency</span></span>             | <span data-ttu-id="24189-160">100</span><span class="sxs-lookup"><span data-stu-id="24189-160">100</span></span>                        | <span data-ttu-id="24189-161">111</span><span class="sxs-lookup"><span data-stu-id="24189-161">111</span></span>                       | <span data-ttu-id="24189-162">83</span><span class="sxs-lookup"><span data-stu-id="24189-162">83</span></span>                       | <span data-ttu-id="24189-163">**83.25**</span><span class="sxs-lookup"><span data-stu-id="24189-163">**83.25**</span></span>          |
| <span data-ttu-id="24189-164">申报币种</span><span class="sxs-lookup"><span data-stu-id="24189-164">Reporting currency</span></span>              | <span data-ttu-id="24189-165">100</span><span class="sxs-lookup"><span data-stu-id="24189-165">100</span></span>                        | <span data-ttu-id="24189-166">111</span><span class="sxs-lookup"><span data-stu-id="24189-166">111</span></span>                       | <span data-ttu-id="24189-167">83</span><span class="sxs-lookup"><span data-stu-id="24189-167">83</span></span>                       | <span data-ttu-id="24189-168">**83**</span><span class="sxs-lookup"><span data-stu-id="24189-168">**83**</span></span>             |

<span data-ttu-id="24189-169">可以根据税务部门的合规性要求配置此参数。</span><span class="sxs-lookup"><span data-stu-id="24189-169">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="24189-170">升级注意事项</span><span class="sxs-lookup"><span data-stu-id="24189-170">Upgrade Consideration</span></span>

<span data-ttu-id="24189-171">此功能仅适用于新交易记录。</span><span class="sxs-lookup"><span data-stu-id="24189-171">This feature will only apply for new transactions.</span></span> <span data-ttu-id="24189-172">对于已经使用 TAXTRANS 表保存，但尚未结算的税务交易记录，系统不会使用税金币种重新计算税额，因为已经错过了过帐税时的汇率。</span><span class="sxs-lookup"><span data-stu-id="24189-172">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="24189-173">为了避免前面的这种情况，我们建议在不包含任何未结算税务交易记录的新（干净）税务结算期间更改此参数值。</span><span class="sxs-lookup"><span data-stu-id="24189-173">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="24189-174">若要在税务结算期间中途更改此值，请在更改此参数值之前，对当前税务结算期间运行“结算并过帐销售税”程序。</span><span class="sxs-lookup"><span data-stu-id="24189-174">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="24189-175">跟踪申报币种税额</span><span class="sxs-lookup"><span data-stu-id="24189-175">Track reporting currency tax amount</span></span>

<span data-ttu-id="24189-176">已向与税务有关的表添加了三个新字段，用于跟踪申报币种的金额。</span><span class="sxs-lookup"><span data-stu-id="24189-176">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="24189-177">这些字段在 TAXUNCOMMITTED 和 TAXTRANS 表中：</span><span class="sxs-lookup"><span data-stu-id="24189-177">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="24189-178">TaxAmountRep：申报币种的税额</span><span class="sxs-lookup"><span data-stu-id="24189-178">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="24189-179">TaxBaseAmountRep：申报币种的基准额</span><span class="sxs-lookup"><span data-stu-id="24189-179">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="24189-180">TaxInCostPriceRep：申报币种的不可扣除金额</span><span class="sxs-lookup"><span data-stu-id="24189-180">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="24189-181">对于仅在 TAXUNCOMMITTED 表中保存，但尚未过帐的税金，系统将在过帐时使用申报币种重新计算税额，然后在 TAXTRANS 表中保存。</span><span class="sxs-lookup"><span data-stu-id="24189-181">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="24189-182">此版本中不包含对使用申报币种显示税额的报表和窗体的更改。</span><span class="sxs-lookup"><span data-stu-id="24189-182">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="24189-183">将在将来的版本中发布对报表和窗体的更改。</span><span class="sxs-lookup"><span data-stu-id="24189-183">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="24189-184">税务结算自动平衡采用申报币种</span><span class="sxs-lookup"><span data-stu-id="24189-184">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="24189-185">如果因为某种原因（如销售税转换路径为“申报币种”或汇率在单个税金结算期间内改变），未使用申报币种平衡税金结算，系统将自动生成会计条目以调整税额差异，并针对实现的汇兑损益金额进行补偿，这在分类帐设置中配置。</span><span class="sxs-lookup"><span data-stu-id="24189-185">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, thebn the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="24189-186">使用前面的示例说明此功能时，假设过帐时 TAXTRANS 表中的数据如下所示：</span><span class="sxs-lookup"><span data-stu-id="24189-186">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="24189-187">销售税转换参数</span><span class="sxs-lookup"><span data-stu-id="24189-187">Sales tax conversion parameters</span></span> | <span data-ttu-id="24189-188">交易币种（欧元）</span><span class="sxs-lookup"><span data-stu-id="24189-188">Transaction currency (EUR)</span></span> | <span data-ttu-id="24189-189">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="24189-189">Accounting currency (USD)</span></span> | <span data-ttu-id="24189-190">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="24189-190">Reporting currency (GBP)</span></span> | <span data-ttu-id="24189-191">税金币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="24189-191">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="24189-192">记帐币种</span><span class="sxs-lookup"><span data-stu-id="24189-192">Accounting currency</span></span>             | <span data-ttu-id="24189-193">100</span><span class="sxs-lookup"><span data-stu-id="24189-193">100</span></span>                        | <span data-ttu-id="24189-194">111</span><span class="sxs-lookup"><span data-stu-id="24189-194">111</span></span>                       | <span data-ttu-id="24189-195">83</span><span class="sxs-lookup"><span data-stu-id="24189-195">83</span></span>                       | <span data-ttu-id="24189-196">**83.25**</span><span class="sxs-lookup"><span data-stu-id="24189-196">**83.25**</span></span>          |
| <span data-ttu-id="24189-197">申报币种</span><span class="sxs-lookup"><span data-stu-id="24189-197">Reporting currency</span></span>              | <span data-ttu-id="24189-198">100</span><span class="sxs-lookup"><span data-stu-id="24189-198">100</span></span>                        | <span data-ttu-id="24189-199">111</span><span class="sxs-lookup"><span data-stu-id="24189-199">111</span></span>                       | <span data-ttu-id="24189-200">83</span><span class="sxs-lookup"><span data-stu-id="24189-200">83</span></span>                       | <span data-ttu-id="24189-201">**83**</span><span class="sxs-lookup"><span data-stu-id="24189-201">**83**</span></span>             |

<span data-ttu-id="24189-202">月末运行销售税结算程序时，会计条目将如下所示：</span><span class="sxs-lookup"><span data-stu-id="24189-202">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="24189-203">方案：销售税转换 =“记帐币种”</span><span class="sxs-lookup"><span data-stu-id="24189-203">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="24189-204">主科目</span><span class="sxs-lookup"><span data-stu-id="24189-204">Main account</span></span>           | <span data-ttu-id="24189-205">交易币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="24189-205">Transaction currency (GBP)</span></span> | <span data-ttu-id="24189-206">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="24189-206">Accounting currency (USD)</span></span> | <span data-ttu-id="24189-207">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="24189-207">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="24189-208">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="24189-208">Tax Payable/Receivable</span></span> | <span data-ttu-id="24189-209">-83.25</span><span class="sxs-lookup"><span data-stu-id="24189-209">-83.25</span></span>                     | <span data-ttu-id="24189-210">-111</span><span class="sxs-lookup"><span data-stu-id="24189-210">-111</span></span>                      | <span data-ttu-id="24189-211">-83.25</span><span class="sxs-lookup"><span data-stu-id="24189-211">-83.25</span></span>                   |
| <span data-ttu-id="24189-212">税务结算</span><span class="sxs-lookup"><span data-stu-id="24189-212">Tax Settlement</span></span>         | <span data-ttu-id="24189-213">83.25</span><span class="sxs-lookup"><span data-stu-id="24189-213">83.25</span></span>                      | <span data-ttu-id="24189-214">111</span><span class="sxs-lookup"><span data-stu-id="24189-214">111</span></span>                       | <span data-ttu-id="24189-215">83.25</span><span class="sxs-lookup"><span data-stu-id="24189-215">83.25</span></span>                    |
| <span data-ttu-id="24189-216">实现的损益</span><span class="sxs-lookup"><span data-stu-id="24189-216">Realized Gain/Loss</span></span>     | <span data-ttu-id="24189-217">0</span><span class="sxs-lookup"><span data-stu-id="24189-217">0</span></span>                          | <span data-ttu-id="24189-218">0</span><span class="sxs-lookup"><span data-stu-id="24189-218">0</span></span>                         | <span data-ttu-id="24189-219">-0.25</span><span class="sxs-lookup"><span data-stu-id="24189-219">-0.25</span></span>                    |
| <span data-ttu-id="24189-220">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="24189-220">Tax Payable/Receivable</span></span> | <span data-ttu-id="24189-221">0</span><span class="sxs-lookup"><span data-stu-id="24189-221">0</span></span>                          | <span data-ttu-id="24189-222">0</span><span class="sxs-lookup"><span data-stu-id="24189-222">0</span></span>                         | <span data-ttu-id="24189-223">0.25</span><span class="sxs-lookup"><span data-stu-id="24189-223">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="24189-224">方案：销售税转换 =“申报币种”</span><span class="sxs-lookup"><span data-stu-id="24189-224">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="24189-225">主科目</span><span class="sxs-lookup"><span data-stu-id="24189-225">Main account</span></span>           | <span data-ttu-id="24189-226">交易币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="24189-226">Transaction currency (GBP)</span></span> | <span data-ttu-id="24189-227">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="24189-227">Accounting currency (USD)</span></span> | <span data-ttu-id="24189-228">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="24189-228">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="24189-229">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="24189-229">Tax Payable/Receivable</span></span> | <span data-ttu-id="24189-230">-83</span><span class="sxs-lookup"><span data-stu-id="24189-230">-83</span></span>                        | <span data-ttu-id="24189-231">-110.67</span><span class="sxs-lookup"><span data-stu-id="24189-231">-110.67</span></span>                   | <span data-ttu-id="24189-232">-83</span><span class="sxs-lookup"><span data-stu-id="24189-232">-83</span></span>                      |
| <span data-ttu-id="24189-233">税务结算</span><span class="sxs-lookup"><span data-stu-id="24189-233">Tax Settlement</span></span>         | <span data-ttu-id="24189-234">83</span><span class="sxs-lookup"><span data-stu-id="24189-234">83</span></span>                         | <span data-ttu-id="24189-235">110.67</span><span class="sxs-lookup"><span data-stu-id="24189-235">110.67</span></span>                    | <span data-ttu-id="24189-236">83</span><span class="sxs-lookup"><span data-stu-id="24189-236">83</span></span>                       |
| <span data-ttu-id="24189-237">实现的损益</span><span class="sxs-lookup"><span data-stu-id="24189-237">Realized Gain/Loss</span></span>     | <span data-ttu-id="24189-238">0</span><span class="sxs-lookup"><span data-stu-id="24189-238">0</span></span>                          | <span data-ttu-id="24189-239">0.33</span><span class="sxs-lookup"><span data-stu-id="24189-239">0.33</span></span>                      | <span data-ttu-id="24189-240">0</span><span class="sxs-lookup"><span data-stu-id="24189-240">0</span></span>                        |
| <span data-ttu-id="24189-241">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="24189-241">Tax Payable/Receivable</span></span> | <span data-ttu-id="24189-242">0</span><span class="sxs-lookup"><span data-stu-id="24189-242">0</span></span>                          | <span data-ttu-id="24189-243">-0.33</span><span class="sxs-lookup"><span data-stu-id="24189-243">-0.33</span></span>                     | <span data-ttu-id="24189-244">0</span><span class="sxs-lookup"><span data-stu-id="24189-244">0</span></span>                        |



<span data-ttu-id="24189-245">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="24189-245">For more information, see the following topics:</span></span>

- [<span data-ttu-id="24189-246">双货币</span><span class="sxs-lookup"><span data-stu-id="24189-246">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="24189-247">销售税概览</span><span class="sxs-lookup"><span data-stu-id="24189-247">Sales tax overview</span></span>](indirect-taxes-overview.md)

