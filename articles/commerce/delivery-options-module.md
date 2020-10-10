---
title: 交货选项模块
description: 此主题介绍交货选项模块，说明如何在 Microsoft Dynamics 365 Commerce 中配置该模块。
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
ms.openlocfilehash: 39e597b88afcca69623b1a23acc95e4da3873082
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818291"
---
# <a name="delivery-options-module"></a><span data-ttu-id="679d3-103">交货选项模块</span><span class="sxs-lookup"><span data-stu-id="679d3-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="679d3-104">此主题介绍交货选项模块，说明如何在 Microsoft Dynamics 365 Commerce 中配置该模块。</span><span class="sxs-lookup"><span data-stu-id="679d3-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="679d3-105">概览</span><span class="sxs-lookup"><span data-stu-id="679d3-105">Overview</span></span>

<span data-ttu-id="679d3-106">交货选项模块使客户可以为在线订单选择交货方式，如装运或提货。</span><span class="sxs-lookup"><span data-stu-id="679d3-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="679d3-107">需要装运地址来确定交货方式。</span><span class="sxs-lookup"><span data-stu-id="679d3-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="679d3-108">如果更改装运地址，则必须重新检索交货选项。</span><span class="sxs-lookup"><span data-stu-id="679d3-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="679d3-109">如果订单中仅包含将在商店提货的项，则自动隐藏此模块。</span><span class="sxs-lookup"><span data-stu-id="679d3-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="679d3-110">有关如何配置交货方式的信息，请参阅[在线渠道设置](channel-setup-online.md)和[设置交货方式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)。</span><span class="sxs-lookup"><span data-stu-id="679d3-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="679d3-111">每种交货方式都可能收取相关费用。</span><span class="sxs-lookup"><span data-stu-id="679d3-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="679d3-112">有关如何为在线商店配置费用的详细信息，请参阅[全渠道高级自动收费](omni-auto-charges.md)。</span><span class="sxs-lookup"><span data-stu-id="679d3-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="679d3-113">在 Commerce 版本 10.0.13 中，交货选项模块已更新，可以支持**不按比例分配的标题费用**和**作为行费用装运**功能。</span><span class="sxs-lookup"><span data-stu-id="679d3-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="679d3-114">如果关闭了按比例分配，预期电子商务工作流将不允许为购物车中的商品提供混合交货方式（即某些商品被选出进行装运，其他商品则被选为采用提货方式）。</span><span class="sxs-lookup"><span data-stu-id="679d3-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="679d3-115">**不按比例分配的标题费用**功能需要在 Commerce headquarters 中打开**支持在渠道中进行一致的交货方式处理**标记。</span><span class="sxs-lookup"><span data-stu-id="679d3-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="679d3-116">打开该标记后，装运费用将在标题级别或行级别应用，具体取决于 Commerce headquarters 中的配置。</span><span class="sxs-lookup"><span data-stu-id="679d3-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="679d3-117">Fabrikam 主题支持混合交货方式，有些商品被选出进行装运，其他商品则被选为采用提货方式。</span><span class="sxs-lookup"><span data-stu-id="679d3-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="679d3-118">在此模式下，将为选出采用装运交货方式的所有商品按比例分配装运费用。</span><span class="sxs-lookup"><span data-stu-id="679d3-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="679d3-119">要能使用混合交货方式，必须首先在 Commerce headquarters 中配置**按比例分配的标题费用**功能。</span><span class="sxs-lookup"><span data-stu-id="679d3-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="679d3-120">有关此配置的详细信息，请参阅[按比例分配标题费用以匹配销售行](pro-rate-charges-matching-lines.md)。</span><span class="sxs-lookup"><span data-stu-id="679d3-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="679d3-121">如果在行项应用装运费用，可以在每一项的购物车行上显示这些费用。</span><span class="sxs-lookup"><span data-stu-id="679d3-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="679d3-122">此功能需要同时为购物车模块和结帐模块打开**在行项上显示装运费用**属性。</span><span class="sxs-lookup"><span data-stu-id="679d3-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="679d3-123">有关详细信息，请参阅[购物车模块](add-cart-module.md)和[结帐模块](add-checkout-module.md)。</span><span class="sxs-lookup"><span data-stu-id="679d3-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="679d3-124">下图显示了结帐页上的交货选项模块的示例。</span><span class="sxs-lookup"><span data-stu-id="679d3-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![结帐页上的交货选项模块的示例](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="679d3-126">交货选项模块属性</span><span class="sxs-lookup"><span data-stu-id="679d3-126">Delivery options module properties</span></span>

| <span data-ttu-id="679d3-127">属性</span><span class="sxs-lookup"><span data-stu-id="679d3-127">Property</span></span> | <span data-ttu-id="679d3-128">值</span><span class="sxs-lookup"><span data-stu-id="679d3-128">Values</span></span> | <span data-ttu-id="679d3-129">说明</span><span class="sxs-lookup"><span data-stu-id="679d3-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="679d3-130">标题</span><span class="sxs-lookup"><span data-stu-id="679d3-130">Heading</span></span> | <span data-ttu-id="679d3-131">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="679d3-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="679d3-132">交货选项模块的可选标题。</span><span class="sxs-lookup"><span data-stu-id="679d3-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="679d3-133">自定义 CSS 类名称</span><span class="sxs-lookup"><span data-stu-id="679d3-133">Custom CSS class name</span></span> | <span data-ttu-id="679d3-134">文本</span><span class="sxs-lookup"><span data-stu-id="679d3-134">Text</span></span> | <span data-ttu-id="679d3-135">将用于呈现此模块的自定义级联样式表 (CSS) 类名称（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="679d3-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="679d3-136">筛选交货模式选项</span><span class="sxs-lookup"><span data-stu-id="679d3-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="679d3-137">**不筛选**或**非装运方式**</span><span class="sxs-lookup"><span data-stu-id="679d3-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="679d3-138">指定交货选项模块是否应筛选掉所有非装运交货方式的值。</span><span class="sxs-lookup"><span data-stu-id="679d3-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="679d3-139">向结帐页添加交货选项模块和设置必需的属性</span><span class="sxs-lookup"><span data-stu-id="679d3-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="679d3-140">交货选项模块只能添加到结帐模块。</span><span class="sxs-lookup"><span data-stu-id="679d3-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="679d3-141">有关如何配置交货选项模块并将其添加到结帐页的详细信息，请参阅[结帐模块](add-checkout-module.md)。</span><span class="sxs-lookup"><span data-stu-id="679d3-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="679d3-142">其他资源</span><span class="sxs-lookup"><span data-stu-id="679d3-142">Additional resources</span></span>

[<span data-ttu-id="679d3-143">购物车模块</span><span class="sxs-lookup"><span data-stu-id="679d3-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="679d3-144">结帐模块</span><span class="sxs-lookup"><span data-stu-id="679d3-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="679d3-145">付款模块</span><span class="sxs-lookup"><span data-stu-id="679d3-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="679d3-146">收货地址模块</span><span class="sxs-lookup"><span data-stu-id="679d3-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="679d3-147">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="679d3-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="679d3-148">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="679d3-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="679d3-149">在线渠道设置</span><span class="sxs-lookup"><span data-stu-id="679d3-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="679d3-150">全渠道高级自动费用</span><span class="sxs-lookup"><span data-stu-id="679d3-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="679d3-151">按比例分配标题费用以匹配销售行</span><span class="sxs-lookup"><span data-stu-id="679d3-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="679d3-152">设置交货方式</span><span class="sxs-lookup"><span data-stu-id="679d3-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
