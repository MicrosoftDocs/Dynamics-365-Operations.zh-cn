---
title: "手动折旧"
description: "本文提供手动折旧法的概览。"
author: twheeloc
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
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e43b9397dd4e362eff9d78f302732e6bcc53d1db
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="manual-depreciation"></a><span data-ttu-id="b811b-103">手动折旧</span><span class="sxs-lookup"><span data-stu-id="b811b-103">Manual depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b811b-104">本文提供手动折旧法的概览。</span><span class="sxs-lookup"><span data-stu-id="b811b-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="b811b-105">在设置固定资产折旧模板并在**“折旧模板”**页的**“方法”**字段中选择**“手动”**之后，对于分配到此折旧模板的固定资产，其折旧均取决于为日历年度中的每个间隔输入的百分比。</span><span class="sxs-lookup"><span data-stu-id="b811b-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="b811b-106">您为其设置百分比的间隔是根据您在**“折旧模板”**页的**“常规”**快速选项卡上的**“期间频率”**字段中选择的值过帐的。</span><span class="sxs-lookup"><span data-stu-id="b811b-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="b811b-107">下面是可供选择的值：</span><span class="sxs-lookup"><span data-stu-id="b811b-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="b811b-108">每年</span><span class="sxs-lookup"><span data-stu-id="b811b-108">Yearly</span></span>
-   <span data-ttu-id="b811b-109">每月</span><span class="sxs-lookup"><span data-stu-id="b811b-109">Monthly</span></span>
-   <span data-ttu-id="b811b-110">每季度</span><span class="sxs-lookup"><span data-stu-id="b811b-110">Quarterly</span></span>
-   <span data-ttu-id="b811b-111">每半年</span><span class="sxs-lookup"><span data-stu-id="b811b-111">Half-Yearly</span></span>
-   <span data-ttu-id="b811b-112">日常</span><span class="sxs-lookup"><span data-stu-id="b811b-112">Daily</span></span>

<span data-ttu-id="b811b-113">在您选择期间频率后，请单击**“手动计划”**，并为每个过帐间隔设置百分比。</span><span class="sxs-lookup"><span data-stu-id="b811b-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="b811b-114">手动计划和过帐间隔共同定义折旧金额，如在本文中的下例所示。</span><span class="sxs-lookup"><span data-stu-id="b811b-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="b811b-115">手动折旧总是以购置价格的百分比形式进行计算。</span><span class="sxs-lookup"><span data-stu-id="b811b-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="b811b-116">对于手动折旧，在折旧间隔中输入的百分比之和不必等于 100%。</span><span class="sxs-lookup"><span data-stu-id="b811b-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="b811b-117">手动折旧是一种灵活的折旧方法，通常用来在“**帐簿**”页上定义特别折旧模板，例如用于特殊用途（例如，纳税）的非定期折旧。</span><span class="sxs-lookup"><span data-stu-id="b811b-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="b811b-118">示例</span><span class="sxs-lookup"><span data-stu-id="b811b-118">Examples</span></span>
<span data-ttu-id="b811b-119">购置价格：11,000.00 预期残值：1,000.00。下表显示您在**“固定资产折旧模板计划”**页上设置的间隔和百分比。</span><span class="sxs-lookup"><span data-stu-id="b811b-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="b811b-120">间隔编号</span><span class="sxs-lookup"><span data-stu-id="b811b-120">Interval number</span></span> | <span data-ttu-id="b811b-121">百分比</span><span class="sxs-lookup"><span data-stu-id="b811b-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="b811b-122">1</span><span class="sxs-lookup"><span data-stu-id="b811b-122">1</span></span>               | <span data-ttu-id="b811b-123">10.00</span><span class="sxs-lookup"><span data-stu-id="b811b-123">10.00</span></span>      |
| <span data-ttu-id="b811b-124">2</span><span class="sxs-lookup"><span data-stu-id="b811b-124">2</span></span>               | <span data-ttu-id="b811b-125">50.00</span><span class="sxs-lookup"><span data-stu-id="b811b-125">50.00</span></span>      |
| <span data-ttu-id="b811b-126">3</span><span class="sxs-lookup"><span data-stu-id="b811b-126">3</span></span>               | <span data-ttu-id="b811b-127">8.00</span><span class="sxs-lookup"><span data-stu-id="b811b-127">8.00</span></span>       |

<span data-ttu-id="b811b-128">下表显示如何计算，每个间隔的折旧：</span><span class="sxs-lookup"><span data-stu-id="b811b-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="b811b-129">间隔编号</span><span class="sxs-lookup"><span data-stu-id="b811b-129">Interval number</span></span> | <span data-ttu-id="b811b-130">年折旧金额的计算</span><span class="sxs-lookup"><span data-stu-id="b811b-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="b811b-131">间隔末期的帐面净值</span><span class="sxs-lookup"><span data-stu-id="b811b-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b811b-132">1</span><span class="sxs-lookup"><span data-stu-id="b811b-132">1</span></span>                | <span data-ttu-id="b811b-133">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="b811b-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="b811b-134">10,000 (11,000 – 1,000)</span><span class="sxs-lookup"><span data-stu-id="b811b-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="b811b-135">2</span><span class="sxs-lookup"><span data-stu-id="b811b-135">2</span></span>                | <span data-ttu-id="b811b-136">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="b811b-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="b811b-137">5,000 (10,000 – 5,000)</span><span class="sxs-lookup"><span data-stu-id="b811b-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="b811b-138">3</span><span class="sxs-lookup"><span data-stu-id="b811b-138">3</span></span>                | <span data-ttu-id="b811b-139">(11,000 – 1,000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="b811b-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="b811b-140">4,200 (5,000 – 800)</span><span class="sxs-lookup"><span data-stu-id="b811b-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="b811b-141">如果在**“期间频率”**字段中选择**“每月”**，则表示设置了 12 个手动计划间隔。</span><span class="sxs-lookup"><span data-stu-id="b811b-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="b811b-142">下表显示前两个间隔的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="b811b-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="b811b-143">间期</span><span class="sxs-lookup"><span data-stu-id="b811b-143">Interval</span></span> | <span data-ttu-id="b811b-144">折旧金额</span><span class="sxs-lookup"><span data-stu-id="b811b-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="b811b-145">一月</span><span class="sxs-lookup"><span data-stu-id="b811b-145">January</span></span>  | <span data-ttu-id="b811b-146">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="b811b-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="b811b-147">二月</span><span class="sxs-lookup"><span data-stu-id="b811b-147">February</span></span> | <span data-ttu-id="b811b-148">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="b811b-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="b811b-149">如果在 ****期间频率**** 字段中选择**每半年**，则表示设置了两个手动计划间隔。</span><span class="sxs-lookup"><span data-stu-id="b811b-149">If you select **Half-Yearly** in the ****Period frequency** field**, you set up two manual schedule intervals.</span></span> <span data-ttu-id="b811b-150">下表显示这两个间隔的折旧金额。</span><span class="sxs-lookup"><span data-stu-id="b811b-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="b811b-151">间期</span><span class="sxs-lookup"><span data-stu-id="b811b-151">Interval</span></span>    | <span data-ttu-id="b811b-152">折旧金额</span><span class="sxs-lookup"><span data-stu-id="b811b-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="b811b-153">6 月 30 日</span><span class="sxs-lookup"><span data-stu-id="b811b-153">June 30</span></span>     | <span data-ttu-id="b811b-154">(11,000 – 1,000) × 10% = 1,000</span><span class="sxs-lookup"><span data-stu-id="b811b-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="b811b-155">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="b811b-155">December 31</span></span> | <span data-ttu-id="b811b-156">(11,000 – 1,000) × 50% = 5,000</span><span class="sxs-lookup"><span data-stu-id="b811b-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="b811b-157">所有间隔的百分比之和不必等于 100。</span><span class="sxs-lookup"><span data-stu-id="b811b-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="b811b-158">但是，如果“**固定资产折旧模板计划**”页上的“**累计百分比**”字段不是“**100**”，您将收到错误消息 。</span><span class="sxs-lookup"><span data-stu-id="b811b-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>




