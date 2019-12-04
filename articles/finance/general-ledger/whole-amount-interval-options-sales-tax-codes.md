---
title: 全部金额和销售税代码的间隔计算选项
description: 本文说明销售税代码上的“计算方法”字段选项，以及如何为间隔和全部金额计算销售税。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d452ccc94324a695f0d203486fc5fa8fe9db79f6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770543"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="57e78-103">全部金额和销售税代码的间隔计算选项</span><span class="sxs-lookup"><span data-stu-id="57e78-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57e78-104">本文说明销售税代码上的“计算方法”字段选项，以及如何为间隔和全部金额计算销售税。</span><span class="sxs-lookup"><span data-stu-id="57e78-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="57e78-105">您可以设置基于整个金额或间隔金额将计算出的增值税代码。</span><span class="sxs-lookup"><span data-stu-id="57e78-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="57e78-106">在“销售税代码”页中，使用字段“计算方法”（在“计算”快速选项卡上）选择如何计算销售税代码。</span><span class="sxs-lookup"><span data-stu-id="57e78-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="57e78-107">全部金额 – 税率适用于整个应纳税金额。</span><span class="sxs-lookup"><span data-stu-id="57e78-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="57e78-108">间隔 – 应纳税金额划分为多个部分，每个部分都处于具有特定增值税税率的范围内。</span><span class="sxs-lookup"><span data-stu-id="57e78-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="57e78-109">处于给定间隔范围内的金额部分根据该间隔的税率计税。</span><span class="sxs-lookup"><span data-stu-id="57e78-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="57e78-110">该增值税是为各个金额间隔计算的税额的总和。</span><span class="sxs-lookup"><span data-stu-id="57e78-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="57e78-111">只有当您在“总帐参数”页的销售税区域中的“计算方法”字段中选择“行”时“间隔”选项才可用。</span><span class="sxs-lookup"><span data-stu-id="57e78-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="57e78-112">间隔在“销售税代码值”页通过输入每个税率的最小和最大限制金额来设置。</span><span class="sxs-lookup"><span data-stu-id="57e78-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="57e78-113">对于要对所有应纳税金额计算的税款（而与所选方法无关），间隔必须符合以下规则：</span><span class="sxs-lookup"><span data-stu-id="57e78-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="57e78-114">第一个间隔必须具有下限 0。</span><span class="sxs-lookup"><span data-stu-id="57e78-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="57e78-115">最后一个间隔必须具有上限 0，表示无穷大。</span><span class="sxs-lookup"><span data-stu-id="57e78-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="57e78-116">任何间隔的上限都必须是下一间隔的下限。</span><span class="sxs-lookup"><span data-stu-id="57e78-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="57e78-117">如果某一金额是上一个间隔的上限和下一间隔的下限，则第一个间隔的税率将适用于该金额。</span><span class="sxs-lookup"><span data-stu-id="57e78-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="57e78-118">如果某一金额处于上限和下限定义的间隔外，则增值税率 0 适用。</span><span class="sxs-lookup"><span data-stu-id="57e78-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="57e78-119">示例：计算的全部金额方法</span><span class="sxs-lookup"><span data-stu-id="57e78-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="57e78-120">在“销售税代码值”页中，以下面间隔设置增值税率：</span><span class="sxs-lookup"><span data-stu-id="57e78-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="57e78-121">**下限**</span><span class="sxs-lookup"><span data-stu-id="57e78-121">**Minimum limit**</span></span> | <span data-ttu-id="57e78-122">**上限**</span><span class="sxs-lookup"><span data-stu-id="57e78-122">**Maximum limit**</span></span> | <span data-ttu-id="57e78-123">**税率**</span><span class="sxs-lookup"><span data-stu-id="57e78-123">**Tax rate**</span></span> |
| <span data-ttu-id="57e78-124">0.00</span><span class="sxs-lookup"><span data-stu-id="57e78-124">0.00</span></span>              | <span data-ttu-id="57e78-125">50.00</span><span class="sxs-lookup"><span data-stu-id="57e78-125">50.00</span></span>             | <span data-ttu-id="57e78-126">30%</span><span class="sxs-lookup"><span data-stu-id="57e78-126">30%</span></span>          |
| <span data-ttu-id="57e78-127">50.00</span><span class="sxs-lookup"><span data-stu-id="57e78-127">50.00</span></span>             | <span data-ttu-id="57e78-128">100.00</span><span class="sxs-lookup"><span data-stu-id="57e78-128">100.00</span></span>            | <span data-ttu-id="57e78-129">20%</span><span class="sxs-lookup"><span data-stu-id="57e78-129">20%</span></span>          |
| <span data-ttu-id="57e78-130">100.00</span><span class="sxs-lookup"><span data-stu-id="57e78-130">100.00</span></span>            | <span data-ttu-id="57e78-131">0.00</span><span class="sxs-lookup"><span data-stu-id="57e78-131">0.00</span></span>              | <span data-ttu-id="57e78-132">10%</span><span class="sxs-lookup"><span data-stu-id="57e78-132">10%</span></span>          |

<span data-ttu-id="57e78-133">增值税基于总应纳税金额计算。</span><span class="sxs-lookup"><span data-stu-id="57e78-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="57e78-134">应纳税金额（价格）</span><span class="sxs-lookup"><span data-stu-id="57e78-134">Taxable amount (price)</span></span> | <span data-ttu-id="57e78-135">计算</span><span class="sxs-lookup"><span data-stu-id="57e78-135">Calculation</span></span>    | <span data-ttu-id="57e78-136">增值税</span><span class="sxs-lookup"><span data-stu-id="57e78-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="57e78-137">35.00</span><span class="sxs-lookup"><span data-stu-id="57e78-137">35.00</span></span>                  | <span data-ttu-id="57e78-138">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="57e78-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="57e78-139">10.50</span><span class="sxs-lookup"><span data-stu-id="57e78-139">10.50</span></span>     |
| <span data-ttu-id="57e78-140">50.00</span><span class="sxs-lookup"><span data-stu-id="57e78-140">50.00</span></span>                  | <span data-ttu-id="57e78-141">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="57e78-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="57e78-142">15.00</span><span class="sxs-lookup"><span data-stu-id="57e78-142">15.00</span></span>     |
| <span data-ttu-id="57e78-143">85.00</span><span class="sxs-lookup"><span data-stu-id="57e78-143">85.00</span></span>                  | <span data-ttu-id="57e78-144">85.00 \* 0.20</span><span class="sxs-lookup"><span data-stu-id="57e78-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="57e78-145">17.00</span><span class="sxs-lookup"><span data-stu-id="57e78-145">17.00</span></span>     |
| <span data-ttu-id="57e78-146">305.00</span><span class="sxs-lookup"><span data-stu-id="57e78-146">305.00</span></span>                 | <span data-ttu-id="57e78-147">305.00 \* 0.10</span><span class="sxs-lookup"><span data-stu-id="57e78-147">305.00 \* 0.10</span></span> | <span data-ttu-id="57e78-148">30.50</span><span class="sxs-lookup"><span data-stu-id="57e78-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="57e78-149">示例：计算的间隔方法</span><span class="sxs-lookup"><span data-stu-id="57e78-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="57e78-150">在“值”页中，以下面间隔设置增值税率：</span><span class="sxs-lookup"><span data-stu-id="57e78-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="57e78-151">**下限**</span><span class="sxs-lookup"><span data-stu-id="57e78-151">**Minimum limit**</span></span> | <span data-ttu-id="57e78-152">**上限**</span><span class="sxs-lookup"><span data-stu-id="57e78-152">**Maximum limit**</span></span> | <span data-ttu-id="57e78-153">**税率**</span><span class="sxs-lookup"><span data-stu-id="57e78-153">**Tax rate**</span></span> |
| <span data-ttu-id="57e78-154">0.00</span><span class="sxs-lookup"><span data-stu-id="57e78-154">0.00</span></span>              | <span data-ttu-id="57e78-155">50.00</span><span class="sxs-lookup"><span data-stu-id="57e78-155">50.00</span></span>             | <span data-ttu-id="57e78-156">30%</span><span class="sxs-lookup"><span data-stu-id="57e78-156">30%</span></span>          |
| <span data-ttu-id="57e78-157">50.00</span><span class="sxs-lookup"><span data-stu-id="57e78-157">50.00</span></span>             | <span data-ttu-id="57e78-158">100.00</span><span class="sxs-lookup"><span data-stu-id="57e78-158">100.00</span></span>            | <span data-ttu-id="57e78-159">20%</span><span class="sxs-lookup"><span data-stu-id="57e78-159">20%</span></span>          |
| <span data-ttu-id="57e78-160">100.00</span><span class="sxs-lookup"><span data-stu-id="57e78-160">100.00</span></span>            | <span data-ttu-id="57e78-161">0.00</span><span class="sxs-lookup"><span data-stu-id="57e78-161">0.00</span></span>              | <span data-ttu-id="57e78-162">10%</span><span class="sxs-lookup"><span data-stu-id="57e78-162">10%</span></span>          |

<span data-ttu-id="57e78-163">该增值税是为各个金额间隔计算的税额的总和。</span><span class="sxs-lookup"><span data-stu-id="57e78-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="57e78-164">应纳税金额（价格）</span><span class="sxs-lookup"><span data-stu-id="57e78-164">Taxable amount (price)</span></span> | <span data-ttu-id="57e78-165">计算</span><span class="sxs-lookup"><span data-stu-id="57e78-165">Calculation</span></span>                                                               | <span data-ttu-id="57e78-166">增值税</span><span class="sxs-lookup"><span data-stu-id="57e78-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="57e78-167">35.00</span><span class="sxs-lookup"><span data-stu-id="57e78-167">35.00</span></span>                  | <span data-ttu-id="57e78-168">35.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="57e78-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="57e78-169">10.50</span><span class="sxs-lookup"><span data-stu-id="57e78-169">10.50</span></span>     |
| <span data-ttu-id="57e78-170">50.00</span><span class="sxs-lookup"><span data-stu-id="57e78-170">50.00</span></span>                  | <span data-ttu-id="57e78-171">50.00 \* 0.30</span><span class="sxs-lookup"><span data-stu-id="57e78-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="57e78-172">15.00</span><span class="sxs-lookup"><span data-stu-id="57e78-172">15.00</span></span>     |
| <span data-ttu-id="57e78-173">85.00</span><span class="sxs-lookup"><span data-stu-id="57e78-173">85.00</span></span>                  | <span data-ttu-id="57e78-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span><span class="sxs-lookup"><span data-stu-id="57e78-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="57e78-175">22.00</span><span class="sxs-lookup"><span data-stu-id="57e78-175">22.00</span></span>     |
| <span data-ttu-id="57e78-176">305.00</span><span class="sxs-lookup"><span data-stu-id="57e78-176">305.00</span></span>                 | <span data-ttu-id="57e78-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span><span class="sxs-lookup"><span data-stu-id="57e78-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="57e78-178">45.50</span><span class="sxs-lookup"><span data-stu-id="57e78-178">45.50</span></span>     |



<span data-ttu-id="57e78-179">有关详细信息，请参阅[基于“边际基数”和“计算方法”的销售税比率](marginal-base-field.md)。</span><span class="sxs-lookup"><span data-stu-id="57e78-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>





