---
title: 雇用个性化产品建议
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中让个性化产品建议可以为客户所用。
author: bebeale
manager: AnnBe
ms.date: 08/18/2020
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
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8a61ef0720839d371701f2f0a1fdec7e85a5feb7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410457"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="67bfb-103">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="67bfb-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67bfb-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中让个性化产品建议可以为客户所用。</span><span class="sxs-lookup"><span data-stu-id="67bfb-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="67bfb-105">概览</span><span class="sxs-lookup"><span data-stu-id="67bfb-105">Overview</span></span>

<span data-ttu-id="67bfb-106">在 Dynamics 365 Commerce 中，零售商可以提供个性化的产品建议（也称为个性化）。</span><span class="sxs-lookup"><span data-stu-id="67bfb-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="67bfb-107">通过这种方式，可以将个性化的建议引入到在线和销售点 (POS) 的客户体验中。</span><span class="sxs-lookup"><span data-stu-id="67bfb-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="67bfb-108">当个性化功能打开时，系统可以将用户的购买和产品信息相关联，以生成个性化的产品建议。</span><span class="sxs-lookup"><span data-stu-id="67bfb-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="67bfb-109">个性化的先决条件</span><span class="sxs-lookup"><span data-stu-id="67bfb-109">Personalization prerequisites</span></span>

<span data-ttu-id="67bfb-110">在向客户提供个性化的产品建议之前，请注意，仅支持为已将存储迁移到 Azure Data Lake Store 的 Commerce 用户提供产品建议。</span><span class="sxs-lookup"><span data-stu-id="67bfb-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="67bfb-111">零售商必须先[打开产品建议](enable-product-recommendations.md)，然后客户才能够收到个性化产品建议。</span><span class="sxs-lookup"><span data-stu-id="67bfb-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="67bfb-112">通过打开产品建议，您还可以打开个性化。</span><span class="sxs-lookup"><span data-stu-id="67bfb-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="67bfb-113">但是，如果关闭个性化，不会关闭其他类型的产品建议。</span><span class="sxs-lookup"><span data-stu-id="67bfb-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="67bfb-114">有关产品建议的详细信息，请参阅[产品建议概述](product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="67bfb-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="67bfb-115">打开个性化</span><span class="sxs-lookup"><span data-stu-id="67bfb-115">Turn on personalization</span></span>

<span data-ttu-id="67bfb-116">若要打开个性化，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="67bfb-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="67bfb-117">在 Commerce headquarters 中，搜索 **功能管理**。</span><span class="sxs-lookup"><span data-stu-id="67bfb-117">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="67bfb-118">选择 **所有** 查看可用功能列表。</span><span class="sxs-lookup"><span data-stu-id="67bfb-118">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="67bfb-119">在搜索框中，输入 **建议**。</span><span class="sxs-lookup"><span data-stu-id="67bfb-119">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="67bfb-120">选择 **个性化产品建议** 功能。</span><span class="sxs-lookup"><span data-stu-id="67bfb-120">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="67bfb-121">在 **个性化产品建议** 属性窗格中，选择 **立即启用**。</span><span class="sxs-lookup"><span data-stu-id="67bfb-121">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![打开个性化](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="67bfb-123">打开个性化时，将启动生成个性化产品建议列表的过程。</span><span class="sxs-lookup"><span data-stu-id="67bfb-123">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="67bfb-124">这些列表最多可能需要一天时间完成在线以及在 POS 上提供和显示。</span><span class="sxs-lookup"><span data-stu-id="67bfb-124">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="67bfb-125">个性化列表</span><span class="sxs-lookup"><span data-stu-id="67bfb-125">Personalized lists</span></span>

<span data-ttu-id="67bfb-126">除了允许现有的计算机生成的列表的个性化外，建议服务还允许在线和 POS 上的产品发现体验的个性化。</span><span class="sxs-lookup"><span data-stu-id="67bfb-126">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="67bfb-127">打开个性化后，零售商可以在线向购买者显示个性化的“为您推荐”列表或在 POS 终端上显示“为客户推荐”列表。</span><span class="sxs-lookup"><span data-stu-id="67bfb-127">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="67bfb-128">此外，零售商可以将个性化应用于现有产品建议列表，并为经过身份验证的用户提供一般数据保护条例 (GDPR) 退出体验。</span><span class="sxs-lookup"><span data-stu-id="67bfb-128">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="67bfb-129">如果关闭个性化，还将关闭这些功能。</span><span class="sxs-lookup"><span data-stu-id="67bfb-129">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="67bfb-130">在线“为您推荐”列表</span><span class="sxs-lookup"><span data-stu-id="67bfb-130">Online "Picks for you" lists</span></span>

<span data-ttu-id="67bfb-131">“为您推荐”列表是一个人工智能机器学习 (AI-ML) 列表，它向经过身份验证的用户显示建议产品的个性化列表。</span><span class="sxs-lookup"><span data-stu-id="67bfb-131">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="67bfb-132">此列表基于用户的全渠道购买历史记录。</span><span class="sxs-lookup"><span data-stu-id="67bfb-132">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="67bfb-133">个性化建议会随着用户进行更多购买而动态更新。</span><span class="sxs-lookup"><span data-stu-id="67bfb-133">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="67bfb-134">这种类型的列表还支持类别筛选，以便零售商可以根据导航层次结构显示首选商品。</span><span class="sxs-lookup"><span data-stu-id="67bfb-134">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="67bfb-135">必须满足以下用户要求，“为您推荐”列表才可以出现在任何电子商务页面上：</span><span class="sxs-lookup"><span data-stu-id="67bfb-135">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="67bfb-136">用户必须登录。</span><span class="sxs-lookup"><span data-stu-id="67bfb-136">Users must be signed in.</span></span> <span data-ttu-id="67bfb-137">匿名用户将看不到个性化推荐。</span><span class="sxs-lookup"><span data-stu-id="67bfb-137">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="67bfb-138">用户必须在其帐户中至少进行了一次购买。</span><span class="sxs-lookup"><span data-stu-id="67bfb-138">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="67bfb-139">用户必须选择接收个性化建议。</span><span class="sxs-lookup"><span data-stu-id="67bfb-139">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="67bfb-140">下图显示了在线商店页面上的“为您推荐”列表的示例。</span><span class="sxs-lookup"><span data-stu-id="67bfb-140">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![在线“为您推荐”列表](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="67bfb-142">POS 上的“为客户推荐”列表</span><span class="sxs-lookup"><span data-stu-id="67bfb-142">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="67bfb-143">为了增强客户服务体验，零售商可以通过添加有上下文的“为客户推荐”列表来个性化现有的客户详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="67bfb-143">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="67bfb-144">下图显示了 POS 终端上的“为客户推荐”列表的示例。</span><span class="sxs-lookup"><span data-stu-id="67bfb-144">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![POS 上的“为客户推荐”列表](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="67bfb-146">将个性化应用于现有建议列表</span><span class="sxs-lookup"><span data-stu-id="67bfb-146">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="67bfb-147">零售商可以将个性化应用于现有建议列表，例如“新品”、“热门”、“最畅销”、“用户也喜欢”和“人气组合”。</span><span class="sxs-lookup"><span data-stu-id="67bfb-147">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="67bfb-148">将个性化应用于现有列表后，登录用户先前购买的商品将从这些列表中删除。</span><span class="sxs-lookup"><span data-stu-id="67bfb-148">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="67bfb-149">对于匿名用户和选择不接收个性化建议的用户，将显示现有列表的默认版本。</span><span class="sxs-lookup"><span data-stu-id="67bfb-149">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="67bfb-150">因此，零售商不必手动维护单独的页面体验。</span><span class="sxs-lookup"><span data-stu-id="67bfb-150">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="67bfb-151">例如，在下图中，某登录用户已经购买了出现在“热门 - 默认”列表中的黑色手表和棕色工作靴。</span><span class="sxs-lookup"><span data-stu-id="67bfb-151">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="67bfb-152">因此，用户将看到新产品，而不是这些产品，如“热门 - 个性化”列表中所示。</span><span class="sxs-lookup"><span data-stu-id="67bfb-152">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![应用个性化](./media/applypersonalization.png)

<span data-ttu-id="67bfb-154">要在 Commerce 站点构建器中将个性化应用到现有建议列表，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="67bfb-154">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="67bfb-155">打开一个包含产品集合模块的现有站点构建器页面。</span><span class="sxs-lookup"><span data-stu-id="67bfb-155">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="67bfb-156">在左侧导航窗格中，选择该产品集合模块。</span><span class="sxs-lookup"><span data-stu-id="67bfb-156">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="67bfb-157">在左侧导航窗格中，在 **产品** 下，选择列表。</span><span class="sxs-lookup"><span data-stu-id="67bfb-157">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="67bfb-158">在 **选择产品列表配置** 对话框，在 **类型** 下，选择列表类型。</span><span class="sxs-lookup"><span data-stu-id="67bfb-158">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="67bfb-159">选择 **应用个性化** 复选框，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="67bfb-159">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![将个性化应用于热门列表](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="67bfb-161">保存页面，完成编辑，然后发布。</span><span class="sxs-lookup"><span data-stu-id="67bfb-161">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="67bfb-162">页面发布后，登录用户将看到个性化的热门列表。</span><span class="sxs-lookup"><span data-stu-id="67bfb-162">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67bfb-163">其他资源</span><span class="sxs-lookup"><span data-stu-id="67bfb-163">Additional resources</span></span>

[<span data-ttu-id="67bfb-164">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="67bfb-164">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="67bfb-165">在 Dynamics 365 Commerce 环境中启用 Azure Data Lake Storage</span><span class="sxs-lookup"><span data-stu-id="67bfb-165">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="67bfb-166">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="67bfb-166">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="67bfb-167">启用“购买类似外观”建议</span><span class="sxs-lookup"><span data-stu-id="67bfb-167">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="67bfb-168">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="67bfb-168">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="67bfb-169">在 POS 中添加产品建议</span><span class="sxs-lookup"><span data-stu-id="67bfb-169">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="67bfb-170">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="67bfb-170">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="67bfb-171">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="67bfb-171">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="67bfb-172">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="67bfb-172">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="67bfb-173">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="67bfb-173">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="67bfb-174">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="67bfb-174">Product recommendations FAQ</span></span>](faq-recommendations.md)
