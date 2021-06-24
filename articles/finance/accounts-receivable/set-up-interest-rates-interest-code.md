---
title: 为利息代码设置多种利率
description: 利息代码包含相关的设置利息时计费，以及如何在逾期科目计算。
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc986ea752d1482f618401058f7a0b18f13efd5f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188702"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="22710-103">为利息代码设置多种利率</span><span class="sxs-lookup"><span data-stu-id="22710-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22710-104">利息代码包含相关的设置利息时计费，以及如何在逾期科目计算。</span><span class="sxs-lookup"><span data-stu-id="22710-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="22710-105">您可以设置一个唯一利息代码和将它应用于多个客户过帐模板，计费代码，或者特定于发票行。</span><span class="sxs-lookup"><span data-stu-id="22710-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="22710-106">在更改利息代码详细信息，使用该代码的所有功能将自动执行在新的交易记录的更改。</span><span class="sxs-lookup"><span data-stu-id="22710-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="22710-107">对于每个利息代码，您可以设置比率的两种类型:</span><span class="sxs-lookup"><span data-stu-id="22710-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="22710-108">利息收入-的汇率表示通过这些收取利息供在发票或利息单的收入。</span><span class="sxs-lookup"><span data-stu-id="22710-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="22710-109">−这些付息的汇率表示为贷方通知单的利息支付的成本。</span><span class="sxs-lookup"><span data-stu-id="22710-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="22710-110">这两个成本率类型可能存在同时在同一和利息代码。</span><span class="sxs-lookup"><span data-stu-id="22710-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="22710-111">可以基于从三种计算类型:</span><span class="sxs-lookup"><span data-stu-id="22710-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="22710-112">利率。</span><span class="sxs-lookup"><span data-stu-id="22710-112">Interest by percentage.</span></span>
-   <span data-ttu-id="22710-113">利息金额。</span><span class="sxs-lookup"><span data-stu-id="22710-113">Interest by amount.</span></span>
-   <span data-ttu-id="22710-114">按范围的利息，将生成一个百分比或金额。</span><span class="sxs-lookup"><span data-stu-id="22710-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="22710-115">在计算利息时，为在付款超出了交易到期日期的时间段中生效的每个利率，都创建单独的利息单。</span><span class="sxs-lookup"><span data-stu-id="22710-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="22710-116">您可以使用 **利息代码** 页上的 **收入** 选项卡为您通过收取利息获取的利息设置利率。</span><span class="sxs-lookup"><span data-stu-id="22710-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="22710-117">使用 **付款** 选项卡可为您支付的利息设置利率。</span><span class="sxs-lookup"><span data-stu-id="22710-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="22710-118">基于百分比的利率</span><span class="sxs-lookup"><span data-stu-id="22710-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="22710-119">您可以设置多种利率计算指定的百分比。</span><span class="sxs-lookup"><span data-stu-id="22710-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="22710-120">利息金额应用于所有币种。</span><span class="sxs-lookup"><span data-stu-id="22710-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="22710-121">可输入可选利息金额限制。</span><span class="sxs-lookup"><span data-stu-id="22710-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="22710-122">**设置利息代码** 页上的 **利息计算依据** 字段中已选择 **百分比**。</span><span class="sxs-lookup"><span data-stu-id="22710-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="22710-123">例如，设置项目 5 的利息每两个月的利息代码发票付款超过交易到期日期，则在 **计算利息间隔** 字段中输入“2”，然后选择 **月**。</span><span class="sxs-lookup"><span data-stu-id="22710-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="22710-124">使用功能管理添加了用于利息单计算的新算法。</span><span class="sxs-lookup"><span data-stu-id="22710-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="22710-125">要使用此算法，请启用 **(GBL) 允许按照年度百分比除以 365 来计算每天利息** 功能。</span><span class="sxs-lookup"><span data-stu-id="22710-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="22710-126">有关如何启用此功能的信息，请参阅[功能管理概述](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="22710-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="22710-127">利息单金额的计算公式为：</span><span class="sxs-lookup"><span data-stu-id="22710-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="22710-128">利息单金额 = 欠款额 \* 年利率%/365 \* 逾期天数</span><span class="sxs-lookup"><span data-stu-id="22710-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="22710-129">版本 10.0.18 或更高版本中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="22710-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="22710-130">基于金额的利率</span><span class="sxs-lookup"><span data-stu-id="22710-130">Interest rates based on amounts</span></span>
<span data-ttu-id="22710-131">您可以设置计算针对指定币种的利率金额。</span><span class="sxs-lookup"><span data-stu-id="22710-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="22710-132">为利息代码中的每个币种指定利息金额。</span><span class="sxs-lookup"><span data-stu-id="22710-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="22710-133">可输入可选利息金额限制。</span><span class="sxs-lookup"><span data-stu-id="22710-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="22710-134">**金额** 是在 **设置利息代码** 页上的 **利息计算依据** 字段中选择的。</span><span class="sxs-lookup"><span data-stu-id="22710-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="22710-135">例如，若要设置发票付款超过交易到期日期每 20 天的 25.00 的利息的利息代码，则在 **计算利息间隔** 字段中输入“20”，然后选择 **天**。</span><span class="sxs-lookup"><span data-stu-id="22710-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="22710-136">基于范围的利率</span><span class="sxs-lookup"><span data-stu-id="22710-136">Interest rates based on ranges</span></span>
<span data-ttu-id="22710-137">您可以设置根据逾期金额更改金额的利率，晚的天数，或金额晚的月份数。</span><span class="sxs-lookup"><span data-stu-id="22710-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="22710-138">您可以使用 **原币收益** 选项卡定义每个币种的特定利息设置。</span><span class="sxs-lookup"><span data-stu-id="22710-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="22710-139">这也是您要定义范围的位置。</span><span class="sxs-lookup"><span data-stu-id="22710-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="22710-140">使用 **范围** 按钮可添加表示您要设孩子的范围的行。</span><span class="sxs-lookup"><span data-stu-id="22710-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="22710-141">**从** 值表示该范围的开始，**利息值** 数字表示百分比或金额，具体取决于 **设置利息代码** 页上的 **利息计算依据** 字段中的选择。</span><span class="sxs-lookup"><span data-stu-id="22710-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="22710-142">示例 1：按大小的利息 = 金额</span><span class="sxs-lookup"><span data-stu-id="22710-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="22710-143">您设置估计利息一次每三个月的利息代码发票付款超过交易到期日期。</span><span class="sxs-lookup"><span data-stu-id="22710-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="22710-144">要基于计算利息百分比值，根据步骤的金额间隔。</span><span class="sxs-lookup"><span data-stu-id="22710-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="22710-145">利息值将与发票金额的 1 金额的 1,000.00，从 1,001.00 到 2 的金额的 5,000.00 和 3，超过 5,000.00。</span><span class="sxs-lookup"><span data-stu-id="22710-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="22710-146">您为利息代码设置了字段的值。</span><span class="sxs-lookup"><span data-stu-id="22710-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="22710-147">**字段名称**</span><span class="sxs-lookup"><span data-stu-id="22710-147">**Field name**</span></span>                  | <span data-ttu-id="22710-148">**字段值**</span><span class="sxs-lookup"><span data-stu-id="22710-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="22710-149">**利息代码**</span><span class="sxs-lookup"><span data-stu-id="22710-149">**Interest code**</span></span>               | <span data-ttu-id="22710-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="22710-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="22710-151">**计算利息间隔**</span><span class="sxs-lookup"><span data-stu-id="22710-151">**Calculate interest every**</span></span>    | <span data-ttu-id="22710-152">3/月</span><span class="sxs-lookup"><span data-stu-id="22710-152">3/Month</span></span>         |
| <span data-ttu-id="22710-153">**按范围的利息**</span><span class="sxs-lookup"><span data-stu-id="22710-153">**Interest by range**</span></span>           | <span data-ttu-id="22710-154">金额</span><span class="sxs-lookup"><span data-stu-id="22710-154">Amount</span></span>          |
| <span data-ttu-id="22710-155">**利息计算依据**</span><span class="sxs-lookup"><span data-stu-id="22710-155">**Calculate interest based on**</span></span> | <span data-ttu-id="22710-156">百分比</span><span class="sxs-lookup"><span data-stu-id="22710-156">Percentage</span></span>      |

<span data-ttu-id="22710-157">您按如下所示设置了范围信息。</span><span class="sxs-lookup"><span data-stu-id="22710-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="22710-158">**源值**</span><span class="sxs-lookup"><span data-stu-id="22710-158">**From value**</span></span> | <span data-ttu-id="22710-159">**利息值**</span><span class="sxs-lookup"><span data-stu-id="22710-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="22710-160">0</span><span class="sxs-lookup"><span data-stu-id="22710-160">0</span></span>              | <span data-ttu-id="22710-161">1</span><span class="sxs-lookup"><span data-stu-id="22710-161">1</span></span>                  |
| <span data-ttu-id="22710-162">1,001</span><span class="sxs-lookup"><span data-stu-id="22710-162">1,001</span></span>          | <span data-ttu-id="22710-163">2</span><span class="sxs-lookup"><span data-stu-id="22710-163">2</span></span>                  |
| <span data-ttu-id="22710-164">5,001</span><span class="sxs-lookup"><span data-stu-id="22710-164">5,001</span></span>          | <span data-ttu-id="22710-165">3</span><span class="sxs-lookup"><span data-stu-id="22710-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="22710-166">示例 2：按大小的利息 = 天</span><span class="sxs-lookup"><span data-stu-id="22710-166">Example 2: Interest by range = Days</span></span>

<span data-ttu-id="22710-167">您设置发票付款超过交易到期日期每 15 天估计一次利息的利息代码。</span><span class="sxs-lookup"><span data-stu-id="22710-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="22710-168">要基于计算利息百分比值，根据步骤的金额间隔。</span><span class="sxs-lookup"><span data-stu-id="22710-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="22710-169">在过去 60 天以来，利息值将为 10.00 每 15 天，在每 15.00 天 61 到 90 和 20.00 个期间的 15 天，从第 91 天的 15 天前和之后。</span><span class="sxs-lookup"><span data-stu-id="22710-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="22710-170">您为利息代码设置了字段的值。</span><span class="sxs-lookup"><span data-stu-id="22710-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="22710-171">**字段名称**</span><span class="sxs-lookup"><span data-stu-id="22710-171">**Field name**</span></span>                  | <span data-ttu-id="22710-172">**字段值**</span><span class="sxs-lookup"><span data-stu-id="22710-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="22710-173">**利息代码**</span><span class="sxs-lookup"><span data-stu-id="22710-173">**Interest code**</span></span>               | <span data-ttu-id="22710-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="22710-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="22710-175">**计算利息间隔**</span><span class="sxs-lookup"><span data-stu-id="22710-175">**Calculate interest every**</span></span>    | <span data-ttu-id="22710-176">15/天</span><span class="sxs-lookup"><span data-stu-id="22710-176">15/Day</span></span>          |
| <span data-ttu-id="22710-177">**按范围的利息**</span><span class="sxs-lookup"><span data-stu-id="22710-177">**Interest by range**</span></span>           | <span data-ttu-id="22710-178">天</span><span class="sxs-lookup"><span data-stu-id="22710-178">Days</span></span>            |
| <span data-ttu-id="22710-179">**利息计算依据**</span><span class="sxs-lookup"><span data-stu-id="22710-179">**Calculate interest based on**</span></span> | <span data-ttu-id="22710-180">金额</span><span class="sxs-lookup"><span data-stu-id="22710-180">Amount</span></span>          |

<span data-ttu-id="22710-181">您按如下所示设置了范围信息。</span><span class="sxs-lookup"><span data-stu-id="22710-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="22710-182">**源值**</span><span class="sxs-lookup"><span data-stu-id="22710-182">**From value**</span></span> | <span data-ttu-id="22710-183">**利息值**</span><span class="sxs-lookup"><span data-stu-id="22710-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="22710-184">0</span><span class="sxs-lookup"><span data-stu-id="22710-184">0</span></span>              | <span data-ttu-id="22710-185">10</span><span class="sxs-lookup"><span data-stu-id="22710-185">10</span></span>                 |
| <span data-ttu-id="22710-186">61</span><span class="sxs-lookup"><span data-stu-id="22710-186">61</span></span>             | <span data-ttu-id="22710-187">15</span><span class="sxs-lookup"><span data-stu-id="22710-187">15</span></span>                 |
| <span data-ttu-id="22710-188">91</span><span class="sxs-lookup"><span data-stu-id="22710-188">91</span></span>             | <span data-ttu-id="22710-189">20</span><span class="sxs-lookup"><span data-stu-id="22710-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="22710-190">示例 3：按大小的利息 = 月</span><span class="sxs-lookup"><span data-stu-id="22710-190">Example 3: Interest by range = Months</span></span>

<span data-ttu-id="22710-191">您设置估计利息一次每三个月的利息代码发票付款超过交易到期日期。</span><span class="sxs-lookup"><span data-stu-id="22710-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="22710-192">要基于计算利息百分比值，根据步骤的金额间隔。</span><span class="sxs-lookup"><span data-stu-id="22710-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="22710-193">对于前三个月逾期，利息值将为每月 1.5%，对于第二个三个月逾期，为每月 2.0%，对于超出前六个月之外的每个月，为每月 2.5%。</span><span class="sxs-lookup"><span data-stu-id="22710-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="22710-194">您为利息代码设置了字段的值。</span><span class="sxs-lookup"><span data-stu-id="22710-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="22710-195">**字段名称**</span><span class="sxs-lookup"><span data-stu-id="22710-195">**Field name**</span></span>                  | <span data-ttu-id="22710-196">**字段值**</span><span class="sxs-lookup"><span data-stu-id="22710-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="22710-197">**利息代码**</span><span class="sxs-lookup"><span data-stu-id="22710-197">**Interest code**</span></span>               | <span data-ttu-id="22710-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="22710-198">1M%ByMth</span></span>        |
| <span data-ttu-id="22710-199">**计算利息间隔**</span><span class="sxs-lookup"><span data-stu-id="22710-199">**Calculate interest every**</span></span>    | <span data-ttu-id="22710-200">1/月</span><span class="sxs-lookup"><span data-stu-id="22710-200">1/Month</span></span>         |
| <span data-ttu-id="22710-201">**按范围的利息**</span><span class="sxs-lookup"><span data-stu-id="22710-201">**Interest by range**</span></span>           | <span data-ttu-id="22710-202">月份</span><span class="sxs-lookup"><span data-stu-id="22710-202">Months</span></span>          |
| <span data-ttu-id="22710-203">**利息计算依据**</span><span class="sxs-lookup"><span data-stu-id="22710-203">**Calculate interest based on**</span></span> | <span data-ttu-id="22710-204">百分比</span><span class="sxs-lookup"><span data-stu-id="22710-204">Percentage</span></span>      |

<span data-ttu-id="22710-205">您按如下所示设置了范围信息。</span><span class="sxs-lookup"><span data-stu-id="22710-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="22710-206">**源值**</span><span class="sxs-lookup"><span data-stu-id="22710-206">**From value**</span></span> | <span data-ttu-id="22710-207">**利息值**</span><span class="sxs-lookup"><span data-stu-id="22710-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="22710-208">0</span><span class="sxs-lookup"><span data-stu-id="22710-208">0</span></span>              | <span data-ttu-id="22710-209">1.5</span><span class="sxs-lookup"><span data-stu-id="22710-209">1.5</span></span>                |
| <span data-ttu-id="22710-210">4</span><span class="sxs-lookup"><span data-stu-id="22710-210">4</span></span>              | <span data-ttu-id="22710-211">2</span><span class="sxs-lookup"><span data-stu-id="22710-211">2</span></span>                  |
| <span data-ttu-id="22710-212">7</span><span class="sxs-lookup"><span data-stu-id="22710-212">7</span></span>              | <span data-ttu-id="22710-213">2.5</span><span class="sxs-lookup"><span data-stu-id="22710-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="22710-214">新版本</span><span class="sxs-lookup"><span data-stu-id="22710-214">New versions</span></span>
<span data-ttu-id="22710-215">利息代码是有生效日期的。</span><span class="sxs-lookup"><span data-stu-id="22710-215">Interest codes are date effective.</span></span> <span data-ttu-id="22710-216">如果您要修改利率，您可以创建截至将来日期生效的 **新版本**。</span><span class="sxs-lookup"><span data-stu-id="22710-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="22710-217">若要查看不同的版本，您可以使用 **开始日期** 菜单选项来选择截止日期。</span><span class="sxs-lookup"><span data-stu-id="22710-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="22710-218">您还可以选择 **显示所有记录** 来查看该页中的所有利息代码。</span><span class="sxs-lookup"><span data-stu-id="22710-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
