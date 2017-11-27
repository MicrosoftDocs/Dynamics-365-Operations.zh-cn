---
title: "125% 余额递减法"
description: "本文提供了 125% 余额递减法折旧方法的概览。"
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
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ec88d799c44e035b6490861383557f8c3beda41
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="02c66-103">125% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="02c66-103">125 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="02c66-104">本文提供了 125% 余额递减法折旧方法的概览。</span><span class="sxs-lookup"><span data-stu-id="02c66-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="02c66-105">如果您设置固定资产折旧模板并在**“折旧模板”**页面上的**“方法”**字段中选择**“125% 余额递减法”**，已分配此折旧模板的固定资产将在每个折旧期间按相同的百分比进行折旧。</span><span class="sxs-lookup"><span data-stu-id="02c66-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="02c66-106">此百分比按资产的使用年限进行计算。</span><span class="sxs-lookup"><span data-stu-id="02c66-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="02c66-107">例如，如果资产的使用年限为 5 年，则该百分比按 25% (125% ÷ 5) 计算。</span><span class="sxs-lookup"><span data-stu-id="02c66-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="02c66-108">要设置 125% 余额递减法，您还必须在**“折旧模板”**页面上的**“折旧年份”**字段和**“期间频率”**字段中选择选项。</span><span class="sxs-lookup"><span data-stu-id="02c66-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="02c66-109">**“期间频率”**字段中提供的选项因**“折旧年份”**字段中所选的值而异。</span><span class="sxs-lookup"><span data-stu-id="02c66-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="02c66-110">选择折旧年份</span><span class="sxs-lookup"><span data-stu-id="02c66-110">Select a depreciation year</span></span>
<span data-ttu-id="02c66-111">您可以在**“折旧模板”**页上的**“折旧年份”**字段中选择**“日历”**或**“会计”**。</span><span class="sxs-lookup"><span data-stu-id="02c66-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="02c66-112">默认值是**“日历”**。</span><span class="sxs-lookup"><span data-stu-id="02c66-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="02c66-113">您的选择将决定“**期间频率**”字段中可用的选项。</span><span class="sxs-lookup"><span data-stu-id="02c66-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="02c66-114">此字段定义整个日历年度的折旧应计过帐日期和金额。</span><span class="sxs-lookup"><span data-stu-id="02c66-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="02c66-115">日历</span><span class="sxs-lookup"><span data-stu-id="02c66-115">Calendar</span></span>

<span data-ttu-id="02c66-116">可以保留“**折旧年份**”字段中的默认值，即“**日历**”。</span><span class="sxs-lookup"><span data-stu-id="02c66-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="02c66-117">**“日历”**选项在每年的 1 月 1 日更新折旧基数。</span><span class="sxs-lookup"><span data-stu-id="02c66-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="02c66-118">通常，折旧基数为帐面净值减去残值所得的结果。</span><span class="sxs-lookup"><span data-stu-id="02c66-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="02c66-119">在此主题后面的示例中，折旧基数是计算列中第一个表达式的分子。</span><span class="sxs-lookup"><span data-stu-id="02c66-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="02c66-120">如果选择**“日历”**作为折旧年份，则**“期间频率”**字段中提供以下选项：</span><span class="sxs-lookup"><span data-stu-id="02c66-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="02c66-121">**“每年”**在 12 月 31 日过帐金额。</span><span class="sxs-lookup"><span data-stu-id="02c66-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="02c66-122">**“每月”**在每个日历月末过帐每月金额。</span><span class="sxs-lookup"><span data-stu-id="02c66-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="02c66-123">**“每季度”**在每个日历季度末（3 月 31 日、6 月 30 日、9 月 30 日和 12 月 31 日）过帐季度金额。</span><span class="sxs-lookup"><span data-stu-id="02c66-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="02c66-124">**“每半年”**在每个日历半年末（6 月 30 日和 12 月 31 日）过帐半年金额。</span><span class="sxs-lookup"><span data-stu-id="02c66-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="02c66-125">**“日常”**通过对每天使用一个交易记录来过帐每日折旧方法的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="02c66-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="02c66-126">会计</span><span class="sxs-lookup"><span data-stu-id="02c66-126">Fiscal</span></span>

<span data-ttu-id="02c66-127">如果在**“折旧年份”**字段中选择**“会计”**，则 125% 余额递减法将基于用于帐簿中指定的会计日历的会计年度或者在**“分类帐”**页面上选择的会计日历的会计年度进行计算。</span><span class="sxs-lookup"><span data-stu-id="02c66-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="02c66-128">会计年度是在**“会计日历”**页上设置的。</span><span class="sxs-lookup"><span data-stu-id="02c66-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="02c66-129">例如，对于会计年度 7 月 1 日至次年 6 月 30 日，折旧计算从 7 月 1 日开始。</span><span class="sxs-lookup"><span data-stu-id="02c66-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="02c66-130">会计年度可以长于或短于 12 个月。</span><span class="sxs-lookup"><span data-stu-id="02c66-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="02c66-131">对于每个期间，折旧都可以自动调整，下一个会计年度的长度取决于**“财务日历”**页面上的期间的设置。</span><span class="sxs-lookup"><span data-stu-id="02c66-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="02c66-132">如果选择**“会计”**作为折旧年份，则**“期间频率”**字段中提供以下选项：</span><span class="sxs-lookup"><span data-stu-id="02c66-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="02c66-133">**“每年”**为会计年度计算的折旧总额作为一笔金额在该会计年度的最后一天进行过帐。</span><span class="sxs-lookup"><span data-stu-id="02c66-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="02c66-134">**“会计期间”**将过帐为该会计年度计算的折旧总额。</span><span class="sxs-lookup"><span data-stu-id="02c66-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="02c66-135">此金额计入在**“会计日历”**页上定义的会计期间。</span><span class="sxs-lookup"><span data-stu-id="02c66-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="02c66-136">125% 余额递减法折旧示例</span><span class="sxs-lookup"><span data-stu-id="02c66-136">Example of 125% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="02c66-137">购置成本</span><span class="sxs-lookup"><span data-stu-id="02c66-137">Acquisition cost</span></span>               | <span data-ttu-id="02c66-138">11,000</span><span class="sxs-lookup"><span data-stu-id="02c66-138">11,000</span></span> |
| <span data-ttu-id="02c66-139">Salvage value / 残值</span><span class="sxs-lookup"><span data-stu-id="02c66-139">Salvage value</span></span>                  | <span data-ttu-id="02c66-140">1,000</span><span class="sxs-lookup"><span data-stu-id="02c66-140">1,000</span></span>  |
| <span data-ttu-id="02c66-141">折旧基数</span><span class="sxs-lookup"><span data-stu-id="02c66-141">Depreciation base</span></span>              | <span data-ttu-id="02c66-142">10,000</span><span class="sxs-lookup"><span data-stu-id="02c66-142">10,000</span></span> |
| <span data-ttu-id="02c66-143">服务年限</span><span class="sxs-lookup"><span data-stu-id="02c66-143">Service life years</span></span>             | <span data-ttu-id="02c66-144">5</span><span class="sxs-lookup"><span data-stu-id="02c66-144">5</span></span>      |
| <span data-ttu-id="02c66-145">每年折旧百分比</span><span class="sxs-lookup"><span data-stu-id="02c66-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="02c66-146">25%</span><span class="sxs-lookup"><span data-stu-id="02c66-146">25%</span></span>    |

<span data-ttu-id="02c66-147">125% 余额递减法将 125% 除以使用年限。</span><span class="sxs-lookup"><span data-stu-id="02c66-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="02c66-148">用此百分比乘以资产的帐面净值来确定年折旧金额。</span><span class="sxs-lookup"><span data-stu-id="02c66-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="02c66-149">期间</span><span class="sxs-lookup"><span data-stu-id="02c66-149">Period</span></span> | <span data-ttu-id="02c66-150">年折旧金额的计算</span><span class="sxs-lookup"><span data-stu-id="02c66-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="02c66-151">帐面值</span><span class="sxs-lookup"><span data-stu-id="02c66-151">Book value</span></span>                    | <span data-ttu-id="02c66-152">年末帐面净值</span><span class="sxs-lookup"><span data-stu-id="02c66-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="02c66-153">第 1 年</span><span class="sxs-lookup"><span data-stu-id="02c66-153">Year 1</span></span> | <span data-ttu-id="02c66-154">(11,000 – 1,000) × 25% = 2,500</span><span class="sxs-lookup"><span data-stu-id="02c66-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="02c66-155">(11,000 – 2,500) = 8,500</span><span class="sxs-lookup"><span data-stu-id="02c66-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="02c66-156">(11,000 – 1,000 – 2,500) = 7,500</span><span class="sxs-lookup"><span data-stu-id="02c66-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="02c66-157">第 2 年</span><span class="sxs-lookup"><span data-stu-id="02c66-157">Year 2</span></span> | <span data-ttu-id="02c66-158">7,500 × 25% = 1,875</span><span class="sxs-lookup"><span data-stu-id="02c66-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="02c66-159">(8,500 – 1,875) = 6,625</span><span class="sxs-lookup"><span data-stu-id="02c66-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="02c66-160">(7,500 – 1,875) = 5,625</span><span class="sxs-lookup"><span data-stu-id="02c66-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="02c66-161">第 3 年</span><span class="sxs-lookup"><span data-stu-id="02c66-161">Year 3</span></span> | <span data-ttu-id="02c66-162">5,625 × 25% = 1,406.25</span><span class="sxs-lookup"><span data-stu-id="02c66-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="02c66-163">(6,625 – 1,406.25) = 5,218.75</span><span class="sxs-lookup"><span data-stu-id="02c66-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="02c66-164">(5,625 – 1,406.25) = 4,218.75</span><span class="sxs-lookup"><span data-stu-id="02c66-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="02c66-165">通常，当使用 125% 余额递减折旧法计算的金额小于使用直线法计算的金额时，对剩余年限转换到直线法。</span><span class="sxs-lookup"><span data-stu-id="02c66-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




