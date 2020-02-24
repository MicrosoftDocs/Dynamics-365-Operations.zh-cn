---
title: 管理 SEO 元数据
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中管理搜索引擎优化 (SEO) 元数据。
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
ms.openlocfilehash: 1e7da7bf5c473746413e92babfa943f546b7724d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003456"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="575da-103">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="575da-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="575da-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中管理搜索引擎优化 (SEO) 元数据。</span><span class="sxs-lookup"><span data-stu-id="575da-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="575da-105">概览</span><span class="sxs-lookup"><span data-stu-id="575da-105">Overview</span></span>

<span data-ttu-id="575da-106">可以使用站点地图和页面元数据管理站点的 SEO 元数据。</span><span class="sxs-lookup"><span data-stu-id="575da-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="575da-107">站点地图</span><span class="sxs-lookup"><span data-stu-id="575da-107">Site maps</span></span>

<span data-ttu-id="575da-108">站点地图是网站中所有页面的 XML 格式机器可识别列表。</span><span class="sxs-lookup"><span data-stu-id="575da-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="575da-109">其供搜索引擎使用，所以可以改善站点的搜索结果。</span><span class="sxs-lookup"><span data-stu-id="575da-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="575da-110">站点地图可以由搜索引擎手动消化，也可以通过 robots.txt 文件发布。</span><span class="sxs-lookup"><span data-stu-id="575da-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="575da-111">Dynamics 365 Commerce 支持自动生成站点地图。</span><span class="sxs-lookup"><span data-stu-id="575da-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="575da-112">发布和取消发布页面时，将自动更新站点地图。</span><span class="sxs-lookup"><span data-stu-id="575da-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="575da-113">开启站点地图生成</span><span class="sxs-lookup"><span data-stu-id="575da-113">Turn on site map generation</span></span>

1. <span data-ttu-id="575da-114">登录创作工具。</span><span class="sxs-lookup"><span data-stu-id="575da-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="575da-115">在**站点**下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="575da-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="575da-116">在左侧的导航窗格中，选择**站点管理**。</span><span class="sxs-lookup"><span data-stu-id="575da-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="575da-117">确保已开启**启用站点地图**选项。</span><span class="sxs-lookup"><span data-stu-id="575da-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="575da-118">页面元数据</span><span class="sxs-lookup"><span data-stu-id="575da-118">Page metadata</span></span>

<span data-ttu-id="575da-119">Dynamics 365 Commerce 允许您管理单个页面的 SEO 元数据。</span><span class="sxs-lookup"><span data-stu-id="575da-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="575da-120">可在页面容器的 **SEO 属性**部分中查看和修改这些信息。</span><span class="sxs-lookup"><span data-stu-id="575da-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="575da-121">支持以下 SEO 元数据属性：</span><span class="sxs-lookup"><span data-stu-id="575da-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="575da-122">称谓</span><span class="sxs-lookup"><span data-stu-id="575da-122">Title</span></span>
- <span data-ttu-id="575da-123">说明</span><span class="sxs-lookup"><span data-stu-id="575da-123">Description</span></span>
- <span data-ttu-id="575da-124">SEO 关键字</span><span class="sxs-lookup"><span data-stu-id="575da-124">SEO keywords</span></span>
- <span data-ttu-id="575da-125">Aria 标签</span><span class="sxs-lookup"><span data-stu-id="575da-125">Aria labels</span></span>
- <span data-ttu-id="575da-126">noindex</span><span class="sxs-lookup"><span data-stu-id="575da-126">noindex</span></span>
- <span data-ttu-id="575da-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="575da-127">nofollow</span></span>
- <span data-ttu-id="575da-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="575da-128">noarchive</span></span>
- <span data-ttu-id="575da-129">nocache</span><span class="sxs-lookup"><span data-stu-id="575da-129">nocache</span></span>
- <span data-ttu-id="575da-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="575da-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="575da-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="575da-131">nosnippet</span></span>
- <span data-ttu-id="575da-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="575da-132">noImageIndex</span></span>
- <span data-ttu-id="575da-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="575da-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="575da-134">修改页面元数据</span><span class="sxs-lookup"><span data-stu-id="575da-134">Modify page metadata</span></span>

<span data-ttu-id="575da-135">若要修改页面元数据，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="575da-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="575da-136">在**站点**下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="575da-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="575da-137">在左侧的导航窗格中，选择**页面**。</span><span class="sxs-lookup"><span data-stu-id="575da-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="575da-138">选择主页在页面编辑器中将其打开。</span><span class="sxs-lookup"><span data-stu-id="575da-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="575da-139">在操作窗格上，选择**签出**。</span><span class="sxs-lookup"><span data-stu-id="575da-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="575da-140">在右侧的属性窗格中，展开**默认元数据**。</span><span class="sxs-lookup"><span data-stu-id="575da-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="575da-141">若要添加新的元标记，请选择**添加**，然后在字段中输入标记。</span><span class="sxs-lookup"><span data-stu-id="575da-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="575da-142">若要删除现有元标记，请选择其右侧的废纸篓符合。</span><span class="sxs-lookup"><span data-stu-id="575da-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="575da-143">选择**保存**，然后选择**签入**。</span><span class="sxs-lookup"><span data-stu-id="575da-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="575da-144">在**注释**字段中，输入**更新的元标记**，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="575da-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="575da-145">选择**预览**预览您的页面。</span><span class="sxs-lookup"><span data-stu-id="575da-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="575da-146">完成后，关闭预览标签页回到创作工具。</span><span class="sxs-lookup"><span data-stu-id="575da-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="575da-147">选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="575da-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="575da-148">其他资源</span><span class="sxs-lookup"><span data-stu-id="575da-148">Additional resources</span></span>

[<span data-ttu-id="575da-149">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="575da-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="575da-150">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="575da-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="575da-151">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="575da-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="575da-152">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="575da-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="575da-153">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="575da-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="575da-154">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="575da-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="575da-155">验证页面内容可访问性</span><span class="sxs-lookup"><span data-stu-id="575da-155">Verify page content accessibility</span></span>](verify-accessibility.md)
