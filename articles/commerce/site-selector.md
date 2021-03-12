---
title: 站点选择器模块
description: 本主题介绍了站点选择器模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ed00836c435bd391e5edef1f6a99889c80f45211
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985578"
---
# <a name="site-selector-module"></a><span data-ttu-id="6ec60-103">站点选择器模块</span><span class="sxs-lookup"><span data-stu-id="6ec60-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6ec60-104">本主题介绍了站点选择器模块以及如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页面。</span><span class="sxs-lookup"><span data-stu-id="6ec60-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6ec60-105">概览</span><span class="sxs-lookup"><span data-stu-id="6ec60-105">Overview</span></span>

<span data-ttu-id="6ec60-106">当企业跨市场、地区和区域具有不同的站点时，站点用户需要通过一种简单的方法在站点之间进行切换并选择他们喜欢的购物站点。</span><span class="sxs-lookup"><span data-stu-id="6ec60-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="6ec60-107">为了适应这种情况，站点选择器模块使用户能够跨多个站点浏览。</span><span class="sxs-lookup"><span data-stu-id="6ec60-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="6ec60-108">站点选择器模块必须配置有站点用户可以浏览的站点列表（市场、地区或区域）。</span><span class="sxs-lookup"><span data-stu-id="6ec60-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="6ec60-109">Dynamics 365 Commerce 10.0.14 版本中提供了站点选择器模块。</span><span class="sxs-lookup"><span data-stu-id="6ec60-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="6ec60-110">下图显示了站点页面标题中具有的站点选择器模块示例。</span><span class="sxs-lookup"><span data-stu-id="6ec60-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![站点页面标题中的站点选择器模块示例](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="6ec60-112">站点选择器模块属性</span><span class="sxs-lookup"><span data-stu-id="6ec60-112">Site selector module properties</span></span>

| <span data-ttu-id="6ec60-113">属性名称</span><span class="sxs-lookup"><span data-stu-id="6ec60-113">Property name</span></span> | <span data-ttu-id="6ec60-114">值</span><span class="sxs-lookup"><span data-stu-id="6ec60-114">Value</span></span>                 | <span data-ttu-id="6ec60-115">说明</span><span class="sxs-lookup"><span data-stu-id="6ec60-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="6ec60-116">标题</span><span class="sxs-lookup"><span data-stu-id="6ec60-116">Heading</span></span>       | <span data-ttu-id="6ec60-117">文本</span><span class="sxs-lookup"><span data-stu-id="6ec60-117">Text</span></span>                  | <span data-ttu-id="6ec60-118">模块的标题。</span><span class="sxs-lookup"><span data-stu-id="6ec60-118">The heading for the module.</span></span> |
| <span data-ttu-id="6ec60-119">站点选项</span><span class="sxs-lookup"><span data-stu-id="6ec60-119">Site options</span></span>  | <span data-ttu-id="6ec60-120">名称、图像、URL</span><span class="sxs-lookup"><span data-stu-id="6ec60-120">Name, Image, URL</span></span>      | <span data-ttu-id="6ec60-121">此属性指定名称、指向站点主页的链接以及为模块中包含的每个站点显示的可选图像。</span><span class="sxs-lookup"><span data-stu-id="6ec60-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="6ec60-122">该图像可以是旗帜，也可以是市场、地区或区域的某种表示形式。</span><span class="sxs-lookup"><span data-stu-id="6ec60-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="6ec60-123">向页面添加站点选择器模块</span><span class="sxs-lookup"><span data-stu-id="6ec60-123">Add a site selector module to a page</span></span>

<span data-ttu-id="6ec60-124">站点选择器模块可以添加到站点选择器插槽下的[标题模块](author-header-module.md)。</span><span class="sxs-lookup"><span data-stu-id="6ec60-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="6ec60-125">添加后，您可以定义模块标题和站点选项。</span><span class="sxs-lookup"><span data-stu-id="6ec60-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ec60-126">其他资源</span><span class="sxs-lookup"><span data-stu-id="6ec60-126">Additional resources</span></span>

[<span data-ttu-id="6ec60-127">模块库概览</span><span class="sxs-lookup"><span data-stu-id="6ec60-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6ec60-128">标题模块</span><span class="sxs-lookup"><span data-stu-id="6ec60-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6ec60-129">痕迹导航模块</span><span class="sxs-lookup"><span data-stu-id="6ec60-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="6ec60-130">导航菜单模块</span><span class="sxs-lookup"><span data-stu-id="6ec60-130">Navigation menu module</span></span>](nav-menu-module.md)
