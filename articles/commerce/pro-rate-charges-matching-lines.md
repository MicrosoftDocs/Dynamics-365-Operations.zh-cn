---
title: 将抬头费用按比例分配给匹配的销售行
description: 本主题介绍通过使用高级自动费用功能为商业渠道订单计算和应用自动费用的附加功能。
author: hhaines
manager: annbe
ms.date: 04/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 5c03b1a1db11098058022a6916dc5bddf5518f9b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021785"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a><span data-ttu-id="25111-103">将抬头费用按比例分配给匹配的销售行</span><span class="sxs-lookup"><span data-stu-id="25111-103">Prorate header charges to matching sales lines</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="25111-104">本主题介绍组合抬头级别自动费用并将其按比例分配给商业销售行的功能。</span><span class="sxs-lookup"><span data-stu-id="25111-104">This topic describes the functionality for grouping header-level auto-charges and prorating them to commerce sales lines.</span></span> <span data-ttu-id="25111-105">此功能适用于在 Retail 版本 10.0.1 中销售终端 (POS) 内创建的交易记录和在 Retail 版本 10.0.2 中在呼叫中心创建的销售。</span><span class="sxs-lookup"><span data-stu-id="25111-105">This functionality is available for transactions that are created at the point of sale (POS) in Retail version 10.0.1 and sales that are created in a call center in Retail version 10.0.2.</span></span>

<span data-ttu-id="25111-106">仅当使用**商业参数**页面中的选项开启了[高级自动费用](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges)功能时，此功能才可用。</span><span class="sxs-lookup"><span data-stu-id="25111-106">This functionality is available only if the [advanced auto-charges](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) feature is turned on by using the option on the **Commerce parameters** page.</span></span> <span data-ttu-id="25111-107">此外，自动费用增强计算方法仅适用于通过商业渠道（POS、呼叫中心和 Dynamics 电子商务平台）创建的销售订单。</span><span class="sxs-lookup"><span data-stu-id="25111-107">Additionally, the enhanced calculation method for auto-charges can be applied only to sales orders that are created through commerce channels (the POS, a call center, and the Dynamics e-Commerce platform).</span></span>

<span data-ttu-id="25111-108">这项新功能可以提高组织在计算抬头级别费用并应用于销售交易记录时的灵活性。</span><span class="sxs-lookup"><span data-stu-id="25111-108">This new functionality gives organizations more flexibility in the way that header-level auto-charges are calculated and applied to sales transactions.</span></span>

<span data-ttu-id="25111-109">在版本 10.0.1 之前应用版本中，仅当存在销售订单抬头中定义的特定交货方式的匹配项时，才计算具有该交货方式关系的抬头级别自动费用。</span><span class="sxs-lookup"><span data-stu-id="25111-109">In versions the app that are earlier than version 10.0.1, header-level auto-charges that have a specific mode of delivery relation are calculated only when there is a match with the mode of delivery that is defined on the sales order header.</span></span>

<span data-ttu-id="25111-110">例如，为交货方式 **99** 和 **11** 定义了抬头级别自动费用。</span><span class="sxs-lookup"><span data-stu-id="25111-110">For example, header-level auto-charges are defined for mode of delivery **99** and mode of delivery **11**.</span></span> <span data-ttu-id="25111-111">创建了一个销售订单，并在订单抬头定义了交货方式 **99**。</span><span class="sxs-lookup"><span data-stu-id="25111-111">A sales order is created, and mode of delivery **99** is defined on the order header.</span></span> <span data-ttu-id="25111-112">但是，设置了一些销售行，以便使用交货方式 **11** 为其发货。</span><span class="sxs-lookup"><span data-stu-id="25111-112">However, some of the sale lines are set up so that they're shipped by using mode of delivery **11**.</span></span> <span data-ttu-id="25111-113">在此情况下，将仅考虑链接到交货方式 **99** 的抬头级别费用，并将这些费用应用于该销售订单。</span><span class="sxs-lookup"><span data-stu-id="25111-113">In this case, only the header-level charges that are linked to mode of delivery **99** are considered and applied to the sales order.</span></span>

<span data-ttu-id="25111-114">在 Commerce 中，抬头级别费用还有一项功能，用于定义基于订单值的[分层费用配置](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery)。</span><span class="sxs-lookup"><span data-stu-id="25111-114">In Commerce, the header-level charges have an additional feature that lets you define a [tiered charge configuration](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) that is based on the order value.</span></span> <span data-ttu-id="25111-115">例如，如果订单值介于 $50.00 与 $200.00 之间，组织可能希望收取 $5.00 的运费。</span><span class="sxs-lookup"><span data-stu-id="25111-115">For example, if the order value is between $50.00 and $200.00, an organization might want to charge a freight charge of $5.00.</span></span> <span data-ttu-id="25111-116">但是，如果订单值介于 $200.01 与 $500.00 之间，运费可能为 $4.00。</span><span class="sxs-lookup"><span data-stu-id="25111-116">However, if the order value is between $200.01 and $500.00, the freight charge might be $4.00.</span></span>

<span data-ttu-id="25111-117">某些组织可能希望享受抬头级别费用的分层费用计算优势。</span><span class="sxs-lookup"><span data-stu-id="25111-117">Some organizations want the benefits of the tiered charge calculation that is provided with header-level charges.</span></span> <span data-ttu-id="25111-118">但是，如果涉及混合交货方式，他们也希望确保基于每个销售行中定义的交货方式的匹配项计算费用。</span><span class="sxs-lookup"><span data-stu-id="25111-118">However, in scenarios that involve mixed modes of delivery, they also want to make sure that the charges that are calculated are based on a match with the mode of delivery that is defined on each sales line.</span></span>

<span data-ttu-id="25111-119">现在可以配置抬头级别自动费用，以便在计算费用时考虑订单中的所有交货方式。</span><span class="sxs-lookup"><span data-stu-id="25111-119">You can now configure header-level auto-charges so that all modes of delivery on the order are considered when charges are calculated.</span></span> <span data-ttu-id="25111-120">此功能需要更复杂的计算逻辑来计算抬头级别费用。</span><span class="sxs-lookup"><span data-stu-id="25111-120">This functionality requires a more complex calculation logic to calculate the header-level charges.</span></span> <span data-ttu-id="25111-121">该逻辑将使用同一种交货方式发货的所有项组合到一起，并在计算抬头级别自动费用时将该组视为这些项的计算组。</span><span class="sxs-lookup"><span data-stu-id="25111-121">The logic groups together all the items that are shipped by using the same mode of delivery, and it treats that group as the calculation group for the items when it calculates the header-level auto-charges.</span></span> <span data-ttu-id="25111-122">对于交货方式相同的项，将基于这些项的销售值之和计算自动费用。</span><span class="sxs-lookup"><span data-stu-id="25111-122">For items that have the same mode of delivery, auto-charges are calculated based on the combined sales value of the items.</span></span> <span data-ttu-id="25111-123">这样就可以确定正确的自动费用。</span><span class="sxs-lookup"><span data-stu-id="25111-123">In this way, the appropriate auto-charge tier is determined.</span></span>

<span data-ttu-id="25111-124">获取了使用同一种交货方式发货的销售行的正确抬头级别费用后，计算所得费用将向下按比例分配给销售行级别。</span><span class="sxs-lookup"><span data-stu-id="25111-124">After the appropriate header-level charges are obtained for the sales lines that are shipped by using the same mode of delivery, the calculated charges are prorated down to the sales line level.</span></span> <span data-ttu-id="25111-125">因为这些费用属于行级别，而不是保留在抬头级别，所以将在项和为其计算的费用值之间建立更具体的链接。</span><span class="sxs-lookup"><span data-stu-id="25111-125">Because these charges are at the line level and not kept at the header level, a more specific link is made between the item and the charge value that calculated for it.</span></span> <span data-ttu-id="25111-126">此行为在部分退货方案中可能非常有用，在这种方案中，因为只有部分项退货，所以组织希望仅退还部分费用，而不是全部费用。</span><span class="sxs-lookup"><span data-stu-id="25111-126">This behavior can be useful in partial return scenarios, where an organization wants to refund only part of the charge instead of the whole charge when only some items are returned.</span></span>

## <a name="scenarios"></a><span data-ttu-id="25111-127">方案</span><span class="sxs-lookup"><span data-stu-id="25111-127">Scenarios</span></span>

<span data-ttu-id="25111-128">下面的两个示例方案概述使用这些新功能和不使用时如何计算这些费用。</span><span class="sxs-lookup"><span data-stu-id="25111-128">The following two sample scenarios outline how these charges are calculated both when the new functionality is used and when it isn't used.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="25111-129">方案 1</span><span class="sxs-lookup"><span data-stu-id="25111-129">Scenario 1</span></span>

<span data-ttu-id="25111-130">此方案概述如果在设置自动费用时将**按比例分配给匹配的销售行**选项设置为**否**后的行为。</span><span class="sxs-lookup"><span data-stu-id="25111-130">This scenario outlines the behavior when the **Pro-rate to matching sales lines** option is set to **No** in the auto-charge setup.</span></span> <span data-ttu-id="25111-131">（此行为等于版本 10.0.1 之前应用版本中的抬头级别费用的行为。）</span><span class="sxs-lookup"><span data-stu-id="25111-131">(The behavior is equivalent to the behavior of header-level charges in app versions that are earlier than version 10.0.1.)</span></span>

<span data-ttu-id="25111-132">在此方案中，组织为交货方式关系 **99** 和 **11** 定义了抬头级别费用。</span><span class="sxs-lookup"><span data-stu-id="25111-132">In this scenario, the organization has defined header-level charges for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="25111-133">没有为交货方式 **21** 配置自动费用。</span><span class="sxs-lookup"><span data-stu-id="25111-133">No auto-charges are configured for mode of delivery **21**.</span></span>

![关闭了匹配行按比例分配时交货方式 99 的自动费用](media/99_disabled.png)

![关闭了匹配行按比例分配时交货方式 11 的自动费用](media/11_disabled.png)

<span data-ttu-id="25111-136">在呼叫中心创建一个销售订单，并将交货方式设置为 **99**。</span><span class="sxs-lookup"><span data-stu-id="25111-136">A sales order is created in the call center, and the mode of delivery is set to **99**.</span></span> <span data-ttu-id="25111-137">此订单中包含五个项。</span><span class="sxs-lookup"><span data-stu-id="25111-137">This order contains five items.</span></span> <span data-ttu-id="25111-138">已将两个订单号配置为使用交货方式 **99**，将两个行配置为使用交货方式 **11**，将一个行配置为使用交货方式 **21**，如下表中所示。</span><span class="sxs-lookup"><span data-stu-id="25111-138">Two order lines have been configured to use mode of delivery **99**, two lines have been configured to use mode of delivery **11**, and one line has been configured to use mode of delivery **21**, as shown in the following table.</span></span>

| <span data-ttu-id="25111-139">项目</span><span class="sxs-lookup"><span data-stu-id="25111-139">Item</span></span>  | <span data-ttu-id="25111-140">行数量</span><span class="sxs-lookup"><span data-stu-id="25111-140">Line quantity</span></span> | <span data-ttu-id="25111-141">传递模式</span><span class="sxs-lookup"><span data-stu-id="25111-141">Delivery mode</span></span> | <span data-ttu-id="25111-142">单位价格</span><span class="sxs-lookup"><span data-stu-id="25111-142">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="25111-143">81331</span><span class="sxs-lookup"><span data-stu-id="25111-143">81331</span></span> | <span data-ttu-id="25111-144">1</span><span class="sxs-lookup"><span data-stu-id="25111-144">1</span></span>             | <span data-ttu-id="25111-145">11</span><span class="sxs-lookup"><span data-stu-id="25111-145">11</span></span>            | <span data-ttu-id="25111-146">$10</span><span class="sxs-lookup"><span data-stu-id="25111-146">$10</span></span>            |
| <span data-ttu-id="25111-147">81332</span><span class="sxs-lookup"><span data-stu-id="25111-147">81332</span></span> | <span data-ttu-id="25111-148">1</span><span class="sxs-lookup"><span data-stu-id="25111-148">1</span></span>             | <span data-ttu-id="25111-149">99</span><span class="sxs-lookup"><span data-stu-id="25111-149">99</span></span>            | <span data-ttu-id="25111-150">$50</span><span class="sxs-lookup"><span data-stu-id="25111-150">$50</span></span>            |
| <span data-ttu-id="25111-151">81333</span><span class="sxs-lookup"><span data-stu-id="25111-151">81333</span></span> | <span data-ttu-id="25111-152">2</span><span class="sxs-lookup"><span data-stu-id="25111-152">2</span></span>             | <span data-ttu-id="25111-153">11</span><span class="sxs-lookup"><span data-stu-id="25111-153">11</span></span>            | <span data-ttu-id="25111-154">$30</span><span class="sxs-lookup"><span data-stu-id="25111-154">$30</span></span>            |
| <span data-ttu-id="25111-155">81334</span><span class="sxs-lookup"><span data-stu-id="25111-155">81334</span></span> | <span data-ttu-id="25111-156">3</span><span class="sxs-lookup"><span data-stu-id="25111-156">3</span></span>             | <span data-ttu-id="25111-157">99</span><span class="sxs-lookup"><span data-stu-id="25111-157">99</span></span>            | <span data-ttu-id="25111-158">$10</span><span class="sxs-lookup"><span data-stu-id="25111-158">$10</span></span>            |
| <span data-ttu-id="25111-159">81334</span><span class="sxs-lookup"><span data-stu-id="25111-159">81334</span></span> | <span data-ttu-id="25111-160">3</span><span class="sxs-lookup"><span data-stu-id="25111-160">3</span></span>             | <span data-ttu-id="25111-161">21</span><span class="sxs-lookup"><span data-stu-id="25111-161">21</span></span>            | <span data-ttu-id="25111-162">$5</span><span class="sxs-lookup"><span data-stu-id="25111-162">$5</span></span>             |

<span data-ttu-id="25111-163">在此方案中，将使用交货方式 **99** 针对自动费用表计算整个订单。</span><span class="sxs-lookup"><span data-stu-id="25111-163">In this scenario, the whole order is evaluated against the auto-charge table for mode of delivery **99**.</span></span> <span data-ttu-id="25111-164">将使用所有订单行的全部总计确定自动费用配置中的匹配层，并在订单抬头级别应用此费用。</span><span class="sxs-lookup"><span data-stu-id="25111-164">The full total of all sales lines is used to determine a matching tier in the auto-charge configuration, and this charge is applied at the order header level.</span></span> <span data-ttu-id="25111-165">在此示例中，订单总计为 $165.00，并为订单抬头应用 $15.00 的运费。</span><span class="sxs-lookup"><span data-stu-id="25111-165">In this example, the order total is $165.00, and the $15.00 freight charge is applied to the order header.</span></span> <span data-ttu-id="25111-166">始终不会引用或应用为交货方式 **11** 配置的自动费用。</span><span class="sxs-lookup"><span data-stu-id="25111-166">Auto-charges that are configured for mode of delivery **11** are never referenced or applied.</span></span>

<span data-ttu-id="25111-167">在此方案中，如果一个客户退还了订单中的部分项，并且[已经为了退款配置了费用代码](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2)，将把抬头级别费用总计系统性地应用于退款，即使只有部分项退货也不例外。</span><span class="sxs-lookup"><span data-stu-id="25111-167">In this scenario, if a customer returns some of the items on the order, and if the [charge code has been configured so that it will be refunded](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), the total header-level charge is systematically applied to the refund, even if only some of the items are returned.</span></span>

### <a name="scenario-2"></a><span data-ttu-id="25111-168">方案 2</span><span class="sxs-lookup"><span data-stu-id="25111-168">Scenario 2</span></span>

<span data-ttu-id="25111-169">在此方案中，为交货方式关系 **99** 和 **11** 定义了抬头级别费用。</span><span class="sxs-lookup"><span data-stu-id="25111-169">In this scenario, header-level charges are defined for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="25111-170">但是，为这些自动费用表把**按比例分配给匹配的销售行**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="25111-170">However, the **Pro-rate to matching sales lines** option is set to **Yes** for these auto-charge tables.</span></span>

![开启了匹配行按比例分配时交货方式 99 的自动费用](media/99_enabled.png)

![开启了匹配行按比例分配时交货方式 11 的自动费用](media/11_enabled.png)

<span data-ttu-id="25111-173">此方案使用同一个包含五个行的销售订单。</span><span class="sxs-lookup"><span data-stu-id="25111-173">This scenario uses the same sales order that contains five lines.</span></span> <span data-ttu-id="25111-174">订单抬头中的交货方式设置为 **99**，但是销售订单中各项的交货方式配置如下表。</span><span class="sxs-lookup"><span data-stu-id="25111-174">The mode of delivery on the order header is set to **99**, but the mode of delivery for each item on the sales order is configured as shown in the following table.</span></span>

| <span data-ttu-id="25111-175">项目</span><span class="sxs-lookup"><span data-stu-id="25111-175">Item</span></span>  | <span data-ttu-id="25111-176">行数量</span><span class="sxs-lookup"><span data-stu-id="25111-176">Line quantity</span></span> | <span data-ttu-id="25111-177">传递模式</span><span class="sxs-lookup"><span data-stu-id="25111-177">Delivery mode</span></span> | <span data-ttu-id="25111-178">单位价格</span><span class="sxs-lookup"><span data-stu-id="25111-178">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="25111-179">81331</span><span class="sxs-lookup"><span data-stu-id="25111-179">81331</span></span> | <span data-ttu-id="25111-180">1</span><span class="sxs-lookup"><span data-stu-id="25111-180">1</span></span>             | <span data-ttu-id="25111-181">11</span><span class="sxs-lookup"><span data-stu-id="25111-181">11</span></span>            | <span data-ttu-id="25111-182">$10</span><span class="sxs-lookup"><span data-stu-id="25111-182">$10</span></span>            |
| <span data-ttu-id="25111-183">81332</span><span class="sxs-lookup"><span data-stu-id="25111-183">81332</span></span> | <span data-ttu-id="25111-184">1</span><span class="sxs-lookup"><span data-stu-id="25111-184">1</span></span>             | <span data-ttu-id="25111-185">99</span><span class="sxs-lookup"><span data-stu-id="25111-185">99</span></span>            | <span data-ttu-id="25111-186">$50</span><span class="sxs-lookup"><span data-stu-id="25111-186">$50</span></span>            |
| <span data-ttu-id="25111-187">81333</span><span class="sxs-lookup"><span data-stu-id="25111-187">81333</span></span> | <span data-ttu-id="25111-188">2</span><span class="sxs-lookup"><span data-stu-id="25111-188">2</span></span>             | <span data-ttu-id="25111-189">11</span><span class="sxs-lookup"><span data-stu-id="25111-189">11</span></span>            | <span data-ttu-id="25111-190">$30</span><span class="sxs-lookup"><span data-stu-id="25111-190">$30</span></span>            |
| <span data-ttu-id="25111-191">81334</span><span class="sxs-lookup"><span data-stu-id="25111-191">81334</span></span> | <span data-ttu-id="25111-192">3</span><span class="sxs-lookup"><span data-stu-id="25111-192">3</span></span>             | <span data-ttu-id="25111-193">99</span><span class="sxs-lookup"><span data-stu-id="25111-193">99</span></span>            | <span data-ttu-id="25111-194">$10</span><span class="sxs-lookup"><span data-stu-id="25111-194">$10</span></span>            |
| <span data-ttu-id="25111-195">81334</span><span class="sxs-lookup"><span data-stu-id="25111-195">81334</span></span> | <span data-ttu-id="25111-196">3</span><span class="sxs-lookup"><span data-stu-id="25111-196">3</span></span>             | <span data-ttu-id="25111-197">21</span><span class="sxs-lookup"><span data-stu-id="25111-197">21</span></span>            | <span data-ttu-id="25111-198">$5</span><span class="sxs-lookup"><span data-stu-id="25111-198">$5</span></span>             |

<span data-ttu-id="25111-199">因为自动费用配置设置为按比例分配给匹配的销售行，所以系统执行以下计算步骤。</span><span class="sxs-lookup"><span data-stu-id="25111-199">Because the auto-charge configuration is set to prorate to matching sales lines, the system performs the following calculation steps.</span></span>

1. <span data-ttu-id="25111-200">交货方式相同的所有项组合在一起，系统将计算组中项的产品值总和。</span><span class="sxs-lookup"><span data-stu-id="25111-200">All items that have the same mode of delivery are grouped together, and the system calculates the total product value of the items in the group.</span></span>

    <span data-ttu-id="25111-201">**交货方式 11**</span><span class="sxs-lookup"><span data-stu-id="25111-201">**Delivery mode 11**</span></span>

    - <span data-ttu-id="25111-202">项 81331，数量 1 = $10</span><span class="sxs-lookup"><span data-stu-id="25111-202">Item 81331, quantity 1 = $10</span></span>
    - <span data-ttu-id="25111-203">项 81333，数量 2 = 净额 $60（每单位 $30）</span><span class="sxs-lookup"><span data-stu-id="25111-203">Item 81333, quantity 2 = $60 net ($30 per unit)</span></span>
    - <span data-ttu-id="25111-204">**交货方式 11 的产品值总和 = $70**</span><span class="sxs-lookup"><span data-stu-id="25111-204">**Total product value for delivery mode 11 = $70**</span></span>

    <span data-ttu-id="25111-205">**交货方式 99**</span><span class="sxs-lookup"><span data-stu-id="25111-205">**Delivery mode 99**</span></span>

    - <span data-ttu-id="25111-206">项 81332，数量 1 = $50</span><span class="sxs-lookup"><span data-stu-id="25111-206">Item 81332, quantity 1 = $50</span></span>
    - <span data-ttu-id="25111-207">项 81334，数量 3 = 净额 $30</span><span class="sxs-lookup"><span data-stu-id="25111-207">Item 81334, quantity 3 = $30 net</span></span>
    - <span data-ttu-id="25111-208">**交货方式 99 的产品值总和 = $80**</span><span class="sxs-lookup"><span data-stu-id="25111-208">**Total product value for delivery mode 99 = $80**</span></span>

    <span data-ttu-id="25111-209">**交货方式 21**</span><span class="sxs-lookup"><span data-stu-id="25111-209">**Delivery mode 21**</span></span>

    - <span data-ttu-id="25111-210">项 81334，数量 3 = 净额 $15</span><span class="sxs-lookup"><span data-stu-id="25111-210">Item 81334, quantity 3 = $15 net</span></span>
    - <span data-ttu-id="25111-211">**交货方式 21 的产品值总和 = $15**</span><span class="sxs-lookup"><span data-stu-id="25111-211">**Total product value for delivery mode 21 = $15**</span></span>

2. <span data-ttu-id="25111-212">系统查找与每组项的客户和交货方式设置匹配的抬头级别自动收费配置。</span><span class="sxs-lookup"><span data-stu-id="25111-212">The system looks for the configuration for header-level auto-charges that matches the customer and mode of delivery settings for each group of items.</span></span> <span data-ttu-id="25111-213">如果找到了该配置，系统将基于交货方式组中的产品值总和在分层配置中查找应该应用的费用。</span><span class="sxs-lookup"><span data-stu-id="25111-213">If the configuration is found, the system looks in the tiered configuration to find the charge that should be applied, based on the total product value of items in the mode of delivery group.</span></span>

    <span data-ttu-id="25111-214">**交货方式 11**</span><span class="sxs-lookup"><span data-stu-id="25111-214">**Delivery mode 11**</span></span>

    - <span data-ttu-id="25111-215">产品值总和 = $70</span><span class="sxs-lookup"><span data-stu-id="25111-215">Total product value = $70</span></span>
    - <span data-ttu-id="25111-216">**费用值 = $7**</span><span class="sxs-lookup"><span data-stu-id="25111-216">**Charge value = $7**</span></span>

    <span data-ttu-id="25111-217">**交货方式 99**</span><span class="sxs-lookup"><span data-stu-id="25111-217">**Delivery mode 99**</span></span>

    - <span data-ttu-id="25111-218">产品值总和 = $80</span><span class="sxs-lookup"><span data-stu-id="25111-218">Total product value = $80</span></span>
    - <span data-ttu-id="25111-219">**费用值 = $15**</span><span class="sxs-lookup"><span data-stu-id="25111-219">**Charge value = $15**</span></span>

    <span data-ttu-id="25111-220">**交货方式 21**</span><span class="sxs-lookup"><span data-stu-id="25111-220">**Delivery mode 21**</span></span>

    - <span data-ttu-id="25111-221">产品值总和 = $15</span><span class="sxs-lookup"><span data-stu-id="25111-221">Total product value = $15</span></span>
    - <span data-ttu-id="25111-222">**费用值 = $0**（尚未为客户和交货方式的此组合配置任何自动费用。）</span><span class="sxs-lookup"><span data-stu-id="25111-222">**Charge value = $0** (No auto-charges have been configured for this combination of a customer and a mode of delivery.)</span></span>

    ![交货方式 11 费用在突出显示的层中](media/step2mode11.png)

    ![交货方式 99 费用在突出显示的层中](media/step2mode99.png)

3. <span data-ttu-id="25111-225">系统基于按比例分配逻辑（这种逻辑将考虑与组的产品值总和有关的行的按比例分配值）计算将为每个行应用的费用值。</span><span class="sxs-lookup"><span data-stu-id="25111-225">The system calculates the charge value that should be applied to each line, based on proration logic that considers the proportional value of the line in relation to the group's total product value.</span></span>

    <span data-ttu-id="25111-226">**交货方式 11**</span><span class="sxs-lookup"><span data-stu-id="25111-226">**Delivery mode 11**</span></span>

    - <span data-ttu-id="25111-227">费用值 = $7</span><span class="sxs-lookup"><span data-stu-id="25111-227">Charge value = $7</span></span>
    - <span data-ttu-id="25111-228">组产品值 = $70</span><span class="sxs-lookup"><span data-stu-id="25111-228">Group product value = $70</span></span>
    - <span data-ttu-id="25111-229">行 1 值 = $10（= 组值的 14.2857%）</span><span class="sxs-lookup"><span data-stu-id="25111-229">Line 1 value = $10 (= 14.2857 percent of the group value)</span></span>
    - <span data-ttu-id="25111-230">行 3 值 = $60（= 组值的 85.7143%）</span><span class="sxs-lookup"><span data-stu-id="25111-230">Line 3 value = $60 (= 85.7143 percent of the group value)</span></span>
    - <span data-ttu-id="25111-231">**行 1 的行费用 = $1**</span><span class="sxs-lookup"><span data-stu-id="25111-231">**Line charge for line 1 = $1**</span></span>
    - <span data-ttu-id="25111-232">**行 3 的行费用 = $6**</span><span class="sxs-lookup"><span data-stu-id="25111-232">**Line charge for line 3 = $6**</span></span>

    <span data-ttu-id="25111-233">**交货方式 99**</span><span class="sxs-lookup"><span data-stu-id="25111-233">**Delivery mode 99**</span></span>

    - <span data-ttu-id="25111-234">费用值 = $15</span><span class="sxs-lookup"><span data-stu-id="25111-234">Charge value = $15</span></span>
    - <span data-ttu-id="25111-235">组产品值 = $80</span><span class="sxs-lookup"><span data-stu-id="25111-235">Group product value = $80</span></span>
    - <span data-ttu-id="25111-236">行 2 值 = $50（= 组值的 62.5%）</span><span class="sxs-lookup"><span data-stu-id="25111-236">Line 2 value = $50 (= 62.5 percent of the group value)</span></span>
    - <span data-ttu-id="25111-237">行 4 值 = $30（= 组值的 37.5%）</span><span class="sxs-lookup"><span data-stu-id="25111-237">Line 4 value = $30 (= 37.5 percent of the group value)</span></span>
    - <span data-ttu-id="25111-238">**行 2 的行费用 = $9.38**</span><span class="sxs-lookup"><span data-stu-id="25111-238">**Line charge for line 2 = $9.38**</span></span>
    - <span data-ttu-id="25111-239">**行 4 的行费用 = $5.62**</span><span class="sxs-lookup"><span data-stu-id="25111-239">**Line charge for line 4 = $5.62**</span></span>

    <span data-ttu-id="25111-240">**交货方式 21**</span><span class="sxs-lookup"><span data-stu-id="25111-240">**Delivery mode 21**</span></span>

    - <span data-ttu-id="25111-241">费用值 = $0</span><span class="sxs-lookup"><span data-stu-id="25111-241">Charge value = $0</span></span>
    - <span data-ttu-id="25111-242">组产品值 = $15</span><span class="sxs-lookup"><span data-stu-id="25111-242">Group product value = $15</span></span>
    - <span data-ttu-id="25111-243">行 5 值 = $15（= 组值的 100%）</span><span class="sxs-lookup"><span data-stu-id="25111-243">Line 5 value = $15 (= 100 percent of the group value)</span></span>
    - <span data-ttu-id="25111-244">**行 5 的行费用 = $0**</span><span class="sxs-lookup"><span data-stu-id="25111-244">**Line charge for line 5 = $0**</span></span>

<span data-ttu-id="25111-245">因此，对于此示例，将为项 81334 分配 $5.62 的运费。</span><span class="sxs-lookup"><span data-stu-id="25111-245">Therefore, for this example, item 81334 will be assigned a freight charge of $5.62.</span></span> <span data-ttu-id="25111-246">可在销售行的**维护费用**页面中查看这些费用。</span><span class="sxs-lookup"><span data-stu-id="25111-246">You can view these charges on the **Maintain charges** page for the sales line.</span></span> <span data-ttu-id="25111-247">下图显示项 81334 的此页面的显示效果。</span><span class="sxs-lookup"><span data-stu-id="25111-247">The following illustration shows what this page looks like for item 81334.</span></span>

![项 81334 的销售行的按比例分配费用](media/proratedlinecharge.png)

<span data-ttu-id="25111-249">如果在部分退货方案中使用这种计算方法，并且费用代码为可退款，则该项退货时仅为分配给该行的那部分费用退款。</span><span class="sxs-lookup"><span data-stu-id="25111-249">When this method of calculation is used in a partial return scenario, if the charge code is refundable, only the part of the charge that is allocated to that line will be refunded when the item is returned.</span></span>