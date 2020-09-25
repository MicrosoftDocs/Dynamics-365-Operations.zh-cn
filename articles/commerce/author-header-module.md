---
title: 页眉模块
description: 此主题介绍标题模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面标题。
author: anupamar
manager: annbe
ms.date: 08/31/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb440a8fb67888c9411ad5998fead4d00982b436
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761216"
---
# <a name="header-module"></a><span data-ttu-id="c4ff2-103">标题模块</span><span class="sxs-lookup"><span data-stu-id="c4ff2-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c4ff2-104">此主题介绍标题模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面标题。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c4ff2-105">概览</span><span class="sxs-lookup"><span data-stu-id="c4ff2-105">Overview</span></span>

<span data-ttu-id="c4ff2-106">在 Dynamics 365 Commerce 中，页面标题配置为页面片段，其中包含页眉、促销横幅和 cookie 同意模块。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="c4ff2-107">标题模块包括站点徽标、指向导航层次结构的链接、指向站点上其他页面的链接、购物车图标模块、愿望列表符号、登录选项和搜索栏。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="c4ff2-108">针对正在用于查看站点的设备（即针对台式机设备或移动设备）自动优化了标题模块。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="c4ff2-109">例如，在移动设备上，导航栏折叠为**菜单**按钮（有时称为*汉堡包按钮*）。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="c4ff2-110">下图显示了主页上的标题模块的示例。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-110">The following image shows an example of a header module on a home page.</span></span>

![标题模块示例](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="c4ff2-112">标题模块的属性</span><span class="sxs-lookup"><span data-stu-id="c4ff2-112">Properties of a header module</span></span>

<span data-ttu-id="c4ff2-113">标题模块支持**徽标图像**、**徽标链接**和**我的帐户连结**属性。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="c4ff2-114">**徽标图像**和**徽标链接**属性用于在页面上定义徽标。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="c4ff2-115">有关详细信息，请参阅[添加徽标](add-logo.md)。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="c4ff2-116">**我的帐户链接**属性可用于在标题中定义站点所有者想要显示快速链接的帐户页面。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="c4ff2-117">标题模块中的可用模块</span><span class="sxs-lookup"><span data-stu-id="c4ff2-117">Modules that are available within a header module</span></span>

<span data-ttu-id="c4ff2-118">页眉模块中可使用以下模块：</span><span class="sxs-lookup"><span data-stu-id="c4ff2-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="c4ff2-119">**导航菜单** – 导航菜单提供渠道导航层次结构和其他静态导航链接。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="c4ff2-120">有关详细信息，请参阅[导航菜单模块](nav-menu-module.md)。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="c4ff2-121">**搜索** – 用户可使用搜索模块输入搜索词以搜索产品。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="c4ff2-122">必须在**站点设置 \> 扩展**中提供默认搜索页面的 URL 和搜索查询参数。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="c4ff2-123">搜索模块的属性可让您根据需要隐藏搜索按钮或标签。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="c4ff2-124">搜索模块还支持自动建议选项，例如产品、关键字和类别搜索结果。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="c4ff2-125">**购物车图标** - 购物车图标模块提供购物车图标，并显示任何给定时间购物车中的商品数量。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="c4ff2-126">有关详细信息，请参阅[购物车图标模块](cart-icon-module.md)。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="c4ff2-127">创建页面的标题片段</span><span class="sxs-lookup"><span data-stu-id="c4ff2-127">Create a header fragment for a page</span></span>

<span data-ttu-id="c4ff2-128">若要创建标题片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="c4ff2-129">转到**片段**，选择**新建**创建新片段。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="c4ff2-130">在**新建片段**对话框中，选择**容器**模块，输入片段的名称，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="c4ff2-131">选择**默认容器**插槽，然后在右侧的属性窗格中将**宽度**属性设置为**填充屏幕**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="c4ff2-132">在**默认容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c4ff2-133">在**添加模块**对话框中，选择 **Cookie 同意**、**页眉**和**促销横幅**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="c4ff2-134">在**促销横幅**模块的属性窗格中，选择**添加消息**，然后选择**消息**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="c4ff2-135">在**消息**对话框中，添加促销内容的文本和链接，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="c4ff2-136">在 **cookie 同意**模块的属性窗格中，添加和配置站点隐私页面的文本和链接。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="c4ff2-137">在标题模块的**导航菜单**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c4ff2-138">在**添加模块**对话框中，选择**导航菜单**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c4ff2-139">在导航菜单模块的属性窗格中**导航菜单的来源**下，选择 **Retail 服务器**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="c4ff2-140">在导航菜单模块的属性窗格中**静态菜单项**下，选择**添加菜单项**，然后选择**菜单项** 。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="c4ff2-141">在**菜单项**对话框中**菜单项文本**下，输入“联系人”。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="c4ff2-142">在**菜单项**对话框中**菜单项链接目标**下，选择**添加链接** 。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="c4ff2-143">在**添加链接**对话框中，选择站点的“联系人”页面的 URL，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="c4ff2-144">在**菜单项**对话框中，选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="c4ff2-145">在标题模块的**搜索**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c4ff2-146">在**添加模块**对话框中，选择**搜索**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c4ff2-147">在搜索模块的属性窗格中，根据需要配置属性。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="c4ff2-148">在标题模块的**购物车图标**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c4ff2-149">在**添加模块**对话框中，选择**购物车图标**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="c4ff2-150">在购物车图标模块的属性窗格中，根据需要配置属性。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="c4ff2-151">如果希望在用户将鼠标悬停在购物车图标上时购物车图标显示购物车摘要（也称为迷你购物车），请选择**显示迷你购物车**。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="c4ff2-152">选择**保存**，选择**完成编辑**签入片段，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="c4ff2-153">若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="c4ff2-154">在**默认页**模块的**标题**插槽中，添加创建的页脚片段。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="c4ff2-155">选择**保存**，选择**完成编辑**签入模板，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="c4ff2-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4ff2-156">其他资源</span><span class="sxs-lookup"><span data-stu-id="c4ff2-156">Additional resources</span></span>

[<span data-ttu-id="c4ff2-157">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="c4ff2-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c4ff2-158">容器模块</span><span class="sxs-lookup"><span data-stu-id="c4ff2-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c4ff2-159">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="c4ff2-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c4ff2-160">促销横幅模块</span><span class="sxs-lookup"><span data-stu-id="c4ff2-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="c4ff2-161">导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="c4ff2-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="c4ff2-162">Cookie 同意</span><span class="sxs-lookup"><span data-stu-id="c4ff2-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="c4ff2-163">页脚模块</span><span class="sxs-lookup"><span data-stu-id="c4ff2-163">Footer module</span></span>](author-footer-module.md)
