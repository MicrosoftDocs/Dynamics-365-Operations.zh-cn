---
title: 丰富产品页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中扩充产品页面。
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799029"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="0151a-103">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="0151a-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0151a-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中扩充产品页面。</span><span class="sxs-lookup"><span data-stu-id="0151a-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0151a-105">默认情况下，站点使用通用页面显示产品数据。</span><span class="sxs-lookup"><span data-stu-id="0151a-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="0151a-106">这种页面中包含有关产品和销售产品需要的控件的基本信息。</span><span class="sxs-lookup"><span data-stu-id="0151a-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="0151a-107">但是，可以使用特定产品的更多图像或文本补充来自 Commerce Scale Unit 的信息。</span><span class="sxs-lookup"><span data-stu-id="0151a-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="0151a-108">此过程称为扩充产品页。</span><span class="sxs-lookup"><span data-stu-id="0151a-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="0151a-109">许多情况下，希望使用产品的更多具体内容。</span><span class="sxs-lookup"><span data-stu-id="0151a-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="0151a-110">在创作工具中转到 **Retail 和 Commerce** 时，将看到来自分配给站点的渠道的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="0151a-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="0151a-111">在此列表中，**已扩充** 列指示是否已扩充了某个产品的产品页。</span><span class="sxs-lookup"><span data-stu-id="0151a-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="0151a-112">如果列中显示复选标记，说明产品有已扩充产品页。</span><span class="sxs-lookup"><span data-stu-id="0151a-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="0151a-113">如果不显示复选标记，说明对产品使用的是默认产品页和内容。</span><span class="sxs-lookup"><span data-stu-id="0151a-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="0151a-114">可通过在列表中选择产品名称预览已扩充产品页和未扩充产品页。</span><span class="sxs-lookup"><span data-stu-id="0151a-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="0151a-115">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="0151a-115">Enrich a product page</span></span>

<span data-ttu-id="0151a-116">若要扩充产品页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="0151a-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="0151a-117">在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="0151a-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0151a-118">在左侧的导航窗格中，选择 **产品**。</span><span class="sxs-lookup"><span data-stu-id="0151a-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="0151a-119">选择没有已扩充产品页的任何产品。</span><span class="sxs-lookup"><span data-stu-id="0151a-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="0151a-120">在操作窗格上，选择 **扩充产品页**。</span><span class="sxs-lookup"><span data-stu-id="0151a-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="0151a-121">选择 **PDP-template**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0151a-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="0151a-122">在左侧的页面大纲树中，展开 **主** 插槽。</span><span class="sxs-lookup"><span data-stu-id="0151a-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="0151a-123">选择 **主** 插槽的省略号按钮 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="0151a-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="0151a-124">选择 **容器 2**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0151a-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="0151a-125">选择 **容器 2** 的省略号按钮，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="0151a-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="0151a-126">选择 **功能**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0151a-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="0151a-127">在右侧的属性窗格中 **富文本** 字段内，输入更新后的产品描述。</span><span class="sxs-lookup"><span data-stu-id="0151a-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="0151a-128">在 **标题** 字段中，输入标题文本，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0151a-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="0151a-129">选择 **保存**，然后选择 **完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="0151a-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="0151a-130">在 **注释** 字段中，输入 **已扩充产品**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="0151a-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="0151a-131">选择 **预览** 预览扩充后的产品页。</span><span class="sxs-lookup"><span data-stu-id="0151a-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="0151a-132">完成后，关闭预览标签页回到创作工具。</span><span class="sxs-lookup"><span data-stu-id="0151a-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="0151a-133">选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="0151a-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0151a-134">其他资源</span><span class="sxs-lookup"><span data-stu-id="0151a-134">Additional resources</span></span>

[<span data-ttu-id="0151a-135">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="0151a-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="0151a-136">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="0151a-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="0151a-137">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="0151a-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="0151a-138">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="0151a-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="0151a-139">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="0151a-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="0151a-140">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="0151a-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="0151a-141">验证页面内容的可访问性</span><span class="sxs-lookup"><span data-stu-id="0151a-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="0151a-142">基于 URL 参数创建动态电子商务页面</span><span class="sxs-lookup"><span data-stu-id="0151a-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
