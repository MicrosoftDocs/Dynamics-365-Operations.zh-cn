---
title: 付款模块
description: 此主题介绍付款模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 894ac35973927c193d6e9c54e326daefb8a3f4a5
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055373"
---
# <a name="payment-module"></a><span data-ttu-id="bd90d-103">付款模块</span><span class="sxs-lookup"><span data-stu-id="bd90d-103">Payment module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bd90d-104">此主题介绍付款模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。</span><span class="sxs-lookup"><span data-stu-id="bd90d-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bd90d-105">概览</span><span class="sxs-lookup"><span data-stu-id="bd90d-105">Overview</span></span>

<span data-ttu-id="bd90d-106">付款模块使客户可以使用信用卡或借记卡支付订单。</span><span class="sxs-lookup"><span data-stu-id="bd90d-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="bd90d-107">此模块的付款集成由适用于 Adyen 的 Dynamics 365 付款连接器提供。</span><span class="sxs-lookup"><span data-stu-id="bd90d-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="bd90d-108">有关如何设置和配置付款连接器的详细信息，请参阅[适用于 Adyen 的 Dynamics 365 付款连接器](dev-itpro/adyen-connector.md)。</span><span class="sxs-lookup"><span data-stu-id="bd90d-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="bd90d-109">付款模块将通过 Adyen 提供的付款信息托管在 HTML 内联框架 (iframe) 中。</span><span class="sxs-lookup"><span data-stu-id="bd90d-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="bd90d-110">付款模块与 Commerce Scale Unit 交互来检索 Adyen 付款信息。</span><span class="sxs-lookup"><span data-stu-id="bd90d-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="bd90d-111">作为 Commerce Scale Unit 交互的一部分，支付模块可以允许在 iframe 中或作为单独的模块提供账单地址信息。</span><span class="sxs-lookup"><span data-stu-id="bd90d-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="bd90d-112">在 Fabrikam 主题中，账单地址显示在单独的模块中。</span><span class="sxs-lookup"><span data-stu-id="bd90d-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="bd90d-113">此方法具有更大的格式灵活性，因为可以呈现地址行，使其类似于装运地址的行。</span><span class="sxs-lookup"><span data-stu-id="bd90d-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="bd90d-114">付款模块还使登录客户可以保存其付款信息。</span><span class="sxs-lookup"><span data-stu-id="bd90d-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="bd90d-115">付款信息和账单地址通过 Adyen 付款连接器保存和管理。</span><span class="sxs-lookup"><span data-stu-id="bd90d-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="bd90d-116">付款模块包含会员积分或礼品卡未覆盖的所有订单费用。</span><span class="sxs-lookup"><span data-stu-id="bd90d-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="bd90d-117">如果订单总计已完全由会员积分或礼品卡积分覆盖，付款模块将被隐藏，客户可以不使用付款模块下订单。</span><span class="sxs-lookup"><span data-stu-id="bd90d-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="bd90d-118">Adyen 付款连接器还支持强大客户身份验证 (SCA)。</span><span class="sxs-lookup"><span data-stu-id="bd90d-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="bd90d-119">欧盟 (EU) 付款服务规定 2.0 (PSD2.0) 的一部分要求在线购物者在使用电子付款方式时，必须在其在线购物体验之外进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="bd90d-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="bd90d-120">在结帐流中，客户将被重定向到他们的银行站点。</span><span class="sxs-lookup"><span data-stu-id="bd90d-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="bd90d-121">然后，在进行身份验证之后，它们将被重定向回 Commerce 结帐流。</span><span class="sxs-lookup"><span data-stu-id="bd90d-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="bd90d-122">在此重定向过程中，客户在结帐流中输入的信息（例如，装运地址、交货选项、礼品卡信息和会员信息）将保持不变。</span><span class="sxs-lookup"><span data-stu-id="bd90d-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="bd90d-123">必须先在 Commerce headquarters 中为 SCA 配置付款连接器，然后才能打开此功能。</span><span class="sxs-lookup"><span data-stu-id="bd90d-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="bd90d-124">有关详细信息，请参阅[使用 Adyen 的强大客户身份验证](adyen_redirect.md)。</span><span class="sxs-lookup"><span data-stu-id="bd90d-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

> [!NOTE]
> <span data-ttu-id="bd90d-125">对于 Adyen 付款连接器，仅在将 Adyen URL 添加到您的站点的允许列表时，才能显示付款模块中的 iframe 模块。</span><span class="sxs-lookup"><span data-stu-id="bd90d-125">For the Adyen payment connector, the iframe module in the payment module can be rendered only if you add the Adyen URL to your site's allow list.</span></span> <span data-ttu-id="bd90d-126">若要完成此步骤，请将 **\*.adyen.com** 添加到您的站点的内容安全策略的 **child-src** 、 **connect-src** 、 **img-src** 、 **script-src** 和 **style-src** 指令。</span><span class="sxs-lookup"><span data-stu-id="bd90d-126">To complete this step, add **\*.adyen.com** to the **child-src** , **connect-src** , **img-src** , **script-src** , and **style-src** directives of your site's content security policy.</span></span> <span data-ttu-id="bd90d-127">有关详细信息，请参阅[管理内容安全策略](manage-csp.md)。</span><span class="sxs-lookup"><span data-stu-id="bd90d-127">For more information, see [Manage Content Security Policy](manage-csp.md).</span></span> 

<span data-ttu-id="bd90d-128">下图显示了结帐页面上的礼品卡、会员和付款模块的示例。</span><span class="sxs-lookup"><span data-stu-id="bd90d-128">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![结帐页面上的礼品卡、会员和付款模块的示例](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="bd90d-130">付款模块属性</span><span class="sxs-lookup"><span data-stu-id="bd90d-130">Payment module properties</span></span>

| <span data-ttu-id="bd90d-131">属性名称</span><span class="sxs-lookup"><span data-stu-id="bd90d-131">Property name</span></span> | <span data-ttu-id="bd90d-132">值</span><span class="sxs-lookup"><span data-stu-id="bd90d-132">Values</span></span> | <span data-ttu-id="bd90d-133">说明</span><span class="sxs-lookup"><span data-stu-id="bd90d-133">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="bd90d-134">标题</span><span class="sxs-lookup"><span data-stu-id="bd90d-134">Heading</span></span> | <span data-ttu-id="bd90d-135">标题文本</span><span class="sxs-lookup"><span data-stu-id="bd90d-135">Heading text</span></span> | <span data-ttu-id="bd90d-136">付款模块的可选标题。</span><span class="sxs-lookup"><span data-stu-id="bd90d-136">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="bd90d-137">iframe 的高度</span><span class="sxs-lookup"><span data-stu-id="bd90d-137">Height of the iframe</span></span> | <span data-ttu-id="bd90d-138">像素</span><span class="sxs-lookup"><span data-stu-id="bd90d-138">Pixels</span></span> | <span data-ttu-id="bd90d-139">iframe 高度（以像素为单位）。</span><span class="sxs-lookup"><span data-stu-id="bd90d-139">The iframe height, in pixels.</span></span> <span data-ttu-id="bd90d-140">可以根据需要调整此高度。</span><span class="sxs-lookup"><span data-stu-id="bd90d-140">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="bd90d-141">显示帐单地址</span><span class="sxs-lookup"><span data-stu-id="bd90d-141">Show billing address</span></span> | <span data-ttu-id="bd90d-142">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="bd90d-142">**True** or **False**</span></span> | <span data-ttu-id="bd90d-143">如果将此属性设置为 **True** ，账单地址将由 Adyen 在付款模块 iframe 中提供。</span><span class="sxs-lookup"><span data-stu-id="bd90d-143">If this property is set to **True** , the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="bd90d-144">如果设置为 **False** ，Adyen 将不会提供账单地址，Commerce 用户必须配置一个模块来在结帐页面上显示账单地址。</span><span class="sxs-lookup"><span data-stu-id="bd90d-144">If it's set to **False** , the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="bd90d-145">付款方式覆盖</span><span class="sxs-lookup"><span data-stu-id="bd90d-145">Payment style override</span></span> | <span data-ttu-id="bd90d-146">级联样式表 (CSS) 代码</span><span class="sxs-lookup"><span data-stu-id="bd90d-146">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="bd90d-147">由于付款模块托管在 iframe 中，因此样式功能有限。</span><span class="sxs-lookup"><span data-stu-id="bd90d-147">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="bd90d-148">您可以使用此属性来实现某些样式。</span><span class="sxs-lookup"><span data-stu-id="bd90d-148">You can achieve some styling by using this property.</span></span> <span data-ttu-id="bd90d-149">要覆盖站点样式，必须粘贴 CSS 代码作为此属性的值。</span><span class="sxs-lookup"><span data-stu-id="bd90d-149">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="bd90d-150">站点构建器 CSS 覆盖和样式不适用于此模块。</span><span class="sxs-lookup"><span data-stu-id="bd90d-150">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="bd90d-151">帐单地址</span><span class="sxs-lookup"><span data-stu-id="bd90d-151">Billing address</span></span>

<span data-ttu-id="bd90d-152">付款模块使客户可以在付款信息中提供账单地址。</span><span class="sxs-lookup"><span data-stu-id="bd90d-152">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="bd90d-153">它还使他们可以将装运地址用作账单地址，从而使结帐流更加轻松快捷。</span><span class="sxs-lookup"><span data-stu-id="bd90d-153">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="bd90d-154">如果将 **显示账单地址** 属性设置为 **False** ，应在结帐页面上配置付款模块。</span><span class="sxs-lookup"><span data-stu-id="bd90d-154">If the **Show billing address** property is set to **False** , the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="bd90d-155">向结帐页面添加付款模块和设置必需的属性</span><span class="sxs-lookup"><span data-stu-id="bd90d-155">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="bd90d-156">付款模块只能添加到结帐模块。</span><span class="sxs-lookup"><span data-stu-id="bd90d-156">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="bd90d-157">有关如何为结帐页面配置付款模块的详细信息，请参阅[结帐模块](add-checkout-module.md)。</span><span class="sxs-lookup"><span data-stu-id="bd90d-157">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bd90d-158">其他资源</span><span class="sxs-lookup"><span data-stu-id="bd90d-158">Additional resources</span></span>

[<span data-ttu-id="bd90d-159">购物车模块</span><span class="sxs-lookup"><span data-stu-id="bd90d-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bd90d-160">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="bd90d-160">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="bd90d-161">结帐模块</span><span class="sxs-lookup"><span data-stu-id="bd90d-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bd90d-162">收货地址模块</span><span class="sxs-lookup"><span data-stu-id="bd90d-162">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="bd90d-163">交付选项模块</span><span class="sxs-lookup"><span data-stu-id="bd90d-163">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="bd90d-164">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="bd90d-164">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="bd90d-165">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="bd90d-165">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="bd90d-166">适用于 Adyen 的 Dynamics 365 付款连接器</span><span class="sxs-lookup"><span data-stu-id="bd90d-166">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="bd90d-167">使用 Adyen 的强大客户身份验证</span><span class="sxs-lookup"><span data-stu-id="bd90d-167">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
