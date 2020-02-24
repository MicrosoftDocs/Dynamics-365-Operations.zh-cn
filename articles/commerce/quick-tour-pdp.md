---
title: 产品详细信息页概述
description: 此主题概述 Microsoft Dynamics 365 Commerce 中的产品详细信息页 (PDP)。
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: dbf8f4c1ea479a508f4a0294020b7201b32fe228
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025917"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="ce47a-103">产品详细信息页概述</span><span class="sxs-lookup"><span data-stu-id="ce47a-103">Overview of product details pages</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ce47a-104">此主题概述 Microsoft Dynamics 365 Commerce 中的产品详细信息页 (PDP)。</span><span class="sxs-lookup"><span data-stu-id="ce47a-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ce47a-105">概览</span><span class="sxs-lookup"><span data-stu-id="ce47a-105">Overview</span></span>

<span data-ttu-id="ce47a-106">PDP 提供有关产品的详细信息，可供客户用于选择产品选项，如尺寸、风格和颜色。</span><span class="sxs-lookup"><span data-stu-id="ce47a-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="ce47a-107">PDP 应展示客户要做出采购决定所需全部产品信息。</span><span class="sxs-lookup"><span data-stu-id="ce47a-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="ce47a-108">下图显示 PDP 的示例。</span><span class="sxs-lookup"><span data-stu-id="ce47a-108">The following illustration shows an example of a PDP.</span></span>

![产品详细信息页示例](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="ce47a-110">标题和页脚模块</span><span class="sxs-lookup"><span data-stu-id="ce47a-110">Header and footer modules</span></span>

<span data-ttu-id="ce47a-111">PDP 顶部是显示所有产品类别的页眉和零售商希望客户浏览的其他页面。</span><span class="sxs-lookup"><span data-stu-id="ce47a-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="ce47a-112">页面底部是页脚，其中包含可能吸引客户的各主题的快速链接。</span><span class="sxs-lookup"><span data-stu-id="ce47a-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="ce47a-113">购买框模块</span><span class="sxs-lookup"><span data-stu-id="ce47a-113">Buy box module</span></span>

<span data-ttu-id="ce47a-114">PDP 上最重要的模块是购买框模块，它在页面主要部分中显示为第一项。</span><span class="sxs-lookup"><span data-stu-id="ce47a-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="ce47a-115">购买框模块显示重要的产品信息，例如产品名称、产品描述、产品价格、产品图像和产品等级。</span><span class="sxs-lookup"><span data-stu-id="ce47a-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="ce47a-116">客户可通过购买框模块选择产品选项（例如，尺寸、风格和颜色）和将产品添加到购物车。</span><span class="sxs-lookup"><span data-stu-id="ce47a-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="ce47a-117">还可供客户在线购买产品并在商店提货。</span><span class="sxs-lookup"><span data-stu-id="ce47a-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="ce47a-118">在线购买后店内提货模块使用与 Bing 地图应用程序编程接口 (API) 之间的集成查找附近商店或客户指定的其他位置的商店。</span><span class="sxs-lookup"><span data-stu-id="ce47a-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="ce47a-119">购买框模块需要产品 ID。</span><span class="sxs-lookup"><span data-stu-id="ce47a-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="ce47a-120">此 ID 派生自页面上下文。</span><span class="sxs-lookup"><span data-stu-id="ce47a-120">This ID is derived from the page context.</span></span> <span data-ttu-id="ce47a-121">如果向页面上下文中不包含产品 ID 的页面添加购买框模块，则不能正确显示此信息。</span><span class="sxs-lookup"><span data-stu-id="ce47a-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="ce47a-122">产品规格模块</span><span class="sxs-lookup"><span data-stu-id="ce47a-122">Product specifications module</span></span>

<span data-ttu-id="ce47a-123">产品规格模块可用于展示有关产品的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="ce47a-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="ce47a-124">这些详细信息取自 Commerce 中的产品属性。</span><span class="sxs-lookup"><span data-stu-id="ce47a-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="ce47a-125">产品规格模块显示其中的**可视**属性设置为 **true** 的每个属性。</span><span class="sxs-lookup"><span data-stu-id="ce47a-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="ce47a-126">它需要产品 ID 才能检索产品属性。</span><span class="sxs-lookup"><span data-stu-id="ce47a-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="ce47a-127">建议模块</span><span class="sxs-lookup"><span data-stu-id="ce47a-127">Recommendations module</span></span>

<span data-ttu-id="ce47a-128">建议模块是 PDP 中的重要模块。</span><span class="sxs-lookup"><span data-stu-id="ce47a-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="ce47a-129">客户浏览产品时，应该会为其提供更多产品选项，以便客户找到正确的产品并进行购买。</span><span class="sxs-lookup"><span data-stu-id="ce47a-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="ce47a-130">建议可帮助客户轻松发现相关内容并继续购物。</span><span class="sxs-lookup"><span data-stu-id="ce47a-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="ce47a-131">提供了不同类型的建议列表：</span><span class="sxs-lookup"><span data-stu-id="ce47a-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="ce47a-132">**用户也喜欢**列表基于机器学习。</span><span class="sxs-lookup"><span data-stu-id="ce47a-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="ce47a-133">它使用其他客户的交易历史记录提供建议。</span><span class="sxs-lookup"><span data-stu-id="ce47a-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="ce47a-134">此列表由建议服务生成，类似“购买了此产品的客户也购买了...”列表。</span><span class="sxs-lookup"><span data-stu-id="ce47a-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="ce47a-135">需要产品 ID 才能生成此列表。</span><span class="sxs-lookup"><span data-stu-id="ce47a-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="ce47a-136">可以在 Commerce 中为产品配置**相关**列表。</span><span class="sxs-lookup"><span data-stu-id="ce47a-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="ce47a-137">例如，对于棕色皮质旅行手提包，可以为相关列表配置皮质或旅行用的更多手提包。</span><span class="sxs-lookup"><span data-stu-id="ce47a-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="ce47a-138">也可以在 Commerce 中配置其他类型的相关列表，如**配饰**和**更多此类产品**。</span><span class="sxs-lookup"><span data-stu-id="ce47a-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="ce47a-139">需要产品 ID 才能生成此列表。</span><span class="sxs-lookup"><span data-stu-id="ce47a-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="ce47a-140">因此，如果将其添加到主页（此处页面上下文中不包含产品 ID），则此列表为空。</span><span class="sxs-lookup"><span data-stu-id="ce47a-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="ce47a-141">可以在 PDP 中使用算法生成的建议列表，如**热门**、**最畅销**和**新品**。</span><span class="sxs-lookup"><span data-stu-id="ce47a-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="ce47a-142">虽然这些列表与 PDP 中的产品没有直接关系，也可以用于帮助客户找到感兴趣的产品。</span><span class="sxs-lookup"><span data-stu-id="ce47a-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="ce47a-143">这些类型的列表不需要产品 ID。</span><span class="sxs-lookup"><span data-stu-id="ce47a-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="ce47a-144">它们是基于站点中的购物模式生成的一般列表。</span><span class="sxs-lookup"><span data-stu-id="ce47a-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="ce47a-145">编辑列表是手动精选的列表。</span><span class="sxs-lookup"><span data-stu-id="ce47a-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="ce47a-146">例如，零售商可能决定手动挑选要展示的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="ce47a-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="ce47a-147">评分和评价模块</span><span class="sxs-lookup"><span data-stu-id="ce47a-147">Ratings and reviews modules</span></span>

<span data-ttu-id="ce47a-148">可以使用三个模块来显示和添加评论：</span><span class="sxs-lookup"><span data-stu-id="ce47a-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="ce47a-149">**评价** – 此模块列出其他客户提供的评分和评价。</span><span class="sxs-lookup"><span data-stu-id="ce47a-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="ce47a-150">客户可以对评价进行排序和筛选。</span><span class="sxs-lookup"><span data-stu-id="ce47a-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="ce47a-151">该模块还使客户可以对评价表示喜欢或不喜欢，并报告问题。</span><span class="sxs-lookup"><span data-stu-id="ce47a-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="ce47a-152">**写评价** – 该模块使客户可以编写自己的产品评价。</span><span class="sxs-lookup"><span data-stu-id="ce47a-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="ce47a-153">**评级直方图** – 此模块包括一个直方图，该直方图显示了产品的评级趋势。</span><span class="sxs-lookup"><span data-stu-id="ce47a-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="ce47a-154">有关详细信息，请参阅[评分和评价概述](ratings-reviews-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="ce47a-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="ce47a-155">市场营销模块</span><span class="sxs-lookup"><span data-stu-id="ce47a-155">Marketing modules</span></span>

<span data-ttu-id="ce47a-156">如果市场营销内容是特定产品的唯一内容，可将任何市场营销模块添加到 PDP。</span><span class="sxs-lookup"><span data-stu-id="ce47a-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="ce47a-157">可以通过“扩展”页面向 PDP 添加市场营销模块。</span><span class="sxs-lookup"><span data-stu-id="ce47a-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="ce47a-158">有关更多详细信息，请参见[丰富产品页面](enrich-product-page.md)。</span><span class="sxs-lookup"><span data-stu-id="ce47a-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce47a-159">其他资源</span><span class="sxs-lookup"><span data-stu-id="ce47a-159">Additional resources</span></span>

[<span data-ttu-id="ce47a-160">主页概览</span><span class="sxs-lookup"><span data-stu-id="ce47a-160">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="ce47a-161">默认类别登陆页面和搜索结果页面概览</span><span class="sxs-lookup"><span data-stu-id="ce47a-161">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="ce47a-162">购物车和结账页面概览</span><span class="sxs-lookup"><span data-stu-id="ce47a-162">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="ce47a-163">帐户管理页概述</span><span class="sxs-lookup"><span data-stu-id="ce47a-163">Overview of account management pages</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="ce47a-164">丰富产品详细信息页面</span><span class="sxs-lookup"><span data-stu-id="ce47a-164">Enrich a product details page</span></span>](enrich-product-page.md)
