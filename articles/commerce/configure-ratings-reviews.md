---
title: 配置评分和评价
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置电子商务站点以显示客户评分和评价。
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770473"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="cda96-103">配置评分和评价</span><span class="sxs-lookup"><span data-stu-id="cda96-103">Configure ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cda96-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置电子商务站点以显示客户评分和评价。</span><span class="sxs-lookup"><span data-stu-id="cda96-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cda96-105">概览</span><span class="sxs-lookup"><span data-stu-id="cda96-105">Overview</span></span>

<span data-ttu-id="cda96-106">电子商务网站中的评分和评价可帮助客户在做出采购决定之前了解产品，方法是对其显示其他客户对这些产品的看法。</span><span class="sxs-lookup"><span data-stu-id="cda96-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="cda96-107">对于电子商务网站，评分和评价也是用于收集有关产品的客户反馈的机制。</span><span class="sxs-lookup"><span data-stu-id="cda96-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="cda96-108">评分在产品列表页、类别列表页、搜索结果页和其他站点页中显示。</span><span class="sxs-lookup"><span data-stu-id="cda96-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="cda96-109">评分直方图和产品评价在产品详细信息页 (PDP) 中显示。</span><span class="sxs-lookup"><span data-stu-id="cda96-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="cda96-110">客户可使用**撰写评价**按钮提交产品的评分和评价。</span><span class="sxs-lookup"><span data-stu-id="cda96-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="cda96-111">PDP 中的评分和评价模块</span><span class="sxs-lookup"><span data-stu-id="cda96-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="cda96-112">PDP 中的三个模块显示评分和评价摘要：</span><span class="sxs-lookup"><span data-stu-id="cda96-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="cda96-113">撰写评价模块</span><span class="sxs-lookup"><span data-stu-id="cda96-113">Write review module</span></span>
- <span data-ttu-id="cda96-114">产品评级列表模块</span><span class="sxs-lookup"><span data-stu-id="cda96-114">Product reviews list module</span></span>
- <span data-ttu-id="cda96-115">评分直方图模块</span><span class="sxs-lookup"><span data-stu-id="cda96-115">Ratings histogram module</span></span>
 
<span data-ttu-id="cda96-116">下图显示评分和评价模块在 PDP 上的外观。</span><span class="sxs-lookup"><span data-stu-id="cda96-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![PDP 上的评分和评价模块](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="cda96-118">有关如何优化 PDP 模板和布局，以便在电子商务站点中的多个 PDP 之间共享评分和评价模块的配置的信息，请参阅[模板和布局概述](templates-layouts-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="cda96-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="cda96-119">下图显示 Dynamics 365 Commerce 中**添加模块**对话框如何显示评分和评价模块。</span><span class="sxs-lookup"><span data-stu-id="cda96-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![“添加模块”对话框](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="cda96-121">撰写评价模块</span><span class="sxs-lookup"><span data-stu-id="cda96-121">Write review module</span></span>

<span data-ttu-id="cda96-122">撰写评价模块中有一个**撰写评价**按钮，供用户登录，分配评分和撰写产品评价。</span><span class="sxs-lookup"><span data-stu-id="cda96-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="cda96-123">用户可使用此模块编辑之前提交的评分或评价。</span><span class="sxs-lookup"><span data-stu-id="cda96-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="cda96-124">此模块通常在 PDP 上的评分直方图和产品评价列表模块上方显示。</span><span class="sxs-lookup"><span data-stu-id="cda96-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="cda96-125">下图显示当客户选择**撰写评价**时显示的**撰写评价**对话框。</span><span class="sxs-lookup"><span data-stu-id="cda96-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="cda96-126">客户可使用此对话框提交评分和评价。</span><span class="sxs-lookup"><span data-stu-id="cda96-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![“撰写评价”对话框](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="cda96-128">下表显示需要在制作工具中配置的撰写评价模块属性。</span><span class="sxs-lookup"><span data-stu-id="cda96-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="cda96-129">属性名称</span><span class="sxs-lookup"><span data-stu-id="cda96-129">Property name</span></span> | <span data-ttu-id="cda96-130">值</span><span class="sxs-lookup"><span data-stu-id="cda96-130">Value</span></span>        | <span data-ttu-id="cda96-131">属性描述</span><span class="sxs-lookup"><span data-stu-id="cda96-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="cda96-132">姓名</span><span class="sxs-lookup"><span data-stu-id="cda96-132">Name</span></span>          | <span data-ttu-id="cda96-133">撰写评价</span><span class="sxs-lookup"><span data-stu-id="cda96-133">Write review</span></span> | <span data-ttu-id="cda96-134">撰写评价模块的名称。</span><span class="sxs-lookup"><span data-stu-id="cda96-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="cda96-135">评分直方图模块</span><span class="sxs-lookup"><span data-stu-id="cda96-135">Ratings histogram module</span></span>

<span data-ttu-id="cda96-136">评分直方图模块显示评分直方图。</span><span class="sxs-lookup"><span data-stu-id="cda96-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="cda96-137">此模块通常在 PDP 中撰写评论模块与产品评论列表模块之间显示。</span><span class="sxs-lookup"><span data-stu-id="cda96-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="cda96-138">评分直方图模块不需要配置。</span><span class="sxs-lookup"><span data-stu-id="cda96-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="cda96-139">只需在 PDP 模板中添加此模块。</span><span class="sxs-lookup"><span data-stu-id="cda96-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="cda96-140">下图显示将评分和评价模块配置为在 PDP 中显示时，PDP 模板在 Dynamics 365 Commerce 中的外观。</span><span class="sxs-lookup"><span data-stu-id="cda96-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![将评分或评价配置为在 PDP 中显示时的 PDP 模板](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="cda96-142">产品评级列表模块</span><span class="sxs-lookup"><span data-stu-id="cda96-142">Product reviews list module</span></span>

<span data-ttu-id="cda96-143">产品评级列表模块显示产品评级列表和排序、筛选和分页选项。</span><span class="sxs-lookup"><span data-stu-id="cda96-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="cda96-144">此模块通常在 PDP 中的评分直方图模块后显示。</span><span class="sxs-lookup"><span data-stu-id="cda96-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="cda96-145">下表显示需要在制作工具中配置的产品评价列表模块属性。</span><span class="sxs-lookup"><span data-stu-id="cda96-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="cda96-146">属性名称</span><span class="sxs-lookup"><span data-stu-id="cda96-146">Property name</span></span>              | <span data-ttu-id="cda96-147">值</span><span class="sxs-lookup"><span data-stu-id="cda96-147">Value</span></span> | <span data-ttu-id="cda96-148">属性描述</span><span class="sxs-lookup"><span data-stu-id="cda96-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="cda96-149">每页显示的评论</span><span class="sxs-lookup"><span data-stu-id="cda96-149">Reviews shown on each page</span></span> | <span data-ttu-id="cda96-150">10</span><span class="sxs-lookup"><span data-stu-id="cda96-150">10</span></span>    | <span data-ttu-id="cda96-151">PDP 中应该同时显示的评论数量。</span><span class="sxs-lookup"><span data-stu-id="cda96-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="cda96-152">包括**下一页**和**上一页**按钮，以便用户在多页评论之间切换。</span><span class="sxs-lookup"><span data-stu-id="cda96-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="cda96-153">评分直方图 – 摘要视图</span><span class="sxs-lookup"><span data-stu-id="cda96-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="cda96-154">产品评论列表模块中有一个插槽，可在其中添加评分直方图模块。</span><span class="sxs-lookup"><span data-stu-id="cda96-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="cda96-155">下图显示如何在 Dynamics 365 Commerce 中的产品评论列表模块内添加评分直方图模块。</span><span class="sxs-lookup"><span data-stu-id="cda96-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![在产品评论列表模块中添加评分直方图模块](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="cda96-157">配置站点以显示评分和评价</span><span class="sxs-lookup"><span data-stu-id="cda96-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="cda96-158">评分或评价的配置值（如租户 ID、评论文本长度和评论标题长度）在站点级别配置。</span><span class="sxs-lookup"><span data-stu-id="cda96-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="cda96-159">若要配置站点以显示评分或评价，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cda96-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="cda96-160">转到**主 \> 站点**。</span><span class="sxs-lookup"><span data-stu-id="cda96-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="cda96-161">选择站点的名称。</span><span class="sxs-lookup"><span data-stu-id="cda96-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="cda96-162">转到**站点管理 \> 扩展性**。</span><span class="sxs-lookup"><span data-stu-id="cda96-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="cda96-163">在**评论文本最大长度**字段中，输入评论文本可包含的最大字符数（例如，**1000**）。</span><span class="sxs-lookup"><span data-stu-id="cda96-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="cda96-164">在**评论标题最大长度**字段中，输入评论标题可包含的最大字符数（例如，**55**）。</span><span class="sxs-lookup"><span data-stu-id="cda96-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="cda96-165">选择**保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="cda96-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="cda96-166">下图显示此配置在 Dynamics 365 Commerce 中的显示效果。</span><span class="sxs-lookup"><span data-stu-id="cda96-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![配置站点以显示评分和评价](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="cda96-168">将产品评分链接到 PDP 的“评论”部分</span><span class="sxs-lookup"><span data-stu-id="cda96-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="cda96-169">将在 PDP 顶部的产品标题下显示产品评分。</span><span class="sxs-lookup"><span data-stu-id="cda96-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="cda96-170">可将产品评分配置为链接到同一个 PDP 的**评论**部分。</span><span class="sxs-lookup"><span data-stu-id="cda96-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="cda96-171">若要将产品评分链接到 PDP 的**评论**部分，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cda96-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="cda96-172">打开 PDP 模板。</span><span class="sxs-lookup"><span data-stu-id="cda96-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="cda96-173">转到**购买框容器模块设置**。</span><span class="sxs-lookup"><span data-stu-id="cda96-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="cda96-174">在**购买框**下，选择**产品评分**，然后选中**链接单击以显示完整评论模块**复选框。</span><span class="sxs-lookup"><span data-stu-id="cda96-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="cda96-175">下图显示此配置在 Dynamics 365 Commerce 中的显示效果。</span><span class="sxs-lookup"><span data-stu-id="cda96-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![将产品评分链接到 PDP 的“评论”部分](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="cda96-177">配置隐私和政策页的链接</span><span class="sxs-lookup"><span data-stu-id="cda96-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="cda96-178">若要配置隐私和政策页的链接，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="cda96-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="cda96-179">转到**主 \> 站点**。</span><span class="sxs-lookup"><span data-stu-id="cda96-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="cda96-180">选择站点的名称。</span><span class="sxs-lookup"><span data-stu-id="cda96-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="cda96-181">转到**站点管理 \> 扩展性**</span><span class="sxs-lookup"><span data-stu-id="cda96-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="cda96-182">在**路由**选项卡中 **RNR 隐私和政策**下，选择**添加链接**。</span><span class="sxs-lookup"><span data-stu-id="cda96-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="cda96-183">如果已经输入了链接，但希望将其替换，请选择该链接。</span><span class="sxs-lookup"><span data-stu-id="cda96-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="cda96-184">在**添加链接**对话框中，选择隐私和政策页的链接，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="cda96-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="cda96-185">选择**保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="cda96-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="cda96-186">下图显示此配置在 Dynamics 365 Commerce 中的显示效果。</span><span class="sxs-lookup"><span data-stu-id="cda96-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![配置隐私和政策页的链接](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="cda96-188">其他资源</span><span class="sxs-lookup"><span data-stu-id="cda96-188">Additional resources</span></span>

[<span data-ttu-id="cda96-189">评分和评价概览</span><span class="sxs-lookup"><span data-stu-id="cda96-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="cda96-190">选择使用评分和评价</span><span class="sxs-lookup"><span data-stu-id="cda96-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="cda96-191">管理评分和评价</span><span class="sxs-lookup"><span data-stu-id="cda96-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="cda96-192">在 Dynamics 365 Retail 中同步产品评分</span><span class="sxs-lookup"><span data-stu-id="cda96-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
