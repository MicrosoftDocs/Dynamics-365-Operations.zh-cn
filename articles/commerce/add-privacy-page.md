---
title: 添加隐私政策页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中添加隐私政策页面。
author: v-chgri
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 07a806ac040df9dee284e2466629221fbc3403a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209267"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="64035-103">添加隐私策略页面</span><span class="sxs-lookup"><span data-stu-id="64035-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="64035-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中添加隐私政策页面。</span><span class="sxs-lookup"><span data-stu-id="64035-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="64035-105">概览</span><span class="sxs-lookup"><span data-stu-id="64035-105">Overview</span></span>

<span data-ttu-id="64035-106">隐私合规性包括通知站点用户如何收集和处理他们的数据的组织措施。</span><span class="sxs-lookup"><span data-stu-id="64035-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="64035-107">然后，用户可以决定他们要如何处理个人数据，并可以采取适当的行动。</span><span class="sxs-lookup"><span data-stu-id="64035-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="64035-108">在 Dynamics 365 Commerce 中查看 Microsoft 隐私声明</span><span class="sxs-lookup"><span data-stu-id="64035-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="64035-109">要在登录 Dynamics 365 Commerce 创作工具时查看 Microsoft 隐私声明，请选择右上角的 **帮助** 按钮 (**?**)，然后选择 **隐私和 Cookie**。</span><span class="sxs-lookup"><span data-stu-id="64035-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="64035-110">将打开一个新选项卡，其中包含指向 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement) 的链接。</span><span class="sxs-lookup"><span data-stu-id="64035-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="64035-111">为您的站点建立隐私政策页面</span><span class="sxs-lookup"><span data-stu-id="64035-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="64035-112">在 Dynamics 365 Commerce 中，有几种方法可以使您的站点用户访问您的隐私权政策。</span><span class="sxs-lookup"><span data-stu-id="64035-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="64035-113">本节说明如何建立隐私政策页面，然后使用页脚片段来引用该页面。</span><span class="sxs-lookup"><span data-stu-id="64035-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="64035-114">后面的指南是一个示例，显示如何为 Commerce 站点建立通用隐私政策页面。</span><span class="sxs-lookup"><span data-stu-id="64035-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="64035-115">您负责设计和实施最能满足公司法律要求的隐私政策页面解决方案。</span><span class="sxs-lookup"><span data-stu-id="64035-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="64035-116">首先，在创作工具中，转到要为其建立隐私政策页面的站点。</span><span class="sxs-lookup"><span data-stu-id="64035-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="64035-117">创建模板</span><span class="sxs-lookup"><span data-stu-id="64035-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="64035-118">如果已经创建了可用于隐私政策页面的模板，请直接跳至[建立隐私政策页面](#build-a-privacy-policy-page)一节。</span><span class="sxs-lookup"><span data-stu-id="64035-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="64035-119">若要创建模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="64035-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="64035-120">转到 **模板**，然后选择 **新建** 创建页面模板。</span><span class="sxs-lookup"><span data-stu-id="64035-120">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="64035-121">在 **新建模板** 对话框的 **模板名称** 下，输入 **促销横幅模板**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="64035-121">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="64035-122">在模板中，将所有需要的模块添加到所需的页面插槽中。</span><span class="sxs-lookup"><span data-stu-id="64035-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="64035-123">要获取指导，将鼠标悬停在红色感叹号上。</span><span class="sxs-lookup"><span data-stu-id="64035-123">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="64035-124">（例如，**HTML 标头** 插槽可能需要 **默认外部脚本** 模块。）</span><span class="sxs-lookup"><span data-stu-id="64035-124">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="64035-125">在 **正文** 插槽中，添加一个 **默认页面** 模块。</span><span class="sxs-lookup"><span data-stu-id="64035-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="64035-126">在 **默认页** 模块的 **主** 插槽中，添加一个 **内容丰富块** 模块。</span><span class="sxs-lookup"><span data-stu-id="64035-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="64035-127">在 **内容丰富块** 模块中，添加一个 **内容丰富块项** 模块。</span><span class="sxs-lookup"><span data-stu-id="64035-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="64035-128">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="64035-128">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="64035-129">建立隐私政策页面</span><span class="sxs-lookup"><span data-stu-id="64035-129">Build a privacy policy page</span></span>

<span data-ttu-id="64035-130">要建立隐私政策页面，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="64035-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="64035-131">转到 **页面**，然后选择 **新建** 创建页面。</span><span class="sxs-lookup"><span data-stu-id="64035-131">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="64035-132">在 **选择模板** 对话框中，为隐私策略页面选择模板。</span><span class="sxs-lookup"><span data-stu-id="64035-132">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="64035-133">输入页面名称和页面 URL，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="64035-133">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="64035-134">在页面的 **主** 插槽中，添加一个 **内容丰富块** 模块。</span><span class="sxs-lookup"><span data-stu-id="64035-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="64035-135">在 **内容丰富块** 模块中，添加一个 **内容丰富块项** 模块。</span><span class="sxs-lookup"><span data-stu-id="64035-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="64035-136">在 **内容丰富块** 模块的属性窗格中，选择 **添加数据源**，然后选择 **富文本内容**。</span><span class="sxs-lookup"><span data-stu-id="64035-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="64035-137">在富文本编辑器中，输入隐私政策页面的内容。</span><span class="sxs-lookup"><span data-stu-id="64035-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="64035-138">根据需要将富文本编辑器扩展到全屏模式。</span><span class="sxs-lookup"><span data-stu-id="64035-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="64035-139">完成内容输入后，选择 **预览** 在 Web 浏览器中预览页面。</span><span class="sxs-lookup"><span data-stu-id="64035-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="64035-140">完成页面和模块属性的所有其余添加。</span><span class="sxs-lookup"><span data-stu-id="64035-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="64035-141">选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="64035-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="64035-142">若要发布隐私政策页面的 URL，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="64035-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="64035-143">转到 **URL**，选择隐私政策页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="64035-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="64035-144">选择 **发布** 发布所选的 URL。</span><span class="sxs-lookup"><span data-stu-id="64035-144">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="64035-145">在页脚中创建指向隐私政策页面的链接</span><span class="sxs-lookup"><span data-stu-id="64035-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="64035-146">您可以将隐私政策页面的链接添加到片段中。</span><span class="sxs-lookup"><span data-stu-id="64035-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="64035-147">这样，您可以共享链接并通过引用片段跨多个站点页面对其进行更新。</span><span class="sxs-lookup"><span data-stu-id="64035-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="64035-148">本示例说明如何将隐私政策页面的链接添加到页脚片段。</span><span class="sxs-lookup"><span data-stu-id="64035-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="64035-149">若要向页脚片段添加链接，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="64035-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="64035-150">转到 **片段**，然后选择 **新建** 创建页面片段。</span><span class="sxs-lookup"><span data-stu-id="64035-150">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="64035-151">在 **新建片段** 对话框中，选择 **页脚** 模块。</span><span class="sxs-lookup"><span data-stu-id="64035-151">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="64035-152">在 **片段名称** 下，输入片段的名称，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="64035-152">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="64035-153">在 **页脚类别** 插槽中，添加一个 **页脚项** 模块。</span><span class="sxs-lookup"><span data-stu-id="64035-153">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="64035-154">在右侧的属性窗格中，选择 **链接文本**。</span><span class="sxs-lookup"><span data-stu-id="64035-154">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="64035-155">在 **链接文本** 对话框中，输入隐私政策页面的链接文本和链接目标，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="64035-155">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="64035-156">要获取隐私政策页面的 URL，请转到 **页面**，转到隐私政策页面，然后从属性窗格中复制 URL。</span><span class="sxs-lookup"><span data-stu-id="64035-156">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="64035-157">选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="64035-157">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="64035-158">预览片段，并测试隐私政策页面的链接。</span><span class="sxs-lookup"><span data-stu-id="64035-158">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="64035-159">现在可以在模板中为其他站点页面引用此片段了。</span><span class="sxs-lookup"><span data-stu-id="64035-159">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="64035-160">当此片段在模板的 **页脚** 模块中引用时，链接引用将出现在使用该模板建立的任何页面上。</span><span class="sxs-lookup"><span data-stu-id="64035-160">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="64035-161">其他资源</span><span class="sxs-lookup"><span data-stu-id="64035-161">Additional resources</span></span>

[<span data-ttu-id="64035-162">合规概述</span><span class="sxs-lookup"><span data-stu-id="64035-162">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="64035-163">辅助功能和功能</span><span class="sxs-lookup"><span data-stu-id="64035-163">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="64035-164">Cookie 合规性</span><span class="sxs-lookup"><span data-stu-id="64035-164">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="64035-165">替换与所跟踪内容更改相关联的用户 ID</span><span class="sxs-lookup"><span data-stu-id="64035-165">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]