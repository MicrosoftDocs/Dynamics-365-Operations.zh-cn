---
title: 导航菜单模块
description: 此主题介绍导航菜单模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055729"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="5ef94-103">导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="5ef94-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5ef94-104">此主题介绍导航菜单模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="5ef94-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5ef94-105">概览</span><span class="sxs-lookup"><span data-stu-id="5ef94-105">Overview</span></span>

<span data-ttu-id="5ef94-106">导航菜单模块的主要用途是让站点用户可以根据 Dynamics 365 Commerce 总部中定义的渠道导航层次结构浏览产品和站点页面。</span><span class="sxs-lookup"><span data-stu-id="5ef94-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="5ef94-107">导航菜单模块中配置的项显示为站点标题导航。</span><span class="sxs-lookup"><span data-stu-id="5ef94-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="5ef94-108">导航菜单模块还支持链接到电子商务网站上其他页面的静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="5ef94-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="5ef94-109">导航菜单模块可以添加到页面的标题模块。</span><span class="sxs-lookup"><span data-stu-id="5ef94-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="5ef94-110">默认情况下，Fabrikam 主题中的导航菜单显示两个级别。</span><span class="sxs-lookup"><span data-stu-id="5ef94-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="5ef94-111">默认情况下，Starter 主题中的导航菜单显示三个级别。</span><span class="sxs-lookup"><span data-stu-id="5ef94-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="5ef94-112">若要切换为级别数量，主题中需要视图扩展。</span><span class="sxs-lookup"><span data-stu-id="5ef94-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="5ef94-113">下图显示 Fabrikam 站点的导航菜单示例，以及两个类别层次结构级别和一些静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="5ef94-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="5ef94-114">![导航菜单模块的示例](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="5ef94-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="5ef94-115">导航菜单模块属性</span><span class="sxs-lookup"><span data-stu-id="5ef94-115">Navigation menu module properties</span></span>

| <span data-ttu-id="5ef94-116">属性名称</span><span class="sxs-lookup"><span data-stu-id="5ef94-116">Property name</span></span>             | <span data-ttu-id="5ef94-117">值</span><span class="sxs-lookup"><span data-stu-id="5ef94-117">Value</span></span>                 | <span data-ttu-id="5ef94-118">说明</span><span class="sxs-lookup"><span data-stu-id="5ef94-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="5ef94-119">源</span><span class="sxs-lookup"><span data-stu-id="5ef94-119">Source</span></span>                  | <span data-ttu-id="5ef94-120">**零售** 、 **手动创作** 、 **零售和手动创作**</span><span class="sxs-lookup"><span data-stu-id="5ef94-120">**Retail** , **Manual authoring** , **Retail and manual authoring**</span></span> | <span data-ttu-id="5ef94-121">**零售** 值允许在导航菜单中显示 Commerce 总部的渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="5ef94-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="5ef94-122">**手动创作** 值允许策划静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="5ef94-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="5ef94-123">**零售和手动创作** 值允许混合使用两者。</span><span class="sxs-lookup"><span data-stu-id="5ef94-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="5ef94-124">显示类别图像</span><span class="sxs-lookup"><span data-stu-id="5ef94-124">Show category images</span></span> | <span data-ttu-id="5ef94-125">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="5ef94-125">**True** or **False**</span></span>    | <span data-ttu-id="5ef94-126">启用后，此属性将在 Commerce 总部中为每个类别定义的导航菜单上显示类别图像。</span><span class="sxs-lookup"><span data-stu-id="5ef94-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="5ef94-127">Commerce 版本 10.0.14 中已添加。</span><span class="sxs-lookup"><span data-stu-id="5ef94-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="5ef94-128">启用多级导航菜单</span><span class="sxs-lookup"><span data-stu-id="5ef94-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="5ef94-129">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="5ef94-129">**True** or **False**</span></span> | <span data-ttu-id="5ef94-130">启用此属性后，导航菜单可以显示多级导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="5ef94-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="5ef94-131">Dynamics 365 Commerce 10.0.15 版本中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="5ef94-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="5ef94-132">层数</span><span class="sxs-lookup"><span data-stu-id="5ef94-132">Number of levels</span></span> | <span data-ttu-id="5ef94-133">整数</span><span class="sxs-lookup"><span data-stu-id="5ef94-133">integer</span></span> | <span data-ttu-id="5ef94-134">如果 **启用多级导航菜单** 属性设置为 **True** ，此属性将定义应该显示的级别数。</span><span class="sxs-lookup"><span data-stu-id="5ef94-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="5ef94-135">静态菜单项</span><span class="sxs-lookup"><span data-stu-id="5ef94-135">Static menu item</span></span>| <span data-ttu-id="5ef94-136">值数组</span><span class="sxs-lookup"><span data-stu-id="5ef94-136">Array of values</span></span>| <span data-ttu-id="5ef94-137">将菜单项名称与静态站点页的链接关联的静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="5ef94-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="5ef94-138">可以在其他菜单项下创建菜单项。</span><span class="sxs-lookup"><span data-stu-id="5ef94-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="5ef94-139">默认情况下，静态菜单在根级别显示，并将追加到渠道导航层次结构（如果有）。</span><span class="sxs-lookup"><span data-stu-id="5ef94-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="5ef94-140">显示根菜单</span><span class="sxs-lookup"><span data-stu-id="5ef94-140">Show root menu</span></span> | <span data-ttu-id="5ef94-141">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="5ef94-141">**True** or **False**</span></span> | <span data-ttu-id="5ef94-142">启用此属性后，可以在自定义根下定义导航菜单（例如， **立即购物** ）。</span><span class="sxs-lookup"><span data-stu-id="5ef94-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now** ).</span></span> <span data-ttu-id="5ef94-143">Dynamics 365 Commerce 10.0.15 版本中提供此功能。</span><span class="sxs-lookup"><span data-stu-id="5ef94-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="5ef94-144">根菜单</span><span class="sxs-lookup"><span data-stu-id="5ef94-144">Root menu</span></span> | <span data-ttu-id="5ef94-145">字符串</span><span class="sxs-lookup"><span data-stu-id="5ef94-145">string</span></span> | <span data-ttu-id="5ef94-146">如果 **显示根菜单** 属性设置为 **True** ，此属性可用于为自定义根定义文本。</span><span class="sxs-lookup"><span data-stu-id="5ef94-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="5ef94-147">下图显示 Fabrikam 站点的导航菜单中显示的类别图像的示例。</span><span class="sxs-lookup"><span data-stu-id="5ef94-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="5ef94-148">![导航菜单模块和类别图像的示例](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="5ef94-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="5ef94-149">向标题模块添加导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="5ef94-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="5ef94-150">有关如何向标题模块添加导航菜单模块的详细信息，请参阅[标题模块](author-header-module.md) 。</span><span class="sxs-lookup"><span data-stu-id="5ef94-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ef94-151">其他资源</span><span class="sxs-lookup"><span data-stu-id="5ef94-151">Additional resources</span></span>

[<span data-ttu-id="5ef94-152">模块库概览</span><span class="sxs-lookup"><span data-stu-id="5ef94-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5ef94-153">痕迹导航模块</span><span class="sxs-lookup"><span data-stu-id="5ef94-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="5ef94-154">站点选择器模块</span><span class="sxs-lookup"><span data-stu-id="5ef94-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="5ef94-155">购买框模块</span><span class="sxs-lookup"><span data-stu-id="5ef94-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5ef94-156">Cookie 合规性</span><span class="sxs-lookup"><span data-stu-id="5ef94-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="5ef94-157">标题模块</span><span class="sxs-lookup"><span data-stu-id="5ef94-157">Header module</span></span>](author-header-module.md)
