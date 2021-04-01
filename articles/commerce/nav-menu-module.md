---
title: 导航菜单模块
description: 此主题介绍导航菜单模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3461993e2bd59d66be1640331e4ef315a078469
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251203"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="6c9f8-103">导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="6c9f8-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6c9f8-104">此主题介绍导航菜单模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6c9f8-105">导航菜单模块的主要用途是让站点用户可以根据 Dynamics 365 Commerce 总部中定义的渠道导航层次结构浏览产品和站点页面。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-105">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="6c9f8-106">导航菜单模块中配置的项显示为站点标题导航。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-106">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="6c9f8-107">导航菜单模块还支持链接到电子商务网站上其他页面的静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-107">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="6c9f8-108">导航菜单模块可以添加到页面的标题模块。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-108">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="6c9f8-109">默认情况下，Fabrikam 主题中的导航菜单显示两个级别。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-109">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="6c9f8-110">默认情况下，Starter 主题中的导航菜单显示三个级别。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-110">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="6c9f8-111">若要切换为级别数量，主题中需要视图扩展。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-111">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="6c9f8-112">下图显示 Fabrikam 站点的导航菜单示例，以及两个类别层次结构级别和一些静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-112">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="6c9f8-113">![导航菜单模块的示例](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="6c9f8-113">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="6c9f8-114">导航菜单模块属性</span><span class="sxs-lookup"><span data-stu-id="6c9f8-114">Navigation menu module properties</span></span>

| <span data-ttu-id="6c9f8-115">属性名称</span><span class="sxs-lookup"><span data-stu-id="6c9f8-115">Property name</span></span>             | <span data-ttu-id="6c9f8-116">值</span><span class="sxs-lookup"><span data-stu-id="6c9f8-116">Value</span></span>                 | <span data-ttu-id="6c9f8-117">说明</span><span class="sxs-lookup"><span data-stu-id="6c9f8-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="6c9f8-118">源</span><span class="sxs-lookup"><span data-stu-id="6c9f8-118">Source</span></span>                  | <span data-ttu-id="6c9f8-119">**零售**、**手动创作**、**零售和手动创作**</span><span class="sxs-lookup"><span data-stu-id="6c9f8-119">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="6c9f8-120">**零售** 值允许在导航菜单中显示 Commerce 总部的渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-120">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="6c9f8-121">**手动创作** 值允许策划静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-121">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="6c9f8-122">**零售和手动创作** 值允许混合使用两者。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-122">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="6c9f8-123">显示类别图像</span><span class="sxs-lookup"><span data-stu-id="6c9f8-123">Show category images</span></span> | <span data-ttu-id="6c9f8-124">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="6c9f8-124">**True** or **False**</span></span>    | <span data-ttu-id="6c9f8-125">启用后，此属性将在 Commerce 总部中为每个类别定义的导航菜单上显示类别图像。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-125">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="6c9f8-126">Commerce 版本 10.0.14 中已添加。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-126">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="6c9f8-127">显示促销</span><span class="sxs-lookup"><span data-stu-id="6c9f8-127">Show promotions</span></span> | <span data-ttu-id="6c9f8-128">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="6c9f8-128">**True** or **False**</span></span> | <span data-ttu-id="6c9f8-129">启用此属性后，可以使用图像、链接和文本配置促销。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-129">When this property is enabled, promotions can be configured by using images, links, and text.</span></span> <span data-ttu-id="6c9f8-130">此属性在 Commerce 版本 10.0.17 中添加。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-130">This property was added in the Commerce version 10.0.17 release.</span></span> |
| <span data-ttu-id="6c9f8-131">添加促销</span><span class="sxs-lookup"><span data-stu-id="6c9f8-131">Add promotions</span></span> | <span data-ttu-id="6c9f8-132">文本、图像或链接</span><span class="sxs-lookup"><span data-stu-id="6c9f8-132">Text, image, or link</span></span> | <span data-ttu-id="6c9f8-133">**显示促销** 属性启用后，您可以在导航菜单上添加文本、图像或链接作为促销内容。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-133">When the **Show promotions** property is enabled, you can add text, an image, or a link as promotional content on the navigation menu.</span></span> |
| <span data-ttu-id="6c9f8-134">启用多级导航菜单</span><span class="sxs-lookup"><span data-stu-id="6c9f8-134">Enable multi-level navigation menu</span></span> | <span data-ttu-id="6c9f8-135">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="6c9f8-135">**True** or **False**</span></span> | <span data-ttu-id="6c9f8-136">启用此属性后，导航菜单可以显示多级导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-136">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="6c9f8-137">Commerce 版本 10.0.15 中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-137">This feature is available in the Commerce version 10.0.15 release.</span></span> |
| <span data-ttu-id="6c9f8-138">级别数</span><span class="sxs-lookup"><span data-stu-id="6c9f8-138">Number of levels</span></span> | <span data-ttu-id="6c9f8-139">整数</span><span class="sxs-lookup"><span data-stu-id="6c9f8-139">integer</span></span> | <span data-ttu-id="6c9f8-140">如果 **启用多级导航菜单** 属性设置为 **True**，此属性将定义应该显示的级别数。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-140">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="6c9f8-141">静态菜单项</span><span class="sxs-lookup"><span data-stu-id="6c9f8-141">Static menu item</span></span>| <span data-ttu-id="6c9f8-142">值数组</span><span class="sxs-lookup"><span data-stu-id="6c9f8-142">Array of values</span></span>| <span data-ttu-id="6c9f8-143">将菜单项名称与静态站点页的链接关联的静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-143">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="6c9f8-144">可以在其他菜单项下创建菜单项。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-144">You can create menu items below other menu items.</span></span> <span data-ttu-id="6c9f8-145">默认情况下，静态菜单在根级别显示，并将追加到渠道导航层次结构（如果有）。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-145">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="6c9f8-146">显示根菜单</span><span class="sxs-lookup"><span data-stu-id="6c9f8-146">Show root menu</span></span> | <span data-ttu-id="6c9f8-147">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="6c9f8-147">**True** or **False**</span></span> | <span data-ttu-id="6c9f8-148">启用此属性后，可以在自定义根下定义导航菜单（例如，**立即购物**）。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-148">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="6c9f8-149">Dynamics 365 Commerce 10.0.15 版本中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-149">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="6c9f8-150">根菜单</span><span class="sxs-lookup"><span data-stu-id="6c9f8-150">Root menu</span></span> | <span data-ttu-id="6c9f8-151">字符串</span><span class="sxs-lookup"><span data-stu-id="6c9f8-151">string</span></span> | <span data-ttu-id="6c9f8-152">如果 **显示根菜单** 属性设置为 **True**，此属性可用于为自定义根定义文本。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-152">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="6c9f8-153">下图显示 Fabrikam 站点的导航菜单中显示的类别图像的示例。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-153">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="6c9f8-154">![导航菜单模块和类别图像的示例](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="6c9f8-154">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="6c9f8-155">向标题模块添加导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="6c9f8-155">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="6c9f8-156">有关如何向标题模块添加导航菜单模块的详细信息，请参阅[标题模块](author-header-module.md) 。</span><span class="sxs-lookup"><span data-stu-id="6c9f8-156">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c9f8-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="6c9f8-157">Additional resources</span></span>

[<span data-ttu-id="6c9f8-158">模块库概览</span><span class="sxs-lookup"><span data-stu-id="6c9f8-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6c9f8-159">痕迹导航模块</span><span class="sxs-lookup"><span data-stu-id="6c9f8-159">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="6c9f8-160">站点选择器模块</span><span class="sxs-lookup"><span data-stu-id="6c9f8-160">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="6c9f8-161">购买框模块</span><span class="sxs-lookup"><span data-stu-id="6c9f8-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6c9f8-162">Cookie 合规性</span><span class="sxs-lookup"><span data-stu-id="6c9f8-162">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="6c9f8-163">标题模块</span><span class="sxs-lookup"><span data-stu-id="6c9f8-163">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]