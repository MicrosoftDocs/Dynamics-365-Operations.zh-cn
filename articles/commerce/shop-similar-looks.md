---
title: 启用“购买相似外观产品”建议
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中启用“购买相似外观产品”产品建议。
author: bebeale
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: da957850072e233a41a042d5857f81ddbf178f7a
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818366"
---
# <a name="enable-shop-similar-looks-recommendations"></a><span data-ttu-id="ed98e-103">启用“购买相似外观产品”建议</span><span class="sxs-lookup"><span data-stu-id="ed98e-103">Enable "shop similar looks" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ed98e-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中启用“购买相似外观产品”产品建议。</span><span class="sxs-lookup"><span data-stu-id="ed98e-104">This topic describes how to enable "shop similar looks" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ed98e-105">概览</span><span class="sxs-lookup"><span data-stu-id="ed98e-105">Overview</span></span>

<span data-ttu-id="ed98e-106">Dynamics 365 Commerce 中的“购买相似外观产品”推荐功能利用人工智能和机器学习 (AI-ML) 的力量向客户提供视觉上相似的产品建议。</span><span class="sxs-lookup"><span data-stu-id="ed98e-106">The "shop similar looks" recommendations feature in Dynamics 365 Commerce uses the power of artificial intelligence and machine learning (AI-ML) to deliver recommendations for visually similar products to customers.</span></span> <span data-ttu-id="ed98e-107">通过为 Commerce 中的所有零售渠道提供“购买相似外观产品”建议，零售商可以通过帮助客户轻松找到他们想要的商品来提高客户满意度。</span><span class="sxs-lookup"><span data-stu-id="ed98e-107">By making "shop similar looks" recommendations available for all retail channels in Commerce, retailers can increase customer satisfaction by helping customers easily find what they want.</span></span>

<span data-ttu-id="ed98e-108">“购买相似外观产品”建议功能使用种子产品变型的产品图像在零售商的产品目录中查找和推荐视觉上相似的产品。</span><span class="sxs-lookup"><span data-stu-id="ed98e-108">The functionality for "shop similar looks" recommendations uses product images of seed product variants to find and recommend visually similar products in a retailer's product catalog.</span></span> 

<span data-ttu-id="ed98e-109">销售点 (POS) 和电子商务体验中都提供“购买相似外观产品”建议。</span><span class="sxs-lookup"><span data-stu-id="ed98e-109">"Shop similar looks" recommendations are available in both the point of sale (POS) and e-Commerce experiences.</span></span>

### <a name="example-scenarios"></a><span data-ttu-id="ed98e-110">示例方案</span><span class="sxs-lookup"><span data-stu-id="ed98e-110">Example scenarios</span></span>

- <span data-ttu-id="ed98e-111">某客户查看一件黑色条纹的毛衣，收到一条推荐类似的红色毛衣的建议。</span><span class="sxs-lookup"><span data-stu-id="ed98e-111">A customer views a black striped sweater and receives a recommendation for a similar sweater in red.</span></span> <span data-ttu-id="ed98e-112">该客户选择建议的产品而不是最初查看的产品，然后收到红色的类似产品的建议。</span><span class="sxs-lookup"><span data-stu-id="ed98e-112">The customer selects the recommended product instead of the originally viewed product and then receives recommendations for similar products in red.</span></span> 
- <span data-ttu-id="ed98e-113">某客户使用“购买相似外观产品”建议来发现与该客户有兴趣购买的戒指匹配的耳环。</span><span class="sxs-lookup"><span data-stu-id="ed98e-113">A customer uses "shop similar looks" recommendations to discover matching earrings for a ring that the customer is interested in buying.</span></span>

## <a name="enable-shop-similar-looks-recommendations-in-commerce-headquarters"></a><span data-ttu-id="ed98e-114">在 Commerce headquarters 中启用“购买相似外观产品”建议</span><span class="sxs-lookup"><span data-stu-id="ed98e-114">Enable "shop similar looks" recommendations in Commerce headquarters</span></span>

<span data-ttu-id="ed98e-115">仅针对已将存储迁移到 Azure Data Lake Gen2 的 Commerce 用户支持产品建议。</span><span class="sxs-lookup"><span data-stu-id="ed98e-115">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ed98e-116">先决条件</span><span class="sxs-lookup"><span data-stu-id="ed98e-116">Prerequisites</span></span>

<span data-ttu-id="ed98e-117">在零售商可以开始向客户显示“购买相似外观产品”建议之前，有两个先决步骤：</span><span class="sxs-lookup"><span data-stu-id="ed98e-117">Before retailers can begin to show "shop similar looks" recommendations to customers, there are two prerequisite steps:</span></span>

- <span data-ttu-id="ed98e-118">在 Commerce headquarters 中[启用产品建议](enable-product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="ed98e-118">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="ed98e-119">确认媒体服务器支持 HTTPS 调用。</span><span class="sxs-lookup"><span data-stu-id="ed98e-119">Confirm that the media server supports HTTPS calls.</span></span>

<span data-ttu-id="ed98e-120">要让建议引擎能够访问产品图像，零售商必须生成产品 URL。</span><span class="sxs-lookup"><span data-stu-id="ed98e-120">For the recommendations engine to access the product images, retailers must generate the product URLs.</span></span> <span data-ttu-id="ed98e-121">要在 Commerce Headquarters 中生成产品 URL，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ed98e-121">To generate product URLs in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ed98e-122">转到**产品图像**。</span><span class="sxs-lookup"><span data-stu-id="ed98e-122">Go to **Product images**.</span></span>
1. <span data-ttu-id="ed98e-123">在操作窗格上，选择**定义媒体模板**。</span><span class="sxs-lookup"><span data-stu-id="ed98e-123">On the Action Pane, select **Define media template**.</span></span>
1. <span data-ttu-id="ed98e-124">在**定义媒体模板**属性窗格中，在**媒体 URL** 下，选择**生成 URL**。</span><span class="sxs-lookup"><span data-stu-id="ed98e-124">In the **Define media template** properties pane, under **Media URLs**, select **Generate URLs**.</span></span>

> [!NOTE]
> <span data-ttu-id="ed98e-125">启用“购买相似外观产品”建议功能后，生成产品建议列表的过程将开始。</span><span class="sxs-lookup"><span data-stu-id="ed98e-125">When you enable the "shop similar looks" recommendations feature, the process of generating product recommendation lists begins.</span></span> <span data-ttu-id="ed98e-126">这些列表最多可能需要一天时间完成在线以及在 POS 终端上提供和显示。</span><span class="sxs-lookup"><span data-stu-id="ed98e-126">Up to a day might be required before those lists are available and visible online and on POS terminals.</span></span>

<span data-ttu-id="ed98e-127">要在 Commerce headquarters 中启用“购买相似外观产品”建议功能，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ed98e-127">To enable the "shop similar looks" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ed98e-128">转到**功能管理**。</span><span class="sxs-lookup"><span data-stu-id="ed98e-128">Go to **Feature management**.</span></span>
1. <span data-ttu-id="ed98e-129">在可用功能列表中，搜索并选择**购买相似外观产品**。</span><span class="sxs-lookup"><span data-stu-id="ed98e-129">In the list of available features, search for and select **Shop similar looks**.</span></span>
1. <span data-ttu-id="ed98e-130">在右窗格中，选择**启用**打开此服务。</span><span class="sxs-lookup"><span data-stu-id="ed98e-130">In the right pane, select **Enable** to turn on the service.</span></span>

<span data-ttu-id="ed98e-131">下图显示了 Commerce headquarters 中**功能管理**页面上的**购买相似外观产品**功能。</span><span class="sxs-lookup"><span data-stu-id="ed98e-131">The following illustration shows the **Shop similar looks** feature on the **Feature management** page in Commerce headquarters.</span></span>

![Commerce headquarters 中“功能管理”页面上的“购买相似外观产品”功能](./media/enableshopsimilarlooks.png)

<span data-ttu-id="ed98e-133">完成上述任务后，POS 终端将自动增强，提供上下文**购买相似外观产品**面板。</span><span class="sxs-lookup"><span data-stu-id="ed98e-133">After the preceding tasks been completed, POS terminals are automatically enhanced with a contextual **Shop similar products** panel.</span></span> <span data-ttu-id="ed98e-134">选择**查看更多**，POS 终端用户可以转到专用的“购买相似外观产品”页面，可以在那里进一步筛选。</span><span class="sxs-lookup"><span data-stu-id="ed98e-134">By selecting **See more**, POS terminal users can be taken to a dedicated "shop similar looks" page that can be filtered further.</span></span>

> [!NOTE]
> <span data-ttu-id="ed98e-135">如果关闭“购买相似外观产品”建议功能，不会影响其他类型产品的建议。</span><span class="sxs-lookup"><span data-stu-id="ed98e-135">If you turn off the "shop similar looks" recommendations feature, no other types of product recommendations are affected.</span></span> <span data-ttu-id="ed98e-136">有关产品建议的详细信息，请参阅[产品建议概述](product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="ed98e-136">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-looks-button-to-product-details-pages-by-using-commerce-site-builder"></a><span data-ttu-id="ed98e-137">使用 Commerce 站点构建器将“购买相似外观产品”按钮添加到产品详细信息页面</span><span class="sxs-lookup"><span data-stu-id="ed98e-137">Add a Shop similar looks button to product details pages by using Commerce site builder</span></span>

<span data-ttu-id="ed98e-138">在 Commerce headquarters 中启用“购买相似外观产品”建议功能之后，Commerce 站点构建器中的一个选项让零售商可以在任何产品详细信息页面 (PDP) 上的购买框中添加**购买相似外观产品**按钮。</span><span class="sxs-lookup"><span data-stu-id="ed98e-138">After you enable the "shop similar looks" recommendations feature in Commerce headquarters, an option in Commerce site builder lets retailers to add a **Shop similar looks** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="ed98e-139">选择此按钮的客户将被带到专用的“购买相似外观产品”页面，该页面返回外观相似的产品。</span><span class="sxs-lookup"><span data-stu-id="ed98e-139">A customer who selects this button is taken to a dedicated "shop similar looks" page that returns visually similar products.</span></span> <span data-ttu-id="ed98e-140">在那里，客户可以使用选择器进一步筛选产品。</span><span class="sxs-lookup"><span data-stu-id="ed98e-140">There, the customer can use selectors to further filter the products.</span></span>

<span data-ttu-id="ed98e-141">要使用 Commerce 站点构建器将**购买相似外观产品**按钮添加到 PDP，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ed98e-141">To add a **Shop similar looks** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ed98e-142">打开一个包含购买框模块的现有站点构建器页面。</span><span class="sxs-lookup"><span data-stu-id="ed98e-142">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="ed98e-143">在左侧导航窗格中，选择购买框模块。</span><span class="sxs-lookup"><span data-stu-id="ed98e-143">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="ed98e-144">在右侧导航窗格中，选择**启用“购买相似外观产品”链接**复选框。</span><span class="sxs-lookup"><span data-stu-id="ed98e-144">In the right navigation pane, select the **Enable Shop Similar Looks Link** check box.</span></span>
1. <span data-ttu-id="ed98e-145">选择**保存**，选择**完成编辑**签入页面，然后选择**发布**进行发布。</span><span class="sxs-lookup"><span data-stu-id="ed98e-145">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="ed98e-146">页面发布后，PDP 将包含一个**购买相似外观产品**按钮。</span><span class="sxs-lookup"><span data-stu-id="ed98e-146">After the page is published, the PDP will include a **Shop similar looks** button.</span></span>

<span data-ttu-id="ed98e-147">下图显示了站点构建器中示例 PDP 上的**启用“购买相似外观产品”链接**复选框和**购买相似外观产品**按钮。</span><span class="sxs-lookup"><span data-stu-id="ed98e-147">The following illustration shows the **Enable Shop Similar Looks Link** check box and **Shop similar looks** button on an example PDP in site builder.</span></span>

![站点构建器中 PDP 上的“启用‘购买相似外观产品’链接”复选框和“购买相似外观产品”按钮](./media/SSLecomtooling.png)

## <a name="additional-resources"></a><span data-ttu-id="ed98e-149">其他资源</span><span class="sxs-lookup"><span data-stu-id="ed98e-149">Additional resources</span></span>

[<span data-ttu-id="ed98e-150">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="ed98e-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ed98e-151">在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="ed98e-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ed98e-152">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="ed98e-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="ed98e-153">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="ed98e-153">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ed98e-154">在 POS 中添加产品建议</span><span class="sxs-lookup"><span data-stu-id="ed98e-154">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ed98e-155">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="ed98e-155">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ed98e-156">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="ed98e-156">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ed98e-157">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="ed98e-157">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ed98e-158">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="ed98e-158">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ed98e-159">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="ed98e-159">Product recommendations FAQ</span></span>](faq-recommendations.md)
