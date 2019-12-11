---
title: 主图模块
description: 此主题介绍主图模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785374"
---
# <a name="hero-module"></a><span data-ttu-id="b724c-103">主图模块</span><span class="sxs-lookup"><span data-stu-id="b724c-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b724c-104">此主题介绍主图模块和如何将其添加到 Microsoft Dynamics 365 Commerce 中的站点页。</span><span class="sxs-lookup"><span data-stu-id="b724c-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b724c-105">概览</span><span class="sxs-lookup"><span data-stu-id="b724c-105">Overview</span></span>

<span data-ttu-id="b724c-106">主图模块用于通过图像和文本的组合营销产品或促销。</span><span class="sxs-lookup"><span data-stu-id="b724c-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="b724c-107">例如，零售商可向电子商务站点的主页添加一个主图模块来促销新产品和吸引客户的注意。</span><span class="sxs-lookup"><span data-stu-id="b724c-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="b724c-108">主图模块由内容管理系统 (CMS) 的数据驱动。</span><span class="sxs-lookup"><span data-stu-id="b724c-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="b724c-109">它是不依赖于页面上的其他任何模块的独立模块。</span><span class="sxs-lookup"><span data-stu-id="b724c-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="b724c-110">可将主图模块放到零售商要进行营销或推广（如产品、销售或特色）的任何站点页中。</span><span class="sxs-lookup"><span data-stu-id="b724c-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="b724c-111">电子商务中的主图模块示例</span><span class="sxs-lookup"><span data-stu-id="b724c-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="b724c-112">可在电子商务站点的主页中使用主图模块来重点展示促销和新产品。</span><span class="sxs-lookup"><span data-stu-id="b724c-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="b724c-113">可在产品详细信息页上使用主图模块来展示产品信息。</span><span class="sxs-lookup"><span data-stu-id="b724c-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="b724c-114">可在一个传送模块中放置多个主图模块来重点展示多个产品或促销。</span><span class="sxs-lookup"><span data-stu-id="b724c-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="b724c-115">主图模块属性</span><span class="sxs-lookup"><span data-stu-id="b724c-115">Hero module properties</span></span>

| <span data-ttu-id="b724c-116">属性名称</span><span class="sxs-lookup"><span data-stu-id="b724c-116">Property name</span></span>  | <span data-ttu-id="b724c-117">值</span><span class="sxs-lookup"><span data-stu-id="b724c-117">Values</span></span> | <span data-ttu-id="b724c-118">说明</span><span class="sxs-lookup"><span data-stu-id="b724c-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b724c-119">头像</span><span class="sxs-lookup"><span data-stu-id="b724c-119">Image</span></span>          | <span data-ttu-id="b724c-120">图像文件</span><span class="sxs-lookup"><span data-stu-id="b724c-120">Image file</span></span> | <span data-ttu-id="b724c-121">可使用图像来展示产品或促销。</span><span class="sxs-lookup"><span data-stu-id="b724c-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="b724c-122">可将图像上传到图像库，也可以使用现有图像。</span><span class="sxs-lookup"><span data-stu-id="b724c-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="b724c-123">标题</span><span class="sxs-lookup"><span data-stu-id="b724c-123">Heading</span></span>        | <span data-ttu-id="b724c-124">标题文本和标题标记（**H1**、**H2**、**H3**、**H4**、**H5** 或 **H6**）</span><span class="sxs-lookup"><span data-stu-id="b724c-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b724c-125">每个主图模块都有标题。</span><span class="sxs-lookup"><span data-stu-id="b724c-125">Every hero module can have a heading.</span></span> <span data-ttu-id="b724c-126">默认情况下，将 **H2** 标题标记用于标题。</span><span class="sxs-lookup"><span data-stu-id="b724c-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="b724c-127">但是，可更改此标记以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="b724c-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="b724c-128">段落</span><span class="sxs-lookup"><span data-stu-id="b724c-128">Paragraph</span></span>      | <span data-ttu-id="b724c-129">段落文本</span><span class="sxs-lookup"><span data-stu-id="b724c-129">Paragraph text</span></span> | <span data-ttu-id="b724c-130">主图模块支持富文本格式的段落文本。</span><span class="sxs-lookup"><span data-stu-id="b724c-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="b724c-131">支持某些基本的富文本功能，如加粗，加下划线、斜体文本和超链接。</span><span class="sxs-lookup"><span data-stu-id="b724c-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="b724c-132">为模块应用的页面主题可替代这些功能中的一部分。</span><span class="sxs-lookup"><span data-stu-id="b724c-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="b724c-133">链接</span><span class="sxs-lookup"><span data-stu-id="b724c-133">Link</span></span>           | <span data-ttu-id="b724c-134">链接文本、链接 URL、可访问丰富 Internet 应用程序 (ARIA) 标签和**在新标签页中打开链接**</span><span class="sxs-lookup"><span data-stu-id="b724c-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="b724c-135">主图模块支持一个或多个“调用操作”链接。</span><span class="sxs-lookup"><span data-stu-id="b724c-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="b724c-136">如果添加链接，则需要链接文本、URL 和 ARIA 标签。</span><span class="sxs-lookup"><span data-stu-id="b724c-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="b724c-137">ARIA 标签应该具有描述性，以满足辅助功能要求。</span><span class="sxs-lookup"><span data-stu-id="b724c-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="b724c-138">可将链接配置为在新标签页中打开。</span><span class="sxs-lookup"><span data-stu-id="b724c-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="b724c-139">文本放置</span><span class="sxs-lookup"><span data-stu-id="b724c-139">Text placement</span></span> | <span data-ttu-id="b724c-140">**左上**、**右上**、**顶部居中**、**左下**、**右下**、**底部居中**、**左中**、**右中**或**居中**</span><span class="sxs-lookup"><span data-stu-id="b724c-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="b724c-141">此属性定义图像相对文本的位置。</span><span class="sxs-lookup"><span data-stu-id="b724c-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="b724c-142">例如，如果选择**靠右**，则图像在文本右侧显示。</span><span class="sxs-lookup"><span data-stu-id="b724c-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="b724c-143">文本主题</span><span class="sxs-lookup"><span data-stu-id="b724c-143">Text theme</span></span>     | <span data-ttu-id="b724c-144">**浅**或**深**</span><span class="sxs-lookup"><span data-stu-id="b724c-144">**Light** or **Dark**</span></span> | <span data-ttu-id="b724c-145">可以基于背景图像为文本定义颜色主题。</span><span class="sxs-lookup"><span data-stu-id="b724c-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="b724c-146">例如，如果图像采用了深色背景，则可应用浅色主题来凸显文本和加强颜色对比度，以达到辅助功能目的。</span><span class="sxs-lookup"><span data-stu-id="b724c-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="b724c-147">渐变</span><span class="sxs-lookup"><span data-stu-id="b724c-147">Gradient</span></span>       | <span data-ttu-id="b724c-148">**True** 或 **False**</span><span class="sxs-lookup"><span data-stu-id="b724c-148">**True** or **False**</span></span> | <span data-ttu-id="b724c-149">可为图像应用渐变效果来加强颜色对比度以达到辅助功能目的。</span><span class="sxs-lookup"><span data-stu-id="b724c-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="b724c-150">向新页面添加主图模块</span><span class="sxs-lookup"><span data-stu-id="b724c-150">Add a hero module to a new page</span></span>

<span data-ttu-id="b724c-151">若要向新页面添加主图模块和设置必需的属性，请执行以下步骤。</span><span class="sxs-lookup"><span data-stu-id="b724c-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b724c-152">转到**模板**，然后创建一个名称为**主图模板**的页面模板。</span><span class="sxs-lookup"><span data-stu-id="b724c-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="b724c-153">在默认页的**主**插槽中，添加一个主图模块。</span><span class="sxs-lookup"><span data-stu-id="b724c-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="b724c-154">签入模板，然后发布。</span><span class="sxs-lookup"><span data-stu-id="b724c-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="b724c-155">使用您刚才创建的主图模板创建一个名称为**主图页**的页面。</span><span class="sxs-lookup"><span data-stu-id="b724c-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="b724c-156">在默认页的**主**插槽，选择省略号按钮 (**...**)，然后选择**添加模块**。</span><span class="sxs-lookup"><span data-stu-id="b724c-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b724c-157">在**添加模块**对话框中**选择模块**下，选择主图模块，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b724c-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="b724c-158">在左侧的大纲树中，选择该主图模块。</span><span class="sxs-lookup"><span data-stu-id="b724c-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="b724c-159">在右侧的属性窗格中，选择**添加图像**。</span><span class="sxs-lookup"><span data-stu-id="b724c-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="b724c-160">然后选择现有图像或上传新图像。</span><span class="sxs-lookup"><span data-stu-id="b724c-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="b724c-161">选择**标题**。</span><span class="sxs-lookup"><span data-stu-id="b724c-161">Select **Heading**.</span></span>
1. <span data-ttu-id="b724c-162">在**标题**对话框中，添加标题文本，选择标题级别，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b724c-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="b724c-163">在**富文本**下，根据需要添加文本。</span><span class="sxs-lookup"><span data-stu-id="b724c-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="b724c-164">选择**添加操作链接**。</span><span class="sxs-lookup"><span data-stu-id="b724c-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="b724c-165">在**操作链接**对话框中，添加链接的链接文本、链接 URL 和 ARIA 标签，然后选择**确定**。</span><span class="sxs-lookup"><span data-stu-id="b724c-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="b724c-166">保存页面，然后预览更改。</span><span class="sxs-lookup"><span data-stu-id="b724c-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="b724c-167">签入页面，然后发布。</span><span class="sxs-lookup"><span data-stu-id="b724c-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b724c-168">其他资源</span><span class="sxs-lookup"><span data-stu-id="b724c-168">Additional resources</span></span>

[<span data-ttu-id="b724c-169">入门套件概览</span><span class="sxs-lookup"><span data-stu-id="b724c-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b724c-170">预警模块</span><span class="sxs-lookup"><span data-stu-id="b724c-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="b724c-171">传送模块</span><span class="sxs-lookup"><span data-stu-id="b724c-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="b724c-172">内容丰富块模块</span><span class="sxs-lookup"><span data-stu-id="b724c-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="b724c-173">内容放置模块</span><span class="sxs-lookup"><span data-stu-id="b724c-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="b724c-174">特色模块</span><span class="sxs-lookup"><span data-stu-id="b724c-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="b724c-175">视频播放器模块</span><span class="sxs-lookup"><span data-stu-id="b724c-175">Video player module</span></span>](add-video-player.md)
