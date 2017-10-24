---
title: "价格模拟"
description: "本文提供有关报价单价格模拟的信息。 价格模拟帮助您在确定特定价格前评估报价流程中将来销售价格扣除额的效果。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationPriceSimulation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 35bf73b63f0b06793df72d4cbb89675f21339127
ms.contentlocale: zh-cn
ms.lasthandoff: 09/29/2017

---

# <a name="price-simulation"></a><span data-ttu-id="96230-104">价格模拟</span><span class="sxs-lookup"><span data-stu-id="96230-104">Price simulation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="96230-105">本文提供有关报价单价格模拟的信息。</span><span class="sxs-lookup"><span data-stu-id="96230-105">This article provides information about price simulation for quotations.</span></span> <span data-ttu-id="96230-106">价格模拟帮助您在确定特定价格前评估报价流程中将来销售价格扣除额的效果。</span><span class="sxs-lookup"><span data-stu-id="96230-106">Price simulation helps you to evaluate the effect of deductions on the future sales price during the quotation process, before you commit to a specific price.</span></span>

<span data-ttu-id="96230-107">报价单的价格模拟基于建议的新价格显示新的总金额。</span><span class="sxs-lookup"><span data-stu-id="96230-107">A price simulation for a quotation shows a new total amount, based on a proposed new price.</span></span> <span data-ttu-id="96230-108">价格模拟还可以显示在现有报价单创建的特定行的新的金额。</span><span class="sxs-lookup"><span data-stu-id="96230-108">A price simulation can also show a new amount for a specific line that is created in an existing quotation.</span></span> <span data-ttu-id="96230-109">您可以输入价格模拟并在以后应用它。</span><span class="sxs-lookup"><span data-stu-id="96230-109">You can enter a price simulation and apply it later.</span></span> <span data-ttu-id="96230-110">或者，您可以使用没有价格模拟的原始报价单，并在您工作时通过与客户的销售流程进行更多更改。</span><span class="sxs-lookup"><span data-stu-id="96230-110">Alternatively, you can use the original quotation without a price simulation and make more changes as you work through the sales process with your customer.</span></span>  

<span data-ttu-id="96230-111">价格模拟并不更改报价单中的价格。</span><span class="sxs-lookup"><span data-stu-id="96230-111">A price simulation doesn't change the price in the quotation.</span></span> <span data-ttu-id="96230-112">如果价格模拟应用于整个报价单，则视作在报价单标题的特别折旧。</span><span class="sxs-lookup"><span data-stu-id="96230-112">If the price simulation is applied to a whole quotation, it’s treated as a special discount on the quotation header.</span></span> <span data-ttu-id="96230-113">如果价格模拟应用于特定的物料，则视作在报价单行的特别折旧。</span><span class="sxs-lookup"><span data-stu-id="96230-113">If the price simulation is applied to specific items, it’s treated as a special discount on the quotation lines.</span></span> <span data-ttu-id="96230-114">在应用价格模拟时，创建的报价单行的单位销售价并不更改。</span><span class="sxs-lookup"><span data-stu-id="96230-114">The unit sales price on a quotation line that is created doesn't change when a price simulation is applied.</span></span> <span data-ttu-id="96230-115">而是应用与报价单行的价格降低相对应的折扣百分比。</span><span class="sxs-lookup"><span data-stu-id="96230-115">Instead, a discount percentage that corresponds to the price reduction of the quotation line is applied.</span></span> <span data-ttu-id="96230-116">在应用价格模拟时，单位销售价和折扣百分比都转移到报价单行或报价单标题中。</span><span class="sxs-lookup"><span data-stu-id="96230-116">When a price simulation is applied, the unit sales price and the discount percentage are transferred to the quotation line or the quotation header.</span></span>  

<span data-ttu-id="96230-117">**注释：**在运行价格模拟时，只使用当前销售币种创建模拟。</span><span class="sxs-lookup"><span data-stu-id="96230-117">**Note:** When you run a price simulation, only the current sales currency is used to create the simulation.</span></span> <span data-ttu-id="96230-118">但是，在您查看报价单总计时，将会看到公司币种和销售币种的组合。</span><span class="sxs-lookup"><span data-stu-id="96230-118">However, when you view the quotation totals, you see a combination of the company currency and the sales currency.</span></span>  

<span data-ttu-id="96230-119">向报价单行添加的附属物料可能触发单行折扣或多行折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-119">Supplementary items that are added to quotation lines might trigger line discounts or multiline discounts.</span></span> <span data-ttu-id="96230-120">它们还可能触发更改报价单行的边际收益和贡献率和整个折扣的总折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-120">They might also trigger total discounts that change the contribution margins and contribution ratios of the quotation lines and the whole discount.</span></span>  

<span data-ttu-id="96230-121">您可以运行多个价格模拟，以便跟踪价格调整对报价单目标的影响。</span><span class="sxs-lookup"><span data-stu-id="96230-121">You can run multiple price simulations to track the effects of price adjustments on the targets of a quotation.</span></span> <span data-ttu-id="96230-122">通过运行这些模拟，您可以调整该报价单的整体价格或该报价单内一个或多个特定行的价格，然后应用最可能帮助成交的价格模拟。</span><span class="sxs-lookup"><span data-stu-id="96230-122">By running these simulations, you can adjust the overall price of the quotation, or the price of one or more specific lines in the quotation, and then apply the price simulation that is most likely to help you close the sale.</span></span>  

<span data-ttu-id="96230-123">您可以在创建报价单时设置一个预警。</span><span class="sxs-lookup"><span data-stu-id="96230-123">When you create a quotation, you can set up an alert.</span></span> <span data-ttu-id="96230-124">下面是使用警告的某些方式：</span><span class="sxs-lookup"><span data-stu-id="96230-124">Here are some of the ways that alerts are used:</span></span>

-   <span data-ttu-id="96230-125">他们可以保留您通知有关组织中的报价单的状态。</span><span class="sxs-lookup"><span data-stu-id="96230-125">They can keep you informed about the status of quotations in the organization.</span></span>
-   <span data-ttu-id="96230-126">它们可以触发对特定报价单的检查，或者通知您何时超出了折扣限制。</span><span class="sxs-lookup"><span data-stu-id="96230-126">They can trigger a review of a specific quotation or inform you when discount limits are exceeded.</span></span>

## <a name="price-simulation-and-discounts"></a><span data-ttu-id="96230-127">价格模拟和折扣</span><span class="sxs-lookup"><span data-stu-id="96230-127">Price simulation and discounts</span></span>
<span data-ttu-id="96230-128">为了确保折扣和价格和正确计算，在运行具有折扣的报价单的价格模拟时，请注意。</span><span class="sxs-lookup"><span data-stu-id="96230-128">To guarantee that discounts and prices are calculated correctly, be careful when you run price simulations on quotations that have discounts.</span></span> <span data-ttu-id="96230-129">因为所有价格模拟都被视作针对处于活动状态的报价单行或整个报价单的特殊折扣，您必须跟踪折扣中的差异。</span><span class="sxs-lookup"><span data-stu-id="96230-129">Because all price simulations are treated as special discounts on the active quotation line or the whole quotation, you must track the differences in the discounts.</span></span>

### <a name="types-of-discounts-in-trade-agreements"></a><span data-ttu-id="96230-130">贸易协议中的折扣类型</span><span class="sxs-lookup"><span data-stu-id="96230-130">Types of discounts in trade agreements</span></span>

<span data-ttu-id="96230-131">Microsoft Dynamics 365 for Finance and Operations 中的贸易协议可能有四种类型的价格折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-131">Trade agreements in Microsoft Dynamics 365 for Finance and Operations can have four types of price discounts.</span></span> <span data-ttu-id="96230-132">可为不同的物料、客户或价格组设置这些折扣，并且可按日期限定折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-132">These discounts can be set up for different items, customers, or price groups, and they can be limited by date.</span></span> <span data-ttu-id="96230-133">若要避免错误计算，在运行价格模拟时，您必须考虑贸易协议。</span><span class="sxs-lookup"><span data-stu-id="96230-133">To avoid miscalculations, you must consider trade agreements when you run price simulations.</span></span> <span data-ttu-id="96230-134">下面是贸易协议中的四种折扣类型：</span><span class="sxs-lookup"><span data-stu-id="96230-134">Here are the four types of discounts in trade agreements:</span></span>

-   <span data-ttu-id="96230-135">**销售价** – 可以为物料指定单独的销售价。</span><span class="sxs-lookup"><span data-stu-id="96230-135">**Sales price** – Separate sales prices can be specified for items.</span></span> <span data-ttu-id="96230-136">在创建报价单行时，程序将搜索物料的正确的销售价并将其转移到报价单行。</span><span class="sxs-lookup"><span data-stu-id="96230-136">When quotation lines are created, the program searches for the correct sales price for an item and transfers it to the quotation lines.</span></span> <span data-ttu-id="96230-137">因此，在具有类折扣的贸易协议并不影响价格模拟。</span><span class="sxs-lookup"><span data-stu-id="96230-137">Therefore, a trade agreement that has this kind of discount doesn't affect the price simulation.</span></span> <span data-ttu-id="96230-138">用于询价行的销售价反映贸易协议。</span><span class="sxs-lookup"><span data-stu-id="96230-138">The sales price that is used in the quotation line reflects the trade agreement.</span></span>
-   <span data-ttu-id="96230-139">**单行折扣** – 根据订购的金额，为物料指定特别折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-139">**Line discount** – Special discounts are specified for items, depending on the quantity that is ordered.</span></span> <span data-ttu-id="96230-140">在运行价格模拟前，通常从行金额中减去单行折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-140">Line amounts are typically reduced by the line discount before a price simulation is run.</span></span> <span data-ttu-id="96230-141">因此，在具有类折扣的贸易协议影响价格模拟。</span><span class="sxs-lookup"><span data-stu-id="96230-141">Therefore, a trade agreement that has this kind of discount affects the price simulation.</span></span>
-   <span data-ttu-id="96230-142">**多行折扣** – 如果合并的金额超出了您定义的限额，则已订购物料的预定义组合将触发对整个订单的折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-142">**Multiline discount** – If the combined quantities exceed the limit that you've defined, predefined combinations of ordered items trigger a discount on the whole order.</span></span> <span data-ttu-id="96230-143">在运行价格模拟前，通常从行金额中减去单行折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-143">Line amounts are typically reduced by the line discount before a price simulation is run.</span></span> <span data-ttu-id="96230-144">因此，在具有类折扣的贸易协议影响价格模拟。</span><span class="sxs-lookup"><span data-stu-id="96230-144">Therefore, a trade agreement that has this kind of discount affects the price simulation.</span></span>
-   <span data-ttu-id="96230-145">**总折扣** – 如果合并的金额超出了您定义的限额，则已订购物料的预定义组合将触发对整个订单的折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-145">**Total discount** – If the combined amounts exceed the limit that you've defined, predefined ordered items trigger a discount on the whole order.</span></span> <span data-ttu-id="96230-146">总折扣由报价单行生成。</span><span class="sxs-lookup"><span data-stu-id="96230-146">The total discount is generated by the quotation lines.</span></span> <span data-ttu-id="96230-147">但是，因为作为折扣应用于总折扣，则减少报价单的总金额。</span><span class="sxs-lookup"><span data-stu-id="96230-147">However, because the total discount is applied to the quotation total as a discount, it reduces the total amount of the quotation.</span></span> <span data-ttu-id="96230-148">因此，在具有类折扣的贸易协议影响价格模拟。</span><span class="sxs-lookup"><span data-stu-id="96230-148">Therefore, a trade agreement that has this kind of discount affects the price simulation.</span></span>

### <a name="quotation-lines-and-trade-agreements"></a><span data-ttu-id="96230-149">报价单行和贸易协议</span><span class="sxs-lookup"><span data-stu-id="96230-149">Quotation lines and trade agreements</span></span>

<span data-ttu-id="96230-150">在您创建或调整某一报价单行时，将自动计算行折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-150">When you create or adjust a quotation line, line discounts are automatically calculated.</span></span> <span data-ttu-id="96230-151">根据贸易协议找到物料的相关销售价。</span><span class="sxs-lookup"><span data-stu-id="96230-151">The relevant sales price is found for the item, based on the trade agreement.</span></span>

## <a name="price-simulation-examples"></a><span data-ttu-id="96230-152">价格模拟示例</span><span class="sxs-lookup"><span data-stu-id="96230-152">Price simulation examples</span></span>
<span data-ttu-id="96230-153">以下示例对于报价单标题和单个行物料使用价格模拟。</span><span class="sxs-lookup"><span data-stu-id="96230-153">The following examples use price simulation for quotation headers and single line items.</span></span>

### <a name="price-simulation-for-quotation-headers"></a><span data-ttu-id="96230-154">报价单标题的价格模拟</span><span class="sxs-lookup"><span data-stu-id="96230-154">Price simulation for quotation headers</span></span>

<span data-ttu-id="96230-155">创建具有以下行的报价单：</span><span class="sxs-lookup"><span data-stu-id="96230-155">You create a quotation that has the following lines:</span></span>

-   <span data-ttu-id="96230-156">10 个单位的物料 BR-12（单位成本价：USD 9.52，单位销售价：USD 15.32）</span><span class="sxs-lookup"><span data-stu-id="96230-156">10 units of item BR-12 (cost price per unit: USD 9.52, sales price per unit: USD 15.32)</span></span>
-   <span data-ttu-id="96230-157">12 个单位的物料 BR-14（单位成本价：USD 7.48，单位销售价：USD 13.75）</span><span class="sxs-lookup"><span data-stu-id="96230-157">12 units of item BR-14 (cost price per unit: USD 7.48, sales price per unit: USD 13.75)</span></span>

<span data-ttu-id="96230-158">下表显示报价单行。</span><span class="sxs-lookup"><span data-stu-id="96230-158">The following table shows the quotation lines.</span></span>

|                            | <span data-ttu-id="96230-159">计算</span><span class="sxs-lookup"><span data-stu-id="96230-159">Calculation</span></span>                          | <span data-ttu-id="96230-160">结果</span><span class="sxs-lookup"><span data-stu-id="96230-160">Result</span></span>   |
|----------------------------|--------------------------------------|----------|
| <span data-ttu-id="96230-161">销售数量</span><span class="sxs-lookup"><span data-stu-id="96230-161">Sales quantity</span></span>             | <span data-ttu-id="96230-162">10 个单位 + 12 个单位</span><span class="sxs-lookup"><span data-stu-id="96230-162">10 units + 12 units</span></span>                  | <span data-ttu-id="96230-163">22 个单位</span><span class="sxs-lookup"><span data-stu-id="96230-163">22 units</span></span> |
| <span data-ttu-id="96230-164">以 USD 为单位的销售价值</span><span class="sxs-lookup"><span data-stu-id="96230-164">Sales value in USD</span></span>         | <span data-ttu-id="96230-165">(10 × 15.32) + (12 × 13.75)</span><span class="sxs-lookup"><span data-stu-id="96230-165">(10 × 15.32) + (12 × 13.75)</span></span>          | <span data-ttu-id="96230-166">318.20</span><span class="sxs-lookup"><span data-stu-id="96230-166">318.20</span></span>   |
| <span data-ttu-id="96230-167">以 USD 为单位的成本价值</span><span class="sxs-lookup"><span data-stu-id="96230-167">Cost value in USD</span></span>          | <span data-ttu-id="96230-168">(10 × 9.52) + (12 × 7.48)</span><span class="sxs-lookup"><span data-stu-id="96230-168">(10 × 9.52) + (12 × 7.48)</span></span>            | <span data-ttu-id="96230-169">184.96</span><span class="sxs-lookup"><span data-stu-id="96230-169">184.96</span></span>   |
| <span data-ttu-id="96230-170">以 USD 为单位的边际收益</span><span class="sxs-lookup"><span data-stu-id="96230-170">Contribution margin in USD</span></span> | <span data-ttu-id="96230-171">318.20 – 184.96</span><span class="sxs-lookup"><span data-stu-id="96230-171">318.20 – 184.96</span></span>                      | <span data-ttu-id="96230-172">133.24</span><span class="sxs-lookup"><span data-stu-id="96230-172">133.24</span></span>   |
| <span data-ttu-id="96230-173">贡献率</span><span class="sxs-lookup"><span data-stu-id="96230-173">Contribution ratio</span></span>         | <span data-ttu-id="96230-174">(\[318.20 – 184.96\] ÷ 318.20) × 100</span><span class="sxs-lookup"><span data-stu-id="96230-174">(\[318.20 – 184.96\] ÷ 318.20) × 100</span></span> | <span data-ttu-id="96230-175">41.87%</span><span class="sxs-lookup"><span data-stu-id="96230-175">41.87%</span></span>   |

<span data-ttu-id="96230-176">运行价格模拟并且为整个报价单或报价单标题应用 15% 的总折扣。</span><span class="sxs-lookup"><span data-stu-id="96230-176">You run a price simulation and apply a 15-percent total discount for the whole quotation, or the quotation header.</span></span> <span data-ttu-id="96230-177">下表显示在价格模拟运行后的报价单的新合计。</span><span class="sxs-lookup"><span data-stu-id="96230-177">The following table shows the new totals of the quotation after the price simulation is run.</span></span>

|                                                      | <span data-ttu-id="96230-178">计算</span><span class="sxs-lookup"><span data-stu-id="96230-178">Calculation</span></span>                               | <span data-ttu-id="96230-179">结果</span><span class="sxs-lookup"><span data-stu-id="96230-179">Result</span></span>   |
|------------------------------------------------------|-------------------------------------------|----------|
| <span data-ttu-id="96230-180">销售数量</span><span class="sxs-lookup"><span data-stu-id="96230-180">Sales quantity</span></span>                                       | <span data-ttu-id="96230-181">10 个单位 + 12 个单位</span><span class="sxs-lookup"><span data-stu-id="96230-181">10 units + 12 units</span></span>                       | <span data-ttu-id="96230-182">22 个单位</span><span class="sxs-lookup"><span data-stu-id="96230-182">22 units</span></span> |
| <span data-ttu-id="96230-183">以 USD 为单位的旧销售价值</span><span class="sxs-lookup"><span data-stu-id="96230-183">Old sales value in USD</span></span>                               | <span data-ttu-id="96230-184">(10 × 15.32) + (12 × 13.75)</span><span class="sxs-lookup"><span data-stu-id="96230-184">(10 × 15.32) + (12 × 13.75)</span></span>               | <span data-ttu-id="96230-185">318.20</span><span class="sxs-lookup"><span data-stu-id="96230-185">318.20</span></span>   |
| <span data-ttu-id="96230-186">以 USD 为单位的旧成本价值</span><span class="sxs-lookup"><span data-stu-id="96230-186">Old cost value in USD</span></span>                                | <span data-ttu-id="96230-187">(10 × 9.52) + (12 × 7.48)</span><span class="sxs-lookup"><span data-stu-id="96230-187">(10 × 9.52) + (12 × 7.48)</span></span>                 | <span data-ttu-id="96230-188">184.96</span><span class="sxs-lookup"><span data-stu-id="96230-188">184.96</span></span>   |
| <span data-ttu-id="96230-189">以 USD 为单位的旧边际收益</span><span class="sxs-lookup"><span data-stu-id="96230-189">Old contribution margin in USD</span></span>                       | <span data-ttu-id="96230-190">318.20 – 184.96</span><span class="sxs-lookup"><span data-stu-id="96230-190">318.20 – 184.96</span></span>                           | <span data-ttu-id="96230-191">133.24</span><span class="sxs-lookup"><span data-stu-id="96230-191">133.24</span></span>   |
| <span data-ttu-id="96230-192">旧贡献率</span><span class="sxs-lookup"><span data-stu-id="96230-192">Old contribution ratio</span></span>                               | <span data-ttu-id="96230-193">(\[318.20 – (10 × 9.52)\] ÷ 318.20) × 100</span><span class="sxs-lookup"><span data-stu-id="96230-193">(\[318.20 – (10 × 9.52)\] ÷ 318.20) × 100</span></span> | <span data-ttu-id="96230-194">41.87%</span><span class="sxs-lookup"><span data-stu-id="96230-194">41.87%</span></span>   |
| <span data-ttu-id="96230-195">以 USD 为单位的价格模拟 15% 总折扣</span><span class="sxs-lookup"><span data-stu-id="96230-195">Price simulation of 15-percent total discount in USD</span></span> | <span data-ttu-id="96230-196">(15 × 318.2) ÷ 100</span><span class="sxs-lookup"><span data-stu-id="96230-196">(15 × 318.2) ÷ 100</span></span>                        | <span data-ttu-id="96230-197">47.73</span><span class="sxs-lookup"><span data-stu-id="96230-197">47.73</span></span>    |
| <span data-ttu-id="96230-198">以 USD 为单位的新销售价值</span><span class="sxs-lookup"><span data-stu-id="96230-198">New sales value in USD</span></span>                               | <span data-ttu-id="96230-199">318.20 – 47.73</span><span class="sxs-lookup"><span data-stu-id="96230-199">318.20 – 47.73</span></span>                            | <span data-ttu-id="96230-200">270.47</span><span class="sxs-lookup"><span data-stu-id="96230-200">270.47</span></span>   |
| <span data-ttu-id="96230-201">以 USD 为单位的新边际收益</span><span class="sxs-lookup"><span data-stu-id="96230-201">New contribution margin in USD</span></span>                       | <span data-ttu-id="96230-202">270.47 – 184.96</span><span class="sxs-lookup"><span data-stu-id="96230-202">270.47 – 184.96</span></span>                           | <span data-ttu-id="96230-203">85.51</span><span class="sxs-lookup"><span data-stu-id="96230-203">85.51</span></span>    |
| <span data-ttu-id="96230-204">新的贡献率</span><span class="sxs-lookup"><span data-stu-id="96230-204">New contribution ratio</span></span>                               | <span data-ttu-id="96230-205">\[(270.47 – 184.96) ÷ 270.47\] × 100</span><span class="sxs-lookup"><span data-stu-id="96230-205">\[(270.47 – 184.96) ÷ 270.47\] × 100</span></span>      | <span data-ttu-id="96230-206">31.61%</span><span class="sxs-lookup"><span data-stu-id="96230-206">31.61%</span></span>   |

### <a name="price-simulation-for-single-line-items"></a><span data-ttu-id="96230-207">单个行物料价格模拟</span><span class="sxs-lookup"><span data-stu-id="96230-207">Price simulation for single line items</span></span>

<span data-ttu-id="96230-208">创建具有以下行的报价单：</span><span class="sxs-lookup"><span data-stu-id="96230-208">You create a quotation that has the following lines:</span></span>

-   <span data-ttu-id="96230-209">10 个单位的物料 BR-12（单位成本价：USD 9.52，单位销售价：USD 15.32）</span><span class="sxs-lookup"><span data-stu-id="96230-209">10 units of item BR-12 (cost price per unit: USD 9.52, sales price per unit: USD 15.32)</span></span>
-   <span data-ttu-id="96230-210">12 个单位的物料 BR-14（单位成本价：USD 7.48，单位销售价：USD 13.75）</span><span class="sxs-lookup"><span data-stu-id="96230-210">12 units of item BR-14 (cost price per unit: USD 7.48, sales price per unit: USD 13.75)</span></span>

<span data-ttu-id="96230-211">下表显示报价单行。</span><span class="sxs-lookup"><span data-stu-id="96230-211">The following table shows the quotation lines.</span></span>

|                                      | <span data-ttu-id="96230-212">计算</span><span class="sxs-lookup"><span data-stu-id="96230-212">Calculation</span></span>                          | <span data-ttu-id="96230-213">结果</span><span class="sxs-lookup"><span data-stu-id="96230-213">Result</span></span>   |
|--------------------------------------|--------------------------------------|----------|
| <span data-ttu-id="96230-214">销售数量</span><span class="sxs-lookup"><span data-stu-id="96230-214">Sales quantity</span></span>                       | <span data-ttu-id="96230-215">10 个单位 + 12 个单位</span><span class="sxs-lookup"><span data-stu-id="96230-215">10 units + 12 units</span></span>                  | <span data-ttu-id="96230-216">22 个单位</span><span class="sxs-lookup"><span data-stu-id="96230-216">22 units</span></span> |
| <span data-ttu-id="96230-217">针对 BR-12 的以 USD 为单位的销售价值</span><span class="sxs-lookup"><span data-stu-id="96230-217">Sales value in USD for BR-12</span></span>         | <span data-ttu-id="96230-218">10 × 15.32</span><span class="sxs-lookup"><span data-stu-id="96230-218">10 × 15.32</span></span>                           | <span data-ttu-id="96230-219">153.20</span><span class="sxs-lookup"><span data-stu-id="96230-219">153.20</span></span>   |
| <span data-ttu-id="96230-220">针对 BR-14 的以 USD 为单位的销售价值</span><span class="sxs-lookup"><span data-stu-id="96230-220">Sales value in USD for BR-14</span></span>         | <span data-ttu-id="96230-221">12 × 13.75</span><span class="sxs-lookup"><span data-stu-id="96230-221">12 × 13.75</span></span>                           | <span data-ttu-id="96230-222">165.00</span><span class="sxs-lookup"><span data-stu-id="96230-222">165.00</span></span>   |
| <span data-ttu-id="96230-223">针对 BR-12 的以 USD 为单位的成本价值</span><span class="sxs-lookup"><span data-stu-id="96230-223">Cost value in USD for BR-12</span></span>          | <span data-ttu-id="96230-224">10 × 9.52</span><span class="sxs-lookup"><span data-stu-id="96230-224">10 × 9.52</span></span>                            | <span data-ttu-id="96230-225">95.20</span><span class="sxs-lookup"><span data-stu-id="96230-225">95.20</span></span>    |
| <span data-ttu-id="96230-226">针对 BR-14 的以 USD 为单位的成本价值</span><span class="sxs-lookup"><span data-stu-id="96230-226">Cost value in USD for BR-14</span></span>          | <span data-ttu-id="96230-227">12 × 7.48</span><span class="sxs-lookup"><span data-stu-id="96230-227">12 × 7.48</span></span>                            | <span data-ttu-id="96230-228">89.76</span><span class="sxs-lookup"><span data-stu-id="96230-228">89.76</span></span>    |
| <span data-ttu-id="96230-229">针对 BR-12 的以 USD 为单位的边际收益</span><span class="sxs-lookup"><span data-stu-id="96230-229">Contribution margin in USD for BR-12</span></span> | <span data-ttu-id="96230-230">153.20 – 95.20</span><span class="sxs-lookup"><span data-stu-id="96230-230">153.20 – 95.20</span></span>                       | <span data-ttu-id="96230-231">58.00</span><span class="sxs-lookup"><span data-stu-id="96230-231">58.00</span></span>    |
| <span data-ttu-id="96230-232">针对 BR-14 的以 USD 为单位的边际收益</span><span class="sxs-lookup"><span data-stu-id="96230-232">Contribution margin in USD for BR-14</span></span> | <span data-ttu-id="96230-233">165.00 – 89.76</span><span class="sxs-lookup"><span data-stu-id="96230-233">165.00 – 89.76</span></span>                       | <span data-ttu-id="96230-234">75.24</span><span class="sxs-lookup"><span data-stu-id="96230-234">75.24</span></span>    |
| <span data-ttu-id="96230-235">针对 BR-12 的以 USD 为单位的贡献率</span><span class="sxs-lookup"><span data-stu-id="96230-235">Contribution ratio in USD for BR-12</span></span>  | <span data-ttu-id="96230-236">\[(153.20 – 95.20) ÷ 153.20\] × 100</span><span class="sxs-lookup"><span data-stu-id="96230-236">\[(153.20 – 95.20) ÷ 153.20\] × 100</span></span>  | <span data-ttu-id="96230-237">37.86</span><span class="sxs-lookup"><span data-stu-id="96230-237">37.86</span></span>    |
| <span data-ttu-id="96230-238">针对 BR-14 的以 USD 为单位的贡献率</span><span class="sxs-lookup"><span data-stu-id="96230-238">Contribution ratio in USD for BR-14</span></span>  | <span data-ttu-id="96230-239">\[(165.00 – 89.76) ÷ 165.00\] × 100</span><span class="sxs-lookup"><span data-stu-id="96230-239">\[(165.00 – 89.76) ÷ 165.00\] × 100</span></span>  | <span data-ttu-id="96230-240">45.60</span><span class="sxs-lookup"><span data-stu-id="96230-240">45.60</span></span>    |
| <span data-ttu-id="96230-241">以 USD 为单位的总销售价值</span><span class="sxs-lookup"><span data-stu-id="96230-241">Total sales value in USD</span></span>             | <span data-ttu-id="96230-242">(10 × 15.32) + (12 × 13.75)</span><span class="sxs-lookup"><span data-stu-id="96230-242">(10 × 15.32) + (12 × 13.75)</span></span>          | <span data-ttu-id="96230-243">318.20</span><span class="sxs-lookup"><span data-stu-id="96230-243">318.20</span></span>   |
| <span data-ttu-id="96230-244">以 USD 为单位的总成本价值</span><span class="sxs-lookup"><span data-stu-id="96230-244">Total cost value in USD</span></span>              | <span data-ttu-id="96230-245">(10 × 9.52) + (12 × 7.48)</span><span class="sxs-lookup"><span data-stu-id="96230-245">(10 × 9.52) + (12 × 7.48)</span></span>            | <span data-ttu-id="96230-246">184.96</span><span class="sxs-lookup"><span data-stu-id="96230-246">184.96</span></span>   |
| <span data-ttu-id="96230-247">以 USD 为单位的总边际收益</span><span class="sxs-lookup"><span data-stu-id="96230-247">Total contribution margin in USD</span></span>     | <span data-ttu-id="96230-248">318.20 – 184.96</span><span class="sxs-lookup"><span data-stu-id="96230-248">318.20 – 184.96</span></span>                      | <span data-ttu-id="96230-249">133.24</span><span class="sxs-lookup"><span data-stu-id="96230-249">133.24</span></span>   |
| <span data-ttu-id="96230-250">总贡献率</span><span class="sxs-lookup"><span data-stu-id="96230-250">Total contribution ratio</span></span>             | <span data-ttu-id="96230-251">\[(318.20 – 184.96) ÷ 318.20\] × 100</span><span class="sxs-lookup"><span data-stu-id="96230-251">\[(318.20 – 184.96) ÷ 318.20\] × 100</span></span> | <span data-ttu-id="96230-252">41.87%</span><span class="sxs-lookup"><span data-stu-id="96230-252">41.87%</span></span>   |

<span data-ttu-id="96230-253">运行价格模拟并且应用 10 % 的总折扣至 BR-12 单位。</span><span class="sxs-lookup"><span data-stu-id="96230-253">You run a price simulation and apply a 10-percent total discount to the BR-12 units.</span></span> <span data-ttu-id="96230-254">下表显示单个行物料在价格模拟运行后的报价单的新合计。</span><span class="sxs-lookup"><span data-stu-id="96230-254">The following table shows the new totals of the quotation after the price simulation is run for the single line item.</span></span>

|                                                   | <span data-ttu-id="96230-255">计算</span><span class="sxs-lookup"><span data-stu-id="96230-255">Calculation</span></span>                             | <span data-ttu-id="96230-256">结果</span><span class="sxs-lookup"><span data-stu-id="96230-256">Result</span></span>   |
|---------------------------------------------------|-----------------------------------------|----------|
| <span data-ttu-id="96230-257">销售数量</span><span class="sxs-lookup"><span data-stu-id="96230-257">Sales quantity</span></span>                                    | <span data-ttu-id="96230-258">10 个单位 + 12 个单位</span><span class="sxs-lookup"><span data-stu-id="96230-258">10 units + 12 units</span></span>                     | <span data-ttu-id="96230-259">22 个单位</span><span class="sxs-lookup"><span data-stu-id="96230-259">22 units</span></span> |
| <span data-ttu-id="96230-260">针对 BR-12 的以 USD 为单位的旧销售价值</span><span class="sxs-lookup"><span data-stu-id="96230-260">Old sales value in USD for BR-12</span></span>                  | <span data-ttu-id="96230-261">10 × 15.32</span><span class="sxs-lookup"><span data-stu-id="96230-261">10 × 15.32</span></span>                              | <span data-ttu-id="96230-262">153.20</span><span class="sxs-lookup"><span data-stu-id="96230-262">153.20</span></span>   |
| <span data-ttu-id="96230-263">价格模拟，针对 BR-12 为 10% 折扣</span><span class="sxs-lookup"><span data-stu-id="96230-263">Price simulation of 10-percent discount for BR-12</span></span> | <span data-ttu-id="96230-264">(10 × 153.2) ÷ 100</span><span class="sxs-lookup"><span data-stu-id="96230-264">(10 × 153.2) ÷ 100</span></span>                      | <span data-ttu-id="96230-265">15.32</span><span class="sxs-lookup"><span data-stu-id="96230-265">15.32</span></span>    |
| <span data-ttu-id="96230-266">针对 BR-12 的以 USD 为单位的新销售价值</span><span class="sxs-lookup"><span data-stu-id="96230-266">New sales value in USD for BR-12</span></span>                  | <span data-ttu-id="96230-267">(10 × 15.32) – 15.32</span><span class="sxs-lookup"><span data-stu-id="96230-267">(10 × 15.32) – 15.32</span></span>                    | <span data-ttu-id="96230-268">137.88</span><span class="sxs-lookup"><span data-stu-id="96230-268">137.88</span></span>   |
| <span data-ttu-id="96230-269">针对 BR-14 的以 USD 为单位的销售价值</span><span class="sxs-lookup"><span data-stu-id="96230-269">Sales value in USD for BR-14</span></span>                      | <span data-ttu-id="96230-270">12 × 13.75</span><span class="sxs-lookup"><span data-stu-id="96230-270">12 × 13.75</span></span>                              | <span data-ttu-id="96230-271">165.00</span><span class="sxs-lookup"><span data-stu-id="96230-271">165.00</span></span>   |
| <span data-ttu-id="96230-272">针对 BR-12 的以 USD 为单位的成本价值</span><span class="sxs-lookup"><span data-stu-id="96230-272">Cost value in USD for BR-12</span></span>                       | <span data-ttu-id="96230-273">10 × 9.52</span><span class="sxs-lookup"><span data-stu-id="96230-273">10 × 9.52</span></span>                               | <span data-ttu-id="96230-274">95.20</span><span class="sxs-lookup"><span data-stu-id="96230-274">95.20</span></span>    |
| <span data-ttu-id="96230-275">针对 BR-14 的以 USD 为单位的成本价值</span><span class="sxs-lookup"><span data-stu-id="96230-275">Cost value in USD for BR-14</span></span>                       | <span data-ttu-id="96230-276">12 × 7.48</span><span class="sxs-lookup"><span data-stu-id="96230-276">12 × 7.48</span></span>                               | <span data-ttu-id="96230-277">89.76</span><span class="sxs-lookup"><span data-stu-id="96230-277">89.76</span></span>    |
| <span data-ttu-id="96230-278">针对 BR-12 的以 USD 为单位的新边际收益</span><span class="sxs-lookup"><span data-stu-id="96230-278">New contribution margin in USD for BR-12</span></span>          | <span data-ttu-id="96230-279">137.88 – 95.20</span><span class="sxs-lookup"><span data-stu-id="96230-279">137.88 – 95.20</span></span>                          | <span data-ttu-id="96230-280">42.68</span><span class="sxs-lookup"><span data-stu-id="96230-280">42.68</span></span>    |
| <span data-ttu-id="96230-281">针对 BR-14 的以 USD 为单位的边际收益</span><span class="sxs-lookup"><span data-stu-id="96230-281">Contribution margin in USD for BR-14</span></span>              | <span data-ttu-id="96230-282">165.00 – 89.76</span><span class="sxs-lookup"><span data-stu-id="96230-282">165.00 – 89.76</span></span>                          | <span data-ttu-id="96230-283">75.24</span><span class="sxs-lookup"><span data-stu-id="96230-283">75.24</span></span>    |
| <span data-ttu-id="96230-284">针对 BR-12 的以 USD 为单位的新贡献率</span><span class="sxs-lookup"><span data-stu-id="96230-284">New contribution ratio in USD for BR-12</span></span>           | <span data-ttu-id="96230-285">\[(137.88 – 95.20) ÷ 137.88\] × 100</span><span class="sxs-lookup"><span data-stu-id="96230-285">\[(137.88 – 95.20) ÷ 137.88\] × 100</span></span>     | <span data-ttu-id="96230-286">30.95</span><span class="sxs-lookup"><span data-stu-id="96230-286">30.95</span></span>    |
| <span data-ttu-id="96230-287">针对 BR-14 的以 USD 为单位的贡献率</span><span class="sxs-lookup"><span data-stu-id="96230-287">Contribution ratio in USD for BR-14</span></span>               | <span data-ttu-id="96230-288">\[(165.00 – 89.76) ÷ 165.00\] × 100</span><span class="sxs-lookup"><span data-stu-id="96230-288">\[(165.00 – 89.76) ÷ 165.00\] × 100</span></span>     | <span data-ttu-id="96230-289">45.60</span><span class="sxs-lookup"><span data-stu-id="96230-289">45.60</span></span>    |
| <span data-ttu-id="96230-290">以 USD 为单位的新的总销售价值</span><span class="sxs-lookup"><span data-stu-id="96230-290">New total sales value in USD</span></span>                      | <span data-ttu-id="96230-291">\[(10 × 15.32) – 15.32\] + (12 × 13.75)</span><span class="sxs-lookup"><span data-stu-id="96230-291">\[(10 × 15.32) – 15.32\] + (12 × 13.75)</span></span> | <span data-ttu-id="96230-292">302.88</span><span class="sxs-lookup"><span data-stu-id="96230-292">302.88</span></span>   |
| <span data-ttu-id="96230-293">以 USD 为单位的总成本价值</span><span class="sxs-lookup"><span data-stu-id="96230-293">Total cost value in USD</span></span>                           | <span data-ttu-id="96230-294">(10 × 9.52) + (12 × 7.48)</span><span class="sxs-lookup"><span data-stu-id="96230-294">(10 × 9.52) + (12 × 7.48)</span></span>               | <span data-ttu-id="96230-295">184.96</span><span class="sxs-lookup"><span data-stu-id="96230-295">184.96</span></span>   |
| <span data-ttu-id="96230-296">以 USD 为单位的新的总边际收益</span><span class="sxs-lookup"><span data-stu-id="96230-296">New total contribution margin in USD</span></span>              | <span data-ttu-id="96230-297">302.88 – 184.96</span><span class="sxs-lookup"><span data-stu-id="96230-297">302.88 – 184.96</span></span>                         | <span data-ttu-id="96230-298">117.92</span><span class="sxs-lookup"><span data-stu-id="96230-298">117.92</span></span>   |
| <span data-ttu-id="96230-299">新的总贡献率</span><span class="sxs-lookup"><span data-stu-id="96230-299">New total contribution ratio</span></span>                      | <span data-ttu-id="96230-300">\[(302.88 – 184.96) ÷ 302.88\] × 100</span><span class="sxs-lookup"><span data-stu-id="96230-300">\[(302.88 – 184.96) ÷ 302.88\] × 100</span></span>    | <span data-ttu-id="96230-301">38.93%</span><span class="sxs-lookup"><span data-stu-id="96230-301">38.93%</span></span>   |

<span data-ttu-id="96230-302">价格模拟只影响它所应用的行，并减少该行的合计。</span><span class="sxs-lookup"><span data-stu-id="96230-302">The price simulation affects only the line that it's applied to and reduces the total for that line.</span></span>



