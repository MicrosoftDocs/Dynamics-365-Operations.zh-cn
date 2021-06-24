---
title: 直线法折旧
description: 本文提供了直线法折旧法的概览。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 610e8c58975a02cf6a4b3c4f79639d94ae8c3d9b
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193822"
---
# <a name="straight-line-service-life-depreciation"></a><span data-ttu-id="b511d-103">直线法折旧</span><span class="sxs-lookup"><span data-stu-id="b511d-103">Straight line service life depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b511d-104">本文提供了直线法折旧法的概览。</span><span class="sxs-lookup"><span data-stu-id="b511d-104">This article gives an overview of the Straight line service life method of depreciation.</span></span>

<span data-ttu-id="b511d-105">在设置固定资产折旧模板并在“折旧模板”页的“方法”字段中选择“直线法”时，分配了该折旧模板的资产将基于资产的总使用年限而折旧。</span><span class="sxs-lookup"><span data-stu-id="b511d-105">When you set up a fixed asset depreciation profile and select Straight line service life in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated based on the total service life of the asset.</span></span> <span data-ttu-id="b511d-106">通常，每个折旧期间的折旧金额相同。</span><span class="sxs-lookup"><span data-stu-id="b511d-106">This generally is the same depreciation amount in each depreciation period.</span></span> 

<span data-ttu-id="b511d-107">直线法（剩余年限）和直线法之间计算的折旧金额的区别在于何时将调整金额过帐给资产。</span><span class="sxs-lookup"><span data-stu-id="b511d-107">The difference in the depreciation amount that is calculated between straight line service life remaining and straight line service life is when there is an adjustment posted to the asset.</span></span> 

<span data-ttu-id="b511d-108">若要设置直线法折旧，您还必须在“折旧模板”页面上的“折旧年份”字段和“期间频率”字段中选择选项。</span><span class="sxs-lookup"><span data-stu-id="b511d-108">To set up straight line service life depreciation, you must also select options in the Depreciation year and Period frequency fields in the Depreciation profiles page.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="b511d-109">选择折旧年份</span><span class="sxs-lookup"><span data-stu-id="b511d-109">Select a depreciation year</span></span>
<span data-ttu-id="b511d-110">您可以在“折旧模板”页上的“折旧年份”字段中选择“日历”或“会计”。</span><span class="sxs-lookup"><span data-stu-id="b511d-110">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="b511d-111">此选择将定义“期间频率”字段中可用的选项。</span><span class="sxs-lookup"><span data-stu-id="b511d-111">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="b511d-112">默认选项为“日历”。</span><span class="sxs-lookup"><span data-stu-id="b511d-112">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="b511d-113">日历</span><span class="sxs-lookup"><span data-stu-id="b511d-113">Calendar</span></span>

<span data-ttu-id="b511d-114">如果您选择“日历”，则假定为一年 1 月 1 日到 12 月 31 日，即使您以不同方式定义会计日历。</span><span class="sxs-lookup"><span data-stu-id="b511d-114">If you select Calendar, a year of January 1 to December 31 is assumed, even if you have defined the fiscal calendar differently.</span></span> 

<span data-ttu-id="b511d-115">使用“日历”选项，可以在每年 1 月 1 日更新折旧基数（通常为帐面净值减去残值）。</span><span class="sxs-lookup"><span data-stu-id="b511d-115">The Calendar option updates the depreciation base, which is typically the net book value minus the salvage value, on January 1 of each year.</span></span> <span data-ttu-id="b511d-116">在此主题后面的示例中，折旧基数是计算列中第一个表达式的分子。</span><span class="sxs-lookup"><span data-stu-id="b511d-116">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="b511d-117">如果选择“日历”，则在“期间频率”字段中提供以下选项，这些选项定义了整个日历年度的折旧应计过帐日期和金额：</span><span class="sxs-lookup"><span data-stu-id="b511d-117">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>
-   <span data-ttu-id="b511d-118">“每年”在 12 月 31 日过帐金额。</span><span class="sxs-lookup"><span data-stu-id="b511d-118">Yearly posts an amount on December 31.</span></span>
-   <span data-ttu-id="b511d-119">“每月”在每个日历月末过帐每月金额。</span><span class="sxs-lookup"><span data-stu-id="b511d-119">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="b511d-120">“每季度”在每个日历季度末（3 月 31 日、6 月 30 日、9 月 30 日和 12 月 31 日）过帐季度金额。</span><span class="sxs-lookup"><span data-stu-id="b511d-120">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="b511d-121">“每半年”在每个日历半年末（6 月 30 日和 12 月 31 日）过帐半年金额。</span><span class="sxs-lookup"><span data-stu-id="b511d-121">Half-Yearly posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="b511d-122">“每日”通过对每天使用一个交易记录来过帐每日折旧方法的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="b511d-122">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="b511d-123">例如，如果您选择每年，年折旧只过帐一次，在每年的 12 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="b511d-123">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="b511d-124">如果您选择“每月”，月折旧每月按年折旧金额的 1/12 过帐。</span><span class="sxs-lookup"><span data-stu-id="b511d-124">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="b511d-125">会计</span><span class="sxs-lookup"><span data-stu-id="b511d-125">Fiscal</span></span>

<span data-ttu-id="b511d-126">如果在折旧年份字段中选择会计，则使用直线法折旧。</span><span class="sxs-lookup"><span data-stu-id="b511d-126">If you select Fiscal in the Depreciation year field, the straight line service life depreciation is used.</span></span> <span data-ttu-id="b511d-127">该计算基于会计年度，由为帐簿指定的会计日历定义，或者由在“分类帐”页中选择的会计日历定义。</span><span class="sxs-lookup"><span data-stu-id="b511d-127">It is calculated based on the fiscal year, which is defined by the fiscal calendar that is specified for the book, or by the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="b511d-128">会计年度是在“会计日历”页中设置的。</span><span class="sxs-lookup"><span data-stu-id="b511d-128">Fiscal calendars are set up in the Fiscal calendars page.</span></span>

<span data-ttu-id="b511d-129">例如，对于会计年度 7 月 1 日至次年 6 月 30 日，折旧计算从 7 月 1 日开始。</span><span class="sxs-lookup"><span data-stu-id="b511d-129">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="b511d-130">会计年度可以长于或短于 12 个月。</span><span class="sxs-lookup"><span data-stu-id="b511d-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="b511d-131">对于每个会计期间，自动调整折旧。</span><span class="sxs-lookup"><span data-stu-id="b511d-131">The depreciation automatically is adjusted for each fiscal period.</span></span> <span data-ttu-id="b511d-132">下一会计年度的长度基于您在“会计日历”窗体中创建新的会计年度时设置的会计期间。</span><span class="sxs-lookup"><span data-stu-id="b511d-132">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars form.</span></span> 

<span data-ttu-id="b511d-133">如果在“期间频率”字段中选择“会计”，以下期间频率选项可用：</span><span class="sxs-lookup"><span data-stu-id="b511d-133">If you select Fiscal, the following options are available in the Period frequency field:</span></span>
-   <span data-ttu-id="b511d-134">“每年”为会计年度计算的折旧总额作为一笔金额在该会计年度的最后一天进行过帐。</span><span class="sxs-lookup"><span data-stu-id="b511d-134">Yearly posts the total amount of the depreciation that is calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="b511d-135">会计期间为会计年度计算的折旧总额应计入在会计日历的“会计日历”窗体中定义的会计期间。</span><span class="sxs-lookup"><span data-stu-id="b511d-135">Fiscal period calculates the total amount of the depreciation for the fiscal year, which is accrued into the periods that are defined in the Fiscal calendars form for the fiscal calendar.</span></span>

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="b511d-136">示例：对未更改的固定资产进行直线法折旧</span><span class="sxs-lookup"><span data-stu-id="b511d-136">Example: Straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="b511d-137">假定固定资产具有以下特征。</span><span class="sxs-lookup"><span data-stu-id="b511d-137">Suppose that a fixed asset has the following characteristics.</span></span>

| <span data-ttu-id="b511d-138">特性</span><span class="sxs-lookup"><span data-stu-id="b511d-138">Characteristic</span></span>      | <span data-ttu-id="b511d-139">值</span><span class="sxs-lookup"><span data-stu-id="b511d-139">Value</span></span>  |
|---------------------|--------|
| <span data-ttu-id="b511d-140">购置成本</span><span class="sxs-lookup"><span data-stu-id="b511d-140">Acquisition cost</span></span>    | <span data-ttu-id="b511d-141">11,000</span><span class="sxs-lookup"><span data-stu-id="b511d-141">11,000</span></span> |
| <span data-ttu-id="b511d-142">Salvage value / 残值</span><span class="sxs-lookup"><span data-stu-id="b511d-142">Salvage value</span></span>       | <span data-ttu-id="b511d-143">1,000</span><span class="sxs-lookup"><span data-stu-id="b511d-143">1,000</span></span>  |
| <span data-ttu-id="b511d-144">折旧基数</span><span class="sxs-lookup"><span data-stu-id="b511d-144">Depreciation base</span></span>   | <span data-ttu-id="b511d-145">10,000</span><span class="sxs-lookup"><span data-stu-id="b511d-145">10,000</span></span> |
| <span data-ttu-id="b511d-146">服务年限</span><span class="sxs-lookup"><span data-stu-id="b511d-146">Service life years</span></span>  | <span data-ttu-id="b511d-147">5</span><span class="sxs-lookup"><span data-stu-id="b511d-147">5</span></span>      |
| <span data-ttu-id="b511d-148">每年折旧</span><span class="sxs-lookup"><span data-stu-id="b511d-148">Yearly depreciation</span></span> | <span data-ttu-id="b511d-149">2,000</span><span class="sxs-lookup"><span data-stu-id="b511d-149">2,000</span></span>  |

<span data-ttu-id="b511d-150">每年的折旧金额相同。</span><span class="sxs-lookup"><span data-stu-id="b511d-150">You get the same depreciation amount each year.</span></span> <span data-ttu-id="b511d-151">(购置成本 - 残值)/使用年限</span><span class="sxs-lookup"><span data-stu-id="b511d-151">(Acquisition cost - Salvage value) / Service life years</span></span>

| <span data-ttu-id="b511d-152">期间</span><span class="sxs-lookup"><span data-stu-id="b511d-152">Period</span></span> | <span data-ttu-id="b511d-153">年折旧金额的计算</span><span class="sxs-lookup"><span data-stu-id="b511d-153">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="b511d-154">年末帐面净值</span><span class="sxs-lookup"><span data-stu-id="b511d-154">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="b511d-155">第 1 年</span><span class="sxs-lookup"><span data-stu-id="b511d-155">Year 1</span></span> | <span data-ttu-id="b511d-156">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="b511d-156">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="b511d-157">9,000</span><span class="sxs-lookup"><span data-stu-id="b511d-157">9,000</span></span>                                 |
| <span data-ttu-id="b511d-158">第 2 年</span><span class="sxs-lookup"><span data-stu-id="b511d-158">Year 2</span></span> | <span data-ttu-id="b511d-159">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="b511d-159">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="b511d-160">7,000</span><span class="sxs-lookup"><span data-stu-id="b511d-160">7,000</span></span>                                 |
| <span data-ttu-id="b511d-161">第 3 年</span><span class="sxs-lookup"><span data-stu-id="b511d-161">Year 3</span></span> | <span data-ttu-id="b511d-162">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="b511d-162">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="b511d-163">5,000</span><span class="sxs-lookup"><span data-stu-id="b511d-163">5,000</span></span>                                 |
| <span data-ttu-id="b511d-164">第 4 年</span><span class="sxs-lookup"><span data-stu-id="b511d-164">Year 4</span></span> | <span data-ttu-id="b511d-165">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="b511d-165">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="b511d-166">3,000</span><span class="sxs-lookup"><span data-stu-id="b511d-166">3,000</span></span>                                 |
| <span data-ttu-id="b511d-167">第 5 年</span><span class="sxs-lookup"><span data-stu-id="b511d-167">Year 5</span></span> | <span data-ttu-id="b511d-168">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="b511d-168">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="b511d-169">1,000</span><span class="sxs-lookup"><span data-stu-id="b511d-169">1,000</span></span>                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a><span data-ttu-id="b511d-170">示例：已更改的固定资产的直线法折旧</span><span class="sxs-lookup"><span data-stu-id="b511d-170">Example: Straight line depreciation of a modified fixed asset</span></span>

<span data-ttu-id="b511d-171">假定在第 2 年向相同的固定资产增加了 4,000 的购置调整。</span><span class="sxs-lookup"><span data-stu-id="b511d-171">Suppose that you add an acquisition adjustment of 4,000 in year 2 to the same fixed asset.</span></span> 

<span data-ttu-id="b511d-172">购置调整的使用年限与固定资产相同，并从购置时开始计算。</span><span class="sxs-lookup"><span data-stu-id="b511d-172">The service life of the acquisition adjustment is the same as that of the fixed asset and starts at the time of its acquisition.</span></span> <span data-ttu-id="b511d-173">对应于购置价格调整的帐面净值，在第五年末将保留帐面净值。</span><span class="sxs-lookup"><span data-stu-id="b511d-173">A net book value remains at the end of year 5, corresponding to the net book value of the acquisition adjustment.</span></span> <span data-ttu-id="b511d-174">按期间计算的折旧如下表所示：</span><span class="sxs-lookup"><span data-stu-id="b511d-174">The depreciation by period is calculated as shown in the following table.</span></span>

| <span data-ttu-id="b511d-175">期间</span><span class="sxs-lookup"><span data-stu-id="b511d-175">Period</span></span> | <span data-ttu-id="b511d-176">年折旧金额的计算</span><span class="sxs-lookup"><span data-stu-id="b511d-176">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="b511d-177">年末帐面净值</span><span class="sxs-lookup"><span data-stu-id="b511d-177">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="b511d-178">第 1 年</span><span class="sxs-lookup"><span data-stu-id="b511d-178">Year 1</span></span> | <span data-ttu-id="b511d-179">10,000 / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="b511d-179">10,000 / 5 = 2,000</span></span>                        | <span data-ttu-id="b511d-180">11,000 - 2,000 = 9,000</span><span class="sxs-lookup"><span data-stu-id="b511d-180">11,000 - 2,000 = 9,000</span></span>                |
| <span data-ttu-id="b511d-181">第 2 年</span><span class="sxs-lookup"><span data-stu-id="b511d-181">Year 2</span></span> | <span data-ttu-id="b511d-182">4,000 （购置调整）</span><span class="sxs-lookup"><span data-stu-id="b511d-182">4,000 (acquisition adjustment)</span></span>            | <span data-ttu-id="b511d-183">9,000 + 4,000 =13,000</span><span class="sxs-lookup"><span data-stu-id="b511d-183">9,000 + 4,000 =13,000</span></span>                 |
| <span data-ttu-id="b511d-184">第 2 年</span><span class="sxs-lookup"><span data-stu-id="b511d-184">Year 2</span></span> | <span data-ttu-id="b511d-185">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="b511d-185">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="b511d-186">13,000 - 2,800 = 10,200</span><span class="sxs-lookup"><span data-stu-id="b511d-186">13,000 - 2,800 = 10,200</span></span>               |
| <span data-ttu-id="b511d-187">第 3 年</span><span class="sxs-lookup"><span data-stu-id="b511d-187">Year 3</span></span> | <span data-ttu-id="b511d-188">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="b511d-188">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="b511d-189">10,200 - 2,800 = 7,400</span><span class="sxs-lookup"><span data-stu-id="b511d-189">10,200 - 2,800 = 7,400</span></span>                |
| <span data-ttu-id="b511d-190">第 4 年</span><span class="sxs-lookup"><span data-stu-id="b511d-190">Year 4</span></span> | <span data-ttu-id="b511d-191">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="b511d-191">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="b511d-192">7,400 - 2,800 = 4,600</span><span class="sxs-lookup"><span data-stu-id="b511d-192">7,400 - 2,800 = 4,600</span></span>                 |
| <span data-ttu-id="b511d-193">第 5 年</span><span class="sxs-lookup"><span data-stu-id="b511d-193">Year 5</span></span> | <span data-ttu-id="b511d-194">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="b511d-194">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="b511d-195">4,600 - 2,800 = 1,800</span><span class="sxs-lookup"><span data-stu-id="b511d-195">4,600 - 2,800 = 1,800</span></span>                 |
| <span data-ttu-id="b511d-196">第 6 年</span><span class="sxs-lookup"><span data-stu-id="b511d-196">Year 6</span></span> | <span data-ttu-id="b511d-197">余额 800\*</span><span class="sxs-lookup"><span data-stu-id="b511d-197">Remaining 800\*</span></span>                           | <span data-ttu-id="b511d-198">1,800 – 800 = 1,000</span><span class="sxs-lookup"><span data-stu-id="b511d-198">1,800 – 800 = 1,000</span></span>                   |

<span data-ttu-id="b511d-199">\*由于余额小于折旧金额，因此只取扣除残值后的余额。</span><span class="sxs-lookup"><span data-stu-id="b511d-199">\*Because the remaining amount is less than the depreciation amount, only the remaining amount minus the salvage value is taken.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]