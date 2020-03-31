---
title: 评分和评价模块
description: 此主题介绍 Microsoft Dynamics 365 Commerce 中产品详细信息页上使用的评分和评论模块。
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
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
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: ee2a2a781537b592fb5f80ce424a7331c4e21d41
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071842"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="088f2-103">评分和评价模块</span><span class="sxs-lookup"><span data-stu-id="088f2-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="088f2-104">此主题介绍 Microsoft Dynamics 365 Commerce 中产品详细信息页 (PDP) 上使用的评分和评论模块。</span><span class="sxs-lookup"><span data-stu-id="088f2-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="088f2-105">概览</span><span class="sxs-lookup"><span data-stu-id="088f2-105">Overview</span></span>

<span data-ttu-id="088f2-106">电子商务网站中的评分和评价可帮助客户在做出采购决定之前了解产品，也是收集客户对产品的反馈的机制。</span><span class="sxs-lookup"><span data-stu-id="088f2-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="088f2-107">评分在产品列表页、类别列表页、搜索结果页和其他站点页中显示。</span><span class="sxs-lookup"><span data-stu-id="088f2-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="088f2-108">评分直方图和产品评价在 PDP 中显示。</span><span class="sxs-lookup"><span data-stu-id="088f2-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="088f2-109">客户可使用**撰写评价**按钮提交产品的评分和评价。</span><span class="sxs-lookup"><span data-stu-id="088f2-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="088f2-110">这些 PDP 功能受评分和评价模块控制。</span><span class="sxs-lookup"><span data-stu-id="088f2-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="088f2-111">PDP 中的评分和评价模块</span><span class="sxs-lookup"><span data-stu-id="088f2-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="088f2-112">PDP 中的三个模块显示评分和评价摘要：</span><span class="sxs-lookup"><span data-stu-id="088f2-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="088f2-113">撰写评价模块</span><span class="sxs-lookup"><span data-stu-id="088f2-113">Write review module</span></span>
- <span data-ttu-id="088f2-114">产品评级列表模块</span><span class="sxs-lookup"><span data-stu-id="088f2-114">Product reviews list module</span></span>
- <span data-ttu-id="088f2-115">评分直方图模块</span><span class="sxs-lookup"><span data-stu-id="088f2-115">Ratings histogram module</span></span>
 
<span data-ttu-id="088f2-116">下图显示评分和评价模块在 PDP 上的外观。</span><span class="sxs-lookup"><span data-stu-id="088f2-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![PDP 上的评分和评价模块](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="088f2-118">有关如何优化 PDP 模板和布局，以便在电子商务站点中的多个 PDP 之间共享评分和评价模块的配置的信息，请参阅[模板和布局概述](templates-layouts-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="088f2-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="088f2-119">下图显示 Dynamics 365 Commerce 中**添加模块**对话框如何显示评分和评价模块。</span><span class="sxs-lookup"><span data-stu-id="088f2-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="088f2-120">![“添加模块”对话框](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="088f2-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="088f2-121">撰写评价模块</span><span class="sxs-lookup"><span data-stu-id="088f2-121">Write review module</span></span>

<span data-ttu-id="088f2-122">撰写评价模块中有一个**撰写评价**按钮，供用户登录，分配评分和撰写产品评价。</span><span class="sxs-lookup"><span data-stu-id="088f2-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="088f2-123">用户可使用此模块编辑之前提交的评分或评价。</span><span class="sxs-lookup"><span data-stu-id="088f2-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="088f2-124">此模块通常在 PDP 上的评分直方图和产品评价列表模块上方显示。</span><span class="sxs-lookup"><span data-stu-id="088f2-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="088f2-125">下图显示当客户选择**撰写评价**时显示的**撰写评价**对话框。</span><span class="sxs-lookup"><span data-stu-id="088f2-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="088f2-126">客户可使用此对话框提交评分和评价。</span><span class="sxs-lookup"><span data-stu-id="088f2-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="088f2-127">![“撰写评价”对话框](media/rnr-eCommerce-write-review-module.png) 下表显示需要在制作工具中配置的撰写评价模块属性。</span><span class="sxs-lookup"><span data-stu-id="088f2-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="088f2-128">属性名称</span><span class="sxs-lookup"><span data-stu-id="088f2-128">Property name</span></span> | <span data-ttu-id="088f2-129">值</span><span class="sxs-lookup"><span data-stu-id="088f2-129">Value</span></span>        | <span data-ttu-id="088f2-130">属性描述</span><span class="sxs-lookup"><span data-stu-id="088f2-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="088f2-131">姓名</span><span class="sxs-lookup"><span data-stu-id="088f2-131">Name</span></span>          | <span data-ttu-id="088f2-132">撰写评价</span><span class="sxs-lookup"><span data-stu-id="088f2-132">Write review</span></span> | <span data-ttu-id="088f2-133">撰写评价模块的名称。</span><span class="sxs-lookup"><span data-stu-id="088f2-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="088f2-134">评分直方图模块</span><span class="sxs-lookup"><span data-stu-id="088f2-134">Ratings histogram module</span></span>

<span data-ttu-id="088f2-135">评分直方图模块显示评分直方图。</span><span class="sxs-lookup"><span data-stu-id="088f2-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="088f2-136">此模块通常在 PDP 中撰写评论模块与产品评论列表模块之间显示。</span><span class="sxs-lookup"><span data-stu-id="088f2-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="088f2-137">评分直方图模块不需要配置。</span><span class="sxs-lookup"><span data-stu-id="088f2-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="088f2-138">只需在 PDP 模板中添加此模块。</span><span class="sxs-lookup"><span data-stu-id="088f2-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="088f2-139">下图显示将评分和评价模块配置为在 PDP 中显示时，PDP 模板在 Dynamics 365 Commerce 中的外观。</span><span class="sxs-lookup"><span data-stu-id="088f2-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="088f2-140">![将评分或评价配置为在 PDP 中显示时的 PDP 模板](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="088f2-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="088f2-141">产品评级列表模块</span><span class="sxs-lookup"><span data-stu-id="088f2-141">Product reviews list module</span></span>

<span data-ttu-id="088f2-142">产品评级列表模块显示产品评级列表和排序、筛选和分页选项。</span><span class="sxs-lookup"><span data-stu-id="088f2-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="088f2-143">此模块通常在 PDP 中的评分直方图模块后显示。</span><span class="sxs-lookup"><span data-stu-id="088f2-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="088f2-144">下表显示需要在制作工具中配置的产品评价列表模块属性。</span><span class="sxs-lookup"><span data-stu-id="088f2-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="088f2-145">属性名称</span><span class="sxs-lookup"><span data-stu-id="088f2-145">Property name</span></span>              | <span data-ttu-id="088f2-146">值</span><span class="sxs-lookup"><span data-stu-id="088f2-146">Value</span></span> | <span data-ttu-id="088f2-147">属性描述</span><span class="sxs-lookup"><span data-stu-id="088f2-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="088f2-148">每页显示的评论</span><span class="sxs-lookup"><span data-stu-id="088f2-148">Reviews shown on each page</span></span> | <span data-ttu-id="088f2-149">10</span><span class="sxs-lookup"><span data-stu-id="088f2-149">10</span></span>    | <span data-ttu-id="088f2-150">PDP 中应该同时显示的评论数量。</span><span class="sxs-lookup"><span data-stu-id="088f2-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="088f2-151">包括**下一页**和**上一页**按钮，以便用户在多页评论之间切换。</span><span class="sxs-lookup"><span data-stu-id="088f2-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="088f2-152">评分直方图 – 摘要视图</span><span class="sxs-lookup"><span data-stu-id="088f2-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="088f2-153">产品评论列表模块中有一个插槽，可在其中添加评分直方图模块。</span><span class="sxs-lookup"><span data-stu-id="088f2-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="088f2-154">下图显示如何在 Dynamics 365 Commerce 中的产品评论列表模块内添加评分直方图模块。</span><span class="sxs-lookup"><span data-stu-id="088f2-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![在产品评论列表模块中添加评分直方图模块](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="088f2-156">其他资源</span><span class="sxs-lookup"><span data-stu-id="088f2-156">Additional resources</span></span>

[<span data-ttu-id="088f2-157">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="088f2-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="088f2-158">容器模块</span><span class="sxs-lookup"><span data-stu-id="088f2-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="088f2-159">购物车模块</span><span class="sxs-lookup"><span data-stu-id="088f2-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="088f2-160">结帐模块</span><span class="sxs-lookup"><span data-stu-id="088f2-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="088f2-161">订单确认模块</span><span class="sxs-lookup"><span data-stu-id="088f2-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="088f2-162">页眉模块</span><span class="sxs-lookup"><span data-stu-id="088f2-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="088f2-163">页脚模块</span><span class="sxs-lookup"><span data-stu-id="088f2-163">Footer module</span></span>](author-footer-module.md)