---
title: 页脚模块
description: 此主题介绍页脚模块和如何在 Dynamics 365 Commerce 中制作页脚模块。
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f8e0290b5af9d0c1fc9ad0279b0d7f81c9feb2fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001122"
---
# <a name="footer-module"></a><span data-ttu-id="7c561-103">页脚模块</span><span class="sxs-lookup"><span data-stu-id="7c561-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="7c561-104">此主题介绍页脚模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。</span><span class="sxs-lookup"><span data-stu-id="7c561-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7c561-105">概览</span><span class="sxs-lookup"><span data-stu-id="7c561-105">Overview</span></span>

<span data-ttu-id="7c561-106">页脚模块是用于承载页脚中显示的模块的特殊容器。</span><span class="sxs-lookup"><span data-stu-id="7c561-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="7c561-107">例如，其中可包含站点中各页面（如**联系我们**和**商店政策**页面）的链接。</span><span class="sxs-lookup"><span data-stu-id="7c561-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="7c561-108">页脚模块属性</span><span class="sxs-lookup"><span data-stu-id="7c561-108">Footer module properties</span></span> 

<span data-ttu-id="7c561-109">与大多数容器一样，页脚模块支持标题和宽度属性。</span><span class="sxs-lookup"><span data-stu-id="7c561-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="7c561-110">还支持添加多个页脚类别模块。</span><span class="sxs-lookup"><span data-stu-id="7c561-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="7c561-111">添加的每个页脚类别模块在页脚模块中显示为一列。</span><span class="sxs-lookup"><span data-stu-id="7c561-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="7c561-112">页脚模块中的可用模块</span><span class="sxs-lookup"><span data-stu-id="7c561-112">Modules available in a footer module</span></span>

<span data-ttu-id="7c561-113">**页脚项** – 页脚项模块中可包含标题、图像和链接。</span><span class="sxs-lookup"><span data-stu-id="7c561-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="7c561-114">标题可以单独使用，也可以与图像和链接组合使用。</span><span class="sxs-lookup"><span data-stu-id="7c561-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="7c561-115">可配置页脚中的每个链接，使其仅包含文本（如“联系我们”和“隐私”链接），或使其同时包含文本和图像（例如，社交媒体链接）。</span><span class="sxs-lookup"><span data-stu-id="7c561-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="7c561-116">**返回顶部** – 返回顶部模块提供用于快速导航到页面顶部的链接。</span><span class="sxs-lookup"><span data-stu-id="7c561-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="7c561-117">需要目标。</span><span class="sxs-lookup"><span data-stu-id="7c561-117">A destination is required.</span></span> <span data-ttu-id="7c561-118">默认目标值为 #，用于将用户带到页面顶部。</span><span class="sxs-lookup"><span data-stu-id="7c561-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="7c561-119">制作页脚模块</span><span class="sxs-lookup"><span data-stu-id="7c561-119">Author a footer module</span></span>

1. <span data-ttu-id="7c561-120">在导航窗格中，选择**片段**，然后选择**新建页面片段**。</span><span class="sxs-lookup"><span data-stu-id="7c561-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="7c561-121">在**新页面片段**对话框中，选择页脚模块，输入页面片段的名称，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c561-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7c561-122">在左侧大纲树中，选择页脚模块的省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="7c561-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="7c561-123">在**添加模块**对话框中，选择页脚类别模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c561-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="7c561-124">在大纲树中，选择页脚类别模块的省略号按钮，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="7c561-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="7c561-125">在**添加模块**对话框中，选择页脚项模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c561-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="7c561-126">在大纲树中，选择页脚项模块。</span><span class="sxs-lookup"><span data-stu-id="7c561-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="7c561-127">然后，在右侧属性窗格中，根据需要配置标题、链接和链接文本，以及图像。</span><span class="sxs-lookup"><span data-stu-id="7c561-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="7c561-128">若要添加更多页脚项，请重复执行第 5 步到第 7 步。</span><span class="sxs-lookup"><span data-stu-id="7c561-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="7c561-129">若要向页脚添加“返回顶部”链接，请选择页脚类别模块的省略号按钮，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="7c561-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="7c561-130">在**添加模块**对话框中，选择返回顶部模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="7c561-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="7c561-131">在大纲树中，选择返回顶部模块。</span><span class="sxs-lookup"><span data-stu-id="7c561-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="7c561-132">然后，在右侧的属性窗格中，根据需要配置返回顶部模块。</span><span class="sxs-lookup"><span data-stu-id="7c561-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="7c561-133">保存页面片段，签入，然后发布。</span><span class="sxs-lookup"><span data-stu-id="7c561-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="7c561-134">在已经为站点创建的每个页面模板中，执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="7c561-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="7c561-135">在默认页的**主**插槽中页脚模块内，添加创建的页脚片段。</span><span class="sxs-lookup"><span data-stu-id="7c561-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="7c561-136">保存模板，签入，然后发布。</span><span class="sxs-lookup"><span data-stu-id="7c561-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="7c561-137">通过向页面模板添加页面片段，可帮助确保在每个页面中显示页脚。</span><span class="sxs-lookup"><span data-stu-id="7c561-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c561-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="7c561-138">Additional resources</span></span>

[<span data-ttu-id="7c561-139">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="7c561-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7c561-140">容器模块</span><span class="sxs-lookup"><span data-stu-id="7c561-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7c561-141">购买框模块</span><span class="sxs-lookup"><span data-stu-id="7c561-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7c561-142">购物车模块</span><span class="sxs-lookup"><span data-stu-id="7c561-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7c561-143">结帐模块</span><span class="sxs-lookup"><span data-stu-id="7c561-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7c561-144">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="7c561-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7c561-145">页眉模块</span><span class="sxs-lookup"><span data-stu-id="7c561-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7c561-146">页脚模块</span><span class="sxs-lookup"><span data-stu-id="7c561-146">Footer module</span></span>](author-footer-module.md)
