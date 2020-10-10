---
title: 导航菜单模块
description: 此主题介绍导航菜单模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817866"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="acf0b-103">导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="acf0b-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="acf0b-104">此主题介绍导航菜单模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="acf0b-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="acf0b-105">概览</span><span class="sxs-lookup"><span data-stu-id="acf0b-105">Overview</span></span>

<span data-ttu-id="acf0b-106">导航菜单模块的主要用途是让站点用户可以根据 Dynamics 365 Commerce 总部中定义的渠道导航层次结构浏览产品和站点页面。</span><span class="sxs-lookup"><span data-stu-id="acf0b-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="acf0b-107">导航菜单模块中配置的项显示为站点标题导航。</span><span class="sxs-lookup"><span data-stu-id="acf0b-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="acf0b-108">导航菜单模块还支持链接到电子商务网站上其他页面的静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="acf0b-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="acf0b-109">导航菜单模块可以添加到页面的标题模块。</span><span class="sxs-lookup"><span data-stu-id="acf0b-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="acf0b-110">默认情况下，Fabrikam 主题中的导航菜单显示两个级别。</span><span class="sxs-lookup"><span data-stu-id="acf0b-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="acf0b-111">默认情况下，Starter 主题中的导航菜单显示三个级别。</span><span class="sxs-lookup"><span data-stu-id="acf0b-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="acf0b-112">若要切换为级别数量，主题中需要视图扩展。</span><span class="sxs-lookup"><span data-stu-id="acf0b-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="acf0b-113">下图显示 Fabrikam 站点的导航菜单示例，以及两个类别层次结构级别和一些静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="acf0b-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="acf0b-114">![导航菜单模块的示例](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="acf0b-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="acf0b-115">导航菜单模块属性</span><span class="sxs-lookup"><span data-stu-id="acf0b-115">Navigation menu module properties</span></span>

| <span data-ttu-id="acf0b-116">属性名称</span><span class="sxs-lookup"><span data-stu-id="acf0b-116">Property name</span></span>             | <span data-ttu-id="acf0b-117">值</span><span class="sxs-lookup"><span data-stu-id="acf0b-117">Value</span></span>                 | <span data-ttu-id="acf0b-118">说明</span><span class="sxs-lookup"><span data-stu-id="acf0b-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="acf0b-119">源</span><span class="sxs-lookup"><span data-stu-id="acf0b-119">Source</span></span>                  | <span data-ttu-id="acf0b-120">**零售**、**手动创作**、**零售和手动创作**</span><span class="sxs-lookup"><span data-stu-id="acf0b-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="acf0b-121">**零售**值允许在导航菜单中显示 Commerce 总部的渠道导航层次结构。</span><span class="sxs-lookup"><span data-stu-id="acf0b-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="acf0b-122">**手动创作**值允许策划静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="acf0b-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="acf0b-123">**零售和手动创作**值允许混合使用两者。</span><span class="sxs-lookup"><span data-stu-id="acf0b-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="acf0b-124">显示类别图像</span><span class="sxs-lookup"><span data-stu-id="acf0b-124">Show category images</span></span> | <span data-ttu-id="acf0b-125">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="acf0b-125">**True** or **False**</span></span>    | <span data-ttu-id="acf0b-126">启用后，此属性将在 Commerce 总部中为每个类别定义的导航菜单上显示类别图像。</span><span class="sxs-lookup"><span data-stu-id="acf0b-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="acf0b-127">Commerce 版本 10.0.14 中已添加。</span><span class="sxs-lookup"><span data-stu-id="acf0b-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="acf0b-128">静态菜单项</span><span class="sxs-lookup"><span data-stu-id="acf0b-128">Static menu item</span></span>| <span data-ttu-id="acf0b-129">值数组</span><span class="sxs-lookup"><span data-stu-id="acf0b-129">Array of values</span></span>| <span data-ttu-id="acf0b-130">将菜单项名称与静态站点页的链接关联的静态菜单项。</span><span class="sxs-lookup"><span data-stu-id="acf0b-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="acf0b-131">可以在其他菜单项下创建菜单项。</span><span class="sxs-lookup"><span data-stu-id="acf0b-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="acf0b-132">默认情况下，静态菜单在根级别显示，并将追加到渠道导航层次结构（如果有）。</span><span class="sxs-lookup"><span data-stu-id="acf0b-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="acf0b-133">下图显示 Fabrikam 站点的导航菜单中显示的类别图像的示例。</span><span class="sxs-lookup"><span data-stu-id="acf0b-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="acf0b-134">![导航菜单模块和类别图像的示例](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="acf0b-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="acf0b-135">向标题模块添加导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="acf0b-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="acf0b-136">有关如何向标题模块添加导航菜单模块的详细信息，请参阅[标题模块](author-header-module.md) 。</span><span class="sxs-lookup"><span data-stu-id="acf0b-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="acf0b-137">其他资源</span><span class="sxs-lookup"><span data-stu-id="acf0b-137">Additional resources</span></span>

[<span data-ttu-id="acf0b-138">模块库概述</span><span class="sxs-lookup"><span data-stu-id="acf0b-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="acf0b-139">购买框模块</span><span class="sxs-lookup"><span data-stu-id="acf0b-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="acf0b-140">Cookie 合规性</span><span class="sxs-lookup"><span data-stu-id="acf0b-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="acf0b-141">标题模块</span><span class="sxs-lookup"><span data-stu-id="acf0b-141">Header module</span></span>](author-header-module.md)
