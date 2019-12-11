---
title: 管理基于 AI-ML 的产品建议结果
description: 此主题介绍如何基于人工智能-机器学习 (AI-ML) 针对您的业务调整产品建议结果。
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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770062"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="b096e-103">管理基于 AI-ML 的产品建议结果</span><span class="sxs-lookup"><span data-stu-id="b096e-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b096e-104">此主题介绍如何基于人工智能-机器学习 (AI-ML) 针对您的业务调整产品建议结果。</span><span class="sxs-lookup"><span data-stu-id="b096e-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="b096e-105">启用产品建议之后，默认设置将生效；这些参数适用于许多需要的许多工作。</span><span class="sxs-lookup"><span data-stu-id="b096e-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="b096e-106">最好计划花一些时间评估结果是否符合产品的销售动态。</span><span class="sxs-lookup"><span data-stu-id="b096e-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="b096e-107">建议在更改参数前根据需要评估一些天的结果，之后再次测试。</span><span class="sxs-lookup"><span data-stu-id="b096e-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="b096e-108">了解建议列表参数</span><span class="sxs-lookup"><span data-stu-id="b096e-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="b096e-109">更改参数之前，在下面了解对结果的影响。</span><span class="sxs-lookup"><span data-stu-id="b096e-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="b096e-110">热门产品列表</span><span class="sxs-lookup"><span data-stu-id="b096e-110">Trending product list</span></span>

<span data-ttu-id="b096e-111">**热门**产品列表有两个可更改的参数：![示例热门列表默认参数](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="b096e-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="b096e-112">**包括过去 X 天的新产品** - 可使用当天前指定天数内已添加的产品选择候选产品。</span><span class="sxs-lookup"><span data-stu-id="b096e-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="b096e-113">图片中的默认值表明旧产品已有 180 天，可在热门产品列表中使用。</span><span class="sxs-lookup"><span data-stu-id="b096e-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="b096e-114">**包括过去 X 天的销售量** - 可使用当天前指定天数内进行的销售交易记录订购产品。</span><span class="sxs-lookup"><span data-stu-id="b096e-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="b096e-115">上面的默认值表明过去 30 天某个产品的所有购买用于决定此产品在热门产品列表中的位置。</span><span class="sxs-lookup"><span data-stu-id="b096e-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="b096e-116">最畅销产品列表</span><span class="sxs-lookup"><span data-stu-id="b096e-116">Best selling product list</span></span>

<span data-ttu-id="b096e-117">最畅销产品可根据您的业务提供不同于热门的结果，即使两者都使用交易记录数据订购产品。</span><span class="sxs-lookup"><span data-stu-id="b096e-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="b096e-118">因为最畅销没有基于分类日期的截止，所以最畅销仍然可以突出显示非常受欢迎，并且可能已从热门列表撤下的较早产品。</span><span class="sxs-lookup"><span data-stu-id="b096e-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="b096e-119">**最畅销**产品列表有一个可更改的参数：</span><span class="sxs-lookup"><span data-stu-id="b096e-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![示例最畅销列表默认参数](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="b096e-121">**包括过去 X 天的销售量** - 可使用当天前指定天数内进行的销售交易记录订购产品。</span><span class="sxs-lookup"><span data-stu-id="b096e-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="b096e-122">上面的默认值表明过去 30 天某个产品的所有购买用于决定此产品在最畅销产品列表中的位置。</span><span class="sxs-lookup"><span data-stu-id="b096e-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="b096e-123">在建议列表中手动添加或删除产品</span><span class="sxs-lookup"><span data-stu-id="b096e-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="b096e-124">对于新品、热门或最畅销</span><span class="sxs-lookup"><span data-stu-id="b096e-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="b096e-125">转到 **Retail**  >  **产品建议**  >  **建议参数**。</span><span class="sxs-lookup"><span data-stu-id="b096e-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="b096e-126">在零售共享参数列表中，选择**建议列表**。</span><span class="sxs-lookup"><span data-stu-id="b096e-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="b096e-127">选择要在其中添加或删除产品的列表。</span><span class="sxs-lookup"><span data-stu-id="b096e-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="b096e-128">若要向表添加产品，请选择**添加行**。</span><span class="sxs-lookup"><span data-stu-id="b096e-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="b096e-129">在“产品”列下，按**名称**或**产品编号**搜索产品。
![搜索“新”产品列表中的产品的示例](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="b096e-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="b096e-130">在“行类型”列下，选择两个选项之一：</span><span class="sxs-lookup"><span data-stu-id="b096e-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="b096e-131">**包含** – 强制产品位于列表前部</span><span class="sxs-lookup"><span data-stu-id="b096e-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="b096e-132">**排除** – 在列表中隐藏某个产品 ![在“新品”产品列表中包含或排除某个产品的示例](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="b096e-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="b096e-133">更改**显示顺序**将更改标记为**包含**的产品在列表中的显示顺序。</span><span class="sxs-lookup"><span data-stu-id="b096e-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="b096e-134">如果两个产品的**显示顺序**值相同，则这两个结果的最终顺序可能与后端不同。</span><span class="sxs-lookup"><span data-stu-id="b096e-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="b096e-135">若要从表中删除产品：选择要删除的行，然后选择**删除**。</span><span class="sxs-lookup"><span data-stu-id="b096e-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="b096e-136">对于“用户也喜欢”或“人气组合”列表</span><span class="sxs-lookup"><span data-stu-id="b096e-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="b096e-137">在**人气组合**或**用户也喜欢**列表的上下文中，使用机器学习分析消费者购买模式为唯一种子产品推荐通常一起购买的相关产品。</span><span class="sxs-lookup"><span data-stu-id="b096e-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="b096e-138">**种子产品**是要生成其结果的产品。</span><span class="sxs-lookup"><span data-stu-id="b096e-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="b096e-139">在手动调整建议列表的上下文中，添加或删除此产品的结果。</span><span class="sxs-lookup"><span data-stu-id="b096e-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="b096e-140">执行以下步骤手动添加或删除种子产品的结果：</span><span class="sxs-lookup"><span data-stu-id="b096e-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="b096e-141">选择**种子产品**。</span><span class="sxs-lookup"><span data-stu-id="b096e-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="b096e-142">在**产品**列下，按**名称**或**产品编号**搜索产品。
![搜索“人气组合”列表中的产品的示例](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="b096e-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="b096e-143">在**行类型**列下，选择两个选项之一：</span><span class="sxs-lookup"><span data-stu-id="b096e-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="b096e-144">**包含** – 强制产品位于列表前部</span><span class="sxs-lookup"><span data-stu-id="b096e-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="b096e-145">**排除** – 在列表中隐藏某个产品。</span><span class="sxs-lookup"><span data-stu-id="b096e-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="b096e-146">![在“人气组合”列表中包含或排除产品的示例](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="b096e-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="b096e-147">若要从表中删除产品：选择要删除的行，然后选择删除。</span><span class="sxs-lookup"><span data-stu-id="b096e-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="b096e-148">其他资源</span><span class="sxs-lookup"><span data-stu-id="b096e-148">Additional resources</span></span>

[<span data-ttu-id="b096e-149">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="b096e-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b096e-150">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="b096e-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b096e-151">向页面添加建议列表</span><span class="sxs-lookup"><span data-stu-id="b096e-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
