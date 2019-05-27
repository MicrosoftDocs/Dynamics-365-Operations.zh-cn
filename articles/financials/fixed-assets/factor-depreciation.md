---
title: 因素/系数折旧
description: 本文提供系数折旧法的概览。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa8bc4566def9dd770a97facb459e6b977bfaffb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546747"
---
# <a name="factor-depreciation"></a><span data-ttu-id="d7656-103">因素/系数折旧</span><span class="sxs-lookup"><span data-stu-id="d7656-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7656-104">本文提供系数折旧法的概览。</span><span class="sxs-lookup"><span data-stu-id="d7656-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="d7656-105">系数是用于对资产进行折旧的百分比。</span><span class="sxs-lookup"><span data-stu-id="d7656-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="d7656-106">在您设置固定资产折旧模板并在**折旧模板**页的**方法**字段中选择**系数**时，可以设置累进、非累进或直线折旧法：</span><span class="sxs-lookup"><span data-stu-id="d7656-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="d7656-107">在累进折旧法中，折旧金额将增加每个折旧期间。</span><span class="sxs-lookup"><span data-stu-id="d7656-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="d7656-108">在非累进折旧法中，每个期间的折旧金额将随着时间减少。</span><span class="sxs-lookup"><span data-stu-id="d7656-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="d7656-109">在直线折旧法中，在每个期间中折旧都相同。</span><span class="sxs-lookup"><span data-stu-id="d7656-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="d7656-110">下面的规则和示例指示您如何为每种折旧类型设置系数。</span><span class="sxs-lookup"><span data-stu-id="d7656-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="d7656-111">当您在**方法**字段中选择**系数**时，**系数**字段和**间隔**字段将显示。</span><span class="sxs-lookup"><span data-stu-id="d7656-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="d7656-112">累进折旧</span><span class="sxs-lookup"><span data-stu-id="d7656-112">Progressive depreciation</span></span>
<span data-ttu-id="d7656-113">**系数**字段中的值大于 **50**。</span><span class="sxs-lookup"><span data-stu-id="d7656-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="d7656-114">示例</span><span class="sxs-lookup"><span data-stu-id="d7656-114">Example</span></span>

<span data-ttu-id="d7656-115">购置价格为 100,000，系数为 70，使用年限为 10 年，并且折旧在 1 月 1 日开始。</span><span class="sxs-lookup"><span data-stu-id="d7656-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="d7656-116">只为使用年限的前 6 年显示折旧金额和帐面净额。</span><span class="sxs-lookup"><span data-stu-id="d7656-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="d7656-117">年</span><span class="sxs-lookup"><span data-stu-id="d7656-117">Year</span></span> | <span data-ttu-id="d7656-118">期间</span><span class="sxs-lookup"><span data-stu-id="d7656-118">Period</span></span>      | <span data-ttu-id="d7656-119">折旧金额</span><span class="sxs-lookup"><span data-stu-id="d7656-119">Depreciation amount</span></span> | <span data-ttu-id="d7656-120">帐面净值</span><span class="sxs-lookup"><span data-stu-id="d7656-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="d7656-121">1</span><span class="sxs-lookup"><span data-stu-id="d7656-121">1</span></span>    | <span data-ttu-id="d7656-122">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-122">December 31</span></span> | <span data-ttu-id="d7656-123">307.69</span><span class="sxs-lookup"><span data-stu-id="d7656-123">307.69</span></span>              | <span data-ttu-id="d7656-124">99,692.31</span><span class="sxs-lookup"><span data-stu-id="d7656-124">99,692.31</span></span>             |
| <span data-ttu-id="d7656-125">2</span><span class="sxs-lookup"><span data-stu-id="d7656-125">2</span></span>    | <span data-ttu-id="d7656-126">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-126">December 31</span></span> | <span data-ttu-id="d7656-127">1,447.21</span><span class="sxs-lookup"><span data-stu-id="d7656-127">1,447.21</span></span>            | <span data-ttu-id="d7656-128">98,245.10</span><span class="sxs-lookup"><span data-stu-id="d7656-128">98,245.10</span></span>             |
| <span data-ttu-id="d7656-129">3</span><span class="sxs-lookup"><span data-stu-id="d7656-129">3</span></span>    | <span data-ttu-id="d7656-130">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-130">December 31</span></span> | <span data-ttu-id="d7656-131">3,104.50</span><span class="sxs-lookup"><span data-stu-id="d7656-131">3,104.50</span></span>            | <span data-ttu-id="d7656-132">95,140.60</span><span class="sxs-lookup"><span data-stu-id="d7656-132">95,140.60</span></span>             |
| <span data-ttu-id="d7656-133">4</span><span class="sxs-lookup"><span data-stu-id="d7656-133">4</span></span>    | <span data-ttu-id="d7656-134">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-134">December 31</span></span> | <span data-ttu-id="d7656-135">5,150.21</span><span class="sxs-lookup"><span data-stu-id="d7656-135">5,150.21</span></span>            | <span data-ttu-id="d7656-136">89,990.39</span><span class="sxs-lookup"><span data-stu-id="d7656-136">89,990.39</span></span>             |
| <span data-ttu-id="d7656-137">5</span><span class="sxs-lookup"><span data-stu-id="d7656-137">5</span></span>    | <span data-ttu-id="d7656-138">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-138">December 31</span></span> | <span data-ttu-id="d7656-139">7,522.95</span><span class="sxs-lookup"><span data-stu-id="d7656-139">7,522.95</span></span>            | <span data-ttu-id="d7656-140">82,467.44</span><span class="sxs-lookup"><span data-stu-id="d7656-140">82,467.44</span></span>             |
| <span data-ttu-id="d7656-141">6</span><span class="sxs-lookup"><span data-stu-id="d7656-141">6</span></span>    | <span data-ttu-id="d7656-142">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-142">December 31</span></span> | <span data-ttu-id="d7656-143">10,184.06</span><span class="sxs-lookup"><span data-stu-id="d7656-143">10,184.06</span></span>           | <span data-ttu-id="d7656-144">72,283.38</span><span class="sxs-lookup"><span data-stu-id="d7656-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="d7656-145">非累进折旧</span><span class="sxs-lookup"><span data-stu-id="d7656-145">Digressive depreciation</span></span>
<span data-ttu-id="d7656-146">**系数**字段中的值小于 **50**。</span><span class="sxs-lookup"><span data-stu-id="d7656-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="d7656-147">示例</span><span class="sxs-lookup"><span data-stu-id="d7656-147">Example</span></span>

<span data-ttu-id="d7656-148">购置价格为 100,000，系数为 20，使用年限为 10 年，并且折旧在 1 月 1 日开始。</span><span class="sxs-lookup"><span data-stu-id="d7656-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="d7656-149">只为使用年限的前 6 年显示折旧金额和帐面净额。</span><span class="sxs-lookup"><span data-stu-id="d7656-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="d7656-150">年</span><span class="sxs-lookup"><span data-stu-id="d7656-150">Year</span></span> | <span data-ttu-id="d7656-151">期间</span><span class="sxs-lookup"><span data-stu-id="d7656-151">Period</span></span>      | <span data-ttu-id="d7656-152">折旧金额</span><span class="sxs-lookup"><span data-stu-id="d7656-152">Depreciation amount</span></span> | <span data-ttu-id="d7656-153">帐面净值</span><span class="sxs-lookup"><span data-stu-id="d7656-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="d7656-154">1</span><span class="sxs-lookup"><span data-stu-id="d7656-154">1</span></span>    | <span data-ttu-id="d7656-155">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-155">December 31</span></span> | <span data-ttu-id="d7656-156">56,080.43</span><span class="sxs-lookup"><span data-stu-id="d7656-156">56,080.43</span></span>           | <span data-ttu-id="d7656-157">43,919.57</span><span class="sxs-lookup"><span data-stu-id="d7656-157">43,919.57</span></span>             |
| <span data-ttu-id="d7656-158">2</span><span class="sxs-lookup"><span data-stu-id="d7656-158">2</span></span>    | <span data-ttu-id="d7656-159">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-159">December 31</span></span> | <span data-ttu-id="d7656-160">10,665.70</span><span class="sxs-lookup"><span data-stu-id="d7656-160">10,665.70</span></span>           | <span data-ttu-id="d7656-161">33,253.87</span><span class="sxs-lookup"><span data-stu-id="d7656-161">33,253.87</span></span>             |
| <span data-ttu-id="d7656-162">3</span><span class="sxs-lookup"><span data-stu-id="d7656-162">3</span></span>    | <span data-ttu-id="d7656-163">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-163">December 31</span></span> | <span data-ttu-id="d7656-164">7,156.22</span><span class="sxs-lookup"><span data-stu-id="d7656-164">7,156.22</span></span>            | <span data-ttu-id="d7656-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="d7656-165">26,097.65</span></span>             |
| <span data-ttu-id="d7656-166">4</span><span class="sxs-lookup"><span data-stu-id="d7656-166">4</span></span>    | <span data-ttu-id="d7656-167">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-167">December 31</span></span> | <span data-ttu-id="d7656-168">5,538.06</span><span class="sxs-lookup"><span data-stu-id="d7656-168">5,538.06</span></span>            | <span data-ttu-id="d7656-169">20,559.59</span><span class="sxs-lookup"><span data-stu-id="d7656-169">20,559.59</span></span>             |
| <span data-ttu-id="d7656-170">5</span><span class="sxs-lookup"><span data-stu-id="d7656-170">5</span></span>    | <span data-ttu-id="d7656-171">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-171">December 31</span></span> | <span data-ttu-id="d7656-172">4,579.89</span><span class="sxs-lookup"><span data-stu-id="d7656-172">4,579.89</span></span>            | <span data-ttu-id="d7656-173">15,979.70</span><span class="sxs-lookup"><span data-stu-id="d7656-173">15,979.70</span></span>             |
| <span data-ttu-id="d7656-174">6</span><span class="sxs-lookup"><span data-stu-id="d7656-174">6</span></span>    | <span data-ttu-id="d7656-175">12 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d7656-175">December 31</span></span> | <span data-ttu-id="d7656-176">3,937.36</span><span class="sxs-lookup"><span data-stu-id="d7656-176">3,937.36</span></span>            | <span data-ttu-id="d7656-177">12,042.34</span><span class="sxs-lookup"><span data-stu-id="d7656-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="d7656-178">直线折旧法</span><span class="sxs-lookup"><span data-stu-id="d7656-178">Straight line depreciation</span></span>
<span data-ttu-id="d7656-179">**系数**字段中的值等于 **50**。</span><span class="sxs-lookup"><span data-stu-id="d7656-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="d7656-180">在此情况下，折旧在每个期间中都相同，并且您应该考虑在其他字段中指定的值的意义，如[直线法折旧](straight-line-service-life-depreciation.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="d7656-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



