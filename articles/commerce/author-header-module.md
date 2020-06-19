---
title: 页眉模块
description: 此主题介绍标题模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面标题。
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: a5f7ad7d9c5ff63c3c3a8fe38275eec0d138891d
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411190"
---
# <a name="header-module"></a><span data-ttu-id="97cbe-103">标题模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97cbe-104">此主题介绍标题模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面标题。</span><span class="sxs-lookup"><span data-stu-id="97cbe-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="97cbe-105">概览</span><span class="sxs-lookup"><span data-stu-id="97cbe-105">Overview</span></span>

<span data-ttu-id="97cbe-106">在 Dynamics 365 Commerce 中，页面标题包含多个模块，例如标题、导航菜单、搜索、促销横幅和 cookie 同意模块。</span><span class="sxs-lookup"><span data-stu-id="97cbe-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="97cbe-107">标题模块包括站点徽标、指向导航层次结构的链接、指向站点上其他页面的链接、购物车符号、愿望列表符号、登录选项和搜索栏。</span><span class="sxs-lookup"><span data-stu-id="97cbe-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="97cbe-108">针对正在用于查看站点的设备（即针对台式机设备或移动设备）自动优化了标题模块。</span><span class="sxs-lookup"><span data-stu-id="97cbe-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="97cbe-109">例如，在移动设备上，导航栏折叠为**菜单**按钮（有时称为*汉堡包按钮*）。</span><span class="sxs-lookup"><span data-stu-id="97cbe-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="97cbe-110">下图显示了主页上的标题模块的示例。</span><span class="sxs-lookup"><span data-stu-id="97cbe-110">The following image shows an example of a header module on a home page.</span></span>

![标题模块示例](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="97cbe-112">标题模块的属性</span><span class="sxs-lookup"><span data-stu-id="97cbe-112">Properties of a header module</span></span>

<span data-ttu-id="97cbe-113">标题模块支持**徽标图像**、**徽标链接**和**我的帐户连结**属性。</span><span class="sxs-lookup"><span data-stu-id="97cbe-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="97cbe-114">**徽标图像**和**徽标链接**属性用于在页面上定义徽标。</span><span class="sxs-lookup"><span data-stu-id="97cbe-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="97cbe-115">有关详细信息，请参阅[添加徽标](add-logo.md)。</span><span class="sxs-lookup"><span data-stu-id="97cbe-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="97cbe-116">**我的帐户链接**属性可用于在标题中定义站点所有者想要显示快速链接的帐户页面。</span><span class="sxs-lookup"><span data-stu-id="97cbe-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="97cbe-117">页眉模块中的可用模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-117">Modules that are available in a header module</span></span>

<span data-ttu-id="97cbe-118">页眉模块中可使用以下模块：</span><span class="sxs-lookup"><span data-stu-id="97cbe-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="97cbe-119">**导航菜单** – 导航菜单提供渠道导航层次结构和其他静态导航链接。</span><span class="sxs-lookup"><span data-stu-id="97cbe-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="97cbe-120">可以在 Dynamics 365 Commerce 中配置渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="97cbe-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="97cbe-121">导航菜单有一个**导航来源**属性，用于指定零售服务器导航菜单项和静态菜单项作为来源。</span><span class="sxs-lookup"><span data-stu-id="97cbe-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="97cbe-122">如果将静态菜单项指定为来源，则可以提供指向站点上其他页面的相对链接。</span><span class="sxs-lookup"><span data-stu-id="97cbe-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="97cbe-123">配置的项然后显示为页眉导航。</span><span class="sxs-lookup"><span data-stu-id="97cbe-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="97cbe-124">**搜索** – 用户可使用搜索模块输入搜索词以搜索产品。</span><span class="sxs-lookup"><span data-stu-id="97cbe-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="97cbe-125">必须在**站点设置 \> 扩展**中提供默认搜索页面的 URL 和搜索查询参数。</span><span class="sxs-lookup"><span data-stu-id="97cbe-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="97cbe-126">搜索模块的属性可让您根据需要隐藏搜索按钮或标签。</span><span class="sxs-lookup"><span data-stu-id="97cbe-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="97cbe-127">搜索模块还支持自动建议选项，例如产品、关键字和类别搜索结果。</span><span class="sxs-lookup"><span data-stu-id="97cbe-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="97cbe-128">**购物车图标** - 购物车图标模块提供购物车图标，并显示任何给定时间购物车中的商品数量。</span><span class="sxs-lookup"><span data-stu-id="97cbe-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="97cbe-129">有关详细信息，请参阅[购物车图标模块](cart-icon-module.md)。</span><span class="sxs-lookup"><span data-stu-id="97cbe-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="97cbe-130">创建页面的标题模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-130">Create a header module for a page</span></span>

<span data-ttu-id="97cbe-131">若要创建页眉模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="97cbe-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="97cbe-132">转到**页面片段**，选择**新建**创建新片段。</span><span class="sxs-lookup"><span data-stu-id="97cbe-132">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="97cbe-133">在**新建页面片段**对话框中，选择**容器**模块，输入页面片段的名称，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-133">In the **New Page Fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="97cbe-134">选择**默认容器**插槽，然后在右侧的属性窗格中将**宽度**属性设置为**填充容器**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="97cbe-135">在**默认容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="97cbe-136">在**添加模块**对话框中，选择**促销横幅**和 **Cookie 同意**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="97cbe-137">在**默认容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="97cbe-138">在**添加模块**对话框中，选择**容器**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="97cbe-139">选择**容器**插槽，然后在右侧的属性窗格中将**宽度**属性设置为**填充容器**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="97cbe-140">在**容器**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="97cbe-141">在**添加模块**对话框中，选择**标题**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="97cbe-142">在标题模块的**导航菜单**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="97cbe-143">在**添加模块**对话框中，选择**导航菜单**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="97cbe-144">在导航菜单模块的属性窗格中，根据需要配置属性。</span><span class="sxs-lookup"><span data-stu-id="97cbe-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="97cbe-145">在标题模块的**搜索**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="97cbe-146">在**添加模块**对话框中，选择**搜索**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="97cbe-147">在搜索模块的属性窗格中，根据需要配置属性。</span><span class="sxs-lookup"><span data-stu-id="97cbe-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="97cbe-148">在标题模块的**购物车图标**插槽中，选择省略号 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="97cbe-149">在**添加模块**对话框中，选择**购物车图标**模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="97cbe-150">在购物车图标模块的属性窗格中，根据需要配置属性。</span><span class="sxs-lookup"><span data-stu-id="97cbe-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="97cbe-151">如果希望在用户将鼠标悬停在购物车图标上时购物车图标显示购物车摘要（也称为迷你购物车），请选择**显示迷你购物车**。</span><span class="sxs-lookup"><span data-stu-id="97cbe-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="97cbe-152">选择**保存**，选择**完成编辑**签入片段，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="97cbe-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="97cbe-153">若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="97cbe-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="97cbe-154">在**默认页**模块的**标题**插槽中，添加创建的页脚片段。</span><span class="sxs-lookup"><span data-stu-id="97cbe-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="97cbe-155">选择**保存**，选择**完成编辑**签入模板，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="97cbe-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97cbe-156">其他资源</span><span class="sxs-lookup"><span data-stu-id="97cbe-156">Additional resources</span></span>

[<span data-ttu-id="97cbe-157">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="97cbe-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="97cbe-158">容器模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="97cbe-159">购买框模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="97cbe-160">购物车模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="97cbe-161">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="97cbe-162">结账模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="97cbe-163">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="97cbe-164">标题模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="97cbe-165">页脚模块</span><span class="sxs-lookup"><span data-stu-id="97cbe-165">Footer module</span></span>](author-footer-module.md)
