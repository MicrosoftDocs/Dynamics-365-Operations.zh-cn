---
title: 丰富产品页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中扩充产品页面。
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ef9e65b2027a41ca152afaf20ac2fb9a69cd9b96
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698134"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="2e69a-103">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="2e69a-103">Enrich a product page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2e69a-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中扩充产品页面。</span><span class="sxs-lookup"><span data-stu-id="2e69a-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2e69a-105">概览</span><span class="sxs-lookup"><span data-stu-id="2e69a-105">Overview</span></span>

<span data-ttu-id="2e69a-106">默认情况下，站点使用通用页面显示产品数据。</span><span class="sxs-lookup"><span data-stu-id="2e69a-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="2e69a-107">这种页面中包含有关产品和销售产品需要的控件的基本信息。</span><span class="sxs-lookup"><span data-stu-id="2e69a-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="2e69a-108">但是，可以使用更多图像或文本和 Retail Server 中的信息补充特定产品。</span><span class="sxs-lookup"><span data-stu-id="2e69a-108">However, you can supplement the information that comes from the Retail Server with additional images or text for a specific product.</span></span> <span data-ttu-id="2e69a-109">此过程称为扩充产品页。</span><span class="sxs-lookup"><span data-stu-id="2e69a-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="2e69a-110">许多情况下，希望使用产品的更多具体内容。</span><span class="sxs-lookup"><span data-stu-id="2e69a-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="2e69a-111">在创作工具中转到  **Retail** 时，将看到来自分配给站点的渠道的产品的列表。</span><span class="sxs-lookup"><span data-stu-id="2e69a-111">When you go to **Retail** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="2e69a-112">在此列表中，**已扩充**列指示是否已扩充了某个产品的产品页。</span><span class="sxs-lookup"><span data-stu-id="2e69a-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="2e69a-113">如果列中显示复选标记，说明产品有已扩充产品页。</span><span class="sxs-lookup"><span data-stu-id="2e69a-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="2e69a-114">如果不显示复选标记，说明对产品使用的是默认产品页和内容。</span><span class="sxs-lookup"><span data-stu-id="2e69a-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="2e69a-115">可通过在列表中选择产品名称预览已扩充产品页和未扩充产品页。</span><span class="sxs-lookup"><span data-stu-id="2e69a-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="2e69a-116">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="2e69a-116">Enrich a product page</span></span>

<span data-ttu-id="2e69a-117">若要扩充产品页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="2e69a-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="2e69a-118">在**站点**下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="2e69a-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2e69a-119">在左侧的导航窗格中，选择**产品**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="2e69a-120">选择没有已扩充产品页的任何产品。</span><span class="sxs-lookup"><span data-stu-id="2e69a-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="2e69a-121">在操作窗格上，选择**扩充产品页**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="2e69a-122">选择 **PDP-template**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="2e69a-123">在左侧的页面大纲树中，展开**主**插槽。</span><span class="sxs-lookup"><span data-stu-id="2e69a-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="2e69a-124">选择**主**插槽的省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2e69a-125">选择**容器 2**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="2e69a-126">选择**容器 2** 的省略号按钮，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="2e69a-127">选择**功能**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="2e69a-128">在右侧的属性窗格中**富文本**字段内，输入更新后的产品描述。</span><span class="sxs-lookup"><span data-stu-id="2e69a-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="2e69a-129">在**标题**字段中，输入标题文本，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="2e69a-130">选择**保存**，然后选择**签入**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-130">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="2e69a-131">在**注释**字段中，输入**已扩充产品**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="2e69a-132">选择**预览**预览扩充后的产品页。</span><span class="sxs-lookup"><span data-stu-id="2e69a-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="2e69a-133">完成后，关闭预览标签页回到创作工具。</span><span class="sxs-lookup"><span data-stu-id="2e69a-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="2e69a-134">选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="2e69a-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e69a-135">其他资源</span><span class="sxs-lookup"><span data-stu-id="2e69a-135">Additional resources</span></span>

[<span data-ttu-id="2e69a-136">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="2e69a-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="2e69a-137">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="2e69a-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2e69a-138">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="2e69a-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="2e69a-139">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="2e69a-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="2e69a-140">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="2e69a-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="2e69a-141">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="2e69a-141">Enrich a category landing page</span></span>](enrich-category-page.md)

