---
title: Modern POS (MPOS) 中的客户订单
description: 此主题提供有 Modern POS (MPOS) 中的客户订单的信息。 客户订单也称为特殊订单。 此主题中包含对相关参数和交易记录流的讨论。
author: josaw1
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
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
ms.openlocfilehash: 87d1217204e0c5cb22f567793b043bf399ca5685
ms.sourcegitcommit: b07434f2bd6db67d8dd712f096329acc902751ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/18/2020
ms.locfileid: "3699361"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="2fff2-105">Modern POS (MPOS) 中的客户订单</span><span class="sxs-lookup"><span data-stu-id="2fff2-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2fff2-106">此主题提供有 Modern POS (MPOS) 中的客户订单的信息。</span><span class="sxs-lookup"><span data-stu-id="2fff2-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="2fff2-107">客户订单也称为特殊订单。</span><span class="sxs-lookup"><span data-stu-id="2fff2-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="2fff2-108">此主题中包含对相关参数和交易记录流的讨论。</span><span class="sxs-lookup"><span data-stu-id="2fff2-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="2fff2-109">在全渠道商业环境中，许多零售商提供客户订单（即特殊订单）选项，以满足各种产品和履行要求。</span><span class="sxs-lookup"><span data-stu-id="2fff2-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="2fff2-110">下面是一些典型方案：</span><span class="sxs-lookup"><span data-stu-id="2fff2-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="2fff2-111">客户希望将产品在特定日期发到特定地址。</span><span class="sxs-lookup"><span data-stu-id="2fff2-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="2fff2-112">客户希望从非购买产品的商店或位置取货。</span><span class="sxs-lookup"><span data-stu-id="2fff2-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="2fff2-113">客户希望其他人取自己购买的产品。</span><span class="sxs-lookup"><span data-stu-id="2fff2-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="2fff2-114">零售商也可以使用客户订单将库存不足可能导致的失单降到最低，因为可以在其他时间或位置发货或取货。</span><span class="sxs-lookup"><span data-stu-id="2fff2-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="2fff2-115">设置客户订单</span><span class="sxs-lookup"><span data-stu-id="2fff2-115">Set up customer orders</span></span>

<span data-ttu-id="2fff2-116">下面是一些可在**商业参数**页面中设置来定义如何履行客户订单的参数。</span><span class="sxs-lookup"><span data-stu-id="2fff2-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="2fff2-117">**默认保证金百分比** – 指定确认订单前客户必须以存款的形式支付的金额。</span><span class="sxs-lookup"><span data-stu-id="2fff2-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="2fff2-118">默认保证金金额为订单值的百分比。</span><span class="sxs-lookup"><span data-stu-id="2fff2-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="2fff2-119">售货员可能可以根据其权限通过使用**保证金覆盖**来覆盖该金额。</span><span class="sxs-lookup"><span data-stu-id="2fff2-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="2fff2-120">**取消费百分比** – 如果取消客户订单时需要收取费用，请指定这笔费用的金额。</span><span class="sxs-lookup"><span data-stu-id="2fff2-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="2fff2-121">**取消费代码** – 如果取消客户订单时需要收取费用，将在销售订单内的收费代码下体现这笔费用。</span><span class="sxs-lookup"><span data-stu-id="2fff2-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="2fff2-122">可使用此参数定义取消费代码。</span><span class="sxs-lookup"><span data-stu-id="2fff2-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="2fff2-123">**装运费用代码** – 零售商可为将商品装运到客户再收取一笔费用。</span><span class="sxs-lookup"><span data-stu-id="2fff2-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="2fff2-124">销售订单内的收费代码下将体现这笔装运费用的金额。</span><span class="sxs-lookup"><span data-stu-id="2fff2-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="2fff2-125">可使用此参数将装运费用代码映射到客户订单中的装运费用。</span><span class="sxs-lookup"><span data-stu-id="2fff2-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="2fff2-126">**退回装运费用** – 指定是否可退回客户订单关联的装运费用。</span><span class="sxs-lookup"><span data-stu-id="2fff2-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="2fff2-127">**未经审核的最大金额** – 如果装运费用可退回，指定退货单中的最大装运费用退款金额。</span><span class="sxs-lookup"><span data-stu-id="2fff2-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="2fff2-128">如果超过了此金额，需要经历覆盖才能继续退款。</span><span class="sxs-lookup"><span data-stu-id="2fff2-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="2fff2-129">为了满足以下方案，装运费用的退款可能超过最初支付的金额。</span><span class="sxs-lookup"><span data-stu-id="2fff2-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="2fff2-130">费用在销售订单抬头级别实施，并且如果退回了某个产品行的一定数量，则不能按照适合所有客户的方式确定为这些产品和数量允许的最大装运费用退款。</span><span class="sxs-lookup"><span data-stu-id="2fff2-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="2fff2-131">每次运货都会产生装运费用。</span><span class="sxs-lookup"><span data-stu-id="2fff2-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="2fff2-132">如果客户多次退货，而零售商的政策规定由零售商承担退货装运费用的成本，退货装运费用将超过实际装运费用。</span><span class="sxs-lookup"><span data-stu-id="2fff2-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>
    
- <span data-ttu-id="2fff2-133">**税款计算行为** - **重新计算**是将订单导入后端办公系统后如何重新计算税款的默认和传统设置。</span><span class="sxs-lookup"><span data-stu-id="2fff2-133">**Tax calculation behavior** - **Recalculate** is the default and traditional setting for how taxes are recalculated when the order is imported into the back office.</span></span> <span data-ttu-id="2fff2-134">当触发重新计算时，**不重新计算**将禁用税款重新计算，直到或除非在后端办公系统中编辑了订单。</span><span class="sxs-lookup"><span data-stu-id="2fff2-134">**Don't recalculate** disables tax recalculation until or unless the order is edited in the back office, when recalculation is triggered.</span></span> 

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="2fff2-135">客户订单的交易记录流</span><span class="sxs-lookup"><span data-stu-id="2fff2-135">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="2fff2-136">在现代 POS 中创建客户订单</span><span class="sxs-lookup"><span data-stu-id="2fff2-136">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="2fff2-137">将客户添加到交易记录。</span><span class="sxs-lookup"><span data-stu-id="2fff2-137">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="2fff2-138">向购物车添加产品</span><span class="sxs-lookup"><span data-stu-id="2fff2-138">Add products to the cart.</span></span>
3. <span data-ttu-id="2fff2-139">单击**创建客户订单**，然后选择订单类型。</span><span class="sxs-lookup"><span data-stu-id="2fff2-139">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="2fff2-140">订单类型可以是**客户订单**或**报价**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-140">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="2fff2-141">单击**装运所选产品**或**全部装运**，将产品装运到客户订单中的地址，指定请求的装运日期，然后指定装运费用。</span><span class="sxs-lookup"><span data-stu-id="2fff2-141">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="2fff2-142">单击**提取所选产品**或**全部提货**，选择将在特定日期从当前商店或其他商店提取的产品。</span><span class="sxs-lookup"><span data-stu-id="2fff2-142">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="2fff2-143">如果需要保证金，收取保证金。</span><span class="sxs-lookup"><span data-stu-id="2fff2-143">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="2fff2-144">编辑现有客户订单</span><span class="sxs-lookup"><span data-stu-id="2fff2-144">Edit an existing customer order</span></span>

1. <span data-ttu-id="2fff2-145">在主页中，单击**查找订单**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-145">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2fff2-146">查找并选择要编辑的订单。</span><span class="sxs-lookup"><span data-stu-id="2fff2-146">Find and select the order to edit.</span></span> <span data-ttu-id="2fff2-147">在页面底部，单击**编辑**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-147">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="2fff2-148">订单拣货</span><span class="sxs-lookup"><span data-stu-id="2fff2-148">Pick up an order</span></span>

1. <span data-ttu-id="2fff2-149">在主页中，单击**查找订单**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-149">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2fff2-150">选择要拣货的订单。</span><span class="sxs-lookup"><span data-stu-id="2fff2-150">Select the order to pick up.</span></span> <span data-ttu-id="2fff2-151">在页面底部，单击**领料和装箱**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-151">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="2fff2-152">单击**提货**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-152">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="2fff2-153">取消订单</span><span class="sxs-lookup"><span data-stu-id="2fff2-153">Cancel an order</span></span>

1. <span data-ttu-id="2fff2-154">在主页中，单击**查找订单**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-154">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2fff2-155">选择要取消的订单。</span><span class="sxs-lookup"><span data-stu-id="2fff2-155">Select the order to cancel.</span></span> <span data-ttu-id="2fff2-156">在页面底部，单击**取消**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-156">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="2fff2-157">创建退货单</span><span class="sxs-lookup"><span data-stu-id="2fff2-157">Create a return order</span></span>

1. <span data-ttu-id="2fff2-158">在主页中，单击**查找订单**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-158">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="2fff2-159">选择要退货的订单，选择订单的发票，然后选择要退货的商品的产品行。</span><span class="sxs-lookup"><span data-stu-id="2fff2-159">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="2fff2-160">在页面底部，单击**退货单**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-160">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="2fff2-161">客户订单的异步交易记录流</span><span class="sxs-lookup"><span data-stu-id="2fff2-161">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="2fff2-162">可以在同步模式或异步模式下，从销售点 (POS) 客户端创建客户订单。</span><span class="sxs-lookup"><span data-stu-id="2fff2-162">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="2fff2-163">将客户订单设置为可在异步模式下创建</span><span class="sxs-lookup"><span data-stu-id="2fff2-163">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="2fff2-164">单击 **Retail 和 Commerce** &gt; **渠道设置** &gt; **POS 设置** &gt; **POS 配置文件** &gt; **功能配置文件**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-164">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="2fff2-165">在**常规**快速选项卡上，将**在异步模式下创建客户订单**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="2fff2-165">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="2fff2-166">当**在异步模式下创建客户订单**选项设置为**是**，将始终在异步模式下创建客户订单，即使 Retail Transaction Service (RTS) 可用。</span><span class="sxs-lookup"><span data-stu-id="2fff2-166">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="2fff2-167">如果将此选项设置为**否**，将始终通过使用 RTS 在同步模式下创建客户订单。</span><span class="sxs-lookup"><span data-stu-id="2fff2-167">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="2fff2-168">在异步模式下创建客户订单时，将通过提取 (P) 作业提取客户订单并插入到 Commerce 中。</span><span class="sxs-lookup"><span data-stu-id="2fff2-168">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="2fff2-169">手动或通过批处理流程运行**同步订单**时，将创建相应销售订单。</span><span class="sxs-lookup"><span data-stu-id="2fff2-169">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2fff2-170">其他资源</span><span class="sxs-lookup"><span data-stu-id="2fff2-170">Additional resources</span></span>

[<span data-ttu-id="2fff2-171">混合客户订单</span><span class="sxs-lookup"><span data-stu-id="2fff2-171">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
