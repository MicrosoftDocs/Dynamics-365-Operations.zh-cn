---
title: 产品详细信息页概述
description: 此主题概述 Microsoft Dynamics 365 Commerce 中的产品详细信息页 (PDP)。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697857"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="f9a02-103">产品详细信息页概述</span><span class="sxs-lookup"><span data-stu-id="f9a02-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f9a02-104">此主题概述 Microsoft Dynamics 365 Commerce 中的产品详细信息页 (PDP)。</span><span class="sxs-lookup"><span data-stu-id="f9a02-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f9a02-105">概览</span><span class="sxs-lookup"><span data-stu-id="f9a02-105">Overview</span></span>

<span data-ttu-id="f9a02-106">PDP 提供有关产品的详细信息，可供客户用于选择产品选项，如尺寸、风格和颜色。</span><span class="sxs-lookup"><span data-stu-id="f9a02-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="f9a02-107">PDP 应展示客户要做出采购决定所需全部产品信息。</span><span class="sxs-lookup"><span data-stu-id="f9a02-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="f9a02-108">下图显示 PDP 的示例。</span><span class="sxs-lookup"><span data-stu-id="f9a02-108">The following illustration shows an example of a PDP.</span></span>

![产品详细信息页示例](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="f9a02-110">标题和页脚模块</span><span class="sxs-lookup"><span data-stu-id="f9a02-110">Header and footer modules</span></span>

<span data-ttu-id="f9a02-111">PDP 顶部是显示所有产品类别的页眉和零售商希望客户浏览的其他页面。</span><span class="sxs-lookup"><span data-stu-id="f9a02-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="f9a02-112">页面底部是页脚，其中包含可能吸引客户的各主题的快速链接。</span><span class="sxs-lookup"><span data-stu-id="f9a02-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="f9a02-113">购买框模块</span><span class="sxs-lookup"><span data-stu-id="f9a02-113">Buy box module</span></span>

<span data-ttu-id="f9a02-114">PDP 中最重要的模块是购买框模块。</span><span class="sxs-lookup"><span data-stu-id="f9a02-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="f9a02-115">因此，这是页面主部分中的第一项。</span><span class="sxs-lookup"><span data-stu-id="f9a02-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="f9a02-116">购买框模块是容器模块，用于承载其中包含有关产品的最重要信息的多个模块。</span><span class="sxs-lookup"><span data-stu-id="f9a02-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="f9a02-117">这些信息包括产品名称、产品图像、描述、价格和产品评分。</span><span class="sxs-lookup"><span data-stu-id="f9a02-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="f9a02-118">客户可通过购买框模块选择产品选项（例如，尺寸、风格和颜色）和将产品添加到购物车。</span><span class="sxs-lookup"><span data-stu-id="f9a02-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="f9a02-119">还可供客户在线购买产品并在商店提货。</span><span class="sxs-lookup"><span data-stu-id="f9a02-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="f9a02-120">在线购买后店内提货模块使用与 Bing 地图应用程序编程接口 (API) 之间的集成查找附近商店或客户指定的其他位置的商店。</span><span class="sxs-lookup"><span data-stu-id="f9a02-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="f9a02-121">购买框模块需要产品 ID。</span><span class="sxs-lookup"><span data-stu-id="f9a02-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="f9a02-122">此 ID 派生自页面上下文。</span><span class="sxs-lookup"><span data-stu-id="f9a02-122">This ID is derived from the page context.</span></span> <span data-ttu-id="f9a02-123">如果向页面上下文中不包含产品 ID 的页面添加购买框模块，则不能正确显示此信息。</span><span class="sxs-lookup"><span data-stu-id="f9a02-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="f9a02-124">产品规格模块</span><span class="sxs-lookup"><span data-stu-id="f9a02-124">Product specifications module</span></span>

<span data-ttu-id="f9a02-125">产品规格模块可用于展示有关产品的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="f9a02-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="f9a02-126">这些详细信息取自 Dynamics 365 Retail 中的产品属性。</span><span class="sxs-lookup"><span data-stu-id="f9a02-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="f9a02-127">产品规格模块显示其中的**可视**属性设置为 **true** 的每个属性。</span><span class="sxs-lookup"><span data-stu-id="f9a02-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="f9a02-128">它需要产品 ID 才能检索产品属性。</span><span class="sxs-lookup"><span data-stu-id="f9a02-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="f9a02-129">建议模块</span><span class="sxs-lookup"><span data-stu-id="f9a02-129">Recommendations module</span></span>

<span data-ttu-id="f9a02-130">建议模块是 PDP 中的重要模块。</span><span class="sxs-lookup"><span data-stu-id="f9a02-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="f9a02-131">客户浏览产品时，应该会为其提供更多产品选项，以便客户找到正确的产品并进行购买。</span><span class="sxs-lookup"><span data-stu-id="f9a02-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="f9a02-132">建议可帮助客户轻松发现相关内容并继续购物。</span><span class="sxs-lookup"><span data-stu-id="f9a02-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="f9a02-133">提供了不同类型的建议列表：</span><span class="sxs-lookup"><span data-stu-id="f9a02-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="f9a02-134">**用户也喜欢**列表基于机器学习。</span><span class="sxs-lookup"><span data-stu-id="f9a02-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="f9a02-135">它使用其他客户的交易历史记录提供建议。</span><span class="sxs-lookup"><span data-stu-id="f9a02-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="f9a02-136">此列表由建议服务生成，类似“购买了此产品的客户也购买了...”列表。</span><span class="sxs-lookup"><span data-stu-id="f9a02-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="f9a02-137">需要产品 ID 才能生成此列表。</span><span class="sxs-lookup"><span data-stu-id="f9a02-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="f9a02-138">可以在 Retail 中为产品配置**相关**列表。</span><span class="sxs-lookup"><span data-stu-id="f9a02-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="f9a02-139">例如，对于棕色皮质旅行手提包，可以为相关列表配置皮质或旅行用的更多手提包。</span><span class="sxs-lookup"><span data-stu-id="f9a02-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="f9a02-140">也可以在 Retail 中配置其他类型的相关列表，如**配饰**和**更多此类产品**。</span><span class="sxs-lookup"><span data-stu-id="f9a02-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="f9a02-141">需要产品 ID 才能生成此列表。</span><span class="sxs-lookup"><span data-stu-id="f9a02-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="f9a02-142">因此，如果将其添加到主页（此处页面上下文中不包含产品 ID），则此列表为空。</span><span class="sxs-lookup"><span data-stu-id="f9a02-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="f9a02-143">可以在 PDP 中使用算法生成的建议列表，如**热门**、**最畅销**和**新品**。</span><span class="sxs-lookup"><span data-stu-id="f9a02-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="f9a02-144">虽然这些列表与 PDP 中的产品没有直接关系，也可以用于帮助客户找到感兴趣的产品。</span><span class="sxs-lookup"><span data-stu-id="f9a02-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="f9a02-145">这些类型的列表不需要产品 ID。</span><span class="sxs-lookup"><span data-stu-id="f9a02-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="f9a02-146">它们是基于站点中的购物模式生成的一般列表。</span><span class="sxs-lookup"><span data-stu-id="f9a02-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="f9a02-147">编辑列表是手动精选的列表。</span><span class="sxs-lookup"><span data-stu-id="f9a02-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="f9a02-148">例如，零售商可能决定手动挑选要展示的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="f9a02-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="f9a02-149">评分和评价模块</span><span class="sxs-lookup"><span data-stu-id="f9a02-149">Ratings and reviews module</span></span>

<span data-ttu-id="f9a02-150">评分和评价模块显示其他客户提供的评分和评价。</span><span class="sxs-lookup"><span data-stu-id="f9a02-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="f9a02-151">还可供客户撰写自己的产品评论。</span><span class="sxs-lookup"><span data-stu-id="f9a02-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="f9a02-152">此外，其中还有一个直方图，该直方图显示产品的评分趋势。</span><span class="sxs-lookup"><span data-stu-id="f9a02-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="f9a02-153">有关详细信息，请参阅[评分和评价概述](ratings-reviews-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f9a02-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="f9a02-154">市场营销模块</span><span class="sxs-lookup"><span data-stu-id="f9a02-154">Marketing modules</span></span>

<span data-ttu-id="f9a02-155">如果市场营销内容是特定产品的唯一内容，可将任何市场营销模块添加到 PDP。</span><span class="sxs-lookup"><span data-stu-id="f9a02-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="f9a02-156">可以通过“扩展”页面向 PDP 添加市场营销模块。</span><span class="sxs-lookup"><span data-stu-id="f9a02-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f9a02-157">其他资源</span><span class="sxs-lookup"><span data-stu-id="f9a02-157">Additional resources</span></span>

[<span data-ttu-id="f9a02-158">主页概览</span><span class="sxs-lookup"><span data-stu-id="f9a02-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="f9a02-159">默认类别登陆页面和搜索结果页面的概述</span><span class="sxs-lookup"><span data-stu-id="f9a02-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="f9a02-160">购物车和结帐页概述</span><span class="sxs-lookup"><span data-stu-id="f9a02-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="f9a02-161">帐户管理页概述</span><span class="sxs-lookup"><span data-stu-id="f9a02-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
