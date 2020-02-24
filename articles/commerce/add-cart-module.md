---
title: 购物车模块
description: 此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025428"
---
# <a name="cart-module"></a><span data-ttu-id="04b36-103">购物车模块</span><span class="sxs-lookup"><span data-stu-id="04b36-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="04b36-104">此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="04b36-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="04b36-105">概览</span><span class="sxs-lookup"><span data-stu-id="04b36-105">Overview</span></span>

<span data-ttu-id="04b36-106">购物车模块用于显示客户继续结帐之前已添加到购物车中的物品。</span><span class="sxs-lookup"><span data-stu-id="04b36-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="04b36-107">例如，其中包含已添加到购物车的所有项和订单摘要。</span><span class="sxs-lookup"><span data-stu-id="04b36-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="04b36-108">它还允许客户应用或删除促销代码。</span><span class="sxs-lookup"><span data-stu-id="04b36-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="04b36-109">购物车模块支持登录结帐和访客结帐。</span><span class="sxs-lookup"><span data-stu-id="04b36-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="04b36-110">它还支持**返回购物**链接。</span><span class="sxs-lookup"><span data-stu-id="04b36-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="04b36-111">您可以在**站点设置 \> 扩展 \> 路由**中为此链接配置路由。</span><span class="sxs-lookup"><span data-stu-id="04b36-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="04b36-112">购物车模块基于购物车 ID 显示数据。</span><span class="sxs-lookup"><span data-stu-id="04b36-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="04b36-113">购物车 ID 是整个站点中可用的浏览器 cookie。</span><span class="sxs-lookup"><span data-stu-id="04b36-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="04b36-114">购物车模块属性和插槽</span><span class="sxs-lookup"><span data-stu-id="04b36-114">Cart module properties and slots</span></span>

<span data-ttu-id="04b36-115">购物车模块有一个**标题**属性，此属性可以设置为**购物袋**和**购物车中的商品**之类的值。</span><span class="sxs-lookup"><span data-stu-id="04b36-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="04b36-116">购物车模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="04b36-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="04b36-117">**文本块** – 此模块支持购物车模块中的自定义消息。</span><span class="sxs-lookup"><span data-stu-id="04b36-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="04b36-118">消息由内容管理系统 (CMS) 驱动。</span><span class="sxs-lookup"><span data-stu-id="04b36-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="04b36-119">可以添加任何消息，如“订单问题请致电 1-800-Fabrikam”。</span><span class="sxs-lookup"><span data-stu-id="04b36-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="04b36-120">**商店选择器** – 此模块显示附近可提货的商店的列表。</span><span class="sxs-lookup"><span data-stu-id="04b36-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="04b36-121">它使用户可以输入位置来查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="04b36-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="04b36-122">商店选择器模块与 Bing 地图地理编码应用程序编程接口 (API) 集成在一起，以将位置转换为纬度和经度。</span><span class="sxs-lookup"><span data-stu-id="04b36-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="04b36-123">必须提供 Bing 地图 API 密钥，并且必须将其添加到 Dynamics 365 Retail 内的“零售共享参数”页面中。</span><span class="sxs-lookup"><span data-stu-id="04b36-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="04b36-124">该模块支持**搜索半径**和**服务条款链接**这两个属性。</span><span class="sxs-lookup"><span data-stu-id="04b36-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="04b36-125">**搜索半径**属性定义以英里为单位的商店搜索半径。</span><span class="sxs-lookup"><span data-stu-id="04b36-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="04b36-126">如果未指定任何值，则使用默认搜索半径（50 英里）。</span><span class="sxs-lookup"><span data-stu-id="04b36-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="04b36-127">如果使用了 Bings 地图或任何外部服务，**服务条款链接**属性可用于提供指向服务条款的链接。</span><span class="sxs-lookup"><span data-stu-id="04b36-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="04b36-128">Bing 地图服务需要一个服务条款链接。</span><span class="sxs-lookup"><span data-stu-id="04b36-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="04b36-129">购物车模块设置</span><span class="sxs-lookup"><span data-stu-id="04b36-129">Cart module settings</span></span>

<span data-ttu-id="04b36-130">购物车框模块中有可在**站点设置 \> 扩展**中配置的以下设置：</span><span class="sxs-lookup"><span data-stu-id="04b36-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="04b36-131">**最大数量** – 此属于用于指定可以添加到购物车的每种项的最大数量。</span><span class="sxs-lookup"><span data-stu-id="04b36-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="04b36-132">例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。</span><span class="sxs-lookup"><span data-stu-id="04b36-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="04b36-133">**库存检查** – 如果此值设置为 **True**，则只有在购买框模块确信某种项有现货时，才能将此项添加到购物车中。</span><span class="sxs-lookup"><span data-stu-id="04b36-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="04b36-134">将在项发货时和在商店中提货时执行库存检查。</span><span class="sxs-lookup"><span data-stu-id="04b36-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="04b36-135">如果此值设置为 **False**，则向购物车添加项和下订单前，不进行库存检查。</span><span class="sxs-lookup"><span data-stu-id="04b36-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="04b36-136">**库存缓冲区** – 此属性用于指定库存的缓冲区号。</span><span class="sxs-lookup"><span data-stu-id="04b36-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="04b36-137">库存会被实时维护，如果多位客户下订单，则很难维持精确的库存计数。</span><span class="sxs-lookup"><span data-stu-id="04b36-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="04b36-138">进行库存检查时，如果库存比缓冲区数量少，则将产品视为库存不足。</span><span class="sxs-lookup"><span data-stu-id="04b36-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="04b36-139">因此，当通过多个渠道快速进行销售，导致库存计数无法充分同步时，出售库存不足的项的风险较低。</span><span class="sxs-lookup"><span data-stu-id="04b36-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="04b36-140">**返回购物** – 该属性用于指定**返回购物**链接的路由。</span><span class="sxs-lookup"><span data-stu-id="04b36-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="04b36-141">可以在站点级别配置此路由。</span><span class="sxs-lookup"><span data-stu-id="04b36-141">This route can be configured at the site level.</span></span> <span data-ttu-id="04b36-142">通过这种配置，零售商可以将客户带回到站点上的主页或任何其他页面。</span><span class="sxs-lookup"><span data-stu-id="04b36-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="04b36-143">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="04b36-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="04b36-144">购物车模块使用 Commerce Scale Unit API 检索产品信息。</span><span class="sxs-lookup"><span data-stu-id="04b36-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="04b36-145">浏览器 cookie 中的购物车 ID 用于从 Commerce Scale Unit 检索所有产品信息。</span><span class="sxs-lookup"><span data-stu-id="04b36-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="04b36-146">向页面添加购物车模块</span><span class="sxs-lookup"><span data-stu-id="04b36-146">Add a cart module to a page</span></span>

<span data-ttu-id="04b36-147">若要向新页面添加购物车模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="04b36-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="04b36-148">创建一个名称为**购物车片段**的片段，然后向其添加一个购物车模块。</span><span class="sxs-lookup"><span data-stu-id="04b36-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="04b36-149">向购物车模块添加一个标题。</span><span class="sxs-lookup"><span data-stu-id="04b36-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="04b36-150">将商店选择器模块添加到购物车模块。</span><span class="sxs-lookup"><span data-stu-id="04b36-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="04b36-151">保存片段，完成编辑，然后发布。</span><span class="sxs-lookup"><span data-stu-id="04b36-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="04b36-152">创建一个名称为**购物车模板**的模板，然后向其添加刚才创建的购物车片段。</span><span class="sxs-lookup"><span data-stu-id="04b36-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="04b36-153">保存模板，完成编辑，然后发布。</span><span class="sxs-lookup"><span data-stu-id="04b36-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="04b36-154">创建一个使用新模板的页面。</span><span class="sxs-lookup"><span data-stu-id="04b36-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="04b36-155">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="04b36-155">Save and preview the page.</span></span>
1. <span data-ttu-id="04b36-156">编辑完页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="04b36-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="04b36-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="04b36-157">Additional resources</span></span>

[<span data-ttu-id="04b36-158">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="04b36-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="04b36-159">容器模块</span><span class="sxs-lookup"><span data-stu-id="04b36-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="04b36-160">购买框模块</span><span class="sxs-lookup"><span data-stu-id="04b36-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="04b36-161">结帐模块</span><span class="sxs-lookup"><span data-stu-id="04b36-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="04b36-162">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="04b36-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="04b36-163">页眉模块</span><span class="sxs-lookup"><span data-stu-id="04b36-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="04b36-164">页脚模块</span><span class="sxs-lookup"><span data-stu-id="04b36-164">Footer module</span></span>](author-footer-module.md)
