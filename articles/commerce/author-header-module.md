---
title: 页眉模块
description: 此主题介绍页眉模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面页眉。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 569fb5ac3d30be30044ef9b928ecf1f6dde20aab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211416"
---
# <a name="header-module"></a><span data-ttu-id="1514b-103">标题模块</span><span class="sxs-lookup"><span data-stu-id="1514b-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1514b-104">此主题介绍页眉模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面页眉。</span><span class="sxs-lookup"><span data-stu-id="1514b-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1514b-105">在 Dynamics 365 Commerce 中，页面标题配置为页面片段，其中包含页眉、促销横幅和 cookie 同意模块。</span><span class="sxs-lookup"><span data-stu-id="1514b-105">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="1514b-106">标题模块包括站点徽标、指向导航层次结构的链接、指向站点上其他页面的链接、购物车图标模块、愿望列表符号、登录选项和搜索栏。</span><span class="sxs-lookup"><span data-stu-id="1514b-106">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="1514b-107">针对正在用于查看站点的设备（即针对台式机设备或移动设备）自动优化了标题模块。</span><span class="sxs-lookup"><span data-stu-id="1514b-107">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="1514b-108">例如，在移动设备上，导航栏折叠为 **菜单** 按钮（有时称为 *汉堡包按钮*）。</span><span class="sxs-lookup"><span data-stu-id="1514b-108">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="1514b-109">下图显示了主页上的标题模块的示例。</span><span class="sxs-lookup"><span data-stu-id="1514b-109">The following image shows an example of a header module on a home page.</span></span>

![标题模块示例](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="1514b-111">标题模块的属性</span><span class="sxs-lookup"><span data-stu-id="1514b-111">Properties of a header module</span></span>

<span data-ttu-id="1514b-112">标题模块支持 **徽标图像**、**徽标链接** 和 **我的帐户连结** 属性。</span><span class="sxs-lookup"><span data-stu-id="1514b-112">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="1514b-113">**徽标图像** 和 **徽标链接** 属性用于在页面上定义徽标。</span><span class="sxs-lookup"><span data-stu-id="1514b-113">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="1514b-114">有关详细信息，请参阅[添加徽标](add-logo.md)。</span><span class="sxs-lookup"><span data-stu-id="1514b-114">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="1514b-115">**我的帐户链接** 属性可用于在标题中定义站点所有者想要显示快速链接的帐户页面。</span><span class="sxs-lookup"><span data-stu-id="1514b-115">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="1514b-116">标题模块中的可用模块</span><span class="sxs-lookup"><span data-stu-id="1514b-116">Modules that are available within a header module</span></span>

<span data-ttu-id="1514b-117">页眉模块中可使用以下模块：</span><span class="sxs-lookup"><span data-stu-id="1514b-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="1514b-118">**导航菜单** – 导航菜单提供渠道导航层次结构和其他静态导航链接。</span><span class="sxs-lookup"><span data-stu-id="1514b-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="1514b-119">有关详细信息，请参阅[导航菜单模块](nav-menu-module.md)。</span><span class="sxs-lookup"><span data-stu-id="1514b-119">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="1514b-120">**搜索** – 用户可使用搜索模块输入搜索词以搜索产品。</span><span class="sxs-lookup"><span data-stu-id="1514b-120">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="1514b-121">必须在 **站点设置 \> 扩展** 中提供默认搜索页面的 URL 和搜索查询参数。</span><span class="sxs-lookup"><span data-stu-id="1514b-121">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="1514b-122">搜索模块的属性可让您根据需要隐藏搜索按钮或标签。</span><span class="sxs-lookup"><span data-stu-id="1514b-122">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="1514b-123">搜索模块还支持自动建议选项，例如产品、关键字和类别搜索结果。</span><span class="sxs-lookup"><span data-stu-id="1514b-123">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="1514b-124">**购物车图标** - 购物车图标模块提供购物车图标，并显示任何给定时间购物车中的商品数量。</span><span class="sxs-lookup"><span data-stu-id="1514b-124">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="1514b-125">有关详细信息，请参阅[购物车图标模块](cart-icon-module.md)。</span><span class="sxs-lookup"><span data-stu-id="1514b-125">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="1514b-126">**站点选择器** - 站点选择器模块允许用户基于市场、地区和区域浏览不同的预定义站点。</span><span class="sxs-lookup"><span data-stu-id="1514b-126">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="1514b-127">有关详细信息，请参阅[站点选择器模块](site-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="1514b-127">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="1514b-128">**商店选择器** - 商店选择器模块可以包含在标题模块的商店选择器插槽中。</span><span class="sxs-lookup"><span data-stu-id="1514b-128">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="1514b-129">它允许用户浏览和查找附近的商店。</span><span class="sxs-lookup"><span data-stu-id="1514b-129">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="1514b-130">用户还可以指定首选商店。</span><span class="sxs-lookup"><span data-stu-id="1514b-130">Users can also specify a preferred store.</span></span> <span data-ttu-id="1514b-131">该商店随后将显示在标题中。</span><span class="sxs-lookup"><span data-stu-id="1514b-131">That store will then be shown in the header.</span></span> <span data-ttu-id="1514b-132">当商店选择器模块包含在标题模块中时，其 **模式** 属性必须设置为 **查找商店**。</span><span class="sxs-lookup"><span data-stu-id="1514b-132">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="1514b-133">有关详细信息，请参阅[商店选择器模块](store-selector.md)。</span><span class="sxs-lookup"><span data-stu-id="1514b-133">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="1514b-134">Dynamics 365 Commerce 10.0.11 版本中提供在标题模块中使用购物车图标模块的支持。</span><span class="sxs-lookup"><span data-stu-id="1514b-134">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="1514b-135">Dynamics 365 Commerce 10.0.14 版本中提供在标题模块中使用站点选择器模块的支持。</span><span class="sxs-lookup"><span data-stu-id="1514b-135">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="1514b-136">Dynamics 365 Commerce 10.0.15 版本中提供在标题模块中使用商店选择器模块的支持。</span><span class="sxs-lookup"><span data-stu-id="1514b-136">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="1514b-137">创建页面的标题片段</span><span class="sxs-lookup"><span data-stu-id="1514b-137">Create a header fragment for a page</span></span>

<span data-ttu-id="1514b-138">若要创建标题片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1514b-138">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="1514b-139">转到 **片段**，选择 **新建** 创建新片段。</span><span class="sxs-lookup"><span data-stu-id="1514b-139">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="1514b-140">在 **新建片段** 对话框中，选择 **容器** 模块，输入片段的名称，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1514b-140">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="1514b-141">选择 **默认容器** 插槽，然后在右侧的属性窗格中将 **宽度** 属性设置为 **填充屏幕**。</span><span class="sxs-lookup"><span data-stu-id="1514b-141">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="1514b-142">在 **默认容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="1514b-142">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1514b-143">在 **添加模块** 对话框中，选择 **Cookie 同意**、**页眉** 和 **促销横幅** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1514b-143">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="1514b-144">在 **促销横幅** 模块的属性窗格中，选择 **添加消息**，然后选择 **消息**。</span><span class="sxs-lookup"><span data-stu-id="1514b-144">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="1514b-145">在 **消息** 对话框中，添加促销内容的文本和链接，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1514b-145">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="1514b-146">在 **cookie 同意** 模块的属性窗格中，添加和配置站点隐私页面的文本和链接。</span><span class="sxs-lookup"><span data-stu-id="1514b-146">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="1514b-147">在标题模块的 **导航菜单** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="1514b-147">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1514b-148">在 **添加模块** 对话框中，选择 **导航菜单** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1514b-148">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1514b-149">在导航菜单模块的属性窗格中 **导航菜单的来源** 下，选择 **Retail 服务器**。</span><span class="sxs-lookup"><span data-stu-id="1514b-149">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="1514b-150">在导航菜单模块的属性窗格中 **静态菜单项** 下，选择 **添加菜单项**，然后选择 **菜单项** 。</span><span class="sxs-lookup"><span data-stu-id="1514b-150">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="1514b-151">在 **菜单项** 对话框中 **菜单项文本** 下，输入“联系人”。</span><span class="sxs-lookup"><span data-stu-id="1514b-151">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="1514b-152">在 **菜单项** 对话框中 **菜单项链接目标** 下，选择 **添加链接** 。</span><span class="sxs-lookup"><span data-stu-id="1514b-152">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="1514b-153">在 **添加链接** 对话框中，选择站点的“联系人”页面的 URL，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1514b-153">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="1514b-154">在 **菜单项** 对话框中，选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1514b-154">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="1514b-155">在标题模块的 **搜索** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="1514b-155">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1514b-156">在 **添加模块** 对话框中，选择 **搜索** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1514b-156">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1514b-157">在搜索模块的属性窗格中，根据需要配置属性。</span><span class="sxs-lookup"><span data-stu-id="1514b-157">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="1514b-158">在标题模块的 **购物车图标** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="1514b-158">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1514b-159">在 **添加模块** 对话框中，选择 **购物车图标** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="1514b-159">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1514b-160">在购物车图标模块的属性窗格中，根据需要配置属性。</span><span class="sxs-lookup"><span data-stu-id="1514b-160">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="1514b-161">如果希望在用户将鼠标悬停在购物车图标上时购物车图标显示购物车摘要（也称为迷你购物车），请选择 **显示迷你购物车**。</span><span class="sxs-lookup"><span data-stu-id="1514b-161">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="1514b-162">选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="1514b-162">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="1514b-163">若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="1514b-163">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="1514b-164">在 **默认页** 模块的 **标题** 插槽中，添加创建的页脚片段。</span><span class="sxs-lookup"><span data-stu-id="1514b-164">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="1514b-165">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="1514b-165">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1514b-166">其他资源</span><span class="sxs-lookup"><span data-stu-id="1514b-166">Additional resources</span></span>

[<span data-ttu-id="1514b-167">模块库概述</span><span class="sxs-lookup"><span data-stu-id="1514b-167">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1514b-168">容器模块</span><span class="sxs-lookup"><span data-stu-id="1514b-168">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="1514b-169">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="1514b-169">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="1514b-170">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="1514b-170">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="1514b-171">导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="1514b-171">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="1514b-172">Cookie 同意</span><span class="sxs-lookup"><span data-stu-id="1514b-172">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="1514b-173">页脚模块</span><span class="sxs-lookup"><span data-stu-id="1514b-173">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="1514b-174">站点选择器模块</span><span class="sxs-lookup"><span data-stu-id="1514b-174">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="1514b-175">商店选择器模块</span><span class="sxs-lookup"><span data-stu-id="1514b-175">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]