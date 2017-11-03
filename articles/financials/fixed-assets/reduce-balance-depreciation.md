---
title: "余额递减法折旧"
description: "本文提供了余额递减法折旧方法的概览。"
author: twheeloc
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 29bc8cd02d98479197d7e5f5664b9859c03893b3
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="reduce-balance-depreciation"></a><span data-ttu-id="36159-103">余额递减法折旧</span><span class="sxs-lookup"><span data-stu-id="36159-103">Reduce balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="36159-104">本文提供了余额递减法折旧方法的概览。</span><span class="sxs-lookup"><span data-stu-id="36159-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="36159-105">如果您设置固定资产折旧模板并在“折旧模板”页面上的“方法”字段中选择“余额递减法”，已分配此折旧模板的资产将在每个折旧期间按相同的百分比进行折旧。</span><span class="sxs-lookup"><span data-stu-id="36159-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="36159-106">若要设置余额递减法，还必须在“折旧模板”页的“常规”快速选项卡上的各个字段中进行选择。</span><span class="sxs-lookup"><span data-stu-id="36159-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="36159-107">首先在“折旧年份”字段中选择某一年份。</span><span class="sxs-lookup"><span data-stu-id="36159-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="36159-108">根据选择，“期间频率”字段中将显示不同的选项，以下部分对它进行了说明。</span><span class="sxs-lookup"><span data-stu-id="36159-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="36159-109">您还必须为折旧模板在“百分比”字段中输入某一值。</span><span class="sxs-lookup"><span data-stu-id="36159-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="36159-110">如果您选择“完全折旧”选项，则剩余折旧基数取自最后折旧期间并且可以是最高金额。</span><span class="sxs-lookup"><span data-stu-id="36159-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="36159-111">某些国家/地区并不使用对直线折旧法的替换折旧。</span><span class="sxs-lookup"><span data-stu-id="36159-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="36159-112">备选折旧大于等于主折旧模板金额并且折旧金额采用备选方法金额的值时，进行转换。</span><span class="sxs-lookup"><span data-stu-id="36159-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="36159-113">因为基于百分比计算资产将永远不会完全折旧，所以，您必须选择“完全折旧”选项以完全折旧某一资产。</span><span class="sxs-lookup"><span data-stu-id="36159-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="36159-114">选择折旧年份</span><span class="sxs-lookup"><span data-stu-id="36159-114">Select a depreciation year</span></span>
<span data-ttu-id="36159-115">您可以在“折旧模板”页上的“折旧年份”字段中选择“日历”或“会计”。</span><span class="sxs-lookup"><span data-stu-id="36159-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="36159-116">此选择将定义“期间频率”字段中可用的选项。</span><span class="sxs-lookup"><span data-stu-id="36159-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="36159-117">默认选项为“日历”。</span><span class="sxs-lookup"><span data-stu-id="36159-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="36159-118">日历</span><span class="sxs-lookup"><span data-stu-id="36159-118">Calendar</span></span>

<span data-ttu-id="36159-119">使用“日历”选项，可以在每年 1 月 1 日更新折旧基数（通常为帐面净值减去残值）。</span><span class="sxs-lookup"><span data-stu-id="36159-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="36159-120">在本主题稍后的余额递减法示例中，折旧基数是计算列中第一个表达式的分子。</span><span class="sxs-lookup"><span data-stu-id="36159-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="36159-121">如果选择“日历”，则在“期间频率”字段中提供以下选项，这些选项定义了整个日历年度的折旧应计过帐日期和金额：</span><span class="sxs-lookup"><span data-stu-id="36159-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="36159-122">在 12 月 31 日进行“每月”过帐。</span><span class="sxs-lookup"><span data-stu-id="36159-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="36159-123">“每月”在每个日历月末过帐每月金额。</span><span class="sxs-lookup"><span data-stu-id="36159-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="36159-124">“每季度”在每个日历季度末（3 月 31 日、6 月 30 日、9 月 30 日和 12 月 31 日）过帐季度金额。</span><span class="sxs-lookup"><span data-stu-id="36159-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="36159-125">每半年在每个日历半年末（6 月 30 日和 12 月 31 日）过帐半年金额。</span><span class="sxs-lookup"><span data-stu-id="36159-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="36159-126">“每日”通过对每天使用一个交易记录来过帐每日折旧方法的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="36159-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="36159-127">例如，如果您选择每年，年折旧只过帐一次，在每年的 12 月 31 日。</span><span class="sxs-lookup"><span data-stu-id="36159-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="36159-128">如果您选择“每月”，月折旧每月按年折旧金额的 1/12 过帐。</span><span class="sxs-lookup"><span data-stu-id="36159-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="36159-129">会计</span><span class="sxs-lookup"><span data-stu-id="36159-129">Fiscal</span></span>

<span data-ttu-id="36159-130">如果在“折旧年份”字段中选择“会计”，则使用直线折旧法。</span><span class="sxs-lookup"><span data-stu-id="36159-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="36159-131">它是基于会计年度计算的，会计年度在“分类帐”页中选择的会计日历的“会计日历”页中设置。</span><span class="sxs-lookup"><span data-stu-id="36159-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="36159-132">例如，对于会计年度 7 月 1 日至次年 6 月 30 日，折旧计算从 7 月 1 日开始。</span><span class="sxs-lookup"><span data-stu-id="36159-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="36159-133">会计年度可以长于或短于 12 个月。</span><span class="sxs-lookup"><span data-stu-id="36159-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="36159-134">对于每个会计期间，都可以调整折旧。</span><span class="sxs-lookup"><span data-stu-id="36159-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="36159-135">下一会计年度的长度基于您在“会计日历”页中创建新的会计年度时设置的会计期间。</span><span class="sxs-lookup"><span data-stu-id="36159-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="36159-136">如果在“期间频率”字段中选择“会计”，以下期间频率选项可用：</span><span class="sxs-lookup"><span data-stu-id="36159-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="36159-137">“每年”为会计年度计算的折旧总额作为一笔金额在该会计年度的最后一天进行过帐。</span><span class="sxs-lookup"><span data-stu-id="36159-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="36159-138">“会计期间”过帐为会计年度计算的总折旧金额。该金额应记入为“分类帐”页中选择的会计日历或为固定资产的帐簿选择的会计日历定义的会计期间中。</span><span class="sxs-lookup"><span data-stu-id="36159-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="36159-139">余额递减法折旧的示例</span><span class="sxs-lookup"><span data-stu-id="36159-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="36159-140">假定固定资产购置价格是 11,000，残值是 1,000，并且折旧百分比系数是 30。</span><span class="sxs-lookup"><span data-stu-id="36159-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="36159-141">使用“余额递减”法，在上一折旧期间结束时计算 30% 的折旧基数（帐面净值减去残值）。</span><span class="sxs-lookup"><span data-stu-id="36159-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="36159-142">前三年的折旧在下表中显示。</span><span class="sxs-lookup"><span data-stu-id="36159-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="36159-143">期间</span><span class="sxs-lookup"><span data-stu-id="36159-143">Period</span></span> | <span data-ttu-id="36159-144">年折旧金额的计算</span><span class="sxs-lookup"><span data-stu-id="36159-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="36159-145">年末帐面净值</span><span class="sxs-lookup"><span data-stu-id="36159-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="36159-146">第 1 年</span><span class="sxs-lookup"><span data-stu-id="36159-146">Year 1</span></span> | <span data-ttu-id="36159-147">(11,000 - 1,000) \* 30% = 3,000</span><span class="sxs-lookup"><span data-stu-id="36159-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="36159-148">(11,000 - 1,000) - 3,000 = 7,000</span><span class="sxs-lookup"><span data-stu-id="36159-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="36159-149">第 2 年</span><span class="sxs-lookup"><span data-stu-id="36159-149">Year 2</span></span> | <span data-ttu-id="36159-150">(7,000 - 1,000) \* 30% = 1,800</span><span class="sxs-lookup"><span data-stu-id="36159-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="36159-151">(7,000 -1,800) = 5,200</span><span class="sxs-lookup"><span data-stu-id="36159-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="36159-152">第 3 年</span><span class="sxs-lookup"><span data-stu-id="36159-152">Year 3</span></span> | <span data-ttu-id="36159-153">(5,200 - 1,000) \* 30% = 1,260</span><span class="sxs-lookup"><span data-stu-id="36159-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="36159-154">(5,200 - 1,260) = 3,940</span><span class="sxs-lookup"><span data-stu-id="36159-154">(5,200 - 1,260) = 3,940</span></span>               |

 
-






