---
title: 模块库概览
description: 此主题概述 Microsoft Dynamics 365 Commerce 模块库。
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76fd75c2ed9a3ba4728129b77a43b50267be3bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795325"
---
# <a name="module-library-overview"></a><span data-ttu-id="cf213-103">模块库概览</span><span class="sxs-lookup"><span data-stu-id="cf213-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf213-104">此主题概述 Microsoft Dynamics 365 Commerce 模块库。</span><span class="sxs-lookup"><span data-stu-id="cf213-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="cf213-105">Dynamics 365 Commerce 模块库是可用于生成电子商务网站的模块的集合。</span><span class="sxs-lookup"><span data-stu-id="cf213-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="cf213-106">模块同时采用用户界面 (UI) 和功能行为。</span><span class="sxs-lookup"><span data-stu-id="cf213-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="cf213-107">可将主题应用于模块库中的模块以更改其外观。</span><span class="sxs-lookup"><span data-stu-id="cf213-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="cf213-108">这些主题使用级联样式表 (CSS)。</span><span class="sxs-lookup"><span data-stu-id="cf213-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="cf213-109">模块库中提供一个名称为“Fabrikam”的虚构电子商务站点主题，可将其用作参考。</span><span class="sxs-lookup"><span data-stu-id="cf213-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="cf213-110">模块库模块</span><span class="sxs-lookup"><span data-stu-id="cf213-110">Module library modules</span></span>

<span data-ttu-id="cf213-111">模块库中提供以下类型的模块：</span><span class="sxs-lookup"><span data-stu-id="cf213-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="cf213-112">**容器模块** – 容器模块是充当其他模块的主机的简单模块。</span><span class="sxs-lookup"><span data-stu-id="cf213-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="cf213-113">用于控制模块在其内的布局。</span><span class="sxs-lookup"><span data-stu-id="cf213-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="cf213-114">**市场营销模块** – 市场营销模块包括内容块、文本块、视频播放器和传送模块。</span><span class="sxs-lookup"><span data-stu-id="cf213-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="cf213-115">所有这些模块都可用于展示内容。</span><span class="sxs-lookup"><span data-stu-id="cf213-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="cf213-116">可以放到任何页面中，并由内容管理系统 (CMS) 的数据驱动。</span><span class="sxs-lookup"><span data-stu-id="cf213-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="cf213-117">**页眉和页脚模块** – 页眉和页脚模块在所有站点页的页眉和页脚中显示。</span><span class="sxs-lookup"><span data-stu-id="cf213-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="cf213-118">可以根据需要通过属性配置这些模块。</span><span class="sxs-lookup"><span data-stu-id="cf213-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="cf213-119">**搜索模块** –可以使用页眉中的搜索模块发现产品。</span><span class="sxs-lookup"><span data-stu-id="cf213-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="cf213-120">搜索结果在搜索结果页中显示。</span><span class="sxs-lookup"><span data-stu-id="cf213-120">Search results appear on the search results page.</span></span> <span data-ttu-id="cf213-121">也可以在类别页中发现产品，类别页是渠道导航层次结构中支持的每个类别的专用页。</span><span class="sxs-lookup"><span data-stu-id="cf213-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="cf213-122">此外，还可以使用优化器模块进一步筛选搜索结果和类别页中的结果。</span><span class="sxs-lookup"><span data-stu-id="cf213-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="cf213-123">**产品详细信息页模块** – 产品详细信息页使用多个模块显示产品信息。</span><span class="sxs-lookup"><span data-stu-id="cf213-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="cf213-124">客户可使用购买框模块查看产品和将产品添加到购物车。</span><span class="sxs-lookup"><span data-stu-id="cf213-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="cf213-125">其他模块（如技术规范模块）显示产品详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf213-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="cf213-126">评分和评价模块可用于查看和提供评价。</span><span class="sxs-lookup"><span data-stu-id="cf213-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="cf213-127">**在线购买，店内提货模块** – 在线购买，店内提货模块与 Bing 地图集成。</span><span class="sxs-lookup"><span data-stu-id="cf213-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="cf213-128">可用于查找客户可提取已购买产品的附近商店。</span><span class="sxs-lookup"><span data-stu-id="cf213-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="cf213-129">**购买模块** – 购买模块中包含购物车模块，后者可用于将商品添加到购物车。</span><span class="sxs-lookup"><span data-stu-id="cf213-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="cf213-130">结帐模块捕获装运地址、交货选项和礼品卡、会员计划与信用卡信息，以便处理订单。</span><span class="sxs-lookup"><span data-stu-id="cf213-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="cf213-131">下订单之后，可使用订单确认模块显示确认详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf213-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="cf213-132">**帐户管理模块** – 客户可使用登录模块登录到现有帐户，可使用注册模块创建新帐户。</span><span class="sxs-lookup"><span data-stu-id="cf213-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="cf213-133">创建帐户之后，可使用订单历史记录模块查看最近订单，可使用订单详细信息模块查看订单详细信息。</span><span class="sxs-lookup"><span data-stu-id="cf213-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="cf213-134">**建议模块** – 可使用产品放置模块显示建议。</span><span class="sxs-lookup"><span data-stu-id="cf213-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="cf213-135">此模块支持算法列表和编辑列表，这些列表可在任何页面中展示。</span><span class="sxs-lookup"><span data-stu-id="cf213-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf213-136">其他资源</span><span class="sxs-lookup"><span data-stu-id="cf213-136">Additional resources</span></span>

[<span data-ttu-id="cf213-137">容器模块</span><span class="sxs-lookup"><span data-stu-id="cf213-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="cf213-138">购买框模块</span><span class="sxs-lookup"><span data-stu-id="cf213-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="cf213-139">购物车模块</span><span class="sxs-lookup"><span data-stu-id="cf213-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="cf213-140">结帐模块</span><span class="sxs-lookup"><span data-stu-id="cf213-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="cf213-141">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="cf213-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="cf213-142">页眉模块</span><span class="sxs-lookup"><span data-stu-id="cf213-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="cf213-143">页脚模块</span><span class="sxs-lookup"><span data-stu-id="cf213-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]