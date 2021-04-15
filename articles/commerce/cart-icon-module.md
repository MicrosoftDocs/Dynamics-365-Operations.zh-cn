---
title: 购物车图标模块
description: 此主题介绍购物车图标模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5ff514f07e8b31abe79775e5011bd3f1b24b2935
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793073"
---
# <a name="cart-icon-module"></a><span data-ttu-id="c38e1-103">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="c38e1-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c38e1-104">此主题介绍购物车图标模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="c38e1-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c38e1-105">购物车图标模块在页面的页眉模块中提供购物车，并显示购物车中的商品数量。</span><span class="sxs-lookup"><span data-stu-id="c38e1-105">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="c38e1-106">将鼠标光标悬停在购物车图标上方时，购物车图标模块还会显示购物车摘要（也称为迷你购物车）。</span><span class="sxs-lookup"><span data-stu-id="c38e1-106">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="c38e1-107">用户不必导航到购物车页面，迷你购物车就为用户提供购物车中的商品摘要。</span><span class="sxs-lookup"><span data-stu-id="c38e1-107">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="c38e1-108">此外，还允许用户在对摘要满意的情况下直接转到结帐页面。</span><span class="sxs-lookup"><span data-stu-id="c38e1-108">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="c38e1-109">这样可以减少页面导航次数，加快结帐速度。</span><span class="sxs-lookup"><span data-stu-id="c38e1-109">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="c38e1-110">Dynamics 365 Commerce 10.0.11 版本中提供对购物车图标模块的支持。</span><span class="sxs-lookup"><span data-stu-id="c38e1-110">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="c38e1-111">下图显示了购物车图标模块的示例，该模块在 Fabrikam 标题中显示迷你购物车。</span><span class="sxs-lookup"><span data-stu-id="c38e1-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![购物车图标模块的示例](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="c38e1-113">模块属性</span><span class="sxs-lookup"><span data-stu-id="c38e1-113">Module properties</span></span>

- <span data-ttu-id="c38e1-114">**显示迷你购物车** – 如果为 true，此属性用于启用将鼠标光标悬停在购物车图标上方时显示的购物车摘要（迷你购物车）。</span><span class="sxs-lookup"><span data-stu-id="c38e1-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="c38e1-115">只有桌面视图端口中才支持此功能。</span><span class="sxs-lookup"><span data-stu-id="c38e1-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="c38e1-116">向页面添加购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="c38e1-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="c38e1-117">若要添加购物车图标模块，请参阅[页眉模块](author-header-module.md)。</span><span class="sxs-lookup"><span data-stu-id="c38e1-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c38e1-118">其他资源</span><span class="sxs-lookup"><span data-stu-id="c38e1-118">Additional resources</span></span>

[<span data-ttu-id="c38e1-119">购物车模块</span><span class="sxs-lookup"><span data-stu-id="c38e1-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c38e1-120">结帐模块</span><span class="sxs-lookup"><span data-stu-id="c38e1-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c38e1-121">付款模块</span><span class="sxs-lookup"><span data-stu-id="c38e1-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="c38e1-122">收货地址模块</span><span class="sxs-lookup"><span data-stu-id="c38e1-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="c38e1-123">交付选项模块</span><span class="sxs-lookup"><span data-stu-id="c38e1-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="c38e1-124">提货信息模块</span><span class="sxs-lookup"><span data-stu-id="c38e1-124">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="c38e1-125">订单详细信息模块</span><span class="sxs-lookup"><span data-stu-id="c38e1-125">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c38e1-126">礼品卡模块</span><span class="sxs-lookup"><span data-stu-id="c38e1-126">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]