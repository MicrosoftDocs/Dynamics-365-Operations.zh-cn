---
title: 启用和使用跨渠道共享
description: 本主题介绍了如何启用和使用 Microsoft Dynamics 365 Commerce 站点构建器的跨渠道共享功能。
author: psimolin
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3990365dda0a0cff7adcc1d97120293d43f6e858
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973114"
---
# <a name="enable-and-use-cross-channel-sharing"></a><span data-ttu-id="33ad8-103">启用和使用跨渠道共享</span><span class="sxs-lookup"><span data-stu-id="33ad8-103">Enable and use cross-channel sharing</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33ad8-104">本主题介绍了如何启用和使用 Microsoft Dynamics 365 Commerce 站点构建器的跨渠道共享功能。</span><span class="sxs-lookup"><span data-stu-id="33ad8-104">This topic describes how to enable and use the cross-channel sharing feature of Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="33ad8-105">概览</span><span class="sxs-lookup"><span data-stu-id="33ad8-105">Overview</span></span>

<span data-ttu-id="33ad8-106">通过跨渠道共享，零售商可以在站点的多个渠道中重复使用和共享内容。</span><span class="sxs-lookup"><span data-stu-id="33ad8-106">Cross-channel sharing lets retailers reuse and share content among multiple channels of a site.</span></span> <span data-ttu-id="33ad8-107">当站点渠道具有兼容的基本语言时，或者当它们具有多个共同的内容项时，此功能很有用。</span><span class="sxs-lookup"><span data-stu-id="33ad8-107">This capability is useful when the site channels have a compatible base language, or when they have numerous content items in common.</span></span>

<span data-ttu-id="33ad8-108">跨渠道共享的工作原理是在找不到所请求内容的渠道特定版本时，启用将搜索可用内容的默认渠道。</span><span class="sxs-lookup"><span data-stu-id="33ad8-108">Cross-channel sharing works by enabling a default channel that will be searched for available content when a channel-specific version of the requested content isn't found.</span></span> <span data-ttu-id="33ad8-109">打算在渠道之间共享的内容将在默认渠道中创建。</span><span class="sxs-lookup"><span data-stu-id="33ad8-109">Content that is intended to be shared among channels is created in the default channel.</span></span> <span data-ttu-id="33ad8-110">可以针对任何站点渠道上使用的任何区域设置对该内容进行本地化。</span><span class="sxs-lookup"><span data-stu-id="33ad8-110">That content can be localized for any locale that is used on any site channel.</span></span>

## <a name="when-to-use-cross-channel-sharing"></a><span data-ttu-id="33ad8-111">何时使用跨渠道共享</span><span class="sxs-lookup"><span data-stu-id="33ad8-111">When to use cross-channel sharing</span></span>

<span data-ttu-id="33ad8-112">当单个站点上的多个渠道可以共享内容时，跨渠道共享非常有用。</span><span class="sxs-lookup"><span data-stu-id="33ad8-112">Cross-channel sharing is useful when multiple channels on a single site can share content.</span></span> <span data-ttu-id="33ad8-113">例如，具有在一个站点下分组的多个品牌和店面的零售商可以在一些或所有店面之间共享某些内容。</span><span class="sxs-lookup"><span data-stu-id="33ad8-113">For example, a retailer that has multiple brands and storefronts that are grouped under a single site can share some content among some or all of the storefronts.</span></span> <span data-ttu-id="33ad8-114">此共享的内容可以包括有关条款和条件、付款期、运输方式和常见问题 (FAQ) 的页面。</span><span class="sxs-lookup"><span data-stu-id="33ad8-114">This shared content can include pages for terms and conditions, payment terms, shipment methods, and frequently asked questions (FAQ).</span></span>

<span data-ttu-id="33ad8-115">跨渠道共享也支持片段。</span><span class="sxs-lookup"><span data-stu-id="33ad8-115">Cross-channel sharing also supports fragments.</span></span> <span data-ttu-id="33ad8-116">因此，可以将包含渠道特定片段的内容页面创建为跨渠道内容。</span><span class="sxs-lookup"><span data-stu-id="33ad8-116">Therefore, a content page that contains channel-specific fragments can be created as cross-channel content.</span></span> <span data-ttu-id="33ad8-117">在这种情况下，尽管大多数内容将在渠道之间共享，但是仅当从相应的店面渠道请求它们时，才会呈现跨渠道页面上的渠道特定片段。</span><span class="sxs-lookup"><span data-stu-id="33ad8-117">In this case, although most of the content will be shared among channels, channel-specific fragments on a cross-channel page will be rendered only when they are requested from the corresponding storefront channel.</span></span>

<span data-ttu-id="33ad8-118">只有一个渠道的站点或具有多个无法共享内容的渠道的站点将无法从跨渠道共享中受益。</span><span class="sxs-lookup"><span data-stu-id="33ad8-118">Sites that have only one channel, or sites that have multiple channels that can't share content, won't benefit from cross-channel sharing.</span></span>

## <a name="enable-cross-channel-sharing"></a><span data-ttu-id="33ad8-119">启用跨渠道共享</span><span class="sxs-lookup"><span data-stu-id="33ad8-119">Enable cross-channel sharing</span></span>

<span data-ttu-id="33ad8-120">在站点级别上启用跨渠道共享。</span><span class="sxs-lookup"><span data-stu-id="33ad8-120">Cross-channel sharing is enabled at the site level.</span></span> <span data-ttu-id="33ad8-121">此操作是单向的。</span><span class="sxs-lookup"><span data-stu-id="33ad8-121">This operation is one-way.</span></span> <span data-ttu-id="33ad8-122">换句话说，启用跨渠道共享后，便无法将其禁用。</span><span class="sxs-lookup"><span data-stu-id="33ad8-122">In other words, after cross-channel sharing is enabled, it can't be disabled.</span></span>

<span data-ttu-id="33ad8-123">若要在 Commerce 站点构建器中启用跨渠道共享，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="33ad8-123">To enable cross-channel sharing in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="33ad8-124">转到 **站点设置 \> 功能**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-124">Go to **Site settings \> Features**.</span></span>
1. <span data-ttu-id="33ad8-125">将 **跨渠道** 功能的选项设置为 **开**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-125">Set the option for the **Cross Channel** feature to **On**.</span></span>

    ![在 Commerce 站点构建器中，将“跨渠道”选项设置为“开”](./media/enabling-cross-channel-sharing.png)

<span data-ttu-id="33ad8-127">启用跨渠道共享后，跨渠道信息将显示在 **站点设置 \> 功能** 的 **渠道** 部分中，如下图示例所示。</span><span class="sxs-lookup"><span data-stu-id="33ad8-127">After you enable cross-channel sharing, cross-channel information will appear in the **Channels** section at **Site settings \> Features**, as the example in the following illustration shows.</span></span>

![渠道信息在启用跨渠道共享后可见](./media/channels-cross-channel.png)

<span data-ttu-id="33ad8-129">此外，启用跨渠道共享后，Commerce 站点构建器右上角的 **渠道** 字段将包含一个 **跨渠道在线商店** 选项，可用于管理跨渠道内容，如下图所示。</span><span class="sxs-lookup"><span data-stu-id="33ad8-129">Additionally, after you enable cross-channel sharing, the **Channel** field in the upper right of Commerce site builder will include a **Cross Channel Online Store** option that you can use to manage cross-channel content, as shown in the following illustration.</span></span>

![启用跨渠道共享后，“渠道”字段中的“跨渠道在线商店”选项](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a><span data-ttu-id="33ad8-131">创建和使用跨渠道内容</span><span class="sxs-lookup"><span data-stu-id="33ad8-131">Create and use cross-channel content</span></span>

<span data-ttu-id="33ad8-132">您可以通过多种方式创建和使用跨渠道内容。</span><span class="sxs-lookup"><span data-stu-id="33ad8-132">You can create and use cross-channel content in multiple ways.</span></span> <span data-ttu-id="33ad8-133">例如，您可以创建跨渠道片段，创建使用跨渠道和渠道特定内容的跨渠道页面，并使用渠道特定版本的片段替代跨渠道片段。</span><span class="sxs-lookup"><span data-stu-id="33ad8-133">For example, you can create cross-channel fragments, create cross-channel pages that use cross-channel and channel-specific content, and override cross-channel fragments with channel-specific versions of fragments.</span></span>

### <a name="create-a-cross-channel-fragment"></a><span data-ttu-id="33ad8-134">创建跨渠道片段</span><span class="sxs-lookup"><span data-stu-id="33ad8-134">Create a cross-channel fragment</span></span>

<span data-ttu-id="33ad8-135">若要在 Commerce 站点构建器中创建跨渠道片段，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="33ad8-135">To create a cross-channel fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="33ad8-136">转到 **片段**，选择 **新建** 创建新片段。</span><span class="sxs-lookup"><span data-stu-id="33ad8-136">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="33ad8-137">在 **新建片段** 对话框中，选择 **促销横幅** 模块，然后在 **片段名称** 下，输入名称（例如，**跨渠道横幅**）。</span><span class="sxs-lookup"><span data-stu-id="33ad8-137">In the **New fragment** dialog box, select the **Promo banner** module, and then, under **Fragment name**, enter a name (for example, **Cross-channel banner**).</span></span> <span data-ttu-id="33ad8-138">然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-138">Then select **OK**.</span></span>
1. <span data-ttu-id="33ad8-139">在 **促销横幅** 模块的属性窗格中，选择 **添加消息**，然后选择 **消息**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-139">In the property pane for the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="33ad8-140">在 **消息** 对话框中，在 **文本** 下，输入 **跨渠道**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-140">In the **Message** dialog box, under **Text**, enter **Cross-channel**, and the select **OK**.</span></span> 
1. <span data-ttu-id="33ad8-141">选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="33ad8-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="33ad8-142">此跨渠道片段可用于在任何站点渠道上创建的跨渠道页面或渠道特定页面。</span><span class="sxs-lookup"><span data-stu-id="33ad8-142">This cross-channel fragment can be used on cross-channel or channel-specific pages that are created on any site channel.</span></span>

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a><span data-ttu-id="33ad8-143">创建使用跨渠道内容的跨渠道页面</span><span class="sxs-lookup"><span data-stu-id="33ad8-143">Create a cross-channel page that uses cross-channel content</span></span>

<span data-ttu-id="33ad8-144">跨渠道页面可用于您的站点的任何渠道。</span><span class="sxs-lookup"><span data-stu-id="33ad8-144">Cross-channel pages can be used on any channel of your site.</span></span> <span data-ttu-id="33ad8-145">因此，您可以一次创建一个共享内容页面，并在单个位置进行任何后续更新。</span><span class="sxs-lookup"><span data-stu-id="33ad8-145">Therefore, you can create a shared content page one time and make any subsequent updates in a single place.</span></span> <span data-ttu-id="33ad8-146">例如，具有 URL `/toc` 的跨渠道 **条款和条件** 页面可以在站点的所有渠道之间共享。</span><span class="sxs-lookup"><span data-stu-id="33ad8-146">For example, a cross-channel **Terms and conditions** page that has the URL `/toc` can be shared among all the channels of a site.</span></span> <span data-ttu-id="33ad8-147">如果站点渠道的基本 URL 是 `www.fabrikam.com/brand1` 和 `www.fabrikam.com/brand2`，相同的跨渠道共享的 **条款和条件** 页面将分别在 `www.fabrikam.com/brand1/toc` 和 `www.fabrikam.com/brand2/toc` 的站点渠道 URL 上提供。</span><span class="sxs-lookup"><span data-stu-id="33ad8-147">If the base URLs for the site channels are `www.fabrikam.com/brand1` and `www.fabrikam.com/brand2`, the same cross-channel, shared **Terms and conditions** page will be available from both site channel URLs, at `www.fabrikam.com/brand1/toc` and `www.fabrikam.com/brand2/toc`, respectively.</span></span> <span data-ttu-id="33ad8-148">如果 **条款和条件** 页面必须稍后更新，您只需更新单个共享页面。</span><span class="sxs-lookup"><span data-stu-id="33ad8-148">If the **Terms and conditions** page must be updated later, you have to update only the single, shared page.</span></span>

<span data-ttu-id="33ad8-149">若要在 Commerce 站点构建器中创建使用跨渠道内容的跨渠道页面，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="33ad8-149">To create a cross-channel page in Commerce site builder that uses cross-channel content, follow these steps.</span></span>

1. <span data-ttu-id="33ad8-150">转到 **页面**，选择 **新建** 创建新页面。</span><span class="sxs-lookup"><span data-stu-id="33ad8-150">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="33ad8-151">在 **选择模板** 对话框中，选择一个模板，例如 **市场营销**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-151">In the **Choose a template** dialog box, select a template, such as **Marketing**.</span></span>
1. <span data-ttu-id="33ad8-152">在 **页面名称** 下，输入页面名称（例如，**跨渠道页面**）。</span><span class="sxs-lookup"><span data-stu-id="33ad8-152">Under **Page name**, enter a name for the page (for example, **Cross-channel page**).</span></span>
1. <span data-ttu-id="33ad8-153">在 **页面 URL** 下，输入页面 URL（例如，**examplepage**），然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-153">Under **Page URL**, enter a page URL (for example, **examplepage**), and then select **OK**.</span></span>
1. <span data-ttu-id="33ad8-154">在新页面的 **主** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-154">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="33ad8-155">在 **添加片段** 对话框中，选择您先前创建的具有促销横幅的跨渠道片段，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-155">In the **Add fragment** dialog box, select the cross-channel fragment that you created earlier that has a promo banner, and then select **OK**.</span></span>
1. <span data-ttu-id="33ad8-156">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="33ad8-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="33ad8-157">您应该看到显示“跨渠道”的促销横幅。</span><span class="sxs-lookup"><span data-stu-id="33ad8-157">You should see the promo banner that says, "Cross-channel."</span></span>
1. <span data-ttu-id="33ad8-158">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="33ad8-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a><span data-ttu-id="33ad8-159">创建使用跨渠道内容的渠道特定页面</span><span class="sxs-lookup"><span data-stu-id="33ad8-159">Create a channel-specific page that uses cross-channel content</span></span>

<span data-ttu-id="33ad8-160">通过在渠道特定页面上使用跨渠道内容，您可以一次创建一个共享内容片段，然后在渠道特定页面上使用它。</span><span class="sxs-lookup"><span data-stu-id="33ad8-160">By using cross-channel content on channel-specific pages, you can create a shared content fragment one time and then use it on channel-specific pages.</span></span> <span data-ttu-id="33ad8-161">此“单一来源”可用于共享内容，例如条款和条件、付款期或联系人信息。</span><span class="sxs-lookup"><span data-stu-id="33ad8-161">This "single sourcing" is useful for shared content such as terms and conditions, payment terms, or contact information.</span></span>

<span data-ttu-id="33ad8-162">若要在 Commerce 站点构建器中创建使用跨渠道内容的渠道特定页面，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="33ad8-162">To create a channel-specific page in Commerce site builder that uses cross-channel content, follow these steps.</span></span>

1. <span data-ttu-id="33ad8-163">从特定渠道（例如 **Fabrikam 扩展的在线商店**）中，转到 **页面**，然后选择 **新建** 来创建一个新页面。</span><span class="sxs-lookup"><span data-stu-id="33ad8-163">From within a specific channel, such as **Fabrikam extended online store**, go to **Pages**, and then select **New** to create a new page.</span></span>
1. <span data-ttu-id="33ad8-164">在 **选择模板** 对话框中，选择一个模板，例如 **市场营销**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-164">In the **Choose a template** dialog box, select a template, such as **Marketing**.</span></span>
1. <span data-ttu-id="33ad8-165">在 **页面名称** 下，输入页面名称（例如，**渠道特定页面**）。</span><span class="sxs-lookup"><span data-stu-id="33ad8-165">Under **Page name**, enter a name for the page (for example, **Channel-specific page**).</span></span>
1. <span data-ttu-id="33ad8-166">在 **页面 URL** 下，输入页面 URL（例如，**channelspecificpage**），然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-166">Under **Page URL**, enter a page URL (for example, **channelspecificpage**), and then select **OK**.</span></span>
1. <span data-ttu-id="33ad8-167">在新页面的 **主** 插槽中，选择省略号 (**...**)，然后选择 **添加片段**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-167">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="33ad8-168">在 **添加片段** 对话框中，在 **渠道** 下，选择 **跨渠道在线商店**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-168">In the **Add fragment** dialog box, under **Channel**, select **Cross Channel Online Store**.</span></span> <span data-ttu-id="33ad8-169">您之前创建的跨渠道片段应显示在列表中。</span><span class="sxs-lookup"><span data-stu-id="33ad8-169">The cross-channel fragment that you created earlier should appear in the list.</span></span> <span data-ttu-id="33ad8-170">选择它，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-170">Select it, and then select **OK**.</span></span>
1. <span data-ttu-id="33ad8-171">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="33ad8-171">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="33ad8-172">您应该看到显示“跨渠道”的促销横幅。</span><span class="sxs-lookup"><span data-stu-id="33ad8-172">You should see the promo banner that says, "Cross-channel."</span></span>
1. <span data-ttu-id="33ad8-173">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="33ad8-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a><span data-ttu-id="33ad8-174">创建渠道特定版本的跨渠道页面</span><span class="sxs-lookup"><span data-stu-id="33ad8-174">Create a channel-specific version of a cross-channel page</span></span>

<span data-ttu-id="33ad8-175">跨渠道共享支持替代跨渠道内容。</span><span class="sxs-lookup"><span data-stu-id="33ad8-175">Cross-channel sharing supports overrides of cross-channel content.</span></span> <span data-ttu-id="33ad8-176">例如，您的站点渠道中除一个渠道之外的所有渠道都共享相同的内容。</span><span class="sxs-lookup"><span data-stu-id="33ad8-176">For example, all but one of your site channels share the same piece of content.</span></span> <span data-ttu-id="33ad8-177">该站点渠道需要不同的内容。</span><span class="sxs-lookup"><span data-stu-id="33ad8-177">That one site channel requires different content.</span></span> <span data-ttu-id="33ad8-178">若要为其实现不同的内容，您可以通过创建渠道特定版本的跨渠道页面来使用渠道特定内容替代跨渠道内容。</span><span class="sxs-lookup"><span data-stu-id="33ad8-178">To implement the different content for it, you override the cross-channel content with channel-specific content by creating a channel-specific version of the cross-channel page.</span></span>

<span data-ttu-id="33ad8-179">若要在 Commerce 站点构建器中创建渠道特定版本的跨渠道页面，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="33ad8-179">To create a channel-specific version of a cross-channel page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="33ad8-180">在右上角的 **渠道** 字段中，选择 **跨渠道在线商店**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-180">In the **Channel** field in the upper right, select **Cross Channel Online Store**.</span></span>
1. <span data-ttu-id="33ad8-181">打开您之前创建的跨渠道页面。</span><span class="sxs-lookup"><span data-stu-id="33ad8-181">Open the cross-channel page that you created earlier.</span></span>
1. <span data-ttu-id="33ad8-182">在右上角的 **渠道** 字段中，选择应具有特定内容的渠道。</span><span class="sxs-lookup"><span data-stu-id="33ad8-182">In the **Channel** field in the upper right, select the channel that should have specific content.</span></span> <span data-ttu-id="33ad8-183">页面编辑器显示一条消息，提示您创建新的页面变体。</span><span class="sxs-lookup"><span data-stu-id="33ad8-183">The page editor shows a message that prompts you to create a new page variant.</span></span>
1. <span data-ttu-id="33ad8-184">选择 **创建页面变体**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-184">Select **Create page variant**.</span></span>
1. <span data-ttu-id="33ad8-185">在页面变体的 **主** 插槽中，选择省略号 (**...**)，然后选择 **添加模块**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-185">In the **Main** slot of the page variant, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="33ad8-186">在 **添加模块** 对话框中，选择 **促销横幅** 模块，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-186">In the **Add Module** dialog box, select the **Promo banner** module, and then select **OK**.</span></span>
1. <span data-ttu-id="33ad8-187">在 **促销横幅** 模块的属性窗格中，选择 **添加消息**，然后选择 **消息**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-187">In the property pane for the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="33ad8-188">在 **消息** 对话框中，在 **文本** 下，输入 **渠道特定**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="33ad8-188">In the **Message** dialog box, under **Text**, enter **Channel-specific**, and the select **OK**.</span></span>
1. <span data-ttu-id="33ad8-189">选择 **保存**，然后选择 **预览** 以预览页面。</span><span class="sxs-lookup"><span data-stu-id="33ad8-189">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="33ad8-190">您应该看到显示“渠道特定”的促销横幅。</span><span class="sxs-lookup"><span data-stu-id="33ad8-190">You should see the promo banner that says, "Channel-specific."</span></span>
1. <span data-ttu-id="33ad8-191">选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="33ad8-191">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="33ad8-192">现在，如果您使用渠道的基本 URL 并转到该站点上的跨渠道页面的 URL，您将看到渠道特定内容，而不是跨渠道内容。</span><span class="sxs-lookup"><span data-stu-id="33ad8-192">Now, if you use the base URL of the channel and go to the URL of the cross-channel page on that site, you will see the channel-specific content instead of the cross-channel content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="33ad8-193">其他资源</span><span class="sxs-lookup"><span data-stu-id="33ad8-193">Additional resources</span></span>

[<span data-ttu-id="33ad8-194">添加内容的方法</span><span class="sxs-lookup"><span data-stu-id="33ad8-194">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="33ad8-195">页面模型词汇表</span><span class="sxs-lookup"><span data-stu-id="33ad8-195">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="33ad8-196">文档状态和生命周期</span><span class="sxs-lookup"><span data-stu-id="33ad8-196">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="33ad8-197">使用发布组</span><span class="sxs-lookup"><span data-stu-id="33ad8-197">Work with publish groups</span></span>](publish-groups.md)
