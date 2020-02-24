---
title: 产品建议概览
description: 本主题提供有关产品建议的一般信息。 客户可通过产品建议轻松、快速地找到所需产品，甚至找到最初不打算购买的产品。
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024971"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="6a34a-104">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="6a34a-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6a34a-105">Microsoft Dynamics 365 Commerce 可用于在电子商务网站和销售点 (POS) 设备上显示产品建议。</span><span class="sxs-lookup"><span data-stu-id="6a34a-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="6a34a-106">产品建议是客户可能感兴趣的项。</span><span class="sxs-lookup"><span data-stu-id="6a34a-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="6a34a-107">建议基于其他客户在在线商店和实体商店中的购买趋势。</span><span class="sxs-lookup"><span data-stu-id="6a34a-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="6a34a-108">客户可通过产品建议轻松、快速地找到所需产品，同时享受良好的服务体验。</span><span class="sxs-lookup"><span data-stu-id="6a34a-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="6a34a-109">甚至可使用交叉销售和向上销售帮助客户找到甚至最初不打算购买的更多产品。</span><span class="sxs-lookup"><span data-stu-id="6a34a-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="6a34a-110">使用建议帮助发现产品时，可以产生更多转化商机，帮助提高销售利润，甚至帮助加强客户满意度和保留。</span><span class="sxs-lookup"><span data-stu-id="6a34a-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="6a34a-111">在 Commerce 中，Microsoft Recommendations 机器学习技术大幅助力产品建议。</span><span class="sxs-lookup"><span data-stu-id="6a34a-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="6a34a-112">方案</span><span class="sxs-lookup"><span data-stu-id="6a34a-112">Scenarios</span></span>

<span data-ttu-id="6a34a-113">以下方案支持产品建议：</span><span class="sxs-lookup"><span data-stu-id="6a34a-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="6a34a-114">**在电子商务中用于浏览或登录页面的任何商店页面上：** 如果客户或商店助理访问某个商店页面，建议引擎可在**新品**、**最畅销**和**热门**列表中推荐产品。</span><span class="sxs-lookup"><span data-stu-id="6a34a-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="6a34a-115">**在“产品详细信息”页中：** 如果客户或商店助理访问**产品详细信息**页，建议引擎将推荐也可能购买的更多商品。</span><span class="sxs-lookup"><span data-stu-id="6a34a-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="6a34a-116">这些商品在**用户也喜欢**列表中显示。</span><span class="sxs-lookup"><span data-stu-id="6a34a-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="6a34a-117">**在“交易记录”页或结帐页中：** 建议引擎基于购物篮中的完整商品列表推荐商品。</span><span class="sxs-lookup"><span data-stu-id="6a34a-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="6a34a-118">这些商品在**人气组合**列表中显示。</span><span class="sxs-lookup"><span data-stu-id="6a34a-118">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="6a34a-119">**个性化建议：** 商品交易商可以为登录客户提供个性化的**为您推荐**列表，以及新功能，从而允许根据该客户对现有列表方案进行个性化设置。</span><span class="sxs-lookup"><span data-stu-id="6a34a-119">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="6a34a-120">要了解更多信息，请参阅功能文档：[启用个性化建议。](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="6a34a-120">To learn more, please see the feature documenation: [enable personalized recommedations.](personalized-recommendations.md)</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="6a34a-121">建议服务</span><span class="sxs-lookup"><span data-stu-id="6a34a-121">Recommendation service</span></span>

<span data-ttu-id="6a34a-122">产品建议按照以下方式使用建议机器学习技术：</span><span class="sxs-lookup"><span data-stu-id="6a34a-122">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="6a34a-123">从 Commerce 操作数据库提取建议服务所需格式的数据并发送到实体商店。</span><span class="sxs-lookup"><span data-stu-id="6a34a-123">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="6a34a-124">建议服务使用这些数据培训**用户也喜欢**、**人气组合**、**新品**、**最畅销**和**热门**列表的建议模型。</span><span class="sxs-lookup"><span data-stu-id="6a34a-124">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a34a-125">其他资源</span><span class="sxs-lookup"><span data-stu-id="6a34a-125">Additional resources</span></span>

[<span data-ttu-id="6a34a-126">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="6a34a-126">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="6a34a-127">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="6a34a-127">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="6a34a-128">产品集合模块概览</span><span class="sxs-lookup"><span data-stu-id="6a34a-128">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="6a34a-129">创建策划的产品建议列表</span><span class="sxs-lookup"><span data-stu-id="6a34a-129">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="6a34a-130">管理基于 AI-ML 的产品建议结果</span><span class="sxs-lookup"><span data-stu-id="6a34a-130">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="6a34a-131">向页面添加建议列表</span><span class="sxs-lookup"><span data-stu-id="6a34a-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
