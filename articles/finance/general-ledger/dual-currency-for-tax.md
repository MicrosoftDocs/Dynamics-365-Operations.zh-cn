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
ms.openlocfilehash: 3673642729aa41fa3c00a09fe8fe205edd0624c7
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/24/2021
ms.locfileid: "6088457"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="7a23f-103">销售税的双币种支持</span><span class="sxs-lookup"><span data-stu-id="7a23f-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a23f-104">此主题介绍如何扩展销售税的双币种记帐功能和对销售税计算、过帐与结算的影响。</span><span class="sxs-lookup"><span data-stu-id="7a23f-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="7a23f-105">版本 8.1（2018 年 10 月）中引入了适用于 Dynamics 365 Finance 的双币种功能。</span><span class="sxs-lookup"><span data-stu-id="7a23f-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="7a23f-106">该功能改变了计算采用申报币种的会计条目的方式。</span><span class="sxs-lookup"><span data-stu-id="7a23f-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="7a23f-107">在早期版本中，交易记录按以下顺序转换为申报币种：</span><span class="sxs-lookup"><span data-stu-id="7a23f-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="7a23f-108">使用交易币种计算交易记录合计 > 交易记录金额转换为记帐币种 > 记帐币种金额转换为申报币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="7a23f-109">启用双币种功能之后，交易记录按照以下顺序转换为申报币种：</span><span class="sxs-lookup"><span data-stu-id="7a23f-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="7a23f-110">交易币种金额 > 申报币种金额</span><span class="sxs-lookup"><span data-stu-id="7a23f-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="7a23f-111">有关双币种的详细信息，请参阅[双币种](dual-currency.md)。</span><span class="sxs-lookup"><span data-stu-id="7a23f-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="7a23f-112">由于支持双币种，所以功能管理中增加了两项新功能：</span><span class="sxs-lookup"><span data-stu-id="7a23f-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="7a23f-113">销售税转换（版本 10.0.13 中的新增功能）</span><span class="sxs-lookup"><span data-stu-id="7a23f-113">Sales tax conversion (new in version 10.0.13)</span></span>
- <span data-ttu-id="7a23f-114">在已实现的币种调整损益科目中输入财务维度以进行销售税结算（版本 10.0.17 中的新功能）</span><span class="sxs-lookup"><span data-stu-id="7a23f-114">Enter financial dimensions in the realized currency adjustment profit/loss accounts for sales tax settlement (new in version 10.0.17)</span></span>

<span data-ttu-id="7a23f-115">销售税的双币种支持确保使用税金币种准确计算税额，以及同时使用记帐币种和申报币种准确计算销售税结算余额。</span><span class="sxs-lookup"><span data-stu-id="7a23f-115">Dual currency support for sales taxes ensures that taxes are accurately calculated in the tax currency, and that the sales tax settlement balance is accurately calculated in both the accounting currency and the reporting currency.</span></span>

## <a name="sales-tax-conversion"></a><span data-ttu-id="7a23f-116">销售税换算</span><span class="sxs-lookup"><span data-stu-id="7a23f-116">Sales tax conversion</span></span>

<span data-ttu-id="7a23f-117">**销售税转换** 参数提供两个选项，用于将税额从交易币种转换为税金币种。</span><span class="sxs-lookup"><span data-stu-id="7a23f-117">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="7a23f-118">记帐币种：路径将为“交易币种的金额 > 记帐币种的金额 > 税金币种的金额”。</span><span class="sxs-lookup"><span data-stu-id="7a23f-118">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="7a23f-119">将把记帐币种汇率类型（在分类帐设置中配置）用于币种转换。</span><span class="sxs-lookup"><span data-stu-id="7a23f-119">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="7a23f-120">申报币种：路径将为“交易币种的金额 > 申报币种的金额 > 税金币种的金额”。</span><span class="sxs-lookup"><span data-stu-id="7a23f-120">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="7a23f-121">将把申报币种汇率类型（在分类帐设置中配置）用于币种转换。</span><span class="sxs-lookup"><span data-stu-id="7a23f-121">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="7a23f-122">示例</span><span class="sxs-lookup"><span data-stu-id="7a23f-122">Example</span></span>

<span data-ttu-id="7a23f-123">下面是一个简单示例，用于介绍此功能：</span><span class="sxs-lookup"><span data-stu-id="7a23f-123">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="7a23f-124">分类帐和税金的币种设置</span><span class="sxs-lookup"><span data-stu-id="7a23f-124">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="7a23f-125">交易币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-125">Transaction currency</span></span> | <span data-ttu-id="7a23f-126">记帐币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-126">Accounting currency</span></span> | <span data-ttu-id="7a23f-127">申报币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-127">Reporting currency</span></span> | <span data-ttu-id="7a23f-128">税金币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-128">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="7a23f-129">欧元</span><span class="sxs-lookup"><span data-stu-id="7a23f-129">EUR</span></span>                  | <span data-ttu-id="7a23f-130">美元</span><span class="sxs-lookup"><span data-stu-id="7a23f-130">USD</span></span>                 | <span data-ttu-id="7a23f-131">GBP</span><span class="sxs-lookup"><span data-stu-id="7a23f-131">GBP</span></span>                | <span data-ttu-id="7a23f-132">GBP</span><span class="sxs-lookup"><span data-stu-id="7a23f-132">GBP</span></span>          |

<span data-ttu-id="7a23f-133">汇率</span><span class="sxs-lookup"><span data-stu-id="7a23f-133">Exchange rate</span></span>

| <span data-ttu-id="7a23f-134">原始币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-134">From currency</span></span> | <span data-ttu-id="7a23f-135">目标币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-135">To currency</span></span> | <span data-ttu-id="7a23f-136">系数</span><span class="sxs-lookup"><span data-stu-id="7a23f-136">Factor</span></span> | <span data-ttu-id="7a23f-137">汇率</span><span class="sxs-lookup"><span data-stu-id="7a23f-137">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="7a23f-138">欧元</span><span class="sxs-lookup"><span data-stu-id="7a23f-138">EUR</span></span>           | <span data-ttu-id="7a23f-139">美元</span><span class="sxs-lookup"><span data-stu-id="7a23f-139">USD</span></span>         | <span data-ttu-id="7a23f-140">1</span><span class="sxs-lookup"><span data-stu-id="7a23f-140">1</span></span>      | <span data-ttu-id="7a23f-141">1.11</span><span class="sxs-lookup"><span data-stu-id="7a23f-141">1.11</span></span>          |
| <span data-ttu-id="7a23f-142">欧元</span><span class="sxs-lookup"><span data-stu-id="7a23f-142">EUR</span></span>           | <span data-ttu-id="7a23f-143">GBP</span><span class="sxs-lookup"><span data-stu-id="7a23f-143">GBP</span></span>         | <span data-ttu-id="7a23f-144">1</span><span class="sxs-lookup"><span data-stu-id="7a23f-144">1</span></span>      | <span data-ttu-id="7a23f-145">0.83</span><span class="sxs-lookup"><span data-stu-id="7a23f-145">0.83</span></span>          |
| <span data-ttu-id="7a23f-146">美元</span><span class="sxs-lookup"><span data-stu-id="7a23f-146">USD</span></span>           | <span data-ttu-id="7a23f-147">GBP</span><span class="sxs-lookup"><span data-stu-id="7a23f-147">GBP</span></span>         | <span data-ttu-id="7a23f-148">1</span><span class="sxs-lookup"><span data-stu-id="7a23f-148">1</span></span>      | <span data-ttu-id="7a23f-149">0.75</span><span class="sxs-lookup"><span data-stu-id="7a23f-149">0.75</span></span>          |

<span data-ttu-id="7a23f-150">不同参数选项中的税额计算</span><span class="sxs-lookup"><span data-stu-id="7a23f-150">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="7a23f-151">税额 = 100 欧元</span><span class="sxs-lookup"><span data-stu-id="7a23f-151">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="7a23f-152">销售税转换参数</span><span class="sxs-lookup"><span data-stu-id="7a23f-152">Sales tax conversion parameters</span></span> | <span data-ttu-id="7a23f-153">交易币种（欧元）</span><span class="sxs-lookup"><span data-stu-id="7a23f-153">Transaction currency (EUR)</span></span> | <span data-ttu-id="7a23f-154">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="7a23f-154">Accounting currency (USD)</span></span> | <span data-ttu-id="7a23f-155">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="7a23f-155">Reporting currency (GBP)</span></span> | <span data-ttu-id="7a23f-156">税金币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="7a23f-156">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="7a23f-157">记帐币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-157">Accounting currency</span></span>             | <span data-ttu-id="7a23f-158">100</span><span class="sxs-lookup"><span data-stu-id="7a23f-158">100</span></span>                        | <span data-ttu-id="7a23f-159">111</span><span class="sxs-lookup"><span data-stu-id="7a23f-159">111</span></span>                       | <span data-ttu-id="7a23f-160">83</span><span class="sxs-lookup"><span data-stu-id="7a23f-160">83</span></span>                       | <span data-ttu-id="7a23f-161">**83.25**</span><span class="sxs-lookup"><span data-stu-id="7a23f-161">**83.25**</span></span>          |
| <span data-ttu-id="7a23f-162">申报币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-162">Reporting currency</span></span>              | <span data-ttu-id="7a23f-163">100</span><span class="sxs-lookup"><span data-stu-id="7a23f-163">100</span></span>                        | <span data-ttu-id="7a23f-164">111</span><span class="sxs-lookup"><span data-stu-id="7a23f-164">111</span></span>                       | <span data-ttu-id="7a23f-165">83</span><span class="sxs-lookup"><span data-stu-id="7a23f-165">83</span></span>                       | <span data-ttu-id="7a23f-166">**83**</span><span class="sxs-lookup"><span data-stu-id="7a23f-166">**83**</span></span>             |

<span data-ttu-id="7a23f-167">可以根据税务部门的合规性要求配置此参数。</span><span class="sxs-lookup"><span data-stu-id="7a23f-167">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="7a23f-168">升级注意事项</span><span class="sxs-lookup"><span data-stu-id="7a23f-168">Upgrade Consideration</span></span>

<span data-ttu-id="7a23f-169">此功能仅适用于新交易记录。</span><span class="sxs-lookup"><span data-stu-id="7a23f-169">This feature will only apply for new transactions.</span></span> <span data-ttu-id="7a23f-170">对于已经使用 TAXTRANS 表保存，但尚未结算的税务交易记录，系统不会使用税金币种重新计算税额，因为已经错过了过帐税时的汇率。</span><span class="sxs-lookup"><span data-stu-id="7a23f-170">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="7a23f-171">为了避免前面的这种情况，我们建议在不包含任何未结算税务交易记录的新（干净）税务结算期间更改此参数值。</span><span class="sxs-lookup"><span data-stu-id="7a23f-171">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="7a23f-172">若要在税务结算期间中途更改此值，请在更改此参数值之前，对当前税务结算期间运行“结算并过帐销售税”程序。</span><span class="sxs-lookup"><span data-stu-id="7a23f-172">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>

<span data-ttu-id="7a23f-173">此功能将添加会计条目来阐明货币兑换的收益和损失。</span><span class="sxs-lookup"><span data-stu-id="7a23f-173">This feature will add accounting entries that clarify gains and losses from currency exchanges.</span></span> <span data-ttu-id="7a23f-174">在销售税结算期间进行重估时，将在已实现的货币调整损益科目中创建条目。</span><span class="sxs-lookup"><span data-stu-id="7a23f-174">The entries will be made in the realized currency adjustment profit and loss accounts when revaluation is done during sales tax settlement.</span></span> <span data-ttu-id="7a23f-175">有关详细信息，请参阅本主题后面的[税务结算自动平衡采用申报币种](#tax-settlement-auto-balance-in-reporting-currency)一节。</span><span class="sxs-lookup"><span data-stu-id="7a23f-175">For more information, see the [Tax settlement auto-balance in reporting currency](#tax-settlement-auto-balance-in-reporting-currency) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="7a23f-176">在结算期间，财务维度的信息从销售税科目（即资产负债表科目）获取，输入到币种调整损益科目（即损益表科目）中。</span><span class="sxs-lookup"><span data-stu-id="7a23f-176">During settlement, information for financial dimensions is taken from sales tax accounts, which are balance sheet accounts, and entered in currency adjustment profit and loss accounts, which are profit and loss statement accounts.</span></span> <span data-ttu-id="7a23f-177">由于资产负债表科目和损益表科目之间对财务维度值的限制不同，因此在“结算和过帐销售税”流程中可能会发生错误。</span><span class="sxs-lookup"><span data-stu-id="7a23f-177">Because restrictions on the value of financial dimensions differ between balance sheet accounts and profit and loss statement accounts, an error can occur during the Settle and post sales tax process.</span></span> <span data-ttu-id="7a23f-178">为避免不得不修改科目结构，您可以启用“将财务维度填充到已实现币种调整损益科目中以进行销售税结算”功能。</span><span class="sxs-lookup"><span data-stu-id="7a23f-178">To avoid having to modify account structures, you can turn on the "Populate financial dimensions to the realized currency adjustment profits/loss accounts for sales tax settlement" feature.</span></span> <span data-ttu-id="7a23f-179">此功能会强制将财务维度派生到币种调整损益科目。</span><span class="sxs-lookup"><span data-stu-id="7a23f-179">This feature will force the derivation of financial dimensions to currency adjustment profits/loss accounts.</span></span> 

## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="7a23f-180">跟踪申报币种税额</span><span class="sxs-lookup"><span data-stu-id="7a23f-180">Track reporting currency tax amount</span></span>

<span data-ttu-id="7a23f-181">已向与税务有关的表添加了三个新字段，用于跟踪申报币种的金额。</span><span class="sxs-lookup"><span data-stu-id="7a23f-181">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="7a23f-182">这些字段在 TAXUNCOMMITTED 和 TAXTRANS 表中：</span><span class="sxs-lookup"><span data-stu-id="7a23f-182">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="7a23f-183">TaxAmountRep：申报币种的税额</span><span class="sxs-lookup"><span data-stu-id="7a23f-183">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="7a23f-184">TaxBaseAmountRep：申报币种的基准额</span><span class="sxs-lookup"><span data-stu-id="7a23f-184">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="7a23f-185">TaxInCostPriceRep：申报币种的不可扣除金额</span><span class="sxs-lookup"><span data-stu-id="7a23f-185">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="7a23f-186">对于仅在 TAXUNCOMMITTED 表中保存，但尚未过帐的税金，系统将在过帐时使用申报币种重新计算税额，然后在 TAXTRANS 表中保存。</span><span class="sxs-lookup"><span data-stu-id="7a23f-186">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="7a23f-187">此版本中不包含对使用申报币种显示税额的报表和窗体的更改。</span><span class="sxs-lookup"><span data-stu-id="7a23f-187">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="7a23f-188">将在将来的版本中发布对报表和窗体的更改。</span><span class="sxs-lookup"><span data-stu-id="7a23f-188">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="7a23f-189">税务结算自动平衡采用申报币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-189">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="7a23f-190">如果因为某种原因（如销售税转换路径为“申报币种”或汇率在单个税金结算期间内改变），未使用申报币种平衡税金结算，系统将自动生成会计条目以调整税额差异，并针对实现的汇兑损益金额进行补偿，这在分类帐设置中配置。</span><span class="sxs-lookup"><span data-stu-id="7a23f-190">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="7a23f-191">使用前面的示例说明此功能时，假设过帐时 TAXTRANS 表中的数据如下所示：</span><span class="sxs-lookup"><span data-stu-id="7a23f-191">Using the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="7a23f-192">销售税转换参数</span><span class="sxs-lookup"><span data-stu-id="7a23f-192">Sales tax conversion parameters</span></span> | <span data-ttu-id="7a23f-193">交易币种（欧元）</span><span class="sxs-lookup"><span data-stu-id="7a23f-193">Transaction currency (EUR)</span></span> | <span data-ttu-id="7a23f-194">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="7a23f-194">Accounting currency (USD)</span></span> | <span data-ttu-id="7a23f-195">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="7a23f-195">Reporting currency (GBP)</span></span> | <span data-ttu-id="7a23f-196">税金币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="7a23f-196">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="7a23f-197">记帐币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-197">Accounting currency</span></span>             | <span data-ttu-id="7a23f-198">100</span><span class="sxs-lookup"><span data-stu-id="7a23f-198">100</span></span>                        | <span data-ttu-id="7a23f-199">111</span><span class="sxs-lookup"><span data-stu-id="7a23f-199">111</span></span>                       | <span data-ttu-id="7a23f-200">83</span><span class="sxs-lookup"><span data-stu-id="7a23f-200">83</span></span>                       | <span data-ttu-id="7a23f-201">**83.25**</span><span class="sxs-lookup"><span data-stu-id="7a23f-201">**83.25**</span></span>          |
| <span data-ttu-id="7a23f-202">申报币种</span><span class="sxs-lookup"><span data-stu-id="7a23f-202">Reporting currency</span></span>              | <span data-ttu-id="7a23f-203">100</span><span class="sxs-lookup"><span data-stu-id="7a23f-203">100</span></span>                        | <span data-ttu-id="7a23f-204">111</span><span class="sxs-lookup"><span data-stu-id="7a23f-204">111</span></span>                       | <span data-ttu-id="7a23f-205">83</span><span class="sxs-lookup"><span data-stu-id="7a23f-205">83</span></span>                       | <span data-ttu-id="7a23f-206">**83**</span><span class="sxs-lookup"><span data-stu-id="7a23f-206">**83**</span></span>             |

<span data-ttu-id="7a23f-207">月末运行销售税结算程序时，会计条目将如下所示。</span><span class="sxs-lookup"><span data-stu-id="7a23f-207">When you run the sales tax settlement program at month-end, the accounting entry will be as follows.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="7a23f-208">方案：销售税转换 =“记帐币种”</span><span class="sxs-lookup"><span data-stu-id="7a23f-208">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="7a23f-209">主帐户</span><span class="sxs-lookup"><span data-stu-id="7a23f-209">Main account</span></span>           | <span data-ttu-id="7a23f-210">交易币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="7a23f-210">Transaction currency (GBP)</span></span> | <span data-ttu-id="7a23f-211">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="7a23f-211">Accounting currency (USD)</span></span> | <span data-ttu-id="7a23f-212">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="7a23f-212">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="7a23f-213">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="7a23f-213">Tax Payable/Receivable</span></span> | <span data-ttu-id="7a23f-214">-83.25</span><span class="sxs-lookup"><span data-stu-id="7a23f-214">-83.25</span></span>                     | <span data-ttu-id="7a23f-215">-111</span><span class="sxs-lookup"><span data-stu-id="7a23f-215">-111</span></span>                      | <span data-ttu-id="7a23f-216">-83.25</span><span class="sxs-lookup"><span data-stu-id="7a23f-216">-83.25</span></span>                   |
| <span data-ttu-id="7a23f-217">税务结算</span><span class="sxs-lookup"><span data-stu-id="7a23f-217">Tax Settlement</span></span>         | <span data-ttu-id="7a23f-218">83.25</span><span class="sxs-lookup"><span data-stu-id="7a23f-218">83.25</span></span>                      | <span data-ttu-id="7a23f-219">111</span><span class="sxs-lookup"><span data-stu-id="7a23f-219">111</span></span>                       | <span data-ttu-id="7a23f-220">83.25</span><span class="sxs-lookup"><span data-stu-id="7a23f-220">83.25</span></span>                    |
| <span data-ttu-id="7a23f-221">实现的损益</span><span class="sxs-lookup"><span data-stu-id="7a23f-221">Realized Gain/Loss</span></span>     | <span data-ttu-id="7a23f-222">0</span><span class="sxs-lookup"><span data-stu-id="7a23f-222">0</span></span>                          | <span data-ttu-id="7a23f-223">0</span><span class="sxs-lookup"><span data-stu-id="7a23f-223">0</span></span>                         | <span data-ttu-id="7a23f-224">-0.25</span><span class="sxs-lookup"><span data-stu-id="7a23f-224">-0.25</span></span>                    |
| <span data-ttu-id="7a23f-225">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="7a23f-225">Tax Payable/Receivable</span></span> | <span data-ttu-id="7a23f-226">0</span><span class="sxs-lookup"><span data-stu-id="7a23f-226">0</span></span>                          | <span data-ttu-id="7a23f-227">0</span><span class="sxs-lookup"><span data-stu-id="7a23f-227">0</span></span>                         | <span data-ttu-id="7a23f-228">0.25</span><span class="sxs-lookup"><span data-stu-id="7a23f-228">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="7a23f-229">方案：销售税转换 =“申报币种”</span><span class="sxs-lookup"><span data-stu-id="7a23f-229">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="7a23f-230">主科目</span><span class="sxs-lookup"><span data-stu-id="7a23f-230">Main account</span></span>           | <span data-ttu-id="7a23f-231">交易币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="7a23f-231">Transaction currency (GBP)</span></span> | <span data-ttu-id="7a23f-232">记帐币种（美元）</span><span class="sxs-lookup"><span data-stu-id="7a23f-232">Accounting currency (USD)</span></span> | <span data-ttu-id="7a23f-233">申报币种（英镑）</span><span class="sxs-lookup"><span data-stu-id="7a23f-233">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="7a23f-234">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="7a23f-234">Tax Payable/Receivable</span></span> | <span data-ttu-id="7a23f-235">-83</span><span class="sxs-lookup"><span data-stu-id="7a23f-235">-83</span></span>                        | <span data-ttu-id="7a23f-236">-110.67</span><span class="sxs-lookup"><span data-stu-id="7a23f-236">-110.67</span></span>                   | <span data-ttu-id="7a23f-237">-83</span><span class="sxs-lookup"><span data-stu-id="7a23f-237">-83</span></span>                      |
| <span data-ttu-id="7a23f-238">税务结算</span><span class="sxs-lookup"><span data-stu-id="7a23f-238">Tax Settlement</span></span>         | <span data-ttu-id="7a23f-239">83</span><span class="sxs-lookup"><span data-stu-id="7a23f-239">83</span></span>                         | <span data-ttu-id="7a23f-240">110.67</span><span class="sxs-lookup"><span data-stu-id="7a23f-240">110.67</span></span>                    | <span data-ttu-id="7a23f-241">83</span><span class="sxs-lookup"><span data-stu-id="7a23f-241">83</span></span>                       |
| <span data-ttu-id="7a23f-242">实现的损益</span><span class="sxs-lookup"><span data-stu-id="7a23f-242">Realized Gain/Loss</span></span>     | <span data-ttu-id="7a23f-243">0</span><span class="sxs-lookup"><span data-stu-id="7a23f-243">0</span></span>                          | <span data-ttu-id="7a23f-244">0.33</span><span class="sxs-lookup"><span data-stu-id="7a23f-244">0.33</span></span>                      | <span data-ttu-id="7a23f-245">0</span><span class="sxs-lookup"><span data-stu-id="7a23f-245">0</span></span>                        |
| <span data-ttu-id="7a23f-246">应付/应收税金</span><span class="sxs-lookup"><span data-stu-id="7a23f-246">Tax Payable/Receivable</span></span> | <span data-ttu-id="7a23f-247">0</span><span class="sxs-lookup"><span data-stu-id="7a23f-247">0</span></span>                          | <span data-ttu-id="7a23f-248">-0.33</span><span class="sxs-lookup"><span data-stu-id="7a23f-248">-0.33</span></span>                     | <span data-ttu-id="7a23f-249">0</span><span class="sxs-lookup"><span data-stu-id="7a23f-249">0</span></span>                        |



<span data-ttu-id="7a23f-250">有关详细信息，请参阅以下主题：</span><span class="sxs-lookup"><span data-stu-id="7a23f-250">For more information, see the following topics:</span></span>

- [<span data-ttu-id="7a23f-251">双货币</span><span class="sxs-lookup"><span data-stu-id="7a23f-251">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="7a23f-252">销售税概览</span><span class="sxs-lookup"><span data-stu-id="7a23f-252">Sales tax overview</span></span>](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
