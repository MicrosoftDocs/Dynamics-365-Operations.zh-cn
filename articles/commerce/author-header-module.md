---
title: 页眉模块
description: 此主题介绍页眉模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885470"
---
# <a name="header-module"></a><span data-ttu-id="55717-103">标题模块</span><span class="sxs-lookup"><span data-stu-id="55717-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="55717-104">此主题介绍页眉模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。</span><span class="sxs-lookup"><span data-stu-id="55717-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="55717-105">概览</span><span class="sxs-lookup"><span data-stu-id="55717-105">Overview</span></span>

<span data-ttu-id="55717-106">页眉模块是用于承载页面页眉中将显示的所有模块的特殊容器。</span><span class="sxs-lookup"><span data-stu-id="55717-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="55717-107">例如，可以包括您的站点徽标、导航层次结构的链接、站点中其他页面的链接，以及搜索栏。</span><span class="sxs-lookup"><span data-stu-id="55717-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="55717-108">针对正在用于查看站点的设备（即台式机设备或移动设备）自动优化了页眉模块。</span><span class="sxs-lookup"><span data-stu-id="55717-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="55717-109">例如，在移动设备上，导航栏折叠为**菜单**按钮（有时称为*汉堡包按钮*）。</span><span class="sxs-lookup"><span data-stu-id="55717-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="55717-110">页眉的属性</span><span class="sxs-lookup"><span data-stu-id="55717-110">Properties of a header</span></span>

<span data-ttu-id="55717-111">与一般容器一样，页眉模块支持**标题**和**宽度**属性。</span><span class="sxs-lookup"><span data-stu-id="55717-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="55717-112">页眉模块有多个插槽。</span><span class="sxs-lookup"><span data-stu-id="55717-112">A header module has multiple slots.</span></span> <span data-ttu-id="55717-113">例如，有参考消息、导航菜单、徽标、搜索栏、购物车图标、愿望列表图标和帐户信息的插槽。</span><span class="sxs-lookup"><span data-stu-id="55717-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="55717-114">每个插槽支持一组特定模块。</span><span class="sxs-lookup"><span data-stu-id="55717-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="55717-115">页眉模块中的可用模块</span><span class="sxs-lookup"><span data-stu-id="55717-115">Modules that are available in a header module</span></span>

<span data-ttu-id="55717-116">页眉模块中可使用以下模块：</span><span class="sxs-lookup"><span data-stu-id="55717-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="55717-117">**导航菜单** – 导航菜单提供渠道导航层次结构和其他静态导航链接。</span><span class="sxs-lookup"><span data-stu-id="55717-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="55717-118">可以在 Dynamics 365 Retail 中配置渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="55717-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="55717-119">配置的项然后显示为页眉导航。</span><span class="sxs-lookup"><span data-stu-id="55717-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="55717-120">此外，可配置静态导航链接，也可以提供电子商务站点中的其他页面的相对链接。</span><span class="sxs-lookup"><span data-stu-id="55717-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="55717-121">可以靠左、靠右或居中对齐页眉本身。</span><span class="sxs-lookup"><span data-stu-id="55717-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="55717-122">**购物车图标** – 购物车图标是表示购物车的特殊图标。</span><span class="sxs-lookup"><span data-stu-id="55717-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="55717-123">其在页眉中显示，指示购物车中的项数。</span><span class="sxs-lookup"><span data-stu-id="55717-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="55717-124">购物车页面的链接应该伴有购物车图标，所以当客户与该图标交互时，可以将客户重定向到购物车页。</span><span class="sxs-lookup"><span data-stu-id="55717-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="55717-125">**愿望列表图标** – 愿望列表图标在页眉中显示，用于指示已向客户的愿望列表添加的项数。</span><span class="sxs-lookup"><span data-stu-id="55717-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="55717-126">愿望列表页面的链接应该伴有此图标，所以当客户与该图标交互时，可以将客户重定向到愿望列表页。</span><span class="sxs-lookup"><span data-stu-id="55717-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="55717-127">**登录模块** – 登录模块在页眉中显示。</span><span class="sxs-lookup"><span data-stu-id="55717-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="55717-128">用于供客户登录其帐户或注册帐户。</span><span class="sxs-lookup"><span data-stu-id="55717-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="55717-129">如果客户已登录，可将模块配置为显示帐户页、订单历史记录页或其他页的链接。</span><span class="sxs-lookup"><span data-stu-id="55717-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="55717-130">**徽标模块** – 此模块显示用于表示零售商和品牌的徽标。</span><span class="sxs-lookup"><span data-stu-id="55717-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="55717-131">这是具有链接的图像。</span><span class="sxs-lookup"><span data-stu-id="55717-131">It's an image that has a link.</span></span> <span data-ttu-id="55717-132">通常将此链接配置为具有到主页的重定向。因此，客户可从站点的任何页面快速回到主页。</span><span class="sxs-lookup"><span data-stu-id="55717-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="55717-133">**预警** – 预警在页眉中显示，用于显示为站点中的所有页面应用的内联消息。</span><span class="sxs-lookup"><span data-stu-id="55717-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="55717-134">例如，一个预警可能显示消息“年度促销将于 2 天后结束”。</span><span class="sxs-lookup"><span data-stu-id="55717-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="55717-135">**搜索栏** – 用户可使用搜索栏输入搜索词，以便搜索产品。</span><span class="sxs-lookup"><span data-stu-id="55717-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="55717-136">必须为模块配置搜索结果页的 URL。</span><span class="sxs-lookup"><span data-stu-id="55717-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="55717-137">可配置查询字符串参数（默认值为 **"q"**）。</span><span class="sxs-lookup"><span data-stu-id="55717-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="55717-138">搜索栏有一个自动建议插槽，应该在其中添加自动建议模块。</span><span class="sxs-lookup"><span data-stu-id="55717-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="55717-139">**自动建议** – 自动建议模块显示自动建议的结果。</span><span class="sxs-lookup"><span data-stu-id="55717-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="55717-140">这些结果可以是可以在其中找到搜索词的关键字、产品或类别。</span><span class="sxs-lookup"><span data-stu-id="55717-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="55717-141">创建标题模块</span><span class="sxs-lookup"><span data-stu-id="55717-141">Create a header module</span></span>

<span data-ttu-id="55717-142">若要创建页眉模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="55717-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="55717-143">创建其中包含页眉模块的页面片段。</span><span class="sxs-lookup"><span data-stu-id="55717-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="55717-144">向页眉模块中的插槽添加模块。</span><span class="sxs-lookup"><span data-stu-id="55717-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="55717-145">更新每个模块的设置。</span><span class="sxs-lookup"><span data-stu-id="55717-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="55717-146">保存页面片段。</span><span class="sxs-lookup"><span data-stu-id="55717-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="55717-147">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="55717-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="55717-148">若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="55717-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="55717-149">在默认页面中，向主插槽中的页眉添加其中包含页眉模块的页面片段。</span><span class="sxs-lookup"><span data-stu-id="55717-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="55717-150">保存模板。</span><span class="sxs-lookup"><span data-stu-id="55717-150">Save the template.</span></span> 
1. <span data-ttu-id="55717-151">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="55717-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55717-152">其他资源</span><span class="sxs-lookup"><span data-stu-id="55717-152">Additional resources</span></span>

[<span data-ttu-id="55717-153">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="55717-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="55717-154">容器模块</span><span class="sxs-lookup"><span data-stu-id="55717-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="55717-155">购买框模块</span><span class="sxs-lookup"><span data-stu-id="55717-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="55717-156">购物车模块</span><span class="sxs-lookup"><span data-stu-id="55717-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="55717-157">结帐模块</span><span class="sxs-lookup"><span data-stu-id="55717-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="55717-158">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="55717-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="55717-159">页眉模块</span><span class="sxs-lookup"><span data-stu-id="55717-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="55717-160">页脚模块</span><span class="sxs-lookup"><span data-stu-id="55717-160">Footer module</span></span>](author-footer-module.md)
