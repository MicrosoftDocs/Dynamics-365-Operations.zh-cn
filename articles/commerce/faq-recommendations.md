---
title: 产品建议常见问题
description: 此主题介绍可用于诊断与产品建议或其结果有关的流程和工具。
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f4f053066ef9a10ca8a60e6eb081f73401760eb4
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770108"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="a6c19-103">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="a6c19-103">Product recommendations FAQ</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a6c19-104">此主题介绍可用于诊断与[产品建议](product-recommendations.md)或其结果有关的流程和工具。</span><span class="sxs-lookup"><span data-stu-id="a6c19-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="a6c19-105">最佳实践</span><span class="sxs-lookup"><span data-stu-id="a6c19-105">Best practices</span></span>
<span data-ttu-id="a6c19-106">请务必利用基础产品和变型概念。</span><span class="sxs-lookup"><span data-stu-id="a6c19-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="a6c19-107">对父产品的变型合理分组可帮助列表算法和服务创建更好的模型。</span><span class="sxs-lookup"><span data-stu-id="a6c19-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="a6c19-108">此外，此服务只能处理一个产品实例，而不是将所有关系密切的变型放到一个列表中。</span><span class="sxs-lookup"><span data-stu-id="a6c19-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="a6c19-109">将所有关系密切的变型放到一个列表中后，可能会产生错误结果或重复结果。</span><span class="sxs-lookup"><span data-stu-id="a6c19-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="a6c19-110">我的建议列表中为什么缺少产品？</span><span class="sxs-lookup"><span data-stu-id="a6c19-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="a6c19-111">如果产品建议列表中缺少项，通常是因为存在产品配置问题。</span><span class="sxs-lookup"><span data-stu-id="a6c19-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="a6c19-112">例如，产品开始日期或结束日期不正确，维度配置不当，或产品不在正确的渠道分类中等。</span><span class="sxs-lookup"><span data-stu-id="a6c19-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="a6c19-113">如果基于人工智能-机器学习 (AI-ML) 的建议列表中缺少某项，可能是因为该项不符合建议列表的条件，或该项的购买交易数量不足，导致建议列表无法显示该项。</span><span class="sxs-lookup"><span data-stu-id="a6c19-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="a6c19-114">建议执行以下检查步骤：</span><span class="sxs-lookup"><span data-stu-id="a6c19-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="a6c19-115">**确保总部已启用产品建议。**</span><span class="sxs-lookup"><span data-stu-id="a6c19-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="a6c19-116">有关如何启用此服务的详细信息，请参阅[启用产品建议](enable-product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c19-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="a6c19-117">**确保设置关键产品属性。**</span><span class="sxs-lookup"><span data-stu-id="a6c19-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="a6c19-118">例如，必须将产品分类设置为**包括**。</span><span class="sxs-lookup"><span data-stu-id="a6c19-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="a6c19-119">**对于新分类产品，可能最多需要 3 小时，才会在新列表中开始显示该产品。**</span><span class="sxs-lookup"><span data-stu-id="a6c19-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="a6c19-120">**如果“热门”、“最畅销”、“用户还喜欢”或“人气组合”中仍然不显示某个产品，说明该产品的交易数量可能不足。**</span><span class="sxs-lookup"><span data-stu-id="a6c19-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="a6c19-121">在此情况下，可以登录进行更多交易，更新默认建议列表参数，或通过手动干预修改建议产品列表结果。</span><span class="sxs-lookup"><span data-stu-id="a6c19-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="a6c19-122">有关建议参数的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c19-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="a6c19-123">**确保产品满足列表的建议条件。**</span><span class="sxs-lookup"><span data-stu-id="a6c19-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="a6c19-124">有关产品建议参数的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c19-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="a6c19-125">如何避免返回质量不佳的建议结果？</span><span class="sxs-lookup"><span data-stu-id="a6c19-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="a6c19-126">建议列表需要大量交易记录才能生成结果。</span><span class="sxs-lookup"><span data-stu-id="a6c19-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="a6c19-127">因此，用户务必提供完整的历史交易数据。</span><span class="sxs-lookup"><span data-stu-id="a6c19-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="a6c19-128">此外，交易不足或较少的产品通常没有**用户还喜欢**或**人气组合**结果，并且不再**热门**或**最畅销**建议列表中显示。</span><span class="sxs-lookup"><span data-stu-id="a6c19-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="a6c19-129">每种新产品或购买数量较小的老产品可能经常发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="a6c19-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="a6c19-130">受欢迎的新品很容易克服这个问题。</span><span class="sxs-lookup"><span data-stu-id="a6c19-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="a6c19-131">建议执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="a6c19-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="a6c19-132">**确保产品满足该列表的建议条件。**</span><span class="sxs-lookup"><span data-stu-id="a6c19-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="a6c19-133">有关产品建议参数的详细信息，请参阅“修改基于 AI-ML 的产品建议结果”。</span><span class="sxs-lookup"><span data-stu-id="a6c19-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="a6c19-134">**如果产品是新产品，请考虑修改建议列表，直到该产品具有更多交易。**</span><span class="sxs-lookup"><span data-stu-id="a6c19-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="a6c19-135">有关如何修改建议列表结果的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c19-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="a6c19-136">**确保产品满足该列表的建议条件。**</span><span class="sxs-lookup"><span data-stu-id="a6c19-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="a6c19-137">有关产品建议参数的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c19-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="a6c19-138">**如果产品是新产品，请考虑修改建议列表，直到该产品具有更多交易**。</span><span class="sxs-lookup"><span data-stu-id="a6c19-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="a6c19-139">有关如何修改建议列表结果的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c19-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="a6c19-140">无法删除某个产品，但是商店中仍然可以看到该产品？</span><span class="sxs-lookup"><span data-stu-id="a6c19-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="a6c19-141">如果需要提高业务，可以调整通过算法生成的类别。</span><span class="sxs-lookup"><span data-stu-id="a6c19-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="a6c19-142">但是，如果从建议列表中删除某个产品，商店中仍然可以发现该产品。</span><span class="sxs-lookup"><span data-stu-id="a6c19-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="a6c19-143">有关如何修改产品建议结果的详细信息，请参阅[管理基于 AI-ML 的产品建议结果](modify-product-recommendation-results.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c19-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="a6c19-144">如果必须阻止商店中发现某项，必须将**项分类**值设置为**排除**。</span><span class="sxs-lookup"><span data-stu-id="a6c19-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="a6c19-145">如何向电子商务页面添加列表？</span><span class="sxs-lookup"><span data-stu-id="a6c19-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="a6c19-146">有关如何向电子商务网站添加产品建议页面的信息，请参阅[向页面添加产品建议列表](add-reco-list-to-page.md)。</span><span class="sxs-lookup"><span data-stu-id="a6c19-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="a6c19-147">如何在 POS 上启用建议？</span><span class="sxs-lookup"><span data-stu-id="a6c19-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="a6c19-148">启用产品建议之后，需要向控制 POS 屏幕添加建议面板。</span><span class="sxs-lookup"><span data-stu-id="a6c19-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="a6c19-149">有关如何向 POS 设备布局添加建议面板的详细信息，请参阅[本功能文档](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)。</span><span class="sxs-lookup"><span data-stu-id="a6c19-149">See [this feature documentation](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen) for more information on how to do add the recommendations panel to your POS device layout.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6c19-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="a6c19-150">Additional resources</span></span>

[<span data-ttu-id="a6c19-151">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="a6c19-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a6c19-152">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="a6c19-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a6c19-153">管理基于 AI-ML 的产品建议结果</span><span class="sxs-lookup"><span data-stu-id="a6c19-153">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)
