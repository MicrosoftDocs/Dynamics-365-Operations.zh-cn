---
title: 剩余年限法折旧
description: 本文提供了直线法（剩余年限）折旧方法的概览。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 823b2569670adfbf04038abca656e34f0199fce1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210087"
---
# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="0aed2-103">剩余年限法折旧</span><span class="sxs-lookup"><span data-stu-id="0aed2-103">Straight line life remaining depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0aed2-104">本文提供了直线法（剩余年限）折旧方法的概览。</span><span class="sxs-lookup"><span data-stu-id="0aed2-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="0aed2-105">在设置固定资产折旧模板并在 **折旧模板** 页的 **方法** 字段中选择 **直线法（剩余年限）** 时，分配给该折旧模板的固定资产折旧将基于资产的剩余使用年限。</span><span class="sxs-lookup"><span data-stu-id="0aed2-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="0aed2-106">通常，每个折旧期间的折旧金额相同。</span><span class="sxs-lookup"><span data-stu-id="0aed2-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="0aed2-107">若要设置直线法（剩余年限）折旧，您还必须在 **折旧模板** 页面上的 **折旧年份** 字段和 **期间频率** 字段中选择选项。</span><span class="sxs-lookup"><span data-stu-id="0aed2-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="0aed2-108">**期间频率** 字段中提供的选项因 **折旧年份** 字段中所选的值而异。</span><span class="sxs-lookup"><span data-stu-id="0aed2-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="0aed2-109">选择折旧年份</span><span class="sxs-lookup"><span data-stu-id="0aed2-109">Select a depreciation year</span></span>
<span data-ttu-id="0aed2-110">您可以在 **折旧模板** 页上的 **折旧年份** 字段中选择 **日历** 或 **会计**。</span><span class="sxs-lookup"><span data-stu-id="0aed2-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="0aed2-111">默认值是 **日历**。</span><span class="sxs-lookup"><span data-stu-id="0aed2-111">The default value is **Calendar**.</span></span> <span data-ttu-id="0aed2-112">您的选择将决定 **期间频率** 字段中可用的选项。</span><span class="sxs-lookup"><span data-stu-id="0aed2-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="0aed2-113">此字段定义整个日历年度的折旧应计过帐日期和金额。</span><span class="sxs-lookup"><span data-stu-id="0aed2-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="0aed2-114">日历</span><span class="sxs-lookup"><span data-stu-id="0aed2-114">Calendar</span></span>

<span data-ttu-id="0aed2-115">如果在 **_折旧年份_*_字段中选择 **日历**，即使对会计日历作了不同定义，仍然假设一年的起止时间为 1 月 1 日到 12 月 31 日。_\* 日历*\* 选项在每年的 1 月 1 日更新折旧基数。</span><span class="sxs-lookup"><span data-stu-id="0aed2-115">If you select **Calendar** in the **_Depreciation year_*_ field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently. The _\* Calendar*\* option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="0aed2-116">通常，折旧基数是帐面净值减去残值。</span><span class="sxs-lookup"><span data-stu-id="0aed2-116">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="0aed2-117">在此主题后面的示例中，折旧基数是计算列中第一个表达式的分子。</span><span class="sxs-lookup"><span data-stu-id="0aed2-117">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="0aed2-118">如果选择 **日历** 作为折旧年份，则 **期间频率** 字段中提供以下选项：</span><span class="sxs-lookup"><span data-stu-id="0aed2-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="0aed2-119">**每年** 在 12 月 31 日过帐金额。</span><span class="sxs-lookup"><span data-stu-id="0aed2-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="0aed2-120">**每月** 在每个日历月末过帐每月金额。</span><span class="sxs-lookup"><span data-stu-id="0aed2-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="0aed2-121">**每季度** 在每个日历季度末（3 月 31 日、6 月 30 日、9 月 30 日和 12 月 31 日）过帐季度金额。</span><span class="sxs-lookup"><span data-stu-id="0aed2-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="0aed2-122">**每半年** 在每个日历半年末（6 月 30 日和 12 月 31 日）过帐半年金额。</span><span class="sxs-lookup"><span data-stu-id="0aed2-122">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="0aed2-123">**每日** 通过对每天使用一个交易记录来过帐每日折旧方法的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="0aed2-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="0aed2-124">例如，如果您选择 **每年**，年折旧只过帐一次，在每年的 12 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="0aed2-124">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="0aed2-125">如果您选择 **每月**，月折旧每月按年折旧金额的 1/12 过帐。</span><span class="sxs-lookup"><span data-stu-id="0aed2-125">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="0aed2-126">会计</span><span class="sxs-lookup"><span data-stu-id="0aed2-126">Fiscal</span></span>

<span data-ttu-id="0aed2-127">如果在 **折旧年份** 字段中选择 **会计**，则使用直线剩余年限折旧法。</span><span class="sxs-lookup"><span data-stu-id="0aed2-127">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="0aed2-128">折旧基于会计年度剩余计算。</span><span class="sxs-lookup"><span data-stu-id="0aed2-128">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="0aed2-129">例如，对于会计年度 2015 年 7 月 1 日至 2016 年 6 月 30 日，折旧计算从 7 月 1 日开始。</span><span class="sxs-lookup"><span data-stu-id="0aed2-129">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="0aed2-130">会计年度可以长于或短于 12 个月。</span><span class="sxs-lookup"><span data-stu-id="0aed2-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="0aed2-131">对于每个会计期间，都可以调整折旧。</span><span class="sxs-lookup"><span data-stu-id="0aed2-131">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="0aed2-132">下一会计年度的长度由 **会计日历** 页面上设置的会计期间决定。</span><span class="sxs-lookup"><span data-stu-id="0aed2-132">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="0aed2-133">如果选择 **会计** 作为折旧年份，则 **期间频率** 字段中提供以下选项：</span><span class="sxs-lookup"><span data-stu-id="0aed2-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="0aed2-134">**每年** 为会计年度计算的折旧总额作为一笔金额在该会计年度的最后一天进行过帐。</span><span class="sxs-lookup"><span data-stu-id="0aed2-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="0aed2-135">**会计期间** 将计算该会计年度的折旧总额。</span><span class="sxs-lookup"><span data-stu-id="0aed2-135">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="0aed2-136">此金额然后计入在为帐簿指定的会计日历的 **会计日历** 页上定义的会计期间。</span><span class="sxs-lookup"><span data-stu-id="0aed2-136">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="0aed2-137">对未更改的固定资产进行直线法折旧的示例</span><span class="sxs-lookup"><span data-stu-id="0aed2-137">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="0aed2-138">固定资产具有以下特征。</span><span class="sxs-lookup"><span data-stu-id="0aed2-138">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="0aed2-139">购置成本</span><span class="sxs-lookup"><span data-stu-id="0aed2-139">Acquisition cost</span></span>    | <span data-ttu-id="0aed2-140">11,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-140">11,000</span></span> |
| <span data-ttu-id="0aed2-141">Salvage value / 残值</span><span class="sxs-lookup"><span data-stu-id="0aed2-141">Salvage value</span></span>       | <span data-ttu-id="0aed2-142">1,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-142">1,000</span></span>  |
| <span data-ttu-id="0aed2-143">折旧基数</span><span class="sxs-lookup"><span data-stu-id="0aed2-143">Depreciation base</span></span>   | <span data-ttu-id="0aed2-144">10,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-144">10,000</span></span> |
| <span data-ttu-id="0aed2-145">使用年限(年)</span><span class="sxs-lookup"><span data-stu-id="0aed2-145">Service life years</span></span>  | <span data-ttu-id="0aed2-146">5</span><span class="sxs-lookup"><span data-stu-id="0aed2-146">5</span></span>      |
| <span data-ttu-id="0aed2-147">每年折旧</span><span class="sxs-lookup"><span data-stu-id="0aed2-147">Yearly depreciation</span></span> | <span data-ttu-id="0aed2-148">2,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-148">2,000</span></span>  |

<span data-ttu-id="0aed2-149">每年的折旧金额相同：（购置成本 – 残值）÷使用年限</span><span class="sxs-lookup"><span data-stu-id="0aed2-149">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="0aed2-150">期间</span><span class="sxs-lookup"><span data-stu-id="0aed2-150">Period</span></span> | <span data-ttu-id="0aed2-151">年折旧金额的计算</span><span class="sxs-lookup"><span data-stu-id="0aed2-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="0aed2-152">年末帐面净值</span><span class="sxs-lookup"><span data-stu-id="0aed2-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="0aed2-153">第 1 年</span><span class="sxs-lookup"><span data-stu-id="0aed2-153">Year 1</span></span> | <span data-ttu-id="0aed2-154">(11,000 – 1,000) ÷ 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-154">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="0aed2-155">9,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-155">9,000</span></span>                                 |
| <span data-ttu-id="0aed2-156">第 2 年</span><span class="sxs-lookup"><span data-stu-id="0aed2-156">Year 2</span></span> | <span data-ttu-id="0aed2-157">(9,000 – 1,000) ÷ 4 = 2,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-157">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="0aed2-158">7,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-158">7,000</span></span>                                 |
| <span data-ttu-id="0aed2-159">第 3 年</span><span class="sxs-lookup"><span data-stu-id="0aed2-159">Year 3</span></span> | <span data-ttu-id="0aed2-160">(7,000 – 1,000) ÷ 3 = 2,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-160">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="0aed2-161">5,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-161">5,000</span></span>                                 |
| <span data-ttu-id="0aed2-162">第 4 年</span><span class="sxs-lookup"><span data-stu-id="0aed2-162">Year 4</span></span> | <span data-ttu-id="0aed2-163">(5,000 – 1,000) ÷ 2 = 2,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-163">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="0aed2-164">3,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-164">3,000</span></span>                                 |
| <span data-ttu-id="0aed2-165">第 5 年</span><span class="sxs-lookup"><span data-stu-id="0aed2-165">Year 5</span></span> | <span data-ttu-id="0aed2-166">(3,000 – 1,000) ÷ 1 = 2,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-166">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="0aed2-167">1,000</span><span class="sxs-lookup"><span data-stu-id="0aed2-167">1,000</span></span>                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]