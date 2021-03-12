---
title: 调整基于 AI-ML 的产品建议结果
description: 此主题介绍如何基于人工智能-机器学习 (AI-ML) 针对您的业务调整产品建议结果。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: aab1b22b844ad14a94e1143f49b69f525d93f5b0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985903"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="a2d05-103">调整基于 AI-ML 的产品建议结果</span><span class="sxs-lookup"><span data-stu-id="a2d05-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a2d05-104">此主题介绍如何基于人工智能-机器学习 (AI-ML) 针对您的业务调整产品建议结果。</span><span class="sxs-lookup"><span data-stu-id="a2d05-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="a2d05-105">启用产品建议之后，默认设置将生效；这些参数适用于许多需要的许多工作。</span><span class="sxs-lookup"><span data-stu-id="a2d05-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="a2d05-106">最好计划花一些时间评估结果是否符合产品的销售动态。</span><span class="sxs-lookup"><span data-stu-id="a2d05-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="a2d05-107">建议在更改参数前根据需要评估一些天的结果，之后再次测试。</span><span class="sxs-lookup"><span data-stu-id="a2d05-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="a2d05-108">了解建议列表参数</span><span class="sxs-lookup"><span data-stu-id="a2d05-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="a2d05-109">更改参数之前，在下面了解对结果的影响。</span><span class="sxs-lookup"><span data-stu-id="a2d05-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="a2d05-110">“热门”产品列表</span><span class="sxs-lookup"><span data-stu-id="a2d05-110">"Trending" product list</span></span>

<span data-ttu-id="a2d05-111">“热门”产品列表有两个可更改的参数：</span><span class="sxs-lookup"><span data-stu-id="a2d05-111">The "Trending" product list has two parameters that can be changed:</span></span>

![示例“热门”列表默认参数](./media/exampletrendingparameters.png)

1. <span data-ttu-id="a2d05-113">**包括过去 X 天的新产品** - 可使用当天前指定天数内已添加的产品选择候选产品。</span><span class="sxs-lookup"><span data-stu-id="a2d05-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="a2d05-114">图片中的默认值表明旧产品已有 180 天，可在热门产品列表中使用。</span><span class="sxs-lookup"><span data-stu-id="a2d05-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="a2d05-115">**包括过去 X 天的销售量** - 可使用当天前指定天数内进行的销售交易记录订购产品。</span><span class="sxs-lookup"><span data-stu-id="a2d05-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="a2d05-116">上面的默认值表明过去 30 天某个产品的所有购买用于决定此产品在热门产品列表中的位置。</span><span class="sxs-lookup"><span data-stu-id="a2d05-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="a2d05-117">“最畅销”产品列表</span><span class="sxs-lookup"><span data-stu-id="a2d05-117">"Best selling" product list</span></span>

<span data-ttu-id="a2d05-118">“最畅销”列表可根据您的业务提供不同于热门的结果，即使两者都使用交易记录数据订购产品。</span><span class="sxs-lookup"><span data-stu-id="a2d05-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="a2d05-119">因为最畅销没有基于分类日期的截止，所以最畅销仍然可以突出显示非常受欢迎，并且可能已从热门列表撤下的较早产品。</span><span class="sxs-lookup"><span data-stu-id="a2d05-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="a2d05-120">“最畅销”产品列表有一个可更改的参数：</span><span class="sxs-lookup"><span data-stu-id="a2d05-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![示例最畅销列表默认参数](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="a2d05-122">**包括过去 X 天的销售量** - 可使用当天前指定天数内进行的销售交易记录订购产品。</span><span class="sxs-lookup"><span data-stu-id="a2d05-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="a2d05-123">上面的默认值表明过去 30 天某个产品的所有购买用于决定此产品在最畅销产品列表中的位置。</span><span class="sxs-lookup"><span data-stu-id="a2d05-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="a2d05-124">在建议列表中手动添加或删除产品</span><span class="sxs-lookup"><span data-stu-id="a2d05-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="a2d05-125">对于“新品”、“热门”或“最畅销”列表</span><span class="sxs-lookup"><span data-stu-id="a2d05-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="a2d05-126">转到 **Retail 和 Commerce** > **产品建议** > **建议参数**。</span><span class="sxs-lookup"><span data-stu-id="a2d05-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="a2d05-127">在共享参数列表中，选择 **建议列表**。</span><span class="sxs-lookup"><span data-stu-id="a2d05-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="a2d05-128">选择要在其中添加或删除产品的列表。</span><span class="sxs-lookup"><span data-stu-id="a2d05-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="a2d05-129">若要向表添加产品，请选择 **添加行**。</span><span class="sxs-lookup"><span data-stu-id="a2d05-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="a2d05-130">在“产品”列下，按 **名称** 或 **产品编号** 搜索产品。</span><span class="sxs-lookup"><span data-stu-id="a2d05-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![在“新品”产品列表中搜索产品的示例](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="a2d05-132">在“行类型”列下，选择两个选项之一：</span><span class="sxs-lookup"><span data-stu-id="a2d05-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="a2d05-133">**包含** – 强制产品位于列表前部</span><span class="sxs-lookup"><span data-stu-id="a2d05-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="a2d05-134">**排除** – 在列表中隐藏某个产品。</span><span class="sxs-lookup"><span data-stu-id="a2d05-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![在“新品”产品列表中包含或排除某个产品的示例](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="a2d05-136">更改 **显示顺序** 将更改标记为 **包含** 的产品在列表中的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="a2d05-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="a2d05-137">如果两个产品的 **显示顺序** 值相同，则这两个结果的最终顺序可能与后端不同。</span><span class="sxs-lookup"><span data-stu-id="a2d05-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="a2d05-138">若要从表中删除产品：选择要删除的行，然后选择 **删除**。</span><span class="sxs-lookup"><span data-stu-id="a2d05-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="a2d05-139">对于“用户也喜欢”或“人气组合”列表</span><span class="sxs-lookup"><span data-stu-id="a2d05-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="a2d05-140">在“人气组合”或“用户也喜欢”列表的上下文中，使用机器学习分析消费者购买模式为唯一种子产品推荐通常一起购买的相关产品。</span><span class="sxs-lookup"><span data-stu-id="a2d05-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="a2d05-141">*种子产品* 是要生成其结果的产品。</span><span class="sxs-lookup"><span data-stu-id="a2d05-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="a2d05-142">在手动调整建议列表的上下文中，添加或删除此产品的结果。</span><span class="sxs-lookup"><span data-stu-id="a2d05-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="a2d05-143">执行以下步骤手动添加或删除种子产品的结果：</span><span class="sxs-lookup"><span data-stu-id="a2d05-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="a2d05-144">选择 **种子产品**。</span><span class="sxs-lookup"><span data-stu-id="a2d05-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="a2d05-145">在 **产品** 列下，按 **名称** 或 **产品编号** 搜索产品。
![搜索“人气组合”列表中的产品的示例](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="a2d05-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="a2d05-146">在 **行类型** 列下，选择两个选项之一：</span><span class="sxs-lookup"><span data-stu-id="a2d05-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="a2d05-147">**包含** – 强制产品位于列表前部</span><span class="sxs-lookup"><span data-stu-id="a2d05-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="a2d05-148">**排除** – 在列表中隐藏某个产品。</span><span class="sxs-lookup"><span data-stu-id="a2d05-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="a2d05-149">![在“人气组合”列表中包含或排除产品的示例](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="a2d05-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="a2d05-150">若要从表中删除产品：选择要删除的行，然后选择删除。</span><span class="sxs-lookup"><span data-stu-id="a2d05-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="a2d05-151">其他资源</span><span class="sxs-lookup"><span data-stu-id="a2d05-151">Additional resources</span></span>

[<span data-ttu-id="a2d05-152">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="a2d05-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="a2d05-153">在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="a2d05-153">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="a2d05-154">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="a2d05-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="a2d05-155">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="a2d05-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="a2d05-156">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="a2d05-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="a2d05-157">启用“购买类似外观”建议</span><span class="sxs-lookup"><span data-stu-id="a2d05-157">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="a2d05-158">在 POS 上添加产品建议</span><span class="sxs-lookup"><span data-stu-id="a2d05-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="a2d05-159">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="a2d05-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="a2d05-160">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="a2d05-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="a2d05-161">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="a2d05-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="a2d05-162">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="a2d05-162">Product recommendations FAQ</span></span>](faq-recommendations.md)
