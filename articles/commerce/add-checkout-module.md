---
title: 结帐模块
description: 此主题介绍如何向页面添加结帐模块和设置必需的属性。
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: bd1d66fc39872019fc38dbbfb56dc3015d57d0dd
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411176"
---
# <a name="checkout-module"></a><span data-ttu-id="4c0a4-103">结帐模块</span><span class="sxs-lookup"><span data-stu-id="4c0a4-103">Checkout module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4c0a4-104">此主题介绍如何向页面添加结帐模块和设置必需的属性。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-104">This topic describes how to add a checkout module to a page and set the required properties.</span></span>

## <a name="overview"></a><span data-ttu-id="4c0a4-105">概览</span><span class="sxs-lookup"><span data-stu-id="4c0a4-105">Overview</span></span>

<span data-ttu-id="4c0a4-106">结帐模块是承载创建订单所需全部模块的特殊容器。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-106">A checkout module is a special container that hosts all modules that are required to create an order.</span></span> <span data-ttu-id="4c0a4-107">它提供分步流程，供客户输入与采购有关的所有信息。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-107">It presents a step-by-step flow that a customer uses to enter all the relevant information to make a purchase.</span></span> <span data-ttu-id="4c0a4-108">它捕获送货地址、送货方式和帐单信息。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-108">It captures the shipping address, shipping method, and billing information.</span></span> <span data-ttu-id="4c0a4-109">它还提供订单摘要以及与客户订单相关的其他信息。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-109">It also provides an order summary and other information that is related to a customer order.</span></span>

<span data-ttu-id="4c0a4-110">结帐模块基于购物车 ID 显示数据。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-110">A checkout module renders data based on the cart ID.</span></span> <span data-ttu-id="4c0a4-111">此购物车 ID 保存为浏览器 cookie。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-111">This cart ID is saved as a browser cookie.</span></span> <span data-ttu-id="4c0a4-112">需要购物车 ID 才能在结帐模块中显示信息，如订单中的项、总量和折扣。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-112">A cart ID is required to render information in the checkout module, such as the items in the order, the total amount, and discounts.</span></span> 

<span data-ttu-id="4c0a4-113">下图显示了结帐页上的 Fabrikam 结帐模块的示例。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-113">The following image shows an example of a Fabrikam checkout module on a checkout page.</span></span>

![结帐模块的示例](./media/Checkout.PNG)

## <a name="checkout-module-properties"></a><span data-ttu-id="4c0a4-115">结帐模块属性</span><span class="sxs-lookup"><span data-stu-id="4c0a4-115">Checkout module properties</span></span>

<span data-ttu-id="4c0a4-116">结帐模块显示订单摘要，并提供下达订单的功能。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-116">A checkout module shows an order summary and provides the functionality for placing an order.</span></span> <span data-ttu-id="4c0a4-117">为了收集下达订单之前所需的所有客户信息，必须将其他模块添加到结帐模块。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-117">To gather all the customer information that is required before an order can be placed, additional modules must be added to the checkout module.</span></span> <span data-ttu-id="4c0a4-118">因此，零售商可以根据自己的需求灵活地将自定义模块添加到结帐流程，或排除模块。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-118">Therefore, retailers have the flexibility to add custom modules to the checkout flow, or to exclude modules, based on their requirements.</span></span>

### <a name="modules-that-can-be-used-in-the-checkout-module"></a><span data-ttu-id="4c0a4-119">结帐模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="4c0a4-119">Modules that can be used in the checkout module</span></span>

- <span data-ttu-id="4c0a4-120">**装运地址** – 客户可使用此模块为订单添加或选择装运地址。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-120">**Shipping address** – This module lets a customer add or select the shipping address for an order.</span></span> <span data-ttu-id="4c0a4-121">如果客户已登录，则显示以前为该客户保存的所有地址。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-121">If the customer is signed in, any addresses that were previously saved for that customer are shown.</span></span> <span data-ttu-id="4c0a4-122">然后，客户可在这些地址中进行选择。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-122">The customer can then select among those addresses.</span></span> <span data-ttu-id="4c0a4-123">客户也可以添加新地址。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-123">The customer can also add a new address.</span></span> <span data-ttu-id="4c0a4-124">装运地址用于订单中需要装运的所有项。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-124">The shipping address is used for all the items in the order that require shipping.</span></span> <span data-ttu-id="4c0a4-125">不能针对单个明细项进行自定义。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-125">It can't be customized for individual line items.</span></span> <span data-ttu-id="4c0a4-126">将针对每个国家或地区定义装运地址格式，而该模块则实施国家/地区特定的规则。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-126">Shipping address formats are defined for each country or region, and the country/region-specific rules are enforced by this module.</span></span> <span data-ttu-id="4c0a4-127">虽然此模块不提供地址验证，但是可以通过自定义设置来实施地址验证。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-127">Although this module doesn't provide address validation, address validation can be implemented through customization.</span></span> <span data-ttu-id="4c0a4-128">如果订单中仅包含将在商店提货的项，则自动隐藏此模块。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-128">If the order includes only items that will be picked up in the store, this module is automatically hidden.</span></span>

    <span data-ttu-id="4c0a4-129">下图显示了结帐页上的装运地址模块的示例。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-129">The following image shows an example of a shipping address module on a checkout page.</span></span>

    ![装运地址模块示例](./media/ecommerce-shippingaddress.PNG)

- <span data-ttu-id="4c0a4-131">**交货选项** – 客户可使用此模块为订单选择交货选项。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-131">**Delivery options** – This module lets a customer select a delivery option for an order.</span></span> <span data-ttu-id="4c0a4-132">交货选项基于装运地址。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-132">Delivery options are based on the shipping address.</span></span> <span data-ttu-id="4c0a4-133">如果更改装运地址，则必须重新检索交货选项。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-133">If the shipping address is changed, the delivery options must be retrieved again.</span></span> <span data-ttu-id="4c0a4-134">如果订单中仅包含将在商店提货的项，则自动隐藏此模块。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-134">If the order includes only items that will be picked up in the store, this module is automatically hidden.</span></span>

    <span data-ttu-id="4c0a4-135">下图显示了结帐页上的交货选项模块的示例。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-135">The following image shows an example of a delivery options module on a checkout page.</span></span>

    ![交付选项模块示例](./media/ecommerce-deliveryoptions.PNG)

- <span data-ttu-id="4c0a4-137">**结帐分区容器** – 此模块是可在其中放置多个模块以在结帐流程中创建分区的容器。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-137">**Checkout section container** – This module is a container that you can put multiple modules inside to create a section within the checkout flow.</span></span> <span data-ttu-id="4c0a4-138">例如，可以将所有与付款有关的模块放在此容器内，以便使其显示为一个分区。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-138">For example, you can put all payment-related modules inside this container to make them appear as one section.</span></span> <span data-ttu-id="4c0a4-139">此模块仅影响流程的布局。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-139">This module affects only the layout of the flow.</span></span>
- <span data-ttu-id="4c0a4-140">**礼品卡** – 客户可通过此模块使用礼品卡支付订单。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-140">**Gift card** – This module lets a customer pay for an order by using a gift card.</span></span> <span data-ttu-id="4c0a4-141">它仅支持 Microsoft Dynamics 365 Commerce 礼品卡。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-141">It supports only Microsoft Dynamics 365 Commerce gift cards.</span></span> <span data-ttu-id="4c0a4-142">可以为一个订单应用一张或多张礼品卡。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-142">One or more gift cards can be applied to an order.</span></span> <span data-ttu-id="4c0a4-143">如果礼品卡的余额不足以支付购物车中的金额，可以将礼品卡与其他付款方式结合使用。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-143">If the balance of the gift card doesn't cover the amount in the cart, the gift card can be combined with another payment method.</span></span> <span data-ttu-id="4c0a4-144">仅当客户已登录，才能兑换礼品卡。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-144">Gift cards can be redeemed only if the customer is signed in.</span></span>
- <span data-ttu-id="4c0a4-145">**积分** – 客户可通过此模块使用积分支付订单。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-145">**Loyalty points** – This module lets a customer pay for an order by using loyalty points.</span></span> <span data-ttu-id="4c0a4-146">它提供可用积分和到期积分的摘要，并可供客户选择要兑换的积分数。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-146">It provides a summary of available points and expiring points, and lets the customer select the number of points to redeem.</span></span> <span data-ttu-id="4c0a4-147">如果客户未登录或不是会员，或者如果购物车中的总金额为 0（零），将自动隐藏此模块。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-147">If the customer isn't signed in or isn't a loyalty member, or if the total amount in the cart is 0 (zero), this module is automatically hidden.</span></span>
- <span data-ttu-id="4c0a4-148">**付款** – 客户可通过此模块使用信用卡支付订单。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-148">**Payment** – This module lets a customer pay for an order by using a credit card.</span></span> <span data-ttu-id="4c0a4-149">如果积分或礼品卡足以支付购物车中的总金额或总金额为 0（零），将自动隐藏此模块。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-149">If the total amount in the cart is covered by loyalty points or a gift card, or if it's 0 (zero), this module is automatically hidden.</span></span> <span data-ttu-id="4c0a4-150">Adyen 付款连接器针对此模块提供信用卡集成。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-150">Credit card integration is provided by the Adyen payment connector for this module.</span></span> <span data-ttu-id="4c0a4-151">有关如何使用此连接器的详细信息，请参阅[适用于 Adyen 的 Dynamics 365 付款连接器](dev-itpro/adyen-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-151">For more information about how to use this connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>
- <span data-ttu-id="4c0a4-152">**记帐地址** – 此模块可供客户提供记帐信息。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-152">**Billing address** – This module lets a customer provide billing information.</span></span> <span data-ttu-id="4c0a4-153">此信息和信用卡信息一起由 Adyen 使用。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-153">This information is processed, together with the credit card information, by Adyen.</span></span> <span data-ttu-id="4c0a4-154">此模块中有一个选项供客户将其记帐地址用作装运地址。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-154">This module includes an option that lets customers use their billing address as the shipping address.</span></span>

    <span data-ttu-id="4c0a4-155">下图显示了结帐页面上的礼品卡、会员积分、付款和帐单地址模块的示例。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-155">The following image shows an example of gift card, loyalty points, payment, and billing address modules on a checkout page.</span></span>

    ![礼品卡、会员积分、付款和帐单地址模块的示例](./media/ecommerce-payments.PNG)

- <span data-ttu-id="4c0a4-157">**联系信息** – 此模块可供客户为订单添加或更改联系信息（电子邮件地址）。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-157">**Contact information** – This module lets a customer add or change the contact information (email address) for an order.</span></span>

- <span data-ttu-id="4c0a4-158">**文本块** – 此模块中包含内容管理系统 (CMS) 驱动的所有消息。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-158">**Text block** – This module contains any messaging that is driven by the content management system (CMS).</span></span> <span data-ttu-id="4c0a4-159">例如，可能包含消息“订单问题请致电 1-800-Fabrikam”。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-159">For example, it might contain a message that states, "For issues with your order, contact 1-800-Fabrikam."</span></span> 

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="4c0a4-160">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="4c0a4-160">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="4c0a4-161">大多数结帐信息（如装运地址和装运方式）存储在购物车中，并作为订单的一部分处理。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-161">Most of the checkout information, such as the shipping address and shipping method, is stored in the cart and processed as part of the order.</span></span> <span data-ttu-id="4c0a4-162">唯一例外是信用卡信息。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-162">The only exception is the credit card information.</span></span> <span data-ttu-id="4c0a4-163">此信息直接使用 Adyen 付款连接器处理。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-163">This information is processed directly by using the Adyen payment connector.</span></span> <span data-ttu-id="4c0a4-164">将为付款授权，但不收费。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-164">The payment is authorized but isn't charged.</span></span>

## <a name="add-a-checkout-module-to-a-page-and-set-the-required-properties"></a><span data-ttu-id="4c0a4-165">向页面添加结帐模块和设置必需的属性</span><span class="sxs-lookup"><span data-stu-id="4c0a4-165">Add a checkout module to a page and set the required properties</span></span>

<span data-ttu-id="4c0a4-166">若要向新页面添加结帐模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-166">To add a checkout module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="4c0a4-167">转到**页面片段**，选择**新建**创建新片段。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-167">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="4c0a4-168">在**新建页面片段**对话框中，选择**结帐**模块。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-168">In the **New Page Fragment** dialog box, select the **Checkout** module.</span></span>
1. <span data-ttu-id="4c0a4-169">在**页面片段名称**下，输入名称**结帐片段**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-169">Under **Page Fragment Name**, enter the name **Checkout fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="4c0a4-170">选择**结帐模块**插槽。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-170">Select the **Checkout module** slot.</span></span>
1. <span data-ttu-id="4c0a4-171">在右侧的属性窗格中，选择铅笔符号，在字段中输入标题文本，然后选择复选标记符号。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-171">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="4c0a4-172">在**结帐信息**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-172">In the **Checkout Information** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4c0a4-173">在**添加模块**对话框中，选择**装运地址**、**交付选项**、**结帐部分容器**和**联系人信息**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-173">In the **Add Module** dialog box, select the **Shipping address**, **Delivery options**, **Checkout section container**, and **Contact information** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="4c0a4-174">在**结帐部分容器**模块，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-174">In the **Checkout section container** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4c0a4-175">在**添加模块**对话框中，选择**礼品卡**、**会员**和**付款**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-175">In the **Add Module** dialog box, select the **Gift card**, **Loyalty**, and **Payment** modules, and then select **OK**.</span></span> <span data-ttu-id="4c0a4-176">这样，就可以确保所有付款方式在一个分区中一起显示。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-176">In this way, you make sure that all the payment methods appear together in a section.</span></span>
1. <span data-ttu-id="4c0a4-177">选择**保存**，然后选择**预览**预览片段。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-177">Select **Save**, and then select **Preview** to preview the fragment.</span></span> <span data-ttu-id="4c0a4-178">预览中可能不显示某些没有购物车上下文的模块。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-178">Some modules that don't have a cart context might not be rendered in the preview.</span></span>
1. <span data-ttu-id="4c0a4-179">选择**完成编辑**签入片段，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-179">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="4c0a4-180">创建一个使用新结帐片段的模板。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-180">Create a template that uses the new checkout fragment.</span></span>
1. <span data-ttu-id="4c0a4-181">创建一个使用新模板的结帐页。</span><span class="sxs-lookup"><span data-stu-id="4c0a4-181">Create a checkout page that uses the new template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c0a4-182">其他资源</span><span class="sxs-lookup"><span data-stu-id="4c0a4-182">Additional resources</span></span>

[<span data-ttu-id="4c0a4-183">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="4c0a4-183">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4c0a4-184">容器模块</span><span class="sxs-lookup"><span data-stu-id="4c0a4-184">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="4c0a4-185">购买框模块</span><span class="sxs-lookup"><span data-stu-id="4c0a4-185">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4c0a4-186">购物车模块</span><span class="sxs-lookup"><span data-stu-id="4c0a4-186">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4c0a4-187">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="4c0a4-187">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4c0a4-188">页眉模块</span><span class="sxs-lookup"><span data-stu-id="4c0a4-188">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="4c0a4-189">页脚模块</span><span class="sxs-lookup"><span data-stu-id="4c0a4-189">Footer module</span></span>](author-footer-module.md)
