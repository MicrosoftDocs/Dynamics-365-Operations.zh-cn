---
title: 补货方法和数量修改
description: 本主题提供有关计划优化中的补货方法的信息。 它还说明了产品的多个订单数量如何影响结果。
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261688"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="e6c13-104">补货方法和数量修改</span><span class="sxs-lookup"><span data-stu-id="e6c13-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6c13-105">本主题提供有关计划优化中的补货方法的信息。</span><span class="sxs-lookup"><span data-stu-id="e6c13-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="e6c13-106">它还说明了产品的多个订单数量如何影响结果。</span><span class="sxs-lookup"><span data-stu-id="e6c13-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="e6c13-107">补货方法也称为覆盖范围方法和批次规模方法。</span><span class="sxs-lookup"><span data-stu-id="e6c13-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="e6c13-108">覆盖范围代码</span><span class="sxs-lookup"><span data-stu-id="e6c13-108">Coverage codes</span></span>

<span data-ttu-id="e6c13-109">计划优化可以配置为使用不同的补货方法。</span><span class="sxs-lookup"><span data-stu-id="e6c13-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="e6c13-110">补货方法是系统用于计算产品需求的技术。</span><span class="sxs-lookup"><span data-stu-id="e6c13-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="e6c13-111">补货方法由您可以在覆盖范围组或产品上设置的覆盖范围代码定义。</span><span class="sxs-lookup"><span data-stu-id="e6c13-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="e6c13-112">以下覆盖范围代码可用于计划优化：</span><span class="sxs-lookup"><span data-stu-id="e6c13-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="e6c13-113">**期间** – 将一个期间的所有需求合并为产品的一个订单的补货方法。</span><span class="sxs-lookup"><span data-stu-id="e6c13-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="e6c13-114">将针对期间的第一天计划订单，其数量将在确定的期间内满足净需求。</span><span class="sxs-lookup"><span data-stu-id="e6c13-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="e6c13-115">期间从产品的第一个需求开始，并覆盖定义的时间长度。</span><span class="sxs-lookup"><span data-stu-id="e6c13-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="e6c13-116">下一个期间将从产品的下一个需求开始。</span><span class="sxs-lookup"><span data-stu-id="e6c13-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="e6c13-117">*期间* 覆盖范围代码通常用于不可预测的库存签发、受季节影响的产品或高成本产品。</span><span class="sxs-lookup"><span data-stu-id="e6c13-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="e6c13-118">下图显示了一个示例。</span><span class="sxs-lookup"><span data-stu-id="e6c13-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="e6c13-119">![期间覆盖范围代码使用的示例](./media/coverage-code-period.png "期间覆盖范围代码使用的示例")</span><span class="sxs-lookup"><span data-stu-id="e6c13-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="e6c13-120">**补货** – 在补货方法中，系统根据需求为产品创建计划采购订单、转移单或生产订单。</span><span class="sxs-lookup"><span data-stu-id="e6c13-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="e6c13-121">此方法用于具有间歇性需求的昂贵产品。</span><span class="sxs-lookup"><span data-stu-id="e6c13-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="e6c13-122">*需求* 覆盖范围代码通常用于可配置产品或按订单生产场景。</span><span class="sxs-lookup"><span data-stu-id="e6c13-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="e6c13-123">下图显示了一个示例。</span><span class="sxs-lookup"><span data-stu-id="e6c13-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="e6c13-124">![需求覆盖范围代码使用的示例](./media/coverage-code-requirement.png "需求覆盖范围代码使用的示例")</span><span class="sxs-lookup"><span data-stu-id="e6c13-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="e6c13-125">**最小值/最大值**</span><span class="sxs-lookup"><span data-stu-id="e6c13-125">**Min./Max.**</span></span> <span data-ttu-id="e6c13-126">– 补货方法基于库存级别。</span><span class="sxs-lookup"><span data-stu-id="e6c13-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="e6c13-127">当预测的现有量级别低于特定阈值时，它将库存补货定义到特定级别。</span><span class="sxs-lookup"><span data-stu-id="e6c13-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="e6c13-128">补货数量将是最大级别与预计现有量级别之间的差值。</span><span class="sxs-lookup"><span data-stu-id="e6c13-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="e6c13-129">*最小值/最大值*</span><span class="sxs-lookup"><span data-stu-id="e6c13-129">The *Min./Max.*</span></span> <span data-ttu-id="e6c13-130">覆盖范围代码通常用于可预测的库存签发、高运行器或较便宜的产品。</span><span class="sxs-lookup"><span data-stu-id="e6c13-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="e6c13-131">下图显示了一个示例。</span><span class="sxs-lookup"><span data-stu-id="e6c13-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="e6c13-132">![最小值/最大值覆盖范围代码使用的示例](./media/coverage-code-min-max.png "最小值/最大值覆盖范围代码使用的示例")</span><span class="sxs-lookup"><span data-stu-id="e6c13-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="e6c13-133">**手动** – 在补货方法中，系统不为产品建议采购订单、转移单或生产订单。</span><span class="sxs-lookup"><span data-stu-id="e6c13-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="e6c13-134">相反，产品的计划员负责为产品补货创建所需的订单。</span><span class="sxs-lookup"><span data-stu-id="e6c13-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="e6c13-135">*手动* 覆盖范围代码通常用于不需要系统生成的计划订单的产品。</span><span class="sxs-lookup"><span data-stu-id="e6c13-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="e6c13-136">默认订单设置对订单数量的影响</span><span class="sxs-lookup"><span data-stu-id="e6c13-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="e6c13-137">在已发放产品的 **默认订单设置** 页面上，您可以在 **采购订单**、**库存** 和 **销售订单** 快速选项卡上指定以下每个数量设置。</span><span class="sxs-lookup"><span data-stu-id="e6c13-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="e6c13-138">（**库存** 快速选项卡用于转移单和生产订单。）</span><span class="sxs-lookup"><span data-stu-id="e6c13-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="e6c13-139">**倍数** – 计划订单将是该数量的倍数。</span><span class="sxs-lookup"><span data-stu-id="e6c13-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="e6c13-140">例如，如果 **倍数** 字段设置为 *5*，订单的数量可以是 5、10、15、20 等。</span><span class="sxs-lookup"><span data-stu-id="e6c13-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="e6c13-141">**最小订单数量** – 计划订单不会小于指定值。</span><span class="sxs-lookup"><span data-stu-id="e6c13-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="e6c13-142">例如，如果 **最小订单数量** 字段设置为 *10*，将创建数量为 10 的计划订单，即使只需要四个即可满足需求。</span><span class="sxs-lookup"><span data-stu-id="e6c13-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="e6c13-143">**最大订单数量** – 计划订单不会超过指定值。</span><span class="sxs-lookup"><span data-stu-id="e6c13-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="e6c13-144">如果需求超过 **最大订单数量** 值，将创建多个计划订单来覆盖它。</span><span class="sxs-lookup"><span data-stu-id="e6c13-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="e6c13-145">例如，如果 **最大订单数量** 字段设置为 *100*，并且需求为 450，将创建四个数量为 100 个计划订单和一个数量为 50 的计划订单。</span><span class="sxs-lookup"><span data-stu-id="e6c13-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="e6c13-146">使用最小值/最大值的补货的示例</span><span class="sxs-lookup"><span data-stu-id="e6c13-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="e6c13-147">覆盖范围代码</span><span class="sxs-lookup"><span data-stu-id="e6c13-147">coverage code</span></span>

<span data-ttu-id="e6c13-148">如果您没有在 **默认订单设置** 页面上为产品指定 **倍数** 字段中的值，并且如果您使用的是 *最小值/最大值*</span><span class="sxs-lookup"><span data-stu-id="e6c13-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="e6c13-149">补货方法，当预测的现有量级别低于特定阈值时，计划优化将库存补货到特定级别。</span><span class="sxs-lookup"><span data-stu-id="e6c13-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="e6c13-150">如果您定义产品的倍数数量，*最小值/最大值*</span><span class="sxs-lookup"><span data-stu-id="e6c13-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="e6c13-151">补货方法将更改其行为并考虑 **倍数** 值。</span><span class="sxs-lookup"><span data-stu-id="e6c13-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="e6c13-152">换句话说，当预测的现有量级别低于定义的最小级别，计划优化仍将库存补货到定义的最大级别。</span><span class="sxs-lookup"><span data-stu-id="e6c13-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="e6c13-153">但是，补货数量必须是 **倍数** 值的倍数。</span><span class="sxs-lookup"><span data-stu-id="e6c13-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="e6c13-154">如果补货数量（最大级别和预测的现有量级别之间的差异）不是已定义倍数的倍数，计划优化将使用低于最大级别的第一个可能的值（连同预测的现有量级别）。</span><span class="sxs-lookup"><span data-stu-id="e6c13-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="e6c13-155">如果总和小于最小级别，计划优化将使用高于最大级别的第一个值（连同预测的现有量）。</span><span class="sxs-lookup"><span data-stu-id="e6c13-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="e6c13-156">以下子部分提供了一些示例，说明产品的多个订单数量如何影响 *最小值/最大值*</span><span class="sxs-lookup"><span data-stu-id="e6c13-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="e6c13-157">补货方法的结果。</span><span class="sxs-lookup"><span data-stu-id="e6c13-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="e6c13-158">示例 1</span><span class="sxs-lookup"><span data-stu-id="e6c13-158">Example 1</span></span>

<span data-ttu-id="e6c13-159">产品具有以下配置：</span><span class="sxs-lookup"><span data-stu-id="e6c13-159">A product has the following configuration:</span></span>

- <span data-ttu-id="e6c13-160">**覆盖范围代码**：*最小值/最大值*</span><span class="sxs-lookup"><span data-stu-id="e6c13-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="e6c13-161">**最小值**：*15*</span><span class="sxs-lookup"><span data-stu-id="e6c13-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="e6c13-162">**最大值**：*22*</span><span class="sxs-lookup"><span data-stu-id="e6c13-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="e6c13-163">**倍数**：*0*</span><span class="sxs-lookup"><span data-stu-id="e6c13-163">**Multiple:** *0*</span></span>

<span data-ttu-id="e6c13-164">该产品现有 10 件库存，无其他需求或供应。</span><span class="sxs-lookup"><span data-stu-id="e6c13-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="e6c13-165">运行主计划时，会创建 12 件的计划订单以将库存补货到最大数量。</span><span class="sxs-lookup"><span data-stu-id="e6c13-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="e6c13-166">示例 2</span><span class="sxs-lookup"><span data-stu-id="e6c13-166">Example 2</span></span>

<span data-ttu-id="e6c13-167">产品具有以下配置：</span><span class="sxs-lookup"><span data-stu-id="e6c13-167">A product has the following configuration:</span></span>

- <span data-ttu-id="e6c13-168">**覆盖范围代码**：*最小值/最大值*</span><span class="sxs-lookup"><span data-stu-id="e6c13-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="e6c13-169">**最小值**：*15*</span><span class="sxs-lookup"><span data-stu-id="e6c13-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="e6c13-170">**最大值**：*22*</span><span class="sxs-lookup"><span data-stu-id="e6c13-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="e6c13-171">**倍数**：*5*</span><span class="sxs-lookup"><span data-stu-id="e6c13-171">**Multiple:** *5*</span></span>

<span data-ttu-id="e6c13-172">该产品现有 10 件库存，无其他需求或供应。</span><span class="sxs-lookup"><span data-stu-id="e6c13-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="e6c13-173">运行主计划时，会创建 10 件的计划订单（因为 15 件补货加上 10 件现有量库存将超过最大数量）。</span><span class="sxs-lookup"><span data-stu-id="e6c13-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="e6c13-174">示例 3</span><span class="sxs-lookup"><span data-stu-id="e6c13-174">Example 3</span></span>

<span data-ttu-id="e6c13-175">产品具有以下配置：</span><span class="sxs-lookup"><span data-stu-id="e6c13-175">A product has the following configuration:</span></span>

- <span data-ttu-id="e6c13-176">**覆盖范围代码**：*最小值/最大值*</span><span class="sxs-lookup"><span data-stu-id="e6c13-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="e6c13-177">**最小值**：*21*</span><span class="sxs-lookup"><span data-stu-id="e6c13-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="e6c13-178">**最大值**：*24*</span><span class="sxs-lookup"><span data-stu-id="e6c13-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="e6c13-179">**倍数**：*5*</span><span class="sxs-lookup"><span data-stu-id="e6c13-179">**Multiple:** *5*</span></span>

<span data-ttu-id="e6c13-180">该产品现有 10 件库存，无其他需求或供应。</span><span class="sxs-lookup"><span data-stu-id="e6c13-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="e6c13-181">运行主计划时，会创建 15 件的计划订单（因为 10 件补货加上 10 件现有量库存将小于最小数量）。</span><span class="sxs-lookup"><span data-stu-id="e6c13-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
