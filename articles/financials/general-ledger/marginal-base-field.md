---
title: "基于“边际基数”和“计算方法”的销售税比率"
description: "本文说明字段“边际基数”和“计算方法”中的值如何确定销售和采购交易记录的税率。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e16e91208cdd6c1a5c904fb763454371b02c71fd
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="2db43-103">基于“边际基数”和“计算方法”的销售税比率</span><span class="sxs-lookup"><span data-stu-id="2db43-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2db43-104">本文说明字段“边际基数”和“计算方法”中的值如何确定销售和采购交易记录的税率。</span><span class="sxs-lookup"><span data-stu-id="2db43-104">This article explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="2db43-105">“销售税代码”页上的“计算”快速选项卡上的“边际基数”确定哪个金额用于从“销售税代码值”页中的比率中选取相应的税率。</span><span class="sxs-lookup"><span data-stu-id="2db43-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="2db43-106">“边际基数”字段中的金额类型与“计算方法”字段中的方法组合可确定逻辑来查找交易记录的正确税率。</span><span class="sxs-lookup"><span data-stu-id="2db43-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="2db43-107">这些字段值的不同组合将产生相差非常大的增值税计算，如下面的示例所示。</span><span class="sxs-lookup"><span data-stu-id="2db43-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="2db43-108">这些示例使用相同的增值税间隔值，这些值是在“销售税代码值”页中为每个纳税代码设置的。</span><span class="sxs-lookup"><span data-stu-id="2db43-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="2db43-109">若要打开此页，请单击“销售税代码”&gt;“销售税代码中的值”页。</span><span class="sxs-lookup"><span data-stu-id="2db43-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="2db43-110">如果一个或多个销售税代码上的边际基数基于行金额或单位，则“总帐参数”页中的“计算方法”字段的值必须设置为“行”。</span><span class="sxs-lookup"><span data-stu-id="2db43-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="2db43-111">每行净额</span><span class="sxs-lookup"><span data-stu-id="2db43-111">Net amount per line</span></span>
<span data-ttu-id="2db43-112">选择此选项，以便基于发票行的净额确定销售税率，并且排除任何其他税种。</span><span class="sxs-lookup"><span data-stu-id="2db43-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="2db43-113">示例</span><span class="sxs-lookup"><span data-stu-id="2db43-113">Example</span></span>

<span data-ttu-id="2db43-114">增值税率按以下间隔设置。</span><span class="sxs-lookup"><span data-stu-id="2db43-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="2db43-115">金额间隔</span><span class="sxs-lookup"><span data-stu-id="2db43-115">Amount interval</span></span>    | <span data-ttu-id="2db43-116">税率</span><span class="sxs-lookup"><span data-stu-id="2db43-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="2db43-117">0 - 50</span><span class="sxs-lookup"><span data-stu-id="2db43-117">0 - 50</span></span>             | <span data-ttu-id="2db43-118">30%</span><span class="sxs-lookup"><span data-stu-id="2db43-118">30%</span></span>      |
| <span data-ttu-id="2db43-119">50 - 100</span><span class="sxs-lookup"><span data-stu-id="2db43-119">50 - 100</span></span>           | <span data-ttu-id="2db43-120">20%</span><span class="sxs-lookup"><span data-stu-id="2db43-120">20%</span></span>      |
| <span data-ttu-id="2db43-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="2db43-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="2db43-122">10%</span><span class="sxs-lookup"><span data-stu-id="2db43-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="2db43-123">最后间隔中的上限零 (0) 意味着超过 100 的所有金额都包括在该间隔中。</span><span class="sxs-lookup"><span data-stu-id="2db43-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="2db43-124">边际基数：**每行净额**</span><span class="sxs-lookup"><span data-stu-id="2db43-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="2db43-125">计算方法：**间隔**</span><span class="sxs-lookup"><span data-stu-id="2db43-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="2db43-126">您购买 8 个灯具，每个灯具的成本是 25.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="2db43-127">发票行的净额是 200.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="2db43-128">计算增值税的公式如下所示：</span><span class="sxs-lookup"><span data-stu-id="2db43-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="2db43-129">增值税总额 = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="2db43-130">发票总金额 = 200.00 + 35.00 = 235.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="2db43-131">**变化**</span><span class="sxs-lookup"><span data-stu-id="2db43-131">**Variation**</span></span> 

<span data-ttu-id="2db43-132">如果发票具有两行，每行四个物料，在每行上的净额是 100.00，计算销售税的公式如下所示：</span><span class="sxs-lookup"><span data-stu-id="2db43-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="2db43-133">增值税行 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="2db43-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="2db43-134">增值税行 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="2db43-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="2db43-135">总增值税 = 25.00 + 25.00 = 50.00</span><span class="sxs-lookup"><span data-stu-id="2db43-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="2db43-136">发票总金额 = 200.00 + 50.00 = 250.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="2db43-137">单位净额</span><span class="sxs-lookup"><span data-stu-id="2db43-137">Net amount per unit</span></span>
<span data-ttu-id="2db43-138">选择此选项，以便基于每个单位的值确定销售税率，并且不包括任何其他税种。</span><span class="sxs-lookup"><span data-stu-id="2db43-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="2db43-139">当基于单位的边际基数被选中时，也必须为“销售税代码”指定单位。</span><span class="sxs-lookup"><span data-stu-id="2db43-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="2db43-140">示例</span><span class="sxs-lookup"><span data-stu-id="2db43-140">Example</span></span>

<span data-ttu-id="2db43-141">增值税率按以下间隔设置。</span><span class="sxs-lookup"><span data-stu-id="2db43-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="2db43-142">本币金额</span><span class="sxs-lookup"><span data-stu-id="2db43-142">Amount</span></span>             | <span data-ttu-id="2db43-143">税率</span><span class="sxs-lookup"><span data-stu-id="2db43-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="2db43-144">0 - 50</span><span class="sxs-lookup"><span data-stu-id="2db43-144">0 - 50</span></span>             | <span data-ttu-id="2db43-145">30%</span><span class="sxs-lookup"><span data-stu-id="2db43-145">30%</span></span>      |
| <span data-ttu-id="2db43-146">50 - 100</span><span class="sxs-lookup"><span data-stu-id="2db43-146">50 - 100</span></span>           | <span data-ttu-id="2db43-147">20%</span><span class="sxs-lookup"><span data-stu-id="2db43-147">20%</span></span>      |
| <span data-ttu-id="2db43-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="2db43-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="2db43-149">10%</span><span class="sxs-lookup"><span data-stu-id="2db43-149">10%</span></span>      |

<span data-ttu-id="2db43-150">边际基数：**每单位净额**</span><span class="sxs-lookup"><span data-stu-id="2db43-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="2db43-151">计算方法：**全部金额**</span><span class="sxs-lookup"><span data-stu-id="2db43-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="2db43-152">您购买 8 个灯具，每个灯具的成本是 25.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="2db43-153">发票行的净额是 200.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="2db43-154">计算税的公式如下所示：单位销售税 = 25.00 x 30% = 7.50 总销售税 = 7.50 x 8 = 60.00 发票总金额 = 200.00 + 60.00 = 260.00</span><span class="sxs-lookup"><span data-stu-id="2db43-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="2db43-155">发票余额的净额</span><span class="sxs-lookup"><span data-stu-id="2db43-155">Net amount of invoice balance</span></span>

<span data-ttu-id="2db43-156">选择此选项，以便基于发票的总额确定销售税率，并且不包括其他税种。</span><span class="sxs-lookup"><span data-stu-id="2db43-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="2db43-157">示例</span><span class="sxs-lookup"><span data-stu-id="2db43-157">Example</span></span>

<span data-ttu-id="2db43-158">增值税率按以下间隔设置。</span><span class="sxs-lookup"><span data-stu-id="2db43-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="2db43-159">本币金额</span><span class="sxs-lookup"><span data-stu-id="2db43-159">Amount</span></span>            | <span data-ttu-id="2db43-160">税率</span><span class="sxs-lookup"><span data-stu-id="2db43-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="2db43-161">0 - 50</span><span class="sxs-lookup"><span data-stu-id="2db43-161">0 - 50</span></span>            | <span data-ttu-id="2db43-162">30%</span><span class="sxs-lookup"><span data-stu-id="2db43-162">30%</span></span>      |
| <span data-ttu-id="2db43-163">50 - 100</span><span class="sxs-lookup"><span data-stu-id="2db43-163">50 - 100</span></span>          | <span data-ttu-id="2db43-164">20%</span><span class="sxs-lookup"><span data-stu-id="2db43-164">20%</span></span>      |
| <span data-ttu-id="2db43-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="2db43-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="2db43-166">10%</span><span class="sxs-lookup"><span data-stu-id="2db43-166">10%</span></span>      |

<span data-ttu-id="2db43-167">边际基数：**发票余额的净额**</span><span class="sxs-lookup"><span data-stu-id="2db43-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="2db43-168">计算方法：**间隔** 销售发票有 2 行，每行 4 个灯具，每个灯具 25.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="2db43-169">发票余额的净额 4 x 25.00 + 4 x 25.00 = 200.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="2db43-170">计算税的公式如下所示：销售税总额 = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 发票总金额 = 200.00 + 35.00 = 235.00</span><span class="sxs-lookup"><span data-stu-id="2db43-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="2db43-171">每行总额</span><span class="sxs-lookup"><span data-stu-id="2db43-171">Gross amount per line</span></span>

<span data-ttu-id="2db43-172">选择此选项，以便基于行值确定销售税率，包括该行的所有其他税种。</span><span class="sxs-lookup"><span data-stu-id="2db43-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="2db43-173">在增值税组中，只能在“边际基数”字段中具有一个含此选择的增值税代码。</span><span class="sxs-lookup"><span data-stu-id="2db43-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="2db43-174">示例</span><span class="sxs-lookup"><span data-stu-id="2db43-174">Example</span></span>

<span data-ttu-id="2db43-175">增值税率按以下间隔设置。</span><span class="sxs-lookup"><span data-stu-id="2db43-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="2db43-176">本币金额</span><span class="sxs-lookup"><span data-stu-id="2db43-176">Amount</span></span>             | <span data-ttu-id="2db43-177">税率</span><span class="sxs-lookup"><span data-stu-id="2db43-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="2db43-178">0 - 50</span><span class="sxs-lookup"><span data-stu-id="2db43-178">0 - 50</span></span>             | <span data-ttu-id="2db43-179">30%</span><span class="sxs-lookup"><span data-stu-id="2db43-179">30%</span></span>      |
| <span data-ttu-id="2db43-180">50 - 100</span><span class="sxs-lookup"><span data-stu-id="2db43-180">50 - 100</span></span>           | <span data-ttu-id="2db43-181">20%</span><span class="sxs-lookup"><span data-stu-id="2db43-181">20%</span></span>      |
| <span data-ttu-id="2db43-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="2db43-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="2db43-183">10%</span><span class="sxs-lookup"><span data-stu-id="2db43-183">10%</span></span>      |

<span data-ttu-id="2db43-184">边际基数：**每行总额** 计算方法：**间隔** 另外每个灯具上还有为一个针对特殊税 5.00 计算的其他税码。</span><span class="sxs-lookup"><span data-stu-id="2db43-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is an other tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="2db43-185">在计算增值税之前，该特殊税将添加到净额。</span><span class="sxs-lookup"><span data-stu-id="2db43-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="2db43-186">您购买 8 个灯具，每个灯具的成本是 25.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="2db43-187">发票行的净额是 200.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="2db43-188">该发票行的总金额是 8 x 25.00 + 8 x 5.00 = 240.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="2db43-189">计算税的公式如下所示：销售税总额 = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 关税合计 = 5.00 x 8 = 40.00 发票总金额 = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="2db43-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="2db43-190">**变化**</span><span class="sxs-lookup"><span data-stu-id="2db43-190">**Variation**</span></span> 

<span data-ttu-id="2db43-191">如果发票是使用 2 个发票行（每行有 4 个物料）创建的，则每个发票行的净额是 100.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="2db43-192">每个发票行的总额（包括关税 4 x 5.00）是 120.00，并且销售税创建公式如下：销售税发票行 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 销售税发票行 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 销售税总额 = 27.00 + 27.00 = 54.00 关税合计 = 5.00 x 8 = 40.00 发票总金额 = 200.00 + 54.00 + 40.00 = 294.00</span><span class="sxs-lookup"><span data-stu-id="2db43-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="2db43-193">单位总额</span><span class="sxs-lookup"><span data-stu-id="2db43-193">Gross amount per unit</span></span>

<span data-ttu-id="2db43-194">选择此选项，以便基于单位值确定销售税率，包括任何其他税种。</span><span class="sxs-lookup"><span data-stu-id="2db43-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="2db43-195">在增值税组中，只能在“边际基数”字段中具有一个含此选择的增值税代码。</span><span class="sxs-lookup"><span data-stu-id="2db43-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="2db43-196">示例</span><span class="sxs-lookup"><span data-stu-id="2db43-196">Example</span></span>

<span data-ttu-id="2db43-197">增值税率按以下间隔设置。</span><span class="sxs-lookup"><span data-stu-id="2db43-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="2db43-198">本币金额</span><span class="sxs-lookup"><span data-stu-id="2db43-198">Amount</span></span>             | <span data-ttu-id="2db43-199">税率</span><span class="sxs-lookup"><span data-stu-id="2db43-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="2db43-200">0 - 50</span><span class="sxs-lookup"><span data-stu-id="2db43-200">0 - 50</span></span>             | <span data-ttu-id="2db43-201">30%</span><span class="sxs-lookup"><span data-stu-id="2db43-201">30%</span></span>      |
| <span data-ttu-id="2db43-202">50 - 100</span><span class="sxs-lookup"><span data-stu-id="2db43-202">50 - 100</span></span>           | <span data-ttu-id="2db43-203">20%</span><span class="sxs-lookup"><span data-stu-id="2db43-203">20%</span></span>      |
| <span data-ttu-id="2db43-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="2db43-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="2db43-205">10%</span><span class="sxs-lookup"><span data-stu-id="2db43-205">10%</span></span>      |

<span data-ttu-id="2db43-206">边际基数：**单位总额** 对于每个灯具，存在 5.00 的特殊税。</span><span class="sxs-lookup"><span data-stu-id="2db43-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="2db43-207">在计算增值税之前，该特殊税将添加到净额。</span><span class="sxs-lookup"><span data-stu-id="2db43-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="2db43-208">您购买 8 个灯具，每个灯具的成本是 25.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="2db43-209">单位总额是 30.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="2db43-210">计算税的公式如下所示：单位销售税 = 30 x 30% = 9.00 销售税总额 = 9.00 x 8 = 72.00 关税合计 = 5.00 x 8 = 40.00 发票总金额 = 200.00 + 72.00 + 40.00 = 312.00</span><span class="sxs-lookup"><span data-stu-id="2db43-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="2db43-211"> 包括其他销售税金额的发票合计</span><span class="sxs-lookup"><span data-stu-id="2db43-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="2db43-212">选择此选项，以便基于发票的总额确定销售税率，包括其他税种。</span><span class="sxs-lookup"><span data-stu-id="2db43-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="2db43-213">在增值税组中，只能在“边际基数”字段中具有一个含此选择的增值税代码</span><span class="sxs-lookup"><span data-stu-id="2db43-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="2db43-214">示例</span><span class="sxs-lookup"><span data-stu-id="2db43-214">Example</span></span>

<span data-ttu-id="2db43-215">增值税率按以下间隔设置。</span><span class="sxs-lookup"><span data-stu-id="2db43-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="2db43-216">本币金额</span><span class="sxs-lookup"><span data-stu-id="2db43-216">Amount</span></span>             | <span data-ttu-id="2db43-217">税率</span><span class="sxs-lookup"><span data-stu-id="2db43-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="2db43-218">0 - 50</span><span class="sxs-lookup"><span data-stu-id="2db43-218">0 - 50</span></span>             | <span data-ttu-id="2db43-219">30%</span><span class="sxs-lookup"><span data-stu-id="2db43-219">30%</span></span>      |
| <span data-ttu-id="2db43-220">50 - 100</span><span class="sxs-lookup"><span data-stu-id="2db43-220">50 - 100</span></span>           | <span data-ttu-id="2db43-221">20%</span><span class="sxs-lookup"><span data-stu-id="2db43-221">20%</span></span>      |
| <span data-ttu-id="2db43-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="2db43-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="2db43-223">10%</span><span class="sxs-lookup"><span data-stu-id="2db43-223">10%</span></span>      |

<span data-ttu-id="2db43-224">边际基数：**包括其他销售税金额的发票合计** 计算方法：**间隔** </span><span class="sxs-lookup"><span data-stu-id="2db43-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="2db43-225">对于每个灯具，存在 5.00 的特殊税。</span><span class="sxs-lookup"><span data-stu-id="2db43-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="2db43-226">在计算增值税之前，该特殊税将添加到净额。</span><span class="sxs-lookup"><span data-stu-id="2db43-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="2db43-227">您购买 8 个灯具，每个灯具的成本是 25.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="2db43-228">发票的净额是 200.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="2db43-229">该发票的总金额是 200.00 + (8 x 5.00) = 240.00。</span><span class="sxs-lookup"><span data-stu-id="2db43-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="2db43-230">计算税的公式如下所示：销售税总额 = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 关税合计 = 5.00 x 8 = 40.00 发票总金额 = 200.00 + 39.00 + 40.00 = 279.00</span><span class="sxs-lookup"><span data-stu-id="2db43-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="2db43-231">有关详细信息，请参阅[销售税代码销的“全部金额”和“间隔计算”选项](whole-amount-interval-options-sales-tax-codes.md)和[“来源”字段中的销售税计算方法](sales-tax-calculation-methods-origin-field.md)。</span><span class="sxs-lookup"><span data-stu-id="2db43-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>



