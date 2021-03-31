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
ms.openlocfilehash: 16c9ca145aff97f0af242da4cf662367f1f4ca3d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211440"
---
# <a name="footer-module"></a><span data-ttu-id="7e697-103">页脚模块</span><span class="sxs-lookup"><span data-stu-id="7e697-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="7e697-104">此主题介绍页脚模块和如何在 Microsoft Dynamics 365 Commerce 中创建该模块。</span><span class="sxs-lookup"><span data-stu-id="7e697-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7e697-105">页脚模块是用于承载页脚中显示的模块的特殊容器。</span><span class="sxs-lookup"><span data-stu-id="7e697-105">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="7e697-106">例如，其中可包含站点中各页面（如 **联系我们** 和 **商店政策** 页面）的链接。</span><span class="sxs-lookup"><span data-stu-id="7e697-106">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="7e697-107">下图显示了站点页上的页脚模块的示例。</span><span class="sxs-lookup"><span data-stu-id="7e697-107">The following image shows an example of a footer module on a site page.</span></span>

![页脚模块示例](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="7e697-109">页脚模块属性</span><span class="sxs-lookup"><span data-stu-id="7e697-109">Footer module properties</span></span> 

<span data-ttu-id="7e697-110">与大多数容器一样，页脚模块支持标题和宽度属性。</span><span class="sxs-lookup"><span data-stu-id="7e697-110">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="7e697-111">还支持添加多个页脚类别模块。</span><span class="sxs-lookup"><span data-stu-id="7e697-111">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="7e697-112">添加的每个页脚类别模块在页脚模块中显示为一列。</span><span class="sxs-lookup"><span data-stu-id="7e697-112">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="7e697-113">页脚模块中的可用模块</span><span class="sxs-lookup"><span data-stu-id="7e697-113">Modules available in a footer module</span></span>

<span data-ttu-id="7e697-114">**页脚项** – 页脚项模块中可包含标题、图像和链接。</span><span class="sxs-lookup"><span data-stu-id="7e697-114">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="7e697-115">标题可以单独使用，也可以与图像和链接组合使用。</span><span class="sxs-lookup"><span data-stu-id="7e697-115">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="7e697-116">可配置页脚中的每个链接，使其仅包含文本（如“联系我们”和“隐私”链接），或使其同时包含文本和图像（例如，社交媒体链接）。</span><span class="sxs-lookup"><span data-stu-id="7e697-116">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="7e697-117">**返回顶部** – 返回顶部模块提供用于快速导航到页面顶部的链接。</span><span class="sxs-lookup"><span data-stu-id="7e697-117">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="7e697-118">需要目标。</span><span class="sxs-lookup"><span data-stu-id="7e697-118">A destination is required.</span></span> <span data-ttu-id="7e697-119">默认目标值为 \#，用于将用户带到页面顶部。</span><span class="sxs-lookup"><span data-stu-id="7e697-119">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="7e697-120">创建页脚模块</span><span class="sxs-lookup"><span data-stu-id="7e697-120">Create a footer module</span></span>

1. <span data-ttu-id="7e697-121">转到 **片段**，选择 **新建** 创建新片段。</span><span class="sxs-lookup"><span data-stu-id="7e697-121">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="7e697-122">在 **新建片段** 对话框中，选择 **容器** 模块，输入片段的名称，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7e697-122">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7e697-123">在 **默认容器** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="7e697-123">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7e697-124">在 **添加模块** 对话框中，选择 **页脚类别** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7e697-124">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7e697-125">在 **页脚类别** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="7e697-125">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7e697-126">在 **添加模块** 对话框中，选择 **页脚项** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7e697-126">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7e697-127">选择 **页脚项** 插槽，然后，在右侧属性窗格中，根据需要配置标题、链接和链接文本，以及图像。</span><span class="sxs-lookup"><span data-stu-id="7e697-127">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="7e697-128">若要添加更多页脚项，请为每个页脚项重复执行步骤 5 到 7。</span><span class="sxs-lookup"><span data-stu-id="7e697-128">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="7e697-129">若要向页脚添加“返回顶部”链接，请选择 **页脚类别** 插槽中的省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="7e697-129">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="7e697-130">在 **添加模块** 对话框中，选择 **返回顶部** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7e697-130">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7e697-131">选择 **返回顶部** 插槽，然后，在右侧属性窗格中，根据需要配置文本及其他模块属性。</span><span class="sxs-lookup"><span data-stu-id="7e697-131">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="7e697-132">选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="7e697-132">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="7e697-133">若要帮助确保每个页面中显示页眉，请在为站点创建的每个页面模板中执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="7e697-133">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="7e697-134">在 **默认页** 模块的 **页脚** 插槽中，添加创建的页脚片段。</span><span class="sxs-lookup"><span data-stu-id="7e697-134">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="7e697-135">选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="7e697-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="7e697-136">通过向页面模板添加片段，可帮助确保在每个页面中显示页脚。</span><span class="sxs-lookup"><span data-stu-id="7e697-136">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e697-137">其他资源</span><span class="sxs-lookup"><span data-stu-id="7e697-137">Additional resources</span></span>

[<span data-ttu-id="7e697-138">模块库概述</span><span class="sxs-lookup"><span data-stu-id="7e697-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7e697-139">容器模块</span><span class="sxs-lookup"><span data-stu-id="7e697-139">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7e697-140">购买框模块</span><span class="sxs-lookup"><span data-stu-id="7e697-140">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7e697-141">购物车模块</span><span class="sxs-lookup"><span data-stu-id="7e697-141">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7e697-142">结帐模块</span><span class="sxs-lookup"><span data-stu-id="7e697-142">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7e697-143">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="7e697-143">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7e697-144">页眉模块</span><span class="sxs-lookup"><span data-stu-id="7e697-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7e697-145">页脚模块</span><span class="sxs-lookup"><span data-stu-id="7e697-145">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]