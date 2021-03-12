---
title: 页脚模块
description: 此主题介绍页脚模块和如何在 Dynamics 365 Commerce 中制作页脚模块。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 038fee32cbf1ed6b4967f440faaf3c0d4fa583f6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979939"
---
# <a name="footer-module"></a><span data-ttu-id="00a66-103">页脚模块</span><span class="sxs-lookup"><span data-stu-id="00a66-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="00a66-104">此主题介绍页脚模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。</span><span class="sxs-lookup"><span data-stu-id="00a66-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="00a66-105">概览</span><span class="sxs-lookup"><span data-stu-id="00a66-105">Overview</span></span>

<span data-ttu-id="00a66-106">页脚模块是用于承载页脚中显示的模块的特殊容器。</span><span class="sxs-lookup"><span data-stu-id="00a66-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="00a66-107">例如，其中可包含站点中各页面（如 **联系我们** 和 **商店政策** 页面）的链接。</span><span class="sxs-lookup"><span data-stu-id="00a66-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="00a66-108">下图显示了站点页上的页脚模块的示例。</span><span class="sxs-lookup"><span data-stu-id="00a66-108">The following image shows an example of a footer module on a site page.</span></span>

![页脚模块示例](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="00a66-110">页脚模块属性</span><span class="sxs-lookup"><span data-stu-id="00a66-110">Footer module properties</span></span> 

<span data-ttu-id="00a66-111">与大多数容器一样，页脚模块支持标题和宽度属性。</span><span class="sxs-lookup"><span data-stu-id="00a66-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="00a66-112">还支持添加多个页脚类别模块。</span><span class="sxs-lookup"><span data-stu-id="00a66-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="00a66-113">添加的每个页脚类别模块在页脚模块中显示为一列。</span><span class="sxs-lookup"><span data-stu-id="00a66-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="00a66-114">页脚模块中的可用模块</span><span class="sxs-lookup"><span data-stu-id="00a66-114">Modules available in a footer module</span></span>

<span data-ttu-id="00a66-115">**页脚项** – 页脚项模块中可包含标题、图像和链接。</span><span class="sxs-lookup"><span data-stu-id="00a66-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="00a66-116">标题可以单独使用，也可以与图像和链接组合使用。</span><span class="sxs-lookup"><span data-stu-id="00a66-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="00a66-117">可配置页脚中的每个链接，使其仅包含文本（如“联系我们”和“隐私”链接），或使其同时包含文本和图像（例如，社交媒体链接）。</span><span class="sxs-lookup"><span data-stu-id="00a66-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="00a66-118">**返回顶部** – 返回顶部模块提供用于快速导航到页面顶部的链接。</span><span class="sxs-lookup"><span data-stu-id="00a66-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="00a66-119">需要目标。</span><span class="sxs-lookup"><span data-stu-id="00a66-119">A destination is required.</span></span> <span data-ttu-id="00a66-120">默认目标值为 \#，用于将用户带到页面顶部。</span><span class="sxs-lookup"><span data-stu-id="00a66-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="00a66-121">创建页脚模块</span><span class="sxs-lookup"><span data-stu-id="00a66-121">Create a footer module</span></span>

1. <span data-ttu-id="00a66-122">转到 **片段**，选择 **新建** 创建新片段。</span><span class="sxs-lookup"><span data-stu-id="00a66-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="00a66-123">在 **新建片段** 对话框中，选择 **容器** 模块，输入片段的名称，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="00a66-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="00a66-124">在 **默认容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="00a66-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="00a66-125">在 **添加模块** 对话框中，选择 **页脚类别** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="00a66-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="00a66-126">在 **页脚类别** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="00a66-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="00a66-127">在 **添加模块** 对话框中，选择 **页脚项** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="00a66-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="00a66-128">选择 **页脚项** 插槽，然后，在右侧属性窗格中，根据需要配置标题、链接和链接文本，以及图像。</span><span class="sxs-lookup"><span data-stu-id="00a66-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="00a66-129">若要添加更多页脚项，请为每个页脚项重复执行步骤 5 到 7。</span><span class="sxs-lookup"><span data-stu-id="00a66-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="00a66-130">若要向页脚添加“返回顶部”链接，请选择 **页脚类别** 插槽中的省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="00a66-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="00a66-131">在 **添加模块** 对话框中，选择 **返回顶部** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="00a66-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="00a66-132">选择 **返回顶部** 插槽，然后，在右侧属性窗格中，根据需要配置文本及其他模块属性。</span><span class="sxs-lookup"><span data-stu-id="00a66-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="00a66-133">选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="00a66-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="00a66-134">若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="00a66-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="00a66-135">在 **默认页** 模块的 **页脚** 插槽中，添加创建的页脚片段。</span><span class="sxs-lookup"><span data-stu-id="00a66-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="00a66-136">选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="00a66-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="00a66-137">通过向页面模板添加片段，可帮助确保在每个页面中显示页脚。</span><span class="sxs-lookup"><span data-stu-id="00a66-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="00a66-138">其他资源</span><span class="sxs-lookup"><span data-stu-id="00a66-138">Additional resources</span></span>

[<span data-ttu-id="00a66-139">模块库概述</span><span class="sxs-lookup"><span data-stu-id="00a66-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="00a66-140">容器模块</span><span class="sxs-lookup"><span data-stu-id="00a66-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="00a66-141">购买框模块</span><span class="sxs-lookup"><span data-stu-id="00a66-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="00a66-142">购物车模块</span><span class="sxs-lookup"><span data-stu-id="00a66-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="00a66-143">结帐模块</span><span class="sxs-lookup"><span data-stu-id="00a66-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="00a66-144">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="00a66-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="00a66-145">页眉模块</span><span class="sxs-lookup"><span data-stu-id="00a66-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="00a66-146">页脚模块</span><span class="sxs-lookup"><span data-stu-id="00a66-146">Footer module</span></span>](author-footer-module.md)
