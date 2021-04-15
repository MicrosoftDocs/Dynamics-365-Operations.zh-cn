---
title: 添加隐私政策页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中添加隐私政策页面。
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797519"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="b2abc-103">添加隐私策略页面</span><span class="sxs-lookup"><span data-stu-id="b2abc-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2abc-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中添加隐私政策页面。</span><span class="sxs-lookup"><span data-stu-id="b2abc-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b2abc-105">隐私合规性包括通知站点用户如何收集和处理他们的数据的组织措施。</span><span class="sxs-lookup"><span data-stu-id="b2abc-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="b2abc-106">然后，用户可以决定他们要如何处理个人数据，并可以采取适当的行动。</span><span class="sxs-lookup"><span data-stu-id="b2abc-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="b2abc-107">在 Dynamics 365 Commerce 中查看 Microsoft 隐私声明</span><span class="sxs-lookup"><span data-stu-id="b2abc-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="b2abc-108">要在登录 Dynamics 365 Commerce 创作工具时查看 Microsoft 隐私声明，请选择右上角的 **帮助** 按钮 (**?**)，然后选择 **隐私和 Cookie**。</span><span class="sxs-lookup"><span data-stu-id="b2abc-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="b2abc-109">将打开一个新选项卡，其中包含指向 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement) 的链接。</span><span class="sxs-lookup"><span data-stu-id="b2abc-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="b2abc-110">为您的站点建立隐私政策页面</span><span class="sxs-lookup"><span data-stu-id="b2abc-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="b2abc-111">在 Dynamics 365 Commerce 中，有几种方法可以使您的站点用户访问您的隐私权政策。</span><span class="sxs-lookup"><span data-stu-id="b2abc-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="b2abc-112">本节说明如何建立隐私政策页面，然后使用页脚片段来引用该页面。</span><span class="sxs-lookup"><span data-stu-id="b2abc-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="b2abc-113">后面的指南是一个示例，显示如何为 Commerce 站点建立通用隐私政策页面。</span><span class="sxs-lookup"><span data-stu-id="b2abc-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="b2abc-114">您负责设计和实施最能满足公司法律要求的隐私政策页面解决方案。</span><span class="sxs-lookup"><span data-stu-id="b2abc-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="b2abc-115">首先，在创作工具中，转到要为其建立隐私政策页面的站点。</span><span class="sxs-lookup"><span data-stu-id="b2abc-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="b2abc-116">创建模板</span><span class="sxs-lookup"><span data-stu-id="b2abc-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="b2abc-117">如果已经创建了可用于隐私政策页面的模板，请直接跳至[建立隐私政策页面](#build-a-privacy-policy-page)一节。</span><span class="sxs-lookup"><span data-stu-id="b2abc-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="b2abc-118">若要创建模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b2abc-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="b2abc-119">转到 **模板**，然后选择 **新建** 创建页面模板。</span><span class="sxs-lookup"><span data-stu-id="b2abc-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="b2abc-120">在 **新建模板** 对话框的 **模板名称** 下，输入 **促销横幅模板**，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b2abc-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="b2abc-121">在模板中，将所有需要的模块添加到所需的页面插槽中。</span><span class="sxs-lookup"><span data-stu-id="b2abc-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="b2abc-122">要获取指导，将鼠标悬停在红色感叹号上。</span><span class="sxs-lookup"><span data-stu-id="b2abc-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="b2abc-123">（例如，**HTML 标头** 插槽可能需要 **默认外部脚本** 模块。）</span><span class="sxs-lookup"><span data-stu-id="b2abc-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="b2abc-124">在 **正文** 插槽中，添加一个 **默认页面** 模块。</span><span class="sxs-lookup"><span data-stu-id="b2abc-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="b2abc-125">在 **默认页** 模块的 **主** 插槽中，添加一个 **内容丰富块** 模块。</span><span class="sxs-lookup"><span data-stu-id="b2abc-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="b2abc-126">在 **内容丰富块** 模块中，添加一个 **内容丰富块项** 模块。</span><span class="sxs-lookup"><span data-stu-id="b2abc-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="b2abc-127">选择 **保存**，选择 **完成编辑** 签入模板，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="b2abc-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="b2abc-128">建立隐私政策页面</span><span class="sxs-lookup"><span data-stu-id="b2abc-128">Build a privacy policy page</span></span>

<span data-ttu-id="b2abc-129">要建立隐私政策页面，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="b2abc-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="b2abc-130">转到 **页面**，然后选择 **新建** 创建页面。</span><span class="sxs-lookup"><span data-stu-id="b2abc-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="b2abc-131">在 **选择模板** 对话框中，为隐私策略页面选择模板。</span><span class="sxs-lookup"><span data-stu-id="b2abc-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="b2abc-132">输入页面名称和页面 URL，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b2abc-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="b2abc-133">在页面的 **主** 插槽中，添加一个 **内容丰富块** 模块。</span><span class="sxs-lookup"><span data-stu-id="b2abc-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="b2abc-134">在 **内容丰富块** 模块中，添加一个 **内容丰富块项** 模块。</span><span class="sxs-lookup"><span data-stu-id="b2abc-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="b2abc-135">在 **内容丰富块** 模块的属性窗格中，选择 **添加数据源**，然后选择 **富文本内容**。</span><span class="sxs-lookup"><span data-stu-id="b2abc-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="b2abc-136">在富文本编辑器中，输入隐私政策页面的内容。</span><span class="sxs-lookup"><span data-stu-id="b2abc-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="b2abc-137">根据需要将富文本编辑器扩展到全屏模式。</span><span class="sxs-lookup"><span data-stu-id="b2abc-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="b2abc-138">完成内容输入后，选择 **预览** 在 Web 浏览器中预览页面。</span><span class="sxs-lookup"><span data-stu-id="b2abc-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="b2abc-139">完成页面和模块属性的所有其余添加。</span><span class="sxs-lookup"><span data-stu-id="b2abc-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="b2abc-140">选择 **保存**，选择 **完成编辑** 签入页面，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="b2abc-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b2abc-141">若要发布隐私政策页面的 URL，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b2abc-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="b2abc-142">转到 **URL**，选择隐私政策页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="b2abc-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="b2abc-143">选择 **发布** 发布所选的 URL。</span><span class="sxs-lookup"><span data-stu-id="b2abc-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="b2abc-144">在页脚中创建指向隐私政策页面的链接</span><span class="sxs-lookup"><span data-stu-id="b2abc-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="b2abc-145">您可以将隐私政策页面的链接添加到片段中。</span><span class="sxs-lookup"><span data-stu-id="b2abc-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="b2abc-146">这样，您可以共享链接并通过引用片段跨多个站点页面对其进行更新。</span><span class="sxs-lookup"><span data-stu-id="b2abc-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="b2abc-147">本示例说明如何将隐私政策页面的链接添加到页脚片段。</span><span class="sxs-lookup"><span data-stu-id="b2abc-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="b2abc-148">若要向页脚片段添加链接，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b2abc-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="b2abc-149">转到 **片段**，然后选择 **新建** 创建页面片段。</span><span class="sxs-lookup"><span data-stu-id="b2abc-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="b2abc-150">在 **新建片段** 对话框中，选择 **页脚** 模块。</span><span class="sxs-lookup"><span data-stu-id="b2abc-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="b2abc-151">在 **片段名称** 下，输入片段的名称，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b2abc-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b2abc-152">在 **页脚类别** 插槽中，添加一个 **页脚项** 模块。</span><span class="sxs-lookup"><span data-stu-id="b2abc-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="b2abc-153">在右侧的属性窗格中，选择 **链接文本**。</span><span class="sxs-lookup"><span data-stu-id="b2abc-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="b2abc-154">在 **链接文本** 对话框中，输入隐私政策页面的链接文本和链接目标，然后单击 **确定**。</span><span class="sxs-lookup"><span data-stu-id="b2abc-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="b2abc-155">要获取隐私政策页面的 URL，请转到 **页面**，转到隐私政策页面，然后从属性窗格中复制 URL。</span><span class="sxs-lookup"><span data-stu-id="b2abc-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="b2abc-156">选择 **保存**，选择 **完成编辑** 签入片段，然后选择 **发布** 进行发布。</span><span class="sxs-lookup"><span data-stu-id="b2abc-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b2abc-157">预览片段，并测试隐私政策页面的链接。</span><span class="sxs-lookup"><span data-stu-id="b2abc-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="b2abc-158">现在可以在模板中为其他站点页面引用此片段了。</span><span class="sxs-lookup"><span data-stu-id="b2abc-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="b2abc-159">当此片段在模板的 **页脚** 模块中引用时，链接引用将出现在使用该模板建立的任何页面上。</span><span class="sxs-lookup"><span data-stu-id="b2abc-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2abc-160">其他资源</span><span class="sxs-lookup"><span data-stu-id="b2abc-160">Additional resources</span></span>

[<span data-ttu-id="b2abc-161">合规概述</span><span class="sxs-lookup"><span data-stu-id="b2abc-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="b2abc-162">辅助功能和功能</span><span class="sxs-lookup"><span data-stu-id="b2abc-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="b2abc-163">Cookie 合规性</span><span class="sxs-lookup"><span data-stu-id="b2abc-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="b2abc-164">替换与所跟踪内容更改相关联的用户 ID</span><span class="sxs-lookup"><span data-stu-id="b2abc-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
