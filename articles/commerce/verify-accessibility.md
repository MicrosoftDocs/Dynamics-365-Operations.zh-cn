---
title: 验证页面内容的可访问性
description: 本主题介绍如何在 Microsoft Dynamics 365 Commerce 中验证页面内容的可访问性。
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 7690f3bb17a56b9a16b6e818b675064b1979948e
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097357"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="2ae37-103">验证页面内容的可访问性</span><span class="sxs-lookup"><span data-stu-id="2ae37-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2ae37-104">本主题介绍如何在 Microsoft Dynamics 365 Commerce 中验证页面内容的可访问性。</span><span class="sxs-lookup"><span data-stu-id="2ae37-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2ae37-105">概览</span><span class="sxs-lookup"><span data-stu-id="2ae37-105">Overview</span></span>

<span data-ttu-id="2ae37-106">完成页面更改后，应确保内容可供 Web 上的所有人访问。</span><span class="sxs-lookup"><span data-stu-id="2ae37-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="2ae37-107">在 Commerce 创作工具中，您可以使用集成的 [Microsoft Accessibility Insights](https://accessibilityinsights.io/) 服务轻松地验证页面内容的可访问性。</span><span class="sxs-lookup"><span data-stu-id="2ae37-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="2ae37-108">此服务可根据最新的[万维网联合会 (W3C) 可访问性](https://www.w3.org/standards/webdesign/accessibility)准则验证您的页面内容。</span><span class="sxs-lookup"><span data-stu-id="2ae37-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="2ae37-109">[Microsoft Accessibility Insights](https://accessibilityinsights.io/) 集成必须先在租户或站点级别打开，然后才能使用。</span><span class="sxs-lookup"><span data-stu-id="2ae37-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="2ae37-110">为租户中的所有站点打开 Microsoft Accessibility Insights</span><span class="sxs-lookup"><span data-stu-id="2ae37-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="2ae37-111">要为租户中的所有 Commerce 站点打开 [Microsoft Accessibility Insights](https://accessibilityinsights.io/) 集成，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2ae37-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="2ae37-112">要访问租户设置，您必须以系统管理员身份登录到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="2ae37-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="2ae37-113">以系统管理员身份登录到 Commerce。</span><span class="sxs-lookup"><span data-stu-id="2ae37-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="2ae37-114">在左侧导航窗格中，选择 **租户设置**（在齿轮符号旁边）将其展开。</span><span class="sxs-lookup"><span data-stu-id="2ae37-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="2ae37-115">在 **租户设置** 下，选择 **功能**。</span><span class="sxs-lookup"><span data-stu-id="2ae37-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="2ae37-116">将 **可访问性检查** 选项设置为 **开**。</span><span class="sxs-lookup"><span data-stu-id="2ae37-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="2ae37-117">为单个站点打开 Microsoft Accessibility Insights</span><span class="sxs-lookup"><span data-stu-id="2ae37-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="2ae37-118">要为单个 Commerce 站点打开 [Microsoft Accessibility Insights](https://accessibilityinsights.io/) 集成，请按照以下步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2ae37-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="2ae37-119">在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="2ae37-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2ae37-120">在左侧导航窗格中，选择 **站点设置** 将其展开。</span><span class="sxs-lookup"><span data-stu-id="2ae37-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="2ae37-121">在 **站点设置** 下，选择 **功能**。</span><span class="sxs-lookup"><span data-stu-id="2ae37-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="2ae37-122">将 **可访问性检查** 选项设置为 **开**。</span><span class="sxs-lookup"><span data-stu-id="2ae37-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="2ae37-123">验证主页上内容的可访问性</span><span class="sxs-lookup"><span data-stu-id="2ae37-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="2ae37-124">要使用集成的 [Microsoft Accessibility Insights](https://accessibilityinsights.io/) 服务扫描和验证 Commerce 中主页的内容，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="2ae37-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2ae37-125">在 **站点** 下，选择 **Fabrikam**（或您的站点的名称）。</span><span class="sxs-lookup"><span data-stu-id="2ae37-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2ae37-126">在左侧导航窗格中，选择 **页面**。</span><span class="sxs-lookup"><span data-stu-id="2ae37-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="2ae37-127">转到并选择主页在页面编辑器中将其打开。</span><span class="sxs-lookup"><span data-stu-id="2ae37-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="2ae37-128">在命令栏中，选择 **检查可访问性**。</span><span class="sxs-lookup"><span data-stu-id="2ae37-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="2ae37-129">**检查可访问性** 页面将出现。</span><span class="sxs-lookup"><span data-stu-id="2ae37-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="2ae37-130">扫描完成后，查看报告内容。</span><span class="sxs-lookup"><span data-stu-id="2ae37-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="2ae37-131">如果有任何检查失败，请选择每个失败的检查项目将其展开，这样可以查看更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="2ae37-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="2ae37-132">要在查看完后关闭报告，滚动到 **检查可访问性** 页面的底部，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="2ae37-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ae37-133">其他资源</span><span class="sxs-lookup"><span data-stu-id="2ae37-133">Additional resources</span></span>

[<span data-ttu-id="2ae37-134">修改现有的站点页面</span><span class="sxs-lookup"><span data-stu-id="2ae37-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="2ae37-135">添加新的站点页面</span><span class="sxs-lookup"><span data-stu-id="2ae37-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2ae37-136">选择页面布局</span><span class="sxs-lookup"><span data-stu-id="2ae37-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="2ae37-137">管理 SEO 元数据</span><span class="sxs-lookup"><span data-stu-id="2ae37-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="2ae37-138">保存、预览和发布页面</span><span class="sxs-lookup"><span data-stu-id="2ae37-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="2ae37-139">丰富产品页面</span><span class="sxs-lookup"><span data-stu-id="2ae37-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="2ae37-140">丰富类别登陆页面</span><span class="sxs-lookup"><span data-stu-id="2ae37-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="2ae37-141">基于 URL 参数创建动态电子商务页面</span><span class="sxs-lookup"><span data-stu-id="2ae37-141">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
