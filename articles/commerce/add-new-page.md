---
title: 添加新的站点页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中添加新的站点页面。
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
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797543"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="59479-103">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="59479-103">Add a new site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="59479-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中添加新的站点页面。</span><span class="sxs-lookup"><span data-stu-id="59479-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="59479-105">为站点创建模板和片段之后，下一步是开始创建使用这些模板和片段的页面。</span><span class="sxs-lookup"><span data-stu-id="59479-105">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="59479-106">首先，必须选择模板或布局，页面名称和页面 URL。</span><span class="sxs-lookup"><span data-stu-id="59479-106">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="59479-107">模板或布局</span><span class="sxs-lookup"><span data-stu-id="59479-107">Template or layout</span></span>

<span data-ttu-id="59479-108">可为新页面使用模板或布局。</span><span class="sxs-lookup"><span data-stu-id="59479-108">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="59479-109">有关详细信息，请参阅[模板和布局概述](templates-layouts-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="59479-109">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="59479-110">页面名称</span><span class="sxs-lookup"><span data-stu-id="59479-110">Page name</span></span>

<span data-ttu-id="59479-111">页面名称对于页面必须唯一。</span><span class="sxs-lookup"><span data-stu-id="59479-111">The page name must be unique to your page.</span></span> <span data-ttu-id="59479-112">应该具有描述性，以便您轻松找到，其他人可以知道页面的用途。</span><span class="sxs-lookup"><span data-stu-id="59479-112">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="59479-113">请仔细选择页面名称，因为以后不能更改。</span><span class="sxs-lookup"><span data-stu-id="59479-113">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="59479-114">页面 URL</span><span class="sxs-lookup"><span data-stu-id="59479-114">Page URL</span></span>

<span data-ttu-id="59479-115">提供了用于为新页面输入 URL 的选项。</span><span class="sxs-lookup"><span data-stu-id="59479-115">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="59479-116">创建页面时，可输入将用于构成完整 URL 的字符串。</span><span class="sxs-lookup"><span data-stu-id="59479-116">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="59479-117">此字符串称为相对 URL 或 URL 数据域。</span><span class="sxs-lookup"><span data-stu-id="59479-117">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="59479-118">然后基于 URL 数据域生成完整 URL，并将新页面分配给它。</span><span class="sxs-lookup"><span data-stu-id="59479-118">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="59479-119">可在以后发布页面前更改 URL 数据域。</span><span class="sxs-lookup"><span data-stu-id="59479-119">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="59479-120">有关详细信息，请参阅[创建页面 URL](create-page-URL.md)。</span><span class="sxs-lookup"><span data-stu-id="59479-120">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="59479-121">Dynamics 365 Commerce 分离 URL 和内容。</span><span class="sxs-lookup"><span data-stu-id="59479-121">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="59479-122">换句话说，可以创建不与 URL 关联的页面，也可以创建不与页面关联的 URL。</span><span class="sxs-lookup"><span data-stu-id="59479-122">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="59479-123">因此，可以为 URL 执行内容交还，并且不需要停机时间，而重定向更容易管理。</span><span class="sxs-lookup"><span data-stu-id="59479-123">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="59479-124">添加新页面</span><span class="sxs-lookup"><span data-stu-id="59479-124">Add a new page</span></span>

<span data-ttu-id="59479-125">若要向站点添加新站点页面，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="59479-125">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="59479-126">在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="59479-126">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="59479-127">选择 **新建页面**。</span><span class="sxs-lookup"><span data-stu-id="59479-127">Select **New Page**.</span></span>
1. <span data-ttu-id="59479-128">在 **新页面** 对话框中，选择一个模板，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="59479-128">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="59479-129">在 **页面名称** 字段中，输入页面名称（例如，**我的新页面**）。</span><span class="sxs-lookup"><span data-stu-id="59479-129">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="59479-130">在 **URL** 字段中，输入一个字符串（URL 数据域）完成该 URL（例如，**mynewpage**）。</span><span class="sxs-lookup"><span data-stu-id="59479-130">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="59479-131">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="59479-131">Select **OK**.</span></span> <span data-ttu-id="59479-132">将显示页面编辑器。</span><span class="sxs-lookup"><span data-stu-id="59479-132">The page editor appears.</span></span> <span data-ttu-id="59479-133">请注意，将根据您选择的模板自动向页面添加页眉和页脚。</span><span class="sxs-lookup"><span data-stu-id="59479-133">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="59479-134">在页面大纲中，选择 **主** 插槽，选择省略号按钮 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="59479-134">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="59479-135">选择 **容器**，然后选择 **确定**</span><span class="sxs-lookup"><span data-stu-id="59479-135">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="59479-136">选择 **流体容器**，选择省略号按钮，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="59479-136">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="59479-137">选择 **内容丰富块**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="59479-137">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="59479-138">选择 **内容丰富块**，选择省略号按钮，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="59479-138">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="59479-139">选择 **内容丰富块项**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="59479-139">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="59479-140">在右侧属性窗格中，选择 **段落**，然后在字段中，输入 **我的测试文本**。</span><span class="sxs-lookup"><span data-stu-id="59479-140">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="59479-141">选择 **保存**，然后选择 **完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="59479-141">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="59479-142">在 **注释** 字段中，输入 **添加的新页面**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="59479-142">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="59479-143">选择 **预览** 预览您的页面。</span><span class="sxs-lookup"><span data-stu-id="59479-143">Select **Preview** to preview your page.</span></span> <span data-ttu-id="59479-144">完成后，关闭预览标签页回到创作工具。</span><span class="sxs-lookup"><span data-stu-id="59479-144">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="59479-145">选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="59479-145">Select **Publish**.</span></span>
1. <span data-ttu-id="59479-146">在导航路径（面包屑导航）中，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="59479-146">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="59479-147">在左侧的导航窗格中，选择 **URL**。</span><span class="sxs-lookup"><span data-stu-id="59479-147">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="59479-148">在列表中找到并选择您的 URL (**mynewpage**)。</span><span class="sxs-lookup"><span data-stu-id="59479-148">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="59479-149">选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="59479-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59479-150">其他资源</span><span class="sxs-lookup"><span data-stu-id="59479-150">Additional resources</span></span>

[<span data-ttu-id="59479-151">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="59479-151">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="59479-152">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="59479-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="59479-153">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="59479-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="59479-154">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="59479-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="59479-155">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="59479-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="59479-156">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="59479-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="59479-157">验证页面内容的可访问性</span><span class="sxs-lookup"><span data-stu-id="59479-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="59479-158">基于 URL 参数创建动态电子商务页面</span><span class="sxs-lookup"><span data-stu-id="59479-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
