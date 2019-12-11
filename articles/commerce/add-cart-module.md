---
title: 购物车模块
description: 此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696753"
---
# <a name="cart-module"></a><span data-ttu-id="9cfe3-103">购物车模块</span><span class="sxs-lookup"><span data-stu-id="9cfe3-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9cfe3-104">此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9cfe3-105">概览</span><span class="sxs-lookup"><span data-stu-id="9cfe3-105">Overview</span></span>

<span data-ttu-id="9cfe3-106">购物车模块是用于承载展示购物车中的项所需全部模块的容器。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-106">A cart module is container that is used to host all the modules that are required to showcase items that are in the cart.</span></span> <span data-ttu-id="9cfe3-107">例如，其中包含已添加到购物车的所有项、订单摘要和促销代码。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-107">For example, it includes all the items that have been added to the cart, the order summary, and promotional codes.</span></span>

<span data-ttu-id="9cfe3-108">购物车模块基于购物车 ID 显示数据。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-108">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="9cfe3-109">购物车 ID 是整个站点中可用的浏览器 cookie。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-109">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="9cfe3-110">购物车模块属性和插槽</span><span class="sxs-lookup"><span data-stu-id="9cfe3-110">Cart module properties and slots</span></span>

<span data-ttu-id="9cfe3-111">作为容器，购物车模块控制某些基本属性，如标题和宽度。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-111">As a container, a cart module controls some basic properties, such as the heading and the width.</span></span> <span data-ttu-id="9cfe3-112">标题通常是**购物袋**、**您的购物车**或**购物车中的项**之类文本。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-112">The heading is typically text such as **Shopping bag**, **Your cart**, or **Items in your cart**.</span></span> <span data-ttu-id="9cfe3-113">宽度设置决定容器内的模块是适应该容器，还是填满屏幕。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-113">The width setting determines whether the modules inside the container must fit within that container, or whether they can fill the screen.</span></span>

<span data-ttu-id="9cfe3-114">购物车页面分为多个区域：购物车明细项、订单摘要和结帐，以及“在店内查找”功能。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-114">The cart page is divided into multiple regions: cart line items, order summary and checkout, and "find in store" functionality.</span></span> <span data-ttu-id="9cfe3-115">每个区域映射到购物车模块中的一个插槽，而每个插槽则接受一组预定义的模块。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-115">Each region is mapped to a slot in the cart module, and every slot accepts a predefined set of modules.</span></span>

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="9cfe3-116">购物车模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="9cfe3-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="9cfe3-117">**购物车明细项** – 此模块显示已添加到购物车的每件项的摘要。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-117">**Cart line items** – This module shows a summary of every item that has been added to the cart.</span></span> <span data-ttu-id="9cfe3-118">信息包括产品标题、所选维度、价格、数量和折扣。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-118">The information includes the product title, selected dimensions, price, quantity, and discounts.</span></span> <span data-ttu-id="9cfe3-119">此模块还支持“从购物车中删除”和“添加到愿望列表”等操作。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-119">This module also supports actions such as "remove from cart" and "add to wish list."</span></span> <span data-ttu-id="9cfe3-120">每件明细项都有一个选项，用于为项发货和从商店取项。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-120">For each line item, there is an option to ship the item or pick it up from the store.</span></span> <span data-ttu-id="9cfe3-121">必须在店内提货模块中配置此选项。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-121">This option must be configured separately in the pick up in store module.</span></span>
- <span data-ttu-id="9cfe3-122">**订单摘要** – 此模块显示订单摘要。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-122">**Order summary** – This module shows an order summary.</span></span> <span data-ttu-id="9cfe3-123">信息包括小计、发货、税和节省。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-123">The information includes the subtotal, shipping, taxes, and savings.</span></span> <span data-ttu-id="9cfe3-124">可以为此模块配置标题。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-124">A heading can be configured for this module.</span></span>
- <span data-ttu-id="9cfe3-125">**促销代码** – 客户可使用此模块兑换促销代码。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-125">**Promo code** – This module lets the customer redeem promotional codes.</span></span> <span data-ttu-id="9cfe3-126">可以应用或删除促销代码。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-126">A promotional code can be applied or removed.</span></span>
- <span data-ttu-id="9cfe3-127">**结帐** – 此模块发起结帐操作，并将用户重定向到结帐页。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-127">**Checkout** – This module initiates the checkout action and redirects the user to the checkout page.</span></span> <span data-ttu-id="9cfe3-128">必须为此模块配置三个链接：</span><span class="sxs-lookup"><span data-stu-id="9cfe3-128">Three links must be configured for this module:</span></span>

    - <span data-ttu-id="9cfe3-129">**结帐** – 如果客户尚未登录，此链接将强制客户登录。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-129">**Checkout** – This link forces customers to sign in if they aren't already signed in.</span></span>
    - <span data-ttu-id="9cfe3-130">**来宾结帐** – 此链接用于供匿名客户下订单。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-130">**Guest checkout** – This link lets anonymous customers place orders.</span></span> <span data-ttu-id="9cfe3-131">仅当客户未登录时才显示。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-131">It's shown only when customers aren't signed in.</span></span>
    - <span data-ttu-id="9cfe3-132">**返回购物** – 此链接用于供客户转到主页或其他任何页，以便继续购物。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-132">**Back to shopping** – This link lets customers go to the home page or any other page, so that they can continue to shop.</span></span>

- <span data-ttu-id="9cfe3-133">**内容丰富块** – 此模块支持购物车模块中的自定义消息。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-133">**Content rich block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="9cfe3-134">消息由内容管理系统 (CMS) 驱动。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-134">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="9cfe3-135">可以添加任何消息，如“订单问题请致电 1-800-Fabrikam”。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-135">Any message can be added, such as "For issues with the order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="9cfe3-136">**在商店中提货** – 此模块显示附近可提货的商店的列表。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-136">**Pick up in store** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="9cfe3-137">默认情况下，此模块显示客户位置半径 50 英里内的商店。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-137">By default, this module shows stores that are within a 50-mile radius of the customer's location.</span></span> <span data-ttu-id="9cfe3-138">但是，可以在模块中自定义搜索半径。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-138">However, the search radius can be customized in the module.</span></span> <span data-ttu-id="9cfe3-139">如果开启了库存检查功能，并且显示了相应的现货或库存不足消息，则可对每家商店执行库存检查。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-139">For each store, an inventory check is done, if the inventory check functionality is turned on, and an appropriate in-stock or out-of-stock message is shown.</span></span>
- <span data-ttu-id="9cfe3-140">**通过 Bing 地图搜索商店** – 可在店内提货模块中使用此模块。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-140">**Store search by Bing Maps** – This module can be used inside the pick up in store module.</span></span> <span data-ttu-id="9cfe3-141">可供客户通过输入位置搜索商店。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-141">It lets customers search for stores by entering a location.</span></span> <span data-ttu-id="9cfe3-142">Bing 地图地理编码应用程序编程接口 (API) 用于将客户输入的位置转换为维度和经度。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-142">The Bing Maps geocoding application programming interface (API) is used to convert the location that the customer entered to a latitude and a longitude.</span></span> <span data-ttu-id="9cfe3-143">如果不使用此模块，则仅显示客户当前位置附近的商店，客户不能搜索其他位置。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-143">If this module isn't used, only stores that are near the customer's current location are shown, and the customer can't search for a different location.</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="9cfe3-144">购物车模块设置</span><span class="sxs-lookup"><span data-stu-id="9cfe3-144">Cart module settings</span></span>

<span data-ttu-id="9cfe3-145">购物车模块中有三个可配置的设置：</span><span class="sxs-lookup"><span data-stu-id="9cfe3-145">Cart modules have three settings that can be configured:</span></span>

- <span data-ttu-id="9cfe3-146">**最大数量** – 可以添加到购物车的每种项的最大数量。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-146">**Maximum quantity** – The maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="9cfe3-147">例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-147">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="9cfe3-148">**库存检查** – 如果此值设置为 **True**，则只有在购买框模块确信某种项有现货时，才能将此项添加到购物车中。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-148">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="9cfe3-149">将在项发货时和在商店中提货时执行库存检查。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-149">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="9cfe3-150">如果此值设置为 **False**，则向购物车添加项和下订单前，不进行库存检查。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-150">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="9cfe3-151">**库存缓冲区** – 库存实时维护，如果多位客户下订单，则很难维持精确的库存计数。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-151">**Inventory buffer** – Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="9cfe3-152">因此，可以为库存定义缓冲区。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-152">Therefore, a buffer can be defined for inventory.</span></span> <span data-ttu-id="9cfe3-153">进行库存检查时，如果库存比缓冲区数量少，则将产品视为库存不足。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-153">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="9cfe3-154">因此，当通过多个渠道快速进行销售，导致库存计数无法充分同步时，出售库存不足的项的风险较低。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-154">Therefore, when sales occur quickly through several channels, so that the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>

## <a name="retail-server-interaction"></a><span data-ttu-id="9cfe3-155">Retail Server 交互</span><span class="sxs-lookup"><span data-stu-id="9cfe3-155">Retail Server interaction</span></span>

<span data-ttu-id="9cfe3-156">购物车模块使用 Retail Server API 检索产品信息。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-156">The cart module retrieves product information by using Retail Server APIs.</span></span> <span data-ttu-id="9cfe3-157">浏览器 cookie 中的购物车 ID 用于从 Retail Server 检索所有产品信息。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-157">The cart ID from the browser cookie is used to retrieve all the product information from Retail Server.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="9cfe3-158">向页面添加购物车模块</span><span class="sxs-lookup"><span data-stu-id="9cfe3-158">Add a cart module to a page</span></span>

<span data-ttu-id="9cfe3-159">若要向新页面添加购物车模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-159">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="9cfe3-160">创建一个名称为**购物车片段**的片段，然后向其添加一个购物车模块。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-160">Create a fragment that is named **cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="9cfe3-161">在购物车模块的**购物车明细项**插槽中，添加购物车明细项模块。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-161">In the **Cart line items** slot of the cart module, add a cart line items module.</span></span>
1. <span data-ttu-id="9cfe3-162">在**订单摘要**插槽中，添加一个订单摘要模块。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-162">In the **Order summary** slot, add an order summary module.</span></span>
1. <span data-ttu-id="9cfe3-163">在**促销代码**插槽中，添加一个促销代码模块。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-163">In the **Promo code** slot, add a promo code module.</span></span>
1. <span data-ttu-id="9cfe3-164">在**结帐**插槽中，添加一个结帐模块。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-164">In the **Checkout** slot, add a checkout module.</span></span>
1. <span data-ttu-id="9cfe3-165">在**在店内查找**插槽中，添加一个店内提货模块。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-165">In the **Find in Store** slot, add a pick up in store module.</span></span>
1. <span data-ttu-id="9cfe3-166">在店内提货模块内的插槽中，选择**商店搜索**插槽，然后添加一个通过 Bing 地图搜索商店模块。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-166">In the pick up in store module, select the **Store search** slot, and add a store search by Bing Maps module.</span></span>
1. <span data-ttu-id="9cfe3-167">签入片段，然后发布。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-167">Check in the fragment, and publish it.</span></span>
1. <span data-ttu-id="9cfe3-168">创建一个名称为**购物车模板**的模板，然后向其添加刚才创建的购物车片段。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-168">Create a template that is named **cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="9cfe3-169">保存模板，签入，然后发布。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-169">Save the template, check it in, and publish it.</span></span>
1. <span data-ttu-id="9cfe3-170">创建一个使用新模板的页面。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-170">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="9cfe3-171">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-171">Save and preview the page.</span></span>
1. <span data-ttu-id="9cfe3-172">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="9cfe3-172">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9cfe3-173">其他资源</span><span class="sxs-lookup"><span data-stu-id="9cfe3-173">Additional resources</span></span>

[<span data-ttu-id="9cfe3-174">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="9cfe3-174">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9cfe3-175">容器模块</span><span class="sxs-lookup"><span data-stu-id="9cfe3-175">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="9cfe3-176">购买框模块</span><span class="sxs-lookup"><span data-stu-id="9cfe3-176">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="9cfe3-177">结帐模块</span><span class="sxs-lookup"><span data-stu-id="9cfe3-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="9cfe3-178">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="9cfe3-178">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="9cfe3-179">页眉模块</span><span class="sxs-lookup"><span data-stu-id="9cfe3-179">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="9cfe3-180">页脚模块</span><span class="sxs-lookup"><span data-stu-id="9cfe3-180">Footer module</span></span>](author-footer-module.md)
