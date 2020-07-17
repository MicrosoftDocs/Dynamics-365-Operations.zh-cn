---
title: 购物车和结账页面概览
description: 此主题概述 Microsoft Dynamics 365 Commerce 中的购物车和结帐页。
author: anupamar-ms
manager: annbe
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c879b90cf49dcab9cf069e4f3613602bd6673aa9
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527554"
---
# <a name="cart-and-checkout-pages-overview"></a><span data-ttu-id="ab314-103">购物车和结账页面概览</span><span class="sxs-lookup"><span data-stu-id="ab314-103">Cart and checkout pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ab314-104">此主题概述 Microsoft Dynamics 365 Commerce 中的购物车和结帐页。</span><span class="sxs-lookup"><span data-stu-id="ab314-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ab314-105">概览</span><span class="sxs-lookup"><span data-stu-id="ab314-105">Overview</span></span>

<span data-ttu-id="ab314-106">电子商务网站的购物车页显示客户已添加到购物车的所有商品。</span><span class="sxs-lookup"><span data-stu-id="ab314-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="ab314-107">购物车页是使用购物车模块生成的。</span><span class="sxs-lookup"><span data-stu-id="ab314-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="ab314-108">购物车模块是承载展示购物车中的商品所需全部模块的容器。</span><span class="sxs-lookup"><span data-stu-id="ab314-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="ab314-109">购物车模块也可以使用其他模块显示订单汇总和已经为客户订单应用的任何促销代码。</span><span class="sxs-lookup"><span data-stu-id="ab314-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="ab314-110">电子商务网站的结帐页提供分步流，供客户输入下订单所需全部信息。</span><span class="sxs-lookup"><span data-stu-id="ab314-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="ab314-111">结帐模块中可以包含用于处理装运地址、装运方式、记帐信息、订单摘要和与客户订单有关的其他信息的模块。</span><span class="sxs-lookup"><span data-stu-id="ab314-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="ab314-112">购物车页</span><span class="sxs-lookup"><span data-stu-id="ab314-112">Cart page</span></span>

<span data-ttu-id="ab314-113">购物车页充当购物袋，其中包含已添加到购物车的所有商品。</span><span class="sxs-lookup"><span data-stu-id="ab314-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="ab314-114">下图显示使用在线入门套件和“Fabrikam”主题生成的购物车页的示例。</span><span class="sxs-lookup"><span data-stu-id="ab314-114">The following illustration show an example of a cart page that was built by using the online starter kit and the "Fabrikam" theme.</span></span>

![购物车页示例](./media/cart2.PNG)

<span data-ttu-id="ab314-116">购物车页的主体显示客户已添加到购物车的所有商品。</span><span class="sxs-lookup"><span data-stu-id="ab314-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="ab314-117">将显示所有适用的折扣。</span><span class="sxs-lookup"><span data-stu-id="ab314-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="ab314-118">这些折扣包括复合折扣。</span><span class="sxs-lookup"><span data-stu-id="ab314-118">These discounts include complex discounts.</span></span> <span data-ttu-id="ab314-119">例如，“买 3 件打九折”或“买一瓶和一个背包打九折”。</span><span class="sxs-lookup"><span data-stu-id="ab314-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="ab314-120">订单汇总模块显示应用折扣、运费、税等后的应付金额。</span><span class="sxs-lookup"><span data-stu-id="ab314-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="ab314-121">还有一个促销代码模块，供客户应用或删除促销代码。</span><span class="sxs-lookup"><span data-stu-id="ab314-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="ab314-122">客户可匿名或作为已登录用户购物。</span><span class="sxs-lookup"><span data-stu-id="ab314-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="ab314-123">如果客户已登录，则购物车中的商品将保留到下个会话。</span><span class="sxs-lookup"><span data-stu-id="ab314-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="ab314-124">因此，客户可以从多个设备继续购物。</span><span class="sxs-lookup"><span data-stu-id="ab314-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="ab314-125">客户可从购物车继续结帐。</span><span class="sxs-lookup"><span data-stu-id="ab314-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="ab314-126">客户可以以访客用户或已登录用户的身份开始结帐。</span><span class="sxs-lookup"><span data-stu-id="ab314-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="ab314-127">有关如何制作购物车页的信息，请参阅[向页面添加购物车模块](add-cart-module.md)。</span><span class="sxs-lookup"><span data-stu-id="ab314-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="ab314-128">结帐页</span><span class="sxs-lookup"><span data-stu-id="ab314-128">Checkout page</span></span>

<span data-ttu-id="ab314-129">结帐页是客户输入下订单所需信息时所在位置。</span><span class="sxs-lookup"><span data-stu-id="ab314-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="ab314-130">下图显示使用入门套件生成的结帐页的示例。</span><span class="sxs-lookup"><span data-stu-id="ab314-130">The following illustration show an example of a checkout page that was built by using the online starter kit.</span></span>

![结帐页示例](./media/Checkout.PNG)

<span data-ttu-id="ab314-132">结帐页的主题是收集所有订单信息的位置。</span><span class="sxs-lookup"><span data-stu-id="ab314-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="ab314-133">此信息包括装运地址、交货选项和付款信息。</span><span class="sxs-lookup"><span data-stu-id="ab314-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="ab314-134">结帐采用分步流程，因为必须按照特定顺序输入要处理的信息。</span><span class="sxs-lookup"><span data-stu-id="ab314-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="ab314-135">例如，必须先输入装运地址，才能计算装运成本和为付款授权。</span><span class="sxs-lookup"><span data-stu-id="ab314-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="ab314-136">装运地址</span><span class="sxs-lookup"><span data-stu-id="ab314-136">Shipping address</span></span>

<span data-ttu-id="ab314-137">如果必须装运商品，则需要装运地址。</span><span class="sxs-lookup"><span data-stu-id="ab314-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="ab314-138">可以在 Dynamics 365 Commerce 中为每个区域设置配置装运地址格式。</span><span class="sxs-lookup"><span data-stu-id="ab314-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="ab314-139">例如，如果要将商品运到美国，则装运地址必须包含街道地址、州和邮政编码。</span><span class="sxs-lookup"><span data-stu-id="ab314-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="ab314-140">将为装运地址字段执行一些基本输入验证，如验证字母数字字符、最大长度和数字。</span><span class="sxs-lookup"><span data-stu-id="ab314-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="ab314-141">虽然不验证地址是否有效，但可以使用自定义的第三方服务进行此项验证。</span><span class="sxs-lookup"><span data-stu-id="ab314-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="ab314-142">装运地址应用于购物车中所有选择了“装运”选项的商品。</span><span class="sxs-lookup"><span data-stu-id="ab314-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="ab314-143">如果使用在线入门套件中提供的结帐流程，则不能将单件购物车商品装运到不同地址。</span><span class="sxs-lookup"><span data-stu-id="ab314-143">If you use the checkout flow that is provided in the online starter kit, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="ab314-144">如果需要此功能，可以通过自定义结帐模块来实施。</span><span class="sxs-lookup"><span data-stu-id="ab314-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="ab314-145">提供装运地址之后，将显示 Dynamics 365 Commerce 在线商店中的可用装运方式。</span><span class="sxs-lookup"><span data-stu-id="ab314-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="ab314-146">可以在 Commerce 中配置装运方式及其支持的地址。</span><span class="sxs-lookup"><span data-stu-id="ab314-146">The shipping methods and the addresses that they support can be configured in Commerce.</span></span>

### <a name="payment"></a><span data-ttu-id="ab314-147">付款</span><span class="sxs-lookup"><span data-stu-id="ab314-147">Payment</span></span>

<span data-ttu-id="ab314-148">结帐流程中的下一步是付款。</span><span class="sxs-lookup"><span data-stu-id="ab314-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="ab314-149">在电子商务中，可使用多种付款方式下订单，如信用卡、礼品卡和积分。</span><span class="sxs-lookup"><span data-stu-id="ab314-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="ab314-150">也可以使用这些付款方式的组合。</span><span class="sxs-lookup"><span data-stu-id="ab314-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="ab314-151">可能需要更多信息，具体取决于所用付款方式。</span><span class="sxs-lookup"><span data-stu-id="ab314-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="ab314-152">例如，信用卡付款需要结算地址。</span><span class="sxs-lookup"><span data-stu-id="ab314-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="ab314-153">信用卡付款通过使用 Adyen 付款连接器处理。</span><span class="sxs-lookup"><span data-stu-id="ab314-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="ab314-154">会员积分</span><span class="sxs-lookup"><span data-stu-id="ab314-154">Loyalty points</span></span>

<span data-ttu-id="ab314-155">结帐流程中，会员计划成员客户和积攒了积分的客户可以兑换这些积分来支付订单。</span><span class="sxs-lookup"><span data-stu-id="ab314-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="ab314-156">仅当客户当前拥有会员资格时，才会显示积分模块。</span><span class="sxs-lookup"><span data-stu-id="ab314-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="ab314-157">此模块对非会员和访客用户隐藏。</span><span class="sxs-lookup"><span data-stu-id="ab314-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="ab314-158">礼品卡</span><span class="sxs-lookup"><span data-stu-id="ab314-158">Gift cards</span></span>

<span data-ttu-id="ab314-159">在线入门套件支持为订单兑换内部礼品卡。</span><span class="sxs-lookup"><span data-stu-id="ab314-159">The online starter kit lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="ab314-160">客户必须先登录，才能应用内部礼品卡。</span><span class="sxs-lookup"><span data-stu-id="ab314-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="ab314-161">为了提高安全，我们建议您为内部礼品卡使用个人标识号 (PIN) 来自定义流程。</span><span class="sxs-lookup"><span data-stu-id="ab314-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="ab314-162">已登录用户和访客用户</span><span class="sxs-lookup"><span data-stu-id="ab314-162">Signed-in and guest users</span></span>

<span data-ttu-id="ab314-163">客户可以以访客用户或已登录用户的身份完成结帐流程。</span><span class="sxs-lookup"><span data-stu-id="ab314-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="ab314-164">如果客户登录，将自动检索帐户信息，如保存的装运地址和保存的信用卡详细信息。</span><span class="sxs-lookup"><span data-stu-id="ab314-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="ab314-165">订单汇总</span><span class="sxs-lookup"><span data-stu-id="ab314-165">Order summary</span></span>

<span data-ttu-id="ab314-166">结帐显示购物车中的明细商品的汇总，所以客户可以在下订单前验证订单。</span><span class="sxs-lookup"><span data-stu-id="ab314-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="ab314-167">结帐流程中不能编辑明细商品。</span><span class="sxs-lookup"><span data-stu-id="ab314-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="ab314-168">但是，提供了购物车链接，以防用户回去编辑明细商品。</span><span class="sxs-lookup"><span data-stu-id="ab314-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="ab314-169">客户提供装运和记帐信息之后，订单汇总体现应用积分、礼品卡和其他付款后的应付金额。</span><span class="sxs-lookup"><span data-stu-id="ab314-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="ab314-170">订单确认和电子邮件</span><span class="sxs-lookup"><span data-stu-id="ab314-170">Order confirmation and email</span></span>

<span data-ttu-id="ab314-171">客户下订单时，将提供确认编号。</span><span class="sxs-lookup"><span data-stu-id="ab314-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="ab314-172">此时，付款已获得授权，但未扣费。</span><span class="sxs-lookup"><span data-stu-id="ab314-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="ab314-173">仅当订单已履行（即已装运或已提货），才会对付款扣费。</span><span class="sxs-lookup"><span data-stu-id="ab314-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="ab314-174">创建订单之后，将向客户发送订单确认电子邮件。</span><span class="sxs-lookup"><span data-stu-id="ab314-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="ab314-175">有关如何制作结帐页的详细信息，请参阅[向页面添加结帐模块](add-checkout-module.md)。</span><span class="sxs-lookup"><span data-stu-id="ab314-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab314-176">其他资源</span><span class="sxs-lookup"><span data-stu-id="ab314-176">Additional resources</span></span>

[<span data-ttu-id="ab314-177">主页概览</span><span class="sxs-lookup"><span data-stu-id="ab314-177">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="ab314-178">产品详细信息页面概览</span><span class="sxs-lookup"><span data-stu-id="ab314-178">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="ab314-179">帐户管理页面概览</span><span class="sxs-lookup"><span data-stu-id="ab314-179">Account management pages overview</span></span>](quick-tour-account-management.md)
