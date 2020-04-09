---
title: 购物车模块
description: 此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154009"
---
# <a name="cart-module"></a><span data-ttu-id="3f20c-103">购物车模块</span><span class="sxs-lookup"><span data-stu-id="3f20c-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f20c-104">此主题介绍购物车模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="3f20c-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3f20c-105">概览</span><span class="sxs-lookup"><span data-stu-id="3f20c-105">Overview</span></span>

<span data-ttu-id="3f20c-106">购物车模块显示客户继续结帐之前已添加到购物车中的物品。</span><span class="sxs-lookup"><span data-stu-id="3f20c-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="3f20c-107">此模块还显示订单摘要，并让客户可以应用或删除促销代码。</span><span class="sxs-lookup"><span data-stu-id="3f20c-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="3f20c-108">购物车模块支持登录结帐和访客结帐。</span><span class="sxs-lookup"><span data-stu-id="3f20c-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="3f20c-109">它还支持**返回购物**链接。</span><span class="sxs-lookup"><span data-stu-id="3f20c-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="3f20c-110">您可以在**站点设置 \> 扩展 \> 路由**中为此链接配置路由。</span><span class="sxs-lookup"><span data-stu-id="3f20c-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="3f20c-111">购物车模块根据购物车 ID 呈现数据，购物车 ID 是整个站点可用的浏览器 cookie。</span><span class="sxs-lookup"><span data-stu-id="3f20c-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="3f20c-112">购物车模块属性和插槽</span><span class="sxs-lookup"><span data-stu-id="3f20c-112">Cart module properties and slots</span></span>

<span data-ttu-id="3f20c-113">购物车模块有一个**标题**属性，此属性可以设置为**购物袋**和**购物车中的商品**之类的值。</span><span class="sxs-lookup"><span data-stu-id="3f20c-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="3f20c-114">购物车模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="3f20c-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="3f20c-115">**文本块** – 此模块支持购物车模块中的自定义消息。</span><span class="sxs-lookup"><span data-stu-id="3f20c-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="3f20c-116">消息由内容管理系统 (CMS) 驱动。</span><span class="sxs-lookup"><span data-stu-id="3f20c-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="3f20c-117">可以添加任何消息，如“订单问题请致电 1-800-Fabrikam”。</span><span class="sxs-lookup"><span data-stu-id="3f20c-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="3f20c-118">**商店选择器** – 此模块显示附近可提货的商店的列表。</span><span class="sxs-lookup"><span data-stu-id="3f20c-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="3f20c-119">它使用户可以输入位置来查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="3f20c-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="3f20c-120">有关此模块的详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="3f20c-120">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="3f20c-121">购物车模块设置</span><span class="sxs-lookup"><span data-stu-id="3f20c-121">Cart module settings</span></span>

<span data-ttu-id="3f20c-122">购物车框模块中有可在**站点设置 \> 扩展**中配置的以下设置：</span><span class="sxs-lookup"><span data-stu-id="3f20c-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="3f20c-123">**最大数量** – 此属于用于指定可以添加到购物车的每种项的最大数量。</span><span class="sxs-lookup"><span data-stu-id="3f20c-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="3f20c-124">例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。</span><span class="sxs-lookup"><span data-stu-id="3f20c-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="3f20c-125">**库存检查** – 如果此值设置为 **True**，则只有在购买框模块确信某种项有现货时，才能将此项添加到购物车中。</span><span class="sxs-lookup"><span data-stu-id="3f20c-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="3f20c-126">将在物料发货时和在商店中提货时执行库存检查。</span><span class="sxs-lookup"><span data-stu-id="3f20c-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="3f20c-127">如果此值设置为 **False**，则向购物车添加项和下订单前，不进行库存检查。</span><span class="sxs-lookup"><span data-stu-id="3f20c-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="3f20c-128">**库存缓冲区** – 此属性用于指定库存的缓冲区号。</span><span class="sxs-lookup"><span data-stu-id="3f20c-128">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="3f20c-129">库存会被实时维护，如果多位客户下订单，则很难维持精确的库存计数。</span><span class="sxs-lookup"><span data-stu-id="3f20c-129">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="3f20c-130">进行库存检查时，如果库存比缓冲区数量少，则将产品视为库存不足。</span><span class="sxs-lookup"><span data-stu-id="3f20c-130">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="3f20c-131">因此，当通过多个渠道快速进行销售，导致库存计数无法充分同步时，出售库存不足的项的风险较低。</span><span class="sxs-lookup"><span data-stu-id="3f20c-131">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="3f20c-132">**返回购物** – 该属性用于指定**返回购物**链接的路由。</span><span class="sxs-lookup"><span data-stu-id="3f20c-132">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="3f20c-133">可以在站点级别配置路由，让零售商可以将客户带回到站点的主页或其他任何页面。</span><span class="sxs-lookup"><span data-stu-id="3f20c-133">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="3f20c-134">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="3f20c-134">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="3f20c-135">购物车模块使用 Commerce Scale Unit API 检索产品信息。</span><span class="sxs-lookup"><span data-stu-id="3f20c-135">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="3f20c-136">浏览器 cookie 中的购物车 ID 用于从 Commerce Scale Unit 检索所有产品信息。</span><span class="sxs-lookup"><span data-stu-id="3f20c-136">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="3f20c-137">向页面添加购物车模块</span><span class="sxs-lookup"><span data-stu-id="3f20c-137">Add a cart module to a page</span></span>

<span data-ttu-id="3f20c-138">若要向新页面添加购物车模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="3f20c-138">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3f20c-139">创建一个名称为**购物车片段**的片段，然后向新片段添加一个购物车模块。</span><span class="sxs-lookup"><span data-stu-id="3f20c-139">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="3f20c-140">向购物车模块添加一个标题。</span><span class="sxs-lookup"><span data-stu-id="3f20c-140">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="3f20c-141">将商店选择器模块添加到购物车模块。</span><span class="sxs-lookup"><span data-stu-id="3f20c-141">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="3f20c-142">保存片段，完成编辑，然后发布片段。</span><span class="sxs-lookup"><span data-stu-id="3f20c-142">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="3f20c-143">创建一个名称为**购物车模板**的模板，然后添加刚才创建的购物车片段。</span><span class="sxs-lookup"><span data-stu-id="3f20c-143">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="3f20c-144">保存模板，完成编辑，然后发布模板。</span><span class="sxs-lookup"><span data-stu-id="3f20c-144">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="3f20c-145">创建一个使用新模板的页面。</span><span class="sxs-lookup"><span data-stu-id="3f20c-145">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="3f20c-146">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="3f20c-146">Save and preview the page.</span></span>
1. <span data-ttu-id="3f20c-147">完成页面编辑，然后发布页面。</span><span class="sxs-lookup"><span data-stu-id="3f20c-147">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f20c-148">其他资源</span><span class="sxs-lookup"><span data-stu-id="3f20c-148">Additional resources</span></span>

[<span data-ttu-id="3f20c-149">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="3f20c-149">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3f20c-150">容器模块</span><span class="sxs-lookup"><span data-stu-id="3f20c-150">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="3f20c-151">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="3f20c-151">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="3f20c-152">购买框模块</span><span class="sxs-lookup"><span data-stu-id="3f20c-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3f20c-153">结账模块</span><span class="sxs-lookup"><span data-stu-id="3f20c-153">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3f20c-154">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="3f20c-154">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3f20c-155">页眉模块</span><span class="sxs-lookup"><span data-stu-id="3f20c-155">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="3f20c-156">页脚模块</span><span class="sxs-lookup"><span data-stu-id="3f20c-156">Footer module</span></span>](author-footer-module.md)
