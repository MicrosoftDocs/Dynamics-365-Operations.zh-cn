---
title: 雇用个性化产品建议
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中让个性化产品建议可以为客户所用。
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
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
ms.openlocfilehash: bdb56a1f45cdea1832bd269502e534efdb207b03
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127897"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="af9df-103">启用个性化建议</span><span class="sxs-lookup"><span data-stu-id="af9df-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="af9df-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中让个性化产品建议可以为客户所用。</span><span class="sxs-lookup"><span data-stu-id="af9df-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="af9df-105">概览</span><span class="sxs-lookup"><span data-stu-id="af9df-105">Overview</span></span>

<span data-ttu-id="af9df-106">在 Dynamics 365 Commerce 中，零售商可以提供个性化的产品建议（也称为个性化）。</span><span class="sxs-lookup"><span data-stu-id="af9df-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="af9df-107">通过这种方式，可以将个性化的建议引入到在线和销售点 (POS) 的客户体验中。</span><span class="sxs-lookup"><span data-stu-id="af9df-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="af9df-108">当个性化功能打开时，系统可以将用户的购买和产品信息相关联，以生成个性化的产品建议。</span><span class="sxs-lookup"><span data-stu-id="af9df-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="af9df-109">个性化的先决条件</span><span class="sxs-lookup"><span data-stu-id="af9df-109">Personalization prerequisites</span></span>

<span data-ttu-id="af9df-110">在向客户提供个性化的产品建议之前，请注意，仅支持为已将存储迁移到 Azure Data Lake Store 的 Commerce 用户提供产品建议。</span><span class="sxs-lookup"><span data-stu-id="af9df-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="af9df-111">零售商必须先[打开产品建议](enable-product-recommendations.md)，然后客户才能够收到个性化产品建议。</span><span class="sxs-lookup"><span data-stu-id="af9df-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="af9df-112">通过打开产品建议，您还可以打开个性化。</span><span class="sxs-lookup"><span data-stu-id="af9df-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="af9df-113">但是，如果关闭个性化，不会关闭其他类型的产品建议。</span><span class="sxs-lookup"><span data-stu-id="af9df-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="af9df-114">有关产品建议的详细信息，请参阅[产品建议概述](product-recommendations.md)。</span><span class="sxs-lookup"><span data-stu-id="af9df-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="af9df-115">打开个性化</span><span class="sxs-lookup"><span data-stu-id="af9df-115">Turn on personalization</span></span>

<span data-ttu-id="af9df-116">若要打开个性化，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="af9df-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="af9df-117">转到 **Retail 和 Commerce \> 产品建议 \> 建议参数**。</span><span class="sxs-lookup"><span data-stu-id="af9df-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="af9df-118">在 Retail 共享参数列表中，选择**建议列表**。</span><span class="sxs-lookup"><span data-stu-id="af9df-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="af9df-119">将**启用个性化**选项设置为**是**。</span><span class="sxs-lookup"><span data-stu-id="af9df-119">Set the **Enable personalization** option to **Yes**.</span></span>

![打开个性化](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="af9df-121">打开个性化时，将启动生成个性化产品建议列表的过程。</span><span class="sxs-lookup"><span data-stu-id="af9df-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="af9df-122">这些列表最多可能需要一天时间完成在线以及在 POS 上提供和显示。</span><span class="sxs-lookup"><span data-stu-id="af9df-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="af9df-123">个性化列表</span><span class="sxs-lookup"><span data-stu-id="af9df-123">Personalized lists</span></span>

<span data-ttu-id="af9df-124">除了允许现有的计算机生成的列表的个性化外，建议服务还允许在线和 POS 上的产品发现体验的个性化。</span><span class="sxs-lookup"><span data-stu-id="af9df-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="af9df-125">打开个性化后，零售商可以在线向购买者显示个性化的“为您推荐”列表或在 POS 终端上显示“为客户推荐”列表。</span><span class="sxs-lookup"><span data-stu-id="af9df-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="af9df-126">此外，零售商可以将个性化应用于现有产品建议列表，并为经过身份验证的用户提供一般数据保护条例 (GDPR) 退出体验。</span><span class="sxs-lookup"><span data-stu-id="af9df-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="af9df-127">如果关闭个性化，还将关闭这些功能。</span><span class="sxs-lookup"><span data-stu-id="af9df-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="af9df-128">在线“为您推荐”列表</span><span class="sxs-lookup"><span data-stu-id="af9df-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="af9df-129">“为您推荐”列表是一个人工智能机器学习 (AI-ML) 列表，它向经过身份验证的用户显示建议产品的个性化列表。</span><span class="sxs-lookup"><span data-stu-id="af9df-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="af9df-130">此列表基于用户的全渠道购买历史记录。</span><span class="sxs-lookup"><span data-stu-id="af9df-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="af9df-131">个性化建议会随着用户进行更多购买而动态更新。</span><span class="sxs-lookup"><span data-stu-id="af9df-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="af9df-132">这种类型的列表还支持类别筛选，以便零售商可以根据导航层次结构显示首选商品。</span><span class="sxs-lookup"><span data-stu-id="af9df-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="af9df-133">必须满足以下用户要求，“为您推荐”列表才可以出现在任何电子商务页面上：</span><span class="sxs-lookup"><span data-stu-id="af9df-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="af9df-134">用户必须登录。</span><span class="sxs-lookup"><span data-stu-id="af9df-134">Users must be signed in.</span></span> <span data-ttu-id="af9df-135">匿名用户将看不到个性化推荐。</span><span class="sxs-lookup"><span data-stu-id="af9df-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="af9df-136">用户必须在其帐户中至少进行了一次购买。</span><span class="sxs-lookup"><span data-stu-id="af9df-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="af9df-137">用户必须选择接收个性化建议。</span><span class="sxs-lookup"><span data-stu-id="af9df-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="af9df-138">下图显示了在线商店页面上的“为您推荐”列表的示例。</span><span class="sxs-lookup"><span data-stu-id="af9df-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![在线“为您推荐”列表](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="af9df-140">POS 上的“为客户推荐”列表</span><span class="sxs-lookup"><span data-stu-id="af9df-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="af9df-141">为了增强客户服务体验，零售商可以通过添加有上下文的“为客户推荐”列表来个性化现有的客户详细信息页面。</span><span class="sxs-lookup"><span data-stu-id="af9df-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="af9df-142">下图显示了 POS 终端上的“为客户推荐”列表的示例。</span><span class="sxs-lookup"><span data-stu-id="af9df-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![POS 上的“为客户推荐”列表](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="af9df-144">将个性化应用于现有建议列表</span><span class="sxs-lookup"><span data-stu-id="af9df-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="af9df-145">零售商可以将个性化应用于现有建议列表，例如“新品”、“热门”、“最畅销”、“用户也喜欢”和“人气组合”。</span><span class="sxs-lookup"><span data-stu-id="af9df-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="af9df-146">将个性化应用于现有列表后，登录用户先前购买的商品将从这些列表中删除。</span><span class="sxs-lookup"><span data-stu-id="af9df-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="af9df-147">对于匿名用户和选择不接收个性化建议的用户，将显示现有列表的默认版本。</span><span class="sxs-lookup"><span data-stu-id="af9df-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="af9df-148">因此，零售商不必手动维护单独的页面体验。</span><span class="sxs-lookup"><span data-stu-id="af9df-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="af9df-149">例如，在下图中，某登录用户已经购买了出现在“热门 - 默认”列表中的黑色手表和棕色工作靴。</span><span class="sxs-lookup"><span data-stu-id="af9df-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="af9df-150">因此，用户将看到新产品，而不是这些产品，如“热门 - 个性化”列表中所示。</span><span class="sxs-lookup"><span data-stu-id="af9df-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![应用个性化](./media/applypersonalization.png)

<span data-ttu-id="af9df-152">要在 Commerce 站点构建器中将个性化应用到现有建议列表，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="af9df-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="af9df-153">打开一个包含产品集合模块的现有站点构建器页面。</span><span class="sxs-lookup"><span data-stu-id="af9df-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="af9df-154">在左侧导航窗格中，选择该产品集合模块。</span><span class="sxs-lookup"><span data-stu-id="af9df-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="af9df-155">在左侧导航窗格中，在**产品**下，选择列表。</span><span class="sxs-lookup"><span data-stu-id="af9df-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="af9df-156">在**选择产品列表配置**对话框，在**类型**下，选择列表类型。</span><span class="sxs-lookup"><span data-stu-id="af9df-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="af9df-157">选择**应用个性化**复选框，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="af9df-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![将个性化应用于热门列表](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="af9df-159">保存页面，完成编辑，然后发布。</span><span class="sxs-lookup"><span data-stu-id="af9df-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="af9df-160">页面发布后，登录用户将看到个性化的热门列表。</span><span class="sxs-lookup"><span data-stu-id="af9df-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af9df-161">其他资源</span><span class="sxs-lookup"><span data-stu-id="af9df-161">Additional resources</span></span>

[<span data-ttu-id="af9df-162">产品建议概览</span><span class="sxs-lookup"><span data-stu-id="af9df-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="af9df-163">在 Dynamics 365 Commerce 环境中启用 ADLS</span><span class="sxs-lookup"><span data-stu-id="af9df-163">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="af9df-164">启用产品建议</span><span class="sxs-lookup"><span data-stu-id="af9df-164">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="af9df-165">选择退出个性化产品建议</span><span class="sxs-lookup"><span data-stu-id="af9df-165">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="af9df-166">向电子商务站点添加建议列表</span><span class="sxs-lookup"><span data-stu-id="af9df-166">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="af9df-167">在 POS 中添加产品建议</span><span class="sxs-lookup"><span data-stu-id="af9df-167">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="af9df-168">向交易记录屏幕添加建议</span><span class="sxs-lookup"><span data-stu-id="af9df-168">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="af9df-169">调整 AI-ML 建议结果</span><span class="sxs-lookup"><span data-stu-id="af9df-169">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="af9df-170">手动创建策划的建议</span><span class="sxs-lookup"><span data-stu-id="af9df-170">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="af9df-171">使用演示数据创建建议</span><span class="sxs-lookup"><span data-stu-id="af9df-171">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="af9df-172">产品建议常见问题</span><span class="sxs-lookup"><span data-stu-id="af9df-172">Product recommendations FAQ</span></span>](faq-recommendations.md)
