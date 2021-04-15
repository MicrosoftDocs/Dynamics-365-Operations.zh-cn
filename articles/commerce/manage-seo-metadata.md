---
title: 管理 SEO 元数据
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中管理搜索引擎优化 (SEO) 元数据。
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
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794203"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="7fec0-103">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="7fec0-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7fec0-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中管理搜索引擎优化 (SEO) 元数据。</span><span class="sxs-lookup"><span data-stu-id="7fec0-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7fec0-105">可以使用站点地图和页面元数据管理站点的 SEO 元数据。</span><span class="sxs-lookup"><span data-stu-id="7fec0-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="7fec0-106">站点地图</span><span class="sxs-lookup"><span data-stu-id="7fec0-106">Site maps</span></span>

<span data-ttu-id="7fec0-107">站点地图是网站中所有页面的 XML 格式机器可识别列表。</span><span class="sxs-lookup"><span data-stu-id="7fec0-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="7fec0-108">其供搜索引擎使用，所以可以改善站点的搜索结果。</span><span class="sxs-lookup"><span data-stu-id="7fec0-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="7fec0-109">站点地图可以由搜索引擎手动消化，也可以通过 robots.txt 文件发布。</span><span class="sxs-lookup"><span data-stu-id="7fec0-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="7fec0-110">Dynamics 365 Commerce 支持自动生成站点地图。</span><span class="sxs-lookup"><span data-stu-id="7fec0-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="7fec0-111">发布和取消发布页面时，将自动更新站点地图。</span><span class="sxs-lookup"><span data-stu-id="7fec0-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="7fec0-112">开启站点地图生成</span><span class="sxs-lookup"><span data-stu-id="7fec0-112">Turn on site map generation</span></span>

1. <span data-ttu-id="7fec0-113">登录创作工具。</span><span class="sxs-lookup"><span data-stu-id="7fec0-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="7fec0-114">在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="7fec0-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="7fec0-115">在左侧的导航窗格中，选择 **站点管理**。</span><span class="sxs-lookup"><span data-stu-id="7fec0-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="7fec0-116">确保已开启 **启用站点地图** 选项。</span><span class="sxs-lookup"><span data-stu-id="7fec0-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="7fec0-117">页面元数据</span><span class="sxs-lookup"><span data-stu-id="7fec0-117">Page metadata</span></span>

<span data-ttu-id="7fec0-118">Dynamics 365 Commerce 允许您管理单个页面的 SEO 元数据。</span><span class="sxs-lookup"><span data-stu-id="7fec0-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="7fec0-119">可在页面容器的 **SEO 属性** 部分中查看和修改这些信息。</span><span class="sxs-lookup"><span data-stu-id="7fec0-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="7fec0-120">支持以下 SEO 元数据属性：</span><span class="sxs-lookup"><span data-stu-id="7fec0-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="7fec0-121">称谓</span><span class="sxs-lookup"><span data-stu-id="7fec0-121">Title</span></span>
- <span data-ttu-id="7fec0-122">说明</span><span class="sxs-lookup"><span data-stu-id="7fec0-122">Description</span></span>
- <span data-ttu-id="7fec0-123">SEO 关键字</span><span class="sxs-lookup"><span data-stu-id="7fec0-123">SEO keywords</span></span>
- <span data-ttu-id="7fec0-124">Aria 标签</span><span class="sxs-lookup"><span data-stu-id="7fec0-124">Aria labels</span></span>
- <span data-ttu-id="7fec0-125">noindex</span><span class="sxs-lookup"><span data-stu-id="7fec0-125">noindex</span></span>
- <span data-ttu-id="7fec0-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="7fec0-126">nofollow</span></span>
- <span data-ttu-id="7fec0-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="7fec0-127">noarchive</span></span>
- <span data-ttu-id="7fec0-128">nocache</span><span class="sxs-lookup"><span data-stu-id="7fec0-128">nocache</span></span>
- <span data-ttu-id="7fec0-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="7fec0-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="7fec0-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="7fec0-130">nosnippet</span></span>
- <span data-ttu-id="7fec0-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="7fec0-131">noImageIndex</span></span>
- <span data-ttu-id="7fec0-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="7fec0-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="7fec0-133">修改页面元数据</span><span class="sxs-lookup"><span data-stu-id="7fec0-133">Modify page metadata</span></span>

<span data-ttu-id="7fec0-134">若要修改页面元数据，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="7fec0-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="7fec0-135">在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="7fec0-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="7fec0-136">在左侧的导航窗格中，选择 **页面**。</span><span class="sxs-lookup"><span data-stu-id="7fec0-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="7fec0-137">选择主页在页面编辑器中将其打开。</span><span class="sxs-lookup"><span data-stu-id="7fec0-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="7fec0-138">在命令栏中，选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="7fec0-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="7fec0-139">在右侧的属性窗格中，展开 **默认元数据**。</span><span class="sxs-lookup"><span data-stu-id="7fec0-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="7fec0-140">若要添加新的元标记，请选择 **添加**，然后在字段中输入标记。</span><span class="sxs-lookup"><span data-stu-id="7fec0-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="7fec0-141">若要删除现有元标记，请选择其右侧的废纸篓符合。</span><span class="sxs-lookup"><span data-stu-id="7fec0-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="7fec0-142">选择 **保存**，然后选择 **完成编辑**。</span><span class="sxs-lookup"><span data-stu-id="7fec0-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="7fec0-143">在 **注释** 字段中，输入 **更新的元标记**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="7fec0-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="7fec0-144">选择 **预览** 预览您的页面。</span><span class="sxs-lookup"><span data-stu-id="7fec0-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="7fec0-145">完成后，关闭预览标签页回到创作工具。</span><span class="sxs-lookup"><span data-stu-id="7fec0-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="7fec0-146">选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="7fec0-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fec0-147">其他资源</span><span class="sxs-lookup"><span data-stu-id="7fec0-147">Additional resources</span></span>

[<span data-ttu-id="7fec0-148">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="7fec0-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="7fec0-149">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="7fec0-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="7fec0-150">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="7fec0-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="7fec0-151">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="7fec0-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="7fec0-152">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="7fec0-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="7fec0-153">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="7fec0-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="7fec0-154">验证页面内容的可访问性</span><span class="sxs-lookup"><span data-stu-id="7fec0-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="7fec0-155">基于 URL 参数创建动态电子商务页面</span><span class="sxs-lookup"><span data-stu-id="7fec0-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
