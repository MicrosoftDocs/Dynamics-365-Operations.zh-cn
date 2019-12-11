---
title: 产品集合模块
description: 此主题概述 Microsoft Dynamics 365 Commerce 中的产品集合模块。
author: v-chgri
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785459"
---
# <a name="product-collection-modules"></a><span data-ttu-id="81db9-103">产品集合模块</span><span class="sxs-lookup"><span data-stu-id="81db9-103">Product collection modules</span></span>  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="81db9-104">此主题概述 Microsoft Dynamics 365 Commerce 中的产品集合模块。</span><span class="sxs-lookup"><span data-stu-id="81db9-104">This topic provides an overview of product collection modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="81db9-105">概览</span><span class="sxs-lookup"><span data-stu-id="81db9-105">Overview</span></span>

<span data-ttu-id="81db9-106">产品发现是零售商在电子商务网站中主要用于联系客户的工具。</span><span class="sxs-lookup"><span data-stu-id="81db9-106">Product discovery is a primary tool that retailers use to engage with their customers on an e-Commerce website.</span></span> <span data-ttu-id="81db9-107">产品集合模块通过提供可用于快速创作产品集合的直观视觉界面，帮助零售商生成出色的购物体验。</span><span class="sxs-lookup"><span data-stu-id="81db9-107">Product collection modules help retailers build compelling shopping experiences by providing an intuitive visual interface that can be used to quickly author product collections.</span></span>

<span data-ttu-id="81db9-108">产品集合模块表示网站中的物理产品和服务。</span><span class="sxs-lookup"><span data-stu-id="81db9-108">Product collection modules represent physical products and services on the website.</span></span> <span data-ttu-id="81db9-109">产品集合模块通常链接到详细信息页，客户可在此页中购买产品或服务，或了解其详情。</span><span class="sxs-lookup"><span data-stu-id="81db9-109">A product collection module is typically linked to a details page where customers can purchase a product or service, or learn more about it.</span></span> 

<span data-ttu-id="81db9-110">产品集合的来源可以是三种类型的列表：</span><span class="sxs-lookup"><span data-stu-id="81db9-110">The sources for product collections can be lists of three types:</span></span>

- <span data-ttu-id="81db9-111">Dynamics 365 Retail 中手动定义为产品的相关产品的产品的编辑列表，或产品列表</span><span class="sxs-lookup"><span data-stu-id="81db9-111">Editorial lists of products that are manually defined in Dynamics 365 Retail as related products for a product, or product lists</span></span>
- <span data-ttu-id="81db9-112">算法列表，如新品列表、最畅销产品或热门产品</span><span class="sxs-lookup"><span data-stu-id="81db9-112">Algorithmic lists, such as lists of new, best-selling, or trending products</span></span>
- <span data-ttu-id="81db9-113">基于机器学习的建议列表</span><span class="sxs-lookup"><span data-stu-id="81db9-113">Recommendation lists that are based on machine learning</span></span>

<span data-ttu-id="81db9-114">下图显示电子商务站点中正在使用的不同产品集合类型。</span><span class="sxs-lookup"><span data-stu-id="81db9-114">The following illustration shows the different types of product collections being used on an e-Commerce site.</span></span>

![电子商务站点中不同产品集合类型的示例](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> <span data-ttu-id="81db9-116">始终使用产品集合模块显示相似类型或主题的一组产品。</span><span class="sxs-lookup"><span data-stu-id="81db9-116">Always use product collection modules to show a group of products of a similar type or theme.</span></span>

## <a name="product-collection-modules-and-types"></a><span data-ttu-id="81db9-117">产品集合模块和类型</span><span class="sxs-lookup"><span data-stu-id="81db9-117">Product collection modules and types</span></span>

<span data-ttu-id="81db9-118">下表介绍 Dynamics 365 Commerce 中的各种产品集合模块。</span><span class="sxs-lookup"><span data-stu-id="81db9-118">The following table describes various types of product collection modules in Dynamics 365 Commerce.</span></span>

| <span data-ttu-id="81db9-119">产品集合模块</span><span class="sxs-lookup"><span data-stu-id="81db9-119">Product collection module</span></span>  | <span data-ttu-id="81db9-120">类型</span><span class="sxs-lookup"><span data-stu-id="81db9-120">Type</span></span> | <span data-ttu-id="81db9-121">说明</span><span class="sxs-lookup"><span data-stu-id="81db9-121">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="81db9-122">类别浏览</span><span class="sxs-lookup"><span data-stu-id="81db9-122">Category browse</span></span>            | <span data-ttu-id="81db9-123">评论</span><span class="sxs-lookup"><span data-stu-id="81db9-123">Editorial</span></span> | <span data-ttu-id="81db9-124">这种产品集合模块使用零售商为零售渠道创建的导航类别层次结构显示在特定站点类别中提供的产品的浏览流程。</span><span class="sxs-lookup"><span data-stu-id="81db9-124">This type of product collection module uses the navigation category hierarchy that the retailer created for a retail channel to show a browsing flow for products that are offered in a specific site category.</span></span> |
| <span data-ttu-id="81db9-125">搜索结果</span><span class="sxs-lookup"><span data-stu-id="81db9-125">Search results</span></span>             | <span data-ttu-id="81db9-126">搜索查询</span><span class="sxs-lookup"><span data-stu-id="81db9-126">Search query</span></span> | <span data-ttu-id="81db9-127">这种产品集合模块显示最符合客户输入的搜索查询的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-127">This type of product collection module shows a list of products that best match the search query that the customer entered.</span></span> |
| <span data-ttu-id="81db9-128">相关产品</span><span class="sxs-lookup"><span data-stu-id="81db9-128">Related products</span></span>           | <span data-ttu-id="81db9-129">评论</span><span class="sxs-lookup"><span data-stu-id="81db9-129">Editorial</span></span> | <span data-ttu-id="81db9-130">这种产品集合模块显示推销经理在 Retail 中为作者选择的关系类型配置为相关产品的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-130">This type of product collection module shows a list of products that a merchandising manager has configured as related products in Retail, for the relation type that the author selected.</span></span> |
| <span data-ttu-id="81db9-131">精选产品列表</span><span class="sxs-lookup"><span data-stu-id="81db9-131">Curated product lists</span></span>      | <span data-ttu-id="81db9-132">评论</span><span class="sxs-lookup"><span data-stu-id="81db9-132">Editorial</span></span> | <span data-ttu-id="81db9-133">这种产品集合模块显示推销者和编辑者在 Retail 中创建的自定义列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-133">This type of product collection module shows custom lists that merchandisers and editors have created in Retail.</span></span> |
| <span data-ttu-id="81db9-134">全新</span><span class="sxs-lookup"><span data-stu-id="81db9-134">New</span></span>                        | <span data-ttu-id="81db9-135">算法</span><span class="sxs-lookup"><span data-stu-id="81db9-135">Algorithmic</span></span> | <span data-ttu-id="81db9-136">这种产品集合模块显示已经归类为渠道和目录的最新产品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-136">This type of product collection module shows a list of the newest products that have been assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="81db9-137">最畅销</span><span class="sxs-lookup"><span data-stu-id="81db9-137">Best selling</span></span>               | <span data-ttu-id="81db9-138">算法</span><span class="sxs-lookup"><span data-stu-id="81db9-138">Algorithmic</span></span> | <span data-ttu-id="81db9-139">这种产品集合模块显示按最大销售数排列的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-139">This type of product collection module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="81db9-140">热门</span><span class="sxs-lookup"><span data-stu-id="81db9-140">Trending</span></span>                   | <span data-ttu-id="81db9-141">算法</span><span class="sxs-lookup"><span data-stu-id="81db9-141">Algorithmic</span></span> | <span data-ttu-id="81db9-142">这种产品集合模块显示给定期间表现最出色的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-142">This type of product collection module shows a list of the highest-performing products for a given period.</span></span> |
| <span data-ttu-id="81db9-143">经常搭配购买的产品</span><span class="sxs-lookup"><span data-stu-id="81db9-143">Frequently bought together</span></span> | <span data-ttu-id="81db9-144">人工智能/机器学习</span><span class="sxs-lookup"><span data-stu-id="81db9-144">Artificial intelligence/Machine learning</span></span> | <span data-ttu-id="81db9-145">这种产品集合模块使用机器学习分析客户购买模式和推荐经常与给定产品搭配购买的相关商品。</span><span class="sxs-lookup"><span data-stu-id="81db9-145">This type of product collection module uses machine learning to analyze consumer purchase patterns and recommend related items that are frequently purchased together with a given product.</span></span> |
| <span data-ttu-id="81db9-146">人们还喜欢</span><span class="sxs-lookup"><span data-stu-id="81db9-146">People also like</span></span>           | <span data-ttu-id="81db9-147">人工智能/机器学习</span><span class="sxs-lookup"><span data-stu-id="81db9-147">Artificial intelligence/Machine learning</span></span> | <span data-ttu-id="81db9-148">这种产品集合模块使用机器学习分析客户购买模式和推荐与给定产品有关的商品。</span><span class="sxs-lookup"><span data-stu-id="81db9-148">This type of product collection module uses machine learning to analyze consumer purchase patterns and recommend items that are related to a given product.</span></span> |

## <a name="add-a-product-collection-module-to-a-category-page"></a><span data-ttu-id="81db9-149">向类别页添加产品集合模块</span><span class="sxs-lookup"><span data-stu-id="81db9-149">Add a product collection module to a category page</span></span>

<span data-ttu-id="81db9-150">若要向类别页添加产品集合模块，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="81db9-150">To add a product collection module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="81db9-151">在 Dynamics 365 Commerce 中，转到您的站点，然后创建一个与默认类别页使用同一个模板的页面。</span><span class="sxs-lookup"><span data-stu-id="81db9-151">In Dynamics 365 Commerce, go to your site, and create a page that uses the same template as your default category page.</span></span>
1. <span data-ttu-id="81db9-152">在页面大纲中，选择**子页脚**插槽，选择省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="81db9-152">In the page outline, select the **Sub footer** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="81db9-153">在**添加模块**对话框中，选择**容器**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="81db9-153">In the **Add Module** dialog box, select **Container**, and then select **OK**.</span></span>
1. <span data-ttu-id="81db9-154">在容器模块中，选择省略号按钮，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="81db9-154">In the container module, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="81db9-155">在**添加模块**对话框中，选择**产品集合**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="81db9-155">In the **Add Module** dialog box, select **Product collection**, and then select **OK**.</span></span>
1. <span data-ttu-id="81db9-156">通过为产品集合选择相应数据源和输入来配置设置。</span><span class="sxs-lookup"><span data-stu-id="81db9-156">Configure settings by selecting an appropriate data source and inputs for the product collection.</span></span>
1. <span data-ttu-id="81db9-157">在产品集合模块的属性窗格中，选择**添加产品列表**。</span><span class="sxs-lookup"><span data-stu-id="81db9-157">In the properties pane for the product collection module, select **Add a product list**.</span></span>
1. <span data-ttu-id="81db9-158">在**选择产品列表配置**对话框中，选择列表类型，输入商品数，然后选择列表类型的其他任何可用选项。</span><span class="sxs-lookup"><span data-stu-id="81db9-158">In the **Select product list configuration** dialog box, select the type of list, enter the number of items, and select any other options that are available for the list type.</span></span> <span data-ttu-id="81db9-159">有关列表类型的详细信息，请参见下表。</span><span class="sxs-lookup"><span data-stu-id="81db9-159">For more information about list types, see the table that follows.</span></span> 
1. <span data-ttu-id="81db9-160">选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="81db9-160">Select **OK**.</span></span>
1. <span data-ttu-id="81db9-161">保存页面，然后签入。</span><span class="sxs-lookup"><span data-stu-id="81db9-161">Save the page, and check it in.</span></span>

<span data-ttu-id="81db9-162">下表显示**选择产品列表配置**对话框中可供选择的列表类型。</span><span class="sxs-lookup"><span data-stu-id="81db9-162">The following table shows the list types that are available for selection in the **Select product list configuration** dialog box.</span></span>
   
| <span data-ttu-id="81db9-163">类型</span><span class="sxs-lookup"><span data-stu-id="81db9-163">Type</span></span>                       | <span data-ttu-id="81db9-164">说明</span><span class="sxs-lookup"><span data-stu-id="81db9-164">Description</span></span> | <span data-ttu-id="81db9-165">一般实践</span><span class="sxs-lookup"><span data-stu-id="81db9-165">General practice</span></span> | <span data-ttu-id="81db9-166">可从页面上下文派生的上下文</span><span class="sxs-lookup"><span data-stu-id="81db9-166">Context that can be derived from the page context</span></span> | <span data-ttu-id="81db9-167">作者可将页面上下文替换为的上下文</span><span class="sxs-lookup"><span data-stu-id="81db9-167">Context that the author can override the page context with</span></span> |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| <span data-ttu-id="81db9-168">产品(按类别)</span><span class="sxs-lookup"><span data-stu-id="81db9-168">Products by category</span></span>       | <span data-ttu-id="81db9-169">属于给定类别的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-169">A list of products that belong to a given category.</span></span> <span data-ttu-id="81db9-170">通过页面上下文或作者提供的上下文确定此类别。</span><span class="sxs-lookup"><span data-stu-id="81db9-170">This category is determined from either the page context or the context that the author provides.</span></span> | <span data-ttu-id="81db9-171">扩充类别页、主页、结帐与购物车页，以及产品页</span><span class="sxs-lookup"><span data-stu-id="81db9-171">Enrich category page, home page, checkout and cart pages, and product pages</span></span> | <span data-ttu-id="81db9-172">类别</span><span class="sxs-lookup"><span data-stu-id="81db9-172">Category</span></span> | <span data-ttu-id="81db9-173">作者决定的类别</span><span class="sxs-lookup"><span data-stu-id="81db9-173">Category determined by author</span></span> |
| <span data-ttu-id="81db9-174">相关产品</span><span class="sxs-lookup"><span data-stu-id="81db9-174">Related products</span></span>           | <span data-ttu-id="81db9-175">推销经理已在 Retail 中为关系类型配置为相关产品的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-175">A list of products that a merchandising manager has configured as related products in Retail for the relation type.</span></span> | <span data-ttu-id="81db9-176">产品页、结帐与购物车页，愿望列表页和客户帐户页</span><span class="sxs-lookup"><span data-stu-id="81db9-176">Product pages, checkout and cart pages, wish list page, and customer account page</span></span> | <span data-ttu-id="81db9-177">产品、关系类型（必需）</span><span class="sxs-lookup"><span data-stu-id="81db9-177">Product, Relation type (Mandatory)</span></span>  | <span data-ttu-id="81db9-178">产品、关系类型</span><span class="sxs-lookup"><span data-stu-id="81db9-178">Product, Relation type</span></span> |
| <span data-ttu-id="81db9-179">策划</span><span class="sxs-lookup"><span data-stu-id="81db9-179">Curated</span></span>                    | <span data-ttu-id="81db9-180">推销者和编辑者已在 Retail 中创建的自定义列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-180">A custom list that merchandisers and editors have created in Retail.</span></span> | <span data-ttu-id="81db9-181">扩充类别页、主页、结帐与购物车页，以及产品页</span><span class="sxs-lookup"><span data-stu-id="81db9-181">Enrich category page, home page, checkout and cart pages, and product pages</span></span> | <span data-ttu-id="81db9-182">不适用</span><span class="sxs-lookup"><span data-stu-id="81db9-182">Not applicable</span></span> | <span data-ttu-id="81db9-183">列表选择器</span><span class="sxs-lookup"><span data-stu-id="81db9-183">List picker</span></span> |
| <span data-ttu-id="81db9-184">算法</span><span class="sxs-lookup"><span data-stu-id="81db9-184">Algorithmic</span></span>                | <ul><li><span data-ttu-id="81db9-185">**新商品** – 已经分类为渠道和目录的最新产品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-185">**New** – A list of the newest products that have been assorted to channels and catalogs.</span></span></li><li><span data-ttu-id="81db9-186">**最畅销** – 按销售数最高排名的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-186">**Best-selling** – A list of products that are ranked by the highest number of sales.</span></span></li><li><span data-ttu-id="81db9-187">**热门** – 给定期间表现最出色的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-187">**Trending** – A list of the highest-performing products for a given period.</span></span></li></ul> | <span data-ttu-id="81db9-188">主页、扩展类别页和结帐与购物车页</span><span class="sxs-lookup"><span data-stu-id="81db9-188">Home page, enrich category page, and checkout and cart pages</span></span> | <span data-ttu-id="81db9-189">类别</span><span class="sxs-lookup"><span data-stu-id="81db9-189">Category</span></span> | <span data-ttu-id="81db9-190">作者决定的类别</span><span class="sxs-lookup"><span data-stu-id="81db9-190">Category determined by author</span></span> |
| <span data-ttu-id="81db9-191">经常搭配购买的产品</span><span class="sxs-lookup"><span data-stu-id="81db9-191">Frequently bought together</span></span> | <span data-ttu-id="81db9-192">使用机器学习分析客户购买模式和推荐经常与给定产品搭配购买的相关商品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-192">A list that uses machine learning to analyze consumer purchase patterns and recommend related items that are frequently purchased together with a given product.</span></span> | <span data-ttu-id="81db9-193">产品页和结帐与购物车页</span><span class="sxs-lookup"><span data-stu-id="81db9-193">Product pages, and checkout and cart pages</span></span> | <span data-ttu-id="81db9-194">产品、购物车</span><span class="sxs-lookup"><span data-stu-id="81db9-194">Product, Cart</span></span> | <span data-ttu-id="81db9-195">包括购物车</span><span class="sxs-lookup"><span data-stu-id="81db9-195">Include cart</span></span> |
| <span data-ttu-id="81db9-196">人们还喜欢</span><span class="sxs-lookup"><span data-stu-id="81db9-196">People also like</span></span>           | <span data-ttu-id="81db9-197">使用机器学习分析客户购买模式和推荐与给定产品有关的商品的列表。</span><span class="sxs-lookup"><span data-stu-id="81db9-197">A list that uses machine learning to analyze consumer purchase patterns and recommend items that are related to a given product.</span></span> | <span data-ttu-id="81db9-198">产品页和结帐与购物车页</span><span class="sxs-lookup"><span data-stu-id="81db9-198">Product pages, and checkout and cart pages</span></span> | <span data-ttu-id="81db9-199">产品、购物车</span><span class="sxs-lookup"><span data-stu-id="81db9-199">Product, Cart</span></span> | <span data-ttu-id="81db9-200">不适用</span><span class="sxs-lookup"><span data-stu-id="81db9-200">Not applicable</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="81db9-201">其他资源</span><span class="sxs-lookup"><span data-stu-id="81db9-201">Additional resources</span></span>

[<span data-ttu-id="81db9-202">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="81db9-202">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="81db9-203">传送模块</span><span class="sxs-lookup"><span data-stu-id="81db9-203">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="81db9-204">内容丰富块模块</span><span class="sxs-lookup"><span data-stu-id="81db9-204">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="81db9-205">内容放置模块</span><span class="sxs-lookup"><span data-stu-id="81db9-205">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="81db9-206">容器模块</span><span class="sxs-lookup"><span data-stu-id="81db9-206">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="81db9-207">购买框模块</span><span class="sxs-lookup"><span data-stu-id="81db9-207">Buy box module</span></span>](add-buy-box.md)

