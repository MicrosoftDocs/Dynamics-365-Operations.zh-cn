---
title: 购买框模块
description: 此主题介绍购买框模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3417156cbf3cb20a5190e5e51b61b3423816895a
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154055"
---
# <a name="buy-box-module"></a><span data-ttu-id="139e6-103">购买框模块</span><span class="sxs-lookup"><span data-stu-id="139e6-103">Buy box module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="139e6-104">此主题介绍购买框模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="139e6-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="139e6-105">概览</span><span class="sxs-lookup"><span data-stu-id="139e6-105">Overview</span></span>

<span data-ttu-id="139e6-106">术语*购买框*通常指的是产品详细信息页中的“第一屏”区域，用于承载进行产品购买所需全部最重要信息。</span><span class="sxs-lookup"><span data-stu-id="139e6-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="139e6-107">（“第一屏”区域在首次加载页面时显示，所以用户不必向下滚动即可看到。）</span><span class="sxs-lookup"><span data-stu-id="139e6-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="139e6-108">购买框模块是特殊容器，用于承载产品详细信息页购买框区域中显示的所有模块。</span><span class="sxs-lookup"><span data-stu-id="139e6-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="139e6-109">产品详细信息页的 URL 中包含产品 ID。</span><span class="sxs-lookup"><span data-stu-id="139e6-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="139e6-110">显示购买框模块所需全部信息派生自此产品 ID。</span><span class="sxs-lookup"><span data-stu-id="139e6-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="139e6-111">如果不提供产品 ID，则不能在页面中正确显示购买框模块。</span><span class="sxs-lookup"><span data-stu-id="139e6-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="139e6-112">因此，购买框模块只能在具有产品上下文的页面上使用。</span><span class="sxs-lookup"><span data-stu-id="139e6-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="139e6-113">要在没有产品上下文的页面（例如，主页或市场营销页面）上使用它，您必须进行其他自定义。</span><span class="sxs-lookup"><span data-stu-id="139e6-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="139e6-114">购买框模块属性和插槽</span><span class="sxs-lookup"><span data-stu-id="139e6-114">Buy box module properties and slots</span></span> 

<span data-ttu-id="139e6-115">在产品详细信息页，购买框拆分为两个区域：左侧媒体区域，右侧内容区域。</span><span class="sxs-lookup"><span data-stu-id="139e6-115">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="139e6-116">默认情况下，媒体区域列的宽度与内容区域列的宽度之比为 2:1。</span><span class="sxs-lookup"><span data-stu-id="139e6-116">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="139e6-117">在移动设备上，这两个区域堆叠，所以一个区域在另一个区域下方显示。</span><span class="sxs-lookup"><span data-stu-id="139e6-117">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="139e6-118">主题可用于自定义列宽和堆叠等级。</span><span class="sxs-lookup"><span data-stu-id="139e6-118">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="139e6-119">购买框模块呈现产品的标题、描述、价格和等级。</span><span class="sxs-lookup"><span data-stu-id="139e6-119">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="139e6-120">还可以让客户选择具有不同产品属性（例如尺寸、样式和颜色）的产品变型。</span><span class="sxs-lookup"><span data-stu-id="139e6-120">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="139e6-121">如果选择了产品变型，将更新购买框中的其他属性（如产品描述和图像）以反映变型信息。</span><span class="sxs-lookup"><span data-stu-id="139e6-121">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="139e6-122">提供数量选择器，以便客户可以指定要购买的商品数量。</span><span class="sxs-lookup"><span data-stu-id="139e6-122">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="139e6-123">可以在站点设置中定义可以购买的最大数量。</span><span class="sxs-lookup"><span data-stu-id="139e6-123">The maximum quantity that can be purchased can be defined in the site settings.</span></span>
 
<span data-ttu-id="139e6-124">客户还可以从购买框中执行一些操作，例如将产品添加到购物车，将产品添加到其愿望列表以及选择取货地点。</span><span class="sxs-lookup"><span data-stu-id="139e6-124">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="139e6-125">可以在产品或产品变型上执行这些操作。</span><span class="sxs-lookup"><span data-stu-id="139e6-125">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="139e6-126">要将产品添加到愿望列表中，客户必须先登录。</span><span class="sxs-lookup"><span data-stu-id="139e6-126">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="139e6-127">主题可用于删除或更改购买框产品属性和操作控件的顺序。</span><span class="sxs-lookup"><span data-stu-id="139e6-127">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="139e6-128">模块属性</span><span class="sxs-lookup"><span data-stu-id="139e6-128">Module properties</span></span>

- <span data-ttu-id="139e6-129">**标题标签** – 此属性定义产品标题的标题标签。</span><span class="sxs-lookup"><span data-stu-id="139e6-129">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="139e6-130">如果购买框位于页面顶部，则此属性应设置为 **h1** 以达到可访问性标准。</span><span class="sxs-lookup"><span data-stu-id="139e6-130">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="139e6-131">购买框模块中可使用的模块</span><span class="sxs-lookup"><span data-stu-id="139e6-131">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="139e6-132">**媒体库** – 此模块用于展示产品详细信息页上的产品图像。</span><span class="sxs-lookup"><span data-stu-id="139e6-132">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="139e6-133">它可以支持一到多个图像。</span><span class="sxs-lookup"><span data-stu-id="139e6-133">It can support one to many images.</span></span> <span data-ttu-id="139e6-134">还支持缩略图。</span><span class="sxs-lookup"><span data-stu-id="139e6-134">It also supports thumbnail images.</span></span> <span data-ttu-id="139e6-135">缩略图可以水平排列（作为图像下的一行），或垂直排列（作为图像旁边的一列）。</span><span class="sxs-lookup"><span data-stu-id="139e6-135">The thumbnail images can be arranged either horizontally (as a row below the image) or vertically (as a column next to the image).</span></span> <span data-ttu-id="139e6-136">可将媒体库模块添加到购买框模块中的**媒体**插槽。</span><span class="sxs-lookup"><span data-stu-id="139e6-136">The media gallery module can be added to the **Media** slot in the buy box module.</span></span> <span data-ttu-id="139e6-137">它当前仅支持图像。</span><span class="sxs-lookup"><span data-stu-id="139e6-137">It currently supports only images.</span></span> 
- <span data-ttu-id="139e6-138">**商店选择器** – 此模块显示附近可提货的商店的列表。</span><span class="sxs-lookup"><span data-stu-id="139e6-138">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="139e6-139">它使用户可以输入位置来查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="139e6-139">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="139e6-140">有关此模块的详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="139e6-140">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="139e6-141">购买框模块设置</span><span class="sxs-lookup"><span data-stu-id="139e6-141">Buy box module settings</span></span>

<span data-ttu-id="139e6-142">购买框模块中有可在**站点设置 \> 扩展**中配置的三个设置：</span><span class="sxs-lookup"><span data-stu-id="139e6-142">Buy box modules have three settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="139e6-143">**最大数量** – 此属于用于指定可以添加到购物车的每种项的最大数量。</span><span class="sxs-lookup"><span data-stu-id="139e6-143">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="139e6-144">例如，一位零售商可能决定一笔交易中只能出售每种产品 10 件。</span><span class="sxs-lookup"><span data-stu-id="139e6-144">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="139e6-145">**库存检查** – 如果此值设置为 **True**，则只有在购买框模块确信某种项有现货时，才能将此项添加到购物车中。</span><span class="sxs-lookup"><span data-stu-id="139e6-145">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="139e6-146">将在项发货时和在商店中提货时执行库存检查。</span><span class="sxs-lookup"><span data-stu-id="139e6-146">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="139e6-147">如果此值设置为 **False**，则向购物车添加项和下订单前，不进行库存检查。</span><span class="sxs-lookup"><span data-stu-id="139e6-147">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="139e6-148">**库存缓冲区** – 此属性用于指定库存的缓冲区号。</span><span class="sxs-lookup"><span data-stu-id="139e6-148">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="139e6-149">库存会被实时维护，如果多位客户下订单，则很难维持精确的库存计数。</span><span class="sxs-lookup"><span data-stu-id="139e6-149">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="139e6-150">进行库存检查时，如果库存比缓冲区数量少，则将产品视为库存不足。</span><span class="sxs-lookup"><span data-stu-id="139e6-150">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="139e6-151">因此，当通过多个渠道快速进行销售，导致库存计数无法充分同步时，出售库存不足的项的风险较低。</span><span class="sxs-lookup"><span data-stu-id="139e6-151">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="139e6-152">Commerce Scale Unit 交互</span><span class="sxs-lookup"><span data-stu-id="139e6-152">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="139e6-153">购买框模块使用 Commerce Scale Unit API 检索产品信息。</span><span class="sxs-lookup"><span data-stu-id="139e6-153">The buy box module retrieves product information using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="139e6-154">产品详细信息页中的产品 ID 用于检索所有信息。</span><span class="sxs-lookup"><span data-stu-id="139e6-154">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="139e6-155">向页面添加购买框模块</span><span class="sxs-lookup"><span data-stu-id="139e6-155">Add a buy box module to a page</span></span>

<span data-ttu-id="139e6-156">若要向新页面添加购买框模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="139e6-156">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="139e6-157">创建一个名称为**购买框片段**的片段，然后向其添加一个购买框模块。</span><span class="sxs-lookup"><span data-stu-id="139e6-157">Create a fragment that is named **buy box fragment**, and add a buy box module to it.</span></span>
1. <span data-ttu-id="139e6-158">在该购买框模块的**媒体**插槽中，添加一个媒体库模块。</span><span class="sxs-lookup"><span data-stu-id="139e6-158">In the **Media** slot of the buy box module, add a media gallery module.</span></span>
1. <span data-ttu-id="139e6-159">在购买框模块的**商店选择器**插槽中，添加商店选择器模块。</span><span class="sxs-lookup"><span data-stu-id="139e6-159">In the **Store selector** slot of the buy box module, add a store selector module.</span></span>
1. <span data-ttu-id="139e6-160">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="139e6-160">Check in the page, and publish it.</span></span>
1. <span data-ttu-id="139e6-161">为产品详细信息页创建一个模块，然后命名为 **PDP 模板**。</span><span class="sxs-lookup"><span data-stu-id="139e6-161">Create a template for a product details page, and name it **PDP template**.</span></span>
1. <span data-ttu-id="139e6-162">添加默认页。</span><span class="sxs-lookup"><span data-stu-id="139e6-162">Add a default page.</span></span>
1. <span data-ttu-id="139e6-163">在默认页的**主**插槽中，添加一个购买框片段。</span><span class="sxs-lookup"><span data-stu-id="139e6-163">In the **Main** slot of the default page, add a buy box fragment.</span></span>
1. <span data-ttu-id="139e6-164">保存模板，完成编辑，然后发布。</span><span class="sxs-lookup"><span data-stu-id="139e6-164">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="139e6-165">使用您刚才创建的模板创建一个名称为 **PDP 页**的页面。</span><span class="sxs-lookup"><span data-stu-id="139e6-165">Use the template that you just created to create a page that is named **PDP page**.</span></span>
1. <span data-ttu-id="139e6-166">在新页的**主**插槽中，添加一个购买框片段。</span><span class="sxs-lookup"><span data-stu-id="139e6-166">In the **Main** slot of the new page, add a buy box fragment.</span></span>
1. <span data-ttu-id="139e6-167">保存并预览页面。</span><span class="sxs-lookup"><span data-stu-id="139e6-167">Save and preview the page.</span></span> <span data-ttu-id="139e6-168">在上一页的 URL 中添加查询字符串参数 **?productid=&lt;product id&gt;**。</span><span class="sxs-lookup"><span data-stu-id="139e6-168">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="139e6-169">这样，将把产品上下文用于加载和显示上一页。</span><span class="sxs-lookup"><span data-stu-id="139e6-169">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="139e6-170">保存页面，完成编辑，然后发布。</span><span class="sxs-lookup"><span data-stu-id="139e6-170">Save the page, finish editing it, and publish it.</span></span> <span data-ttu-id="139e6-171">应该会在产品详细信息页显示一个购买框。</span><span class="sxs-lookup"><span data-stu-id="139e6-171">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="139e6-172">其他资源</span><span class="sxs-lookup"><span data-stu-id="139e6-172">Additional resources</span></span>

[<span data-ttu-id="139e6-173">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="139e6-173">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="139e6-174">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="139e6-174">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="139e6-175">容器模块</span><span class="sxs-lookup"><span data-stu-id="139e6-175">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="139e6-176">购物车模块</span><span class="sxs-lookup"><span data-stu-id="139e6-176">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="139e6-177">结账模块</span><span class="sxs-lookup"><span data-stu-id="139e6-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="139e6-178">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="139e6-178">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="139e6-179">页眉模块</span><span class="sxs-lookup"><span data-stu-id="139e6-179">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="139e6-180">页脚模块</span><span class="sxs-lookup"><span data-stu-id="139e6-180">Footer module</span></span>](author-footer-module.md)
