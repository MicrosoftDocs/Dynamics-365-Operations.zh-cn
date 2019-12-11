---
title: 保存、预览和发布页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中保存、预览和发布页面。
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
ms.openlocfilehash: 8c1b82b1b8423c63d442ee581ed0cc8789ee63fd
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697880"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="730b5-103">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="730b5-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="730b5-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中保存、预览和发布页面。</span><span class="sxs-lookup"><span data-stu-id="730b5-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="730b5-105">保存页面</span><span class="sxs-lookup"><span data-stu-id="730b5-105">Save a page</span></span>

<span data-ttu-id="730b5-106">若要保存页面，必须先将其签出给您自己，然后在页面编辑器中打开。</span><span class="sxs-lookup"><span data-stu-id="730b5-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="730b5-107">应该在修改页面之后立即保存页面，以帮助确保存储更改。</span><span class="sxs-lookup"><span data-stu-id="730b5-107">You should save a page immediately after you modify it, to help guarantee that your changes are stored.</span></span>

<span data-ttu-id="730b5-108">保存页面时，更改仅对您显示。</span><span class="sxs-lookup"><span data-stu-id="730b5-108">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="730b5-109">保存操作应该主要用于在页面尚未准备好签入时存储更改。</span><span class="sxs-lookup"><span data-stu-id="730b5-109">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="730b5-110">修改完页面后，建议将其签入，这样就可以对其他人显示更改。</span><span class="sxs-lookup"><span data-stu-id="730b5-110">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="730b5-111">此时，其他必须修改页面的用户也可以签出该页面。</span><span class="sxs-lookup"><span data-stu-id="730b5-111">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="730b5-112">预览页面</span><span class="sxs-lookup"><span data-stu-id="730b5-112">Preview a page</span></span>

<span data-ttu-id="730b5-113">创作工具提供两种预览功能：页面编辑器中的“所见即所得”(WYSIWYG) 预览窗格和单独的预览窗口。</span><span class="sxs-lookup"><span data-stu-id="730b5-113">The authoring tool offers two kinds of preview features: a "what you see is what you get" (WYSIWYG) preview pane in the page editor and a separate preview window.</span></span>

<span data-ttu-id="730b5-114">使用页面编辑器时，中央窗格中将显示“所见即所得”(WYSIWYG) 预览。</span><span class="sxs-lookup"><span data-stu-id="730b5-114">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="730b5-115">只要保存页面，都将自动更新此预览。</span><span class="sxs-lookup"><span data-stu-id="730b5-115">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="730b5-116">也可以通过选择命令栏中的**刷新**手动更新。</span><span class="sxs-lookup"><span data-stu-id="730b5-116">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="730b5-117">WYSIWYG 预览呈现的页面和站点用户看到的完全一样，但是创作帮助器在顶部显示。</span><span class="sxs-lookup"><span data-stu-id="730b5-117">The WYSIWYG preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="730b5-118">修改完页面之后，您可能希望预览页面以查看客户将看到的效果。</span><span class="sxs-lookup"><span data-stu-id="730b5-118">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="730b5-119">若要预览页面，请在命令栏中选择**预览**。</span><span class="sxs-lookup"><span data-stu-id="730b5-119">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="730b5-120">将在一个单独的浏览器窗口中显示预览。</span><span class="sxs-lookup"><span data-stu-id="730b5-120">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="730b5-121">预览窗口中显示的页面和站点用户将看到的完全一样。</span><span class="sxs-lookup"><span data-stu-id="730b5-121">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="730b5-122">可以调整窗口大小以确保所有查看端口中都正确显示响应模块。</span><span class="sxs-lookup"><span data-stu-id="730b5-122">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="730b5-123">需要身份验证和正确的权限才能预览未发布的内容。</span><span class="sxs-lookup"><span data-stu-id="730b5-123">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="730b5-124">因此，如果与某用户共享预览的 URL，该用户必须具有正确的权限才能访问内容。</span><span class="sxs-lookup"><span data-stu-id="730b5-124">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="730b5-125">发布页面</span><span class="sxs-lookup"><span data-stu-id="730b5-125">Publish a page</span></span>

<span data-ttu-id="730b5-126">页面准备就绪之后，下一步是发布，以便外部用户查看内容。</span><span class="sxs-lookup"><span data-stu-id="730b5-126">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="730b5-127">页面只有在签入后，才能发布。</span><span class="sxs-lookup"><span data-stu-id="730b5-127">Before you can publish a page, you must check it in.</span></span>

<span data-ttu-id="730b5-128">可从页面检查器或页面编辑器发布和取消发布页面。</span><span class="sxs-lookup"><span data-stu-id="730b5-128">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="730b5-129">页面检查器显示页面列表，并允许执行批量操作。</span><span class="sxs-lookup"><span data-stu-id="730b5-129">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="730b5-130">页面编辑器只能用于发布或取消发布其中打开的单个页面。</span><span class="sxs-lookup"><span data-stu-id="730b5-130">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="730b5-131">若要从页面检查器发布一个或多个页面，请选择页面，确保已签入这些页面，然后在命令栏中选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="730b5-131">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="730b5-132">将发布这些页面，而您会在创作工具中收到有关此操作的通知。</span><span class="sxs-lookup"><span data-stu-id="730b5-132">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="730b5-133">从页面编辑器发布单个页面的过程相似。</span><span class="sxs-lookup"><span data-stu-id="730b5-133">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="730b5-134">在页面编辑器中打开页面后，确保已签入该页面，然后在命令栏中选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="730b5-134">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="730b5-135">将发布此页面，而您会收到有关此操作的通知。</span><span class="sxs-lookup"><span data-stu-id="730b5-135">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="730b5-136">发布页面时，仅发布页面内容。</span><span class="sxs-lookup"><span data-stu-id="730b5-136">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="730b5-137">仅当为该页面关联了 URL，您和其他用户才可以转到该页面并查看。</span><span class="sxs-lookup"><span data-stu-id="730b5-137">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="730b5-138">URL 必须单独发布。</span><span class="sxs-lookup"><span data-stu-id="730b5-138">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="730b5-139">必须已经发布了页面引用的所有图像或片段，才能发布页面。</span><span class="sxs-lookup"><span data-stu-id="730b5-139">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="730b5-140">保存、预览和发布主页</span><span class="sxs-lookup"><span data-stu-id="730b5-140">Save, preview, and publish a home page</span></span>

<span data-ttu-id="730b5-141">若要保存，预览和发布主页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="730b5-141">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="730b5-142">在**站点**下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="730b5-142">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="730b5-143">在左侧的导航窗格中，选择**页面**。</span><span class="sxs-lookup"><span data-stu-id="730b5-143">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="730b5-144">转到并选择主页在页面编辑器中将其打开。</span><span class="sxs-lookup"><span data-stu-id="730b5-144">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="730b5-145">选择**签出**。</span><span class="sxs-lookup"><span data-stu-id="730b5-145">Select **Check Out**.</span></span>
1. <span data-ttu-id="730b5-146">根据需要修改页面。</span><span class="sxs-lookup"><span data-stu-id="730b5-146">Modify the page as you require.</span></span>
1. <span data-ttu-id="730b5-147">选择**保存**，然后选择**签入**。</span><span class="sxs-lookup"><span data-stu-id="730b5-147">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="730b5-148">在**注释**字段中，输入有关您所做更改的注释，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="730b5-148">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="730b5-149">选择**预览**预览您的页面。</span><span class="sxs-lookup"><span data-stu-id="730b5-149">Select **Preview** to preview your page.</span></span> <span data-ttu-id="730b5-150">完成后，关闭预览标签页回到创作工具。</span><span class="sxs-lookup"><span data-stu-id="730b5-150">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="730b5-151">选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="730b5-151">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="730b5-152">发布 URL</span><span class="sxs-lookup"><span data-stu-id="730b5-152">Publish a URL</span></span>

<span data-ttu-id="730b5-153">若要发布 URL，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="730b5-153">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="730b5-154">在**站点**下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="730b5-154">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="730b5-155">在左侧的导航窗格中，选择 **URL**。</span><span class="sxs-lookup"><span data-stu-id="730b5-155">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="730b5-156">找到并选择要发布的 URL。</span><span class="sxs-lookup"><span data-stu-id="730b5-156">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="730b5-157">在命令栏中，选择**发布**。</span><span class="sxs-lookup"><span data-stu-id="730b5-157">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="730b5-158">其他资源</span><span class="sxs-lookup"><span data-stu-id="730b5-158">Additional resources</span></span>

[<span data-ttu-id="730b5-159">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="730b5-159">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="730b5-160">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="730b5-160">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="730b5-161">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="730b5-161">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="730b5-162">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="730b5-162">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="730b5-163">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="730b5-163">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="730b5-164">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="730b5-164">Enrich a category landing page</span></span>](enrich-category-page.md)

