---
title: 添加隐私政策页面
description: 此主题介绍如何在 Microsoft Dynamics 365 Commerce 中添加隐私政策页面。
author: v-chgri
manager: annbe
ms.date: 01/08/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ee9a68f46c91299065732e5f65479906f9e06079
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001315"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="4661b-103">添加隐私政策页面</span><span class="sxs-lookup"><span data-stu-id="4661b-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4661b-104">此主题介绍如何在 Microsoft Dynamics 365 Commerce 中添加隐私政策页面。</span><span class="sxs-lookup"><span data-stu-id="4661b-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4661b-105">概览</span><span class="sxs-lookup"><span data-stu-id="4661b-105">Overview</span></span>

<span data-ttu-id="4661b-106">隐私合规性包括通知站点用户如何收集和处理他们的数据的组织措施。</span><span class="sxs-lookup"><span data-stu-id="4661b-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="4661b-107">然后，用户可以决定他们要如何处理个人数据，并可以采取适当的行动。</span><span class="sxs-lookup"><span data-stu-id="4661b-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="4661b-108">在 Dynamics 365 Commerce 中查看 Microsoft 隐私声明</span><span class="sxs-lookup"><span data-stu-id="4661b-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="4661b-109">要在登录 Dynamics 365 Commerce 创作工具时查看 Microsoft 隐私声明，请选择右上角的**帮助**按钮 (**?**)，然后选择**隐私和 Cookie**。</span><span class="sxs-lookup"><span data-stu-id="4661b-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="4661b-110">将打开一个新选项卡，其中包含指向 [Microsoft 隐私声明](https://privacy.microsoft.com/privacystatement) 的链接。</span><span class="sxs-lookup"><span data-stu-id="4661b-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="4661b-111">为您的站点建立隐私政策页面</span><span class="sxs-lookup"><span data-stu-id="4661b-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="4661b-112">在 Dynamics 365 Commerce 中，有几种方法可以使您的站点用户访问您的隐私权政策。</span><span class="sxs-lookup"><span data-stu-id="4661b-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="4661b-113">本节说明如何建立隐私政策页面，然后使用页脚片段来引用该页面。</span><span class="sxs-lookup"><span data-stu-id="4661b-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="4661b-114">后面的指南是一个示例，显示如何为 Commerce 站点建立通用隐私政策页面。</span><span class="sxs-lookup"><span data-stu-id="4661b-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="4661b-115">您负责设计和实施最能满足公司法律要求的隐私政策页面解决方案。</span><span class="sxs-lookup"><span data-stu-id="4661b-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="4661b-116">首先，在创作工具中，转到要为其建立隐私政策页面的站点。</span><span class="sxs-lookup"><span data-stu-id="4661b-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="4661b-117">创建模板</span><span class="sxs-lookup"><span data-stu-id="4661b-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="4661b-118">如果已经创建了可用于隐私政策页面的模板，请直接跳至[建立隐私政策页面](#build-a-privacy-policy-page)一节。</span><span class="sxs-lookup"><span data-stu-id="4661b-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="4661b-119">若要创建模板，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4661b-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="4661b-120">转到**模板 \> 新建模板**。</span><span class="sxs-lookup"><span data-stu-id="4661b-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="4661b-121">输入模板名称，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="4661b-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="4661b-122">在模板中，将所有需要的模块添加到所需的页面插槽中。</span><span class="sxs-lookup"><span data-stu-id="4661b-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="4661b-123">要获取指导，将鼠标悬停在红色感叹号上。</span><span class="sxs-lookup"><span data-stu-id="4661b-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="4661b-124">例如，**HTML 标头**插槽可能需要**默认外部脚本**模块。</span><span class="sxs-lookup"><span data-stu-id="4661b-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="4661b-125">在**正文**插槽中，添加一个**默认页面**模块。</span><span class="sxs-lookup"><span data-stu-id="4661b-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="4661b-126">在**默认页**模块的**主**插槽中，添加一个**内容丰富块**模块。</span><span class="sxs-lookup"><span data-stu-id="4661b-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="4661b-127">在**内容丰富块**模块中，添加一个**内容丰富块项**模块。</span><span class="sxs-lookup"><span data-stu-id="4661b-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="4661b-128">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="4661b-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="4661b-129">建立隐私政策页面</span><span class="sxs-lookup"><span data-stu-id="4661b-129">Build a privacy policy page</span></span>

<span data-ttu-id="4661b-130">要建立隐私政策页面，请按照下列步骤操作。</span><span class="sxs-lookup"><span data-stu-id="4661b-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="4661b-131">转到**页面 \> 新建页面**。</span><span class="sxs-lookup"><span data-stu-id="4661b-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="4661b-132">为隐私政策页面选择模板。</span><span class="sxs-lookup"><span data-stu-id="4661b-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="4661b-133">输入页面名称和 URL，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="4661b-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="4661b-134">在页面的**主**插槽中，添加一个**内容丰富块**模块。</span><span class="sxs-lookup"><span data-stu-id="4661b-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="4661b-135">在**内容丰富块**模块中，添加一个**内容丰富块项**模块。</span><span class="sxs-lookup"><span data-stu-id="4661b-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="4661b-136">在**内容丰富块**模块的属性窗格中，选择**添加数据源**，然后选择**富文本内容**。</span><span class="sxs-lookup"><span data-stu-id="4661b-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="4661b-137">在富文本编辑器中，输入隐私政策页面的内容。</span><span class="sxs-lookup"><span data-stu-id="4661b-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="4661b-138">根据需要将富文本编辑器扩展到全屏模式。</span><span class="sxs-lookup"><span data-stu-id="4661b-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="4661b-139">完成内容输入后，选择**预览**在 Web 浏览器中预览页面。</span><span class="sxs-lookup"><span data-stu-id="4661b-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="4661b-140">完成页面和模块属性的所有其余添加。</span><span class="sxs-lookup"><span data-stu-id="4661b-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="4661b-141">签入隐私政策页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="4661b-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="4661b-142">若要发布隐私政策页面的 URL，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4661b-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="4661b-143">转到 **URL**，选择隐私政策页面的 URL。</span><span class="sxs-lookup"><span data-stu-id="4661b-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="4661b-144">发布所选的 URL。</span><span class="sxs-lookup"><span data-stu-id="4661b-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="4661b-145">在页脚中创建指向隐私政策页面的链接</span><span class="sxs-lookup"><span data-stu-id="4661b-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="4661b-146">您可以将隐私政策页面的链接添加到片段中。</span><span class="sxs-lookup"><span data-stu-id="4661b-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="4661b-147">这样，您可以共享链接并通过引用片段跨多个站点页面对其进行更新。</span><span class="sxs-lookup"><span data-stu-id="4661b-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="4661b-148">本示例说明如何将隐私政策页面的链接添加到页脚片段。</span><span class="sxs-lookup"><span data-stu-id="4661b-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="4661b-149">若要向页脚片段添加链接，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="4661b-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="4661b-150">转到**页面片段 \> 新建页面片段**。</span><span class="sxs-lookup"><span data-stu-id="4661b-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="4661b-151">选择**页脚**模块，然后在**页面片段名称**字段中输入名称。</span><span class="sxs-lookup"><span data-stu-id="4661b-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="4661b-152">在**页脚类别**插槽中，添加一个**页脚项**模块。</span><span class="sxs-lookup"><span data-stu-id="4661b-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="4661b-153">在右侧的属性窗格中，选择**链接文本**。</span><span class="sxs-lookup"><span data-stu-id="4661b-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="4661b-154">在**链接文本**对话框中，输入隐私政策页面的链接文本和链接目标，然后单击**确定**。</span><span class="sxs-lookup"><span data-stu-id="4661b-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="4661b-155">要获取隐私政策页面的 URL，请转到**页面**，转到隐私政策页面，然后从属性窗格中复制 URL。</span><span class="sxs-lookup"><span data-stu-id="4661b-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="4661b-156">保存片段，签入，然后发布。</span><span class="sxs-lookup"><span data-stu-id="4661b-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="4661b-157">预览片段，并测试隐私政策页面的链接。</span><span class="sxs-lookup"><span data-stu-id="4661b-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="4661b-158">现在可以在模板中为其他站点页面引用此片段了。</span><span class="sxs-lookup"><span data-stu-id="4661b-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="4661b-159">当此片段在模板的**页脚**模块中引用时，链接引用将出现在使用该模板建立的任何页面上。</span><span class="sxs-lookup"><span data-stu-id="4661b-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4661b-160">其他资源</span><span class="sxs-lookup"><span data-stu-id="4661b-160">Additional resources</span></span>

[<span data-ttu-id="4661b-161">合规概述</span><span class="sxs-lookup"><span data-stu-id="4661b-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="4661b-162">辅助功能和功能</span><span class="sxs-lookup"><span data-stu-id="4661b-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="4661b-163">Cookie 合规</span><span class="sxs-lookup"><span data-stu-id="4661b-163">Cookie compliance</span></span>](cookie-compliance.md)
