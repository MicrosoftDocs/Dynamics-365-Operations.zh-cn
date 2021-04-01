---
title: 装运地址模块
description: 此主题介绍装运地址模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: anupamar-ms
manager: annbe
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e590c966ca6bd8111df5f91cbac0485afaa45c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234405"
---
# <a name="shipping-address-module"></a><span data-ttu-id="995bd-103">收货地址模块</span><span class="sxs-lookup"><span data-stu-id="995bd-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="995bd-104">此主题描述装运地址模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。</span><span class="sxs-lookup"><span data-stu-id="995bd-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="995bd-105">装运地址模块使客户可以在结帐流中添加或选择订单的装运地址。</span><span class="sxs-lookup"><span data-stu-id="995bd-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="995bd-106">如果客户已登录，则显示以前为该客户保存的所有地址，然后客户可以在其中进行选择。</span><span class="sxs-lookup"><span data-stu-id="995bd-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="995bd-107">客户也可以添加新地址。</span><span class="sxs-lookup"><span data-stu-id="995bd-107">The customer can also add a new address.</span></span> <span data-ttu-id="995bd-108">装运地址模块用于订单中需要装运的所有项。</span><span class="sxs-lookup"><span data-stu-id="995bd-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="995bd-109">装运地址格式可以在 Commerce headquarters 中为每个国家或地区定义，然后装运地址模块强制执行特定于国家/地区的规则。</span><span class="sxs-lookup"><span data-stu-id="995bd-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="995bd-110">当客户在结帐流中输入装运地址时，他们可以选择将地址保存为主要地址。</span><span class="sxs-lookup"><span data-stu-id="995bd-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="995bd-111">仅当客户登录后才显示此选项。</span><span class="sxs-lookup"><span data-stu-id="995bd-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="995bd-112">虽然装运地址模块不提供地址验证，但是可以通过自定义设置来实现此功能。</span><span class="sxs-lookup"><span data-stu-id="995bd-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="995bd-113">下图显示了结帐页上的新装运地址模块的示例。</span><span class="sxs-lookup"><span data-stu-id="995bd-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![结帐页上的装运地址模块的示例](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="995bd-115">模块属性</span><span class="sxs-lookup"><span data-stu-id="995bd-115">Module properties</span></span>

| <span data-ttu-id="995bd-116">属性名称</span><span class="sxs-lookup"><span data-stu-id="995bd-116">Property name</span></span> | <span data-ttu-id="995bd-117">值</span><span class="sxs-lookup"><span data-stu-id="995bd-117">Values</span></span> | <span data-ttu-id="995bd-118">说明</span><span class="sxs-lookup"><span data-stu-id="995bd-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="995bd-119">标题</span><span class="sxs-lookup"><span data-stu-id="995bd-119">Heading</span></span> | <span data-ttu-id="995bd-120">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="995bd-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="995bd-121">装运地址模块的可选标题。</span><span class="sxs-lookup"><span data-stu-id="995bd-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="995bd-122">显示地址类型</span><span class="sxs-lookup"><span data-stu-id="995bd-122">Show address type</span></span> | <span data-ttu-id="995bd-123">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="995bd-123">**True** or **False**</span></span> | <span data-ttu-id="995bd-124">如果将此可选属性设置为 **True**，地址类型（如 **住宅** 或 **企业**）将显示。</span><span class="sxs-lookup"><span data-stu-id="995bd-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="995bd-125">如果未指定地址类型，地址将自动保存为 **类型**=**其他**。</span><span class="sxs-lookup"><span data-stu-id="995bd-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="995bd-126">启用自动建议</span><span class="sxs-lookup"><span data-stu-id="995bd-126">Enable auto suggestion</span></span>| <span data-ttu-id="995bd-127">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="995bd-127">**True** or **False**</span></span> | <span data-ttu-id="995bd-128">如果将此可选属性设置为 **真**，系统会提供自动地址建议。</span><span class="sxs-lookup"><span data-stu-id="995bd-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="995bd-129">这些建议由必应地图提供支持。</span><span class="sxs-lookup"><span data-stu-id="995bd-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="995bd-130">有关如何为您的站点设置必应地图集成的信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="995bd-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="995bd-131">从 Commerce 版本 10.0.15 起提供此功能。</span><span class="sxs-lookup"><span data-stu-id="995bd-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="995bd-132">自动建议选项</span><span class="sxs-lookup"><span data-stu-id="995bd-132">Auto suggest options</span></span>| <span data-ttu-id="995bd-133">数字</span><span class="sxs-lookup"><span data-stu-id="995bd-133">A number</span></span>| <span data-ttu-id="995bd-134">如果启用了自动地址建议，则可以指定其他选项，例如应提供的最大建议数量。</span><span class="sxs-lookup"><span data-stu-id="995bd-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="995bd-135">向结帐页添加装运地址模块和设置必需的属性</span><span class="sxs-lookup"><span data-stu-id="995bd-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="995bd-136">装运地址模块只能添加到结帐模块。</span><span class="sxs-lookup"><span data-stu-id="995bd-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="995bd-137">有关如何配置装运地址模块并将其添加到结帐页的详细信息，请参阅[结帐模块](add-checkout-module.md)。</span><span class="sxs-lookup"><span data-stu-id="995bd-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="995bd-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="995bd-138">Additional resources</span></span>

[<span data-ttu-id="995bd-139">购物车模块</span><span class="sxs-lookup"><span data-stu-id="995bd-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="995bd-140">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="995bd-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="995bd-141">结帐模块</span><span class="sxs-lookup"><span data-stu-id="995bd-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="995bd-142">付款模块</span><span class="sxs-lookup"><span data-stu-id="995bd-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="995bd-143">交付选项模块</span><span class="sxs-lookup"><span data-stu-id="995bd-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="995bd-144">提货信息模块</span><span class="sxs-lookup"><span data-stu-id="995bd-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="995bd-145">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="995bd-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="995bd-146">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="995bd-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="995bd-147">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="995bd-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]