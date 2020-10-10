---
title: 结帐模块
description: 此主题介绍如何向页面添加结帐模块和设置必需的属性。
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8439b88ccda3f72e5a9b918c6c89bd406599b516
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818218"
---
# <a name="checkout-module"></a><span data-ttu-id="1339f-103">结帐模块</span><span class="sxs-lookup"><span data-stu-id="1339f-103">Checkout module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1339f-104">此主题介绍如何向页面添加结帐模块和设置必需的属性。</span><span class="sxs-lookup"><span data-stu-id="1339f-104">This topic describes how to add a checkout module to a page and set the required properties.</span></span>

## <a name="overview"></a><span data-ttu-id="1339f-105">概览</span><span class="sxs-lookup"><span data-stu-id="1339f-105">Overview</span></span>

<span data-ttu-id="1339f-106">结帐模块是承载创建订单所需全部模块的特殊容器。</span><span class="sxs-lookup"><span data-stu-id="1339f-106">A checkout module is a special container that hosts all modules that are required to create an order.</span></span> <span data-ttu-id="1339f-107">它提供分步流程，供客户输入与采购有关的所有信息。</span><span class="sxs-lookup"><span data-stu-id="1339f-107">It presents a step-by-step flow that a customer uses to enter all the relevant information to make a purchase.</span></span> <span data-ttu-id="1339f-108">它捕获送货地址、送货方式和帐单信息。</span><span class="sxs-lookup"><span data-stu-id="1339f-108">It captures the shipping address, shipping method, and billing information.</span></span> <span data-ttu-id="1339f-109">它还提供订单摘要以及与客户订单相关的其他信息。</span><span class="sxs-lookup"><span data-stu-id="1339f-109">It also provides an order summary and other information that is related to a customer order.</span></span>

<span data-ttu-id="1339f-110">结帐模块基于购物车 ID 显示数据。</span><span class="sxs-lookup"><span data-stu-id="1339f-110">A checkout module renders data based on the cart ID.</span></span> <span data-ttu-id="1339f-111">此购物车 ID 保存为浏览器 cookie。</span><span class="sxs-lookup"><span data-stu-id="1339f-111">This cart ID is saved as a browser cookie.</span></span> <span data-ttu-id="1339f-112">需要购物车 ID 才能在结帐模块中显示信息，如订单中的项、总量和折扣。</span><span class="sxs-lookup"><span data-stu-id="1339f-112">A cart ID is required to render information in the checkout module, such as the items in the order, the total amount, and discounts.</span></span> 

<span data-ttu-id="1339f-113">下图显示了结帐页上的 Fabrikam 结帐模块的示例。</span><span class="sxs-lookup"><span data-stu-id="1339f-113">The following image shows an example of a Fabrikam checkout module on a checkout page.</span></span>

![结帐模块的示例](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a><span data-ttu-id="1339f-115">结帐模块属性</span><span class="sxs-lookup"><span data-stu-id="1339f-115">Checkout module properties</span></span>

<span data-ttu-id="1339f-116">结帐模块显示订单摘要，并提供下达订单的功能。</span><span class="sxs-lookup"><span data-stu-id="1339f-116">A checkout module shows an order summary and provides the functionality for placing an order.</span></span> <span data-ttu-id="1339f-117">为了收集下达订单之前所需的所有客户信息，必须将其他模块添加到结帐模块。</span><span class="sxs-lookup"><span data-stu-id="1339f-117">To gather all the customer information that is required before an order can be placed, additional modules must be added to the checkout module.</span></span> <span data-ttu-id="1339f-118">因此，零售商可以根据自己的需求灵活地将自定义模块添加到结帐流程，或排除模块。</span><span class="sxs-lookup"><span data-stu-id="1339f-118">Therefore, retailers have the flexibility to add custom modules to the checkout flow, or to exclude modules, based on their requirements.</span></span>

| <span data-ttu-id="1339f-119">属性名称</span><span class="sxs-lookup"><span data-stu-id="1339f-119">Property name</span></span> | <span data-ttu-id="1339f-120">值</span><span class="sxs-lookup"><span data-stu-id="1339f-120">Values</span></span> | <span data-ttu-id="1339f-121">说明</span><span class="sxs-lookup"><span data-stu-id="1339f-121">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="1339f-122">结帐标题</span><span class="sxs-lookup"><span data-stu-id="1339f-122">Checkout heading</span></span> | <span data-ttu-id="1339f-123">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="1339f-123">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1339f-124">结帐模块的标题。</span><span class="sxs-lookup"><span data-stu-id="1339f-124">A heading for the checkout module.</span></span> |
| <span data-ttu-id="1339f-125">订单汇总标题</span><span class="sxs-lookup"><span data-stu-id="1339f-125">Order summary heading</span></span> | <span data-ttu-id="1339f-126">标题文本</span><span class="sxs-lookup"><span data-stu-id="1339f-126">Heading text</span></span> | <span data-ttu-id="1339f-127">模块订单摘要部分的标题。</span><span class="sxs-lookup"><span data-stu-id="1339f-127">A heading for the order summary section of the module.</span></span> |
| <span data-ttu-id="1339f-128">购物车行项标题</span><span class="sxs-lookup"><span data-stu-id="1339f-128">Cart line items heading</span></span> | <span data-ttu-id="1339f-129">标题文本</span><span class="sxs-lookup"><span data-stu-id="1339f-129">Heading text</span></span> | <span data-ttu-id="1339f-130">结帐模块中显示的购物车行项的标题。</span><span class="sxs-lookup"><span data-stu-id="1339f-130">A heading for cart line items that are shown in the checkout module.</span></span> |
| <span data-ttu-id="1339f-131">在行项上显示装运费用</span><span class="sxs-lookup"><span data-stu-id="1339f-131">Show shipping charges on line item</span></span> | <span data-ttu-id="1339f-132">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="1339f-132">**True** or **False**</span></span> | <span data-ttu-id="1339f-133">如果将此属性设置为 **True**，适用于行项的装运费用将显示在购物车行上。</span><span class="sxs-lookup"><span data-stu-id="1339f-133">If this property is set to **True**, the shipping charges that are applicable for line items will be shown on cart lines.</span></span> <span data-ttu-id="1339f-134">如果在 Commerce headquarters 中打开了**不按比例的标题费用**功能，装运费用将在标题级别而不是行级别应用。</span><span class="sxs-lookup"><span data-stu-id="1339f-134">If the **Header charge with no proration** feature is turned on in Commerce headquarters, the shipping charge will be applied at the header level, not the line level.</span></span> <span data-ttu-id="1339f-135">Commerce 版本 10.0.13 中添加了此功能。</span><span class="sxs-lookup"><span data-stu-id="1339f-135">This feature was added in Commerce version 10.0.13.</span></span> |

## <a name="modules-that-can-be-used-in-the-checkout-module"></a><span data-ttu-id="1339f-136">结帐模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="1339f-136">Modules that can be used in the checkout module</span></span>

- <span data-ttu-id="1339f-137">**装运地址** – 客户可使用此模块为订单添加或选择装运地址。</span><span class="sxs-lookup"><span data-stu-id="1339f-137">**Shipping address** – This module lets a customer add or select the shipping address for an order.</span></span> <span data-ttu-id="1339f-138">有关此模块的详细信息，请参阅[装运地址模块](ship-address-module.md)。</span><span class="sxs-lookup"><span data-stu-id="1339f-138">For more information about this module, see [Shipping address module](ship-address-module.md).</span></span>

    <span data-ttu-id="1339f-139">下图显示了结帐页上的装运地址模块的示例。</span><span class="sxs-lookup"><span data-stu-id="1339f-139">The following image shows an example of a shipping address module on a checkout page.</span></span>

    ![装运地址模块示例](./media/ecommerce-shippingaddress.PNG)

- <span data-ttu-id="1339f-141">**交货选项** – 客户可使用此模块为订单选择交货方式。</span><span class="sxs-lookup"><span data-stu-id="1339f-141">**Delivery options** – This module lets a customer select a mode of delivery for an order.</span></span> <span data-ttu-id="1339f-142">有关此模块的详细信息，请参阅[交货选项模块](delivery-options-module.md)。</span><span class="sxs-lookup"><span data-stu-id="1339f-142">For more information about this module, see [Delivery options module](delivery-options-module.md).</span></span>

    <span data-ttu-id="1339f-143">下图显示了结帐页上的交货选项模块的示例。</span><span class="sxs-lookup"><span data-stu-id="1339f-143">The following image shows an example of a delivery options module on a checkout page.</span></span>
 
    ![交付选项模块示例](./media/ecommerce-deliveryoptions.PNG)

- <span data-ttu-id="1339f-145">**结帐分区容器** – 此模块是可在其中放置多个模块以在结帐流程中创建分区的容器。</span><span class="sxs-lookup"><span data-stu-id="1339f-145">**Checkout section container** – This module is a container that you can put multiple modules inside to create a section within the checkout flow.</span></span> <span data-ttu-id="1339f-146">例如，可以将所有与付款有关的模块放在此容器内，以便使其显示为一个分区。</span><span class="sxs-lookup"><span data-stu-id="1339f-146">For example, you can put all payment-related modules inside this container to make them appear as one section.</span></span> <span data-ttu-id="1339f-147">此模块仅影响流程的布局。</span><span class="sxs-lookup"><span data-stu-id="1339f-147">This module affects only the layout of the flow.</span></span>

- <span data-ttu-id="1339f-148">**礼品卡** – 客户可通过此模块使用礼品卡支付订单。</span><span class="sxs-lookup"><span data-stu-id="1339f-148">**Gift card** – This module lets a customer pay for an order by using a gift card.</span></span> <span data-ttu-id="1339f-149">有关此模块的详细信息，请参阅[礼品卡模块](add-giftcard.md)。</span><span class="sxs-lookup"><span data-stu-id="1339f-149">For more information about this module, see [Gift card module](add-giftcard.md).</span></span>

- <span data-ttu-id="1339f-150">**积分** – 客户可通过此模块使用积分支付订单。</span><span class="sxs-lookup"><span data-stu-id="1339f-150">**Loyalty points** – This module lets a customer pay for an order by using loyalty points.</span></span> <span data-ttu-id="1339f-151">它提供可用积分和到期积分的摘要，并可供客户选择要兑换的积分数。</span><span class="sxs-lookup"><span data-stu-id="1339f-151">It provides a summary of available points and expiring points, and lets the customer select the number of points to redeem.</span></span> <span data-ttu-id="1339f-152">如果客户未登录或不是会员，或者如果购物车中的总金额为 0（零），将自动隐藏此模块。</span><span class="sxs-lookup"><span data-stu-id="1339f-152">If the customer isn't signed in or isn't a loyalty member, or if the total amount in the cart is 0 (zero), this module is automatically hidden.</span></span>

- <span data-ttu-id="1339f-153">**付款** – 客户可通过此模块使用信用卡或借记卡支付订单。</span><span class="sxs-lookup"><span data-stu-id="1339f-153">**Payment** – This module lets a customer pay for an order by using a credit or debit card.</span></span> <span data-ttu-id="1339f-154">客户还可以为其选择的付款方式提供账单地址。</span><span class="sxs-lookup"><span data-stu-id="1339f-154">Customers can also provide a billing address for the payment option that they select.</span></span> <span data-ttu-id="1339f-155">有关此模块的详细信息，请参阅[付款模块](payment-module.md)。</span><span class="sxs-lookup"><span data-stu-id="1339f-155">For more information about this module, see [Payment module](payment-module.md).</span></span>

    <span data-ttu-id="1339f-156">下图显示了结帐页面上的礼品卡、会员积分和付款模块的示例。</span><span class="sxs-lookup"><span data-stu-id="1339f-156">The following image shows an example of gift card, loyalty points, and payment modules on a checkout page.</span></span>

    ![结帐页面上的礼品卡、会员积分和付款模块的示例](./media/ecommerce-payments.PNG)

- <span data-ttu-id="1339f-158">**联系信息** – 此模块可供客户为订单添加或更改联系信息（电子邮件地址）。</span><span class="sxs-lookup"><span data-stu-id="1339f-158">**Contact information** – This module lets a customer add or change the contact information (email address) for an order.</span></span>

- <span data-ttu-id="1339f-159">**文本块** – 此模块中包含内容管理系统 (CMS) 驱动的所有消息。</span><span class="sxs-lookup"><span data-stu-id="1339f-159">**Text block** – This module contains any messaging that is driven by the content management system (CMS).</span></span> <span data-ttu-id="1339f-160">例如，可能包含消息“订单问题请致电 1-800-Fabrikam”。</span><span class="sxs-lookup"><span data-stu-id="1339f-160">For example, it might contain a message that states, "For issues with your order, contact 1-800-Fabrikam."</span></span> 

- <span data-ttu-id="1339f-161">**结帐条款和条件** – 此模块显示富文本，其中包含条款和条件以及一个供客户输入的复选框。</span><span class="sxs-lookup"><span data-stu-id="1339f-161">**Checkout terms and conditions** – This module shows rich text that contains the terms and conditions and a check box for the customer input.</span></span> <span data-ttu-id="1339f-162">此复选框是可选的并且可以配置。</span><span class="sxs-lookup"><span data-stu-id="1339f-162">The check box is optional and configurable.</span></span> <span data-ttu-id="1339f-163">输入由模块捕获，可以用作触发订单下达之前的检查，但不会包含在订单摘要信息中。</span><span class="sxs-lookup"><span data-stu-id="1339f-163">The input is captured by the module and can be used as a check before order placement is triggered, but it isn't included in the order summary information.</span></span> <span data-ttu-id="1339f-164">可以根据业务需要将此模块添加到结帐容器、结帐部分容器或条款和条件插槽中。</span><span class="sxs-lookup"><span data-stu-id="1339f-164">This module can be added to the checkout container, checkout section container, or terms and conditions slot, according to business needs.</span></span> <span data-ttu-id="1339f-165">如果将其添加到结帐容器或结帐部分容器插槽中，它将显示为结帐流程中的一个步骤。</span><span class="sxs-lookup"><span data-stu-id="1339f-165">If it's added to the checkout container or checkout section container slot, it will appear as a step in the checkout process.</span></span> <span data-ttu-id="1339f-166">如果将其添加到条款和条件插槽中，它将显示在订单下达按钮附近。</span><span class="sxs-lookup"><span data-stu-id="1339f-166">If it's added to the terms and conditions slot, it will appear near the order placement button.</span></span>

    <span data-ttu-id="1339f-167">下图显示了结帐页上的条款和条件的示例。</span><span class="sxs-lookup"><span data-stu-id="1339f-167">The following image shows an example of terms and conditions on a checkout page.</span></span>

    ![结帐页上条款和条件的示例](./media/ecommerce-checkout-terms.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="1339f-169">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="1339f-169">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="1339f-170">大多数结帐信息（如装运地址和装运方式）存储在购物车中，并作为订单的一部分处理。</span><span class="sxs-lookup"><span data-stu-id="1339f-170">Most of the checkout information, such as the shipping address and shipping method, is stored in the cart and processed as part of the order.</span></span> <span data-ttu-id="1339f-171">唯一例外是信用卡信息。</span><span class="sxs-lookup"><span data-stu-id="1339f-171">The only exception is the credit card information.</span></span> <span data-ttu-id="1339f-172">此信息直接使用 Adyen 付款连接器处理。</span><span class="sxs-lookup"><span data-stu-id="1339f-172">This information is processed directly by using the Adyen payment connector.</span></span> <span data-ttu-id="1339f-173">此付款已被授权，但在履行订单之前不会扣费。</span><span class="sxs-lookup"><span data-stu-id="1339f-173">The payment is authorized, but it isn't charged until the order is fulfilled.</span></span>

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a><span data-ttu-id="1339f-174">向页面添加结帐模块和设置必需的属性</span><span class="sxs-lookup"><span data-stu-id="1339f-174">Add a checkout module to a page and set the required properties</span></span>

<span data-ttu-id="1339f-175">若要向新页面添加结帐模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1339f-175">To add a checkout module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1339f-176">转到**片段**，选择**新建**创建新片段。</span><span class="sxs-lookup"><span data-stu-id="1339f-176">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="1339f-177">在**新建片段**对话框中，选择**结帐**模块。</span><span class="sxs-lookup"><span data-stu-id="1339f-177">In the **New fragment** dialog box, select the **Checkout** module.</span></span>
1. <span data-ttu-id="1339f-178">在**片段名称**下，输入名称**结帐片段**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1339f-178">Under **Fragment name**, enter the name **Checkout fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="1339f-179">选择**结帐模块**插槽。</span><span class="sxs-lookup"><span data-stu-id="1339f-179">Select the **Checkout module** slot.</span></span>
1. <span data-ttu-id="1339f-180">在右侧的属性窗格中，选择铅笔符号，在字段中输入标题文本，然后选择复选标记符号。</span><span class="sxs-lookup"><span data-stu-id="1339f-180">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="1339f-181">在**结帐信息**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="1339f-181">In the **Checkout Information** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1339f-182">在**添加模块**对话框中，选择**装运地址**、**交付选项**、**结帐部分容器**和**联系人信息**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1339f-182">In the **Add Module** dialog box, select the **Shipping address**, **Delivery options**, **Checkout section container**, and **Contact information** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="1339f-183">在**结帐部分容器**模块，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="1339f-183">In the **Checkout section container** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1339f-184">在**添加模块**对话框中，选择**礼品卡**、**会员**和**付款**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="1339f-184">In the **Add Module** dialog box, select the **Gift card**, **Loyalty**, and **Payment** modules, and then select **OK**.</span></span> <span data-ttu-id="1339f-185">这样，就可以确保所有付款方式在一个分区中一起显示。</span><span class="sxs-lookup"><span data-stu-id="1339f-185">In this way, you make sure that all the payment methods appear together in a section.</span></span>
1. <span data-ttu-id="1339f-186">如果需要，在**条款和条件**插槽中添加**结帐条款和条件**模块。</span><span class="sxs-lookup"><span data-stu-id="1339f-186">In the **Terms and conditions** slot, add a **Checkout terms and conditions** module if it's required.</span></span> <span data-ttu-id="1339f-187">在模块的属性窗格中，根据需要配置条款和条件文本。</span><span class="sxs-lookup"><span data-stu-id="1339f-187">In the module's properties pane, configure the terms and condition text as appropriate.</span></span>
1. <span data-ttu-id="1339f-188">选择**保存**，然后选择**预览**预览片段。</span><span class="sxs-lookup"><span data-stu-id="1339f-188">Select **Save**, and then select **Preview** to preview the fragment.</span></span> <span data-ttu-id="1339f-189">预览中可能不显示某些没有购物车上下文的模块。</span><span class="sxs-lookup"><span data-stu-id="1339f-189">Some modules that don't have a cart context might not be rendered in the preview.</span></span>
1. <span data-ttu-id="1339f-190">选择**完成编辑**签入片段，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="1339f-190">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="1339f-191">创建一个使用新结帐片段的模板。</span><span class="sxs-lookup"><span data-stu-id="1339f-191">Create a template that uses the new checkout fragment.</span></span>
1. <span data-ttu-id="1339f-192">创建一个使用新模板的结帐页。</span><span class="sxs-lookup"><span data-stu-id="1339f-192">Create a checkout page that uses the new template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1339f-193">其他资源</span><span class="sxs-lookup"><span data-stu-id="1339f-193">Additional resources</span></span>

[<span data-ttu-id="1339f-194">购物车模块</span><span class="sxs-lookup"><span data-stu-id="1339f-194">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1339f-195">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="1339f-195">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="1339f-196">付款模块</span><span class="sxs-lookup"><span data-stu-id="1339f-196">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="1339f-197">装运地址模块</span><span class="sxs-lookup"><span data-stu-id="1339f-197">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="1339f-198">交货选项模块</span><span class="sxs-lookup"><span data-stu-id="1339f-198">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="1339f-199">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="1339f-199">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1339f-200">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="1339f-200">Gift card module</span></span>](add-giftcard.md)
