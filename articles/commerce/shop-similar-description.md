---
title: 启用“购买相似说明产品”建议
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中启用“购买相似说明产品”产品建议。
author: bsokolov
manager: AnnBe
ms.date: 01/13/2021
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
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b3b7abf47a3bdacaa4b91ae32b68a809a84b0b1d
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098614"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="ff5b0-103">启用“购买相似说明产品”建议</span><span class="sxs-lookup"><span data-stu-id="ff5b0-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ff5b0-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中启用“购买相似说明产品”产品建议。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ff5b0-105">Dynamics 365 Commerce 中的“购买相似说明产品”推荐功能利用人工智能和机器学习 (AI-ML) 提供说明与客户正在查找的产品相似的产品建议。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="ff5b0-106">通过为 Commerce 中的所有零售渠道提供“购买相似说明产品”建议，零售商可以帮助客户轻松找到他们想要的商品。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="ff5b0-107">“购买相似说明产品”建议功能使用种子产品的产品名称和说明在零售商的产品目录中查找和推荐相似产品。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="ff5b0-108">销售点 (POS) 和电子商务体验中都提供“购买相似说明产品”建议。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="ff5b0-109">示例方案</span><span class="sxs-lookup"><span data-stu-id="ff5b0-109">Example scenarios</span></span>

<span data-ttu-id="ff5b0-110">下面的示例场景说明了“购买相似说明产品”功能可以提供的建议类型：</span><span class="sxs-lookup"><span data-stu-id="ff5b0-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="ff5b0-111">客户查看一副复古风的角质架眼镜，然后收到了基于零售商行业上下文的其他设计相似的眼镜的建议。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="ff5b0-112">客户使用“购买相似说明产品”建议来发现与他们先前从零售商处购买的咖啡口味相似的咖啡口味。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="ff5b0-113">设置“购买相似说明产品”建议</span><span class="sxs-lookup"><span data-stu-id="ff5b0-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="ff5b0-114">仅针对已将存储迁移到 Azure Data Lake Storage Gen2 的 Commerce 用户支持产品建议。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ff5b0-115">先决条件</span><span class="sxs-lookup"><span data-stu-id="ff5b0-115">Prerequisites</span></span>

<span data-ttu-id="ff5b0-116">您必须完成以下先决条件，然后才能够向客户显示“购买相似说明产品”建议：</span><span class="sxs-lookup"><span data-stu-id="ff5b0-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="ff5b0-117">在 Commerce headquarters 中[启用产品建议](enable-product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="ff5b0-118">确认媒体服务器支持 HTTPS 调用。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="ff5b0-119">启用“购买相似说明产品”建议功能</span><span class="sxs-lookup"><span data-stu-id="ff5b0-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="ff5b0-120">要在 Commerce headquarters 中启用“购买相似说明产品”建议功能，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="ff5b0-121">在 **功能管理** 工作区中，在可用功能列表中，搜索并选择 **购买相似说明产品**。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="ff5b0-122">从右窗格中，选择 **启用**。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="ff5b0-123">启用此功能时，系统将开始生成产品建议列表。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="ff5b0-124">这些列表最多可能需要一天时间来在线和在 POS 终端上提供和显示。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="ff5b0-125">如果关闭此功能，其他类型的产品建议不会受到影响。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="ff5b0-126">有关产品建议的详细信息，请参阅[产品建议概述](product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="ff5b0-127">在产品详细信息页上添加“购买相似说明产品”按钮</span><span class="sxs-lookup"><span data-stu-id="ff5b0-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="ff5b0-128">在 Commerce headquarters 中启用“购买相似说明产品”建议功能之后，您可以在任何产品详细信息页 (PDP) 上的购买框中添加 **购买相似说明产品** 按钮。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="ff5b0-129">选择此按钮的客户将被带到专用的 **购买相似说明产品** 页面，该页面显示相似的产品。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="ff5b0-130">然后，客户可以使用选择器进一步筛选产品。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="ff5b0-131">要使用 Commerce 站点构建器将 **购买相似说明产品** 按钮添加到 PDP，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ff5b0-132">打开一个包含购买框模块的现有站点构建器页面。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="ff5b0-133">在左侧导航窗格中，选择购买框模块。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="ff5b0-134">在右侧窗格中，选择 **启用“购买相似说明产品”链接** 复选框。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="ff5b0-135">选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-135">Select **Save**.</span></span>
1. <span data-ttu-id="ff5b0-136">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="ff5b0-137">页面发布后，PDP 将包含一个 **购买相似说明产品** 按钮。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="ff5b0-138">下图显示了站点构建器中示例 PDP 上的 **启用“购买相似说明产品”链接** 复选框和 **购买相似说明产品** 按钮。</span><span class="sxs-lookup"><span data-stu-id="ff5b0-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![站点构建器中 PDP 上的“启用‘购买相似说明产品’链接”复选框和“购买相似说明产品”按钮](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="ff5b0-140">其他资源</span><span class="sxs-lookup"><span data-stu-id="ff5b0-140">Additional resources</span></span>

[<span data-ttu-id="ff5b0-141">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="ff5b0-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ff5b0-142">在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="ff5b0-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ff5b0-143">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="ff5b0-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="ff5b0-144">启用“购买相似外观产品”建议</span><span class="sxs-lookup"><span data-stu-id="ff5b0-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="ff5b0-145">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="ff5b0-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ff5b0-146">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="ff5b0-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ff5b0-147">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="ff5b0-147">Product recommendations FAQ</span></span>](faq-recommendations.md)
