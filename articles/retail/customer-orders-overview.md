---
title: "客户订单概览"
description: "此主题提供有关 Retail Modern POS (MPOS) 中的客户订单的信息。 客户订单也称为特殊订单。 此主题中包含对相关参数和交易记录流的讨论。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ce6774ede836eb29e6ef2cd8d4baa9efb931020c
ms.contentlocale: zh-cn
ms.lasthandoff: 11/03/2017

---

# <a name="customer-orders-overview"></a><span data-ttu-id="d77f5-105">客户订单概览</span><span class="sxs-lookup"><span data-stu-id="d77f5-105">Customer orders overview</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="d77f5-106">此主题提供有关 Retail Modern POS (MPOS) 中的客户订单的信息。</span><span class="sxs-lookup"><span data-stu-id="d77f5-106">This topic provides information about customer orders in Retail Modern POS (MPOS).</span></span> <span data-ttu-id="d77f5-107">客户订单也称为特殊订单。</span><span class="sxs-lookup"><span data-stu-id="d77f5-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="d77f5-108">此主题中包含对相关参数和交易记录流的讨论。</span><span class="sxs-lookup"><span data-stu-id="d77f5-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="d77f5-109">在 omni 渠道零售环境中，许多零售商提供客户订单（即特殊订单）选项，以满足各种产品和履行要求。</span><span class="sxs-lookup"><span data-stu-id="d77f5-109">In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="d77f5-110">下面是一些典型方案：</span><span class="sxs-lookup"><span data-stu-id="d77f5-110">Here are some typical scenarios:</span></span>

-   <span data-ttu-id="d77f5-111">客户希望将产品在特定日期发到特定地址。</span><span class="sxs-lookup"><span data-stu-id="d77f5-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
-   <span data-ttu-id="d77f5-112">客户希望从非购买产品的商店或位置取货。</span><span class="sxs-lookup"><span data-stu-id="d77f5-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
-   <span data-ttu-id="d77f5-113">客户希望其他人取自己购买的产品。</span><span class="sxs-lookup"><span data-stu-id="d77f5-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="d77f5-114">零售商也可以使用客户订单将库存不足可能导致的失单降到最低，因为可以在其他时间或位置发货或取货。</span><span class="sxs-lookup"><span data-stu-id="d77f5-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="d77f5-115">设置客户订单</span><span class="sxs-lookup"><span data-stu-id="d77f5-115">Set up customer orders</span></span>
<span data-ttu-id="d77f5-116">下面是一些可在**零售参数**页面中设置来定义如何履行客户订单的参数。</span><span class="sxs-lookup"><span data-stu-id="d77f5-116">Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:</span></span>

-   <span data-ttu-id="d77f5-117">**默认保证金百分比** – 指定确认订单前客户必须以存款的形式支付的金额。</span><span class="sxs-lookup"><span data-stu-id="d77f5-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="d77f5-118">默认保证金金额为订单值的百分比。</span><span class="sxs-lookup"><span data-stu-id="d77f5-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="d77f5-119">售货员可能可以根据其权限通过使用**保证金覆盖**来覆盖该金额。</span><span class="sxs-lookup"><span data-stu-id="d77f5-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
-   <span data-ttu-id="d77f5-120">**取消费百分比** – 如果取消客户订单时需要收取费用，请指定这笔费用的金额。</span><span class="sxs-lookup"><span data-stu-id="d77f5-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
-   <span data-ttu-id="d77f5-121">**取消费代码** – 如果取消客户订单时需要收取费用，将在销售订单内的收费代码下体现这笔费用。</span><span class="sxs-lookup"><span data-stu-id="d77f5-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="d77f5-122">可使用此参数定义取消费代码。</span><span class="sxs-lookup"><span data-stu-id="d77f5-122">Use this parameter to define the cancellation charge code.</span></span>
-   <span data-ttu-id="d77f5-123">**装运费用代码** – 零售商可为将商品装运到客户再收取一笔费用。</span><span class="sxs-lookup"><span data-stu-id="d77f5-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="d77f5-124">销售订单内的收费代码下将体现这笔装运费用的金额。</span><span class="sxs-lookup"><span data-stu-id="d77f5-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="d77f5-125">可使用此参数将装运费用代码映射到客户订单中的装运费用。</span><span class="sxs-lookup"><span data-stu-id="d77f5-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
-   <span data-ttu-id="d77f5-126">**退回装运费用** – 指定是否可退回客户订单关联的装运费用。</span><span class="sxs-lookup"><span data-stu-id="d77f5-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
-   <span data-ttu-id="d77f5-127">**未经审核的最大金额** – 如果装运费用可退回，指定退货单中的最大装运费用退款金额。</span><span class="sxs-lookup"><span data-stu-id="d77f5-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="d77f5-128">如果超过了此金额，需要经历覆盖才能继续退款。</span><span class="sxs-lookup"><span data-stu-id="d77f5-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="d77f5-129">为了满足以下方案，装运费用的退款可能超过最初支付的金额。</span><span class="sxs-lookup"><span data-stu-id="d77f5-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>
    -   <span data-ttu-id="d77f5-130">费用在销售订单抬头级别实施，并且如果退回了某个产品行的一定数量，则不能按照适合所有零售客户的方式确定为这些产品和数量允许的最大装运费用退款。</span><span class="sxs-lookup"><span data-stu-id="d77f5-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.</span></span>
    -   <span data-ttu-id="d77f5-131">每次运货都会产生装运费用。</span><span class="sxs-lookup"><span data-stu-id="d77f5-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="d77f5-132">如果客户多次退货，而零售商的政策规定由零售商承担退货装运费用的成本，退货装运费用将超过实际装运费用。</span><span class="sxs-lookup"><span data-stu-id="d77f5-132">If a customer returns products multiple times, and the retailer’s policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="d77f5-133">客户订单的交易记录流</span><span class="sxs-lookup"><span data-stu-id="d77f5-133">Transaction flow for customer orders</span></span>
### <a name="create-a-customer-order-in-retail-modern-pos"></a><span data-ttu-id="d77f5-134">在 Retail Modern POS 中创建客户订单</span><span class="sxs-lookup"><span data-stu-id="d77f5-134">Create a customer order in Retail Modern POS</span></span>

1.  <span data-ttu-id="d77f5-135">将客户添加到交易记录。</span><span class="sxs-lookup"><span data-stu-id="d77f5-135">Add a customer to the transaction.</span></span>
2.  <span data-ttu-id="d77f5-136">向购物车添加产品</span><span class="sxs-lookup"><span data-stu-id="d77f5-136">Add products to the cart.</span></span>
3.  <span data-ttu-id="d77f5-137">单击**创建客户订单**，然后选择订单类型。</span><span class="sxs-lookup"><span data-stu-id="d77f5-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="d77f5-138">订单类型可以是**客户订单**或**报价**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-138">The order type can be either **Customer order** or **Quote**.</span></span>
4.  <span data-ttu-id="d77f5-139">单击**装运所选产品**或**全部装运**，将产品装运到客户订单中的地址，指定请求的装运日期，然后指定装运费用。</span><span class="sxs-lookup"><span data-stu-id="d77f5-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5.  <span data-ttu-id="d77f5-140">单击**提取所选产品**或**全部提货**，选择将在特定日期从当前商店或其他商店提取的产品。</span><span class="sxs-lookup"><span data-stu-id="d77f5-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6.  <span data-ttu-id="d77f5-141">如果需要保证金，收取保证金。</span><span class="sxs-lookup"><span data-stu-id="d77f5-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="d77f5-142">编辑现有客户订单</span><span class="sxs-lookup"><span data-stu-id="d77f5-142">Edit an existing customer order</span></span>

1.  <span data-ttu-id="d77f5-143">在主页中，单击**查找订单**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-143">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="d77f5-144">查找并选择要编辑的订单。</span><span class="sxs-lookup"><span data-stu-id="d77f5-144">Find and select the order to edit.</span></span> <span data-ttu-id="d77f5-145">在页面底部，单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="d77f5-146">订单拣货</span><span class="sxs-lookup"><span data-stu-id="d77f5-146">Pick up an order</span></span>

1.  <span data-ttu-id="d77f5-147">在主页中，单击**查找订单**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-147">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="d77f5-148">选择要拣货的订单。</span><span class="sxs-lookup"><span data-stu-id="d77f5-148">Select the order to pick up.</span></span> <span data-ttu-id="d77f5-149">在页面底部，单击**领料和装箱**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-149">At the bottom of the page, click **Picking and packing**.</span></span>
3.  <span data-ttu-id="d77f5-150">单击**提货**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="d77f5-151">取消订单</span><span class="sxs-lookup"><span data-stu-id="d77f5-151">Cancel an order</span></span>

1.  <span data-ttu-id="d77f5-152">在主页中，单击**查找订单**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-152">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="d77f5-153">选择要取消的订单。</span><span class="sxs-lookup"><span data-stu-id="d77f5-153">Select the order to cancel.</span></span> <span data-ttu-id="d77f5-154">在页面底部，单击**取消**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-154">At the bottom of the page, click **Cancel**.</span></span>

#### <a name="create-a-return-order"></a><span data-ttu-id="d77f5-155">创建退货单</span><span class="sxs-lookup"><span data-stu-id="d77f5-155">Create a return order</span></span>

1.  <span data-ttu-id="d77f5-156">在主页中，单击**查找订单**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-156">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="d77f5-157">选择要退货的订单，选择订单的发票，然后选择要退货的商品的产品行。</span><span class="sxs-lookup"><span data-stu-id="d77f5-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3.  <span data-ttu-id="d77f5-158">在页面底部，单击**退货单**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="d77f5-159">客户订单的异步交易记录流</span><span class="sxs-lookup"><span data-stu-id="d77f5-159">Asynchronous transaction flow for customer orders</span></span>
<span data-ttu-id="d77f5-160">可以在同步模式或异步模式下，从销售点 (POS) 客户端创建客户订单。</span><span class="sxs-lookup"><span data-stu-id="d77f5-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="d77f5-161">将客户订单设置为可在异步模式下创建</span><span class="sxs-lookup"><span data-stu-id="d77f5-161">Enable customer orders to be created in asynchronous mode</span></span>

1.  <span data-ttu-id="d77f5-162">单击**零售** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **功能配置文件**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-162">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2.  <span data-ttu-id="d77f5-163">在**常规**快速选项卡上，将**在异步模式下创建客户订单**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="d77f5-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="d77f5-164">当**在异步模式下创建客户订单**选项设置为**是**，将始终在异步模式下创建客户订单，即使 Retail Transaction Service (RTS) 可用。</span><span class="sxs-lookup"><span data-stu-id="d77f5-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="d77f5-165">如果将此选项设置为**否**，将始终通过使用 RTS 在同步模式下创建客户订单。</span><span class="sxs-lookup"><span data-stu-id="d77f5-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="d77f5-166">在异步模式下创建客户订单时，将通过提取 (P) 作业提取客户订单并插入到 Retail 中。</span><span class="sxs-lookup"><span data-stu-id="d77f5-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Retail by Pull (P) jobs.</span></span> <span data-ttu-id="d77f5-167">手动或通过批处理流程运行**同步订单**时，将在 Retail 中创建相应销售订单。</span><span class="sxs-lookup"><span data-stu-id="d77f5-167">The corresponding sales orders are created in Retail when **Synchronize orders** is run either manually or through a batch process.</span></span>

<a name="see-also"></a><span data-ttu-id="d77f5-168">请参阅</span><span class="sxs-lookup"><span data-stu-id="d77f5-168">See also</span></span>
--------

[<span data-ttu-id="d77f5-169">混合客户订单</span><span class="sxs-lookup"><span data-stu-id="d77f5-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)




