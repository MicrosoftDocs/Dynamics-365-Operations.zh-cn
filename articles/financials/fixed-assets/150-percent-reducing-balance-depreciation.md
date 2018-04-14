---
title: "150% 余额递减法"
description: "本文提供了 150% 余额递减法折旧方法的概览。"
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 931c12278853d87e6fddbb166b56c6079d40b142
ms.contentlocale: zh-cn
ms.lasthandoff: 04/13/2018

---

# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="25c31-103">150% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="25c31-103">150 percent reducing balance depreciation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="25c31-104">本文提供了 150% 余额递减法折旧方法的概览。</span><span class="sxs-lookup"><span data-stu-id="25c31-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="25c31-105">如果您设置固定资产折旧模板并在**“折旧模板”**页面上的**“方法”**字段中选择**“150% 余额递减法”**，已分配此折旧模板的固定资产将在每个折旧期间按相同的百分比进行折旧。</span><span class="sxs-lookup"><span data-stu-id="25c31-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="25c31-106">此百分比按资产的使用年限进行计算。</span><span class="sxs-lookup"><span data-stu-id="25c31-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="25c31-107">例如，如果资产的使用年限为 5 年，则该百分比按 30% (150% ÷ 5) 计算。</span><span class="sxs-lookup"><span data-stu-id="25c31-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="25c31-108">要设置 150% 余额递减法，您还必须在**“折旧模板”**页面上的**“折旧年份”**字段和**“期间频率”**字段中选择选项。</span><span class="sxs-lookup"><span data-stu-id="25c31-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="25c31-109">**“期间频率”**字段中提供的选项因**“折旧年份”**字段中所选的值而异。</span><span class="sxs-lookup"><span data-stu-id="25c31-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="25c31-110">折旧年份的选择</span><span class="sxs-lookup"><span data-stu-id="25c31-110">Selection of depreciation year</span></span>
<span data-ttu-id="25c31-111">您可以在**“折旧模板”**页上的**“折旧年份”**字段中选择**“日历”**或**“会计”**。</span><span class="sxs-lookup"><span data-stu-id="25c31-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="25c31-112">默认值是**“日历”**。</span><span class="sxs-lookup"><span data-stu-id="25c31-112">The default value is **Calendar**.</span></span> <span data-ttu-id="25c31-113">您的选择将决定“**期间频率**”字段中可用的选项。</span><span class="sxs-lookup"><span data-stu-id="25c31-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="25c31-114">此字段定义整个日历年度的折旧应计过帐日期和金额。</span><span class="sxs-lookup"><span data-stu-id="25c31-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="25c31-115">日历</span><span class="sxs-lookup"><span data-stu-id="25c31-115">Calendar</span></span>

<span data-ttu-id="25c31-116">可以保留“**折旧年份**”字段中的默认值，即“**日历**”。</span><span class="sxs-lookup"><span data-stu-id="25c31-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="25c31-117">**“日历”**选项在每年的 1 月 1 日更新折旧基数。</span><span class="sxs-lookup"><span data-stu-id="25c31-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="25c31-118">通常，折旧基数为帐面净值减去残值所得的结果。</span><span class="sxs-lookup"><span data-stu-id="25c31-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="25c31-119">在此主题后面的示例中，折旧基数是计算列中第一个表达式的分子。</span><span class="sxs-lookup"><span data-stu-id="25c31-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="25c31-120">如果选择**“日历”**作为折旧年份，则**“期间频率”**字段中提供以下选项：</span><span class="sxs-lookup"><span data-stu-id="25c31-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="25c31-121">**“每年”**在 12 月 31 日过帐金额。</span><span class="sxs-lookup"><span data-stu-id="25c31-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="25c31-122">**“每月”**在每个日历月末过帐每月金额。</span><span class="sxs-lookup"><span data-stu-id="25c31-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="25c31-123">**“每季度”**在每个日历季度末（3 月 31 日、6 月 30 日、9 月 30 日和 12 月 31 日）过帐季度金额。</span><span class="sxs-lookup"><span data-stu-id="25c31-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="25c31-124">**“每半年”**在每个日历半年末（6 月 30 日和 12 月 31 日）过帐半年金额。</span><span class="sxs-lookup"><span data-stu-id="25c31-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="25c31-125">**“日常”**通过对每天使用一个交易记录来过帐每日折旧方法的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="25c31-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="25c31-126">会计</span><span class="sxs-lookup"><span data-stu-id="25c31-126">Fiscal</span></span>

<span data-ttu-id="25c31-127">如果在**“折旧年份”**字段中选择**“会计”**，则 150% 余额递减法将基于用于帐簿中指定的会计日历的会计年度或者在**“分类帐”**页面上选择的会计日历的会计年度进行计算。</span><span class="sxs-lookup"><span data-stu-id="25c31-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="25c31-128">会计年度是在**“会计日历”**页上设置的。</span><span class="sxs-lookup"><span data-stu-id="25c31-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="25c31-129">例如，对于会计年度 7 月 1 日至次年 6 月 30 日，折旧计算从 7 月 1 日开始。</span><span class="sxs-lookup"><span data-stu-id="25c31-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="25c31-130">会计年度可以长于或短于 12 个月。</span><span class="sxs-lookup"><span data-stu-id="25c31-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="25c31-131">对于每个期间，都可以调整折旧。</span><span class="sxs-lookup"><span data-stu-id="25c31-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="25c31-132">下一会计年度的长度由**“会计日历”**页面上的期间设置决定。</span><span class="sxs-lookup"><span data-stu-id="25c31-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="25c31-133">如果选择**“会计”**作为折旧年份，则**“期间频率”**字段中提供以下选项：</span><span class="sxs-lookup"><span data-stu-id="25c31-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="25c31-134">**“每年”**在会计年度的最后一天过帐针对会计年度计算的折旧总额。</span><span class="sxs-lookup"><span data-stu-id="25c31-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="25c31-135">**“会计期间”**将过帐为该会计年度计算的折旧总额。</span><span class="sxs-lookup"><span data-stu-id="25c31-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="25c31-136">此金额计入在**“会计日历”**页上定义的会计期间。</span><span class="sxs-lookup"><span data-stu-id="25c31-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="25c31-137">150% 余额递减法的示例</span><span class="sxs-lookup"><span data-stu-id="25c31-137">Example of 150% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="25c31-138">购置成本</span><span class="sxs-lookup"><span data-stu-id="25c31-138">Acquisition cost</span></span>               | <span data-ttu-id="25c31-139">11,000</span><span class="sxs-lookup"><span data-stu-id="25c31-139">11,000</span></span> |
| <span data-ttu-id="25c31-140">Salvage value / 残值</span><span class="sxs-lookup"><span data-stu-id="25c31-140">Salvage value</span></span>                  | <span data-ttu-id="25c31-141">1,000</span><span class="sxs-lookup"><span data-stu-id="25c31-141">1,000</span></span>  |
| <span data-ttu-id="25c31-142">折旧基数</span><span class="sxs-lookup"><span data-stu-id="25c31-142">Depreciation base</span></span>              | <span data-ttu-id="25c31-143">10,000</span><span class="sxs-lookup"><span data-stu-id="25c31-143">10,000</span></span> |
| <span data-ttu-id="25c31-144">服务年限</span><span class="sxs-lookup"><span data-stu-id="25c31-144">Service life years</span></span>             | <span data-ttu-id="25c31-145">5</span><span class="sxs-lookup"><span data-stu-id="25c31-145">5</span></span>      |
| <span data-ttu-id="25c31-146">每年折旧百分比</span><span class="sxs-lookup"><span data-stu-id="25c31-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="25c31-147">30%</span><span class="sxs-lookup"><span data-stu-id="25c31-147">30%</span></span>    |

<span data-ttu-id="25c31-148">150% 余额递减法将 150% 除以使用年限。</span><span class="sxs-lookup"><span data-stu-id="25c31-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="25c31-149">用此百分比乘以资产的帐面净值来确定年折旧金额。</span><span class="sxs-lookup"><span data-stu-id="25c31-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="25c31-150">期间</span><span class="sxs-lookup"><span data-stu-id="25c31-150">Period</span></span> | <span data-ttu-id="25c31-151">年折旧金额的计算</span><span class="sxs-lookup"><span data-stu-id="25c31-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="25c31-152">帐面值</span><span class="sxs-lookup"><span data-stu-id="25c31-152">Book value</span></span>             | <span data-ttu-id="25c31-153">年末帐面净值</span><span class="sxs-lookup"><span data-stu-id="25c31-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="25c31-154">第 1 年</span><span class="sxs-lookup"><span data-stu-id="25c31-154">Year 1</span></span> | <span data-ttu-id="25c31-155">(11,000 – 1,000) × 30% = 3,000</span><span class="sxs-lookup"><span data-stu-id="25c31-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="25c31-156">11,000 – 3,000 = 8,000</span><span class="sxs-lookup"><span data-stu-id="25c31-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="25c31-157">11,000 – 1,000 – 3,000 = 7,000</span><span class="sxs-lookup"><span data-stu-id="25c31-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="25c31-158">第 2 年</span><span class="sxs-lookup"><span data-stu-id="25c31-158">Year 2</span></span> | <span data-ttu-id="25c31-159">7,000 × 30% = 2,100</span><span class="sxs-lookup"><span data-stu-id="25c31-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="25c31-160">8,000 – 2,100 = 5,900</span><span class="sxs-lookup"><span data-stu-id="25c31-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="25c31-161">7,000 – 2,100 = 4,900</span><span class="sxs-lookup"><span data-stu-id="25c31-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="25c31-162">第 3 年</span><span class="sxs-lookup"><span data-stu-id="25c31-162">Year 3</span></span> | <span data-ttu-id="25c31-163">4,900 × 30% = 1,470</span><span class="sxs-lookup"><span data-stu-id="25c31-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="25c31-164">5,900 – 1,470 = 4,430</span><span class="sxs-lookup"><span data-stu-id="25c31-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="25c31-165">4,900 – 1,470 = 3,430</span><span class="sxs-lookup"><span data-stu-id="25c31-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="25c31-166">通常，当使用 150% 余额递减折旧法计算的金额小于使用直线法计算的金额时，对剩余年限转换到直线法。</span><span class="sxs-lookup"><span data-stu-id="25c31-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




