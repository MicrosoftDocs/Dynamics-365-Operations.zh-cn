---
title: 页眉模块
description: 此主题介绍标题模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面标题。
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261436"
---
# <a name="header-module"></a><span data-ttu-id="c179c-103">标题模块</span><span class="sxs-lookup"><span data-stu-id="c179c-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c179c-104">此主题介绍标题模块和如何在 Microsoft Dynamics 365 Commerce 中创建页面标题。</span><span class="sxs-lookup"><span data-stu-id="c179c-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c179c-105">概览</span><span class="sxs-lookup"><span data-stu-id="c179c-105">Overview</span></span>

<span data-ttu-id="c179c-106">在 Dynamics 365 Commerce 中，页面标题包含多个模块，例如标题、导航菜单、搜索、促销横幅和 cookie 同意模块。</span><span class="sxs-lookup"><span data-stu-id="c179c-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="c179c-107">标题模块包括站点徽标、指向导航层次结构的链接、指向站点上其他页面的链接、购物车符号、愿望列表符号、登录选项和搜索栏。</span><span class="sxs-lookup"><span data-stu-id="c179c-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="c179c-108">针对正在用于查看站点的设备（即针对台式机设备或移动设备）自动优化了标题模块。</span><span class="sxs-lookup"><span data-stu-id="c179c-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="c179c-109">例如，在移动设备上，导航栏折叠为**菜单**按钮（有时称为*汉堡包按钮*）。</span><span class="sxs-lookup"><span data-stu-id="c179c-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="c179c-110">标题模块的属性</span><span class="sxs-lookup"><span data-stu-id="c179c-110">Properties of a header module</span></span>

<span data-ttu-id="c179c-111">标题模块支持**徽标图像**、**徽标链接**和**我的帐户连结**属性。</span><span class="sxs-lookup"><span data-stu-id="c179c-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="c179c-112">**徽标图像**和**徽标链接**属性用于在页面上定义徽标。</span><span class="sxs-lookup"><span data-stu-id="c179c-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="c179c-113">有关详细信息，请参阅[添加徽标](add-logo.md)。</span><span class="sxs-lookup"><span data-stu-id="c179c-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="c179c-114">**我的帐户链接**属性可用于在标题中定义站点所有者想要显示快速链接的帐户页面。</span><span class="sxs-lookup"><span data-stu-id="c179c-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="c179c-115">页眉模块中的可用模块</span><span class="sxs-lookup"><span data-stu-id="c179c-115">Modules that are available in a header module</span></span>

<span data-ttu-id="c179c-116">页眉模块中可使用以下模块：</span><span class="sxs-lookup"><span data-stu-id="c179c-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="c179c-117">**导航菜单** – 导航菜单提供渠道导航层次结构和其他静态导航链接。</span><span class="sxs-lookup"><span data-stu-id="c179c-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="c179c-118">可以在 Dynamics 365 Commerce 中配置渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="c179c-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c179c-119">导航菜单有一个**导航来源**属性，用于指定零售服务器导航菜单项和静态菜单项作为来源。</span><span class="sxs-lookup"><span data-stu-id="c179c-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="c179c-120">如果将静态菜单项指定为来源，则可以提供指向站点上其他页面的相对链接。</span><span class="sxs-lookup"><span data-stu-id="c179c-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="c179c-121">配置的项然后显示为页眉导航。</span><span class="sxs-lookup"><span data-stu-id="c179c-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="c179c-122">**搜索** – 用户可使用搜索模块输入搜索词以搜索产品。</span><span class="sxs-lookup"><span data-stu-id="c179c-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="c179c-123">必须在**站点设置 \> 扩展**中提供默认搜索页面的 URL 和搜索查询参数。</span><span class="sxs-lookup"><span data-stu-id="c179c-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="c179c-124">搜索模块的属性可让您根据需要隐藏搜索按钮或标签。</span><span class="sxs-lookup"><span data-stu-id="c179c-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="c179c-125">搜索模块还支持自动建议选项，例如产品、关键字和类别搜索结果。</span><span class="sxs-lookup"><span data-stu-id="c179c-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="c179c-126">**购物车图标** - 购物车图标模块提供购物车图标，并显示任何给定时间购物车中的商品数量。</span><span class="sxs-lookup"><span data-stu-id="c179c-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="c179c-127">有关详细信息，请参阅[购物车图标模块](cart-icon-module.md)。</span><span class="sxs-lookup"><span data-stu-id="c179c-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="c179c-128">创建页面的标题模块</span><span class="sxs-lookup"><span data-stu-id="c179c-128">Create a header module for a page</span></span>

<span data-ttu-id="c179c-129">若要创建页眉模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c179c-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="c179c-130">创建一个名称为**标题片段**的片段，然后向其添加一个容器模块。</span><span class="sxs-lookup"><span data-stu-id="c179c-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="c179c-131">在容器模块的属性窗格中，将**宽度**属性设置为**填充容器**。</span><span class="sxs-lookup"><span data-stu-id="c179c-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="c179c-132">将促销横幅和 Cookie 同意模块添加到容器模块。</span><span class="sxs-lookup"><span data-stu-id="c179c-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="c179c-133">向片段添加另一个容器模块，将**宽度**属性设置为**填充容器**。</span><span class="sxs-lookup"><span data-stu-id="c179c-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="c179c-134">向第二个容器模块添加一个标题模块。</span><span class="sxs-lookup"><span data-stu-id="c179c-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="c179c-135">在标题模块的**导航菜单**插槽中，添加导航菜单模块。</span><span class="sxs-lookup"><span data-stu-id="c179c-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="c179c-136">在导航菜单模块的属性窗格中，配置导航菜单模块的属性。</span><span class="sxs-lookup"><span data-stu-id="c179c-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="c179c-137">在标题模块的**搜索**插槽中，添加搜索模块。</span><span class="sxs-lookup"><span data-stu-id="c179c-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="c179c-138">在搜索模块的属性窗格中，配置搜索模块的属性。</span><span class="sxs-lookup"><span data-stu-id="c179c-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="c179c-139">在页眉模块的**购物车图标**插槽中，添加购物车图标模块。</span><span class="sxs-lookup"><span data-stu-id="c179c-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="c179c-140">在购物车图标模块的属性窗格中，配置购物车图标模块的属性。</span><span class="sxs-lookup"><span data-stu-id="c179c-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="c179c-141">如果要在将鼠标光标悬停在购物车图标上方时显示迷你购物车，请为**显示迷你购物车**选择 **True**。</span><span class="sxs-lookup"><span data-stu-id="c179c-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="c179c-142">保存页面片段，完成编辑，然后发布。</span><span class="sxs-lookup"><span data-stu-id="c179c-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="c179c-143">若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="c179c-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="c179c-144">在默认页面的**主**插槽中，向标题添加其中包含标题模块的标题页面片段。</span><span class="sxs-lookup"><span data-stu-id="c179c-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="c179c-145">保存模板，完成编辑，然后发布。</span><span class="sxs-lookup"><span data-stu-id="c179c-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c179c-146">其他资源</span><span class="sxs-lookup"><span data-stu-id="c179c-146">Additional resources</span></span>

[<span data-ttu-id="c179c-147">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="c179c-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c179c-148">容器模块</span><span class="sxs-lookup"><span data-stu-id="c179c-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c179c-149">购买框模块</span><span class="sxs-lookup"><span data-stu-id="c179c-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c179c-150">购物车模块</span><span class="sxs-lookup"><span data-stu-id="c179c-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c179c-151">购物车图标模块</span><span class="sxs-lookup"><span data-stu-id="c179c-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c179c-152">结账模块</span><span class="sxs-lookup"><span data-stu-id="c179c-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c179c-153">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="c179c-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c179c-154">标题模块</span><span class="sxs-lookup"><span data-stu-id="c179c-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c179c-155">页脚模块</span><span class="sxs-lookup"><span data-stu-id="c179c-155">Footer module</span></span>](author-footer-module.md)
