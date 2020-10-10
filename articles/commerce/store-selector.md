---
title: 商店选择器模块
description: 此主题介绍商店选择器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 4438e46d4653a0cd2060092695f08613cd696f4e
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818242"
---
# <a name="store-selector-module"></a><span data-ttu-id="20015-103">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="20015-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="20015-104">此主题介绍商店选择器模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="20015-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="20015-105">概览</span><span class="sxs-lookup"><span data-stu-id="20015-105">Overview</span></span>

<span data-ttu-id="20015-106">客户可以在在线购买后使用商店选择器模块在选定商店提货。</span><span class="sxs-lookup"><span data-stu-id="20015-106">Customers can use the store selector module to pick up a product in a selected store after an online purchase.</span></span> <span data-ttu-id="20015-107">在 Commerce 版本 10.0.13 中，商店选择器模块还包括其他功能，可以展示显示附近商店的**查找商店**页面。</span><span class="sxs-lookup"><span data-stu-id="20015-107">In Commerce version 10.0.13, the store selector module also includes additional capabilities that can showcase a **Find a Store** page that shows nearby stores.</span></span>

<span data-ttu-id="20015-108">商店选择器模块允许用户输入位置（城市、省/自治区/直辖市、地址等）来在搜索半径内搜索商店。</span><span class="sxs-lookup"><span data-stu-id="20015-108">The store selector module lets users enter a location (city, state, address, and so on) to search for stores within a search radius.</span></span> <span data-ttu-id="20015-109">首次打开此模块时，它使用客户的浏览器位置来查找商店（如果确认同意）。</span><span class="sxs-lookup"><span data-stu-id="20015-109">When the module is first opened, it uses the customer's browser location to find stores (if consent is provided).</span></span>

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="20015-110">电子商务中商店选择器模块的使用</span><span class="sxs-lookup"><span data-stu-id="20015-110">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="20015-111">可以在产品详细信息页面 (PDP) 使用商店选择器模块来选择提货商店。</span><span class="sxs-lookup"><span data-stu-id="20015-111">A store selector module can be used on a product details page (PDP) to select a store for pickup.</span></span>
- <span data-ttu-id="20015-112">可以在购物车页面使用商店选择器模块来选择提货商店。</span><span class="sxs-lookup"><span data-stu-id="20015-112">A store selector module can be used on a cart page to select a store for pickup.</span></span>
- <span data-ttu-id="20015-113">商店选择器模块可以在显示所有可选择商店的独立页面上使用。</span><span class="sxs-lookup"><span data-stu-id="20015-113">A store selector module can be used on a standalone page that shows all available stores.</span></span>

## <a name="bing-maps-integration"></a><span data-ttu-id="20015-114">必应地图集成</span><span class="sxs-lookup"><span data-stu-id="20015-114">Bing Maps integration</span></span>

<span data-ttu-id="20015-115">商店选择器模块与[必应地图 REST 应用程序编程接口 (API)](https://docs.microsoft.com/bingmaps/rest-services/) 集成来使用必应的地理编码和自动建议功能。</span><span class="sxs-lookup"><span data-stu-id="20015-115">The store selector module is integrated with the [Bing Maps REST application programming interfaces (APIs)](https://docs.microsoft.com/bingmaps/rest-services/) to use Bing's Geocoding and Autosuggest features.</span></span> <span data-ttu-id="20015-116">必须提供必应地图 API 密钥，并且必须将其添加到 Commerce headquarters 内的共享参数页面中。</span><span class="sxs-lookup"><span data-stu-id="20015-116">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="20015-117">地理编码 API 用于将位置转换为纬度和经度值。</span><span class="sxs-lookup"><span data-stu-id="20015-117">The Geocoding API is used to convert a location to latitude and longitude values.</span></span> <span data-ttu-id="20015-118">与自动建议 API 的集成用于在用户在搜索字段中输入位置时显示搜索建议。</span><span class="sxs-lookup"><span data-stu-id="20015-118">The integration with the Autosuggest API is used to show search suggestions when users enter locations in the search field.</span></span>

<span data-ttu-id="20015-119">对于自动建议 REST API，您必须确保根据站点的内容安全策略 (CSP) 允许以下 URL（也称为“加入允许列表”）。</span><span class="sxs-lookup"><span data-stu-id="20015-119">For the Autosuggest REST API, you must ensure that the following URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="20015-120">通过在站点的各个 CSP 指令中添加允许的 URL（例如，**img-src**），在 Commerce 站点构建器中完成此设置。</span><span class="sxs-lookup"><span data-stu-id="20015-120">This setup is done in Commerce site builder, by adding allowed URLs to various CSP directives for the site (for example, **img-src**).</span></span> <span data-ttu-id="20015-121">有关详细信息，请参阅[内容安全策略](manage-csp.md)。</span><span class="sxs-lookup"><span data-stu-id="20015-121">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="20015-122">对于 **connect-src** 指令，添加 **&#42;.bing.com**。</span><span class="sxs-lookup"><span data-stu-id="20015-122">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="20015-123">对于 **img-src** 指令，添加 **&#42;.virtualearth.net**。</span><span class="sxs-lookup"><span data-stu-id="20015-123">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="20015-124">对于 **script-src** 指令，**添加 &#42;.bing.com、&#42;.virtualearth.net**。</span><span class="sxs-lookup"><span data-stu-id="20015-124">To the **script-src** directive, **add &#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="20015-125">对于 **script style-src** 指令，添加 **&#42;.bing.com**。</span><span class="sxs-lookup"><span data-stu-id="20015-125">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>
 
## <a name="pickup-in-store-mode"></a><span data-ttu-id="20015-126">店内提货模式</span><span class="sxs-lookup"><span data-stu-id="20015-126">Pickup in store mode</span></span>

<span data-ttu-id="20015-127">商店选择器模块支持**店内提货**模式，其显示可提货的商店列表。</span><span class="sxs-lookup"><span data-stu-id="20015-127">The store selector module supports a **Pick up in store** mode that shows a list of stores where a product is available for pickup.</span></span> <span data-ttu-id="20015-128">它还在列表中显示每个商店的营业时间和产品库存。</span><span class="sxs-lookup"><span data-stu-id="20015-128">It also shows store hours and product inventory for each store in the list.</span></span> <span data-ttu-id="20015-129">如果产品的交货方式设置为在所选商店**提货**，商店选择器模块将需要产品的上下文来呈现产品可用性并允许用户将产品添加到购物车。</span><span class="sxs-lookup"><span data-stu-id="20015-129">The store selector module requires the context of a product to render product availability and to let the user add the product to the cart, if the product's delivery mode is set to **pickup** at the selected store.</span></span> <span data-ttu-id="20015-130">有关详细信息，请参阅[库存设置](inventory-settings.md)。</span><span class="sxs-lookup"><span data-stu-id="20015-130">For more information, see [Inventory settings](inventory-settings.md).</span></span> 

<span data-ttu-id="20015-131">商店选择器模块可以添加到购买框模块中，来显示可提货的商店。</span><span class="sxs-lookup"><span data-stu-id="20015-131">The store selector module can be added to a buy box module on a PDP to show stores where a product is available for pickup.</span></span> <span data-ttu-id="20015-132">也可以将其添加到购物车模块。</span><span class="sxs-lookup"><span data-stu-id="20015-132">It can also be added to a cart module.</span></span> <span data-ttu-id="20015-133">如果是这种情况，商店选择器模块将显示购物车中每个行项的提货选项。</span><span class="sxs-lookup"><span data-stu-id="20015-133">In this case, the store selector module shows pickup options for each line item in the cart.</span></span> <span data-ttu-id="20015-134">商店选择器模块还可以通过扩展和自定义添加到其他页面或模块。</span><span class="sxs-lookup"><span data-stu-id="20015-134">The store selector module can also be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="20015-135">为了使此方案正常工作，产品应配置为使用**提货**交货方式。</span><span class="sxs-lookup"><span data-stu-id="20015-135">For this scenario to work, products should be configured so that the **pickup** delivery mode is used.</span></span> <span data-ttu-id="20015-136">否则，此模块不会在产品页面上显示。</span><span class="sxs-lookup"><span data-stu-id="20015-136">Otherwise, the module won't be shown on the product pages.</span></span> <span data-ttu-id="20015-137">有关如何配置交货方式的详细信息，请参阅[设置交货方式](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)。</span><span class="sxs-lookup"><span data-stu-id="20015-137">For more information about how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="20015-138">下图显示了 PDP 上使用的商店选择器模块的示例。</span><span class="sxs-lookup"><span data-stu-id="20015-138">The following image shows an example of a store selector module used on a PDP.</span></span>

![PDP 上使用的商店选择器模块的示例](./media/BOPIS.PNG)

## <a name="find-stores-mode"></a><span data-ttu-id="20015-140">查找商店模式</span><span class="sxs-lookup"><span data-stu-id="20015-140">Find stores mode</span></span>

<span data-ttu-id="20015-141">商店选择器模块还支持**查找商店**模式。</span><span class="sxs-lookup"><span data-stu-id="20015-141">The store selector module also supports a **Find stores** mode.</span></span> <span data-ttu-id="20015-142">此模式可用于创建显示可选择商店及其信息的商店位置页面。</span><span class="sxs-lookup"><span data-stu-id="20015-142">This mode can be used to create a store locations page that shows available stores and their information.</span></span> <span data-ttu-id="20015-143">在此模式下，商店选择器模块可以在没有产品上下文的情况下工作，并可以在任何站点页面上用作独立模块。</span><span class="sxs-lookup"><span data-stu-id="20015-143">In this mode, the store selector module works without product context and can be used as a standalone module on any site page.</span></span> <span data-ttu-id="20015-144">此外，如果为模块打开了相关设置，用户可以选择一个商店作为其首选商店。</span><span class="sxs-lookup"><span data-stu-id="20015-144">In addition, if the relevant settings are turned on for the module, users can select a store as their preferred store.</span></span> <span data-ttu-id="20015-145">当选择一个商店作为用户的首选商店时，该商店 ID 将保留在浏览器 Cookie 中。</span><span class="sxs-lookup"><span data-stu-id="20015-145">When a store is selected as a user's preferred store, the store ID is maintained in the browser cookie.</span></span> <span data-ttu-id="20015-146">因此，用户必须接受 Cookie 同意消息。</span><span class="sxs-lookup"><span data-stu-id="20015-146">Therefore, the user must accept a cookie consent message.</span></span>

<span data-ttu-id="20015-147">下图显示了与商店位置页面上的地图模块一起使用的商店选择器模块的示例。</span><span class="sxs-lookup"><span data-stu-id="20015-147">The following illustration shows an example of a store selector module that is used together with a map module on a store locations page.</span></span>

![商店位置页面上的商店选择器模块和地图模块的示例](./media/ecommerce-Storelocator.PNG)

## <a name="render-a-map"></a><span data-ttu-id="20015-149">呈现地图</span><span class="sxs-lookup"><span data-stu-id="20015-149">Render a map</span></span>

<span data-ttu-id="20015-150">商店选择器模块可与地图模块一起使用，来在地图上显示商店位置。</span><span class="sxs-lookup"><span data-stu-id="20015-150">The store selector module can be used together with the map module to show the store locations on a map.</span></span> <span data-ttu-id="20015-151">有关地图模块的详细信息，请参阅[地图模块](map-module.md)</span><span class="sxs-lookup"><span data-stu-id="20015-151">For more information about the map module, see [Map module](map-module.md)</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="20015-152">商店选择器模块属性</span><span class="sxs-lookup"><span data-stu-id="20015-152">Store selector module properties</span></span>

| <span data-ttu-id="20015-153">属性名称</span><span class="sxs-lookup"><span data-stu-id="20015-153">Property name</span></span> | <span data-ttu-id="20015-154">值</span><span class="sxs-lookup"><span data-stu-id="20015-154">Value</span></span> | <span data-ttu-id="20015-155">说明</span><span class="sxs-lookup"><span data-stu-id="20015-155">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="20015-156">标题</span><span class="sxs-lookup"><span data-stu-id="20015-156">Heading</span></span> | <span data-ttu-id="20015-157">文本</span><span class="sxs-lookup"><span data-stu-id="20015-157">Text</span></span> | <span data-ttu-id="20015-158">模块的标题。</span><span class="sxs-lookup"><span data-stu-id="20015-158">The heading for the module.</span></span> |
| <span data-ttu-id="20015-159">模式</span><span class="sxs-lookup"><span data-stu-id="20015-159">Mode</span></span> | <span data-ttu-id="20015-160">**查找商店**或**店内提货**</span><span class="sxs-lookup"><span data-stu-id="20015-160">**Find stores** or **Pick up in store**</span></span> | <span data-ttu-id="20015-161">**查找商店**模式显示可选择的商店。</span><span class="sxs-lookup"><span data-stu-id="20015-161">**Find stores** mode shows available stores.</span></span> <span data-ttu-id="20015-162">**店内提货**模式可让用户选择要提货的商店。</span><span class="sxs-lookup"><span data-stu-id="20015-162">**Pick up in store** mode lets users select a store for pickup.</span></span> |
| <span data-ttu-id="20015-163">样式</span><span class="sxs-lookup"><span data-stu-id="20015-163">Style</span></span> | <span data-ttu-id="20015-164">**对话**或**内联**</span><span class="sxs-lookup"><span data-stu-id="20015-164">**Dialog** or **Inline**</span></span> | <span data-ttu-id="20015-165">此模块可以内联或在对话框中呈现。</span><span class="sxs-lookup"><span data-stu-id="20015-165">The module can be rendered either inline or in a dialog box.</span></span> |
| <span data-ttu-id="20015-166">设置为首选商店</span><span class="sxs-lookup"><span data-stu-id="20015-166">Set as preferred store</span></span> | <span data-ttu-id="20015-167">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="20015-167">**True** or **False**</span></span> | <span data-ttu-id="20015-168">当此属性设置为 **True**，用户可以设置首选商店。</span><span class="sxs-lookup"><span data-stu-id="20015-168">When this property is set to **True**, users can set a preferred store.</span></span> <span data-ttu-id="20015-169">此功能需要用户接受 Cookie 同意消息。</span><span class="sxs-lookup"><span data-stu-id="20015-169">This feature requires that users accept a cookie consent message.</span></span> |
| <span data-ttu-id="20015-170">显示所有商店</span><span class="sxs-lookup"><span data-stu-id="20015-170">Show all stores</span></span> | <span data-ttu-id="20015-171">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="20015-171">**True** or **False**</span></span> | <span data-ttu-id="20015-172">当此属性设置为 **True** 时，用户可以绕过**搜索半径**属性，查看所有商店。</span><span class="sxs-lookup"><span data-stu-id="20015-172">When this property is set to **True**, users can bypass the **Search radius** property and view all stores.</span></span> |
| <span data-ttu-id="20015-173">自动建议选项：最多结果</span><span class="sxs-lookup"><span data-stu-id="20015-173">Autosuggest options: Max results</span></span> | <span data-ttu-id="20015-174">数值</span><span class="sxs-lookup"><span data-stu-id="20015-174">Number</span></span> | <span data-ttu-id="20015-175">此属性定义可通过必应自动建议 API 显示的自动建议结果的最大数量。</span><span class="sxs-lookup"><span data-stu-id="20015-175">This property defines the maximum number of autosuggest results that can be shown via the Bing Autosuggest API.</span></span> |
| <span data-ttu-id="20015-176">搜索半径</span><span class="sxs-lookup"><span data-stu-id="20015-176">Search radius</span></span> | <span data-ttu-id="20015-177">数值</span><span class="sxs-lookup"><span data-stu-id="20015-177">Number</span></span> | <span data-ttu-id="20015-178">此属性定义商店的搜索半径，以英里为单位。</span><span class="sxs-lookup"><span data-stu-id="20015-178">This property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="20015-179">如果未指定任何值，则使用默认的 50 英里搜索半径。</span><span class="sxs-lookup"><span data-stu-id="20015-179">If no value is specified, the default search radius of 50 miles is used.</span></span> |
| <span data-ttu-id="20015-180">服务条款</span><span class="sxs-lookup"><span data-stu-id="20015-180">Terms of service</span></span> | <span data-ttu-id="20015-181">URL</span><span class="sxs-lookup"><span data-stu-id="20015-181">URL</span></span> |  <span data-ttu-id="20015-182">此属性指定使用必应地图服务所需的服务条款 URL。</span><span class="sxs-lookup"><span data-stu-id="20015-182">This property specifies the terms of service URL that is required to use the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="20015-183">向页面添加商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="20015-183">Add a store selector module to a page</span></span>

<span data-ttu-id="20015-184">对于**店内提货**模式，此模块只能在 PDP 和购物车页面使用。</span><span class="sxs-lookup"><span data-stu-id="20015-184">For **Pickup in store** mode, the module can be used only on PDPs and cart pages.</span></span> <span data-ttu-id="20015-185">您必须在模块的属性窗格中将模式设置为**店内提货**。</span><span class="sxs-lookup"><span data-stu-id="20015-185">You must set the mode to **Pickup in store** in the module's property pane.</span></span>

- <span data-ttu-id="20015-186">有关如何将商店选择器模块添加到购买框模块的信息，请参阅[购买框模块](add-buy-box.md)。</span><span class="sxs-lookup"><span data-stu-id="20015-186">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="20015-187">有关如何将商店选择器模块添加到购物车模块的信息，请参阅[购物车模块](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="20015-187">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

<span data-ttu-id="20015-188">要将商店选择器模块配置为在商店位置页面显示可选择的商店（如本主题前面的插图中所示），请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="20015-188">To configure the store selector module to show available stores for a store locations page, as in the illustration that appears earlier in this topic, follow these steps.</span></span>

1. <span data-ttu-id="20015-189">转到**模板**，选择**新建**创建新模板。</span><span class="sxs-lookup"><span data-stu-id="20015-189">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="20015-190">在**新建模板**对话框的**模板名称**下，输入**市场营销模板**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="20015-190">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="20015-191">选择**保存**，选择**完成编辑**签入模板，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="20015-191">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="20015-192">转到**页面**，选择**新建**创建新页面。</span><span class="sxs-lookup"><span data-stu-id="20015-192">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="20015-193">在**选择模板**对话框中，选择**市场营销模板**模板。</span><span class="sxs-lookup"><span data-stu-id="20015-193">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="20015-194">在**页面名称**下，输入**商店位置**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="20015-194">Under **Page name**, enter **Store locations**, and then select **OK**.</span></span>
1. <span data-ttu-id="20015-195">在新页面的**主**插槽，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="20015-195">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="20015-196">在**添加模块**对话框中，选择**容器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="20015-196">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="20015-197">在**容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="20015-197">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="20015-198">在**添加模块**对话框中，选择 **2 列容器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="20015-198">In the **Add Module** dialog box, select the **Container with 2 columns** module, and then select **OK**.</span></span>
1. <span data-ttu-id="20015-199">在模块的属性窗格中，将**宽度**值设置为**填充容器**。</span><span class="sxs-lookup"><span data-stu-id="20015-199">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="20015-200">将**超小查看端口配置**值设置为 **100%**。</span><span class="sxs-lookup"><span data-stu-id="20015-200">Set the **X-Small view port column configuration** value to **100%**.</span></span>
1. <span data-ttu-id="20015-201">将**小查看端口配置**值设置为 **100%**。</span><span class="sxs-lookup"><span data-stu-id="20015-201">Set the **Small view port column configuration** value to **100%**.</span></span>
1. <span data-ttu-id="20015-202">将**中等查看端口配置**值设置为 **33% 67%**。</span><span class="sxs-lookup"><span data-stu-id="20015-202">Set the **Medium view port column configuration** value to **33% 67%**.</span></span>
1. <span data-ttu-id="20015-203">将**大查看端口配置**值设置为 **33% 67%**。</span><span class="sxs-lookup"><span data-stu-id="20015-203">Set the **Large view port column configuration** value to **33% 67%**.</span></span>
1. <span data-ttu-id="20015-204">在 **2 列容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="20015-204">In the **Container with 2 columns** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="20015-205">在**添加模块**对话框中，选择**商店选择器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="20015-205">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="20015-206">在模块的属性窗格中，将**模式**值设置为**查找商店**。</span><span class="sxs-lookup"><span data-stu-id="20015-206">In the module's properties pane, set the **Mode** value to **Find stores**.</span></span>
1. <span data-ttu-id="20015-207">设置**搜索半径**值，以英里为单位。</span><span class="sxs-lookup"><span data-stu-id="20015-207">Set the **Search radius** value in miles.</span></span>
1. <span data-ttu-id="20015-208">根据您的需要设置其他属性，如**设置为首选商店**、**显示所有商店**和**启用自动建议**。</span><span class="sxs-lookup"><span data-stu-id="20015-208">Set other properties, such as **Set as preferred store**, **Show all stores**, and **Enable auto suggestion**, as you require.</span></span>
1. <span data-ttu-id="20015-209">在 **2 列容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="20015-209">In the **Container with 2 columns** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="20015-210">在**添加模块**对话框中，选择**地图**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="20015-210">In the **Add Module** dialog box, select the **Map** module, and then select **OK**.</span></span>
1. <span data-ttu-id="20015-211">在模块的属性窗格中，根据需要设置任何其他属性。</span><span class="sxs-lookup"><span data-stu-id="20015-211">In the module's properties pane, set any additional properties as you require.</span></span>
1. <span data-ttu-id="20015-212">选择**保存**，选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="20015-212">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="20015-213">其他资源</span><span class="sxs-lookup"><span data-stu-id="20015-213">Additional resources</span></span>

[<span data-ttu-id="20015-214">模块库概述</span><span class="sxs-lookup"><span data-stu-id="20015-214">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="20015-215">购买框模块</span><span class="sxs-lookup"><span data-stu-id="20015-215">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="20015-216">购物车模块</span><span class="sxs-lookup"><span data-stu-id="20015-216">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="20015-217">快速浏览 PDP</span><span class="sxs-lookup"><span data-stu-id="20015-217">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="20015-218">快速浏览购物车和结帐</span><span class="sxs-lookup"><span data-stu-id="20015-218">Quick tour of cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="20015-219">设置交货方式</span><span class="sxs-lookup"><span data-stu-id="20015-219">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="20015-220">为您的组织管理必应地图</span><span class="sxs-lookup"><span data-stu-id="20015-220">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="20015-221">必应地图 REST API</span><span class="sxs-lookup"><span data-stu-id="20015-221">Bing Maps REST APIs</span></span>](https://docs.microsoft.com/bingmaps/rest-services/)

[<span data-ttu-id="20015-222">地图模块</span><span class="sxs-lookup"><span data-stu-id="20015-222">Maps module</span></span>](map-module.md)
