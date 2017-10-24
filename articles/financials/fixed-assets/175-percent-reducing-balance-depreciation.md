---
title: "175% 余额递减法"
description: "本文提供了 175% 余额递减法折旧方法的概览。"
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 318e111f784157666c2853bcd6d5b3af2c9ffdc5
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="d833c-103">175% 余额递减法</span><span class="sxs-lookup"><span data-stu-id="d833c-103">175 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d833c-104">本文提供了 175% 余额递减法折旧方法的概览。</span><span class="sxs-lookup"><span data-stu-id="d833c-104">This article gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="d833c-105">如果您设置固定资产折旧模板并在**“折旧模板”**页面上的**“方法”**字段中选择**“175% 余额递减法”**，已分配此折旧模板的固定资产将在每个折旧期间按相同的百分比进行折旧。</span><span class="sxs-lookup"><span data-stu-id="d833c-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="d833c-106">要设置 175% 余额递减法，您还必须在**“折旧模板”**页面上的**“折旧年份”**字段和**“期间频率”**字段中选择选项。</span><span class="sxs-lookup"><span data-stu-id="d833c-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="d833c-107">**“期间频率”**字段中提供的选项因**“折旧年份”**字段中所选的值而异。</span><span class="sxs-lookup"><span data-stu-id="d833c-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="d833c-108">选择折旧年份</span><span class="sxs-lookup"><span data-stu-id="d833c-108">Select a depreciation year</span></span>
<span data-ttu-id="d833c-109">您可以在**“折旧模板”**页上的**“折旧年份”**字段中选择**“日历”**或**“会计”**。</span><span class="sxs-lookup"><span data-stu-id="d833c-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="d833c-110">默认值是**“日历”**。</span><span class="sxs-lookup"><span data-stu-id="d833c-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="d833c-111">您的选择将决定“**期间频率**”字段中可用的选项。</span><span class="sxs-lookup"><span data-stu-id="d833c-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="d833c-112">此字段定义整个日历年度的折旧应计过帐日期和金额。</span><span class="sxs-lookup"><span data-stu-id="d833c-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="d833c-113">日历</span><span class="sxs-lookup"><span data-stu-id="d833c-113">Calendar</span></span>

<span data-ttu-id="d833c-114">可以保留“**折旧年份**”字段中的默认值，即“**日历**”。</span><span class="sxs-lookup"><span data-stu-id="d833c-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="d833c-115">**“日历”**选项在每年的 1 月 1 日更新折旧基数。</span><span class="sxs-lookup"><span data-stu-id="d833c-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="d833c-116">通常，折旧基数为帐面净值减去残值所得的结果。</span><span class="sxs-lookup"><span data-stu-id="d833c-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="d833c-117">在此主题后面的示例中，折旧基数是计算列中第一个表达式的分子。</span><span class="sxs-lookup"><span data-stu-id="d833c-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="d833c-118">如果选择**“日历”**作为折旧年份，则**“期间频率”**字段中提供以下选项：</span><span class="sxs-lookup"><span data-stu-id="d833c-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="d833c-119">**“每年”**在 12 月 31 日过帐金额。</span><span class="sxs-lookup"><span data-stu-id="d833c-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="d833c-120">**“每月”**在每个日历月末过帐每月金额。</span><span class="sxs-lookup"><span data-stu-id="d833c-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="d833c-121">**“每季度”**在每个日历季度末（3 月 31 日、6 月 30 日、9 月 30 日和 12 月 31 日）过帐季度金额。</span><span class="sxs-lookup"><span data-stu-id="d833c-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="d833c-122">**“每半年”**在每个日历半年末（6 月 30 日和 12 月 31 日）过帐半年金额。</span><span class="sxs-lookup"><span data-stu-id="d833c-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="d833c-123">**“日常”**通过对每天使用一个交易记录来过帐每日折旧方法的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="d833c-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="d833c-124">会计</span><span class="sxs-lookup"><span data-stu-id="d833c-124">Fiscal</span></span>

<span data-ttu-id="d833c-125">如果在**“折旧年份”**字段中选择**“会计”**，则 175% 余额递减法将基于用于帐簿中指定的会计日历的会计年度或者在**“分类帐”**页面上选择的会计日历的会计年度进行计算。</span><span class="sxs-lookup"><span data-stu-id="d833c-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="d833c-126">会计年度是在**“会计日历”**页上设置的。</span><span class="sxs-lookup"><span data-stu-id="d833c-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="d833c-127">有关详细信息，请参阅[会计日历、会计和年度期间](..\budgeting\fiscal-calendars-fiscal-years-periods.md)。</span><span class="sxs-lookup"><span data-stu-id="d833c-127">For more information, see [Fiscal calendars, fiscal years, and periods.](..\budgeting\fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="d833c-128">例如，对于会计年度 7 月 1 日至次年 6 月 30 日，折旧计算从 7 月 1 日开始。</span><span class="sxs-lookup"><span data-stu-id="d833c-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="d833c-129">会计年度可以长于或短于 12 个月。</span><span class="sxs-lookup"><span data-stu-id="d833c-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="d833c-130">对于每个期间，折旧都可以自动调整，下一个会计年度的长度取决于**“财务日历”**页面上的期间的设置。</span><span class="sxs-lookup"><span data-stu-id="d833c-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="d833c-131">如果选择**“会计”**作为折旧年份，则**“期间频率”**字段中提供以下选项：</span><span class="sxs-lookup"><span data-stu-id="d833c-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="d833c-132">**“每年”**在会计年度的最后一天过帐针对会计年度计算的折旧总额。</span><span class="sxs-lookup"><span data-stu-id="d833c-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="d833c-133">**“会计期间”**将计算该会计年度的折旧总额。</span><span class="sxs-lookup"><span data-stu-id="d833c-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="d833c-134">此金额计入在**“会计日历”**页上定义的会计期间。</span><span class="sxs-lookup"><span data-stu-id="d833c-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="d833c-135">175% 余额递减法折旧的示例</span><span class="sxs-lookup"><span data-stu-id="d833c-135">Example of 175% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="d833c-136">购置成本</span><span class="sxs-lookup"><span data-stu-id="d833c-136">Acquisition cost</span></span>               | <span data-ttu-id="d833c-137">11,000</span><span class="sxs-lookup"><span data-stu-id="d833c-137">11,000</span></span> |
| <span data-ttu-id="d833c-138">Salvage value / 残值</span><span class="sxs-lookup"><span data-stu-id="d833c-138">Salvage value</span></span>                  | <span data-ttu-id="d833c-139">1,000</span><span class="sxs-lookup"><span data-stu-id="d833c-139">1,000</span></span>  |
| <span data-ttu-id="d833c-140">折旧基数</span><span class="sxs-lookup"><span data-stu-id="d833c-140">Depreciation base</span></span>              | <span data-ttu-id="d833c-141">10,000</span><span class="sxs-lookup"><span data-stu-id="d833c-141">10,000</span></span> |
| <span data-ttu-id="d833c-142">使用年限(年)</span><span class="sxs-lookup"><span data-stu-id="d833c-142">Service life years</span></span>             | <span data-ttu-id="d833c-143">5</span><span class="sxs-lookup"><span data-stu-id="d833c-143">5</span></span>      |
| <span data-ttu-id="d833c-144">每年折旧百分比</span><span class="sxs-lookup"><span data-stu-id="d833c-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="d833c-145">35%</span><span class="sxs-lookup"><span data-stu-id="d833c-145">35%</span></span>    |

<span data-ttu-id="d833c-146">175% 余额递减折旧法将 175% 除以使用年限。</span><span class="sxs-lookup"><span data-stu-id="d833c-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="d833c-147">用此百分比乘以资产的帐面净值来确定年折旧金额。</span><span class="sxs-lookup"><span data-stu-id="d833c-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="d833c-148">期间</span><span class="sxs-lookup"><span data-stu-id="d833c-148">Period</span></span> | <span data-ttu-id="d833c-149">年折旧金额的计算</span><span class="sxs-lookup"><span data-stu-id="d833c-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="d833c-150">帐面值</span><span class="sxs-lookup"><span data-stu-id="d833c-150">Book value</span></span>                  | <span data-ttu-id="d833c-151">年末帐面净值</span><span class="sxs-lookup"><span data-stu-id="d833c-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="d833c-152">第 1 年</span><span class="sxs-lookup"><span data-stu-id="d833c-152">Year 1</span></span> | <span data-ttu-id="d833c-153">(11,000 – 1,000) × 35% = 3,500</span><span class="sxs-lookup"><span data-stu-id="d833c-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="d833c-154">11,000 – 3,500 = 7,500</span><span class="sxs-lookup"><span data-stu-id="d833c-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="d833c-155">11,000 – 1,000 – 3,500 = 6,500</span><span class="sxs-lookup"><span data-stu-id="d833c-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="d833c-156">第 2 年</span><span class="sxs-lookup"><span data-stu-id="d833c-156">Year 2</span></span> | <span data-ttu-id="d833c-157">6,500 × 35% = 2,275</span><span class="sxs-lookup"><span data-stu-id="d833c-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="d833c-158">7,500 – 2,275 = 5,225</span><span class="sxs-lookup"><span data-stu-id="d833c-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="d833c-159">6,500 – 2,275 = 4,225</span><span class="sxs-lookup"><span data-stu-id="d833c-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="d833c-160">第 3 年</span><span class="sxs-lookup"><span data-stu-id="d833c-160">Year 3</span></span> | <span data-ttu-id="d833c-161">4,225 × 35% = 1,478.75</span><span class="sxs-lookup"><span data-stu-id="d833c-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="d833c-162">5,225 – 1,478.75 = 3,746.25</span><span class="sxs-lookup"><span data-stu-id="d833c-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="d833c-163">4,225 – 1,478.75 = 2,746.25</span><span class="sxs-lookup"><span data-stu-id="d833c-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="d833c-164">通常，当使用 175% 余额递减折旧法计算的金额小于使用直线法计算的金额时，对剩余年限转换到直线法。</span><span class="sxs-lookup"><span data-stu-id="d833c-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



