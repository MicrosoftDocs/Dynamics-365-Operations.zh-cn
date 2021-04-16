---
title: 默认类别登陆页面和搜索结果页面概览
description: 此主题概述 Dynamics 365 Commerce 中的默认类别登陆页和搜索结果页。
author: ashishmsft
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f380f3f56727d927d7cd328fef3c9d999afa2873
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794341"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a><span data-ttu-id="46b13-103">默认类别登陆页面和搜索结果页面概览</span><span class="sxs-lookup"><span data-stu-id="46b13-103">Default category landing page and search results page overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46b13-104">此主题概述 Microsoft Dynamics 365 Commerce 电子商务中的默认类别登陆页和搜索结果页。</span><span class="sxs-lookup"><span data-stu-id="46b13-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="46b13-105">默认类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="46b13-105">Default category landing page</span></span>

<span data-ttu-id="46b13-106">默认类别登陆页是网站用户选择导航层次结构中的类别时将把他们带到的页面。</span><span class="sxs-lookup"><span data-stu-id="46b13-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="46b13-107">类别页用于浏览，也可以对已分类产品进行排序和优化。</span><span class="sxs-lookup"><span data-stu-id="46b13-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![默认类别登陆页面](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="46b13-109">页面顶部是显示所有产品类别的页眉和促销经理已分类的其他页面。</span><span class="sxs-lookup"><span data-stu-id="46b13-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="46b13-110">配置渠道导航层次结构时进行配置。</span><span class="sxs-lookup"><span data-stu-id="46b13-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="46b13-111">页面底部是页脚，其中包含购物者可能感兴趣的各主题的快速链接。</span><span class="sxs-lookup"><span data-stu-id="46b13-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="46b13-112">以下组件对类别至关重要：</span><span class="sxs-lookup"><span data-stu-id="46b13-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="46b13-113">**产品放置磁贴** 显示配置导航层次结构时促销经理定义的产品。</span><span class="sxs-lookup"><span data-stu-id="46b13-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="46b13-114">**优化器和选项摘要** 是提供计数且可用于优化项的筛选器。</span><span class="sxs-lookup"><span data-stu-id="46b13-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="46b13-115">配置与渠道类别和产品属性有关的元数据时，促销经理配置这些。</span><span class="sxs-lookup"><span data-stu-id="46b13-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="46b13-116">网站访问者使用 **排序选项** 对产品排序。</span><span class="sxs-lookup"><span data-stu-id="46b13-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="46b13-117">默认情况下，可使用以下排序选项：</span><span class="sxs-lookup"><span data-stu-id="46b13-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="46b13-118">价格 – 从低到高</span><span class="sxs-lookup"><span data-stu-id="46b13-118">Price – low to high</span></span>
    - <span data-ttu-id="46b13-119">价格 – 从高到低</span><span class="sxs-lookup"><span data-stu-id="46b13-119">Price – high to low</span></span>
    - <span data-ttu-id="46b13-120">产品名称 – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="46b13-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="46b13-121">产品名称 – \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="46b13-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="46b13-122">评分 – 从低到高</span><span class="sxs-lookup"><span data-stu-id="46b13-122">Ratings – low to high</span></span>
    - <span data-ttu-id="46b13-123">评分 – 从高到低</span><span class="sxs-lookup"><span data-stu-id="46b13-123">Ratings – high to low</span></span>

- <span data-ttu-id="46b13-124">网站访问者可使用 **分页** 从一页已分类产品结果移到另一页。</span><span class="sxs-lookup"><span data-stu-id="46b13-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="46b13-125">**总计数** 提供类别中定义的产品总数。</span><span class="sxs-lookup"><span data-stu-id="46b13-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="46b13-126">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="46b13-126">Enrich a category landing page</span></span>

<span data-ttu-id="46b13-127">如果希望类别登陆页中包含特定类别定制程度更深的体验，可以“扩充”该类别的类别登陆页。</span><span class="sxs-lookup"><span data-stu-id="46b13-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="46b13-128">例如，可添加市场营销视频和某些类别故事分享吸引购物者的注意。</span><span class="sxs-lookup"><span data-stu-id="46b13-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="46b13-129">有关详细信息，请参阅[扩充类别登陆页](enrich-category-page.md)。</span><span class="sxs-lookup"><span data-stu-id="46b13-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![扩充的类别登陆页面](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="46b13-131">自动建议和搜索结果页</span><span class="sxs-lookup"><span data-stu-id="46b13-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="46b13-132">网站用户可通过从导航层次结构转到类别或通过在搜索字段中输入搜索词，浏览站点。</span><span class="sxs-lookup"><span data-stu-id="46b13-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="46b13-133">只要用户开始在搜索字段中键入，就可以体验沉浸式自动建议功能以建议搜索词。</span><span class="sxs-lookup"><span data-stu-id="46b13-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="46b13-134">下面是可以显示的一些建议类型：</span><span class="sxs-lookup"><span data-stu-id="46b13-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="46b13-135">**关键字** 用于在所有产品中查找归类为渠道的项。</span><span class="sxs-lookup"><span data-stu-id="46b13-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="46b13-136">**产品** 提供产品详细信息页的直接链接。</span><span class="sxs-lookup"><span data-stu-id="46b13-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="46b13-137">**作用域类别搜索建议** 列举各类别，可供用户在特定类别中搜索关键字。</span><span class="sxs-lookup"><span data-stu-id="46b13-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![沉浸式自动建议](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="46b13-139">当用户选择一个关键字或作用域类别搜索建议时，或当没有所输入搜索词的建议时，将把用户重定向到搜索结果页。</span><span class="sxs-lookup"><span data-stu-id="46b13-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="46b13-140">然后，用户可浏览、排序和优化搜索结果列以查找所需项。</span><span class="sxs-lookup"><span data-stu-id="46b13-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![搜索登录](./media/SearchLanding.png)

<span data-ttu-id="46b13-142">以下组件对搜索结果页至关重要：</span><span class="sxs-lookup"><span data-stu-id="46b13-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="46b13-143">**产品放置磁贴** 显示用户搜索的产品。</span><span class="sxs-lookup"><span data-stu-id="46b13-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="46b13-144">默认情况下，这些磁贴按用户搜索的云助力搜索相关性分数排序。</span><span class="sxs-lookup"><span data-stu-id="46b13-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="46b13-145">**优化器和选项摘要** 是提供计数且可用于优化项的筛选器。</span><span class="sxs-lookup"><span data-stu-id="46b13-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="46b13-146">配置“渠道类别和产品属性”元数据时，促销经理配置这些。</span><span class="sxs-lookup"><span data-stu-id="46b13-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="46b13-147">网站访问者使用 **排序选项** 对产品排序。</span><span class="sxs-lookup"><span data-stu-id="46b13-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="46b13-148">默认情况下，可使用以下排序选项：</span><span class="sxs-lookup"><span data-stu-id="46b13-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="46b13-149">价格 – 从低到高</span><span class="sxs-lookup"><span data-stu-id="46b13-149">Price – low to high</span></span>
    - <span data-ttu-id="46b13-150">价格 – 从高到低</span><span class="sxs-lookup"><span data-stu-id="46b13-150">Price – high to low</span></span>
    - <span data-ttu-id="46b13-151">产品名称 – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="46b13-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="46b13-152">产品名称 – \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="46b13-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="46b13-153">评分 – 从低到高</span><span class="sxs-lookup"><span data-stu-id="46b13-153">Ratings – low to high</span></span>
    - <span data-ttu-id="46b13-154">评分 – 从高到低</span><span class="sxs-lookup"><span data-stu-id="46b13-154">Ratings – high to low</span></span>
    - <span data-ttu-id="46b13-155">默认</span><span class="sxs-lookup"><span data-stu-id="46b13-155">Default</span></span>

- <span data-ttu-id="46b13-156">网站访问者可使用 **分页** 从一页已分类产品结果移到另一页。</span><span class="sxs-lookup"><span data-stu-id="46b13-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="46b13-157">**总计数** 提供类别中定义且与搜索条件匹配的产品的总数。</span><span class="sxs-lookup"><span data-stu-id="46b13-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

>[!NOTE]
><span data-ttu-id="46b13-158">从版本 10.0.8 开始可使用这些云助力的搜索功能。</span><span class="sxs-lookup"><span data-stu-id="46b13-158">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="46b13-159">确保 **Commerce 参数 > 配置参数** 下有一个条目是“ProductSearch.UseAzureSearch 设置为 true”。</span><span class="sxs-lookup"><span data-stu-id="46b13-159">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="46b13-160">![云助力搜索的配置参数](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="46b13-160">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46b13-161">其他资源</span><span class="sxs-lookup"><span data-stu-id="46b13-161">Additional resources</span></span>

[<span data-ttu-id="46b13-162">云助力的搜索概览</span><span class="sxs-lookup"><span data-stu-id="46b13-162">Cloud-powered search overview</span></span>](cloud-powered-search-overview.md)

[<span data-ttu-id="46b13-163">主页概览</span><span class="sxs-lookup"><span data-stu-id="46b13-163">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="46b13-164">产品详细信息页面概览</span><span class="sxs-lookup"><span data-stu-id="46b13-164">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="46b13-165">购物车和结账页面概览</span><span class="sxs-lookup"><span data-stu-id="46b13-165">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="46b13-166">帐户管理页面概览</span><span class="sxs-lookup"><span data-stu-id="46b13-166">Account management pages overview</span></span>](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]