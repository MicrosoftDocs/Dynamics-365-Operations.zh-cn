---
title: 添加收藏夹图标
description: 此主题介绍如何向站点添加收藏夹图标。
author: bicyclingfool
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9268bc74a4131256f5a2e88df833104db271b56a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797711"
---
# <a name="add-a-favicon"></a><span data-ttu-id="d09bb-103">添加收藏夹图标</span><span class="sxs-lookup"><span data-stu-id="d09bb-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d09bb-104">此主题介绍如何向站点添加收藏夹图标。</span><span class="sxs-lookup"><span data-stu-id="d09bb-104">This topic explains how to add a favicon to your site.</span></span>

<span data-ttu-id="d09bb-105">收藏夹图标是在 Web 浏览器标签页上、地址栏中、浏览历史记录中和书签或收藏夹中及其他位置内显示的小图形文件。</span><span class="sxs-lookup"><span data-stu-id="d09bb-105">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="d09bb-106">建议向站点添加收藏夹图标，因为这样可以展示和强化您的品牌形象，帮助您的站点从客户访问的其他站点中脱颖而出。</span><span class="sxs-lookup"><span data-stu-id="d09bb-106">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="d09bb-107">虽然可以向站点添加各种大小和文件类型的多个收藏夹图标，此主题介绍如何添加一个收藏夹图标。</span><span class="sxs-lookup"><span data-stu-id="d09bb-107">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="d09bb-108">但是，可使用相同流程和位置添加更多收藏夹图标。</span><span class="sxs-lookup"><span data-stu-id="d09bb-108">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="d09bb-109">将收藏夹图标上传到站点的资产集中</span><span class="sxs-lookup"><span data-stu-id="d09bb-109">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="d09bb-110">若要将收藏夹图标上传到站点的资产集中，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d09bb-110">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="d09bb-111">在左侧导航窗格中，选择 **媒体库**。</span><span class="sxs-lookup"><span data-stu-id="d09bb-111">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="d09bb-112">在命令栏上，选择 **上传 \> 上传媒体项**。</span><span class="sxs-lookup"><span data-stu-id="d09bb-112">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="d09bb-113">在“文件资源管理器”窗口中，浏览到要上传的收藏夹图标图像文件，选择它，然后选择 **打开**。</span><span class="sxs-lookup"><span data-stu-id="d09bb-113">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="d09bb-114">在 **上传媒体项** 对话框中，输入必需的标题和替代文本。</span><span class="sxs-lookup"><span data-stu-id="d09bb-114">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="d09bb-115">如果要在上传后立即发布图像，请选中 **在上传后发布媒体项目** 复选框。</span><span class="sxs-lookup"><span data-stu-id="d09bb-115">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d09bb-116">如果您未选中 **在上传后发布媒体项目** 复选框，则必须返回到 **媒体项目** 页面并稍后手动发布收藏夹图标。</span><span class="sxs-lookup"><span data-stu-id="d09bb-116">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="d09bb-117">选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d09bb-117">Select **OK**.</span></span>
1. <span data-ttu-id="d09bb-118">在右侧的属性窗格中，复制收藏夹图标的公共 URL。</span><span class="sxs-lookup"><span data-stu-id="d09bb-118">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="d09bb-119">您稍后将使用此 URL。</span><span class="sxs-lookup"><span data-stu-id="d09bb-119">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="d09bb-120">为您的收藏夹图标创建 HTML</span><span class="sxs-lookup"><span data-stu-id="d09bb-120">Create the HTML for your favicon</span></span>

<span data-ttu-id="d09bb-121">要为收藏夹图标创建 HTML，请使用以下 HTML 字符串。</span><span class="sxs-lookup"><span data-stu-id="d09bb-121">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="d09bb-122">对于 **href** 属性，请将 **您的\_收藏夹\_图标\_的\_公共 URL** 替换为您先前复制的公共 URL。</span><span class="sxs-lookup"><span data-stu-id="d09bb-122">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="d09bb-123">创建一个包含收藏夹图标元标记的片段</span><span class="sxs-lookup"><span data-stu-id="d09bb-123">Create a fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="d09bb-124">要创建一个包含收藏夹图标元标记的片段，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d09bb-124">To create a fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="d09bb-125">转到 **片段**，然后选择 **新建**.</span><span class="sxs-lookup"><span data-stu-id="d09bb-125">Go to **Fragments**, and select **New**.</span></span>
1. <span data-ttu-id="d09bb-126">在 **新建片段** 对话框中，选择 **元标记** 作为片段所基于的模块。</span><span class="sxs-lookup"><span data-stu-id="d09bb-126">In the **New fragment** dialog box, select **Metatags** as the module that the fragment is based on.</span></span>
1. <span data-ttu-id="d09bb-127">输入片段名称，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d09bb-127">Enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d09bb-128">在片段层次结构树中，选择 **默认元标记** 子项。</span><span class="sxs-lookup"><span data-stu-id="d09bb-128">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="d09bb-129">在右窗格中的 **元标记** 下，选择 **添加**，然后输入您先前为该收藏夹图标创建的 HTML 字符串。</span><span class="sxs-lookup"><span data-stu-id="d09bb-129">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="d09bb-130">选择 **完成编辑**，然后选择 **发布** 以发布片段。</span><span class="sxs-lookup"><span data-stu-id="d09bb-130">Select **Finish editing**, and then select **Publish** to publish the fragment.</span></span>

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="d09bb-131">将元标记片段添加到页面的 HTML 标头部分</span><span class="sxs-lookup"><span data-stu-id="d09bb-131">Add the metatag fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="d09bb-132">要将元标记片段添加到页面的 HTML **标头** 部分，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="d09bb-132">To add the metatag fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="d09bb-133">转到 **模板**，打开要向其中添加收藏夹图标的页面的模板，然后选择 **编辑**。</span><span class="sxs-lookup"><span data-stu-id="d09bb-133">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="d09bb-134">在模板层次结构树中，选择 **HTML 标头** 容器右侧的省略号 (**...**) 按钮，然后选择 **添加片段**。</span><span class="sxs-lookup"><span data-stu-id="d09bb-134">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add fragment**.</span></span>
1. <span data-ttu-id="d09bb-135">在 **选择片段** 对话框中，选择您之前创建的元标记片段，然后选择 **确定**。</span><span class="sxs-lookup"><span data-stu-id="d09bb-135">In the **Select fragment** dialog box, select the metatag fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="d09bb-136">选择 **完成编辑**，然后选择 **发布** 以发布模板。</span><span class="sxs-lookup"><span data-stu-id="d09bb-136">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="d09bb-137">如果您的站点使用多个模板，则必须将元标记片段添加到所有项中。</span><span class="sxs-lookup"><span data-stu-id="d09bb-137">If your site uses more than one template, you must add the metatags fragment to all of them.</span></span>

<span data-ttu-id="d09bb-138">当您预览的页面基于元标记片段所添加到的模板时，您现在应该会在浏览器选项卡上看到收藏夹图标。</span><span class="sxs-lookup"><span data-stu-id="d09bb-138">When you preview pages that are based on the template that you added the metatags fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d09bb-139">其他资源</span><span class="sxs-lookup"><span data-stu-id="d09bb-139">Additional resources</span></span>

[<span data-ttu-id="d09bb-140">添加徽标</span><span class="sxs-lookup"><span data-stu-id="d09bb-140">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="d09bb-141">选择站点主题</span><span class="sxs-lookup"><span data-stu-id="d09bb-141">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="d09bb-142">处理 CSS 覆盖文件</span><span class="sxs-lookup"><span data-stu-id="d09bb-142">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="d09bb-143">添加欢迎消息</span><span class="sxs-lookup"><span data-stu-id="d09bb-143">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="d09bb-144">添加版权声明</span><span class="sxs-lookup"><span data-stu-id="d09bb-144">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="d09bb-145">向站点添加语言</span><span class="sxs-lookup"><span data-stu-id="d09bb-145">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="d09bb-146">将脚本代码添加到站点页面以支持遥测</span><span class="sxs-lookup"><span data-stu-id="d09bb-146">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
