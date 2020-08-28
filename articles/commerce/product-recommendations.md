---
title: 产品建议概览
description: 本主题提供有关产品建议的一般信息。 客户可通过产品建议轻松、快速地找到所需产品，甚至找到最初不打算购买的产品。
author: Moonma
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5aa7db8e53906f9e1416b912fe2c3b70d5430258
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664874"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="d2f80-104">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="d2f80-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2f80-105">Microsoft Dynamics 365 Commerce 可用于在电子商务网站和销售点 (POS) 设备上显示产品建议。</span><span class="sxs-lookup"><span data-stu-id="d2f80-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="d2f80-106">产品建议是客户可能感兴趣的项。</span><span class="sxs-lookup"><span data-stu-id="d2f80-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="d2f80-107">建议基于其他客户在在线商店和实体商店中的购买趋势。</span><span class="sxs-lookup"><span data-stu-id="d2f80-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="d2f80-108">客户可通过产品建议轻松、快速地找到所需产品，同时享受良好的服务体验。</span><span class="sxs-lookup"><span data-stu-id="d2f80-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="d2f80-109">甚至可使用交叉销售和向上销售帮助客户找到甚至最初不打算购买的更多产品。</span><span class="sxs-lookup"><span data-stu-id="d2f80-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="d2f80-110">使用建议增强产品发现时，可以产生更多转化商机，帮助提高销售利润，甚至帮助加强客户满意度和保留。</span><span class="sxs-lookup"><span data-stu-id="d2f80-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="d2f80-111">在电子商务中，Microsoft Recommendations 机器学习技术大幅助力产品建议。</span><span class="sxs-lookup"><span data-stu-id="d2f80-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="d2f80-112">建议服务</span><span class="sxs-lookup"><span data-stu-id="d2f80-112">Recommendation service</span></span>

<span data-ttu-id="d2f80-113">产品建议服务按照以下方式使用人工智能和机器学习 (AI-ML) 技术：</span><span class="sxs-lookup"><span data-stu-id="d2f80-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="d2f80-114">从 Commerce 操作数据库提取建议服务所需格式的数据并发送到 Azure Data Lake Storage 或实体商店。</span><span class="sxs-lookup"><span data-stu-id="d2f80-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="d2f80-115">建议服务使用存储的数据培训**用户也喜欢**、**人气组合**、**新品**、**最畅销**和**热门**列表的建议模型。</span><span class="sxs-lookup"><span data-stu-id="d2f80-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="d2f80-116">方案</span><span class="sxs-lookup"><span data-stu-id="d2f80-116">Scenarios</span></span>

<span data-ttu-id="d2f80-117">以下方案支持产品建议：</span><span class="sxs-lookup"><span data-stu-id="d2f80-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="d2f80-118">**在电子商务中用于浏览或登录页面的任何商店页面上：** 如果客户或商店助理访问某个商店页面，建议引擎可在**新品**、**最畅销**和**热门**列表中推荐产品。</span><span class="sxs-lookup"><span data-stu-id="d2f80-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="d2f80-119">**在“产品详细信息”页中：** 如果客户或商店助理访问**产品详细信息**页，建议引擎将推荐也可能购买的更多商品。</span><span class="sxs-lookup"><span data-stu-id="d2f80-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="d2f80-120">这些商品在**用户也喜欢**列表中显示。</span><span class="sxs-lookup"><span data-stu-id="d2f80-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="d2f80-121">**在“交易记录”页或结帐页中：** 建议引擎基于购物篮中的完整商品列表推荐商品。</span><span class="sxs-lookup"><span data-stu-id="d2f80-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="d2f80-122">这些商品在**人气组合**列表中显示。</span><span class="sxs-lookup"><span data-stu-id="d2f80-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="d2f80-123">**个性化建议：** 商品交易商可以为登录客户提供个性化的**为您推荐**列表，以及新功能，从而允许根据该客户对现有列表方案进行个性化设置。</span><span class="sxs-lookup"><span data-stu-id="d2f80-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="d2f80-124">若要了解详细信息，请参阅[启用个性化建议](personalized-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="d2f80-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="d2f80-125">产品建议的类型</span><span class="sxs-lookup"><span data-stu-id="d2f80-125">Types of product recommendations</span></span>

<span data-ttu-id="d2f80-126">下表介绍可供零售商在其 Dynamics 365 Commerce 解决方案中通过[产品收集模块](product-collection-module-overview.md)实施的各种自动化产品建议。</span><span class="sxs-lookup"><span data-stu-id="d2f80-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="d2f80-127">零售商还可以为登录用户显示个性化结果（如果站点作者选择该选项）。</span><span class="sxs-lookup"><span data-stu-id="d2f80-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="d2f80-128">产品集合模块</span><span class="sxs-lookup"><span data-stu-id="d2f80-128">Product collection module</span></span>  | <span data-ttu-id="d2f80-129">类型</span><span class="sxs-lookup"><span data-stu-id="d2f80-129">Type</span></span> | <span data-ttu-id="d2f80-130">说明</span><span class="sxs-lookup"><span data-stu-id="d2f80-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="d2f80-131">全新</span><span class="sxs-lookup"><span data-stu-id="d2f80-131">New</span></span>                        | <span data-ttu-id="d2f80-132">算法</span><span class="sxs-lookup"><span data-stu-id="d2f80-132">Algorithmic</span></span> | <span data-ttu-id="d2f80-133">此模块显示最近已经分类为渠道和目录的最新产品的列表。</span><span class="sxs-lookup"><span data-stu-id="d2f80-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="d2f80-134">最畅销</span><span class="sxs-lookup"><span data-stu-id="d2f80-134">Best selling</span></span>               | <span data-ttu-id="d2f80-135">算法</span><span class="sxs-lookup"><span data-stu-id="d2f80-135">Algorithmic</span></span> | <span data-ttu-id="d2f80-136">此模块显示按销售数最高排名的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="d2f80-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="d2f80-137">热门</span><span class="sxs-lookup"><span data-stu-id="d2f80-137">Trending</span></span>                   | <span data-ttu-id="d2f80-138">算法</span><span class="sxs-lookup"><span data-stu-id="d2f80-138">Algorithmic</span></span> | <span data-ttu-id="d2f80-139">此模块显示给定期间表现最出色的产品的列表，并按最高销售数排名。</span><span class="sxs-lookup"><span data-stu-id="d2f80-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="d2f80-140">经常搭配购买的产品</span><span class="sxs-lookup"><span data-stu-id="d2f80-140">Frequently bought together</span></span> | <span data-ttu-id="d2f80-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="d2f80-141">AI-ML</span></span> | <span data-ttu-id="d2f80-142">此模块推荐通常与客户的当前购物车内容一起购买的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="d2f80-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="d2f80-143">人们还喜欢</span><span class="sxs-lookup"><span data-stu-id="d2f80-143">People also like</span></span>           | <span data-ttu-id="d2f80-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="d2f80-144">AI-ML</span></span> | <span data-ttu-id="d2f80-145">此模块根据消费者购物模式为给定种子产品推荐产品。</span><span class="sxs-lookup"><span data-stu-id="d2f80-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="d2f80-146">为您推荐</span><span class="sxs-lookup"><span data-stu-id="d2f80-146">Picks for you</span></span>              | <span data-ttu-id="d2f80-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="d2f80-147">AI-ML</span></span> | <span data-ttu-id="d2f80-148">此模块根据已登录用户的购买模式推荐个性化的产品列表。</span><span class="sxs-lookup"><span data-stu-id="d2f80-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="d2f80-149">对于来宾用户，此列表将被折叠。</span><span class="sxs-lookup"><span data-stu-id="d2f80-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="d2f80-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="d2f80-150">Additional resources</span></span>

[<span data-ttu-id="d2f80-151">在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="d2f80-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="d2f80-152">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="d2f80-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d2f80-153">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="d2f80-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="d2f80-154">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="d2f80-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d2f80-155">启用“购买类似外观”建议</span><span class="sxs-lookup"><span data-stu-id="d2f80-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="d2f80-156">在 POS 上添加产品建议</span><span class="sxs-lookup"><span data-stu-id="d2f80-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="d2f80-157">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="d2f80-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d2f80-158">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="d2f80-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="d2f80-159">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="d2f80-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="d2f80-160">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="d2f80-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="d2f80-161">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="d2f80-161">Product recommendations FAQ</span></span>](faq-recommendations.md)
