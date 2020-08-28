---
title: 装运地址模块
description: 此主题介绍装运地址模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
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
ms.openlocfilehash: 380d268ec0ba64367f090c31408eac1c54d0ff17
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661433"
---
# <a name="shipping-address-module"></a><span data-ttu-id="d2a6c-103">装运地址模块</span><span class="sxs-lookup"><span data-stu-id="d2a6c-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="d2a6c-104">此主题介绍装运地址模块，以及如何在 Microsoft Dynamics 365 Commerce 中配置此模块。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d2a6c-105">概览</span><span class="sxs-lookup"><span data-stu-id="d2a6c-105">Overview</span></span>

<span data-ttu-id="d2a6c-106">装运地址模块使客户可以在结帐流中添加或选择订单的装运地址。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="d2a6c-107">如果客户已登录，则显示以前为该客户保存的所有地址，然后客户可以在其中进行选择。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="d2a6c-108">客户也可以添加新地址。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-108">The customer can also add a new address.</span></span> <span data-ttu-id="d2a6c-109">装运地址模块用于订单中需要装运的所有项。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="d2a6c-110">装运地址格式可以在 Commerce headquarters 中为每个国家或地区定义，然后装运地址模块强制执行特定于国家/地区的规则。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="d2a6c-111">当客户在结帐流中输入装运地址时，他们可以选择将地址保存为主要地址。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="d2a6c-112">仅当客户登录后才显示此选项。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="d2a6c-113">虽然装运地址模块不提供地址验证，但是可以通过自定义设置来实现此功能。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="d2a6c-114">下图显示了结帐页上的新装运地址模块的示例。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![结帐页上的装运地址模块的示例](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="d2a6c-116">模块属性</span><span class="sxs-lookup"><span data-stu-id="d2a6c-116">Module properties</span></span>

| <span data-ttu-id="d2a6c-117">属性名称</span><span class="sxs-lookup"><span data-stu-id="d2a6c-117">Property name</span></span> | <span data-ttu-id="d2a6c-118">值</span><span class="sxs-lookup"><span data-stu-id="d2a6c-118">Values</span></span> | <span data-ttu-id="d2a6c-119">说明</span><span class="sxs-lookup"><span data-stu-id="d2a6c-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="d2a6c-120">标题</span><span class="sxs-lookup"><span data-stu-id="d2a6c-120">Heading</span></span> | <span data-ttu-id="d2a6c-121">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="d2a6c-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="d2a6c-122">装运地址模块的可选标题。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="d2a6c-123">显示地址类型</span><span class="sxs-lookup"><span data-stu-id="d2a6c-123">Show address type</span></span> | <span data-ttu-id="d2a6c-124">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="d2a6c-124">**True** or **False**</span></span> | <span data-ttu-id="d2a6c-125">如果将此可选属性设置为 **True**，地址类型（如**住宅**或**企业**）将显示。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="d2a6c-126">如果未指定地址类型，地址将自动保存为**类型**=**其他**。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="d2a6c-127">向结帐页添加装运地址模块和设置必需的属性</span><span class="sxs-lookup"><span data-stu-id="d2a6c-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="d2a6c-128">装运地址模块只能添加到结帐模块。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="d2a6c-129">有关如何配置装运地址模块并将其添加到结帐页的详细信息，请参阅[结帐模块](add-checkout-module.md)。</span><span class="sxs-lookup"><span data-stu-id="d2a6c-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d2a6c-130">其他资源</span><span class="sxs-lookup"><span data-stu-id="d2a6c-130">Additional resources</span></span>

[<span data-ttu-id="d2a6c-131">购物车模块</span><span class="sxs-lookup"><span data-stu-id="d2a6c-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d2a6c-132">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="d2a6c-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d2a6c-133">结帐模块</span><span class="sxs-lookup"><span data-stu-id="d2a6c-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d2a6c-134">付款模块</span><span class="sxs-lookup"><span data-stu-id="d2a6c-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="d2a6c-135">交货选项模块</span><span class="sxs-lookup"><span data-stu-id="d2a6c-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="d2a6c-136">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="d2a6c-136">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d2a6c-137">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="d2a6c-137">Gift card module</span></span>](add-giftcard.md)
