---
title: 批次平衡
description: 此主题介绍批次平衡流程。
author: johanhoffmann
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c1f52239b2050425c37a8130507e689b29205a8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966547"
---
# <a name="batch-balancing"></a><span data-ttu-id="76125-103">批次平衡</span><span class="sxs-lookup"><span data-stu-id="76125-103">Batch balancing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76125-104">此主题介绍对批次平衡流程的支持。</span><span class="sxs-lookup"><span data-stu-id="76125-104">This topic describes how the batch balancing process is supported.</span></span>

<span data-ttu-id="76125-105">有关详细信息，请观看[有关批次平衡的视频](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be)。</span><span class="sxs-lookup"><span data-stu-id="76125-105">For more information, watch a [video on batch balancing](https://www.youtube.com/watch?v=4SNLWsU9KyI&feature=youtu.be).</span></span>

<span data-ttu-id="76125-106">在批次平衡流程中，生产批次中使用的成分量通过所选产品批次中的有效成分浓度计算。</span><span class="sxs-lookup"><span data-stu-id="76125-106">In the batch balancing process, the amount of ingredients to use in a production batch is calculated from the concentration of active ingredients in selected product batches.</span></span>

## <a name="products-that-have-an-active-ingredient"></a><span data-ttu-id="76125-107">具有有效成分的产品</span><span class="sxs-lookup"><span data-stu-id="76125-107">Products that have an active ingredient</span></span>

<span data-ttu-id="76125-108">可通过有效成分量定义产品。</span><span class="sxs-lookup"><span data-stu-id="76125-108">A product can be defined by its concentration of an active ingredient.</span></span> <span data-ttu-id="76125-109">产品有效成分的建模方法是，使用产品特定且具有最小值、最大值和目标级别的批次属性。</span><span class="sxs-lookup"><span data-stu-id="76125-109">The active ingredient of a product is modeled by using a product-specific batch attribute that has a minimum value, a maximum value, and a target level.</span></span>

<span data-ttu-id="76125-110">批次属性的目标级别表示产品中的有效成分的预计百分比。</span><span class="sxs-lookup"><span data-stu-id="76125-110">The target level of a batch attribute represents the estimated percentage of an active ingredient in a product.</span></span> <span data-ttu-id="76125-111">最小值和最大值表示接受与目标级别之间的偏差。</span><span class="sxs-lookup"><span data-stu-id="76125-111">The minimum and maximum values represent the accepted deviation from the target level.</span></span> <span data-ttu-id="76125-112">例如，可将其在收货时用作接受的批次容差。</span><span class="sxs-lookup"><span data-stu-id="76125-112">They can be used, for example, as an accepted tolerance for batches at product receipt.</span></span>

<span data-ttu-id="76125-113">一个产品只能有一种有效成分。</span><span class="sxs-lookup"><span data-stu-id="76125-113">A product can have only one active ingredient.</span></span> <span data-ttu-id="76125-114">若要指定产品的有效成分，必须首先定义产品特定的批次属性。</span><span class="sxs-lookup"><span data-stu-id="76125-114">To specify the active ingredient of a product, you must first define a product-specific batch attribute.</span></span> <span data-ttu-id="76125-115">然后将属性作为产品的基本属性关联。</span><span class="sxs-lookup"><span data-stu-id="76125-115">You then associate the attribute as a base attribute of the product.</span></span>

<span data-ttu-id="76125-116">在产品级别，还必须指定应如何记录产品批次有效成分的级别：作为采购收货流程的一部分，还是作为质检订单流程的一部分。</span><span class="sxs-lookup"><span data-stu-id="76125-116">On the product level, you must also specify how the level of the active ingredient for a batch of the product should be recorded: as part of the purchase receipt process or as part of a quality order process.</span></span>

<span data-ttu-id="76125-117">若要将基本属性与产品关联，需执行以下设置：</span><span class="sxs-lookup"><span data-stu-id="76125-117">To associate a base attribute with a product, the following setup is required:</span></span>

- <span data-ttu-id="76125-118">产品必须受批次控制。</span><span class="sxs-lookup"><span data-stu-id="76125-118">The product must be batch-controlled.</span></span> <span data-ttu-id="76125-119">若要使产品受批次控制，必须为产品分配具有有效批次维度的跟踪维度组。</span><span class="sxs-lookup"><span data-stu-id="76125-119">To make a product batch-controlled, you must assign a tracking dimension group to the product that has an active Batch dimension.</span></span>

- <span data-ttu-id="76125-120">必须将用于指示成分级别的属性定义为特定于产品的产品批次属性。</span><span class="sxs-lookup"><span data-stu-id="76125-120">The attribute that indicates the ingredient levels must be defined as a product-specific batch attribute for the product.</span></span>

<span data-ttu-id="76125-121">要查找和编辑批次有效成分的实际值：</span><span class="sxs-lookup"><span data-stu-id="76125-121">To look up and edit the actual value of the active ingredient for a batch:</span></span>
1. <span data-ttu-id="76125-122">转到 **库存管理 \> 查询和报表 \> 跟踪维度 \> 批次**。</span><span class="sxs-lookup"><span data-stu-id="76125-122">Go to **Inventory management \> Inquiries and reports \> Tracking dimensions \> Batches**.</span></span>
1. <span data-ttu-id="76125-123">从网格中选择一个批号。</span><span class="sxs-lookup"><span data-stu-id="76125-123">Select a batch number from the grid.</span></span>
1. <span data-ttu-id="76125-124">在操作窗格上，打开 **视图** 选项卡，然后选择 **库存批次属性**。</span><span class="sxs-lookup"><span data-stu-id="76125-124">On the Action Pane, open the **View** tab and then select **Inventory batch attributes**.</span></span>

## <a name="ingredient-types-and-how-they-interact-in-the-batch-balancing-process"></a><span data-ttu-id="76125-125">成分类型及其在批次平衡流程中的交互方式</span><span class="sxs-lookup"><span data-stu-id="76125-125">Ingredient types and how they interact in the batch balancing process</span></span>

<span data-ttu-id="76125-126">创建的配方行可以包含以成分类型之一：</span><span class="sxs-lookup"><span data-stu-id="76125-126">A formula line that is created can have one of these ingredient types:</span></span>

- <span data-ttu-id="76125-127">None</span><span class="sxs-lookup"><span data-stu-id="76125-127">None</span></span>
- <span data-ttu-id="76125-128">活动</span><span class="sxs-lookup"><span data-stu-id="76125-128">Active</span></span>
- <span data-ttu-id="76125-129">补偿</span><span class="sxs-lookup"><span data-stu-id="76125-129">Compensating</span></span>
- <span data-ttu-id="76125-130">填写人</span><span class="sxs-lookup"><span data-stu-id="76125-130">Filler</span></span>

<span data-ttu-id="76125-131">本节的其余部分提供了示例，用于显示各种成分类型如何工作。</span><span class="sxs-lookup"><span data-stu-id="76125-131">The rest of this section provides examples that show how each ingredient type works.</span></span> <span data-ttu-id="76125-132">这些示例基于以下配方，该配方的总批次大小为 100 升。</span><span class="sxs-lookup"><span data-stu-id="76125-132">The examples are based on the following formula that has a total batch size of 100 liters.</span></span>

| <span data-ttu-id="76125-133">成分类型</span><span class="sxs-lookup"><span data-stu-id="76125-133">Ingredient type</span></span> | <span data-ttu-id="76125-134">物料编号</span><span class="sxs-lookup"><span data-stu-id="76125-134">Item number</span></span> | <span data-ttu-id="76125-135">配方行数量</span><span class="sxs-lookup"><span data-stu-id="76125-135">Formula line quantity</span></span> | <span data-ttu-id="76125-136">单位</span><span class="sxs-lookup"><span data-stu-id="76125-136">Unit</span></span> |
|---|---|---|---|
| <span data-ttu-id="76125-137">None</span><span class="sxs-lookup"><span data-stu-id="76125-137">None</span></span> | <span data-ttu-id="76125-138">A</span><span class="sxs-lookup"><span data-stu-id="76125-138">A</span></span> | <span data-ttu-id="76125-139">20</span><span class="sxs-lookup"><span data-stu-id="76125-139">20</span></span> | <span data-ttu-id="76125-140">升</span><span class="sxs-lookup"><span data-stu-id="76125-140">Liter</span></span> |
| <span data-ttu-id="76125-141">可用</span><span class="sxs-lookup"><span data-stu-id="76125-141">Active</span></span> | <span data-ttu-id="76125-142">B</span><span class="sxs-lookup"><span data-stu-id="76125-142">B</span></span> | <span data-ttu-id="76125-143">30</span><span class="sxs-lookup"><span data-stu-id="76125-143">30</span></span> | <span data-ttu-id="76125-144">升</span><span class="sxs-lookup"><span data-stu-id="76125-144">Liter</span></span> |
| <span data-ttu-id="76125-145">补偿</span><span class="sxs-lookup"><span data-stu-id="76125-145">Compensating</span></span> | <span data-ttu-id="76125-146">C</span><span class="sxs-lookup"><span data-stu-id="76125-146">C</span></span> | <span data-ttu-id="76125-147">10</span><span class="sxs-lookup"><span data-stu-id="76125-147">10</span></span> | <span data-ttu-id="76125-148">升</span><span class="sxs-lookup"><span data-stu-id="76125-148">Liter</span></span> |
| <span data-ttu-id="76125-149">填写人</span><span class="sxs-lookup"><span data-stu-id="76125-149">Filler</span></span> | <span data-ttu-id="76125-150">日</span><span class="sxs-lookup"><span data-stu-id="76125-150">D</span></span> | <span data-ttu-id="76125-151">40</span><span class="sxs-lookup"><span data-stu-id="76125-151">40</span></span> | <span data-ttu-id="76125-152">升</span><span class="sxs-lookup"><span data-stu-id="76125-152">Liter</span></span> |

<span data-ttu-id="76125-153">下表提供了每个示例的结果的概览。</span><span class="sxs-lookup"><span data-stu-id="76125-153">The following table provides an overview of the results of each example.</span></span>

| <span data-ttu-id="76125-154">物料编号</span><span class="sxs-lookup"><span data-stu-id="76125-154">Item number</span></span> | <span data-ttu-id="76125-155">成分类型</span><span class="sxs-lookup"><span data-stu-id="76125-155">Ingredient type</span></span> | <span data-ttu-id="76125-156">估计数量</span><span class="sxs-lookup"><span data-stu-id="76125-156">Estimated quantity</span></span> | <span data-ttu-id="76125-157">结余数量</span><span class="sxs-lookup"><span data-stu-id="76125-157">Balanced quantity</span></span> | <span data-ttu-id="76125-158">有效数量</span><span class="sxs-lookup"><span data-stu-id="76125-158">Active quantity</span></span> | <span data-ttu-id="76125-159">单位</span><span class="sxs-lookup"><span data-stu-id="76125-159">Unit</span></span> | <span data-ttu-id="76125-160">基值</span><span class="sxs-lookup"><span data-stu-id="76125-160">Base value</span></span> |
|---|---|---|---|---|---|---|
| <span data-ttu-id="76125-161">A</span><span class="sxs-lookup"><span data-stu-id="76125-161">A</span></span> | <span data-ttu-id="76125-162">None</span><span class="sxs-lookup"><span data-stu-id="76125-162">None</span></span> | <span data-ttu-id="76125-163">20</span><span class="sxs-lookup"><span data-stu-id="76125-163">20</span></span> | <span data-ttu-id="76125-164">20</span><span class="sxs-lookup"><span data-stu-id="76125-164">20</span></span> | | <span data-ttu-id="76125-165">升</span><span class="sxs-lookup"><span data-stu-id="76125-165">Liter</span></span> | |
| <span data-ttu-id="76125-166">B</span><span class="sxs-lookup"><span data-stu-id="76125-166">B</span></span> | <span data-ttu-id="76125-167">活动</span><span class="sxs-lookup"><span data-stu-id="76125-167">Active</span></span> | <span data-ttu-id="76125-168">30</span><span class="sxs-lookup"><span data-stu-id="76125-168">30</span></span> | <span data-ttu-id="76125-169">25.71</span><span class="sxs-lookup"><span data-stu-id="76125-169">25.71</span></span> | <span data-ttu-id="76125-170">9.00</span><span class="sxs-lookup"><span data-stu-id="76125-170">9.00</span></span> | <span data-ttu-id="76125-171">升</span><span class="sxs-lookup"><span data-stu-id="76125-171">Liter</span></span> | <span data-ttu-id="76125-172">30.00</span><span class="sxs-lookup"><span data-stu-id="76125-172">30.00</span></span> |
| <span data-ttu-id="76125-173">C</span><span class="sxs-lookup"><span data-stu-id="76125-173">C</span></span> | <span data-ttu-id="76125-174">补偿</span><span class="sxs-lookup"><span data-stu-id="76125-174">Compensating</span></span> | <span data-ttu-id="76125-175">10</span><span class="sxs-lookup"><span data-stu-id="76125-175">10</span></span> | <span data-ttu-id="76125-176">14.72</span><span class="sxs-lookup"><span data-stu-id="76125-176">14.72</span></span> | | <span data-ttu-id="76125-177">升</span><span class="sxs-lookup"><span data-stu-id="76125-177">Liter</span></span> | |
| <span data-ttu-id="76125-178">日</span><span class="sxs-lookup"><span data-stu-id="76125-178">D</span></span> | <span data-ttu-id="76125-179">填写人</span><span class="sxs-lookup"><span data-stu-id="76125-179">Filler</span></span> | <span data-ttu-id="76125-180">40</span><span class="sxs-lookup"><span data-stu-id="76125-180">40</span></span> | <span data-ttu-id="76125-181">39.57</span><span class="sxs-lookup"><span data-stu-id="76125-181">39.57</span></span> | | <span data-ttu-id="76125-182">升</span><span class="sxs-lookup"><span data-stu-id="76125-182">Liter</span></span> | |

### <a name="active-ingredients"></a><span data-ttu-id="76125-183">有效成分</span><span class="sxs-lookup"><span data-stu-id="76125-183">Active ingredients</span></span>

<span data-ttu-id="76125-184">如果向配方行添加具有基本属性的产品，该产品在配方中将称为 *有效成分*。</span><span class="sxs-lookup"><span data-stu-id="76125-184">When a product that has a base attribute is added to a formula line, it's referred to as an *active ingredient* of the formula.</span></span> <span data-ttu-id="76125-185">可将具有包含有效成分的配方的批次订单用于批次平衡流程。</span><span class="sxs-lookup"><span data-stu-id="76125-185">Batch orders that have formulas that include active ingredients can be used for the batch balancing process.</span></span> <span data-ttu-id="76125-186">对于配方中的各成分，批次平衡流程去除生成产品所需量。</span><span class="sxs-lookup"><span data-stu-id="76125-186">For each ingredient in the formula, the batch balancing process estimates the amount that is required to produce the product.</span></span> <span data-ttu-id="76125-187">量的去除基于所选批次中的有效成分浓度。</span><span class="sxs-lookup"><span data-stu-id="76125-187">The estimate of amounts is based on the concentration of active ingredients in the selected batches.</span></span>

#### <a name="active-ingredient-example"></a><span data-ttu-id="76125-188">有效成分示例</span><span class="sxs-lookup"><span data-stu-id="76125-188">Active ingredient example</span></span>

<span data-ttu-id="76125-189">成分 B 的基本属性为 X，目标级别为 30，并且其所在的配方为每 100 升产品需要 30 升成分 B。</span><span class="sxs-lookup"><span data-stu-id="76125-189">Ingredient B has base attribute X and a target level of 30, and it's included in a formula that requires 30 liters of ingredient B for every 100 liters of the product.</span></span> <span data-ttu-id="76125-190">将创建批次大小为 100 升的批次订单。</span><span class="sxs-lookup"><span data-stu-id="76125-190">A batch order is created that has a batch size of 100 liters.</span></span> <span data-ttu-id="76125-191">将启动批次订单，而在批次平衡流程中，用户将选择含量级别为 35 的成分 B 的批次。</span><span class="sxs-lookup"><span data-stu-id="76125-191">The batch order is started, and during the batch balancing process, the user selects a batch of ingredient B that has a potency level of 35.</span></span> <span data-ttu-id="76125-192">由于含量级别 35 超过了 30 这一目标级别，所以将减少成分 B 的平衡数量，方法是含量值除以批次目标级别，然后乘以估计的数量。</span><span class="sxs-lookup"><span data-stu-id="76125-192">Because the potency level of 35 is higher than the target level of 30, the balanced quantity of ingredient B is reduced by using the ratio of the potency value to the target level of the batch, which is multiplied by the estimated quantity.</span></span> <span data-ttu-id="76125-193">下面是平衡数量的计算方法：balanced quantity looks like this:</span><span class="sxs-lookup"><span data-stu-id="76125-193">The calculation of the balanced quantity looks like this:</span></span>

<span data-ttu-id="76125-194">(30 ÷ 35) × 30 升 = 25.71 升</span><span class="sxs-lookup"><span data-stu-id="76125-194">(30 ÷ 35) × 30 liters = 25.71 liters</span></span>

### <a name="none-ingredients"></a><span data-ttu-id="76125-195">无成分</span><span class="sxs-lookup"><span data-stu-id="76125-195">None ingredients</span></span>

<span data-ttu-id="76125-196">如果在 **成分类型** 为 *无* 时应用批次平衡流程，批次订单中的配方行估计数量将与平衡数量相同。</span><span class="sxs-lookup"><span data-stu-id="76125-196">When you apply the batch balancing process when the **Ingredient type** is *None*, the estimated quantity and the balanced quantity of the formula line in the batch order are the same.</span></span>

#### <a name="none-ingredient-example"></a><span data-ttu-id="76125-197">无成分示例</span><span class="sxs-lookup"><span data-stu-id="76125-197">None ingredient example</span></span>

<span data-ttu-id="76125-198">将成分 A 分配给类型为 *无* 的成分，然后添加到成品的配方。</span><span class="sxs-lookup"><span data-stu-id="76125-198">Ingredient A is assigned to an ingredient of the *None* type and added to a formula for a finished product.</span></span> <span data-ttu-id="76125-199">此配方要求每 100 升成品需要 10 升成分 A。</span><span class="sxs-lookup"><span data-stu-id="76125-199">The formula requires 10 liters of ingredient A for every 100 liters of the finished product.</span></span> <span data-ttu-id="76125-200">如果批次订单需要 200 升，则成分 A 的估计数量和平衡数量的计算结果均应为 20 升。</span><span class="sxs-lookup"><span data-stu-id="76125-200">When a batch order requires 200 liters, both the estimated quantity and the balanced quantity of ingredient A are calculated as 20 liters.</span></span>

### <a name="compensating-ingredients"></a><span data-ttu-id="76125-201">补偿成分</span><span class="sxs-lookup"><span data-stu-id="76125-201">Compensating ingredients</span></span>

<span data-ttu-id="76125-202">补偿成分可以抵消或补偿产品中有效成分的作用。</span><span class="sxs-lookup"><span data-stu-id="76125-202">A compensating ingredient can either offset or complement the effect of the active ingredient in a product.</span></span> <span data-ttu-id="76125-203">因此，使用的补偿成分数量取决于产品的含量：</span><span class="sxs-lookup"><span data-stu-id="76125-203">Therefore, the quantity of a compensating ingredient that is consumed depends on the potency of the product:</span></span>

- <span data-ttu-id="76125-204">**抵消作用** – 如果有效成分的量超过了预期量，则必须减少补偿成分。</span><span class="sxs-lookup"><span data-stu-id="76125-204">**Opposing effect** – If the amount of the active ingredient is more than anticipated, you must add less of the compensating ingredient.</span></span>

- <span data-ttu-id="76125-205">**补偿作用** – 如果有效成分的量低于预期量，则必须增加补偿成分。</span><span class="sxs-lookup"><span data-stu-id="76125-205">**Complementary effect** – If the amount of the active ingredient is less than anticipated, you must add more of the compensating ingredient.</span></span>

<span data-ttu-id="76125-206">有效成分与补偿成分之间的关系在 **补偿原则** 页中设置。</span><span class="sxs-lookup"><span data-stu-id="76125-206">The relation between an active ingredient and a complementary ingredient is set up on the **Compensating principle** page.</span></span>

<span data-ttu-id="76125-207">请按照以下步骤设置成分之间的关系。</span><span class="sxs-lookup"><span data-stu-id="76125-207">Follow these steps to set up relations between ingredients.</span></span>

1. <span data-ttu-id="76125-208">选择 **产品信息管理 \> 物料清单和配方 \> 配方**。</span><span class="sxs-lookup"><span data-stu-id="76125-208">Select **Product information management \> Bills and materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="76125-209">打开一个配方行，然后选择 **成分** 打开 **补偿原则** 页。</span><span class="sxs-lookup"><span data-stu-id="76125-209">Open a formula line, and then select **Ingredients** to open the **Compensating principle** page.</span></span>
1. <span data-ttu-id="76125-210">选择表示补偿原则的行，然后选择要补偿的有效成分。</span><span class="sxs-lookup"><span data-stu-id="76125-210">Select the line that represents a compensating principle, and then select the active ingredient to compensate.</span></span>

<span data-ttu-id="76125-211">在补偿原则中，还输入正或负补偿系数以指定补偿量，以及原则应为抵消还是补偿。</span><span class="sxs-lookup"><span data-stu-id="76125-211">In the compensating principle, you also enter a positive or negative compensating factor to specify how much to compensate for, and whether the principle should be opposing or complementary.</span></span> <span data-ttu-id="76125-212">正系数表示补偿作用，负系数表示抵消作用。</span><span class="sxs-lookup"><span data-stu-id="76125-212">A positive factor indicates a complementary effect, and a negative factor indicates an opposing effect.</span></span>

#### <a name="compensating-ingredient-example"></a><span data-ttu-id="76125-213">补偿成分示例</span><span class="sxs-lookup"><span data-stu-id="76125-213">Compensating ingredient example</span></span>

<span data-ttu-id="76125-214">成分 B 是基本属性为 X 且目标级别为 30 的有效成分。</span><span class="sxs-lookup"><span data-stu-id="76125-214">Ingredient B is an active ingredient that has base attribute X and a target level of 30.</span></span> <span data-ttu-id="76125-215">其所在配方要求每 100 升产品需要 30 升成分 B。</span><span class="sxs-lookup"><span data-stu-id="76125-215">It's included in a formula that requires 30 liters of ingredient B for every 100 liters of the product.</span></span> <span data-ttu-id="76125-216">成分 C 是补偿成分，同一个配方中包含的数量为 10。</span><span class="sxs-lookup"><span data-stu-id="76125-216">Ingredient C is a compensating ingredient, and a quantity of 10 is included in the same formula.</span></span> <span data-ttu-id="76125-217">为补偿原则设置了补偿系数 1.10。</span><span class="sxs-lookup"><span data-stu-id="76125-217">A compensating factor of 1.10 is set up for the compensating principle.</span></span> <span data-ttu-id="76125-218">因此，平衡的补偿成分数量将减去有效成分平衡数量与估计所需数量，然后乘以 1.10。</span><span class="sxs-lookup"><span data-stu-id="76125-218">Therefore, the balanced quantity of the compensating ingredient will be reduced by the difference between the active ingredient's balanced quantity and the estimated required quantity multiplied by 1.10.</span></span>

<span data-ttu-id="76125-219">在此示例中，对于 *有效* 成分类型，所需有效成分的平衡数量计算结果为 25.71，预计所需数量计算结果为 30。</span><span class="sxs-lookup"><span data-stu-id="76125-219">In the example for the *Active* ingredient type, the balanced quantity of the required active ingredient was calculated as 25.71, and the estimated required quantity was calculated as 30.</span></span> <span data-ttu-id="76125-220">在此情况下，平衡的补偿成分数量计算方法如下：</span><span class="sxs-lookup"><span data-stu-id="76125-220">In this case, the balanced quantity of the compensating ingredient will be calculated like this:</span></span>

1. <span data-ttu-id="76125-221">确定估计数量与平衡数量之差：</span><span class="sxs-lookup"><span data-stu-id="76125-221">The difference between the estimated and the balanced quantity is determined:</span></span>  
    <span data-ttu-id="76125-222">25.71 – 30 = –4.29</span><span class="sxs-lookup"><span data-stu-id="76125-222">25.71 – 30 = –4.29</span></span>

1. <span data-ttu-id="76125-223">结果乘以补偿系数：</span><span class="sxs-lookup"><span data-stu-id="76125-223">The result is multiplied by the compensating factor:</span></span>  
    <span data-ttu-id="76125-224">4.29 × 1.10 = –4.72</span><span class="sxs-lookup"><span data-stu-id="76125-224">4.29 × 1.10 = –4.72</span></span>

1. <span data-ttu-id="76125-225">估计补偿数量减去 –4.72 以确定平衡补偿数量：</span><span class="sxs-lookup"><span data-stu-id="76125-225">The estimated compensating quantity is reduced by –4.72 to determine the balanced compensating quantity:</span></span>  
    <span data-ttu-id="76125-226">10 – (–4.72) = 14.72</span><span class="sxs-lookup"><span data-stu-id="76125-226">10 – (–4.72) = 14.72</span></span>

<span data-ttu-id="76125-227">因为 1.10 是正补偿系数，所以此补偿原则具有补偿作用。</span><span class="sxs-lookup"><span data-stu-id="76125-227">Because 1.10 is a positive compensating factor, this compensating principle has a complementary effect.</span></span> <span data-ttu-id="76125-228">在此情况下，有效成分比预期效果更强。</span><span class="sxs-lookup"><span data-stu-id="76125-228">In this case, the active ingredient is more potent than anticipated.</span></span> <span data-ttu-id="76125-229">因此，需要更多补偿成分。</span><span class="sxs-lookup"><span data-stu-id="76125-229">Therefore, more of the compensating ingredient is required.</span></span>

### <a name="filler-ingredients"></a><span data-ttu-id="76125-230">填充料成分</span><span class="sxs-lookup"><span data-stu-id="76125-230">Filler ingredients</span></span>

<span data-ttu-id="76125-231">*填充料成分* 是用于达到所需成品输出数量的中性成分。</span><span class="sxs-lookup"><span data-stu-id="76125-231">A *filler ingredient* is a neutral ingredient that is used to reach the desired output quantity of the finished product.</span></span> <span data-ttu-id="76125-232">填充料数量调节的计算方法基于有效成分和补偿成分与标准数量相比之差。</span><span class="sxs-lookup"><span data-stu-id="76125-232">Adjustments to filler quantities are calculated based on variations in the active ingredient and the compensating ingredient compared to the standard quantity.</span></span>

#### <a name="filler-ingredient-example"></a><span data-ttu-id="76125-233">填充料成分示例</span><span class="sxs-lookup"><span data-stu-id="76125-233">Filler ingredient example</span></span>

<span data-ttu-id="76125-234">您已配置了包含成分 A、B、C 和 D 的一个产品的配方，该配方的大小为 100 升。</span><span class="sxs-lookup"><span data-stu-id="76125-234">You've formulated a product that includes ingredients A, B, C, and D for a formula size of 100 liters.</span></span> <span data-ttu-id="76125-235">您计算了除一行上使用的 *填充料* 成分类型之外的其他所有成分类型的数量。</span><span class="sxs-lookup"><span data-stu-id="76125-235">You've calculated the balanced quantity of all the ingredient types except the *Filler* ingredient type that is used on one line.</span></span>
<span data-ttu-id="76125-236">填充料成分平衡数量的计算结果是批次大小 100 升减去成分 A、B 和 C 之和：</span><span class="sxs-lookup"><span data-stu-id="76125-236">The balanced quantity of the filler ingredient is calculated as the difference between the batch size of 100 liters and the sum of ingredients A, B, and C:</span></span>

<span data-ttu-id="76125-237">100 – (20 + 25.71 + 14.72) = 39.57</span><span class="sxs-lookup"><span data-stu-id="76125-237">100 – (20 + 25.71 + 14.72) = 39.57</span></span>

## <a name="the-batch-balancing-process"></a><span data-ttu-id="76125-238">批次平衡流程</span><span class="sxs-lookup"><span data-stu-id="76125-238">The batch balancing process</span></span>

<span data-ttu-id="76125-239">批次平衡流程从 **批次平衡** 页执行。</span><span class="sxs-lookup"><span data-stu-id="76125-239">The batch balancing process is performed from the **Batch balancing** page.</span></span>
<span data-ttu-id="76125-240">选择 **成本管理 \> 批次订单**，然后在 **流程** 选项卡上，选择 **批次平衡**。</span><span class="sxs-lookup"><span data-stu-id="76125-240">Select **Cost management \> Batch orders**, and then, on the **Process** tab, select **Batch balancing**.</span></span> <span data-ttu-id="76125-241">批次平衡可用于状态为 **已开始** 的批次订单。</span><span class="sxs-lookup"><span data-stu-id="76125-241">Batch balancing is available for batch orders that have a status of **Started**.</span></span>

<span data-ttu-id="76125-242">一般而言，如果配方至少有一个配方行中的 **成分类型** 为 *有效*，则可为批次订单应用批次平衡。</span><span class="sxs-lookup"><span data-stu-id="76125-242">In general, batch balancing can be applied to batch orders if the formula has at least one formula line where the **Ingredient type** is *Active*.</span></span> <span data-ttu-id="76125-243">（有关此规则的例外，请参阅此主题后文的“不适用批次平衡的批次订单”章节。）</span><span class="sxs-lookup"><span data-stu-id="76125-243">(For the exception to this rule, see the "Batch orders that aren't applicable for batch balancing" section later in this topic.)</span></span>

<span data-ttu-id="76125-244">批次平衡流程可分为两个子流程：</span><span class="sxs-lookup"><span data-stu-id="76125-244">The batch balancing process can be divided into two subprocesses:</span></span>

1. <span data-ttu-id="76125-245">平衡批次成分</span><span class="sxs-lookup"><span data-stu-id="76125-245">Balance batch ingredients</span></span>
1. <span data-ttu-id="76125-246">确认和下达配方</span><span class="sxs-lookup"><span data-stu-id="76125-246">Confirm and release the formula</span></span>

### <a name="balance-batch-ingredients"></a><span data-ttu-id="76125-247">平衡批次成分</span><span class="sxs-lookup"><span data-stu-id="76125-247">Balance batch ingredients</span></span>

<span data-ttu-id="76125-248">在平衡批次成分子流程中，生产批次使用的成分量基于具有有效成分的所选批次计算。</span><span class="sxs-lookup"><span data-stu-id="76125-248">In the Balance batch ingredients subprocess, the amount of ingredients to use for the production batch is calculated based on the selected batches that have active ingredients.</span></span> <span data-ttu-id="76125-249">通常，只有涵盖所有成分，才能完成计算。</span><span class="sxs-lookup"><span data-stu-id="76125-249">As a rule, the calculation can be completed only if there is full coverage of all ingredients.</span></span> <span data-ttu-id="76125-250">不能仅平衡将批次订单设置为生产的批次部分。</span><span class="sxs-lookup"><span data-stu-id="76125-250">You can't balance only part of the batch that the batch order is set up to produce.</span></span>

> [!NOTE]
> <span data-ttu-id="76125-251">不能先保存计算，以后再完成批次平衡流程。</span><span class="sxs-lookup"><span data-stu-id="76125-251">You can't save a calculation and then complete the batch balancing process later.</span></span> <span data-ttu-id="76125-252">如果关闭 **批次平衡** 页，则必须重新计算才能完成流程。</span><span class="sxs-lookup"><span data-stu-id="76125-252">If you close the **Batch balancing** page, you must repeat the calculation to complete the process.</span></span>

### <a name="confirm-and-release-the-formula"></a><span data-ttu-id="76125-253">确认和下达配方</span><span class="sxs-lookup"><span data-stu-id="76125-253">Confirm and release the formula</span></span>

<span data-ttu-id="76125-254">计算了成分数量之后，可以确认并下达配方。</span><span class="sxs-lookup"><span data-stu-id="76125-254">After the ingredient quantities have been calculated, you can confirm and release the formula.</span></span> <span data-ttu-id="76125-255">下达流程各不相同，具体取决于是否为仓库管理流程启用了产品：</span><span class="sxs-lookup"><span data-stu-id="76125-255">The release process differs, depending on whether the products are enabled for the warehouse management processes:</span></span>

- <span data-ttu-id="76125-256">如果为仓库管理流程启用了某个产品，将根据仓库管理流程的原则把配方行下达给仓库。</span><span class="sxs-lookup"><span data-stu-id="76125-256">If a product is enabled for the warehouse management processes, the formula line is released to the warehouse according to the principles for the warehouse management processes.</span></span> <span data-ttu-id="76125-257">配方行按照匹配平衡数量的数量下达，并针对为有效成分选择的特定批次下达。</span><span class="sxs-lookup"><span data-stu-id="76125-257">The formula line is released in quantities that match the balanced quantities, and it's released for the specific batches that are selected for the active ingredients.</span></span>

    > [!NOTE]
    > <span data-ttu-id="76125-258">配方行只能作为批次平衡流程的一部分下达给仓库。</span><span class="sxs-lookup"><span data-stu-id="76125-258">Formula lines can be released to warehouse only as part of the batch balancing process.</span></span> <span data-ttu-id="76125-259">尽管可通过其他选项将生产物料下达给仓库，但是那些选项不能用于配方行。</span><span class="sxs-lookup"><span data-stu-id="76125-259">Although there are other options for releasing materials for production to warehouse, those options can't be used for formula lines.</span></span>

- <span data-ttu-id="76125-260">如果不为仓库管理流程启用产品，确认并下达配方时，将为产品创建生产领料单。</span><span class="sxs-lookup"><span data-stu-id="76125-260">If a product isn't enabled for the warehouse management processes, a production picking list is created for the product when you confirm and release the formula.</span></span>

<span data-ttu-id="76125-261">在单个配方中，可合并为仓库管理流程启用的产品和未为仓库管理流程启用的产品。</span><span class="sxs-lookup"><span data-stu-id="76125-261">In a single formula, you can combine products that are enabled for the warehouse management processes and products that aren't enabled for the warehouse management processes.</span></span> <span data-ttu-id="76125-262">如果一个配方中同时包含这两种产品，将把为仓库管理流程启用的产品下达给仓库。</span><span class="sxs-lookup"><span data-stu-id="76125-262">When the two types of products are included in one formula, the products that are enabled for the warehouse management processes are released to warehouse.</span></span> <span data-ttu-id="76125-263">对于未为仓库管理流程启用的产品，将在确认并下达配方时创建领料单。</span><span class="sxs-lookup"><span data-stu-id="76125-263">For the products that aren't enabled for the warehouse management processes, a picking list is created when the formula is confirmed and released.</span></span>

### <a name="batch-orders-that-arent-applicable-for-batch-balancing"></a><span data-ttu-id="76125-264">不适用批次平衡的批次订单</span><span class="sxs-lookup"><span data-stu-id="76125-264">Batch orders that aren't applicable for batch balancing</span></span>

<span data-ttu-id="76125-265">以下规则有两个例外：如果配方至少有一个配方行中的 **成分类型** 为 *有效*，则批次订单适用批次平衡。</span><span class="sxs-lookup"><span data-stu-id="76125-265">There are two exceptions to the rule that batch orders are applicable for batch balancing if the formula has at least one formula line where the **Ingredient type** is *Active*.</span></span>

1. <span data-ttu-id="76125-266">如果配方中包含为仓库管理流程启用的产品的有效成分，但批次号低于预留层次结构中的位置，则批次订单不适用批次平衡。</span><span class="sxs-lookup"><span data-stu-id="76125-266">If a formula contains an active ingredient for a product that is enabled for the warehouse management processes, but batch number is below location in the reservation hierarchy, the batch order isn't applicable for batch balancing.</span></span>
1. <span data-ttu-id="76125-267">如果配方度量单位与有效成分的库存度量单位不同，批次订单则不适用于批次平衡。</span><span class="sxs-lookup"><span data-stu-id="76125-267">If the formula unit of measure is different from the inventory unit of measure of the active ingredient, the batch order isn't applicable for batch balancing.</span></span>

<span data-ttu-id="76125-268">不适用批次平衡的批次订单将完成批次订单的常规流程周期。</span><span class="sxs-lookup"><span data-stu-id="76125-268">A batch order that isn't applicable for batch balancing goes through the regular process cycle for batch orders.</span></span>
