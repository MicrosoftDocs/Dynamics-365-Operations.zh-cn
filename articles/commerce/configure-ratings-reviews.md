---
title: 配置评分和评价
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置电子商务站点以显示客户评分和评价。
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071558"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="675c6-103">配置评分和评价</span><span class="sxs-lookup"><span data-stu-id="675c6-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="675c6-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中配置电子商务站点以显示客户评分和评价。</span><span class="sxs-lookup"><span data-stu-id="675c6-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="675c6-105">概览</span><span class="sxs-lookup"><span data-stu-id="675c6-105">Overview</span></span>

<span data-ttu-id="675c6-106">电子商务网站中的评分和评价可帮助客户在做出采购决定之前了解产品，方法是对其显示其他客户对这些产品的看法。</span><span class="sxs-lookup"><span data-stu-id="675c6-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="675c6-107">对于电子商务网站，评分和评价也是用于收集有关产品的客户反馈的机制。</span><span class="sxs-lookup"><span data-stu-id="675c6-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="675c6-108">配置站点以显示评分和评价</span><span class="sxs-lookup"><span data-stu-id="675c6-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="675c6-109">评分或评价的配置值（如租户 ID、评论文本长度和评论标题长度）在站点级别配置。</span><span class="sxs-lookup"><span data-stu-id="675c6-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="675c6-110">若要配置站点以显示评分或评价，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="675c6-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="675c6-111">转到**主 \> 站点**。</span><span class="sxs-lookup"><span data-stu-id="675c6-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="675c6-112">选择站点的名称。</span><span class="sxs-lookup"><span data-stu-id="675c6-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="675c6-113">转到**站点设置 \> 扩展**。</span><span class="sxs-lookup"><span data-stu-id="675c6-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="675c6-114">在**评论文本最大长度**字段中，输入评论文本可包含的最大字符数（例如，**1000**）。</span><span class="sxs-lookup"><span data-stu-id="675c6-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="675c6-115">在**评论标题最大长度**字段中，输入评论标题可包含的最大字符数（例如，**55**）。</span><span class="sxs-lookup"><span data-stu-id="675c6-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="675c6-116">选择**保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="675c6-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="675c6-117">下图显示此配置在 Dynamics 365 Commerce 中的显示效果。</span><span class="sxs-lookup"><span data-stu-id="675c6-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![配置站点以显示评分和评价](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="675c6-119">将产品评分链接到 PDP 的“评论”部分</span><span class="sxs-lookup"><span data-stu-id="675c6-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="675c6-120">将在 PDP 顶部的产品标题下显示产品评分。</span><span class="sxs-lookup"><span data-stu-id="675c6-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="675c6-121">可将产品评分配置为链接到同一个 PDP 的**评论**部分。</span><span class="sxs-lookup"><span data-stu-id="675c6-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="675c6-122">若要将产品评分链接到 PDP 的**评论**部分，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="675c6-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="675c6-123">打开 PDP 模板。</span><span class="sxs-lookup"><span data-stu-id="675c6-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="675c6-124">转到**购买框容器模块设置**。</span><span class="sxs-lookup"><span data-stu-id="675c6-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="675c6-125">在**购买框**下，选择**产品评分**，然后选中**链接单击以显示完整评论模块**复选框。</span><span class="sxs-lookup"><span data-stu-id="675c6-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="675c6-126">下图显示此配置在 Dynamics 365 Commerce 中的显示效果。</span><span class="sxs-lookup"><span data-stu-id="675c6-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![将产品评分链接到 PDP 的“评论”部分](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="675c6-128">配置隐私和政策页的链接</span><span class="sxs-lookup"><span data-stu-id="675c6-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="675c6-129">若要配置隐私和政策页的链接，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="675c6-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="675c6-130">转到**主 \> 站点**。</span><span class="sxs-lookup"><span data-stu-id="675c6-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="675c6-131">选择站点的名称。</span><span class="sxs-lookup"><span data-stu-id="675c6-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="675c6-132">转到**站点设置 \> 扩展**。</span><span class="sxs-lookup"><span data-stu-id="675c6-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="675c6-133">在**路由**选项卡中 **RNR 隐私和政策**下，选择**添加链接**。</span><span class="sxs-lookup"><span data-stu-id="675c6-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="675c6-134">如果已经输入了链接，但希望将其替换，请选择该链接。</span><span class="sxs-lookup"><span data-stu-id="675c6-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="675c6-135">在**添加链接**对话框中，选择隐私和政策页的链接，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="675c6-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="675c6-136">选择**保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="675c6-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="675c6-137">下图显示此配置在 Dynamics 365 Commerce 中的显示效果。</span><span class="sxs-lookup"><span data-stu-id="675c6-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![配置隐私和政策页的链接](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="675c6-139">配置产品详细信息页中的评分和评论模块</span><span class="sxs-lookup"><span data-stu-id="675c6-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="675c6-140">有关配置产品详细信息页中的评分和评论模块的信息，请参阅[评分和评论模块](ratings-reviews-modules.md)。</span><span class="sxs-lookup"><span data-stu-id="675c6-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="675c6-141">其他资源</span><span class="sxs-lookup"><span data-stu-id="675c6-141">Additional resources</span></span>

[<span data-ttu-id="675c6-142">评分和评价概览</span><span class="sxs-lookup"><span data-stu-id="675c6-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="675c6-143">选择使用评分和评价</span><span class="sxs-lookup"><span data-stu-id="675c6-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="675c6-144">管理评分和评价</span><span class="sxs-lookup"><span data-stu-id="675c6-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="675c6-145">配置产品详细信息页中的评分和评论模块</span><span class="sxs-lookup"><span data-stu-id="675c6-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="675c6-146">在 Dynamics 365 Retail 中同步产品评分</span><span class="sxs-lookup"><span data-stu-id="675c6-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
