---
title: 商店选择器模块
description: 此主题介绍商店选择器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157332"
---
# <a name="store-selector-module"></a><span data-ttu-id="d81f8-103">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="d81f8-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d81f8-104">此主题介绍商店选择器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="d81f8-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d81f8-105">概览</span><span class="sxs-lookup"><span data-stu-id="d81f8-105">Overview</span></span>

<span data-ttu-id="d81f8-106">商店选择器模块用于“在线购买，店内提货”(BOPIS) 客户方案。</span><span class="sxs-lookup"><span data-stu-id="d81f8-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="d81f8-107">它显示可以提走产品的商店列表，以及每个商店的商店营业时间和产品库存。</span><span class="sxs-lookup"><span data-stu-id="d81f8-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="d81f8-108">商店选择器模块需要产品的上下文和查找商店的搜索位置。</span><span class="sxs-lookup"><span data-stu-id="d81f8-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="d81f8-109">在没有搜索位置的情况下，如果客户给出同意表示，搜索位置将默认为客户的浏览器位置。</span><span class="sxs-lookup"><span data-stu-id="d81f8-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="d81f8-110">此模块有一个输入框，允许客户输入位置（邮政编码或城市和州/省）来查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="d81f8-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="d81f8-111">商店选择器模块与 Bing 地图地理编码应用程序编程接口 (API) 集成在一起，以将位置转换为纬度和经度。</span><span class="sxs-lookup"><span data-stu-id="d81f8-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="d81f8-112">必须提供 Bing 地图 API 密钥，并且必须将其添加到 Dynamics 365 Commerce 内的“Commerce 共享参数”页面中。</span><span class="sxs-lookup"><span data-stu-id="d81f8-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d81f8-113">商店选择器模块可以添加到“产品详细信息”页面 (PDP) 上的购买框模块中，来显示可提走产品的商店。</span><span class="sxs-lookup"><span data-stu-id="d81f8-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="d81f8-114">也可以将其添加到购物车模块。</span><span class="sxs-lookup"><span data-stu-id="d81f8-114">It can also be added to a cart module.</span></span> <span data-ttu-id="d81f8-115">当添加到购物车模块时，商店选择器模块将显示每个购物车行项的提货选项。</span><span class="sxs-lookup"><span data-stu-id="d81f8-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="d81f8-116">另外，使用自定义编码，可以通过扩展和自定义将此模块添加到其他页面或模块。</span><span class="sxs-lookup"><span data-stu-id="d81f8-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="d81f8-117">为了使 BOPIS 方案正常工作，应使用“客户提货”交货模式配置产品。</span><span class="sxs-lookup"><span data-stu-id="d81f8-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="d81f8-118">否则，此模块将不会在相应页面上显示。</span><span class="sxs-lookup"><span data-stu-id="d81f8-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="d81f8-119">有关如何配置交货模式的详细信息，请参阅[设置交货模式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)。</span><span class="sxs-lookup"><span data-stu-id="d81f8-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="d81f8-120">下图显示了 PDP 上使用的商店选择器模块的示例。</span><span class="sxs-lookup"><span data-stu-id="d81f8-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![商店选择器模块的示例](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="d81f8-122">电子商务中商店选择器模块的使用</span><span class="sxs-lookup"><span data-stu-id="d81f8-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="d81f8-123">商店选择器模块可以在“产品详细信息”页面 (PDP) 上用于查找附近可提走产品的商店。</span><span class="sxs-lookup"><span data-stu-id="d81f8-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="d81f8-124">商店选择器模块可以在购物车页面上用于查找附近可提走购物车中产品的商店。</span><span class="sxs-lookup"><span data-stu-id="d81f8-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="d81f8-125">商店选择器模块属性</span><span class="sxs-lookup"><span data-stu-id="d81f8-125">Store selector module properties</span></span>

| <span data-ttu-id="d81f8-126">属性名称</span><span class="sxs-lookup"><span data-stu-id="d81f8-126">Property name</span></span>             | <span data-ttu-id="d81f8-127">值</span><span class="sxs-lookup"><span data-stu-id="d81f8-127">Value</span></span>                 | <span data-ttu-id="d81f8-128">说明</span><span class="sxs-lookup"><span data-stu-id="d81f8-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="d81f8-129">搜索半径</span><span class="sxs-lookup"><span data-stu-id="d81f8-129">Search radius</span></span> | <span data-ttu-id="d81f8-130">数值</span><span class="sxs-lookup"><span data-stu-id="d81f8-130">Number</span></span> | <span data-ttu-id="d81f8-131">定义商店的搜索半径，以英里为单位。</span><span class="sxs-lookup"><span data-stu-id="d81f8-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="d81f8-132">如果未指定任何值，则使用默认的 50 英里搜索半径。</span><span class="sxs-lookup"><span data-stu-id="d81f8-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="d81f8-133">服务条款</span><span class="sxs-lookup"><span data-stu-id="d81f8-133">Terms of Service</span></span> | <span data-ttu-id="d81f8-134">URL</span><span class="sxs-lookup"><span data-stu-id="d81f8-134">URL</span></span>    |  <span data-ttu-id="d81f8-135">Bing 地图服务需要的服务条款 URL。</span><span class="sxs-lookup"><span data-stu-id="d81f8-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="d81f8-136">向页面添加商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="d81f8-136">Add a store selector module to a page</span></span>

<span data-ttu-id="d81f8-137">商店选择器模块需要产品的上下文，因此只能在购买框和购物车模块中使用。</span><span class="sxs-lookup"><span data-stu-id="d81f8-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="d81f8-138">商店选择器模块在这些模块之外不起作用。</span><span class="sxs-lookup"><span data-stu-id="d81f8-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="d81f8-139">有关如何将商店选择器模块添加到购买框模块的信息，请参阅[购买框模块](add-buy-box.md)。</span><span class="sxs-lookup"><span data-stu-id="d81f8-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="d81f8-140">有关如何将商店选择器模块添加到购物车模块的信息，请参阅[购物车模块](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="d81f8-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d81f8-141">其他资源</span><span class="sxs-lookup"><span data-stu-id="d81f8-141">Additional resources</span></span>

[<span data-ttu-id="d81f8-142">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="d81f8-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d81f8-143">购买框模块</span><span class="sxs-lookup"><span data-stu-id="d81f8-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="d81f8-144">购物车模块</span><span class="sxs-lookup"><span data-stu-id="d81f8-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d81f8-145">快速浏览 PDP</span><span class="sxs-lookup"><span data-stu-id="d81f8-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="d81f8-146">快速浏览购物车和结帐</span><span class="sxs-lookup"><span data-stu-id="d81f8-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="d81f8-147">设置交货方式</span><span class="sxs-lookup"><span data-stu-id="d81f8-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
