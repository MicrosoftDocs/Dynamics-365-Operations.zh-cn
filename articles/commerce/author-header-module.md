---
title: 页眉模块
description: 此主题介绍标题模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面标题。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 52069af5ca2211473d4a096ad850b5be1290bba1
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055442"
---
# <a name="header-module"></a><span data-ttu-id="5c532-103">标题模块</span><span class="sxs-lookup"><span data-stu-id="5c532-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5c532-104">此主题介绍标题模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面标题。</span><span class="sxs-lookup"><span data-stu-id="5c532-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5c532-105">概览</span><span class="sxs-lookup"><span data-stu-id="5c532-105">Overview</span></span>

<span data-ttu-id="5c532-106">在 Dynamics 365 Commerce 中，页面标题配置为页面片段，其中包含页眉、促销横幅和 cookie 同意模块。</span><span class="sxs-lookup"><span data-stu-id="5c532-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="5c532-107">标题模块包括站点徽标、指向导航层次结构的链接、指向站点上其他页面的链接、购物车图标模块、愿望列表符号、登录选项和搜索栏。</span><span class="sxs-lookup"><span data-stu-id="5c532-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="5c532-108">针对正在用于查看站点的设备（即针对台式机设备或移动设备）自动优化了标题模块。</span><span class="sxs-lookup"><span data-stu-id="5c532-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="5c532-109">例如，在移动设备上，导航栏折叠为 **菜单** 按钮（有时称为 *汉堡包按钮* ）。</span><span class="sxs-lookup"><span data-stu-id="5c532-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu* ).</span></span>

<span data-ttu-id="5c532-110">下图显示了主页上的标题模块的示例。</span><span class="sxs-lookup"><span data-stu-id="5c532-110">The following image shows an example of a header module on a home page.</span></span>

![标题模块示例](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="5c532-112">标题模块的属性</span><span class="sxs-lookup"><span data-stu-id="5c532-112">Properties of a header module</span></span>

<span data-ttu-id="5c532-113">标题模块支持 **徽标图像** 、 **徽标链接** 和 **我的帐户连结** 属性。</span><span class="sxs-lookup"><span data-stu-id="5c532-113">A header module supports **Logo image** , **Logo link** , and **My account links** properties.</span></span> 

<span data-ttu-id="5c532-114">**徽标图像** 和 **徽标链接** 属性用于在页面上定义徽标。</span><span class="sxs-lookup"><span data-stu-id="5c532-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="5c532-115">有关详细信息，请参阅[添加徽标](add-logo.md)。</span><span class="sxs-lookup"><span data-stu-id="5c532-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="5c532-116">**我的帐户链接** 属性可用于在标题中定义站点所有者想要显示快速链接的帐户页面。</span><span class="sxs-lookup"><span data-stu-id="5c532-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="5c532-117">标题模块中的可用模块</span><span class="sxs-lookup"><span data-stu-id="5c532-117">Modules that are available within a header module</span></span>

<span data-ttu-id="5c532-118">页眉模块中可使用以下模块：</span><span class="sxs-lookup"><span data-stu-id="5c532-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="5c532-119">**导航菜单** – 导航菜单提供渠道导航层次结构和其他静态导航链接。</span><span class="sxs-lookup"><span data-stu-id="5c532-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="5c532-120">有关详细信息，请参阅[导航菜单模块](nav-menu-module.md)。</span><span class="sxs-lookup"><span data-stu-id="5c532-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="5c532-121">**搜索** – 用户可使用搜索模块输入搜索词以搜索产品。</span><span class="sxs-lookup"><span data-stu-id="5c532-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="5c532-122">必须在 **站点设置 \> 扩展** 中提供默认搜索页面的 URL 和搜索查询参数。</span><span class="sxs-lookup"><span data-stu-id="5c532-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="5c532-123">搜索模块的属性可让您根据需要隐藏搜索按钮或标签。</span><span class="sxs-lookup"><span data-stu-id="5c532-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="5c532-124">搜索模块还支持自动建议选项，例如产品、关键字和类别搜索结果。</span><span class="sxs-lookup"><span data-stu-id="5c532-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="5c532-125">**购物车图标** - 购物车图标模块提供购物车图标，并显示任何给定时间购物车中的商品数量。</span><span class="sxs-lookup"><span data-stu-id="5c532-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="5c532-126">有关详细信息，请参阅[购物车图标模块](cart-icon-module.md)。</span><span class="sxs-lookup"><span data-stu-id="5c532-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="5c532-127">**站点选择器** - 站点选择器模块允许用户基于市场、地区和区域浏览不同的预定义站点。</span><span class="sxs-lookup"><span data-stu-id="5c532-127">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="5c532-128">有关详细信息，请参阅[站点选择器模块](site-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="5c532-128">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="5c532-129">**商店选择器** - 商店选择器模块可以包含在标题模块的商店选择器插槽中。</span><span class="sxs-lookup"><span data-stu-id="5c532-129">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="5c532-130">它允许用户浏览和查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="5c532-130">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="5c532-131">用户还可以指定首选商店。</span><span class="sxs-lookup"><span data-stu-id="5c532-131">Users can also specify a preferred store.</span></span> <span data-ttu-id="5c532-132">该商店随后将显示在标题中。</span><span class="sxs-lookup"><span data-stu-id="5c532-132">That store will then be shown in the header.</span></span> <span data-ttu-id="5c532-133">当商店选择器模块包含在标题模块中时，其 **模式** 属性必须设置为 **查找商店** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-133">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="5c532-134">有关详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="5c532-134">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="5c532-135">Dynamics 365 Commerce 10.0.11 版本中提供在标题模块中使用购物车图标模块的支持。</span><span class="sxs-lookup"><span data-stu-id="5c532-135">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="5c532-136">Dynamics 365 Commerce 10.0.14 版本中提供在标题模块中使用站点选择器模块的支持。</span><span class="sxs-lookup"><span data-stu-id="5c532-136">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="5c532-137">Dynamics 365 Commerce 10.0.15 版本中提供在标题模块中使用商店选择器模块的支持。</span><span class="sxs-lookup"><span data-stu-id="5c532-137">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="5c532-138">创建页面的标题片段</span><span class="sxs-lookup"><span data-stu-id="5c532-138">Create a header fragment for a page</span></span>

<span data-ttu-id="5c532-139">若要创建标题片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5c532-139">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="5c532-140">转到 **片段** ，选择 **新建** 创建新片段。</span><span class="sxs-lookup"><span data-stu-id="5c532-140">Go to **Fragments** , and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="5c532-141">在 **新建片段** 对话框中，选择 **容器** 模块，输入片段的名称，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-141">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="5c532-142">选择 **默认容器** 插槽，然后在右侧的属性窗格中将 **宽度** 属性设置为 **填充屏幕** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-142">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="5c532-143">在 **默认容器** 插槽中，选择省略号 ( **...** )，然后选择 **添加模块** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-143">In the **Default container** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5c532-144">在 **添加模块** 对话框中，选择 **Cookie 同意** 、 **页眉** 和 **促销横幅** 模块，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-144">In the **Add Module** dialog box, select the **Cookie consent** , **Header** , and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="5c532-145">在 **促销横幅** 模块的属性窗格中，选择 **添加消息** ，然后选择 **消息** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-145">In the properties pane of the **Promo banner** module, select **Add Message** , and then select **Message**.</span></span>
1. <span data-ttu-id="5c532-146">在 **消息** 对话框中，添加促销内容的文本和链接，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-146">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="5c532-147">在 **cookie 同意** 模块的属性窗格中，添加和配置站点隐私页面的文本和链接。</span><span class="sxs-lookup"><span data-stu-id="5c532-147">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="5c532-148">在标题模块的 **导航菜单** 插槽中，选择省略号 ( **...** )，然后选择 **添加模块** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-148">In the **Navigation menu** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5c532-149">在 **添加模块** 对话框中，选择 **导航菜单** 模块，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-149">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5c532-150">在导航菜单模块的属性窗格中 **导航菜单的来源** 下，选择 **Retail 服务器** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-150">In the property pane for the navigation menu module, under **Source for navigation menu** , select **Retail Server**.</span></span>
1. <span data-ttu-id="5c532-151">在导航菜单模块的属性窗格中 **静态菜单项** 下，选择 **添加菜单项** ，然后选择 **菜单项** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-151">In the property pane for the navigation menu module, under **Static menu items** , select **Add Menu item** , and then select **Menu item**.</span></span> 
1. <span data-ttu-id="5c532-152">在 **菜单项** 对话框中 **菜单项文本** 下，输入“联系人”。</span><span class="sxs-lookup"><span data-stu-id="5c532-152">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="5c532-153">在 **菜单项** 对话框中 **菜单项链接目标** 下，选择 **添加链接** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-153">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="5c532-154">在 **添加链接** 对话框中，选择站点的“联系人”页面的 URL，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-154">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="5c532-155">在 **菜单项** 对话框中，选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-155">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="5c532-156">在标题模块的 **搜索** 插槽中，选择省略号 ( **...** )，然后选择 **添加模块** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-156">In the **Search** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5c532-157">在 **添加模块** 对话框中，选择 **搜索** 模块，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-157">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5c532-158">在搜索模块的属性窗格中，根据需要配置属性。</span><span class="sxs-lookup"><span data-stu-id="5c532-158">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="5c532-159">在标题模块的 **购物车图标** 插槽中，选择省略号 ( **...** )，然后选择 **添加模块** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-159">In the **Cart icon** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5c532-160">在 **添加模块** 对话框中，选择 **购物车图标** 模块，然后选择 **确定** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-160">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5c532-161">在购物车图标模块的属性窗格中，根据需要配置属性。</span><span class="sxs-lookup"><span data-stu-id="5c532-161">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="5c532-162">如果希望在用户将鼠标悬停在购物车图标上时购物车图标显示购物车摘要（也称为迷你购物车），请选择 **显示迷你购物车** 。</span><span class="sxs-lookup"><span data-stu-id="5c532-162">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="5c532-163">选择 **保存** ，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="5c532-163">Select **Save** , select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="5c532-164">若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="5c532-164">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="5c532-165">在 **默认页** 模块的 **标题** 插槽中，添加创建的页脚片段。</span><span class="sxs-lookup"><span data-stu-id="5c532-165">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="5c532-166">选择 **保存** ，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="5c532-166">Select **Save** , select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c532-167">其他资源</span><span class="sxs-lookup"><span data-stu-id="5c532-167">Additional resources</span></span>

[<span data-ttu-id="5c532-168">模块库概述</span><span class="sxs-lookup"><span data-stu-id="5c532-168">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5c532-169">容器模块</span><span class="sxs-lookup"><span data-stu-id="5c532-169">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5c532-170">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="5c532-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="5c532-171">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="5c532-171">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="5c532-172">导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="5c532-172">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="5c532-173">Cookie 同意</span><span class="sxs-lookup"><span data-stu-id="5c532-173">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="5c532-174">页脚模块</span><span class="sxs-lookup"><span data-stu-id="5c532-174">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="5c532-175">站点选择器模块</span><span class="sxs-lookup"><span data-stu-id="5c532-175">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="5c532-176">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="5c532-176">Store selector module</span></span>](store-selector.md)
