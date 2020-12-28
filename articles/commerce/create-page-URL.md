---
title: 创建页面 URL
description: 此主题介绍有关在站点中创建页面 URL 的基本概念和过程。
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 588cbedb077fab0663d3d62fc4a8b8ed915635b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410443"
---
# <a name="create-a-page-url"></a><span data-ttu-id="fdefb-103">创建页面 URL</span><span class="sxs-lookup"><span data-stu-id="fdefb-103">Create a page URL</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fdefb-104">此主题介绍有关在站点中创建页面 URL 的基本概念和过程。</span><span class="sxs-lookup"><span data-stu-id="fdefb-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="fdefb-105">概览</span><span class="sxs-lookup"><span data-stu-id="fdefb-105">Overview</span></span>

<span data-ttu-id="fdefb-106">指向站点中的页面的完全或绝对 URL 包含以下独有部分。</span><span class="sxs-lookup"><span data-stu-id="fdefb-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="fdefb-107">例如，URL `https://www.contoso.com/en-us/contactus` 具有以下部分：</span><span class="sxs-lookup"><span data-stu-id="fdefb-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="fdefb-108">`https://www.contoso.com` – HTTP 协议和站点的域。</span><span class="sxs-lookup"><span data-stu-id="fdefb-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="fdefb-109">`/en-us` – 站点的语言路径。</span><span class="sxs-lookup"><span data-stu-id="fdefb-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="fdefb-110">`/contactus` – **联系我们** 页面的相对 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="fdefb-111">相对 URL 也称为 URL *数据域*。</span><span class="sxs-lookup"><span data-stu-id="fdefb-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="fdefb-112">设置站点时，将建立站点的域和可选语言路径。</span><span class="sxs-lookup"><span data-stu-id="fdefb-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="fdefb-113">可通过站点的设置中的在线商店页面向站点添加更多域和语言路径。</span><span class="sxs-lookup"><span data-stu-id="fdefb-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="fdefb-114">页面的 URL 数据域在站点创作环境中以独立实体的形式存在。</span><span class="sxs-lookup"><span data-stu-id="fdefb-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="fdefb-115">页面 URL 中包含两个部分：表示 URL 数据域的名称，和站点或外部站点上的页面的指针。</span><span class="sxs-lookup"><span data-stu-id="fdefb-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="fdefb-116">也可以将页面 URL 配置为到充当站点或外部站点上另一个页面的重定向。</span><span class="sxs-lookup"><span data-stu-id="fdefb-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="fdefb-117">创建页面 URL</span><span class="sxs-lookup"><span data-stu-id="fdefb-117">Create a page URL</span></span>

<span data-ttu-id="fdefb-118">可通过两种方法创建页面 URL：</span><span class="sxs-lookup"><span data-stu-id="fdefb-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="fdefb-119">自动，在创建页面时</span><span class="sxs-lookup"><span data-stu-id="fdefb-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="fdefb-120">手动，从 **URL** 页面</span><span class="sxs-lookup"><span data-stu-id="fdefb-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="fdefb-121">创建页面时创建页面 URL</span><span class="sxs-lookup"><span data-stu-id="fdefb-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="fdefb-122">如果在创建新页面时在 **URL** 字段中提供名称，将在 **URL** 页面中自动创建指向该页面的页面 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="fdefb-123">发布 URL 及其指向的页面后，站点用户（即您的客户）可访问与该 URL 关联的页面。</span><span class="sxs-lookup"><span data-stu-id="fdefb-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="fdefb-124">如果发布 URL 但不发布其指向的页面，则站点用户在尝试访问该页面时，将遇到 404 错误。</span><span class="sxs-lookup"><span data-stu-id="fdefb-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="fdefb-125">如果发布页面但不发布指向该页面的 URL，则不能使用 URL 访问该页面。</span><span class="sxs-lookup"><span data-stu-id="fdefb-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="fdefb-126">手动创建页面 URL</span><span class="sxs-lookup"><span data-stu-id="fdefb-126">Manually create a page URL</span></span>

<span data-ttu-id="fdefb-127">创建新页面时，无需指定页面 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="fdefb-128">如果让 URL 字段保持为空，将在未链接状态下创建页面。</span><span class="sxs-lookup"><span data-stu-id="fdefb-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="fdefb-129">在此情况下，客户不能访问页面，即使已发布了该页面。</span><span class="sxs-lookup"><span data-stu-id="fdefb-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="fdefb-130">若要使该页面可访问，必须手动创建 URL 并将其链接到该页面。</span><span class="sxs-lookup"><span data-stu-id="fdefb-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="fdefb-131">若要为页面手动创建页面 URL，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="fdefb-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="fdefb-132">在 **URL** 页面上，选择 **新建**。</span><span class="sxs-lookup"><span data-stu-id="fdefb-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="fdefb-133">选择要与 URL 关联的站点页面。</span><span class="sxs-lookup"><span data-stu-id="fdefb-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="fdefb-134">输入 URL 数据域，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="fdefb-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="fdefb-135">此时，URL 处于草稿状态。</span><span class="sxs-lookup"><span data-stu-id="fdefb-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="fdefb-136">必须先发布它，站点用户才能访问关联的页面。</span><span class="sxs-lookup"><span data-stu-id="fdefb-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="fdefb-137">更新页面 URL</span><span class="sxs-lookup"><span data-stu-id="fdefb-137">Update a page URL</span></span>

<span data-ttu-id="fdefb-138">若要更新页面 URL 的目标页，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="fdefb-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="fdefb-139">在 **URL** 页中，选择要更新的 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="fdefb-140">在右侧的属性窗格中，选择目标页字段旁边的省略号按钮 (**...**)。</span><span class="sxs-lookup"><span data-stu-id="fdefb-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="fdefb-141">在对话框中，选择其他页，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="fdefb-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="fdefb-142">保存并发布 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="fdefb-143">重定向页面 URL</span><span class="sxs-lookup"><span data-stu-id="fdefb-143">Redirect a page URL</span></span>

<span data-ttu-id="fdefb-144">有时，您可能希望客户在请求特定 URL 时查看其他页。</span><span class="sxs-lookup"><span data-stu-id="fdefb-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="fdefb-145">在这些情况下，最好，最简单的方法通常是更改页面 URL 指向的页面。</span><span class="sxs-lookup"><span data-stu-id="fdefb-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="fdefb-146">但是，您可能有正当理由使用 HTTP 301 或 3023 重定向将 URL 的请求重定向到其他 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="fdefb-147">若要将 URL 重定向到其他 URL，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="fdefb-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="fdefb-148">在 **URL** 页中，选择要更新的 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="fdefb-149">在右侧属性窗格中，选择 **重定向**。</span><span class="sxs-lookup"><span data-stu-id="fdefb-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="fdefb-150">选择重定向的目标：</span><span class="sxs-lookup"><span data-stu-id="fdefb-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="fdefb-151">若要执行站点中的其他页面，请选择 **内部 URL**，选择省略号按钮 (**...**)，然后选择要重定向到的 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="fdefb-152">若要指向外部站点中的页面，请选择 **外部 URL**，然后输入该页面的完整 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="fdefb-153">务必包含协议。</span><span class="sxs-lookup"><span data-stu-id="fdefb-153">Be sure to include the protocol.</span></span> <span data-ttu-id="fdefb-154">例如，输入 `https://domain.com/new/page`。</span><span class="sxs-lookup"><span data-stu-id="fdefb-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="fdefb-155">如果 URL 已经重定向到内部 URL，必须在输入外部 URL 前选择 **清除选择**。</span><span class="sxs-lookup"><span data-stu-id="fdefb-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="fdefb-156">选择重定向类型：</span><span class="sxs-lookup"><span data-stu-id="fdefb-156">Select a redirect type:</span></span>

    - <span data-ttu-id="fdefb-157">**永久重定向 (301)** – 如果知道内容将永久移动，不会恢复为之前的 URL，请选择此选项。</span><span class="sxs-lookup"><span data-stu-id="fdefb-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="fdefb-158">搜索引擎将把重定向 URL 的搜索引擎优化 (SEO) 值分配给将重定向到的 URL，并更新其记录以显示新 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="fdefb-159">**临时重定向 (302)** – 选择此选项以重定向流量，但不更新搜索引擎。</span><span class="sxs-lookup"><span data-stu-id="fdefb-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="fdefb-160">如果内容很快将恢复为之前的 URL，通常使用此方法。</span><span class="sxs-lookup"><span data-stu-id="fdefb-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="fdefb-161">准备好实施重定向时，保存并发布 URL。</span><span class="sxs-lookup"><span data-stu-id="fdefb-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fdefb-162">其他资源</span><span class="sxs-lookup"><span data-stu-id="fdefb-162">Additional resources</span></span>

[<span data-ttu-id="fdefb-163">自定义站点导航</span><span class="sxs-lookup"><span data-stu-id="fdefb-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="fdefb-164">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="fdefb-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="fdefb-165">配置域名</span><span class="sxs-lookup"><span data-stu-id="fdefb-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="fdefb-166">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="fdefb-166">Add languages to your site</span></span>](add-languages-to-site.md)
