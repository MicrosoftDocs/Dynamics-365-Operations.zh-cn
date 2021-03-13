---
title: 基于 URL 参数创建动态电子商务页面
description: 本主题介绍如何基于 URL 参数设置可以提供动态内容的 Microsoft Dynamics 365 Commerce 电子商务页面。
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: e72b738133b396848848d167cace80fe23694334
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2021
ms.locfileid: "5098613"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="869a7-103">基于 URL 参数创建动态电子商务页面</span><span class="sxs-lookup"><span data-stu-id="869a7-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="869a7-104">本主题介绍如何基于 URL 参数设置可以提供动态内容的 Microsoft Dynamics 365 Commerce 电子商务页面。</span><span class="sxs-lookup"><span data-stu-id="869a7-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="869a7-105">可以基于 URL 路径中的段将电子商务页面配置为提供不同的内容。</span><span class="sxs-lookup"><span data-stu-id="869a7-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="869a7-106">因此，该页面称为动态页面。</span><span class="sxs-lookup"><span data-stu-id="869a7-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="869a7-107">段用作检索页面内容的参数。</span><span class="sxs-lookup"><span data-stu-id="869a7-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="869a7-108">例如，创建了一个名为 **blog\_viewer** 的页面，并将其与 URL `https://fabrikam.com/blog` 关联。</span><span class="sxs-lookup"><span data-stu-id="869a7-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="869a7-109">然后可以基于 URL 路径中的最后一个段使用此页面来显示不同的内容。</span><span class="sxs-lookup"><span data-stu-id="869a7-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="869a7-110">例如，URL `https://fabrikam.com/blog/article-1` 中的最后一个段是 **article-1**。</span><span class="sxs-lookup"><span data-stu-id="869a7-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="869a7-111">替代动态页面的单独的自定义页面也可以与 URL 路径中的段相关联。</span><span class="sxs-lookup"><span data-stu-id="869a7-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="869a7-112">例如，创建了一个名为 **blog\_summary** 的页面，并将其与 URL `https://fabrikam.com/blog/about-this-blog` 关联。</span><span class="sxs-lookup"><span data-stu-id="869a7-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="869a7-113">当请求此 URL 时，将返回与 **/about-this-blog** 参数关联的 **blog\_summary** 页面，而不是 **blog\_viewer** 页面。</span><span class="sxs-lookup"><span data-stu-id="869a7-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="869a7-114">托管、检索和显示动态页面内容的功能通过使用自定义模块实现。</span><span class="sxs-lookup"><span data-stu-id="869a7-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="869a7-115">有关详细信息，请参阅[在线渠道可扩展性](e-commerce-extensibility/overview.md)。</span><span class="sxs-lookup"><span data-stu-id="869a7-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="869a7-116">设置动态电子商务页面</span><span class="sxs-lookup"><span data-stu-id="869a7-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="869a7-117">要设置动态电子商务页面，必须创建动态页面，创建基本 URL，并配置到达动态页面的路由。</span><span class="sxs-lookup"><span data-stu-id="869a7-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="869a7-118">创建将提供动态内容的页面</span><span class="sxs-lookup"><span data-stu-id="869a7-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="869a7-119">要创建将提供动态内容的页面，请按照[添加新的站点页面](add-new-page.md)中的步骤操作。</span><span class="sxs-lookup"><span data-stu-id="869a7-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="869a7-120">您创建的页面将需要实现一个模块，该模块使用 URL 路径中的最后一个段来从外部数据源检索内容。</span><span class="sxs-lookup"><span data-stu-id="869a7-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="869a7-121">有关自定义模块开发的详细信息，请参阅[在线渠道可扩展性](e-commerce-extensibility/overview.md)。</span><span class="sxs-lookup"><span data-stu-id="869a7-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="869a7-122">创建动态页面的基本 URL</span><span class="sxs-lookup"><span data-stu-id="869a7-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="869a7-123">要在 Commerce 站点构建器中为动态页面创建基本 URL，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="869a7-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="869a7-124">转到 **URL**，选择 **新建 \> 新建 URL**。</span><span class="sxs-lookup"><span data-stu-id="869a7-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="869a7-125">在 **创建新 URL** 对话框中，选择 **内部页面**。</span><span class="sxs-lookup"><span data-stu-id="869a7-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="869a7-126">在 **URL 路径** 下，输入将用作动态页面根目录的路径（在此示例中为 **/blog**）。</span><span class="sxs-lookup"><span data-stu-id="869a7-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="869a7-127">然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="869a7-127">Then select **Next**.</span></span>
1. <span data-ttu-id="869a7-128">在 **选择页面** 对话框中，选择您创建的要用作动态页面的页面，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="869a7-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="869a7-129">选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="869a7-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="869a7-130">配置到达动态页面的路由</span><span class="sxs-lookup"><span data-stu-id="869a7-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="869a7-131">要在 Commerce 站点构建器中配置到达动态页面的路由，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="869a7-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="869a7-132">转到 **站点设置 \> 扩展**。</span><span class="sxs-lookup"><span data-stu-id="869a7-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="869a7-133">在 **参数化 URL 路径** 下，选择 **添加**，然后输入您在创建 URL 时输入的 URL 路径（在本示例中为 **/blog**）。</span><span class="sxs-lookup"><span data-stu-id="869a7-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="869a7-134">选择 **保存并发布**。</span><span class="sxs-lookup"><span data-stu-id="869a7-134">Select **Save and publish**.</span></span>

<span data-ttu-id="869a7-135">配置路由后，对参数化 URL 路径的所有请求都将返回与该 URL 关联的页面。</span><span class="sxs-lookup"><span data-stu-id="869a7-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="869a7-136">如果任何请求包含附加段，将返回关联的页面，并将该段用作参数来检索页面内容。</span><span class="sxs-lookup"><span data-stu-id="869a7-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="869a7-137">例如，`https://fabrikam.com/blog/article-1` 将返回 **blog\_summary** 页面，页面内容将使用 **/article-1** 参数进行检索。</span><span class="sxs-lookup"><span data-stu-id="869a7-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="869a7-138">使用自定义页面替代参数化 URL</span><span class="sxs-lookup"><span data-stu-id="869a7-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="869a7-139">要在 Commerce 站点构建器中使用自定义页面替代参数化 URL，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="869a7-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="869a7-140">转到 **URL**，选择 **新建 \> 新建 URL**。</span><span class="sxs-lookup"><span data-stu-id="869a7-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="869a7-141">在 **创建新 URL** 对话框中，选择 **内部页面**。</span><span class="sxs-lookup"><span data-stu-id="869a7-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="869a7-142">在 **URL 路径** 下，输入包含要替代的段的路径（在此示例中为 **/blog/about-this-blog**）。</span><span class="sxs-lookup"><span data-stu-id="869a7-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="869a7-143">然后选择 **下一步**。</span><span class="sxs-lookup"><span data-stu-id="869a7-143">Then select **Next**.</span></span>
1. <span data-ttu-id="869a7-144">在 **选择页面** 对话框中，选择自定义页面，然后选择 **保存**。</span><span class="sxs-lookup"><span data-stu-id="869a7-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="869a7-145">选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="869a7-145">Select **Publish**.</span></span>
1. <span data-ttu-id="869a7-146">如果自定义页面尚未发布，转到 **页面**，选择自定义页面，然后选择 **发布**。</span><span class="sxs-lookup"><span data-stu-id="869a7-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="869a7-147">自定义页面发布后，将提供该页面，而不是包含参数化内容的动态页面。</span><span class="sxs-lookup"><span data-stu-id="869a7-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="869a7-148">其他资源</span><span class="sxs-lookup"><span data-stu-id="869a7-148">Additional resources</span></span>

[<span data-ttu-id="869a7-149">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="869a7-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="869a7-150">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="869a7-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="869a7-151">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="869a7-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="869a7-152">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="869a7-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="869a7-153">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="869a7-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="869a7-154">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="869a7-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="869a7-155">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="869a7-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="869a7-156">验证页面内容的可访问性</span><span class="sxs-lookup"><span data-stu-id="869a7-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="869a7-157">在线渠道可扩展性</span><span class="sxs-lookup"><span data-stu-id="869a7-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)
