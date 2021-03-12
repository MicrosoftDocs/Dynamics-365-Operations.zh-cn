---
title: 移动平均
description: 移动平均是一种基于平均原则的永久成本方法，在执行采购成本时在库存发货的成本不更改。 该差异基于一种比例的计算资本化。 支出剩余金额。
author: AndersGirke
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0957fee111ec1fd5bb66951126869cf46d88b36e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967475"
---
# <a name="moving-average"></a><span data-ttu-id="3ab7e-105">移动平均</span><span class="sxs-lookup"><span data-stu-id="3ab7e-105">Moving average</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ab7e-106">移动平均是一种基于平均原则的永久成本方法，在执行采购成本时在库存发货的成本不更改。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-106">Moving average is a perpetual costing method based on the average principle, where the costs on inventory issues do not change when the purchase cost does.</span></span> <span data-ttu-id="3ab7e-107">该差异基于一种比例的计算资本化。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-107">The difference is capitalized and is based on a proportional calculation.</span></span> <span data-ttu-id="3ab7e-108">支出剩余金额。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-108">The amount that remains is expensed.</span></span>

<span data-ttu-id="3ab7e-109">在您使用移动平均时，不支持库存结算和库存标记。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-109">When you use moving average, inventory settlements and inventory marking are not supported.</span></span> <span data-ttu-id="3ab7e-110">库存结转不会影响具有作为库存模型组的移动平均的产品，并且不生成交易记录之间的任何结算。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-110">Inventory close does not affect products that have moving average as the inventory model group, and it does not generate any settlements between the transactions.</span></span>

<span data-ttu-id="3ab7e-111">在您使用移动平均成本作为成本计算方法时，以下选项是先决条件。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-111">The following are prerequisites when you use moving average cost as a costing method.</span></span>

1. <span data-ttu-id="3ab7e-112">在 **物料模型组** 页中，设置在 **库存模型** 字段中选择了 **移动平均** 的物料模型组。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-112">On the **Item model groups** page, set up an item model group that has **Moving average** selected in the **Inventory model** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3ab7e-113">默认情况下，当选择了 **移动平均** 后，**过帐实际库存** 和 **过帐财务库存** 字段也将选择。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-113">By default, when **Moving average** is selected, the **Post physical inventory** and **Post financial inventory** fields are also selected.</span></span>

1. <span data-ttu-id="3ab7e-114">在 **过帐** 页上，将科目分配给 **移动平均价差**。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-114">On the **Posting** page, assign accounts to the **Price difference for moving average**.</span></span> <span data-ttu-id="3ab7e-115">在成本必须按比例支出时，使用 **移动平均价差** 科目。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-115">You use the **Price difference for moving average** account when cost has to be proportionally expensed.</span></span> <span data-ttu-id="3ab7e-116">以下两种情况下会发生这种情况：</span><span class="sxs-lookup"><span data-stu-id="3ab7e-116">This occurs in following two scenarios:</span></span>
    - <span data-ttu-id="3ab7e-117">因为原始库存数量和现有数量之间存在差异，所以采购收货和采购发票之间存在成本差异。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-117">There is a difference in cost between a purchase receipt and the purchase invoice because there is a difference between the original inventory quantity and the current on-hand quantity.</span></span>
    - <span data-ttu-id="3ab7e-118">交易记录导致库存从负变为零，并且交易记录成本和当前移动平均成本之间存在差异。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-118">The transactions bring the inventory from negative to zero, and there is a difference between the transaction cost and the current moving average cost.</span></span>

1. <span data-ttu-id="3ab7e-119">在 **过帐** 页中，将科目分配给 **库存** 选项卡上的 **重估移动平均成本** 科目。当您要为产品调整移动平均成本到新的单位价格时，请使用 **重估移动平均成本** 科目。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-119">On the **Posting** page, assign accounts to the **Cost revaluation for moving average** accounts on the **Inventory** tab. You use the **Cost revaluation for moving average** account when you want to adjust the moving average cost for a product to a new unit price.</span></span>

1. <span data-ttu-id="3ab7e-120">在 **已发布产品** 页中，分配移动平均物料模型组到产品。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-120">On the **Released products** page, assign the moving average item model group to the product.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3ab7e-121">库存结转过程只结束会计期间。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-121">The inventory close process only closes the accounting period.</span></span> <span data-ttu-id="3ab7e-122">不影响具有作为物料模型组分配到它们的移动平均的产品。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-122">It does not affect products that have moving average assigned to them as an item model group.</span></span>

## <a name="convert-to-the-moving-average-costing-method"></a><span data-ttu-id="3ab7e-123">转换到移动平均成本计算方法</span><span class="sxs-lookup"><span data-stu-id="3ab7e-123">Convert to the moving average costing method</span></span>

<span data-ttu-id="3ab7e-124">转换产品使用移动平均库存评估方法。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-124">Products can be converted to use the moving average inventory valuation method.</span></span> <span data-ttu-id="3ab7e-125">在当前年度的最后一个月结束后，转换的此类型通常在年末完成。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-125">This type of conversion is usually done at the end of the year, after the last month of the current year is closed.</span></span> <span data-ttu-id="3ab7e-126">通过使用产品的当前成本模型执行。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-126">It is done by using the product’s current costing model.</span></span> <span data-ttu-id="3ab7e-127">您可以从基于平均成本或标准成本的成本计算方法更改您的库存结转法到基于移动平均的方法。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-127">You can change your inventory costing method from a costing method that is based on average cost or standard cost to a method that is based on moving average.</span></span>

<span data-ttu-id="3ab7e-128">如果您从标准成本计算方法更改您的成本计算方法到移动平均方法，必须完成以下任务:</span><span class="sxs-lookup"><span data-stu-id="3ab7e-128">If you are changing your costing method from a standard costing method to a moving average method, you have to complete the following tasks:</span></span>

1. <span data-ttu-id="3ab7e-129">进行调整记下库存数量和值为 0（零）。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-129">Make adjustments to get inventory quantities and values down to 0 (zero).</span></span>
1. <span data-ttu-id="3ab7e-130">在库存值和数量为 0（零）后，更改物料模型组到移动平均。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-130">After the inventory value and quantity are 0 (zero), change the item model group to moving average.</span></span>
1. <span data-ttu-id="3ab7e-131">进行调整获取数量和值直接移回库存。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-131">Make adjustments to get the quantity and value back into inventory.</span></span>

<span data-ttu-id="3ab7e-132">您不能将您的库存结转法从移动平均方法更改到先进先出 (FIFO) 方法、后进先出 (LIFO) 方法或加权平均方法。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-132">You cannot change your inventory costing method from a moving average method to a First in, First out (FIFO) method, a Last in, First out (LIFO) method, or a weighted average method.</span></span>

> [!NOTE]
> <span data-ttu-id="3ab7e-133">从未标准成本到移动加权平均的转换是手动程序。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-133">Converting from standard cost to moving weighted average is a manual process.</span></span>

<span data-ttu-id="3ab7e-134">以下示例说明使用移动平均成本计算方法的影响。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-134">The following examples illustrate the effect of using the moving average costing method.</span></span> <span data-ttu-id="3ab7e-135">有以下四种配置：</span><span class="sxs-lookup"><span data-stu-id="3ab7e-135">There are four configurations:</span></span>

- <span data-ttu-id="3ab7e-136">采购订单和比例支出的成本差异</span><span class="sxs-lookup"><span data-stu-id="3ab7e-136">Purchase order and proportionally expensed cost difference</span></span>
- <span data-ttu-id="3ab7e-137">移动平均产品和库存调整</span><span class="sxs-lookup"><span data-stu-id="3ab7e-137">Moving average product and inventory adjustment</span></span>
- <span data-ttu-id="3ab7e-138">具有生产的移动平均</span><span class="sxs-lookup"><span data-stu-id="3ab7e-138">Moving average with production</span></span>
- <span data-ttu-id="3ab7e-139">使用回溯交易记录的移动平均</span><span class="sxs-lookup"><span data-stu-id="3ab7e-139">Moving average with a backdated transaction</span></span>

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a><span data-ttu-id="3ab7e-140">采购订单和比例支出的成本差异</span><span class="sxs-lookup"><span data-stu-id="3ab7e-140">Purchase order and proportionally expensed cost difference</span></span>

<span data-ttu-id="3ab7e-141">使用移动平均，采购收货取决于产品的成本。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-141">With moving average, the product’s cost is determined by the purchase receipt.</span></span> <span data-ttu-id="3ab7e-142">在过帐采购发票时，如果存在在采购收货和采购发票之间的成本差异，差额按比例调整到库存的当前产品，并且支出所有剩余金额。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-142">When the purchase invoice is posted, if there is a difference in cost between the purchase receipt and the purchase invoice, the difference is proportionally adjusted to the current products in stock, and any remaining amount is expensed.</span></span>

<span data-ttu-id="3ab7e-143">在此示例中，以一致的成本创建和接收采购订单，使用不同的成本过帐采购发票。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-143">In this example, a purchase order is created and received at one cost, and the purchase invoice is posted with a different cost.</span></span>

1. <span data-ttu-id="3ab7e-144">创建针对数量 2 和单价为 10.00 的采购订单。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-144">Create a purchase order for a quantity of 2 and a unit price of 10.00.</span></span>
1. <span data-ttu-id="3ab7e-145">创建产品的采购收货。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-145">Create a purchase receipt of the product.</span></span>
1. <span data-ttu-id="3ab7e-146">创建针对数量 1 和单价为 10.00 的销售订单。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-146">Create a sales order for a quantity of 1 and a unit price of 10.00.</span></span>
1. <span data-ttu-id="3ab7e-147">创建针对数量 2 和单价为 12.00 的采购发票。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-147">Create a purchase invoice for a quantity of 2 and a unit price of 12.00.</span></span>

<span data-ttu-id="3ab7e-148">在采购发票过帐时，在单位价格中 2.00 的差异过帐到“移动平均价差”帐户。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-148">The difference in unit price, 2.00, is posted to the Price difference for moving average account when the purchase invoice is posted.</span></span> <span data-ttu-id="3ab7e-149">该原因是为成本 20.00 购置两种产品。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-149">The reason is that two products were purchased for a cost of 20.00.</span></span> <span data-ttu-id="3ab7e-150">为单位价格 10.00 销售产品中的一个。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-150">One of the products was sold for a unit price of 10.00.</span></span> <span data-ttu-id="3ab7e-151">采购发票以单位价格 12.00 和数量 2 过帐。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-151">The purchase invoice was posted at a unit price of 12.00 with a quantity of 2.</span></span> <span data-ttu-id="3ab7e-152">产品的单位价格不能以 14.00 过帐。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-152">The unit price of the product cannot be posted at 14.00.</span></span>

## <a name="moving-average-product-and-inventory-adjustment"></a><span data-ttu-id="3ab7e-153">移动平均产品和库存调整</span><span class="sxs-lookup"><span data-stu-id="3ab7e-153">Moving average product and inventory adjustment</span></span>

<span data-ttu-id="3ab7e-154">如果您需要调整产品的移动平均成本，库存调整截至今天的日期设置访问权限。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-154">If you need to adjust the moving average cost of a product, inventory adjustments are allowed as of today’s date.</span></span> <span data-ttu-id="3ab7e-155">您不能追溯库存调整更正产品的移动平均成本。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-155">You cannot backdate an inventory adjustment to correct the moving average cost of a product.</span></span> <span data-ttu-id="3ab7e-156">您不能通过后续交易记录具有成本流。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-156">You cannot have the cost flow through subsequent transactions.</span></span>

<span data-ttu-id="3ab7e-157">在此示例中，移动平均成本为产品进行调整。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-157">In this example, the moving average cost is adjusted for a product.</span></span>

1. <span data-ttu-id="3ab7e-158">选择要调整移动平均成本的产品。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-158">Select the product that you want to adjust the moving average cost for.</span></span> 

 > [!NOTE]
 > <span data-ttu-id="3ab7e-159">**重估移动平均** 页检查库存是否可用于产品。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-159">The **Revaluation for moving average** page examines the inventory available for a product.</span></span> <span data-ttu-id="3ab7e-160">所选产品具有已过帐的数量 1，过帐值 12.00，已过帐的单位成本 12.00 和单位成本 12.00。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-160">The product selected has a posted quantity of 1, a posted a value of 12.00, a posted unit cost of 12.00, and a unit cost of 12.00.</span></span>
    
1. <span data-ttu-id="3ab7e-161">更新 **单位成本** 字段为 16.00。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-161">Update the **Unit cost** field to 16.00.</span></span> <span data-ttu-id="3ab7e-162">系统计算其余字段。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-162">The system calculates the remaining fields.</span></span>
1. <span data-ttu-id="3ab7e-163">过帐调整。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-163">The adjustment is posted.</span></span>

> [!NOTE]
> <span data-ttu-id="3ab7e-164">您可以从今天的日期仅调整移动平均成本。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-164">You can only adjust the moving average cost as of today’s date.</span></span>

<span data-ttu-id="3ab7e-165">在 **凭证的结算** 页中，您可以看到调整 4.00 过帐到成本重估。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-165">On the **Settlements for voucher** page, you can see an adjustment of 4.00 posted to the Cost revaluation for moving average account.</span></span>

## <a name="moving-average-with-production"></a><span data-ttu-id="3ab7e-166">具有生产的移动平均</span><span class="sxs-lookup"><span data-stu-id="3ab7e-166">Moving average with production</span></span>

<span data-ttu-id="3ab7e-167">移动平均支持生产物料。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-167">Moving average supports produced items.</span></span> <span data-ttu-id="3ab7e-168">如果您计划在生产环境中使用移动平均，请选择 **生产控制参数** 页的 **使用估计的成本价**。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-168">If you plan to use moving average in a production environment, select **Use estimated cost price** on the **Production control parameters** page.</span></span> <span data-ttu-id="3ab7e-169">这意味着使用估计期间计算的成本价而不使用实际物料清单计算成本价。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-169">This means that the cost price that is calculated during estimation is used instead of the actual BOM calculation cost price.</span></span>

## <a name="moving-average-with-a-backdated-transaction"></a><span data-ttu-id="3ab7e-170">使用回溯交易记录的移动平均</span><span class="sxs-lookup"><span data-stu-id="3ab7e-170">Moving average with a backdated transaction</span></span>

<span data-ttu-id="3ab7e-171">回溯交易记录分配当前移动平均成本，并且更新产品的实际数量，不过，不影响产品的移动平均成本。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-171">Backdated transactions are assigned the current moving average cost, and the product’s physical quantity is updated, but the product’s moving average cost is not affected.</span></span> <span data-ttu-id="3ab7e-172">在此移动平均示例中，过帐移动平均产品的一个回溯交易记录。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-172">In this moving average example, a backdated transaction for a moving average product is posted.</span></span>

1. <span data-ttu-id="3ab7e-173">为数量 1 和成本 20.00 的移动平均产品创建库存调整。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-173">Create an inventory adjustment for the moving average product for a quantity of 1 and a cost of 20.00.</span></span>
1. <span data-ttu-id="3ab7e-174">产品的库存交易记录历史记录将类似于以下操作:</span><span class="sxs-lookup"><span data-stu-id="3ab7e-174">The inventory transaction history for the product would resemble the following:</span></span>
    - <span data-ttu-id="3ab7e-175">库存交易记录 1、成本 16.00、过帐日期 1 月 15 日和交易记录日期 1 月 15 日。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-175">An inventory transaction of 1, a cost of 16.00, a posting date of January 15, and a transaction date of January 15.</span></span>
    - <span data-ttu-id="3ab7e-176">库存调整 1、成本 20.00、过帐日期 1 月 1 日和交易记录日期 1 月 15 日。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-176">An inventory adjustment of 1, a cost of 20.00, a posting date of January 1, and a transaction date of January 15.</span></span>
1. <span data-ttu-id="3ab7e-177">过帐调整。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-177">Post the adjustment.</span></span>

<span data-ttu-id="3ab7e-178">在 **库存交易记录** 页中，您可以查看为产品作为当前移动平均支出的 4.00 是 16.00。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-178">On the **Inventory transactions** page, you can see that 4.00 is expensed as the current moving average for the product is 16.00.</span></span> <span data-ttu-id="3ab7e-179">您可以在以前过帐，但是支出成本差异，以便不影响移动平均成本。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-179">You can post in the past, but the difference in cost is expensed, so the moving average cost is not affected.</span></span>

## <a name="negative-inventory-balances"></a><span data-ttu-id="3ab7e-180">库存余额为负</span><span class="sxs-lookup"><span data-stu-id="3ab7e-180">Negative inventory balances</span></span>

<span data-ttu-id="3ab7e-181">交易记录的处理方式取决于交易记录后新的现有数量为负、零还是正。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-181">Transactions are handled differently depending on whether the new on-hand quantity after the transaction is negative, zero, or positive.</span></span>

### <a name="new-balance-is-negative-or-zero"></a><span data-ttu-id="3ab7e-182">新余额为负或零</span><span class="sxs-lookup"><span data-stu-id="3ab7e-182">New balance is negative or zero</span></span>

<span data-ttu-id="3ab7e-183">如果新的现有数量为负或零，则按当前的平均成本计算交易记录的成本。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-183">If the new on-hand quantity is negative or zero, the transaction is costed at the current average costs.</span></span> <span data-ttu-id="3ab7e-184">如果采购价和当前平均成本之间存在差异，则将其过帐到 **移动平均价差**。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-184">If there is a difference between the purchase price and the current average costs, it's posted to **Price difference for moving average**.</span></span>

### <a name="new-balance-is-positive"></a><span data-ttu-id="3ab7e-185">新余额为正</span><span class="sxs-lookup"><span data-stu-id="3ab7e-185">New balance is positive</span></span>

<span data-ttu-id="3ab7e-186">如果交易记录后新的现有数量为正，这将交易记录拆分为两个部分并对这两个部分以不同方式计算成本，然后汇总到下表中。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-186">If the new on-hand quantity is positive after the transaction, the transaction is split into two parts and costed differently, as summarized in the following table.</span></span>

| <span data-ttu-id="3ab7e-187">部分</span><span class="sxs-lookup"><span data-stu-id="3ab7e-187">Part</span></span> | <span data-ttu-id="3ab7e-188">说明</span><span class="sxs-lookup"><span data-stu-id="3ab7e-188">Description</span></span> |
|---|---|
| <span data-ttu-id="3ab7e-189">数量从负到零</span><span class="sxs-lookup"><span data-stu-id="3ab7e-189">Quantity from negative to zero</span></span> | <span data-ttu-id="3ab7e-190">库存使用物料的当前移动平均成本，而不是将现有余额从负增加到零的该部分收货数量的交易记录成本。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-190">Inventory uses the current moving average cost of the item rather than the transaction cost for that portion of the receipt quantity that increases the on-hand balance from negative to zero.</span></span> <span data-ttu-id="3ab7e-191">将把交易记录成本和当前移动平均成本之间的差异过帐到 **移动平均价差**。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-191">The difference between the transaction cost and the current moving average cost is posted to **Price difference for moving average**.</span></span> |
| <span data-ttu-id="3ab7e-192">数量从零到负</span><span class="sxs-lookup"><span data-stu-id="3ab7e-192">Quantity from zero to positive</span></span> | <span data-ttu-id="3ab7e-193">存货使用将现有余额从零增加到正的该部分收货数量的交易记录成本。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-193">Inventory uses the transaction cost for that portion of the receipt quantity that increases the on-hand balance from zero to positive.</span></span>                                                  |

## <a name="inventory-value-report"></a><span data-ttu-id="3ab7e-194">库存值报表</span><span class="sxs-lookup"><span data-stu-id="3ab7e-194">Inventory value report</span></span>

<span data-ttu-id="3ab7e-195">在此移动平均示例中，打印库存值报表支持产品的当前移动平均计算。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-195">In this moving average example, the inventory value report is printed to support the current moving average calculation for a product.</span></span> <span data-ttu-id="3ab7e-196">库存价值报表可以按时间顺序打印交易记录，与成本一起支持产品的移动平均成本计算。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-196">The Inventory value report can print the transactions in chronological order, together with the cost to support the moving average cost calculation of a product.</span></span> <span data-ttu-id="3ab7e-197">报表显示产品的移动平均成本。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-197">The report displays the moving average cost for the product.</span></span> <span data-ttu-id="3ab7e-198">在 **库存价值报表** 对话框中，日期间隔允许您选择对报表排序使用的 **交易记录时间** 或 **过帐日期**。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-198">In the **Inventory value reports** dialog box, a date interval allows you to select the **Transaction time** or the **Posting date** to sort the report by.</span></span> <span data-ttu-id="3ab7e-199">**过帐日期** 选项是传统上打印报表的方式。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-199">The **Posting date** option is how the report is traditionally printed.</span></span> <span data-ttu-id="3ab7e-200">**交易记录时间** 选项是报表交易记录和更新产品的移动平均成本的实际日期。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-200">The **Transaction time** option is the actual date that the transaction is reported and the moving average cost for the product is updated.</span></span> <span data-ttu-id="3ab7e-201">如果您要随时间查看移动平均成本，可以通过使用 **交易记录时间排序** 选项打印库存价值报表。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-201">You can print the Inventory value report by using the **Transaction time sorting** option if you want to see the moving average cost calculation over time.</span></span> <span data-ttu-id="3ab7e-202">下表显示使用 **交易记录时间排序** 选项时打印报表的产品的交易记录。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-202">The following table displays the transactions for the product that the report is printed for when the **Transaction time sorting** option is used.</span></span>

| <span data-ttu-id="3ab7e-203">交易记录时间</span><span class="sxs-lookup"><span data-stu-id="3ab7e-203">Transaction time</span></span> | <span data-ttu-id="3ab7e-204">日期</span><span class="sxs-lookup"><span data-stu-id="3ab7e-204">Date</span></span>         | <span data-ttu-id="3ab7e-205">交易记录类型</span><span class="sxs-lookup"><span data-stu-id="3ab7e-205">Transaction type</span></span>           | <span data-ttu-id="3ab7e-206">已</span><span class="sxs-lookup"><span data-stu-id="3ab7e-206">Quantity</span></span> | <span data-ttu-id="3ab7e-207">金额</span><span class="sxs-lookup"><span data-stu-id="3ab7e-207">Amount</span></span> | <span data-ttu-id="3ab7e-208">平均单位成本</span><span class="sxs-lookup"><span data-stu-id="3ab7e-208">Average unit cost</span></span> |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | <span data-ttu-id="3ab7e-209">10 月 1 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-209">October 1</span></span>    | <span data-ttu-id="3ab7e-210">起初余额</span><span class="sxs-lookup"><span data-stu-id="3ab7e-210">Beginning balance</span></span>          | <span data-ttu-id="3ab7e-211">0</span><span class="sxs-lookup"><span data-stu-id="3ab7e-211">0</span></span>        | <span data-ttu-id="3ab7e-212">0.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-212">0.00</span></span>   | <span data-ttu-id="3ab7e-213">0.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-213">0.00</span></span>              |
| <span data-ttu-id="3ab7e-214">10 月 8 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-214">October 8</span></span>        | <span data-ttu-id="3ab7e-215">9 月 28 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-215">September 28</span></span> | <span data-ttu-id="3ab7e-216">追溯的收货</span><span class="sxs-lookup"><span data-stu-id="3ab7e-216">Backdated receipt</span></span>          | <span data-ttu-id="3ab7e-217">1</span><span class="sxs-lookup"><span data-stu-id="3ab7e-217">1</span></span>        | <span data-ttu-id="3ab7e-218">16.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-218">16.00</span></span>  | <span data-ttu-id="3ab7e-219">16.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-219">16.00</span></span>             |
| <span data-ttu-id="3ab7e-220">10 月 3 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-220">October 3</span></span>        | <span data-ttu-id="3ab7e-221">10 月 3 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-221">October 3</span></span>    | <span data-ttu-id="3ab7e-222">采购收货</span><span class="sxs-lookup"><span data-stu-id="3ab7e-222">Purchase receipt</span></span>           | <span data-ttu-id="3ab7e-223">2</span><span class="sxs-lookup"><span data-stu-id="3ab7e-223">2</span></span>        | <span data-ttu-id="3ab7e-224">20.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-224">20.00</span></span>  | <span data-ttu-id="3ab7e-225">12.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-225">12.00</span></span>             |
| <span data-ttu-id="3ab7e-226">10 月 5 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-226">October 5</span></span>        | <span data-ttu-id="3ab7e-227">10 月 5 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-227">October 5</span></span>    | <span data-ttu-id="3ab7e-228">销售订单</span><span class="sxs-lookup"><span data-stu-id="3ab7e-228">Sales order</span></span>                | <span data-ttu-id="3ab7e-229">-1</span><span class="sxs-lookup"><span data-stu-id="3ab7e-229">-1</span></span>       | <span data-ttu-id="3ab7e-230">-10.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-230">-10.00</span></span> | <span data-ttu-id="3ab7e-231">13.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-231">13.00</span></span>             |
| <span data-ttu-id="3ab7e-232">10 月 7 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-232">October 7</span></span>        | <span data-ttu-id="3ab7e-233">10 月 7 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-233">October 7</span></span>    | <span data-ttu-id="3ab7e-234">采购发票</span><span class="sxs-lookup"><span data-stu-id="3ab7e-234">Purchase invoice</span></span>           |          | <span data-ttu-id="3ab7e-235">2.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-235">2.00</span></span>   | <span data-ttu-id="3ab7e-236">14.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-236">14.00</span></span>             |
| <span data-ttu-id="3ab7e-237">10 月 8 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-237">October 8</span></span>        | <span data-ttu-id="3ab7e-238">10 月 8 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-238">October 8</span></span>    | <span data-ttu-id="3ab7e-239">移动平均重估</span><span class="sxs-lookup"><span data-stu-id="3ab7e-239">Moving average revaluation</span></span> |          | <span data-ttu-id="3ab7e-240">4.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-240">4.00</span></span>   | <span data-ttu-id="3ab7e-241">16.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-241">16.00</span></span>             |
|                  | <span data-ttu-id="3ab7e-242">10 月 31 日</span><span class="sxs-lookup"><span data-stu-id="3ab7e-242">October 31</span></span>   | <span data-ttu-id="3ab7e-243">合计</span><span class="sxs-lookup"><span data-stu-id="3ab7e-243">Total</span></span>                      | <span data-ttu-id="3ab7e-244">2</span><span class="sxs-lookup"><span data-stu-id="3ab7e-244">2</span></span>        | <span data-ttu-id="3ab7e-245">32.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-245">32.00</span></span>  | <span data-ttu-id="3ab7e-246">16.00</span><span class="sxs-lookup"><span data-stu-id="3ab7e-246">16.00</span></span>             |

> [!NOTE]
> <span data-ttu-id="3ab7e-247">您不能通过使用 **交易记录时间排序** 选项对帐具有库存的总帐。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-247">You cannot reconcile the general ledger with inventory by using the **Transaction time sorting** option.</span></span> <span data-ttu-id="3ab7e-248">必须通过使用 **过帐日期** 选项打印报表。</span><span class="sxs-lookup"><span data-stu-id="3ab7e-248">The report must be printed by using the **Posting date** option.</span></span>
