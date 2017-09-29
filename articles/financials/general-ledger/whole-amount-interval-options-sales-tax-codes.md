---
title: "全部金额和销售税代码的间隔计算选项"
description: "本文说明销售税代码上的“计算方法”字段选项，以及如何为间隔和全部金额计算销售税。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 55cb0f20dbd671e39d0f409a87cec93efd9ce4d6
ms.openlocfilehash: bab0f6ca21f4216b70cccf24f5781e0dbf48b7f8
ms.contentlocale: zh-cn
ms.lasthandoff: 07/07/2017


---

# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="d90a7-103">全部金额和销售税代码的间隔计算选项</span><span class="sxs-lookup"><span data-stu-id="d90a7-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]



<span data-ttu-id="d90a7-104">本文说明销售税代码上的“计算方法”字段选项，以及如何为间隔和全部金额计算销售税。</span><span class="sxs-lookup"><span data-stu-id="d90a7-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="d90a7-105">您可以设置基于整个金额或间隔金额将计算出的增值税代码。</span><span class="sxs-lookup"><span data-stu-id="d90a7-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="d90a7-106">在“销售税代码”页中，使用字段“计算方法”（在“计算”快速选项卡上）选择如何计算销售税代码。</span><span class="sxs-lookup"><span data-stu-id="d90a7-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
-   <span data-ttu-id="d90a7-107">全部金额 – 税率适用于整个应纳税金额。</span><span class="sxs-lookup"><span data-stu-id="d90a7-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
-   <span data-ttu-id="d90a7-108">间隔 – 应纳税金额划分为多个部分，每个部分都处于具有特定增值税税率的范围内。</span><span class="sxs-lookup"><span data-stu-id="d90a7-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="d90a7-109">处于给定间隔范围内的金额部分根据该间隔的税率计税。</span><span class="sxs-lookup"><span data-stu-id="d90a7-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="d90a7-110">该增值税是为各个金额间隔计算的税额的总和。</span><span class="sxs-lookup"><span data-stu-id="d90a7-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
> [!NOTE]                                                                                                                              
> <span data-ttu-id="d90a7-111">只有当您在“总帐参数”页的销售税区域中的“计算方法”字段中选择“行”时“间隔”选项才可用。</span><span class="sxs-lookup"><span data-stu-id="d90a7-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="d90a7-112">间隔在“销售税代码值”页通过输入每个税率的最小和最大限制金额来设置。</span><span class="sxs-lookup"><span data-stu-id="d90a7-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="d90a7-113">对于要对所有应纳税金额计算的税款（而与所选方法无关），间隔必须符合以下规则：</span><span class="sxs-lookup"><span data-stu-id="d90a7-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="d90a7-114">第一个间隔必须具有下限 0。</span><span class="sxs-lookup"><span data-stu-id="d90a7-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="d90a7-115">最后一个间隔必须具有上限 0，表示无穷大。</span><span class="sxs-lookup"><span data-stu-id="d90a7-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="d90a7-116">任何间隔的上限都必须是下一间隔的下限。</span><span class="sxs-lookup"><span data-stu-id="d90a7-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="d90a7-117">如果某一金额是上一个间隔的上限和下一间隔的下限，则第一个间隔的税率将适用于该金额。</span><span class="sxs-lookup"><span data-stu-id="d90a7-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="d90a7-118">如果某一金额处于上限和下限定义的间隔外，则增值税率 0 适用。</span><span class="sxs-lookup"><span data-stu-id="d90a7-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="d90a7-119">示例：计算的全部金额方法</span><span class="sxs-lookup"><span data-stu-id="d90a7-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="d90a7-120">在“销售税代码值”页中，以下面间隔设置增值税率：</span><span class="sxs-lookup"><span data-stu-id="d90a7-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>
|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="d90a7-121">**下限**</span><span class="sxs-lookup"><span data-stu-id="d90a7-121">**Minimum limit**</span></span> | <span data-ttu-id="d90a7-122">**上限**</span><span class="sxs-lookup"><span data-stu-id="d90a7-122">**Maximum limit**</span></span> | <span data-ttu-id="d90a7-123">**税率**</span><span class="sxs-lookup"><span data-stu-id="d90a7-123">**Tax rate**</span></span> |
| <span data-ttu-id="d90a7-124">0.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-124">0.00</span></span>              | <span data-ttu-id="d90a7-125">50.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-125">50.00</span></span>             | <span data-ttu-id="d90a7-126">30%</span><span class="sxs-lookup"><span data-stu-id="d90a7-126">30%</span></span>          |
| <span data-ttu-id="d90a7-127">50.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-127">50.00</span></span>             | <span data-ttu-id="d90a7-128">100.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-128">100.00</span></span>            | <span data-ttu-id="d90a7-129">20%</span><span class="sxs-lookup"><span data-stu-id="d90a7-129">20%</span></span>          |
| <span data-ttu-id="d90a7-130">100.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-130">100.00</span></span>            | <span data-ttu-id="d90a7-131">0.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-131">0.00</span></span>              | <span data-ttu-id="d90a7-132">10%</span><span class="sxs-lookup"><span data-stu-id="d90a7-132">10%</span></span>          |

<span data-ttu-id="d90a7-133">增值税基于总应纳税金额计算。</span><span class="sxs-lookup"><span data-stu-id="d90a7-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="d90a7-134">应纳税金额（价格）</span><span class="sxs-lookup"><span data-stu-id="d90a7-134">Taxable amount (price)</span></span> | <span data-ttu-id="d90a7-135">计算</span><span class="sxs-lookup"><span data-stu-id="d90a7-135">Calculation</span></span>    | <span data-ttu-id="d90a7-136">增值税</span><span class="sxs-lookup"><span data-stu-id="d90a7-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="d90a7-137">35.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-137">35.00</span></span>                  | <span data-ttu-id="d90a7-138">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="d90a7-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="d90a7-139">1050</span><span class="sxs-lookup"><span data-stu-id="d90a7-139">10.50</span></span>     |
| <span data-ttu-id="d90a7-140">50.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-140">50.00</span></span>                  | <span data-ttu-id="d90a7-141">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="d90a7-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="d90a7-142">15.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-142">15.00</span></span>     |
| <span data-ttu-id="d90a7-143">85.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-143">85.00</span></span>                  | <span data-ttu-id="d90a7-144">85.00 \* 0.20</span><span class="sxs-lookup"><span data-stu-id="d90a7-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="d90a7-145">17.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-145">17.00</span></span>     |
| <span data-ttu-id="d90a7-146">305.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-146">305.00</span></span>                 | <span data-ttu-id="d90a7-147">305.00 \* 0.10</span><span class="sxs-lookup"><span data-stu-id="d90a7-147">305.00 \* 0.10</span></span> | <span data-ttu-id="d90a7-148">30.50</span><span class="sxs-lookup"><span data-stu-id="d90a7-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="d90a7-149">示例：计算的间隔方法</span><span class="sxs-lookup"><span data-stu-id="d90a7-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="d90a7-150">在“值”页中，以下面间隔设置增值税率：</span><span class="sxs-lookup"><span data-stu-id="d90a7-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="d90a7-151">**下限**</span><span class="sxs-lookup"><span data-stu-id="d90a7-151">**Minimum limit**</span></span> | <span data-ttu-id="d90a7-152">**上限**</span><span class="sxs-lookup"><span data-stu-id="d90a7-152">**Maximum limit**</span></span> | <span data-ttu-id="d90a7-153">**税率**</span><span class="sxs-lookup"><span data-stu-id="d90a7-153">**Tax rate**</span></span> |
| <span data-ttu-id="d90a7-154">0.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-154">0.00</span></span>              | <span data-ttu-id="d90a7-155">50.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-155">50.00</span></span>             | <span data-ttu-id="d90a7-156">30%</span><span class="sxs-lookup"><span data-stu-id="d90a7-156">30%</span></span>          |
| <span data-ttu-id="d90a7-157">50.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-157">50.00</span></span>             | <span data-ttu-id="d90a7-158">100.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-158">100.00</span></span>            | <span data-ttu-id="d90a7-159">20%</span><span class="sxs-lookup"><span data-stu-id="d90a7-159">20%</span></span>          |
| <span data-ttu-id="d90a7-160">100.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-160">100.00</span></span>            | <span data-ttu-id="d90a7-161">0.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-161">0.00</span></span>              | <span data-ttu-id="d90a7-162">10%</span><span class="sxs-lookup"><span data-stu-id="d90a7-162">10%</span></span>          |

<span data-ttu-id="d90a7-163">该增值税是为各个金额间隔计算的税额的总和。</span><span class="sxs-lookup"><span data-stu-id="d90a7-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="d90a7-164">应纳税金额（价格）</span><span class="sxs-lookup"><span data-stu-id="d90a7-164">Taxable amount (price)</span></span> | <span data-ttu-id="d90a7-165">计算</span><span class="sxs-lookup"><span data-stu-id="d90a7-165">Calculation</span></span>                                                               | <span data-ttu-id="d90a7-166">增值税</span><span class="sxs-lookup"><span data-stu-id="d90a7-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d90a7-167">35.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-167">35.00</span></span>                  | <span data-ttu-id="d90a7-168">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="d90a7-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="d90a7-169">1050</span><span class="sxs-lookup"><span data-stu-id="d90a7-169">10.50</span></span>     |
| <span data-ttu-id="d90a7-170">50.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-170">50.00</span></span>                  | <span data-ttu-id="d90a7-171">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="d90a7-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="d90a7-172">15.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-172">15.00</span></span>     |
| <span data-ttu-id="d90a7-173">85.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-173">85.00</span></span>                  | <span data-ttu-id="d90a7-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span><span class="sxs-lookup"><span data-stu-id="d90a7-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="d90a7-175">22.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-175">22.00</span></span>     |
| <span data-ttu-id="d90a7-176">305.00</span><span class="sxs-lookup"><span data-stu-id="d90a7-176">305.00</span></span>                 | <span data-ttu-id="d90a7-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span><span class="sxs-lookup"><span data-stu-id="d90a7-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="d90a7-178">45.50</span><span class="sxs-lookup"><span data-stu-id="d90a7-178">45.50</span></span>     |

 

<span data-ttu-id="d90a7-179">有关详细信息，请参阅[基于“边际基数”和“计算方法”字段确定销售税比率](marginal-base-field.md)。</span><span class="sxs-lookup"><span data-stu-id="d90a7-179">For more information, see [Determining sale tax rates based on the Marginal base and Calculation method fields](marginal-base-field.md).</span></span>






