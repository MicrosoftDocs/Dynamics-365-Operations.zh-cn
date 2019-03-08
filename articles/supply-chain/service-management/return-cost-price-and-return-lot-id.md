---
title: 退货成本价和退货批次 ID
description: 您可能希望在您将产品销售给客户时，退回的产品的成本等于产品的成本。 可通过使用**退货批次 ID** 执行此操作。
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33cd3d50fe342ba12a17419f4e759c243a60b3e0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2019
ms.locfileid: "335132"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="17f05-104">退货成本价和退货批次 ID</span><span class="sxs-lookup"><span data-stu-id="17f05-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="17f05-105">通过使用产品的当前成本计算返回到库存的产品成本。</span><span class="sxs-lookup"><span data-stu-id="17f05-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="17f05-106">但是，您可能希望在您将产品销售给客户时，退回的产品的成本等于产品的成本。</span><span class="sxs-lookup"><span data-stu-id="17f05-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="17f05-107">可通过**销售订单**窗体**行明细**快速选项卡上的**退货批次 ID** 字段执行此操作。</span><span class="sxs-lookup"><span data-stu-id="17f05-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="17f05-108">例如，考虑以下方案。</span><span class="sxs-lookup"><span data-stu-id="17f05-108">For example, consider the following scenario.</span></span> <span data-ttu-id="17f05-109">您为客户开票。</span><span class="sxs-lookup"><span data-stu-id="17f05-109">You invoice a customer.</span></span> <span data-ttu-id="17f05-110">然后，该客户退回已交付给您的产品。</span><span class="sxs-lookup"><span data-stu-id="17f05-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="17f05-111">您将产品返回到库存。</span><span class="sxs-lookup"><span data-stu-id="17f05-111">You return the products to stock.</span></span> <span data-ttu-id="17f05-112">在这种情况下，在您为退回的产品贷记客户时，可以使用产品的当前成本计算这些产品成本。</span><span class="sxs-lookup"><span data-stu-id="17f05-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="17f05-113">但是，如果您使用**退货批次 ID** 字段，通过使用原始销售给客户的发票成本计算退回的产品的成本。</span><span class="sxs-lookup"><span data-stu-id="17f05-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="17f05-114">若要使用成本而不是来自某一客户退货的当前成本，请使用以下方法之一。</span><span class="sxs-lookup"><span data-stu-id="17f05-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="17f05-115">方法 1：手动输入退货成本价</span><span class="sxs-lookup"><span data-stu-id="17f05-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="17f05-116">默认情况下，当您将物料添加到退货单时，该物料以当前成本价返回到库存。</span><span class="sxs-lookup"><span data-stu-id="17f05-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="17f05-117">若要指定不同的退货成本价，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="17f05-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="17f05-118">单击**销售和市场营销** \> **通用** \> **退货单** \> **所有退货单**。</span><span class="sxs-lookup"><span data-stu-id="17f05-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="17f05-119">在**操作窗格**中的**新建**组中，单击**退货单**。</span><span class="sxs-lookup"><span data-stu-id="17f05-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="17f05-120">在**创建退货单**窗体中，选择一个客户帐户，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="17f05-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="17f05-121">在**退货单 - 物料退回授权号: %1、%2** 窗体中，选择某一物料，然后在**数量**字段中输入负数量。</span><span class="sxs-lookup"><span data-stu-id="17f05-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="17f05-122">单击**行明细**快速选项卡。</span><span class="sxs-lookup"><span data-stu-id="17f05-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="17f05-123">在**常规**选项卡中，在**退货成本价**字段中选择某一值。</span><span class="sxs-lookup"><span data-stu-id="17f05-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="17f05-124">在货物返回到库存时，使用此值。</span><span class="sxs-lookup"><span data-stu-id="17f05-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="17f05-125">如果未输入一个值，则在货物返回到库存时使用当前成本价。</span><span class="sxs-lookup"><span data-stu-id="17f05-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="17f05-126">方法 2：自动生成基于客户发票行的成本价</span><span class="sxs-lookup"><span data-stu-id="17f05-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="17f05-127">这是用于创建退货行的首选的方法。</span><span class="sxs-lookup"><span data-stu-id="17f05-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="17f05-128">若要在您将产品销售给客户时使用产品的成本，创建退货单并指定销售行到退货。</span><span class="sxs-lookup"><span data-stu-id="17f05-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="17f05-129">单击**销售和市场营销** \> **通用** \> **退货单** \> **所有退货单**。</span><span class="sxs-lookup"><span data-stu-id="17f05-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="17f05-130">在**操作窗格**中的**新建**组中，单击**退货单**。</span><span class="sxs-lookup"><span data-stu-id="17f05-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="17f05-131">在**创建退货单**窗体中，选择一个客户帐户，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="17f05-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="17f05-132">在**退货单 - 物料退回授权号: %1、%2** 窗体中的**操作窗格**上，单击**查找销售订单**。</span><span class="sxs-lookup"><span data-stu-id="17f05-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="17f05-133">在**查找销售订单**窗体中，选择要返回的发票行，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="17f05-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="17f05-134">在**行明细**快速选项卡的**常规**选项卡上，**退货批次 ID** 字段显示原始销售行中的值。</span><span class="sxs-lookup"><span data-stu-id="17f05-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="17f05-135">此外，**退货成本价**字段显示原始销售行的成本价值。</span><span class="sxs-lookup"><span data-stu-id="17f05-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="17f05-136">成本计算示例</span><span class="sxs-lookup"><span data-stu-id="17f05-136">Cost calculation example</span></span>

<span data-ttu-id="17f05-137">在您使用退货单行的**退货批次 ID** 字段中指定退货成本价时，使用退货单行的成本。</span><span class="sxs-lookup"><span data-stu-id="17f05-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="17f05-138">如果您执行库存结转或重新计算功能，该成本将在原始销售订单行进行调整。</span><span class="sxs-lookup"><span data-stu-id="17f05-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="17f05-139">自动调整退货单行的成本，反映每件的相同成本。</span><span class="sxs-lookup"><span data-stu-id="17f05-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="17f05-140">创建和下达称作“测试”的产品。</span><span class="sxs-lookup"><span data-stu-id="17f05-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="17f05-141">在**已发放产品详细信息** 窗体中，指定以下信息：</span><span class="sxs-lookup"><span data-stu-id="17f05-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="17f05-142">在**管理成本**快速选项卡上**物料组**字段中，选择**部件**组。</span><span class="sxs-lookup"><span data-stu-id="17f05-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="17f05-143">在**常规**快速选项卡上的**物料模型组**字段中，选择 **DEF**。</span><span class="sxs-lookup"><span data-stu-id="17f05-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="17f05-144">在**采购**快速选项卡的**价格**字段中，键入 10.00 作为物料的成本价。</span><span class="sxs-lookup"><span data-stu-id="17f05-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="17f05-145">在**操作窗格**上单击**维度组**。</span><span class="sxs-lookup"><span data-stu-id="17f05-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="17f05-146">在**存储维度组**字段中，选择 **仅站点和仓库**。</span><span class="sxs-lookup"><span data-stu-id="17f05-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="17f05-147">在**跟踪维度组**字段中，选择**不存在有效跟踪维度**。</span><span class="sxs-lookup"><span data-stu-id="17f05-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="17f05-148">按每件 6.00 创建 10 件测试物料的采购订单，然后为采购订单过帐发票。</span><span class="sxs-lookup"><span data-stu-id="17f05-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="17f05-149">按每件 8.00 创建 10 件测试物料的第二采购订单，然后为采购订单过帐发票。</span><span class="sxs-lookup"><span data-stu-id="17f05-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="17f05-150">过帐销售订单的发票以销售五件测试物料。</span><span class="sxs-lookup"><span data-stu-id="17f05-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="17f05-151">在这种情况下，销售订单行成本为 35.00（5 件 \* 7.00 每件平均成本）。</span><span class="sxs-lookup"><span data-stu-id="17f05-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="17f05-152">为客户创建退货单。</span><span class="sxs-lookup"><span data-stu-id="17f05-152">Create a return order for the customer.</span></span> <span data-ttu-id="17f05-153">在**查找销售订单**窗体中，选择发票行，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="17f05-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="17f05-154">在**退货单 - 物料退回授权号: %1、%2** 窗体中，验证生成退回测试物料的退货单。</span><span class="sxs-lookup"><span data-stu-id="17f05-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="17f05-155">将退货单的数量设置为 -5.00。</span><span class="sxs-lookup"><span data-stu-id="17f05-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="17f05-156">**退货批次 ID** 字段显示批次 ID。</span><span class="sxs-lookup"><span data-stu-id="17f05-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="17f05-157">此批 ID 从已向客户销售的物料的原始销售订单中获得。</span><span class="sxs-lookup"><span data-stu-id="17f05-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="17f05-158">**退货成本价**字段显示原始销售行的成本价。</span><span class="sxs-lookup"><span data-stu-id="17f05-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="17f05-159">登记退回物料的接收。</span><span class="sxs-lookup"><span data-stu-id="17f05-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="17f05-160">过帐退回物料的装箱单。</span><span class="sxs-lookup"><span data-stu-id="17f05-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="17f05-161">过帐退货单的发票。</span><span class="sxs-lookup"><span data-stu-id="17f05-161">Post an invoice for the return order.</span></span> <span data-ttu-id="17f05-162">在**所有销售订单**列表页中，订单类型为**退回订单**的销售订单。</span><span class="sxs-lookup"><span data-stu-id="17f05-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="17f05-163">打开**库存交易记录**窗体。</span><span class="sxs-lookup"><span data-stu-id="17f05-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="17f05-164">通过使用**退货成本价**字段中的值，为**成本额**字段中的总计 35.00 验证退货成本为每件 7.00。</span><span class="sxs-lookup"><span data-stu-id="17f05-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="17f05-165">可从**退货单 - 物料退回授权号: %1、%2** 窗体打开**库存交易记录**窗体。</span><span class="sxs-lookup"><span data-stu-id="17f05-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="17f05-166">在**行**网格中，单击**库存** \> **交易记录**。</span><span class="sxs-lookup"><span data-stu-id="17f05-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="17f05-167">在库存和仓库管理中，使用**结转与调整**窗体运行 **3. 结转**过程。</span><span class="sxs-lookup"><span data-stu-id="17f05-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="17f05-168">此操作将成本为 -35.00（5 件 \* 7.00）的原始销售订单行上的成本调整为 -30.00（5 件 \* 6.00）。</span><span class="sxs-lookup"><span data-stu-id="17f05-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="17f05-169">原因在于，库存模型组使用先进先出 (FIFO)，并且，每件 6.00 是来自第一采购订单的成本。</span><span class="sxs-lookup"><span data-stu-id="17f05-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="17f05-170">此外，该操作调整退货销售行上的成本，以匹配原始销售行上每件的成本。</span><span class="sxs-lookup"><span data-stu-id="17f05-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="17f05-171">因此，退货行的成本从 35.00 调整为 30.00。</span><span class="sxs-lookup"><span data-stu-id="17f05-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




